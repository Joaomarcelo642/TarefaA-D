# Conversores A/D

## Descrição
Este projeto implementa o controle de LEDs e um display OLED usando um Raspberry Pi Pico. O sistema utiliza um joystick para ajustar a intensidade dos LEDs e mover um quadrado na tela do display OLED SSD1306. Além disso, botões permitem ativar ou desativar o PWM nos LEDs e alternar a exibição de bordas no display.

## Funcionalidades
- Controle da intensidade dos LEDs vermelho e azul baseado na posição do joystick.
- Movimentação de um quadrado na tela do display OLED conforme o joystick.
- Alternação de bordas no display ao pressionar o botão do joystick.
- Ativação e desativação do controle PWM dos LEDs ao pressionar o botão A.

## Hardware Utilizado
- Raspberry Pi Pico
- Display OLED SSD1306 (com comunicação I2C)
- Joystick analógico
- LEDs RGB (Verde, Azul e Vermelho)
- Botões

## Conexões
| Componente  | Pino do Pico |
|------------|-------------|
| LED Verde  | GP11        |
| LED Azul   | GP12        |
| LED Vermelho | GP13      |
| Botão A   | GP5         |
| Botão do Joystick | GP22  |
| Joystick X | GP26 (ADC0) |
| Joystick Y | GP27 (ADC1) |
| I2C SDA (Display) | GP14  |
| I2C SCL (Display) | GP15  |

## Dependências
O projeto utiliza a biblioteca `pico-sdk` e os seguintes módulos:
- `hardware/adc.h`
- `hardware/i2c.h`
- `hardware/pwm.h`
- `pico/stdlib.h`
- `ssd1306.h` (para controle do display OLED)
- `font.h` (para exibição de texto no display)

## Compilação e Execução
1. Certifique-se de que o `pico-sdk` está configurado corretamente no seu ambiente.
2. Compile o código usando `cmake` e `make`:
   ```sh
   mkdir build
   cd build
   cmake ..
   make
   ```
3. Envie o arquivo `.uf2` para o Raspberry Pi Pico via USB.

## Como Usar
- Mova o joystick para controlar a intensidade dos LEDs vermelho e azul.
- Pressione o botão do joystick para alternar a borda do display.
- Pressione o botão A para ativar/desativar o PWM dos LEDs e alternar a exibição do quadrado na tela.

## Vídeo de Demonstração
https://drive.google.com/file/d/15612vnRo_8yJrPZZ66SBA6RDDXUqKuM9/view?usp=sharing


