# ProyectoEmbebidos

## Componentes

### Hardware

<img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/ArduinoUNO.jpg" alt="ArduinoUNO">    |                                                             <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/CNC-Shield.jpg" alt="CNC-Shield">    |                                                             <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/CNC-SinConexiones.jpg" alt="CNC">
:--------------------------------------------: | :--------------------------------------------: | :----------------------------------:
Arduino UNO | CNC Shield | CNC

### Elementos adicionales

## Proceso

- Se conectó el CNC-Shield al Arduino y los pololus al CNC-Shield. Luego se ensamblaron a la base acrílica.

Se realizaron las conexiones a la fuente de alimentación. El cable de alimentación se conectó a la entrada de corriente alterna.   |                             <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Conexiones_Fuente.jpg" alt="Conexiones fuente">
:---------: | :--------:
Se verificó la salida de voltajes mediante un voltímetro, y se comprobó que esta sea de 24V.    |                                                                <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Voltimetro.jpg" alt="Verificar voltaje">
Se conectaron los cables para la salida de corriente continua. El cable con nudo señala la salida del voltaje negativo, mientras que en el otro, el voltaje positivo.   |  <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Conexiones_CC.jpg" alt="Conexiones CC">
Se conectan los cables que trasladan corriente continua al CNC-Shield.  |                                                                                        <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Conexiones_CC-CNC_Shield.jpg" alt="Conexiones CC-CNC Shield">
La salida de corriente continua se realiza a traves de las conexiones que van directamente al cnc shield y a su vez al arduino.    |                             <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Conexiones_CNC-Arduino.jpg" alt="Conexiones CC-CNC Shield-Arduino">
Se realizan las conexiones de los motores con el CNC-Shield y Arduino | <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Conexiones_Motores-CNC_Shield-Arduino.jpg" alt="Conexiones Motores CNC Shield Arduino">
Se pegan los dispersadores a los pololus. | <img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Pegado_Dispersadores-Pololus.jpg" alt="Dispersadores-Pololus">

### Configuración de softwares
<img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/Software_Xloader.jpg" alt="Xloader"> | Se utiliza el software Xloader para instalar el firmware GRBL directamente al Gcode Sender.
:---------: | :--------:
<img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/GcodeSender_Version.png" alt="Versión Gcode Sender"> | Versión utilizada de Gcode Sender en el proyecto.
<img src="https://github.com/u201712431/ProyectoEmbebidos/blob/main/Imagenes/GcodeSender_Comandos.png" alt="Comandos Gcode Sender"> |Se configuran los comandos para obtener un correcto uso de los motores.

### Explicación de los comandos

## Resultados

## Equipo
Patrick De La Cruz

Richard Paredes

Estefano Sovero

Alonso Terán

Maria Valdez
