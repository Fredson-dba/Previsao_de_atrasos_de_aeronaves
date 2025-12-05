# Previsão de atrasos de aeronaves

OBJETIVO DA ATIVIDADE 

Implementar um modelo de Machine Learning em Google Colab, utilizando o dataset de voos para prever atrasos de aeronaves. 

Objetivos específicos: 

Separar os dados em treino, validação e teste. 

Treinar um modelo preditivo no Colab (por exemplo, XGBoost). 

Avaliar métricas de desempenho (ex.: accuracy, F1, recall, precision). 

Ajustar hiperparâmetros e registrar os impactos nos resultados. 

Realizar inferências com novos dados e analisar os resultados. 

 

DESAFIO 

Utilizando o Google Colab, implemente um pipeline completo de treinamento de modelo para prever atrasos de voos. 

O seu notebook deve, no mínimo: 

Preparar os dados para o treinamento, dividindo-os entre treino, validação e teste. 

Configurar e treinar um modelo de Machine Learning (ex.: XGBoost). 

Ajustar hiperparâmetros para otimizar o desempenho do modelo. 

Avaliar os resultados utilizando métricas adequadas. 


PREVISÃO DE ATRASOS DE AERONAVES

🎯 OBJETIVO DA ATIVIDADE

Implementar um modelo de Machine Learning em Google Colab, utilizando o dataset de voos para prever atrasos de aeronaves.

Objetivos específicos:

- Separar os dados em treino, validação e teste.
- Treinar um modelo preditivo no Colab (por exemplo, XGBoost).
- Avaliar métricas de desempenho (ex.: accuracy, F1, recall, precision).
- Ajustar hiperparâmetros e registrar os impactos nos resultados.
- Realizar inferências com novos dados e analisar os resultados.

🧩 DESAFIO

Utilizando o Google Colab, implemente um pipeline completo de treinamento de modelo para prever atrasos de voos.

O seu notebook deve, no mínimo:

1.	Preparar os dados para o treinamento, dividindo-os entre treino, validação e teste.
2.	Configurar e treinar um modelo de Machine Learning (ex.: XGBoost).
3.	Ajustar hiperparâmetros para otimizar o desempenho do modelo.
4.	Avaliar os resultados utilizando métricas adequadas.

OBS: Antes de treinar qualquer modelo, é preciso inspecionar, compreender e organizar os dados. Este desafio cobre somente as etapas de treinamento do modelo. A parte de preparação dos dados já foi abordada em módulo anterior.

🛠️ ORIENTAÇÕES TÉCNICAS

Na construção do seu notebook, é obrigatório fazer, se aplicável:

| Etapa | Ações mínimas requeridas | Funções/Ferramentas-chave |
| --- | --- | --- |
| Carregamento seguro | Ler o CSV flights_delays_120.csv. Garantir separador, decimal e encoding corretos. | pd.read_csv, dtype= |
| Preparação dos dados | Separar treino, validação e teste. Tratar variáveis categóricas. | train_test_split, pd.get_dummies |
| Configuração do modelo | Definir algoritmo e hiperparâmetros iniciais. | XGBClassifier() |
| Treinamento | Ajustar modelo com dados de treino. | .fit() |
| Avaliação | Calcular métricas: accuracy, F1, recall, precision. | sklearn.metrics |
| Ajuste de hiperparâmetros | Testar combinações automáticas ou manuais. | GridSearchCV ou laços manuais |
| Inferência | Usar novos dados para validar previsões. | .predict(), .predict_proba() |

💡 DICAS

1.	Divisão e Estratificação: 

- Separe os dados em treino, validação e teste usando train_test_split, com estratificação da variável-alvo (ex.: atraso = 1 se atraso > 15min).

2.	Preparação dos Dados:
- Verifique tipos de variáveis (int, float, object).
- Normalize ou padronize colunas numéricas, se necessário.
- Elimine colunas redundantes.

3.	Escolha do Algoritmo:

- Comece com um baseline simples (Regressão Logística ou Árvore de Decisão).
- Em seguida, use XGBoost para obter melhor desempenho.

4.	Configuração do Modelo:

-	Defina hiperparâmetros iniciais: max_depth, learning_rate, subsample, colsample_bytree, n_estimators.
-	Registre esses parâmetros no notebook para comparação.

5.	Treinamento e Avaliação:

-	Treine o modelo.
-	Avalie com accuracy, precision, recall e F1-score.
-	Gere uma matriz de confusão para visualizar erros e acertos.

6.	Ajuste de Hiperparâmetros (HPO):
-	Use GridSearchCV ou loops manuais para testar diferentes combinações.
-	Registre os melhores resultados e compare com o baseline.

7.	Documentação dos Insights:
-	Anote no notebook:
a. Quais parâmetros foram testados.
b. Como as métricas variaram.
c. Conclusões sobre o desempenho.

