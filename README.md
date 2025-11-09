# Classificador de Machine Learning PRM para EDR

## Visão Geral do Projeto
Este projeto implementa uma solução de machine learning para prever códigos de tarifação EDR (Event Detail Record) com base em dados PRM (Pre-Rating Message). O sistema utiliza um Classificador Random Forest para aprender padrões a partir de dados históricos e prever os códigos de tarifação corretos para serviços de telecomunicações.

## Requisitos
As seguintes bibliotecas Python são necessárias:
- pandas
- scikit-learn
- numpy
- matplotlib
- seaborn

## Arquivos de Dados
O projeto requer três arquivos principais de dados:
1. `amostra_prm.json` - PRMs de entrada em formato JSON
2. `amostra_edr_correto.csv` - Dados EDR de referência (ground truth) em formato CSV
3. `tabela_lookup.csv` - Tabela de contexto/lookup em formato CSV

## Estrutura do Projeto
O projeto consiste nos seguintes componentes principais:

1. **Carregamento e Pré-processamento de Dados**
   - Carrega dados PRM do JSON
   - Carrega dados EDR corretos do CSV
   - Carrega tabela de lookup para enriquecimento de contexto

2. **Engenharia de Features**
   - Padroniza nomes das colunas
   - Realiza enriquecimento de dados através de joins
   - Combina dados PRM com informações de lookup

3. **Pipeline de Machine Learning**
   - Preparação de features com one-hot encoding
   - Codificação de labels para variável alvo
   - Divisão de dados em treino (80%) e teste (20%)
   - Treinamento e avaliação do modelo Random Forest

4. **Avaliação do Modelo**
   - Medição de acurácia nos dados de teste
   - Análise de importância das features
   - Diagnóstico do modelo

## Funcionalidades Principais
- Pré-processamento e enriquecimento de dados
- Engenharia de features automatizada
- Classificação usando Random Forest
- Avaliação de performance do modelo
- Análise de importância das features

## Features do Modelo
O modelo utiliza as seguintes features para previsão:
- Codigo_Servico
- OPERADORA
- TIPO_SERVICO
- PORTADO
- Duracao_Seg (Duração em Segundos)

## Variável Alvo
- COD_TARIFACAO_FINAL (Código de Tarifação Final)

## Como Usar
1. Coloque seus arquivos de dados de entrada no diretório do projeto
2. Execute as células do notebook Jupyter em sequência
3. O modelo será treinado e fornecerá métricas de acurácia
4. A análise de importância das features mostrará quais fatores mais influenciam as previsões

## Performance do Modelo
As métricas de performance do modelo serão exibidas após o treinamento, incluindo:
- Acurácia da classificação
- Ranking de importância das features
- Distribuição das classes previstas

## Contribuindo
Sinta-se à vontade para submeter issues e solicitações de melhorias.


---
*Nota: Atualize os arquivos de dados de entrada com seus dados reais antes de executar o modelo.*