<div align="center">
    <h1>Curso de Matemáticas para Data Science: Estadística Descriptiva</h1>
    <img src="https://imgur.com/ogFpzj7.png" width="">
</div>

### Indice
- [¿Para qué sirve la estadística descriptiva?](#para-qué-sirve-la-estadística-descriptiva)
  - [Estadística descriptiva vs. inferencial](#estadística-descriptiva-vs-inferencial)
  - [Flujo de trabajo en data science](#flujo-de-trabajo-en-data-science)
  - [Plan del curso](#plan-del-curso)
- [Estadística descriptiva para analítica](#estadística-descriptiva-para-analítica)
  - [¿Cómo usar Deepnote?](#cómo-usar-deepnote)
  - [Tipos de datos](#tipos-de-datos)
  - [Medidas de tendencia central](#medidas-de-tendencia-central)
  - [Metáfora de Bill Gates en un bar](#metáfora-de-bill-gates-en-un-bar)
  - [Medidas de tendencia central en Python](#medidas-de-tendencia-central-en-python)
  - [Medidas de dispersion](#medidas-de-dispersion)
  - [Desviación estándar](#desviación-estándar)
  - [Medidas de dispersión en Python](#medidas-de-dispersión-en-python)
  - [Exploración visual de los datos](#exploración-visual-de-los-datos)
  - [Diagramas de dispersión en el análisis de datos](#diagramas-de-dispersión-en-el-análisis-de-datos)
- [Estadística en la ingesta de datos](#estadística-en-la-ingesta-de-datos)
  - [Pipelines de procesamiento para variables numéricas](#pipelines-de-procesamiento-para-variables-numéricas)
  - [Transformación no lineal](#transformación-no-lineal)
  - [Procesamiento de datos numéricos en Python](#procesamiento-de-datos-numéricos-en-python)
  - [Pipelines de procesamiento para variables categóricas](#pipelines-de-procesamiento-para-variables-categóricas)
  - [Procesamiento para variables categóricas con Python](#procesamiento-para-variables-categóricas-con-python)
  - [Correlaciones](#correlaciones)
  - [Matriz de covarianza](#matriz-de-covarianza)
- [Proyecto de aplicación](#proyecto-de-aplicación)
  - [Cálculo de valores propios de una matriz](#cálculo-de-valores-propios-de-una-matriz)
  - [PCA: análisis de componentes principales](#pca-análisis-de-componentes-principales)
  - [Reducción de dimensionalidad con PCA](#reducción-de-dimensionalidad-con-pca)

# ¿Para qué sirve la estadística descriptiva?
## Estadística descriptiva vs. inferencial

Es importante entender la diferencia entre las dos principales ramas de la estadística en el area de las matemáticas:

- **Estadística descriptiva**: Se trata de resumir información de manera cuantitativa para entender de forma sencilla y concreta sobre algún determinado asunto
- **Estadística inferencia**: Se basa en realizar inferencias, deducir que podría pasar en el futuro en base a lo datos que tenemos acceso en la actualidad

**¿Puede mentir la estadística?**

La estadística descriptiva tiene un problema al momento de definir que métrica es la que nos va a brindar la mayor relevancia para nuestro estudio.

El resultado podría estar sesgado a nuestro criterio personal, mostrando mayor interés a un cierto parámetro. dejando de lado a otro que también podría ser relevante. Mostramos solo una cara de la moneda.

No existen definiciones objetivas en estadística, sin embargo sobre estas definiciones podemos realizar cálculos exactos lo cual es un problema.

Los diferentes estadísticos descriptivos dan nociones diferentes sobre los mismos datos.

**¿Por que aprender estadística?**

A pesar de los problemas que pueda presentar es muy importante entender que la estadística nos puede ayudar a:

- Resumir grandes cantidades de información
- Tomar mejores decisiones
- Responder preguntas con relevancia social
- Reconocer patrones en los datos
- Descubrir a quien usan estas herramientas con fines nefastos

## Flujo de trabajo en data science

El flujo de trabajo del data science esta compuesto de:

![flujo de trabajo del data science](https://imgur.com/mm9IwOE.png)

Puede existir profesiones que se enfoquen mas a cada una de fases, no existe un perfil de data science que se encargue a todo el flujo de trabajo.

**¿En que partes del flujo de trabajo se necesita de estadística?**

![flujo de trabajo se necesita de estadística](https://imgur.com/2GbFVqk.png)

Todos las partes del flujo requiere del conocimiento en ciertas ramas de la estadística. La estadística descriptiva se va a emplear más en los dos primeros bloques de trabajo.

- **Ingesta de datos y Validación**: Se encarga de todo el procesamiento de ETL (Extract Transform Load), obtener los datos, limpiarlos y estructurarlos, crear pipelines de análisis automatizado, es decir que transformaciones vamos a realizar a los datos para que estén listos para el caso especifico de estudio que vamos a realizar.

- **Preparación y entrenamiento del modelo**: En este bloque se va a realizar un análisis exploratorio de los datos con estadística descriptiva, entender correlaciones y realizar posibles reducciones de datos.

- **Evaluar el modelo, Producción e Interacción**: esta parte del flujo se basa mas en la estadística inferencial.

## Plan del curso

**¿Cuál es diferenciador de este curso?**

Sabemos y tenemos bien claro que la estadística descriptiva es súper común, pero el diferenciador más grande de este curso es que estamos contextualizando la estadística descriptiva específicamente para Ciencia de Datos. No solo vamos a entender las fórmulas matemáticas si no el contexto de la estadística para descubrir todas las caras que tiene.

![estadisticas descriptivas - curso](https://imgur.com/IkXg9UC.png)

¿Cuáles serán los puntos específicos que vamos a tratar en este curso?

1. **Estadisticos para ingesta y procesamiento**:

- Conocer los tipos de datos o variables: si son numéricos, cadenas de texto, estructurado, etc.
- Definir el pipeline o flujo de procesamiento (cambio de formato, normalización, escalamiento), o sea lo que haremos con los datos para que estos sean utiles.

2. **Estadísticos para analítica y exploración**:

- Análisis exploratorio de los datos o EDA
- Identificar correlaciones de los datos y con ello poder reducir el conjunto de datos que necesitamos para un modelo.

# Estadística descriptiva para analítica

## ¿Cómo usar Deepnote?

[La mejor herramienta para Data Science: Deepnote - Blog Platzi
](https://platzi.com/blog/deepnote/)

## Tipos de datos
## Medidas de tendencia central
## Metáfora de Bill Gates en un bar
## Medidas de tendencia central en Python
## Medidas de dispersion
## Desviación estándar
## Medidas de dispersión en Python
## Exploración visual de los datos
## Diagramas de dispersión en el análisis de datos

# Estadística en la ingesta de datos

## Pipelines de procesamiento para variables numéricas
## Transformación no lineal
## Procesamiento de datos numéricos en Python
## Pipelines de procesamiento para variables categóricas
## Procesamiento para variables categóricas con Python
## Correlaciones
## Matriz de covarianza

# Proyecto de aplicación

## Cálculo de valores propios de una matriz
## PCA: análisis de componentes principales
## Reducción de dimensionalidad con PCA
