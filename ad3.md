# AD3

Esta es la **actividad dirigida 3**, que consiste en hacer un ejercicio de programación literaria aprovechando el código que hemos usado en programación con **Python** y dónde realizamos *web scrapping*. A continuación pongo el **código fuente**:

## Código fuente

El siguiente código será el que convertiremos posteriormente en programación literaria:

```
import requests
import time
import csv
import re
from bs4 import BeautifulSoup
import os
import pandas as pd
from termcolor import colored

resultados = []

req = requests.get("https://resultados.elpais.com")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup = BeautifulSoup(req.text, 'html.parser')

tags = soup.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req2 = requests.get("https://elpais.com/internacional")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup2 = BeautifulSoup(req2.text, 'html.parser')

tags = soup2.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req3 = requests.get("https://elpais.com/opinion")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup3 = BeautifulSoup(req3.text, 'html.parser')

tags = soup3.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req4 = requests.get("https://elpais.com/espana/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup4 = BeautifulSoup(req4.text, 'html.parser')

tags = soup4.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req5 = requests.get("https://elpais.com/economia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup5 = BeautifulSoup(req5.text, 'html.parser')

tags = soup5.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req6 = requests.get("https://elpais.com/sociedad/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup6 = BeautifulSoup(req6.text, 'html.parser')

tags = soup6.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req7 = requests.get("https://elpais.com/educacion/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup7 = BeautifulSoup(req7.text, 'html.parser')

tags = soup7.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req8 = requests.get("https://elpais.com/clima-y-medio-ambiente/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup8 = BeautifulSoup(req8.text, 'html.parser')

tags = soup8.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req9 = requests.get("https://elpais.com/ciencia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup9 = BeautifulSoup(req9.text, 'html.parser')

tags = soup9.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req10 = requests.get("https://elpais.com/cultura/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup10 = BeautifulSoup(req10.text, 'html.parser')

tags = soup10.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req11 = requests.get("https://elpais.com/babelia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup11 = BeautifulSoup(req11.text, 'html.parser')

tags = soup11.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req12 = requests.get("https://elpais.com/deportes/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup12 = BeautifulSoup(req12.text, 'html.parser')

tags = soup12.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req13 = requests.get("https://elpais.com/tecnologia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup13 = BeautifulSoup(req13.text, 'html.parser')

tags = soup13.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req14 = requests.get("https://elpais.com/tecnologia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup14 = BeautifulSoup(req14.text, 'html.parser')

tags = soup14.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req15 = requests.get("https://elpais.com/gente/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup15 = BeautifulSoup(req15.text, 'html.parser')

tags = soup15.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req16 = requests.get("https://elpais.com/television/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup16 = BeautifulSoup(req16.text, 'html.parser')

tags = soup16.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req17 = requests.get("https://elpais.com/eps/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup17 = BeautifulSoup(req17.text, 'html.parser')

tags = soup17.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)


os.system("clear")

print(colored("A continuación se muestran los titulares de las páginas principales del diario El País que contienen las siguientes palabras:", 'blue', attrs=['bold']))
print(colored("Feminismo", 'green', attrs=['bold']))

str_match = [s for s in resultados if "feminismo" in s]
print("\n".join(str_match))

print(colored("Igualdad", 'green', attrs=['bold']))

str_match = [s for s in resultados if "igualdad" in s]
print("\n".join(str_match))

print(colored("Mujeres", 'green', attrs=['bold']))

str_match = [s for s in resultados if "mujeres" in s]
print("\n".join(str_match))

print(colored("Mujer", 'green', attrs=['bold']))

str_match = [s for s in resultados if "mujer" in s]
print("\n".join(str_match))

print(colored("Brecha salarial", 'green', attrs=['bold']))

str_match = [s for s in resultados if "brecha salarial" in s]
print("\n".join(str_match))

print(colored("Machismo", 'green', attrs=['bold']))

str_match = [s for s in resultados if "machismo" in s]
print("\n".join(str_match))

print(colored("Violencia", 'green', attrs=['bold']))

str_match = [s for s in resultados if "violencia" in s]
print("\n".join(str_match))

print(colored("Maltrato", 'green', attrs=['bold']))

str_match = [s for s in resultados if "maltrato" in s]
print("\n".join(str_match))

print(colored("Homicidio", 'green', attrs=['bold']))

str_match = [s for s in resultados if "homicidio" in s]
print("\n".join(str_match))

print(colored("Género", 'green', attrs=['bold']))

str_match = [s for s in resultados if "género" in s]
print("\n".join(str_match))

print(colored("Asesinato", 'green', attrs=['bold']))

str_match = [s for s in resultados if "asesinato" in s]
print("\n".join(str_match))

print(colored("Sexo", 'green', attrs=['bold']))

str_match = [s for s in resultados if "sexo" in s]
print("\n".join(str_match))
```

## Programación literaria

### Librerías y módulos
Vamos a importar los siguientes módulos y librerías:

