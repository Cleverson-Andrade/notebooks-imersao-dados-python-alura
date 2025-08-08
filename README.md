# Análise de Salários no Mercado de Dados 📊

Este repositório contém o notebook de análise exploratória de dados sobre salários no mercado de trabalho de dados, usando a biblioteca **Pandas** em Python. O projeto foi dividido em etapas que cobrem desde a importação inicial dos dados até a sua visualização final.

---

## 📝 Jornada de Análise

### **Aula 1: Exploração e Preparação Inicial**

Nesta etapa, o objetivo foi entender a estrutura dos dados. As principais ações realizadas foram:
* **Importação do Dataset:** Carregamento do arquivo CSV usando `pd.read_csv()`.
* **Inspeção dos Dados:** Uso de funções como `df.head()`, `df.info()` e `df.describe()` para ter uma visão geral do dataset, verificar os tipos de dados e encontrar informações estatísticas básicas.
* **Limpeza e Organização:** As colunas foram renomeadas para nomes mais simples e em português (`ano`, `senioridade`, etc.), e os valores categóricos (como a coluna `remoto`) foram traduzidos para facilitar a compreensão.

---

### **Aula 2: Tratamento e Limpeza de Dados**

Aqui, o foco foi na qualidade dos dados. A tarefa principal foi lidar com valores ausentes.
* **Identificação de Nulos:** Utilização de `df.isnull().sum()` para contar a quantidade de valores nulos em cada coluna.
* **Remoção de Nulos:** Os valores nulos na coluna `ano` foram removidos usando o método `df.dropna()`.
* **Ajuste de Tipos:** O tipo de dado da coluna `ano` foi convertido de ponto flutuante (`float64`) para inteiro (`int64`), pois o ano não precisa de casas decimais.

---

### **Aula 3: Visualização dos Dados**

Nesta fase, usamos bibliotecas de visualização para extrair insights.
* **Distribuição de Salários:** Foram criados gráficos como **Histograma** (`sns.histplot`) e **Boxplot** (`sns.boxplot`) para entender como os salários em USD se distribuem e identificar possíveis valores discrepantes (`outliers`).
* **Salário por Senioridade:** Um gráfico de barras (`sns.barplot`) foi usado para comparar a média salarial entre os diferentes níveis de senioridade (Júnior, Pleno, Sênior, Executivo).
* **Proporção de Trabalho:** Um **Gráfico de Rosca** (`px.pie` com `hole=0.5`) foi utilizado para visualizar a proporção de tipos de trabalho (Presencial, Remoto, Híbrido).

---

### **Aula 4: Construção de um Mapa Interativo**

A última etapa foi a criação de uma visualização geográfica para contextualizar os dados globalmente.
* **Conversão de Países:** A biblioteca **`pycountry`** foi usada para converter os códigos de país de 2 letras (ISO-2) para 3 letras (ISO-3).
* **Mapa Interativo:** Um **Mapa de Cloropleth** (`px.choropleth`) foi criado para visualizar a média salarial de Cientista de Dados em cada país.

---

## 💻 Bibliotecas Utilizadas
* **Pandas**: Para manipulação e análise de dados.
* **Numpy**: Para auxiliar em operações numéricas.
* **Matplotlib / Seaborn**: Para a criação de gráficos estatísticos.
* **Plotly Express**: Para gráficos interativos e o mapa de cloropleth.
* **pycountry**: Para converter códigos de países.
