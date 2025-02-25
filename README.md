
# 🚀 Proyecto de Ingeniería de Datos en Azure + Clustering  

Este proyecto es una solución de canalización de ingeniería de datos para un problema empresarial inventado, creado para ayudarme en mi aprendizaje en la comprensión de la canalización de datos y segmentación de clientes.  

![image alt](https://github.com/frankcc1/Project-DataAnalytics-DataEnginnier-DataScience/blob/b0fff8bced6d17f41c7f2a99861fda100be9becc/Databricks/image.png)
![image alt](https://github.com/frankcc1/Project-DataAnalytics-DataEnginnier-DataScience/blob/8d917dde94ea2d057254f4dcad9dcf34f94ed846/Databricks/image.png)

## 📌 **Descripción general del proyecto**  
Este proyecto aborda una necesidad empresarial crítica mediante la creación de una canalización de datos integral en Azure. El objetivo es extraer datos de clientes, ventas, productos y sucursales de una base de datos SQL local, transformarlos en la nube y aplicar técnicas de Machine Learning en la agrupación de clientes para generar información procesable a través de un panel de Power BI.  

El panel resaltará los indicadores clave de rendimiento (KPI) relacionados con:  
- Ventas por categoría de producto  
- Ventas de carácter mensual y anual  
- Filtros por fecha, categoría de producto y sucursal  

## 🎯 **Requisitos empresariales**  
La empresa ha identificado una brecha en comprender más a sus clientes (específicamente por la frecuencia y recencia en las compras). Los requisitos clave incluyen:  

✔️ **Ventas por sucursal y categoría de producto**: un panel que muestre el total de productos vendidos, los ingresos totales por ventas y una división por sucursal entre los clientes.  

✔️ **Filtrado de datos**: capacidad para filtrar los datos por categoría de producto, sucursal y fecha.  

✔️ **Interfaz fácil de usar**: las partes interesadas deben tener acceso a una interfaz intuitiva para realizar consultas.  

## ⚙️ **Descripción general de la solución**  
Para cumplir con estos requisitos, la solución se divide en los siguientes componentes:  

### 🔄 **Ingestión de datos**  
✔️ Extraer datos de clientes, ventas, productos, categorías y sucursales de una base de datos SQL local.  
✔️ Cargar los datos en **Azure Data Lake Storage (ADLS)** mediante **Azure Data Factory (ADF)**.  

### 🔍 **Transformación de datos**  
✔️ Usar **Azure Databricks** para limpiar y transformar los datos.  
✔️ Organizar los datos en capas **Bronze y Silver** para datos sin procesar y limpios, respectivamente.  

### 📊 **Carga de datos e informes**  
✔️ Cargar los datos transformados en **Azure Synapse Analytics**.  
✔️ Crear un **panel de Power BI** para visualizar los datos, permitiendo a las partes interesadas explorar las ventas y los insights demográficos.  

### ⏳ **Automatización**  
✔️ Programar la canalización para que se ejecute **diariamente**, garantizando que los datos y los informes estén siempre actualizados.  

## 🛠️ **Pila de tecnología**  
- **Azure Data Factory (ADF)**: Orquestación del movimiento y transformación de datos.  
- **Azure Data Lake Storage (ADLS)**: Almacenamiento de datos procesados y sin procesar.  
- **Azure Databricks**: Transformación y procesamiento de datos.  
- **Azure Synapse Analytics**: Almacenamiento de datos y análisis basado en SQL.  
- **Power BI**: Visualización y generación de informes.  
- **Azure Key Vault**: Gestión segura de credenciales y secretos.  
- **SQL Server (local)**: Fuente de los datos de ventas, clientes, productos y sucursales.  

## 🏗️ **Instrucciones de configuración**  

### 🔧 **Requisitos previos**  
✔️ Una cuenta de Azure con créditos suficientes.  
✔️ Acceso a una base de datos local de **SQL Server**.  

### 🚀 **Paso 1: Configuración del entorno de Azure**  
✔️ **Crear un grupo de recursos**: Configurar un nuevo grupo de recursos en Azure.  
✔️ **Aprovisionar servicios**:  
   - Crear una instancia de **Azure Data Factory**.  
   - Configurar **Azure Data Lake Storage** con contenedores Bronze, Silver y Gold.  
   - Configurar un área de trabajo de **Azure Databricks** y un área de trabajo de **Synapse Analytics**.  
   - Configurar **Azure Key Vault** para la administración de secretos.  

### 📥 **Paso 2: Ingesta de datos**  
✔️ **Configurar SQL Server**: Instalar **SQL Server** y **SQL Server Management Studio (SSMS)**. Restaurar la base de datos compartida.  
✔️ **Ingerir datos con ADF**: Crear canalizaciones en **ADF** para copiar datos de **SQL Server** a la capa de **bronce** en **ADLS**.  

### 🔄 **Paso 3: Transformación de datos**  
✔️ **Montar Data Lake en Databricks**: Configurar **Databricks** para acceder a **ADLS**.  
✔️ **Transformar datos**:  
   - Utilizar los cuadernos de **Databricks** para limpiar y agregar los datos, moviéndolos de **Bronze a Silver**.  
   - **Clustering**: Extraer data del contenedor **Silver** para el análisis correspondiente. *(Repositorio disponible)*.  

### 📤 **Paso 4: Carga de datos e informes**  
✔️ **Cargar datos en Synapse**: Configurar un grupo de SQL en **Synapse** y cargar los datos para su análisis.  
✔️ **Crear un panel de Power BI**: Conectar **Power BI** a **Synapse** y generar visualizaciones basadas en los requisitos comerciales.  

### ⏳ **Paso 5: Automatización y supervisión**  
✔️ **Programar canalizaciones**: Usar **ADF** para programar las canalizaciones de datos de ejecución diaria.  
✔️ **Supervisar ejecuciones**: Utilizar herramientas de monitoreo en **ADF** y **Synapse** para garantizar la correcta ejecución de las canalizaciones.  

### 🔒 **Paso 6: Seguridad y gobernanza**  
✔️ **Administrar el acceso**: Configurar el **Control de Acceso Basado en Roles (RBAC)** mediante **Azure Entra ID**.  

### ✅ **Paso 7: Prueba**  
✔️ **Activar y probar canales**: Insertar nuevos registros en la base de datos SQL y verificar que el canal se ejecute correctamente, reflejando los cambios en el **panel de Power BI**.  

## 🎯 **Conclusión**  
Este proyecto proporciona una **solución integral** para comprender la **demografía de los clientes** y su impacto en las ventas. La automatización garantiza que las partes interesadas siempre tengan acceso a **datos actualizados** y procesables.
