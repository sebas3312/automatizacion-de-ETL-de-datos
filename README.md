# Automatización de Procesos de Extracción, Transformación y Carga (ETL) de Datos

Este proyecto utiliza Apache Airflow para automatizar los procesos de extracción, transformación y carga (ETL) de datos.

## Requisitos

- Python 3.7 o superior
- Apache Airflow 2.0 o superior

## Instalación y Configuración

1. **Instalar Apache Airflow**:
   - Utiliza pip para instalar Airflow:
     ```
     pip install apache-airflow
     ```
   - Asegúrate de instalar la versión adecuada de Airflow compatible con tu entorno y versión de Python.

2. **Inicializar la base de datos de Airflow**:
   - Crea el directorio de trabajo de Airflow:
     ```
     airflow db init
     ```

3. **Crear un usuario Airflow**:
   - Crea un usuario Airflow para acceder a la interfaz web:
     ```
     airflow users create --username admin --password admin --firstname Admin --lastname User --role Admin --email admin@example.com
     ```

4. **Configurar variables de entorno de Airflow**:
   - Establece las variables de entorno de Airflow:
     ```
     export AIRFLOW_HOME=~/airflow
     export AIRFLOW__CORE__DAGS_FOLDER=~/airflow/dags
     export AIRFLOW__CORE__EXECUTOR=LocalExecutor
     ```
   - Reemplaza `~/airflow` con la ruta donde quieres que se cree el directorio de Airflow.

5. **Iniciar el servidor web de Airflow**:
   - Inicia el servidor web de Airflow:
     ```
     airflow webserver --port 8080
     ```

6. **Iniciar el scheduler de Airflow**:
   - En otra terminal, inicia el scheduler de Airflow:
     ```
     airflow scheduler
     ```

## Uso

1. Guarda el código del proyecto de ETL en el directorio de DAGs de Airflow (`~/airflow/dags`).
2. Verifica la ejecución del DAG en la interfaz web de Airflow (generalmente en `http://localhost:8080`).
3. Ejecuta manualmente el DAG para probar su funcionamiento.
4. Monitorea la ejecución del DAG y verifica que los datos se carguen correctamente en la base de datos.
5. Programa la ejecución automática del DAG según tus necesidades.
6. Monitorea y optimiza el proceso de ETL según sea necesario.

¡Disfruta de la automatización de tus procesos de ETL con Apache Airflow!
