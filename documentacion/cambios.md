Historial de cambios en el formato xml del GHC
==============================================

En este documento se puede ver un historial con los cambios en el formato xml del Generador de Horarios a partir de la versión 20130514.

En los cambios se omite (de no ser necesario su mención) que el número de versión también se ha actualizado. Por ejemplo, para los cambios de la versión 20130514, se omite que el xml tendrá la versión 20130514.


Cambios de la versión 20250509
------------------------------

Fecha de publicación 09/05/2025

Ahora la etiqueta de los grupos `<profesorTutor>` permite de forma opcional incluir los atributos `imparteAPrimeras` y/o `imparteAUltimas`, que son de tipo `boolean`.

Permite que el motor intente optimizar que el tutor del grupo tenga asignada clase con su grupo a primera y última hora.

Cambios de la versión 20250304
------------------------------

Fecha de publicación 04/03/2024

Los grupos ahora incorporan de forma opcional la etiqueta `<limiteOcupacionDia>` que permite indicar un máximo de intervalos al día para el grupo.

Cambios de la versión 20240701
------------------------------

Fecha de publicación 02/10/2024

Los profesores ya no son obligatorios dentro de la etiqueta ``<aula> `de los tramos de resultado.` ``

Cambios de la versión 20240701
------------------------------

Fecha de publicación 01/07/2024

Se añade el atributo opcional de las sesiones . A partir de ahora se integra dentro de `<opciones></opciones> `de `<sesion>`.

Cambios de la versión 20240619
------------------------------

Fecha de publicación 19/06/2024

Se añaden el atributo opcional `<sinCambioAula>`. Que puede tener valores `true` o `false`.

Indica si deben asignarse todas las horas de la sesion en el mismo aula de forma estricta. No importará si se asigna el aula principal o un aula del conjunto alternativo (si hubiera), pero deberá ser el mismo para toda la sesion.

Cambios de la versión 20240618
------------------------------

Fecha de publicación 18/06/2024

