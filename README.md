# Projeto Pré-processamento etapa 01
<img width="1408" height="768" alt="etapa 1 pre modelagem" src="https://github.com/user-attachments/assets/c5be0f95-3b13-44a1-a040-fc2968e22c1c" />

## 📌 Sobre o Projeto
Projeto de análise exploratória e pré-processamento de dados de clientes de uma empresa de telecomunicações que oferece serviços de internet, telefone e TV.

O trabalho busca compreender o comportamento dos clientes, identificar características associadas ao cancelamento dos serviços (Churn) e preparar a base de dados para uma possível etapa futura de modelagem preditiva.

O projeto foi desenvolvido em duas etapas: limpeza e tratamento dos dados, seguidos de análise exploratória univariada e bivariada.

## 🎯 Objetivo

Analisar o comportamento dos clientes e identificar padrões e características que podem estar relacionados ao cancelamento dos serviços, preparando os dados para uma futura construção de um modelo de previsão de Churn.

## 💻​ Problema de Negócio / Pergunta de Pesquisa

O principal problema de negócio é compreender quais características dos clientes e dos serviços contratados estão associadas ao cancelamento.

As principais perguntas investigadas foram:
- Existe relação entre o estado civil e o cancelamento?

- O tipo de serviço de internet influencia o Churn?

- Clientes que contratam StreamingTV apresentam comportamento diferente?

- O tipo de contrato está relacionado à permanência do cliente?

- Existe associação entre o método de pagamento e o cancelamento?

- O tempo de relacionamento e o valor pago influenciam a permanência dos clientes?

## 📊 Fonte de Dados

Base de dados: CHURN_TELECON_MOD08_TAREFA.csv.

A base inicial apresenta 2.500 registros e 16 colunas, com informações sobre:

Grupo —————————————— Variáveis

Identificação e perfil ———————— ID do cliente, gênero, idade avançada, estado civil e dependentes

Relacionamento —————————— Tempo como cliente

Serviços contratados ———————— Telefone, internet, segurança, suporte técnico e StreamingTV

Contrato e pagamento ——————— Tipo de contrato e método de pagamento

Informações financeiras ——————— Pagamento mensal e total pago

Variável preditora —————————— Churn

## 🛠️ LINGUAGENS E BIBLIOTECAS

- Python: linguagem de programação.

- Pandas: manipulação, limpeza e tratamento dos dados.

- NumPy: operações e manipulação numérica.

- Matplotlib: visualização de dados.

- Seaborn: construção de gráficos estatísticos.

- Plotly Express: visualizações interativas.

## 🔍 Metodologia

*Etapa 1 — Pré-processamento e limpeza dos dados*

- Importação e análise dos tipos de dados.

- Identificação e tratamento de valores ausentes.

- Conversão da variável Idoso para tipo booleano.

- Exclusão de 5 registros sem informação na variável Churn.

- Exclusão de 7 registros sem informação na variável Gênero.

- Preenchimento dos valores ausentes de Pagamento_Mensal utilizando a mediana (71,45).

- Preenchimento dos valores ausentes de PhoneService com a categoria "No", considerando a interpretação adotada no exercício.

- Padronização dos valores categóricos, incluindo letras maiúsculas, minúsculas e diferenças de escrita.

- Padronização dos nomes das colunas.

## 📈  Resultados e Métricas

*Tratamento dos registros*

Indicador ———————————————————————— Resultado

Registros iniciais ————————————————————— 2.500

Registros sem informação de Churn excluídos ———————— 5

Registros sem informação de gênero excluídos ——————— 7

Registros finais ————————————————————— 2.488

Colunas analisadas ——————————————————— 16

Valores ausentes após tratamento ————————————— 0


*Tratamento dos valores ausentes*

Variável ———————— Valores ausentes ——————— Percentual —————— Tratamento

Gênero —————————————— 7 ———————— 0,28% ————————— Exclusão dos registros

Pagamento mensal ———————— 320 ———————— 12,83% ———————— Imputação pela mediana

Serviço telefônico ———————— 1.482 ———————— 59,40% ———————— Preenchimento com "No"

Churn —————————————— 5 ————————— 0,20% ———————— Exclusão dos registros

Indicadores da imputação:
- Pagamento mensal: média de R$ 65,61.
- Pagamento mensal: mediana de R$ 71,45.
- Mediana utilizada para preenchimento: R$ 71,45.
- Valores ausentes após imputação: zero.

Padronização e transformação:
- Conversão da variável Idoso de inteiro para booleano.
- Padronização das categorias de gênero, internet e demais variáveis categóricas.
- Conversão dos valores de texto para letras minúsculas.
- Padronização dos nomes das colunas para português.
- Adequação dos tipos de dados das variáveis numéricas.


