# 1.Business Problem
Com 79 variáveis explicativas que descrevem (quase) todos os aspectos das residências em Ames, Iowa, o desafio desse projeto foi prever o preço final de cada casa.

# 2.Context Analysis
SalePrice - the property's sale price in dollars. This is the target variable that you're trying to predict.
MSSubClass: The building class
MSZoning: The general zoning classification
LotFrontage: Linear feet of street connected to property
LotArea: Lot size in square feet
Street: Type of road access
Alley: Type of alley access
LotShape: General shape of property
LandContour: Flatness of the property
Utilities: Type of utilities available
LotConfig: Lot configuration
LandSlope: Slope of property
Neighborhood: Physical locations within Ames city limits
Condition1: Proximity to main road or railroad
Condition2: Proximity to main road or railroad (if a second is present)
BldgType: Type of dwelling
HouseStyle: Style of dwelling
OverallQual: Overall material and finish quality
OverallCond: Overall condition rating
YearBuilt: Original construction date
YearRemodAdd: Remodel date
RoofStyle: Type of roof
RoofMatl: Roof material
Exterior1st: Exterior covering on house
Exterior2nd: Exterior covering on house (if more than one material)
MasVnrType: Masonry veneer type
MasVnrArea: Masonry veneer area in square feet
ExterQual: Exterior material quality
ExterCond: Present condition of the material on the exterior
Foundation: Type of foundation
BsmtQual: Height of the basement
BsmtCond: General condition of the basement
BsmtExposure: Walkout or garden level basement walls
BsmtFinType1: Quality of basement finished area
BsmtFinSF1: Type 1 finished square feet
BsmtFinType2: Quality of second finished area (if present)
BsmtFinSF2: Type 2 finished square feet
BsmtUnfSF: Unfinished square feet of basement area
TotalBsmtSF: Total square feet of basement area
Heating: Type of heating
HeatingQC: Heating quality and condition
CentralAir: Central air conditioning
Electrical: Electrical system
1stFlrSF: First Floor square feet
2ndFlrSF: Second floor square feet
LowQualFinSF: Low quality finished square feet (all floors)
GrLivArea: Above grade (ground) living area square feet
BsmtFullBath: Basement full bathrooms
BsmtHalfBath: Basement half bathrooms
FullBath: Full bathrooms above grade
HalfBath: Half baths above grade
Bedroom: Number of bedrooms above basement level
Kitchen: Number of kitchens
KitchenQual: Kitchen quality
TotRmsAbvGrd: Total rooms above grade (does not include bathrooms)
Functional: Home functionality rating
Fireplaces: Number of fireplaces
FireplaceQu: Fireplace quality
GarageType: Garage location
GarageYrBlt: Year garage was built
GarageFinish: Interior finish of the garage
GarageCars: Size of garage in car capacity
GarageArea: Size of garage in square feet
GarageQual: Garage quality
GarageCond: Garage condition
PavedDrive: Paved driveway
WoodDeckSF: Wood deck area in square feet
OpenPorchSF: Open porch area in square feet
EnclosedPorch: Enclosed porch area in square feet
3SsnPorch: Three season porch area in square feet
ScreenPorch: Screen porch area in square feet
PoolArea: Pool area in square feet
PoolQC: Pool quality
Fence: Fence quality
MiscFeature: Miscellaneous feature not covered in other categories
MiscVal: $Value of miscellaneous feature
MoSold: Month Sold
YrSold: Year Sold
SaleType: Type of sale
SaleCondition: Condition of sale

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
**True** Realmente há meses em que há mais vendas que outros meses, e nesses meses com mais vendas houve redução de preço.

### H2 - Data de construção original (YearBuilt). Quanto mais antigo mais barato o imóvel.
![age](https://github.com/pammagalhaes/Predict_house_prices/assets/113152370/8b84dbed-755c-4a67-86f6-1657e46e657f)
**True** A idade do imóvel influencia no preço de venda.

### H3 - Propriedades com lotes maiores tendem a ter preços mais altos devido ao espaço adicional e potencial para expansão.
![shape](https://github.com/pammagalhaes/Predict_house_prices/assets/113152370/c0395056-d746-4188-8adb-b8e29f653696)
**False** - A maioria  dos lotes tem um tamanho parecido, e o preço do imóvel pode ser mais alto devido a outros fatores.


