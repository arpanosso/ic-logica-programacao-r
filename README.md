
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Iniciação Científica

## 1) Lógica de Programação

1)  Crie um código que dado dois pontos quaisquer $P$ e $Q$ com
    coordenadas $P(x1 , y1)$ e $Q(x2 , y2)$,encontre a distância entre
    eles. Lembre-se que a distância $D$ é calculada como:

$D= \sqrt{(x_2-x_1)^2+(y_2-y_1)^2 )}$

2)  Implemente a partir do exercício anterior o cálculo da inclinação da
    reta que passa pelos pontos $P$ e $Q$. Lembre-se que a inclinação
    $m$ pode ser calculada pela expressão:
    $m=\frac{(y_2-y_1)}{(x_2-x_1 )}$, para retas horizontais, $m=0$ e
    para retas verticais não existe inclinação

3)  Escreva código que dado as coordenadas dos pontos A, B e C, teste se
    esses pontos formam um triângulo, se formarem, classifique o
    triângulo em Isósceles, equilátero e escaleno. Lembre-se, sendo DAB
    a distância entre os pontos A e B, DAC a distância entre os pontos A
    e C e DBC a distância entre os pontos B e C, temos as condições:

se: DAB = DAC e DAB = DBC e DAC=DBC ↔ triângulo equilátero; se: DAB =
DAC ou DAB = DBC ou DAC=DBC ↔ triângulo isósceles; se: DAB $\neq$ DAC e
DAB $\neq$ DBC e DAC $\neq$ DBC ↔ triângulo escaleno;

4)  Implemente a partir do exercício anterior a verificação se os pontos
    não formam um triângulo, ou seja, as inclinações das retas que AB,
    AC e BC devem ser iguais ou houver alguma distância igual a zero
    (0). Implemente também um teste para verificação se o triângulo é
    retângulo, ou seja, se pelo menos um par de retas são
    perpendiculares. Lembre-se, duas retas com inclinação m1 e m2 são
    perpendiculares se e somente se: m_2=-1/m_1 ⇒m_2-1/m_1 \<0,0000001

5)  Escreva um código que dado dois vetores numéricos inteiros, com
    tamanhos diferentes. Imprima a união e a Interseção entre esses
    vetores.

Lembre-se:
$(A \cup B) = \{x ∣ \in A \text { ou }x \in BA \text { ou } (x \in A, x \in B)$
e $(A \cap B) = \{x ∣ (x \in A, x \in B)\}$

Exemplo dados os conjuntos A = { 1, 2, 3, 5} e B {2,4,5}, temos:
(A∪B={1,2,3,4,5} e A∩B={2,5})

6)  Implemente o código anterior para ele funcionar como um programa que
    pergunte ao usuário o tamanho dos vetores (numéricos inteiros) e o
    preenchimento seja feito pelo usuário, digitando os elementos dos
    vetores A e B, em seguida o programa deve fazer as operações de
    união e interseção dos conjuntos.

### 1.1) Estrutura sequencial

### 1.2) Estrutura de Decisão

### 1.3) Estrutura de Repetição

### 1.4) Tipos de variáveis

### 1.5) Tipos de objetos (vetores, matrizes, data.frames, lista)

### 1.6) Modulação - subrotinas e funções

``` r
library(tidyverse)
#> ── Attaching core tidyverse packages ──────────────────────── tidyverse 2.0.0 ──
#> ✔ dplyr     1.1.4     ✔ readr     2.1.4
#> ✔ forcats   1.0.0     ✔ stringr   1.5.1
#> ✔ ggplot2   3.4.4     ✔ tibble    3.2.1
#> ✔ lubridate 1.9.3     ✔ tidyr     1.3.0
#> ✔ purrr     1.0.2     
#> ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
#> ✖ dplyr::filter() masks stats::filter()
#> ✖ dplyr::lag()    masks stats::lag()
#> ℹ Use the conflicted package (<http://conflicted.r-lib.org/>) to force all conflicts to become errors
```

## 2) Modelagem de qualidade da água em bacias hidrológicas do estado de São Paulo
