
# Métricas

## Desvio padrão (RMSE)

O desvio padrão é calculado por:

![](https://latex.codecogs.com/gif.latex?RMSE&space;=&space;\sqrt{\frac{1}{N}\sum_{i=0}^N&space;(f_i&space;-&space;y_i)^2})

Onde ![](https://latex.codecogs.com/gif.latex?f_i) é o valor predito pelo modelo e ![](https://latex.codecogs.com/gif.latex?y_i) o valor real. Esta medida informa o quanto os valores reais se distanciam da função de predição. Portanto, quanto menor, melhor. 

Devido ao fator quadrático, um resíduo maior é mais penalizado. Portanto, esta métrica é mais adequada quando a penalidade por um erro não é simplesmente proporcional ao tamanho desse erro.

O termo dentro da raíz também pode ser utilizado diretamente como métrica, que nesse caso é o **MSE**.

## Erro médio absoluto (MAE)
O erro médio absoluto é dado por:

![](https://latex.codecogs.com/gif.latex?MAE&space;=&space;\frac{1}{N}\sum_{i=0}^N&space;|f_i&space;-&space;y_i|)

Onde ![](https://latex.codecogs.com/gif.latex?f_i) é o valor predito pelo modelo e ![](https://latex.codecogs.com/gif.latex?y_i) o valor real. 

Assim como o desvio padrão, indica quão distantes as predições estão dos valores reais, sendo que seu valor ideal é zero.

Diferentemente do desvio padrão, porém, esta métrica atribui pesos proporcionais aos resíduos individuais, ou seja, não penaliza tanto mais um resíduo quanto maior ele for. Por exemplo, um erro 5 vezes maior que outro afeta o resultado final 5 vezes mais.

Devido ao fator quadrático, o RMSE é sempre maior ou igual ao MAE.

## Coeficiente de determinação (R2)


## Fontes
* [Performance measures (Datacamp)](https://campus.datacamp.com/courses/introduction-to-machine-learning-with-r/chapter-2-performance-measures?ex=1)
* [sklearn.metrics.mean_absolute_error (Scikit-Learn)](http://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_absolute_error.html)
* [sklearn.metrics.mean_squared_error (Scikit-Learn)](http://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_squared_error.html)
* [sklearn.metrics.r2_score (Scikit-Learn)](http://scikit-learn.org/stable/modules/generated/sklearn.metrics.r2_score.html)
* [Mean absolute error (Wikipedia)](https://en.wikipedia.org/wiki/Mean_absolute_error)
* [Root mean square deviation (Wikipedia)](https://en.wikipedia.org/wiki/Root-mean-square_deviation)
* [Coefficient of determination (Wikipedia)](https://en.wikipedia.org/wiki/Coefficient_of_determination)
* [How is the R2 value in Scikit learn calculated? (StackOverflow)](https://stackoverflow.com/questions/23309073/how-is-the-r2-value-in-scikit-learn-calculated)
* [RMSE: Root Mean Square Error (Statistics How To)](http://www.statisticshowto.com/rmse/)
* [MAE and RMSE — Which Metric is Better? (Human in a Machine World)](https://medium.com/human-in-a-machine-world/mae-and-rmse-which-metric-is-better-e60ac3bde13d)
* [Metrics – Regression (Josh Lawman)](http://joshlawman.com/metrics-regression/)
