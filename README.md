## Integrantes 
- Eduardo Cruz
- Pilar Flores
- Lian Giaccone
- Antony Llactarima
- Agustín Forestieri


## Proyecto: Semáforo con buzzer.

## Descripción
El proyecto consta de un semáforo de 2 luces por color (2R,2Y,2G) y un buzzer que funciona como alerta para no videntes cuando la luz se encuentra en rojo.

## Función principal - encender_led() / apagar_led()
Estas funciones se encargan de encender y apagar los leds. A su vez, entre implementaciones, llama a la funcion buzzerSonar() para activar el sonido del dispositivo.

Los parámetros que reciben las funcioens anteriores son: 

int ledEncender1 & 2: recibe el led previamente definido al inicio del código, aquel que se encuentra conectado el led N°1 y se desea encender.

int ledApagar1 & 2: recibe el led previamente definido al inicio del código, aquel que se encuentra conectado el led N°1 y se desea encender.

int timeOn: recibe el tiempo a ser aplicado en el delay que posee en su interior.

Según lo expuesto hacia el final de la clase, la solución correcta implicaba el uso de
millis(), situación que no advertimos en la totalidad del grupo y revertiremos en la siguiente entrega.

~~~ C
void encenderLed(int ledEncender1, int ledEncender2){
  digitalWrite(ledEncender1, 1);
  digitalWrite(ledEncender2, 1);
}

void apagarLed(int ledApagar1, int ledApagar2){
  digitalWrite(ledApagar1, 0);
  digitalWrite(ledApagar2, 0);
}

void buzzerSonar(int timeOn){
  tone(BUZZER, 200);
  delay(timeOn);
  noTone(BUZZER);
}
~~~

## :robot: Link al proyecto (principal Antony Llactarima)
- [Antony Llactarima](https://www.tinkercad.com/things/kXsdZDNvJgr-copy-of-ejercicio1dojo1spd/editel?sharecode=06vqNL1lPvXCI983qTiV1LnEfXw8uGnG0u7eQL63tvw)

- [Eduardo Cruz](https://www.tinkercad.com/things/8QwKX4AZXLV-dojo-eje-1/editel?sharecode=8iSmEHG2VN_YzUBn3qvBR9WEnuSq8YWAPDKaQzCZ76o)

- [Pilar Flores](https://www.tinkercad.com/things/amaHSScJ1uF)

- [Lian Giaccone](https://www.tinkercad.com/things/bbYj47gKiaq-surprising-lappi/editel?sharecode=zvLRXvkNyn7AwXUnfVVHZhyhxIriZwMPTGoEyKHd7T0)

- [Agustín Forestieri](https://www.tinkercad.com/things/kw3I8IlFSfv-spd-2023-div-b-dojo-g-agustin-forestieri/editel?sharecode=NYzcZdt4x5vzjoNPYdcT1GEqU9z4MqbU3cKS4j_D7L8)

---
### Fuentes
- [Consejos para documentar](https://www.sohamkamani.com/how-to-write-good-documentation/#architecture-documentation).

- [Lenguaje Markdown](https://markdown.es/sintaxis-markdown/#linkauto).

- [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

- [Tutorial](https://www.youtube.com/watch?v=oxaH9CFpeEE).

- [Emojis](https://gist.github.com/rxaviers/7360908).

---