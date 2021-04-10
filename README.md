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
### Contexto
___________________________________________________

A casa inteligente ou smart house é uma das aplicações de Iot que mais cresce no mundo, com empresas como Google, Amazon, Apple, Samsung e várias outras do ramo de tecnologia, investindo bilhões de dólares em estudos de aprimoramento e implementações dessas tecnologias.

Um dos campos da tecnologia que mais atrai a atenção atualmente são as "assistentes" que reconhecem do usuário um comando de voz e realizam uma ação pré-programada. Por exemplo, temos informações que, em 2017, mesmo esse tipo de tecnologia não estando tão presente e desejada nas casas de cidadões comuns como ocorre hoje em dia, vendeu, segundo o CEO da Amazon, Jeff Bezzos, "Dezenas de milhões".

Assim, esse ramo de estudo e aplicação vem se tornando cada vez mais desejado e trabalhado. Portanto, decidimos fazer a nossa própria Alexa, onde enviamos um comando de voz, e uma ação é realizada. 

 
___________________________________________________

### Funcionamento
___________________________________________________

O sistema é composto por um aparelho celular, responsável por capturar o áudio e enviar o comando via Bluetooth, um componente chamado HC-05, que tem o papel de receber o comando via Bluetooth, e um microcontrolador que toma as decisões a partir do comando recebido. No caso da aplicação inicial do projeto, utilizamos leds para demonstrar a realização dos comandos recebidos. Entretanto, o objetivo é expandir o projeto e controlar outras coisas em uma residência, por exemplo.
 
___________________________________________________
### Objetivos:
 * Conseguir comunicar o aparelho celular com o HC-05, viabilizando o envio da string detectada a partir do áudio;
 * Comparar os comandos recebidos pelo microcontrolador via comunicação serial com os comandos pre-estabelecidos que realizam determinada ação;
___________________________________________________
### Materiais Recomendados
 * Microcontrolador STM32F103C8 Bluepill;
 * Módulo Bluetooth RS232 HC-05;
 * Gravador ST-LINK;
 * Aparelho celular;
 * 3x Leds;
 * Jumpers;
 * Resistores;
 * Protoboad;
___________________________________________________
## Diagrama de Blocos
![alt text](https://github.com/Lucasvitoriano25/A-low-cost-alexa/blob/master/Schematics/Diagrama-de-Blocos.png)
___________________________________________________
## Desenvolvimento
Primeiramente nós tivemos que nos preocupar em como transmitir o comando de voz para o microprocessador e como o microprocessador receberia esse comando. Assim, após pesquisarmos em diversos sites brasileiros e estrangeiros, encontramos alguns aplicativos que utilizam o banco de dados de milhares de horas do Google, transformando um comando de voz em uma string(texto). Essa string é enviada por Bluetooth a qualquer dispositivo pareado ao celular. Optamos por utilizar o AMR_Voice, pois possui interface simplificada e não codifica a mensagem enviada por voz, não sendo necessário implementar nenhuma biblioteca para transformar a mensagem encriptada em algo trabalhável.

Depois da parte do reconhecimento de voz feita, nós tivemos que decidir qual dispositivo bluetooth utilizar. Primeiramente, utilizamos um HM-10 que já tinhamos, mas, ao realizar diversos testes, vimos que ele ou possuia algum conflito na troca de informações de segurança com o Android ou estava com defeito. Portanto, por não termos muito tempo disponível para operar com a primeira possibilidade, optamos por trocar de dispositivo bluetooth,comprando um HC-05, o que acabou aumentando nossos custos pois não era possível importar da China a tempo do final do prazo. Com o HC-05 recém adiquirido, foi possível conectá-lo  com o celular, resolvendo uma parte imprescindível de nosso trabalho.

Resolvidos esses problemas fomos para a bluepill, como já sabiamos o formato em que ela recebia informações , por exemplo, se falarmos "Ligar leds" era enviado "\*Ligar Leds#", com \* marcando o começo da frase e # marcando o fim. O código não foi um grande problema , estudando sobre o uso e o funcionamento da função de Debuggar, disponível na STM32CubeIDE, ficou mais fácil termos controle sobre o código e as etapas de execução. Entretanto, um passo que causou bastante problemas foi a comunicação entre a BluePill e a interface. Inicialmente, utilizamos a STLink Utility, mas depois descobrimos que a CUBE também podia ser utilizada. Um dos problemas que encontramos foi sobre a utilização do pinos para debuggar, custando-nos algumas horas pra descobrir que eram necessários, e outro problema percebido foi que a ordem dos pinos que está apontada no stlink difere da conexão apontada na própria placa do Stlink.
___________________________________________________
## Apresentação em vídeo e demonstração do funcionamento do projeto
### Link do vídeo:
 * https://youtu.be/XtcsdfO3XXw
___________________________________________________
## Resultados
Passadas as dificuldades, chegamos ao projeto final. Conseguimos implementar com sucesso a parte de reconhecimento de voz, onde cada comando foi realizado uma função pré-programada com sucesso. Logo, foi possível sintetizar uma Alexa. Além disso, o nosso projeto possui uma enorme capacidade de expansão. Então, precisando apenas de um pouco de conhecimento de programação em C e uma noção de utilização da IDE é possível conectar diversos dispostivos BLE para realização de diversos comandos.


