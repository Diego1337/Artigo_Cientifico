📊 Análise de Desempenho do ENADE 2023
Este projeto consiste em uma análise exploratória e estatística dos dados do Exame Nacional de Desempenho dos Estudantes (ENADE) de 2023. O objetivo principal é investigar padrões de desempenho acadêmico ("Conceito Enade") e correlacioná-los com variáveis geográficas, tipos de instituição e taxas de abstenção.

📝 Sobre o Projeto
O estudo utiliza dados públicos do ENADE 2023 para responder a questões sobre a qualidade do ensino superior no Brasil. A análise foca em entender como o desempenho dos alunos varia entre diferentes estados, regiões e categorias administrativas (Pública vs. Privada), além de verificar se o absenteísmo influencia a nota média das UFs.

🛠️ Tecnologias Utilizadas
O projeto foi desenvolvido em Python utilizando as seguintes bibliotecas para manipulação de dados e visualização:

Pandas: Leitura, limpeza e agregação dos dados.

Seaborn & Matplotlib: Criação de gráficos estáticos para análise visual (Boxplots, Gráficos de Barras, Dispersão e Regressão).

Estrutura da Análise
O notebook segue um fluxo lógico de processamento de dados:

1. Pré-processamento e Limpeza
Importação da base de dados conceito_enade_2023.xlsx.

Remoção de duplicatas e linhas com dados nulos.

Filtragem de registros sem conceito atribuído (exclusão da faixa 'SC').

Padronização de nomes de colunas e mapeamento de categorias administrativas para dois grandes grupos: Pública e Privada.

Criação de colunas auxiliares, como agrupamento por Regiões (Sul, Sudeste, etc.) e cálculo de taxas de abstenção.

2. Análises Realizadas
A. Pública vs. Privada
Comparação direta das medianas do Conceito Enade (Contínuo) entre instituições públicas e privadas utilizando Boxplots. O gráfico destaca a distribuição das notas e exibe os valores das medianas para cada categoria.

B. Análise Regional e Estadual
Por Região: Gráfico de barras comparando a média do conceito Enade entre as regiões do Brasil.

Por Estado (UF):

Identificação dos estados com maior média (ex: ES), menor média (ex: AM) e maior volume de participantes (ex: SP).

Visualização da distribuição de notas de todos os estados através de Boxplots ordenados.

Ranking de estados por Taxa de Abstenção.

C. Estudo de Caso: Estados-Chave
Uma análise aprofundada comparando métricas específicas (Nota Média, Abstenção e Composição Pública/Privada) entre os estados de destaque (Maior Média, Menor Média e Maior Volume).

D. Correlação: Abstenção vs. Desempenho
Verificação estatística e visual (Scatter Plot com linha de regressão) para determinar se existe uma correlação significativa entre a taxa de abstenção de um estado e sua média no Conceito Enade.

🚀 Principais Resultados Observados
Com base na execução do código, o estudo apontou:

Disparidade Institucional: Análise visual das medianas indicando diferenças de desempenho entre o ensino público e privado.

Destaques Geográficos:

O estado do Espírito Santo (ES) foi identificado com a maior média do Conceito Enade.

O estado do Amazonas (AM) apresentou a menor média.

São Paulo (SP) lidera em volume de concluintes.

Correlação: A análise de dispersão sugere que não há evidências estatísticas fortes para afirmar que a taxa de abstenção dita a média do conceito de um estado (correlação não estatisticamente significante).

📦 Como Executar
Certifique-se de ter o arquivo conceito_enade_2023.xlsx no mesmo diretório do notebook.

Instale as dependências necessárias:

Bash

pip install pandas seaborn matplotlib openpyxl
Execute o Jupyter Notebook:

Bash

jupyter notebook Artigo_Final.ipynb
