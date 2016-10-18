# Exercício 2

## Requisitos

1. Função 1: ABS Warning Lamp

  1. Deverá ligar o sinal de aviso de ABS se o sistema estiver em modo $AE:DeviceControl e a seleção de lâmpada estiver habilitada;
  2. Deverá desligar o sinal de aviso de ABS se o sistema estiver em modo $AE:DeviceControl e a seleção de lâmpada estiver desabilitada;
  3. Deverá enviar a mensagem CAN ID $17D = $1 (Antilock Brake System Indication On) se o sistema estiver em modo $AE:DeviceControl e a seleção de lâmpada estiver habilitada;
  4. Deverá enviar a mensagem CAN ID $17D = $0 (Antilock Brake System Indication On) se o sistema estiver em modo $AE:DeviceControl e a seleção de lâmpada estiver desabilitada;
  5. Deverá ligar o sinal de aviso de ABS se diagnosticado mal funcionamento (detectado ou em execução) que proiba a existência de controle do ABS em outro lugar que não seja no controle do ABS;
  6. Deverá enviar a mensagem CAN ID $17D = $1 (Antilock Brake System Indication On) se diagnosticado mal funcionamento (detectado ou em execução) que proiba a existência de controle do ABS em outro lugar que não seja no controle do ABS;
  7. Deverá ligar o sinal de aviso de ABS se o relé de proteção estiver desligado (aberto);
  8. Deverá enviar a mensagem CAN ID $17D = $1 (Antilock Brake System Indication On) se o relé do ABS estiver desligado (aberto);
  9. Deverá enviar a mensagem CAN ID $1E19 = $1 (Antilock Brake System Active) quando o sistema de ABS estiver ativo;
  10. Deverá desligar o sinal de aviso de ABS em situações normais de funcionamento;
  11. Deverá enviar a mensagem CAN ID $17D = $0 (Antilock Brake System Indication On) em situações normais de funcionamento;
  12. Deverá enviar a mensagem CAN ID $1E19 = $0 (Antilock Brake System Active) em situações normais de funcionamento.

2. Função 2: Brake Warning Lamp

  1. Deverá ligar a lâmpada de aviso do freio se o sistema estiver em modo $AE:DeviceControl e a seleção de lâmpada estiver habilitada;
  2. Deverá desligar a lâmpada de aviso do freio se o sistema estiver em modo $AE:DeviceControl e a seleção de lâmpada estiver desabilitada;
  3. Deverá enviar o sinais D (Brake System Red Brake Telltale Request) e I (Electronic Brake Distribution Failed) com a mensagem CAN ID $17D = $1 se o sistema estiver em modo $AE:DeviceControl e a seleção de lâmpada estiver habilitada;
  4. Deverá enviar o sinais D (Brake System Red Brake Telltale Request) e I (Electronic Brake Distribution Failed) com a mensagem CAN ID $17D = $0 se o sistema estiver em modo $AE:DeviceControl e a seleção de lâmpada estiver desabilitada;
  5. Deverá ligar a lâmpada de aviso do freio se diagnosticado mal functionamento (detectado ou em execução) que proíba a existência de controle do EBD;
  6. Deverá enviar o sinais D (Brake System Red Brake Telltale Request) e I (Electronic Brake Distribution Failed) com a mensagem CAN ID $17D = $1 se diagnosticado mal functionamento (detectado ou em execução) que proíba a existência de controle do EBD;
  7. Deverá ligar a lâmpada de aviso do freio se o relé de proteção estiver desligado (aberto);
  8. Deverá enviar o sinais D (Brake System Red Brake Telltale Request) e I (Electronic Brake Distribution Failed) com a mensagem CAN ID $17D = $1 se o relé de proteção estiver desligado (aberto);
  9. Deverá ligar a lâmpada de aviso do freio se o nível do fluído de freio estiver baixo, apenas para ADS-V2;
  10. Deverá enviar os sinais D (Brake System Red Brake Telltale Request) e I (Electronic Brake Distribution Failed) com a mensagem CAN ID $17D = $1, e o sinal C (Brake Fluid Level Low) com a mensagem CAN ID = $1 se o nível do fluído de freio estiver baixo, apenas para ADS-V2;
  11. Deverá desligar a lâmpada de aviso do freio em situações normais de funcionamento;
  12. Deverá enviar os sinais D (Brake System Red Brake Telltale Request) e I (Electronic Brake Distribution Failed) com a mensagem CAN ID $17D = $0, e o sinal C (Brake Fluid Level Low) com a mensagem CAN ID = $0 em situações normais de funcionamento.

