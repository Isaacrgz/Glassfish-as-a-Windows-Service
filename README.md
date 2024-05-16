<h2>How to install Glassfish Server as a Windows Service</h2>

<h4>¿Por qué es recomendable poner GF como un Servicio de Windows</h4>
Al ser parte de un servicio se puede configurar el inicio automático o inicio automático con retraso*, es decir, se inicia el servidor GF al encender el equipo de cómputo. 

*En caso de inicio automático con retraso, los servicios con esta configuración inicial al finalizar el inicio de los servicios de inicio auto automático.

<h5>Pasos a seguir</h5>
1. Ejecuta el archivo asadmin.bat ubicado en bin principal. 
<br/>
&ensp; Ejemplo: C:/My-Pc/documents/Server/glassfish-7.12/bin/asadmin.bat
<br/>
&ensp; Resultado: debe abrirse una ventana cmd
<br/>
2. Ejecuta el comando create-service.