## 💡 Principais Insights e Implicações

#### *Qualidade e consistência dos dados:* a base inicial apresentava inconsistências de preenchimento, diferentes padrões de escrita e valores ausentes em três variáveis importantes. Após o tratamento, foi possível obter uma base consistente, sem valores ausentes.

#### *Preservação dos registros:* a variável Gênero apresentava apenas 0,28% de valores ausentes. A exclusão desses registros foi uma alternativa para preservar a qualidade da variável sem comprometer significativamente o tamanho da base.

#### *Tratamento de variáveis numéricas:* a utilização da mediana no Pagamento_Mensal permitiu preencher os valores ausentes utilizando uma medida menos sensível a valores extremos.

#### *Tratamento de variáveis categóricas:* a substituição dos valores ausentes de PhoneService pela categoria "No" foi adotada considerando a interpretação de que os registros ausentes representavam clientes sem serviço telefônico. Entretanto, como essa variável apresentava aproximadamente 59,4% de valores ausentes, essa premissa merece validação antes de utilizar os dados em análises mais aprofundadas.

#### *Preparação para análises futuras:* a padronização e a limpeza dos dados possibilitaram a criação de uma base estruturada, adequada para análises exploratórias e futuras etapas de modelagem preditiva.

# Projeto Pré-processamento etapa 02
<img width="1408" height="768" alt="etapa 2 pre modelagem" src="https://github.com/user-attachments/assets/08f35381-3147-4a91-9185-8bffa2167c28" />

## 📌 Sobre o Projeto

Projeto de análise exploratória e pré-processamento de dados de clientes de uma empresa de telecomunicações que oferece serviços de internet, telefone e TV.

## 🎯 Objetivo

Analisar o comportamento dos clientes e identificar padrões e características que podem estar relacionados ao cancelamento dos serviços, preparando os dados para uma futura construção de um modelo de previsão de Churn.

## 💻​ Problema de Negócio / Pergunta de Pesquisa

O principal problema de negócio é compreender quais características dos clientes e dos serviços contratados estão associadas ao cancelamento.

As principais perguntas investigadas foram:
- Existe relação entre o estado civil e o cancelamento?

- O tipo de serviço de internet influencia o Churn?

- Clientes que contratam StreamingTV apresentam comportamento diferente?

- O tipo de contrato está relacionado à permanência do cliente?

- Existe associação entre o método de pagamento e o cancelamento?

- O tempo de relacionamento e o valor pago influenciam a permanência dos clientes?

## 📊 Fonte de Dados

Base de dados: CHURN_TELECON_MOD08_TAREFA.csv.

A base inicial apresenta 2.500 registros e 16 colunas, com informações sobre:

Grupo —————————————— Variáveis

Identificação e perfil ———————— ID do cliente, gênero, idade avançada, estado civil e dependentes

Relacionamento —————————— Tempo como cliente

Serviços contratados ———————— Telefone, internet, segurança, suporte técnico e StreamingTV

Contrato e pagamento ——————— Tipo de contrato e método de pagamento

Informações financeiras ——————— Pagamento mensal e total pago

Variável preditora —————————— Churn

## 🛠️ LINGUAGENS E BIBLIOTECAS

- Python: linguagem de programação.

- Pandas: manipulação, limpeza e tratamento dos dados.

- NumPy: operações e manipulação numérica.

- Matplotlib: visualização de dados.

- Seaborn: construção de gráficos estatísticos.

- Plotly Express: visualizações interativas.

## 🔍 Metodologia

Etapa 2 — Análise exploratória dos dados
- Análise univariada utilizando estatísticas descritivas.
- Construção de histogramas e boxplots.
- Identificação de possíveis outliers utilizando o método do intervalo interquartil (IQR).
- Análise da distribuição das variáveis booleanas e identificação de desbalanceamentos.
- Análise bivariada por meio de gráficos de barras empilhadas e comparações entre Churn e características dos clientes.
- Investigação das relações entre Churn, tipo de contrato, serviços contratados, estado civil e método de pagamento.
  
## 📈  Resultados e Métricas

Qualidade da base

- Registros analisados: 2.488.
- Colunas: 16.
- Valores ausentes: zero.
- Base sem necessidade de novos tratamentos de valores ausentes.


*Estatísticas descritivas*

Indicador  ————————————	 Média   |	Mediana |	Mínimo |	Máximo

Tempo como cliente (meses)  ————	32,35   |	 0029     |	 0000	  | 0072

