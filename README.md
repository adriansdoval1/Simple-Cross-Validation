# Simple-Cross-Validation
Simple Cross Validation Methodology
## 1. Descripción de la Metodología

La metodología de *Cross Validation* sirve para evaluar el desempeño de un modelo y también funciona para identificar si el modelo tuvo mucho *overfit*, ya que la variabilidad sería alta.

El algoritmo se evalúa siguiendo los siguientes pasos:

1. **División de la muestra**  
   La muestra se divide de forma aleatoria en *k* partes iguales (en inglés conocidas como *folds*, por eso la metodología también se conoce como *k-fold validation*):


2. **Entrenamiento del modelo excluyendo una submuestra**  
Se toma una submuestra *j* (con j = 1, ..., k) y se estima el modelo con el resto de las submuestras (es decir, con toda la muestra excepto con los datos que correspondan a la Submuestra *j*):

3. **Evaluación del modelo**  
Con el modelo estimado en el paso anterior, se evalúa el modelo en la submuestra excluida (es decir, con la Submuestra *j*):


4. **Repetición del proceso**  
El paso 2-3 se repite hasta que se hayan excluido todas las *k* submuestras (es decir, hasta que se haya estimado el modelo y calculado el error excluyendo cada una de las submuestras).
