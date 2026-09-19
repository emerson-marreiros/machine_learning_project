# machine_learning_project
Projeto: Aprendizagem de Máquina

### Questão_1 - Considere a base de dados "spambase" (arquivos anexados com o projeto, https://archive.ics.uci.edu/dataset/94/spambase).

a) Considere o algoritmo double k-means (arquivos anexados).
       
b) Execute o algoritmo double k-means 100 vezes com K ∈ {2, 3, 4} e para cada K com H ∈ {1, . . . , K }. Para cada par (K , H) (executado 100 vezes) selecione o melhor resultado segundo a função objetivo.
       
c) Para cada par (K , H), calcule a silhueta (Sil). Faça o plot Sil × (K , H) e escolha o numero de clusters de objetos: 

    K* = arg max(K ,H Sil((K , H)).
       
d) Para a partição de objetos com K* dada pelo algoritmo double k-means calcule o índice de Rand corrigido. Comente.
       
e) Para o double k-means e melhor resultado segundo a função objetivo com K* mostrar: 
    
    i) a matriz de protótipos dos blocos (G);

    ii) a matrix de confusão da partição de objetos dada pelo algoritmo versus a partição a priori; 

    iv) o plot da função objetivo versus as iterações.



### Questão_2 - Considere 2 versões do dataset "spambase". A primeira com a variavel resposta original (2 classes a priori). A segunda com a variavel resposta com o número de classes igual ao número de clusters de objetos (K*) obtido na questão 1.

a) Use validação cruzada estratificada “30 × 10-folds” para avaliar e comparar os 5 classificadores em cada versão de spambase: 
    
    i) bayesiano gaussiano,
    
    ii) bayesiano baseado em k-vizinhos,
    
    iii) bayesiano baseado na janela de Parzen,
    
    iv) regressão logística,

    v) usando a regra do voto majoritário a partir dos 4 primeiros classificadores. Quando necessario, faça validação cruzada 5-folds nos 9 folds restantes para fazer ajuste de hiper-parametros e depois treine o modelo novamente com o conjunto aprendizagem de 9-folds usando os valores selecionados para os hiper-parametros. Use amostragem estratificada.


b) Obtenha uma estimativa pontual e um intervalo de confiança para cada metrica de avaliação do classificadores (Taxa de erro, precisão, cobertura, F-measure);


c) Usar o Friedman test (teste não parametrico) para comparar os classificadores, e o pós teste (Nemenyi test), usando cada uma das métricas


d) Para a metrica de avaliação F-measure, plot a curva de aprendizagem para os 5 classificadores. Mais precisamente, considere conjuntos de treinamento e teste de (5%, 95%) a (95%, 5%) do conjunto original de treinamento, com passo de 5% (usando amostragem estratificada). Para cada par de conjuntos de treinamento e teste, compute as metricas de avaliação tanto no conjunto de treinamento como no conjunto de teste. Comente.