Pagamento mensal  ———————— 66,34	 |   71,45	| 18,40	| 118,65

Total pago  ———————————	2.290,09 | 1.402,90 |	18,80 |	8.564,75


*Distribuição das variáveis booleanas*

Variável  —————	Categoria predominante  —————	Percentual

Gênero  ——————	Masculino  ——————————	51,00%

Idoso  ———————	Não  ————————————	83,84%

Casado  ——————	Não  ————————————	50,72%

Dependentes  ———	Não	 ———————————— 68,53%

Serviço telefônico  —	Não  ————————————	63,02%

*Análise de outliers*

Foi utilizado o método do Intervalo Interquartil (IQR) e a visualização por boxplots para investigar possíveis valores extremos.

Nenhum valor observado ultrapassou os limites calculados. Portanto, não foi identificada necessidade de exclusão de outliers nessas três variáveis.

Também foram identificados cinco clientes com tempo de relacionamento igual a zero, correspondendo a aproximadamente 0,20% da base.

*Análise bivariada*

Foram desenvolvidas visualizações para investigar as relações entre Churn e cinco variáveis:

1. Estado civil.
2. Tipo de serviço de internet.
3. Contratação de StreamingTV.
4. Tipo de contrato.
5. Método de pagamento.

Também foram elaborados gráficos para comparar Churn com Total_Pago, Tempo_como_Cliente e Idoso.

## 💡 Principais Insights e Implicações

#### *1. Tipo de contrato e cancelamento:* Clientes com contratos mensais (month-to-month) apresentam maior concentração de cancelamentos. Já os contratos anuais e bienais aparecem associados a uma maior permanência.

Implicação para o negócio: investigar estratégias para incentivar a adesão a contratos de maior duração e reduzir a rotatividade de clientes com contratos mensais.

#### *2. Tempo de relacionamento e permanência:* A análise dos boxplots sugere que clientes que cancelaram os serviços apresentam menor tempo de relacionamento com a empresa. O comentário do notebook também aponta uma mediana de tempo menor para esse grupo.

Implicação para o negócio: desenvolver estratégias de acompanhamento e retenção durante os primeiros meses do relacionamento com os clientes.

#### *3. Total pago e Churn:* Clientes que permaneceram apresentam valores de Total_Pago geralmente mais elevados e maior variação nesses valores. Clientes que cancelaram apresentam valores menores e menor dispersão.

Implicação para o negócio: investigar a relação entre tempo de permanência, valor acumulado pago e cancelamento, buscando identificar clientes que apresentam maior risco de evasão.

#### *4. Idade e cancelamento:* A base apresenta 16,16% de clientes idosos. A análise registrada no notebook aponta uma participação maior de idosos entre os clientes que cancelaram.

Implicação para o negócio: investigar possíveis diferenças de comportamento e necessidades entre os grupos etários para orientar ações de relacionamento e atendimento.

Observação: o gráfico utilizado compara a composição etária dentro de cada grupo de Churn. Isso, isoladamente, não comprova que clientes idosos tenham maior probabilidade individual de cancelar.

#### *5. Método de pagamento e cancelamento:* O notebook identifica o método Electronic Check como associado a 58,42% em relação ao Churn.

Implicação para o negócio: investigar o comportamento dos clientes que utilizam essa modalidade de pagamento e verificar se existem diferenças nas taxas de cancelamento entre os métodos disponíveis.

Observação: o denominador dessa porcentagem não está explicitado no notebook, portanto o percentual precisa ser validado antes de ser utilizado como indicador definitivo.

#### *6. Tipo de internet e comportamento dos clientes:* 
A análise considera o tipo de internet contratada, especialmente fibra óptica, como possível fator relacionado à insatisfação e ao cancelamento.

Implicação para o negócio: investigar diferenças de experiência e satisfação entre clientes de DSL e fibra óptica, verificando possíveis oportunidades de melhoria nos serviços.

#### *7. Serviços adicionais e engajamento:* A contratação de StreamingTV foi investigada como possível característica relacionada ao comportamento de permanência. O notebook levanta a hipótese de que clientes com mais serviços contratados podem apresentar maior engajamento.

Implicação para o negócio: avaliar a relação entre contratação de serviços adicionais, engajamento e permanência dos clientes.

#### *8. Estado civil e cancelamento:* O estado civil foi considerado uma variável relevante por representar características do perfil dos clientes e possíveis diferenças de comportamento.

Implicação para o negócio: investigar se existem diferenças consistentes nas taxas de cancelamento entre clientes casados e não casados.

## ⚠️ Observações 
Principais variáveis apontadas como relevantes para estudar o Churn:

