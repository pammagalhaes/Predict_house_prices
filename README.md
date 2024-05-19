# 1.Business Problem
Com 79 variáveis explicativas que descrevem (quase) todos os aspectos das residências em Ames, Iowa, o desafio desse projeto foi prever o preço final de cada casa.

# 2.Context Analysis
- **SalePrice**: o preço de venda da propriedade em dólares. Esta é a variável alvo que você está tentando prever.
- **MSSubClass**: a classe do edifício.
- **MSZoning**: a classificação geral de zoneamento.
- **LotFrontage**: metros lineares de rua conectados à propriedade.
- **LotArea**: tamanho do lote em pés quadrados.
- **Street**: tipo de acesso à estrada.
- **Alley**: tipo de acesso ao beco.
- **LotShape**: forma geral da propriedade.
- **LandContour**: planicidade da propriedade.
- **Utilities**: tipo de utilidades disponíveis.
- **LotConfig**: configuração do lote.
- **LandSlope**: inclinação da propriedade.
- **Neighborhood**: localizações físicas dentro dos limites da cidade de Ames.
- **Condition1**: proximidade à estrada principal ou ferrovia.
- **Condition2**: proximidade à estrada principal ou ferrovia (se houver uma segunda).
- **BldgType**: tipo de habitação.
- **HouseStyle**: estilo da habitação.
- **OverallQual**: qualidade geral do material e acabamento.
- **OverallCond**: avaliação geral das condições.
- **YearBuilt**: data de construção original.
- **YearRemodAdd**: data da reforma.
- **RoofStyle**: tipo de telhado.
- **RoofMatl**: material do telhado.
- **Exterior1st**: revestimento exterior da casa.
- **Exterior2nd**: revestimento exterior da casa (se houver mais de um material).
- **MasVnrType**: tipo de revestimento de alvenaria.
- **MasVnrArea**: área do revestimento de alvenaria em pés quadrados.
- **ExterQual**: qualidade do material exterior.
- **ExterCond**: condição atual do material exterior.
- **Foundation**: tipo de fundação.
- **BsmtQual**: altura do porão.
- **BsmtCond**: condição geral do porão.
- **BsmtExposure**: paredes do porão walkout ou garden level.
- **BsmtFinType1**: qualidade da área acabada do porão.
- **BsmtFinSF1**: tipo 1 de área acabada em pés quadrados.
- **BsmtFinType2**: qualidade da segunda área acabada (se houver).
- **BsmtFinSF2**: tipo 2 de área acabada em pés quadrados.
- **BsmtUnfSF**: área não acabada do porão em pés quadrados.
- **TotalBsmtSF**: área total do porão em pés quadrados.
- **Heating**: tipo de aquecimento.
- **HeatingQC**: qualidade e condição do aquecimento.
- **CentralAir**: ar condicionado central.
- **Electrical**: sistema elétrico.
- **1stFlrSF**: área do primeiro andar em pés quadrados.
- **2ndFlrSF**: área do segundo andar em pés quadrados.
- **LowQualFinSF**: área acabada de baixa qualidade (todos os andares).
- **GrLivArea**: área habitável acima do solo em pés quadrados.
- **BsmtFullBath**: banheiros completos no porão.
- **BsmtHalfBath**: banheiros de meio no porão.
- **FullBath**: banheiros completos acima do solo.
- **HalfBath**: banheiros de meio acima do solo.
- **Bedroom**: número de quartos acima do nível do porão.
- **Kitchen**: número de cozinhas.
- **KitchenQual**: qualidade da cozinha.
- **TotRmsAbvGrd**: total de quartos acima do solo (não inclui banheiros).
- **Functional**: avaliação da funcionalidade da casa.
- **Fireplaces**: número de lareiras.
- **FireplaceQu**: qualidade da lareira.
- **GarageType**: localização da garagem.
- **GarageYrBlt**: ano de construção da garagem.
- **GarageFinish**: acabamento interior da garagem.
- **GarageCars**: capacidade da garagem em número de carros.
- **GarageArea**: área da garagem em pés quadrados.
- **GarageQual**: qualidade da garagem.
- **GarageCond**: condição da garagem.
- **PavedDrive**: entrada pavimentada.
- **WoodDeckSF**: área do deck de madeira em pés quadrados.
- **OpenPorchSF**: área da varanda aberta em pés quadrados.
- **EnclosedPorch**: área da varanda fechada em pés quadrados.
- **3SsnPorch**: área da varanda de três estações em pés quadrados.
- **ScreenPorch**: área da varanda com tela em pés quadrados.
- **PoolArea**: área da piscina em pés quadrados.
- **PoolQC**: qualidade da piscina.
- **Fence**: qualidade da cerca.
- **MiscFeature**: característica miscelânea não coberta em outras categorias.
- **MiscVal**: valor em dólares da característica miscelânea.
- **MoSold**: mês de venda.
- **YrSold**: ano de venda.
- **SaleType**: tipo de venda.
- **SaleCondition**: condição de venda.

