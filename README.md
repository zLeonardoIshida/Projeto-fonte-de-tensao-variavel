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
<<<<<<< HEAD
			<td><strong>VALORES (R$)</strong></td>
=======
			<td>VALORES (R$)</td>
>>>>>>> 0ec299579a404cff3c77aec04225517519195542
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
Tem como objetivo transformar a diferença de potencial de pico de 179v, vinda da tomada, para uma tensão próxima de 18V.

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

<<<<<<< HEAD
<p>
<h3>Potenciômetro</h3>


- É, resumidamente, um resistor variável. 

- Tem como objetivo regular a tensão e corrente que passa pelo transistor.

- Usamos um potenciômetro de 5kΩ, que permite que a tensão varie de 3 a 12V, isto é, o valor proposto. 
<p align="center">
</br>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c9/Webysther_20170627_-_Logo_ICMC-USP.svg/2560px-Webysther_20170627_-_Logo_ICMC-USP.svg.png" alt="Instituto de Ciências Matemáticas e de Computação" width="150"/>
</p>

=======
>>>>>>> 0ec299579a404cff3c77aec04225517519195542
</p>

## Circuito no [Falstad](https://falstad.com/circuit/)
O circuito começa na fonte, à esquerda, que aplica uma corrente alternada. Em seguida, a corrente passa pelo transformador, que reduz a tensão de entrada de 180V para 18,5V. Depois, passa pela ponte de diodo, responsável por deixar a corrente continua, isto é, sempre positiva. A corrente, após isso, passa pelo capacitor, que atua no ripple, diminuindo a variação da tensão, tornando-a mais constante. Por fim, a corrente chega no bloco final, onde há o diodo de zener, o potênciometro e o transistor. Nesse bloco, ocorre a filtração da voltagem nos 13V pelo diodo de zener e a variação entre 3V e 12V, que depende do potênciometro e do resistor de 2.2kΩ. 

## Circuito no Eagle
No Eagle, temos a representação do circuito na vida real, ou seja, como é na placa. 
## Fonte
Imagens da fonte contruída pelo grupo. 
