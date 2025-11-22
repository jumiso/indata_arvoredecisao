# Analise de cancelamentos de clientes

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]((https://colab.research.google.com/drive/1wLV7aLHahsO1vFuoJ953vAvOCNdPN1UT?usp=sharing))

Link do dataset - [https://www.kaggle.com/datasets/abhinav89/telecom-customer]

## Sobre o Projeto
Este projeto visa prever a probabilidade de cancelamento de serviço (Churn) por clientes de uma empresa de telecomunicações. Utilizando dados históricos de uso, plano e perfil demográfico, foi desenvolvido um modelo de classificação para identificar clientes em risco, permitindo ações preventivas de retenção.

## Tecnologias Utilizadas
* **Linguagem:** Python
* **Bibliotecas:** Pandas, Numpy, Matplotlib, Seaborn, Scikit-learn, Imbalanced-learn (SMOTE).
* **Modelo:** Decision Tree Classifier.

## Etapas do Projeto
1.  **Análise Exploratória (EDA):** Identificação de variáveis redundantes e análise de correlação.
2.  **Pré-processamento:**
    * Limpeza de dados (remoção de nulos e colunas irrelevantes).
    * Tratamento de outliers (IQR).
    * Codificação de variáveis categóricas (One-Hot Encoding).
3.  **Balanceamento de Classes:** Utilização da técnica **SMOTE** para equilibrar a classe alvo (Churn).
4.  **Modelagem:** Treinamento de Árvore de Decisão com otimização de hiperparâmetros via **RandomizedSearchCV**.
5.  **Avaliação:** Análise de Acurácia, Recall, Precisão e Matriz de Confusão.

## Resultados e Insights
O modelo obteve um foco maior na métrica de **Recall (66%)** para a classe de cancelamento, o que é estratégico para o negócio (é melhor errar tentando salvar um cliente que não sairia, do que deixar sair um cliente que o modelo não viu).

**Fatores determinantes para o cancelamento:**
* **Tempo de equipamento (eqpdays):** Clientes com equipamentos muito antigos tendem a cancelar mais.
* **Uso excedente (vceovr_Mean):** Clientes que estouram seus planos de voz com frequência estão mais propensos ao Churn.
* **Média de uso (mou_Mean):** O padrão de consumo mensal é um forte indicador de retenção.

## Como Executar
1.  Clone o repositório.
2.  Instale as dependências: `pip install -r requirements.txt`
3.  Execute o notebook `analise_cancelamento_clientes.ipynb`.

---
*Desenvolvido por Jussara Miliano Soares*
