----Security_Impovement_Program----

#Urgente

Desactivar depuración usb: La depuración está habilitada, lo que facilita a los ingenieros inversos 
o atacantes conectar un depurador a la aplicación. Esto permite: Extraer un rastreo de pila (stack trace).

Respaldo de Datos Habilitado: La opción allowBackup está activada, lo que permite 
a cualquier usuario con acceso a ADB (Android Debug Bridge) realizar un respaldo de los datos de la aplicación.

Receptor de Broadcast Exportado con Permisos Inadecuados
El receptor está protegido por el permiso android.permission.DUMP, pero este permiso 
no está bien definido en la app analizada. Si el permiso tiene un nivel de protección "normal" o "peligroso", 
una app maliciosa podría solicitarlo y tener acceso al receptor.

#Proximamente
A tener en cuenta es mantenernos seguros de cyber ataques, por lo que lo primero que debemos hacer cuando 
trabajamos en nuestra app es usar una herramienta en busca de vulnerabilidades y hacer esto cada vez que se 
avanza en el proyecto, ya sea crear una clase o agregar alguna librería.

Debemos tener cuidado con los permisos que usaremos para la aplicación, 
esto con el fin de garantizar el uso adecuado de la aplicación y mantener datos personales intactos.





𝙙𝙚𝙨𝙞𝙜𝙣 𝙗𝙮 𝙥𝙧𝙤𝙜𝙧𝙖𝙢𝙞𝙣𝙙 𝙎𝙁
