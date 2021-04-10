## EQUIPE 8 - LOW COST ALEXA
João Lucas Lima Monteiro - Matrícula: 473521;
Caio Martim Barros - Matrícula: 472713;
Lucas Vitoriano de Queiroz Lira - Matrícula: 473599;

### Projeto
O projeto consiste em um dispositivo HC-05, onde o mesmo se comunicará com um aplicativo de celular via bluetooth e ele será passada informações necessárias, por meio de instruções programadas no hardware, para que seja possível a realização de atividades via comando de voz. Dessa forma, será garantido o sucesso da prática após a realização de comandos de voz para acender um LED RGB, onde será possível alterar a sua cor, por exemplo: azul para vermelho, vermelho para verde, por meio da voz.

### Informações

___________________________________________________

Na pasta docs há documentos importantes tal quais:
 * documentos da visão geral do projeto;
 
___________________________________________________

Na pasta Schematics, encontra-se o esquemático do sistema e imagens relacionadas ao projeto.
___________________________________________________

Na pasta src se encontram os códigos dos programas que desenvolvemos para o sistema.

___________________________________________________

## Introdução

### Funcionamento
___________________________________________________

O sistema é composto por um aparelho celular, responsável por capturar o áudio e enviar o comando via Bluetooth, um componente chamado HC-05, que tem o papel de receber o comando via Bluetooth, e um microcontrolador que toma as decisões a partir do comando recebido. No caso da aplicação inicial do projeto, utilizamos leds para demonstrar a realização dos comandos recebidos. Entretanto, o objetivo é expandir o projeto e controlar outras coisas em uma residência, por exemplo.
 
___________________________________________________
### Objetivos:
 * Conseguir comunicar o aparelho celular com o HC-05, viabilizando o envio da string detectada a partir do áudio;
 * Comparar os comandos recebidos pelo microcontrolador via comunicação serial com os comandos pre-estabelecidos que realizam determinada ação;
___________________________________________________
### Materiais Recomendados
 * Microcontrolador -  STM32 - Bluepill;
 * Módulo Bluetooth RS232 HC-05;
 * Gravador ST-LINK;
 * Aparelho celular;
 * Led RGB;
 * Resistores;
 * Protoboad;
___________________________________________________
## Diagrama de Blocos
![alt text](https://github.com/Lucasvitoriano25/A-low-cost-alexa/blob/master/Schematics/Diagrama-de-Blocos.png)
___________________________________________________
## Apresentação em vídeo e demonstração do funcionamento do projeto
### Link do vídeo:
 * https://youtu.be/XtcsdfO3XXw

