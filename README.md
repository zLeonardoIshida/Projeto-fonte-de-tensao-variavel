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

<p>
<h3>Peças utilizadas</h3>

<table align="right">
	<tbody>
		<tr>
			<td><strong>VALORES (R$)</strong></td>
		</tr>
		<tr>
			<td>-</td>
		</tr>
		<tr>
			<td>7,00 (1 unidade)</td>
		</tr>
		<tr>
			<td>0,07 (1 unidade)</td>
		</tr>
		<tr>
			<td>0,14 (2 unidades)</td>
		</tr>
		<tr>
			<td>5,00 (5 unidades)</td>
		</tr>
		<tr>
			<td>0,48 (1 unidade)</td>
		</tr>
		<tr>
			<td>0,69 (1 unidade)</td>
		</tr>
		<tr>
			<td>5,78 (1 unidade)</td>
		</tr>
		<tr>
			<td>TOTAL:   19,16
</td>
		</tr>
	</tbody>
</table>

</br>

- Transformador

- Potenciômetro de 5kΩ linear

- Resistor de 2.2kΩ

- Resistores de 1kΩ

- Diodos N4004 + LED 

- Diodo de Zener 13V 1W

- Transistor NPN

- Capacitor 680uF 25V
</br>
</p>

### Trasformador
> Tem como objetivo transformar a diferença de potencial de pico de 179v, vinda da tomada, para uma tensão próxima de 18V.

<p align="center">
Cálculo da tensão de pico e cálculo da tensão transformada
<table align="center">
	<tbody>
		<tr>
			<td>Vpico = Vrms * √2</td>
			<td>Ven/Vtr = (N1 / N2)</td>
		</tr>
		<tr>
			<td>Vpico = 127V* √2</td>
			<td>179/Vtr = 9,5</td>
		</tr>
		<tr>
			<td>Vpico = 179,60V.</td>
			<td>Vtr = 18,84V</td>
		</tr>
	</tbody>
</table>


### Potenciômetro

- É, resumidamente, um resistor variável. 

- Tem como objetivo regular a tensão e corrente que passa pelo transistor.

- Usamos um potenciômetro de 5kΩ, que permite que a tensão varie de 3 a 12V, isto é, o valor proposto. 
<p align="center">
</br>
<img src="https://github.com/zLeonardoIshida/Projeto-fonte-de-tensao-variavel/blob/main/readmeImagens/potenciometro.png?raw=true" alt="Potenciometro" width="150"/>

### Ponte de diodo
Tem como objetivo retificar a onda de entrada, ou seja, transformar uma tensão de corrente alternada (CA) bifásica em uma tensão monofásica positiva.
Como os diodos precisam de uma tensão mínima de ativação, a tensão sofre uma perda. No nosso projeto, cada diodo consome, aproximadamente, 0,7V.
Por estarem ligados em série, o consumo da tensão é de: 2 * 0,7 = 1,4V.

</br>
<p align="center">
<img src="https://github.com/zLeonardoIshida/Projeto-fonte-de-tensao-variavel/blob/main/readmeImagens/ponte%20de%20diodo.png?raw=true" alt="pontedediodo" width="500"/>
</p>

### Capacitor

Para o cálculo da capacitância, escolhemos utilizar um ripple de aproximadamente 10%.

C = (5 * 100mA) / (16,98 * 60hz)
C = 490uF.

> Foi utilizado um capacitor de 680uF no projeto por ausência de opções para compra.

<p align="center">
<img src="https://github.com/zLeonardoIshida/Projeto-fonte-de-tensao-variavel/blob/main/readmeImagens/ocapacitor.png?raw=true" alt="pontedediodo" width="350"/>
</p>


### Diodo de Zener
Tem como objetivo estabilizar a onda de entrada, ou seja, transformar uma tensão de corrente alternada (CA) em uma tensão de corrente contínua (CC). Como foi utilizado um diodo de zener 13v, a tensão de saída é de aproximadamente 13v

</br>

<table align="center">
	<tbody>
		<tr>
			<td>Assim, a tensão mantém-se próxima dos 13V, o que facilitará o ajuste entre 3 e 12V.</td>
			<td><img src="https://github.com/zLeonardoIshida/Projeto-fonte-de-tensao-variavel/blob/main/readmeImagens/diododezenerl.png?raw=true" alt="pontedediodo" width="200"/></td>
		</tr>
	</tbody>
</table>

### Transistor

Juntamente com o potenciômetro, e o diodo de zener, o transistor faz parte da função de regular a tensão e corrente na saída da fonte.
Foi utilizado o modelo NPN, que é ativado quando há tensão no gate. Quando ativado, o transistor cria um caminho com menor resistência, facilitando a passagem de corrente, evitando, assim, que o diodo de zener queime devido à alta potência.

<p align="center">
<img src="https://github.com/zLeonardoIshida/Projeto-fonte-de-tensao-variavel/blob/main/readmeImagens/transitor.png?raw=true" alt="pontedediodo" width="200"/>
</p>

<h3 align="right">
<a href="https://github.com/zLeonardoIshida/Projeto-fonte-de-tensao-variavel/blob/main/Apresenta%C3%A7%C3%A3o%20em%20Slides.pdf" target="_blank">Apresentação em Slides</a>
</p>

## Circuito no [Falstad](https://tinyurl.com/2gs8bmub)
O circuito começa na fonte, à esquerda, que aplica uma corrente alternada. Em seguida, a corrente passa pelo transformador, que reduz a tensão de entrada de 180V para 18,5V. Depois, passa pela ponte de diodo, responsável por deixar a corrente continua, isto é, sempre positiva. A corrente, após isso, passa pelo capacitor, que atua no ripple, diminuindo a variação da tensão, tornando-a mais constante. Por fim, a corrente chega no bloco final, onde há o diodo de zener, o potênciometro e o transistor. Nesse bloco, ocorre a filtração da voltagem nos 13V pelo diodo de zener e a variação entre 3V e 12V, que depende do potênciometro e do resistor de 2.2kΩ. 

<p align="center">
	<img src="https://github.com/zLeonardoIshida/Projeto-fonte-de-tensao-variavel/blob/main/readmeImagens/falstad.jpeg?raw=true" width="600">
</p>

## Circuito no Eagle
No Eagle, temos a representação do circuito na vida real, ou seja, como é na placa.
<p align="center">
<img src="https://github.com/zLeonardoIshida/Projeto-fonte-de-tensao-variavel/blob/main/readmeImagens/eagle2.jpeg?raw=true" width="400">
<img src="https://github.com/zLeonardoIshida/Projeto-fonte-de-tensao-variavel/blob/main/readmeImagens/eagle1.jpeg?raw=true" width="600">
</p>

## Fonte
Imagens da fonte contruída pelo grupo. 
