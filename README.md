# Ejemplo Documentación Dojos
![Tinkercad](./img/ArduinoTinkercad.jpg)


## Integrantes 
- Agustín Forestieri - Dojo G


## Proyecto: Semáforo con buzzer.

## Descripción
El proyecto consta de un semáforo de 2 luces por color (2R,2Y,2G) y un buzzer que funciona como alerta
para no videntes cuando la luz se encuentra en rojo.

## Función principal - encender_par()
Esta funcion se encarga de encender y apagar los leds. A su vez, en su interior, llama a la funcion activar_buzzer() si se cumple la condición de igualdad con los leds ingresados por parámetro. 

Los parámetros anteriormente mencionados son: 

int led1: recibe el número de pin al que se encuentra conectado el led N°1 que se desea encender.
int led2: recibe el número de pin al que se encuentra conectado el led N°2 que se desea encender.
int segundos: recibe un entero que será multiplicado por 1000 para trabajar en milisegundos.

La función encender_par() recibe por parámetro los números de pin de los dos leds que conforman el par a encender / apagar. Esta última funcionalidad se implementó por medio de delays, por lo que el desempeño final no es el esperado. Según lo expuesto hacia el final de la clase, la solución correcta implicaba el uso de
millis(), situación que no advertimos en la totalidad del grupo y revertiremos en la siguiente entrega.

~~~ C
void encender_par(int led1, int led2, int segundos)
{
  int tiempo = segundos*1000;
  int duracionSonido = 100;
  
  	digitalWrite(led1, HIGH);
  	digitalWrite(led2, HIGH);
        if (led1 == 5 && led2 == 6){
      		activar_buzzer(duracionSonido, 500, segundos);
      }
    delay(tiempo);
  	digitalWrite(led1, LOW);
  	digitalWrite(led2, LOW);
}

void activar_buzzer (int tiempo, int demora, int segundos)
{
  for (int i = 0; i <= segundos; i++) {
    
    tone(0,300,100);
    delay(demora);
    
  }
}
~~~

## :robot: Link al proyecto
- [proyecto](https://www.tinkercad.com/things/kw3I8IlFSfv-spd-2023-div-b-dojo-g-agustin-forestieri/editel?sharecode=NYzcZdt4x5vzjoNPYdcT1GEqU9z4MqbU3cKS4j_D7L8)

---
### Fuentes
- [Consejos para documentar](https://www.sohamkamani.com/how-to-write-good-documentation/#architecture-documentation).

- [Lenguaje Markdown](https://markdown.es/sintaxis-markdown/#linkauto).

- [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

- [Tutorial](https://www.youtube.com/watch?v=oxaH9CFpeEE).

- [Emojis](https://gist.github.com/rxaviers/7360908).

---