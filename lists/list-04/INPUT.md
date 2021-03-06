# Lista de Exercícios 4: Complexidade de algoritmos
*Lista de exercícios da Prof. Mirtha Lina, CMCC/UFABC.*

## Notações assintóticas

1. Ordene as seguintes funções por ordem de crescimento assintótico de forma não
decrescente. Preencha a tabela com os números correspondentes à ordem de 
crescimento. Use o mesmo número caso duas funções tenham a mesma ordem de 
crescimento, i.e. $f(n) = \Theta(g(n))$. Justifique de forma apropriada
sua ordenação.

| Função | $4^n$ | $n \log(n)$ | $3^n$ | $4^{\log_2(n)}$ | $n^{4/7}$ | $5000$ | $5n^2 + 8$ | $(n-1)!$ | $n2^n$ | $e^{2n}$ | $\log^4(n)$ |
| ------ | - | - | - | - | - | - | - | - | - | - | - |
| Ordem  | | | | | | | | | | | | |


1. Responda se as seguintes afirmações são verdadeiras ou falsas. Justifique de
forma apropriada sua resposta.

1. $100n^3 = \Omega(n^4 - 300n)$
1. $2^{2n} = O(2^n)$
1. $3^{\sqrt{n}} = O(3^n)$
1. $\log(n^2) = \Theta(\log(n))$
1. $n^{1/3} = \Theta\left(\sqrt{n}\right)$
1. $f(n) - g(n) = O(min(f(n), g(n)))$
1. $f(n) - g(n) = \Omega(g(n))$
1. $f(n) = \Theta(f(n/2))$

## Complexidade de algoritmos

1. Qual a complexidade assintótica das seguintes funções?

   ```c
   int a (int n) {
     int i, j, count = 0;
     for (i = n; i >= 1; i /= 2)
       for (j = 1; j <= n * n; j++)
         count++
     return count;
   }

   int b (int n) {
     int i, j, k, count = 0;
     for (i = n / 2; i <= n; i++)
       for (j = 1; j <= n; j *= 2)
         for (k = 1; k <= n; k *= 2)
           count++;
     return count;
   }
   ```

1. Qual a complexidade assintótica no caso pior do programa que você usou para
resolver o Exercício 1 da Lista 1?

1. Preencha a seguinte tabela com a complexidade no caso pior das seguintes
operações sobre **conjuntos** (não há repetições de elementos).

   | Operação                   | Tamanho Entrada | Vetores | Listas enlaçadas |
   | -------------------------- | --------------- | ------- | ---------------- |
   | Pertinencia de um elemento |                 |         |                  |
   | União                      |                 |         |                  |
   | Interseção                 |                 |         |                  |
   | Diferença                  |                 |         |                  |
   | Inserir elemento no final  |                 |         |                  |
   | Eliminar um elemento       |                 |         |                  |
   | Produto cartesiano         |                 |         |                  |
   | Conjunto potência          |                 |         |                  |

## Complexidade de algoritmos recursivos

1. Qual a complexidade assintótica das seguintes recorrências e funções?
1. $T(n) = 9T\left(\frac{n}{2}\right) + n^2$
1. $T(n) = 4T\left(\frac{n}{2}\right) + n^2\sqrt{n}$
1. $T(n) = 5T\left(\frac{n}{5}\right) + \frac{n}{2}$
1. $T(n) = 3T\left(\frac{n}{3}\right) + \sqrt{n}$

   ```c
   void e (int n) {
     if (n <= 1)
       return;
     int i = 1;
     for (; i <= n; i++)
       printf("*");
     e(0.8 * n);
   }

   void f (int n) {
     if (n <= 2)
       return;
     int i = 1, count = 0;
     for (; i <= 8; i++)
       f(n / 2);
     for (i = 1; i <= n * n * n; i++)
       count++;
   }
   ```