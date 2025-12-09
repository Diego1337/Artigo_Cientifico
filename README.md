# 📊 Análise de Desempenho do ENADE 2023

> Uma análise exploratória e estatística dos dados do **Exame Nacional de Desempenho dos Estudantes (ENADE) de 2023**.

O objetivo principal deste projeto é investigar padrões de desempenho acadêmico ("Conceito Enade") e correlacioná-los com **variáveis geográficas**, **tipos de instituição** e **taxas de abstenção**.

👥 **Autores:**
* **Diego Ribeiro Lima**
* **Giulia Santiago Barreto**

---

## 📝 Sobre o Projeto

O estudo utiliza dados públicos do **ENADE 2023** para responder a questões fundamentais sobre a qualidade do ensino superior no Brasil. A análise foca em entender como o desempenho dos alunos varia entre:

- Diferentes **Estados e Regiões**;
- Categorias administrativas (**Pública vs. Privada**);
- A influência do **absenteísmo** na nota média das UFs.

---

## 🛠️ Tecnologias Utilizadas

O projeto foi desenvolvido em **Python** utilizando as seguintes bibliotecas para manipulação de dados e visualização:

- **Pandas:** Leitura, limpeza e agregação dos dados.
- **Seaborn & Matplotlib:** Criação de gráficos estáticos para análise visual (Boxplots, Gráficos de Barras, Dispersão e Regressão).

---

## 📂 Estrutura da Análise

O notebook segue um fluxo lógico de processamento de dados, dividido em duas grandes etapas:

### 1. Pré-processamento e Limpeza
- Importação da base de dados `conceito_enade_2023.xlsx`.
- Remoção de duplicatas e linhas com dados nulos.
- Filtragem de registros sem conceito atribuído (exclusão da faixa 'SC').
- Padronização de nomes de colunas e mapeamento de categorias administrativas para dois grandes grupos: **Pública** e **Privada**.
- Criação de colunas auxiliares, como agrupamento por **Regiões** (Sul, Sudeste, etc.) e cálculo de taxas de abstenção.

### 2. Análises Realizadas

- **Pública vs. Privada**
  Comparação direta das medianas do *Conceito Enade (Contínuo)* entre instituições públicas e privadas utilizando **Boxplots**. O gráfico destaca a distribuição das notas e exibe os valores das medianas para cada categoria.

- **Análise Regional e Estadual**
  - **Por Região:** Gráfico de barras comparando a média do conceito Enade entre as regiões do Brasil.
  - **Por Estado (UF):** Identificação dos estados com maior média, menor média e maior volume de participantes. Visualização da distribuição de notas de todos os estados através de Boxplots ordenados e Ranking de estados por Taxa de Abstenção.

- **Estudo de Caso: Estados-Chave**
  Uma análise aprofundada comparando métricas específicas (Nota Média, Abstenção e Composição Pública/Privada) entre os estados de destaque (**Maior Média**, **Menor Média** e **Maior Volume**).

- **Correlação: Abstenção vs. Desempenho**
  Verificação estatística e visual (*Scatter Plot* com linha de regressão) para determinar se existe uma correlação significativa entre a taxa de abstenção de um estado e sua média no Conceito Enade.

---

## 🚀 Principais Resultados Observados

Com base na execução do código e análise dos dados, o estudo apontou:

- **Disparidade Institucional:** Análise visual das medianas indicando diferenças de desempenho entre o ensino público e privado.
- **Destaques Geográficos:**
  - 🏆 O estado do **Espírito Santo (ES)** foi identificado com a **maior média** do Conceito Enade.
  - 🔻 O estado do **Amazonas (AM)** apresentou a **menor média**.
  - 📦 **São Paulo (SP)** lidera em **volume de concluintes**.
- **Correlação:** A análise de dispersão sugere que **não há evidências estatísticas fortes** para afirmar que a taxa de abstenção dita a média do conceito de um estado (correlação não estatisticamente significante).

---

## 📦 Como Executar

1. Certifique-se de ter o arquivo `conceito_enade_2023.xlsx` no mesmo diretório do notebook.
2. Instale as dependências necessárias:

```bash
pip install pandas seaborn matplotlib openpyxl
```
3. Execute o Jupyter Notebook

```bash
jupyter notebook Artigo_Final.ipynb
```   
---

## 📸 Prévia das Visualizações

Abaixo estão alguns dos principais insights visuais gerados por este estudo:

### 1. Disparidade: Pública vs. Privada
Este boxplot ilustra a diferença na distribuição das notas entre instituições públicas e privadas. Observe como a mediana das públicas tende a ser superior, indicando um desempenho geral mais consistente.

<img width="837" height="611" alt="image" src="https://github.com/user-attachments/assets/17570e31-a7d3-4bae-b7e4-388d6f023806" />

### 2. Panorama Nacional: Desempenho por Estado
Visualização da distribuição das notas em todas as Unidades da Federação.
- **Destaque Superior:** Estados como ES aparecem no topo.
- **Variação:** É possível notar a amplitude das notas dentro de cada estado.

<img width="1990" height="790" alt="image" src="https://github.com/user-attachments/assets/f2d5402c-0fbc-4993-9c13-8c9308a04c2a" />

### 3. Correlação: Abstenção afeta a Nota?
O gráfico de dispersão com linha de regressão investiga a hipótese de que estados com mais faltas teriam notas menores. A linha quase horizontal sugere uma correlação fraca ou inexistente.

<img width="1389" height="593" alt="image" src="https://github.com/user-attachments/assets/11999194-0f1d-4bbb-9dc3-34eb026500ce" />
