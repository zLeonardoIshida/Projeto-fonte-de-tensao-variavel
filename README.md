# Fonte de tensão variável 3-12V
## Universidade de São Paulo - Instituto de Ciências Matemáticas e Computação
Um projeto orientado pelo professor Eduardo do Valle Simões, da disciplina de Eletrônica para Computação (SSC0180).
Alunos:
  - Miguel Bragante Henriques nUSP: 13671894
  - Leonardo Ishida nUSP: 
  - Isaac Harim nUSP:
  - Luiz Felipe nUSP: 
## Os componentes e nossos cálculos
Confira as informações no slide abaixo.

## O circuito no Falstad
O circuito começa na fonte, à esquerda, que aplica uma corrente alternada. Em seguida, a corrente passa pelo transformador, que reduz a tensão de entrada de 180V para 18,5V. Depois, passa pela ponte de diodo, responsável por deixar a corrente continua, isto é, sempre positiva. A corrente, após isso, passa pelo capacitor, que atua no ripple, diminuindo a variação da tensão, tornando-a mais constante. Por fim, a corrente chega no bloco final, onde há o diodo de zener, o potênciometro e o transistor. Nesse bloco, ocorre a filtração da voltagem nos 13V pelo diodo de zener e a variação entre 3V e 12V, que depende do potênciometro e do resistor de 2.2kΩ. 
## O circuito no Eagle
No Eagle, temos a representação do circuito na vida real, ou seja, como é na placa. 
## A fonte em si
Imagens da fonte contruída pelo grupo. 
