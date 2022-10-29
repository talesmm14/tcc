# 1. TRABALHO DE CONCLUSÃO DE CURSO UNITINS
ORIENTADOR: Prof. Me. Marco Antonio Firmino De Sousa
ALUNO: Tales Monteiro Melquiades

## 1.1. Entrega

- [ ] Introdução
- [X] Objetivos e Escopo de Pesquisa
- [X] Escopo de Pesquisa
- [X] Justificativas
- [X] Revisão bibliométrica
- [ ] Trabalhos Relacionados
- [ ] Metodologia
- [ ] Resultados
- [ ] Conclusão


## 1.2. Resumo

A leitura de dados vindos de sensores em tempo real sempre foi uma tarefa difícil e custosa. Há uma grande quantidade de ruído proveniente da baixa qualidade dos sensores, que produzem uma imensa quantidade de dados imprecisos e incorretos, atrapalhando a tomada de decisão de sistemas embarcados. O problema é muito estudado pela comunidade científica, diversos trabalhos apontam diferentes formas de tratar e ignorar ruídos advindos de sensores. Notou-se a grande presença de artigos recentes que aprofundam o assunto em diversas áreas do conhecimento como a leitura de dados tem um papel critico e decisivo ao resultado final, os quais são tratados e apresentados aqui com uma revisão bibliométrica que apresenta uma visão dos termos, artigos e autores dos último 5 anos deste a concepção deste trabalho. Neste trabalho foram implementadas funções de filtro populares e uma função de filtragem probabilística, em um repositório de código aberto apelidado de zscilib, focado em um conjunto de funções úteis para computação científica no contexto de dispositivos de hardware embarcado, desenvolvido especialmente para o sistema operacional de tempo real Zephyr mantido pela fundação Linux. 

As contribuições aqui propostas serão integradas a comunidade de código aberto e servirão para que outros pesquisadores, estudantes e atuantes da área possam usufruir e contribuir com a implementação código proposto.

Mudar aonde, e tirar final



## 1.3. Introdução




### 1.3.1. Organização do Trabalho
Este trabalho está organizado da seguinte forma, para o capítulo 1 apresentou-se a introdução da pesquisa, com dados e justificativas baseadas na bibliografia de suas áreas, contendo também os objetivos do trabalho, além do escopo e justificativas. Já no capítulo 2 apresenta-se uma revisão bibliométrica acerca dos trabalhos relacionados e do escopo deste projeto. O capítulo 3 contém aspectos da metodologia adotada e os requisitos necessários, com o capítulo 4 trazendo as conclusões retiradas desta pesquisa, com suas possíveis contribuições e benefícios para a sociedade, comunidade científica e interessados no tratamento de dados ruidosos.

## 1.4. Objetivos e Escopo de Pesquisa

### 1.4.1. Objetivos
```OKR 
Eu vou **desenvolver uma biblioteca c** para ser usada em qualquer RTOS, no auxiliar da **filtragem de dados** ruidosos ou discrepantes coletada de sensores. 
```
Visto a exorbitante quantidade de dados provindo de sensores, somando a incerteza da qualidade de fabricação dos componentes eletrônicos de baixo custo disponíveis em ampla quantidade no mercado, torna o desenvolvimento para sistemas criticos que dependem da veracidade dos valores provindos dos sensores, ambiente assíncrono com múltiplas tarefas em simultâneo, complexos e custosos para as equipes de engenheiros de software, que utilizam de tempo para garantir a integridade e veracidades de todos os valores. 

Com isso em mente o trabalho aqui proposto se dispõem de construir uma biblioteca de código aberto, que disponibilizara funções adequadas para a filtragem de dados provindo de sensores em ambiente de tempo real com multitarefas, testando a coleta e filtragem de dados no processador dual core ESP32 no sistema operacional de tempo real Zephyr.

#### 1.4.1.1. Objetivos Secundários
- Desenvolver uma biblioteca c de filtragem de dados

- Escrever código amigável a utilização em Sistemas Operacionais de Tempo Real

- Realizar uma revisão bibliométrica de trabalhos que utilizam de métodos probabilísticos para filtragem de dados de sensores   

- Disponibilizar o código de forma aberta a comunidade, para que possa ser utilizado por qualquer outro interessado em tratar dados de sensores em ambiente de multitarefas

- Escrever funções de filtragem utilizando os métodos de **Desvio padrão** e **Intervalo de confiança**

#### 1.4.1.2. Escopo de Pesquisa

O escopo desta pesquisa abrange um conjunto de funções escritas na linguagem C para a filtragem de dados indesejáveis vindos de sensores diversos, funções quais... , tento como característica atuar de forma amigável junto a um sistema operacional de tempo real. Assim, em um primeiro momento considerou-se desenvolver e testar a biblioteca sobre o Chip ESP32 da fabricante Espressif e em conjunto com o sistema operacional Zephyr um projeto mantido pela Fundação Linux.  

## 1.5. Justificativa

