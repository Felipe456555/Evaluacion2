# Respuestas Evaluación 2 introducción a Tecnología de Información

Andres Gomez /Juan Capera /David Valenzuela /Santiago Agudelo

## Pregunta 1
Un Técnico desarrolla en la terminal de la Raspberry Pi 5 con Debian 13 un sketch .ino para una maqueta de Internet de las Cosas que simula un semáforo vehicular de tres tiempos en la placa Arduino UNO R3. El sketch mantiene el verde durante 5000 milisegundos, el amarillo durante 2000 milisegundos y el rojo durante 4000 milisegundos mediante la función delay(). Al contrastar la temporización real con la esperada en el monitor serial de Arduino CLI (interfaz de línea de comandos), ¿qué duración total tiene un ciclo completo?
(linea en blanco)
 ** Respuesta: 11000 milisegundos **
(linea en blanco)
La función delay() pausa la ejecución del programa durante el tiempo indicado en cada etapa en la que las LEDS se encienden. Por eso, un ciclo completo dura aproximadamente 11 segundos, sin contar pequeños tiempos adicionales de ejecución del programa.
