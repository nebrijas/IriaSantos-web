# Repositorio de trabajo del módulo 

Índice de actividades realizadas en la materia **2122-PD0D09-PERIODISMO DE DATOS II: HERRAMIENTAS DIGITALES PARA LA VISUALIZACIÓN Y PRESENTACIÓN DE DATOS (MPDD21)** del **Máster Universitario en Periodismo Digital y de Datos** de la **Universidad Nebrija**:

- [Actividad dirigida 1](ad1.md)
- [Actividad dirigida 2](ad2.md)
- [Actividad dirigida 3](ad3.md)
- [Actividad voluntaria perteneciente a la actividad dirigida 3](ad3_2.md)
- [Actividad dirigida 4](api-covid-pandas.md)


## ¿Qué he aprendido durante el desarrollo de la materia?

Durante el desarrollo de la materia he aprendido conceptos básicos relevantes a la hora de llevar a cabo visualización de datos.
A continuación, cito lo realizado durante las distintas actividades de modo resumido y qué conceptos puedo destacar de cada una de ellas, que me podrán servir a futuro:

1. **Actividad dirigida 1**:
La primera actividad ha consistido en buscar una visualización de datos y analizarla a través del uso de `Markdown`. 
En esta actividad he aprendido el uso de este tipo de código (*Markdown*), que no conocía previamente con total soltura y que a día de hoy ya puedo emplear fácilmente.
Para poner títulos se emplea el `#` a principio de frase si es `h1` y se continúa con el número de almuadillas pertinentes en función del número de título (hasta `h6`), es decir, si quiero poner un `h2` tendré que poner al inicio de la línea 2 almuadillas, para un `h3` serían 3 almuadillas y así sucesivamente.
Para añadir cursiva hay que poner antes y después de la palabra o frase **un** asterisco(`*`). 
Para añadir negrita hay que poner antes y después de la palabra o frase **dos** asteriscos (`**`).
Para añadir ambos, negrita y cursiva, hay que poner antes y después de la palabra o frase **tres** asteriscos.
Si quiero emplear una lista desordenada debo poner al inicio de cada elemento de la lista un guion (`-`).
En el caso de que lo que quiera emplear sea una lista ordenada, en lugar del guión, emplearé el número de lista seguido de punto (`1. `)
Tanto para títulos como para listados entre el elemento identificador y el texto hay que dejar un espacio.
Por último, pero no menos importante, los enlaces se identifican con el uso de `[]` para marcar la parte del texto que será enlace y posteriormente (sin espacio entre ambos) el uso de paréntesis (`()`) para identificar el enlace, que no se visualizará en el texto, pero que será al lugar que diriga clicar en el texto enlazado.
Esta actividad la llevamos a cabo a través de GitHub. 

2. **Actividad dirigida 2**:
En esta actividad hemos como convertir el contenido de GitHub a página *web* a través de la pestaña de **Ajustes** y en la opción **Páginas**. De este modo, lo que se hace en GitHub puede visualizarse como página *web*.En esta actividad hemos aprendido sobre programación literaria.
También hemos aprendido como emplear Git Bash. Puede verse todo lo llevado a cabo directamente en el enlace de la [Actividad dirigida 2](ad2.md).
Gracias a esta práctica tengo varios conceptos importantes del uso de la terminal claros:
- `cd` sirve para moverse de una carpeta a otra dentro de la terminal.
- `pwd` es el código empleado para identificar en que carpeta nos encontramos.
- `ls` se emplea para visualizar el contenido dentro de una carpeta. Si añadimos `-a` podremos ver también los archivos ocultos.
- `git clone` seguido del enlace a GitHub sirve para clonar el repositorio dentro del archivo local.
- `git config` es el código para configuración de GitHub y para identificarnos y que podamos tener acceso debemos darle el `user.name` y el `user.email`.
- `mv` sirve para mover un archivo de un lugar a otro.
- `rm` es el código empleado para eliminar archivos.
- `nano` es un editor con forma de consola, que sirve para editar archivos directamente a través de Git Bash.
- `git status` se utiliza para saber el estado o la diferencia entre los archivos de la carpeta local y de GitHub.
- `git add` sirve para agregar modificaciones al repositorio de GitHub. Tanto esta opción como las dos siguientes pueden llevarse a cabo en varios archivos simultáneamente.
- `git restore` se usa para restaurar archivos a la versión previa.
- `git commit -m "Mensaje"` es para añadir un comentario identificativo a los cambios realizados.
- `git push` guarda los cambios en el repositorio. En caso de que queramos forzar un cambio, aunque Git Bash nos avise de que algo puede suceder (por ejemplo una reescritura) debemos añadir `--force`. 
- `git pull` funciona en el sentido contrario para guardar los cambios del repositorio en el archivo local.

