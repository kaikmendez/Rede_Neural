# Rede Neural para Predição de Desempenho de Alunos

Este projeto utiliza uma rede neural para prever o desempenho de alunos com base em fatores de entrada. A implementação é feita com a biblioteca TensorFlow e Keras, e o processo inclui etapas de pré-processamento, construção e treinamento do modelo.

Descrição do Código
1. Importação de Bibliotecas
As bibliotecas necessárias são importadas, incluindo numpy, pandas, matplotlib, e várias funções do sklearn e tensorflow.keras.

2. Carregamento dos Dados
Os dados são carregados de um arquivo CSV chamado StudentPerformanceFactors.csv. O DataFrame é impresso para verificação e são exibidas informações básicas sobre os dados.

3. Pré-processamento dos Dados
Análise Descritiva: Estatísticas básicas dos dados numéricos são exibidas.
Codificação One-Hot: Colunas categóricas são identificadas e codificadas utilizando OneHotEncoder, que transforma as variáveis categóricas em variáveis binárias (dummy variables).
Separação de Recursos e Alvo: Os dados de entrada (X) são separados das saídas (y), onde Exam_Score é a variável alvo.
4. Normalização
Os dados de entrada são normalizados utilizando StandardScaler para que os modelos de aprendizado de máquina possam convergir mais rapidamente e com mais eficácia.

5. Divisão dos Dados
Os dados são divididos em conjuntos de treinamento e teste, utilizando uma proporção de 70% para treinamento e 30% para teste.

6. Definição do Modelo
Uma rede neural sequencial é construída com as seguintes camadas:

Camada de entrada.
Duas camadas ocultas com 5 neurônios cada, usando a função de ativação ReLU.
Camadas de Dropout são adicionadas após cada camada oculta para ajudar a prevenir o overfitting.
Uma camada de saída com um neurônio, adequada para problemas de regressão.
7. Compilação do Modelo
O modelo é compilado utilizando a função de perda mean_squared_error, o otimizador adam, e a métrica mae (mean absolute error).

8. Treinamento do Modelo
O modelo é treinado com os dados de treinamento por 50 épocas, com um tamanho de lote de 10. O desempenho é validado usando os dados de teste.

Conclusão
Este projeto demonstra a construção de uma rede neural simples para predição, abrangendo desde o pré-processamento dos dados até a avaliação do modelo. O uso de técnicas como a codificação One-Hot e Dropout ajuda a melhorar a robustez do modelo contra overfitting e a eficácia na predição do desempenho dos alunos.
