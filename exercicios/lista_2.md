### Fundamentação da Teoria da Computação e Linguagens Formais - Linguagens regulares

01) Desenvolva AFD que reconheçam as seguintes linguagens sobre Σ = {a, b}

a) {w | w possui aaa como subpalavra}

<div align="center">
    <img src="figuras/lista_2/exe_1_afd.jpg">
</div>

b) {w | o sufixo de w é aa}

<div align="center">
    <img src="figuras/lista_2/exe_2_afd.jpg">
</div>

c) {w | w possui número ímpar de a e b} 

<div align="center">
    <img src="figuras/lista_2/exe_3_afd.jpg">
</div>

2) Desenvolva AFN que reconheçam as seguintes linguagens sobre Σ = {a,b}

a) {$w_1$ $w_2$ $w_1$ | $w_2$ é qualquer e |$w_1$| = 3}

<div align="center">
    <img src="figuras/lista_2/exe_4_afnd.jpg">
</div>

b) {w | o décimo símbolo da direita para a esquerda de w é a} 

<div align="center">
    <img src="figuras/lista_2/exe_5_afnd.jpg">
</div>

3) Mostre  a  seqüência  de  configurações  assumidas  pelo  AFD  abaixo  durante  a  análise  das  cadeias  `abcdabc` e `abdabcd`. Determine se essas cadeias pertencem ou não a linguagem reconhecida pelo AFD. 

M = ({ q0, q1, q2, q3}, { a, b, c, d }, δ, q0, {q3})  

δ(q0, a) = q1
δ(q1, b) = q2
δ(q2, c) = q3
δ(q3, c) = q3
δ(q3, d) = q0

Para facilitar o entendimento dos passos realizados pelo AFD, façamos a representação visual através de um grafo direcionado

<div align="center">
    <img src="figuras/lista_2/exe_6_afd.jpg">
</div>

Com a visualização do autômato, é possível verificar qual será aceita e qual não será. Desta forma temos que:

| Cadeia de entrada |      Status     |
|:-----------------:|:---------------:|
|      abcdabc      |   Reconhecido   |
|      abdabcd      | Não Reconhecido |

Para entender melhor como cada um dos comportamento foi obtidos, vejamos os passos realizados pelo autômato.

- Para a cadeia `abcdabc`

<div align="center">
    <img src="figuras/lista_2/exe_6_trace_accept.png">
</div>

- Para a cadeia `abdabcd`

<div align="center">
    <img src="figuras/lista_2/exe_6_trace_reject.PNG">
</div>

4) Considere a Gramática Linear à Direita, G = ({S, A, B}, {a,b}, P, S), onde P é dado por

P = { S → aA, A → bB, B → cC, C → c}

Mostre 5 cadeias geradas por G. Encontre o Autômato Finito M = {Q, {a, b}, $\delta$, S, F} que reconhece a linguagem gerada por G.

* Produções
  * abbba
  * abba
  * aa
  * aaaa
  * abbbaa

As produções desta gramática sempre começam e terminam com `a`.

* Autômato para reconhecer a linguagem gerada por esta gramática

<div align="center">
    <img src="figuras/lista_2/exe_7_afnd.jpg">
</div>

5) Considere a Gramática Linear à Direita, G = ({S, X, Y}, {a,b,c}, P, S), onde P é dado por

P = { S → aX | λ, X → bX | bbY | c, Y → cY | cc | abc | λ}

Mostre 5 cadeias geradas por G. Encontre o Autômato Finito M = {Q, {a,b,c}, δ , S, F} que reconhece a linguagem gerada por G

* Produções
  * abc
  * abbccc
  * abbbabc
  * abbcc
  * ac

* Autômato para reconhecer a linguagem gerada por esta gramática

<div align="center">
    <img src="figuras/lista_2/exe_8_afd_rg.jpg">
</div>

* Consideração sobre o tipo de linguagem.

No exercício original há uma pequena regra de produção que altera o tipo da gramática

Para o exercício original as seguintes regras de produção eram consideradas
P = { S → aX | λ, X → bX | bbY | c, Y → Yc | cc | abc | λ}

Porém se for observado atentamente, a produção Y → Yc é linear à esquerda, enquanto todas as demais são lineares a direita, o que faz esta não ser uma linguagem regular, somente livre de contexto.

Então para se adequar ao contexto dos exercícios a regra foi alterada, gerando a seguinte.

P = { S → aX | λ, X → bX | bbY | c, Y → cY | cc | abc | λ}

Por conta de cursiosidade sobre como ficaria a forma de produção dessas regras com essa mudança, gerei uma produção de cada uma no JFlap.

Para a gramática livre de contexto, a produção teria esta aparência

<div align="center">
    <img src="figuras/lista_2/exe_8_grammar_cfg.jpg">
</div>

Para a gramática regular, a produção fica parecido com o que foi apresentado no exercício, como pode ser visto abaixo.

<div align="center">
    <img src="figuras/lista_2/exe_8_grammar_rg.jpg">
</div>

Isto não mudaria muito a linguagem gerada pela gramática, pelo menos nos testes feitos durante o exercício, porém para outras cadeias não testadas comportamentos diferentes poderiam ser gerados.

**Sobre os exercícios**: Os exercícios presentes nesta página foram retirados das seguintes referências:
- [Lista de exercícios - UEM](http://www.din.uem.br/yandre/TC/lista3-resp.pdf);
- [Lista de exercícios - UNESP](http://wwwp.fc.unesp.br/~simonedp/zipados/Lista-TC02.pdf)

**Software utilizado**: Os exercícios acima foram desenvolvidos e validados com o auxílio do [JFlap](http://www.jflap.org/jflaptmp/)
