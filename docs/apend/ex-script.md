# Script exemplo para GPIO

Exemplo de um script para teste dos pinos IO do Raspberry PI, qual define certos pinos como output e liga/desliga-os.

Cada pino representa uma roda e sua direção, por exemplo: pino 29 é a roda direita que gira para trás (sentido anti-horário); e etc.

**Não simplesmente copie e cole esse exemplo!**

Essa livraria (RPiGPIO) está obsoleta e não funciona no Raspberry PI 5 (que é o nosso, acredito eu). Utilizaremos a gpiozero que é um wrapper para outras livarias GPIO, isto é, provê API comum para que possamos usar qualquer suíte dessas livrarias sem precisar mudar o código. lgpio é o backend padrão para gpiozero, portanto, também será a que utilizaremos.

```python
import time
import RPi.GPIO as GPIO

GPIO.setwarnings(False)
# refere-se para os números de pinos como os números que aparecem no chart de GPIO.
GPIO.setmode(GPIO.BOARD)

print("0")

GPIO.setup(29, GPIO.OUT) # pino 29 definido para output
GPIO.setup(31, GPIO.OUT) # etc.
GPIO.setup(32, GPIO.OUT)
GPIO.setup(33, GPIO.OUT)

print("1")

# define o pino 29 para o estado ligado (3,3V)
GPIO.output(29, True)
# espera 3 segundos
time.sleep(3)
# desliga-o (0V)
GPIO.output(29, False)

print("2")

GPIO.output(31, True)
time.sleep(3)
GPIO.output(31, False)

print("3")

GPIO.output(32, True)
time.sleep(3)
GPIO.output(32, False)

print("4")

GPIO.output(33, True)
time.sleep(3)
GPIO.output(33, False)

print("5")

time.sleep(3)

exit()
print("6")
```
