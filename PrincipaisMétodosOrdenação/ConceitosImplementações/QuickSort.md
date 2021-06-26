# <p align="center"> Quick Sort </p>

- `Quicksort` adota a estratégia de divisão e conquista. A estratégia consiste em rearranjar as chaves de modo que as chaves "menores" 
precedam as chaves "maiores". Em seguida o quicksort ordena as duas sublistas de chaves menores e maiores recursivamente até que a 
lista completa se encontre ordenada. Os passos são:
1.  Escolha um elemento da lista, denominado pivô;
2. Particiona: rearranje a lista de forma que todos os elementos anteriores ao pivô sejam menores que ele, e todos os elementos posteriores 
ao pivô sejam maiores que ele. Ao fim do processo o pivô estará em sua posição final e haverá duas sub listas não ordenadas. Essa operação 
é denominada partição;
3. Recursivamente ordene a sub lista dos elementos menores e a sub lista dos elementos maiores;
- O caso base da recursão são as listas de tamanho zero ou um, que estão sempre ordenadas. O processo é finito, pois a cada iteração pelo 
menos um elemento é posto em sua posição final e não será mais manipulado na iteração seguinte.
A escolha do pivô e os passos do Particiona podem ser feitos de diferentes formas e a escolha de uma implementação específica afeta fortemente a performance do algoritmo. `Exemplo:`


<p align="center"> 
<img src="https://upload.wikimedia.org/wikipedia/commons/9/9c/Quicksort-example.gif" width="500">
</p>

---

### Exemplo Implementação: 

```Java
package br.com;

public class QuickSort {

    int assistant;                     // axiliar as trocas

    public static void main(String[] args) {

        QuickSort um = new QuickSort();
        int vetor[] = {3, 5, 4, 6, 1, 2};      //representa o vetor 1 
        um.quickSort(vetor, 0, vetor.length - 1); //retornar {1, 2, 3, 4, 5, 6}
        imprimirVetor(vetor);
        int vetor2[] = {9, 11, 8, 12, 7, 10};  //representa o vetor 2
        um.quickSort(vetor2, 0, vetor.length - 1); //retornar {7, 8, 9, 10, 11, 12}
        imprimirVetor(vetor2);
    }

    void quickSort(int vetor[], int left, int right) {
        //vetor a ordenar
        int pivo = vetor[left];

        //no elementos > o pivo vai a direita
        //no elemento < o pivo vai a esquerda
        int a = left;
        int b = right;

        //os elementos são avaliados para localizar o novo pivô
        while (a < b) {
            while (vetor[a] <= pivo && a < b) {
                a++;
            }
            while (vetor[b] > pivo) {
                b--;
            }
            //sempre quando "a" seja menor que "b" fazem um intercambio de elementos
            if (a < b) {
                assistant = vetor[a];
                vetor[a] = vetor[b];
                vetor[b] = assistant;
            }
        }
        vetor[left] = vetor[b];
        vetor[b] = pivo;
        if (left < b - 1) {
            quickSort(vetor, left, b - 1);
        }
        if (b + 1 < right) {
            quickSort(vetor, b + 1, right);
        }
    }

    //metodo para imprimir
    public static void imprimirVetor(int vetor[]) {
        // retornar a ordem correta (1, 2, 3, 4, 5, 6}{7, 8, 9, 10, 11, 12}
        for (int a = 0; a < vetor.length; a++) {
            System.out.println(vetor[a]);
        }
    }
}
```
