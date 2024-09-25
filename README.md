# Previsão de Churn com Classificação

Aqui, o objetivo é classificar quais clientes serão churn, utilizando modelos de classificação. 

## Bibliotecas:
* Pandas.
* Scikit-Learn.

## Análise Exploratória:
1. Não há dados nulos, nem duplicados.
2. Há muitos dados nulos, e eles precisarão ser tratados de formas diferentes.

## Tratamento dos Dados:
1. Substituímos os dado nulos numéricos po 0.
2. Dropamos as linhas com *UserID* nulo.
3. Transformamos os dados de *Churn* em No e Yes ao ivés de 0 e 1.
4. Transformamos dados *float* em *int*.

## Modelo:
1. Separamos as variáveis em features(*x*) e target(*y*).
2. Utilizamos *pd.get_dummies()* e *LabelEncoder()* para tratar as variáveis categóricas.
3. Normalizamos com *MinMaxScaler()*.
4. Modelamos com Regressão Logística e Random Forest Classifier.
5. Para avaliar o modelo foram usados: Matriz de Confusão, Acurácia, Acurácia Balanceada e F1 Score.

## Conclusão:
* Os modelos perfomaram de forma muito discrepante nos treinos e tetes.
* O Random Forest mostrou desempenho um pouco melhor, mas mesmo depois do Tunning continuou performando mal.
* Infelizmente, os dados tinham uma distribuição muito desigual, o que prejudicou o desemprenho do modelo. E, potanto, ele se mostrou obsoleto.
