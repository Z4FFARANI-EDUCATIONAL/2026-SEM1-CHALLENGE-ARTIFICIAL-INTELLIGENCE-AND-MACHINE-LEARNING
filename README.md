# Altermax · Inteligência Artificial & Machine Learning

| Integrante | RM |
|---|---|
| [Guilherme Santos Nunes](https://github.com/sannunez) | RM558989 |
| [Kaique Zaffarani](https://github.com/Z4ffarani) | RM556677 |
| [Kairo da Silva Silvestre de Carvalho](https://github.com/KairoSilvestre) | RM558288 |
| [Pedro Josué Pereira Almeida](https://github.com/Pedro-Josue) | RM554913 |

Challenge 2026.1 · Ford · Engenharia de Software · FIAP

---

## Esta entrega: Inteligência Artificial & Machine Learning

**Segmentação comportamental e classificação de perfis de clientes em e-commerce**, aplicando clustering e modelagem preditiva supervisionada sobre dados transacionais reais de um e-commerce britânico.

- **Segmentação (Base 1 – Histórico Completo):** engenharia das métricas RFM (Recência, Frequência, Monetário), remoção de outliers, padronização e clusterização via K-Means (k=3, validado por Silhouette Score e Método do Cotovelo) e Clustering Hierárquico. Identificação de três perfis de negócio: *Cliente Premium*, *Cliente Potencial* e *Cliente em Risco*.
- **Classificação (Base 2 – Primeira Compra):** treinamento de modelo preditivo (Gradient Boosting, selecionado por F1 Macro) usando apenas variáveis disponíveis no momento da primeira compra, respeitando a regra de data leakage. Os perfis da segmentação tornam-se a variável-alvo.
- Leitura executiva com estratégias de retenção por segmento e inferência de perfil para novos clientes.

**Dados:** [Online Retail — UCI ML Repository](https://archive.ics.uci.edu/dataset/502/online+retail), com 541.909 transações de e-commerce (2010–2011).

| Entregável | Onde |
|---|---|
| Notebook | [`CHALLENGE-AI.ipynb`](CHALLENGE-AI.ipynb) |
| Base de dados | [`Online Retail.xlsx`](Online%20Retail.xlsx) |

## Como executar

```bash
pip install pandas numpy matplotlib seaborn scikit-learn scipy openpyxl jupyter
jupyter notebook CHALLENGE-AI.ipynb
```

---

## Tecnologias

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)](https://jupyter.org)
[![pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white)](https://pandas.pydata.org)
[![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)](https://numpy.org)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)](https://scikit-learn.org)
[![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=flat-square&logo=scipy&logoColor=white)](https://scipy.org)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat-square)](https://matplotlib.org)
[![seaborn](https://img.shields.io/badge/seaborn-4C72B0?style=flat-square)](https://seaborn.pydata.org)

---

## Referências

| # | Referência | Aplicação no projeto |
|---|---|---|
| 1 | [UCI ML Repository — Online Retail](https://archive.ics.uci.edu/dataset/502/online+retail) | Base de dados real de transações |
| 2 | [scikit-learn — `KMeans`](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html) | Segmentação dos clientes |
| 3 | [scikit-learn — `GradientBoostingClassifier`](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.GradientBoostingClassifier.html) | Classificação do perfil na primeira compra |