3. **Actividad dirigida 3**:
En la tercera actividad hemos aprendido a realizar programación literaria. Algo que se ha añadido también en la actividad previa y que se realizado hasta el final de la materia.
Se trata de explicar el código a través de la terminal empleando *Markdown* para el texto y, por tanto, para los códigos las <``> (una al inicio y otra al final)  para identificar palabras/líneas de código o para identificar fragmentos de código (tres al inicio y tres al final).
También en esta actividad hemos aprendido como se usa Jupyter con documentos de Python, y como estos mismos se pueden visualizar en la *web* de GitHub descargándolos con formato de Markdown.
Én Jupyter, lo más llamativo es que al emplear Python podemos ir llevando a cabo la programación literaria a la vez que ejecutamos el código. De este modo, se mezcla el uso de código con el texto en Markdown.
El atajo de teclado para crear un nuevo recuadro es `b`. Si queremos que el recuadro sea de código tendremos que marcar `r` y para que el tipo de recuadro sea Markdown tendremos el atajo es `m`.  
Para ejecutar el código o finalizar la edición de *Markdown* debemos pulsar `Ctrl + enter`. 
Todo lo que se modifica en Jupyter está siendo actualizado en local, por lo tanto, hay que ir a la terminal de Git Bash para *pushear* los archivos.
Esta actividad la hemos realizado con el código de *Web Scrapping* de una práctica llevada a cabo previamente en otra materia (Programación). Se ha llevado a cabo también una actividad voluntaria de programación literaria para otra actividad de la misma materia de otros compañeros, *El juego del Calamar*.

4. **Actividad dirigida 4**: En esta última actividad hemos aprendido lo más 
interesante de la materia. Como recoger datos de tablas, a trabajar con 
ellos y, sobre todo, a convertir el contenido importante de las mismas 
en gráficas. Esto se ha llevado a cabo también con el uso de Jupyter en 
archivo Python, pero se puede replicar a través del código de R, por 
ejemplo. En este caso, aunque todo era nuevo y de gran interés, me quedo 
con los siguientes códigos aprendidos e información relevante: - `df` el 
uso de creación de variables *dataframe* para buscar fragmentos de 
información en los conjuntos de datos. - La recomendación de nombrar las 
URLs que se vayan a utilizar en varias ocasiones como variables, para no 
tener que escribir siempre la URL extensa. - Para que una variable lea 
código en Json hay que llamarla de la siguiente forma `pd.read_json()`. 
- Si lo que quisieramos leer fuese un archivo csv el código sería 
`pd.read_csv()`. - Para seleccionar datos debemos crear una variable que 
defina el contenido de la variable previa definida y añadiéndole 
`.set_index('Valor eje X')['Valor eje Y']`. 
- Si queremos *plotear* esta variable para visualizarla en una gráfica normal tendremos que éscribir el nombre de la variable seguido de `.plot()` y dentro de los paréntesis podremos añadir, por ejemplo, `title="Título en la gráfica"`. También dentro del paréntesis se podrá seleccionar el tipo de gráfica a emplear, podría ser `,kind="area"` para que se coloree el área o `,kind="bar"` en caso de que interese una gráfica de barras (por ejemplo).
- También se pueden agrupar los contenidos de gráficas con valores similares a través de la concatenación (`pd.concat([contenido-1,contenido-2...contenido-n], axis=1)`). A esta gráfica podemos ponerle el encabezado de las columnas con el nombre de la gráfica actualmente creada (debe haber sido nombrada como variable) seguido de `.columns= ['Nombre-1', 'Nombre-2'...'Nombre-n']`. Para finalizar, podemos hacer el *ploteo* de los elementos concatenados (esta última variable).
