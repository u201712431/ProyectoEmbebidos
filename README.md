# ProyectoEmbebidos

## Componentes

### Hardware Principal

<img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/ArduinoUNO.jpg" alt="ArduinoUNO">    |                                                             <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/CNC-Shield.jpg" alt="CNC-Shield">    |                                                             <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/CNC-SinConexiones.jpg" alt="CNC">
:--------------------------------------------: | :--------------------------------------------: | :----------------------------------:
Arduino UNO | CNC Shield | [CNC](https://github.com/u201712431/ProyectoEmbebidos/blob/main/CNC_add.md)
<img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/CNC-Shield-Pololus.jpg" alt="Pololus"> | <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Dispersador.jpg" alt="Dispersador"> | <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Figura24.jpg" alt="Relay">
Pololus | Dispersador | Relay

#### [**Elementos adicionales*](https://github.com/u201712431/ProyectoEmbebidos/blob/main/elementos.md)

## Proceso

- Se conectó el CNC-Shield al Arduino y los pololus al CNC-Shield. Luego se ensamblaron a la base acrílica.

Acción | Foto
:---------: | :--------:
Se realizaron las conexiones a la fuente de alimentación. El cable de alimentación se conectó a la entrada de corriente alterna.   |                             <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Conexiones_Fuente.jpg" alt="Conexiones fuente">
Se verificó la salida de voltajes mediante un voltímetro, y se comprobó que esta sea de 24V.    |                                                                <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Voltimetro.jpg" alt="Verificar voltaje">
Se conectaron los cables para la salida de corriente continua. El cable con nudo señala la salida del voltaje negativo, mientras que en el otro, el voltaje positivo.   |  <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Conexiones_CC.jpg" alt="Conexiones CC">
Se conectan los cables que trasladan corriente continua al CNC-Shield.  |                                                                                        <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Conexiones_CC-CNC_Shield.jpg" alt="Conexiones CC-CNC Shield">
La salida de corriente continua se realiza a traves de las conexiones que van directamente al cnc shield y a su vez al arduino.    |                             <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Conexiones_CNC-Arduino.jpg" alt="Conexiones CC-CNC Shield-Arduino">
Se realizan las conexiones de los motores con el CNC-Shield y Arduino | <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Conexiones_Motores-CNC_Shield-Arduino.jpg" alt="Conexiones Motores CNC Shield Arduino">
Se pegan los dispersadores a los pololus. | <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Pegado_Dispersadores-Pololus.jpg" alt="Dispersadores-Pololus">

### Configuración de softwares
Foto | Explicación
:---------: | :--------:
<img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Software_Xloader.jpg" alt="Xloader"> | Se utiliza el software Xloader para instalar el firmware GRBL directamente al Gcode Sender.
<img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/GcodeSender_Version.png" alt="Versión Gcode Sender"> | Versión utilizada de Gcode Sender en el proyecto.
<img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/GcodeSender_Comandos.png" alt="Comandos Gcode Sender"> |Se configuran los comandos para obtener un correcto uso de los motores.

### Explicación de los comandos
`$100 = 160.000 (X-Axis travel resolution, step/mm)`

`$101 = 160.000 (Y-Axis travel resolution, step/mm)`

> Dato: El motor necesita 200 pasos para obtener un correcto uso de los motores.

- La varilla que conecta la faja con el motor tiene un diámetro de 12.7 mm.

<img src="https://github.com/u201712431/ProyectoEmbebidos/blob/cb7f856b0726b51162c3755b5372260882d145b7/Imagenes/varilla.JPG" alt="Varilla con diámetro">  

Dado que necesitamos saber cuál es el número de pasos o medios pasos que se requieren para que los ejes puedan avanzar 1 mm, realizamos los siguientes pasos:

## Paso 1:
- Debemos hallar la longitud de arco de la varilla que conecta el motor con la faja:

<img src="https://github.com/u201712431/ProyectoEmbebidos/blob/3c0b9179d057773e6a420eae4bd05e3d0e138f1f/Imagenes/formula%201.JPG">
     
## Paso 2:
- Se hallará el número de pasos completos que se requieren para que el motor avance 1 mm:
     
 <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/3c0b9179d057773e6a420eae4bd05e3d0e138f1f/Imagenes/formula%202.JPG">
 
## Paso 3:
- Se hallará el número de medios pasos que se requieren para que el motor avance 1 mm:

<img src="https://github.com/u201712431/ProyectoEmbebidos/blob/fb99f7b9a43951b33d8695231fefb6b6e3049133/Imagenes/formula%203%20b.JPG">

### --------------------------------------------------------- Segunda Parte ---------------------------------------------------------
Acción | Foto
:------: | :------:
El relay será conectado al CNC Shield. | <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Figura24.jpg" alt="">
Conexión del relay al puerto COM y al puerto NO. | <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Figura25.jpg" alt="">
Demostración de la conexión. | <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Figura26.jpg" alt="">
El relay se conecta al solenoide. | <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Figura%2027.jpg" alt="">
Dos nuevas conexiones a la fuente de alimentación. | <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Figura28.jpg" alt="">
Se instaló inkscape para dibujar una figura y comprobar el funcionamiento del solenoide. Se configuraron los comandos `M8` (activar solenoide) y `M9` (desactivar solenoide). Sin embargo, luego de enviar el código a Gcode Sender, se verificó que la máquina no lograba completar el recorrido (*[Video 1]()*). Esto debido a la interferencia del voltaje de 24V, lo cual también provocaba el movimiento brusco del solenoide. | <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Figura29.png" alt="">
Aquí se comprobó el funcionamiento del relay. | <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Figura30.jpg" alt="">


## Resultados

## Equipo
- Patrick De La Cruz

- Richard Paredes

- Estéfano Sovero

- Alonso Terán

- Maria Valdez
