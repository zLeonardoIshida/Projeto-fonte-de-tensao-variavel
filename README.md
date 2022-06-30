<p align="center">
<a href="https://www.icmc.usp.br/">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c9/Webysther_20170627_-_Logo_ICMC-USP.svg/2560px-Webysther_20170627_-_Logo_ICMC-USP.svg.png" alt="Instituto de Ciências Matemáticas e de Computação" width="150"/>
</a>
</br>
</p>

# Fonte de tensão variável 3-12V

## Descrição

Um projeto orientado pelo professor [Eduardo do Valle Simões](https://gitlab.com/simoesusp), da disciplina de Eletrônica para Computação (SSC0180)

## Participantes

  - Isaac Harim - 13673235
  - Leonardo Ishida - 12873424
  - Luiz Felipe Diniz Costa - 13782032
  - Miguel Bragante Henriques - 13671894

      
## Componentes e cálculos
Confira as informações no slide abaixo.

## Circuito no [Falstad](https://falstad.com/circuit/)
O circuito começa na fonte, à esquerda, que aplica uma corrente alternada. Em seguida, a corrente passa pelo transformador, que reduz a tensão de entrada de 180V para 18,5V. Depois, passa pela ponte de diodo, responsável por deixar a corrente continua, isto é, sempre positiva. A corrente, após isso, passa pelo capacitor, que atua no ripple, diminuindo a variação da tensão, tornando-a mais constante. Por fim, a corrente chega no bloco final, onde há o diodo de zener, o potênciometro e o transistor. Nesse bloco, ocorre a filtração da voltagem nos 13V pelo diodo de zener e a variação entre 3V e 12V, que depende do potênciometro e do resistor de 2.2kΩ. 

## Circuito no Eagle
No Eagle, temos a representação do circuito na vida real, ou seja, como é na placa. 
## Fonte
Imagens da fonte contruída pelo grupo. 