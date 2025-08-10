# 1. Ensaio de Machine Learning

## 1.1 Objetivo

Colocar em prática todos os algoritmos que foram estudados  na matéria de fundamentos de Machine Learning pela empresa Comunidade DS. O objetivo desse projeto será realizar ensaios com algoritmos de Classificação, Regressão e Clusterização, para estudar a mudança do comportamento da performance, a medida que os valores dos principais parâmetros de controle de overfitting e underfitting mudam.

## 1.2 Planejamento da solução

O produto final será 7 tabelas mostrando a performance dos algoritmos, avaliados usando múltiplas
métricas, para 3 conjuntos de dados diferentes: Treinamento, validação e teste.

## 1.3 Algoritmos ensaiados

### Classificação:

Algoritmos: KNN, Decision Tree, Random Forest e Logistic Regression
Métricas de performance: Accuracy, Precision, Recall e F1-Score

### Regressão:

Algoritmos: Linear Regression, Decision Tree Regressor, Random Forest Regressor, Polinomial
Regression, Linear Regression Lasso, Linear Regression Ridge, Linear Regression Elastic Net,
Polinomial Regression Lasso, Polinomial Regression Ridge e Polinomial Regression Elastic Net
Métricas de performance: R2, MSE, RMSE, MAE e MAPE

### Agrupamento:

Algoritmos: K-Means e Affinity Propagation
Métricas de performance: Silhouette Score

### Ferramentas utilizadas:

Python 3.10 e Scikit-learn

# 2. Desenvolvimento

## 2.1  Estratégia da solução

Para o objetivo de ensaiar os algoritmos de Machine Learning, eu vou escrever os códigos
utilizando a linguagem Python, para treinar cada um dos algoritmos e vou variar seus principais
parâmetros de ajuste de overfitting e observar a métrica final.
O conjunto de valores que fizerem os algoritmos alcançarem a melhor performance, serão aqueles
escolhidos para o treinamento final do algoritmo.

## 2.2 O passo a passo

Passo 1: Divisão dos dados em treino, teste e validação.

Passo 2: Treinamento dos algoritmos com os dados de treinamento, utilizando os parâmetros
“default”.

Passo 3: Medir a performance dos algoritmos treinados com o parâmetro default, utilizando o
conjunto de dados de treinamento.

Passo 4: Medir a performance dos algoritmos treinados com o parâmetro “default”, utilizando o
conjunto de dados de validação.

Passo 5: Alternar os valores dos principais parâmetros que controlam o overfitting do algoritmo até
encontrar o conjunto de parâmetros apresente a melhor performance dos algoritmos.

Passo 6: Unir os dados de treinamento e validação

Passo 7: Retreinar o algoritmo com a união dos dados de treinamento e validação, utilizando os
melhores valores para os parâmetros de controle do algoritmo.

Passo 8: Medir a performance dos algoritmos treinados com os melhores parâmetro, utilizando o
conjunto de dados de teste.

Passo 9: Avaliar os ensaios e anotar os 3 principais Insights que se destacaram.

# Os top 3 Insights

## Insight Top 1

Os algoritmos baseado em árvores possuem uma performance melhores em todas as métricas,
quando aplicados sobre os dados de teste, no ensaio de Classificação.

## Insight Top 2

Os modelos de Regressão Linear obtiveram os piores resultados, 

## Insight Top 3

**O K-Means (k=4)** apresenta melhor desempenho e é o **modelo mais apropriado neste cenário** com base no Silhouette Score

# 3.0 Resultados

## Ensaio de Classificação:

 Sobre os dados de treinamento

| **Nome do Algoritimo** | **Accuracy** | **Precision** | **Recall** | **F1-Score** |
| --- | --- | --- | --- | --- |
| KNN | 0,756 | 0,731 | 0,692 | 0,711 |
| Decision Tree | 0,966 | 0,977 | 0,944 | 0,960 |
| Random Forest | 1,000 | 1,000 | 1,000 | 1,000 |
| Logistic Regression | 0,566 | 0,000 | 0,000 | 0,000 |

 Sobre os dados de validação

| **Nome do Algoritimo** | **Accuracy** | **Precision** | **Recall** | **F1-Score** |
| --- | --- | --- | --- | --- |
| KNN | 0,666 | 0,622 | 0,587 | 0,604 |
| Decision Tree | 0,951 | 0,957 | 0,920 | 0,943 |
| Random Forest | 0,964 | 0,974 | 0,943 | 0,958 |
| Logistic Regression | 0,566 | 0,000 | 0,000 | 0,000 |

 Sobre os dados de teste

| **Nome do Algoritimo** | **Accuracy** | **Precision** | **Recall** | **F1-Score** |
| --- | --- | --- | --- | --- |
| KNN | 0,667 | 0,630 | 0,587 | 0,608 |
| Decision Tree | 0,949 | 0,956 | 0,927 | 0,942 |
| Random Forest | 0,963 | 0,972 | 0,944 | 0,950 |
| Logistic Regression | 0,561 | 0,000 | 0,000 | 0,000 |

