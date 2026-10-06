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

## Conflicto resuelto

1. **¿Por qué se produjo?** El conflicto ocurrió porque modifiqué exactamente la misma línea de código (el párrafo dentro del header) en dos ramas diferentes (`main` y `feature/nuevo-eslogan`) antes de fusionarlas.
2. **¿Qué archivo estaba afectado?** El archivo afectado fue `index.html`.
3. **¿Qué decisión se tomó?** Se decidió conservar ambas ideas. Entré al archivo, eliminé los marcadores automáticos de Git (`<<<<<<<`, `=======`, `>>>>>>>`) y redacté una frase nueva que combinaba el concepto de "aprender y publicar" de una rama con las "fases de despliegue" de la otra.
4. **¿Cómo se comprobó la resolución?** Se comprobó añadiendo el archivo corregido con `git add`, realizando un nuevo commit de fusión y verificando que el comando `git log --graph --oneline --all` mostraba las ramas unidas correctamente.

## Instrucciones de uso
Para visualizar esta página web, simplemente descarga o clona este repositorio en tu equipo y haz doble clic sobre el archivo `index.html` para abrirlo en tu navegador web predeterminado. No requiere de ningún servidor ni configuración adicional.