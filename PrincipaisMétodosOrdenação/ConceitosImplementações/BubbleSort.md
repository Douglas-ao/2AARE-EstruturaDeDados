# <p align="center">  Bubble Sort </p>
* `Bubble sort` ou ordenação por flutuação A ideia é percorrer o vector diversas vezes, e a cada passagem fazer flutuar para o topo o maior elemento da sequência. 
Essa movimentação lembra a forma como as bolhas em um tanque de água procuram seu próprio nível, e disso vem o nome do algoritmo.
* Uma forma de trabalhar com o algoritmo `Bubble Sorte` é comparando os elementos adjacentes (dois a dois), por exemplo: compara-se a 
primeira posição do vetor com a segunda, na segunda iteração (repetição), compara-se a segunda posição do vetor com a terceira, e 
assim sucessivamente. De acordo com o algoritmo, podemos ordenar o vetor de forma crescente ou decrescente.
* O algoritmo `Bubble Sort` percorre todo o vetor diversas vezes, por isso, não é recomendado o uso dele para aplicações que requerem 
velocidade ou trabalhem com uma grande quantidade de dados.
* É o algoritmo mais simples, mas o menos eficiente. O elemento da posição 1 será comparado com o elemento da posição 2 , 
caso a posição 1 seja maior que a posição 2 será trocado, se não, não é trocado,  e assim sucessivamente. `Exemplo:`

<p align="center"> 
<img src="https://upload.wikimedia.org/wikipedia/commons/0/06/Bubble-sort.gif" width="500">
</p>

---

### Exemplo Implementação: 

```Java
package br.com;

public class BubbleSort {

    int assistant;                     // auxiliar as trocas
    boolean control;                   //controle se o vetor esta ordenado

    void bubbleSort(int vetor[]) {
        //repetir o processo no tamanho do vetor
        for (int a = 0; a < vetor.length; ++a) {
            //se o vetor ja esteja ordenado, quebra etapa de repetir o processo
            control = true;
            //responsavel por analisar dois valores
            //não deixar de passe da quantidade de elemento no vetor
            for (int b = 0; b < (vetor.length - 1); ++b) {
                //responsavel por ordenar de forma crescente ou decrescente
                //verificar se um elemento é maior que o outro 
                //fazer a troca se necessario
                if (vetor[b] > vetor[b + 1]) {
                    assistant = vetor[b];
                    vetor[b] = vetor[b + 1];
                    vetor[b + 1] = assistant;
                    //não quebra a etapa
                    control = false;
                }
            }

            if (control) {
                //quebra a etapa
                break;
            }
        }
        //percorer o vetor e dar print em cada elemnto
        for (int a = 0; a < vetor.length; ++a) {
            // retornar a ordem correta (1, 2, 3, 4, 5, 6}{7, 8, 9, 10, 11, 12}
            System.out.print(vetor[a] + " ");
        }
    }

    public static void main(String[] args) {

        BubbleSort um = new BubbleSort();
        int vetor[] = {3, 5, 4, 6, 1, 2};       //representa o vetor 1 
        um.bubbleSort(vetor);                   //retorna {1, 2, 3, 4, 5, 6}
        int vetor2[] = {9, 11, 8, 12, 7, 10};  //representa o vetor 2
        um.bubbleSort(vetor2);                  //retorna {7, 8, 9, 10, 11, 12}
    }
}
```