## Ensaio de Regressão:

 Sobre os dados de treinamento

| **Algoritmo** | **R2** | **MSE** | **RMSE** | **MAE** | **MAPE** |
| --- | --- | --- | --- | --- | --- |
| Decision Tree Regressor | 0,111 | 423,74 | 20,58 | 16,36 | 7,86 |
| Random Forest Regressor | 0,14 | 410,71 | 20,26 | 16,09 | 8,32 |
| Polinomial Regression | 0,09 | 432,99 | 20,81 | 16,46 | 8,43 |
| Linear Regression | 0,04 | 455,96 | 21,36 | 16,98 | 8,65 |
| Linear Regression Ridge | 0,04 | 455,99 | 21,35 | 16,99 | 8,65 |
| Linear Regression Elastic Net | 0,03 | 463,34 | 21,52 | 17,12 | 8,68 |
| Polinomial Regression Lasso | 0,08 | 436,51 | 20,89 | 16,32 | 8,32 |
| Polinomial Regression Ridge | 0,09 | 433,74 | 20,82 | 16,47 | 8,37 |
| Polinomial Regression Elastic Net | 0,01 | 471,21 | 21,72 | 17,42 | 0,01 |

 Sobre os dados de validação

| **Algoritmo** | **R2** | **MSE** | **RMSE** | **MAE** | **MAPE** |
| --- | --- | --- | --- | --- | --- |
| Decision Tree Regressor | 0,06 | 447,16 | 21,14 | 16,84 | 8,39 |
| Random Forest Regressor | 0,09 | 429,89 | 20,73 | 16,49 | 8,69 |
| Polinomial Regression | 0,06 | 445,77 | 21,11 | 16,75 | 8,75 |
| Linear Regression | 0,03 | 458,44 | 21,41 | 17,03 | 8,68 |
| Linear Regression Ridge | 0,03 | 458,44 | 21,41 | 17,03 | 8,66 |
| Linear Regression Elastic Net | 0,02 | 463,95 | 21,53 | 17,09 | 8,67 |
| Polinomial Regression Lasso | 0,06 | 444,81 | 21,92 | 16,73 | 8,59 |
| Polinomial Regression Ridge | 0,06 | 445,18 | 21,09 | 16,73 | 8,56 |
| Polinomial Regression Elastic Net | 0,01 | 471,48 | 21,71 | 17,19 | 8,67 |

 Sobre os dados de teste

| **Algoritmo** | **R2** | **MSE** | **RMSE** | **MAE** | **MAPE** |
| --- | --- | --- | --- | --- | --- |
| Decision Tree Regressor | 0,06 | 451,75 | 21,25 | 17,01 | 7,83 |
| Random Forest Regressor | 0,111 | 432,76 | 20,8 | 16,61 | 8,02 |
| Polinomial Regression | 0,09 | 443,04 | 21,05 | 16,72 | 8,12 |
| Linear Regression | 0,05 | 461,42 | 21,48 | 17,12 | 8,52 |
| Linear Regression Ridge | 0,05 | 461,43 | 21,48 | 17,12 | 8,52 |
| Linear Regression Elastic Net | 0,03 | 471,01 | 21,7 | 17,25 | 8,66 |
| Polinomial Regression Lasso | 0,85 | 445,07 | 21,09 | 16,71 | 8,32 |
| Polinomial Regression Ridge | 0,08 | 443,48 | 21,05 | 16,72 | 8,63 |
| Polinomial Regression Elastic Net | 0,01 | 21,94 | 21,94 | 17,42 | 8,75 |

## Ensaio de Clusterização:

| **Algoritmo** | **Número de clusters** | **Average Silhouette Score** |
| --- | --- | --- |
| K-Means | 4 | 0,2483 |
| Affinity Propagation | 8 | 0,2022 |

# Conclusões

Nesse ensaio de Machine Learning, consegui adquirir experiência e entender melhor sobre os limites
dos algoritmos entre os estados de underffiting e overfitting.

Algoritmos baseados em árvores são sensível quanto a profundidade do crescimento e do número de árvores na floresta, fazendo com que a escolha correta dos valores desses parâmetros impeçam os algoritmos de entrar no estado de overfitting.

Os algoritmos de regressão, por outro lado, são sensíveis ao grau do polinômio. Esse parâmetro
controla o limite entre o estado de underfitting e overfitting desses algoritmos.
Esse ensaio de Machine Learning foi muito importante para aprofundar o entendimento sobre o
funcionamento de diversos algoritmos de classificação, regressão e clusterização e quais os principais parâmetros de controle entre os estados de underfitting e overfitting.

## Próximos passos

Como próximos passos desse ensaio, pretendo ensaiar novos algoritmos de Machine Learning e usar
diferentes conjuntos de dados para aumentar o conhecimento sobre os algoritmos e quais cenários são mais favoráveis para o aumento da performance dos mesmos
