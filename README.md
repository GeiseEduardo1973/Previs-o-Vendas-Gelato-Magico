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
* **Custos**: Para a execução do AutoML, optou-se pela Computação Sem Servidor (Serverless), visando a otimização de custos e a escalabilidade automática conforme a demanda do treinamento, garantindo eficiência no uso dos recursos do Azure.

## 📊 Insights e Resultados
* O modelo identificou uma forte correlação positiva entre o aumento da temperatura e o volume de vendas.
* Através do AutoML, o Azure testou diversos algoritmos (como VotingEnsemble e Gradient Boosting) para encontrar o de menor erro.
* **Métrica Final**:"O modelo final foi concluído com sucesso utilizando o algoritmo VotingEnsemble. A métrica de erro (NRMSE) alcançada foi de 0.21663, demonstrando uma capacidade preditiva sólida para as vendas da sorveteria."

🏆 Conclusão do Projeto: Previsão de Vendas Gelato Mágico
Objetivo Alcançado: O projeto demonstrou a viabilidade de utilizar Machine Learning para prever a demanda de vendas baseada em variações climáticas. Através da plataforma Azure, foi possível automatizar a seleção do melhor algoritmo preditivo.

Destaques Técnicos:

Modelo Vencedor: O algoritmo VotingEnsemble foi identificado como a melhor solução, combinando as forças de múltiplos modelos para reduzir o erro.
Métrica de Performance: Alcançamos um NRMSE de 0.21663, um resultado excelente que permite uma margem de segurança segura para a gestão de estoques.
Tratamento de Dados: Superamos o desafio inicial de volume de dados ao expandir o dataset para 305 registros, garantindo a robustez estatística necessária para o treino.
Eficiência de Custos: A utilização de Computação Sem Servidor (Serverless) permitiu que o treino fosse interrompido após 30 minutos (timeout), garantindo o melhor modelo dentro do orçamento previsto.

Impacto no Negócio: Com este modelo, a "Gelato Mágico" pode agora antecipar picos de venda em dias de calor intenso, otimizando a escala de funcionários e evitando a falta de produtos, ao mesmo tempo que reduz desperdícios em dias de baixa temperatura.  
---
Desenvolvido por Geise Severo Eduardo para o desafio de ML da DIO.