3. Função 3: ESC Indicator Lamp and ESC Off Lamp

1. Deverá ligar a lâmpada de aviso de ESC IL se o sistema estiver em modo $AE:DeviceControl e a seleção de lâmpada estiver habilitada;
  1. Deverá desligar a lâmpada de aviso de ESC IL se o sistema estiver em modo $AE:DeviceControl e a seleção de lâmpada estiver desabilitada;
  1. Deverá enviar os sinais F (Vehicle Stability Enhancement Statuus) e G (Traction Control System Operating Status) com a mensagem CAN ID $17D = $2 se o sistema estiver em modo $AE:DeviceControl e a seleção de lâmpada estiver habilitada;
  1. Deverá enviar os sinais F (Vehicle Stability Enhancement Statuus) e G (Traction Control System Operating Status) com a mensagem CAN ID $17D = $0 se o sistema estiver em modo $AE:DeviceControl e a seleção de lâmpada estiver desabilitada;
  1. Deverá ligar a lâmpada de aviso de ESC IL se diagnosticado mal funcionamento (detectado ou em execução) que proíba a existência de controle do ESC;
  1. Deverá ligar a lâmpada de aviso de ESC IL se diagnosticado mal funcionamento (detectado ou em execução) que proíba a existência de controle do TCS;
  1. Deverá ligar a lâmpada de aviso de ESC IL se o relé de proteção estiver desligado (aberto);
  1. Deverá enviar os sinais F (Vehicle Stability Enhancement Statuus) e G (Traction Control System Operating Status) com a mensagem CAN ID $17D = $2 se diagnosticado mal funcionamento (detectado ou em execução) que proíba a existência de controle do ESC;
  1. Deverá enviar os sinais F (Vehicle Stability Enhancement Statuus) e G (Traction Control System Operating Status) com a mensagem CAN ID $17D = $2 se diagnosticado mal funcionamento (detectado ou em execução) que proíba a existência de controle do TCS;
  1. Deverá enviar os sinais F (Vehicle Stability Enhancement Statuus) e G (Traction Control System Operating Status) com a mensagem CAN ID $17D = $2 se o relé de proteção estiver desligado (aberto);
  1. Deverá piscar a lâmpada de ESC IL se o controle de TSC estiver em execução;
  1. Deverá piscar a lâmpada de ESC IL se o controle de ESC estiver em execução;
  1. Deverá enviar o sinal G (Traction Control System Operating Status) com a mensage $17D = $1 se o controle de TSC estiver em execução;
  1. Deverá enviar o sinal F (Vehicle Stability Enhancement Status) com a mensage $17D = $1 se o controle de ESC estiver em execução;
  1. Deverá desligar a lâmpada de aviso ESC IL e a lâmpada de ESC OFF se o modo operacional de eixo secundário for 2 (Wheel Drive) ou 4 (Wheel Drive High) e CUT-SW = OFF ou CUT-SW = Short OFF;
  1. Deverá desligar a lâmpada de aviso ESC IL e ligar a lâmpada de ESC OFF se o modo operacional de eixo secundário for 2 (Wheel Drive) ou 4 (Wheel Drive High) e CUT-SW = Long OFF;
  1. Deverá enviar os sinais E (Vehicle Stability Enhancement Mode) com a mensagem $17D = $1 e H (Traction Control System Operating Mode) com a mensagem $17D = $1 se o modo operacional de eixo secundário for 2 (Wheel Drive) ou 4 (Wheel Drive High) e CUT-SW = OFF;
  1. Deverá enviar os sinais E (Vehicle Stability Enhancement Mode) com a mensagem $17D = $1 e H (Traction Control System Operating Mode) com a mensagem $17D = $0 se o modo operacional de eixo secundário for 2 (Wheel Drive) ou 4 (Wheel Drive High) e CUT-SW = Short OFF;
  1. Deverá enviar os sinais E (Vehicle Stability Enhancement Mode) com a mensagem $17D = $0 e H (Traction Control System Operating Mode) com a mensagem $17D = $0 se o modo operacional de eixo secundário for 2 (Wheel Drive) ou 4 (Wheel Drive High) e CUT-SW = Long OFF;
  1. Deverá desligar a lâmpada de aviso ESC IL e ligar a lâmpada de ESC OFF se o modo operacional de eixo secundário for 4 (Wheel Drive Low) e CUT-SW = Long OFF;
  1. Deverá enviar os sinais E (Vehicle Stability Enhancement Mode) com a mensagem $17D = $0 e H (Traction Control System Operating Mode) com a mensagem $17D = $1 se o modo operacional de eixo secundário for 4 (Wheel Drive Low), CUT-SW = OFF e CUT-SW = Short OFF;
  1. Deverá enviar os sinais E (Vehicle Stability Enhancement Mode) com a mensagem $17D = $0 e H (Traction Control System Operating Mode) com a mensagem $17D = $0 se o modo operacional de eixo secundário for 4 (Wheel Drive Low) e CUT-SW = Long OFF;
  1. Deverá desligar a lâmpada de aviso de ESC IL e a lâmpada de ESC OFF em situações normais de funcionamento;
  1. Deverá enviar os sinais F (Vehicle Stability Enhancement Statuus) e G (Traction Control System Operating Status) com a mensagem CAN ID $17D = $0, e os sinais E (Vehicle Stability Enhancement Mode) e H (Traction Control System Operating Mode) com a mensagem $17D = $1 em situações normais de funcionamento.

