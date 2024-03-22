
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Iniciação Científica

## 1) Lógica de Programação

### Comandos básicos

#### Atribuição, use `<-`.

``` r
x <- 4
```

Atribuição por teclado, use a função `readLine`. Você precisa digitar o
valor no console.

``` r
x <- readline("Digite número: ")
#> Digite número:
x
#> [1] ""
```

#### Imprimindo um valor na tela

``` r
x <- "Oi mundo"
print(x)
#> [1] "Oi mundo"
```

#### Estrutura de decisão:

Estrutura se: executada somente se a condição for verdadeira.

Imprima x se x for maior que zero.

``` r
x <- 3
if(x > 0){
  print(x)
}
#> [1] 3
```

Imprima x se x for maior que zero, caso contrário imprima “valor menor
que zero”.

``` r
x <- -5
if(x > 0){
  print(x)
}else{
  print("Valor menor que zero")
}
#> [1] "Valor menor que zero"
```

Estrutura do if utilizada em vetores.

``` r
notas <- c(9,3,4,2,6,5)
```

Se a nota for maior ou igual que 5, `aprovado`, caso contrário,
`reprovado`.

``` r
ifelse(notas >=5, "aprovado","reprovado")
#> [1] "aprovado"  "reprovado" "reprovado" "reprovado" "aprovado"  "aprovado"
```

Usando o `case_when()`, pacote `{tidyverse}`.

CLassificar o dia de semana, 1 a 7, de domingo a sábado.

``` r
# Carregando o pacote
library(tidyverse)

# gerando numeros aleatorios de 1 a 7
num <- trunc(runif(20,1,8))
case_when(
  num == 1 ~ "domingo",
  num == 2 ~ "segunda-feira",
  num == 3 ~ "terca-feira",
  num == 4 ~ "quarta-feira",
  num == 5 ~ "quinta-feira",
  num == 6 ~ "sexta-feira",
  num == 7 ~ "sabado",
  .default = "Erro"
)
#>  [1] "sexta-feira"   "quarta-feira"  "sexta-feira"   "sabado"       
#>  [5] "domingo"       "quarta-feira"  "segunda-feira" "quarta-feira" 
#>  [9] "quinta-feira"  "quinta-feira"  "sabado"        "quinta-feira" 
#> [13] "segunda-feira" "sabado"        "terca-feira"   "segunda-feira"
#> [17] "domingo"       "sexta-feira"   "quarta-feira"  "quinta-feira"
```

#### Estrutura de Repetição:

Imprimir número de 1 a 10

``` r
for(i in 1:10){
  print(i)
}
#> [1] 1
#> [1] 2
#> [1] 3
#> [1] 4
#> [1] 5
#> [1] 6
#> [1] 7
#> [1] 8
#> [1] 9
#> [1] 10
```

Diferente de “criar um vetor contendo os números de 1 a 10”;

``` r
meu_vetor <- 1:10
meu_vetor 
#>  [1]  1  2  3  4  5  6  7  8  9 10
```

Repetição condicional usando o `while`. Enquanto a condição for
verdadeira, a repetição continua (loop).

``` r
x <- 1
while (x <=10) {
  print(x)
  x <- x + 1 #o x é alterado em cada iteração
}
#> [1] 1
#> [1] 2
#> [1] 3
#> [1] 4
#> [1] 5
#> [1] 6
#> [1] 7
#> [1] 8
#> [1] 9
#> [1] 10
```

# Exercícios

### 1.1) Estrutura sequencial

1.  Crie um código que dado dois pontos quaisquer $P$ e $Q$ com
    coordenadas $P(x1 , y1)$ e $Q(x2 , y2)$,encontre a distância entre
    eles. Lembre-se que a distância $D$ é calculada como:

$D= \sqrt{(x_2-x_1)^2+(y_2-y_1)^2 )}$

2.  Implemente a partir do exercício anterior o cálculo da inclinação da
    reta que passa pelos pontos $P$ e $Q$. Lembre-se que a inclinação
    $m$ pode ser calculada pela expressão:
    $m=\frac{(y_2-y_1)}{(x_2-x_1 )}$, para retas horizontais, $m=0$ e
    para retas verticais não existe inclinação

### 1.2) Estrutura de Decisão

1.  Faça um programa que peça dois números e imprima o maior deles.

2.  Faça um programa que peça um valor e mostre na tela se o valor é
    positivo ou negativo.

3.  Faça um programa que peça para entrar com um ano com 4 dígitos e
    determine se o mesmo é ou não bissexto (procure regra na rede).

4.  Faça um programa que verifique se uma letra digitada é vogal ou
    consoante.

5.  Faça um programa para a leitura de duas notas parciais de um aluno.
    O programa deve calcular a média alcançada por aluno e apresentar: •
    A mensagem “Aprovado”, se a média alcançada for maior ou igual a
    sete; • A mensagem “Reprovado”, se a média for menor do que sete; •
    A mensagem “Aprovado com Distinção”, se a média for igual a dez.

6.  Faça um programa que leia três números e mostre o maior e o menor
    deles.

7.  Faça um programa que pergunte o preço de três produtos e informe
    qual produto você deve comprar, sabendo que a decisão é sempre pelo
    mais barato.

