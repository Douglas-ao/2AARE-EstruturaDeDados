#  <p align="center"> Selection Sort </p>
* `Selection Sort` compara a cada interação um elemento com os outros, visando encontrar o menor. Dessa forma, podemos entender 
que não existe um melhor caso mesmo que o vetor esteja ordenado ou em ordem inversa serão executados os dois laços do algoritmo, 
o externo e o interno. A complexidade deste algoritmo será sempre <i> O(n log n).</i>
* Ele é um dos mais lentos para vetores de tamanhos grandes e não é estável.
* `Selection Sort:` é baseado em se passar sempre o menor/maior valor do vetor para a posição 1 dependendo da ordem requerida,
2º menor valor para a posição 2 e assim sucessivamente. Se algum número de uma posição não encontrar nenhum número menor que 
ele à sua direita, então não troque. `Exemplo:`

<p align="center">
<img src="https://i2.wp.com/algorithms.tutorialhorizon.com/files/2019/01/Selection-Sort-Gif.gif?ssl=1" width ="500">
</p>

---

### Exemplo Implementação: 

```Java
package br.com;

public class SelectionSort {

    int assistant;                     // axiliar as trocas

    void selectionSort(int vetor[]) {
        //repetir o processo no tamanho do vetor
        for (int a = 0; a < vetor.length; a++) {
            //armazenando o elemento a
            int smaller = a;
            //não deixar de passe da quantidade de elemento no vetor
            for (int b = a + 1; b < vetor.length; b++) {
                //responsavel por analisar dois valores
                // comparar de vetor b é menor que smaller(numero menor)           
                if (vetor[b] < vetor[smaller]) {
                    // se for verdadeiro smaller(numero menor) é igual a "b"
                    smaller = b;
                }
            }
            //trocas de elementos no vetor
            assistant = vetor[smaller];
            vetor[smaller] = vetor[a];
            vetor[a] = assistant;
        }
        // retornar a ordem correta (1, 2, 3, 4, 5, 6}{7, 8, 9, 10, 11, 12}
        for (int a = 0; a < vetor.length; a++) {
            System.out.println(vetor[a]);
        }
    }

    public static void main(String[] args) {

        SelectionSort um = new SelectionSort();
        int vetor[] = {3, 5, 4, 6, 1, 2};      //representa o vetor 1 
        um.selectionSort(vetor);               //retornar {1, 2, 3, 4, 5, 6}
        int vetor2[] = {9, 11, 8, 12, 7, 10};  //representa o vetor 2
        um.selectionSort(vetor2);              //retornar {7, 8, 9, 10, 11, 12}
    }
}
```
