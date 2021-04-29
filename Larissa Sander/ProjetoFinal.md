# Projeto Final

## Parte 1

![Circuito 1](https://github.com/larissasander/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Larissa%20Sander/Circuito%201.png)

### Considerando o circuito da figura 01 que representa uma fonte linear com regulador MOSFET, temos o seguinte problema: 

### Qual relação entre a tensão de alimentação do ampop e a tensão de saída? 

Devido ao nível de saturação que o AmpOp possui, temos que a tensão de saída será aproximadamente o valor da tensão de alimentação.

### O que devemos considerar para esse circuito operar como um LDO? 

Para que o circuito opere como um LDO é necessário que haja uma baixa queda de tensão no mosfet.

### Como obter as tensões de alimentação para o AmpOp (VCC e VEE)?

Com um dobrador de tensão, pois a tensão de alimentação deve ser maior que a tensão requerida na saída do regulador somada a queda de tensão VDS. 

### Circuito proposto (01) para a alimentação do AmpOp:

![Circuito 1 para alimentação do ampopo](https://github.com/larissasander/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Larissa%20Sander/Circuito%201%20para%20alimenta%C3%A7%C3%A3o%20do%20ampop.png)

### Utilizando o circuito dobrador de tensão, qual valor de VCC você obtêm para um sinal Vin+ de 12Vrms?

VD4 = 0,7 V
VD5 = 0,7 V
Vin = 12 V
Vcc = 2*Vin*2^1/2-VD4-VD5 = 32,54 V

### Quais problemas apresentam esse circuito? Podemos melhorar?

O problema deste circuito é o ripple de saída, pois ocasiona ruídos na saída. A solução para este problema seria colocar um regulador linear para eliminar estes possíveis ruídos.

![Circuito 2 para alimentação do ampop](https://github.com/larissasander/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Larissa%20Sander/Circuito%202%20para%20alimenta%C3%A7%C3%A3o%20do%20ampop.png)

### Considere: AmpOp LM324, MOSFET IRF540, VOUT = 15V, IOUT = 1A, vin+ = 12Vrms, vripple_pós_retificador = 1V, considere as quedas de tensão nos diodos de 0,7V.
### Pontos Importantes para iniciar o projeto responda justificando as escolhas.

• Qual a Tensão VGS? Descreva como obter o valor.

Podemos obter a tensão VGS por meio do datasheet (https://www.ti.com/lit/ds/symlink/lm2902.pdf?HQS=TI-null-null-alldatasheets-df-pf-SEP-wwe&ts=1619637315809&ref_url=https%253A%252F%252Fwww.alldatasheet.com%252Fdatasheet-pdf%252Fpdf%252F97343%252FTI%252FLM324.html)

![](https://github.com/larissasander/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Larissa%20Sander/datasheet%20ampop.PNG)

Por meio do gráfico podemos obter que a tensão VGS é 4,5 V.

• Qual a corrente de alimentação do AmpOp?

![](https://github.com/larissasander/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Larissa%20Sander/datasheet%20corrente%20ampop.PNG)

Obtemos por meio do datasheet que: Corrente de alimentação (Icc) = 1 mA até 3 mA.

• Qual a tensão de alimentação do AmpOP?

![](https://github.com/larissasander/ELN22104_2020_2/blob/prof-lohmann-Alunos_01/Larissa%20Sander/datasheet%20ampop%20tens%C3%A3o.PNG)

A tensão de alimentação é 32 V (máx).

• Qual fator devo considerar para escolher o transistor Q1?

O beta precisa ser elevado.

• Qual valor da tensão do diodo zener D6?

VGS = 4,5 V 

Vout = 15 V

Vo = Vout + VGS

Vo = 19,5 V

A tensão do diodo Zener tem que ser maior que 19,5 V. 

• Como escolher o diodo zener D6, maximizando a eficiência energética e minimizando os ruídos no circuito?

Para isto é necessário escolher um diodo que possua a menor impedância possível, evitando assim oscilações na corrente.

• Considere que, por alterações futuras no circuito, o AmpOp poderá ter uma aumento de 10mA na corrente de alimentação, o circuito proposto continuará funcionando?


## Parte 2

## Parte 3
