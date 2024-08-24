**Seminário 2023**

# Estudos sobre Regressão Linear

>[!IMPORTANT]
>
>  Neste estudo, a regressão logística não será abordada, devido ao foco da pesquisa ser em modelos de regressão, e não em modelos de classificação.


## O que é Análise de Regressão?

A análise de regressão é um método estatístico que estuda a relação entre uma variável dependente e uma ou mais variáveis independentes. A variável dependente é aquela que se deseja prever ou explicar, enquanto as variáveis independentes são aquelas que podem influenciar a variável dependente.É uma ferramenta poderosa que pode ser usada em diversas áreas, como economia, marketing, medicina, engenharia e ciências sociais. Ela pode ser usada para:

* **Prever valores futuros**: uma empresa pode usar a análise de regressão para prever as vendas futuras de um produto.
* **Explicar a relação entre variáveis**: um pesquisador pode usar a análise de regressão para entender como o preço de um produto afeta a demanda por ele.
* **Identificar fatores importantes**: um médico pode usar a análise de regressão para identificar os fatores que contribuem para o desenvolvimento de uma doença.

### Exemplo: Prever o valor de uma casa om base em seu tamanho 

Para expressar esta relação e resolver esse problema, precisamos buscar dados históricos de tamanho e preço de casa. Com esses dados, podemos desenvolver e treinar um modelo que aprenda a relação matemática entre o preço e o tamanho da casa. Esse modelo pode ser usado para fazer previsões de preços com base em outros tamanhos de casa.

Como estamos analisando dados históricos para prever um novo preço, esse é um problema de regressão. O fato de preço e tamanho estarem linearmente relacionados (quanto maior o tamanho da casa, maior o preço) torna esse um problema de regressão linear.

<img src="https://github.com/user-attachments/assets/31f7f372-eb26-4597-8f17-cd22b7f2a953" height="500">


## Variáveis Dependente e Independente

Uma variável independente (ou preditora) é utilizada para prever ou explicar variações na variável dependente (ou resposta). Uma variável independente **x** é usada para explicar a variação na variável dependente **y**. Este relacionamento existe em apenas uma direção: 

*variável independente (x) --> variável dependente (y)*. 

Por exemplo, ao prever o preço da casa baseado em seu tamanho, à medida que o tamanho da casa aumenta, o preço tende a crescer. Nesse caso, o tamanho da casa (variável independente) afeta o preço (variável dependente).

## Correlação

A análise de correlação na estatística é procurar o relacionamento ou a  a associação entre as variáveis que estão sendo estudadas, que é interdependência entre duas variáveis ou mais variáveis.  Essa interdependência pode ser:

- **positiva**: quando as variáveis apresentam valores positivos.
- **negativa**: quando as variáveis apresentam valores negativos.
- **nula**: quando não existe correlação.

![image](https://github.com/user-attachments/assets/953525ba-57a1-4181-9e7a-520dd869ea0b)

No exemplo anterior, podemos notar que o tamanho das casas estão diretamente correlacionadas, ou seja, as variáveis movem na mesma direção. 

Um ponto importante é que a **correlação não implica causalidade**. Ou seja, não determina relação de **causa e efeito** entre duas variáveis.

## Tipos de Modelo de Regressão

<img src="https://github.com/user-attachments/assets/50e17e16-e28b-48d1-bc42-c2855cf03881" height="400">

### Regressão Linear Simples

A Regressão Linear Simples é um dos tipos mais simples e básicos de regressão. Ela consiste em traçar uma linha reta entre os pontos de dados para minimizar o erro entre a linha e os pontos.  Na regressão simples temos uma variável dependente **Y** e uma variável independente **X**. 

### Regressão Linear Múltipla

A Regressão Linear Múltipla é usada quando se utilizam mais de uma variável independente para prever uma variável dependente. Ela proporciona um ajuste melhor em comparação com a regressão linear simples quando múltiplas variáveis independentes estão envolvidas.

Na imagem abaixo mostra claramente a principal diferença entre a regressão simples e múltipla:

<img src="https://github.com/user-attachments/assets/4eb78e77-2f2d-421d-861e-6d3e8200e73f" height="400">

Uma regressão linear simples é representada pela equação, que consiste de 2 parâmetros, que correspondem aos coeficientes de uma equação da reta qualquer:

***`E(Y) = α + βX`***

Onde: 

- E(Y) é a variável dependente que estamos prevendo.
- x é a variável independente.
- a é o termo de viés, que representa a inclinação da linha.
- B é a inclinação da variável (o peso atribuído à variável independente).

### Método dos Mínimos Quadrados

Este método tem como objetivo minimizar o erro quadrático geral (mínimos quadrados comuns) em todos os pontos de dados, evitando, assim, que a maioria dos pontos de dados seja excluída da equação. Isso significa que, dada uma linha de regressão através dos dados, calculamos a distância de cada ponto de dados até a linha de regressão, elevamos ao quadrado e somamos todos os erros quadráticos para encontrar a  linha de regressão que melhor se ajusta aos dados.

<img src="https://github.com/user-attachments/assets/21dfbd77-eebb-49fe-9b43-98596aea3caf" height="400">

A reta de regressão que se obtém através do método dos mínimos quadrados é uma aproximação da realidade, pois ela é baseada em um conjunto de dados finito. Como os dados são sempre incompletos, a reta de regressão nunca será perfeita.

Para indicar o quanto útil ou aproximado da realidade é a reta duas medida podem ser utilizadas: 

- **Erro padrão da estimativa →** mede a distância média entre os valores observados e a linha de regressão. Valores menores indicam que a reta de regressão está mais próxima dos dados.
- **Coeficiente de Determinação (R²):** mede a proporção da variância total na variável dependente **Y** que é explicada por uma ou mais variáveis independentes **X**. O coeficiente de determinação é igual ao quadrado do coeficiente de correlação. Portanto, a partir do valor do coeficiente de determinação, podemos inferir o valor do coeficiente de correlação. O coeficiente de determinação é sempre positivo, variando de 0 a 1, enquanto o coeficiente de correlação varia de -1 a 1. Um valor igual a 1 indica um relacionamento positivo perfeito, enquanto um valor igual a -1 indica um relacionamento negativo perfeito. Valores próximos de zero indicam que não há correlação. O coeficiente de determinação indica o quanto a linha de regressão explica o ajuste do modelo, enquanto o coeficiente de correlação mede a força da relação entre as variáveis.


## Referências

* [https://medium.com/data-hackers/tutorial-ajuste-e-interpretação-de-regressão-linear-com-r-5b23c4ddb72](https://medium.com/data-hackers/tutorial-ajuste-e-interpreta%C3%A7%C3%A3o-de-regress%C3%A3o-linear-com-r-5b23c4ddb72)

* [https://www.seldon.io/machine-learning-regression-explained#:~:text=Machine Learning Regression is a,used to predict continuous outcomes](https://www.seldon.io/machine-learning-regression-explained#:~:text=Machine%20Learning%20Regression%20is%20a,used%20to%20predict%20continuous%20outcomes)

* [https://ivanildo-batista13.medium.com/regress%C3%A3o-linear-m%C3%BAltipla-em-python-eb4b6603a3](https://ivanildo-batista13.medium.com/regress%C3%A3o-linear-m%C3%BAltipla-em-python-eb4b6603a3)

* https://www.kaggle.com/datasets/rkiattisak/salaly-prediction-for-beginer


