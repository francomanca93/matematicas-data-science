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
    - [Distribución normal](#distribución-normal)
  - [Medidas de dispersión en Python](#medidas-de-dispersión-en-python)
    - [Asimetría en distribuciones](#asimetría-en-distribuciones)
  - [Exploración visual de los datos](#exploración-visual-de-los-datos)
  - [Diagramas de dispersión en el análisis de datos](#diagramas-de-dispersión-en-el-análisis-de-datos)
- [Estadística en la ingesta de datos](#estadística-en-la-ingesta-de-datos)
  - [Pipelines de procesamiento para variables numéricas](#pipelines-de-procesamiento-para-variables-numéricas)
    - [Escalamiento lineal (Normalización)](#escalamiento-lineal-normalización)
    - [Transformación no lineal](#transformación-no-lineal)
  - [Procesamiento de datos numéricos en Python](#procesamiento-de-datos-numéricos-en-python)
  - [Pipelines de procesamiento para variables categóricas](#pipelines-de-procesamiento-para-variables-categóricas)
  - [Procesamiento para variables categóricas con Python](#procesamiento-para-variables-categóricas-con-python)
  - [Correlaciones](#correlaciones)
  - [Matriz de covarianza](#matriz-de-covarianza)
- [Proyecto de aplicación](#proyecto-de-aplicación)
  - [Reducción de dimensionalidad con PCA (análisis de componentes principales)](#reducción-de-dimensionalidad-con-pca-análisis-de-componentes-principales)
  - [Conclusión](#conclusión)

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

Son medidas que nos ayudan a resumir una gran cantidad de información en un solo numero.

- **Media**: Es el promedio de todos los datos, puede ser susceptible a valores atípicos. La media a su vez puede ser:
  - **Media aritmética o promedio**: Es la suma de un conjunto de valores entre el número de observaciones.
  - **Media ponderada**: es una medida de tendencia central, *que es apropiada cuando en un conjunto de datos cada uno de ellos tiene una importancia relativa (o peso) respecto de los demás datos.* Se obtiene multiplicando cada uno de los datos por su ponderación (peso) para luego sumarlos, obteniendo así una suma ponderada; después se divide esta entre la suma de los pesos, dando como resultado la media ponderada.
  - **Media armónica**: La media armónica es igual al número de elementos de un grupo de cifras entre la suma de los inversos de cada una de estas cifras.
  En otras palabras, la media armónica es una medida estadística *recíproca a la media aritmética*.
  - **Media geométrica**: es una cantidad arbitraria de números (por decir n números) es la raíz n-ésima del producto de todos los números; *es recomendada para datos de progresión geométrica, para promediar razones, interés compuesto y números índice*.
- **Mediana**: es el dato central es decir tiene la misa cantidad de datos a su izquierda y derecha, no es lo mismo que la media.
- **Moda**: es el dato que mas se repite, la moda no aplica para datos numéricos continuos

**Diagrama de frecuencia**

Es la representación grafica asociada a la tabla de frecuencia, normalmente todos los estadísticos descriptivos discretos se pueden representar en términos de esta distribución.
Los pasos para obtener los valores son:

1. Seleccionar una columna con tipo de datos discretos.
2. Sacar la cantidad de veces que aparece cada valor, guardaremos este dato en una columna llamada **frecuencia**, ya que es la frecuencia con la que aparece cada dato.
3. Graficamos un diagrama de barras llamada diagrama de frecuencia donde `la altura de la barra es la frecuencia` y el `tipo de dato discreto es el label de cada columna`.

![diagrama-de-frecuencia](https://imgur.com/miKIn32.png)

## Metáfora de Bill Gates en un bar

**Calculo de la media aritmetica**
![media](https://imgur.com/DqXTMsn.png)

**Calculo de la mediana**

![mediana](https://imgur.com/3OmISxi.png)


Resumen de la metafora de BIll Gates:

Caso 1:
Tenemos 11 personas con un salario de 35k USD anuales, el promedio y la mediana seran iguales, de 35k USD.
![caso1](https://imgur.com/O5P3gnB.png)

Caso 2:
Si llega un caso atípico, ejemplo Bill Gates y se sienta con estas 11 personas, y su salario es por ejemplo de 1M USD anuales, la media se dispersa abruptamente y no nos representa a toda la población de estudio.
![caso2-media-atipica](https://imgur.com/IiNfZUK.png)

Por lo tanto deberemos tener en cuenta la mediana tambien cuando sepamos o sospechemos que tenemos valores atípicos y con ello poder comprar.
![caso2-mediana](https://imgur.com/NRVbcdv.png)

- Esta metáfora nos muestra que al tener valores atípicos nuestra media se vera sesgada o desviada.
- La mediana será un mejor valor para manejar un conjunto de datos con valores atípicos.
- Ejemplo: Por esto hablar del ingreso per cápita de un país es equivocado si no lo acompañamos con otros indices que nos midan la distribucion de la riqueza, como por ejemplo el indice de Gini o nos aportan el valor de la mediana para sacar nuestras conclusiones.

## Medidas de tendencia central en Python

Notebook ejercitando los conceptos medidas de tendencia central en Python --> [[clase-07]medidas-central](clases_notebooks/[clase-07]medidas-central.ipynb)

## Medidas de dispersion

Las medidas de dispersión, también llamadas medidas de variabilidad, muestran la variabilidad de una distribución, indicando por medio de un número, si las diferentes puntuaciones de una variable están muy alejadas de la media. Cuanto mayor sea ese valor, mayor será la variabilidad, cuanto menor sea, más homogénea será. Así se sabe si todos los casos son parecidos o varían mucho entre ellos.

- **Rango**: El Rango es el intervalo entre el valor máximo y el valor mínimo.
- **Cuartiles**: Los cuartiles son valores que dividen una muestra de datos en cuatro partes iguales.
  - **1er cuartil (Q1)**: 25% de los datos es menor que o igual a este valor.
  - **2do cuartil (Q2)**: La mediana. 50% de los datos es menor que o igual a este valor.
  - **3er cuartil (Q3)**: 75% de los datos es menor que o igual a este valor.
- **Rango intercuartil**: La distancia entre el primer 1er cuartil y el 3er cuartil (Q3-Q1); de esta manera, abarca el 50% central de los datos.

- [**Desviacion estandar**: Siguiente seccion](#desviación-estándar)

**Diagrama de caja o box plot**: representa gráficamente una serie de datos numéricos a través de sus cuartiles. De esta manera, el diagrama de caja muestra a simple vista la mediana y los cuartiles de los datos. También puede representar los valores atípicos de estos.

![representacion-rango-q](https://imgur.com/FmA5v7p.png)

## Desviación estándar

- **Desviación estándar**: es la medida de dispersión más común, que indica qué tan dispersos están los datos con respecto a la media. Mientras mayor sea la desviación estándar, mayor será la dispersión de los datos.
El símbolo **σ (sigma)** se utiliza frecuentemente para representar la desviación estándar de una **población**, mientras que **s** se utiliza para representar la desviación estándar de una **muestra**.
La desviación estándar se puede utilizar para establecer un valor de referencia para estimar la variación general de un proceso.

- **Varianza**: es una medida de dispersión que representa la variabilidad de una serie de datos respecto a su media. Formalmente se calcula como la suma de los residuos al cuadrado divididos entre el total de observaciones. Su fórmula es la siguiente:
X → Variable sobre la que se pretenden calcular la varianza
xi → Observación número i de la variable X. i puede tomará valores entre 1 y n.
n → Número de observaciones.
x̄ → Es la media de la variable X.

![std-var](https://imgur.com/LEmWuz3.png)

La diferencia entre la desviación estándar o típica y la varianza, es que la la desviación típica es la raíz cuadrada de la varianza

Coeficiente de variación:

Su cálculo se obtiene de dividir la desviación típica entre el valor absoluto de la media del conjunto y por lo general se expresa en porcentaje para su mejor comprensión.

X → Variable sobre la que se pretenden calcular la varianza
σx → Desviación típica de la variable X.
| x̄ | → Es la media de la variable X en valor absoluto con x̄ ≠ 0
El coeficiente de variación de utiliza para comparar la dispersión (variación) de conjuntos de datos de medidas diferentes o con medias aritméticas diferentes.

### Distribución normal

![dis-norm](https://imgur.com/stpXERG.png)

¿Qué implicaciones tiene la desviación estándar en una distribución de datos?

![dis-norm2](https://imgur.com/4cFWQ0w.png)

Normalmente en los extremos se ponen los valores mínimos y máximos, pero esto se puede ajustar para excluir a los datos atípicos (*outliers*).

Usando la **desviación estándar** se puede dividir a la distribución normal en varias partes.

A tres veces la \sigma a ambos lados de la media se concentra el 99.73% de los datos. Esto es relevante porque con base en eso podemos decir que a más de 3 veces \sigma se encontrarían los datos atípicos en el caso de la distribución normal.

Como se definen los outliers en términos del IQR:

- **Límite inferior:** ($\text{Q1} - 1.5 * \text{IQR}$)
- **Límite superior:** ($\text{Q3} + 1.5 * \text{IQR}$)

Cualquier dato menor que el límite inferior o mayor que el límite superior se considera un valor atípico. Esto se puede identificar usando un diagrama de caja y brazos con los límites definidos.

**Distribución sesgada**
![dis-sesgada](https://imgur.com/gnHpohG.png)

Se definen los límites de la siguiente manera:

- **Límite inferior: $Q_1-1.5*f(\text{IQR})$**
- **Límite superior: $Q_3+1.5*g(\text{IQR})$**

Donde $f$ y $g$ son una función cualquiera que dependa del rango intercuartil.

## Medidas de dispersión en Python

Notebook ejercitando los conceptos de medidas de dispersión en Python --> [[clase-10]medidas-dispersion](clases_notebooks/[clase-10]medidas-dispersion.ipynb)

### Asimetría en distribuciones

El hecho de que nuestra distribución tenga una tendencia a la derecha o a izquierda nos representa un problema, ya que no a acorde con una distribución y eso puede afectar a nuestros análisis si no tomamos en cuenta ese sesgo. No siempre hay que confiar en nuestra intuición o lo que vemos a simple vista, hay métodos como:

- Primer coeficiente de asimetría de Pearson (asimetría de modo)
- Segundo coeficiente de asimetría de Pearson (asimetría mediana)
- Coeficiente de Groeneveld y Meeden
- Coeficiente de Fisher
- Entre otros. Buscar en Google.

Y por último, no hay que olvidar la **curtosis**:
Una curtosis grande implica una mayor concentración de valores de la variable tanto muy cerca de la media de la distribución (pico) como muy lejos de ella (colas), al tiempo que existe una relativamente menor frecuencia de valores intermedios. Esto explica una forma de la distribución de frecuencias/probabilidad con colas más gruesas, con un centro más apuntado y una menor proporción de valores intermedios entre el pico y colas.
Una mayor curtosis no implica una mayor varianza, ni viceversa.

[Curtosis explicada en detalle](https://www.youtube.com/watch?v=gt6bpsGGp44)

## Exploración visual de los datos

La estadística descriptiva se divide en 2 bloques:
• **El analítico**: medidas de tendencia central y medidas de dispersión
• **La gráfica**: diagramas de caja, histogramas, entre otros

La gráfica, el tipo de visualización, a usar depende de la situación a describir ( pastel por ejemplo para para votaciónes, de dispersión para ver correlaciones, etc.)

La siguiente app web nos muestra los tipos de visualización y una explicación de ellos:

> EXCELENTE PÁGINA --> [DataVizProject](https://datavizproject.com/)

Entre graficas comunes tenemos:

- Pastel o donut
- Barras apiladas
- Radiales
- De dispersión

Hasta ahora hemos realizado análisis univariado: analizar la media, la mediana, etc. De una columna de un conjunto de datos. Hemos visto como se comporta una variable numérico respecto a una categórica.

En la siguiente seccion trabajaremos para observar como se comporta una variable numérica respecto a otra numerica por lo cual usaremos las gráficas de dispersión que ayudan a visualizar la correlación. Correlación es un concepto a usar con mucho cuidado.

## Diagramas de dispersión en el análisis de datos

Notebook realizando diagramas de dispersión para usos de análisis de datos en Python --> [[clase-12]Visualizaciones](clases_notebooks/[clase-12]Visualizaciones.ipynb)

# Estadística en la ingesta de datos

## Pipelines de procesamiento para variables numéricas

Llamamos pipeline a una secuencia de procesamiento de datos que permite optimizar mi flujo de trabajo. Estos son comunes en machine learning pues no solo permiten la manipulación y transformación de multiples datos, sino que además tenemos una alta reducción en código. Este consiste en encadenar una serie de estimadores, que me permiten ir trasformando un conjunto de datos en un proceso comprendido por varias etapas de manera secuencial, donde cada componente del pipeline toma los datos, los trasforma y su salida va a la siguiente componente del pipeline, dandose esto hasta pasar por todas las componentes de éste.

### Escalamiento lineal (Normalización)

Pipeline: Distribucion simetrica? Si --> Aplico escalamiento lineal

La normalización es una técnica que a menudo se aplica como parte de la preparación de datos para el aprendizaje automático. **El objetivo de la normalización es cambiar los valores de las columnas numéricas en el conjunto de datos para usar una escala común, sin distorsionar las diferencias en los rangos de valores ni perder información**. La normalización también es necesaria para que algunos algoritmos modelen los datos correctamente.

Por ejemplo, suponga que su conjunto de datos de entrada contiene una columna con valores que van de 0 a 1 y otra columna con valores que van de 10,000 a 100,000. La gran diferencia en la escala de los números podría causar problemas al intentar combinar los valores como características durante el modelado.

La normalización evita estos problemas al crear nuevos valores que mantienen la distribución general y las proporciones en los datos de origen, mientras mantienen los valores dentro de una escala aplicada en todas las columnas numéricas utilizadas en el modelo.

Tenemos varias opciones para transformar datos numéricos:

- Cambiar todos los valores a una escala de 0 a 1 o transformar los valores representándolos como rangos de percentiles en lugar de valores absolutos.
- Aplicar la normalización a una sola columna o a varias columnas en el mismo conjunto de datos.
- Si necesita repetir el experimento o aplicar los mismos pasos de normalización a otros datos, puede guardar los pasos como una transformación de normalización y aplicarlos a otros conjuntos de datos que tengan el mismo esquema.

> Nota importante: Algunos algoritmos requieren que los datos se normalicen antes de entrenar un modelo. Otros algoritmos realizan su propia normalización o escalado de datos.

Algunas preguntas que nos podemos hacer:

**¿Por qué usarlo?** --> Porque los modelos de machine learning son eficientes en el rango [-1, 1].

**¿Hay diferentes tipos?**

- max-min

$$x_s=\frac{2x-\max - \min}{\max - \min}$$

- **Clipping:** se toma la distribución y se le define un límite superior e inferior. Los valores que superen el límite superior se "colapsan", es decir se convierten en el valor del límite. Los valores que estén por debajo del límite inferior se colapsan en el valor del límite inferior. ***Ejemplo:***
    - Se define como **límite inferior** 2.0
    - Se define como **límite superior** 4.0
    
    $$x_s = 3.8 \to 3.8 \\
    6.0 \to 4.0 \\
    1.0 \to 2.0$$
    
    Los valores que no sobrepasen el rango permanecen igual, los valores que superen los límites se colapsan en el límite definido.
    
    Este método tiene una desventaja y es que omite datos que pueden ser útiles para el modelo aunque sean outliers. Por esta razón no se recomienda mucho usar este escalador.
    
- **Winsorizing:** es algo muy similar al clipping, solo que los límites se definen con base en los percentiles.
- **Z-Score**: se tiene un conjunto de datos {x_1,...,x_n} al que se le calcula mu y sigma. Para normalizar los datos se hace lo siguiente:

$$x_s=\frac{x-\mu}{\sigma}$$

![z-score](https://imgur.com/v9pTbrZ.png)

> Más información en la [Documentación de Normalization de Google Developers](https://developers.google.com/machine-learning/data-prep/transform/normalization)

**¿Cuándo usarlos?** --> cuando tenemos data simétrica o uniformemente distribuida


### Transformación no lineal

> Pipeline: Distribucion simetrica? No --> Aplico transformacion no lineal --> Aplico escalamiento lineal

**¿Por qué usarlos?**
En el caso donde haya datos fuertemente sesgados y no simétricos.

**¿Cual es el efecto que tiene?** - **Algunos tipos**:

- **Tanh**: Puedo agarrar los valores de una columna y aplicarle la funcion `f(x) = tanh(x)`. El efecto que tendría sobre los datos sesgado se puede visualizar en la siguiente imagen, generando una distribución normal corrigiendo la distribución sesgada.

![tnl-tanh](https://imgur.com/2P5fu6z.png)

Puedo variar la forma de la distribución con un parametro `a` que me aplana mas o menos la curva de distribución
![tnl-tanh2](https://imgur.com/adKW3Vo.png)

- **Monomios o polinomios**: Podemos aplicar una transformacion no lineal usando `f(x) = x ^ 1/2` o raiz cuadrada. La transformación seria como se ve en la imagen.

![tnl-raiz2](https://imgur.com/T4yellj.png)

- **Logística**
- **LogNormal**
- Las formulas de estas transformaciones se pueden encontrar en Numpy

**¿Cuándo usarlos?**
Justo antes de aplicar el escalamiento lineal, las transformaciones no lineales solo son para que nuestros datos queden lineales para luego aplicar la normalización lineal. Siempre se debe aplicar la normalización lineal.


## Procesamiento de datos numéricos en Python

Notebook aplicando transformaciones lineales y no lineales en Python --> [[clase-15]Procesamiento-datos-numericos](clases_notebooks/[clase-15]Procesamiento-datos-numericos.ipynb)

## Pipelines de procesamiento para variables categóricas

> Pipeline: Tipo de variable? Categorica --> Hacer mapeo numérico --> Numero de valores < 15 --> One-hot. De lo contrario usa Dummy .

- **Dummy** : es la representación más compacta que se puede tener de los datos. Es mejor usarla cuando los inputs son variables linealmente independientes (no tienen un grado de correlación significativo). Es decir, las cuando se sabe que las categorías son independientes entre sí.
- **One-hot** : es más extenso. Permite incluir categorías que no estaban en el dataset inicialmente. De forma que si se filtra una categoría que no estaba incluida, igual se pueda representar numéricamente y no de error en el modelo.

> [Categorical Variables](https://www.kaggle.com/alexisbcook/categorical-variables) --> One-hot encoding generally does not perform well if the categorical variable takes on a large number of values (i.e., you generally won’t use it for variables taking more than 15 different values).

> [Strategies for working with discrete, categorical data](https://towardsdatascience.com/understanding-feature-engineering-part-2-categorical-data-f54324193e63)

## Procesamiento para variables categóricas con Python

Notebook aplicando procesamiento para variables categóricas en Python --> [[clase-17]Procesamiento-datos-categoricos](clases_notebooks/[clase-17]Procesamiento-datos-categoricos.ipynb)

Aplicat One-hot encoding inplica crear nuevas variables que antes no existian, lo que generará que perdamos rendimiento a la hora entrenar a nuestro algoritmo. La mejor forma de reducir variables que no se utilicen realmente es hacer un analisis de correlación y de componentes principales.

## Correlaciones

¿Qué es correlación?

- **Correlación:** la correlación es una medida estadística que expresa hasta qué punto dos variables están relacionadas linealmente (esto es, cambian conjuntamente a una tasa constante).

¿Por qué es importante la correlación?

- Si se tienen 2 variables que están correlacionadas entre sí, no tiene sentido incluir ambas variables en un modelo de ML porque probablemente las 2 van a aportar la misma información si la correlación es muy alta. En ese caso se elimina a una de las 2, básicamente en eso consiste la *reducción de datos.*

¿Qué es la covarianza?

- **Covarianza:** es un valor que indica el grado de variación conjunta de dos variables aleatorias respecto a sus medias

    $$\text{covarianza}=\frac{1}{n-1}\sum_{i=1}^n(x_i-\bar{x})(y_i-\bar{y})$$

¿Qué es el coeficiente de correlación?

- **Coeficiente de correlación:** es la medida específica que cuantifica la intensidad de la relación lineal entre dos variables en un análisis de correlación.

    $$\rho=\frac{\text{covarianza}}{\text{std(x)std(y)}}$$

![coefi-corre](https://imgur.com/6s39d78.png)

- Si las variables tienen un **coeficiente de correlación muy alto** las variables tienen una **correlación muy elevada.**
- Si el **coeficiente de correlación es muy bajo** las variables tienen una **correlación muy baja.**

![coefi-corre2](https://imgur.com/Bxra0H7.png)
> Siempre debemos considerar que: Correlación no implica causalidad.  

## Matriz de covarianza

Una matriz de varianzas-covarianzas es una matriz cuadrada que contiene las varianzas y covarianzas asociadas con diferentes variables. Los elementos de la diagonal de la matriz contienen las varianzas de las variables, mientras que los elementos que se encuentran fuera de la diagonal contienen las covarianzas entre todos los pares posibles de variables.

![matriz-cov](https://imgur.com/DLHIDzO.png)

![matriz-cov2](https://imgur.com/rapcqeI.png)

Notebook haciendo estudio con matriz de covarianza en Python --> [[clase-19]matriz-covarianza](clases_notebooks/[clase-19]matriz-covarianza.ipynb)

# Proyecto de aplicación

## Reducción de dimensionalidad con PCA (análisis de componentes principales)

Notebook aplicando reducción de dimensionalidad con PCA en Python --> [[clase-22]PCA](clases_notebooks/[clase-22]PCA.ipynb)

## Conclusión

**Visión de la estadística descriptiva:** Resumir información con números y con visualizaciones

La estadística descriptiva nos permite trabajar con **2 bloques fundamentales de la ciencia de datos**:

- El análisis exploratorio de datos.
- En el procesamiento de la información, antes de pasar al modelo de Machine Learning.

**¿Por qué es tan importante el procesamiento de datos?** 

El procesamiento de datos es muy importante para que todo tenga un formato estandarizado (**escalamiento**) para que sea de fácil entendimiento para un modelo de Machine Learning. 


Sabiendo eso, las correlaciones son fundamentales para ver que variables tienen una alta relación y de ahí evidenciar que puede haber variables que pueden resultan redundantes para el modelo.

Y como conclusión final vimos la **técnica PCA**: el análisis de componentes principales es una técnica utilizada para describir un conjunto de datos en términos de nuevas variables no correlacionadas. PCA es para reducir la cantidad de datos. Puedo preparar los datos crudos a un solo formato numerico y ese formato numerico que tenga la menor cantidad de informacion, pero la suficiente para que nuestro algoritmo pueda funcionar bien y pueda hacer predicciones que sigan representando lo que los datos originales estaban mostrandome, en termino de clasificacion, prediccion con regresiones.
