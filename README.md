# 🏠 House Prices — Advanced Regression Techniques
### Data Analysis and Machine Learning Hackathon — FAESA Centro Universitário

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-1.x-F7931E?logo=scikit-learn)
![XGBoost](https://img.shields.io/badge/XGBoost-1.x-189BCC)
![License](https://img.shields.io/badge/license-MIT-green)

---

## 📋 Sobre o Projeto

Este projeto realiza uma análise completa do dataset [House Prices - Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data) do Kaggle, cobrindo todas as etapas do pipeline de Data Science:

- 🔍 Análise Exploratória de Dados (EDA)
- ⚙️ Feature Engineering
- 🤖 Aprendizagem Supervisionada (Regressão e Classificação)
- 🔮 Aprendizagem Não Supervisionada (Clusterização, PCA, Apriori, LOF)
- 📊 Visualização e Comparação de Métricas

---

## 🗂️ Estrutura do Repositório

```
C3 ANALISE DE DADOS FINAL/
│
├── 📓 house_prices_analysis.ipynb   # Notebook principal com toda a análise
├── 📄 README.md                     # Este arquivo
├── 📦 requirements.txt              # Dependências do projeto
│
└── data/                            # (não versionado — baixar do Kaggle)
    ├── train.csv
    ├── test.csv
```

> ⚠️ Os arquivos de dados **não estão incluídos** neste repositório.
> Faça o download em: https://www.kaggle.com/c/house-prices-advanced-regression-techniques/data

---

## 🚀 Como Executar

### 1. Clone o repositório
```bash
git clone https://github.com/seu_usuario/c3-analise-dados-final.git
cd c3-analise-dados-final
```

### 2. Instale as dependências
```bash
pip install -r requirements.txt
```

### 3. Adicione os dados
Baixe `train.csv` e `test.csv` do Kaggle e coloque-os na **mesma pasta** do notebook.

### 4. Execute o notebook
```bash
jupyter notebook house_prices_analysis.ipynb
```

---

## 📦 Dependências

| Biblioteca     | Versão mínima | Uso                              |
|----------------|---------------|----------------------------------|
| pandas         | 1.5+          | Manipulação de dados             |
| numpy          | 1.23+         | Operações numéricas              |
| matplotlib     | 3.6+          | Visualizações                    |
| seaborn        | 0.12+         | Gráficos estatísticos            |
| scikit-learn   | 1.2+          | ML — modelos e métricas          |
| xgboost        | 1.7+          | Gradient Boosting                |
| mlxtend        | 0.21+         | Apriori e regras de associação   |

---

## 📊 Resultados Obtidos

### Regressão (previsão de SalePrice)

| Modelo              | R²    | RMSE (log) | R² CV-5 |
|---------------------|-------|------------|---------|
| XGBoost             | ~0.92 | ~0.12      | ~0.91   |
| Gradient Boosting   | ~0.91 | ~0.13      | ~0.90   |
| Random Forest       | ~0.88 | ~0.15      | ~0.87   |
| Ridge               | ~0.82 | ~0.18      | ~0.81   |
| Regressão Linear    | ~0.80 | ~0.19      | ~0.79   |
| Lasso               | ~0.80 | ~0.19      | ~0.79   |

### Classificação (casa cara vs. barata)

| Modelo              | Acurácia | AUC-ROC | Acc CV-5 |
|---------------------|----------|---------|---------|
| XGBoost             | ~0.92    | ~0.97   | ~0.91   |
| Random Forest       | ~0.91    | ~0.97   | ~0.90   |
| Árvore de Decisão   | ~0.87    | ~0.87   | ~0.86   |
| Regressão Logística | ~0.86    | ~0.94   | ~0.85   |
| KNN                 | ~0.83    | ~0.91   | ~0.82   |

---

## 🔍 Técnicas Aplicadas

### EDA
- Análise de valores faltantes e distribuições
- Matriz de correlação (Top 14 features)
- Boxplots por variáveis categóricas
- Análise de skewness do target `SalePrice`

### Feature Engineering
- Criação de `TotalSF`, `TotalBath`, `HouseAge`, `RemodAge` e outros
- Indicadores binários: `HasGarage`, `HasPool`, `HasFireplace`, `HasBsmt`
- Imputação contextual de valores faltantes
- Log-transformação de features assimétricas
- Encoding ordinal (qualidade) + One-Hot (demais categóricas)
- Normalização com RobustScaler

### Não Supervisionado
- **PCA**: ~25 componentes explicam 95% da variância
- **K-Means (k=4)**: 4 segmentos de imóveis identificados
- **LOF**: ~5% de outliers detectados
- **Apriori**: regras com lift > 1.2, ex: `Alta qualidade + 3+ banheiros → Preço Luxo`

---

## 🏆 Principais Insights

1. **Qualidade geral** (`OverallQual`) é a variável mais correlacionada com o preço
2. **Área habitável** (`GrLivArea`) e **área total** (`TotalSF`) têm forte impacto
3. **Bairro** (`Neighborhood`) explica grande variabilidade de preço
4. Casas **remodeladas** tendem a valer mais que casas de mesma idade sem reforma
5. A presença de **lareira** e **garagem** está associada a preços mais altos

---

## 👥 Equipe

| Nome | GitHub |
|------|--------|
| [Miguel] | [@Miguelamm0911](https://github.com/Miguelamm0911) |
| [Caio] | [@CaioBrenoAlvesMachado](https://github.com/caiobrenoalvesmachado-commits) |
| [Alexandre] | [@AlexandrePlacencia](https://github.com/AlexandrePlacencia) |
| [Joao Pedro] | [@jptwelvee](https://github.com/jptwelvee) |

---

## 📚 Referências

- [Kaggle — House Prices Competition](https://www.kaggle.com/c/house-prices-advanced-regression-techniques)
- [Scikit-learn Documentation](https://scikit-learn.org/stable/)
- [XGBoost Documentation](https://xgboost.readthedocs.io/)
- [MLxtend — Apriori](http://rasbt.github.io/mlxtend/)

---

*Projeto desenvolvido para a disciplina de Data Analysis and Machine Learning — FAESA Centro Universitário — Prof. M.Sc. Howard Roatti*
