# Como instalar GlassFish como un Servicio de Windows

¿Por qué es recomendable poner GF como un Servicio de Windows
Al ser parte de un servicio se puede configurar el `Inicio Automático` o `Inicio Automático con Retraso`, es decir, se inicia el servidor GF al encender el equipo de cómputo. 

> En caso de `Inicio Automático con Retraso`, los servicios con esta configuración inician cuando todos los servicios con la configuración `Inicio Automático` estan iniciado.


## Pasos a seguir

1. Ejecuta el archivo asadmin.bat ubicado en bin principal.
> Ruta de ejemplo: C:/My-Pc/documents/Server/glassfish-7.0.14/bin/asadmin.bat
2. Tras abrirse la ventana de **cmd**.
> Es recomenadable tener apagador el servidor GF para futuros pasos.
3. Ejecuta el siguiente comando:
```
   create-service
```
4. Una vez creado el servicio, este se encuentra en bin del dominio.
> Ruta de ejemplo: C:/My-Pc/documents/Server/glassfish-7.0.14/glassfish/domains/domain1/bin