O próprio notebook destaca cinco variáveis como importantes para futuras investigações:

- Estado civil (Casado).
- Tipo de serviço de internet.
- StreamingTV.
- Tipo de contrato.
- Método de pagamento.

Essas variáveis abrangem características pessoais, contratuais e de consumo, oferecendo diferentes perspectivas para compreender o comportamento dos clientes.

# Projeto Pré-processamento etapa 03
<img width="1200" height="896" alt="credit score" src="https://github.com/user-attachments/assets/72b49d84-f550-4084-95b9-dd5fd144c951" />

## 📌 Sobre o Projeto

Projeto de análise exploratória e pré-processamento de dados voltado à preparação de uma base de informações financeiras e demográficas para o desenvolvimento de um modelo de classificação de Score de Crédito.

O trabalho investiga como características pessoais, socioeconômicas e financeiras dos clientes se relacionam com as categorias de score: alto (High), médio (Average) e baixo (Low).

A proposta é preparar os dados para uma futura aplicação de Machine Learning na avaliação de risco de crédito.

## 🎯 Objetivo

Preparar e analisar uma base de dados de clientes para uma futura construção de um modelo de classificação capaz de identificar a categoria de Score de Crédito, utilizando características como idade, renda, escolaridade, estado civil, quantidade de filhos e tipo de residência.

## 💻​ Problema de Negócio / Pergunta de Pesquisa

O problema de negócio está relacionado à avaliação de risco de crédito e à necessidade de compreender o perfil dos clientes de acordo com sua classificação de crédito.

*É possível identificar padrões nas características pessoais e financeiras dos clientes que estejam relacionados à classificação de seus scores de crédito?*

As perguntas investigadas incluem:
- Existe relação entre idade e estado civil?
- Qual a relação entre score de crédito e nível de escolaridade?
- A renda apresenta relação com a idade?
- A renda apresenta relação com o score de crédito?
- Clientes que possuem casa própria tendem a apresentar score mais elevado?
- Existe diferença no score de crédito entre homens e mulheres?
- A quantidade de filhos está relacionada ao score e à renda dos clientes?
  
## 📊 Fonte de Dados

Base de dados: CREDIT_SCORE_PROJETO_PARTE1.csv.

A base apresenta 164 registros e 8 colunas.

Variável ————— Descrição

Age ————— Idade dos clientes

Gender —————	Gênero

Income —————	Renda mensal

Education —————	Nível de escolaridade

Marital Status —————	Estado civil

Number of Children —————	Quantidade de filhos

Home Ownership —————	Tipo de residência: própria ou alugada

Credit Score —————	Classificação do score de crédito

## 🛠️ LINGUAGENS E BIBLIOTECAS

Python: linguagem de programação.

- Pandas: manipulação e tratamento dos dados.
- NumPy: operações numéricas.
- Matplotlib: visualização gráfica.
- Seaborn: análise e visualização estatística.
- Plotly Express: gráficos interativos.
- Scikit-learn: Label Encoding e divisão entre treino e teste.
- Imbalanced-learn: aplicação do SMOTE para balanceamento das classes.
- SciPy: biblioteca importada no ambiente do projeto.

## 🔍 Metodologia

*Etapa 1 — Pré-processamento*
- Importação e análise dos tipos de dados.
- Conversão da variável Income de texto para formato numérico.
- Identificação de valores ausentes.
- Preenchimento dos dados faltantes da variável Age utilizando a mediana (36 anos).
- Padronização das variáveis categóricas, convertendo os textos para letras minúsculas.
- Verificação da consistência dos dados.

*Etapa 2 — Análise exploratória*
- Análise univariada das variáveis numéricas e categóricas.
- Construção de gráficos de distribuição e boxplots.
- Investigação de possíveis outliers.
- Análise bivariada para investigar relações entre idade, renda, escolaridade, estado civil, residência, quantidade de filhos e score de crédito.
- Análise das distribuições das categorias de score.

*Etapa 3 — Preparação para modelagem*
- Análise de correlação entre variáveis numéricas.
- Aplicação de Label Encoding nas variáveis Gender, Marital Status e Home Ownership.
- Aplicação de One-Hot Encoding nas variáveis Education e Credit Score.
- Conversão de variáveis booleanas para formato numérico.
- Análise de correlação após a transformação das variáveis categóricas.
- Separação dos dados em treino e teste.
- Verificação do balanceamento das classes.
- Aplicação do SMOTE somente nos dados de treinamento.
- Exportação das bases balanceadas e de teste em arquivos CSV.

## 📈  Resultados e Métricas

Registros iniciais: 164.

