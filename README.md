# Venda de Carros Toyota Usados
## Modelos de Machine Learning para prever o preço de carros usados com base em suas características


### Projeto desenvolvido utilizando R, com análise exploratória dos dados, estatística descritiva, modelo supervisionado de machine learning (regressão linear e árvore de decisão) para prever o preço de carros usados usando como base de avaliação o critério do negócio.


Os dados e instruções são da certificação de professional data scientist do Datacamp: 
#### Company Background

You have been hired as a data scientist at Discount Motors, a used car dealership in the UK. The dealership is expanding and has hired a large number of junior salespeople. Although promising, these junior employees have difficulties pricing used cars that arrive at the dealership. Sales have declined 18% in recent months.

The sales team have reached out to the data science team to get help with this problem.


#### Customer Question
The sales team wants to know:

● Can you predict the price that a used car should be listed at based on features of the car?

#### Success Criteria
It is known that cars that are more than £1500 from the estimated price will not sell. The sales team wants to know whether you can make predictions within this range.


#### Desenvolvimento e comentários: 
. A maior parte dos veículos a venda são de 2015 até 2019, sendo 2017 o mais comum. 

. A maior parte dos veículos a venda são movidos a petroleo e com transmissão manual. 

. O preço por modelo pode variar principalmente para modelos que estão no mercado há bastante tempo, por exemplo: corolla tem desde veículos bem baratos (mais antigos) até a faixa de preço mais cara (para veículos mais novos). O modelo Supra tem pouca variação de anos, sendo sempre um veículo considerado acima da média nos preços. 

. Analisando o preço somente pelo ano, o padrão de antigo-mais barato, novo-mais caro se mantém, exceto por um Land Cruiser de 1998 que tem preço bem acima da média - o que se explica pelo motor bem superior dele, engineSize de 4.2.

. Veículos menos rodados tendem a ter um preço superior.

. Road tax se explica principalmente pelo ano ou tipo de combustível (hibridos poluem menos = menor imposto)

. MPG (miles per gallon) é indice de economia de combustível e os bem alto ou bem baixo tem preços maiores, o que se justifica pelo combustivel (hibrido consome menos e é mais caro) ou pelo engine size (maiores consomem mais e são mais caros).

. Maiores engine sizes tem preços mais elevados. 

. Usando uma separação de treino/teste de 75%/25% e usando método de regressão linear e árvore de decisão regressão (e transformando as variáveis categóricas em numéricas), foi obtido um rmse (raiz quadrada do erro médio) de 17% em regressão linear e 19% na árvore de decisão na base de teste. 

. Utilizando os modelos em toda a base e avaliando pelo critério do negócio (não ter uma diferença entre o preço real e o previsto em mais de 1500) cheguei em 19,5% de preços fora do critério estabelecido utilizando regressão linear e 18% utilizando árvore de decisão. Ou seja, com ambos os modelos o sucesso foi maior de 80%.

. Como no enunciado foi dito que já havia caído 18% as vendas, o resultado obtido não é tão melhor, portanto há espaço para melhorias que serão aplicadas posteriormente. 

Algumas modificações possíveis:
. Normalizar os dados antes de aplicar os modelos - eles estão em escalas bem diferentes e isso atrapalha o resultado. 

. Utilizar feature engineering para unir features que possam fazer sentido juntas, colocar tax como fatores, unir faixas de mpg com o tipo de combustível...

. Utilizar clustering para verificar grupos similares de carros para melhorar o atendimento ao cliente oferecendo veículos similares ao que ele esteja querendo comprar. 


