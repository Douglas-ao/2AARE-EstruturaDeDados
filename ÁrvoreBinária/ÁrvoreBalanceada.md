# <p align="center">  Conceito </p>
* Uma árvore é considerada balanceada se e somente se para qualquer nó, a altura de suas duas subárvores diferem de no máximo uma unidade.
O nó desta árvore que satisfaz o balanceamento é chamado de nó regulado. Se não satisfizer, ele é considerado desregulado.
As árvores balanceadas são também chamadas de árvores AVL em homenagem aos seus inventores: Adelson-Velskii e Land. 
Elas minimizam o número de comparações efetuadas no pior caso para uma busca com chaves de probabilidades de ocorrências idênticas. 
Contudo, para garantir essa propriedade em aplicações dinâmicas, é preciso reconstruir a árvore para seu estado ideal a cada operação 
sobre seus nós (inclusão ou exclusão), para ser alcançado um custo de algoritmo com o tempo de pesquisa tendendo a O (log n). 

---
### `Rotação`
* Na inserção basta encontrar o primeiro nó desregulado (fb= -2 ou fb= 2), aplicar a operação de rotação necessária, não havendo necessidade 
de verificar os demais nós. Na remoção a verificação deverá prosseguir até a raiz, podendo requerer mais de uma rotação.
* Cada nó numa árvore binária balanceada (AVL) tem balanceamento de 1, -1 ou 0. 
* Se o valor do balanceamento do nó for diferente de 1, -1 e 0. Essa árvore não é balanceada (AVL).

Rotação Simples para Direita: Quando pivô e filho esquerdo têm mais elementos no lado esquerdo. | Rotação Simples para Esquerda: Quando pivô e filho direito têm mais elementos no lado direito.
----- | ------
<img src="http://albertocn.sytes.net/2012-2/ed1/aulas/figuras/arvore_avl_rot_simp_dir_ex.png" height="390" width="500"> | <img src="http://albertocn.sytes.net/2012-2/ed1/aulas/figuras/arvore_avl_rot_simp_esq_ex.png" height="390" width="500">


---

* Se a probabilidade de pesquisar um dado for a mesma para todos os dados, uma árvore binária balanceada determinará a busca mais eficiente.

<p align="center"> 
<img src="https://www.ime.usp.br/~pf/algoritmos/aulas/img/binary-search-tree-sorted-array-animation.gif" height="390" width="400">
</p>

---
  
* Os algoritmos de `inserção` e `remoção` não garantem que essa árvore permanecerá balanceada. Cada vez que for alterado 
tera que verificar o balanceamento e se for necessario fazer a rotação.

<p align="center"> 
<img src="https://pythonhelp.files.wordpress.com/2015/01/image11.gif" height="390" width="400">
</p>



> ### Regra para saber o fator de balanceamento:
>	`Fator(nó) = alturaSubEs - alturaSubDir` 	`Fator(nó) = -1, 0, 1 está balanceado`    `Se Fator(nó) = 2, -2 ele não está balanceado`

---

# `Diferença da Árvore não Balanceada e Árvore Balanceada` 

* A diferença é que na Árvore Balanceada a cada remoção ou inserção é necessário verificar o fator de balanceamento, e se necessário 
aplicar uma das rotações para fazer o balanceamento dos mesmos, enquanto a não balanceada é indiferente.
* Uma árvore binária balanceada determinará a busca mais eficiente enquanto a não balanceada não determinará uma busca mais eficiente.


