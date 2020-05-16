teste: 

O funcionamento do algoritmo consiste em, após passados os parâmetros solicitados, encontrar um caminho ótimo entre uma ORIGEM até um DESTINO. O MAPA foi construído com base em um grafo, onde os nós são os pontos dados como CIDADES e as arestas são os caminhos entre elas. Cada aresta é ponderada com uma distância.

Em cada ponto de origem são depositadas um número N de formigas que atualizam, a cada iteração, a taxa de ferômonio contida em cada aresta, o que influencia na decisão de qual caminho a próxima formiga deve tomar.

Para fins de testes, foram utilizados os seguintes parâmetros:

ORIGEM:

DESTINO: 

COEFICIENTE DE EVAPORAÇÃO: 

NÚMERO DE ITERAÇÕES: 

VELOCIDADE DE EXECUÇÃO: 

NÚMERO DE FORMIGAS: 1000000000

##########################################################

PARA EXECUTAR O CÓDIGO, BASTA EXECUTAR O SEGUINTE COMANDO:

python3 main.py

##########################################################


Formigas  >

Formigas Artificiais depositando e seguindo  trilhas de ferormônio*


Cada Formiga viaja aleatoriamente de uma cidade para outra favorecendo cidades + próximas  

** Rastro ( Partículas dispersivas de vírus viajam, se concentrando em distancias menores ***

Quando vai de uma cidade a outra a formiga deposita feromônio na trilha 

Maior Rota *- Menor Ferormônio 

Maior Distancia  - Menor Contaminação 

 Ferormônio evapora com o tempo :   

*14 dias de incubação vírus  / 1 mês de sobrevivência  - ( coeficiente de evaporação 14/30)= 0,4

Rotas menos reforçadas- Cidade menos infectadas  
- Índice de contaminação menor


A escolha do caminho mais curto permite 
que as formigas minimizem o tempo gasto 
na viagem entre o ninho e a fonte de 
alimento


** Rastro de virus em cidade vizinhas ou pessoas mais próximas -maior velocidade de contaminação   

viagem entre ninho e fonte  - Infectado --- 2º—infectado  



Grafo A,B – Caminho mais curto  -( Distancia menor / Cidade Vizinha )




 Coleta mais rápida minimiza risco de que a 
fonte de alimento seja achada e monopolizada 
por um competidor mais forte, como uma 
colônia maior.

* Açoes de  combate minimiza o contágio

-Qual a melhor ação de combate ?? 



***Depois que todas as formigas 
completaram suas viagem, os elos que 
pertencem ao maior número de rotas 
mais curtas terão mais 
feromônio
depositado


Depois que o os infectados concluir a cadeia de infeccção,  os lugares que pertencem á lugares com menor distanciamento social terá maior concentração [


Repetindo o processo várias vezes, é 
possível encontrar progressivamente as 
rotas mais curtas.

**Distanciamento menor--- maior rastro---maiores casos 



Ao depositar 
feromônios
em uma aresta, 
a formiga aumenta as chances dessa 
aresta ser selecionada por outra formiga.------------------**

A presença de um infectado em um lugar aumenta á chances desse lugar ter mais um infectado  


Reforça a trilha que passa por esta aresta.
◦
O reforço positivo favorece a seleção de 
caminhos mais curtos.-------------------------------------------Maior número de casos em razão do  distanciamento social . 








A probabilidade de uma aresta ser inclusa na 
solução sendo construída é função do 
desejo heurístico e da trilha de  feromônio




* A probabilidade de um lugar ser colocado na cadeia de contaminação( apresentar casos ) é função da probabilidade de um infectado ir para este lugar

Desejo Heurístico: 

Probabilidade da formiga se mover para um nó.----- Probabilidade de um infectado passar no local .


Atualização de trilhas de 
feromônio

As quantidades de 
feromônio
nas arestas 
do grafo são atualizadas

* Atualização do número de casos

Colônia de formigas que será usada para 
construir a solução no grafo.------------------------------- Cadeia de infectados
◦
Regra de transição probabilística
 responsável por determinar o próximo nó do 
grafo para qual a formiga irá mover------------------------------Onde haverá uma nova colonia( Onde haverá maior concentração) 


Desejo heurístico- que irá influenciar a 
probabilidade da formiga se mover para dado nó. -------------Probabilidade de haver casos de virus no local 
◦
Nível de 
feromônio de cada aresta que ----------------ARESTA BOA= Caminho favorável para contaminação -Maior rastro viral=maior número de infectados 
indicará quão boa ela é.



ACO--TCP


O objetivo é encontrar a rota mais curta conectando 
cidades, sendo que cada cidade deve ser visitada apenas 
uma vez.


Descrever cidades vizinhas dentro da cadeia de contaminação   conectando cidades **
Simular com cidades pequenas  geograficamente  – menor aglomeração 
Simular com cidades grandes  - Maior aglomeração  
Basta apenas um passo de um infectado no lugar  **

Para cada formiga, a transição da cidade para a cidade na iteração depende de:

A cidade ter sido visitada ou não 

Independente do número de casos, se a cidade apresentar pode vir a formar colonia ( cadeia de contaminação)


As formigas precisam ter memória para saber as 
cidades que já 
visitaram


Memoria Imunológica Viral  - 
Se o organismo entrar em contato com qualquer agente infeccioso, ele desenvolverá linfócitos especiais, que são chamados de células da memória, capazes de reconhecer esse agente infeccioso. Essas células permanecem em nosso organismo pelo resto de nossas vidas, mesmo sem termos nenhum tipo de contato com esse agente infeccioso.

Se tivermos contato com um agente infeccioso e se este for reconhecido pelas células de memória, os linfócitos deverão se reproduzir, com o objetivo de debelar os agentes infecciosos. Esses agentes, portanto, serão descartados do organismo sem que tenham causado prejuízo.


Se um lugar tiver contato com um infectado, o sistema reconhecerá os próximos infectados    ((( Sistema de diagnóstico terceira fase)


API – CIDADES QUE JÁ POSSUEM CASOS.


O número de formigas é um parâmetro 
importante do algoritmo

O número de infectados(casos) é um parametro importante  “***( Usar API) 

Poucas formigas resultam em comportamento 
cooperativo insuficiente por conta da taxa de decaimento do feromônio

Poucos infectados –menor probabilidade de formar um surto 


O desempenho cai com uma grande quantidade de 
cidades

O algortmo diminui a precisão para quantidades grandes de cidades--(Usar o modelo atualizado de dorigo) 













Necessário a instalação de algumas dependencias para a execução, testes e demonstração do projeto.

sudo pip install networkx && sudo pip install matplotlib && sudo pip install numpy && sudo pip install pandas && sudo pip install seaborn

** A interface gráfica é a execução do projeto kivi > 1.9

Instalar e verificar documentação sobre como implementá-la

Demais dependências já resolvidas na instalação do python 3.5 ou superior






