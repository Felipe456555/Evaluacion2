# Respuestas Evaluación 2 introducción a Tecnología de Información

Andres Gomez // Juan Capera // David Valenzuela // Santiago Agudelo

## Pregunta 1
Un Técnico desarrolla en la terminal de la Raspberry Pi 5 con Debian 13 un sketch .ino para una maqueta de Internet de las Cosas que simula un semáforo vehicular de tres tiempos en la placa Arduino UNO R3. El sketch mantiene el verde durante 5000 milisegundos, el amarillo durante 2000 milisegundos y el rojo durante 4000 milisegundos mediante la función delay(). Al contrastar la temporización real con la esperada en el monitor serial de Arduino CLI (interfaz de línea de comandos), ¿qué duración total tiene un ciclo completo?

### Respuesta: D. 11000 milisegundos 

La función delay() pausa la ejecución del programa durante el tiempo indicado en cada etapa en la que las LEDS se encienden. Por eso, un ciclo completo dura aproximadamente 11 segundos, sin contar pequeños tiempos adicionales de ejecución del programa.
 
 ## Pregunta 2
En la terminal de la Raspberry Pi 5 con Debian 13, un Tecnólogo ubica la carpeta del
sketch semaforo_tres_tiempos, que contiene el archivo semaforo_tres_tiempos.ino
para la placa Arduino UNO R3. Antes de conectar la placa, necesita detectar errores
de sintaxis del código mediante Arduino CLI (interfaz de línea de comandos). ¿Qué
acción ejecuta para lograrlo?

### Respuesta: C. Ejecuta el subcomando compile e indica el identificador de la placa.
El subcomando compile de Arduino CLI permite compilar el código fuente de un sketch para una placa específica, con el fin de detectar errores de sintaxis y otros errores de compilación antes de cargar el programa en el microcontrolador. Para una Arduino UNO R3, se debe especificar el identificador de la placa, que normalmente es arduino:avr:uno.

 ## Pregunta 3
Un Técnico programa un contador binario de 4 bits en Arduino UNO R3 desde la
terminal de la Raspberry Pi 5 con Debian 13. Cada pulsación incrementa en uno la
variable contador, y el sketch enciende el LED (diodo emisor de luz) del bit i cuando el
resultado de desplazar contador i posiciones a la derecha y aplicar la operación lógica
AND bit a bit con el valor 1 es igual a 1. Tras trece pulsaciones, ¿cuáles LEDs
permanecen encendidos?
### Respuesta: B. Los LEDs de los bits 0, 1 y 3.
El programa utiliza operaciones bit a bit para comprobar el estado de cada posición. Cuando el resultado es 1, el LED correspondiente se enciende; cuando es 0, permanece apagado. Por esta razón, los LEDs de los bits 0, 2 y 3 permanecen encendidos, mientras que el LED del bit 1 permanece apagado.


 ## Pregunta 4
 Un contador binario de 4 bits en Arduino UNO R3 incrementa su valor en más de una
unidad cada vez que el Tecnólogo presiona el pulsador mecánico, porque el contacto
genera varias transiciones eléctricas durante unos pocos milisegundos. El sketch .ino
se compila y se carga desde la terminal de la Raspberry Pi 5 con Debian 13 mediante
Arduino CLI (interfaz de línea de comandos). ¿Qué técnica de software corrige este
comportamiento?
### Respuesta: C. ignora nuevas lecturas del pulsador durante un breve intervalo tras detectar el primer cambio.
El rebote mecánico ocurre cuando los contactos internos de un pulsador generan varias transiciones eléctricas en un intervalo muy corto al presionarlo. Esto puede provocar que Arduino registre varias pulsaciones en lugar de una sola y, por lo tanto, incremente incorrectamente el contador.

 ## Pregunta 5
 Un Técnico conecta un DIP switch (conmutador de posiciones fijas) de 4 canales a la