Se añaden el atributo opcional `estricto`. Que puede tener valores `true` o `false` en las etiquetas:`

- `<maximasHorasSeguidas>`
- `<penalizarAlrededorGuardiaRecreo>`

Se inlcuyen para permitir que estas condiciones se puedan indicar como obligatorias.

Cambios de la versión 20231212
------------------------------

Fecha de publicación 12/12/2023

Se añaden dos nuevas etiquetas dentro de <tarea>. Son opcionales y su valor puede ser `true` o `false`. Su ausencia será interpretada como `undefined`.

Estas etiquetas son:

* `<requiereMateria>`
* `<requiereGrupo>`

Sirven para validar si el tipo de tarea o actividad se puede asignar a las lectivas, con grupo y materia, o a las actividades del profesorado sin grupo de alumnos ni materia. También pueden ser tareas sin materia, pero con profesor y grupo, por ejemplo las tutorías. En caso de no informarse, simplemente no se realizaría validación alguna al respecto.

Ejemplo:

    
    			<tarea>
    				<nombre>LEC</nombre>
    				<requiereMateria>true</requiereMateria>
    				<requiereGrupo>false</requiereGrupo>
    			</tarea>
    		

Cambios de la versión 20230831
------------------------------

Fecha de publicación 31/08/2023

Cauando se define otro profesor en el aula, asociado a una materia distinta a la principal con un elemento `<otraMateriaProfesor>`, ahora se puede indicar, de forma opcional una tarea distinta a la principal de la sesión lectiva.

Ejemplo:

    
    			<otrasMateriasProfesores>				
    				<otraMateriaProfesor tarea="PDC">
    					<profesor>Nuria</profesor>
    					<materia>Lengua PDC</materia>
    				</otraMateriaProfesor>				
    			</otrasMateriasProfesores>
  

Cambios de la versión 20230206
------------------------------

_Fecha de publicación 06/02/2023_

Se aumenta la duración posible de la sesiones a 7 intervalos diarios, **solo en distribuciones variables**. Cambio de valores posibles en elemento `DuracionesType` y creacion del elemento `DuracionesDistFijaType` para limitar a 5 la duración de las sesiones en las distribuciones no variables (fija y personalizada).

El nuevo máximo de duración afecta a los campos `<numMaximoDeSesiones>`, `<numMinimoDeSesiones>`y `<numSesiones>` de las distribuciones variables. Dentro de la etiqueta `<distribucionVariable>`

Cambios de la versión 20220520
------------------------------

_Fecha de publicación 20/05/2022_

Los Grupos, dentro de su etiqueta `<grupo>`, ahora incluyen la etiqueta `<eliminarHuecos></eliminarHuecos>`, cuyo valor por defecto cuando no venga informada será `true`. Esto permite indicar que no se trabaje en tratar de compactar los horarios de los subgrupos o grupos compartidos, y solo se haga en los grupos reales o académicos.

Cambios de la versión 20220324
------------------------------

_Fecha de publicación 24/03/2022_

Los grupos pueden incluir una lista de grupos incluidos

Ejemplo:

    
    			<grupo>				
    				....
    				<nombre>1ºETICA</nombre>
    				....
    				<gruposIncluidos>
    					<grupoIncluido>1ºA</grupoIncluido>
    					<grupoIncluido>1ºB</grupoIncluido>
    				</gruposIncluidos>				
    			</grupo>
    		

De esta forma pueden crearse grupos circunstanciales, formados por alumnos de varios grupos reales, que se junten para recibir docencia de una determinada materia o materias en común. Esto puede facilitar el intercambio con algunos gestores académicos.

En `SesionLectivaType`. Dentro de la etiqueta `<grupo>`, que puede encontrarse en `<otrosGrupos>`, o bien `<materiaGrupo>` (dentro de `<otrasMateriasGrupos>`), se añade el atributo `autogenerado`, que vendra informado a _true_ cuando el grupo incluido se haya añadido automaticamente por ser un grupo incluido del grupo principal. Este atributo por defecto es _false_.

Cambios de la versión 20220222
------------------------------

_Fecha de publicación 22/02/2022_

En las distribuciones variables ahora se puede detallar el número de intervalos mímino que debe de asignar en el día una distribución variable. Esto se indica mediante la etiqueta `numMinimoDeSesiones`. Dentro de esta etiqueta se pueden indicar los valores `M`, `T`, `1`, `S`, `2`, `3` o `4`. Depenediendo de si el marco y el total de horas de la sesión son coherentes con estos valores. Los valores `M`, `T` y `S` se corresponden con los valores para tramos fraccionados de 1/2, 3/4 y & (1+1/2) respectivamente.

También se añade la etiqueta `penalizarBloquesMinimos`, que permite optimizar el horario evitando que dentro de lo posible en la sesión se eviten las distribuciones de duración menor según el marco.

Cambios de la versión 20220114
------------------------------

_Fecha de publicación 14/01/2022_

Corrección sobre el tipo de dato en elemento `profesor` dentro de `otraMateriaProfesor`. Se establece de tipo `NombreType`.

Cambios de la vesión 20220112
-----------------------------

_Fecha de publicación 12/01/2022_

Se añade la subetiqueta `otrasMateriasProfesores` a la etiqueta [sesión lectiva](elementos.md#) .Indica las otras materias impartidas por otros profesores en el aula,que se incluirán el orden definido en el planificador. Si los otros profesores en el aula imparten la misma materia que el profesor principal se debe usar otrosProfesores.

Ejemplo: `<otrasMateriasProfesores> <otraMateriaProfesor> <profesor> Jose </profesor> <materia> Lengua </materia> </otraMateriaProfesor> </otrasMateriasProfesores>`

Cambios de la versión 20210506
------------------------------

_Fecha de publicación 06/05/2021_

Se añade el atributo opcional `claveX` a varios subelementos de la [sesión lectiva](elementos.md#) del tipo de "otroElemento". Este elemento sirve para guardar información adicional para aplicaciones externas, como pudiera ser un grupomateria diferente al de la sesión principal. El valor en caso de estar presente será una cadena de texto que puede representar cualquier valor necesario por la aplicación externa.

Por ejemplo:

*   `<otrasMateriasGrupos><materiaGrupo claveX="">...`
*   `<otrosGrupos><grupo claveX="">...`
*   `<otrosProfesores><profesor claveX="">...`
*   `<otrasMaterias><materia claveX="">...`
*   `<otrasAulas><otraAula claveX="">...`

También se ha agregado el elemento `<origenDatos>` al elemento `<datosGHC><otros>` . Este elemento permite guardar de forma opcional un identificador que indicaría la aplicación desde la que se obtuvieron los datos, por ejemplo el gestor académico del que se importó.

Cambios de la versión 20200505
------------------------------

_Fecha de publicación 05/05/2020_

Cambios en el Profesor:

*   Se añade la etiqueta `<salirUltimaEntrarPrimeraLunes>` a las [`incompatibilidades entre sesiones del profesor`](elementos.md#incompatibilidadEntreSesiones), para permitir diferenciar el tiempo de descanso, que debe de haber entre que sale a ultima hora el viernes y entra a primera el lunes el Profesor, de la distancia indicada para el resto de días de la semana.
    

_Para indicar el tiempo de descanso entre ultima hora de un día y primera del siguiente, del resto de días de la semana, ya exístia la etiqueta etiqueta `<salirUltimaEntrarPrimera>` en [`incompatibilidades entre sesiones del profesor`](elementos.md#incompatibilidadEntreSesiones)._

Cambios en el elemento `DiaLectivoType` (en XSD):

*   La modificación del esquema permite indicar días lectivos ( `DiaLectivoType` en XSD) hasta el valor máximo de 35 _(inclusive)_. Esto permite definir horarios de lunes a sábado de hasta 6 semanas/periodos [(Para horarios de varias semanas ver información sobre `<periodos>`)](elementos.md#periodos) .

Cambios de la versión 20200415
------------------------------

_Fecha de publicación 15/04/2020_

Se han cambiado las [`opciones de los profesores`](elementos.md#opcionesDeProfesor) para que se puedan diferenciar máximos y mínimos diarios de ocupación y de Sesiones Lectivas. Los máximos y mínimos de ocupación se refieren a la duración del docente con la suma de Sesiones Lectivas, y aquellas Sesiones No Lectivas que se ha indicado en el planificador que se desean contabilizar para la ocupación.

Para esta modificación se añaden las etiquetas:

*   `<considerarMaximasHorasDiariasSolamenteLectivas>`: Indica cómo se debe considerar el número máximo de horas diarias en las el profesor imparte sesiones lectivas.
*   `<valorMaximasHorasCalculadoSolamenteLectivas>`: Indica cómo se ha actualizar el valor del número de horas diarias máximo que el profesor puede impartir sesiones lectivas.
*   `<considerarMinimasHorasDiariasSolamenteLectivas>`: Indica cómo se debe considerar el número mínimo de horas diarias definidas en las que el profesor imparte sesiones lectivas.
*   `<valorMinimasHorasCalculadoSolamenteLectivas>`: Indica cómo se ha de actualizar el valor del número de horas diarias mínimo que el profesor puede impartir sesiones lectivas.

Sobre las siguientes etiquetas ya existentes, no sufren variación y ahora representan las preferencias los intervalos máximos y mínimos de **ocupación** del docente. La ocupación diaria del docente se considera las Sesiones Lectivas que imparte, más las No Lectivas que se ha indicado en el planificador que deben computar como tal.

*   `<considerarMaximasHorasDiariasSolamenteLectivas>`
*   `<valorMaximasHorasCalculadoSolamenteLectivas>`
*   `<considerarMinimasHorasDiariasSolamenteLectivas>`
*   `<valorMinimasHorasCalculadoSolamenteLectivas>`: En este caso el valor `minimizarDiasOcupados` queda _Deprecated_ debido al siguiente cambio que se introduce.

Se añade otra nueva etiqueta a las [`opciones de los profesores`](elementos.md#opcionesDeProfesor) para indicar si se quiere intentar minimizar los días con clase del docente buscando días libres en la optimización (true), o no (false). Esta opción es compatible con los máximos y mínimos del profesor, que se comprobarían solo en los días que no quedaran libres. Este nuevo elemento es:

*   `<minimizarDiasOcupados>`

Aunque se mantiene como _Deprecated_ por compatibilidad, este elemento hace innecesario el valor `minimizarDiasOcupados` del elemento `<valorMinimasHorasCalculadoSolamenteLectivas>` .

Cambios de la versión 20190729
------------------------------

_Fecha de publicación 29/07/2019_

Se han cambiado las [`opciones de los profesores`](elementos.md#opcionesDeProfesor) para que sea una secuencia y que permita que los elementos `intervalosDePermanenciaSemanales` e `intervalosDePermanenciaDiarios` pudan ser duplicados (uno para la versión estricta y el otro para la versión ponderable).

**Advertencia:** Se mantiene el número de versión 20190612.

Cambios de la versión 20190612
------------------------------

_Fecha de publicación 12/06/2019_

Se ha movido el elemento [`periodos`](elementos.md#periodos) delante del elemento [`marcos`](elementos.md#marcosDeHorario) para permitir una lectura más secuencial del xml.

Cambios de la versión 20190514
------------------------------

_Fecha de publicación 14/05/2019_

Nuevo elemento del esquema **periodos**

En profesores

*   Nuevo atributo **minutos** al elemento **menosDeDosIntervalosLibres**

En grupos

*   **noAdmiteHuecos**
*   **huecosEnNoPreferentes**

En reuniones, los nuevos elementos:

*   **distribucionPeriodica**
*   **mismaPosicionDistintosPeriodos**

En guardias, los nuevos elementos:

*   **enPeriodos**
*   **mismaPosicionDistintosPeriodos**

En sesiones complemantarias, los nuevos elementos:

*   **distribucionPeriodica**
*   **mismaPosicionDistintosPeriodos**

En sesiones lectivas, los nuevos elementos:

*   **distribucionPeriodica**
*   **mismaPosicionDistintosPeriodos**
*   **noCoincidentes** (de relación entres sesiones)
*   **previoA** (de relación entres sesiones)
*   **posteriorA** (de relación entres sesiones)
*   **separadosNDiasOMas** (de relación entres sesiones)
*   **separadosNDiasOMenos** (de relación entres sesiones)

Cambios de la versión 20170606
------------------------------

_Fecha de publicación 06/06/2017_

Se amplía la longitud del tipo `NombreType` de 12 a 30 caracteres, pues había gestores que necesitaban que este campo fuese más grande. También se cambia el campo _departamento_, en el [profesor](elementos.md#profesor) que estaba limitado a 25, para que también pueda hacer referencia a departamentos, que pueden tener un nombre de hasta 30 caracteres.

Se añade el campo _NombreCompleto_ a los grupos, para que puedan definir un nombre mayor de lo que permite su campo nombre.

Actualiza en distintos sitios el número máximo de elementos a crear, como en [PeriodosLibres](elementos.md#periodosLibres), [PeriodosLibresJornadaPartida](elementos.md#periodoLibreJornadaPartida) o [Reuniones](elementos.md#reunion). En ellos, hay un límite que hace referencia al número de días máximos, que antes eran 5, pero se cambió para que pudieran ser 6, con lo que se deben actualizar también sus valores. También actualiza los máximos de `intervalosSemanales` y `maxIntervalosDiarios` de las [Complementarias](elementos.md#complementaria). Por último, modifica el número de sesiones que se pueden definir en `DistribucionType` , para indicar que se pueden dar 6 duraciones, una por cada día, en vez de 5. Pero, aunque todos estos límites se amplien a 6, deben de ser el número máximo de días de los marcos definidos: no tiene sentido indicar 6 si el número de días de los marcos es 5.

Cambios de la versión 20170511
------------------------------

_Fecha de publicación 11/05/2017_

Agregados nuevos elementos y atributos para poder dar más funcionalidad.

*   Agregados atributos para poder identificar de donde procedía el aula asignada en un resultado, ya que hasta ahora podría ser ambiguo si la sesión tenía varios conjuntos con aulas compartidas. Para ello se ha agregado el identificador `origenAula` a las [`otraAula`](elementos.md#otraAula) del listado [otrasAulas](elementos.md#otrasAulas) de las sesiones y se hace referencia a él en el atributo `refAula` del elemento `sesion` de las [`aula`](elementos.md#aulaDeHorario) del resultado. El identificador `0` está reservado para el `refAula` que representa el aula principal de la sesión y por tanto no se puede usar como identificador en `origenAula`.
*   Agregado un nuevo tipo en el esquema, llamado [`Horas`](index.md#Horas) que representa un entero de 0 a 23 (ambos inclusive).
*   Se ha añadido el atributo `nIntervalos` a los elementos `salirUltimaEntrarPrimera` y `entrarPrimeraSalirUltima` de la [`incompatibilidadEntreSesiones`](elementos.md#incompatibilidadEntreSesiones). Este atributo indica el número de intervalos que tiene que haber considerar que se respeta la condición y es del tipo [`Horas`](index.md#Horas).
*   Se ha restringido los valores de `losPrimerosIntervalos`, `losUltimosIntervalos` e `intervalosSeguidos` del [`tipoDeperiodo`](elementos.md#tipoDePeriodo) de los [periodos libres del profesor](elementos.md#periodosLibres), para que sean del tipo `Horas`.
*   Se ha añadido el elemento [`otrosPeriodosLibresJornadaPartida`](elementos.md#otrosPeriodosLibresJornadaPartida) a las [opciones del profesor](elementos.md#opcionesDeProfesor). Este permite definir una lista de [periodos libres de jornada partida](elementos.md#periodoLibreJornadaPartida) que quiere que cumpla el profesor, además del propio elemento periodoLibreJornadaPartida que ya tiene definido en sus opciones. Sólo puede haber un periodoLibreJornadaPartida de cada `tipoDePeriodoLibre`.
*   Añadido el campo `intervalosDePermanenciaDiarios` a las [opciones del profesor](elementos.md#opcionesDeProfesor), para indicar el número de intervalos máximos de permanencia diaria del profesor. Puede ser un criterio estricto, o un criterio de optimización según determine el atributo `estricto`.
*   Añadido el campo `lectiva` a las [complementarias](elementos.md#complementaria) y a las [guardias](elementos.md#guardia) para que las horas de estas sesiones puedan considerarse como lectivas para los profesores que las imparten.
*   Añadido el campo `penalizarAlrededorGuardiaRecreo` a las [opciones del profesor](elementos.md#opcionesDeProfesor). En él indica si se quieren penalizar la existencia de sesiones a ambos lados de una guardia de recreo por parte de un profesor.

Cambios de la versión 20161222
------------------------------

_Fecha de publicación 22/12/2016_

Agregado un nuevo atributo `tipo` al elemento `evitarDobleDesp` .

*   Se ha agregado el atributo `tipo` al elemento `<evitarDobleDesp>` en las [opciones de grupos alejados](elementos.md#opcionesDeGruposAlejados) de las opciones generales. Este nuevo atributo permite hacer que el criterio sea estricto en vez de ponderable.

Cambios de la versión 20160705
------------------------------

_Fecha de publicación 05/07/2016_

Añade el campo `email` (que es siempre opcional) a ciertos elementos

*   Email al elemento `grupo` para poder realizar notificaciones o exportaciones del calendario.
*   Email al elemento `aula` para poder realizar notificaciones o exportaciones del calendario.
*   Email el elemento `departamento`, para tener una manera de notificar la publicación de un archivo desde la plataforma.
*   El elemento `profesor` ya tenía un campo email, pero de tipo String. No se modifica por tema de compatibilidad con versiones antiguas.

Cambios para la compatibilidad con DAE, y adaptación para Captadesidertas y Plataforma

*   Añade el elemento `numeroAlumnos` a los grupos, para indicar cuántos alumnos forman el grupo. Es opcional.
*   Añade el elemento `numeroAlumnos` a las aulas, para indicar cuántos alumnos caben en cada aula. Es opcional.
*   Añade el atributo `numeroAlumnos` al elemento grupo de las sesiones lectivas, para indicar cuántos alumnos de ese grupo reciben esa sesión. Es opcional.
*   Añade el atributo `numeroAlumnos` al elemento grupo del elemento otrosGrupos de las sesiones lectivas, para indicar cuántos alumnos de ese grupo reciben esa sesión. Es opcional.
*   Añade el atributo `numeroAlumnos` al elemento grupo del elemento materiaGrupo de otrasMateriasGrupos, dentro de cada sesión lectiva, para indicar cuántos alumnos de ese grupo reciben esa sesión. Es opcional.

Cambios en los elementos de las opciones del profesor.

*   Ya no se usan los elementos `maximoSesionesDiarias` ni `minimoSesionesDiarias` de las [opciones de los profesores](elementos.md#opcionesDeProfesor). Se marcan como **Deprecated**. No se eliminan para mantener la compatibilidad con versiones anteriores. El motivo de no usarlo es que hay nuevos atributos que sobrescriben su funcionalidad, y la amplían.
*   Se añade el elemento `considerarMaximasHorasDiarias` a las [opciones de los profesores](elementos.md#opcionesDeProfesor). Sirve para indicar cómo se considera la restricción del máximo número de horas diarias que puede impartir un profesor.
*   Se añade el elemento `valorMaximasHorasCalculado` a las [opciones de los profesores](elementos.md#opcionesDeProfesor). Indica cómo se actualiza el valor del máximo número de horas diario del profesor, que se calcula automáticamente según el número de sesiones del profesor.
*   Se añade el elemento `considerarMinimasHorasDiarias` a las [opciones de los profesores](elementos.md#opcionesDeProfesor). Sirve para indicar cómo se considera la restricción del mínimo número de horas diarias que puede impartir un profesor.
*   Se añade el elemento `valorMinimasHorasCalculado` a las [opciones de los profesores](elementos.md#opcionesDeProfesor). Indica cómo se actualiza el valor del mínimo número de horas diario del profesor, que se calcula automáticamente según el número de sesiones del profesor.
*   Se actualiza toda la documentación y el ejemplo.

Cambios de la versión 20150525
------------------------------

_Fecha de publicación 25/05/2015_

Corrección de la documentación.

**Advertencia:** Se mantiene el número de versión 20150513.

*   Se ha actualizado el número de versión del xml en la documentación ya que no se había actualizado con los últimos cambios.

Cambios de la versión 20150513
------------------------------

_Fecha de publicación 18/05/2015_

Version que será usada en GHC 17.

*   Se ha agregado el valor `estricto` al elmento `minimoSesionesDiarias` de las [opciones de los profesores](elementos.md#opcionesDeProfesor). Este nuevo valor indica que el mínimo autocalculado se cumplirá de forma estricta.
*   Se ha agregado el atributo `tipo` a las incompatibilidades entre sesiones de los profesores (subelementos de [`<incompatibilidadEntreSesiones>`](elementos.md#incompatibilidadEntreSesiones)). Con este atributo se puede definir el tipo de incompatibilidad (estricto o solo evitar) de manera individualizada para cada tipo de incompatibilidad.
*   Se ha agregado el atributo `estricto` al elemento `<intervalosDePermanenciaSemanales>` de las [opciones de los profesores](elementos.md#opcionesDeProfesor). Este nuevo atributo permite indicar si la condición de la cantidad máxima de sesiones de permanencia semanal del profesor se debe considerar como estricta o solo como algo a evitar.
*   Ya no se usa el elemento `<minMaxSesiones>` ni `<maxHoraPermanencia>`, subelementos de las [opciones generales](elementos.md#opcionesGenerales). Uso está desaconsejado y serán ignorados por GHC. Esto es debido a que ahora se implementan como restricciones estrictas y por tanto no son necesarios.
*   Ahora se permite un máximo de 4 marcos.
*   Se ha agregado el elemento `<penaCoincidanDespuesDelRecreo>` a los elementos de las [opciones de las sesiones](elementos.md#OpcionesDeSesionType). Este permite que se pueda penalizar el que más del 50% de las horas se asignen después del recreo.
*   Se ha actualizado la documentación del elemento `<permitirImpartanEnDiasSeguidos>` de las [opciones de las sesiones](elementos.md#OpcionesDeSesionType) para hacer más claro que es lo que hace y advertir de su funcionamiento ya que puede ser diferente del esperado.
*   Actualizados los valores por defecto de los elementos de las [opciones de las sesiones](elementos.md#OpcionesDeSesionType) para que sean los mismos de la aplicación.

Cambios de la versión 20141006
------------------------------

_Fecha de publicación 06/10/2014_

Subtareas de las simultaneas.

*   Se ha agregado el atributo opcional `tarea` de tipo `NombreType` a los elementos de las listas: `<otrasMateriasGrupos>`, `<otrosGrupos>`, `<otrosProfesores>`, `<otrasMaterias>`, `<otrasAulas>`; del tipo [`SesionLectivaType`](elementos.md#sesion). Este atributo indica otra tarea que la otra-materia, otro-profesor, etc. tienen como tarea diferente a la de la sesión.

Cambios de la versión 20140710
------------------------------

_Fecha de publicación 10/07/2014_

Más opciones para las reuniones.

*   Agregado el elemento `<lectiva>` a la definición de las reuniones. Permite indicar si la reunión se contará como hora lectiva para los profesores.

Cambios de la versión 20140520
------------------------------

_Fecha de publicación 20/05/2014_

Cambios básicos en profesores.

*   Agregado el elemento `<horarioAsoc>` a la definición de los profesores.

Cambios de la versión 20140512
------------------------------

_Fecha de publicación 12/05/2014_

Correción de errores en la documentación.

**Advertencia:** Se mantiene el número de versión 20140409.

*   Se ha agregado la documentación del atributo _tipo_ del elemento _grupoMateria_ que solo estaba en el xsd.
*   Actualizado el valor de la versión del ejemplo para reflejar el último valor (20140409).
*   Agregada más información de como se usan los elementos `<profesor>` de las [aulas de un horario](elementos.md#aulaDeHorario).

Cambios de la versión 20140409
------------------------------

_Fecha de publicación 09/04/2014_

Correción de errores en la definición y en la documentación.

*   El tipo _NombreType_ ahora tiene un restricción máxima de 12 caracteres.
*   Cambiado el nombre del conjunto de optativas del tipo _NCName_ a _NombreType_.
*   Se han corregido referencias a elementos de tipo _NombreType_ que estaban tipificadas como _string_ o _NCName_. Concretamente el profesor de una sesión y el grupo de un conjunto de optativas.
*   Se ha actualizado la documentación para aclarar que elementos usan el tipo _NombreType_.
*   Actualizado el archivo de documentación index.md para conformarlo a html5.

Cambios de la versión 20131007
------------------------------

_Fecha de publicación 07/10/2013_

Versión inicial del historial de cambios.
