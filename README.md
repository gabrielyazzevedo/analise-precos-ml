# Analisando Dados de Preços de Casas nos Estados Unidos

Desenvolvido por **[Gabriely Barbosa da Silva Azevedo e Guilherme dos Santos Gonçalves Bispo]**

---

## Dataset

**House Prices: Advanced Regression Techniques**  
Fonte: [Kaggle](https://www.kaggle.com/datasets/rishitaverma02/house-prices-advanced-regression-techniques?resource=download)  
1.460 imóveis | 80 variáveis (numéricas e categóricas) | Target: `SalePrice`

---

## Estrutura do Repositório

```
├── analise_precos.ipynb   # Notebook principal com toda a análise
├── data/                                
│   ├── train.csv
│   ├── test.csv
│   └── sample_submission.csv
└── README.md
```

---

## O que foi feito

### 1. Análise Exploratória de Dados (EDA)
- Identificação de variáveis numéricas e categóricas
- Análise de valores faltantes
- Distribuição do preço de venda e correlações com as demais variáveis

### 2. Feature Engineering
- Criação de 4 novas variáveis:
  - `HouseAge`: idade da casa no momento da venda
  - `YearsSinceRemod`: anos desde a última reforma
  - `TotalBaths`: total de banheiros (somando parciais)
  - `TotalSF`: área total construída (subsolo + térreo + 2º andar)

### 3. Aprendizagem Supervisionada: Regressão
| Modelo | RMSE | R² |
|---|---|---|
| Regressão Linear | ~ | ~ |
| Árvore de Decisão | ~ | ~ |

### 4. Aprendizagem Supervisionada: Classificação
> `SalePrice` convertido em variável binária (acima/abaixo da mediana)

| Modelo | Acurácia | F1-Score |
|---|---|---|
| Regressão Logística | ~ | ~ |
| Random Forest | ~ | ~ |

### 5. Aprendizagem Não Supervisionada
- **K-Means**: agrupamento de imóveis por características semelhantes (método do cotovelo para escolha do K)
- **PCA**: redução de dimensionalidade para visualização em 2D
- **Apriori**: regras de associação entre qualidade, garagem e faixa de preço
- **Local Outlier Factor (LOF)**: detecção de imóveis com características atípicas

---

## Como executar

1. Clone o repositório:
```bash
git clone https://github.com/gabrielyazzevedo/analise-precos-ml.git
cd analise-precos-ml
```

2. Instale as dependências:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn mlxtend jupyter
```

3. Coloque os arquivos `train.csv` e `test.csv` na pasta data/ do projeto (baixe no [Kaggle](https://www.kaggle.com/datasets/rishitaverma02/house-prices-advanced-regression-techniques?resource=download))

4. Execute o notebook:
```bash
jupyter notebook analise_precos.ipynb
```

---

## Tecnologias utilizadas

- Python 3
- Pandas e NumPy
- Matplotlib e Seaborn
- Scikit-learn
- MLxtend

---
