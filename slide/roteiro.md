# Cumprimentos;
## Identificação do autor, do orientador e do trabalho;

Boa noite senhores avaliadores, boa noite a noite a todos, meu nome e Tales Monteiro Melquiades e o meu orientador e o professor mestre Marco Firmino.

O tema do trabalho e sobre a apresentação de uma alternativa aos métodos de filtragem de dados de sensores utilizando intervalo de confiança.

# Problema e Justificativa;

A pesquisa partiu do seguinte problema, o método de intervalo de confiança pode ser uma alternativa aos métodos tradicionais para obtenção de dados provindos de sensores sem interferência de ruídos.

O mundo moderno é cercado por sensores passivos que coletam dados de praticamente tudo, para monitoramento ou tomada de decisão, hoje em dia a sensores estão des de uma lampada ate em um carro para ajudar em manobras, a maioria desses dispositivos é bombardeada de interferências indesejáveis o tempo todo. Seja pela baixa qualidade dos equipamentos ou pela grande quantidade de intervenções aleatórias de fontes externas, fatores naturais como umidade ou estática, ou ate mesmo interferências vindas de outros mecanismos eletrônicos.

Para lidar com esses dados imprecisos, os engenheiros precisam desenvolver filtros digitais que irão retirar ou descaracterizar um valor impreciso do valor final. Um dos exemplos mais utilizados e a média móvel, que pode suavizar o resultado dando a impressão de resultado livre de ruido.

Mesmo que seja uma das soluções mais utilizadas, essas ainda apresentam alguns problemas, já que o valor provindo por elas não e o dado real vindo do sensor, mas sim um resultado provindo do seu histórico, esses métodos nem sempre acompanham com fidelidade e velocidade esperada em um contexto de tempo real, onde a leitura de picos ou o valor que pode durar alguns segundos e muito importe na tomada de decisão do programa. Por isso e importante capturar o valor real e armazena-lo para um futuro processamento. 

Também e importe visar que em ambiente de sistema embarcado, o processamento e memoria são muito limitados, por isso a importância de um calculo que respeite esses limites e entregue um resultado verdadeiro o mais rápido possível visando estar em ambiente de tempo real.

# Objetivos;

Desse moto o objetivo geral foi avaliar a utilização do método de intervalo de confiança na filtragem de dados provindos de sensores, dentro do contexto de ambiente embarcado, para retornar dados mais confiáveis, livres de ruídos e puros para um posterior processamento de dados ou tomada de decisão em tempo real. 


# Revisão de literatura
## Intervalo de confiança

Intervalo de confiança é um intervalo numérico (como a média ou o desvio-padrão), associado a uma probabilidade, que representa a confiança de que o intervalo contém o parâmetro populacional em questão. Ou seja, baseado na distribuição amostral, podemos obter uma faixa de valores  com uma determinada nível de confiança de conter o valor que estamos analisando. Essa técnica caso seja móvel, busca sempre adaptar-se ao contexto dos dados, e sofre pouca interferência de outliers. 
## Filtragem de dados de sensores

### Revisão bibliometrica
Em cima do tema filtragem de dados de sensores, esse trabalho fez uma pesquisa bibliometrica sobre os termos redução de ruído, algoritmos de filtragem e
sensores. Na base da I3E, no período de 2018 a 2022, resultando em 675 resultados, sendo eles 450 conferencias, 215 artigos, 8 artigos com acesso antecipado e 2 revistas, e fizemos a revisão em cima dos 215 artigos.

# Metodologia;

Aqui foi realizada uma pesquisa experimental, onde utilizamos os dados coletados de um kit de desenvolvimento embarcado com o chip esp32, com um sensor de temperatura termistor de 100k, onde os dados coletados por aproximadamente 2 minutos foram salvos em uma planilha csv e posteriormente analisados com a linguagem python.

## Descrição do DataSet

O conjunto contém 1592 linhas sem valores ausentes, tendo média de 37.19◦c, com os valores flutuando entre 1.05◦c e 97.35◦c graus. Os valores foram coletados no intervalo de aproximadamente 2 minutos, com todos os valores sendo processados na linguagem Python.

# Resultados;

Nesse trabalho a gente utilizou um algortimo que coleta os dados do sensor, armazena em um vetor com tamanho predefinido, realiza o calculo de intervalo de confiança e verifica se o proximo valor esta dentro do intervalo, o ignorando caso não esteja, mas o colocando dentro do vetor de amostras. Retornando apenas quando encontrado um valor dentro do intervalo.

Nesse caso notou-se um problema, caso os valores coletados nunca se encaixem em um intervalo de confiança, o programa poderia ficar por um tempo indeterminado esperando um valor, nisso as rotinas do sistema embarcado poderiam caracterizar como um problema no sistema, reiniciando o programa. Ou em outros casos, comprometendo a operação de um sistema que deve ter uma resposta rápida para estar dentro do contexto de tempo real.

Para tanto foi desenvolvida uma segunda versão do algoritmo, onde e utilizado um tempo limite para coleta de amostras, com o valor sendo retornado ao fim desse tempo mesmo que não esteja dentro do intervalo de confiança.

Esse algoritmo não foi utilizado no dataset aqui em amostra, já que o mesmo não passaria a real característica dos dados coletados e tratados pelo intervalo de confiança, passando a falsa impressão de que alguns dos valores estavam dentro do intervalo.



# Conclusão.

algoritmo proposto é capaz de manipular um vetor de amostra móvel com eficácia, além de manter os dados de forma original mas com o crivo dos valores dentro de um intervalo aceitável de confiança

Mas observou-se problemas importantes, como não
conseguir registrar sinais em curvas muito prolongadas

possibilidade do método ser utilizado em conjunto com outros


Retornando à comunidade de desenvolvimento de filtros digitais em
sistemas embarcados uma alternativa aberta a ser utilizada

### Trabalhos futuros


Utilizar o filtro apresentado com outras funções de filtragem.

Escrever o filtro em uma aplicação real de coleta de dados.
