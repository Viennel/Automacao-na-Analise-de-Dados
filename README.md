# Projeto de Automação na Análise de Dados da Crise Global da Água Potável

## Descrição

Este projeto tem como objetivo realizar a análise exploratória de dados e comparar diferentes algoritmos de Machine Learning para prever a potabilidade da água a partir de características físico-químicas das amostras.

O notebook contempla todo o fluxo de análise, incluindo:

* carregamento dos dados;
* tratamento de valores ausentes;
* análise exploratória;
* balanceamento das classes utilizando SMOTE;
* treinamento de modelos de classificação;
* avaliação dos resultados;
* comparação entre modelos;
* registro dos experimentos utilizando MLflow.

O projeto foi desenvolvido para execução no **Google Colab**.

---

# Estrutura do Projeto

O projeto é composto pelos seguintes arquivos:

```text
Projeto/
│
├── Projeto_de_Automação_na_Análise_de_Dados_da_Crise_Global_da_Água_Potável_(Equipe_3).ipynb
├── water_potability.csv
└── README.md
```

## Arquivos necessários

Para executar o projeto são necessários apenas:

* `Projeto_de_Automação_na_Análise_de_Dados_da_Crise_Global_da_Água_Potável_(Equipe_3).ipynb`
* `water_potability.csv`

---

# Requisitos

Para reproduzir o projeto é necessário possuir apenas:

* Conta Google
* Acesso ao Google Colab
* Navegador de Internet

Não é necessário instalar Python ou bibliotecas localmente, pois toda a execução ocorre no ambiente do Google Colab.

---

# Como executar o projeto

## 1. Abrir o notebook

Faça upload do arquivo

```text
Projeto_de_Automação_na_Análise_de_Dados_da_Crise_Global_da_Água_Potável_(Equipe_3).ipynb
```

para o Google Colab ou abra-o diretamente pelo Google Drive.

---

## 2. Executar a célula de instalação

O notebook possui uma célula inicial responsável por instalar automaticamente todas as bibliotecas necessárias para execução do projeto.

Execute essa célula antes das demais.

---

## 3. Fazer upload do dataset

Durante a execução será exibida uma janela para envio do arquivo de dados através do comando:

```python
from google.colab import files
uploaded = files.upload()
```

Selecione o arquivo:

```text
water_potability.csv
```

---

## 4. Executar todas as células

Após o upload do dataset, execute o restante do notebook na ordem em que as células estão organizadas.

O notebook realizará automaticamente todas as etapas da análise.

---

# Fluxo de execução

O notebook executa automaticamente as seguintes etapas:

## 1. Instalação das dependências

Instalação das bibliotecas utilizadas durante a análise e treinamento dos modelos.

---

## 2. Importação das bibliotecas

Carregamento das bibliotecas de análise de dados, visualização e Machine Learning.

---

## 3. Carregamento do dataset

Leitura do arquivo:

```text
water_potability.csv
```

---

## 4. Análise Exploratória dos Dados

Nesta etapa são realizadas análises como:

* visualização das primeiras linhas;
* estatísticas descritivas;
* identificação de valores ausentes;
* distribuição das variáveis;
* gráficos exploratórios;
* matriz de correlação.

---

## 5. Pré-processamento

O notebook realiza automaticamente:

* tratamento dos valores ausentes;
* separação entre atributos e variável alvo;
* preparação dos dados para treinamento.

---

## 6. Divisão da base

Os dados são divididos em conjuntos de treino e teste utilizando amostragem estratificada.

---

## 7. Balanceamento

É utilizado o algoritmo **SMOTE** para reduzir o desbalanceamento entre as classes.

---

## 8. Treinamento dos modelos

São treinados os seguintes algoritmos:

* Regressão Logística
* Random Forest
* XGBoost

---

## 9. Avaliação dos modelos

Os modelos são comparados utilizando métricas como:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC
* Matriz de Confusão

---

## 10. Registro dos experimentos

Os resultados são registrados utilizando **MLflow**, permitindo acompanhar o desempenho de cada modelo treinado.

---

# Resultados Esperados

Ao término da execução, o notebook apresenta:

* análise exploratória completa;
* gráficos estatísticos;
* métricas de desempenho dos modelos;
* matrizes de confusão;
* comparação entre os algoritmos;
* registro dos experimentos realizados no MLflow.

---

# Observações

* O notebook foi desenvolvido especificamente para o ambiente **Google Colab**.
* O dataset deve ser enviado quando solicitado durante a execução.
* Recomenda-se executar todas as células em sequência para garantir a reprodução correta dos resultados.

---

# Video

* Link para video, elaborando o que foi feito no projeto: https://www.youtube.com/watch?v=IsMEZbfUdWY

---

# Autores

Projeto desenvolvido para fins acadêmicos na disciplina de Ciência de Dados e Machine Learning, com foco na automação da análise de dados relacionados à crise global da água potável.
