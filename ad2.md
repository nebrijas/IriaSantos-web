# Actividad dirigida 2

En esta actividad dirigida se explica el proceso llevado a cabo para realizar el cambio de **README.md** a la *Actividad dirigida 1* (**ad1.md**). Aunque al inicio de ver el transcurso de la clase tuve confusión y realicé el cambio de forma online en **GitHub** posteriormente llevé a cabo las modificaciones oportunas a través de **GitBash** y serán las que se expliquen a continuación.

1. Primero había que convertir los archivos de **Markdown** a formato **HTML**. Para ello se siguen los siguientes pasos:
- Acceder a https://github.com/nebrijas/IriaSantos-web/settings/pages (esto se llevaría a cabo de la misma forma para cualquier otro repositorio tan solo cambiando el enlace por el del repositorio a modificar).
- Seleccionar en *Source* en la opción 1: *main* y en la opción 2: *root*.
De este modo ya está convertido el directorio raíz en **HTML**.

2. Posteriormente había que crear un nuevo archivo desde la web (con *Add file*) nombrándolo como **ad2.md** (que se trata del documento actual).

3. Los siguientes cambios se realizarán en local, para ello hay que descargar [Git Bash](https://git-scm.com/downloads) y posteriormente abrir la aplicación para acceder a la terminal.

3. Escribimos inicialmente `pwd` y damos *enter* para ver en que directorio nos encontramos.

4. Escribimos `git clone https://github.com/nebrijas/IriaSantos-web` y damos *enter* para copiar el directorio de nuestro repositorio (podría modificarse el nombre del repositorio por el que se quisiera clonar) al directorio local del ordenador.

5. Ahora ya tendremos la carpeta creada en nuestro directorio. Podemos verlo con `ls` (y *enter*).

6. Para acceder a ella empleamos `cd` y el nombre de la carpeta, en este caso `cd IriaSantos-web` y damos *enter*.

7. De nuevo, ahora que estamos en el interior de la carpeta, podemos usar `ls` (y *enter*) para ver el contenido que se encuentra en su interior.

8. Escribimos `git config user.name` (seguido de nuestro nombre de usuario de **GitHub**) y damos *enter*. En mi caso `git config user.name IriaSantos`.

9. Escribimos `git config user.email` (seguido del correo que se utiliza en **GitHub**) y damos *enter*. En mi caso `git config user.email iria.santos@udc.es`.

10. En el **navegador** vamos a la *web*: https://github.com/settings/tokens

11. Le damos a "*Generate new token*" y le damos el nombre en **Note** que queremos (por ejemplo, pd2). En *expiration* le marcamos la fecha de expiración (en este caso para que dure lo suficiente hasta el final del curso utilizaremos 60 días). En *select scopes* seleccionamos "Repo" (para que se activen todas las casillas de repo). Las demás casillas se dejan sin seleccionar. Posteriormente le damos a "Generar *token*".

12. Copiamos el *token* que se ha creado (se trata de una cadena de muchos caractéres en mayúscula y minúscula).

13. Regresamos a **Git Bash** y escribimos `echo "(aquí dentro el token copiado previamente)"> ../.token` para añadir un archivo oculto en la carpeta superior del árbol con el *token* que acabamos de copiar impreso.

14. Escribimos `README.md ad1.md` y damos *enter* para copiar el contenido de **README.md** a una nueva carpeta de nombre **ad1.md**.

15. Escribimos `nano README.md` y damos *enter*. Se abre la consola de *nano* para editar el archivo poniéndole un título y dos enlaces, uno a **ad1.md** y otro a este directorio (**ad2.md**). Dentro de la consola aparece la ayuda para realizar los cambios. Por ejemplo, para salir sería CTRL+X (siempre que sale `^` se refiere a la tecla *control*).

16. Escribimos `git status` y damos *enter*. Para ver las modificaciones realizadas.

17. La nueva carpeta que no existía o está modificada aparece como sin *trackear* y para que *online* esté disponible hay que escribir `git add` seguido del nombre de la carpeta y dar *enter*. En este caso el texto sería `git add README.md ad1.md`. Se pueden incluir varios elementos en conjunto.

18. Escribimos `git commit -m "modifico README.md y añado ad1.md"` y damos *enter*, por ejemplo, para escribir el comentario explicativo de los cambios realizados.

19. Escribimos `git push` y damos *enter* para guardar el contenido en **GitHub**.

20. Comprobamos que ahora ya aparece la nueva carpeta *online*.

En caso de que realicemos cambios a través de la *web* podemos obtener el contenido similar en nuestro archivo local a través del código `git pull` (+ *enter*).