#### Módulos internos del sistema
- `time`➡️ [Este módulo proporciona varias funciones relacionadas con el tiempo.](https://docs.python.org/es/3/library/time.html)
- `csv`➡️ [Este módulo sirve para la lectura y escritura de archivos en el formato de valores separados por comas (CSV).](https://docs.python.org/es/3/library/csv.html)
- `re`➡️ [Módulo que proporciona operaciones con expresiones regulares similares a las de Perl.](https://docs.python.org/es/3/library/re.html)
- `os`➡️ [Este módulo permite emplear funciones dependientes del sistema operativo.](https://docs.python.org/es/3.10/library/os.html)

#### Librerías externas
- `requests`➡️ [Esta librería permite enviar solicitudes HTTP/1.1 de forma sencilla.](https://pypi.org/project/requests/)
- `bs4`➡️ [Beautiful Soup se trata de la librería que permite recopilar información de las páginas, es decir, realizar el web scrapping.](https://pypi.org/project/beautifulsoup4/)
- `pandas`➡️ [Es un paquete de Python que proporciona estructuras de datos rápidas, flexibles y expresivas diseñadas para hacer que trabajar con datos "relacionales" o "etiquetados" sea fácil e intuitivo.](https://pypi.org/project/pandas/)
- `termcolor`➡️ [Esta librería permite imprimir texto coloreado.](https://replit.com/talk/learn/How-to-Use-Termcolor-In-Python/24684)

#### Instalamos las librerías
Las librerías que vienen con Python no es necesario instalarlas, pero las otras deben ser instaladas.


```python
pip install requests bs4 pandas termcolor
```

#### Importamos las librerías
Empleamos tres modos distintos para importar librerías:
1. Algunas librerías son importadas directamente. Este sería el caso de `requests`. 
2. Otras, en cambio, se importan cambiándoles el nombre que se va a emplear para invocarlas. El único caso de este tipo sería `pandas`.
3. Por último, están las librerías de las que importamos determinados componentes. En este caso tenemos `bs4` y `termcolor`.


```python
import requests
import time
import csv
import re
from bs4 import BeautifulSoup
import os
import pandas as pd
from termcolor import colored
```

### Objetos/variables
Vamos a crear una serie de objetos o variables:

#### Resultados
Creamos un objeto vacío denominado `resultados` en el que se añadirán los resultados del *scrapping**.


```python
resultados = []
```

Si pasamos la función `type()` podemos observar que este objeto es de tipo *lista* de Python. Este tipo de elemento es básico y fundamental para organizar información/datos.


```python
type(resultados)
```




    list



#### Solicitud de acceso a datos en un sitio en línea
Se añade una variable con la que se hace uso de la solicitud `req=requests.get("https://resultados.elpais.com")` para recoger la información de esa **URL**.


```python
req = requests.get("https://resultados.elpais.com")
```

Si pasamos la función `type()` podemos observar que este objeto es de tipo *Respuesta* de modelo `requests`.


```python
type(req)
```




    requests.models.Response



Como está comentado en el propio código, se emplea un condicional `if` para que cuando el *estatus* no sea 200 el valor de vuelta no pueda leerse. **Este valor 200 significa que la solicitud fue exitosa y el servidor respondió con los datos solicitados.** En caso de que no se encuentre un resultado como el indicado se mostrará el mensaje *No se puede hacer Web Scrapping en* seguido de la **URL errónea**.


```python
# Si el estatus no es 200 no se puede leer la página
if (req.status_code != 200):
    raise Exception("No se puede hacer Web Scraping en"+ URL)
```

Si pasamos la función `type()` podemos observar que el objeto `req.status_code` es de tipo *entero*, por lo que el resultado será numérico.


```python
type(req.status_code)
```




    int



#### Beautiful Soup
Se añade otra variable para aplicar el *Web Scrapping*.


```python
soup = BeautifulSoup(req.text,'html.parser')
```

Si pasamos la función `type()` podemos observar que este objeto es de tipo `bs4`.


```python
type(soup)
```




    bs4.BeautifulSoup



También se añade la variable que sirve para encontrar todas las etiquetas `<h2>` dentro de la página anteriormente especificada.


```python
tags = soup.findAll("h2")
```

Si pasamos la función `type()` podemos observar que el objeto `tags` es de tipo *Resultado del set* de elementos `bs4`.


```python
type(tags)
```




    bs4.element.ResultSet



Se indica a través de un `for`, que se recorran todos los h2 dentro de la variable anterior y se imprima el texto dentro de la etiqueta. Posteriormente con `resultados.append(h2.text)` se añaden todos los textos dentro de las etiquetas a la lista inicial **resultados**.


```python
for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```

    Mónica Oltra dimite como vicepresidenta y portavoz del Gobierno valenciano
    Perfil | Oltra, la lideresa indomable
    Aitana Mas se perfila como sustituta de Mónica Oltra
    Sánchez acelera las medidas anticrisis tras el fiasco andaluz con un Consejo de Ministros el sábado 
    Feijóo vincula la victoria en Andalucía con la política “de moderación”
    Un viaje de dos meses para escalar la ruta más difícil en Yosemite y fallar en el último movimiento
    Colombia gira a la izquierda 
    Lo que Andalucía no resuelve
    Esto se arregla con otro partido de izquierdas
    Exiliados rusos
    Subcontratar la infamia
    La urna caliente
    Los errores se pagan
    Riki Blanco
    La oposición francesa rechaza un pacto con Macron aunque sopesa acuerdos puntuales
    El Gobierno saliente de Israel trata de bloquear el retorno de Netanyahu al poder
    Luigi Di Maio abandona el Movimiento 5 Estrellas y provoca una gran escisión
    
    
    Kiev trata de olvidar lo peor de la guerra: “Da miedo acostumbrarse a las sirenas de alarma”
    Sánchez y Biden conversan por teléfono sobre la agenda de la cumbre de la OTAN en Madrid
    Dos secretarios de Estado de Escrivá anuncian su salida del ministerio en 24 horas
    
    
    Los independentistas desafían la prohibición de hablar lenguas cooficiales en el Congreso
    Las farmacias podrán dispensar compuestos del cannabis dentro de seis meses 
    Vídeo | Así era la sierra de la Culebra antes del incendio que ha quemado más de 30.000 hectáreas
    El conde de Atarés, asesino de su pareja y una amiga, no tenía licencia de armas a pesar de tener un arsenal
    El Tribunal Superior de Madrid levanta las cautelares que impedían exhumar en el Valle de los Caídos
    La Fiscalía rebaja a 80 años la petición de cárcel a Villarejo en su primer gran juicio
    El Comité Olímpico Español finiquita la candidatura de los Juegos de Invierno en Cataluña y Aragón
    Gobierno y Generalitat intentan encarrilar el diálogo tras el ‘caso Pegasus’ con una reunión en Madrid
    ¿Puede una operación de descrédito por redes sociales a un gobierno ser igual de peligrosa que una amenaza física?
    Anatomía de la PrEP: la cara y la cruz de la exitosa pastilla para prevenir el VIH
    Caos en el concierto de Marc Anthony en Madrid: cientos de personas tiradas en la carretera antes y durante la actuación
    La hija transgénero de Elon Musk quiere borrarse el apellido para romper los lazos con su padre
    Rosa Olucha, mujer de Santi Millán: “Me da pereza ver que el sexo consentido siga escandalizando”
    Los bulos sobre el VIH que persisten 40 años después
    Un doble asesinato durante la Guerra Civil saca a la luz un monasterio medieval en Zaragoza
    Mónica Ojeda, pedagoga: “Tanto chicos como chicas envían contenido erótico-sexual propio. Pero las consecuencias son distintas”
    Un manual ayuda a aprender ortografía con vídeos inspirados en TikTok
    “Nos quitan los camareros como si fueran violinistas”
    Empiezan las rebajas de verano: un alivio para el bolsillo en tiempos de elevada inflación
    ‘Podcast’ | Un viaje al lugar donde se conserva (y se destruye) el planeta
    El Togado de Pompelo vuelve a casa por casualidad  116 años después
    El Zendal se vacía en primavera: 39 jornadas sin nuevos pacientes y un día con nueve ingresados 
    El fotógrafo de la naturaleza
    ¿Qué tienen en común la música y el reciclaje?
    ¿No te gustan los insectos? Tu supervivencia depende de ellos
    La caída de Sevilla, el símbolo del socialismo andaluz
    Las izquierdas ahondan su crisis e intentan salvar la apuesta de Yolanda Díaz
    El ‘pinchazo’ electoral en Andalucía desarbola la estrategia política de Vox
    Decenas de cargos de Cs piden a Arrimadas que dimita tras el batacazo andaluz
    La comisión del asalto al Capitolio se centra en las presiones y amenazas de Trump a varios funcionarios
    EE UU planea reducir la cantidad de nicotina de los cigarrillos para que no sean adictivos
    El consejo de Twitter apoya por unanimidad la venta de la compañía a Elon Musk
    
    
    Bruno Pereira, un funcionario convertido en activista para proteger a los indígenas en Brasil
    El virus de la viruela del mono se hace fuerte en cinco grandes capitales europeas
    La ofensiva de Lula para conquistar el voto evangélico
    ¿Será el hidrógeno verde el catalizador definitivo de la transición energética?
    El día en que Petro ganó a Petro
    Verónica Alcocer, la construcción de una primera dama
    Por qué no confío en Gustavo Petro
    Valencia estrena el CaixaForum más singular: un paisaje futurista dentro de un edificio icónico
    Admiración, respeto y amor por la música: lo que se puede aprender de la relación de Patti Smith y Bob Dylan
    Las reseñas de los turistas, tan útiles o tan inútiles: una cuenta de Twitter señala comentarios absurdos sobre Asturias
    ‘Gran Sol’: una pequeña gran historia para una madre de siete hijos que espera a un marino rodeado de icebergs
    María Pagés: “A los lugares cercanos se va a seguir yendo, pero a los lejanos… quién va a poder comprar los billetes”
    Ahorro y otras ventajas de las compras de kilómetro cero
    ¿Es cruel con las vacas la producción de leche?
    El auge del vestido-desnudo o por qué la moda estampa pezones en las prendas
    Los ‘stickers’ y la era de la distracción
    Llega ‘el Spotify de la lectura’: 300.000 títulos en el dispositivo
    Dressel se retira de los 100 libre del Mundial y emerge el gran Popovici
    Jordi Sargatal: “Cuando tienes a alguien como Marc Gasol, tienes que adaptar tus ideas a él”
    La campaña electoral del Athletic se enfanga entre acusaciones de machismo y homofobia
    Míchel conquista a Guardiola
    Así se convenció Ancelotti de que necesitaba a Rüdiger, y así le persuadió de fichar por el Madrid
    El Real Madrid añade más trapío en el éxito
    Por qué todos hablan de este ‘smartphone’ de diseño atractivo y rendimiento prémium
    El Nobel de Economía, Krugman: “No creo que vayamos a una crisis como la de los setenta”
    Los últimos días de Elvis: cómo la soledad y las drogas cambiaron al Rey del Rock
    Especial | Lasañas vegetales que revolucionan el comedor escolar
    La felicidad de trabajar cuatro días a la semana: “Me tendrían que pagar el doble para volver al horario anterior”
    Operación oligarca: así se rastrean los bienes del entorno de Putin en España
    Pepa Bueno analiza el resultado de las elecciones en Andalucía y las claves de la victoria del PP
    La odisea de los pasajeros del tren averiado de Ouigo
    EE UU sentencia al científico mexicano Alejandro Cabrera a cuatro años de cárcel por espionaje
    Lasso extiende el estado de excepción tras ocho días de protestas indígenas en Ecuador: “Quieren botar al presidente”
    La guerra de Putin deshace las alianzas tradicionales dentro de la UE
    Los siete de Terradillos contra las termitas de un retablo del siglo XVI
    Un día de trabajo en los servicios sociales de los distritos de Madrid: “Todo el que puede huye”
    La Audiencia Nacional imputa al exjuez Presencia por calumniar a magistrados del Supremo
    Un viaje de alta velocidad y alto riesgo: Ouigo deja encerrados a casi 1.000 pasajeros durante seis horas
    Los Países Bajos aumentan la actividad de las centrales eléctricas de carbón para reducir el uso de gas
    La regulación inmobiliaria ahuyenta a los inversores de Barcelona
    ‘La lucha contra la ELA: el 8 de marzo nació un colectivo esperanzado’, por María José Arregui
    María Madariaga: “El cannabis medicinal no es fumarse un porro, es un medicamento más”
    Ventanilla única para las víctimas de la violencia machista: una atención pionera, integral, con ayuda emocional  
    Subirats reinterpreta la ley de Universidades: freno a la precariedad, facilidades para los alumnos extranjeros y ciencia abierta
    Así puede convertirse un colegio en un espacio más fresco sin usar aire acondicionado
    “Los profesores no van a cambiar de golpe su forma de trabajar el curso que viene por la nueva ley educativa”
    Drama en la sierra de la Culebra, el paraíso del lobo ibérico que quedó abrasado por un rayo
    Las nutrias crecen en los ríos valencianos gracias a una especie invasora, el cangrejo americano, que ha mejorado su dieta
    Jardines en los tejados, árboles africanos y calles pintadas de blanco: cómo adaptar la ciudad al calor extremo
    Una piedra hallada en Egipto podría ser la primera evidencia en la Tierra de una supernova insólita
    Lucía Martínez: “¿En serio no puedes dedicar 10 minutos más a pensar el menú cuando nos estamos cargando el planeta y los animales?”
    Eloísa del Pino sustituye a Rosa Menéndez al frente del CSIC
    Por qué retuitear el vídeo sexual de Santi Millán también es delito: la desprotección de la intimidad en internet
    La inteligencia artificial reconocerá el arte gracias a la ciencia ciudadana
    ‘En esta crisis energética se mató la transformación digital’, por Paloma Llaneza
    ‘Antecedentes confirmados’, por Juanma Iturriaga
    Operación Conífera: una decena de detenidos por amañar partidos del fútbol modesto para apuestas
    La reconversión contracultural de Tavares
    ‘La tercera vía de Mark Padmore’, por Luis Gago
    Así suena ‘Break My Soul’, lo nuevo de Beyoncé 
    Isabel Pantoja, invitada estrella de las fiestas del Orgullo 2022 
    ‘Sanditon’ resucita a Jane Austen
    ‘Intimidad’, protagonizada por Santi Millán’, por Paloma Rando
    Ciencia, tecnología y entrevistas en las novedades de la programación de verano en la Cadena SER
    Mariano Alameda: “Tardé años en librarme de Íñigo”
    Los 40 años de Guillermo de Inglaterra en 16 fotos
    Shaquille O’Neal, el rey de las franquicias: 155 hamburgueserías, 40 gimnasios y una fortuna de 400 millones
    Contar bien las crisis humanitarias
    Remendar una Colombia rota a puntadas
    Viaje al fin de Occidente, en la gran frontera entre Finlandia y Rusia
    ‘Influencers’, por Rosa Montero
    Brooke Shields: «Fue duro querer a mi madre alcohólica porque me sentía responsable de ella»
    Aura García-Junco, sobre las relaciones abiertas: “Quería entender por qué generan tanto rechazo”
    Las frustraciones de Wes Craven, el genio del terror que quería dirigir melodramas
    El adiós de la entrevistadora más cafre de EE UU: Wendy Williams cierra su programa tras 14 años de impertinencias
    La horchata: el refrescante tesoro de Valencia
    Un viaje por Vic entre los murales de Josep Maria Sert y el imprescindible fuet
    Jóvenes trans, en el centro de una guerra cultural
    Así era América antes de que Colón la descubriera
    Ya no se viaja igual que antes de la pandemia: estas son las nuevas modas del turismo 
    El salto mortal de Estrella Galicia 
    Elena Ferrante a Elizabeth Strout: “Nosotras, las mujeres, somos Nadie, pero nuestra escritura es muy ambiciosa”
    Nebrija, el humanista que se enfrentó a la Inquisición
    Los cinco coches eléctricos más baratos del mercado
    El Bugatti Veyron de Cristiano Ronaldo, estrellado en Mallorca
    Diez recetas para entrar en el lujurioso mundo de las mantequillas de sabores
    Pepino con lima, sopa fría de sandía y una tarta pavlova: el menú semanal de El Comidista
    Niepómniashi castiga la insensatez de Firouzja
    Obra maestra del ataque en tromba
    Cuarenta y seis años leyendo a los lectores
    El archivo fotográfico de EL PAÍS, donde duermen algunos de los mejores retratos de la historia 
    Probamos UFO 2: el dispositivo de FOREO con masaje y calor para el rostro
    Organiza el equipaje de la mejor manera con el set de bolsas más vendido en Amazon
    Seis chanclas de los años ochenta para hombre y mujer que son ahora tendencia
    Los mejores dispositivos para aliviar las picaduras de mosquito
    Los mejores ‘eyeliners’ waterproof
    La SEPI se reúne con Abengoa en el límite para evitar un concurso de acreedores
    Autorizan la eutanasia al pistolero de Tarragona, el exvigilante de seguridad que abrió fuego contra sus compañeros
    Esperanza Aguirre desvela lo que le dijo a Abascal sobre Olona... ‘spoiler’: él no hizo caso
    Al Khelaïfi: “¿Mbappé? El Madrid ofreció mucho más que nosotros...”
    Viaje al fin del Sónar. Crónicas de la nueva fe
    Resumen Xbox & Bethesda Games Showcase | Novedades: Starfield, Pentiment, Persona 5 Royal, Diablo 4...
    

Si pasamos la función `type()` podemos observar que el objeto `resultados.append` es de tipo *función o método integrado*.


```python
type(resultados.append)
```




    builtin_function_or_method



Se repite el mismo proceso para las **URLs** de las subsecciones de https://elpais.com: internacional, opinión, España, economía, sociedad, educación, clima y medio ambiente, ciencia, cultura, babelia, deportes, tecnología, gente, televisión y eps. Para ello, se realiza el proceso previo de forma similar y se modifican los nombres de las variables poniéndosele números, por ejemplo, `req2` para la **URL** https://elpais.com/internacional, y así sucesivamente.


```python
req2 = requests.get("https://elpais.com/internacional")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup2 = BeautifulSoup(req2.text, 'html.parser')

tags = soup2.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req3 = requests.get("https://elpais.com/opinion")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup3 = BeautifulSoup(req3.text, 'html.parser')

tags = soup3.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req4 = requests.get("https://elpais.com/espana/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup4 = BeautifulSoup(req4.text, 'html.parser')

tags = soup4.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req5 = requests.get("https://elpais.com/economia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup5 = BeautifulSoup(req5.text, 'html.parser')

tags = soup5.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req6 = requests.get("https://elpais.com/sociedad/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup6 = BeautifulSoup(req6.text, 'html.parser')

tags = soup6.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req7 = requests.get("https://elpais.com/educacion/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup7 = BeautifulSoup(req7.text, 'html.parser')

tags = soup7.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req8 = requests.get("https://elpais.com/clima-y-medio-ambiente/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup8 = BeautifulSoup(req8.text, 'html.parser')

tags = soup8.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req9 = requests.get("https://elpais.com/ciencia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup9 = BeautifulSoup(req9.text, 'html.parser')

tags = soup9.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req10 = requests.get("https://elpais.com/cultura/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup10 = BeautifulSoup(req10.text, 'html.parser')

tags = soup10.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req11 = requests.get("https://elpais.com/babelia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup11 = BeautifulSoup(req11.text, 'html.parser')

tags = soup11.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req12 = requests.get("https://elpais.com/deportes/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup12 = BeautifulSoup(req12.text, 'html.parser')

tags = soup12.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req13 = requests.get("https://elpais.com/tecnologia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup13 = BeautifulSoup(req13.text, 'html.parser')

tags = soup13.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req14 = requests.get("https://elpais.com/tecnologia/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup14 = BeautifulSoup(req14.text, 'html.parser')

tags = soup14.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req15 = requests.get("https://elpais.com/gente/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup15 = BeautifulSoup(req15.text, 'html.parser')

tags = soup15.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req16 = requests.get("https://elpais.com/television/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup16 = BeautifulSoup(req16.text, 'html.parser')

tags = soup16.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)

req17 = requests.get("https://elpais.com/eps/")
# Si el estatus code no es 200 no se puede leer la página
if (req.status_code != 200):
 raise Exception("No se puede hacer Web Scraping en"+ URL)
soup17 = BeautifulSoup(req17.text, 'html.parser')

tags = soup17.findAll("h2")

for h2 in tags:
    print(h2.text)
    resultados.append(h2.text)
```

    La oposición francesa rechaza un pacto con Macron aunque sopesa acuerdos puntuales
    Luigi Di Maio abandona el Movimiento 5 Estrellas y provoca una gran escisión
    Kiev trata de olvidar lo peor de la guerra: “Da miedo acostumbrarse a las sirenas de alarma”
    Exiliados rusos
    Cambio en Colombia
    Las elecciones reparlamentarizan Francia
    Emmanuel Macron pierde las legislativas en Francia 
    ¿La democracia es una sola mujer trabajadora en la Asamblea de Francia?
    La comisión del 6 de enero se centra en las presiones y amenazas de Trump a varios funcionarios  para que no certificaran el triunfo de Biden
    El Gobierno saliente de Israel trata de bloquear el retorno de Netanyahu al poder
    El cordón sanitario a la ultraderecha se rompe en Francia
    El Nobel de la paz ruso Dmitri Muratov subasta la medalla del premio para los niños desplazados de Ucrania
    El día en que Petro ganó a Petro
    Macron busca fórmulas para evitar la parálisis tras el revés en las elecciones legislativas en Francia
    Vídeo | Operación oligarca: así se rastrean los bienes del entorno de Putin en España
    Borrell acusa a Rusia de “crímenes de guerra” por retener el grano de Ucrania 
    Un grupo yihadista asesina a 132 civiles en una nueva matanza en el centro de Malí
    Vídeo | Día del Refugiado: así han cambiado los flujos durante la guerra de Ucrania
    Macron pierde la mayoría absoluta en las elecciones legislativas de Francia
    Las protestas en Ecuador, en imágenes
    El Supremo de EE UU vota a favor de conceder fondos públicos a escuelas religiosas en el Estado de Maine
    La ofensiva de Lula para conquistar el voto evangélico
    Bruno Pereira, un funcionario convertido en activista para proteger a los indígenas en Brasil
    Lasso extiende el estado de excepción tras ocho días de protestas indígenas en Ecuador: “Quieren botar al presidente”
    Colombia gira a la izquierda 
    La dimisión de Oltra
    Exiliados rusos
    Lo que Andalucía no resuelve
    Vidas gitanas
    Un eclipse de Sol
    Subcontratar la infamia
    Esto se arregla con otro partido de izquierdas
    La urna caliente
    Los errores se pagan
    Casa rota
    Vuelco en Andalucía
    Macron en precario
    El Roto
    Peridis
    Flavita Banana
    Riki Blanco
    Sciammarella
    Planeta de Plástico, por Malagón
    Envía tu carta
    ¿Aún hay guerra?
    Ideología y elecciones andaluzas
    ¿Lista de espera disuasoria?
    Opinar sin insultar
    Contra el conflicto de intereses, transparencia
    Entre los derechos de Esther López y los de los lectores
    El defensor del lector contesta
    Mónica Oltra dimite como vicepresidenta y portavoz del Gobierno valenciano
    Sánchez acelera las medidas anticrisis con un consejo extraordinario el sábado tras el fiasco andaluz
    Los malos resultados en Andalucía y la presión de las bases precipitan la “refundación” de Ciudadanos 
    Los errores se pagan
    Desborde popular en Andalucía
    Demasiado ruido en el Gobierno de coalición
    La ‘confederalización’ del PP
    El hombre que quiso reinar
    Los socios del Gobierno le piden en el Congreso una “reflexión profunda” tras el fracaso andaluz
    Los independentistas desafían la prohibición de hablar lenguas cooficiales en el Congreso
    Gobierno y Generalitat intentan encarrilar el diálogo tras la crisis por el ‘caso Pegasus’ con una reunión en Madrid
    Feijóo traza el rumbo al PP e insta a seguir una política “de centralidad y moderación”
    La caída de Sevilla, el símbolo del socialismo andaluz
    Sánchez encaja el “golpe muy duro” y acelera las medidas anticrisis 
    El hartazgo tras el incendio de la sierra de la Culebra salta a las Cortes y a la calle por la falta de prevención de la Junta
    Tezanos pronostica que el PSOE “está por encima del 28-29%” de intención de voto “y va a estarlo” 
    El Tribunal Superior de Madrid levanta las cautelares que impedían exhumar en el Valle de los Caídos
    La Fiscalía rebaja a 80 años la petición de cárcel a Villarejo en su primer gran juicio
    El PSOE retira la iniciativa para blindar al fiscal general cuando deje el cargo
    El secreto de Fuerteventura se hace viral: la ‘playa de las palomitas’
    Locos por meterse en todos los charcos
    Artesanía y cultura que conquista a las ‘influencers’
    Más allá de la capital. El triunfo de la vida rural madrileña
    Así lucha la tierra del cerezo para conseguir un nuevo florecimiento económico
    “Siempre me ha parecido que los que iban disfrazados eran los demás”
    “La herramienta más poderosa para salvar a la humanidad son las matemáticas”
    La regulación inmobiliaria ahuyenta a los inversores de Barcelona
    Dos secretarios de Estado de Escrivá anuncian en apenas 24 horas su salida del ministerio
    El Corte Inglés recompra la mitad de las acciones en manos del inversor catarí Al Thani por 387 millones de euros
    Los fondos dan a Abengoa hasta el viernes para salvarse del concurso de acreedores
    Aterrizaje suave sin fragmentación
    El ajuste fiscal que viene: ¿Qué opinan los ciudadanos?
    Las finanzas que corroen la industria 
    Una oportunidad perdida en el proceso de las energías renovables 
    El despertar de las primas de riesgo
    Un viaje de alta velocidad y alto riesgo: Ouigo deja encerrados a casi 1.000 pasajeros durante seis horas
    Empiezan las rebajas de verano de 2022: un alivio para el bolsillo en tiempos de elevada inflación
    Los sindicatos exigen a la CEOE volver a la mesa de negociación de los salarios: “Si no hay acuerdo, la conflictividad va a crecer”
    Kellog se divide en tres compañías para acelerar su crecimiento
    La CNMV redoblará la vigilancia sobre la publicidad de criptomonedas en eventos deportivos
    El consejo de Twitter apoya por unanimidad la venta de la compañía a Elon Musk 
    La Airef critica al Gobierno la falta de información sobre la ejecución de los fondos europeos
    Los Países Bajos aumentan la actividad de las centrales eléctricas de carbón para reducir el uso de gas
    Montero enfría la propuesta de Yolanda Díaz y avanza que el recargo a las eléctricas se aplicará en 2023
    Los tripulantes de EasyJet en España irán también a la huelga en julio
    Yolanda Díaz reactiva tras las elecciones andaluzas la propuesta de un cheque de 300 euros para mitigar el golpe de la inflación
    Ferrari corre hacia un mundo más verde y caro
    Vientres de alquiler: una boyante y turbia industria que aprovecha las rendijas legales para enriquecerse
    Ya no se viaja igual que antes de la pandemia: estas son las nuevas modas del turismo 
    El salto mortal de Estrella Galicia 
    Así es la española que revoluciona las burbujas de champán más exclusivas
    La SEPI se reúne con Abengoa en el límite para evitar un concurso de acreedores
    Hasta 12 cotizadas pagan el doble en dividendos que el bono soberano
    Six Senses Ibiza estrena dos mansiones a 15.000 euros la noche
    Hacienda eleva el control de las criptomonedas: obligará a expresar en euros saldos y operaciones
    Parir en casa, educarlo por mi cuenta… ¿Qué puedo decidir sobre mi hijo y qué no?
    Saltarse un paso a nivel de camino a la oficina es accidente laboral
    Sonría a la cámara: ¿Cuándo te pueden grabar legalmente en la oficina?
    ¿Es esta la edad dorada del emprendimiento universitario?
    Y después de la EBAU, ¿qué?
    Joan Ramón Castelló: “En la formación ‘online’ hay que ser realistas con el tiempo disponible y contar con el apoyo de la familia”
    Cancerberos del bienestar de la empresa
    Salud a golpe de clic con la cercanía del médico de cabecera
    Cómo garantizar la seguridad en un mundo de amenazas híbridas
    ¿Cuáles son los dilemas éticos del uso de la inteligencia artificial?
    Las aventuras de un par de calcetines que dan empleo a todo un pueblo
    Cultura financiera como punto de partida para volver a empezar
    Logística a bajas temperaturas, la revolución que vino del frío
    Una cartera contra la despoblación financiera
    ‘Coopetir’: la actitud DFactory
    Así serán las ciudades de la (nueva) última milla
    PERTE Agroalimentario: ¿cómo acceder a los fondos europeos?
    Las preguntas más frecuentes al acceder a las ayudas europeas
    ¿Crisis de deuda mundial a la vista?
    ¿Está al frente España de la revolución del hidrógeno? 
    El momento de la energía solar
    Las principales reformas (con subvención europea) para ahorrar energía en la vivienda
    Gloria Ramos, cuando el afán de superación acaba en la alfombra roja 
    La importancia de la cultura financiera para tener una buena jubilación
    Hotmart y su plataforma 360 para creadores de contenidos
    Una aplicación para presentar la declaración desde casa y conseguir los máximos beneficios
    Las farmacias podrán dispensar compuestos del cannabis dentro de seis meses 
    Estados Unidos planea reducir la cantidad de nicotina de los cigarrillos para que no sean adictivos
    El conde de Atarés, asesino de su pareja y una amiga, nunca tuvo licencia de armas a pesar de tener un arsenal en casa
    La lucha contra la ELA: el 8 de marzo nació un colectivo esperanzado
    La pederastia, problema de poder
    Educación y trabajo: ¿cómo lograr este binomio perfecto en Iberoamérica?
    Sin currículos
    Subirats reinterpreta la ley de Universidades: freno a la precariedad, facilidades para los alumnos extranjeros y ciencia abierta
    Andalucía inmoviliza las conservas vegetales de la marca El Hortelano fabricadas en Málaga por falta de control alimentario
    El virus de la viruela del mono se hace fuerte en cinco grandes capitales europeas
    Las víctimas tendrán una vía directa para asesorar al Defensor en su investigación sobre los abusos en la Iglesia
    Ventanilla única para las víctimas de la violencia machista: una atención pionera, integral, con ayuda emocional  
    Anatomía de la PrEP: la cara y la cruz de la exitosa pastilla para prevenir el VIH
    La lucha contra la ELA: el 8 de marzo nació un colectivo esperanzado
    “Los profesores no van a cambiar de golpe su forma de trabajar el curso que viene por la nueva ley educativa”
    Jardines en los tejados, árboles africanos y calles pintadas de blanco: cómo adaptar la ciudad al calor extremo
    “El cannabis medicinal no es fumarse un porro, es un medicamento más”
    El director Paul Haggis, detenido en Italia acusado de abusar sexualmente durante dos días de una mujer
    Mitos, falsedades, bulos y realidades sobre el VIH 40 años después
    Educadores con VIH para minimizar el impacto tras el primer diagnóstico
    Interactivo | Los 14 cambios en los aeropuertos españoles que no ves y que ya están ocurriendo
    La fórmula de Carboneros para evitar el éxodo rural: trabajar cuidando a los vecinos 
    “Me sentí solo 17 años”. La batalla por romper con el aislamiento
    ¿Qué tienen en común perros y gatos cuando son cachorros?
    La guía definitiva para alimentarnos mejor (y cuidar nuestra salud y la del planeta)
    Más vida después del cáncer de próstata avanzado 
    Cáncer de ovario, el más rebelde de los tumores ginecológicos
    El metro como refugio. De los andenes de Madrid en 1936 a los de Kiev en 2022
    La salud mental de los refugiados: cómo abrirse para cerrar las heridas
    El desconocido (y esencial) apoyo de los farmacéuticos a los pacientes crónicos
    El esfuerzo de una paciente por convertirse en su doctora
    Así es la vida de los refugiados ucranianos en España
    ¿Cómo será el envase para alimentos y bebidas del futuro?
    Subirats reinterpreta la ley de Universidades: freno a la precariedad, facilidades para los alumnos extranjeros y ciencia abierta
    “Los profesores no van a cambiar de golpe su forma de trabajar el curso que viene por la nueva ley educativa”
    Trampantojo de pescado y lasaña vegetal en el comedor: cientos de colegios buscan fórmulas para que llevar la alimentación responsable a los niños
    Vídeo | Las recetas del cocinero escolar para que los niños de El Grau coman sano y rico 
    Así puede convertirse un colegio en un espacio más fresco sin usar aire acondicionado
    209.691 candidatos compiten por una plaza en la última convocatoria sin ventaja aplastante para los interinos
    El mileurismo asoma en la mitificada carrera de dentista: “Nunca imaginé una situación así”
    Las notas de la Selectividad 2022: del 93% de aprobados en Canarias y el 94,5% en Madrid, al éxito casi total en La Rioja
    Las universitarias desertan del grado de Matemáticas ahora que tiene pleno empleo. ¿Por qué?
    Educación y trabajo: ¿cómo lograr este binomio perfecto en Iberoamérica?
    El Consejo de Navarra avala la creación de 350 plazas para profesorado de inglés al entender que no vulnera la normativa estatal
    Sin currículos
    La escuela concertada ante las desigualdades: el debate pendiente
    La equidad frente a las políticas educativas de privatización en Andalucía
    No hay lunes al sol en la Universidad
    Ofrecer comedor gratis en todos los colegios públicos es “alcanzable y urgente”: costaría 1.664 millones al año, según la ONG Educo  
    Una fórmula para que la escuela pública compita mejor con la concertada
    La pérdida de alumnos por el descenso de la natalidad está afectando con más fuerza a la escuela pública que a la concertada
    El Ayuntamiento de Madrid guarda en un cajón una herramienta ya pagada para ver los datos de contaminación al detalle 
    La implantación del nuevo Bachillerato general fracasa pese a su demanda potencial: “Creímos que lo pedirían seis alumnos y lo han hecho 27”
    Toni Solano, director de instituto: “Veo mal a los niños, necesitan muchísima ayuda”
    Niños, Administraciones y redes sociales: prohibir su uso con una mano y enseñar a crear contenidos con la otra
    El Gobierno aprueba el decreto de bachillerato: los alumnos podrán terminar con un suspenso y desembocará en una nueva Selectividad
    La ley del silencio dentro y fuera del aula
    Las universitarias desertan del grado de Matemáticas ahora que tiene pleno empleo. ¿Por qué?
    Golpe a la temporalidad en las universidades: 25.000 profesores asociados serán indefinidos a tiempo parcial
    Antonio Abril: “Yo le decía a Castells: ‘Tienes que aguantar la presión, tienes que hacer la reforma universitaria”
    Los universitarios extranjeros podrán quedarse un año en España automáticamente al terminar la carrera
    La indignación crece sobre las ascuas del incendio en la sierra de la Culebra
    Jardines en los tejados, árboles africanos y calles pintadas de blanco: cómo adaptar la ciudad al calor extremo
    Un continente mortal para los defensores de la tierra
    Drama en la sierra de la Culebra, el paraíso del lobo ibérico que quedó abrasado por un rayo
    Alemania anuncia que recurrirá al carbón ante el recorte de suministro de gas ruso
    La inacción frente al cambio climático hará que sea habitual superar los 40 grados en junio en España
    Ibrahim Thiaw: “Hay que prepararse mejor frente a las sequías, los agricultores franceses están cultivando ya cereales africanos”
    La ola de calor provoca la caída de cientos de crías de vencejo en las calles de Sevilla y Córdoba
    “En Singapur ya se vende carne cultivada para alimentación” 
    Las claves de la ola calor de junio en cinco gráficos
    El consumo mundial de petróleo marcará un nuevo máximo en 2023
    La lección del martín pescador para afrontar la crisis ecológica
    Estocolmo+50: mirar atrás para tomar impulso
    El verano ya no es lo que era 
    Juan Serna, Premio Nacional de Medio Ambiente: un reconocimiento merecido
    Ríos imposibles: las 171.000 barreras que rompen el curso de agua en España
    La UE abraza las renovables para romper la dependencia de Rusia
    La lucha en un pueblo de Teruel para salvar su última montaña
    ¿Qué aire respiran los niños de Madrid y Barcelona? En el 46% de los colegios se supera la contaminación permitida
    Eloísa del Pino sustituye a Rosa Menéndez al frente del CSIC
    Los restos de un cohete chino, visibles desde varios puntos de España al atravesar el cielo
    Así se puede ver la alineación de cinco planetas a simple vista, justo antes de cada amanecer 
    Los humanos, más próximos a la tolerancia de los bonobos que a la belicosidad de los chimpancés
    Escarabajos peloteros: insectos dialogando con el firmamento
    Una piedra hallada en Egipto en 1996 podría ser la primera evidencia en la Tierra de una supernova insólita
    La costa de los gigantes: huellas en el golfo de Cádiz confirman la coexistencia de uros enormes con otra megafauna y neandertales 
    El problema del huerto
    Una población de osos polares descubierta en Groenlandia, genéticamente aislada, no necesita el hielo marino para sobrevivir
    Los premios Fronteras honran a los expertos que cambiaron el mundo enfrentándose a la soledad
    Drew Weissman: “Creemos que en los próximos seis o siete años tendremos una vacuna eficaz contra el VIH”
    La locura como juego; más allá del Quijote y de las novelas de Pérez Galdós
    El mayor estudio de las aberraciones genómicas del cáncer muestra cómo atajar los tumores más letales
    Los dientes de personas enterradas hace 700 años señalan el origen de la peste negra, la mayor pandemia de la historia
    Thomas Halliday: “La vida siempre busca la forma de permanecer, pero la manera en la que lo hace puede cambiar radicalmente”
    Universo o libertad
    Universo o libertad
    Reaparece la tesis de María Wonenburger, la pionera matemática española que permaneció décadas en el olvido
    Técnicas criptográficas que se fundamentan en lo impredecible
    Las matemáticas de los juegos malabares
    Matemáticas para apilar naranjas
    Números McNugget
    La moneda de Frobenius
    D’Alembert y el cálculo de probabilidades
    La locura como juego; más allá del Quijote y de las novelas de Pérez Galdós
    El andar del borracho, las huellas del azar y el juego de dados en algunos libros malditos
    El campo vibratorio y las fronteras de la ciencia desde un punto de vista científico
    Paul Auster fluctuando entre el pudin de pasas y la nube de mosquitos
    Falsas atribuciones, así en la vida como en la ciencia
    ¿Son mejores las hormonas bioidénticas?
    ¿Qué surgió antes, el ARN o el ADN?
    ¿Por qué se sabe que los núcleos de la Tierra rotan?
    ¿Qué son los mini reactores nucleares?
    Invitados indeseables por Navidad: el muérdago y otras plagas que evitar durante las fiestas
    Las ‘apps’ nutricionales o cómo comer bien no debería depender de uno mismo
    Malnutrición invisible: el impacto de la pobreza en la salud infantil
    El óxido de etileno, la sustancia cancerígena que ha obligado a retirar miles de alimentos en la UE
    Que no te líen con los ingredientes: aceites y grasas de mala calidad nutricional
    Valencia estrena el CaixaForum más singular: un paisaje futurista dentro de un edificio icónico
    ‘Gran Sol’: una pequeña gran historia para una madre de siete hijos que espera a un marino rodeado de icebergs
    Un doble asesinato durante la Guerra Civil saca a la luz un monasterio medieval en Zaragoza
    El poeta
    Ese país salvaje llamado España
    Mercedes, mira por nosotros
    Santíguate antes de ponerlo en marcha
    Así suena ‘Break My Soul’, lo nuevo de Beyoncé 
    Arte, admiración, respeto y amor por la música: lo que se puede aprender de la relación de Patti Smith y Bob Dylan
    María Pagés: “A los lugares cercanos se va a seguir yendo, pero a los lejanos… quién va a poder comprar los billetes”
    La tercera vía de Mark Padmore
    Los abonados a las plataformas y televisiones de pago superan el número de hogares españoles 
    Pinocho en tiempos de Mussolini o la guerra entre ositos y unicornios: la animación se entrega a los adultos
    La rabiosa actualidad de Frank Lloyd Wright 
    Muere a los 97 años el arquitecto Jordi Bonet, continuador de las obras de la Sagrada Familia
    Una red de investigadores trata de separar la leyenda de la historia de Tarteso
    El Supremo condena a un festival de música a pagar 20.000 euros por utilizar una fotografía de Germán Coppini en su cartel
    Anarquistas, barricadas y Hollywood: la joven neoyorquina que contó la revolución española
    Victoria Alonso, presidenta de producción de Marvel: “El beso de ‘Lightyear’ es una actualización de la familia, y lo vamos a seguir mostrando”
    Controlado un incendio en las plantas superiores del Alcázar de Toledo
    Un paseo fluvial con museos y otro lleno de piscinas termales. Las sorpresas de la Vía de la Plata
    Una fuente termal en el centro del pueblo y cómo distinguir a los pájaros por su canto. Las sorpresas del Camino Portugués de la Costa
    El Pirineo oscense, para entrar a vivir
    Olite revive el Medievo para asentarse en el futuro
    Toda la lectura del verano, en el bolsillo
    Libros que te volarán la cabeza, recomendados por Litus
    Diez de los mejores libros de relatos jamás escritos
    Asiste al preestreno de 'Mamá no enRedes'
    'Aquí, siempre' en la Sala Cuarta Pared
    Descubre el Museo Picasso Málaga
    Visita la muestra de Juan Muñoz en el Centro Botín
    José Fernando Molina gusta y abre una generosa puerta grande en su presentación en Madrid
    Escaso (y festivo) público
    Muere el torero Andrés Vázquez a los 89 años de edad
    ¿Podría un juez prohibir los toros en España?
    Lo que siento (no se olviden de Ucrania) 
    Elena Ferrante a Elizabeth Strout: “Nosotras, las mujeres, somos Nadie, pero nuestra escritura es muy ambiciosa”
    Nebrija, el humanista que se enfrentó a la Inquisición
    Un tomo inédito de John Fante, la filosofía de Rüdiger Safranski y otros libros de la semana
    Lucy Ellmann: “Los hombres deberían callarse y dejarnos resolver los problemas”
    Wilco contra el mundo cruel: un nuevo disco delicioso, natural, sencillo y sin sorpresas
    La Documenta sí invita a la lógica
    Mercucio salva la función en el ‘Romeu i Julieta’ de David Selvas
    ‘El amor enamorado’: Eros no sabe querer
    Trampantojo: Metatrampantojo
    ‘Hambre’, así se resucita a Arturo Bandini
    Alex sin Ada
    ¡Alerta naranja!
    La guerra y el mestizaje explicados a mi hijo
    El amor por España de J. B. Trend
    ‘Jung y la imaginación alquímica’, máquinas  de imaginar
    ‘Ser único’, singulares del pensamiento
    ‘La novela ideal’, vida de un vampiro nudista
    ‘Economía en Transición’, el precio de ser europeos
    Óscar Esquivias: “No hace falta ser creyente para leer la Biblia”
    Amelia Castilla: “Los ritos nos ayudan a hacer viable el trance de la muerte”
    Shuarma: “Me gusta de la poesía el silencio que encierra”
    Eva Orúe: “Haría cola por la firma de Margaret Atwood”
    Fernando Castro Flórez: “Mortadelo y Filemón’ es uno de mis ‘textos sagrados”
    El COE finiquita la candidatura de los Juegos Olímpicos de Invierno para el 2030 pero mantiene abierta la puerta al 2034
    Operación Conífera: una decena de detenidos por amañar partidos del fútbol modesto para apuestas
    Un viaje de dos meses y medio para escalar la ruta más difícil en Yosemite y fallar en el último movimiento
    Antecedentes confirmados
    El Real Madrid añade más trapío en el éxito
    De lo imposible al cielo
    Un fútbol femenino más profesional
    Dressel se retira del 100 libre del Mundial y emerge el gran Popovici
    Sadio Mané ya es del Bayern
    Así se convenció Ancelotti de que necesitaba a Rüdiger, y así le persuadió de fichar por el Madrid
    La campaña electoral del Athletic se enfanga entre acusaciones de machismo y homofobia
    Niepómniashi castiga la insensatez de Firouzja
    Míchel conquista a Guardiola
    David Ferrer, nuevo director de la Copa Davis
    La reconversión contracultural de Tavares
    Thomas Ceccon corona la revolución italiana con el récord mundial de 100 espalda  
    Bielsa irrumpe en la campaña electoral del Athletic
    Jordi Sargatal: “Cuando tienes a alguien como Marc Gasol, tienes que adaptar tus ideas a él”
    El US Open es también el primer grande de Billy Foster, ‘caddie’ de Seve
    Girona ingresa en la élite deportiva
    Una final que se juega fuera del estadio
    “Nunca acepto un no por respuesta”
    La mayor fábrica de baloncesto de Europa
    Crónica de dos ciudades moldeadas por la misma pasión 
    Honda toca fondo sin Marc Márquez y entra en su peor crisis en 40 años
    Dónde ver la final ACB 2022 entre Barcelona y Real Madrid: fechas y horarios de los partidos
    Rüdiger: “Ancelotti me dijo que me quería y a mi edad eso es suficiente”
    Tadej Pogacar, adelante con su sonrisa hacia su tercer Tour de Francia
    Jon Rahm, de aprender inglés con Eminem a líder en EEUU
    Jesús Rollán y la ruta de aquel Sancheski
    Girona como punto de cita de madridistas 
    Matt Fitzpatrick gana el US Open: la gloria no está en venta
    Mónica Ojeda, pedagoga: “Los adolescentes utilizan sus imágenes sexuales como moneda de cambio o como prueba de amor”
    Zuckerberg desvela cómo serán las gafas para entrar en el metaverso
    Por qué retuitear el vídeo sexual de Santi Millán también es delito: la desprotección de la intimidad en internet
    LaMDA, la máquina que “parecía un niño de siete años”: ¿puede un ordenador tener conciencia?
    La inteligencia artificial reconocerá el arte gracias a la ciencia ciudadana
    “Gano 1.500 euros al mes con los videojuegos”: así funciona el negocio de la compraventa de cuentas
    Cinco aplicaciones móviles, con aval científico, que salvan vidas o mejoran tu salud
    Cómo contarle tus ciclos menstruales a una app puede llevarte a la cárcel
    Bill Gates dice que las criptomonedas y los NFT están basados en encontrar a “alguien más tonto”
    El Princesa de Asturias de Investigación Científica distingue a cuatro expertos en sistemas que imitan al cerebro
    Ha llegado el final de Internet Explorer. Y ahora, ¿qué?
    Crece el número de españoles que evitan las noticias duras como la pandemia o la guerra de Ucrania
    Putin, Messi y otros 500 intereses masculinos: así puede explotarse Facebook, “la mayor base de datos de la cultura humana”
    Resuelta la polémica en los emojis: no habrá más banderas
    El desafío de la tecnología para detener la despoblación rural
    En defensa de la procrastinación. Elogio del tiempo perdido (frente al que las redes te roban)
    Instagram, el mejor de los mundos posibles
    Del terrorismo youtuber al influencer rabioso: el odio inunda la red
    Cronodiversidad. ¿Por qué el tiempo cada vez va más rápido?
    Herramientas que ayudan a crecer a las empresas (más allá de los pagos)
    La solución definitiva para vender más (y mejor) en la web
    Por qué todos hablan de este ‘smartphone’ de diseño atractivo y rendimiento prémium
    Este es el ‘smartphone’ que desafía las leyes del diseño
    Mónica Ojeda, pedagoga: “Los adolescentes utilizan sus imágenes sexuales como moneda de cambio o como prueba de amor”
    Zuckerberg desvela cómo serán las gafas para entrar en el metaverso
    Por qué retuitear el vídeo sexual de Santi Millán también es delito: la desprotección de la intimidad en internet
    LaMDA, la máquina que “parecía un niño de siete años”: ¿puede un ordenador tener conciencia?
    La inteligencia artificial reconocerá el arte gracias a la ciencia ciudadana
    “Gano 1.500 euros al mes con los videojuegos”: así funciona el negocio de la compraventa de cuentas
    Cinco aplicaciones móviles, con aval científico, que salvan vidas o mejoran tu salud
    Cómo contarle tus ciclos menstruales a una app puede llevarte a la cárcel
    Bill Gates dice que las criptomonedas y los NFT están basados en encontrar a “alguien más tonto”
    El Princesa de Asturias de Investigación Científica distingue a cuatro expertos en sistemas que imitan al cerebro
    Ha llegado el final de Internet Explorer. Y ahora, ¿qué?
    Crece el número de españoles que evitan las noticias duras como la pandemia o la guerra de Ucrania
    Putin, Messi y otros 500 intereses masculinos: así puede explotarse Facebook, “la mayor base de datos de la cultura humana”
    Resuelta la polémica en los emojis: no habrá más banderas
    El desafío de la tecnología para detener la despoblación rural
    En defensa de la procrastinación. Elogio del tiempo perdido (frente al que las redes te roban)
    Instagram, el mejor de los mundos posibles
    Del terrorismo youtuber al influencer rabioso: el odio inunda la red
    Cronodiversidad. ¿Por qué el tiempo cada vez va más rápido?
    Herramientas que ayudan a crecer a las empresas (más allá de los pagos)
    La solución definitiva para vender más (y mejor) en la web
    Por qué todos hablan de este ‘smartphone’ de diseño atractivo y rendimiento prémium
    Este es el ‘smartphone’ que desafía las leyes del diseño
    Guillermo de Inglaterra cumple 40 años como el candidato ideal para seguir la estela de Isabel II
    Shaquille O’Neal, el rey de las franquicias: 155 hamburgueserías, 40 gimnasios y una fortuna de 400 millones
    La hija transgénero de Elon Musk quiere borrarse el apellido para romper los lazos con su padre
    Los 40 años de Guillermo de Inglaterra en 16 fotos
    Rosa Olucha, mujer de Santi Millán, sobre el vídeo filtrado: “Me da mucha pereza ver que el sexo consentido y privado siga causando escándalos”
    Mariano Alameda: “Tardé años en librarme de Íñigo”
    La moda masculina toma en Milán las riendas de su propio ‘revival’
    Camila de Cornualles posa y habla para celebrar su 75º cumpleaños: “Fui examinada durante tanto tiempo que tuve que aprender a vivir con eso”
    Nicky y Simone Zimmermann: “Nos dijeron que no nos dedicáramos a la moda y que no trabajáramos en familia. No les hicimos caso y nos fue bien”
    Daniela Requena: “Mi vaginoplastia se puede ver en YouTube, hay que tratar este tema con naturalidad”
    Ana Mena: “Tengo muchas ganas de colaborar con más chicas, pero necesito canciones que sean apropiadas para ello”
    Querido papá: así felicitan los famosos el Día del Padre en sus redes sociales
    Cumbre de futuras reinas (sin Leonor) por el 18º cumpleaños de Ingrid de Noruega
    Desembarco de celebridades internacionales en Sevilla para el desfile de Dior
    Kim Kardashian causó graves daños al histórico vestido de Marilyn Monroe que llevó en la gala del Met
    Mi extraña nostalgia por Abercrombie & Fitch & lo que fuimos
    Bikôkô y Julio Peña, dos estrellas en ebullición  
    Cuando Chufy encontró a Rossy: dos amigas, una isla y una colección de moda
    La evolución de los modales al comer en la mesa
    Ibiza, entre la noche desenfrenada y el turismo tranquilo 
    Los 33, el nuevo local de tapeo a la brasa con esencia uruguaya en Madrid
    Iñigo Urrechu, cocinero: “Tienes que hacer una cocina instagrameable porque todo el mundo saca pecho de comer en un sitio bonito”
    ‘Sanditon’ resucita a Jane Austen
    Ciencia, tecnología y entrevistas en las novedades de la programación de verano en la Cadena SER
    Los abonados a las plataformas y televisiones de pago superan el número de hogares españoles 
    ‘Intimidad’, protagonizada por Santi Millán
    En el nombre de Rociito
    El escote de Schrodinger
    A la playa
    ‘Intimidad’, protagonizada por Santi Millán
    La historia de Warren Jeffs, un profeta tirano, violador y líder mormón
    ‘Pasapalabra’ busca a su próxima gran estrella
    Mueren en un accidente de tráfico dos actores mexicanos durante el rodaje de la serie de Netflix ‘El Elegido’  
    La nueva ley audiovisual abre la veda a la contraprogramación y la saturación publicitaria en la televisión
    Ucrania no acogerá Eurovisión 2023 y la UER ya se lo ha ofrecido a Reino Unido 
    HBO ata a Kit Harington para una posible secuela de ‘Juego de tronos’ centrada en Jon Nieve
    ‘Intimidad’, violadores y mucho más
    Una versión cantada del ‘true crime’ castizo
    Netflix prepara un concurso basado en ‘El juego del calamar’ con el mayor premio económico en la historia de la televisión
    ¿Qué ver hoy en TV? Martes 21 de junio de 2022
    Nueve capítulos para recordar ‘The Wire’ en su 20º aniversario
    Harry Palmer: el tercer vértice del mágico triángulo de espías británicos
    Las series de junio de 2022: ‘The Boys’ en Amazon Prime Video; ‘Peaky Blinders’ en Netflix y otras
    La fuerza acompaña a ‘Obi-Wan Kenobi’, una serie deslumbrante
    Viaje al fin de Occidente, en la gran frontera entre Finlandia y Rusia
    Viktor & Rolf, 30 años de moda y rebelión: “No puedes estar siempre arriba”
    Maggie O’Farrell: “Es fundamental escribir sobre cosas que duelen para que nos sintamos menos solos”
    Hola, desconocido, cuéntanos tu vida
    Ahorro y otras ventajas de las compras de kilómetro cero
    Proyectos sociales de inclusión y empleo para que nadie se quede atrás
    El refugio campestre de dos arquitectos en el valle de Arán
    Epidemia de violencia: claves del negocio de las armas en Estados Unidos
    Jorge Drexler: “Fui un ejemplo de fracaso en la industria discográfica durante mucho tiempo”
    La Noche de San Juan y cómo quemar la mochila de trastos y malos hábitos que cargamos
    La evolución de los modales al comer en la mesa
    Rashid Johnson: “Los pensadores y creadores negros estamos cansados de que nos nieguen un espacio autónomo”
    Ibiza, entre la noche desenfrenada y el turismo tranquilo 
    La palabra épica
    ‘Influencers’
    Cuento del profesor Pírfano 5
    Harina enriquecida para acabar con el “hambre oculta”
    Lugares de esperanza para salvar los océanos
    Hola, desconocido, cuéntanos tu vida
    Los ejecutivos voladores y la ética medioambiental
    Yaiza Rubio: “Internet ha traído nuevos y muy preocupantes modos de espionaje”
    Los ucranios ya tienen casa en París
    Tenemos que hablar de la alopecia (Jada Pinkett estaría de acuerdo)
    Néstor Pablo Roldán, el ceramista de ‘Los herederos de la tierra’
    Las manos maestras del Palacio Real
    Sergio Hernández: “En el mundo, la gente ya no quiere verdades, quiere mentiras”
    El café de los abuelos o, simplemente, el lugar donde comer las mejores tartas de Viena
    Riesgo, dolor y placer: cómo los humanos se aficionaron al picante 
    Cómo es la vida en un apartamento del siglo XXI... dentro de un palacio decimonónico
    La nueva edad de oro de la coctelería en Barcelona
    Los cinco coches eléctricos más baratos del mercado
    Ilusiones hipnóticas
    El poder del hormigón
    Maulévrier, Japón a la francesa
    ‘Fantasías en el Prado’, por Alberto García-Alix
    ¡‘Yee-haw’! Esto también es Brasil
    

#### Clear
Empleamos `os.system(clear)` para que después de realizarse el *Web Scrapping* se limpie la pantalla de Python. Para utilizarlo con Jupyter y otros sistemas es necesario emplear `!cls`.


```python
!cls
```

    
    

Si pasamos la función `type()` para `os.system` podemos observar que este objeto es de tipo *función o método integrado*, igual que lo era `resultados.append`.


```python
type(os.system)
```




    builtin_function_or_method



#### Print y str_match
Imprimimos una cadena de carácteres coloreándola de <span style="color:blue">azul</span> y con su texto en **negrita**. Esta cadena actuará como explicación del contenido que mostrarán los resultados obtenidos en Python.


```python
print(colored("A continuación se muestran los titulares de las páginas principales del diario El País que contienen las siguientes palabras:", 'blue', attrs=['bold']))
```

    [1m[34mA continuación se muestran los titulares de las páginas principales del diario El País que contienen las siguientes palabras:[0m
    

Posteriormente imprimimos el título del contenido, que posteriormente se seleccionará. En un primer caso sería la palabra *Feminismo* en color <span style="color:green">verde</span> y también en **negrita**. Estos elementos actuarán como subtítulos identificativos para los resultados que se obtendrán posteriormente en Python.


```python
print(colored("Feminismo", 'green', attrs=['bold']))
```

    [1m[32mFeminismo[0m
    

Si pasamos la función `type()` para `print` podemos observar que este objeto es de tipo *función o método integrado*, igual que lo eran `resultados.append` y `os.system`.


```python
type(print)
```




    builtin_function_or_method



Se emplea una variable de búsqueda de cadena para que identifique los resultados que contengan una palabra determinada. En este primer caso la palabra buscada dentro de los resultados que se han añadido anteriormente a la lista sería "feminismo". 

En este caso se imprimirán todos los resultados que contengan esta palabra.


```python
str_match = [s for s in resultados if "feminismo" in s]
print("\n".join(str_match))
```

    
    

Si pasamos la función `type()` para `str_match` podemos observar que este objeto es de tipo *lista* igual que lo era al inicio `resultados = []`.


```python
type(str_match)
```




    list



Se repite de nuevo lo mismo para las palabras: igualdad, mujeres, mujer, brecha salarial, machismo, violencia, maltrato, homicidio, género, asesinato y sexo.


```python
print(colored("Igualdad", 'green', attrs=['bold']))

str_match = [s for s in resultados if "igualdad" in s]
print("\n".join(str_match))

print(colored("Mujeres", 'green', attrs=['bold']))

str_match = [s for s in resultados if "mujeres" in s]
print("\n".join(str_match))

print(colored("Mujer", 'green', attrs=['bold']))

str_match = [s for s in resultados if "mujer" in s]
print("\n".join(str_match))

print(colored("Brecha salarial", 'green', attrs=['bold']))

str_match = [s for s in resultados if "brecha salarial" in s]
print("\n".join(str_match))

print(colored("Machismo", 'green', attrs=['bold']))

str_match = [s for s in resultados if "machismo" in s]
print("\n".join(str_match))

print(colored("Violencia", 'green', attrs=['bold']))

str_match = [s for s in resultados if "violencia" in s]
print("\n".join(str_match))

print(colored("Maltrato", 'green', attrs=['bold']))

str_match = [s for s in resultados if "maltrato" in s]
print("\n".join(str_match))

print(colored("Homicidio", 'green', attrs=['bold']))

str_match = [s for s in resultados if "homicidio" in s]
print("\n".join(str_match))

print(colored("Género", 'green', attrs=['bold']))

str_match = [s for s in resultados if "género" in s]
print("\n".join(str_match))

print(colored("Asesinato", 'green', attrs=['bold']))

str_match = [s for s in resultados if "asesinato" in s]
print("\n".join(str_match))

print(colored("Sexo", 'green', attrs=['bold']))

str_match = [s for s in resultados if "sexo" in s]
print("\n".join(str_match))
```

    [1m[32mIgualdad[0m
    La escuela concertada ante las desigualdades: el debate pendiente
    [1m[32mMujeres[0m
    Elena Ferrante a Elizabeth Strout: “Nosotras, las mujeres, somos Nadie, pero nuestra escritura es muy ambiciosa”
    Elena Ferrante a Elizabeth Strout: “Nosotras, las mujeres, somos Nadie, pero nuestra escritura es muy ambiciosa”
    [1m[32mMujer[0m
    Rosa Olucha, mujer de Santi Millán: “Me da pereza ver que el sexo consentido siga escandalizando”
    Elena Ferrante a Elizabeth Strout: “Nosotras, las mujeres, somos Nadie, pero nuestra escritura es muy ambiciosa”
    Seis chanclas de los años ochenta para hombre y mujer que son ahora tendencia
    ¿La democracia es una sola mujer trabajadora en la Asamblea de Francia?
    El director Paul Haggis, detenido en Italia acusado de abusar sexualmente durante dos días de una mujer
    Elena Ferrante a Elizabeth Strout: “Nosotras, las mujeres, somos Nadie, pero nuestra escritura es muy ambiciosa”
    Rosa Olucha, mujer de Santi Millán, sobre el vídeo filtrado: “Me da mucha pereza ver que el sexo consentido y privado siga causando escándalos”
    [1m[32mBrecha salarial[0m
    
    [1m[32mMachismo[0m
    La campaña electoral del Athletic se enfanga entre acusaciones de machismo y homofobia
    La campaña electoral del Athletic se enfanga entre acusaciones de machismo y homofobia
    [1m[32mViolencia[0m
    Ventanilla única para las víctimas de la violencia machista: una atención pionera, integral, con ayuda emocional  
    Ventanilla única para las víctimas de la violencia machista: una atención pionera, integral, con ayuda emocional  
    Epidemia de violencia: claves del negocio de las armas en Estados Unidos
    [1m[32mMaltrato[0m
    
    [1m[32mHomicidio[0m
    
    [1m[32mGénero[0m
    La hija transgénero de Elon Musk quiere borrarse el apellido para romper los lazos con su padre
    La hija transgénero de Elon Musk quiere borrarse el apellido para romper los lazos con su padre
    [1m[32mAsesinato[0m
    Un doble asesinato durante la Guerra Civil saca a la luz un monasterio medieval en Zaragoza
    Un doble asesinato durante la Guerra Civil saca a la luz un monasterio medieval en Zaragoza
    [1m[32mSexo[0m
    Rosa Olucha, mujer de Santi Millán: “Me da pereza ver que el sexo consentido siga escandalizando”
    Rosa Olucha, mujer de Santi Millán, sobre el vídeo filtrado: “Me da mucha pereza ver que el sexo consentido y privado siga causando escándalos”
    

## FIN 
Aquí finaliza el código de la actividad. Cómo se ha podido ver durante el texto previo, consistía en un código de *Web Scrapping*, que recolectaba todos los titulares de las distintas secciones de la página *web* del periódico **El País** y de esos titulares seleccionaba los que correspondían con determinadas palabras relacionadas con violencia de género, pudiendo, de este modo, tener un vistazo general de lo ocurrido al respecto en el momento del *scrappeo*.

Este código podría mejorarse eliminando las librerías que finalmente no se han empleado, ya que no tiene sentido instalar e importar librerías que finalmente no tienen uso, por ejemplo, `time` y `csv`; así como acortando código realizando una *lista* con las **URLs** y luego recorriéndolas a través de un **bucle** con el fin de aplicar el mismo código solo una vez, sin repeticiones.
