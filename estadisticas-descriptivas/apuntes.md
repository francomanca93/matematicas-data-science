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
    - [Datos categóricos](#datos-categóricos)
    - [Datos numéricos](#datos-numéricos)
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

Notebook de la clase: [[clase-04]tipos-de-datos](clases_notebooks/[clase-04]tipos-de-datos.ipynb)

### Datos categóricos

Los datos categóricos también conocidos como datos cualitativos, representan características como el género, el idioma, etc. de una persona o caracteristicas de un objeto. También pueden tomar valores numéricos, por ejemplo: 1 para mujeres y 0 para hombres. Hay que tener en cuenta que esos números no tienen significado matemático.

Los tipos de datos estadísticos categóricos se clasifican en:

- **Datos nominales**: Otros de los tipos de datos estadísticos son los que tienen valores nominales que representan unidades discretas y se usan para etiquetar variables que no tienen un valor cuantitativo.
Estos datos no tienen un orden, aunque cambiara el orden de sus valores, no cambia su significado. Ejemplo: Tenemos 3 clases de coches y cada uno lo podemos representar con un numero `--> - 1: Subaru - 2:Ford - 3: Tesla` y da lo mismo el orden de estos, no importará si sabemos que significa cada numero.
- **Datos ordinales**: Los datos ordinales representan unidades discretas y ordenadas. Por lo tanto, es casi lo mismo que los datos nominales, excepto que su orden es importante.
Las escalas ordinales generalmente, se usan para medir características no numéricas como la `felicidad, la satisfacción del cliente, etc.`

### Datos numéricos

Estos tipos de datos estadísticos también se conocen como datos cuantitativos, y se refieren a una medida o recuento. Se clasifican de la siguiente manera:

- **Datos discretos**: Los datos estadísticos son discretos cuando sus valores son distintos y separados. Es decir, cuando los datos sólo pueden tomar ciertos valores.
Este tipo de datos no se puede medir, pero se pueden contar. Básicamente representan información que se puede clasificar.
- **Datos continuos**: Los datos continuos representan mediciones y, por lo tanto, sus valores. no se pueden contar, pero se pueden medir. A su vez, estos se clasifican de la siguiente manera:
  - **Datos de intervalo**: Los datos de intervalo representan unidades ordenadas que tienen la misma diferencia . Por lo tanto, hablamos de datos de intervalo cuando tenemos una variable que contiene valores numéricos que están ordenados y donde conocemos las diferencias exactas entre los valores. El problema con los datos de valores de intervalo es que podemos sumar y restar, pero no podemos multiplicar, dividir o calcular razones. Debido a que no existe un cero verdadero, no se pueden aplicar muchas estadísticas descriptivas e inferenciales.
  - **Datos de relación**: También son unidades ordenadas que tienen la misma diferencia. Los datos de relación son los mismos que los valores de intervalo, con la diferencia de que tienen un cero absoluto.


> En **pandas** cuando analizamos las variables nos encontramos los datos pueden tener un tipo segun el tipo de dato estadistico:
> * Categoricos: `object`, `bool`
> * Numéricos: `int64` (discreto), `float64` (contínuo)


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
