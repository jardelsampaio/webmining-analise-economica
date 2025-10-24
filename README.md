# WebMining — Coleta e Análise de Dados Econômicos

Projeto desenvolvido como parte da disciplina **Web mining & crawler scraping (MBA em Engenharia de Dados)**.  
O objetivo é construir um pipeline completo de **coleta, tratamento, armazenamento e análise de dados econômicos e financeiros**, utilizando **Python, Jupyter Notebook e DuckDB**.

---

## Objetivo

Realizar a coleta automatizada de **séries históricas financeiras** (como SELIC, IPCA, IBOVESPA e Bitcoin) e **notícias econômicas**, estruturando os dados em um formato analítico (banco DuckDB) para posterior análise exploratória e visualização.

---

## Estrutura do Projeto

```
WebMining/
│
├── banco/
│   └── banco_analitico.duckdb        # Banco principal com as tabelas normalizadas
│
├── data/
│   ├── raw/                          # Dados brutos (coleta de APIs e scrapers)
│   ├── processed/                    # Dados limpos e transformados
│   └── outputs/                      # Resultados analíticos e exportações
│
├── notebooks/
│   ├── 01_planejamento_setup.ipynb   # Planejamento e setup do ambiente
│   ├── 02_coleta_series_api.ipynb    # Coleta de séries históricas (BCB, IBOV, CoinGecko)
│   ├── 03_coleta_noticias.ipynb      # Web Scraping de notícias financeiras (SeuDinheiro)
│   └── 04_analise_exploratoria.ipynb # Análise exploratória e correlação entre indicadores
│
├── requirements.txt
└── README.md
```

---

## Tecnologias Utilizadas

- **Python 3.10+**
- **Jupyter Notebook**
- **DuckDB** → Banco de dados analítico colunar  
- **Pandas / NumPy** → Manipulação de dados  
- **Requests / BeautifulSoup / Selenium** → Coleta e Web Scraping  
- **APIs públicas** → Banco Central, CoinGecko, B3  
- **Matplotlib / Seaborn / Plotly** → Visualizações (na análise exploratória)

---

## Escopo Mínimo Atendido

- **Séries históricas:** +12 meses contínuos de dados (SELIC, IPCA, IBOV, BTC/BRL etc.)  
- **Notícias:** Coleta automática de manchetes e datas via Web Scraping  
- **Banco DuckDB:** pelo menos 3 tabelas (`indicadores`, `noticias`, `series_brutas`)  
- **Integração ETL:** pipelines de coleta, transformação e carga  
- **Análise:** correlação entre indicadores econômicos e principais manchetes

---

## Como Executar o Projeto

### 1️. Clone o repositório
```bash
git clone https://github.com/seuusuario/webmining-analise-economica.git
cd webmining-analise-economica
```

### 2️. Crie e ative o ambiente virtual
```bash
python -m venv venv
venv\Scripts\activate    # Windows
source venv/bin/activate # Linux/Mac
```

### 3️. Instale as dependências
```bash
pip install -r requirements.txt
```

### 4️. Execute os notebooks em ordem
Abra o Jupyter e rode:
```
01_planejamento_setup.ipynb
02_coleta_series_api.ipynb
03_coleta_noticias.ipynb
04_analise_exploratoria.ipynb
```

---

## Estrutura de Dados no DuckDB

| Tabela | Descrição |
|:--------|:-----------|
| `indicadores` | Séries econômicas consolidadas (SELIC, IPCA, IBOV, BTC, etc.) |
| `noticias` | Notícias coletadas via scraping |
| `series_brutas` | Dados intermediários coletados das APIs |

---

## Exemplos de Insights

- Correlação entre a **variação do IBOVESPA** e a **taxa SELIC**.  
- Relação entre **alta do Bitcoin** e **sentimento das manchetes econômicas**.  
- Tendência temporal dos principais indicadores de inflação e juros.

---

## Autor

**José Jardel Sampaio Siqueira**  
💼 Engenheiro de Dados | BI & Integração de ERPs  
🔗 [LinkedIn](https://www.linkedin.com/in/jardelsampaio) • [GitHub](https://github.com/seuusuario)

---

## Licença

Este projeto é de uso acadêmico e livre para fins educacionais, conforme os termos da licença MIT.