placa Arduino UNO R3 para un tablero de señalización. Los canales 1 y 2 seleccionan
el patrón de encendido de 4 LEDs (diodos emisores de luz) mediante una tabla de
verdad, y los canales 3 y 4 seleccionan la velocidad del efecto. El sketch .ino se carga
desde la terminal de la Raspberry Pi 5 con Debian 13 usando Arduino CLI (interfaz de
línea de comandos). ¿Cuántos patrones distintos permite seleccionar el tablero?
### Respuesta: A. 4 patrones
Los canales 1 y 2 del DIP switch controlan la selección de patrones y cada uno posee dos estados posibles: ON y OFF. Por lo tanto, existen \(2^2 = 4\) combinaciones posibles. Los canales 3 y 4 regulan la velocidad del efecto, sin modificar la cantidad de patrones disponibles.

 ## Pregunta 6
 Un Tecnólogo conecta cada canal de un DIP switch entre un pin digital de Arduino
UNO R3 y tierra (referencia de 0 voltios). En el sketch .ino, cada pin se declara con el
modo INPUT_PULLUP, que activa una resistencia interna conectada a 5 voltios. Si un
canal se coloca en la posición ON, que cierra el contacto con tierra, entonces la
función digitalRead() sobre ese pin devuelve:
### Respuesta: D. Nivel LOW porque el contacto cerrado impone sobre el pin una tensión de cero voltios.
En Arduino UNO R3, la configuración INPUT_PULLUP activa una resistencia interna que conecta el pin digital a la alimentación de 5 V. Esta resistencia mantiene el pin en un estado lógico HIGH cuando el interruptor está abierto, evitando que la entrada quede flotante. Cuando el canal del DIP switch se coloca en ON, el contacto se cierra y conecta el pin directamente a tierra (GND). Como consecuencia, la tensión en el pin se aproxima a 0 V y la función digitalRead() devuelve LOW.

 ## Pregunta 7
 Un Técnico programa un efecto de luces de persecución con 6 LEDs (diodos emisores
de luz) en Arduino UNO R3, cargado desde la terminal de la Raspberry Pi 5 con Debian
13 . El efecto enciende un LED por paso durante 80 milisegundos, recorre los LEDs de
izquierda a derecha y regresa, con cada LED de los extremos encendido una sola vez
por ciclo. ¿Cuánto dura un ciclo completo de ida y vuelta?

### Respuesta: B. 800 milisegundos.
Para completar el recorrido, los LEDs se encienden primero de izquierda a derecha y después regresan, sin repetir los LEDs de los extremos. En total se realizan 10 pasos y, como cada uno dura 80 milisegundos, se multiplica 10 × 80, dando como resultado 800 milisegundos.

 ## Pregunta 8
 Un Tecnólogo escribe en la Raspberry Pi 5 con Debian 13 el sketch .ino de un efecto
de luces para la placa Arduino UNO R3. La compilación finaliza con éxito, pero al
ejecutar el subcomando upload de Arduino CLI (interfaz de línea de comandos), el
sistema muestra un mensaje de permiso denegado sobre el dispositivo /dev/ttyACM0.
¿Qué acción habilita el acceso al puerto serie para este usuario?

### Respuesta : A. Agregar el usuario al grupo dialout y reiniciar su sesión en Debian 13.
Esto sucede porque el usuario no tiene los permisos necesarios para acceder al puerto serie de Arduino. Al agregarlo al grupo dialout y volver a iniciar sesión, puede obtener los permisos necesarios para cargar el programa en la placa.

 ## Pregunta 9
 Un Técnico conecta un potenciómetro de 10 kiloohmios al pin analógico A0 de
Arduino UNO R3 para atenuar un LED mediante modulación por ancho de pulso
(PWM). El conversor analógico-digital (ADC) de 10 bits entrega una lectura de 819, y el
sketch .ino la convierte al rango de 0 a 255 con la función map() antes de llamar a
analogWrite(). El sketch se compila y se carga desde la terminal de la Raspberry Pi 5
con Debian 13 con Arduino CLI (interfaz de línea de comandos). ¿Qué valor recibe
analogWrite()?
### Respuesta : D. 204
La lectura del potenciómetro es 819, pero la función analogWrite() trabaja con valores de 0 a 255. Por eso, se utiliza la función map() para convertir la lectura al rango que necesita Arduino. Al hacer la conversión, el resultado es aproximadamente 204.

 ## Pregunta 10
 Un Tecnólogo carga desde la terminal de la Raspberry Pi 5 con Debian 13, mediante
