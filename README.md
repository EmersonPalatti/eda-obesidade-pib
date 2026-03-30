# Análise de Dados de Obesidade e PIB

Análise exploratória de dados relacionando taxas de obesidade global com indicadores de PIB per capita ao longo do tempo.

## 📁 Estrutura do Projeto

```
├── data/
│   ├── obesity_cleaned.csv    # Dados de obesidade por país/ano/sexo
│   └── gdp.csv                # Dados de PIB per capita por país/ano
├── sample.ipynb               # Notebook principal com a análise completa
├── pyproject.toml             # Configuração do projeto e dependências
├── requirements.txt           # Dependências do projeto
└── README.md                  # Este arquivo
```

## 📊 Conjuntos de Dados

### Dados de Obesidade (`obesity_cleaned.csv`)
- **Período**: 1975–2016
- **Registros**: 24.570
- **Variáveis**: `Country`, `Year`, `Obesity (%)`, `Sex` (Both sexes / Male / Female)

### Dados de PIB (`gdp.csv`)
- **Período**: 1901–2011
- **Registros**: 4.419 (193 países, intervalo de 5 anos)
- **Variáveis**: `Country`, `Region`, `Year`, `GDP_pp` (PIB per capita em USD)

## 🔍 Análises Realizadas

### Obesidade
- Percentual médio por sexo no mundo (2015)
- Países com maior e menor taxa de obesidade
- Top 5 países com maior crescimento de obesidade entre 1975 e 2016
- Evolução temporal global para ambos os sexos
- Diferença percentual entre sexos ao longo dos anos (Brasil)

### PIB per capita
- Primeiros registros por país
- Regiões com maior crescimento de PIB no século passado
- Preenchimento de anos ausentes via estimativa linear por taxa de variação anual
- Identificação e marcação de dados reais vs. estimados

## 🛠️ Tecnologias Utilizadas

- **Python 3.14+**
- **Pandas 3.0+** — Manipulação e análise de dados
- **NumPy** — Operações numéricas
- **Matplotlib 3.10+** — Visualizações
- **JupyterLab 4.5+** — Ambiente interativo

## 🚀 Como Executar

**Com `uv` (recomendado):**
```bash
uv sync
uv run jupyter lab
```

**Com `pip`:**
```bash
pip install -r requirements.txt
jupyter lab
```

Abra o arquivo `sample.ipynb` e execute as células sequencialmente.

## 📝 Observações

- Os dados de PIB possuem registros a cada 5 anos; anos intermediários foram estimados com base na taxa de variação anual entre registros consecutivos por país
- O campo `kind` identifica dados como `real` (originais) ou `estimated` (interpolados)
- Kosovo é o único país com primeiro registro em 1991 (demais países iniciam em 1901)