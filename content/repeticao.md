
#### 📄 `repeticao.md`
```md

# 🔁 Laços de Repetição

Usados para repetir tarefas, como um robô!

## 📌 Estrutura básica do `while`:
````
```c
while (condicao) {
    // Bloco de código a ser executado enquanto a condição for verdadeira
}
```
Se a condição for verdadeira, o bloco de código dentro do while será executado repetidamente até que a condição se torne falsa.

🔍 Explicação Didática
Imagine que você quer contar de 1 a 5 usando um loop. Em vez de escrever printf() cinco vezes, podemos usar um while para tornar o código mais eficiente.

✨ Exemplo 1: Contagem de números de 1 a 5 
```c
#include <stdio.h>

int main() {
    int contador = 1; // Inicializamos a variável contador com 1

    while (contador <= 5) { // Enquanto contador for menor ou igual a 5
        printf("Número: %d\\n", contador);
        contador++; // Incrementamos contador para evitar um loop infinito
    }

    return 0;
}
```
💡 Comentários sobre o código:

A variável contador começa com 1.

O while verifica se contador <= 5.

Se verdadeiro, ele imprime o número e aumenta contador em 1.

Quando contador chega a 6, a condição contador <= 5 se torna falsa e o loop termina.

Exemplo: Solicitando entrada do usuário até que seja válido

```c
#include <stdio.h>

int main() {
    int idade;

    printf("Digite sua idade (deve ser maior que 0): ");
    scanf("%d", &idade);

    while (idade <= 0) { // Verifica se a entrada é inválida
        printf("Idade inválida! Digite novamente: ");
        scanf("%d", &idade);
    }

    printf("Idade válida registrada: %d anos\\n", idade);
    
    return 0;
}
```

💬 Comentários sobre o código:

O usuário fornece um valor inicial.

Se for menor ou igual a 0, o programa informa erro e pede outra entrada.

O loop while continua até o usuário fornecer um número válido (> 0).



## 🔂 Exemplo com `for`:
```c
for (int i = 0; i < 5; i++) {
    printf("Linha %d\n", i);
}
```

## ♻️ Exemplo com `while`:
```c
int x = 0;
while (x < 3) {
    printf("x = %d\n", x);
    x++;
}
```
```