Arduino CLI (interfaz de línea de comandos), un sketch .ino que inicia la comunicación
serial a 9600 baudios para mostrar las lecturas de un potenciómetro. Al abrir el
monitor serial con una configuración de 115200 baudios, la terminal presenta
caracteres ilegibles. ¿Cuál es la causa de este comportamiento?

### Respuesta: C. El monitor muestrea los bits con una tasa distinta a la configurada en el sketch
El problema ocurre porque el programa está configurado a 9600 baudios, mientras que el monitor serial está a 115200. Como ambos tienen velocidades diferentes, los datos no se interpretan correctamente y aparecen caracteres extraños. Para solucionarlo, hay que configurar ambos con la misma velocidad.


 ## Pregunta 11
 Un Técnico analiza la carga de un capacitor electrolítico de 470 microfaradios a través
de una resistencia de 10 kiloohmios, alimentados con 5 voltios desde la placa Arduino
UNO R3. Desde la terminal de la Raspberry Pi 5 con Debian 13, compila y carga el
sketch .ino con Arduino CLI (interfaz de línea de comandos) y recibe las lecturas en el
monitor serial. ¿Qué valor tiene la constante de tiempo del circuito RC
(resistencia-capacitor)?
### Respuesta: C. 4,7 segundos.
Para conocer la constante de tiempo del circuito, se multiplica el valor de la resistencia por el de la capacitancia. En este caso, la resistencia es de 10.000 ohmios y el capacitor es de 470 microfaradios. Al realizar la operación, el resultado es 4,7 segundos.

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
### Respuesta: A. Solo la declaración 1 es verdadera
La primera afirmación es verdadera porque, cuando el capacitor se descarga, su voltaje va disminuyendo poco a poco hasta acercarse a cero. En cambio, la segunda es falsa porque, después de una constante de tiempo, el capacitor alcanza aproximadamente el 63,2 % del voltaje de la fuente, no el 100 %.

 ## Pregunta 13
 Un Técnico conmuta un LED con un transistor NPN 2N2222 (transistor bipolar de
unión) desde un pin digital de Arduino UNO R3 que entrega 5 voltios, mediante una
resistencia de base de 1 kiloohmio. El sketch .ino se carga desde la terminal de la
Raspberry Pi 5 con Debian 13 con Arduino CLI (interfaz de línea de comandos). Si la
unión base-emisor presenta una caída de 0,7 voltios en saturación, ¿qué corriente de
base circula aproximadamente?
### Respuesta: B. 4,3 miliamperios.
La corriente de base se calcula aplicando la ley de Ohm:
I = (Voltaje de entrada − Caída base-emisor) / Resistencia
I = (5 V − 0,7 V) / 1000 Ω
I = 4,3 / 1000 = 0,0043 A = 4,3 mA.
Por lo tanto, la corriente que circula por la base del transistor es aproximadamente 4,3 miliamperios.

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

### Respuesta: B. Ambas proposiciones son verdaderas y la razón sustenta de forma directa la afirmación.
La afirmación es verdadera porque el diodo protege al transistor de los picos de tensión generados por el motor. La razón también es verdadera, ya que la bobina del motor produce una tensión inducida de polaridad inversa cuando se interrumpe la corriente. El diodo proporciona un camino para esa corriente y reduce el riesgo de dañar el transistor.

 ## Pregunta 15
 Un Técnico controla la velocidad de un motor de corriente continua mediante
modulación por ancho de pulso (PWM) con la función analogWrite() en un sketch .ino
para Arduino UNO R3, cargado desde la terminal de la Raspberry Pi 5 con Debian 13
usando Arduino CLI (interfaz de línea de comandos). La base del transistor de
potencia se conecta a un pin digital con salida PWM. ¿Cuál pin digital de la placa tiene
esta capacidad?
### Respuesta: C. Pin digital 9. 
El Arduino UNO R3 permite generar señales PWM mediante los pines digitales 3, 5, 6, 9, 10 y 11. El pin 9 es uno de ellos, por lo que puede utilizarse con la función analogWrite() para controlar la velocidad del motor mediante un transistor.

 ## Pregunta 16
 Un Tecnólogo activa un relé electromecánico de 5 voltios, con una bobina que
