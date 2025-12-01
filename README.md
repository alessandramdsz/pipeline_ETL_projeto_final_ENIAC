# 🎬 Projeto final de Bootcamp BI: Uma análise do perfil dos conteúdos da renomada Netflix - Data Pipeline (ETL)

[![Status](https://img.shields.io/badge/Status-Completo-green.svg)]()

> [!WARNING]
> ⚠️ **Antes de iniciar a execução, você precisa baixar os arquivos que constam nesse repositório, junto ao read.me**

### 🚀 `pipeline_ETL_projeto_final_ENIAC`

Este projeto representa o trabalho final do Bootcamp de Business Intelligence, focado na construção de um **Pipeline ETL** completo (Extração, Transformação e Carregamento) para analisar o catálogo da Netflix.

---

### **Sobre o projeto**

O objetivo principal foi transformar dados brutos da Netflix em **insights estratégicos** sobre o perfil de conteúdo e o crescimento anual de lançamentos da plataforma. O resultado final é um dashboard analítico no **Power BI**, embasado em dados limpos e estruturados.

### **Problema central**
Qual é o perfil de conteúdo que a Netflix mais prioriza e como esse conteúdo se relaciona com o volume de títulos lançados anualmente, pensando em tendências de mercado e possibilidades de investimento?

#### **Objetivos da análise**

* Perfil de conteúdo da plataforma (Filmes vs. Séries).
* Crescimento anual de lançamentos (2016 a 2021).
* Tendências de gêneros, tipos e países de origem.
* Comportamento do catálogo e identificação de nichos.

#### **Relevância**

Este estudo é fundamental para entender as **estratégias de conteúdo** da Netflix, fornecer análises de mercado no setor de streaming e suportar **decisões estratégicas** sobre a oferta e o engajamento do catálogo.

#### **Membros**

* Alessandra Machado
* Caroline Cruz
* Clara Maria
* Dayane Lurdes
* Elaine Castro
* Maria Elacide
* Tandara Jesus

---

### 📊 Base de dados

| Detalhe | Informação |
| :--- | :--- |
| **Fonte** | Kaggle - Netflix Movies and TV Shows (shivamb) |
| **Formato** | CSV |
| **Tamanho** | 3.4 MB |
| **Registros** | 8.807 linhas |
| **Colunas** | 12 (show_id, type, title, director, cast, country, date_added, release_year, rating, duration, listed_in, description) |

#### **Perguntas Norteadoras**

* Como se distribui a adição de Filmes vs. Séries ao longo dos anos?
* Quais são os gêneros mais adicionados e como se distribuem por país?
* Qual a relação País x Ano de Adição no catálogo?
* Quais são os nichos de maior engajamento explorados?
* Qual foi o crescimento anual de lançamentos entre 2016 e 2021?

---

### Pipeline ETL (Extração, Transformação e Carregamento)

#### 1. EXTRAÇÃO (Python / Google Colab)

* Importação e carregamento do dataset CSV.
* Análise inicial de tipos de dados, valores nulos e estatísticas descritivas.

#### 2. TRANSFORMAÇÃO (Python / Pandas)

* **Limpeza de Dados:** Tratamento de valores nulos e padronização de formatos.
* **Modelagem:** Conversão de formatos e criação de tabelas normalizadas.
* **Camada Gold:** Preparação final dos dados (limpos e estruturados) para consumo no BI.

#### 3. CARREGAMENTO (SQLite / Power BI)

* Carregamento da **camada gold** em um banco de dados **SQLite**.
* Exportação dos dados tratados para o **Power BI**.

---

### Dashboard e Insights Principais

O dashboard no Power BI permite uma visualização dinâmica e clara dos resultados obtidos com o tratamento acima.

#### 🖼️ **Principais Visualizações**

* **Gráficos de linhas:** Crescimento de lançamentos por ano.
* **Gráficos de barras:** Relação país de vs. ano de adição ao catálogo.
* **Cards de resumo:** Total de títulos, proporção filmes vs. séries.
* **Distribuição:** Gêneros mais frequentes e distribuição geográfica.

#### ✅ **Conclusões Chave (2016 – 2021)**

* **Conteúdo:** Catálogo majoritariamente composto por **filmes (70%)**.
* **Crescimento:** **Crescimento consistente** de lançamentos de 2016 a 2020, com uma queda em 2021.
* **Tendências:** Gêneros mais adicionados: **Drama, comédia e ação**.
* **Geografia:** **EUA** lidera o volume de títulos, seguido pela **Índia**.
* **Estratégia:** Foco em conteúdo antigo (**retrocatálogo** - 10+ anos) e gêneros populares.

---

### Tecnologias Utilizadas

| Categoria | Ferramentas |
| :--- | :--- |
| **Linguagem** | Python |
| **Manipulação de Dados** | Pandas |
| **Banco de Dados** | SQLite |
| **Gerenciamento de DB** | DBeaver |
| **Visualização** | Power BI |
| **Fonte de Dados** | Kaggle |

---

### 🛠️ Como executar este projeto

## 1. Clonar o repositório

Execute os comandos para baixar o projeto e acessar o diretório:
```bash
git clone [https://github.com/seu-usuario/pipeline_ETL_projeto_final_ENIAC.git](https://github.com/seu-usuario/pipeline_ETL_projeto_final_ENIAC.git)
cd pipeline_ETL_projeto_final_ENIAC
```
## 2. Preparar o ambiente

Certifique-se de ter instalado:
* Python 3.8
* Jupyter Notebook ou Google Colab
* SQLite3
* DBeaver (opcional)
* Power BI Desktop

## 3. Instalar dependências

Caso utilize localmente, execute:
pip install -r requirements.txt

Se não existir o arquivo, você pode instalar manualmente: pip install pandas numpy matplotlib sqlite3

## 4. Executar o Notebook de ETL

etl/notebook_ETL.ipynb

Você pode rodá-lo em:

## Google Colab (recomendado)
1. Acesse o Colab
2. Faça upload do notebook disponível neste repositório
3. Faça upload do arquivo CSV na pasta/content
4. Execute todas as células na ordem

## Localmente com Jupyter
jupyter notebook etl/notebook_ETL.ipynb
Execute célula por célula para:
* Fazer a extração dos dados
* Aplicar as transformações
* Gerar a camada gold
* Criar o arquivo final para o banco SQLite

## 5. Executar o banco de dados
Após a execução do ETL, o arquivo SQLite será criado em: database/netflix.db
Você pode abrir o banco com:

**DBeaver**
1. Criar nova conexão SQLite
2. Selecionar netflix.db
3. Explorar as tabelas gold criadas

**SQLite CLI**
- sqlite3 netflix.db

## 6. Abrir o Dashboard no Power BI
O relatório está em: dashboard/Netflix.pbix

Para abrir:
1. Instale o Power BI Desktop
2. Abra o arquivo Netflix.pbix
3. Certifique-se que a conexão com o banco ou CSV tratado está correta
4. Atualize os dados clicando em Atualizar

## 7. Reproduzir o pipeline completo

Resumo do fluxo:
1. Extrair o CSV original
2. Transformar no Python (Colab ou Jupyter)
3. Gerar a camada gold
4. Carregar no SQLite
5. Visualizar no Power BI

---

## Explicando os arquivos do repositório
1. Consolidado_Apresentação_Final.pptx.pdf: É um PDF completo explicando o projeto em forma de relatório.
2. Collab_Tratamento_Netflix.ipynb: É o ambiente Google Collab com as execuções. Você também pode acessar neste link: https://colab.research.google.com/drive/1oWVQSI7Dt01RaCvzovo8kzl03x-4vdqs
3. Netflix_Dashboard_BI.pbix: É o arquivo Power BI
4. README.md: Esta leitura, como executar o projeto
5. collab_tratamento_netflix.py: É o arquivo final do código gerado no Collab, na linguagem python

---

📄 Licença
Este projeto é de código aberto e está sob a licença MIT.

📧 Contato
- Alessandra Machado - @alessandramdsz
- Link do projeto: [https://github.com/alessandramdsz/pipeline_ETL_projeto_final_ENIAC]