## Estratégia do Controlador

A implementação do controlador foi feita baseada em entradas físicas e entradas lógicas no sistema. Como o sistema completo exige muitas entradas, preferi por reutilizar os componentes para simular algumas funções do sistema:

* Protoboard para montagem eletrônica;
* 4 LEDs para indicação das luzes do sistema de frenagem:
  * 1 vermelho para luz do ABS;
  * 1 amarelo para luz de freio;
  * 1 verde para luz do indicador de ESC;
  * 1 azul para luz de ESC OFF.
* Um botão para simular o controle de lâmpadas (modo device control);
* Um botão para simular a chave de testes das luzes ou para simular falha externa do ABS ou do freio;
* Um botão para simular a função de ABS ativo, ou para simular a falha de configuração do ESC;
* Um potênciometro para simular o nível do fluído de freio;
* Uma chave para simular o relé de proteção do sistema ou uma falha externa em qualquer dos sistemas (ABS, freio ou ESC);

As configurações de TSC e ESC foram optadas para serem realizadas através de chaves de configuração por software, utilizando componentes de entrada do MATLAB Simulink, economizando espaço e compoenentes nas placas.


## Testes de validação

* Habilitar modo device control ligar sinais de controle das lâmpadas
* Gerar sinal externo de falha do ABS e verificar lâmpadas e sinais gerados
* Abrir relé de proteção do sistema de controle e verificar lâmpadas e sinais gerados
* Forçar utilização do ABS e verificar mensagem de saída
* Gerar falha no sistema de ABS e verificar lâmpadas e saídas após normalização
* Gerar falha interna no sistema do EBD e verificar lâmpada e saídas de mensagens
* Esvaziar fluído de freio e verificar saídas de mensagens e a lâmpada do EBD
* Gerar falha no sistema de EBD e verificar lâmpada e saídas após a normalização
* Gerar falha no ESC e verificar saídas e lâmpadas de aviso do ESC (IL e OFF)
* Gerar falha no TCS e verificar saídas e lâmpadas de aviso do ESC (IL e OFF)
* Habilitar o TSC e verificar lâmpada ESC IL e saída de mensagens
* Habilitar o ESC e verificar lâmpada ESC IL e saída de mensagens
* Colocar o sistema em modo de operação de eixo secundário (2 Wheel Drive) e variar CUT-SW em OFF, Short OFF e Long OFF, repetir para modo de operação 4 Wheel drive high e verificar as lâmpadas de ESC IL e ESC OFF e as mensagens geradas
* Colocar o sistema em modo de operação de eixo secundário (4 Wheel Drive Low) e variar CUT-SW em OFF, Short OFF e Long OFF e verificar as lâmpadas de ESC IL e ESC OFF e as mensagens geradas
* Gerar falha no sistema de ESC e verificar lâmpadas ESC IL e ESC OFF após a normalização, repetir para o sistema TCS

## Implementação Simulink
