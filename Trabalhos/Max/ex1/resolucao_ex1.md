# Exercício 1

## Materiais e métodos

Para realizar o desenvolvimento deste exercício optei por utilizar um microcontrolador embarcado em uma placa Arduíno UNO R3, já que existem bibliotecas nativas para geração de código no MATLAB Simulink. As ferramentas foram instaladas em aula através das ferramentas de auto-instalação de pacotes do MATLAB.

A simulação foi feita em duas partes, a primeira via componentes de simulação do MATLAB Simulink e a segunda embarcando o código gerado pelo MATLAB no Arduino UNO R3. Para realizar a simulação eletrônica, utilizei os seguintes componentes:
* Um LED vermelho para indicar quando o nível de combustível entrasse em estado de alerta;
* Um potênciometro para simular o sensor de nível de combustível;
* Um protoboard para montagem dos circuitos;
* Jumpers para conexões.

Para gerar o relatório utilizei o software Frietzing para o esquemático e a imagem da montagem do protoboard.

## Resolução

Para atingir o controle da luz do nível de combustível implementei uma solução no MATLAB Simulink, utilizando a ferramenta de máquina de estados para implementar o controle de estados do sistema e a histerese da leitura do sensor. A máquina de estados recebe como entrada o valor de tensão lido do sensor (estipulado de 0 à 10V na simulação no MATLAB e 0 à 5Vcc na simulação eletrônica) e o tempo (em segundos) lido de um relógio, que determina o momento de início do funcionamento do sistema, como também determinado pelo enunciado do exercício, 2s de espera. A saída da máquina de estados foi definida como valor do estado lâmpada, ON = 1 e OFF = 0.
A figura abaixo mostra o sistema montado no MATLAB Simulink.


Para simular o sensor de nível de combustível o potênciometro foi ligado à tensão de 5Vcc gerado pelo Arduino, sua saída variável foi ligada ao pino A0 para realizar a leitura dos valores analógicos. Para esta leitura, o bloco de Analog In foi utilizado no simulink. A saída da função foi ligada ao pino D1 do Arduino, e este pino ligado ao LED. Para modificar o sinal de saída deste pino, o bloco Digital Out do conjunto de funções do Arduino foi utilizado. Para conseguir atingir os mesmos valores do exercício na simulação eletrônica, um multiplicador foi colocado logo após a entrada do sensor, normalizando os valores para limites de 0Vcc à 10Vcc.

# Conclusão

Foi observado que ao girar o potênciometro e alterar o valor de entrada de tensão no pino de leitura do analógica do Arduino, a partir de 2 segundos do sistema ligado, é possível verificar o funcionamento do sensor de nível de combustível. Entre valores de 0Vcc à 8.5Vcc o LED permanece apagado. Se a chave for virada ácima deste nível, o LED se acenderá indicando que o nível de combustível está abaixo do limite. Para que o LED fosse desligado, a chave teve de ser girada até atingir valor de 8Vcc na entrada do sistema. Entre 8Vcc e 8,5Vcc o sistema trabalha em histerese, ou seja, se o LED estiver ligado, permanecerá ligado até atingit 8Vcc, se estiver desligado, ligará após atingir 8.5Vcc.
