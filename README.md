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

Grupo	Variáveis

Identificação e perfil	ID do cliente, gênero, idade avançada, estado civil e dependentes

Relacionamento	Tempo como cliente

Serviços contratados	Telefone, internet, segurança, suporte técnico e StreamingTV

Contrato e pagamento	Tipo de contrato e método de pagamento

Informações financeiras	Pagamento mensal e total pago

Variável preditora	Churn

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

Base inicial: 2.500 registros.

- Base após exclusão dos registros com dados ausentes em Gênero e Churn: 2.488 registros.
- Dados ausentes em Pagamento_Mensal: 320 registros, tratados com a mediana de 71,45.
- Dados ausentes em PhoneService: aproximadamente 59,4%, preenchidos com "No".
- Valores ausentes restantes após o tratamento: zero.

## 💡 Principais Insights e Implicações

A análise permitiu identificar alguns padrões relevantes:

#### *Tipo de contrato:* clientes com contratos mensais (month-to-month) apresentam maior concentração de cancelamentos. Contratos de um ou dois anos aparecem associados a uma maior permanência.

#### *Tempo de relacionamento:* clientes que cancelaram apresentam menor tempo de relacionamento com a empresa, sugerindo que os primeiros períodos da relação comercial merecem atenção.

#### *Total pago:* clientes que permaneceram apresentam valores de Total_Pago geralmente mais elevados do que aqueles que cancelaram.

#### *Idade:* a análise aponta uma proporção maior de cancelamentos entre clientes idosos, embora esse grupo represente apenas 16,16% da base.

#### *Método de pagamento:* o notebook destaca o pagamento por Electronic Check, registrando uma associação de 58,42% com o Churn, embora não deixe suficientemente claro o denominador dessa porcentagem.

#### *Serviços contratados:* tipo de internet e contratação de serviços adicionais, como StreamingTV, foram investigados como possíveis fatores relacionados à permanência dos clientes.

#### *Implicações para o negócio:* esses resultados podem orientar estratégias de retenção, acompanhamento de clientes novos, revisão de contratos e investigação de padrões de cancelamento por tipo de serviço e pagamento.

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

Grupo	Variáveis

Identificação e perfil	ID do cliente, gênero, idade avançada, estado civil e dependentes

Relacionamento	Tempo como cliente

Serviços contratados	Telefone, internet, segurança, suporte técnico e StreamingTV

Contrato e pagamento	Tipo de contrato e método de pagamento

Informações financeiras	Pagamento mensal e total pago

Variável preditora	Churn

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

## 💡 Principais Insights e Implicações



# Projeto Pré-processamento etapa 03
<img width="1200" height="896" alt="credit score" src="https://github.com/user-attachments/assets/72b49d84-f550-4084-95b9-dd5fd144c951" />

## 📌 Sobre o Projeto

## 🎯 Objetivo

## 💻​ Problema de Negócio / Pergunta de Pesquisa

## 📊 Fonte de Dados

## 🛠️ LINGUAGENS E BIBLIOTECAS

## 🔍 Metodologia

## 📈  Resultados e Métricas

## 💡 Principais Insights e Implicações


## 👩‍💻 Sobre a Autora

Desenvolvido por Marina Napoleão — Cientista de Dados / Analista de Dados. 
### LinkedIn <https://www.linkedin.com/in/marina-napoleao/>
### GitHub <https://github.com/marinanapoleao> 
