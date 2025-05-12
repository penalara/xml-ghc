
### Índice

* [Inicio.](#Inicio)
* [Índice de elementos.](#%C3%8Dndice)

Elementos por orden alfabético:

* [aula.](#aula)
* [Aula de horario.](#aulaDeHorario)
* [aulas.](#aulas)
* [Bloque de sesiones consecutivas](#bloqueConsecutivas).
* [Bloque de sesiones simultaneas](#bloqueSimultaneas).
* [claveXDias.](#claveXDias)
* [colocarSesionesLectivas.](#colocarSesionesLectivas)
* [complementaria.](#complementaria)
* [complementarias.](#complementarias)
* [conjuntoDeAulas.](#conjuntoDeAulas)
* [consecutivas.](#consecutivas)
* [criterios.](#criterios)
* [curso.](#curso)
* [cursos](#cursos).
* [datosGHC](#datosGHC).
* [Definición de tramo.](#DefinicionDeTramo)
* [departamentos.](#departamentos)
* [DepartamentoType](#departamentoType).
* [distribucionFija.](#distribucionFija)
* [distribucionPeriodica.](#distribucionPeriodica)
* [distribucionPeriodicaFija.](#distribucionPeriodicaFija)
* [distribucionPeriodicaVariable.](#distribucionPeriodicaVariable)
* [distribucionPersonalizada.](#distribucionPersonalizada)
* [distribucionSemanal.](#distribucionSemanal)
* [distribucionSemanalReducida.](#distribucionSemanalReducida)
* [distribucionVariable.](#distribucionVariable)
* [DuracionesTramoType](#duracionesTramoType)
* [DuracionesType](#duracionesType)
* [enPeriodos](#enPeriodos)
* [enDistintoDia.](#enDistintoDia)
* [extensiones.](#extensiones)
* [funcionesAdicionales.](#funcionesAdicionales)
* [general.](#otroConjunto)
* [grupo.](#grupo)
* [grupos](#grupos).
* [gruposAlejados.](#gruposAlejados)
* [guardia.](#guardia)
* [Guardia de horario.](#guardiaDeHorario)
* [guardias](#guardias).
* [haciaDesideratas.](#haciaDesideratas)
* [horario](#horario).
* [horarioDeProfesores.](#horarioDeProfesores)
* [huecosEnHorario.](#huecosEnHorario)
* [Incompatibilidad entre sesiones.](#incompatibilidadEntreSesiones)
* [Integrante de guardia](#integranteDeGuardia).
* [Integrantes de guardia.](#integrantesDeGuardia)
* [Integrantes de reunión.](#integrantesDeReunion)
* [listasDeRelacion](#listasDeRelacion).
* [Lista de grupos alejados.](#listaDeGruposAlejados)
* [marcoHorario](#marcoHorario).
* [marcosDeHorario](#marcosDeHorario).
* [materia.](#materia)
* [materiaGrupo](#parMateriaGrupo).
* [materias](#materias).
* [mensajesIntercambio.](#mensajesIntercambio)
* [noCoincidentes.](#noCoincidentes)
* [noConsecutivas.](#noConsecutivas)
* [OpcionesDeGruposAlejados.](#opcionesDeGruposAlejados)
* [OpcionesDeProfesor.](#opcionesDeProfesor)
* [OpcionesDeSesion.](#OpcionesDeSesionType)
* [Optativas](#optativas).
* [otraAula.](#otraAula)
* [otrasAulas](#otrasAulas).
* [otrasMaterias](#otrasMaterias).
* [otrasMateriasGrupos](#otrasMateriasGrupos).
* [otrasMateriasProfesores](#otrasMateriasProfesores).
* [Otras opciones.](#otrasOpciones)
* [otroConjunto.](#otroConjunto)
* [otros](#otros).
* [otrosGrupos](#otrosGrupos).
* [otrosPeriodosLibresJornadaPartida.](#otrosPeriodosLibresJornadaPartida)
* [otrosProfesores.](#otrosProfesores)
* [perfil.](#perfil)
* [periodo.](#periodo)
* [periodos.](#periodos)
* [periodosLibres.](#periodosLibres)
* [PeriodoLibreJornadaPartida](#periodoLibreJornadaPartida).
* [Plantilla.](#PlantillaType)
* [PlantillaPDType.](#PlantillaPDType)
* [PlantillaPDFType.](#plantillaPDFType)
* [PlantillaSinFType.](#plantillaSinFType)
* [porTramo.](#porTramo)
* [posicionesNoPreferentes.](#posicionesNoPreferentes)
* [previoA.](#previoA)
* [posteriorA.](#posteriorA)
* [profesor.](#profesor)
* [profesores](#profesores).
* [profesoresACadaHora.](#profesoresACadaHora)
* [Profesores Intercambiables.](#profesoresIntercambiables)
* [restriccionDePlantilla.](#restriccionDePlantilla)
* [restriccionesCD.](#restriccionesCD)
* [reunion.](#reunion)
* [reuniones.](#reuniones)
* [sesion.](#sesion)
* [Sesiones de los bloques.](#sesionesDeLosBloques)
* [Sesiones en distinto día.](#sesionesDistintoDia)
* [sesionesLectivas](#sesionesLectivas).
* [SeparacionSesionesType](#SeparacionSesionesType).
* [separadosNDiasOMas](#separadosNDiasOMas).
* [separadosNDiasOMenos](#separadosNDiasOMenos).
* [simultaneas.](#simultaneas)
* [tarea.](#tarea)
* [tareas.](#tareas)
* [Tramo de horario.](#tramoDeHorario)
* [TramoPDType.](#tramoPDType)
* [TramoPDFType.](#tramoPDFType)
* [TramoSinFType.](#tramoSinFType)
* [TramoType.](#tramoType)
* [version.](#version)

Elementos del XML GHC
=====================

Esta página muestra el conjunto de elementos que se usa en la definición del xml de intercambio de la aplicación GHC (Generador de Horarios para Centros).

Puede ver el manual abriendo el archivo [index.html](index.html).

Notas
-----

En los elementos que aparezcan tipificados como obligatorios, indica que deben aparecer 1 vez y no se pueden omitir.

En los elementos que aparezcan tipificados como opcionales, indican que puede aparecer 1 vez o que se puede omitir.

Si puede aparecer un rango distinto de veces, aparecerá su rango como valores entre mín. y máx. ambos valores inclusive en el rango válido.

El tipo del valor de los elementos hojas (que no contienen subelementos) será de tipo [String](index.html#string) a no ser que se indique lo contrario. Además a no ser que se indique lo contrario, en los nombres e identificadores deben tener como mínimo un carácter y un máximo de doce, en los demás elementos es aconsejable que también tengan almenos un carácter (para que no haya confusión de si está vacío o no).

Índice de elementos
-------------------

El siguiente índice muestra los elementos que se pueden usar o están definidos en el esquema del archivo de definición del archivo de intercambio xml de GHC. Para saber más sobre uno de los elementos haga click sobre él, o desplacese la página hasta encontrarlo.

### Por A:

* [aula](#aula).
* [Aula de horario](#aulaDeHorario).
* [aulas](#aulas).

### Por B:

* [Bloque de sesiones consecutivas](#bloqueConsecutivas).
* [Bloque de sesiones simultaneas](#bloqueSimultaneas).

### Por C:

* [claveXDias](#claveXDias).
* [colocarSesionesLectivas](#colocarSesionesLectivas).
* [complementaria](#complementaria).
* [complementarias](#complementarias).
* [conjuntoDeAulas](#conjuntoDeAulas).
* [consecutivas](#consecutivas).
* [criterios](#criterios).
* [curso](#curso).
* [cursos](#cursos).

### Por D:

* [datosGHC](#datosGHC). El elemento raíz del archivo.
* [Definición de tramo](#DefinicionDeTramo).
* [departamentos](#departamentos).
* [DepartamentoType](#departamentoType).
* [distribucionFija](#distribucionFija).
* [distribucionPeriodica](#distribucionPeriodica).
* [distribucionPeriodicaFija](#distribucionPeriodicaFija).
* [distribucionPeriodicaVariable](#distribucionPeriodicaVariable).
* [distribucionPersonalizada](#distribucionPersonalizada).
* [distribucionSemanal](#distribucionSemanal).
* [distribucionSemanalReducida](#distribucionSemanalReducida).
* [distribucionVariable](#distribucionVariable).
* [DuracionesTramoType](#duracionesTramoType)
* [DuracionesType](#duracionesType)

### Por E:

* [enPeriodos](#enPeriodos).
* [enDistintoDia](#enDistintoDia).
* [extensiones](#extensiones).

### Por F:

* [funcionesAdicionales](#funcionesAdicionales).

### Por G:

* [general](#general).
* [grupo](#grupo).
* [grupos](#grupos).
* [gruposAlejados](#gruposAlejados).
* [guardia](#guardia).
* [Guardia de horario](#guardiaDeHorario).
* [guardias](#guardias).

### Por H:

* [haciaDesideratas](#haciaDesideratas).
* [horario](#horario).
* [horarioDeProfesores](#horarioDeProfesores).
* [huecosEnHorario](#huecosEnHorario).

### Por I:

* [incompatibilidadEntreSesiones](#incompatibilidadEntreSesiones).
* [Integrante de guardia](#integranteDeGuardia).
* [Integrantes de guardia](#integrantesDeGuardia).
* [Integrantes de reunión](integrantesDeReunion).

### Por L:

* [listasDeRelacion](#listasDeRelacion).
* [Lista de grupos alejados](#listaDeGruposAlejados).

### Por M:

* [marcoHorario.](#marcoHorario)
* [marcosDeHorario](#marcosDeHorario).
* [materia](#materia).
* [materiaGrupo](#parMateriaGrupo).
* [materias](#materias).
* [mensajesIntercambio](#mensajesIntercambio).

### Por N:

* [noCoincidentes](#noCoincidentes).
* [noConsecutivas](#noConsecutivas).

### Por O:

* [Opciones de grupos alejados](#opcionesDeGruposAlejados).
* [Opciones de profesor](#opcionesDeProfesor).
* [Opciones de sesión](#OpcionesDeSesionType).
* [Optativas](#optativas).
* [otraAula](#otraAula).
* [otrasAulas](#otrasAulas).
* [otrasMaterias](#otrasMaterias).
* [otrasMateriasGrupos](#otrasMateriasGrupos).
* [otrasMateriasProfesores](#otrasMateriasProfesores).
* [Otras opciones](#otrasOpciones).
* [otroConjunto](#otroConjunto).
* [otros](#otros).
* [otrosGrupos](#otrosGrupos).
* [otrosPeriodosLibresJornadaPartida.](#otrosPeriodosLibresJornadaPartida)
* [otrosProfesores.](#otrosProfesores)

### Por P:

* [perfil](#perfil).
* [periodo](#periodo).
* [periodos](#periodos).
* [periodosLibres](#periodosLibres).
* [periodoLibreJornadaPartida](#periodoLibreJornadaPartida).
* [Plantilla](#PlantillaType).
* [PlantillaPDType](#PlantillaPDType).
* [PlantillaPDFType](#plantillaPDFType).
* [PlantillaSinFType](#plantillaSinFType).
* [porTramo](#porTramo).
* [posicionesNoPreferentes](#posicionesNoPreferentes).
* [previoA](#previoA).
* [posteriorA](#posteriorA).
* [profesor](#profesor).
* [profesores](#profesores).
* [profesoresACadaHora](#profesoresACadaHora).
* [profesoresIntercambiables](#profesoresIntercambiables).

### Por R:

* [restriccionDePlantilla](#restriccionDePlantilla).
* [restriccionesCD](#restriccionesCD).
* [reunion](#reunion).
* [reuniones](#reuniones).

### Por S:

* [sesion](#sesion).
* [Sesiones de los bloques](#sesionesDeLosBloques).
* [Sesiones en distinto día](#sesionesDistintoDia).
* [sesionesLectivas](#sesionesLectivas).
* [SeparacionSesionesType](#SeparacionSesionesType).
* [separadosNDiasOMas](#separadosNDiasOMas).
* [separadosNDiasOMenos](#separadosNDiasOMenos).
* [simultaneas](#simultaneas).

### Por T:

* [tarea](#tarea).
* [tareas](#tareas).
* [Tramo de horario](#tramoDeHorario).
* [TramoPDType](#tramoPDType).
* [TramoPDFType](#tramoPDFType).
* [TramoSinFType](#tramoSinFType).
* [TramoType](#tramoType).

### Por V:

* [version](#version).

datosGHCC
---------

Es el elemento raíz del archivo de intercambio y debe ir justo después de la colocación de la declaración del tipo de archivo xml.

Tiene dos atributos:

* `xmlns:xsi` que define el espacio xsi, que está definido en la dirección de su valor. Su valor debe ser siempre `"http://www.w3.org/2001/XMLSchema-instance"` que indica la ruta de los elementos estandares de los xml. Es obligatorio.
* `xsi:noNamespaceSchemaLocation` que define los elementos sin un espacio declarado. Todos los elementos propios al formato de GHC, no tienen un nombre declarado. Su valor será la ruta al esquema, por ejemplo `"./GHCFile.xsd"` que indica que el esquema que valida los elementos sin un nombre de espacio está en el mismo directorio que el xml y el archivo se llama GHCFile.xsd. No es necesario poner este elemento, sobre todo si no se va a validar el xml.

Puede contener los siguientes elementos (en orden):

* [`<version>`](#version). Obligatorio.
* [`<periodos>`](#periodos). Opcional, indica los periodos en que se agrupan los días del horario. Si no se define el elemento, se considera que todos los días pertenecen al mismo periodo.
* [`<marcosDeHorario>`](#marcosDeHorario). Obligatorio (para generar un horario).
* [`<aulas>`](#aulas). Opcional, se debe declarar algún aula para generar un horario (se pueden declarar en el conjunto de aulas de forma anónima).
* [`<conjuntoDeAulas>`](#conjuntoDeAulas). Opcional, se debe declarar algún aula para generar un horario.
* [`<tareas>`](#tareas). Obligatorio (para crear sesiones, guardias, etc).
* [`<departamentos>`](#departamentos). Opcional.
* [`<profesores>`](#profesores). Obligatorio (para crear sesiones, guardias, etc).
* [`<materias>`](#materias). Obligatorio (para crear sesiones).
* [`<grupos>`](#grupos). Obligatorio (para crear sesiones).
* [`<cursos>`](#cursos). Opcional.
* [`<sesionesLectivas>`](#sesionesLectivas). Obligatorio para generar un horario.
* [`<listasDeRelacion>`](#listasDeRelacion). Opcional (necesario si las sesiones tienen relaciones).
* [`<reuniones>`](#reuniones). Opcional.
* [`<guardias>`](#guardias). Opcional.
* [`<complementarias>`](#complementarias). Opcional.
* [`<criterios>`](#criterios). Opcional.
* [`<horario>`](#horario). Opcional. Es el resultado del horario y por lo tanto aparecerá si ya se ha generado un horario.
* [`<otros>`](#otros). Opcional.

version
-------

Este elemento (perteneciente al elemento [`<datosGHC>`](#datosGHC)) identifica la versión del archivo de intercambio. La versión actual tiene el valor `20160705` . Aunque solo pueda tener un valor este elemento es obligatorio, ya que permite identificar la versión del formato del xml.

Hay que tener en cuenta que los programas que lean el archivo pueden dar como válido un rango de versiones compatibles, no es necesario que se atengan a una sola versión.

Al ser constante siempre será de la forma `<version>20160705</version>` .

Puede (y debe, para esta versión concreta) contener el valor:

`20160705`

No puede contener ni subelementos ni atributos.

Aparece en:

* [`<datosGHC>`](#datosGHC).

marcosDeHorario
---------------

El elemento &lt;marcosDeHorario&gt; (perteneciente al elemento [`<datosGHC>`](#datosGHC)) contiene la lista de marcos que definen los tramos horarios disponibles.

Contiene los elementos:

* [`<marcoHorario>`](#marcoHorario). De 1 a 4. _En futuras implementaciones se podrá poner más._

Aparece en:

* [`<datosGHC>`](#datosGHC).

marcoHorario
------------

Define un marco horario general, indicado los tramos que lo forman así como su tipo.

Contiene los atributos:

* `id`. Obligatorio. Es de tipo [NCName](index.html#NCName). Es el identificador del marco. Sirve para referenciarlo (e identificarlo) en el xml. Debe ser único en la lista de marcos. Actualmente debe ser `A`, `B`, `C` o `D`.
* `nombre`. Opcional. Tipo [string](index.html#string). Es un nombre descriptivo del marco para facilitar al usuario su identificación.
* `claveX`. Opcional. Tipo [string](index.html#string). Sirve para guardar información adicional usada en la exportación de los resultados pero que no se use en GHC directamente.

Contiene los subelementos:

* `[<tramo>](#DefinicionDeTramo)` . Mín. 0, máx. ∞. Es de tipo [Definición de tramo](#DefinicionDeTramo).

Aparece en:

* `[<marcosDeHorario>](#marcosDeHorario)` .

Definición de tramo
-------------------

El elemento `<tramo>` define un tramo.

La duración del tramo será _horaSalida - horaEntrada_. La hora de entrada no puede ser mayor o igual que la hora de salida.

El trío de elementos: `<submarco>` , `<dia>` e `<indice>` , son el identificador del tramo.

Contiene los subelementos:

* `<submarco>`. Obligatorio. Es de tipo [NCName](index.html#NCName). Es el identificador del marco al que pertenece. Se pone por seguridad y por facilitar su identificación. Debe ser igual al identificador del marco en el que está incluido.
* `<dia>`. Obligatorio. Es de tipo [unsignedByte](index.html#unsignedByte) pero restringido a un valor mínimo de 0 (no se define valor máximo para permitir periodos de cualquier número de días). Indica el día al que pertenece el tramo (0 es Lunes, 1 es Martes, 2 es Miércoles, 3 es Jueves y 4 es Viernes, ...).
* `<indice>`. Obligatorio. Es de tipo [unsignedInt](index.html#unsignedInt). Define el índice del tramo. Debería respetarse el orden de la hora de entrada y el de los tramos, que la primera hora tenga el indice 0, la segunda el 1, etc.
* `<horaEntrada>`. Obligatorio. Es de tipo [time](index.html#time). Indica la hora de inicio del tramo.
* `<horaSalida>`. Obligatorio. Es de tipo [time](index.html#time). Indica la hora de finalización del tramo.
* `<tipo>`. Obligatorio. Puede tener los valores:
    * `lectivo`. Indica que el tramo es de tipo lectivo, en él se colocarán sesiones, etc.
    * `recreo`. Indica que el tramo es un recreo, en él se podrán colocar guardias de recreo.
    * `mediodia`. Indica una parada de mediodía, señalando la división de turnos de mañana y de tarde.
* `<clavX>`. Opcional. Es de tipo [string](index.html#string). Indica una clave que es usado por algunos programas externos para identificar el tramo.
* `<duracion>`. Opcional. Es de tipo [DuracionesTramoType](#duracionesTramoType). Indica la duración (en proporción a los demás tramos) que tendrá este tramo. Por defecto vale `1`.
* `<permitido>`. Opcional. Es de tipo [booleano](index.html#booleano). Indica si el tramo está permitido usarlo (`true`) o prohibido (`false`). Si se omite este elemento se supone que el tramo será permitido.

Aparece en:

* [`<marcoHorario>`](#marcoHorario).

periodos
--------

El elemento `<periodos>` (perteneciente al elemento [`<datosGHC>`](#datosGHC)) contiene la lista de periodos que agrupan a los días del horario. Si no se define el elemento, o ningún [`<periodo>`](#periodo) dentro de él, se considera que todos los días pertenecen al (único) mismo periodo.

Contiene los elementos:

* [`<periodo>`](#periodo). Permite definir los días que pertenecen a cada periodo. Todo día pertenece a un y solo un periodo.

Aparece en:

* [`<datosGHC>`](#datosGHC).

periodo
-------

El elemento `<periodo>` (perteneciente al elemento `[<periodos>](#periodos)`) declara una agrupación de días que pertenece a un mismo periodo.

Contiene los elementos:

* `<nombre>`. Obligatorio (mín. 1, máx. 1). Es de tipo [NombreType](index.html#NombreType). Es el nombre que tendrá el periodo. Es su identificativo, y debe ser único/li>
* `<descripcion>`. Opcional (mín. 0, máx. 1). Es un texto descriptivo indicando de qué se trata el periodo (semana, trimestre, cuatrimestre, ...).
* `<diaFin>`. Obligatorio (mín. 0, máx. 1). Indica el día en que acaba el periodo. Este día está incluido en el periodo. Para saber el día de inicio se coge el siguiente día libre al diaFin menor más cercano a este del resto de periodos (o el primer día de los marcos si este es el periodo con el diaFin menor).

Aparece en:

* [`<periodos>`](#periodos).

aulas
-----

Este elemento ( `<aulas>` , perteneciente al elemento [`<datosGHC>`](#datosGHC)) contiene la lista de las aulas con nombre que están disponibles en el centro. Las aulas con nombre son aquellas aulas que se pueden identificar mediante su nombre.

Contiene los elementos:

* [`<aula>`](#aula). Mín. 0, máx. ∞

Aparece en:

* [`<datosGHC>`](#datosGHC).

aula
----

El elemento `<aula>` (perteneciente al elemento `[<aulas>](#aulas)` ) declara un aula con nombre.

Contiene los elementos:

* `<nombre>`. Obligatorio (mín. 1, máx. 1). Es de tipo [NombreType](index.html#NombreType). Es el nombre que tendrá el aula.
* `<abreviatura>`. Opcional (mín. 0, máx. 1). Es un texto normalmente corto (aunque puede ser más largo que el nombre) para visualizarlo de forma alternativa al nombre según las preferencias del usuario.
* `<descripcion>`. Opcional. Es un texto que agrega una descripción del aula para que el usuario pueda saber más sobre el aula.
* `<dedicada>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `true`. Indica si el aula es dedicada, es decir, que es útil para determinadas actividades, aunque no para uso general.
* `<claveDeExportacion>`. Opcional. Es usado por programas externos para relacionar las referencias.
* [`<plantilla>`](#PlantillaPDType). Opcional. Es una plantilla del tipo [PlantillaPDType](#PlantillaPDType).
* `<email>`. Opcional. Es de tipo [Email](index.html#Email). Asocia al aula una dirección de email, por si se quiere exportar al calendario asociado a ese email.
* `<numeroAlumnos>`. Opcional. Es de tipo [unsignedInt. Indica el número de alumnos que pueden recibir clase en esta aula, es decir, su capacidad. Por defecto vale 0.](index.html#unsignedInt)
[](index.html#unsignedInt)

[Aparece en:](index.html#unsignedInt)

[](index.html#unsignedInt)* [](index.html#unsignedInt)[`<aulas>`](#aulas).

conjuntoDeAulas
---------------

El `<conjuntoDeAulas>` contiene la lista de los conjuntos alternativos de aulas.

Contiene los subelementos:

* [`<general>`](#general). Obligatorio.
* [`<otroConjunto>`](#otroConjunto). Mín. 0, máx. ∞.

Aparece en:

* [`<datosGHC>`](#datosGHC).

general
-------

Es elemento `<general>` declara el conjunto de aulas de proposito general. En él se incluirán las aulas que puedan ser usadas para cualquier materia.

Tiene los atributos:

* `nombre`. Opcional. Es de tipo [NombreType](index.html#NombreType). El nombre deberá tener siempre el valor "general".
* `sinDeclarar`. Opcional. Es de tipo [unsignedInt](index.html#unsignedInt). Por defecto vale `0`. Indica cuantas aulas sin nombre contiene el conjunto general.

Contiene los subelementos:

* `<aula>`. Mín. 0, máx. ∞. Es de tipo [NombreType](index.html#NombreType). Cada elemento aula, contiene (como valor) el nombre de un aula de la [lista de aulas](#aulas), la cual pertenece al conjunto de aulas general.

Aparece en:

* [`<conjuntoDeAulas>`](#conjuntoDeAulas).

otroConjunto
------------

El elemento `<otroConjunto>` declara un conjunto de aulas alternativas. Sirve para poder agrupar aulas alternativas que puedan cumplir la misma función, como por ejemplo laboratorios de informática o talleres de tecnología.

Tiene los atributos:

* `nombre`. Obligatorio. Es de tipo [NombreType](index.html#NombreType). El nombre que identifica al conjunto de aulas.
* `sinDeclarar`. Opcional. Es de tipo [unsignedInt](index.html#unsignedInt). Por defecto vale `0`. Indica cuantas aulas sin nombre contiene el conjunto declarado.

Contiene los subelementos:

* `<aula>`. Mín. 0, máx. ∞. Es de tipo [NombreType](index.html#NombreType). Cada elemento aula, contiene (como valor) el nombre de un aula de la [lista de aulas](#aulas), la cual pertenece al conjunto de aulas declarado.

Aparece en:

* [`<conjuntoDeAulas>`](#conjuntoDeAulas).

tareas
------

El elemento `<tareas>` declara la lista de tareas disponibles. Como mínimo se debe declarar una tarea, ya que todas las sesiones tienen que tener una tarea asignada (normalmente lectiva).

Contiene los subelementos:

* [`<tarea>`](#tarea). Mín. 1, máx. ∞.
* `<lectivaPorDefecto>`. Obligatoria. Tipo [NombreType](index.html#NombreType). Indica el nombre de la tarea que se usará por defecto en las sesiones lectivas y de docencia directa con los alumnos. Esta tarea debe estar declarada en la lista de tareas.
* `<guardiaPorDefecto>`. Obligatoria. Tipo [NombreType](index.html#NombreType). Indica el nombre de la tarea que se usará por defecto en las guardias. Esta tarea debe estar declarada en la lista de tareas.
* `<reunionPorDefecto>`. Obligatoria. Tipo [NombreType](index.html#NombreType). Indica el nombre de la tarea que se usará por defecto en las reuniones. Esta tarea debe estar declarada en la lista de tareas.

Aparece en:

* [`<datosGHC>`](#datosGHC).

tarea
-----

El elemento `<tarea>` define una tarea.

Contiene los subelementos:

* `<nombre>`. Obligatorio. Es de tipo [NombreType](index.html#NombreType). Es el identificador de la tarea. Debe ser único en la [lista de tareas](#tareas). Debe tener 1 carácter como mínimo.
* `<nombreCompleto>`. Opcional. Es de tipo [NombreCompletoType](index.html#NombreCompletoType). Es un texto para que el usuario pueda identificar más fácilmente la tarea y su función.
* `<claveDeExportacion>`. Opcional. Es de tipo [string](index.html#string). Es una cadena de texto usada por programas externos para tener una referencia de la tarea.
* [`<plantilla>`](#plantillaSinFType). Opcional. Es una plantilla del tipo [PlantillaSinFType](#plantillaSinFType).
* `<requiereMateria>`. Opcional. Es de tipo [boolean](index.html#boolean). Indica si es una tarea que debe de asignarse a una materia y profesor.
* `<requiereGrupo>`. Opcional. Es de tipo [boolean](index.html#boolean).Indica si es una tarea que debe de asignarse a un profesor y grupo.

Aparece en:

* [`<tareas>`](#tareas).

departamentos
-------------

El elemento `<departamentos>` declara una lista de los departamentos disponibles.

Contiene los subelementos:

* `<departamento>`. Mín. 0, máx. ∞. Es de tipo [DepartamentoType](#departamentoType).

Aparece en:

* [`<datosGHC>`](#datosGHC).

DepartamentoType
----------------

El elemento `<departamento>` , define un departamento y sus opciones.

Contiene los subelementos:

* `<nombre>`. Opcional. Es de tipo [NombreType](index.html#NombreType). Es el identificador del departamento.
* `<nombreCompleto>`. Opcional. Es de tipo [NombreCompletoType](index.html#NombreCompletoType). Indica un nombre más aclaratorio sobre el departamento que es.
* `<mensajeAlDepartamento>`. Opcional. Es de tipo [string](index.html#string). Indica un mensaje que será mostrado al departamento en el programa de captación de desideratas.
* `<esNuevo>`. Opcional. Es de tipo [booleano](index.html#booleano). Indica si el departamento ha sido creado nuevo en el módulo de capta desideratas.
* `<claveDeExportacion>`. Opcional. Es de tipo [string](index.html#string). Este elemento suele guardar información para que se pueda identificar al departamento por otros programas cuando se exporta una solución.
* `email`. Opcional. Es de tipo [Email](index.html#Email). Asocia al departamento una dirección de email, por si se quiere comunicar algo, o exportar al calendario asocaido a ese email.

Aparece en:

* [`<departamentos>`](#departamentos).

profesores
----------

El elemento `<profesores>` declara la lista de los profesores disponibles. Ya que todas las sesiones necesitan de un profesor, como mínimo debe aparecer un profesor.

Contiene los subelementos:

* `[<profesor>](#profesor)` . Mín. 1, máx. ∞.

Aparece en:

* [`<datosGHC>`](#datosGHC).

profesor
--------

El elemento `<profesor>` declara un profesor.

Contiene los elementos:

* `<nombre>`. Obligatorio. Tipo [NombreType](index.html#NombreType). Es el identificador del profesor.
* `<abreviatura>`. Opcional. Tipo [AbreviaturaType](index.html#AbreviaturaType). Es un nombre corto para representar al profesor.
* `<nombreCompleto>`. Opcional. Es de tipo [NombreCompletoType](index.html#NombreCompletoType). Es una forma larga de describir al profesor para que al usuario le resulte más fácil reconocerlo.
* `<departamento>`. Opcional. Es de tipo [NombreType](index.html#NombreType). El nombre del departamento al que pertenece el profesor. Hay que tener en cuenta que se distinguen mayúsculas y minúsculas, así como letras acentuadas (con lo que son distintas Matemáticas, Matematicas y matemáticas).
* `<claveDeExportacion>`. Opcional. Es una cadena de texto usada por programas externos para tener una referencia de la tarea.
* `<tomaDePosesion>`. Opcional. Indica la toma de posesión del profesor (usado por algunos programas externos).
* [`<plantilla>`](#plantillaSinFType). Opcional. Es una plantilla del tipo [PlantillaSinFType](#plantillaSinFType).
* [`<opciones>`](#opcionesDeProfesor). Opcional. Si no aparece se toman los valores por defecto de todas las opciones. Es del tipo de [Opciones de profesor](#opcionesDeProfesor).
* `<practicasDeFP>`. Opcional. De tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si el profesor imparte prácticas de FP.
* `<reduccionCargaLectiva>`. Opcional. Es de tipo [entero](index.html#entero). Por defecto vale _0_. Indica la cantidad de sesiones de reducción de carga lectiva que tiene el profesor.
* `<mensaje>`. Opcional. Es de tipo [string](index.html#string). Indica el texto de respuesta del profesor con las preferencias recogidas.
* `<esNuevo>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale _false_. Indica si el profesor se agregó en el captadesideratas y que lo mismo es necesario revisar si es correcto.
* `<prioridad>`. Opcional. Es de tipo [entero](index.html#entero). Por defecto vale _0_. Especifica un valor que indica cuan importante es hacer caso a las preferencias de este profesor con respecto a las de los demás. Cuanto mayor sea el valor, mayor es la prioridad.
* `<email>`. Opcional. Es de tipo [string](index.html#string). Indica la dirección de correo electrónico del profesor. Es útil cuando se usan funciones de desideratas online, por ejemplo para mandarles la contraseña a esta dirección.
* `<horarioAsoc>`. Opcional. Es de tipo [NombreType](index.html#NombreType). Especifica un nombre, y para todos los profesores en los que coincida, el motor intentará igualar las primeras horas y salidas de los horarios para que entren y salgan a la misma hora. Útil para profesores que compartan el coche.

Aparece en:

* [`<profesores>`](#profesores).

Opciones de profesor
--------------------

Las opciones del profesor son declaradas mediante el elemento `<opciones>` . Este elemento define opciones asociadas a un profesor (menos la plantilla que tiene su propio elemento).

Contiene los subelementos:

* `<intervalosDePermanenciaSemanales>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte) restringido al rango 0 a 300 (ambos inclusive). Por defecto vale 30. Máximo número de intervalos de permanencia semanales. Tiene el atributo `estricto` de tipo [booleano](index.html#booleano) que indica si esta condición será tenida en cuenta como estricta (valor `true`) o solo como condición a evitar (valor `false`), por defecto se considerará como evitar si no se especifica el atributo.
* `<intervalosDePermanenciaDiarios>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte) restringido al rango 0 a 99 (ambos inclusive). Por defecto vale 5. Máximo número de intervalos de permanencia diarios. Tiene el atributo `estricto` de tipo [booleano](index.html#booleano) que indica si esta condición será tenida en cuenta como estricta (valor `true`) o solo como condición a evitar (valor `false`), por defecto se considerará como evitar si no se especifica el atributo.
* `<eliminarHuecos>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `true`. Indica si se quieren eliminar los huecos de este profesor.
* `<maximasHorasSeguidas>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte) restringido al rango 0 a 14 (ambos inclusive). Por defecto vale 5. Indica el número máximo de sesiones lectivas continuadas que se admiten sin incluir un hueco o una complementaria. Tiene el atributo `estricto` de tipo [booleano](index.html#booleano) que indica si esta condición será tenida en cuenta como estricta (valor `true`) o solo como condición a evitar (valor `false`), por defecto se considerará como evitar si no se especifica el atributo.
* `<penalizarAlrededorGuardiaRecreo>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si se quiere penalizar la existencia de sesiones a ambos lados de una guardia de recreo que imparta este profesor. Tiene el atributo `estricto` de tipo [booleano](index.html#booleano) que indica si esta condición será tenida en cuenta como estricta (valor `true`) o solo como condición a evitar (valor `false`), por defecto se considerará como evitar si no se especifica el atributo.
* [`<periodosLibres>`](#periodosLibres). Opcional.
* [`<periodoLibreJornadaPartida>`](#periodoLibreJornadaPartida). Opcional.
* [`<otrosPeriodosLibresJornadaPartida>`](#otrosPeriodosLibresJornadaPartida) Opcional.
* [`<incompatibilidadEntreSesiones>`](#incompatibilidadEntreSesiones). Opcional.
* `<maximoSesionesDiarias>`._**Deprecated.** Ahora se debe utilizar `<considerarMaximasHorasDiarias>` y `<valorMaximasHorasCalculado≶`. No se elimina por compatibilidad. Opcional. Por defecto vale `limitado`. Indica como se gestiona el máximo de sesiones diarias de cada profesor. Puede tener los valores: `limitado`, el cual establece un máximo que se calcula automáticamente; `ampliado` el cual establece un máximo pero ampliandolo en una sesión más; `sinlimite`, que indica que no se estable ningún límite superior; `nopenalizar`, que indica que no se penalizará el máximo de sesiones._
* `<minimoSesionesDiarias>`. _**Deprecated.** Ahora se debe utilizar `<considerarMinimasHorasDiarias>` y `<valorMinimasHorasCalculado>`. No se elimina por compatibilidad. Opcional. Por defecto vale `limitado`. Indica como se gestiona el mínimo de sesiones diarias de cada profesor. Puede tener los valores: `limitado`, el cual establece un mínimo autocalculado pero no estricto; `nopenalizar` el cual no penaliza el que no se cumpla el límite mínimo aunque sí que intente cumplirlo; `concentrar`, que intenta concentrar las sesiones en el menor número de días posible; `estricto` el cual establece un mínimo autocalculado estricto._
* `<minimizarDiasOcupados>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si se quiere intentar minimizar los días con clase del docente buscando días libres en la optimización (true), o no (false). Esta opción es compatible con los máximos y mínimos del profesor, que se comprobarían solo en los días que no quedan libres.
* `<considerarMaximasHorasDiariasSolamenteLectivas>`: Opcional. Indica cómo se considera la restricción del máximo número de horas diarias de Sesiones Lectivas que puede impartir el profesor. Por defecto vale `estricto`. Sus posibles valores son: `estricto`, `optimizacionPreferente`,`ponderable` o `nada`.
* `<valorMaximasHorasCalculadoSolamenteLectivas>`: Opcional. Indica cómo se actualiza el valor del máximo número de horas diario para Sesiones Lectivas del profesor, que se calcula automáticamente según el número de sesiones del profesor. Por defecto vale `automatico`. Sus posibles valores son: `unaHoraMas`, `automatico` o `unaHoraMenos`.
* `<considerarMinimasHorasDiariasSolamenteLectivas>`: Opcional. Indica cómo se considera la restricción del mínimo número de horas diarias de Sesiones Lectivas que puede impartir el profesor. Por defecto vale `estricto`. Sus posibles valores son: `estricto`, `optimizacionPreferente`, `ponderable` o `nada`.
* `<valorMinimasHorasCalculadoSolamenteLectivas>`: Opcional. Indica cómo se actualiza el valor del mínimo número de horas diario para Sesiones Lectivas del profesor, que se calcula automáticamente según el número de sesiones del profesor. Por defecto vale `automatico`. Sus posibles valores son: `unaHoraMas`, `automatico`, `unaHoraMenos`.
* `<considerarMaximasHorasDiarias>`: Opcional. Indica cómo se considera la restricción del máximo número de horas de ocupación (lectivas y no lectivas indicadas como computables) diarias que puede impartir el profesor. Por defecto vale `estricto`. Sus posibles valores son: `estricto`, `optimizacionPreferente`, `ponderable` o `nada`.
* `<valorMaximasHorasCalculado>`: Opcional. Indica cómo se actualiza el valor del máximo número de horas de ocupación (lectivas y no lectivas indicadas como computables) diarias del profesor, que se calcula automáticamente según el número de sesiones del profesor. Por defecto vale `automatico`. Sus posibles valores son: `unaHoraMas`, `automatico` o `unaHoraMenos`.
* `<considerarMinimasHorasDiarias>`: Opcional. Indica cómo se considera la restricción del mínimo número de horas de ocupación (lectivas y no lectivas indicadas como computables) diarias que puede impartir el profesor. Por defecto vale `estricto`. Sus posibles valores son: `estricto`, `optimizacionPreferente`, `ponderable` o `nada`.
* `<valorMinimasHorasCalculado>`: Opcional. Indica cómo se actualiza el valor del mínimo número de horas de ocupación (lectivas y no lectivas indicadas como computables) diarias del profesor, que se calcula automáticamente según el número de sesiones del profesor. Por defecto vale `automatico`. Sus posibles valores son: `unaHoraMas`, `automatico`, `unaHoraMenos`. También `minimizarDiasOcupados` (**Deprecated:** se mantiene por compatibilidad, ahora se usa elemento `<minimizarDiasOcupados>`).

Aparece en:

* [`<profesor>`](#profesor).

periodosLibres
--------------

El elemento `<periodosLibres>` indica el número mínimo de periodos libres que tendrá el profesor y de que tipo.

Contiene los elementos:

* `<cantidadDeDias>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte) restringido al rango 0 a 4 (ambos inclusive). Por defecto vale 0. Indica cuantos días tendrán periodos libres.
* [`<tipoDePeriodo>`](#tipoDePeriodo). Opcional.

Aparece en:

* [`<opcionesDeProfesor>`](#opcionesDeProfesor).

tipoDePeriodo
-------------

El elemento `<tipoDePeriodo>` indica como serán los periodos libres de un profesor.

Si no se escoge uno de los subelementos, se escogerá por defecto diasCompletos.

Se **puede** elegir (uno) de los subelementos:

* `<diasCompletos>`. Es un elemento vacío (sin valor ni subelementos). Indica que se toma libre el día entero.
* `<losPrimerosIntervalos>`. Es de tipo [`Horas`](index.html#Horas) restringido al rango 0 a 20 (ambos inclusive). Sin valor por defecto. Indica que libra los n primeros intervalos.
* `<losUltimosIntervalos>`. Es de tipo [`Horas`](index.html#Horas) restringido al rango 0 a 20 (ambos inclusive). Sin valor por defecto. Indica que libra los n últimos intervalos.
* `<intervalosSeguidos>`. Es de tipo [`Horas`](index.html#Horas) restringido al rango 0 a 20 (ambos inclusive). Sin valor por defecto. Indica que libra n intervalos seguidos.

Aparece en:

* [`<periodosLibres>`](#periodosLibres).

periodoLibreJornadaPartida
--------------------------

El elemento `<periodoLibreJornadaPartida>` indica la cantidad de tardes o mañanas libres que tiene que tener libre como mínimo. Si se omite el elemento entero se toma como que no se quiere poner un mínimo, es decir `<cantidad>0</cantidad>` . Si el valor de cantidad es 0, se ignora la opción de tipo de periodo libre.

Contiene los subelementos:

* `<cantidad>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte) restringido al rango 0 a 5 (ambos inclusive). Por defecto vale 0. Indica la cantidad de tardes o mañanas que debe tener libre como mínimo.
* `<preferentes>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte) restringido al rango 0 a 5 (ambos inclusive). Por defecto vale 0. Indica la cantidad de tardes o mañanas que, de ser posible, se intentará que tenga libre.
* `<tipoDePeriodoLibre>`. Opcional. Por defecto vale `indistintamente`. Indica si tiene que tener libres las tardes, las mañanas o cualquiera de las dos. Puede tener los valores: `tardes`, `mañanas` e `indistintamente`.

Aparece en:

* [`Opciones de profesor`](#opcionesDeProfesor).

otrosPeriodosLibresJornadaPartida
---------------------------------

El elemento `<otrosPeriodosLibresJornadaPartida>` indica otros periodos libres de jornada partida definidos para el profesor, que también se tendrán en cuenta. El tipoDePeriodoLibre de cada uno de estos elementos debe ser único. No puede haber dos periodos del mismo tipo en esta lista, y además debe ser distinto del tipo de periodoLibreJornadaPartida definida en las opciones del profesor.

Contiene los subelementos:

* `<periodoLibreJornadaPartida>`. Mín. 0, máx. ∞. Es de tipo [PeriodoLibreJornadaPartidaType](#periodoLibreJornadaPartida). Contiene otro de los Periodos libres de jornada partida que se hayan definido para el profesor.
    

Aparece en:

* [`Opciones de profesor`](#opcionesDeProfesor).

incompatibilidadEntreSesiones
-----------------------------

El elemento `<incompatibilidadEntreSesiones>` define las incompatibilidades de un profesor.

Todos los subelementos exceptuando, el elemento `<tipoDeIncompatibilidad>`, tienen el atributo opcional `tipo` que tiene la misma funcionalidad y valores (`prohibición` o `evitar`) que el elemento `<tipoDeIncompatibilidad>` pero que solo afecta a esa incompatibilidad en concreto. Si se omite este atributo, se usará el valor especificado por el elemento `<tipoDeIncompatibilidad>`.

Contiene los subelementos:

* `<tipoDeIncompatibilidad>`. **Deprecated**. Opcional. Puede tener los valores: `prohibición` o `evitar`. Por defecto vale `evitar`. Indica si esta opción es una prohibición, nunca se saltará la norma pero complica que se hagan horarios completos, o que se intente evitar en la medida de lo posible.
* `<salirUltimaEntrarPrimera>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica la incompatibilidad de que salga a la última hora y entre a primera hora del día siguiente. Tiene el atributo opcional `tipo`. También tiene el atributo `nIntervalos` donde se define el número de intervalos que debe de cumplirse la condición. Si no se define el atributo, por defecto vale 1.
* `<salirUltimaEntrarPrimeraLunes>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica la incompatibilidad de que salga a la última hora y entre a primera hora, específicamente, entre el Viernes y el Lunes. Tiene el atributo opcional `tipo`. También tiene el atributo `nIntervalos` donde se define el número de intervalos que debe de cumplirse la condición. Si no se define el atributo, por defecto vale 1.
* `<entrarPrimeraSalirUltima>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica la incompatibilidad de que entre a primera hora y salga a última del mismo día. Tiene el atributo opcional `tipo`. También tiene el atributo `nIntervalos` donde se define el número de intervalos que debe de cumplirse la condición. Si no se define el atributo, por defecto vale 1.
* `<entrarPrimeraSalirUltimaTarde>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica la incompatibilidad de que entre a primera hora y salga a última hora de la tarde cuando hay jornada partida. Tiene el atributo opcional `tipo`.
* `<entrarPrimeraSalirUltimaManana>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica la incompatibilidad de que entre a primera hora y salga a última hora de la mañana cuando hay jornada partida. Tiene el atributo opcional `tipo`.
* `<salirUltimaMananaEntrarPrimeraTarde>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica la incompatibilidad de que salga a última de la mañana y entre a primera de la tarde. Tiene el atributo opcional `tipo`.
* `<salirUltimaMananaTardeCompleta>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica la incompatibilidad de que salga a la última hora de la mañana y tenga la tarde ocupada. Tiene el atributo opcional `tipo`.
* `<menosDeDosIntervalosLibres>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica la incompatibilidad de que tenga un determinado tiempo libre alrededor del mediodía. Tiene el atributo opcional `tipo`, y el atributo opcional `minutos`, que indica el tiempo que se quiere respetar. Por defecto vale 120 (2 horas).
* `<entrarPrimeraSalirTarde>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica la incompatibilidad de que entre a primera hora y tenga clase por la tarde, cuando hay jornada partida. Tiene el atributo opcional `tipo`.

Aparece en:

* [Opciones del profesor](#opcionesDeProfesor).

materias
--------

El elemento `<materias>` declara la lista de materias disponibles.

Contiene los subelementos:

* [`<materia>`](#materia). Mín. 1, máx. ∞.

Aparece en:

* [`<datosGHC>`](#datosGHC).

materia
-------

El elemento `<materia>` define una materia y sus opciones.

Contiene los subelementos:

* `<nombre>`. Obligatorio. Es de tipo [NombreType](index.html#NombreType). Es el identificador de la materia.
* `<abreviatura>`. Opcional. Es de tipo [AbreviaturaType](index.html#AbreviaturaType). Es una forma abreviada del nombre para que sea más fácil visualizar la materia.
* `<nombreCompleto>`. Opcional. Es de tipo [NombreCompletoType](index.html#NombreCompletoType). Es una descripción más larga para facilitar al usuario a identificar la materia.
* `<departamento>`. Opcional. Es de tipo [NombreType](index.html#NombreType). Es el departamento al que pertenece la materia.
* `<claveDeExportacion>`. Opcional. Es de tipo [string](index.html#string). Es usado como valor de referencia por algunos programas externos.
* `<esTutoria>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si la materia es una tutoría.
* `<esDeFP>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si es una materia perteneciente a un ciclo de formación profesional o no.
* [`<plantilla>`](#plantillaSinFType). Opcional. Es una plantilla del tipo [PlantillaSinFType](#plantillaSinFType).

Aparece en:

* [`<materias>`](#materias).

grupos
------

El elemento `<grupos>` declara la lista de grupos disponibles.

Contiene los subelementos:

* [`<grupo>`](#grupo). Mín. 1, máx. ∞.

Aparece en:

* [`<datosGHC>`](#datosGHC).

grupo
-----

El elemento `<grupo>` define un grupo y sus características.

Tiene los atributos:

* `submarco`. Obligatorio. Es del tipo [NCName](index.html#NCName). Indica el submarco al que está asociado el grupo. Debe ser el identificador de un marco existente en el elemento `[<marcos>](#marcosDeHorario)` . Los tramos de la plantilla que no pertenezcan a este marco serán ignorados.

Contiene los elementos:

* `<nombre>`. Obligatorio. Es de tipo [NombreType](index.html#NombreType). Es el identificador del grupos.
* `<abreviatura>`. Opcional. Es de tipo [AbreviaturaType](index.html#AbreviaturaType). Es una forma abreviada del nombre para que sea más fácil visualizar la materia.
* `<nombreCompleto>`. Opcional. Es de tipo [NombreCompletoType](index.html#NombreCompletoType). Sirve para indicar el nombre del grupo si no cabe en su campo nombre.
* `<cursoPerteneciente>`. Opcional. Es de tipo [NombreType](index.html#NombreType). Indica el nombre del curso al que pertenece. Si no tiene curso asociado a él, no se debe poner el elemento.
* `<profesorTutor>`. Opcional. Es de tipo [NombreType](index.html#NombreType). Es el nombre de un profesor (de la [lista de profesores](#profesores)) el cual es el tutor del grupo. Permite definir de forma opcional los atributos `<imparteTodosLosDias>`, `<imparteAPrimeras>` y/o `<imparteAUltimas>` de tipo <code>boolean</code> para procurar en la optimización que el tutor del grupo tenga asignada clase todos los días con el grupo, a primera hora y ultima hora correspondientemente.
* `<aula>`. Opcional. Es de tipo [NombreType](index.html#NombreType). Es el nombre de un aula de la [lista de aulas](#aulas) la cual estará asociada al grupo, y en ellas se intentará colocar las sesiones asociadas a este grupo.
* `<claveDeExportacion>`. Opcional. Es de tipo [string](index.html#string). Es usado como valor de referencia por algunos programas externos.
* `<tardesLibres>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte) restringido al rango 0 a 4 (ambos inclusive). Por defecto vale 0. El número de tardes libres a la semana.
* `<eliminarHuecos>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `true`. Indica si se quieren eliminar los huecos de este grupo.
* `<limiteOcupacionDia>`. Opcional. Es de tipo [unsignedInt](index.html#unsignedInt). Indica el máximo de intervalos al día que se le pueden asignar al grupo.
* [`<plantilla>`](#plantillaSinFType). Opcional. Es de tipo [PlantillaSinFType](#plantillaSinFType).
* `<email>`. Opcional. Es de tipo [Email](index.html#Email). Asocia al grupo una dirección de email, por si se quiere comunicar algo, o exportar al calendario asociado a ese email.
* `<numeroAlumnos>`. Opcional. Es de tipo [unsignedInt](index.html#unsignedInt). Indica el número de alumnos que compone el grupo. Por defecto vale 0.
* `<noAdmiteHuecos>`. es opcional y del tipo [boolean](index.html#booleano). Es una condición estricta que impiede los huecos en el horario del grupo.
* `<huecosEnNoPreferentes>`. es opcional y del tipo [boolean](index.html#booleano). Es una condición estricta que obliga a que las posiciones desocupadas (no asignadas al grupo) estén siempre en posiciones señaladas como no preferentes en su plantilla.
* [`<gruposIncluidos>`](#gruposIncluidosType). Opcional. Permite indicar que se trata de un grupo circunstancial, formado por grupos oficiales del centro, para recibir determinadas materias optativas o troncales .Es de tipo [GruposIncluidosType](#gruposIncluidosType).

Aparece en:

* [`<grupos>`](#grupos).

cursos
------

Define la lista de los cursos que están disponibles. Se declara con el elemento `<cursos>` .

Contiene los subelementos:

* [`<curso>`](#curso). Mín. 0, máx. ∞.

Aparece en:

* [`<datosGHC>`](#datosGHC).

curso
-----

Define un curso ( `<curso>` ) y sus características. También declara las materias que pertenecen al curso.

Contiene los subelementos:

* `<nombre>`. Obligatorio. Es de tipo [NombreType](index.html#NombreType). Debe tener 1 carácter como mínimo. Es el identificador del curso.
* `<nombreCompleto>`. Opcional. Es de tipo [NombreCompletoType](index.html#NombreCompletoType). Es una descripción más larga para facilitar al usuario el identificar el curso.
* `<claveDeExportacion>`. Opcional. Es de tipo [string](index.html#string). Es usado como valor de referencia por algunos programas externos.
* [`<materiasDelCurso>`](#materiasDelCurso). Opcional.

Aparece en:

* [`<cursos>`](#cursos).

materiasDelCurso
----------------

Define una lista con las materias que están asociadas a un curso.

Contiene los subelementos:

* `<materia>`. Mín. 0, máx. ∞. Identifica una materia y cuantos tramos tendrá en los grupos de ese curso. El subelemento `<materia>` tiene como valor (de tipo [NombreType](index.html#NombreType)) el nombre de la materia que pertenece al curso. Además cada elemento `<materia>` tiene un atributo `numSesiones` de tipo [unsignedByte](index.html#unsignedByte) que indica la cantidad de tramos a la semana que debe tener las sesiones de esa materia en el curso. Nota: no confundirlo con el elemento [`<materia>`](#materia) que define las materias.

Aparece en:

* [`<curso>`](#curso).

sesionesLectivas
----------------

Contiene la lista de sesiones lectivas que se deben colocar.

Contiene los subelementos:

* [`<sesion>`](#sesion). Mín. 0, máx. ∞.

Aparece en:

* [`<datosGHC>`](#datosGHC).

sesion
------

Define una sesión y sus opciones. Para ver una guía y ejemplos sobre la sesión consulte la [guía del xml de ghc - cuarto paso](index.html#CuartoPaso).

Los tramos de la plantilla que no pertenezcan al marco del grupo, serán ignorados.

Tiene los atributos:

* `id`. Obligatorio. Es de tipo [nonNegativeInteger](index.html#nonNegativeInteger). Es el identificador de la sesión.

Contiene los subelementos:

* `<materia>`. Obligatorio. Es de tipo [NombreType](index.html#NombreType). Es el nombre de la materia que se impartirá en la sesión.
* `<grupo>`. Obligatorio. Es de tipo [NombreType](index.html#NombreType). Es el identificador del grupo al que se quiere impartir la sesión. Puede tener el atributo `numeroAlumnos`, que indica el número de alumnos de este grupo en esta sesión. Es opcional, y por defecto vale 0.
* `<profesor>`. Opcional. Es de tipo [NombreType](index.html#NombreType). Es el nombre del profesor que impartirá la sesión.
* `<duracionSemanal>`. Opcional. Es de tipo [float](index.html#float). Indica la duración semanal (en horas) que tendrá la sesión.
* [`<distribucionSemanal>`](#distribucionSemanal). _**Deprecated.**_. Utilizar el elemento `distribucionPeriodica` para definir la distribución de la sesión.
* [`<distribucionPeriodica>`](#distribucionPeriodica). Obligatorio (aunque si no viene este elemento obtiene su valor de `distribucionSemanal`. Indica la distribución de la sesión, y los [periodos](#periodos) en que tiene que colocarse.
* [`<listaDeAulas>`](#listaDeAulas). Opcional.
* [`<listaDeAlternativas>`](#listaDeAlternativas). Opcional.
* `<tarea>`. Obligatorio. Es de tipo [NombreType](index.html#NombreType). Es el identificador de la tarea asociada a la sesión.
* `<grupoMateria>`. Opcional. Es de tipo [string](index.html#string) y puede tener los atributos `modificado` y/o `tipo`. Es el grupo-materia al que pertenece la sesión. El atributo `modificado` es opcional y del tipo [boolean](index.html#booleano) indica si ha sido especificado por el usuario (`true`) o ha sido generado automáticamente (`false`), por defecto es `false`. El atributo `tipo` es opcional y del tipo [string](index.html#string) indica el tipo del grupo-materia y es usado por algunos gestores.
* `<departamento>`. Opcional. Es de tipo [NombreType](index.html#NombreType). El departamento al que pertenece la sesión, que no tiene por qué ser el mismo de sus profesores o materias.
* `<notas>`. Opcional. Es de tipo [string](index.html#string). Declara un texto que aclara información sobre las preferencias de la sesión.
* [`<profesoresIntercambiables>`](#profesoresIntercambiables). Opcional.
* [`<opciones>`](#OpcionesDeSesionType). Opcional. Es de tipo [Opciones de sesión](#OpcionesDeSesionType).
* [`<plantilla>`](#PlantillaType). Opcional. Es de tipo [PlantillaType](PlantillaType).
* [`<otrasMateriasGrupos>`](#otrasMateriasGrupos). Opcional.
* [`<otrasMateriasProfesores>`](#otrasMateriasProfesores). Opcional.
* [`<otrosGrupos>`](#otrosGrupos). Opcional.
* [`<otrosProfesores>`](#otrosProfesores). Opcional.
* [`<otrasMaterias>`](#otrasMaterias). Opcional.
* [`<otrasAulas>`](#otrasAulas). Opcional.
* `<sesionesSimultaneas>`. Opcional. Es de tipo [nonNegativeInteger](index.html#nonNegativeInteger). Indica el identificador del [bloque de simultaneas](#simultaneas) al que pertenece.
* [`<enDistintoDia>`](#enDistintoDia). Opcional.
* `<consecutivas>`. Opcional. Es de tipo [nonNegativeInteger](index.html#nonNegativeInteger). Indica el identificador del [bloque de consecutivas](#consecutivas) al que pertenece.
* [`<noConsecutivas>`](#noConsecutivas). Opcional.
* [`<noCoincidentes>`](#noCoincidentes). Opcional.
* [`<previoA>`](#previoA). Opcional.
* [`<posteriorA>`](#posteriorA). Opcional.
* [`<separadosNDiasOMas>`](#separadosNDiasOMas). Opcional.
* [`<separadosNDiasOMenos>`](#separadosNDiasOMenos). Opcional.

Aparece en:

* [`<sesionesLectivas>`](#sesionesLectivas).

distribucionSemanal
-------------------

Define las distintas posibilidades de declarar que distribución tendrán las sesiones a lo largo de la semana.

Se **debe** elegir (uno) de los subelementos:

* [`<distribucionFija>`](#distribucionFija).
* [`<distribucionVariable>`](#distribucionVariable).
* [`<distribucionPersonalizada>`](#distribucionPersonalizada).

Aparece en:

* [`<sesion>`](#sesion).
* [`<reunion>`](#reunion).
* [`<complementaria>`](#complementaria).
* [`<distribucionPeriodicaFija>`](#distribucionPeriodicaFija).

distribucionSemanalReducida
---------------------------

Define las distintas posibilidades de declarar que distribución tendrán las sesiones a lo largo de la semana, pero sabiendo que no se puede tener distribucionPersonalizada.

Se **debe** elegir (uno) de los subelementos:

* [`<distribucionFija>`](#distribucionFija).
* [`<distribucionVariable>`](#distribucionVariable).

Aparece en:

* [`<sesion>`](#sesion).
* [`<distribucionPeriodicaVariable>`](#distribucionPeriodicaVariable).

distribucionFija
----------------

Contiene una única posible distribución semanal.

Cada subelemento `<numSesiones>` indica cuantos tramos se deben impartir en un día de la semana (sin especificar que día es, lunes, martes, etc.).

Contiene los subelemetos:

* `<numSesiones>`. Es de tipo [DuracionesDistFijaType](#duracionesDistFijaType). Indica en cuantos tramos se impartirá la sesión en un día. Su valor máximo es 5.

Aparece en:

* [`<distribucionSemanal>`](#distribucionSemanal).

distribucionVariable
--------------------

Permite definir la distribución como una cantidad de tramos a la semana y un rango máximo de tramos al día. Permitiendo así una mayor flexibilidad en la creación del horario.

Contiene los subelementos:

* `<numSesiones>`. Obligatorio. Es de tipo [decimal](index.html#decimal) restringido al rango de 0.5 a 35 (ambos inclusive) con incrementos de `0.25`. Indica el número de tramos a la semana que tendrá la sesión.
* `<numMaximoDeSesiones>`. Obligatorio. Es de tipo [DuracionesType](#duracionesType). Indica el tamaño máximo de una sesión. El valor máximo es 7.
* `<numMinimoDeSesiones>`. Opcional. Es de tipo [DuracionesType](#duracionesType). Indica el tamaño máximo de una sesión. El valor máximo es 7.
* `<penalizarBloquesMaximos>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si se penalizará el que tenga el máximo de tramos permitidos en un día.
* `<penalizarBloquesMinimos>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si se penalizará el que tenga el mínimo posible de tramos permitidos en un día.
* `<admitirBloquesDiscontinuos>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si se admiten bloques discontinuos, es decir que tengan tramos de otras sesiones o recreos entre medias.
* `<distribucionInicial>`. Opcional. Es igual que el elemento [`<distribucionFija>`](#distribucionFija). Indica la distribución inicial de la sesión que se mostrará en el planificador.
* `<penalizarSesionesSueltas>`. Opcional. `Deprecated` Permite indicar si se deben permitir, evitar o prohibir las sesiones de duracion minima posible. Puede tomar los valores `permitido`, `penalizado` o `Prohibido`.

Aparece en:

* [`<distribucionSemanal>`](#distribucionSemanal).

distribucionPersonalizada
-------------------------

Esta distribución permite especificar un número indeterminado de distribuciones fijas (aunque todas con el mismo número de tramos a la semana).

Contiene los subelementos:

* `<distribucion>`. Mín. 1, máx. ∞. Cada elemento `<distribucion>` es exactamente igual que el elemento [`<distribucionFija>`](#distribucionFija).

Aparece en:

* [`<distribucionSemanal>`](#distribucionSemanal).

distribucionPeriodica
---------------------

Define las distintas posibilidades de declarar que distribución tendrán las sesiones entre los periodos definidos en el horario.

Se **debe** elegir (uno) de los subelementos:

* [`<distribucionPeriodicaFija>`](#distribucionPeriodicaFija).
* [`<distribucionPeriodicaVariable>`](#distribucionPeriodicaVariable).

Aparece en:

* [`<sesion>`](#sesion).
* [`<reunion>`](#reunion).
* [`<complementaria>`](#complementaria).

distribucionPeriodicaFija
-------------------------

Indica qué distribucionSemanal y en qué periodos se debe colocar esta sesión. Se colocará (repite) la misma distribucionSemanal en cada uno de los periodos.

Contiene los subelemetos:

* `<distribucionSemanal>`. Obligatorio. Es de tipo [DistribucionSemanal](#distribucionSemanal). Indica la distribución que tendrá la sesión dentro de los días de cada periodo en que se imparte esta sesión.
* `<enPeriodos>`. Obligatorio. Es de tipo `[enPeriodos](#enPeriodos)`. Indica los periodos en que se **repite** la distribucionSemanal de esta distribucionPeriodicaFija.

Aparece en:

* [`<distribucionPeriodica>`](#distribucionPeriodica).

distribucionPeriodicaVariable
-----------------------------

Permite definir la distribucion total de esta sesión, que se tiene que **repartir** entre los distinos periodos de esta distribución. No indica la distribución de cada periodo, sino la distribución total de la sesión entre todos los periodos. También se indican los periodos entre los que se **reparte**, y las condiciones que deben de respetarse en cada periodo para que la repartición sea válida.

Contiene los subelementos:

* `<distribucionTotal>`. Obligatorio. Es de tipo [distribucionSemanalReducida](#distribucionSemanalReducida). Indica la distribución que tendrá la sesión, entre todos los periodos entre los que se reparte. No es la distribuición de cada periodo, sino la total de esta sesión.
* `<enPeriodos>`. Obligatorio. Es de tipo `[enPeriodos](#enPeriodos)`. Indica los periodos en que se **reparte** la distribucionSemanal de esta distribucionPeriodicaVariable.
* `<numMaximoDeSesionesEnPeriodo>`. Opcional. Es de tipo [nonNegativeInteger](index.html#nonNegativeInteger). Indica el número máximo de sesiones (duración semanal, media en la tipificación de los tramos) que se puede colocar en cada periodo con entidades de esta sesión. Si no se define, se considera que no hay un límite máximo.
* `<numMinimoDeSesionesEnPeriodo>`. Opcional. Es de tipo [nonNegativeInteger](index.html#nonNegativeInteger). Indica el número mínimo de sesiones (duración semanal, media en la tipificación de los tramos) que hay que colocar en cada periodo con entidades de esta sesión. Por defecto vale 0

Aparece en:

* [`<distribucionPeriodica>`](#distribucionPeriodica).

enPeriodos
----------

Lista que referencia a uno o varios periodos.

Contiene los elementos:

* `<refPeriodo>`. Mín. 0, máx. ∞. Es de tipo [NombreType](index.html#NombreType). Es el identificador de un [periodo](#periodo) de la lista de [periodos](#periodos) en que se dividen los días del horario.

Aparece en:

* [`<distribucionPeriodicaFija>`](#distribucionPeriodicaFija).
* [`<distribucionPeriodicaVariable>`](#distribucionPeriodicaVariable).

listaDeAulas
------------

Indica una lista de aulas en las que debe ir la sesión.

El orden de las aulas es significativo, se intentará poner primero en la primera, si no está disponible en la segunda, etc.

Si no aparece ningún aula indica que se puede colocar la sesión en cualquier aula.

Contiene los subelementos:

* `<aula>`. Mín. 0, máx. ∞. Es de tipo [NombreType](index.html#NombreType). Es el identificador un aula de la [lista de aulas](#aulas) en el que se debe impartir la sesión.

Aparece en:

* [`<sesion>`](#sesion).

listaDeAlternativas
-------------------

Define la lista de conjunto de aulas alternativas a las aulas principales de una sesión.

Al igual que la lista de aulas de la sesión, el orden de los conjuntos es significativo. Primero se cogerá un aula del primer grupo, si no hay ninguna disponibles se pondrá alguna del segundo grupo, etc.

Si no se pone ningún conjunto (o si nisiquiera aparece este elemento), indica que no se quiere ningún conjunto alternativo, debiendose colocar solo en las aulas especificadas en la lista de aulas principal de la sesión.

Contiene los subelementos:

* `<conjuntoAlternativo>`. Mín. 0, máx. ∞. Es de tipo [NombreType](index.html#NombreType). Es el identificador un conjunto de aulas de la [lista de conjuntos de aulas](#conjuntoDeAulas) en el que se debe impartir la sesión si no están disponibles las aulas principales de la sesión.

Aparece en:

* [`<sesion>`](#sesion).

profesoresIntercambiables
-------------------------

Define una lista de sesiones con las que se puede intercambiar el profesor.

Contiene los subelementos:

* `<sesion>`. Mín. 0, máx. ∞. Es de tipo [nonNegativeInteger](index.html#nonNegativeInteger). Indica el identificador de una sesión cuyo profesor se puede intercambiar con la de la sesión actual.

Aparece en:

* [`<sesion>`](#sesion).

Opciones de sesión
------------------

Define las opciones que tiene una sesión. Es el elemento `<opciones>` del elemento `[<sesion>](#sesion)` . Si no se pone o falta alguna opción se tomará los valores por defecto de las opciones que falten.

Contiene los subelementos:

* `<penaSesionesAPrimera>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `true`. Indica si se penaliza el que se ponga más del 50% de las veces en tramos a primera hora.
* `<penaSesionesAUltima>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `true`. Indica si se penaliza el que se ponga más del 50% de las veces en tramos a última hora.
* `<penaSalirUltimaEntrarPrimera>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `true`. Indica si se penaliza que se ponga en un tramo a última hora y que al día siguiente lo tenga en el primer tramo.
* `<penaSesionMismaHora>`. Opcional. Es de tipo [string](index.html#string). Por defecto vale `distinta`. Puede tener uno de los siguientes valores: distinta, indiferente o misma. Indica si se penaliza que coincidan los tramos a la misma hora, distinta o si es indiferente.
* `<penaCoincidanPorLaTarde>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `true`. Indica si se penalizará el que se coloque en tramos de la tarde (después del tramo de medio día).
* `<penaCoincidanDespuesDelRecreo>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `true`. Indica si se penalizará el que se coloque más del 50% en tramos después de los recreos.
* `<noPermitirRecreosEntreSesiones>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si se permite o no que en el caso de que en un mismo día haya varios tramos, no se coloque un recreo entre medias (o sí se pueda colocar).
* `<recreosSeparanSesionesContinuas>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Prohíbe que se coloquen las sesiones configuradas como consecutivas si están separadas por recreos. Esta opción no se tiene en cuenta si las sesiones consecutivas contienen bloques de más de un intervalo de duración. Para las sesiones configuradas como '_no consecutivas'_ siempre se considera que las separa un recreo.
* `<permitirImpartanEnDiasSeguidos>`. Opcional. Permite uno de los siguientes valores: `obligatoriamente`, `preferiblemente`, `indiferente`, `prohibido` o `penalizaNoSeguidas`. Por defecto será `preferiblemente`. **Advertencia:** Tenga en cuenta que el nombre usado para este elemento no corresponde correctamente con lo que representa y puede ser confuso su uso, su significado es realmente _"permitir que se impartan en dias alternos"_. Sus valores tienen los siguientes significados:
    * `preferiblemente`. Indica que el motor intentará ponerlas en días alternos (penaliza que estén en días seguidos). Es el valor por defecto.
    * `obligado`. Indica que el motor obligatoriamente colocará las sesiones en días alternos.
    * `indiferente`. Indica que el motor no aplicará ninguna regla respecto a si son en días seguidos o alternos.
    * `penalizaNoSeguidas`. Indica que el motor intentará ponerlas en días seguidos.
    * `prohibido`. Indica que el motor obligatoriamente las colocará en días seguidos (prohibe que estén en días alternos).
* `<considerarLunesViernesSeguidos>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica que, en caso de tener 2 o 4 días semanales, el Viernes y el Lunes de la semana siguiente sean consecutivos.
* `<sinCambioAula>`. Opcional. Es de tipo [booleano](index.html#booleano). Indica si deben asignarse todas las horas de la sesion en el mismo aula de forma estricta. No importara si se asigna el aula principal o un aula del conjunto alternativo (si hubiera), pero deberá ser el mismo para toda la sesion.
* `<mismaPosicionDistintosPeriodos>`. Opcional. Es de tipo [preferenciaMismaPosicionDistintosPeriodos](#preferenciaMismaPosicionDistintosPeriodos). Por defecto vale `ignorar`. Indica el tipo de criterio con el que se ha de intentar colocar las entidades de esta sesión que pertenecen a distintos periodos en la misma posición.

Aparece en:

* [`<sesion>`](#sesion).

otrasMateriasGrupos
-------------------

El elemento `<otrasMateriasGrupos>` indica otros pares de materias y grupos, a parte de los principales, que también se incluirán en el aula de la sesión.

Este elemento es redundante con los elementos `<otrosGrupos>` y `<otrasMaterias>` . Esto quiere decir que los elementos que aquí aparecen también aparecerán en las otras listas y viceversa. Es aconsejado usar este elemento en vez de las otras listas ya que este contiene los elementos según son definidos en el planificador.

Contiene los subelementos:

* [`<materiaGrupo>`](#parMateriaGrupo). Mín. 0, máx. ∞. Define uno de los pares de materia-grupo que serán agregados (junto con los principales) a la sesión.

Aparece en:

* [`<sesion>`](elementos.html#sesion).

materiaGrupo
------------

El elemento `<materiaGrupo>` indica un par de materia y grupo que será agregado al aula de la sesión junto con la materia y grupo principal.

Si se omite alguno de los dos elementos se tomará como parte del par el correspondiente principal. Es decir, si por ejemplo se omite el grupo, será como si el par materia-grupo estuviera compuesto por la materia indicada y el grupo principal de la sesión definido por el elemento `<grupo>` de la [sesión](#sesion).

Advertencia: No hay que confundir este elemento con el elemento `<grupoMateria>` hijo del elemento [`<sesion>`](#sesion).

Tiene los atributos:

* `tarea` Opcional. Es de tipo [NombreType](index.html#NombreType). Indica la tarea de este grupo-materia en caso de ser diferente al de la sesión.
* `claveX` Opcional. Es de tipo [string](index.html#string). Guarda un valor para ser usado por las aplicaciones externas, normalmente un grupomateria diferente al de la sesión principal.

Contiene los subelementos:

* `<materia>`. Mín. 0, máx. 1\. Es de tipo [NombreType](index.html#NombreType). Contiene el nombre de la materia que también se incluirá junto con el principal.
* `<grupo>`. Mín. 0, máx. 1\. Es de tipo [NombreType](index.html#NombreType). Contiene el nombre del grupo que también se incluirá junto con el principal. Sus atributos son:
    
    * `numeroAlumnos` que indica el número de alumnos de este grupo en esta sesión para esta materia. Es opcional, y por defecto vale 0.
    * `autogenerado` Es de tipo [booleano](index.html#booleano) y valor por defecto _false_. Indica si el grupo ha sido añadido a la lista de forma automática por ser un grupo incluido en el grupo principal de la sesión.__
    

__

Aparece en:

* [`<otrasMateriasGrupos>`](#otrasMateriasGrupos).

otrasMateriasProfesores
-----------------------

El elemento `<otrasMateriasProfesores>` indica otros pares de materias y profesores, a parte de los principales, que también se incluirán en el aula de la sesión.

Este elemento es redundante con los elementos `<otrosProfesores>` y `<otrasMaterias>` . Esto quiere decir que los elementos que aquí aparecen también aparecerán en las otras listas y viceversa. Es aconsejado usar este elemento en vez de las otras listas ya que este contiene los elementos según son definidos en el planificador.

Contiene los subelementos:

* [`<otraMateriaProfesor>`](#otraMateriaProfesor). Mín. 0, máx. ∞. Define uno de los pares de materia-profesor que serán agregados (junto con los principales) a la sesión.

Aparece en:

* [`<sesion>`](elementos.html#sesion).

otraMateriaProfesor
-------------------

El elemento `<otraMateriaProfesor>` indica un par de materia y profesor que será agregado al aula de la sesión junto con la materia y profesor principal.

Si se omite alguno de los dos elementos se tomará como parte del par el correspondiente principal. Es decir, si por ejemplo se omite el profesor, será como si el par materia-profesor estuviera compuesto por la materia indicada y el profesor principal de la sesión definido por el elemento `<profesor>` de la [sesión](#sesion).

Contiene atributo:

* `<tarea>`. _Opcional_. Es de tipo [NombreType](index.html#NombreType). Contiene el nombre de la tarea especifica que realiza la relacion profesor-materia en el aula si difiere de la tarea principal de la sesion.

Contiene los subelementos:

* `<profesor>`. Mín. 1, máx. 1\. Es de tipo [NombreType](index.html#NombreType). Contiene el nombre del profesor que también se incluirá junto con el principal.
* `<materia>`. Mín. 1, máx. 1\. Es de tipo [NombreType](index.html#NombreType). Contiene el nombre de la materia que también se incluirá junto con el principal.

Aparece en:

* [`<otrasMateriasProfesores>`](#otrasMateriasProfesores).

otrosGrupos
-----------

El elemento `<otrosGrupos>` indica otros grupos, a parte del principal, que también se incluirán en el aula de la sesión.

Contiene los subelementos:

* `<grupo>`. Mín. 0, máx. ∞. Es de tipo [NombreType](index.html#NombreType). Contiene el nombre del grupo que también se incluirá junto con el principal. Sus atributos son:
    
    * `tarea` que es opcional y de tipo [NombreType](index.html#NombreType). Indica la tarea de este grupo en caso de ser diferente al de la sesión.
    * `numeroAlumnos` que indica el número de alumnos de este grupo en esta sesión. Es opcional, y por defecto vale 0.
    * `claveX` Opcional. Es de tipo [string](index.html#string). Guarda un valor para ser usado por las aplicaciones externas, normalmente un grupomateria diferente al de la sesión principal.
    * `autogenerado` Es de tipo [booleano](index.html#booleano) y valor por defecto _false_. Indica si el grupo ha sido añadido a la lista de otrosGrupos de forma automática por ser un grupo incluido en el grupo principal de la sesión.__
    

__

Aparece en:

* [`<sesion>`](#sesion).

otrosProfesores
---------------

El elemento `<otrosProfesores>` indica otros profesores, a parte del principal, que también se deben incluir en el aula de la sesión.

Contiene los subelementos:

* `<profesor>`. Mín. 0, máx. ∞. Es de tipo [NombreType](index.html#NombreType). Contiene el nombre del profesor que también se incluirá junto con el principal.
    
    Tiene los atributos:
    
    * `tarea` que es opcional y de tipo [NombreType](index.html#NombreType). Indica la tarea de este profesor en caso de ser diferente al de la sesión.
    * `claveX` Opcional. Es de tipo [string](index.html#string). Guarda un valor para ser usado por las aplicaciones externas, normalmente un grupomateria diferente al de la sesión principal.

Aparece en:

* [`<sesion>`](#sesion).

otrasMaterias
-------------

El elemento `<otrasMaterias>` indica otras materias que también se incluirán (impartirán) junto con la principal de la sesión.

Contiene los subelementos:

* `<materia>` . Mín. 0, máx. ∞. Es de tipo [NombreType](index.html#NombreType). Contiene el nombre de la materia que también se incluirá junto con la principal.
    
    Tiene los atributos:
    
    * `tarea` que es opcional y de tipo [NombreType](index.html#NombreType). Indica la tarea de esta materia en caso de ser diferente al de la sesión.
    * `claveX` Opcional. Es de tipo [string](index.html#string). Guarda un valor para ser usado por las aplicaciones externas, normalmente un grupomateria diferente al de la sesión principal.

Aparece en:

* [`<sesion>`](#sesion).

otrasAulas
----------

El elemento `<otrasAulas>` declara otras aulas/conjuntos que se usarán junto con el aula/conjunto principal.

Contiene los subelementos:

* `[<otraAula>](#otraAula)` . Mín. 0, máx. ∞.

Aparece en:

* [`<sesion>`](#sesion).

otraAula
--------

Indica una asociación de aula y conjunto alternativo que también tienen que estar disponibles para la sesión.

Si solo aparece un aula pero no el conjunto alternativo, indica que es obligatoria ese aula y no hay alternativa a la misma. Si solo aparece el conjunto alternativo, indica que se requiere una de las aulas del conjunto pero que es indiferente cual de ellas se coja. Si aparecen ambos indica que se necesita el aula pero que en caso de no estar disponible, se cogerá una de las alternativas. Es obligatorio que aparezca el elemento `<aula>` , el `<grupo>` o ambos (pero no puede estar vacío).

Tiene los atributos:

* `tarea` Opcional. Es de tipo [NombreType](index.html#NombreType). Indica la tarea de este aula en caso de ser diferente al de la sesión.
* `origenAula` Opcional. Es de tipo [NombreType](index.html#NombreType). Indica un identificador para después poder saber con qué aula de las asignadas se correspondía esta definición de otro aula.
* `claveX` Opcional. Es de tipo [string](index.html#string). Guarda un valor para ser usado por las aplicaciones externas, normalmente un grupomateria diferente al de la sesión principal.

Contiene los subelementos:

* `<aula>`. Opcional. Es de tipo [NombreType](index.html#NombreType). Indica el nombre del aula que es requerída.
* `<grupo>`. Opcional. Es de tipo [NombreType](index.html#NombreType). Indica el identificador del conjunto de aulas alternativas a la requerída.

Aparece en:

* [`<otrasAulas>`](#otrasAulas).

enDistintoDia
-------------

Declara otras sesiones que deben impartirse en disitinto día al de la sesión actual.

Contiene los subelementos:

* [`<sesiones>`](#sesionesDistintoDia). Opcional. Es de tipo de [Sesiones en distinto día](#sesionesDistintoDia).
* `<enDiasSeguidos>`. Opcional. Puede tener uno de los valores:
    
    * obligado. Indica que obligatoriamente deben ser en días consecutivos (pero no en el mismo día).
    * preferentemente. Indica que se intentará colocarlas en días consecutivos (pero no en el mismo día).
    * indistinto. Indica que no importa si se colocan en días consecutivos o no (seguirán sin estar en el mismo día).
    * prohibido. Indica que está prohibido (nunca ocurrirá) que se coloquen en días consecutivos ni en el mismo día.
    
    Por defecto vale `preferentemente`.

Aparece en:

* [`<sesion>`](#sesion).

Sesiones en distinto día
------------------------

Indica una lista de sesiones que se deberán impartir en distinto día de la principal.

Contiene los subelementos:

* `<sesion>`. Mín. 0, máx. ∞. Es de tipo [nonNegativeInteger](index.html#nonNegativeInteger). El identificador de la sesión que se debe impartir en distinto día de la principal.

Aparece en:

* [`<enDistintoDia>`](#enDistintoDia).

noConsecutivas
--------------

Declara una lista con las sesiones que no se deben impartir de forma consecutiva a la sesión actual.

Contiene los suelementos:

* `<sesion>`. Mín. 0, máx. ∞. Es de tipo [nonNegativeInteger](index.html#nonNegativeInteger). Es el identificador de una sesión que no pueda colocarse de forma consecutiva a la sesión actual.

Aparece en:

* [`<sesion>`](#sesion).

noCoincidentes
--------------

Declara una lista con las sesiones que no deben impartir en los mismos tramos que la sesión actual.

Contiene los suelementos:

* `<sesion>`. Mín. 0, máx. ∞. Es de tipo [nonNegativeInteger](index.html#nonNegativeInteger). Es el identificador de una sesión que no pueda colocarse en los mismos tramos que la sesión actual.

Aparece en:

* [`<sesion>`](#sesion).

previoA
-------

Declara una lista con las sesiones que deben ser posteriores a los días en que se imparten las entidades de esta sesión. Es decir, esta sesión es previa a las sesiones que aparecen en la lista.

Contiene los suelementos:

* `<sesion>`. Mín. 0, máx. ∞. Es de tipo [nonNegativeInteger](index.html#nonNegativeInteger). Es el identificador de una sesión que debe colocarse en días posteriores a los días ocupados por la sesión actual.

Aparece en:

* [`<sesion>`](#sesion).

posteriorA
----------

Declara una lista con las sesiones que deben ser previas a los días en que se imparten las entidades de esta sesión. Es decir, esta sesión es posterior a las sesiones que aparecen en la lista.

Contiene los suelementos:

* `<sesion>`. Mín. 0, máx. ∞. Es de tipo [nonNegativeInteger](index.html#nonNegativeInteger). Es el identificador de una sesión que debe colocarse en días previos a los días ocupados por la sesión actual.

Aparece en:

* [`<sesion>`](#sesion).

separadosNDiasOMas
------------------

Declara una lista con relaciones de separación entre una sesión y otras sesiones. En cada relación se indica la sesión con la que tiene la relación, y el número de días que, como mínimo, debe haber entre los días de ambas sesiones. Si se indican 0 días, la relación es equivalente a [`enDiasDistintos`](#enDiasDistintos).

Contiene los suelementos:

* `<separacion>`. Mín. 0, máx. ∞. Es de tipo [SeparacionSesionesType](#SeparacionSesionesType). Indica la separación, que como mínimo, debe cumplir la sesión actual con la sesión con la que está relacionada.

Aparece en:

* [`<sesion>`](#sesion).

separadosNDiasOMenos
--------------------

Declara una lista con relaciones de separación entre una sesión y otras sesiones. En cada relación se indica la sesión con la que tiene la relación, y el número de días que, como máximo, debe haber entre los días de ambas sesiones. Si se indican 0 días, los días pueden ser los mismos, o ser seguidos.

Contiene los suelementos:

* `<separacion>`. Mín. 0, máx. ∞. Es de tipo [SeparacionSesionesType](#SeparacionSesionesType). Indica la separación, que como máximo, debe cumplir la sesión actual con la sesión con la que está relacionada.

Aparece en:

* [`<sesion>`](#sesion).

SeparacionSesionesType
----------------------

.

Contiene los suelementos:

* `<sesion>`. Obligatorio. Es de tipo [](index.html#nonNegativeInteger). Indica el identificador de la sesión con el que guarda la relación.
* `<dias>`. Obligatorio. Es de tipo [](index.html#nonNegativeInteger). Indica el número de días definido sobre la relación.

Aparece en:

* [`<separadosNDiasOMas>`](#separadosNDiasOMas).
* [`<separadosNDiasOMenos>`](#separadosNDiasOMenos).

listasDeRelacion
----------------

El elemento `<listasDeRelacion>` declara la listas de relación e incompatibilidad entre sesiones así como sus opciones.

Contiene los subelementos:

* `[<simultaneas>](#simultaneas)` . Opcional.
* `[<consecutivas>](#consecutivas)` . Opcional.

Aparece en:

* [`<datosGHC>`](#datosGHC).

simultaneas
-----------

Indica la lista de bloques de sesiones que tienen que colocarse en el mismo tramo.

Contiene los subelementos:

* `[<bloqueDeSesiones>](#bloqueSimultaneas)` . Mín. 0, máx. ∞. Es de tipo [bloque de sesiones simultaneas](#bloqueSimultaneas). Nota, no confundir con el de [consecutivas](#bloqueConsecutivas).

Aparece en:

* [&lt;listasDeRelacion&gt;](#listasDeRelacion).

Bloque de sesiones simultaneas
------------------------------

El elemento `<bloqueDeSesiones>` perteneciente al elemento `[<simultaneas>](#simultaneas)` , declara un bloque de sesiones que deben ir en el mismo tramo.

Contiene los atributos:

* `id`. Obligatorio. Es de tipo [nonNegativeInteger](index.html#nonNegativeInteger). Es el identificador del bloque de sesiones simultaneas. Debe ser único. Será la referencia que usen las sesiones.
* `submarco`. Obligatorio. Es de tipo [NCName](index.html#NCName). Indica el submarco al que irán asociadas las sesiones que pertenezcan al bloque.

Contiene los subelementos:

* `[<sesiones>](#sesionesDeLosBloques)` . Obligatorio. Es de tipo [sesiones de los bloques](#sesionesDeLosBloques). Contiene una lista con las sesiones que deben ser simultaneas.
* `[<plantilla>](#PlantillaType)` . Opcional. Es de tipo [PlantillaType](#PlantillaType).

Aparece en:

* `[<simultaneas>](#simultaneas)` .

sesiones de los bloques
-----------------------

Indica una lista de identificadores de sesiones.

Contiene los subelementos:

* `<sesion>`. Mín. 1, máx. ∞. Es de tipo [nonNegativeInteger](index.html#nonNegativeInteger). Es el identificador de una sesión que pertenece a este bloque.

Aparece en:

* [Bloque de sesiones simultaneas](#bloqueSimultaneas).
* [Bloque de sesiones consecutivas](#bloqueConsecutivas).

consecutivas
------------

El elemento `<consecutivas>` indica los bloques de sesiones que se deben impartir de forma consecutiva. Las sesiones de un mismo bloque deben tener el mismo número de días con sesiones y la distribución debe ser fija.

Contiene los subelementos:

* `[<bloqueDeSesiones>](#bloqueConsecutivas)` . Mín. 0, máx. ∞. Es de tipo [bloque de sesiones consecutivas](#bloqueConsecutivas). No confundir con el [bloque de sesiones simultaneas](#bloqueSimultaneas).

Aparece en:

* [`<listasDeRelacion>`](#listasDeRelacion).

Bloque de sesiones consecutivas
-------------------------------

El elemento `<bloqueDeSesiones>` del elemento `[<consecutivas>](#consecutivas)` , declara un bloque de sesiones que deben colocarse de forma consecutivas.

Contiene los atributos:

* `id`. Obligatorio. Es de tipo [nonNegativeInteger](index.html#nonNegativeInteger). Es el identificador del bloque de sesiones consecutivas. Debe ser único. Será la referencia que usen las sesiones.

Contiene los subelementos:

* `[<sesiones>](#sesionesDeLosBloques)` . Obligatorio. Es de tipo [sesiones de los bloques](#sesionesDeLosBloques). Contiene una lista con las sesiones que deben ser consecutivas entre sí.
* `<conOrden>`. Opcional. Por defecto vale `desordenadas`. Es de tipo [string](index.html#string) restringido a los valores:
    * `desordenadas`. Indica que las sesiones deben ir seguidas pero no importa en que orden.
    * `seguidas`. Indica que las sesiones deben ir seguidas y en el orden en que están definidas.
    * `separadas`. Indica que las sesiones pueden ir en cualquier orden y no tienen que estar seguidas, solamente deben estar en el mismo día.

Aparece en:

* `[<consecutivas>](#consecutivas)` .

Optativas
---------

El elemento `<optativas>` declara la lista de conjuntos de de optativas.

Los datos de este elemento son usados por la versión de universidad de GHC.

Contiene los subelementos:

* `[<optativa>](#OptativaType)`. Mín. 0, máx. ∞. Es de tipo [OptativaType](#OptativaType).

Aparece en:

* [`<datosGHC>`](#datosGHC).

Optativa
--------

El elemento `<optativa>` declara un conjuntos de optativas que se pueden dar de forma simultanea.

Contiene los subelementos:

* `<nombre>`. Obligatorio. Es de tipo [NCName](index.html#NCName). Indica el nombre del conjunto de optativas. Debe ser único entre los conjuntos de optativas.
* `<grupo>`. Obligatorio. Es de tipo [NCName](index.html#NCName). Indica el nombre del grupo al que pertenecen las optativas.
* `<maxSolapadas>`. Obligatorio. Es de tipo [nonNegativeInteger](index.html#nonNegativeInteger). Indica la cantidad de sesiones lectivas que se pueden solapar al mismo tiempo.
* `<asignaturasOptativas>`. Obligatorio. Es del tipo anónimo [asignaturasOptativasType](#asignaturasOptativasType).

Aparece en:

* [`<optativas>`](#optativas).

Asignaturas de las Optativas
----------------------------

El elemento `<asignaturasOptativas>` es una lista de las sesiones lectivas que pertenecen a un conjunto de optativas y que pueden hacerse simultaneas entre ellas de acuerdo a las características del conjunto al que pertenezcan.

Contiene los subelementos:

* `<asignaturaOptativa>`. Mín. 0, máx. ∞. Es de tipo [nonNegativeInteger](index.html#nonNegativeInteger). Indica el id de la [sesión lectiva](#sesion) que pertenece al conjunto de optativas. Tenga en cuenta que las sesiones deben pertenecer al grupo indicado en el [conjunto de optativas](#OptativaType). Tiene el parámetro opcional `solapable` de tipo [booleano](index.html#booleano) que indica si la asignatura se puede solapar o no con las demás del conjunto, por defecto vale `true`.

Aparece en:

* [`<optativa>`](#OptativaType).

reuniones
---------

Indica una lista de las reuniones existentes.

Contiene los subelementos:

* `[<reunion>](#reunion)` . Mín. 0, máx. ∞.

Aparece en:

* [`<datosGHC>`](#datosGHC).

reunion
-------

El elemento `<reunion>` define una reunión.

Contiene los atributos:

* `subMarco`. Obligatorio. Es de tipo [NCName](index.html#NCName). Indica el marco al que está asociada la reunión.

Contiene los subelementos:

* `<nombre>`. Obligatorio. Es de tipo [NombreType](index.html#NombreType). Es el identificador de la reunión.
* `<numeroDeReuniones>`. Obligatorio. Es de tipo [unsignedByte](index.html#unsignedByte) restringido al rango 1 a 5 (ambos inclusive). Indica la cantidad de reuniones a la semana que deberán tener los profesores asignados.
* `<dobleDuracion>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si la reunión ocupará uno (`false`) o dos (`true`) tramos.
* `<tipoDeTarea>`. Obligatorio. Es de tipo [NombreType](index.html#NombreType). Indica el identificador de la tarea a la que va asociada la reunión.
* `<lectiva>`. Opcional. Es de tipo [Booleano](index.html#booleano). Por defecto vale `false`. Indica si se tendrá en cuenta para la preferencia sobre intervalos de duración diaria del profesor (si es `true`).
* `[<plantilla>](#plantillaPDFType)` . Opcional. Es de tipo [PlantillaPDFType](#plantillaPDFType).
* `[<integrantes>](integrantesDeReunion)` . Obligatorio. Es de tipo [integrantes de reunión](#integrantesDeReunion).
* [`<distribucionSemanal>`](#distribucionSemanal) _**Deprecated.**_. Utilizar el elemento `distribucionPeriodica` Define cómo es la distribución sobre la que se deben impartir esta reunión.
* [`<distribucionPeriodica>`](#distribucionPeriodica). Obligatorio (aunque si no viene este elemento obtiene su valor de `distribucionSemanal`. Indica la distribución y los [periodos](#periodos) en que tiene que colocarse.
* `<mismaPosicionDistintosPeriodos>`. Opcional. Es de tipo [preferenciaMismaPosicionDistintosPeriodos](#preferenciaMismaPosicionDistintosPeriodos). Por defecto vale `ignorar`. Indica el tipo de criterio con el que se ha de intentar colocar las entidades de esta sesión que pertenecen a distintos periodos en la misma posición.

Aparece en:

* `[<reuniones>](#reuniones)` .

Integrantes de reunión
----------------------

El elemento `<integrantes>` indica una lista de integrantes que deben asistir a la reunión.

Contiene los subelementos:

* `<integrante>`. Mín. 1, máx. ∞. Es de tipo [NombreType](index.html#NombreType). Es el nombre de uno de los profesores que pertenecen a la lista (y por lo tanto deben asistir a la reunión).

Aparece en:

* `[<reunion>](#reunion)` .

guardias
--------

Indica la lista de guardias existentes.

Contiene los subelementos:

* `[<guardia>](#guardia)` . Mín. 0, máx. ∞.

Aparece en:

* [`<datosGHC>`](#datosGHC).

guardia
-------

Define una guardia. Esta guardia será identificada por el nombre.

Contiene los atributos:

* `subMarco`. Obligatorio. Es de tipo [NCName](index.html#NCName). Indica el marco al que está asociada la guardia.

Contiene los subelementos:

* `<nombre>`. Obligatorio. Es de tipo [NombreType](index.html#NombreType). Sirve para identificar la guardia y por lo tanto debe ser único en la lista de guardias.
* `<tipoDeTarea>`. Obligatorio. Es de tipo [NombreType](index.html#NombreType). Indica la tarea asociada a la guardia.
* `<enRecreos>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si será una guardia de recreos (`true`) o no (`false`).
* `<lectiva>`. Opcional. Es de tipo [Booleano](index.html#booleano). Por defecto vale `false`. Indica si se tendrá en cuenta para la preferencia sobre intervalos de duración diaria del profesor (si es `true`).
* `[<profesoresACadaHora>](#profesoresACadaHora)` . Obligatorio.
* `[<integrantes>](#integrantesDeGuardia)` . Obligatorio. Es de tipo [integrantes de guardia](#integrantesDeGuardia).
* [`<plantilla>`](#PlantillaPDType). Opcional. Es una plantilla del tipo [PlantillaPDType](#PlantillaPDType). Indica si se puede colocar la guardia en los diferentes tramos, los tramos omitidos si consideran como permitidos.
* `<enPeriodos>`. Opcional. Es de tipo `[enPeriodos](#enPeriodos)`. Indica los periodos en que se **repite** el servicio de guardias. Para cada periodo es independiente el servicio de guardias. Si no aparece, se considera que se refiere únicamente al primer periodo.
* `<mismaPosicionDistintosPeriodos>`. Opcional. Es de tipo [preferenciaMismaPosicionDistintosPeriodos](#preferenciaMismaPosicionDistintosPeriodos). Por defecto vale `ignorar`. Indica el tipo de criterio con el que se ha de intentar colocar las entidades de esta sesión que pertenecen a distintos periodos en la misma posición.

Aparece en:

* [`<guardias>`](#guardias).

profesoresACadaHora
-------------------

El elemento `<profesoresACadaHora>` indica cuantos profesores son necesarios a cada hora de la guardia.

Contiene los subelementos:

* `<cantidad>`. Obligatorio. Es de tipo [unsignedByte](index.html#unsignedByte) restringido al rango 1 a 8 (ambos inclusive). Indica la cantidad de profesores que tiene que haber en cada tramo. En caso de que falte algún tramo (o si no se ponen tramos) este será el valor que tendrán.
* [`<porTramo>`](#porTramo). Opcional.

Aparece en:

* [`<guardia>`](#guardia).

porTramo
--------

El elemento `<porTramo>` indica una lista con la cantidad de profesores que tendrá que haber especificamente en cada tramo.

Los tramos vendrán indicados mediante los atributos `dia` , `indice` y el submarco asociado a la guardia.

Contiene los subelementos:

* `<cantidadTramo>`. Mín. 0, máx. ∞. Tiene el valor de tipo [unsignedByte](index.html#unsignedByte) restringido al rango 0 a 8 (ambos inclusive). Que indica la cantidad de profesores que se tienen que colocar en este tramo. También tiene los atributos:
    * `dia`. Obligatorio. Es de tipo [unsignedByte](index.html#unsignedByte) pero restringido al rango 0 a 4 (ambos inclusive). Indica el día del tramo.
    * `indice`. Obligatorio. Es de tipo [int](index.html#int). Indica el índice del tramo.

Aparece en:

* `[<profesoresACadaHora>](#profesoresACadaHora)` .

Integrantes de guardias
-----------------------

El elemento `<integrantes>` indica la lista de profesores que tienen que cubrir las guardias.

Contiene los subelementos:

* `[<integrante>](#integranteDeGuardia)` . Mín. 0, máx. ∞. Es de tipo [integrante de guardia](#integranteDeGuardia).

Integrante de guardia
---------------------

El elemento `<integrante>` de las guardias declara uno de los profesores que deben cubrir la guardia.

Contiene los subelementos:

* `<nombre>`. Obligatorio. Es de tipo [NombreType](index.html#NombreType). Indica el nombre del profesor que tiene que cubrir la guardia.
* `<numeroDeGuardias>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte) pero restringido al rango 1 a 20 (ambos inclusive). Por defecto vale 1. Indica cuantas guardias a la semana debe cubrir el profesor.
* `[<plantilla>](#plantillaPDFType)` . Opcional. Es de tipo [PlantillaPDFType](#plantillaPDFType). Indica preferencia de cubrir ciertos tramos.

Aparece en:

* [`<integrantes>`](#integrantesDeGuardia). [Integrantes de guardia](#integrantesDeGuardia).

complementarias
---------------

El elemento `<complementarias>` declara una lista de sesiones complementarias que se deben colocar en el horario.

Contiene los subelementos:

* [`<complementaria>`](#complementaria). Mín. 0, máx. ∞.

Aparece en:

* [`<datosGHC>`](#datosGHC).

complementaria
--------------

Define una sesión complementaria y sus opciones.

Contiene los atributos:

* `subMarco`. Obligatorio. Es de tipo [NCName](index.html#NCName). Indica el marco al que está asociada la sesión complementaria.

Contiene los subelementos:

* `<identificador>`. Obligatorio. Es de tipo [string](index.html#string). Debería tener 1 carácter como mínimo y ser único en la lista de sesiones complementarias. Es el identificador de la sesión complementaria.
* `<tarea>`. Obligatorio. Es de tipo [NombreType](index.html#NombreType). Es el identificador de la tarea que tiene asignada la sesión complementaria.
* `<profesor>`. Obligatorio. Es de tipo [NombreType](index.html#NombreType). Es el nombre del profesor que debe impartir la sesión complementaria.
* `<lectiva>`. Opcional. Es de tipo [Booleano](index.html#booleano). Por defecto vale `false`. Indica si se tendrá en cuenta para la preferencia sobre intervalos de duración diaria del profesor (si es `true`).
* `[<plantilla>](#plantillaPDFType)` . Opcional. Es de tipo [PlantillaPDFType](#plantillaPDFType). Indica preferencia de colocar la sesión complementaria en ciertos tramos.
* [`<distribucionSemanal>`](#distribucionSemanal) _**Deprecated.**_. Utilizar el elemento `distribucionPeriodica` Define cómo es la distribución sobre la que se deben impartir esta complementaria.
* [`<distribucionPeriodica>`](#distribucionPeriodica). Obligatorio (aunque si no viene este elemento obtiene su valor de `distribucionSemanal`. Indica la distribución y los [periodos](#periodos) en que tiene que colocarse.
* `<mismaPosicionDistintosPeriodos>`. Opcional. Es de tipo [preferenciaMismaPosicionDistintosPeriodos](#preferenciaMismaPosicionDistintosPeriodos). Por defecto vale `ignorar`. Indica el tipo de criterio con el que se ha de intentar colocar las entidades de esta sesión que pertenecen a distintos periodos en la misma posición.
* `<intervalosSemanales>`. _**Deprecated.**_. Es de tipo [unsignedByte](index.html#unsignedByte) pero restringido al rango 1 a 20 (ambos inclusive). Indica la cantidad de tramos a la semana que tendrá esta sesión complementaria.
* `<maxIntervalosDiarios>`. _**Deprecated.**_. Es de tipo [unsignedByte](index.html#unsignedByte) pero restringido al rango 1 a 5 (ambos inclusive). Por defecto vale 5. Indica el número máximo de tramos que puede tener en un mismo día.
* `<noConsecutivos>`. _**Deprecated.**_. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si los tramos de un mismo día deben ir consecutivos (`false`) o si se pueden no colocar consecutivos (`true`).

Aparece en:

* [`<complementarias>`](#complementarias).

criterios
---------

El elemento `<criterios>` guarda los pesos que tendrán las distintas opciones.

Los elementos que no aparezcan se les tomará como con los valores por defecto.

Contiene los subelementos:

* `[<huecosEnHorario>](#huecosEnHorario)` . Opcional.
* `[<posicionesNoPreferentes>](#posicionesNoPreferentes)` . Opcional.
* `[<colocarSesionesLectivas>](#colocarSesionesLectivas)` . Opcional.
* `[<horarioDeProfesores>](#horarioDeProfesores)` . Opcional.

Aparece en:

* [`<datosGHC>`](#datosGHC).

huecosEnHorario
---------------

Agrupa las opciones relacionadas con los pesos de los huecos.

Contiene los subelementos:

* `<huecosEnGrupos>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte). Por defecto vale 5. Indica el peso que se asigna al hecho de dejar huecos en los horarios de los grupos.
* `<huecosEnProfesores>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte). Por defecto vale 2. Indica el peso que se asigna a dejar huecos en los horarios de los profesores.

Aparece en:

* `[<criterios>](#criterios)` .

posicionesNoPreferentes
-----------------------

Agrupa las opciones relacionadas con con los pesos de la colocación en tramos no preferentes.

Contiene los subelementos:

* `<enGrupos>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte). Por defecto vale 4. Indica el peso de colocar en un tramo no preferente de un grupo.
* `<enProfesores>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte). Por defecto vale 3. Indica el peso de colocar en un tramo no preferente de un profesor.
* `<enMateriasYTareas>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte). Por defecto vale 1. Indica el peso de colocar en un tramo no preferente de las materias o tareas.
* `<enSesionesLectivas>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte). Por defecto vale 2. Indica el peso de colocar en un tramo no preferente de una sesión lectiva.

Aparece en:

* `[<criterios>](#criterios)` .

colocarSesionesLectivas
-----------------------

Agrupa las opciones relacionadas con los pesos de colocar las sesiones lectivas en tramos extremos o de manera especial.

Contiene los subelementos:

* `<enDiasConsecutivos>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte). Por defecto vale 1. Indica el peso de colocar las sesiones en días seguidos (solo es aplicable cuando solo se imparte en 2 o 3 días).
* `<enAulaNoPreferente>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte). Por defecto vale 3. Indica el peso de colocar una sesión en una aula del conjunto de alternativas en vez de en la preferente.
* `<enHorasExtremas>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte). Por defecto vale 2. Indica el peso de colocar una sesión en las horas de los extremos de un horario.
* `<coincidanPorLaTarde>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte). Por defecto vale 1. Indica el peso de colocar varias veces la misma sesión en los turnos de la tarde.
* `<coincidanALaMismaHora>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte). Por defecto vale 0. Indica el peso de colocar la sesión en misma hora varios días.
* `<conCambiosDeAula>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte). Por defecto vale 1. Indica el peso de colocar las sesiones en aulas diferentes o de que se un grupo deba cambiar de aula.
* `<optativaSolapada>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte). Por defecto vale 1. Indica el peso de colocar varias sesiones optativas de universidad de manera que se solapen.

Aparece en:

* `[<criterios>](#criterios)` .

horarioDeProfesores
-------------------

Agrupa las opciones de los pesos de los horarios de los profesores.

Contiene los subelementos:

* `<horasExcluyentes>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte). Por defecto vale 3. Indica el peso de colocar las sesiones del profesor en horas problemáticas (a primera y a última, por la mañana y por la tarde en el mismo día, etc).
* `<masClasesEnUnDiaQueEnOtro>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte). Por defecto vale 3. Indica el peso de colocar las sesiones de un profesor de forma no uniforme durante la semana.
* `<horasDeClaseSeguidas>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte). Por defecto vale 2. Indica el peso de colocar más sesiones seguidas que las declaradas en su cuadro de opciones.
* `<masPermanencia>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte). Por defecto vale 2. Indica el peso de que tenga más horas de permanencia semanal, contando los huecos entre sesiones, que las declaradas como máximo en el cuadro de propiedades de cada uno.
* `<seguidoConElMismoGrupo>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte). Por defecto vale 1. Indica el peso de tenga sesiones seguidas impartidas al mismo grupo.
* `<guardiasEnExtremos>`. Opcional. Es de tipo [unsignedByte](index.html#unsignedByte). Por defecto vale 1. Indica el peso de que le toquen las guardias en los extremos de su horario, intentando así encajarlas en los huecos de sus sesiones lectivas.
* `<ordenProfesores>`. Opcional. Es de tipo [unsignedShort](index.html#unsignedShort). Por defecto vale 1. Indica el peso de que no se respete el orden del profesor, con lo que a mayor valor más se intentará respetar el orden de los profesores.

Aparece en:

* `[<criterios>](#criterios)` .

horario
-------

El elemento `<horario>` define una solución del horario.

Contiene los subelementos:

* `[<tramo>](#tramoDeHorario)` . Mín. 0, máx. ∞. Es de tipo [tramo de horario](#tramoDeHorario).

Aparece en:

* [`<datosGHC>`](#datosGHC).

Tramo de horario
----------------

El elemento `<tramo>` del [horario](#horario), contiene las referencias de lo que se ha colocado en un determinado tramo.

Contiene los atributos:

* `marco`. Obligatorio. Es de tipo [NCName](index.html#NCName). Indica el marco al que pertenece el tramo referenciado.
* `dia`. Obligatorio. Es de tipo [unsignedByte](index.html#unsignedByte) pero restringido al rango 0 a 4 (ambos inclusive). Indica el día al que pertenece el tramo.
* `indice`. Obligatorio. Es de tipo [int](index.html#int). Indica el índice del tramo referenciado.

Contiene los subelementos:

* `[<aula>](#aulaDeHorario)` . Mín. 0, máx. ∞. Es de tipo [aula de horario](#aulaDeHorario).
* `<reunion>`. Mín. 0, máx. ∞. Tipo [NombreType](index.html#NombreType). Es el nombre de la reunión colocada en este tramo.
* `[<guardia>](#guardiaDeHorario)` . Mín. 0, máx. ∞. Es de tipo [guardia de horario](#guardiaDeHorario).
* `<complementaria>`. Mín. 0, máx. ∞. Es de tipo [string](index.html#string). Es el identificador de una sesión complementaria que esté colocada en este tramo.

Aparece en:

* `[<horario>](#horario)` .

Aula de horario
---------------

El elemento `<aula>` de los [tramos de horario](#tramoDeHorario), declara las sesiones y profesores que se han colocado en una determinada aula.

En caso de aparecer el atributo `anonima` , indica que el aula es anónima y el valor es el conjunto del que se ha seleccionado (en este caso el `id` solo sería para diferenciar aulas anónimas y podría ser cualquier valor, además de poder ser omitido). Si no aparece indica que es un aula con nombre y el `id` indica el identificador del aula (que debería aparecer en la lista de aulas). Debe aparecer obligatoriamente uno de los dos atributos, o el `id` o el `anonima` .

Solo aparecerá el profesor principal asignado a la sesión; Es decir el principal original de la sesión o el alternativo si el motor escogió el profesor alternativo configurado en la sesión. El profesor principal de las sesiones no se debe tener en cuenta a no ser que no haya subelementos `<profesor>`, sin embargo el resto de profesores ([&lt;otrosProfesores&gt;](#otrosProfesores)) sí que se tienen que tener en cuenta y siempre se consideran asignados en el aula, tramo y sesión correspondiente.

Para calcular que profesores están asignados, se deberá realizar el siguiente proceso:

1.  Si hay un elemento `<profesor>`, se toma este. Si no, se tomara el principal de la sesión.
2.  Se tomarán todos los profesores del elemento [`<otrosProfesores>`](#otrosProfesores) de la sesión.

Contiene los atributos:

* `id`. Opcional. Tipo [NombreType](index.html#NombreType). Es el identificador del aula que se está usando en el tramo o un identificador temporal si es un aula anónima.
* `anonima`. Opcional. Tipo [NombreType](index.html#NombreType). Indica el nombre de un conjunto de aulas.

Contiene los subelementos:

* `<sesion>`. Mín. 1, máx. ∞. Extiende al tipo [nonNegativeInteger](index.html#nonNegativeInteger). Es el identificador de una sesión que está colocada en esta aula (en el tramo al que pertenezca). Contiene los siguientes atributos:
    * `refAula`. Opcional. Tipo [NombreType](index.html#NombreType). Indica a qué aula definida en la sesión se corresponde esta asignación.
* `<profesor>`. Mín. 0, máx. ∞. Tipo [NombreType](index.html#NombreType). Es el nombre de un profesor que se ha usado para impartir la/las sesiones en este aula (del tramo al que pertenezca).

Aparece en:

* `[<tramo>](#tramoDeHorario)` . [Tramo de horario](#tramoDeHorario).

Guardia de horario
------------------

El elemento `<guardia>` declara una guardia que ha sido asignada a un determinado tramo.

Contiene los subelementos:

* `<nombre>`. Obligatorio. Tipo [NombreType](index.html#NombreType). Indica el nombre de la guardia que se está cubriendo.
* `<profesor>`. Obligatorio. Mín. 1, máx. ∞. Tipo [NombreType](index.html#NombreType). Indica los nombres de los profesores que cubren la guardia. Deberían ser uno de sus integrantes.

Aparece en:

* `[<tramo>](#tramoDeHorario)` . [Tramo de horario](#tramoDeHorario).

otros
-----

El elemento `<otros>` contiene otras funciones auxiliares del xml, como puede ser el intercambio de mensajes entre el planificador y la captación de desideratas.

Contiene los subelementos:

* `[<restriccionesCD>](#restriccionesCD)` . Opcional.
* `[<funcionesAdicionales>](#funcionesAdicionales)` . Opcional.
* `[<mensajesIntercambio>](#mensajesIntercambio)` . Opcional.
* `[<opciones>](#otrasOpciones)` . Opcional. Es del tipo [Otras opciones](#otrasOpciones).
* `<notas>`. Opcional. Es de tipo [string](index.html#string). Guarda una anotación que puede usar el usuario.
* [`<gruposAlejados>`](#gruposAlejados). Opcional.
* [`<extensiones>`](#extensiones). Opcional.
* [`<perfil>`](#perfil). Opcional.
* [`<claveXDias>`](#claveXDias). Opcional.  
    
* `<origenDatos>`. Opcional. Es de tipo [string](index.html#string). Guarda un identificador de la aplicación de terceros de la que se obtuvieron los datos, por ejemplo al hacer una importación.

Aparece en:

* [`<datosGHC>`](#datosGHC).

restriccionesCD
---------------

Contiene las opciones de restricción del modulo de captación de desideratas.

Contiene los subelementos:

* `<permitirAgregarProfesor>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si está permitido que se puedan agregar nuevos profesores en el módulo de captación de desideratas.
* `<permitirAgregarDepartamento>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si está permitido que se agregen nuevos departamentos en el módulo de captación de desideratas.
* `<permitirAgregarAsignatura>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si esta permitido agregar nuevas asignaturas (sesiones) en el módulo de captación de desideratas.
* `<permitirCamDepProfesor>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si está permitido cambiar de departamento a los profesores en el módulo de captación de desideratas.
* `<permitirCamDepAsignatura>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si está permitido cambiar el departamento de las asignaturas en el módulo de captación de desideratas.
* `<permitirCamDuracion>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si se permite cambiar la duración semanal de las sesiones en el módulo de captación de desideratas.
* `<permitirCamHorasReduccion>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si se permite cambiar la cantidad de reducción de horas por cargo del profesor en el módulo de captación de desideratas.

Aparece en:

* `[<otros>](#otros)` .

funcionesAdicionales
--------------------

El elemento `<funcionesAdicionales>` indica si están disponibles las distintas funcinoes y opciones en el modulo de captación de desideratas.

Contiene los subelementos:

* `[<restriccionDePlantilla>](#restriccionDePlantilla)` . Opcional.
* `<definirTutor>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `true`. Indica si se permite que se establezca si un profesor quiere ser tutor o no en el módulo de captación de desideratas.
* `<elegirGrupoTutor>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica que en caso de que se pueda decidir si un profesor es tutor o no, pueda escoger también el grupo del que posiblemente será tutor.
* `<hacerGuardias>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `true`. Indica si se permite que los profesores elijan que puedan hacer guardias o no.
* `<cambiarAula>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si se permite que en el módulo de captación de desideratas se permita cambiar el aula de una sesión.
* `<permitirDistAlt>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si se permite en el módulo de captación de desideratas permitir o no establecer una distribución alternativa de los tramos de las sesiones.

Aparece en:

* `[<otros>](#otros)` .

restriccionDePlantilla
----------------------

El elemento `<restriccionDePlantilla>` contiene los elementos que declaran las restricciones de las plantillas de los profesores.

Contiene los subelementos:

* `<cantidadDeProhibidos>`. Opcional. Es de tipo [entero](#entero). Por defecto vale _0_. Indica la cantidad de prohibidos que se puede colocar en la plantilla de los profesores. Un valor negativo indica que no hay ninguna restricción.
* `<cantidadDePrefNo1>`. Opcional. Es de tipo [entero](#entero). Por defecto vale _-1_. Indica la cantidad de PreferentementeNo1 que se puede colocar en la plantilla de los profesores. Un valor negativo indica que no hay ninguna restricción.
* `<cantidadDePrefNo2>`. Opcional. Es de tipo [entero](#entero). Por defecto vale _-1_. Indica la cantidad de PreferentementeNo2 que se pueden colocar en la plantilla de los profesores. Un valor negativo indica que no hay ninguna restricción.

Aparece en:

* `[<funcionesAdicionales>](#funcionesAdicionales)` .

mensajesIntercambio
-------------------

Contiene los elementos que dan soporte al intercambio de mensajes.

Contiene los subelementos:

* `[<haciaDesideratas>](#haciaDesideratas)` . Opcional.

Aparece en:

* `[<otros>](#otros)` .

Otras opciones
--------------

El elemento `<opciones>` declara las opciones globales del horario.

Contiene los subelementos:

* `[<opcionesGenerales>](#opcionesGenerales)` . Opcional.
* `[<valorInicialProfesores>](#opcionesDeProfesor)` . Opcional. Es de tipo [Opciones de profesor](#opcionesDeProfesor). Indica los valores de las opciones de los profesores que inicialmente tendrán los profesores al ser creados.
* `[<valorInicialSesiones>](#OpcionesDeSesionType)` . Opcional. Es de tipo [Opciones de sesión](#OpcionesDeSesionType). Indica los valores de las opciones de las sesiones que tendrán inicialmente al ser creadas.

Aparece en:

* `[<otros>](#otros)` .

opcionesGenerales
-----------------

Declara las opciones generales.

Contiene los subelementos:

* `<contarHuecosMediodia>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `true`. Indica para los profesores que tengan mañana y tarde contar como huecos los intervalos entre las sesiones de la mañana y las de la tarde. Si a un profesores se le asignan sesiones de cualquier tipo, de mañana y de tarde el mismo día, se les contarán como huecos en su horario y horas de permanencia en el centro los intervalos no ocupados situados entre las correspondientes sesiones de la mañana y de la tarde.
* `<desecharGuardias>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si se generan resultados completos aunque no coloque todas las guardias (desechar las guardias no colocadas). Esta opción que permite generar resultados completos aunque no se puedan encajar todas las guardias previstas. Simplemente se desecharían las posiciones de guardia que no se hayan podido encajar en el resultado.
* `<mantener5Sesiones>`. _**Deprecated.** Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. En el caso de profesores con 20, 21, 22, 23 ó 24 sesiones lectivas semanales, mantener un máximo de 5 sesiones al día. Esta opción le permite, en estos casos particulares, reducir el máximo de 6 a 5 sesiones lectivas diarias._
* `<minimoHuecosGrupos>`. _**Deprecated.**Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si se da prioridad a quitar los huecos del horario de los grupos._
* `<minMaxSesiones>`. _**Deprecated.** Este elemento ya no se debe usar y solo aparece definido por compatibilidad con versiones anteriores. Su uso será ignorado. Antigua definición: Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si se dará prioridad al máximo/mínimo de sesiones diarias de los profesores._
* `<posNoPrefDeGrupos>`. _**Deprecated.** Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si se prioriza el horario cuando se observa colocaciones en posiciones no preferentes de los grupos._
* `<maxHoraPermanencia>`. _**Deprecated.** Este elemento ya no se debe usar y solo aparece definido por compatibilidad con versiones anteriores. Su uso será ignorado. Antigua definición: Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si se priorizará al observar la máximas horas de permanencia de los profesores._

Aparece en:

* [Otras opciones](#otrasOpciones).

gruposAlejados
--------------

Declara los grupos que se encuentran alejados.

Contiene los subelementos:

* `[<opciones>](#opcionesDeGruposAlejados)` . Opcional. Es de tipo [Opciones de grupos alejados](#opcionesDeGruposAlejados).
* `[<listaDeGrupos>](#listaDeGruposAlejados)` . Opcional. Es de tipo [Lista de grupos alejados](#listaDeGruposAlejados).

Aparece en:

* `[<otros>](#otros)` .

Opciones de grupos alejados
---------------------------

Declara las opciones de los grupos alejados.

Contiene los subelementos:

* `<actualizarAlGenerar>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si se actualizarán las relaciones cada vez que se vaya a generar un horario, haciendo que aunque se cambien las relaciones estas estén actualizadas al generar el horario.
* `<evitarDobleDesp>`. Opcional. Es de tipo [booleano](index.html#booleano). Por defecto vale `false`. Indica si se intentará evitar que un profesor tenga que desplazarse varias veces en un mismo día. Además tiene el atributo opcional `tipo` que puede tener los valores `evitar` o `prohibir`. El valor `evitar` del atributo `tipo` indica que será una condición ponderable (es el valor por defecto si no aparece el atributo), mientras que el valor `prohibir` indica que no se considerará válido un horario con un profesor tenga un doble desplazamiento en el mismo día (criterio estricto).

Aparece en:

* [`<gruposAlejados>`](#gruposAlejados).

Lista de grupos alejados
------------------------

Declara la lista de los grupos alejados.

Contiene los subelementos:

* `<grupo>`. Mín. 0, máx. ∞. Es de tipo [NombreType](index.html#NombreType). Indica el nombre de uno de los grupos alejados. El nombre debe existir en la lista de grupos.

Aparece en:

* [`<gruposAlejados>`](#gruposAlejados).

haciaDesideratas
----------------

Contiene los mensajes que serán leidos y mostrados por el capta desideratas, y supuestamente a los profesores.

Contiene los subelementos:

* `<texto>`. Opcional. Es de tipo [string](index.html#string). Contiene el texto que se mostrará al cargar el archivo en Capta desideratas GHC.

Aparece en:

* `[<mensajesIntercambio>](#mensajesIntercambio)` .

Plantilla
---------

Esta plantilla define las preferencias de los tramos. La plantilla (como todas las plantillas) se declara mediante el elemento `<plantilla>` .

Si no aparece algún tramo se tomará como si fuese disponible o si no aparece la plantilla, se tomarán todos los tramos como disponibles.

Contiene los subelementos:

[`<tramo>`](#tramoType). Mín. 0, máx. ∞. Es de tipo [TramoType](#tramoType).

Aparece en:

* [`<sesion>`](#sesion).

TramoType
---------

Define la preferencia de un tramo concreto. Como todos los tramos, está definido mediante el elemento `<tramo>` . El tramo al que hace referencia viene determinado por los atributos. Por defecto vale disponible.

Puede tener uno de los valores:

* `prohibido`. Indica que no se puede usar el tramo referenciado.
* `preferentementeNo2`. Indica que se intentará no usar el tramo referenciado.
* `preferentementeNo1`. Indica que se intentará no usar el tramo referenciado pero en menor medida que la 2.
* `disponible`. Indica que se puede usar el tramo referenciado.
* `fijado`. Indica que está en uso el tramo referenciado.

Tiene los atributos:

* `dia`. Obligatorio. Es de tipo [unsignedByte](index.html#unsignedByte) pero restringido al rango 0 a 4 (ambos inclusive). Indica el día al que pertenece el tramo.
* `indice`. Obligatorio. Es de tipo [int](index.html#int). Indica el índice del tramo referenciado.

Aparece en:

* [`<plantilla>`](#PlantillaType). [PlantillaType](#PlantillaType).

Plantilla sin fijado
--------------------

Esta plantilla define las preferencias de los tramos pero sin el valor fijado. La plantilla (como todas las plantillas) se declara mediante el elemento `<plantilla>` .

Si no aparece algún tramo se tomará como si fuese disponible o si no aparece la plantilla, se tomarán todos los tramos como disponibles.

Contiene los subelementos:

[`<tramo>`](#tramoSinFType). Mín. 0, máx. ∞. Es de tipo [TramoSinFType](#tramoSinFType).

Aparece en:

* [`<materia>`](#materia).
* [`<grupo>`](#grupo).
* [`<profesor>`](#profesor).
* [`<tarea>`](#tarea).

TramoSinFType
-------------

Define la preferencia de un tramo concreto pero sin el valor fijado. Como todos los tramos, está definido mediante el elemento `<tramo>` . El tramo al que hace referencia viene determinado por los atributos. Por defecto vale disponible.

Puede tener uno de los valores:

* `prohibido`. Indica que no se puede usar el tramo referenciado.
* `preferentementeNo2`. Indica que se intentará no usar el tramo referenciado.
* `preferentementeNo1`. Indica que se intentará no usar el tramo referenciado pero en menor medida que la 2.
* `disponible`. Indica que se puede usar el tramo referenciado.

Tiene los atributos:

* `marco`. Obligatorio. Es de tipo [NCName](index.html#NCName). Indica el marco al que pertenece el tramo referenciado.
* `dia`. Obligatorio. Es de tipo [unsignedByte](index.html#unsignedByte) pero restringido al rango 0 a 4 (ambos inclusive). Indica el día al que pertenece el tramo.
* `indice`. Obligatorio. Es de tipo [int](index.html#int). Indica el índice del tramo referenciado.

Aparece en:

* [`<plantilla>`](#plantillaSinFType). [PlantillaSinFType](#plantillaSinFType).

Plantilla de prohibido, disponible y fijado
-------------------------------------------

Esta plantilla define si los tramos son no disponibles, disponibles o en uso. La plantilla (como todas las plantillas) se declara mediante el elemento `<plantilla>` .

Si no aparece algún tramo se tomará como si fuese disponible o si no aparece la plantilla, se tomarán todos los tramos como disponibles.

Contiene los subelementos:

[`<tramo>`](#tramoPDFType). Mín. 0, máx. ∞. Es de tipo [TramoPDFType](#tramoPDFType).

Aparece en:

TramoPDFType
------------

Define si un tramo no está disponible, si sí que lo está o si está en uso. Como todos los tramos, está definido mediante el elemento `<tramo>` . El tramo al que hace referencia viene determinado por los atributos. Por defecto vale disponible.

Puede tener uno de los valores:

* `prohibido`. Indica que no se puede usar el tramo referenciado.
* `disponible`. Indica que se puede usar el tramo referenciado.
* `fijado`. Indica que el tramo está en uso.

Tiene los atributos:

* `marco`. Obligatorio. Es de tipo [NCName](index.html#NCName). Indica el marco al que pertenece el tramo referenciado.
* `dia`. Obligatorio. Es de tipo [unsignedByte](index.html#unsignedByte) pero restringido al rango 0 a 4 (ambos inclusive). Indica el día al que pertenece el tramo.
* `indice`. Obligatorio. Es de tipo [int](index.html#int). Indica el índice del tramo referenciado.

Aparece en:

* [`<plantilla>`](#plantillaPDFType). [PlantillaPDFType](#plantillaPDFType).

Plantilla de prohibido y disponible
-----------------------------------

Esta plantilla define si los tramos estan disponibles o no. La plantilla (como todas las plantillas) se declara mediante el elemento `<plantilla>` .

Si no aparece algún tramo se tomará como si fuese disponible o si no aparece la plantilla, se tomarán todos los tramos como disponibles.

Contiene los subelementos:

[`<tramo>`](#tramoPDType). Mín. 0, máx. ∞. Es de tipo [TramoPDType](#tramoPDType).

Aparece en:

* [`<aula>`](#aula).

TramoPDType
-----------

Define si un tramo está disponible o no. Como todos los tramos, está definido mediante el elemento `<tramo>` . El tramo al que hace referencia viene determinado por los atributos. Por defecto vale disponible.

Puede tener uno de los valores:

* `prohibido`. Indica que no se puede usar el tramo referenciado.
* `disponible`. Indica que se puede usar el tramo referenciado.

Tiene los atributos:

* `marco`. Obligatorio. Es de tipo [NCName](index.html#NCName). Indica el marco al que pertenece el tramo referenciado.
* `dia`. Obligatorio. Es de tipo [unsignedByte](index.html#unsignedByte) pero restringido al rango 0 a 4 (ambos inclusive). Indica el día al que pertenece el tramo.
* `indice`. Obligatorio. Es de tipo [int](index.html#int). Indica el índice del tramo referenciado.

Aparece en:

* [`<plantilla>`](#PlantillaPDType). [PlantillaPDType](#PlantillaPDType).

Extensiones
-----------

Permite extender el xml con elementos personalizados, que puedan definirse en un futuro o para uso concreto de otras aplicaciones externas.

Se declara mediante el elemento `<extensiones>` . Los subelementos pueden ser de cualquier tipo y tener cualquier nombre además de poder aparecer repetido.

Estos elementos serán validados si se encuentra el esquema adecuado pero sino simplemente serán ignorados.

Contiene los subelementos:

* `any`. Es cualquier definición de elemento. Mín. 0, máx. ∞. Es de tipo any.

Aparece en:

* `[<otros>](#otros)` .

Perfil
------

Indica con que perfil de GHC se creó el archivo.

Puede tener uno de los siguientes valores:

* `primaria`. Indica que se creó con el perfil de primaria.
* `secundaria`. Indica que se creó con el perfil de secundaria.
* `universidad`. Indica que se creó con el perfil de universidad.

Aparece en:

* `[<otros>](#otros)` .

claveXDias
----------

Contiene una lista con las claves de exportación de los días de las semanas.

Contiene los subelementos:

* `lunes`. Indica la clave de exportación correspondiente a los lunes. Mín. 0, máx. 1\. Es de tipo [String](index.html#string).
* `martes`. Indica la clave de exportación correspondiente a los martes. Mín. 0, máx. 1\. Es de tipo [String](index.html#string).
* `miercoles`. Indica la clave de exportación correspondiente a los miércoles. Mín. 0, máx. 1\. Es de tipo [String](index.html#string).
* `jueves`. Indica la clave de exportación correspondiente a los jueves. Mín. 0, máx. 1\. Es de tipo [String](index.html#string).
* `viernes`. Indica la clave de exportación correspondiente a los viernes. Mín. 0, máx. 1\. Es de tipo [String](index.html#string).
* `sabado`. Indica la clave de exportación correspondiente a los sábado. Mín. 0, máx. 1\. Es de tipo [String](index.html#string).
* `domingo`. Indica la clave de exportación correspondiente a los domingo. Mín. 0, máx. 1\. Es de tipo [String](index.html#string).

Aparece en:

* `[<otros>](#otros)` .

DuracionesType
--------------

Define la proporción de un tramo con respecto a los demás.

Puede tener uno de los valores:

* `M`. Media duración.
* `1`. Duración completa.
* `T`. Duración de tres cuartos.
* `S`. Duración de seis cuartos (una y media).
* `2`. Duración doble.
* `3`. Duración triple.
* `4`. Duración cuadruple.
* `5`. Duración quintuple.
* `6`. Duración sextuple.
* `7`. Duración sextuple.

Aparece en:

* [`<numSesiones>`](#distribucionVariable).
* [`<numMaximoDeSesiones>`](#distribucionVariable).
* [`<numMinimoDeSesiones>`](#distribucionVariable).
* [distribucionVariable](#distribucionVariable).

DuracionesDistFijaType
----------------------

Define la proporción de un tramo con respecto a los demás.

Puede tener uno de los valores:

* `M`. Media duración.
* `1`. Duración completa.
* `T`. Duración de tres cuartos.
* `S`. Duración de seis cuartos (una y media).
* `2`. Duración doble.
* `3`. Duración triple.
* `4`. Duración cuadruple.
* `5`. Duración quintuple.

Aparece en:

* [`<numSesiones>`](#distribuicionFija).
* [distribucionFija](#distribucionFija).

DuracionesTramoType
-------------------

Define las proporciones de un tramo restringiendo el tipo [DuracionesType](#duracionesType).

Puede tener uno de los valores:

* `M`. Media duración.
* `1`. Duración completa.
* `T`. Duración de tres cuartos.

Aparece en:

* [`<duracion>`](#DefinicionDeTramo).
* [Definicion de tramo](#DefinicionDeTramo).

PreferenciaMismaPosicionDistintosPeriodos
-----------------------------------------

Define la preferencia que se observa sobre colocar las entidades de una sesión que ocupa varios periodos en las mismas posiciones.

Aparece en:

* [`<OpcionesDeSesionType>`](#OpcionesDeSesionType).

GruposIncluidosType
-------------------

Indica la lista de grupos reales que forman parte de un grupo ficticio/circunstancial formado para que unos determiandos alumnos de los grupos que lo forman se agrupen para recibir una determinada materia o materias.

Contiene una lista de elementos tipo:

* `grupoIncluido`. Es de tipo [NombreType](index.html#NombreType). Indica el nombre identificativo de un grupo del horario.

Aparece en:

* [`<grupo>`](#grupo).

____
