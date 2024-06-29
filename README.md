# Fonte de tensão ajustável

*Projeto para a disciplina Eletronica para Computação - SSC0180*

# Sobre o Projeto

Neste trabalho, projetamos uma fonte de tensão regulável 3v a 12v. Para isso, utilizamos a voltagem alternada de 127v 60hz vinda da tomada e transformamos em volatagem contínua utilizando um tranformador e um circuito retificador feito com diodos.

# Tabela dos componentes
| componente | quantidade | custo por unidade |
| :----: | :----: | :----: |
|Transformador 24.2V|1|*|
|Diodos |placeholder|placeholder|
|----- | **`TOTAL: xx`** | **`Preço Total: R$ XXX.XX`** |

# Informações sobre os componentes
- **transformador**: tem o papel de reduzir a voltagem de 127v vinda de uma fonte de corrente alternada (a tomada) para 24.2v, ainda alternada.
- **ponte de diodo**: a ponte de diodo é um arranjo de 4 diodos dispostos de uma forma com que a corrente alternada se tranforme em contínua
- **capacitor**: armazena carga no circuito durante os ciclos, liberando corrente quando a tensão provinda da fonte for menor do que a tensão interna do capacitor. Com base em um cálculo de 10% de ripple, chegamos próximos ao valor comercial de 820uF
- **diodo zener**: quando a voltagem passa de 13v, ele mantém esse valor como máximo em seus terminais, porém quando a voltagem é menor do que 13v, ele não conduz, logo não interfere
- **potenciômetro**: é um resistor regulável que será usado como o controle da tensão final.
- **transistor**: amplifica a corrente com base na resistência do potenciometro.
- **resistores**: utilizado em diversoss momentos no circuito, possui a função de limitar a corrente, o que garante uma certa segurança para os outros componentes do circuito.
- **led**: tem como função indicar quando a voltagem atingir 5 volts na parte final do circuito. de modo geral, não interfere nos valores obtidos no circuito, servindo unicamente como indicação da voltagem e corrente ajustáveis.

# Imagem do Falstad

![Screenshot from 2024-06-29 16-26-51](https://github.com/fernandovtorres/fonte-de-tensao-ajustavel/assets/54219097/3d010d52-58a6-4602-856b-af1317ef7481)

[Link para o falstad](https://tinyurl.com/2gezskvp)

# PCB no Eagle

  
# Esquemático no Eagle


# Vídeo Explicativo
