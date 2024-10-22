# Previsão de Score de Crédito com Machine Learning

## Descrição
Este projeto utiliza algoritmos de Machine Learning para prever o score de crédito de clientes com base em suas características, como profissão, comportamento de pagamento e mix de crédito. Foram utilizados dois modelos de aprendizado supervisionado para avaliação: **RandomForestClassifier** e **KNeighborsClassifier**, sendo que o primeiro apresentou maior acurácia nos testes. O código também inclui a capacidade de aplicar previsões em novos clientes após o treinamento dos modelos.

## Funcionalidades
1. **Importação e Preparação dos Dados**: Importa a base de dados `clientes.csv`, realiza o pré-processamento necessário e transforma as variáveis categóricas em numéricas utilizando o `LabelEncoder`.
2. **Treinamento de Modelos de Machine Learning**: Utiliza dois modelos: 
   - **RandomForestClassifier**
   - **KNeighborsClassifier**
3. **Avaliação de Modelos**: Avalia os modelos treinados utilizando o conjunto de testes e mede a acurácia de cada modelo.
4. **Previsão para Novos Clientes**: Aplica o modelo de maior acurácia para prever o score de crédito de uma nova base de clientes (`novos_clientes.csv`).

## Tecnologias Utilizadas
- **Pandas**: Para manipulação e leitura de arquivos CSV.
- **Scikit-learn**: Para aplicação dos algoritmos de Machine Learning e pré-processamento de dados.
  - `RandomForestClassifier`
  - `KNeighborsClassifier`
  - `LabelEncoder`
  - `train_test_split`
  - `accuracy_score`

## Requisitos
- **Python 3.x**
- Bibliotecas:
  - `pandas`: Para instalar, execute `pip install pandas`
  - `scikit-learn`: Para instalar, execute `pip install scikit-learn`

## Como Rodar o Projeto

1. **Instalar Dependências**:
   - Execute o seguinte comando no terminal:
     ```bash
     pip install pandas scikit-learn
     ```

2. **Preparar a Base de Dados**:
   - Certifique-se de ter o arquivo `clientes.csv` com as seguintes colunas:
     - `id_cliente`
     - `profissao`
     - `mix_credito`
     - `comportamento_pagamento`
     - `score_credito`
   - E o arquivo `novos_clientes.csv` contendo os novos clientes sem a coluna `score_credito`.

3. **Rodar o Jupyter Notebook**:
   - Abra e execute o código no Jupyter Notebook para treinar os modelos e gerar as previsões.
   
4. **Ajustar os Modelos (opcional)**:
   - Caso queira ajustar a proporção entre dados de treino e teste, modifique o valor de `test_size` na função `train_test_split`.

## Explicação do Código

### Passo 1: Importar e Preparar a Base de Dados
- A base de dados é carregada usando o **Pandas** e passa por um processo de transformação, onde as colunas categóricas são convertidas em valores numéricos usando o **LabelEncoder**.

### Passo 2: Treinamento dos Modelos
- Os dados são divididos entre treino e teste usando a função `train_test_split`, com 80% dos dados sendo usados para treino e 20% para teste.
- Dois modelos de Machine Learning são treinados:
  - **RandomForestClassifier**
  - **KNeighborsClassifier**

### Passo 3: Avaliação dos Modelos
- Após o treinamento, ambos os modelos fazem previsões no conjunto de teste e a acurácia de cada um é calculada usando a métrica `accuracy_score`.

### Passo 4: Previsão para Novos Clientes
- O modelo vencedor (com maior acurácia) é utilizado para prever o score de crédito de novos clientes a partir de uma nova base de dados (`novos_clientes.csv`).

## Autor
- **Angelo Sequinel**

## Licença
Este projeto não possui licença.