demanda 72 miliamperios, para energizar un motor de corriente continua desde una
fuente independiente. Cada pin digital de Arduino UNO R3 suministra como máximo
40 miliamperios. El sketch .ino se carga desde la terminal de la Raspberry Pi 5 con
Debian 13 mediante Arduino CLI (interfaz de línea de comandos). ¿Por qué el pin
digital controla un transistor de disparo en lugar de conectarse a la bobina?

### Respuesta: D. Porque la demanda de la bobina excede la capacidad de corriente que soporta el pin.
La bobina del relé consume 72 mA, mientras que el pin digital del Arduino tiene un límite indicado de 40 mA. Por esta razón, se utiliza un transistor como interruptor electrónico para controlar la corriente de la bobina sin sobrecargar el pin del Arduino

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

### Respuesta: B. Solo la declaración 2 es verdadera
La declaración 1 es falsa porque la bobina del relé y los contactos que controlan el motor pertenecen a circuitos eléctricamente separados. La declaración 2 es verdadera porque el diodo conectado en paralelo con la bobina limita el pico de tensión que aparece cuando se interrumpe la corriente, protegiendo los componentes electrónicos.

 ## Pregunta 18
 Un Tecnólogo simula un sistema de riego con un potenciómetro como sensor de
humedad y un relé que energiza una bomba simulada con un motor de corriente
continua. El sketch .ino de Arduino UNO R3, cargado desde la terminal de la
Raspberry Pi 5 con Debian 13 con Arduino CLI (interfaz de línea de comandos), activa
el relé cuando la lectura supera 700 y lo desactiva cuando desciende por debajo de
600 . ¿Qué situación evita esta diferencia entre los dos umbrales?

### Respuesta: A. Los cierres y aperturas repetidos del relé cuando la señal fluctúa alrededor de un único valor.
Utilizar dos umbrales, uno de encendido en 700 y otro de apagado en 600, implementa una técnica llamada histéresis. Esta evita que el relé se active y desactive repetidamente cuando la lectura fluctúa cerca de un mismo valor, proporcionando mayor estabilidad al sistema de riego.


 ## Pregunta 19
 Un Técnico conecta un microinterruptor que cierra el contacto entre el pin 2 y 5
voltios mientras la puerta permanece cerrada, con una resistencia pull-down
(resistencia hacia tierra) en el mismo pin. El sketch .ino de Arduino UNO R3, cargado
desde la terminal de la Raspberry Pi 5 con Debian 13 usando Arduino CLI (interfaz de
línea de comandos), activa un buzzer con la función tone() cuando detecta la apertura.
Si la puerta se abre, entonces:
### Respuesta: B. el pin 2 lee nivel LOW y el sketch activa el buzzer con la función tone().
Cuando la puerta se abre, el microinterruptor deja de conectar el pin 2 a los 5 V. La resistencia pull-down mantiene el pin conectado a tierra, por lo que se lee un nivel LOW. El programa detecta este nivel como una apertura y activa el buzzer mediante la función .


 ## Pregunta 20
 Un Tecnólogo programa una alarma con un buzzer pasivo en un sketch .ino para Arduino UNO R3,
compilado y cargado desde la terminal de la Raspberry Pi 5 con Debian 13 con Arduino CLI (interfaz
de línea de comandos). Se analizan la siguiente afirmación y la siguiente razón:
AFIRMACIÓN: La función tone() permite que un buzzer pasivo emita un sonido de frecuencia definida.
PORQUE
RAZÓN: La función entrega en el pin un nivel HIGH constante hasta que se ejecuta la función
noTone().
Con base en el análisis, se concluye que:
### Respuesta: B. La afirmación es verdadera, mientras que la razón es falsa
 La afirmación:* tone(pin, frecuencia) sí hace sonar un buzzer pasivo. El pasivo necesita una señal de frecuencia, a diferencia del activo que solo necesita voltaje.
 Falsa:* No entrega un nivel HIGH constante. Entrega una onda cuadrada que alterna HIGH/LOW a la frecuencia pedida. Si fuera HIGH constante solo escuchas un "clic". Por eso noTone() es necesario para detener la onda.

 ## Pregunta 21
 Un Técnico construye un alumbrado inteligente con un divisor de voltaje: una
