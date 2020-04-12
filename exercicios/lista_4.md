### Fundamentação da Teoria da Computação e Linguagens Formais - Máquinas de turing

1) **Qual a linguagem aceita pela Máquina de Turing    M = ({q0,q1,q2,q3}, {a,b}, {a,b,$\square$}, δ,  q0,  {q3}), onde:**

δ(q0, a) = (q1, a, R), 
δ(q0, b) = (q2, b, R), 
δ(q1, b) = (q1, b, R), 
δ(q1, $\square$) = (q3, $\square$, R),
δ(q2, a) = (q3, a, R),
δ(q2, b) = (q2, b, R).

O primeiro passo para verificar as linguagens reconhecidas pela máquina M foi criar uma representação gráfica da mesma, para uma visualização inicial e possívelmente ajuda durante o reconhecimento das cadeias de entrada.

<div align="center">
    <img src="figuras/lista_4/exe_1a_mt.png">
</div>

Com a visualização da máquina sendo feita através de um grafo, já foi possível perceber os padrões de entrada, então alguns testes com diferentes cadeias foram feitos.

* δ(q0, [a]b) → δ(q1, a[b]) → δ(q1, ab$\square$) → δ(q3, ab$\square$) (**Cadeia aceita**)
* δ(q0, [a]ab) → δ(q1, a[a]b) (**Cadeia rejeitada**)

Bem, com os testes acima e interpretado as regras foi possível perceber que as cadeias aceitas por M são aquelas que começam ou terminam com o símbolo `a`, sendo que este símbolo não aparece nas cadeias em sequência. Para comprovar tal questão, mais testes foram feitos utilizando o JFlap.

<div align="center">
    <img src="figuras/lista_4/exe_1a_mt_mp.png">
</div>

**Sobre os exercícios**: Os exercícios presentes nesta página foram retirados das seguintes referências:
- [Lista de exercícios - UNESP](http://wwwp.fc.unesp.br/~simonedp/zipados/Lista-TC04.pdf)

**Software utilizado**: Os exercícios acima foram desenvolvidos e validados com o auxílio do [JFlap](http://www.jflap.org/jflaptmp/)
