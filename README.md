# 1. TRABALHO DE CONCLUSÃO DE CURSO UNITINS
ORIENTADOR: Prof. Me. Marco Antonio Firmino De Sousa
ALUNO: Tales Monteiro Melquiades

## 1.1. Entrega

- [ ] Introdução
- [X] Objetivos e Escopo de Pesquisa
- [X] Escopo de Pesquisa
- [X] Justificativas
- [ ] Revisão bibliométrica
- [ ] Trabalhos Relacionados
- [ ] Metodologia
- [ ] Resultados
- [ ] Conclusão


## 1.2. Introdução


## 1.3. Objetivos e Escopo de Pesquisa

### 1.3.1. Objetivos
```OKR 
Eu vou **desenvolver uma biblioteca c** para ser usada em qualquer RTOS, no auxiliar da **filtragem de dados** ruidosos ou discrepantes coletada de sensores. 
```
Visto a exorbitante quantidade de dados provindo de sensores, somando a incerteza da qualidade de fabricação dos componentes eletrônicos de baixo custo disponíveis em ampla quantidade no mercado, torna o desenvolvimento para sistemas criticos que dependem da veracidade dos valores provindos dos sensores, ambiente assíncrono com múltiplas tarefas em simultâneo, complexos e custosos para as equipes de engenheiros de software, que utilizam de tempo para garantir a integridade e veracidades de todos os valores. 

Com isso em mente o trabalho aqui proposto se dispõem de construir uma biblioteca de código aberto, que disponibilizara funções adequadas para a filtragem de dados provindo de sensores em ambiente de tempo real com multitarefas, testando a coleta e filtragem de dados no processador dual core ESP32 no sistema operacional de tempo real Zephyr.

#### 1.3.1.1. Objetivos Secundários
- Desenvolver uma biblioteca c de filtragem de dados

- Escrever código amigável a utilização em Sistemas Operacionais de Tempo Real

- Realizar uma revisão bibliométrica de trabalhos que utilizam de métodos probabilísticos para filtragem de dados de sensores   

- Disponibilizar o código de forma aberta a comunidade, para que possa ser utilizado por qualquer outro interessado em tratar dados de sensores em ambiente de multitarefas

- Escrever funções de filtragem utilizando os métodos de **Desvio padrão** e **Intervalo de confiança**

#### 1.3.1.2. Escopo de Pesquisa

O escopo desta pesquisa abrange um conjunto de funções escritas na linguagem C para a filtragem de dados indesejáveis vindos de sensores diversos, funções quais... , tento como característica atuar de forma amigável junto a um sistema operacional de tempo real. Assim, em um primeiro momento considerou-se desenvolver e testar a biblioteca sobre o Chip ESP32 da fabricante Espressif e em conjunto com o sistema operacional Zephyr um projeto mantido pela Fundação Linux.  

## 1.4. Justificativa

Dados provindos do mundo real são constantemente contaminados com ruídos ou podem não corresponder a realidade, esse tipo de situação pode afetar perigosamente um software qualquer que lida com dados de sensores. Muitos programas podem depender que essa resposta deva ser rápida o suficiente para não comprometer o desempenho e a segurança do programa, um veiculo automato ou um equipamento medico por exemplo não podem trabalhar com dados incorretos, mesmo que sejam em curtos períodos de tempo, os mesmos dependem que a resposta vinda dos sensores sejam rápidas e verdadeiras, com as respostas discrepantes sendo descartadas não comprometendo sua missão. Assim então este trabalho visa contribuir com a construção de uma biblioteca na linguagem C é de código aberto, onde será oferecido funções para tratamento de dados ruidosos advindos do mundo real, cuidando de se preocupar em trabalhar em conjunto com o RTOS Zephyr, economizando tempo de desenvolvimento e centralizando código aberto para todo e qualquer projetista de software interessado em consumir e contribuir ao projeto.

## 1.5. Trabalhos Relacionados


## 1.6. Revisão Bibliométrica


## 1.7. Metodologia


## 1.8. Resultados


## 1.9. Conclusão

