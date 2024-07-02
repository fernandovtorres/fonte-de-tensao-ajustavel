# Fonte de tensão ajustável

*Projeto para a disciplina Eletronica para Computação - SSC0180*

# Integrantes do Grupo

- Nicholas Eiti Dan - 14600749
- João Gabriel Araújo de Bastos - 15462633
- Matheus Vieira Fernandes - 14615993
- Fernando Valentim Torres - 15452340

# Sobre o Projeto

Neste trabalho, projetamos uma fonte de tensão regulável 3v a 12v. Para isso, utilizamos a voltagem alternada de 127v 60hz vinda da tomada e transformamos em volatagem contínua utilizando um tranformador e um circuito retificador feito com diodos.

# Tabela dos componentes
| Componente               | Quantidade | Custo por unidade |
|--------------------------|------------|-------|
|Transformador 24.2v        |1          |emprestado|
| Resistor 100 ohms, 2 watts|  2        |  1.70 |
| Transistor NPN            | 4         |  1.55 |
| Resistor 100 ohms, 0.25 watt | 6      |  0.08 |
| Capacitor 840 µF         | 1          |  5.20 |
| Diodos (ponte retificadora) | 4       |  0.20 |
| Zener 13V                | 1          |  0.50 |
| Zener 3.9V (queda de 2.4V) | 1        |  0.37 |
| Potenciômetro 10 kOhms   | 1          |  7.00 |
| LED vermelho             | 1          |  0.50 |
| Protoboard 830 pontos    | 2          | 12.26 |
| Jumpers                  | 27         |  0.70 |
|Resistor 4.7k ohms        |2           |  0.58 |  
|Resistor 2.2k ohms        |1           |  0.60 |
|Resistor 3.3k ohms        |1           |  0.39 |
|Resistor 1k ohms          |1           |  0.59 |
|Resistor 10k ohms         |1           |  0.46 |
|----- | **`TOTAL: 57`** | **`Preço Total: R$ 32,68`** |

# Informações sobre os componentes
- **transformador**: tem o papel de reduzir a voltagem de 127v vinda de uma fonte de corrente alternada (a tomada) para 24.2v, ainda alternada.
- **ponte de diodo**: a ponte de diodo é um arranjo de 4 diodos dispostos de uma forma com que a corrente alternada se tranforme em contínua
- **capacitor**: armazena carga no circuito durante os ciclos, liberando corrente quando a tensão provinda da fonte for menor do que a tensão interna do capacitor. Com base em um cálculo de 4% de ripple, chegamos próximos ao valor comercial de 820uF
- **diodo zener**: quando a voltagem passa de 13v, ele mantém esse valor como máximo em seus terminais, porém quando a voltagem é menor do que 13v, ele não conduz, logo não interfere
- **potenciômetro**: é um resistor regulável que será usado como o controle da tensão final.
- **transistor**: amplifica a corrente com base na resistência do potenciometro.
- **resistores**: utilizado em diversoss momentos no circuito, possui a função de limitar a corrente, o que garante uma certa segurança para os outros componentes do circuito.
- **led**: tem como função indicar quando a voltagem atingir 5 volts na parte final do circuito. de modo geral, não interfere nos valores obtidos no circuito, servindo unicamente como indicação da voltagem e corrente ajustáveis.

# Cálculos

### Antes do transformador:

$$ \ V_{\text{tomada}} = 127\ V \quad \Rightarrow \quad V_{\text{pico da tomada}} = 127 \cdot \sqrt{2} \approx 179,6\ V \ $$

### Após o transformador:

$$ \ V_0\ \text{pico} \approx 179,6 \cdot 0,1533 \approx 26,1\ V \ $$

### Depois da ponte retificadora:

$$ \ V_1\ \text{pico} \approx 26,1 - 2,6 \approx 23,5\ V \ $$

### Buscando a capacitância mínima para um ripple de no máximo 10%:

$$ \ R_{\text{eq}} \approx 230Ω \ $$

$$\ V_{\text{ripple}} = \frac{V_{\text{cc}}}{f \cdot C \cdot R_{\text{eq}}} \quad \Rightarrow \quad 2,35 \geq \frac{V_1\ \text{pico}}{120 \cdot C \cdot R_{\text{eq}}} \ $$

$$ \ \quad 2,35 \geq \frac{23,5}{120 \cdot C \cdot 230} \ $$

$$ \ C \geq \frac{23,5}{120 \cdot 2,35 \cdot 230} \approx 362\ \mu F \ $$

### Com um capacitor de 820µF, é possível obter um ripple de:

$$ \ \frac{10^6}{120 \cdot 820 \cdot 230} \approx 4\\% \ $$


# Imagem do Falstad

![Screenshot from 2024-06-29 16-26-51](https://github.com/fernandovtorres/fonte-de-tensao-ajustavel/assets/54219097/3d010d52-58a6-4602-856b-af1317ef7481)

[Link para o falstad](https://tinyurl.com/2gezskvp)

# PCB no Eagle

![Board](https://github.com/fernandovtorres/fonte-de-tensao-ajustavel/assets/54219097/28a7da90-fae2-4f18-99cf-1c8df9814398)
  
# Esquemático no Eagle

![schematic](https://github.com/fernandovtorres/fonte-de-tensao-ajustavel/assets/54219097/700c18d4-4089-4b3c-9f57-c2d5acd77638)

# Vídeos

https://github.com/fernandovtorres/fonte-de-tensao-ajustavel/assets/54219097/06e4c6fe-193a-48ef-a1b3-73d7a6c7bd2a

[Video Explicativo](https://youtu.be/Dz2hcll39sc)