8.  Faça um programa que pergunte em que turno você estuda. Peça para
    digitar M-matutino ou V-Vespertino ou N- Noturno. Imprima a mensagem
    “Bom Dia!”, “Boa Tarde!” ou “Boa Noite!” ou “Valor Inválido!”,
    conforme o caso.

9.  Uma empresa resolveu dar um aumento de salário aos seus
    colaboradores e lhe contrataram para desenvolver o programa que
    calculará os reajustes. Faça um programa que recebe o salário de um
    colaborador e o reajuste segundo o seguinte critério, baseado no
    salário atual:  
    • salários até R\$ 280,00 (incluindo) : aumento de 20%  
    • salários entre `R$` 280,00 e R\$ 700,00 : aumento de 15%  
    • salários entre `R$` 700,00 e R\$ 1500,00 : aumento de 10%  
    • salários de R\$ 1500,00 em diante : aumento de 5%.

Após o aumento ser realizado, informe na tela:  
• o salário antes do reajuste;  
• o percentual de aumento aplicado;  
• o valor do aumento;  
• o novo salário, após o aumento.

11. Faça um programa que leia um número e exiba o dia correspondente da
    semana. (1- Domingo, 2- Segunda, etc.), se digitar outro valor deve
    aparecer valor inválido.

12. Faça um programa que tendo como dados de entrada o preço de custo de
    um produto e um código de origem, emita o preço junto de sua
    procedência. Caso o código não seja nenhum dos especificados, o
    produto deve ser classificado como importado. Código de origem: 1 -
    Sul, 2 - Norte 3 - Leste, 4 - Oeste, 5 ou 6 - nordeste 7 ou 8
    Centro-oeste.

13. Faça um programa que leia as duas notas parciais obtidas por um
    aluno numa disciplina ao longo de um semestre, e calcule a sua
    média. A atribuição de conceitos obedece à tabela abaixo:  
    • Média de Aproveitamento Conceito  
    Entre 9.0 e 10.0 A  
    Entre 7.5 e 9.0 B  
    Entre 6.0 e 7.5 C  
    Entre 4.0 e 6.0 D  
    Entre 4.0 e zero E

O programa deve mostrar na tela as notas, a média, o conceito
correspondente e a mensagem “APROVADO” se o conceito for A, B ou C ou
“REPROVADO” se o conceito for D ou E.

14. Faça um programa que peça os 3 lados de um triângulo. O programa
    deverá informar se os valores podem ser um triângulo. Indique, caso
    os lados formem um triângulo, se o mesmo é: equilátero, isósceles ou
    escaleno.

Dicas:  
• Três lados formam um triângulo quando a soma de quaisquer dois lados
for maior que o terceiro;  
• Triângulo Equilátero: três lados iguais;  
• Triângulo Isósceles: quaisquer dois lados iguais;  
• Triângulo Escaleno: três lados diferentes;

15. Escreva código que dado as coordenadas dos pontos A, B e C, teste se
    esses pontos formam um triângulo, se formarem, classifique o
    triângulo em Isósceles, equilátero e escaleno. Lembre-se, sendo DAB
    a distância entre os pontos A e B, DAC a distância entre os pontos A
    e C e DBC a distância entre os pontos B e C, temos as condições:

se: DAB = DAC e DAB = DBC e DAC=DBC ↔ triângulo equilátero; se: DAB =
DAC ou DAB = DBC ou DAC=DBC ↔ triângulo isósceles; se: DAB $\neq$ DAC e
DAB $\neq$ DBC e DAC $\neq$ DBC ↔ triângulo escaleno;

16. Implemente a partir do exercício anterior a verificação se os pontos
    não formam um triângulo, ou seja, as inclinações das retas que AB,
    AC e BC devem ser iguais ou houver alguma distância igual a zero
    (0). Implemente também um teste para verificação se o triângulo é
    retângulo, ou seja, se pelo menos um par de retas são
    perpendiculares. Lembre-se, duas retas com inclinação m1 e m2 são
    perpendiculares se e somente se: m_2=-1/m_1 ⇒m_2-1/m_1 \<0,0000001

### 1.3) Estrutura de Repetição

### 1.4) Tipos de variáveis

### 1.5) Tipos de objetos (vetores, matrizes, data.frames, lista)

1.  Escreva um código que dado dois vetores numéricos inteiros, com
    tamanhos diferentes. Imprima a união e a Interseção entre esses
    vetores.

Lembre-se:
$(A \cup B) = \{x ∣ \in A \text { ou }x \in BA \text { ou } (x \in A, x \in B)$
e $(A \cap B) = \{x ∣ (x \in A, x \in B)\}$

Exemplo dados os conjuntos A = { 1, 2, 3, 5} e B {2,4,5}, temos:
(A∪B={1,2,3,4,5} e A∩B={2,5})

2.  Implemente o código anterior para ele funcionar como um programa que
    pergunte ao usuário o tamanho dos vetores (numéricos inteiros) e o
    preenchimento seja feito pelo usuário, digitando os elementos dos
    vetores A e B, em seguida o programa deve fazer as operações de
    união e interseção dos conjuntos.

### 1.6) Modulação - subrotinas e funções

## 2) Modelagem de qualidade da água em bacias hidrológicas do estado de São Paulo
