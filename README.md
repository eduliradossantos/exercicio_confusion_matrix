## Análise de Classificação com Redes Neurais e Métricas de Avaliação

# Descrição

Este projeto implementa uma rede neural para classificação de imagens e calcula métricas de desempenho, incluindo matriz de confusão, sensibilidade (recall), especificidade, precisão e F1-score. O modelo é treinado em um conjunto de dados de imagens e avaliado com base em previsões feitas sobre um conjunto de teste.

# Estrutura do Código

1.  Pré-processamento dos dados:

* Carrega o conjunto de imagens e rótulos.
* Redimensiona as imagens para adequação ao modelo.

2.  Treinamento do modelo:

*  Define a arquitetura da rede neural.
  Treina o modelo usando TensorFlow/Keras.

3.  Avaliação do modelo:

*  Gera previsões sobre os dados de teste.
*  Cria a matriz de confusão e a normaliza para facilitar a análise.
*  Calcula e exibe as métricas de desempenho.


# Tecnologias Utilizadas

Python 3
TensorFlow/Keras
NumPy
Pandas
Matplotlib
Seaborn
Scikit-learn

# Como Executar

Instale as dependências necessárias:

```
pip install tensorflow numpy pandas matplotlib seaborn scikit-learn
```

Execute o script Python:

```
python nome_do_arquivo.py
```

# Métricas Implementadas

1. Matriz de Confusão

Representa a comparação entre as previsões do modelo e os valores reais.

2. Sensibilidade (Recall)

Mede a capacidade do modelo de identificar corretamente as instâncias positivas:

```
recall = recall_score(test_labels, y_pred, average='macro')
```

3. Especificidade

Mede a taxa de identificação correta das instâncias negativas:

```
tn = con_mat[0, 0]
fp = con_mat[0, 1]
specificity = tn / (tn + fp)
```

4. Precisão

Mede a taxa de acertos entre as previsões positivas:

```
precision = precision_score(test_labels, y_pred, average='macro')
```

5. F1-Score

Equilíbrio entre precisão e recall:

```
f1 = f1_score(test_labels, y_pred, average='macro')
```

# Visualização

A matriz de confusão é representada graficamente usando Seaborn:

```
sns.heatmap(con_mat_df, annot=True, cmap=plt.cm.Blues)
```

# Contribuições

Sinta-se à vontade para sugerir melhorias ou relatar problemas criando uma issue ou um pull request neste repositório.


# Licença

Este projeto é distribuído sob a licença MIT.

