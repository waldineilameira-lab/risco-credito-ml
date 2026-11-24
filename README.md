# 🏦 Risco de Crédito — Pipeline Preditivo com KNN e Árvore de Decisão

> Projeto avaliativo do curso **Machine Learning e Visão Computacional [T5]** — SENAI/SC
> Autor: **Waldinei Lameira Rosa** · [github.com/waldineilameira-lab](https://github.com/waldineilameira-lab)

---

## 1. Problema de negócio

Um banco precisa prever se um cliente se tornará **inadimplente** (`loan_status = 1`)
ou pagará o empréstimo em dia (`loan_status = 0`).

**Pergunta central:** qual é o impacto financeiro de cada tipo de erro do modelo?

| Erro | O que acontece | Impacto para o banco |
|---|---|---|
| **Falso Positivo** | Bom pagador classificado como "risco de calote" | Crédito negado → perda de receita de juros e do cliente |
| **Falso Negativo** | Mau pagador classificado como "seguro" | Crédito concedido → perda do capital emprestado |

> _Seção a ser concluída na Fase 6 com o veredito final._

---

## 2. Estrutura do repositório

```
risco-credito-ml/
├── data/
│   └── raw/
│       └── credit_risk_dataset.csv   # base original (não editada)
├── notebooks/
│   └── pipeline_risco_credito.ipynb  # pipeline completo, fase por fase
├── reports/
│   └── figures/                      # gráficos exportados para o README
├── .gitignore
├── requirements.txt
└── README.md
```

---

## 3. Como executar

```bash
# 1. Clonar o repositório
git clone https://github.com/waldineilameira-lab/risco-credito-ml.git
cd risco-credito-ml

# 2. Criar e ativar o ambiente virtual
python -m venv .venv
.venv\Scripts\activate          # Windows (PowerShell)
# source .venv/bin/activate     # Linux / macOS

# 3. Instalar as dependências
pip install -r requirements.txt

# 4. Abrir o notebook no VS Code e selecionar o kernel .venv
code .
```

---

## 4. Dicionário de dados

> _A ser preenchido na Fase 1 (EDA) e atualizado na Fase 3 com a coluna `comprometimento_renda`._

---

## 5. Principais insights da EDA

> _A ser preenchido ao final da Fase 1._

---

## 6. Resumo executivo e veredito

> _A ser preenchido ao final da Fase 6._

---

## 7. Fluxo de versionamento

Cada fase foi desenvolvida em uma branch própria e integrada à `main` via Pull Request:

| Branch | Conteúdo |
|---|---|
| `fase/setup` | Estrutura do projeto e ambiente |
| `fase/eda` | Análise Exploratória de Dados |
| `fase/data-prep` | Duplicados, nulos e outliers |
| `fase/feature-engineering` | Coluna `comprometimento_renda` |
| `fase/pre-processamento` | Encoding, split, SMOTE e scaler |
| `fase/modelagem` | KNN × Árvore e diagnóstico de overfitting |
| `fase/avaliacao` | Matrizes de confusão e veredito de negócio |
| `docs/readme` | Documentação final |
