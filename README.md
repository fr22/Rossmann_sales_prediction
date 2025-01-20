# Previsão de Vendas - Rossmann

Este projeto visa resolver um problema que é a previsão do faturamento de uma rede de farmácias para um período de 6 semanas. Para tal, foi desenvolvido um modelo de aprendizado de máquina utilizando dados da empresa Rossmann disponibilizados na plataforma Kaggle. A partir do resultado, seria possível fazer um planejamento para auxiliar em tomadas de decisões estratégicas.

## Índice

1. [Introdução](#introdução)
2. [Dados](#dados)
3. [Objetivos do Projeto](#objetivos-do-projeto)
4. [Metodologia](#metodologia)
5. [Tecnologias Utilizadas](#tecnologias-utilizadas)
6. [Resultados](#resultados)
7. [Estrutura do Projeto](#estrutura-do-projeto)
8. [Licença](#licença)

---

### Introdução

A Rossmann é uma rede de farmácias na Europa com milhares de lojas em diversos países. A empresa precisa fazer reformas em suas lojas, mas pra isso precisa de uma previsão do faturamento diário por loja dentro de um período de seis semanas. A partir dessa informação, seria possível para o time de negócio planejar qual valor seria disponibilizado para cada loja, bem como estabelecer prioridades.

---

### Dados

Os dados utilizados neste projeto foram extraídos da competição no Kaggle e incluem:

- **Informações da Loja**: Dados como tipo de loja e concorrência.
- **Histórico de Vendas**: Vendas diárias de diferentes lojas.
- **Fatores Externos**: Incluem promoções e feriados.

---

### Objetivos do Projeto

1. Criar um modelo preditivo para vendas diárias das lojas.
2. Identificar os principais fatores que influenciam as vendas.
3. Fazer o deploy de uma API que disponibilize o modelo para um bot do Telegram.

---

### Metodologia

1. **Descrição dos dados**:
   - Estatística descritiva.
   - Tratamento de valores ausentes.

2. **Engenharia de Features**:
   - Levantamento de hipóteses.
   - Criação de variáveis de sazonalidade.

3. **Filtragem de variáveis**:
   - Remover features que não poderão ser usadas no momento da previsão.

4. **Análise exploratória de dados**:
   - Validação das hipóteses e compreensão do problema de negócio.
   - Análise univariada, bivariada e multivariada.

5. **Preparação dos dados**:
   - Reescala e encoding.

6. **Seleção de features**:
   - Utilização do método Boruta.

7. **Modelagem de Machine Learning**:
   - Testes de diferentes modelos.

8. **Fine tuning**:
   - Definição dos melhores parâmetros para o modelo XGBoost através do método Random Search.
   - Cross validation.

9. **Tradução e interpretação do erro**:
   - Avaliação das métricas de performance.
   - Conversão da métrica em termos financeiros para o negócio.

10. **Deploy do modelo em produção**:
    - Criação e teste das APIs.
    - Criação do bot no Telegram.

---

### Tecnologias Utilizadas

- **Linguagem de Programação**: Python 3
- **Bibliotecas**:
  - Análise de Dados: `pandas`, `numpy`
  - Visualização: `seaborn`
  - Modelagem: `scikit-learn`, `xgboost`
  - Ambiente de Desenvolvimento: Jupyter Notebook, Google Colab
  - Serviço de nuvem: Render

---

### Resultados

Os principais insights e métricas obtidos foram:

- Melhor modelo: **XGBoost**, com RMSE de **1164.96 +/- 190.07** no cross validation.
- Insight:
  1. Ao contrário do que se imaginava, lojas com competidores próximos vendem mais.

---

### Estrutura do Projeto

- O notebook com as análises está na raiz.
- Os dados estão na pasta `data`.
- O mindmap de agentes e atributos feito no Passo 2 está na pasta `img`.
- O arquivo da API de previsão de vendas está na pasta `api`.
- O arquivo da API que conecta com o bot do Telegram está na pasta `rossmann-telegram-api`.
- Os arquivos do modelo e funções de preparação dos dados exportados em formato `.pkl` estão nas pastas `model` e `parameter`, respectivamente.

---

### Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

