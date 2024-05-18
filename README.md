Análise e Modelagem de Churn
Introdução
O churn, ou a taxa de cancelamento de clientes, é uma métrica crucial para qualquer empresa, especialmente para prestadores de serviços. Neste projeto, exploramos um conjunto de dados que contém informações sobre clientes e usamos modelos de aprendizado de máquina para prever o churn. O objetivo é identificar os principais fatores que influenciam os clientes a cancelar seus serviços.

Objetivo do Projeto: Prever se um cliente irá cancelar o serviço (churn) ou não, com base nas variáveis disponíveis.

Principais Variáveis:
Numéricas:

Tenuring: Número de meses que o cliente está na base
MonthlyCharges: Valor consumido pelo cliente mensalmente
TotalCharges: Valor total consumido pelo cliente
Categóricas:

ID do cliente
Gênero (Masculino, Feminino)
Idoso (Sim, Não)
Casado (Sim, Não)
Dependentes (Sim, Não)
Serviço de telefone (Sim, Não)
Múltiplas linhas de telefone (Sim, Não)
Tipo de serviço de internet
Segurança online (Sim, Não)
Backup online (Sim, Não)
Proteção de dispositivos (Sim, Não)
Suporte técnico (Sim, Não)
Streaming de TV (Sim, Não)
Streaming de filmes (Sim, Não)
Contrato (Mensal, Anual)
Fatura por papel (Sim, Não)
Pagamento eletrônico (Sim, Não)
Método de pagamento (Cartão de crédito, Débito, Boleto, Transferência)
Passos Realizados
Importação e Visualização dos Dados: Importamos as bibliotecas necessárias: pandas, seaborn e matplotlib. Carregamos os dados do arquivo "churn_data.xlsx" e visualizamos as primeiras linhas do conjunto de dados.
Análise Descritiva: Realizamos uma análise descritiva das variáveis numéricas, como 'Tenure' e 'MonthlyCharges', e calculamos a quantidade de valores nulos em cada coluna.
Análise de Churn: Agregamos os dados para contar a quantidade de churners e não churners e visualizamos a distribuição usando um gráfico de barras.
Análise por Método de Pagamento: Agrupamos os dados por método de pagamento para analisar a distribuição de clientes e visualizamos a quantidade de clientes por método de pagamento usando um gráfico de barras.
Preparação dos Dados: Removemos as colunas "customerID" e "Churn" do conjunto de dados, transformamos a variável de destino "Churn" em numérica usando Label Encoding, transformamos as variáveis categóricas em variáveis dummy, normalizamos os dados usando Min-Max Scaler e dividimos os dados em conjuntos de treino e teste.
Modelagem de Dados: Utilizamos a Regressão Logística como primeiro modelo de classificação, treinamos o modelo e realizamos previsões nos conjuntos de treino e teste. Avaliamos o desempenho do modelo usando métricas como acurácia, precisão, recall, F1-score e ROC AUC.
Tunagem do Modelo: Utilizamos o algoritmo Random Forest para melhorar o desempenho, realizamos uma busca em grade para encontrar os melhores hiperparâmetros, treinamos o modelo com os melhores parâmetros encontrados e avaliamos o desempenho do modelo tunado usando as mesmas métricas.
Resultados e Conclusão
Resultados da Regressão Logística:

Acurácia (Treino): 0.88
Acurácia (Teste): 0.81
Precision (Teste): 0.69
Recall (Teste): 0.54
F1-Score (Teste): 0.61
ROC AUC (Teste): 0.85
Resultados do Random Forest (Após Tunagem):

Acurácia (Treino): 0.996
Acurácia (Teste): 0.795
Precision (Teste): 0.673
Recall (Teste): 0.441
F1-Score (Teste): 0.533
ROC AUC (Teste): 0.838
Conclusão e Insights de Ação:

