# DAW Project Hub
Pequeña página web para practicar un flujo profesional de trabajo con Git y GitHub.

Conexión SSH con GitHub: comprobada correctamente

## Historial del proyecto

Resulta preferible realizar varios commits pequeños y coherentes (también conocidos como commits atómicos) en lugar de un único commit gigante porque facilita enormemente la trazabilidad y la corrección de errores. Si cada commit representa un único cambio lógico, es mucho más sencillo aislar e identificar cuándo se introdujo un fallo, revertir un cambio específico sin afectar al resto del proyecto y permitir que otros desarrolladores entiendan paso a paso la evolución del código.

## Reflexión de seguridad

1. **¿Por qué .env.example puede publicarse?**
Porque es una plantilla vacía. No contiene datos reales, solo sirve para enseñar a otros desarrolladores qué variables necesita el proyecto para funcionar.

2. **¿Por qué .env debe ignorarse?**
Porque contiene las contraseñas reales y tokens de acceso de nuestro proyecto. Si se publica, cualquier persona podría acceder a nuestros servicios privados o bases de datos.

3. **¿Qué habría que hacer si una contraseña o un token reales se hubieran publicado en GitHub?**
Habría que entrar inmediatamente al servicio original (la base de datos, la API, etc.), revocar o borrar esa contraseña/token y generar una nueva.

4. **¿Bastaría con eliminar el archivo en un commit posterior? Justificar la respuesta.**
No bastaría. Git guarda todo el historial de cambios para siempre. Si borramos el archivo en un commit nuevo, cualquier persona podría seguir viendo la contraseña simplemente revisando los commits antiguos en GitHub.