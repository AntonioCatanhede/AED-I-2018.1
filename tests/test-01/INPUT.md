# Prova 01

## 1. Parte Teórica (6 pontos)

Marque como verdadeiro ou falso as afirmações abaixo e justifique.

1. **( )** O custo de execução do algoritmo abaixo é $\Omega(n^4)$.

   ```c
   int k = 0;
   for (i = n / 2; i < n; i++)
     for (j = 1; j <= n * n; j++)
       k = k + 1;
   ```

2. **( )** A função de recorrência abaixo tem custo $T(n) = \Theta(n)$

$$T(n) = 4T\left(\frac{n}{2}\right) + \sqrt{n}\log(n)$$

3. **( )** É possível imprimir as chaves de uma árvore binária em ordem
decrescente com o percurso pós-ordem.

4. **( )** Um usuário realizou uma sequência misturada de `push`'s e `pop`s
em uma pilha. O `push` é responsável por uma entrada de 0 a 9, enquanto o
`pop` é realizado para a impressão. Uma dessas saídas possíveis seria
`2 1 4 3 6 5 8 7 9 0`.

## 2. Parte Prática (4 pontos)

Escreva um programa em C que leia um *texto A* arbitrariamente grande e um 
*texto B* de no máximo 100 caracteres, e se *texto B* é sufixo de
*texto A* imprima `SIM`, caso contrário, imprima `NAO`. Salve o programa
como: `sufixo.c`.

### Exemplos

<table>
  <thead>
    <th>Exemplo</th>
    <th>Entrada</th>
    <th>Saída</th>
  </thead>
  <tbody>
    <tr>
      <td>Exemplo 01</td>
      <td>
        <pre><code>professor
sor</code></pre>
      </td>
      <td valign="top"><pre><code>SIM<br> </code></pre></td>
    </tr>
    <tr>
      <td>Exemplo 02</td>
      <td>
        <pre><code>estudante
estuda</code></pre>
      </td>
      <td valign="top"><pre><code>NAO<br> </code></pre></td>
    </tr>
    <tr>
      <td>Exemplo 03</td>
      <td>
        <pre><code>estudante
corante</code></pre>
      </td>
      <td valign="top"><pre><code>NAO<br> </code></pre></td>
    </tr>
  </tbody>
</table>

### Observações

- O *texto A* **deve** ser implementado utilizando uma **estrutura enlaçada**;
- O `NAO` é sem o til;
- Libere da memória as estruturas ao fim do uso.

### Exemplo de implementação

```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main (int argc, char ** argv) {
  // Leitura da primeira cadeia de entrada.
  char atual = getchar();
  while (atual != '\n') {

    atual = getchar();
  }

  // Leitura da segunda cadeia de entrada.
  char entrada2[100];
  scanf("%s", &entrada2);

  return EXIT_SUCCESS;
}
```