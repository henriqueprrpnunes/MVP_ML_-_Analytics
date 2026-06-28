# MVP_ML_&_Analytics

# Previsão de Preços de Imóveis com Machine Learning

## Descrição

Este projeto foi desenvolvido como MVP (Minimum Viable Product) da disciplina de Machine Learning & Analytics e tem como objetivo construir e comparar modelos de aprendizado de máquina capazes de prever o preço de imóveis residenciais a partir de suas características físicas e estruturais.

O trabalho contempla todas as etapas de um projeto de Ciência de Dados, desde a definição do problema até a avaliação final dos modelos, seguindo uma abordagem reprodutível e baseada em boas práticas.


## Objetivo

Desenvolver modelos de regressão capazes de estimar o preço de imóveis utilizando informações como:

- Área construída
- Número de quartos
- Número de banheiros
- Número de pavimentos
- Proximidade de rodovia principal
- Quarto de hóspedes
- Porão
- Aquecimento de água
- Ar-condicionado
- Número de vagas de estacionamento
- Localização em área preferencial
- Nível de mobiliário

Além de realizar a previsão dos preços, o projeto busca comparar diferentes algoritmos de Machine Learning e analisar seus desempenhos.


## Dataset

**Housing Prices Dataset**

Fonte:
https://www.kaggle.com/datasets/yasserh/housing-prices-dataset

O conjunto de dados contém **545 imóveis**, sendo composto por uma variável alvo (preço) e doze variáveis explicativas relacionadas às características dos imóveis.


## Tecnologias utilizadas

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Scikit-Learn
- XGBoost


## Etapas do projeto

O notebook foi organizado nas seguintes etapas:

1. Definição do problema
2. Ambiente e bibliotecas
3. Carregamento e compreensão dos dados
4. Análise exploratória dos dados (EDA)
5. Preparação dos dados e divisão treino/teste
6. Pré-processamento e construção dos pipelines
7. Treinamento dos modelos
8. Avaliação inicial
9. Otimização de hiperparâmetros
10. Avaliação final
11. Comparação dos modelos
12. Conclusão


## Pré-processamento

Foram realizadas as seguintes etapas de preparação dos dados:

- transformação logarítmica das variáveis `price` e `area`;
- codificação das variáveis categóricas binárias;
- codificação ordinal da variável `furnishingstatus`;
- separação entre variáveis preditoras e variável alvo;
- divisão dos dados em treino (80%) e teste (20%).


## Modelos avaliados

Foram comparados três modelos de regressão:

- Regressão Linear (baseline)
- Random Forest Regressor
- XGBoost Regressor

Além disso, foi realizada otimização de hiperparâmetros do modelo XGBoost utilizando Grid Search com validação cruzada.


## Resultados

| Modelo | R² | RMSE | MAE |
|---------|---:|---:|---:|
| Regressão Linear | **0.6635** | **0.2549** | **0.2042** |
| XGBoost | 0.6600 | 0.2562 | 0.2045 |
| Random Forest | 0.6338 | 0.2659 | 0.2084 |

Após a otimização de hiperparâmetros, o XGBoost apresentou desempenho semelhante ao modelo inicial, não superando a Regressão Linear.


## Principais conclusões

- A Regressão Linear apresentou o melhor desempenho entre os modelos avaliados.
- A transformação logarítmica contribuiu para melhorar a relação entre as variáveis e o preço dos imóveis.
- Modelos mais complexos não produziram ganhos significativos para este conjunto de dados.
- O conjunto de dados apresentou boa qualidade, sem valores ausentes e com poucas necessidades de tratamento.


## Possíveis melhorias

- Utilizar uma base de dados maior.
- Incorporar informações geográficas mais detalhadas.
- Testar novos algoritmos de regressão.
- Explorar técnicas adicionais de engenharia de atributos.
- Comparar os modelos com e sem transformação logarítmica.
- Realizar otimização mais abrangente dos hiperparâmetros.


## Autor

Henrique Nunes


## Licença

Este projeto foi desenvolvido exclusivamente para fins acadêmicos.
