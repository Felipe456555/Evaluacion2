# Respuestas Evaluación 2 introducción a Tecnología de Información

Andres Gomez /Juan Capera /David Valenzuela /Santiago Agudelo

## Pregunta 1
Un Técnico desarrolla en la terminal de la Raspberry Pi 5 con Debian 13 un sketch .ino para una maqueta de Internet de las Cosas que simula un semáforo vehicular de tres tiempos en la placa Arduino UNO R3. El sketch mantiene el verde durante 5000 milisegundos, el amarillo durante 2000 milisegundos y el rojo durante 4000 milisegundos mediante la función delay(). Al contrastar la temporización real con la esperada en el monitor serial de Arduino CLI (interfaz de línea de comandos), ¿qué duración total tiene un ciclo completo?

### Respuesta: 11000 milisegundos 

La función delay() pausa la ejecución del programa durante el tiempo indicado en cada etapa en la que las LEDS se encienden. Por eso, un ciclo completo dura aproximadamente 11 segundos, sin contar pequeños tiempos adicionales de ejecución del programa.
 
 ## Pregunta 2
En la terminal de la Raspberry Pi 5 con Debian 13, un Tecnólogo ubica la carpeta del
sketch semaforo_tres_tiempos, que contiene el archivo semaforo_tres_tiempos.ino
para la placa Arduino UNO R3. Antes de conectar la placa, necesita detectar errores
de sintaxis del código mediante Arduino CLI (interfaz de línea de comandos). ¿Qué
acción ejecuta para lograrlo?

 ## Pregunta 3
Un Técnico programa un contador binario de 4 bits en Arduino UNO R3 desde la
terminal de la Raspberry Pi 5 con Debian 13. Cada pulsación incrementa en uno la
variable contador, y el sketch enciende el LED (diodo emisor de luz) del bit i cuando el
resultado de desplazar contador i posiciones a la derecha y aplicar la operación lógica
AND bit a bit con el valor 1 es igual a 1. Tras trece pulsaciones, ¿cuáles LEDs
permanecen encendidos?


 ## Pregunta 4
 Un contador binario de 4 bits en Arduino UNO R3 incrementa su valor en más de una
unidad cada vez que el Tecnólogo presiona el pulsador mecánico, porque el contacto
genera varias transiciones eléctricas durante unos pocos milisegundos. El sketch .ino
se compila y se carga desde la terminal de la Raspberry Pi 5 con Debian 13 mediante
Arduino CLI (interfaz de línea de comandos). ¿Qué técnica de software corrige este
comportamiento?

 ## Pregunta 5
 Un Técnico conecta un DIP switch (conmutador de posiciones fijas) de 4 canales a la
placa Arduino UNO R3 para un tablero de señalización. Los canales 1 y 2 seleccionan
el patrón de encendido de 4 LEDs (diodos emisores de luz) mediante una tabla de
verdad, y los canales 3 y 4 seleccionan la velocidad del efecto. El sketch .ino se carga
desde la terminal de la Raspberry Pi 5 con Debian 13 usando Arduino CLI (interfaz de
línea de comandos). ¿Cuántos patrones distintos permite seleccionar el tablero?

 ## Pregunta 6
 Un Tecnólogo conecta cada canal de un DIP switch entre un pin digital de Arduino
UNO R3 y tierra (referencia de 0 voltios). En el sketch .ino, cada pin se declara con el
modo INPUT_PULLUP, que activa una resistencia interna conectada a 5 voltios. Si un
canal se coloca en la posición ON, que cierra el contacto con tierra, entonces la
función digitalRead() sobre ese pin devuelve:

 ## Pregunta 7
 Un Técnico programa un efecto de luces de persecución con 6 LEDs (diodos emisores
de luz) en Arduino UNO R3, cargado desde la terminal de la Raspberry Pi 5 con Debian
13 . El efecto enciende un LED por paso durante 80 milisegundos, recorre los LEDs de
izquierda a derecha y regresa, con cada LED de los extremos encendido una sola vez
por ciclo. ¿Cuánto dura un ciclo completo de ida y vuelta?


 ## Pregunta 8
 Un Tecnólogo escribe en la Raspberry Pi 5 con Debian 13 el sketch .ino de un efecto
de luces para la placa Arduino UNO R3. La compilación finaliza con éxito, pero al
ejecutar el subcomando upload de Arduino CLI (interfaz de línea de comandos), el
sistema muestra un mensaje de permiso denegado sobre el dispositivo /dev/ttyACM0.
¿Qué acción habilita el acceso al puerto serie para este usuario?

 ## Pregunta 9
 Un Técnico conecta un potenciómetro de 10 kiloohmios al pin analógico A0 de
