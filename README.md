Vamos abordar o uso de interrupções, PWM, controle de LEDs e comunicação I2C no RP2040, integrando hardware e software para controlar LEDs e interagir com o display OLED SSD1306 e os LEDs RGB utilizando um joystick e botões.

🎯 Objetivos

Compreender o funcionamento de interrupções e debouncing em sistemas embarcados.
Implementar controle de LEDs RGB usando PWM.
Gerenciar a exibição de informações no display SSD1306 via I2C.
Desenvolver funcionalidades de interação com botões e joystick.
Integrar GPIOs, ADC e comunicação I2C para controlar dispositivos externos.

🛠️ Descrição do Projeto
O projeto utiliza os seguintes componentes conectados à placa RP2040:
Display OLED SSD1306 conectado via I2C (GPIO 14 e GPIO 15).
LEDs RGB com pinos conectados às GPIOs 11, 12 e 13.
Joystick com pinos conectados às GPIOs 22, 26 (X) e 27 (Y).
Botão A conectado à GPIO 5.
Botão B conectado à GPIO 6.

⚙️ Funcionalidades do Projeto
1️⃣ Controle de LEDs
LEDs RGB controlados por PWM (GPIOs 11, 12, 13) para indicar a intensidade de cor conforme a leitura do joystick.
Liga/desliga dos LEDs alternado pelo botão A.
2️⃣ Controle do Display OLED SSD1306
Exibe um pixel de 8x8 bits que representa o sinal analógico do joystick.
Alterna a borda do display entre círculo e retângulo ao pressionar o botão do joystick.
3️⃣ Leitura do Joystick
Fornece entradas analógicas lidas através do ADC e mapeadas para controlar a posição de um quadrado no display.
A movimentação do joystick altera a posição do quadrado no display SSD1306 e a intensidade dos LEDs RGB.
4️⃣ Interrupções e Debouncing
Utiliza interrupções para detectar a pressão dos botões (A e B).
Implementa debouncing para evitar múltiplas interrupções ao pressionar os botões.

📋 Requisitos do Projeto
Interrupções: Implementar todas as funcionalidades dos botões (A, B, Joystick) com rotinas de interrupção (IRQ).
Debouncing: Implementar tratamento de bouncing via software para garantir que os botões não gerem múltiplas interrupções.
Controle de LEDs: Utilizar LEDs RGB com PWM para controlar a cor conforme as leituras do joystick.
Uso do Display SSD1306:
Exibir informações sobre o status dos LEDs.
Mostrar o quadrado movido pelo joystick e alternar a borda entre círculo e retângulo.
Comunicação I2C: Demonstrar compreensão e implementação do protocolo I2C para controlar o display.
Controle de LEDs via Joystick: O movimento do joystick deve refletir na posição do quadrado no display SSD1306 e na intensidade dos LEDs RGB.

🚀 Como Executar o Projeto
📥 Clone o repositório:
git clone https://github.com/garccias/conversorADC
📂 Acesse a pasta do projeto:
cd conversor
🛠️ Instalação e Configuração do VS Code
Instale as dependências:
Raspberry Pi Pico SDK
Extensões do VS Code para RP2040
▶️ Compile e execute

LINK DO VÍDEO:

