# Análise de Dados Demografico

!["imagem da web"](https://cognatis.com.br/wp-content/uploads/2015/11/2022-04-Post-Demografia-banner.jpg)
[Fonte](https://cognatis.com.br/a-importancia-dos-dados-demograficos-para-entender-o-mercado/)

## Objectivos

Esse projecto tem como objectivo o estudo de dados demofraficos de expectativa de vida de uma dada população.

## Descrição do Dataset

1. **Country**: Nome do país (tipo de dado: `object`).
2. **Year**: Ano em que os dados foram coletados (tipo de dado: `int64`).
3. **Status**: Status do país (desenvolvido ou em desenvolvimento) (tipo de dado: `object`).
4. **Life expectancy (men)**: Expectativa de vida dos homens (tipo de dado: `int64`).
5. **Life expectancy (women)**: Expectativa de vida das mulheres (tipo de dado: `int64`).
6. **Adult Mortality (men)**: Taxa de mortalidade adulta masculina (tipo de dado: `int64`).
7. **Adult Mortality (women)**: Taxa de mortalidade adulta feminina (tipo de dado: `int64`).
8. **Infant deaths**: Número de mortes infantis (tipo de dado: `int64`).
9. **Alcohol**: Consumo de álcool per capita (tipo de dado: `float64`).
10. **Percentage expenditure**: Percentual de gastos com saúde em relação ao PIB (tipo de dado: `float64`).
11. **Hepatitis B (men)**: Cobertura de vacinação contra hepatite B em homens (tipo de dado: `int64`).
12. **Hepatitis B (women)**: Cobertura de vacinação contra hepatite B em mulheres (tipo de dado: `int64`).
13. **Measles**: Número de casos de sarampo (tipo de dado: `int64`).
14. **BMI**: Índice de Massa Corporal médio da população (tipo de dado: `float64`).
15. **Under-five deaths**: Número de mortes de crianças menores de cinco anos (tipo de dado: `int64`).
16. **Polio**: Cobertura de vacinação contra poliomielite (tipo de dado: `float64`).
17. **Total expenditure**: Gastos totais com saúde per capita (tipo de dado: `float64`).
18. **Diphtheria**: Cobertura de vacinação contra difteria (tipo de dado: `float64`).
19. **HIV/AIDS**: Taxa de prevalência de HIV/AIDS (tipo de dado: `float64`).
20. **GDP**: Produto Interno Bruto per capita (tipo de dado: `float64`).
21. **Population**: População total (tipo de dado: `float64`).
22. **thinness 1-19 years**: Percentual de magreza em crianças e adolescentes de 1 a 19 anos (tipo de dado: `float64`).
23. **thinness 5-9 years**: Percentual de magreza em crianças de 5 a 9 anos (tipo de dado: `float64`).
24. **Income composition of resources**: Índice de composição de renda (tipo de dado: `float64`).
25. **Schooling**: Média de anos de escolaridade (tipo de dado: `float64`).

Essas colunas fornecem uma visão abrangente sobre a saúde e o desenvolvimento socioeconômico dos países ao longo do tempo.

## Análises passisveis de serem feitas

Uma análise demográfica baseada no seu conjunto de dados envolveria o estudo das características da população representada pelos dados. Aqui estão alguns aspectos que você poderia explorar:

### 1. Distribuição Populacional por País e Ano

Analisar como a população está distribuída entre diferentes países e ao longo dos anos.

### 2. Expectativa de Vida

Comparar a expectativa de vida entre homens e mulheres em diferentes países e anos.

Identificar tendências e mudanças na expectativa de vida ao longo do tempo.

### 3. Mortalidade Adulta e Infantil

Examinar as taxas de mortalidade adulta e infantil para entender os padrões de saúde e mortalidade.

Comparar essas taxas entre diferentes países e ao longo dos anos.

### 4. Status Socioeconômico

Analisar a relação entre o status do país (desenvolvido ou em desenvolvimento) e indicadores de saúde como expectativa de vida, mortalidade e vacinação.

### 5. Vacinação e Doenças

Estudar a cobertura de vacinação contra Hepatite B, Polio e Difteria e sua relação com a mortalidade infantil e adulta.
Analisar a incidência de doenças como sarampo e HIV/AIDS.

### 6. Fatores de Saúde e Nutrição

Explorar a relação entre consumo de álcool, índice de massa corporal (BMI), magreza em diferentes faixas etárias e indicadores de saúde.

Analisar como a composição de renda e escolaridade influenciam a saúde da população.

### 7. Gastos com Saúde

Examinar o percentual de gastos com saúde em relação ao PIB e os gastos totais per capita.

Analisar como esses gastos estão relacionados com a expectativa de vida e a mortalidade.

### Exemplos de Perguntas de Pesquisa

1. Como a expectativa de vida mudou ao longo dos anos em países desenvolvidos versus países em desenvolvimento?
2. Qual é a relação entre a cobertura de vacinação e a mortalidade infantil em diferentes países?
3. Como os gastos com saúde influenciam a expectativa de vida e a mortalidade adulta?

## O Conceito Fato-Dimensão

O Conceito Fato-Dimensão, proposto por Ralph Kimball, é uma abordagem central no design de data warehouse

### Fato

Uma  tabela(planilha) fato armazena dados quantitativos de eventos de negocios, como vendas ou transações. Essas tabelas contêm métricas ou medidas numericas que os analistas desejam analisar. como quantidade de vendas, receita ou duração de uma viagem

### Dimensões

As tabelas de dimensções, por outro lado, armazenam dados qualitativos que descrevem as dimensções dos eventos de negocios. Por exemplo, uma tabela de dimensão pode conter informações sobre o tempo (data, mes, ano) localização (cidade, estado, país).

---

Antes de analisar uma planilha de dados é importante definir o Fato de interesse e identificar as dimenções que as colunas pertencem. O fato vai direcionar o tipo de resposta você espera obter da planilha de dados eas dimensões podem auxiliar na compreensão de como o Fato de interesse pode ser visto por uma ou mais dimensções.

Em resumo, o conceito de fato-dimensão é uma metodologia poderosa para organizar e analisar dados, possibilitando uma visão multidimensional dos dados de negócios.

Aplicando esse conceito nos nossos dados temos:

 | **Fatos**                        |
|----------------------------------|
| Life expectancy (men)            |
| Life expectancy (women)          |
| Adult Mortality (men)            |
| Adult Mortality (women)          |
| Infant deaths                    |
| Alcohol                          |
| Percentage expenditure           |
| Hepatitis B (men)                |
| Hepatitis B (women)              |
| Measles                          |
| BMI                              |
| Under-five deaths                |
| Polio                            |
| Total expenditure                |
| Diphtheria                       |
| HIV/AIDS                         |
| GDP                              |
| Population                       |
| thinness 1-19 years              |
| thinness 5-9 years               |
| Income composition of resources  |
| Schooling                        |
| Country (chave estrangeira)      |
| Year (chave estrangeira)         |
| Status (chave estrangeira)       |

| **Dimensão de Localização** |
|-------------------|
| Country           |

| **Dimensão de Tempo** |
|------------------|
| Year             |

| **Dimensão Status** |
|---------------------|
| Status              |

Com base nisso podemos responder as perguntas e definir que tipo de grafico seria melhor para cada tipo de grafico a ser exibido.
