# Deep_Learning_Lightning_initialization_optimization
Os efeitos dos processos de inicialização e otimização em deep learning de funções de peso e custo.

## O que em um modelo de Deep Learning está realmente sendo aprendido?

  Valores de pesos. A mudança dos valores respectivamente em suas funções faz o modelo de deep learning ser validado. A funções usam os melhores valores. Relacionando os valores de entrada com saída. O aprendizado é a adequação destes valores para o melhor cenário. A formulação matemática do modelo direciona os valores à otimização. Quando o modelo já treinado receber novos valores de entrada será capaz de aplicar essa formulação e prever uma saída.

## Quando começo um modelo de deep learning sabe-se os valores ideais de pesos?

  NÃO! Se caso já soubesse esses valores nem precisaria de deep learning. Um observação vale ser ressaltada, dependendo dos valores que são inicializados o aprendizado poderar ter diferentes desempenhos. Rapidez e precisão são as variáveis relevantes. A comparação do modelo previsto ao valor real gera um erro. Em cada passada podemos calcular a função de custo/perda/erro. Otimizar a função para achar os melhores valores nas proxímas passadas. Isto é o aprendizado!
  Chamamos o processo de inicialização em Deep Learning a atribuíção de valores iniciais dos pesos das camadas da rede neural antes do treinamento. A escolha adequada dos valores iniciais é importante para garantir que a rede converge para uma solução ótima durante o treinamento. Existem várias técnicas diferentes de inicialização, como inicialização aleatória, inicialização com zero. inicialização com valores pequenos próximos a zero, entre outras. Algumas técnicas são mais adequadas para certos tipos de redes neurais ou certos tipos de problemas. Em geral, é importante experimentar diferentes técnicas de inicialização e escolher a que melhor funciona para o problema específico.

## O que é o processo de otimização?

  O processo de otimização em Deep Learning é o processo de encontrar os melhores pesos para a rede neural, de modo que ela possa realizar bem em tarefas específicas, como classificação ou regressão. Existem vários algoritmos diferentes de otimização que podem ser usados, mas os mais comuns são: 

  ### Gradiente Descendente (SGD): 
  Este é o algoritmo de otimização mais básico e amplamente utilizado. Ele utiliza a derivada da função de perda para atualizar os pesos da rede, movendo-os na direção oposta do gradiente.

  ### Gradiente Descendente Estocástico (SGD):
    Este é similar ao SGD, mas ao invés de usar todos os exemplos de treinamento para calcular o gradiente, ele utiliza apenas um subconjunto (batch) de exemplo para calcular o gradiente. Isso é útil para lidar com grandes conjuntos de dados.

    ### Momentum:
    Este algoritmo adiciona uma compenente de inércia às atualizações de peso, permitindo que a rede passe por regiões de baixa inclinação mais rapidamente.

    ### Adagrad:
    Este algoritmo adapta a taxa de aprendizado para casa parâmetro de forma independente, permitindo que a rede aprenda mais rapidamente para alguns parâmetros e mais devagar para outros.

    ### Adadelta:
    Este algoritmo é semelhante ao Adagrad, mas ao invés de ajustar a taxa de aprendizado para cada parâmetro, ele ajusta o tamanho do passo para cada parâmetro.

    ### Adam:
    Este algoritmo combina elementos de Adagrad e Momentum, adaptando o tamanho do passo para cada parâmetro e incluindo uma componente de inércia nas atualizações de peso.

    ### RMSprop:
    Este algoritmo é similar ao Adagrad, mas ele utiliza uma médida móvel exponencial para ajustar a taxa de aprendizado para cada parâmetro.

    Cada algoritmo tem suas próprias vantagens e desvantagens e o melhor algoritmo a ser usado dependerá do problema específico e da arquitetura da rede.
