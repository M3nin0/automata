### Fundamentação da Teoria da Computação e Linguagens Formais - Conceitos fundamentais

1. Seja $\Sigma$ o alfabeto ${a, b}$. Quais as linguagens abaixo ? 
(Liste as cadeias que pertencem a cada uma das linguagens)

a. { x ∈ Σ* | |x| é par }
- {ab, ba, aabb, baab, baba, bbaa, ...}

b. { x ∈ Σ* | |x| ≤ 2 }
- {$\Lambda$, a, b, aa, bb, ab, ba}

c. { x ∈ Σ* | o primeiro símbolo de x é igual ao último símbolo de x }
- {aa, bb, aba, bab, bbaabb, bbab, ...}

d. { x ∈ Σ* | o penúltimo caracter de x é a}
- {aa, bab, bbaa, bbbaaa, abab, ...}

e. { x ∈ Σ* | x não contém a subcadeia aba } 
- { aa, bab, bbaa, aaabbb, bbaabb, aabbaa, aab, ... }

f. { x ∈ Σ* | x não contém dois a consecutivos 
- {$\Lambda$, a, b, bbbb, bba, bbbba, bbabb, abbbb, babbb, ...}

2. Dadas as linguagens

$$
L_1 = \{ axa | z ∈ \{a, b\}* \}
$$

$$
L_2 = \{ xx | x ∈ \{a, b\}* \}
$$

(a) Qual é a linguagem $L_1 ∪ L_2$ ?

$$
L_1 ∪ L_2 = \{ w: w ∈ L_1 \ ou \ w ∈ L_2\}
$$

As cadeias aceitas seriam parecidas com:

$$
L_1 ∪ L_2 = \{ aaa, aba, aaba, bb, aa, aaabbb, ... \}
$$

> A linguagem resultante aceita cadeias tanto de $L_1$ quanto de $L_2$

(b) Qual é a linguagem $L_1 ∩ L_2$ ?

$$
L_1 ∩ L_2 = \{ w: w ∈ L_1 \ e \ w ∈ L_2\}
$$

As cadeias aceitam seriam parecidas com:

$$
L_1 ∩ L_2 = \{ aaa, aba, aaaa, abbbba, ... \}
$$

> A linguagem resultante só aceita cadeias que estejam presentes nas duas linguagens

(c) Qual é a linguagem $\overline{L_1} ∪ \overline{L_2}$ ?

$$
\overline{L_1} = \{ bbaa, baba, ... \}
$$

$$
\overline{L_2} = \{ a, b \}
$$

A linguagem reconhecida será $\overline{L_1} ∪ \overline{L_2} = \{a, b, bbaa, baba, ... \}$ 

> A linguagem resultante representa a aceitação de todos os elementos que não são aceitos em $L_1$ e $L_2$ (Conjuntos complementos)

**Sobre os exercícios**: Os exercícios presentes nesta página foram retirados das seguintes referências:
- [Lista de exercícios - UNESP](http://wwwp.fc.unesp.br/~simonedp/zipados/Lista-TC01.pdf)

