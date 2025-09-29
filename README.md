Dashboard y analisis de datos excel

Se ha buscado una tabla de datos en bruto y se ha obtenido el archivo salariestrabajosAI.csv obtenido en el enclace web https://www.kaggle.com/datasets/adilshamim8/salaries-for-data-science-jobs.

La descripción de los datos es:
Este conjunto de datos captura datos salariales reales para puestos en ciencia de datos, inteligencia artificial y aprendizaje automático entre 2020 y 2025. Cada fila representa un salario reportado, enriquecido con atributos como el puesto, el nivel de experiencia, el tamaño de la empresa, la tasa de teletrabajo y el contexto geográfico. 

1º importar CSV a Excel
2º análisis previo de los datos
Se trata de un conjunto de datos que recoge el salario de trabajadores de distintos paises y posiciones, todas ellas relacionadas con analisiis y procesamiento de datos e inteligencia artifical. Contiene inicialmente 10 columnas con 141.566.
En primer lugar, la primera columna señala el año del dato de salario
En la segunda columna se recogen diferentes niveles de experiencia (SE: Senior, EX:experto, MI:medio, EN:principiante)
Se recogen a su vez tipos de contratos (CT:por contrato  , FT: tiempo completo, PT:jornada parcial, y FL:tiempo completo) .Se ve que hay dos clasificaciones para considerar tiempo completo, que se trataran más adelante.
En la cuarta columna, se consideran los títulos de los empleos, se recogen 410 tipos diferentes (conociendo el trabajo que realizan, es posible que se pudieran unificar diferentes categorías)
La quinta y la sexta columna muestran el salario anual y la moneda en la que se paga respectivamente, siendo la septima y la octava columna una transformación del salario a dolares estadounidenses
LA novena columna indica si el trabajo es presencial (0%), mixto (50%) y remoto(100%)
La décima columna indica el lugar donde esta localizada la empresa 
La undécima hace distinción del tamaño de la empresa (S: pequeña, M: Mediana, L: Grande) 
3ºAnalisis de duplicados:
Como no hay un identificador único para cada entrada de datos, se decide comprobar que datos son excatamente iguales en cada una de las filas. Se decide hacer mediante una concatenación de todas las columnas, nos econtramos 73.678 entradas duplicadas de 141.566. Esto nos hace pensar que al no haber un identificador unico como un nombre o un id de empleado, en los diferentes paises pueden existir varias posiciones iguales con el mismo salario. Podría ser, que una compañía tenga varias personas con el mismo puesto de trabajo y el mismo salario y categoría. 
Se decide que la muestra de duplicados es demasiado grande para ignorarla por lo que desecha esta opción tomando como hipotesis lo comentado en el anterior parrafo.
4ºRealización del Dashboard
Se quiere analizar los datos comparando el numero de empleos y la masa salarial movida por los mismos en los años en los que hay registros.
Asi pues se introducen big numbers con el numero total del empleos, Masa salarial y promedio salarial. Se decide añadir el promedio salarial por nivel de experiencia ya que la diferencia es significativa.
Se añaden tres gráficos al Dashboard
1.	Muestra el numero de empleos en los años contemplados
2.	Muestra la distribución en los diferentes paises (los 10 con más empleos)
3.	Muestra el procentaje de presencialidad 

Se añaden dos tablas que muestran los 5 mejores empleos:
1.	Encuanto a numero de empleos existentes
2.	En cuanto a mejor pagados
Se añaden 3 segmentadores de datos que aplican a todos los datos mostrados en el dashboard, para que el usuario pueda filtras según el año del dato (2020-2025), el tamaño de la empresa(S, M,L), y el tipo de contrato que tenga el empleado(FT completo, CT contrato por tiempo fijo, PT parcial)
