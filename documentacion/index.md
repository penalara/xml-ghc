### Índice general

*   [Página de inicio.](#índice-general)
*   [Índice completo.](#Indice)
*   [XML básico.](#xml-básico)
*   [XML Avanzado.](#xml-avanzado)
*   [Información básica sobre el XML.](#información-básica-sobre-el-xml)
*   [Documentación adicional](#documentación-adicional).

Manual de XML GHC
=================

Este documento mostrará como crear y utilizar el formato de intercambio utilizado por GHC (Generador de Horarios para Centros).

Para saber más sobre uno de los elementos pinche sobre él, o abra la página [elementos.md](elementos.md "Definición de elementos") y busque el elemento deseado.

Índice completo
---------------

*   [Página de inicio.](#índice-general)
*   [Índice.](#índice-completo)
*   [XML básico](#xml-básico):
    *   [Primer paso, la cabecera](#primer-paso-la-cabecera.).
    *   [Segundo paso, la estructura general](#segundo-paso-la-estructura-general).
    *   [Tercer paso, los datos básicos](#tercer-paso-los-datos-básicos):
        *   [Definir los marcos](#definir-los-marcos).
        *   [Declaramos las aulas que tiene el centro](#declaramos-las-aulas-que-tiene-el-centro).
        *   [Declaramos los tipos de tareas disponibles](#declaramos-los-tipos-de-tareas-disponibles).
        *   [Declaramos los profesores](#declaramos-los-profesores).
        *   [Declarando las materias](#declarando-las-materias).
        *   [Declarando los grupos](#declarando-los-grupos).
    *   [Cuarto paso, las sesiones básicas](#cuarto-paso-las-sesiones-básicas).
        *   [Materia que se imparte](#materia-que-se-imparte).
        *   [Grupo al que se imparte](#grupo-al-que-se-imparte).
        *   [Profesor que la imparte](#profesor-que-la-imparte).
        *   [Distribución de la sesión](#distribución-de-la-sesión).
        *   [Lista de aulas de la sesión](#lista-de-aulas-de-la-sesión).
        *   [Aulas alternativas de la sesión](#aulas-alternativas-de-la-sesión).
        *   [Tarea de la sesión](#tarea-de-la-sesión).
        *   [Departamento de la sesión](#departamento-de-la-sesión).
        *   [Opciones de la sesión](#opciones-de-la-sesión).
        *   [Plantilla de la sesión](#plantilla-de-la-sesión).
    *   [Ejemplo de la sesión básica](#ejemplo-de-la-sesión-básica).
*   [XML Avanzado](#xml-avanzado):
    *   [Agregados a la sesión](#agregados-a-la-sesión).
    *   [Relaciones entre las sesiones](#relaciones-en-las-sesiones).
    *   [Las listas de relación](#las-listas-de-relación-de-sesiones).
    *   [Relaciones materia-curso](#relaciones-materia-curso).
    *   [Reuniones](#reuniones).
    *   [Guardias](#guardias).
    *   [Complementarias](#complementarias).
    *   [Criterios](#criterios).
*   [Los tipos de distribución de las sesiones](#los-tipos-de-distribución-de-las-sesiones):
    *   [La distribución fija](#la-distribución-fija).
    *   [La distribución personalizada](#la-distribución-personalizada).
    *   [La distribución variable](#la-distribución-variable).
*   [Información básica sobre el XML](#información-básica-sobre-el-xml).
    *   [Contenido de los elementos](#contenido-de-los-elementos).
    *   [Tipos de valores](#tipos-de-los-valores).
    *   [Más información sobre XML](#más-información-sobre-xml).
*   [Documentación adicional](#documentación-adicional).


XML básico
----------

En esta sección se va a definir y mostrar la definición básica del archivo que permite la generación de un horario válido.

### Primer paso, la cabecera.

Lo primero que debe contener el xml es la cabecera de declaración propia de todo documento xml. Esta declaración es `<?xml version="1.0"?>` esta indica que el archivo corresponde con el formato xml en su versión 1.0.

A continuación de este elemento se declara el elemento raíz, que contendrá el resto de elementos.

`<datosGHC xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="./GHCFile.xsd">`

El atributo `xsi:noNamespaceSchemaLocation` es el que indica la localización del esquema que define la estructura del `xml` . En este caso el archivo de esquema `GHCFile.xsd` se localizaría en la misma carpeta del archivo de intercambio (el xml).

El elemento [<datosGHC>](elementos.md#datosGHC) , como todos los elementos de un xml, necesitan ser cerrados. Para ello hay que usar el cierre del elemento mediante la etiqueta `</datosGHC>` después de los elementos que contenga. En este caso no se puede cerrar con la forma corta ( `<datosGHC />` ) ya que debe contener otros elementos.

### Segundo paso, la estructura general.

Lo siguiente son los elementos que componen los datos en sí.

Dentro del elemento [<datosGHC>](elementos.md#datosGHC) , se tienen que colocar en orden los siguientes elementos como mínimo:

*   [version](elementos.md#version). Es la versión del archivo de intercambio.
*   [marcosDeHorario](elementos.md#marcosDeHorario). Define los marcos y tramos horarios disponibles.
*   [conjuntoDeAulas](elementos.md#conjuntoDeAulas). Declara los conjuntos de aulas y las aulas anónimas.
*   [tareas](elementos.md#tareas). Declara los tipos de tareas disponibles, lectivas, reuniones, etc.
*   [profesores](elementos.md#profesores). Declara los profesores que están disponibles y sus preferencias.
*   [materias](elementos.md#materias). Declara las distintas materias que se tienen que impartir.
*   [grupos](elementos.md#grupos). Declara los grupos a los que se impartirán las materias.
*   [sesionesLectivas](elementos.md#sesionesLectivas). Define las sesiones, es decir las clases en sí. Agrupan una materia, un profesor y un grupo, además de otras opciones.

Estos elementos son los mínimos para hacer un horario, pero no son los únicos que se pueden poner, para ver una lista completa de sus elementos consulte su definición en [<datosGHC>](elementos.md#datosGHC) .

Con lo que tendríamos por ahora el siguiente código (sin el contenido de los elementos):

				`<?xml version="1.0"?>   <datosGHC xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"    xsi:noNamespaceSchemaLocation="./GHCFile.xsd">   	<version>20160705</version>   	<marcosDeHorario>...</marcosDeHorario>   	<conjuntoDeAulas>...</conjuntoDeAulas>   	<tareas>...</tareas>   	<profesores>...</profesores>   	<materias>...</materias>   	<grupos>...</grupos>   	<sesionesLectivas>...</sesionesLectivas>   </datosGHC>`
			

Como se puede observar en el código, el elemento [`<version>`](elementos.md#version) siempre tiene el mismo contenido, `20160705` este sirve para identificar que es un archivo de intercambio de la versión 20160705. Este valor debe ser el del formato del xml, pero al leerlo, las aplicaciones pueden aceptar diferentes rangos de valores con los que sea compatibles.

**Nota:** En el xml, el orden de los diferentes tipos de elementos es significativo. No se pueden desordenarar, y los que pueden tener varias copias, no se pueden mezclar.

### Tercer paso, los datos básicos.

En esta sección definiremos los contenidos de los elementos mínimos para hacer un horario, sin tener en cuenta el de [`<version>`](elementos.md#version) que se vio antes y el de [`<sesionesLectivas>`](elementos.md#sesionesLectivas) que se verá en la siguiente sección.

#### Definir los marcos

El segundo elemento (ya que el primero es el de [`<version>`](elementos.md#version)) que tiene que tener es el del [<marcosDeHorario>](elementos.md#marcosDeHorario) . Este definirá la forma del marco horario, es decir las horas de entrada y salida de los tramos, los recreos, parada al medio día o si hay varios marcos.

Para ello este elemento se tiene que rellenar con los elementos [<marcoHorario>](elementos.md#marcoHorario) que definen un marco. Hay que poner uno por cada marco solapado que haya o solo uno si no hay solapamientos. Como mínimo debe haber uno, y como máximo 4 (aunque en un futuro se soportará poner más).

Este elemento ( [<marcoHorario>](elementos.md#marcoHorario) ) tiene el atributo `id` que es el que identifica al marco. El atributo `id` es del tipo estandar [NCName](#NCName) y para su uso en GHC debe ser `A`, `B`, `C` o `D`. También contiene el atributo `nombre` , que es del tipo estadar [string](#string), y aunque opcional, es conveniente ponerlo para identificar el marco de forma más clara para el usuario.

El contenido del marco es un conjunto de tramos (elementos `<tramo>` ) que definen cada uno de los momentos en que se pueden colocar las sesiones y demás tareas. En el elemento tramo hay que definir los elementos `<submarco>` , `<dia>` , `<indice>` , `<horaEntrada>` , `<horaSalida>` , `<tipo>` . También hay un elemento `<clavX>` que es opcional, aunque para algunas aplicaciones es necesario, ya que es con lo que identifican el tramo.

El elemento `<submarco>` es el `id` del marco que lo contiene. Es una información redundante que se ha puesto para mejorar la eficiencia y para verificación.

El elemento `<dia>` es el día de la semana al que corresponde el tramo. Los días de la semana son del 0 (lunes) al 4 (viernes).

El elemento `<indice>` es el identificador del tramo en el día y marco al que pertenece. Es un valor [entero no negativo](#nonNegativeInteger) (mayor o igual que 0). Deberían ser consecutivos y que corresponda con el orden temporal de los tramos.

Los elementos `<horaEntrada>` y `<horaSalida>` indican la hora de entrada y la hora de salida respectivamente. Su valor es del tipo estandar [time](#time) (una hora especificada como `hh:mm:ss.ss` ).

El elemento `<tipo>` indica que función se lleva a cabo en el tramo. Puede tener los valores: `lectivo` , `recreo` o `mediodia` . Que indican, respectivamente, que es un tramo en el que se colocan sesiones, un recreo o una parada de mediodia. Mientras que de `lectivo` y `recreo` puede haber un número indeterminado, solo puede haber un tramo del tipo `mediodia` .

Por ejemplo un marco en el que se da clase de lunes y miércoles, de 9 a 9:50, de 10 a 10:50, un recreo de 20 minutos, y otros dos tramos de 50 minutos, sería:

```
<marcoHorario id="A">
	<tramo>
		<submarco>A</submarco>
		<dia>0</dia>
		<indice>0</indice>
		<horaEntrada>09:00:00</horaEntrada>
		<horaSalida>09:50:00</horaSalida>
		<tipo>lectivo</tipo>
	</tramo>
	<tramo>
		<submarco>A</submarco>
		<dia>0</dia>
		<indice>1</indice>
		<horaEntrada>10:00:00</horaEntrada>
		<horaSalida>10:50:00</horaSalida>
		<tipo>lectivo</tipo>
	</tramo>
	<tramo>
		<submarco>A</submarco>
		<dia>0</dia>
		<indice>2</indice>
		<horaEntrada>10:50:00</horaEntrada>
		<horaSalida>11:10:00</horaSalida>
		<tipo>recreo</tipo>
	</tramo>
	<tramo>
		<submarco>A</submarco>
		<dia>0</dia>
		<indice>3</indice>
		<horaEntrada>11:10:00</horaEntrada>
		<horaSalida>12:00:00</horaSalida>
		<tipo>lectivo</tipo>
	</tramo>
	<tramo>
		<submarco>A</submarco>
		<dia>0</dia>
		<indice>4</indice>
		<horaEntrada>12:10:00</horaEntrada>
		<horaSalida>13:00:00</horaSalida>
		<tipo>lectivo</tipo>
	</tramo>
	<tramo>
		<submarco>A</submarco>
		<dia>2</dia>
		<indice>0</indice>
		<horaEntrada>09:00:00</horaEntrada>
		<horaSalida>09:50:00</horaSalida>
		<tipo>lectivo</tipo>
	</tramo>
	<tramo>
		<submarco>A</submarco>
		<dia>2</dia>
		<indice>1</indice>
		<horaEntrada>10:00:00</horaEntrada>
		<horaSalida>10:50:00</horaSalida>
		<tipo>lectivo</tipo>
	</tramo>
	<tramo>
		<submarco>A</submarco>
		<dia>2</dia>
		<indice>2</indice>
		<horaEntrada>10:50:00</horaEntrada>
		<horaSalida>11:10:00</horaSalida>
		<tipo>recreo</tipo>
	</tramo>
	<tramo>
		<submarco>A</submarco>
		<dia>2</dia>
		<indice>3</indice>
		<horaEntrada>11:10:00</horaEntrada>
		<horaSalida>12:00:00</horaSalida>
		<tipo>lectivo</tipo>
	</tramo>
	<tramo>
		<submarco>A</submarco>
		<dia>2</dia>
		<indice>4</indice>
		<horaEntrada>12:10:00</horaEntrada>
		<horaSalida>13:00:00</horaSalida>
		<tipo>lectivo</tipo>
	</tramo>
</marcoHorario>
```

#### Declaramos las aulas que tiene el centro

El siguiente elemento sería la lista de aulas con nombre (no anónimas). Pero esta no es obligatoria a no ser que se necesite usarla. Para más información mira la documentación del elemento de la [lista de aulas](elementos.md#aulas).

Tras la lista de aulas, viene la lista de conjuntos de aulas. El mínimo posible para hacer un horario es el conjunto de aulas generales. El cual declara la cantidad de aulas sin nombre para uso general.

Esto se realiza de la siguiente manera:

```
<conjuntoDeAulas>
	<general nombre="general" sinDeclarar="5" />
</conjuntoDeAulas>
```

El elemento [<conjuntoDeAulas>](elementos.md#conjuntoDeAulas) debe contener como primer elemento el [<general>](elementos.md#general) y a continuación tantos elementos [<otroConjunto>](elementos.md#otroConjunto) como necesites.

Por ahora nos vale con declarar cuantas aulas generales hay en el centro, esto se hace mediante el atributo `sinDeclarar` , que es del tipo [nonNegativeInteger](#nonNegativeInteger) (entero mayor o igual que 0). Dado que no vamos a añadir aulas con nombre ni de otro conjunto, debe ser mayor que 0, de otra manera no habría aulas donde colocar las sesiones. En este caso hay 5 aulas de tipo general. El atributo `nombre` siempre tiene el valor `general` (aunque puede cambiar para otros conjuntos) y aunque es opcional ponerlo, es aconsejable ponerlo por legibilidad.

#### Declaramos los tipos de tareas disponibles

El siguente elemento es la [lista de tareas](elementos.md#tareas), la cual define que se hace en las diferentes sesiones. Por ejemplo puede haber tutorías, guardias, y por supuesto tipo lectivas.

La lista de tareas viene definida por el elemento [`<tareas>`](elementos.md#tareas) en cuyo interior se declaran 1 o más tipos de tareas mediante elementos [<tarea>](elementos.md#tarea) consecutivos.

Después de los elementos [<tarea>](elementos.md#tarea) se deben declarar 3 elementos más:

*   `<lectivaPorDefecto>`. Contiene el nombre de la tarea que por defecto se usará para las sesiones lectivas.
*   `<guardiaPorDefecto>`. Contiene el nombre de la tarea que por defecto se usará para las guardias.
*   `<reunionPorDefecto>`. Contiene el nombre de la tarea que por defecto se usará para las reuniones.

Así un ejemplo en el que se declaran las 3 tareas básicas por defecto sería:

```
<tareas>
	<tarea>
		<nombre>LEC</nombre>
		<nombreCompleto>Docencia directa con el grupo de alumnos.</nombreCompleto>
		<claveDeExportacion>LEC</claveDeExportacion>
		<plantilla>
			<tramo marco="A" dia="0" indice="0">preferentementeNo1</tramoConPreferencia>
		</plantilla>
	</tarea>
	<tarea>
		<nombre>G</nombre>
	</tarea>
	<tarea>
		<nombre>RDP</nombre>
	</tarea>
	<lectivaPorDefecto>LEC</lectivaPorDefecto>
	<guardiaPorDefecto>G</guardiaPorDefecto>
	<reunionPorDefecto>RDP</reunionPorDefecto>
</tareas>
```

Como se ve en el ejemplo existen 3 tareas, cada una delimitada entre `<tarea>` y `</tarea>` . La primera declara la tarea básica que se usa casi siempre, la docencia con los alumnos.

Esta primera tarea, tiene el nombre de `LEC` que es lo que la identifica en posteriores referencias. Además se le ha agregado un nombre largo ( `<nombreCompleto>` ) para poder identificarlo más fácilmente. El elemento `<nombreCompleto>` es opcional, aunque se suele poner para facilitar el reconocimiento por parte del usuario. A continuación tiene definida la preferencia horaria mediante el elemento [<plantilla>](elementos.md#plantillaSinFType) , esta plantilla es una lista de [<tramo>](elementos.md#tramoSinFType) que indican el deseo de colocar este tipo de tareas en determinado tramo.

El [<tramo>](elementos.md#tramoSinFType) referencia a un tramo de un marco mediante sus atributos, los cuales son obligatorios (ya que sino no se puede identificar el tramo al que se refiere). Los atributos son: `marco` , `dia` e `indice` . Que corresponden con el identificador del marco, el día del tramo, de 0 (lunes) a 4 (viernes), el indice del tramo (que debe corresponder con el índice de un tramo del día y marco indicado). En el ejemplo sería el tramo 0 del lunes del marco A.

El contenido del tramo es la preferencia de ese tramo. Puede ser una de las siguientes cadenas de texto (de menor preferencia a mayor): `prohibido` , `preferentementeNo2` , `preferentementeNo1` , `disponible` . En el caso del ejemplo es `preferentementeNo1` , con lo que la plantilla indicaría que no se desea que esta tarea se asigne en el tramo 0 del lunes del marco A. La cadena prohibido, es una restricción que siempre se cumple haciendo que sea más difícil la obtención de un horario completo, con lo que no es aconsejable su uso.

Después de la primera tarea se han puesto las otras dos tareas que suelen venir por defecto. En estas tareas solo se ha declarado su nombre ya que el resto de elementos son opcionales.

Y se indica cuales son las tareas por defecto de los distintos tipos.

#### Declaramos los profesores

Nota: Tras la lista de tareas viene la lista de departamentos, pero es un elemento opcional (aunque es conveniente ponerlo).

Tras la lista de departamentos viene la lista de profesores. Esta lista se declara mediante el elemento [`<profesores>`](elementos.md#profesores).

El elemento profesores contiene una lista de los profesores existentes, es decir 1 o más elementos [<profesor>](elementos.md#profesor) . El elemento tiene los siguientes subelementos: `<nombre>` , `<abreviatura>` , `<nombreCompleto>` , `<departamento>` , `<claveDeExportación>` , `<tomaDePosesion>` , `<plantilla>` , `<opciones>, <practicasDeFP>, <reduccionCargaLectiva>, <mensaje>` y alguno más. El único elemento obligatorio es el nombre. Los demás elementos son opcionales, aunque algunos, como el departamento, es muy recomendable que se ponga.

El elemento `<nombre>` es el identificativo del profesor, y será usado para referenciar al profesor. Este debe tener almenos un carácter (y doce como máximo), es decir `<nombre></nombre>` o `<nombre />` serían incorrectos. Además no puede haber varios profesores con el mismo nombre.

Un ejemplo de una lista mínima de profesores podría ser:

```
<profesores>
	<profesor>
		<nombre>Raúl</nombre>
		<departamento>Matemáticas</departamento>
	</profesor>
	<profesor>
		<nombre>Antonio</nombre>
		<departamento>Inglés</departamento>
	</profesor>
	<profesor>
		<nombre>Ana</nombre>
		<departamento>Inglés</departamento>
	</profesor>
</profesores>
```

**Aviso**: Tenga en cuenta que el elemento departamento distingue mayúsculas y minúsculas y que es importante que los profesores que son del mismo departamento tengan el elemento departamento exactamente igual. Por ejemplo los departamentos "Inglés", "inglés" e "Ingles" son departamentos distintos, ya sea por la mayúscula o por el acento.

El elemento [`<profesor>`](elementos.md#profesor) tiene muchos más elementos opcionales, como por ejemplo una `<plantilla>` (parecida a la de las tareas), si quieres más información sobre este elemento consulte la [especificación del mismo](elementos.md#profesor).

#### Declarando las materias

A continuación de la lista de los profesores se coloca la lista de las materias. Está lista se define mediante el elemento [<materias>](elementos.md#materias) .

El elemento materia está compuesto por una lista de elementos [<materia>](elementos.md#materia) que son los que declaran cada materia disponible. El elemento [<materia>](elementos.md#materia) tiene varios subelementos, de los cuales solo es obligatorio el `<nombre>` (como en el de [`<profesor>`](elementos.md#profesor)).

El elemento `<nombre>` es el identificativo de la materia (al igual que en los profesores), y será usado para referenciar la materia. Este debe tener almenos un carácter (y un máximo de 12), es decir `<nombre></nombre>` o `<nombre />` serían incorrectos. Además no puede haber varias materias con el mismo nombre.

Uno de los elementos opcionales que tiene la materia y que no tiene el profesor es el elemento `<esTutoria>` que indica si la materia corresponde con una tutoría. `<esTutoria>` es de tipo [booleano](#booleano), es decir que solo puede tener dos valores `true` (verdadero) y `false` (falso) como contenido. En este caso, cuando es `true` indica que es tutoría y cuando es `false` indica que no es una tutoría. Por defecto si se omite el elemento `<esTutoria>` se tomará como `false` .

Un pequeño ejemplo de una lista de materias sería:

```
<materias>
	<materia>
		<nombre>Inglés</nombre>
	</materia>
	<materia>
		<nombre>Matemáticas</nombre>
	</materia>
	<materia>
		<nombre>Tutoria1A</nombre>
		<esTutoria>true</esTutoria>
	</materia>
</materias>
```

En este ejemplo se declaran 2 materias y 1 tutoría que se llaman respectivamente, Inglés, Matemáticas y Tutoria1A.

#### Declarando los grupos

El siguiente elemento en [<datosGHC>](elementos.md#datosGHC) es la lista de los grupos, que viene indicada por el elemento [<grupos>](elementos.md#grupos) .

El elemento [<grupos>](elementos.md#grupos) contiene una lista de subelementos [`<grupo>`](elementos.md#grupo).

Cada elemento [`<grupo>`](elementos.md#grupo) declara un grupo. Un grupo tiene que ir asociado a un submarco, para ello se utiliza el atributo `submarco` que es obligatorio. Este atributo tiene como valor el identificador del submarco al que se debe asociar el grupo y, como es lógico, el submarco debe existir en la [lista de marcos](elementos.md#marcosDeHorario).

El grupo contiene el subelemento `<nombre>` (entre otros). Este subelemento es obligatorio y va en primer lugar. Indica el nombre del grupo ([Ver NombreType](#NombreType)), que es como se le va a identificar en el resto del archivo.

Un pequeño ejemplo de la lista de grupos podría ser:

```
<grupos>
	<grupo submarco="A">
		<nombre>1ºA</nombre>
	</grupo>
	<grupo submarco="B">
		<nombre>1ºB</nombre>
	</grupo>
</grupos>
```

En el ejemplo se declaran dos grupos llamados "`1ºA`" y "`1ºB`", asociados al marco `A` y al `B` respectivamente. Estos grupos tendrán los valores por defecto aunque se pueden personalizar más usando los subelemetos opcionales.

Nota: Los siguientes elementos serían la [lista de cursos](elementos.md#cursos) y la [lista de relación de materia-curso](elementos.md#relacionesMateriasCurso), pero estos elementos no son obligatorios (aunque como siempre es aconsejable sus uso).

### Cuarto paso, las sesiones básicas.

El siguiente elemento obligatorio para hacer un horario es la lista de las sesiones. Esta es la más importante de todas ya que declara las sesiones que se van a colocar, como se deben colocar y otras implicaciones como si es necesario un cierto tipo de aula, tiene que ir en el mismo día que otra, etc.

En este cuarto paso vamos a indicar las opciones básicas de las sesiones.

Lo primero es que la lista se declara mediante el elemento [<sesionesLectivas>](elementos.md#sesionesLectivas) , que es el que contiene una lista de elementos [`<sesion>`](elementos.md#sesion) que son los que definen cada sesión.

El elemento [`<sesion>`](elementos.md#sesion) tiene el atributo `id` , el cual es obligatorio, y que declara el identificador de la sesión. Su valor es de tipo [`nonNegativeInteger`](#nonNegativeInteger) (entero mayor o igual que 0) y debe ser único.

#### Materia que se imparte

El primer subelemento de la sesión es el nombre de la materia que se quiere impartir. Se declara con la etiqueta `<materia>` (no confundir con el subelemento [<materia>](elementos.md#materia) del elemento [<materias>](elementos.md#materias) ). Y su valor tiene que ser el nombre de una materia que haya sido declarada en la [lista de materias](elementos.md#materias). Por ejemplo `<materia>Matemáticas</materia>` .

#### Grupo al que se imparte

El segundo subelemento es el nombre del grupo al que se va a impartir la sesión. Esto se indica mediante la etiqueta `<grupo>` (no confundir con el subelemento [<grupo>](elementos.md#grupo) del elemento [`<grupos>`](elementos.md#grupos)). Al igual que con la materia, su valor tiene que ser el nombre de un grupo definido en la [lista de grupos](elementos.md#grupos). Por ejemplo `<grupo>1ºA</grupo>` .

#### Profesor que la imparte

El tercer elemento es el nombre del profesor que lo imparte. Este se indica mediante la etiqueta `<profesor>` (no confundir con el subelemento [`<profesor>`](elementos.md#profesor) del elemento [`<profesores>`](elementos.md#profesores)). Y como en la materia y en el grupo, el valor tiene que ser un nombre de un profesor de la [lista de profesores](elementos.md#profesores).

#### Distribución de la sesión

El siguiente elemento es la distribución, que se define con el elemento [<distribucionSemanal>](elementos.md#distribucionSemanal) . Este elemento indica los "tramos" que se deben dar y con que distribución. Por ejemplo dos clases un día y otra en otro (3 en total).

Para ello se puede usar uno de tres subelementos disponibles (solo debe aparecer uno de ellos, ya que es una elección en vez de una lista como hasta ahora). Los tres posibles subelementos son: [<distribucionFija>](elementos.md#distribucionFija) , [<distribucionVariable>](elementos.md#distribucionVariable) y [<distribucionPersonalizada>](elementos.md#distribucionPersonalizada) .

La [distribución fija](elementos.md#distribucionFija) permite que se indique una distribución concreta. La [distribución variable](elementos.md#distribucionVariable) permite indicar varias distribuciónes que se encuentren en un determinado rango (por ejemplo 5 sesiones distribuidas entre días con 1 a 2 tramos por día), esta permite mucha flexibilidad al horario haciendo que sea más fácil la aparición de un horario completo. La [distribución personalizada](elementos.md#distribucionPersonalizada) permite indicar varias distribuciones fijas entre las que puede elegir el generador de horarios.

Explicaré la [distribución fija](elementos.md#distribucionFija) que es la más sencilla. Esta distribución viene indicada por el elemento [<distribucionFija>](elementos.md#distribucionFija) , el cual contiene una lista de subelementos `<numSesiones>` que indican la cantidad de tramos que se impartirán en un mismo día. Puede haber de 1 a 5 de estos elementos (uno para cada día de la semana). Por ejemplo:

```
<distribucionSemanal>
	<distribucionFija>
		<numSesiones>2</numSesiones>
		<numSesiones>1</numSesiones>
		<numSesiones>1</numSesiones>
	</distribucionFija>
</distribucionSemanal>
```

Este ejemplo indica que un día se deben dar dos clases, y en otros dos días se debe dar una en cada uno, 4 clases (tramos) en total. Aquí no se indica si se deben impartir en determinado día de la semana (lunes, martes, etc), sino que solo se indica como se debe distribuir la carga lectiva, para indicar si se debe dar en determinados días de la semana se debe usar la plantilla de la sesión. El orden en el que se colocan los elementos `<numSesiones>` no es importante, no se tiene en cuenta.

Para saber más sobre los tipos de distribución mire el capitulo "[Los tipos de distribución de las sesiones](#TiposDeDistribucion)".

#### Lista de aulas de la sesión

Lo siguiente que tenemos que indicar en la sesión es la aula en la que se puede impartir. Esto se realiza mediante el elemento `<listaDeAulas>` , que contiene una lista de elementos `<aula>` . Los elementos `<aula>` contienen el nombre de un aula de la [lista de aulas](elementos.md#aulas), en el que se debe impartir la sesión.

Este elemento es opcional, si no aparece o la lista de aulas está vacía, quiere decir que da igual en que aula se coloque. Es decir de no estar este elemento se usará un aula general disponible.

Si se indican más de una aula, el orden en el que están delcaradas es significativo. Primero se intentará colocar la sesión en el primer aula, si no está disponible, se intentará en la segunda, etc.

Un ejemplo de lista de aulas podría ser:

```
<listaDeAulas>
	<aula>A1</aula>
	<aula>Gimnasio1</aula>
</listaDeAulas>
```
			

Donde `A1` y `Gimnasio1` son nombre de aulas de la lista de aulas.

#### Aulas alternativas de la sesión

A continuación de la lista de aulas se pone la lista de conjuntos de aulas alternativos (es opcional). Esto se realiza mediante el elemento `<listaDeAlternativas>` que contiene una lista de elementos `<conjuntoAlternativo>` . El elemento `<conjuntoAlternativo>` es el nombre de un conjunto de aulas de la [lista de conjuntos de aulas](elementos.md#conjuntoDeAulas).

Si la lista está vacía o no se pone el elemento `<listaDeAlternativas>` , indica que no se quiere alternativa a la lista de aulas y si no están o están vacías ambas, indica que puede ser cualquiera.

Por ejemplo:

```
<listaDeAlternativas>
	<conjuntoAlternativo>general</conjuntoAlternativo>
</listaDeAlternativas>
```
			

El ejemplo indicaría que si no están disponibles las aulas indicadas en `<listaDeAulas>` de la sesión, se debe elegir una del conjunto de aulas llamado "general". En este caso el conjunto general, que es el nombre del conjunto especial que siempre debe estar y que contiene, como su propio nombre indica, aulas de proposito general.

#### Tarea de la sesión

Lo siguiente sería la tarea a la que corresponde la sesión.

Esto se realiza mediante el subelemento `<tarea>` que contiene el nombre de la tarea a la que corresponde la sesión (es obligatorio). Ese nombre debe existir en la [lista de tareas](elementos.md#tareas).

Por ejemplo:

```
<tarea>LEC</tarea>
```
			

El ejemplo indicaría que es del tipo `LEC` (Lectivo), que suele ser el común en las sesiones.

**Nota**: El siguiente elemento sería el `<grupoMateria>` . Pero este elemento es opcional.

#### Departamento de la sesión

El siguiente elemento de una sesión es el subelemento <departamento>. Este indica el departamento al que pertenece la sesión.

No tiene subelementos, solo el valor que es el nombre del departamento al que pertenece. Hay que tener en cuenta que se distinguen mayúsculas y minúsculas como en el departamento de los [profesores](elementos.md#profesor).

Por ejemplo:

```
<departamento>Matemáticas</departamento>
```
			

Que indicaría que la sesión pertenece al departamento de `Matemáticas` , que es diferente al departamento de `matemáticas` .

#### Opciones de la sesión

Nota: El siguiente elmemento sería el subelemento `<notas>` , para más información ver la documentación de la [`<sesion>`](elementos.md#sesion).

Lo siguiente son las opciones de la sesión. Estas son definidas mediante el subelemento `<opciones>` , no hay que confundir este elemento con el subelemento `<opciones>` de otros elementos (como por ejemplo el de los [profesores](elementos.md#profesor)). Este elemento es opcional, tomandose los valores por defecto en caso de que no se ponga. O si alguno de los elementos falta, se tomarán su valor por defecto.

El elemento `<opciones>` contiene los siguientes subelementos:

*   `<penaSesionesAPrimera>`. Indica si se penaliza que más del 50% de los turnos de la sesión se coloquen a primera hora. Es de tipo [booleano](#booleano). Por defecto es `true`.
*   `<penaSesionesAUltima>`. Indica que se penalizará que más del 50% de los turnos de la sesión se coloquen a última hora. Es de tipo [booleano](#booleano). Por defecto es `true`.
*   `<penaSalirUltimaEntrarPrimera>`. Indica si se penaliza que se coloque a última hora y a primera del día siguiente. Es de tipo [booleano](#booleano). Por defecto es `true`.
*   `<penaSesionMismaHora>`. Indica si se penalizará que se coloque los turnos a la misma hora. Es de tipo [string](#string). Por defecto es `misma`. Puede tener los valores `distinta`, `indiferente`, `misma`.
*   `<penaCoincidanPorLaTarde>`. Indica si se penalizará que los turnos de la sesión coincidan en el turno de tarde. Es de tipo [booleano](#booleano). Por defecto es `true`. Esta opción solo es válida cuando hay un tramo de tipo `mediodia` en el marco. En caso de no haber jornada partida, se ignora esta opción.
*   `<noPermitirRecreosEntreSesiones>`. Indica que no se permitirá que si la sesión tiene varios tramos en un día, se coloque un recreo entre medias. Es de tipo [booleano](#booleano). Por defecto es `false`. En caso de que la sesión no tenga varios tramos en un día, esta opción se ignora.
*   `<recreosSeparanSesionesContinuas>`. Prohíbe o permite que se coloquen las sesiones configuradas como consecutivas si están separadas por recreos. Esta opción se ignora si no tiene sesiones consecutivas o si la sesión tiene varios tramos en un día. Es de tipo [booleano](#booleano). Por defecto es `false`.
*   `<permitirImpartanEnDiasSeguidos>`. Indica como se tendrá en cuenta el que se impartan en varios días seguidos si se da en 2 o 3 días. Puede tomar los valores: `obligatoriamente`, `preferiblemente`, `indiferente`, `prohibido` o `penalizaNoSeguidas`. El valor `penalizaNoSeguidas` indica que se quiere que se impartan en días seguidos. En el caso de `preferiblemente`, se usará la ponderación configurada en las opciones generales.
*   `<considerarLunesViernesSeguidos>`. Indica, en caso de que la sesión se imparta en 2 o 3 días, si se considera el Lunes como día seguido al Viernes. Es de tipo [booleano](#booleano). Por defecto es `false`.

#### Plantilla de la sesión

Después de las opciones viene la plantilla. Esta es definida mediante el elemento [<plantilla>](elementos.md#PlantillaType) , este elemento es opcional, tomandose los tramos que falten (o todos si no se pone el elemento) por preferentes. Que es como la de la de [las tareas](#declaramosLasTareas) y profesores pero además tiene el valor fijado (que es usado para indicar un tramo en el que ya está colocada la sesión).

El marco de los tramos debe ser el mismo que el del grupo asignado a la sesión. Si no tiene el mismo marco que el grupo, el tramo será ignorado.

Por ejemplo:

```
<plantilla>  
	<tramoHorario marco="A" dia="0" indice"0">prohibido</tramoHorario>  
	<tramoHorario marco="A" dia="0"  
 indice"1">preferentementeNo</tramoHorario>  
</plantilla>
```

El ejemplo indicaría que el Lunes en el tramo _0_, no se puede colocar. Y que en el tramo _1_ se intentará no colocarlo. Los dos pertenecientes al marco _A_.

### Ejemplo de la sesión básica

Un ejemplo básico de sesión (sin relaciones, ni los subelementos avanzados), sería:

```
<sesion id="0">  
	<materia>Inglés1ESO</materia>  
	<grupo>1ºESOA</grupo>  
	<profesor>Raúl</profesor>  
	<distribucionSemanal>  
		<distribucionFija>  
			<numSesiones>2</numSesiones>  
			<numSesiones>1</numSesiones>  
			<numSesiones>1</numSesiones>  
		</distribucionFija>  
	</distribucionSemanal>  
	<listaDeAulas>  
		<aula>Aula1</aula>  
	</listaDeAulas>  
	<listaDeAlternativas>  
		<conjuntoAlternativo>general</conjuntoAlternativo>  
	</listaDeAlternativas>  
	<tarea>LEC</tarea>  
	<departamento>Inglés</departamento>  
	<opciones>  
		<penaSesionesAPrimera>false</penaSesionesAPrimera>  
		<penaSesionesAUltima>false</penaSesionesAUltima>  
	</opciones>  
	<plantilla>  
		<tramo marco="A" dia="0" indice="0">prohibido</tramoHorario>  
		<tramo marco="A" dia="0"  
 indice="1">preferentementeNo1</tramoHorario>  
		<tramo marco="A" dia="1"  
 indice="0">preferentementeNo1</tramoHorario>  
	</plantilla>  
</sesion>
```

Esta sesión da la materia _Inglés1ESO_, al grupo _1ºESOA_ y la imparte el profesor _Raúl_. Esta distribuida en tres días, dos con una sesión y otro con dos tramos (o sesión doble). También indica que se debe impartir en el aula _Aula1_ y alternativamente (si no está disponible el aula _Aula1_) se puede asignar a un aula del conjunto _general_. Es de tipo _LEC_ (que probablemente equivaldrá a docencia directa con el grupo de alumnos). Pertenece al departamento de _Inglés_. Tiene las opciones por defecto excepto para la penalización de tener un 50% o más de las sesiones a primera (o última) hora, que están desactivadas; es decir da igual si se dan a primera (o última) hora más del 50% de los tramos. Y además declara que no se puede colocar en el tramo _0_ del Lunes, y que se debe intentar no colocarla en el tramo _1_ del Lunes y en el _0_ del Martes; el marco al que pertenecen los tramos será el mismo que el del grupo _1ºESOA_.

Nota: Con los elementos visto se podría hacer un horario. Pero las sesiones no tendrían relaciones entre ellas, para ello habría que definir los demás elementos de la sesión y los elementos del esquema asociados a ellos (como se verá en la [siguiente sección](#Relaciones)).

XML Avanzado
------------

### Agregados a la sesión

En las sesiones, después de la plantilla y antes de los elementos de los elementos de las relaciones ([ver más abajo](#Relaciones)), se pueden poner los elementos: [`<otrasMateriasGrupos>`](elementos.md#otrasMateriasGrupos), [`<otrosGrupos>`](elementos.md#otrosGrupos), [`<otrosProfesores>`](elementos.md#otrosProfesores), [`<otrasMaterias>`](elementos.md#otrasMaterias), [`<otrasAulas>`](elementos.md#otrasAulas). Todos estos elementos son opcionales.

Estos elementos indican otros grupos, profesores, etc, que se deben agregar a la sesión. Así por ejemplo si una asignatura necesita varios profesores (por ejemplo, al ser una sesión práctica), se agregaría el otro profesor a la lista `<otrosProfesores>` .

El elemento [`<otrasMateriasGrupos>`](elementos.md#otrasMateriasGrupos), define una lista de elementos [`<materiaGrupo>`](elementos.md#parMateriaGrupo) que a su vez contienen dos elementos, `<materia>` y `<grupo>` , que contienen el nombre de la materia y el grupo que también se agregarán a la sesión. Es redundante con la listas [`<otrosGrupos>`](elementos.md#otrosGrupos) y [`<otrasMaterias>`](elementos.md#otrasMaterias), con lo que tendrán los mismos elementos, aunque se prefiere esta lista a las independientes.

El elemento [`<otrosGrupos>`](elementos.md#otrosGrupos), define otros grupos que se incluyen en la sesión. Este elemento contiene una lista de elementos `<grupo>` , cuyo valor es el nombre del grupo al que también se le imparte la sesión de forma conjunta con el grupo principal. Se prefiere usar la lista `<otrasMateriasGrupos>`

El elemento [`<otrosProfesores>`](elementos.md#otrosProfesores), define otros profesores que se incluyen en la sesión. Este elemento tiene una lista de elementos `<profesor>` , cuyo valor es el nombre del profesor que se quiere agregar.

El elemento [`<otrasMaterias>`](elementos.md#otrasMaterias), define otras asignaturas que se deben impartir conjuntamente con la principal. Este elemento contiene una lista de elementos `<materia>` , cuyo valor es el nombre de la otra materia que se imparte conjuntamente con la principal.

El elemento [`<otrasAulas>`](elementos.md#otrasAulas), define otras aulas que también son necesarias para la sesión. Este elemento contiene una lista de elementos `<otraAula>` , cuyo contenido es un elemento `<aula>` seguido de un elemento `<grupo>` . El elemento `<aula>` indica el nombre del aula adicional que se requiere y el elemento `<grupo>` indica el nombre del conjunto de un conjunto de aulas alternativas que se pueden usar en caso de que no esté disponible el aula declarado en `<aula>` .

Un ejemplo (parcial) de una sesión que use estos elementos podría ser:

```
<sesion>  
	...  
	<plantilla>  
		...  
	</plantilla>  
	<otrosGrupos>  
		<grupo>ESO1B</grupo>  
		<grupo>ESO1C</grupo>  
	</otrosGrupos>  
	<otrosProfesores>  
		<profesor>Javier</profesor>  
	</otrosProfesores>  
	<otrasMaterias>  
		<materia>LenguasHispanas</materia>  
		<materia>Castellano</materia>  
	</otrasMaterias>  
	<otrasAulas>  
		<otraAula>  
			<aula>A2</aula>  
			<grupo>general</grupo>  
		</otraAula>  
		<otraAula>  
			<grupo>general</grupo>  
		</otraAula>  
	</otrasAulas>  
	<sesionesSimultaneas>  
	...  
</sesion>
```

Este ejemplo indicaría que la sesión se impartirá a los grupos _`ESO1B`_ y _`ESO1C`_ (además del grupo principal). Además, el profesor _`Javier`_ también la dará (en conjunto con el principal). También se incluyen las materias `_LenguasHispanas_` y `_Castellano_` además de la principal (puede que aunque tengan nombre distinto, den el mismo contenido). Y también se requieren otras dos aulas más (además de la principal), de estas dos aulas más, se prefiere que una sea la `_A2_` (y otra general) pero si no está disponible, que sean las dos generales.

### Relaciones en las sesiones

Las sesiones pueden estar relacionadas entre ellas. Por ejemplo una sesión puede que se tenga que impartir a la vez que otra debido a que sea una alternativa para los alumnos de esta.

Para definir estas relaciones se usan los siguientes subelementos de las sesiones: `<sesionesSimultaneas>` , `<enDistintoDia>` , `<consecutivas>` , `<noConsecutivas>` .

En el elemento `<sesionesSimultaneas>` definen un bloque de sesiones que se deben dar en el mismo tramo horario. Este elemento contiene el valor del identificador del bloque de sesiones simultaneas al que pertenece ([ver más adelante](#LasListasDeRelacion)). El identificador de la sesión debería estar en la lista de sesiones del bloque indicado.

El elemento [<enDistintoDia>](elementos.md#enDistintoDia) declara una lista de sesiones que se deben impartir en distinto día. Para saber más sobre este elemento ver la [documentación](elementos.md#enDistintoDia) del mismo.

El elemento `<consecutivas>` indica el identificador del bloque de sesiones consecutivas (que deben darse en tramos seguidos). El identificador de la sesión debería estar en la lista de sesiones del bloque indicado ([ver más adelante](#LasListasDeRelacion)).

Y el elemento [<noConsecutivas>](elementos.md#noConsecutivas) declara una lista de sesiones que no deben darse en tramos consecutivos. Para saber más, consulte la [documentación](elementos.md#noConsecutivas) del elemento.

Los elementos son necesarios si se tienen que usar, si no se tiene alguna de las relaciones, no se pone el elemento correspondiente.

Por ejemplo:

```
<sesion>  
	...  
	<otrosAulas>  
		...  
	</otrosAulas>  
	<sesionesSimultaneas>0</sesionesSimultaneas>  
	<enDistintoDia>  
		<sesiones>  
			<sesion>2</sesion>  
			<sesion>8</sesion>  
		</sesiones>  
		<enDiasSeguidos>preferentemente</enDiasSeguidos>  
	</enDistintoDia>  
	<consecutivas>0</consecutivas>  
	<noConsecutivas>  
		<sesion>13</sesion>  
		<sesion>14</sesion>  
	</noConsecutivas>  
</sesion>
```

Este ejemplo (parcial) de una sesión indicaría que pertenece al bloque de sesiones simultaneas con identificador _0_, que se debe dar en días distintos a los usados por las sesiones _2_ y _8_ pero que preferentemente serán días seguidos, que pertenece al bloque de consecutivas con identificador _0_ y que no se puede dar de forma consecutiva a las sesiones con identificadores _13_ y _14_.

Para saber con que sesiones tiene relación habría que mirar en el elemento de bloque correspondiente de la lista de relaciones adecuada ([ver más adelante](#LasListasDeRelacion)).

### Las listas de relación de sesiones

Después del elemento [<sesionesLectivas>](elementos.md#sesionesLectivas) , va el elemento [`<listasDeRelacion>`](elementos.md#listasDeRelacion) que es el que contiene los bloques de sesiones que tienen relación entre ellas, como por ejemplo si son simultaneas, continuas, etc.

El elemento [`<listasDeRelacion>`](elementos.md#listasDeRelacion) tiene los subelementos (en orden): `<simultaneas>` y `<consecutivas>` .

El elemento `<simultaneas>` , tiene una lista de elementos `<bloqueDeSesiones>` , que indican las sesiones que se deben impartir en el mismo tramo (a la misma hora y días). El `<bloqueDeSesiones>` tiene dos atributos: `id` y `submarco` . El `id` es el que identifica el bloque de sesiones simultaneas y es el que hacen referencia en las sesiones, es de tipo [`nonNegativeInteger`](#nonNegativeInteger). El `submarco` indica el submarco al que pertenecen todas las sesiones simultaneas del bloque, este remplaza al de las sesiones que contiene, es de tipo [NCName](#NCName) . Los `<bloqueDeSesiones>` también tienen los subelementos `<sesiones>` y `<plantilla>` . En el subelemento `<sesiones>` es una lista de elementos `<sesion>` cuyo valor es el identificador de una sesión que sea simultanea con las demás del bloque. El elemento `<plantilla>` es una [plantilla exactamente como la de las sesiones](#PlantillaDeLaSesion) pero el marco que le falta es tomado del atributo `submarco` del bloque. Esta plantilla reemplazará a la de las sesiones que pertenezcan al bloque. La distribución del bloque es el que venga dado con la primera sesión de la lista de sesiones.

El elemento `<consecutivas>` tiene una lista de elementos `<bloqueDeSesiones>` , que indica las sesiones que se deben impartir en tramos seguidos. Este bloque tiene el atributo `id` que es el identificador del bloque, es de tipo [`nonNegativeInteger`](#nonNegativeInteger). Además también contiene los siguientes subelementos: `<sesiones>` y `<conOrden>` . El subelemento `<sesiones>` es una lista de elementos `<sesion>` cuyo valor es el identificador de las sesión que pertenece al bloque y que se debe dar en un tramo consecutivo a las demás. El elemento `<conOrden>` es de tipo [booleano](#booleano) e indica si el orden en el que están indicados las sesiones es significativo (deben colocarse en el orden indicado) o no (se pueden desordenar, aunque se sigan manteniendo consecutivas).

Un ejemplo de lista de relaciones podría ser:

```
<listasDeRelacion>  
	<simultaneas>  
		<bloqueDeSesiones id="0" submarco="A">  
			<sesiones>  
				<sesion>0</sesion>  
				<sesion>1</sesion>  
			</sesiones>  
			<plantilla>  
				<tramoHorario dia="0"  
 indice="0">preferentementeNo</tramoHorario>  
			</plantilla>  
		</bloqueDeSesiones>  
		<bloqueDeSesiones id="1" submarco="B">  
			<sesiones>  
				<sesion>12</sesion>  
				<sesion>5</sesion>  
			</sesiones>  
		</bloqueDeSesiones>  
	</simultaneas>  
	<consecutivas>  
		<bloqueDeSesiones id="0">  
			<sesiones>  
				<sesion>6</sesion>  
				<sesion>2</sesion>  
				<sesion>7</sesion>  
			</sesiones>  
			<conOrden>true</conOrden>  
		</bloqueDeSesiones>  
	</consecutivas>  
</listasDeRelacion>
```

Esta lista de relaciones declararía cinco bloques en total, dos en simultaneas y los otros tres uno en cada tipo.

El bloque de simultaneas `0` está asociado al marco `A` . También indica que el _Lunes_ en el tramo `0` del marco `A` es preferible no colocarla. Y son las sesiones `0` y `1` las que tienen que colocarse en el mismo tramo horario.

El bloque de simultaneas `1` está asociado al marco `B` (las sesiones se colocarán en tramos del marco `B` ). Y las sesiones que tienen que ser simultaneas son la `12` y la `5` .

El bloque de consecutivas (identificado con el `0` ) indica que las sesiones `6` , `2` y `7` deben colocarse en tramos seguidos. Además, debido a que la opción `<conOrden>` tiene el valor `true` , deben colocarse en ese orden, primero la `6` , en el siguiente tramo la `2` y en el siguiente la `7` .

### Relaciones materia-curso

Después del elemento [Grupos](#DeclarandoLosGrupos) viene la definición de los cursos.

Aunque no es una lista ensencial, ayudará a crear las sesiones ya que permite que se filtren las materias que tiene disponible un grupo depediendo del curso al que pertenece.

Esta lista viene especificada por el elemento [cursos](elementos.md#cursos) .

Este elemento contienen elementos [curso](elementos.md#curso) que, además de tener atributos propios de este, contiene el elemento [materiasDelCurso](elementos.md#materiasDelCurso) , que define la lista de materias que pertenecen al curso.

Cada materia de esta lista permite, además de especificar el nombre del la materia, indicar la duración semanal que debe tener una sesión de esta materia y curso (aunque no indica su distribución).

### Reuniones

Después de la [lista de relación](#LasListasDeRelacion), viene la lista de las reuniones que como es lógico definen las reuniones que se van a realizar. Esta lista viene dada por el elemento [<reuniones>](elementos.md#reuniones) .

El elemento [<reuniones>](elementos.md#reuniones) contiene una lista de elementos `<reunion>` que cada una define una reunión. El elemento tiene un atributo llamado `subMarco` cuyo valor es el identificativo del marco al que va asociada la reunión.

El elemento [<reuniones>](elementos.md#reuniones) también contiene los subelementos: `<nombre>` , `<numeroDeReuniones>` , `<dobleDuracion>` , `<tipoDeTarea>` , `<plantilla>` e `<integrantes>` .

El elemento `<nombre>` indica el nombre de la reunión que será su identificador (y por lo tanto debe ser único respecto al resto de reuniones).

El elemento `<numeroDeReuniones>` es la cantidad de veces que se tendría que llevar a cabo esta reunión a lo largo de la semana. Debe valer entre 1 y 5 (ambos inclusive).

El elemento `<dobleDuracion>` indica si las reuniónes tendrán una duración de 1 tramo ( `false` ) o de 2 tramos ( `true` ). Es de tipo [booleano](#booleano) y por defecto vale `false` .

El elemento `<tipoDeTarea>` define la tarea que se realizará en la reunión, lo normal sería que el tipo de tarea sea del estilo de reuniones. El valor tiene que ser el identificador de una tarea de la lista de tareas.

El elemento [<plantilla>](elementos.md#plantillaPDFType) indica los tramos en los que está permitido colocar la reunión. Esta plantilla tiene una lista de subelementos [<tramo>](elementos.md#tramoPDFType) . Este subelemento tiene los atributos `marco` el identificador del marco al que pertenece el tramo, `día` (el día de 0 a 4) e `indice` (el índice del tramo) que junto con el marco de la reunión tienen que identificar a un tramo definido en los marcos. Los valores que puede tener el [<tramo>](elementos.md#tramoPDFType) son `prohibido` , `disponible` y `fijado` . Los tramos que no se pongan (o la plantilla entera si no se pone) se tomarán como `disponible` .

El elemento `<integrantes>` es el que contiene los profesores que tendrán que asistir a la reunión. Está formado por una lista de subelementos `<integrante>` cuyo valor es el nombre de un profesor que tendrá que asistir a la reunión. El mismo profesor no puede estar varias veces en la misma reunión, pero sí que puede aparecer en varias reuniones distintas, además el profesor debe estar definido en la [lista de profesores](elementos.md#profesores).

Un ejemplo de reuniones podría ser:

```
<reuniones>  
	<reunion submarco="A">  
		<nombre>ReuMatematicas</nombre>  
		<numeroDeReuniones>1</numeroDeReuniones>  
		<dobleDuracion>true</dobleDuracion>  
		<tipoDeTarea>RDP</tipoDeTarea>  
		<plantilla>  
			<tramo marco="A" dia="0" indice="0">prohibido</tramo>  
		</plantilla>  
		<integrantes>  
			<integrante>Javier</integrante>  
			<integrante>Laura</integrante>  
			<integrante>Raúl</integrante>  
			<integrante>Ester</integrante>  
		</integrantes>  
	</reunion>  
	<reunion submarco="B">  
		<nombre>ReuIdiomas</nombre>  
		<numeroDeReuniones>1</numeroDeReuniones>  
		<tipoDeTarea>RDP</tipoDeTarea>  
		<integrantes>  
			<integrante>Laura</integrante>  
			<integrante>Jesús</integrante>  
			<integrante>Nuria</integrante>  
		</integrantes>  
	</reunion>  
</reuniones>
```

El ejemplo declara 2 reuniones. La primera (llamada `ReuMatematicas` ), indica que se debe colocar en el marco `A` pero no se puede colocar en el tramo `0` del Lunes. También indica que se realizará una vez a la semana y que tomará dos tramos de duración. Será una reunión de tipo `RDP` (normalmente esta tarea está predefinida y significa Reunión de Departamento). Además deberán asistir los profesores: `Javier` , `Laura` , `Raúl` y `Ester` .

En la segunda reunión (llamada `ReuIdiomas` ), se indica que tendrá que ser colocada en el marco `B` . Se hará una vez a la semana y durará un tramo. El tipo es el mismo que el de la primera reunión ( `RDP` ). Y deberán asistir los profesores `Laura` , `Jesús` y `Nuria` .

### Guardias

Despues de las reuniones van las guardias, que están declaradas con el elemento `<guardias>` . El elemento `<guardias>` contiene una lista de elementos `<guardia>` y cada uno de ellos declara una guardia. Este subelemento tiene el atributo `subMarco` que indica el marco al que irá asociada la guardia. Además, tiene los subelementos `<nombre>` , `<tipoDeTarea>` , `<enRecreos>` , `<profesoresACadaHora>` e `<integrantes>` .

El subelemento `<nombre>` es el identificador de la guardia y como tal debe ser único.

El subelemento `<tipoDeTarea>` (al igual que en las reuniones) indica la tarea que se realiza en la guardia. Por norma general, este será el tipo de tarea `G` (Guardia de Aula), que suele estar predefinido en el gestor de horarios. Su valor debe ser el identificador de una tarea de la [lista de tareas](elementos.md#tareas).

El subelemento `<enRecreos>` indica si será una guardia de tramos de recreos o de tramos lectivos. Es de tipo [booleano](#booleano), indicando si vale `false` que es en tramos lectivos y si es `true` que será una guardia de recreos. Si después se establecen los profesores a cada hora en tramos que no correspondan con esta opción, serán ignorados.

El subelemento `<profesoresACadaHora>` sirve para establecer cuantos profesores son necesarios en cada tramo. Tiene los subelementos `<cantidad>` y `<porTramo>` . El subelemento `<cantidad>` puede tener un valor entero en el rango 1 a 8 (ambos inclusive) e indica la cantidad de profesores que tienen que cubrir un tramo (del tipo indicado por el elemento `<enRecreos>` ). Además si se define el elemento `<porTramo>` pero no se define algún tramo, se tomará la cantidad como la establecida en el elemento `<cantidad>` . El subelemento `<porTramo>` indica especificamente, cuantos profesores son necesarios en determinados tramos. Contiene una lista de subelementos `<cantidadTramo>` , los cuales tienen dos atributos, el atributo `dia` y el atributo `indice` . La unión de estos atributos y el submarco de la guardia tienen que identificar un tramo existente. El valor de `<cantidadTramo>` es un valor entre 0 y 8 (ambos inclusive) que indica cuantos profesores tienen que cubrir la guardia en el tramo identificado por los atributos.

El subelemento `<integrantes>` define la lista con los profesores que se usarán para cubrir la guardia. Contiene una lista de subelementos `<integrante>` , este elemento contiene los subelementos `<nombre>` , `<numeroDeGuardias>` y `<plantilla>` . El elemento `<nombre>` es el nombre del profesor que se quiere agregar para cubrir la guardia. El subelemento `<numeroDeGuardias>` indica cuantas guardias semanales debe cubrir el profesor, como valor debe estar entre 1 y 20. Y el subelemento `<plantilla>` indica los tramos en los que tiene permitido cubrir la guardia el profesor. Esta plantilla es excatamente igual que la de las [reuniones](#reuniones) (aunque con el submarco de la guardia).

Un ejemplo de guardias podría ser:

```
<guardias>  
	<guardia subMarco="A">  
		<nombre>GuardiaAula</nombre>  
		<tipoDeTarea>G</tipoDeTarea>  
		<enRecreos>false</enRecreos>  
		<profesoresACadaHora>  
			<cantidad>1</cantidad>  
			<porTramo>  
				<cantidadTramo dia="1" indice="0">0</cantidadTramo>  
				<cantidadTramo dia="2" indice="0">0</cantidadTramo>  
				<cantidadTramo dia="3" indice="0">0</cantidadTramo>  
			</porTramo>  
		</profesoresACadaHora>  
		<integrantes>  
			<integrante>  
				<nombre>Nuria</nombre>  
				<numeroDeGuardias>4</numeroDeGuardias>  
				<plantilla>  
					<tramo marco="A" dia="0"  
 indice="0">prohibido</tramo>  
				</plantilla>  
			</integrante>  
			<integrante>  
				<nombre>Jesús</nombre>  
				<numeroDeGuardias>4</numeroDeGuardias>  
			</integrante>  
		</integrantes>  
	</guardia>  
</guardias>
```

Este ejemplo declara una guardia llamada `GuardiaAula` y que es de tipo `G` (normalmente corresponde con Guardia de aula). Además está asociada al marco `A` y a los tramos lectivos. También indica que debe haber `1` profesor en cada tramo, excepto en tres de ellos: el tramo de indice `0` de los _Martes_, _Miércoles_ y _Jueves_; en los cuales no se requieren profesores. Los profesores que tienen que cubrir la guardia son `Nuria` y `Jesús` , ambos cubriendo 4 tramos, hay que tener en cuenta que si hay más tramos a cubrir que puestos cubiertos por profesores, se intentará cubrir el máximo aunque queden algunos sin cubrir. Además Nuria no puede hacer guardia en el tramo `0` del _Lunes_ del marco asociado a la guardia ( `A` ).

### Complementarias

Después de las guardias, van las sesiones complementarias. Estas se definen con el elemento `<complementarias>` , el cual contiene una lista de elementos `<complementaria>` .

Cada elemento `<complementaria>` especifica una sesión complementaria. Tiene un atributo, `subMarco` , que indica a que marco está asociada la sesión complementaria. También tiene los subelementos: `<tarea>` , `<profesor>` , `<intervalosSemanales>` , `<maxIntervalosDiarios>` , `<noConsecutivos>` y `<plantilla>` .

El subelemento `<tarea>` indica la tarea asociada a la sesión complementaria. Debe ser una tarea de la [lista de tareas](elementos.md#tareas).

El subelemento `<profesor>` es el nombre del profesor que tiene que realizar la sesión complementaria. Debe existir en la [lista de profesores](elementos.md#profesores).

El subelemento `<distribucionPeriodica>` indica la distribucion de la complementaria a través de las semanas/peridos del horario.

El subelemento `<plantilla>` establece los tramos en las que se puede colocar. Esta plantilla es excatamente igual que la de las [reuniones](#reuniones) (aunque con el submarco de la complementaria). Y como la de reuniones, si se omite (o la parte que se omita) un tramo, se toma como permitido.

Un ejemplo de la lista de complementarias podría ser:

```
<complementarias>  
	<complementaria subMarco="A">  
		<tarea>Tutoria</tarea>  
		<profesor>Jesús</profesor>  
		<distribucionPeriodica>  
		    <distribucionPeriodicaFija>  
		        <distribucionSemanal>  
		            <distribucionVariable>  
		                <numSesiones>4</numSesiones>  
		                <numMaximoDeSesiones>3</numMaximoDeSesiones>  
		            </distribucionVariable>  
		        </distribucionSemanal>  
		    </distribucionPeriodicaFija>  
		</distribucionPeriodica>  
		<plantilla>  
			<tramo marco="A" dia="0" indice="0">prohibido</tramo>  
			<tramo marco="A" dia="0" indice="4">prohibido</tramo>  
		</plantilla>  
	</complementaria>  
<complementarias>
```

Este ejemplo indicaría que hay una sesión complementaria que está asignada al marco `A.` La sesión complementaria será una tutoría (debe estar declarada en la lista de tareas) y será impartida por el profesor Jesús. Además se indica que deben ser 2 intervalos a la semana y que como mucho se pueden dar los 2 en el mismo día, aunque no tienen por que darse en tramos seguidos. También establece que no se puede colocar en el Lunes en los tramos `0` ni `4` del marco asociado ( `A` ).

### Criterios

Después de las sesiones complementarias va el elemento `<criterios>` , el cual establece los valores de ponderación de las distintas opciones. Las opciones que no aparezcan (o todas si no se pone este elemento) se tomarán sus valores por defecto.

El elemento `<criterios>` contiene los subelementos: `<huecosEnHorario>` , `<posicionesNoPreferentes>` , `<colocarSesionesLectivas>` y `<horarioDeProfesores>` .

El elemento `<huecosEnHorario>` agrupa las ponderaciones relativas a dejar tramos libres en los horarios. Contiene los elementos `<huecosEnGrupos>` y `<huecosEnProfesores>` .

El subelemento `<huecosEnGrupos>` indica el peso de dejar huecos en los horarios de los grupos. Por defecto vale 5, es de tipo [unsignedByte](#unsignedByte). Se le aplica un modificador de 20X (veinte veces el valor puesto).

El subelemento `<huecosEnProfesores>` indice el peso de dejar huecos en los horarios de los profesores. Por defecto vale 2, es de tipo [unsignedByte](#unsignedByte).

El elemento `<posicionesNoPreferentes>` agrupa los pesos relativos a la colocación en tramos no preferentes. Contiene los elementos `<enGrupos>` , `<enProfesores>` , `<enMateriasYTareas>` y `<enSesionesLectivas>` .

El subelemento `<enGrupos>` indica el peso de colocar sesiones en tramos no preferentes de los grupos. Se le aplica un modificador de 20X (veinte veces el valor puesto). Es de tipo [unsignedByte](#unsignedByte). Por defecto vale 4.

El subelemento `<enProfesores>` indica el peso de colocar las sesiones en tramos no preferentes de los profesores. Es de tipo [unsignedByte](#unsignedByte). Por defecto vale 3.

El subelemento `<enMateriasYTareas>` indica el peso de colocar las sesiones en tramos no preferentes de las materias o de las tareas. Es de tipo [unsignedByte](#unsignedByte). Por defecto vale 1.

El subelemento `<enSesionesLectivas>` indica el peso de colocar las sesiones en tramos no preferentes de las sesiones lectivas. Es de tipo [unsignedByte](#unsignedByte). Por defecto vale 2.

El elemento `<colocarSesionesLectivas>` agrupa las ponderaciones relacionadas con colocar las sesiones en tramos extremos y por el estilo. Contiene los subelementos `<enDiasConsecutivos>` , `<enAulaNoPreferente>` , `<enHorasExtremas>` , `<coincidanPorLaTarde>` , `<coincidanALaMismaHora>` y `<conCambiosDeAula>` .

El subelemento `<enDiasConsecutivos>` indica el peso de colocar las sesiones en días seguidos (solo es aplicable cuando solo se imparte en 2 o 3 días). Es de tipo [unsignedByte](#unsignedByte). Por defecto vale 1.

El subelemento `<enAulaNoPreferente>` indica el peso de colocar una sesión en una aula del conjunto de alternativas en vez de en la preferente. Es de tipo [unsignedByte](#unsignedByte). Por defecto vale 3.

El subelemento `<enHorasExtremas>` indica el peso de colocar una sesión en las horas de los extremos de un horario. Es de tipo [unsignedByte](#unsignedByte). Por defecto vale 2.

El subelemento `<coincidanPorLaTarde>` indica el peso de colocar varias veces la misma sesión en los turnos de la tarde. Es de tipo [unsignedByte](#unsignedByte). Por defecto vale 1.

El subelemento `<coincidanALaMismaHora>` indica el peso de colocar la sesión en misma hora varios días. Es de tipo [unsignedByte](#unsignedByte). Por defecto vale 0.

El subelemento `<conCambiosDeAula>` indica el peso de colocar las sesiones en aulas diferentes o de que se un grupo deba cambiar de aula. Es de tipo [unsignedByte](#unsignedByte). Por defecto vale 1.

El elemento `<horarioDeProfesores>` agrupa las ponderaciones relacionadas con el horario de los profesores. Contiene los elementos `<horasExcluyentes>` , `<masClasesEnUnDiaQueEnOtro>` , `<horasDeClaseSeguidas>` , `<masPermanencia>` , `<seguidoConElMismoGrupo>` , `<guardiasEnExtremos>` y `<ordenProfesores>` .

El subelemento `<horasExcluyentes>` indica el peso de colocar las sesiones del profesor en horas problemáticas (a primera y a última, por la mañana y por la tarde en el mismo día, etc). Es de tipo [unsignedByte](#unsignedByte). Por defecto vale 3.

El subelemento `<masClasesEnUnDiaQueEnOtro>` indica el peso de colocar las sesiones de un profesor de forma no uniforme durante la semana. Es de tipo [unsignedByte](#unsignedByte). Por defecto vale 3.

El subelemento `<horasDeClaseSeguidas>` indica el peso de colocar más sesiones seguidas que las declaradas en su cuadro de opciones. Es de tipo [unsignedByte](#unsignedByte). Por defecto vale 2.

El subelemento `<masPermanencia>` indica el peso de que tenga más horas de permanencia semanal, contando los huecos entre sesiones, que las declaradas como máximo en el cuadro de propiedades de cada uno. Es de tipo [unsignedByte](#unsignedByte). Por defecto vale 2.

El subelemento `<seguidoConElMismoGrupo>` indica el peso de tenga sesiones seguidas impartidas al mismo grupo. Es de tipo [unsignedByte](#unsignedByte). Por defecto vale 1.

El subelemento `<guardiasEnExtremos>` indica el peso de que le toquen las guardias en los extremos de su horario, intentando así encajarlas en los huecos de sus sesiones lectivas. Es de tipo [unsignedByte](#unsignedByte). Por defecto vale 1.

El subelemento `<ordenProfesores>` indica el peso de que no se respete su orden con respecto a los demás profesores. Es de tipo [unsignedShort](#unsignedShort). Por defecto vale 1.

Un ejemplo de criterios podría ser:

```
<criterios>  
	<huecosEnHorario>  
		<huecosEnGrupos>4</huecosEnGrupos>  
		<huecosEnProfesores>3</huecosEnProfesores>  
	</huecosEnHorario>  
	<posicionesNoPreferentes>  
		<enGrupos>4</enGrupos>  
		<enProfesores>2</enProfesores>  
		<enMateriasYTareas>1</enMateriasYTareas>  
		<enSesionesLectivas>3</enSesionesLectivas>  
	</posicionesNoPreferentes>  
	<colocarSesionesLectivas>  
		<enDiasConsecutivos>0</enDiasConsecutivos>  
		<enAulaNoPreferente>4</enAulaNoPreferente>  
		<enHorasExtremas>3</enHorasExtremas>  
		<coincidanPorLaTarde>2</coincidanPorLaTarde>  
		<coincidanALaMismaHora>0</coincidanALaMismaHora>  
		<conCambiosDeAula>1</conCambiosDeAula>  
	</colocarSesionesLectivas>  
	<horarioDeProfesores>  
		<horasExcluyentes>4</horasExcluyentes>  
		<masClasesEnUnDiaQueEnOtro>1</masClasesEnUnDiaQueEnOtro>  
		<horasDeClaseSeguidas>3</horasDeClaseSeguidas>  
		<masPermanencia>4</masPermanencia>  
		<seguidoConElMismoGrupo>0</seguidoConElMismoGrupo>  
		<guardiasEnExtremos>1</guardiasEnExtremos>  
		<ordenProfesores>1</ordenProfesores>  
	</horarioDeProfesores>  
</criterios>
```

Este ejemplo declara todos los valores para las opciones, aunque se podrían haber omitido los que son iguales al valor por defecto (como en el elemento `<guardiasEnExtremos>` ).

Los tipos de distribución de las sesiones
-----------------------------------------

Hay tres tipos de distribución que vienen definidos mediante los elementos [<distribucionFija>](elementos.md#distribucionFija) , [<distribucionVariable>](elementos.md#distribucionVariable) y [<distribucionPersonalizada>](elementos.md#distribucionPersonalizada) .

En la distribución solo se puede poner uno de los tres tipos de distribución. Es aconsejable usar el tipo de distribución variable, ya que permite colocar más fácilmente la sesión, al poder colocarla de múltiples formas y no se tienen que definir todos los posibles valores.

Los tres tipos indican cuantas clases (tramos lectivos) tienen que impartirse en cada día (y por lo tanto, cuantos se dan en total). Ninguno de ellos especifica que día de la semana en concreto es el que tiene que tener lo especificado, esto lo elige el generador de horarios para adecuarlo a las distintas plantillas (la de las sesiones, de los profesores, etc).

### La distribución fija

La [distribución fija](elementos.md#distribucionFija) es la más sencilla. Solo permite una distribución (la especificada) con lo que es la más restrictiva de los tres tipos.

Esta distribución viene indicada por el elemento [<distribucionFija>](elementos.md#distribucionFija) , el cual contiene una lista de subelementos `<numSesiones>` que indican la cantidad de tramos que se impartirán en un mismo día. Puede haber de 1 a 5 de estos elementos (uno para cada día de la semana). Por ejemplo:

```
<distribucionSemanal>
	<distribucionFija>
		<numSesiones>2</numSesiones>
		<numSesiones>1</numSesiones>
		<numSesiones>1</numSesiones>
	</distribucionFija>
</distribucionSemanal>
```

Este ejemplo indica que un día se deben dar dos clases, y en otros dos días se debe dar una en cada uno. Con lo que en total tenemos que la sesión tendrá cuatro clases (tramos) a la semana.

El orden en el que se colocan los elementos `<numSesiones>` no es importante, no se tiene en cuenta.

### La distribución personalizada

La [distribución personalizada](elementos.md#distribucionPersonalizada) es, en potencia, la que permite una mayor flexibilidad a la hora de definir la distribución, ya que permite definir una lista de distribuciones fijas.

Esta distribución se indica mediante el elemento [<distribucionPersonalizada>](elementos.md#distribucionPersonalizada) . Este contiene una lista de elementos `<distribucion>` , que son del mismo tipo que la [distribución fija](elementos.md#distribucionFija).

Los elementos `<distribucion>` tienen una lista de subelementos `<numSesiones>` que indican la cantidad de tramos que se impartirán en un mismo día. Como en la [distribución fija](elementos.md#distribucionFija) deben haber entre uno y cinco de ellos. Todas las distribuciones tienen que tener el mismo número de sesiones a la semana, por ejemplo no puede haber una distribución 111 (3 en total) y otra 31 (4 en total).

Un ejemplo de esta distribución sería:

```
<distribucionSemanal>  
	<distribucionPersonalizada>  
		<distribucion>  
			<numSesiones>2</numSesiones>  
			<numSesiones>2</numSesiones>  
			<numSesiones>1</numSesiones>  
		</distribucion>  
		<distribucion>  
			<numSesiones>3</numSesiones>  
			<numSesiones>2</numSesiones>  
		</distribucion>  
	</distribucionPersonalizada>  
</distribucionSemanal>
```

Esta distribución indicaría que se puede elegir entre colocar dos tramos en dos días (dos en cada uno) y otro en otro día o colocar tres en un día y dos en otro.

### La distribución variable

La [distribución variable](elementos.md#distribucionVariable) permite todas las posibles convinaciones, con un límite en el número máximo de sesiones por día, de sesiones y sin tener que especificarlas una a una.

Se usa mediante el elemento [<distribucionVariable>](elementos.md#distribucionVariable) , que contiene la siguiente lista de subelementos (en orden):

*   `<numSesiones>`. Indica el número de tramos por semana que tiene la sesión. Que es del tipo [decimal](#decimal) restringido para que tenga que ser menor o igual que 25 con incrementos de 0.25. Es obligatorio.
*   `<numMaximoDeSesiones>`. Indica cuantos tramos como máximo habrá en un mismo día. Puede tomar valores entre 1 y 5 además del valor "M" (media duración), "T" (tres cuartos de la duración), "S" (seis cuartos). Es opcional, si se omite se tomará como 5.
*   `<numMinimoDeSesiones>`. Indica cuantos tramos como mínimo habrá en un mismo día. Puede tomar valores entre M (1/2) y 4. Además del valor "M" (media duración), "T" (tres cuartos de la duración), "S" (seis cuartos). Es opcional, si se omite se tomará el tramo de duración minima en el marco.
*   `<penalizarBloquesMaximos>`. Indica si se intentará evitar que quede algún día con la cantidad máxima permitida. Es de tipo [booleano](#booleano). Es opcional, por defecto es `false`.
*   `<penalizarBloquesMinimos>`. Indica si se intentará evitar que quede algún día con la asignación en tramos mínima permitida. Es de tipo [booleano](#booleano). Es opcional, por defecto es `false`.
*   `<admitirBloquesDiscontinuos>`. Indica si se permite que se intercalen otras sesiones entre los tramos de un mismo día. Es de tipo [booleano](#booleano). Es opcional, por defecto es `false`.
*   `<distribucionInicial>`. Opcional. Es igual que el elemento [`<distribucionFija>`](#distribucionFija). Indica la distribución inicial de la sesión que se mostrará en el planificador.

Un ejemplo sería:

```
<distribucionSemanal>  
	<distribucionVariable>  
		<numSesiones>5</numSesiones>  
		<numMaximodeSesiones>3</numMaximoDeSesiones>  
	</distribucionVariable>  
</distribucionSemanal>
```

El ejemplo indica que la sesión se compone de 5 tramos semanales, y que se pueden distribuir teniendo como máximo 3 tramos en un mismo día. Además dado que no se indica ningún parámetro opcional, en los casos de que haya más de 1 tramo en un mismo día, estos se deben dar de forma seguida (sin intercalos con otras sesiones).

Así el ejemplo nos daría lugar a siguiente lista de distribuciones: 11111, 2111, 221, 311, 32 y si además hay duración fraccionada: 111SM, 11SS, 21SM, etc. Como se puede ver también se podría haber puesto con una distribución personalizada, pero es mucho más comodo usar la distribución variable, además de que permite más opciones (evitar bloque máximos, sueltas, etc).

Información básica sobre el XML
-------------------------------

### Contenido de los elementos

Los elementos pueden tener tres tipos de contenido: Los atributos, los subelementos y el valor.

Los atributos se declaran en la etiqueta de apertura de un elemento y da igual en que orden se coloquen, siempre y cuando se les separe correctamente (mediante un espacio) y vayan detras del nombre de la etiqueta. El atributo se forma con el siguiente patrón `_atributo_="_valor_"` , donde "_atributo_" es el nombre del atributo, y "_valor_" es lo que se quiere asignar al atributo. El valor **siempre** debe ir entre comillas, ya sean dobles ( `"` ) o simples ( `'` ).

Los subelementos son los elementos que se declaran entre las etiquetas de apertura ( `<elemento>` ) y las de cierre ( `</elemento>` ) es decir `<elemento><subelemento /></elemento>.` Un subelemento es un elemento con lo que puede tener a su vez más subelementos.

Por último también pueden contener un valor. El valor es todo aquello que se escribe entre los elementos de apertura y de cierre, pero que no forme un elemento (subelemento), es decir el texto sin más. Por ejemplo `<elemento>valor</elemento>` , es un elemento que tiene el valor " `valor` ".

Aunque no es lo normal, se pueden mezclar valores y subelementos. Por ejemplo: `<cabecera>Vendido a 500<simboloEuro /> el <fecha>12/12/2012</fecha> a la dirección de correo electrónico <correo>anonimous@neverland.com</correo>.</cabezera>` . Contiene un texto en el que se intercalan los elementos `<fecha>` , `<correo>` , y `<simboloEuro>` , a su vez los subelementos `<fecha>` y `<correo>` tienen sus propios contenidos.

### Tipos de los valores

En el xml hay cierto tipos de valores predefinidos, entro los más comunes son:

* <a name="string"></a>  **string**. Indican una cadena de texto. Pueden contener todo tipo de caracteres, (letras, acentos, "ñ", números, etc). Los caracteres especiales, "<" y el ">", se deben poner mediante las secuencias de escape "&lt;" y "&gt;" respectivamente (sin comillas).
* <a name="booleano"></a>  **booleano**. Indica un tipo que solo pueden tomar dos valores, `true` (verdad, sí) y `false` (falso, no). Deben ponerse en inglés, no se reconoce si se pone sus equivalentes españoles (verdad, falso, sí, no). Normalmente, al poner `true` se acepta la condición del elemento, y con `false` se indica que se desactiva.
* <a name="NombreType"></a>  **NombreType**. Es un tipo personalizado definido en el xsd que restringe un string. Tiene un mínimo de 1 caracter y un máximo de 30.
* <a name="AbreviaturaType"></a>  **AbreviaturaType**. Es un tipo personalizado definido en el xsd que restringe un string. Tiene un mínimo de 1 caracter y un máximo de 20.
* <a name="NombreCompletoType"></a>  **NombreCompletoType**. Es un tipo personalizado definido en el xsd que restringe un string. Tiene un mínimo de 1 caracter y un máximo de 50.
* <a name="NCName"></a>  **NCName**. Que es una restricción del tipo [string](#string). Puede contener una cadena de texto sin caracteres especiales ("/", "\*", ".", ",", etc) y que comienza con una letra, aunque puede contener números.
* <a name="Email"></a>  **Email**. Es un tipo personalizado definido en el xsd que restringe un string. Tiene que tener la forma de una dirección de email, es decir xxxx@xxxxx.xxx
* <a name="time"></a>  **time**. Este tipo es utilizado para indicar horas de un día. Utiliza el formato `hh:mm:ss[Z|(+|-)hh:mm]`. La parte encerrada entre "`[`" y "`]`" es opcional y se debe colocar "`Z`" (indica hora zulu) o un signo (ya sea `+` o `-`) seguido de las horas de diferencia horaria. Todos los dígitos son obligatorios. Por ejemplo, valores válidos son: `10:00:00`, `22:00:12.123`, `02:33:00Z`, `05:01:01+05:00`, `01:00:00-08:30`. Valores inválidos serían: `1:00:30` (falta un dígito en la hora), `-10:00:00` o `25:00:00` (fuera de rango), `05:00:00Z+01:00` (no se pueden especificar la Z y la diferencia horaria a la vez), `22:30` (faltan los segundos).
* <a name="entero"></a>  **entero**. Son los números enteros, -464216468, -5, -4, 0, 1, 3, 265433169, etc.
* <a name="nonNegativeInteger"></a>  **nonNegativeInteger (entero no negativo)**. Es una restricción del tipo [entero](#entero) en el que solo se permiten los valores mayores o iguales que 0.
* <a name="positiveInteger"></a>  **positiveInteger (entero positivo)**. Es una restricción del tipo [`nonNegativeInteger`](#nonNegativeInteger) en el que no se permite el 0. Es decir es un entero mayor (estricto) que 0.
* <a name="int"></a>  **int**. Es un entero de 32 bits con signo. Su rango de volores permitidos va desde -2147483648 hasta 2147483647 (ambos inclusive).
* <a name="unsignedInt"></a>  **unsignedInt**. Es una restricción del tipo unsignedLong (un entero sin signo de 64 bits) con un tamaño de 32 bits que solo permite valores desde 0 al 4294967295 (ambos inclusive).
* <a name="unsignedShort"></a>  **unsignedShort**. Es una restricción del tipo [unsignedInt](#unsignedInt), con un tamaño de 16 bits que solo pertime valores desde el 0 al 65535 (ambos inclusive).
* <a name="unsignedByte"></a>  **unsignedByte**. Es una restricción del tipo [unsignedShort](#unsignedShort) con un tamaño de 8 bits que solo pertime valores desde el 0 al 255 (ambos inclusive).
* <a name="decimal"></a>  **decimal**. Es tipo generál numérico. Permite tener valores decimales; 5, -1, 153.82, -954385.045. Se usa el punto como separador decimal.
* <a name="float"></a>  **float**. Es el float definido por el IEEE, un numero decimal en coma flotante de precisión simple de 32bits. Permite valores como: 5, -1, 153.82, -952.1, 523e-10, 0.001e3. Se usa el punto como separador decimal y la e o E para separar el exponente.
* <a name="Horas"></a>  **Horas**. Es un restricción del tipo [unsignedInt](#unsignedInt), que sólo permite valores del 0 al 23 (ambos inclusive).

### Más información sobre XML

También puede consultar la información en la web sobre XML.

Puede ver una pequeña introducción (en español) en la enciclopedia libre (wikipedia) localizada en la página [http://es.wikipedia.org/wiki/XML.](http://es.wikipedia.org/wiki/XML)

Tiene una guía sobre xml (en inglés) en [http://www.w3schools.com/xml/default.asp](http://www.w3schools.com/xml/default.asp).

También puede consultar la página principal de la definición del XML de su versión 1.0 (en inglés) en [http://www.w3.org/TR/xml/](http://www.w3.org/TR/xml/).

Documentación adicional
-----------------------

Además tiene una lista de los elementos y su uso en la página [elementos.xml](elementos.md "Definición de elementos").

Puede ver la lista de cambios en el formato en la página [cambios.md](cambios.md).