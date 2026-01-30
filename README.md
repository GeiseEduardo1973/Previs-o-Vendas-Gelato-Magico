# 🍦 Previsão de Vendas - Gelato Mágico com Azure ML

Este projeto utiliza Machine Learning Automatizado (AutoML) no Azure para prever o volume de vendas de sorvetes com base na temperatura média diária.

## 🚀 Racional do Projeto
O objetivo é auxiliar a gestão da sorveteria "Gelato Mágico" a otimizar seu estoque e produção. Ao prever picos de demanda em dias quentes, evitamos a falta de produtos; em dias frios, reduzimos o desperdício.

## 📁 Estrutura do Repositório
- `/inputs`: 
  - `dados_sorvete_azure.csv`: Dataset com histórico de 200 dias de vendas.
  - `sentencas.txt`: Exemplos de análise de demanda.
- `README.md`: Documentação completa do projeto.

## 🛠️ Configurações do Experimento
- **Tipo de Tarefa**: Regressão (previsão de valores numéricos).
- **Dados**: Dataset tabular registrado com colunas de Data, Temperatura e Vendas.
- **Computação**: Cluster dedicado para garantir a execução do pipeline.
- **Gestão**: Uso de MLflow para registro automático de métricas e modelos.

## 📈 Insights obtidos
*