# 3. Solution Strategy
Para este projeto, o método CRISP-DM foi utilizado, contando com os 10 passos abaixo: 

1 - Problema de Negócio: Identificar o problema de negócio a ser solucionado;

2 - Entendimento do Problema de Negócio: Compreender a motivação, a causa e propor a estratégia de solução para este problema.

3 - Coleta de Dados: Os dados foram obtidos através do Kaggle. (House Prices - Advanced Regression Techniques)

4 - Limpeza dos Dados: Consiste em renomear colunas, converter as variáveis para seus tipos corretos, verificar e preencher NA´s quando necessário, seguindo as motivações do negócio, além de fornecer um breve resumo descritivo dos dados.

5 - Exploração dos Dados: Esta etapa busca analisar e compreender as variáveis que impactam a variável resposta do projeto. Também ocorre a filtragem de variáveis, de acordo com a problemática de negócio. Aqui também são validadas as hipóteses de negócio com a utilização de análise univariada, bivariada e multivariada, o que acarreta na geração de insights.

6 - Modelagem dos Dados: Esta etapa é fundamental para preparar os dados conforme os requisitos dos algoritmos de Machine Learning. Aqui, são realizadas Rescaling e Encoding, com o objetivo de padronizar os dados em uma mesma escala, além de converter variáveis categóricas em numéricas.

7 - Seleção de Features: Esta etapa do projeto filtra as features mais relevantes para o treinamento de Machine Learning que vem a seguir. Não é interessante para o projeto ter um número muito grande de colunas que não impactam na explicação do problema estudado.

8 - Machine Learning: Em seguida, os dados preparados são treinados em diversos algoritmos de Machine Learning, a fim de obter o melhor modelo para explicar o fenômeno. Antes da escolha final, nesta etapa também é realizado o processo de Cross-Validation (validação cruzada) visando impedir que o modelo esteja enviesado, devido a uma separação específica para os dados de validação. Realizados esses procedimentos, aplica-se o Hyperparameter Fine Tuning para o modelo que apresentar melhor resultado, encontrando os melhores parâmetros para o algoritmo e maximizando ainda mais a performance do modelo.

9 - Avaliação do Algoritmo: Aqui, avalia-se o algoritmo com os dados de teste previamente separados, de acordo com métricas alinhadas ao tipo de aprendizado dos modelos de Machine Learning. Ao final, a parte mais importante: traduzir a performance do algoritmo para resultados em termos de negócio e receitas para a empresa e mostrar a diferença, além do impacto que a utilização das técnicas trabalhadas aqui proporcionam para o desenvolvimento da empresa.

10 - Modelo em Produção: Por fim, o modelo avaliado é publicado (Deploy).

# 4. Top 3 Insights
### H1 - O momento da venda pode afetar os preços, com possíveis variações sazonais.
![sales](https://github.com/pammagalhaes/Predict_house_prices/assets/113152370/fc1b864e-a522-4360-8fa3-eb802f8b550a)
**True** - Realmente há meses em que há mais vendas que outros meses, e nesses meses com mais vendas houve redução de preço.

### H2 - Data de construção original (YearBuilt). Quanto mais antigo mais barato o imóvel.
![age](https://github.com/pammagalhaes/Predict_house_prices/assets/113152370/8b84dbed-755c-4a67-86f6-1657e46e657f)
**True** - A idade do imóvel influencia no preço de venda.

### H3 - Propriedades com lotes maiores tendem a ter preços mais altos devido ao espaço adicional e potencial para expansão.
![shape](https://github.com/pammagalhaes/Predict_house_prices/assets/113152370/c0395056-d746-4188-8adb-b8e29f653696)
**False** - A maioria  dos lotes tem um tamanho parecido, e o preço do imóvel pode ser mais alto devido a outros fatores.

# 5. Machine Learning Model
Após a preparação dos dados, foram desenvolvidos e treinados dois modelos de Aprendizado de Máquina para identificar o algoritmo mais eficaz em descrever e resolver o problema proposto:

**LightGBM**

**XGBoost Regressor**

Cada modelo foi treinado e avaliado usando métricas como **MAE**, **MAPE** e **RMSE**. Além disso, foi realizado o processo de Cross-Validation (validação cruzada) nesta etapa para garantir que os modelos não apresentassem viés devido à separação específica dos dados de validação.

O modelo final escolhido foi o **XGBoost Regressor**, devido a um bom desempenho na análise das métricas e por ter um processamento mais leve que os modelos de árvore.

# 6. Resultado do modelo
<img width="365" alt="image" src="https://github.com/pammagalhaes/Predict_house_prices/assets/113152370/341bfda5-9660-4082-b896-dfd1073123bb">
Esse modelo de regressão para previsão de preços de casas obteve um MAPE (Erro Percentual Absoluto Médio) de 9,77%. Isso significa que, em média, as previsões do modelo desviam-se dos valores reais em aproximadamente 9,77%. No contexto de negociações imobiliárias, um MAPE de 9,77% indica que o modelo é relativamente preciso, mas ainda há margem para melhorias. 