fotorresistencia (LDR) entre 5 voltios y el pin analógico A0 de Arduino UNO R3, y una
resistencia de 10 kiloohmios entre A0 y tierra. El sketch .ino se carga desde la terminal
de la Raspberry Pi 5 con Debian 13 usando Arduino CLI (interfaz de línea de
comandos). Si la luz ambiental disminuye, entonces la lectura de A0:
### Respuesta: A. disminuye porque la LDR aumenta su resistencia y la resistencia fija recibe menos tensión.
Montaje: 5V -> LDR -> A0 -> 10k -> GND
Es un divisor: V_A0 = 5V _ (10k / (R_LDR + 10k))
 Con luz: R_LDR baja (1k-2k) -> V_A0 alto.
 Sin luz: R_LDR sube (100k-1M) -> el denominador crece -> V_A0 baja. La caída de tensión se la queda la LDR.

 ## Pregunta 22
 Un Tecnólogo construye un indicador de nivel tipo VU-meter (medidor de unidades de
volumen) con 5 LEDs (diodos emisores de luz) y un potenciómetro conectado al pin
analógico A0 de Arduino UNO R3. El sketch .ino, cargado desde la terminal de la
Raspberry Pi 5 con Debian 13 usando Arduino CLI (interfaz de línea de comandos),
aplica la función map() para convertir la lectura de 0 a 1023 en una cantidad de LEDs
de 0 a 5, descartando los decimales. Si la lectura vale 450, ¿cuántos LEDs permanecen
encendidos?
### Respuesta: A. 2 LEDs.
map() hace regla de tres:
450 _ 5 / 1023 = 2.19
La función map() convierte la lectura analógica de 0 a 1023 en un rango de 0 a 5. Para una lectura de 450, el resultado aproximado es 2,19. Como la función descarta los decimales, el valor se trunca a 2, por lo que permanecen encendidos dos LEDs.


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
### Respuesta: C. II, I, III, IV.
Al presionar el pulsador peatonal, el semáforo vehicular cambia primero de verde a amarillo para advertir la detención, y posteriormente pasa a rojo. Una vez detenido el tráfico vehicular, el semáforo peatonal cambia a verde, permitiendo el cruce seguro. Finalmente, el semáforo peatonal vuelve a rojo y el vehicular retorna a verde, restableciendo la circulación normal.

 ## Pregunta 24
 Un Tecnólogo ejecuta en la Raspberry Pi 5 con Debian 13 un script en Python que
abre el puerto serie de la placa Arduino UNO R3 con la biblioteca pyserial y envía de
inmediato el comando para encender un LED (diodo emisor de luz). El sketch .ino se
cargó previamente con Arduino CLI (interfaz de línea de comandos) y recibe
comandos con la función Serial.read(), pero el LED permanece apagado en el primer
envío. ¿Cuál es la causa más probable?
### Respuesta: B. La placa se reinicia al abrirse el puerto serie y tarda unos segundos en iniciar el sketch.
Al abrir el puerto serie desde Python mediante la biblioteca pyserial, la placa Arduino UNO R3 puede reiniciarse automáticamente. Durante este proceso, el sketch necesita unos segundos para inicializarse y comenzar a recibir comandos. Si el script envía la instrucción inmediatamente, el primer comando puede perderse porque Arduino todavía no está preparado para procesarlo. Por ello, se recomienda establecer una breve espera antes de transmitir los datos.

 ## Pregunta 25
 Un Técnico instala Arduino CLI (interfaz de línea de comandos) en una Raspberry Pi 5
con Debian 13 recién configurada y crea el sketch .ino de un semáforo vehicular para
Arduino UNO R3. Al ejecutar el subcomando compile con el identificador
arduino:avr:uno, la terminal informa que el soporte de la placa está ausente. ¿Qué
acción permite continuar con la compilación?
### Respuesta: D. Ejecutar core update-index y core
install con el paquete arduino:avr.
Arduino CLI requiere instalar el paquete de soporte correspondiente a la placa para poder compilar el código. El comando core update-index actualiza el índice de paquetes disponibles, mientras que core install arduino:avr instala los recursos necesarios para Arduino UNO R3. Una vez instalado el paquete, es posible ejecutar nuevamente el subcomando compile para verificar y compilar el sketch