# 🏢 Analisador de Fundos Imobiliários (FIIs)

Projeto em **Python** voltado à análise de **Fundos de Investimento Imobiliário (FIIs)**, com cálculo automático de:
- Média de proventos pagos nos últimos **3, 6 e 12 meses**  
- Proventos do **último mês**
- **Percentual dos proventos em relação ao preço atual da cota**
- **Variação da cota nos últimos 12 meses**
- Gráficos de **preço** e **proventos mensais** por FII

Desenvolvido para rodar em **notebook (Jupyter/Lab/Colab)** com células segmentadas por fases.

---

## 📊 Exemplo de saída

| Ticker | Preço atual | Δ 12m (%) | Média mensal 3m (R$) | % do preço (3m/mês) | Yield TTM (%) |
|:-------|-------------:|-----------:|----------------------:|--------------------:|---------------:|
| HGLG11 | 171.32 | +4.85 | 1.18 | 0.69% | 7.95% |
| MXRF11 | 10.10 | +2.41 | 0.12 | 1.17% | 14.01% |

E gráficos automáticos, como:

- 📈 **Evolução do preço (últimos 12 meses)**  
- 📊 **Proventos mensais com valores no topo das barras**

---

## 🧠 Estrutura do Notebook

O notebook está dividido em **9 fases** para permitir uso modular:

| Fase | Descrição |
|------|------------|
| 0 | Instalação de dependências |
| 1 | Imports e parâmetros iniciais |
| 2 | Funções auxiliares de data |
| 3 | Download de dados via `yfinance` |
| 4 | Cálculo das métricas principais |
| 5 | Geração da tabela final |
| 6 | Formatação dos resultados |
| 7 | Gráficos de **preço (12m)** |
| 8 | Gráficos de **proventos mensais** |
| 9 | Exportação para CSV/Excel |

---

## ⚙️ Instalação das dependências

### 💻 Via `pip`
```bash
pip install --upgrade pandas numpy yfinance python-dateutil matplotlib XlsxWriter openpyxl lxml
```

---

## 🚀 Uso

Abra o notebook (analisador_fii.ipynb) em seu ambiente preferido (Jupyter, VSCode ou Colab).

Edite a lista de FIIs na variável TICKERS_RAW:

    TICKERS_RAW = "HGLG11, KNRI11, MXRF11"


Execute as células na ordem (Fases 1 → 9).

Veja a tabela com métricas e os gráficos gerados automaticamente.


## 🧩 Funcionalidades extras

Parâmetro de controle:
CONSIDERAR_ULTIMO_MES_CIVIL = True

    True → considera o mês civil completo anterior
    False → considera os últimos 30 dias corridos

Exportação automática:

    fii_metricas.csv
    fii_metricas.xlsx

Gráficos aprimorados:

    Valores dos proventos no topo das colunas
    Sem linhas de grade para visual mais limpo


## 🧰 Tecnologias utilizadas

    Python
    Pandas
    NumPy
    Matplotlib
    yFinance
    dateutil
    XlsxWriter / OpenPyXL

## 🧑‍💻 Autor

    Rudson Rocha
    <pre> '''💼 Coordenador do Laboratório de Tecnologia contra Lavagagem de Dinheiro - LABLD
    📊 Desenvolvimento de ferramentas de análise de dados financeiros e inteligência de dados
    📧 [LinkedIn - https://br.linkedin.com/in/rudson-rocha-79b550300] '''</pre>