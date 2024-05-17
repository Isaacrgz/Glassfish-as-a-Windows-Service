# Como instalar GlassFish como un Servicio de Windows

¿Por qué es recomendable poner GF como un Servicio de Windows
Al ser parte de un servicio se puede configurar el `Inicio Automático` o `Inicio Automático con Retraso`, es decir, se inicia el servidor GF al encender el equipo de cómputo. 
> [!NOTE]
> En caso de `Inicio Automático con Retraso`, los servicios con esta configuración inician cuando todos los servicios con la configuración `Inicio Automático` estan iniciado.


## Pasos a seguir

1. Ejecuta el archivo asadmin.bat ubicado en bin principal.
> Ruta de ejemplo: C:/My-Pc/documents/Server/glassfish7/bin/asadmin.bat
2. Tras abrirse la ventana de ***cmd***.
> [!TIP]
> Es recomenadable tener apagador el servidor GF para futuros pasos.
3. Ejecuta el siguiente comando para crear el servicio:
```
   create-service
```
> [!IMPORTANT]
> Windows puede pedir permiso de administrador para crear el servicio. 
   - Resultado esperado:
     ```
         Command create-service executed successfully
     ```
4. Una vez creado el servicio, este se encuentra en bin del dominio.
> Ruta de ejemplo: C:/My-Pc/documents/Server/glassfish7/glassfish/domains/domain1/bin/domain1Service.exe
> 
> Despues de ser creado, el servicio se encuentra apagado.
5. Para configurar el `Inicio Automático` o `Inicio Automático con Retraso` del servicio es necesario iniciar el programa ***services.msc***.
6. En la lista de servicios buscamos _Domain1 GlassFish Server_ para encontrar la siguiente configuración.

| Nombre | Descripción | Estado | Tipo de inicio | Iniciar sesión como |
| :---: | :---: | :---: | :---: | :---: |
| Domain1 GlassFish Server | GlassFish Server | | Manual | Sistema local | 

7. Para cambiar configuración actual hay que dar clic derecho sobre el servicio > Propiedades
8. 



