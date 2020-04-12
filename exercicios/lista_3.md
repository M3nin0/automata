### Fundamentação da Teoria da Computação e Linguagens Formais - Linguagens livre de contexto

(1) **Considere a seguinte gramática: G = ({S}, {a,b}, S, P), onde P = { S → SS | aSa | bSb | $\lambda$ }**

a) Qual é a linguagem gerada

Alguns exemplos de cadeias que pertencem a linguagem gerada pela gramática G são apresentadas pelas produções abaixo:
* 1: S → SS → SaSa → SabSba → abSba → abba
* 2: S → aSa → abSba → abba
* 3: S → bSb → bb

b) A gramática é ambígua ?

> Lembrando que: **Gramática ambígua** é aquela que, através de diferentes derivações chega-se as mesmas cadeias

Seguindo a definição apresentada acima, é possível afirmar que esta é uma gramática ambígua. Isso pode ser observado nos seguintes exemplos abaixo: 

* 1: S → SS → SaSa → SabSba → abSba → abba
* 2: S → aSa → abSba → abba

Perceba que, através de diferentes derivações, chegou-se na mesma cadeia

c) Considere a cadeia `aabbaaaa`:

Antes de iniciar o exercícios e suas considerações, façamos de maneira simples as derivações da gramática G para determinar se a cadeia pertence a L(G).

Aplicando as regras de derivação, a cadeia `aabbaaaa` é obtida através das seguintes derivações:

P = { S → SS | aSa | bSb | λ }

* S → SS → SSSS → aSaSSS → aaSSS → aabSbSS → aabbSS → aabbaSaaSa → aabbaaaa

Com este teste foi possível determinar que a cadeia apresentada no exercício pertence a L(G).

* Construa uma árvore de derivação

A árvore de derivação para a cadeia apresentada no exercício é exibida na Figura abaixo.

<div align="center">
    <img src="figuras/lista_3/exe_1_arvore_derivacao.png">
</div>

*Neste exercício é interessante notar o motivo da L(G) ser apenas Livre de contexto, e não ser considerada uma linguagem regular. Isso ocorre por conta da forma de produção perceba que as mesmas ocorrem com substituições do lado esquerdo e do lado direito, quando a regra das produções das gramáticas regulares diz que esta deve ocorrer em apenas um dos lados (Esquerda ou direita)*

<!-- * Para a árvore construída, determine as derivações mais à esquerda e a mais à direita. -->

(2) **Considere a gramática G = ({S}, {a, b, c, +, *, ( , ), |}, S, P), onde**
P = { S → SS | S + S | S\* | (S) | a | b | c | λ }

a) Qual é a linguagem definida por essa gramática.

Para responder a esta questão, algumas produções serão feitas, para que a lógica da linguagem definida por G seja compreendida

* S → S + S → a + S → a + b
* S → SS → S\*S → a\*S → a \* b
* S → SS → SS + S → S*S + S →\* a\* b + c

Com base nos testes de derivações realizados acima, é possível afirmar que a gramática define a linguagem de operações aritméticas básicas.  

b) Essa gramática é ambígua? Justifique.

Sim! Tratando-se do domínio da L(G), é possível realizar tal afirmação, porém, como forma de confirmação, exemplos de ambíguidade são apresentados abaixo

* S → S + S → a + b
* S → SS → S + SS → a + SS → a + bS → a + b 

c) Verifique se as cadeias abaixo pertencem à L(G), mostrando as respectivas seqüências de derivação:

* λ 
  * S → λ 
* a (b | cc)\* (de | λ ) ea\*
  * Possuí símbolos de entrada que não estão no conjunto de símbolos finais!
* a\*b (ca\* + bcc)\* + λ
  * S → SS → SSS → SSSS → S\*SSS → a\*bSSS → a\*b (SS → a\*b (SSS → a\*b (caS → (SSS → a\*b (caSS →* a\*b (caS\*S+S →\* a\*b (caS\* + bcc)* + λ 
* (a\*)\*
  * S → SS → (S)S → (S*)S* → (a*)*

4) **Construa as gramáticas livres de contexto que gerem as seguintes linguagens**

a) L = {$a^nb^{2n}$ | n ≥ 0}

Definindo a gramática

G = ({S}, {a, b}, S, P), sendo definido para P as seguintes regras:
- S → aSbb
- S → $\lambda$

Para validar tal gramática, a mesma foi inserida no JFlap, abaixo é apresentado sua árvore de derivação.

<div align="center">
    <img src="figuras/lista_3/exe_4a_arvore_derivacao.png">
</div>

**Sobre os exercícios**: Os exercícios presentes nesta página foram retirados das seguintes referências:
- [Lista de exercícios - UNESP](http://wwwp.fc.unesp.br/~simonedp/zipados/Lista-TC03.pdf)

**Software utilizado**: Os exercícios acima foram desenvolvidos e validados com o auxílio do [JFlap](http://www.jflap.org/jflaptmp/)