Ambos os modelos têm desempenho razoável na previsão do churn.
O modelo de Regressão Logística obteve resultados um pouco melhores em termos de acurácia e recall.
No entanto, o modelo de Random Forest após a tunagem mostrou um aumento significativo na acurácia, mas com uma queda no recall.
Isso sugere que a tunagem do modelo de Random Forest pode não ter sido completamente eficaz, pois o recall diminuiu.
Para melhorar ainda mais o desempenho do modelo, podemos tentar diferentes abordagens de tunagem ou explorar outros algoritmos de aprendizado de máquina.
Além disso, investigar mais a fundo as características dos clientes que cancelam os serviços pode fornecer insights valiosos para ações de retenção de clientes. Isso pode incluir análises mais detalhadas das variáveis e a identificação de padrões específicos que precedem o churn.
Desafios Futuros
Existem muitas outras técnicas e algoritmos que poderiam ser testados para tentar melhorar ainda mais a acurácia na predição de churn, como redes neurais, Support Vector Machines, entre outros. Fica o desafio para trabalhos futuros.

_____________________________________________________________________________________________________________________________________________________________________________________________________________________________________________

Churn Analysis and Modeling
Introduction
Churn, or customer cancellation rate, is a crucial metric for any business, especially service providers. In this project, we explored a dataset containing customer information and used machine learning models to predict churn. The goal is to identify the key factors influencing customers to cancel their services.

Project Objective: Predict whether a customer will cancel the service (churn) or not, based on the available variables.

Key Variables:
Numeric:

Tenuring: Number of months the customer has been with the company
MonthlyCharges: Amount spent by the customer monthly
TotalCharges: Total amount spent by the customer
Categorical:

Customer ID
Gender (Male, Female)
Senior Citizen (Yes, No)
Married (Yes, No)
Dependents (Yes, No)
Phone Service (Yes, No)
Multiple Lines (Yes, No)
Internet Service Type
Online Security (Yes, No)
Online Backup (Yes, No)
Device Protection (Yes, No)
Tech Support (Yes, No)
Streaming TV (Yes, No)
Streaming Movies (Yes, No)
Contract (Monthly, Annual)
Paperless Billing (Yes, No)
Electronic Payment (Yes, No)
Payment Method (Credit Card, Debit, Bank Transfer)
Steps Taken
Data Import and Visualization: We imported the necessary libraries: pandas, seaborn, and matplotlib. We loaded the data from the "churn_data.xlsx" file and visualized the first few rows of the dataset.
Descriptive Analysis: We performed descriptive analysis of the numeric variables, such as 'Tenure' and 'MonthlyCharges', and calculated the quantity of null values in each column.
Churn Analysis: We aggregated the data to count the number of churners and non-churners and visualized the distribution using a bar plot.
Payment Method Analysis: We grouped the data by payment method to analyze the distribution of customers and visualized the quantity of customers per payment method using a bar plot.
Data Preparation: We removed the "customerID" and "Churn" columns from the dataset, transformed the target variable "Churn" into numeric using Label Encoding, transformed categorical variables into dummy variables, normalized the data using Min-Max Scaler, and split the data into training and testing sets.
Data Modeling: We used Logistic Regression as the initial classification model, trained the model, and made predictions on the training and testing sets. We evaluated the model's performance using metrics such as accuracy, precision, recall, F1-score, and ROC AUC.
Model Tuning: We used the Random Forest algorithm to improve performance, conducted a grid search to find the best hyperparameters, trained the model with the best parameters found, and evaluated the performance of the tuned model using the same metrics.
Results and Conclusion
Logistic Regression Results:

Accuracy (Training): 0.88
Accuracy (Testing): 0.81
Precision (Testing): 0.69
Recall (Testing): 0.54
F1-Score (Testing): 0.61
ROC AUC (Testing): 0.85
Random Forest Results (After Tuning):

Accuracy (Training): 0.996
Accuracy (Testing): 0.795
Precision (Testing): 0.673
Recall (Testing): 0.441
F1-Score (Testing): 0.533
ROC AUC (Testing): 0.838
Conclusion and Action Insights:

Both models have reasonable performance in predicting churn.
The Logistic Regression model achieved slightly better results in terms of accuracy and recall.
However, the Random Forest model after tuning showed a significant increase in accuracy but with a decrease in recall.
This suggests that the tuning of the Random Forest model may not have been entirely effective, as recall decreased.
To further improve the model's performance, we can try different tuning approaches or explore other machine learning algorithms.
Additionally, further investigation into the characteristics of customers who cancel services can provide valuable insights for customer retention actions. This may include more detailed analyses of variables and identifying specific patterns preceding churn.
Future Challenges
There are many other techniques and algorithms that could be tested to further improve accuracy in predicting churn, such as neural networks, Support Vector Machines, among others. The challenge remains for future work.