Dados provindos do mundo real são constantemente contaminados com ruídos ou podem não corresponder a realidade, esse tipo de situação pode afetar perigosamente um programa de computador qualquer que lida com dados de sensores. Muitos programas podem depender que essa resposta deva ser rápida o suficiente para não comprometer o desempenho e a segurança do programa, um veiculo automato ou um equipamento medico por exemplo não podem trabalhar com dados incorretos, mesmo que sejam em curtos períodos de tempo, os mesmos dependem que a resposta vinda dos sensores sejam rápidas e verdadeiras, com as respostas discrepantes sendo descartadas não comprometendo sua missão. Assim então este trabalho visa contribuir com a construção de uma biblioteca na linguagem C é de código aberto, onde será oferecido funções para tratamento de dados ruidosos advindos do mundo real, cuidando de se preocupar em trabalhar em conjunto com o RTOS Zephyr, economizando tempo de desenvolvimento e centralizando código aberto para todo e qualquer projetista de software interessado em consumir e contribuir ao projeto.

## 1.6. Trabalhos Relacionados
```` Revisar essa introdução!! ````

Aqui será dedicado a descrever os trabalhos relacionados, descrevendo cada um dos estudos e abordando seus pontos fortes e fracos.

O autor (ZHUANG et al., 2007) <!-- \cite{International_Conference__Zhuang} --> propõem uma abordagem de limpeza de dados de sensores, com um algoritmo de média móvel ponderada inteligente que coleta dados já validados e realiza com eles um calculo de média móvel ponderada, comparando a mesma com o calculo de média móvel. Em (NARKHEDE; DESHPANDE; WALAMBE, 2019)<!-- \cite{particle_swarm__Narkhede} --> o artigo apresenta um novo procedimento para a limpeza de dados ruidosos advinda de sensores, utilizando uma técnica de otimização de enxame de partículas demonstrando a viabilização do algoritmo. No livro (ELNAHRAWY; NATH, 2003) <!-- \cite{Statistical_approach__Elnahrawy} -->


## 1.7. Revisão Bibliométrica

<!-- TODO: Inserir descrição de alguns artigos encontrados -->

Nesta seção são consideraras as informações referentes á produção acadêmica mundial, que abordam os termos em ingles Noise reduction, noise abatement, Filtering algorithm e Sensor, significando em sequencia redução de ruído, algoritmos de filtragem e sensores. 

Ambos os tópicos foram pesquisados na base IEEE Xplore, com a busca limitada aos termos noise reduction e noise abatement no titulo do documento e filtering algorithm, sensor e noise reduction apenas no texto completo, delimitando exclusivamente aos artigos de 2018 a 2022. Resultando em 675 resultados sendo eles 450 conferencias, 215 artigos, 8 artigos com acesso  antecipado e 2 revistas, foi realizado uma revisão bibliométrica sobre estes 215 artigos resultantes. 

Dados provenientes de sensores são constantemente bombardeados com interferências aleatórias do ambiente onde se encontram, também devido a baixa qualidade provenientes dos sensores de baixo custo disponíveis, inserindo valores incorretos que são caracterizados como ruídos nas amostras. Esse problema desperta um grande interesse de pesquisadores, que buscam lidar com o tratamento e a filtragem de dados ruidosos provindos de sensores diversos, o artigo \cite{chiang_noise_reduction_in_ECG} se destaca por ser o trabalho mais citado nessa pesquisa bibliométrica, o mesmo aborda o problema da interferência de ruídos nos sinais provindos dos sensores de eletrocardiograma, esses dados podem ser contaminados por fatores como a estática da pele ou mesmo pela respiração do paciente, para isso técnicas como wavelet são muito populares, utilizadas para filtrar dados cancelando o ruído analisando mudanças bruscas ou picos na frequência do sinal, o método de decomposição do modo empírico também e bastante utilizado, definindo fronteiras entre o local máximo e mínimo de uma subtração de sequencia que consequentemente ajudam na triagem do tratamento do sinal.   

...

A Figura ... representa um mapa de visualização de rede, onde podemos visualizar os termos mais predominantes. Aqui são percebidos o termos que se repetiram mais de 5 vezes nos textos e resumos, nota-se a formação de grupos de acordo com suas áreas de atuação, alguns termos em destaque são em azul relacionados a motores, vibrações e forças mecânicas, os em verdes referentes a componentes eletrônicos, roxo a sensores ópticos, amarelo o tratamento de imagem e em vermelho sensores embarcados e processamento de sinais. 

![alt text](anexos/ris/IEEE/Noise_reduction_and_noise_abatement_andsensor_filtering_algorithm/network_visualization_with_lines.png "Title")
<!-- ![alt text](anexos/ris/IEEE/Noise_reduction_and_noise_abatement_andsensor_filtering_algorithm/network_visualization.png "Title") -->

Todos essas expressões aprofundam a problemática no qual tratamento de ruídos, algoritmos de filtragem e sensores estão correlacionados, indo de problemas em programas de computador a desenvolvimento de circuitos eletrônicos e peças mecânicas. O error na fabricação de sensores ópticos pode levar a fenômenos de interferência nos resultados \cite{liu_interference_stripe}, essas anomalias prejudicam sistemas de medição holográfica digital, afim de melhorar a captação de imagens sem ruído o autor propõem um novo método de processamento de imagem utilizando pirâmide laplaciana para destacar o ruído de faixa de interferência.
Em \cite{duarte_speckle_noise} afim de melhorar aplicações biomédicas em imagens de ultrassom, o trabalho descreveu 27 técnicas para tratamento eliminação de ruido em em imagens de ultra-som, essas imagens são de verdadeira importância para o diagnóstico clínico e procedimentos terapêuticos não invasivos, fundamentais em diversas áreas da saúde.


