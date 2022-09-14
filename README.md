# **Detección del número máximo de partículas de una cascada de astropartículas**
<center>
<img src="https://drive.google.com/uc?id=1ZWClpEv4nsRthBfZAwgXH7S-5Hm6rnLB" width="800px" height="300px">
</center>

## **Autores:**
* José Fredy Navarro, 2190044 [Freed219](https://github.com/Freed219).
* Juan Andrés Guarín Rojas, 2201870 [AndresGuarin](https://github.com/AndresGuarin/).
* Brayan Sneider Daza Suárez, 2190040 [BrayanDaza](https://github.com/BrayanDaza).

## **Objetivo**
Aplicar un modelo de regresión para estimar el número máximo de partículas (**MC Xmax**).

## **Dataset** 
El dataset consta de datos simulados por investigadores del [Observatorio Pierre Auger](https://www.auger.org/), y fueron dados por cortesía de [Cristian Sarmiento](https://github.com/csarmiento03) investigador asociado a la Escuela de Física de la UIS. Como los datos no están disponibles de manera online para todo público, se dejaron anexados en este repositorio en la carpeta ```datos```.

El dataset contiene dos archivos. El primero de ellos se llama ```CutEvents_IronRefDist140.txt``` y contiene los datos simulados de 2323 cascadas de astropartículas producidas por la colisión de un núcleo de Hierro con la atmósfera. El segundo de ellos llamado ```CutEvents_ProtonRefDist140.txt``` contiene 2142 datos de cascadas de astropartículas producidas por la llegada de un protón a la atmósfera. Estos dos datasets son usados en conjunto para entrenar el modelo. La relación entre los datos de hierro y protón es cercana al 50%. En los modelos, se revolvieron las filas de datos de manera que el modelo no diferenciaba los datos del hierro y los del protón. Esto lo hicimos considerando que en el caso de tener datos experimentales no tendríamos este tipo de información de la partícula entrante. Usamos estos datasets porque en la vida real el protón y el hierro están en los extremos de masa de las partículas que nos llegan a la Tierra. Siendo el protón el elemento más liviano, y el hierro, el más pesado. En cuanto a las features, el dataset contiene 58 columnas de datos que incluyen caracteristícas relevantes de la cascada como: **GeoCeXmax** medido por un detector de radio, **energía** de la partícula entrante, **ángulo cenital** de incidencia, y **área de esparcimiento** de las partículas de la cascada, entre otros.

## **Modelos**
DecisionTreeRegressor, RandomForestRegressor, cross_val_score.

## **Enlaces**
* Código alojado en Google colab: https://drive.google.com/file/d/1ulZC5_Xf6kswnCSGph2clLh9ZJ5znNLV/view?usp=sharing
* Vídeo en YouTube: https://youtu.be/pqu8OazJmHQ
* Este repositorio: https://github.com/AndresGuarin/ML_Estimacion_Xmax/
