-----Vulnerabilidades-----

1. Depuración Habilitada (android:debuggable=true)

Problema: La depuración está habilitada, lo que facilita a los ingenieros inversos o atacantes conectar 
un depurador a la aplicación. Esto permite: Extraer un rastreo de pila (stack trace).
Acceder a clases y herramientas de depuración.
Obtener información crítica del funcionamiento de la app, como la lógica del código, que puede facilitar la explotación de vulnerabilidades.

Impacto: Alto. Permite un mayor riesgo de ingeniería inversa y exposición de datos sensibles.

2. Respaldo de Datos Habilitado (android:allowBackup=true)
Problema: La opción allowBackup está activada, lo que permite a cualquier usuario con acceso a ADB
(Android Debug Bridge) realizar un respaldo de los datos de la aplicación. Si un atacante tiene acceso físico al
dispositivo y la depuración USB está habilitada, puede copiar los datos de la app.

Impacto: Advertencia. Facilita el robo de datos en dispositivos comprometidos o cuando se habilita la depuración USB.

3. Receptor de Broadcast Exportado con Permisos Inadecuados
Problema: Se detectó un BroadcastReceiver (androidx.profileinstaller.ProfileInstallReceiver) que está exportado (accesible por otras apps en el dispositivo).

El receptor está protegido por el permiso android.permission.DUMP, pero este permiso no está bien definido en la app analizada. Si el permiso tiene un nivel de protección "normal" o "peligroso", una app maliciosa podría solicitarlo y tener acceso al receptor.

Impacto: Advertencia. Esto podría permitir a otras aplicaciones interactuar con este componente, comprometiendo la seguridad de la app si el permiso es insuficientemente restrictivo.




𝙙𝙚𝙨𝙞𝙜𝙣 𝙗𝙮 𝙥𝙧𝙤𝙜𝙧𝙖𝙢𝙞𝙣𝙙 𝙎𝙁
