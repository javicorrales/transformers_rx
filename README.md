# Trabajo final de master Ciencia de Datos, Universitat Oberta de Catalunya (UOC) #
**Clasificación de imágenes radiológicas aplicando modelos Transformers**
** Autor: Francisco Javier Corrales Estrella**
**Tutor: Carlos Luis Sanchez Bocanegra**

La detección temprana de enfermedades mediante el estudio de imágenes es clave para aumentar la esperanza de vida del paciente. Existen diferentes tipos de pruebas como radiografías, tomografía, resonancias magnéticas, mamografía, ecografía.
La aplicación de técnicas de IA es una nueva forma de abordar este problema y que permite a los radiologos detectar enfermedades.
Mediante el presente trabajo se pretente hacer una revisión del estado del arte de las  redes neuronales basadas en  Transformers para el diagostico por imágenes y realizar una aplicación práctica sobre un conjunto de imágenes para evaluar sus resultados.
Se ha seleccionado como dataset de pruebas el CBIS-DDSM, (Subconjunto curado de imágenes mamarias de DDSM), que incluye imágenes descomprimidas, seleccionadas y curadas de mamografías. El CBIS-DDSM (Subconjunto curado de imágenes mamarias de DDSM) es una versión actualizada y estandarizada de la base de datos digital para mamografías de detección (DDSM). El DDSM es una base de datos de 2620 estudios de mamografía de película escaneada. Contiene casos normales, benignos y malignos con información patológica verificada. El conjunto de datos proporciona un tamaño de conjunto de datos capaz de analizar los sistemas de apoyo a la toma de decisiones en mamografía.
Otros de los motivos que nos han ayudado a seleccionar este conjunto de datos como veremos mas adelante es que ya vienen etiquetados los subconjuntos de entrenamiento y test balanceados correctamente en función de la dificultad del diagnóstico


Para el entorno de trabajo al no disponer de GPU en el equipo doméstico, se ha trabajado con Google Colab ya que es un entorno que dispone de GPU, no necesita ningún tipo de instalación y existen librerias compatibles con Drive, esto último es importante, pues nos ha permitido descargar el juego de pruebas una sola vez y dejarlo preparado en nuestro drive, por lo que en sucesivas ejecuciones solo teníamos que montar drive como una unidad de trabajo y ya tenemos acceso.
El trabajo se ha estructurado todo en dos notebook:
  * LecturaCBIS_DDSM: Se descarga el juego de datos de kaagle, se hacen las tareas propias de limpieza y analisis, y por ultimo se implementa una sencilla red convulocional para explorar unos resultados iniciales.
  * ViT: Se implementa un modelo basado en la arquitectura ViT (Vision transformers).
