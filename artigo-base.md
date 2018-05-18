# Informações do artigo base
Comment Volume Prediction using Neural Networks and Decision Trees - Kamaljot Singh, Ranjeet Kaur, Dinesh Kumar [[pdf](http://uksim.info/uksim2015/data/8713a015.pdf)].
 
 ## Divisão Treino/Teste
 
 Uma divisão temporal foi realizada entre dados passados (para treinar o modelo) e futuros (para testar o modelo), a partir de um limiar de data.

Após a divisão em duas partes (conjuntos de treino e teste), os dados foram vetorizados. A transformação em vetores é necessária para permitir a análise  correta dos dados, e é realizada de forma específica em cada um dos dois conjuntos:

No conjunto de treino, a vetorização ocorre em paralelo à geração de variante (quantas instâncias do conjunto final são derivadas por uma única instância original). Isto é feito atribuindo diferentes datas à mesma postagem, de forma aleatória.

No conjunto de teste, 10 casos são desenvolvidos aleatoriamente com 100 instâncias cada para avaliação, e então são transformados em vetores.

## Modelos

Os modelos utilizados para os experimentos são:

* Multi-Layer preceptron (MLP)
* RBF Networks
* REP Tree
* M5P Tree

A implementação dos modelos foi em WEKA (The Waikato Environment for Knowledge Analysis).

## Métricas

As métricas adotadas para avaliar os modelos foram:

* Hits@10
* Área sob a curva (AUC)
* Tempo de execução
* Erro Médio Absoluto (MAE)

### Hits@10

Para cada caso de teste, consideram-se as 10 postagens preditas com maior número de comentários e contam-se quantas de fato estão no conjunto de postagens com maior número de comentários. Esta avaliação é chamada Hits@10. A média desta métrica é avaliada em todos casos de teste.

### AUC@10

De acordo com a métrica Hits@10, pode-se obter uma matriz de confusão e assim calcular a área sob a curva ROC (Receiver operating characteristic). Para determinar os números de verdadeiros e falsos positivos e negativos, avalia-se cada predição do conjunto dos 10 mais comentados. Assim, a AUC é dada por:

![](https://latex.codecogs.com/gif.latex?AUC&space;=&space;\frac{Tp}{Tp&space;&plus;&space;Fp})

Onde ![](https://latex.codecogs.com/gif.latex?T_p) é o número de verdadeiros positivos e ![](https://latex.codecogs.com/gif.latex?F_p) o número de falsos positivos.

### Erro Médio Absoluto (MAE)

Esta medida define quão perto a predição chegou do número real de comentários, e é determinada pela equação seguinte:

![](https://latex.codecogs.com/gif.latex?M.A.E&space;=&space;\frac{1}{n}&space;\sum_{i&space;=&space;1}^{n}&space;|&space;f_i&space;-&space;y_i&space;|)

Onde ![](https://latex.codecogs.com/gif.latex?f_i) é o valor predito e ![](https://latex.codecogs.com/gif.latex?y_i) o valor verdadeiro.

### Tempo de Execução

Medição do tempo de treino e teste de cada modelo.