Coluna Age: 34 valores ausentes, correspondentes a 20,73% da base.

Mediana da idade utilizada na imputação: 36 anos.

Após o tratamento, a base permaneceu com 164 registros.

Variável Income convertida para formato numérico.

*ESTATÍSTICAS DESCRITIVAS*

Indicador ——————— Média ——————— Mediana

Idade ————————— 37,20 ——————— 36

Renda mensal ————— 83.765,24 —————— 83.750

Quantidade de filhos —— 0,65 ———————— 0

Outros resultados:
- Idade mínima: 25 anos.
- Idade máxima: 53 anos.
- Renda mínima: 25.000.
- Renda máxima: 162.500.
- 59,15% dos clientes não possuem filhos.

A correlação entre idade e renda foi de 0,6215, indicando uma relação positiva moderada a relativamente forte entre as variáveis.

A análise sugere que, nessa amostra, clientes mais velhos tendem a apresentar rendas mais elevadas.

*DISTRIBUIÇÃO DO SCORE DE CRÉDITO*

Categoria ——————— Percentual

Score alto ——————— 68,90%

Score médio —————— 21,95%

Score baixo —————— 9,15%

O score baixo apresenta maior desbalanceamento, pois apenas 9,15% dos registros pertencem a essa categoria.

*DIVISÃO TREINO E TESTE*
- Treinamento: 123 registros (75%).
- Teste: 41 registros (25%).
- Foram criadas duas tarefas binárias: classificação de score alto e classificação de score baixo.

*BALANCEAMENTO COM SMOTE*

Classificação ———— Classe 0 ——— Classe 1

Score alto —————— 84 —————— 84

Score baixo ————— 114 —————— 114

O SMOTE foi aplicado somente às bases de treinamento, equilibrando a quantidade de registros entre as classes de cada tarefa.

## 💡 Principais Insights e Implicações

#### *Renda e score de crédito:* clientes com renda inferior a 40 mil aparecem associados ao score baixo. Clientes com renda entre 40 mil e 68 mil apresentam maior presença de score médio, enquanto rendas a partir de 80 mil aparecem associadas ao score alto.

#### *Escolaridade:* clientes com mestrado e doutorado apresentam maior participação na categoria de score alto. Já clientes com ensino médio apresentam maior participação na categoria de score baixo.

#### *Idade e estado civil:* a análise identificou uma associação entre idade e estado civil. Até os 33 anos, aproximadamente 80% dos clientes eram solteiros; a partir dos 34 anos, aproximadamente 70% eram casados, segundo os resultados registrados no notebook.

#### *Propriedade residencial:* entre os clientes com imóvel próprio, 98,19% apresentam score alto. Entre os clientes que alugam imóvel, 64,15% apresentam score baixo.

#### *Quantidade de filhos:* clientes sem filhos apresentam maior dispersão entre as categorias de score. Clientes com um ou dois filhos aparecem mais concentrados na categoria de score alto.

#### *Gênero:* homens e mulheres apresentam distribuições semelhantes de score alto. O notebook identifica maior presença masculina no score médio e feminina no score baixo.

#### *Implicações para o negócio:* os resultados podem auxiliar na identificação de padrões socioeconômicos relacionados à classificação de crédito, apoiar análises de risco e orientar a investigação de características relevantes para a construção de modelos preditivos.

## ⚠️ Observações técnicas importantes

1. Tratamento de outliers: a variável Number of Children possui valores de 3 filhos, que ultrapassam o limite superior de 2,5 calculado pelo IQR. Há 5 registros nessa condição (3,05% da base). Entretanto, o código utilizado para contabilizar os outliers apresenta um problema e informa zero. Também não encontrei uma etapa efetiva de tratamento desses registros.

2. Possível vazamento de dados (Data Leakage): na preparação das bases de treino, a variável indicadora de uma categoria de Credit Score permanece entre as variáveis explicativas da outra classificação. Como ambas foram derivadas da própria variável preditora, isso pode fornecer informações sobre a resposta ao futuro modelo. O ideal é retirar as duas variáveis indicadoras de score de X e manter a classificação original separada como variável-alvo.

Também é importante destacar que, embora a introdução do projeto mencione previsão de risco de inadimplência, a variável efetivamente trabalhada é a categoria do score de crédito. São objetivos relacionados, mas não equivalentes.​

## 👩‍💻 Sobre a Autora

Desenvolvido por Marina Napoleão — Cientista de Dados / Analista de Dados. 
### LinkedIn <https://www.linkedin.com/in/marina-napoleao/>
### GitHub <https://github.com/marinanapoleao> 
