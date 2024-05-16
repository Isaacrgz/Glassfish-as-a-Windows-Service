# How to install Glassfish Server as a Windows Service

¿Por qué es recomendable poner GF como un Servicio de Windows
Al ser parte de un servicio se puede configurar el `Inicio Automático` o `Inicio Automático con Retraso*`, es decir, se inicia el servidor GF al encender el equipo de cómputo. 

---
> *En caso de `Inicio Automático con Retraso`, los servicios con esta configuración inician cuando todos los servicios con la configuración `Inicio Automático` estan iniciado.

---
> If we pull together and commit ourselves, then we can push through anything.

# Pasos a seguir</h5>
1. Ejecuta el archivo asadmin.bat ubicado en bin principal. 
<br/>
&ensp; Ejemplo: C:/My-Pc/documents/Server/glassfish-7.12/bin/asadmin.bat
<br/>
&ensp; Resultado: debe abrirse una ventana cmd
<br/>
2. Ejecuta el comando create-service.

