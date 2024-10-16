GUÍA PARA DESPLEGAR EL PROYECTO POKEDEX EN AZURE
Paso 1
Inicia sesión en tu cuenta de Azure utilizando tu correo institucional, que te otorga acceso a un año gratuito.

Paso 2
En la página principal de Azure, después de iniciar sesión, busca el ícono de App Service.

Paso 3
Crea una nueva aplicación web. Asegúrate de que la suscripción seleccionada sea Azure for Students. Asigna un nombre único a la instancia. En la pila de entorno de la aplicación, elige Node 20 LTS, que fue el que funcionó para nosotros. Selecciona Windows como sistema operativo. Para infraestructura gratuita, selecciona la opción F1, que está disponible para estudiantes, y verifica que todos los datos sean correctos.

Paso 4
Haz clic en el botón azul en la esquina inferior izquierda de la pantalla que dice Revisar y Crear. Espera unos momentos y luego selecciona Crear. Tendrás que esperar unos minutos hasta que tu instancia esté completamente creada. En la pantalla, deberías ver el estado Implementación en curso.

Paso 5
Accede al recurso creado y verifica que el dominio se haya generado correctamente. Copia este dominio y pégalo en tu navegador.

Paso 6
Para desplegar la aplicación, ve a Herramientas Avanzadas y haz clic en el botón que dice Ir en la parte superior, donde dice Debug. Selecciona CMD. En la parte izquierda, localiza la carpeta dist que se generó al abrir el proyecto en Visual Studio Code. Ejecuta los siguientes comandos:

bash
Copiar código
npm install
Una vez que se haya instalado, ejecuta:

bash
Copiar código
npm run build
Esto generará una carpeta dist. Comprime los archivos de esta carpeta en un archivo .zip y luego súbelo en la sección correspondiente a la derecha de la pantalla. Así podrás desplegar la aplicación en la instancia.

Paso 7
Corrección de errores: Al cargar la aplicación, es posible que las imágenes de los Pokémon no se muestren. Esto sucede porque la ruta de las imágenes se encuentra en una carpeta llamada pokedex-angular y no está en la ubicación correcta. Para solucionarlo, crea una carpeta pokedex-angular y coloca la carpeta assets dentro del proyecto. Con esto, las imágenes de tu proyecto deberían aparecer correctamente y la aplicación estará completamente desplegada.

Paso 8
Implementación de seguridad: En este caso, deberás crear un archivo llamado web.config. Dentro de este archivo, utiliza el formato XML para incluir las directivas de seguridad. Es importante que tengas cuidado con el contenido que agregas a este archivo, ya que una configuración incorrecta podría afectar el funcionamiento de la aplicación. En nuestro caso, logramos un nivel de seguridad A; cuando intentamos alcanzar A+, las animaciones de la aplicación se interrumpían. Después de varios intentos, conseguimos establecerlo en A.

¡Muchas gracias por tu atención!
