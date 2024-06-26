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

## Arquitetura do Modelo

  A arquitetura de Rede Neural Convolucional (CNN - Convolutional Neural Network) é um tipo de modelo de rede neural projetado para processar dados que têm uma estrutura de grade, como imagens. A estrutura da CNN é inspirada na organização do córtex visual do cérebro humano, que tem neurônios que respondem a regiões específicas do campo visual. Uma CNN é composta por uma série de camadas, cada uma das quais executa uma operação específica na entrada de dados.
  ### Camadas de Convolução:
  Essas camadas aplicam filtros a pequenas regiões da entrada, de modo a extrair características visuais importantes como bordas, texturas e formas.
  ### Camadas de Pooling:
  Essas camadas reduzem o tamanho da representação da entrada, mantendo as características mais importantes. Isso ajuda a reduzir a complexidade do modelo e a aumentar a eficiência computacional.
  ### Camadas de Totalmente Conectadas:
  Essas camadas são semelhantes às camadas usadas em redes neurais padrão. Eles recebem as caracteristicas extraídas pelas camadas anteriores e as usam para gerar uma saída.

  As camadas sao organizadas em uma topologia específica que é projetada para extrair características relevantes da entrada e classificar a imagem corretamente. Essa topologia pode variar dependendo da tarefa específica, como classificação de imagem, detecção de objeto, segmentação de imagem, entre outras. As CNNs são amplamente utilizadas em tarefas relacionadas a imagens, como classificação, detecção de objeto, reconhecimento facial, entre outras. Seu sucesso em muitas dessas tarefas se deve em grande parte à sua capacidade de aprender representações hierárquicas de características visuais relevantes, tornando-as muito eficientes para lidar com grandes volumes de dados de imagens.

  A arquitetura ResNet (Nesidual Network) é uma arquitetura de Rede Neural Convolucional (CNN) desenvolvido pela Microsoft Research em 2015. É uma arquitetura profunda que se destaca por suas conexões residuais, que permitem que as informações fluam diretamente das camadas de entrada para as camadas de saída, contornando as camadas intermediárias. Isso ajuda a prevenir o problema de desvanecimento de gradientes, que é comum em redes muito profundas e pode dificultar o treinamento. O ResNet consiste em várias camadas de convolução e normalização, seguidas por blocos residuais. Cada bloco residual é composto por várias camadas convolucionais, que são seguidas por um caminho residual. O caminho residual consiste em uma conexão direta da entrada do bloco à saída do bloco, o que permite que as informações fluam diretamente da entrada para a saída, sem passar por todas as camadas intermediárias. A ResNet é conhecida por sua capacidade de criar modelos muito profundos e poderosos, com um número muito grande de camadas. Por exemplo, a ResNet-152 tem 152 camadas e ainda pode ser treinada com sucesso em tarefas de reconhecimento de imagem. A arquitetura ResNet tem sido usada com sucessso em várias tarefas relacionadas a imagens, como classificação de imagens, detecção de objetos, segmentação de imagens, entre outras. Ela é considerada uma das arquiteturas mais influentes e eficazes em tarefas de visão computacional, tendo ganhado várias competições de reconhecimento de imagem, como o ImageNet Large Scale Visual Recognition Challenge (ILSVRC).

### Função de Inicialização dos Pesos
  nn.init.kaiming_uniform_ é uma função de inicialização de pesos do PyTorch que implementa a técnica de inicialização He uniforme, proposta por He et al. em 2015. A inicialização He uniforme é uma técnica popular de inicialização de pesos que é usada comumente em redes neurais que usam ativações ReLU. A ideia por trás dessa técnica é que a inicialização aleatória dos pesos deve ser feita de tal maneira que a saída de cada camada tenha aproximadamente a mesma variância da entrada. Isso evita o problema de gradiente explodindo ou desaparecendo que pode ocorrer em redes neurais profundas. O argumento mode na função nn.init.kaiming_uniform_() especifica qual dos dois valores deve ser usado no denominador da equação: fan_in ou fan_out. O valor padrão para o argumento mode é fan_in, que significa que o denominador da equação será definido como o número de entradas para a camada.

### Função para o Loop de Treinamento
Cria-se 3 funções para auxiliar no treinamento do modelo. Começa-se com a função de avaliação.
@torch.no_grad() é um decorador usado no PyTorch para desativar o restreamento de gradiente durante uma passagem de inferência ou validação em um modelo treinado. Quando um modelo é treinado, o PyTorch mantém o rastreamento dos gradientes dos tensores para atualizar os pesos do modelo durante o processo de treinamento. No entanto, durante o processo de inferência ou validação, não precisam atualizar os pesos do modelo e portanto, não precisamos manter o rastreamento dos gradientes. Ao usar o decorador @torch.no_grad(), podemos desativar o rastreamento de gradiente durante a inferência ou validação de um modelo treinado, reduzindo o uso de memória e aumentando a velocidade de cálculo.

## Conclusão sobre a Inicialização de Pesos
  A inicialização dos pesos teve um impacto menor na performance dos dados, mas isso nem sempre será verdade e o ideal é experimentar diferentes técnicas e comparar os resultados.
