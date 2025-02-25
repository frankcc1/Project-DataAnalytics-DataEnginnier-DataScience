# Project-DataAnalytics-DataEnginnier-DataScience

# Proyecto de ingeniería de datos en Azure + Clustering

Este proyecto es una solución de canalización de ingeniería de datos para un problema empresarial inventado, creado para ayudarme en mi aprendizaje en la comprensión de la canalización de datos y segmentación de Clientes.

Descripción general del proyecto
Este proyecto aborda una necesidad empresarial crítica mediante la creación de una canalización de datos integral en Azure. El objetivo es extraer datos de clientes, ventas, productos y sucursales de una base de datos SQL local, transformarlos en la nube y aplicar técnicas de Machine Learning en la agrupación de clientes para generar información procesable a través de un panel de Power BI. El panel resaltará los indicadores clave de rendimiento (KPI) relacionados con las ventas por categoría de producto, las ventas de carácter mensual, anual, entre otras métricas, lo que permitirá a las partes interesadas filtrar y analizar los datos por fecha, categoría de producto y Sucursal.

Requisitos empresariales
La empresa ha identificado una brecha en comprender más a sus clientes (específicamente por la frecuencia y recencia en las compras). Los requisitos clave incluyen:

✓ Ventas por sucursal y categoría de producto: un panel que muestre el total de productos vendidos, los ingresos totales por ventas y una división por sucursal entre los clientes.

✓ Filtrado de datos: capacidad para filtrar los datos por categoría de producto, sucursal y fecha.

✓ Interfaz fácil de usar: las partes interesadas deben tener acceso a una interfaz fácil de usar para realizar consultas.

Descripción general de la solución
Para cumplir con estos requisitos, la solución se divide en los siguientes componentes:

Ingestión de datos:

✓ Extraiga datos de clientes, ventas, Productos, Categorías y Sucursales de una base de datos SQL local.

✓ Cargue los datos en Azure Data Lake Storage (ADLS) mediante Azure Data Factory (ADF).

Transformación de datos:

✓ Use Azure Databricks para limpiar y transformar los datos.

✓ Organice los datos en capas Bronze y Silver para datos sin procesar y limpios respectivamente.

Carga de datos e informes:

✓ Cargue los datos transformados en Azure Synapse Analytics.

✓ Cree un panel de Power BI para visualizar los datos, lo que permite a las partes interesadas explorar las ventas y los conocimientos demográficos.

Automatización:

✓ Programe la canalización para que se ejecute diariamente, lo que garantiza que los datos y los informes estén siempre actualizados.

Pila de tecnología
Azure Data Factory (ADF): para orquestar el movimiento y la transformación de datos.
Azure Data Lake Storage (ADLS): para almacenar datos procesados ​​y sin procesar.
Azure Databricks: para la transformación y el procesamiento de datos.
Azure Synapse Analytics: para el almacenamiento de datos y el análisis basado en SQL.
Power BI: para la visualización y la generación de informes de datos.
Azure Key Vault: para administrar de forma segura credenciales y secretos.
SQL Server (local): origen de los datos de ventas, clientes, productos y Sucursales.
Instrucciones de configuración
Requisitos previos

✓ Una cuenta de Azure con créditos suficientes.

✓ Acceso a una base de datos local de SQL Server.

Paso 1: Configuración del entorno de Azure

✓ Crear un grupo de recursos: configure un nuevo grupo de recursos en Azure.

✓ Aprovisionar servicios:

Cree una instancia de Azure Data Factory.
Configure Azure Data Lake Storage con contenedores Bronze, Silver y Gold.
Configure un área de trabajo de Azure Databricks y un área de trabajo de Synapse Analytics.
Configure Azure Key Vault para la administración de secretos.
Paso 2: Ingesta de datos

✓ Configurar SQL Server: instale SQL Server y SQL Server Management Studio (SSMS). Restaurar la base de datos que compartiré.

✓ Ingerir datos con ADF: crear canalizaciones en ADF para copiar datos de SQL Server a la capa de bronce en ADLS.

Paso 3: Transformación de datos

✓ Montar Data Lake en Databricks: configurar Databricks para acceder a ADLS.

✓ Transformar datos: utilizar los cuadernos de Databricks para limpiar y agregar los datos moviéndolos de bronce a plata. En este caso no fue necesario el contenedor Gold.

✓ Clustering: extraer data del contenedor silver (plata) para el respectivo análisis (Está en mi repositorio).

Paso 4: Carga de datos e informes

✓ Cargar datos en Synapse: configurar un grupo de SQL de Synapse y cargar los datos de oro para su análisis.

✓ Crear un panel de Power BI: conectar Power BI a Synapse y crear visualizaciones basadas en los requisitos comerciales.

Paso 5: Automatización y supervisión

✓ Programar canalizaciones: utilizar ADF para programar las canalizaciones de datos para que se ejecuten a diario.

✓ Supervisar las ejecuciones de canalizaciones: utilizar las herramientas de supervisión en ADF y Synapse para garantizar la ejecución correcta de las canalizaciones.

Paso 6: Seguridad y gobernanza

✓ Administrar el acceso: configure el control de acceso basado en roles (RBAC) mediante Azure Entra ID.

Paso 7: Prueba

✓ Activar y probar canales: inserte nuevos registros en la base de datos SQL y verifique que todo el canal se ejecute correctamente, actualizando el panel de Power BI.

Conclusión
Este proyecto proporciona una solución integral sólida para comprender la demografía de los clientes y su impacto en las ventas. El canal de datos automatizado garantiza que las partes interesadas siempre tengan acceso a la información más actualizada y procesable.
