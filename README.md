# Actividad 4 Teoria de la computacion. Laboratorio en AWS o su Notebook elegido

Hecho Por: Santiago Chacon Serrano

## Introduccion

Este trabajo sera realizado en el laboratorio de AWS, el cual sobra decir, es un entorno limitante, pero lo que debemos saber es que el pilar de este proyecto es Amazon SageMaker, un entorno usado para crear y entrenar modelos de Machine Learning (ML), el entorno en si mismo tiene dos facetas, la codificacion por medio de Python y los bloques de MarkDown el cual es un formato sumamente parecido a los HTML, pero que a diferencia de ellos son mucho mas limitados para asi ser a su vez mucho mas simples de usar.

Con lo basico propuesto, nos moveremos ahora por los ejercicios.

## Laboratorio 3.1 - Amazon SageMaker - Creacion e importacion de datos

El primer ejercicio es sencillo, solo crearemos el... "entorno de trabajo" o el NoteBook mejor dicho, crearemos el notebook con las indicaciones solicitadas, un incapie principal que en el texto de la guia, hay un error de traduccion que pide que la instancia sea ml.m4.xlarge, cuando en el idioma original se solicita es ml.m5.xlarge, pero dejando eso de lado, AWS comenzara a cargar el entorno, un proceso de unos pocos minutos, una vez se complete, se habilitaran los botones "Open_Jupiter" y "Open_JupiterLab", el que nos compete es este ultimo.

Al presionar dicho boton se nos abrira una nueva ventana del entorno de markdown de AWS, una vez dentro seleccionaremos el idioma original para evitar mas errores como paso antes, dentro de esa carpeta tendremos ya dos archivos de markdown, mas para est trabajo realmente no tenemos que hacer casi nada, las instrucciones nos solicitan es familiarizarnos al entorno, usar el codigo, crear bloques, crear markdown, hacer un nuevo notebook, codigo, duplicar archivos, lo basico, pero una cosa, uno de los archivos, el de linear, utiliza funciones de E3 NO brindadas por el ejercicio, por lo tanto su contenido es practicamente inservible y solo funciona de guia,  ademas de eso, en el nuevo notebook llamaremos de internet datasets con los que crearemos una tabla, todo incluido en el archivo de Tarea 1.

## Laboratorio 3.2 - Amazon SageMaker - Exploracion de Datos

Para la segunda tarea, tenemos las instrucciones dentro del notebook, una cosa importante a recalcar es que el codigo no me sirvio, utiliza librerias NO instaladas y por ello me vi en la necesidad de descarcar librerias por medio del codigo "!pip install", algo recurrente que veran de aqui en adelante, de todas formas, instalaremos un nuevo dataser con el cual trabajaremos por el resto de este ejercicio.

Como primer ejercicio nos piden ver las estadisticas de datos que queramos por medio del "df[' '].describe(), en mi caso elejgi el de "pelvic_tilt" y "degree_spondylolisthesis".

Luego de eso tras mostrarnos una tabla con los datos del dataset nos solicitan desglosar la informacion y asi responder ciertas preguntas.

### Hay alguna categoria la cual no este bien distribuida?

Si, el de "degree_spondylolisthesis" tiene varios detalles anormales, el principal siendo que sus valores maximos son absurdamente altos, algo que suena un poco confuso en un inicio, mas si tomamos los datos como P75 = 41.287 y el P100 = 418.543, el valor deja de cobrar sentido.

### Hay valores atipicos?

Realmente el de "degree_spondylolisthesis" tambien entraria aqui, pero como ya lo mencione lo omitire y en vez tomare otros dos datos, el de "pelvic_incidence", "sacral_slope" y el de "lumbar_lordosis_angle" el cual tienen los mismos problemas de valores desproporcionados pero cuyos casos son menos extremos.

### Hay alguna correlacion entre las categorias?

Esta pregunta fue algo compleja en su propio sentido pues era dificil saber con los datos que poseia ahi, mas termine optando por lo que la tabla me ofrecia y con ello vi que los datos de "lumbar_lordosis_angle" y "pelvic_radius" eran bastante similares.

## Matplotlib

Tras eso el laboratorio me solicito crear graficas de ese mismo dataset usando Matplolib, el cual evidentemente tambien tuve que instalar de forma aparte, ahora las graficas son de todo tibo, de barras, calor, bigote y demas.

### Ejercicio Final

Ademas de eso, como ejercicio final se me pidio crear otra vez esas graficas pero con un nuevo dataset, aqui me decante por importar el de iris por la poca cantidad de datos que posee, esto permitio que fuera mucho mas facil de manejar y a su vez mucho mas ligero.

## Laboratorio 3.3 - Amazon SageMaker - Codificacion de Datos Categoricos

Para este ejercicio nuevamente tenemos un nuevo NoteBook con las instrucciones, mas a su vez tambien se nos da un archivo de excel/tablas, el cual sera el dataset que se usara para esta actividad.

## Encode
Este dataset es gigantesco, tiene 25 tipos de datos, datos de automoviles para ser mas exactos, aqui nos van a mostrar como organizar tablas para interactuar con el modelo de machine learning, o mejor dicho, como preparar los datos para entrenarlo, primero que todo debemos recordar algo, los modelos de machine learning NO funcionan por medio de strings, funcionan por medio de ints de los cuales determinan mayor o menor, esta informacion no suena importante en un principio, pero que pasaria si de pronto tenemos archivos que complican esto? bueno, estos serian datos de los cuales no haya un mayor o un menor en si mismo, por ejemplo el numero de puertas, digamos que tenemos dos autos de 4 puertas y luego dos de dos puertas, si ponemos esos datos como int, el modelo predecira que el proximo auto sera de 3 puertas... algo ilogico en todo sentido, para resolver esto tenemos los metodos booleanos o mejor dicho... el encode, los cuales podemos hacer un drop first y tomar en cuenta uno de estos datos, seria tipo "El auto es de dos puertas?" y la respuesta seria True o false, de esta forma si hay muchos trues el modelo puede predecir de forma mas segura que el auto sera de dos puertas, caso opuesto para que sea de 4, esto se puede aplicar a mas de dos datos, mas tocaria hacer un boolean para cada tipo de dato posible.

### Ejercicio Final

Para este ejercicio final nos pedian crear una nueva tabla teniendo en cuenta datos que no se tomaron en cuenta antes y encodearlos.

Para resolver esto primero debiamos hacer que el programa releyera todos los datos, pues al ir avanzando el ejercicio los datos se dejaron de tomar en cuenta y se "borraron" o mejor dicho, dejaron de ser tenidos en cuenta, una vez esto se hizo decidi agregar los siguientes datos "fuel-type" y "body-style", los cuales tienen la misma necesidad del encode anterior, un dato que posee dos datos que no poseen mayor o menor (el tipo de combustible) y el segundo lo mismo pero con muchos mas datos a tomar en cuenta, unos 5 datos para ser exactos, una vez se hizo eso se realizo la tabla y se culmino el ejercicio.
## Evidencias

Las evidencias es un archivo de word con todas las imagenes del ejercicio, para que mentir, este ejercicio me costo bastante, principalmente el proceso entre github y markdown, nunca lo habia hecho de esta forma y ha decir verdad aun no me siento seguro de haberlo realizado correctamente del todo, sin embargo, siento felicidad de haberlo completado y espero con ansias el resultado para asi tomarlo en cuenta en futuros ejercicios.
