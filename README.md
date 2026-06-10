# Análisis ConnectaTel - Proyecto final Sprint 7

### Objetivo
Explorar, limpiar y analizar datos de usuarios y su comportamiento de uso para responder preguntas de negocio clave

### Datasets
1. plans.csv: Catálogo de planes con sus precios y beneficios. 
2. users_latam.csv: Información de cada usuario: datos personales, plan, fecha de registro (4,000 registros).
3. usage.csv: Actividad generada por los usuarios: llamadas, mensajes, duración, longitud (40,000 registros).

### Etapas del Análisis
1. Carga y exploración inicial — revisión de estructura, tipos de datos y primeras estadísticas descriptivas.
2. Limpieza de datos:
  - Corrección de valores sentinel ("?" en city, -999 en age)
  - Tratamiento de nulos y fechas inválidas (reg_date con año > 2024)
  - Identificación de nulos estructurales MAR en duration y length
  3. Feature engineering — creación de columnas auxiliares (is_call, is_text) y tabla agregada por usuario (usage_agg)
  4. Visualización de distribución y detección de outliers: distribuciones de edad, mensajes, llamadas y minutos por plan, metodo IQR sobre variables numéricas clave
  5. Segmentación: creación de gripos por edad y nivel de uso
  6. Análisis ejecutivo: insights y recomendaciones de negocio

### Cómo ejecutar el notebook
En Google Colab (recomendado)
1. Abre Google Colab
2. Ve a Archivo → Subir notebook y selecciona el archivo .ipynb
3. Sube los datasets users.csv y usage.csv desde el panel lateral izquierdo (ícono de carpeta)
4. Ejecuta todas las celdas (Run all)

### Guía de reproducción
Para reproducir el análisis desde cero:
1. Tener los archivos plans.csv, users.csv y usage.csv en la misma carpeta que el notebook.
2. Ejecutar las celdas en orden secuencial.
3. El notebook genera automáticamente el dataframe final user_profile, que consolida usuarios con sus métricas de uso agregadas.
 