Arduino UNO R3 para atenuar un LED mediante modulación por ancho de pulso
(PWM). El conversor analógico-digital (ADC) de 10 bits entrega una lectura de 819, y el
sketch .ino la convierte al rango de 0 a 255 con la función map() antes de llamar a
analogWrite(). El sketch se compila y se carga desde la terminal de la Raspberry Pi 5
con Debian 13 con Arduino CLI (interfaz de línea de comandos). ¿Qué valor recibe
analogWrite()?

 ## Pregunta 10
 Un Tecnólogo carga desde la terminal de la Raspberry Pi 5 con Debian 13, mediante
Arduino CLI (interfaz de línea de comandos), un sketch .ino que inicia la comunicación
serial a 9600 baudios para mostrar las lecturas de un potenciómetro. Al abrir el
monitor serial con una configuración de 115200 baudios, la terminal presenta
caracteres ilegibles. ¿Cuál es la causa de este comportamiento?


 ## Pregunta 11
 Un Técnico analiza la carga de un capacitor electrolítico de 470 microfaradios a través
de una resistencia de 10 kiloohmios, alimentados con 5 voltios desde la placa Arduino
UNO R3. Desde la terminal de la Raspberry Pi 5 con Debian 13, compila y carga el
sketch .ino con Arduino CLI (interfaz de línea de comandos) y recibe las lecturas en el
monitor serial. ¿Qué valor tiene la constante de tiempo del circuito RC
(resistencia-capacitor)?


 ## Pregunta 12
 Un Tecnólogo grafica desde el monitor serial de Arduino CLI (interfaz de línea de
comandos), ejecutado en la Raspberry Pi 5 con Debian 13, las lecturas de
analogRead() del voltaje de un capacitor en un circuito RC (resistencia-capacitor)
conectado a la placa Arduino UNO R3.
Declaración 1: Durante la descarga, las lecturas disminuyen de forma exponencial
hacia cero.
Declaración 2: Al transcurrir una constante de tiempo de carga, el capacitor alcanza el
100 % de la tensión de la fuente.
De acuerdo con el comportamiento del circuito, se puede afirmar que:

 ## Pregunta 13
 Un Técnico conmuta un LED con un transistor NPN 2N2222 (transistor bipolar de
unión) desde un pin digital de Arduino UNO R3 que entrega 5 voltios, mediante una
resistencia de base de 1 kiloohmio. El sketch .ino se carga desde la terminal de la
Raspberry Pi 5 con Debian 13 con Arduino CLI (interfaz de línea de comandos). Si la
unión base-emisor presenta una caída de 0,7 voltios en saturación, ¿qué corriente de
base circula aproximadamente?


 ## Pregunta 14
 Un Tecnólogo controla un motor de corriente continua con un transistor NPN TIP31 y un diodo
1N4007 conectado en paralelo con el motor, mediante un sketch .ino con modulación por ancho de
pulso (PWM) cargado en Arduino UNO R3 desde la terminal de la Raspberry Pi 5 con Debian 13 con
Arduino CLI (interfaz de línea de comandos). Se analizan la siguiente afirmación y la siguiente razón:
AFIRMACIÓN: El diodo protege al transistor cuando el pin PWM deja de energizar el motor.
PORQUE
RAZÓN: La bobina del motor genera una tensión inducida de polaridad inversa al interrumpirse la
corriente que la atraviesa.
Con base en el análisis, se concluye que:


 ## Pregunta 15
 Un Técnico controla la velocidad de un motor de corriente continua mediante
modulación por ancho de pulso (PWM) con la función analogWrite() en un sketch .ino
para Arduino UNO R3, cargado desde la terminal de la Raspberry Pi 5 con Debian 13
usando Arduino CLI (interfaz de línea de comandos). La base del transistor de
potencia se conecta a un pin digital con salida PWM. ¿Cuál pin digital de la placa tiene
esta capacidad?

 ## Pregunta 16
 Un Tecnólogo activa un relé electromecánico de 5 voltios, con una bobina que
demanda 72 miliamperios, para energizar un motor de corriente continua desde una
fuente independiente. Cada pin digital de Arduino UNO R3 suministra como máximo
40 miliamperios. El sketch .ino se carga desde la terminal de la Raspberry Pi 5 con
Debian 13 mediante Arduino CLI (interfaz de línea de comandos). ¿Por qué el pin
digital controla un transistor de disparo en lugar de conectarse a la bobina?


 ## Pregunta 17
 Un Técnico energiza un motor de corriente continua con un relé electromecánico
