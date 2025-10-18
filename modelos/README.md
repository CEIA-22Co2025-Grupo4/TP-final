### Métricas de Comparación Elegidas

Para evaluar nuestros modelos de clasificación utilizamos un conjunto de métricas que nos ofrecen una visión completa del rendimiento del modelo, especialmente en su capacidad para identificar la clase minoritaria (Arrest_tag=1).

1. *Exactitud (*Accuracy)**

    * Es el porcentaje total de predicciones correctas (Verdaderos Positivos + Verdaderos Negativos) sobre el total de muestras.
    * Proporciona una visión global y rápida del rendimiento general. Sin embargo, la usamos con precaución, ya que en un dataset desbalanceado, un modelo que siempre predice la clase mayoritaria puede obtener una exactitud alta pero ser inútil.

2. *Precisión (*Precision)**

    * Mide la calidad de las predicciones positivas. Responde a la pregunta: "De todos los casos que el modelo predijo como Arrest_tag=1, ¿cuántos eran realmente Arrest_tag=1?"
    * Es crucial cuando el costo de un Falso Positivo es alto. Queremos estar seguros de que cuando el modelo "levanta una alarma" (predice un 1), tiene razón la mayoría de las veces.

3. *Sensibilidad (*Recall)**

    * Mide la capacidad del modelo para encontrar todos los casos positivos. Responde a la pregunta: "De todos los casos que realmente eran Arrest_tag=1, ¿cuántos logró detectar el modelo?"
    * Es la métrica más importante cuando el costo de un Falso Negativo es alto. En nuestro caso, "no detectar" un caso de arresto (un 1) es probablemente el peor error, por lo que un Recall alto es fundamental.

4. *Puntuación F1 (*F1-Score)**

    * Es la media armónica entre Precisión y Sensibilidad. Proporciona una sola puntuación que balancea ambas métricas.
    * Es una métrica de resumen excelente cuando nos importan tanto los Falsos Positivos como los Falsos Negativos. Un modelo debe tener buena Precisión y buena Sensibilidad para obtener un F1-Score alto.

5. *Coeficiente de Correlación de Matthews (MCC)*

    * Mide la calidad de la clasificación binaria considerando las cuatro categorías de la matriz de confusión (VP, VN, FP, FN). Su resultado es un valor entre -1 (desacuerdo total) y +1 (acuerdo perfecto), donde 0 es un rendimiento aleatorio.
    * Es considerada la métrica más robusta y fiable para datasets desbalanceados. A diferencia del F1-Score, el MCC también incluye explícitamente los Verdaderos Negativos en su cálculo, dándonos una medida de correlación completa y equilibrada entre la predicción y la realidad

6. *AUC (Área Bajo la Curva ROC)* 
    * Mide la capacidad del modelo para discriminar entre la clase positiva (1) y la negativa (0). Representa la probabilidad de que el modelo le asigne una puntuación (probabilidad) más alta al caso positivo que al negativo.
    * Su principal ventaja es que es independiente del umbral de decisión.