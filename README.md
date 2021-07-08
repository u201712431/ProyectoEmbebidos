# ProyectoEmbebidos

Hola! Bienvenido a nuestro proyecto.
En esta página pordrás apreciar todo el proceso de creación realizado en nuestro proyecto final del curso Sistemas Informáticos Embebidos. El objetivo de este proyecto fue realizar una experiencia haciendo uso de softwares y herramientas mecánicas. 
El proyecto fue realizado por estudiantes de la carrera de Ingeniería Industrial y con el apoyo del profesor del curso, el Ingeniero Luis Enrique Peña Mendoza.

## 1. Componentes

### 1.1. Hardware Principal

<img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/ArduinoUNO.jpg" alt="ArduinoUNO">    |                                                             <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/CNC-Shield.jpg" alt="CNC-Shield">    |                                                             <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/CNC-SinConexiones.jpg" alt="CNC">
:--------------------------------------------: | :--------------------------------------------: | :----------------------------------:
Arduino UNO | CNC Shield | [CNC](https://github.com/u201712431/ProyectoEmbebidos/blob/main/CNC_add.md)
<img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/CNC-Shield-Pololus.jpg" alt="Pololus"> | <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Dispersador.jpg" alt="Dispersador"> | <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Figura24.jpg" alt="Relay">
Pololus | Dispersador | Relay

#### 1.2. [**Elementos adicionales*](https://github.com/u201712431/ProyectoEmbebidos/blob/main/elementos.md)

## 2. Proceso

- Se conectó el CNC-Shield al Arduino y los pololus al CNC-Shield. Luego se ensamblaron a la base acrílica.

Acción | Foto
:---------: | :--------:
Se realizaron las conexiones a la fuente de alimentación. El cable de alimentación se conectó a la entrada de corriente alterna.   |                             <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Conexiones_Fuente.jpg" alt="Conexiones fuente">
Se verificó la salida de voltajes mediante un voltímetro, y se comprobó que esta sea de 24V.    |                                                                <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Voltimetro.jpg" alt="Verificar voltaje">
Se conectaron los cables para la salida de corriente continua. El cable con nudo señala la salida del voltaje negativo, mientras que en el otro, el voltaje positivo.   |  <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Conexiones_CC.jpg" alt="Conexiones CC">
Se conectan los cables que trasladan corriente continua al CNC-Shield.  |                                                                                        <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Conexiones_CC-CNC_Shield.jpg" alt="Conexiones CC-CNC Shield">
La salida de corriente continua se realiza a traves de las conexiones que van directamente al CNC Shield y a su vez al Arduino.    |                             <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Conexiones_CNC-Arduino.jpg" alt="Conexiones CC-CNC Shield-Arduino">
Se realizan las conexiones de los motores con el CNC-Shield y Arduino | <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Conexiones_Motores-CNC_Shield-Arduino.jpg" alt="Conexiones Motores CNC Shield Arduino">
Se pegan los dispersadores a los pololus. | <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Pegado_Dispersadores-Pololus.jpg" alt="Dispersadores-Pololus">

### 2.1. Configuración de softwares
Foto | Explicación
:---------: | :--------:
<img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Software_Xloader.jpg" alt="Xloader"> | Se utiliza el software Xloader para instalar el firmware GRBL directamente al Gcode Sender.
<img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/GcodeSender_Version.png" alt="Versión Gcode Sender"> | Versión utilizada de Gcode Sender en el proyecto.
<img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/GcodeSender_Comandos.png" alt="Comandos Gcode Sender"> |Se configuran los comandos para obtener un correcto uso de los motores.

### 2.2. Explicación de los comandos
`$100 = 160.000 (X-Axis travel resolution, step/mm)`

`$101 = 160.000 (Y-Axis travel resolution, step/mm)`

> Dato: El motor necesita 200 pasos para obtener un correcto uso de los motores.

- La varilla que conecta la faja con el motor tiene un diámetro de 12.7 mm.

<img src="https://github.com/u201712431/ProyectoEmbebidos/blob/cb7f856b0726b51162c3755b5372260882d145b7/Imagenes/varilla.JPG" alt="Varilla con diámetro">  

Dado que necesitamos saber cuál es el número de pasos o medios pasos que se requieren para que los ejes puedan avanzar 1 mm, realizamos los siguientes pasos:

#### Paso 1:
- Debemos hallar la longitud de arco de la varilla que conecta el motor con la faja:

<img src="https://github.com/u201712431/ProyectoEmbebidos/blob/3c0b9179d057773e6a420eae4bd05e3d0e138f1f/Imagenes/formula%201.JPG">
     
#### Paso 2:
- Se hallará el número de pasos completos que se requieren para que el motor avance 1 mm:
     
 <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/3c0b9179d057773e6a420eae4bd05e3d0e138f1f/Imagenes/formula%202.JPG">
 
#### Paso 3:
- Se hallará el número de medios pasos que se requieren para que el motor avance 1 mm:

<img src="https://github.com/u201712431/ProyectoEmbebidos/blob/fb99f7b9a43951b33d8695231fefb6b6e3049133/Imagenes/formula%203%20b.JPG">

### ----------------------------------------------- Segunda Parte -----------------------------------------------
Acción | Foto
:------: | :------:
El relay será conectado al CNC Shield. | <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Figura24.jpg" alt="">
Conexión del relay al puerto COM y al puerto NO. | <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Figura25.jpg" alt="">
Demostración de la conexión. | <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Figura26.jpg" alt="">
El relay se conecta al solenoide. | <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Figura%2027.jpg" alt="">
Dos nuevas conexiones a la fuente de alimentación. | <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Figura28.jpg" alt="">
Se instaló inkscape para dibujar una figura y comprobar el funcionamiento del solenoide. Se configuraron los comandos `M8` (activar solenoide) y `M9` (desactivar solenoide). Sin embargo, luego de enviar el código a Gcode Sender, se verificó que la máquina no lograba completar el recorrido (*[Video 1](https://youtu.be/N6gLUjlWxIs)*). Esto debido a la interferencia del voltaje de 24V, lo cual también provocaba el movimiento brusco del solenoide. | <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Figura29.png" alt="">
Aquí se comprobó el funcionamiento del relay. | <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Figura30.jpg" alt="">

- Dado que las bobinas, que son cargas resistivas, al momento de energizarlas pueden ocurrir bajos de tensión. Esto provoca que se interrumpa la transferencia de datos.
- Por ello, se le implementó un diodo con condensador interno. Este almacena la carga de modo que compensa la energía faltante cuando la tensión es baja.
- De esta manera, se compensa los bajones de tensión y la comunicación es perenne.

Foto | Explicación
:---------: | :--------:
<img src="https://github.com/u201712431/ProyectoEmbebidos/blob/feb004de71edc8348d5bab0935f02a1f59acf9db/Imagenes/Diodoconcondensador.jpg" alt="Diodo con condensador"> | Imagen del diodo con el condensador interno. 
<img src="https://github.com/u201712431/ProyectoEmbebidos/blob/feb004de71edc8348d5bab0935f02a1f59acf9db/Imagenes/diodoconectado.jpg" alt="Diodo conectado"> | Imagen del diodo conectado.


## 3. Resultados

![Dibujo1](https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Dibujo_1.gif)
![Perro](https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Perro.gif)

## 4. Observaciones

- El funcionamiento del relay no era el correcto porque la máquina no lograba completar el recorrido. 
- Notamos que había una baja en la tensión y esto se pudo arreglar con un condensador. 
- La base de vidrio tiene una influencia aparente en los componentes. 

## 5. Recomendaciones 

- Mantener una mesa de trabajo ordenada y limpia. 
- Utilizar una base de madera ya que, como se comentó previamente, La base de vidrio pareciera tener influencia de los componentes (sobre todo con el relay). 
- Conservar Los cables ordenados ya que podrían causar una interferencia con el voltaje. 

## 6. Equipo
- Patrick De La Cruz [@PatrickDLCruz](https://github.com/PatrickDLCruz)

- Richard Paredes [@RichardJahir99](https://github.com/RichardJahir99)

- Estéfano Sovero [@u201712431](https://github.com/u201712431)

- Alonso Terán [@AlonsoTeran](https://github.com/AlonsoTeran)

- Maria Valdez [@MariaV1247](https://github.com/MariaV1247)
