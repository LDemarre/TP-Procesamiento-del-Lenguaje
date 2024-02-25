# Trabajo Práctico - Procesamiento del Lenguaje Natural
### Integrante: Lucas Demarré
### Año: 2024

## **IMPORTANTE**
Para poder ejecutar correctamente este archivo es necesario que en la sección *3. Variables Globales* se complete de forma correcta la variable **API_KEY** con su KEY para acceder a la api de **HuggingFace**. En caso de no hacerlo, no se podrá acceder al LLM para crear la respuesta a las consultas hechas por el usuario. 

## **Instrucciones para la Ejecución del Trabajo Práctico**
Este repositorio alberga una estructura organizada en una carpeta principal que contiene tres subcarpetas. Cada subcarpeta almacena datos específicos destinados a la creación de distintas bases de datos, identificadas claramente por el nombre de cada una. Por ejemplo, la subcarpeta **graphDB** incluye los PDF utilizados para generar la **Base de Datos de Grafos**.

Además, se encuentra el archivo principal **Trabajo Práctico - Procesamiento del Lenguaje Natural.ipynb**, que está diseñado para la construcción del **Chatbot**. Es relevante mencionar que si ya se dispone de los documentos PDF que acompañan al proyecto, no es necesario ejecutar la sección *5. Creación de Fuentes de Información*. En su lugar, se puede continuar directamente con la sección 6.

## **Archivos Adicionales**
* *requirements.txt*: Este archivo de texto facilita la instalación de las librerías requeridas, asegurando las versiones adecuadas para el óptimo funcionamiento del Trabajo Práctico.

## Identificación y Solución de Errores Comunes
Durante la primera ejecución del programa, es posible encontrar algunos errores específicos:

### *Base de datos Chroma*
Al intentar crear la base de datos Chroma en la sección *7.2. Conversión a Embeddings y Almacenamiento en Chroma*, puede surgir el siguiente mensaje de error: 

`ValueError: Trying to load a model of incompatible/unknown type. 'RUTA-A-CARPETA' contains neither 'saved_model.pb' nor 'saved_model.pbtxt'.`

Para solucionar este inconveniente, se recomienda descargar directamente el modelo **Universal-Sentence-Encoder** desde esta página: [Descargar modelo](https://www.kaggle.com/models/google/universal-sentence-encoder/frameworks/tensorFlow2/variations/multilingual-large/versions/2?tfhub-redirect=true). Debe seleccionarse la variante **multilingual-large**, **Versión 2**, y proceder con la descarga utilizando el botón ubicado junto a *+ New Notebook*. Tras descomprimir el archivo: **archive.tar.gz** y colocar su contenido en la ruta indicada por el error, el proceso de creación de la base de datos Chroma debería completarse sin problemas.