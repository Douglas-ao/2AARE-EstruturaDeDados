 # <p align="center"> Comparativos de performance</p>
 
 ### Ordenação por comparação
 - Um algoritmo de comparação é um tipo de algoritmo de ordenação que lê apenas os elementos da lista através de uma operação de comparação determina a classificação na lista
  e manipula dados, colocando os elementos de uma dada sequência em uma certa ordem.
 - Existem várias razões para se ordenar uma sequência. Uma delas é a possibilidade se acessar seus dados de modo mais eficiente.
 - Comparação de performance `Bubble Sort`, `Insertion Sort`, `Quick Sort`, `Selection Sort`.

---

> ### BubbleSort

* Analisando a Tabela podemos perceber que até 1000 elementos o BubbleSort é eficiente e realiza a ordenação de forma eficaz, porém com valores maiores já se torna mais lento. 
No melhor caso quase não há alteração para o tempo de resposta deste algoritmo, visto que ele apenas passará dentro do laço for sem entrar nenhuma vez na condição para 
realizar a troca de elementos.
               
Elementos     | Caso médio (n²)  | Melhor Caso (n)
------------- | -------------    | -------------
100           | 0 ms             | 0 ms
1.000         | 15 ms            | 0 ms
10.000        | 200 ms           | 0 ms
100.000       | 20.426 ms        | 2 ms
200.000       | 81.659 ms        | 4 ms

---
> ### Insertion Sort

- O que podemos perceber na tabela é que no caso médio temos uma alteração exponencial, aumentando muito o tempo conforme o aumento do número de elementos. 
Ao analisar os tempos você verá um aumento considerável quando trabalhamos comn². Por outro lado, no melhor caso o tempo mantem-se quase constante, 
enquanto temos 20.272 ms para 200.000 no caso Médio, temos 8 ms para a mesma quantidade no melhor Caso.


Elementos     | Caso médio (n²)  | Melhor Caso (n)
------------- | -------------    | -------------
100           | 0 ms             | 0 ms
1.000         | 11 ms            | 0 ms
10.000        | 220 ms           | 1 ms
100.000       | 5.110 ms         | 6 ms
200.000       | 20.272 ms        | 8 ms

---
> ### Quick Sort
- Ao analisar o tempo de processamento do QuickSort é notavel que quando tratamos do caso médio ele é muito bom,
é o método de ordenação interna mais rápido que se conhece para uma ampla variedade de situações. 
Provavelmente é o mais utilizado.

Elementos     | Caso médio (n²)  
------------- | -------------    
100           | 0 ms             
1.000         | 0 ms            
10.000        | 39 ms          
100.000       | 43 ms         
200.000       | 50 ms        

---
> ### Selection Sort

- No SelectionSort a implementação torna-se simples, porém perdemos muito com o desempenho. Como podemos analisar
na tabela.

Elementos     | Caso médio (n²)  | Melhor Caso (n)
------------- | -------------    | -------------
100           | 0 ms             | 0 ms
1.000         | 12 ms            | 10 ms
10.000        | 67 ms            | 62 ms
100.000       | 5.110 ms         | 4.561 ms
200.000       | 20.435 ms        | 18.181 ms
 
 ---
 ### Ordenação Mais Rápida
 
>QuickSort

 - `QuickSort`, mostrou-se o algoritmo mais rápido de todos e consequentemente o mais complexo de ser implementado.
É perceptível que o `QuickSort`, `BubbleSort` e `InsertionSort` possuem quase o mesmo tempo de resposta quando estamos 
tratando com até 1000 elementos no vetor, a variação é tão insignificante que a escolha de um destes algoritmos é 
mais uma questão pessoal do que profissional.
 Isso ocorre principalmente pelo fato de ele trabalhar com recursos como recursividade para alcançar um desempenho notável.

Tabelas abaixo de comparações:

<img src="https://upload.wikimedia.org/wikipedia/commons/e/eb/Grafico_comparacao_alg_sort.png" width="500">

> O mais lento é o `BubbleSort` , depois vem o `SelectionSort`, `InsertionSort` e o mais rapido é o `QuickSort`. 

<img src="https://4.bp.blogspot.com/-EyeELX6FcgI/WzAk5BAA7nI/AAAAAAAAIFM/rjJ4_kKZ4P8Izyp15y2xZaJ0peYdtW29QCLcBGAs/s1600/comparativo-desempenho-bubble-selection-insertion-sort.png" width="500">

> Comparações entee `BubbleSort`, `SelectionSort` e `InsertionSort` usando a quantidade de 1.000.000 elementos. 

