# Projeto de Automação na Análise de Dados da Crise Global da Água Potável

## Descrição

Este projeto realiza uma análise exploratória e a construção de modelos de Machine Learning para prever a potabilidade da água utilizando o conjunto de dados **Water Potability**.

O objetivo é comparar diferentes algoritmos de classificação e identificar qual apresenta o melhor desempenho para determinar se uma amostra de água é potável ou não.

Além da análise estatística e visual dos dados, o projeto inclui:

* tratamento de valores ausentes;
* balanceamento das classes utilizando SMOTE;
* treinamento de múltiplos modelos;
* comparação de métricas de desempenho;
* registro dos experimentos utilizando MLflow.

---

# Estrutura do Projeto

```
Projeto/
│
├── Projeto_de_Automação_na_Análise_de_Dados_da_Crise_Global_da_Água_Potável_(Equipe_3).ipynb
├── water_potability.csv
├── comparacao_modelos.csv              # Gerado ao final da execução
├── requirements.txt
└── README.md
```

## Arquivos necessários

### Obrigatórios

* `Projeto_de_Automação_na_Análise_de_Dados_da_Crise_Global_da_Água_Potável_(Equipe_3).ipynb`
* `water_potability.csv`

### Gerados automaticamente

* `comparacao_modelos.csv`
* diretório `mlruns/` criado pelo MLflow contendo o histórico dos experimentos.

---

# Dataset

O projeto utiliza o conjunto de dados **Water Potability Dataset**, contendo atributos físico-químicos da água.

Entre as variáveis utilizadas estão:

* pH
* Hardness
* Solids
* Chloramines
* Sulfate
* Conductivity
* Organic Carbon
* Trihalomethanes
* Turbidity

A variável alvo é:

```
Potability
```

* 0 → Água não potável
* 1 → Água potável

O arquivo deve possuir o nome:

```
water_potability.csv
```

e permanecer na mesma pasta do notebook.

---

# Tecnologias utilizadas

* Python 3.10+
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Plotly
* Scikit-Learn
* XGBoost
* Imbalanced-Learn (SMOTE)
* MLflow

---

# Instalação

## 1. Clone o projeto

```bash
git clone <repositorio>
cd <repositorio>
```

ou simplesmente coloque todos os arquivos em uma mesma pasta.

---

## 2. Crie um ambiente virtual (opcional, porém recomendado)

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### Linux/Mac

```bash
python3 -m venv venv

source venv/bin/activate
```

---

## 3. Instale as dependências

Crie um arquivo chamado **requirements.txt** com o seguinte conteúdo:

```text
pandas
numpy
matplotlib
seaborn
plotly
scikit-learn
imbalanced-learn
xgboost
mlflow
jupyter
notebook
ipykernel
```

Em seguida execute:

```bash
pip install -r requirements.txt
```

---

# Configuração

Não é necessária nenhuma configuração adicional.

Apenas certifique-se de que:

```
water_potability.csv
```

está na mesma pasta do notebook.

Caso o notebook seja executado no Google Colab, existe uma célula que utiliza:

```python
from google.colab import files
uploaded = files.upload()
```

Em execução local essa etapa pode ser ignorada, desde que o dataset já esteja disponível na pasta do projeto.

---

# Execução

Inicie o Jupyter Notebook:

```bash
jupyter notebook
```

ou

```bash
jupyter lab
```

Abra o notebook:

```
Projeto_de_Automação_na_Análise_de_Dados_da_Crise_Global_da_Água_Potável_(Equipe_3).ipynb
```

Execute todas as células em ordem.

---

# Fluxo de execução

O notebook realiza automaticamente as seguintes etapas:

## 1. Importação das bibliotecas

Carregamento de todas as dependências necessárias para manipulação de dados, visualização e Machine Learning.

---

## 2. Carregamento do dataset

Leitura do arquivo:

```
water_potability.csv
```

---

## 3. Análise Exploratória

São realizadas análises como:

* primeiras linhas do dataset;
* estatísticas descritivas;
* tipos das variáveis;
* identificação de valores ausentes;
* gráficos de distribuição;
* histogramas;
* mapa de correlação.

---

## 4. Pré-processamento

O notebook realiza:

* identificação dos valores nulos;
* substituição dos valores ausentes pela mediana;
* separação entre atributos e variável alvo.

---

## 5. Divisão dos dados

Os dados são separados em:

* treino (80%)
* teste (20%)

utilizando estratificação das classes.

---

## 6. Balanceamento

Como existe desbalanceamento entre as classes, é utilizado:

```
SMOTE
```

para gerar exemplos sintéticos da classe minoritária.

---

## 7. Padronização

Os atributos são normalizados através de:

```
StandardScaler
```

antes do treinamento da Regressão Logística.

---

## 8. Treinamento dos modelos

São treinados três modelos:

* Regressão Logística
* Random Forest
* XGBoost

---

## 9. Avaliação

Os modelos são comparados utilizando:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC
* Matriz de Confusão
* Classification Report

---

## 10. Comparação

É criada uma tabela contendo todas as métricas dos modelos.

Também são gerados gráficos comparativos.

---

## 11. Registro dos experimentos

O notebook registra automaticamente todas as métricas utilizando:

```
MLflow
```

Cada modelo recebe um experimento contendo:

* Accuracy
* Precision
* Recall
* F1
* ROC-AUC

---

## 12. Exportação

Ao final da execução é criado o arquivo:

```
comparacao_modelos.csv
```

contendo a comparação entre os modelos.

---

# Resultados Esperados

Ao final da execução deverão ser obtidos:

* análise exploratória completa;
* gráficos estatísticos;
* modelos treinados;
* métricas de desempenho;
* matriz de confusão;
* comparação entre modelos;
* arquivo `comparacao_modelos.csv`;
* histórico dos experimentos registrado pelo MLflow.

---

# Executando o MLflow

Caso deseje visualizar os experimentos registrados:

```bash
mlflow ui
```

Depois acesse no navegador:

```
http://127.0.0.1:5000
```

---

# Possíveis Problemas

## Erro ao encontrar o dataset

Verifique se:

```
water_potability.csv
```

está na mesma pasta do notebook.

---

## Erro de biblioteca não instalada

Execute novamente:

```bash
pip install -r requirements.txt
```

---

## Erro relacionado ao Google Colab

A célula:

```python
from google.colab import files
uploaded = files.upload()
```

é exclusiva do Google Colab.

Caso utilize Jupyter Notebook local, essa etapa pode ser ignorada.

---

# Autores

Projeto desenvolvido para fins acadêmicos na disciplina de Ciência de Dados e Machine Learning, com foco na automação da análise da crise global da água potável.
