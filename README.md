# Introdução

Esse relatório se refere a atividade de laboratório 2 da disciplina CSW41. O objetivo dessa atividade é desenvolver uma aplicação embarcada que por meio da biblioteca TivaWare faz uso de interrupções e interage com dispositivos de I/O.

# Planejamento das fases do processo de desenvolvimento

O desenvolvimento do projeto se dará da seguinte maneira:
 * Entender o problema proposto na descrição do laboratório, bem como suas especificações.
 * Estudar a plataforma de hardware entendendo quais funcionalidade serão necessárias e como se dá o seu funcionamento.
 * Estudar plataforma de software buscando funções e bibliotecas que auxilem no cumprimento dos requisitos do projeto.
 * Configurar o projeto na IDE com as caracteristicas pertinentes ao projeto.
 * Planejamento do código e então implementação.
 * Teste e depuração a fim de garantir o funcionamento do sistema. 
  
# Definição do problema a ser resolvido

O projeto tem, então, como objetivo medir o tempo de reação de um usuário. Um led é aceso e o tempo é marcado até que o usuário aperte um botão.

# Especificação da solução

## Requisitos funcionais:

* RF1 - O jogo deve ligar o LED D1 para informar ao jogador o início da contagem de tempo.
    * RF1.1 - o LED deve ser aceso até 1 segundo após o início da operação da placa.

* RF2 - O jogo usa o botão SW1 para entrada de dados pelo usuário.

* RF3 - O jogo deve apresentar a contagem de tempo no Terminal do IAR indicando o número de clocks entre o LED acender e o botão SW1 ser pressionado e o valor de tempo correspondente em ms.

## Requisitos e Restrições não funcionais:

* RNF 1 - o limite superior de contagem de tempo é o equivalente a 3 segundos.
* RNF 2 - usar funções da TivaWare para acesso a I/O, SysTick e temporização.
* RNF 3 - a solução deve fazer uso de interrupções, obrigatoriamente de GPIO e opcionalmente do SysTick.
* RNF 4 – o vetor de exceções deve estar em memória Flash e não na RAM.

# Estudo da plataforma de HW

Para o desenvolvimento deste projeto será utilizado a plataforma TM4C1294 que é uma plataforma de desenvolvimento de baixo custo para microcontroladores (MCUs) baseados em Arm® Cortex-M4F. Algumas das principais caracteristicas da placa EK-TM4C1294XL
são:
* High Performance TM4C1294NCPDT MCU:
    * 120MHz 32-bit ARM Cortex-M4 CPU
    * 1MB Flash, 256KB SRAM, 6KB EEPROM
    * Integrated 10/100 Ethernet MAC+PHY
    * Dual 12-bit 2MSPS ADCs, motion control PWMs
    * USB 2.0 Full-speed Host, Device, and OTG (High-speed with external USB PHY)

Uma imagem da Connected LaunchPad com as caracteristicas pricipais destacadas pode ser vista a seguir:

![Imagem da placa com suas principais caracteristicas destacadas](/imagens/placa-caracteristica_principais/.png)




