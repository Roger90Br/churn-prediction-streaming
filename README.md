# Prevendo Churn de Usuários em Plataforma de Streaming

## 📌 Descrição
Este projeto tem como objetivo prever quais usuários possuem maior probabilidade de cancelar sua assinatura em uma plataforma de streaming. A previsão de churn é essencial para que a empresa possa tomar medidas estratégicas que aumentem a retenção dos clientes e reduzam as perdas.

## 📊 Conjunto de Dados
Os dados foram fornecidos pela empresa e contêm informações sobre as contas dos clientes. As principais colunas do dataset incluem:

- **ID do Cliente**: Código identificador do cliente.
- **Idade**: Idade do cliente.
- **Gênero**: Masculino/Feminino/Outro.
- **Região**: Localização do cliente.
- **Dias de Assinatura**: Tempo em dias desde que o cliente assinou a plataforma.
- **Ativo**: Se o cliente está atualmente ativo.
- **Tipo de Conta**: Plano de assinatura do cliente.
- **Quantidade de Conteúdo Assistido**: Volume de conteúdo consumido pelo cliente.
- **Avaliação Média do Conteúdo**: Nota média atribuída pelo cliente aos conteúdos assistidos.
- **Número de Perfis Ativos**: Quantidade de perfis em uso na conta.
- **Quantidade de Serviços de Streaming Utilizados**: Outros serviços de streaming que o cliente também assina.
- **Quantidade de Dispositivos Conectados**: Número de dispositivos vinculados à conta.
- **Cancelamento da Conta**: Indicador se o cliente cancelou ou não a assinatura (variável alvo).

## 🔍 Metodologia
O processo de desenvolvimento do modelo segue as seguintes etapas:

1. **Exploração e Limpeza de Dados**: Análise inicial dos dados, incluindo tratamento de valores nulos, outliers e inconsistências.
2. **Análise Estatística**: Avaliação das distribuições e correlações das variáveis.
3. **Pré-processamento**: Normalização, codificação de variáveis categóricas e tratamento de dados desbalanceados.
4. **Modelagem**: Testes de modelos de classificação, como Regressão Logística e Random Forest.
5. **Avaliação de Desempenho**: Análise dos resultados utilizando métricas como Acurácia, Precisão, Recall e AUC-ROC.

## 🧠 Modelos Utilizados

### 1️⃣ **Regressão Logística**
A Regressão Logística foi utilizada para prever a probabilidade de um cliente cancelar sua assinatura. A modelagem envolveu:

- **Pré-processamento**: Codificação de variáveis categóricas com `LabelEncoder`, normalização com `MinMaxScaler` e balanceamento de classes com `SMOTE`.
- **Tuning de Hiperparâmetros**: A técnica de GridSearchCV foi aplicada para otimizar os parâmetros da Regressão Logística.

### 2️⃣ **Random Forest**
O modelo Random Forest foi utilizado como uma abordagem alternativa para a previsão de churn. O processo incluiu:

- **Pré-processamento**: Similar ao modelo de Regressão Logística, com codificação e normalização de dados.
- **Tuning de Hiperparâmetros**: A busca de melhores parâmetros foi feita através de GridSearchCV.

### 3️⃣ **Balanceamento de Dados com SMOTE**
Devido ao desbalanceamento das classes (churn vs não churn), foi utilizado o **SMOTE** (Synthetic Minority Over-sampling Technique) para aumentar a quantidade de exemplos da classe minoritária.

## 🚀 Como Rodar o Projeto

1. Clone este repositório:
   ```bash
   git clone https://github.com/seu-usuario/churn-prediction-streaming.git
