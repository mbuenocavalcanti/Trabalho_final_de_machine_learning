<div align="center">

  ![Imagem](Imagens/Cabecalho.png)



# Trabalho final de Machine Learning

Aluna: Mariana Bueno Cavalcanti.

Prof. Responsável: Dr. Daniel R. Cassar.

</div>

### Descrição/Motivação

A toxicidade de nanomateriais depende tanto do material (composição, tamanho, potencial zeta) quanto das condições do ensaio (linhagem celular, tempo de exposição, concentração). Avaliar tudo experimentalmente é caro e lento. Este trabalho investiga até que ponto modelos de aprendizado de máquina conseguem prever a toxicidade a partir dessas variáveis e, principalmente, o quanto o desempenho depende do protocolo de validação.

### Tecnologias Utilizadas:

O projeto foi desenvolvido em Python 3.13.7, com as seguintes bibliotecas:

1. Pandas e NumPy: manipulação e organização dos dados, e operações numéricas.

2. Matplotlib: gráficos de análise.

3. Scikit-learn:

  Pré-processamento: ColumnTransformer e Pipeline encadeiam normalizadores (StandardScaler, MinMaxScaler, MaxAbsScaler, RobustScaler) e codificadores (OneHotEncoder, TargetEncoder), reajustados a cada fold para evitar vazamento de dados.

  Modelos: DummyClassifier (baseline), KNeighborsClassifier, LogisticRegression, RandomForestClassifier, DecisionTreeClassifier e GradientBoostingClassifier.

  Validação: StratifiedGroupKFold, usado na divisão treino/teste e na validação cruzada.

  Métricas: PR-AUC, ROC-AUC, F1, MCC, recall, precisão, acurácia e matriz de confusão.

4. Optuna: otimização de hiperparâmetros com amostragem bayesiana (TPE), com no mínimo 100 tentativas por modelo e PR-AUC como métrica otimizada.

### Conteúdos do Repositório
Este repositório possui todos os códigos, no notebook jupyter, necessários para realizar as predições, bem como os dados utilizados em arquivos csv e os gráficos da Análise Exploratória do dados.


### Dados
Fonte: [https://github.com/mcurcumin/mayoufu-rcs-I-ML-Predicts-Antitumor-Effects-of-Metal-Metal-Oxide-NMs/blob/main/model.py]

Tamanho: 2.765 medidas, 25 nanopartículas distintas, 621 experimentos distintos.

Alvo: toxicidade binária (0 = não tóxico, 1 = tóxico).

Variáveis numéricas: diâmetro, concentração (µM), potencial zeta, tempo de exposição e descritores do material (χ, soma de χ, número de metais e de oxigênios, massa molar, estado de oxidação, HoF, CA, HOMO, NFL, TX, Eg, Pol, entre outros).

Variáveis categóricas: revestimento, linhagem celular e ensaio.



### Referências
[MA, Youfu et al. Interpretable machine learning models for predicting the antitumor effects of metal and metal oxide nanomaterials. RSC Advances, v. 15, n. 21, p. 17036-17048, 2025. Acesso em: 01 out. 2026.](https://pubs.rsc.org/ra/article/15/21/17036/906739/Interpretable-machine-learning-models-for)

<div align="center">

  ![Imagem](Imagens/Rodape.png)