![alt text](anexos/ris/IEEE/Noise_reduction_and_noise_abatement_andsensor_filtering_algorithm/overlay_visualization_cites.png "Title")

A figura ... apresenta um mapa semelhante a figura anterior, onde podemos notar os autores mais citados destacando-os pelo tamanho e sua presença media em artigos mais recentes marcado pela cor mais amarela.

Na Figura .. abaixo podemos visualizar um mapa de sobreposição, onde os vocabulários mais amarelos representam os que se encontram em publicações em media mais recentes, também podemos notar a relação entre as palavras encontradas em todos os títulos e resumos. 

![alt text](anexos/ris/IEEE/Noise_reduction_and_noise_abatement_andsensor_filtering_algorithm/overlay_visualization.png "Title")
<!-- ![alt text](anexos/ris/IEEE/Noise_reduction_and_noise_abatement_andsensor_filtering_algorithm/overlay_visualization_zoom.png "Title") -->

Há de se notar que os termos filtragem e algoritmos de filtragem se destacam pela sua quantidade acima da media de trabalhos mais recentes, não se distanciando das definições de redução de ruído, sensores e algoritmos de processamento de sinais próximos do centro do mapa.

#### 1.7.0.1. Conclusões sobre a Revisão Bibliométrica realizada
Percebesse que o estudo na área de tratamento de dados de sensores concentra-se em média uma grande quantidade de trabalhos recentes, com diferentes abordagens de como remover ou reduzir dados ruidosos, apresentando a ideia de que o tema e de interesse atual da comunidade acadêmica mundial. A diversos ramos nos quais tratamento e eliminação de ruídos de sensores podem peregrinar, podendo verificar a ocorrência dos termos em problemas que não necessariamente estão interessados na obtenção do sinal limpo, mas sim na caracterização e coleta dos ruídos na amostra ou que fogem do escopo deste trabalho com a eliminação de ruído, sendo feita através de equipamento físico.

## 1.8. Metodologia

### 1.8.1. Tabela de referencias

Aqui serão apresentados os 5 artigos recentes do ano de 2022 relacionados a esse trabalho, tendo suas vantagens e desvantagens levantadas com relação aos seus métodos propostos e uma breve descrição do trabalho.

| Referência              | Vantagem                                                                           | Desvantagem                                                                                                                         | Descrição                                                                                                                                                                                                                                     |
| ----------------------- | ---------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| \cite{Arab_LSTM_ResNet} | Algoritmo pode ser treinado em tempo real e acompanhar diferentes tipos de ruídos. | Necessita de uma grande quantidade de dados já coletados para treinamento, exigência de grande capacidade de recurso de computação. | O trabalho propõe utilizar uma técnica de aprendizado profundo para classificar e eliminar ruídos de sistemas de comunicação via micro-ondas, aproveitando-se da aptidão do algorítimo em se adestrasse com os dados coletados em tempo real. |
| \cite{Kamata_mems}      | A técnica pode ser utilizada também para acelerômetros, e viabiliza o uso de componentes de custo baixo e alta precisão. | Limitasse a um ambiente de sensores específicos. | O seguinte estudo propõe uma filtragem para processamento de sinal de um componente eletrônico giroscópio embarcado e avaliando seu desempenho. |
| \cite{Ning_magnetometer} | O método utilizado e adaptativo e abrangente, podendo resolver ruídos dinamicamente. | Os testes não foram realizados durante o processo de coleta de dados. | Aqui os autores implementa uma combinações de filtros para eliminar dados ruidosos em tempo real e compensar a interferência dos erros de um sensor magnético, utilizando de diversos métodos como Auto-Regressão e Média móvel, para modelar a medição de  ruído, afim de excluir dados errados  do resultado final. |
|\cite{Kaan_emg} | Seu comportamento adaptativo exibe uma vantagem em manter os dados coletados o mais proximo possível dos dados reais, sem diminuir a potência do sinal. | Por estar no estado da arte, ainda não apresenta outros estudos comprovando sua utilização em tempo real. | Aqui e proposto um novo método de processamento de dados de sensores de eletromiografia sensível, utilizando um algorítimo adaptativo em tempo real para eliminar os ruídos provindos de fontes elétricas de corrente alternada, sem perturbar os dados reais do sensor, ao qual conseguiu superar cinco alternativas existentes de ultima geração para tratamento de sinal de eletromiografia, mantendo a qualidade do sinal. |
| | | | |


Para este trabalho, a metodologia proposta pode ser resumida da seguinte forma: 


## 1.9. Resultados


## 1.10. Desenvolvimento

## 1.11. Conclusão

## 1.12. Contribuições e Trabalhos futuros