gobernado por un pin digital de Arduino UNO R3, mediante un sketch .ino cargado
desde la terminal de la Raspberry Pi 5 con Debian 13 con Arduino CLI (interfaz de línea
de comandos). Sobre el circuito se formulan las siguientes declaraciones:
Declaración 1: La bobina del relé y los contactos del motor comparten el mismo
circuito eléctrico.
Declaración 2: El diodo en paralelo con la bobina limita el pico de tensión generado al
interrumpirse su corriente.
De acuerdo con la especificación, se puede afirmar que:


 ## Pregunta 18
 Un Tecnólogo simula un sistema de riego con un potenciómetro como sensor de
humedad y un relé que energiza una bomba simulada con un motor de corriente
continua. El sketch .ino de Arduino UNO R3, cargado desde la terminal de la
Raspberry Pi 5 con Debian 13 con Arduino CLI (interfaz de línea de comandos), activa
el relé cuando la lectura supera 700 y lo desactiva cuando desciende por debajo de
600 . ¿Qué situación evita esta diferencia entre los dos umbrales?

 ## Pregunta 19
 Un Técnico conecta un microinterruptor que cierra el contacto entre el pin 2 y 5
voltios mientras la puerta permanece cerrada, con una resistencia pull-down
(resistencia hacia tierra) en el mismo pin. El sketch .ino de Arduino UNO R3, cargado
desde la terminal de la Raspberry Pi 5 con Debian 13 usando Arduino CLI (interfaz de
línea de comandos), activa un buzzer con la función tone() cuando detecta la apertura.
Si la puerta se abre, entonces:


 ## Pregunta 20
 Un Tecnólogo programa una alarma con un buzzer pasivo en un sketch .ino para Arduino UNO R3,
compilado y cargado desde la terminal de la Raspberry Pi 5 con Debian 13 con Arduino CLI (interfaz
de línea de comandos). Se analizan la siguiente afirmación y la siguiente razón:
AFIRMACIÓN: La función tone() permite que un buzzer pasivo emita un sonido de frecuencia definida.
PORQUE
RAZÓN: La función entrega en el pin un nivel HIGH constante hasta que se ejecuta la función
noTone().
Con base en el análisis, se concluye que:


 ## Pregunta 21
 Un Técnico construye un alumbrado inteligente con un divisor de voltaje: una
fotorresistencia (LDR) entre 5 voltios y el pin analógico A0 de Arduino UNO R3, y una
resistencia de 10 kiloohmios entre A0 y tierra. El sketch .ino se carga desde la terminal
de la Raspberry Pi 5 con Debian 13 usando Arduino CLI (interfaz de línea de
comandos). Si la luz ambiental disminuye, entonces la lectura de A0:


 ## Pregunta 22
 Un Tecnólogo construye un indicador de nivel tipo VU-meter (medidor de unidades de
volumen) con 5 LEDs (diodos emisores de luz) y un potenciómetro conectado al pin
analógico A0 de Arduino UNO R3. El sketch .ino, cargado desde la terminal de la
Raspberry Pi 5 con Debian 13 usando Arduino CLI (interfaz de línea de comandos),
aplica la función map() para convertir la lectura de 0 a 1023 en una cantidad de LEDs
de 0 a 5, descartando los decimales. Si la lectura vale 450, ¿cuántos LEDs permanecen
encendidos?

 ## Pregunta 23
 Un Técnico programa en Arduino UNO R3 un cruce peatonal coordinado: un script en
Python ejecutado en la Raspberry Pi 5 con Debian 13 se comunica por puerto serie con el
sketch .ino cargado mediante Arduino CLI (interfaz de línea de comandos). Con el
semáforo vehicular en verde, el peatón presiona el pulsador. La secuencia de eventos es:
I. El semáforo vehicular pasa a rojo.
II. El semáforo vehicular pasa a amarillo.
III. El semáforo peatonal pasa a verde.
IV. El semáforo peatonal vuelve a rojo y el vehicular a verde.
¿En qué orden ocurren los eventos

 ## Pregunta 24
 Un Tecnólogo ejecuta en la Raspberry Pi 5 con Debian 13 un script en Python que
abre el puerto serie de la placa Arduino UNO R3 con la biblioteca pyserial y envía de
inmediato el comando para encender un LED (diodo emisor de luz). El sketch .ino se
cargó previamente con Arduino CLI (interfaz de línea de comandos) y recibe
comandos con la función Serial.read(), pero el LED permanece apagado en el primer
envío. ¿Cuál es la causa más probable?

 ## Pregunta 25
 Un Técnico instala Arduino CLI (interfaz de línea de comandos) en una Raspberry Pi 5
con Debian 13 recién configurada y crea el sketch .ino de un semáforo vehicular para
Arduino UNO R3. Al ejecutar el subcomando compile con el identificador
arduino:avr:uno, la terminal informa que el soporte de la placa está ausente. ¿Qué
acción permite continuar con la compilación?