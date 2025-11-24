# pipeline_ETL_projeto_final_ENIAC
Projeto final de Bootcamp de Bussiness Inteligence
# Sobre o projeto

Visão Detalhada do Perfil de Conteúdo e do Crescimento Anual de Lançamentos da Netflix
Projeto desenvolvido para o Projeto Final da Turma ENIAC pelas integrantes:

Alessandra Machado • Aline de Oliveira • Caroline Cruz • Clara Maria • Dayane Lurdes • Elaine Castro • Maria Elacide • Tandara Jesus

# Objetivo do Projeto

Construir um pipeline ETL completo (Extração, Transformação e Carregamento) utilizando dados da Netflix, com o propósito de gerar análises sobre:
Perfil de conteúdo da plataforma
* Crescimento anual de lançamentos
* Tendências de gêneros, tipos e países
* Comportamento do catálogo de 2016 a 2021
Transformamos dados brutos em insights claros, estruturados e visualizados em dashboard no Power BI.

# Relevância do Tema

O estudo é relevante para:
* Entendimento de estratégias de conteúdo
* Análises de mercado no setor de streaming
* Insights sobre engajamento, oferta e tendências
* Suporte a decisões estratégicas de catálogo

# Base de Dados

* Fonte: Kaggle
* Dataset: Netflix Movies and TV Shows (netflix-shows), por shivamb
* Formato: .csv
* Tamanho: 3.4 MB
* Linhas: 8.807
* Colunas (12):
 show_id, type, title, director, cast, country,
date_added, release_year, rating, duration,
listed_in, description

# Perguntas Norteadoras

* Distribuição Filmes vs Séries ao longo dos anos
* Gêneros mais frequentes e sua distribuição por país
* Quais gêneros são mais adicionados?
* Relação País x Ano de Adição
* Nichos de maior engajamento
* Crescimento anual entre 2016 e 2021

# Pipeline ETL

1. EXTRAÇÃO
Realizada a partir do arquivo .csv no Kaggle.

Atividades:
* Importação das bibliotecas
* Carregamento no Google Colab
* Análise de tipos
* Verificação de valores nulos
* Estatísticas iniciais

2. TRANSFORMAÇÃO
Transformações aplicadas:
* Limpeza de dados
* Padronização de colunas
* Tratamento de nulos
* Conversão de formatos
* Criação da camada gold
* Criação de tabelas normalizadas
* Preparação dos dados para consumo no BI

3. CARREGAMENTO
* Carregamento no SQLite
* Visualização e manipulação via DBeaver
* Exportação dos dados tratados para o Power BI

# Dashboard – Principais Visualizações

Criado no Power BI com base na camada gold.
nclui:

* Gráfico de linha: lançamentos por ano
* Gráfico de barras: país × ano
* Cards resumidos:
* Total de títulos
Filmes vs Séries
Títulos por ano
* Gêneros mais frequentes
* Distribuição geográfica
* Análises gerais do catálogo

# Insights Gerais

Principais conclusões:
* Crescimento consistente de lançamentos entre 2016–2020, seguido de queda em 2021
* Catálogo majoritariamente composto por filmes (70%)
* Gêneros mais adicionados: Drama, Comédia, Ação
* EUA lidera em número de títulos; Índia fica em segundo
* Expansão internacional e foco em nichos de engajamento (Crime, Anime, Séries)
* Entre 2019–2021, a maioria dos títulos adicionados são retrocatálogo (10+ anos)
* Estratégia observada: conteúdo antigo + gêneros populares para manter volume e variedade

# Tecnologias Utilizadas

* Python (Google Colab)
* Pandas
* SQLite
* DBeaver
* Power BI
* Kaggle

# Conclusão

Este projeto entrega um pipeline ETL completo, da extração à visualização. Permite entender profundamente como a Netflix estrutura e expande seu catálogo ao longo dos anos.

# Como Executar o Projeto

## 1. Clonar o Repositório
git clone https://github.com/seu-usuario/pipeline_ETL_projeto_final_ENIAC.git
cd pipeline_ETL_projeto_final_ENIAC

## 2. Preparar o Ambiente
Certifique-se de ter instalado:
* Python 3.8
* Jupyter Notebook ou Google Colab
* SQLite3
* DBeaver (opcional)
* Power BI Desktop

## 3. Instalar Dependências
Caso utilize localmente, execute:
pip install -r requirements.txt

Se não existir o arquivo, você pode instalar manualmente:
pip install pandas numpy matplotlib sqlite3

## 4. Executar o Notebook de ETL
etl/notebook_ETL.ipynb

Você pode rodá-lo em:
## Google Colab (recomendado)

1. Acesse o Colab
2. Faça upload do noteboo
3. Faça upload do arquivo CSV na pasta /content
4. Execute todas as células na ordem

## Localmente com Jupyter
jupyter notebook etl/notebook_ETL.ipynb

Execute célula por célula para:
* Fazer a extração dos dados
* Aplicar as transformações
* Gerar a camada gold
* Criar o arquivo final para o banco SQLite

## 5. Executar o Banco de Dados

Após a execução do ETL, o arquivo SQLite será criado em:
database/netflix.db

Você pode abrir o banco com:

DBeaver
1. Criar nova conexão SQLite
2. Selecionar netflix.db
3. Explorar as tabelas gold criadas

SQLite CLI
sqlite3 netflix.db

## 6. Abrir o Dashboard no Power BI

O relatório está em:
dashboard/Netflix.pbix

Para abrir:
1. Instale o Power BI Deskto
2.  Abra o arquivo Netflix.pbix
3. Certifique-se que a conexão com o banco ou CSV tratado está correta
4. Atualize os dados clicando em Atualizar


## 7. Reproduzir o Pipeline Completo

Resumo do fluxo:
1. Extrair o CSV original
2. Transformar no Python (Colab ou Jupyter)
3. Gerar a camada gold
4. Carregar no SQLite
5. Visualizar no Power BI


