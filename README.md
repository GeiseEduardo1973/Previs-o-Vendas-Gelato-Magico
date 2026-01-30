# 🍦 Previsão de Vendas - Gelato Mágico com Azure ML

Este projeto foi desenvolvido como parte de um desafio prático da DIO para aplicar conceitos de **Machine Learning Automatizado (AutoML)** na nuvem. O objetivo é prever o volume de vendas diárias da sorveteria "Gelato Mágico" com base na temperatura média.

## 🚀 Racional do Projeto
A gestão de estoque é um desafio para negócios sazonais. Utilizando inteligência artificial, este projeto busca:
1. **Reduzir Desperdício**: Evitar a superprodução em dias frios.
2. **Otimizar Receita**: Garantir estoque suficiente para picos de demanda em dias de calor intenso.

## 📁 Estrutura do Repositório
* **/inputs**: 
    * `dados_sorvete_azure.csv`: Dataset histórico com 200 registros de temperatura e vendas.
    * `sentencas.txt`: Exemplos de interpretação de negócio para o modelo.
* `README.md`: Documentação do processo e decisões técnicas.

## 🛠️ Configurações do Experimento no Azure ML
Para cumprir os requisitos de um pipeline estruturado e gerenciável, foram utilizadas as seguintes configurações:

* **Tipo de Tarefa**: Regressão (previsão de valores numéricos contínuos).
* **Métrica Primária**: `Normalized root mean squared error` (NRMSE) para avaliar a precisão.
* **Dados**: Divisão de 80% para treinamento e 20% para teste/validação.
* **Computação**: Utilização de instância de CPU dedicada para garantir a integridade do processamento.
* **Gestão**: Registro automático de métricas e modelos via **MLflow**.

## 📊 Insights e Resultados
* O modelo identificou uma forte correlação positiva entre o aumento da temperatura e o volume de vendas.
* Através do AutoML, o Azure testou diversos algoritmos (como VotingEnsemble e Gradient Boosting) para encontrar o de menor erro.
* **Métrica Final**:O modelo foi otimizado para minimizar o NRMSE, garantindo que as previsões de vendas de sorvete sejam as mais precisas possíveis".

---
Desenvolvido por Geise Severo Eduardo para o desafio de ML da DIO.
