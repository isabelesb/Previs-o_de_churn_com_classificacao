# Previsão de Churn com Classificação

Aqui, o objetivo é prever quais clientes poodem cancelar o serviço de streamming, utilizando modelos de classificação. 

## Bibliotecas:
* Pandas.
* Scikit-Learn.

## Análise Exploratória:
1. Não há outliers, nem dados duplicados.
2. Há muitos dados nulos, e eles precisarão ser tratados de formas diferentes, pois algins são de ID e outros numéricos.
3. É necessário normalizar, para que o medelo não seja influenciado pela diferença de valores entre as colunas.

## Tratamento dos Dados:
1. Substituímos os dado nulos numéricos por 0.
2. Excluímos as linhas com *UserID* nulo.
3. Transformamos os dados de *Churn* em No e Yes ao ivés de 0 e 1.
4. Transformamos dados *float* em *int*.

## Modelo:
1. Separamos as variáveis em features(varoáveis explicativas) e target(objetivo da previsão).
2. Utilizamos *pd.get_dummies()* e *LabelEncoder()* para tratar as variáveis categóricas, pois precisamos que todos os dados utilizados no modelo sejam numéricos.
3. Normalizamos com *MinMaxScaler()*.
4. Modelamos com Regressão Logística e Random Forest Classifier.
5. Para avaliar o modelo foram usados: Matriz de Confusão, Acurácia, Acurácia Balanceada e F1 Score.

## Conclusão Inicial:
* Os modelos perfomaram de forma muito discrepante nos treinos e tetes.
* O Random Forest mostrou desempenho um pouco melhor, mas mesmo depois do Tunning continuou performando mal.
* Infelizmente, os dados tinham uma distribuição muito desigual, o que prejudicou o desemprenho do modelo. E, potanto, ele se mostrou obsoleto.
