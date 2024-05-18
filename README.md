# Como instalar GlassFish como un Servicio de Windows

## ¿Por qué es recomendable poner GF como un Servicio de Windows?
Al ser parte de un servicio se puede configurar el `Inicio Automático` o `Inicio Automático con Retraso`, es decir, se inicia el servidor GF al encender el equipo de cómputo. 
> [!NOTE]
> En caso de `Inicio Automático con Retraso`, los servicios con esta configuración inician cuando todos los servicios con la configuración `Inicio Automático` estan iniciado.

## Pasos a seguir
1. Ejecuta el archivo ***asadmin.bat*** ubicado en bin principal. 
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

7. Para cambiar configuración actual hay que dar clic derecho sobre el *servicio > Propiedades*
> [!NOTE]
> La siguinte configuración esta basada en mi experiencia, tu puedes utilizar la configuración que desees.     
8. En la pestaña *Propiedades > General*
   + Tipo de inicio: `Inicio Automático`
   + Estado del servicio: `Iniciar`
> [!WARNING]
> Si inicias el sericio, debes de asegurarte que se encuntre apagado el **Servidor GlassFish**.
> Error: ***Windows no pudo iniciar el servicio domain1 GlassFish Server en Equipo Local***.

> [!TIP]
> Utiliza el siguiente comando en asadmin.bat como en los pasos 1-3, para apagar el Servidor GlassFish.
> ```
>    stop-domain
> ```
9. En la pestaña *Propiedades > Iniciar sesión*
   + Esta cuenta: `.Administrador`
   + Contraseña: `contraseña de la cuenta`
10. En la pestaña *Propiedades > Recuperación*
   + Primer error: `Reiniciar el servicio`
   + Segundo error: `Reiniciar el servicio`
   + Siguientes errores: `Reiniciar el servicio`
   + Restablecer recuento de errores después de: `0` días
   + Reiniciar el servidor después de: `2` minutos



