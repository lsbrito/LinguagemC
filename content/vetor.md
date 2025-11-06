# 📘 Vetores em Linguagem C

Vetores (ou arrays) são estruturas de dados fundamentais na linguagem C. Eles permitem armazenar múltiplos valores de um mesmo tipo em posições contíguas de memória, facilitando o acesso e a manipulação de dados em massa.

## 🔍 O que é um vetor?

Um vetor é uma sequência de elementos do mesmo tipo, acessados por um índice. O índice em C começa do **zero**, ou seja, o primeiro elemento está na posição `0`, o segundo na `1`, e assim por diante.

# 🧵 Entrada de Strings em C: `fgets`, `gets` e `scanf`

Ao trabalhar com entrada de dados do tipo texto na linguagem C, é importante entender as diferenças entre as funções `fgets()`, `gets()` e `scanf("%s")`. Abaixo estão exemplos, vantagens, desvantagens e um comparativo entre elas.

---

## 1️⃣ `fgets()`

```c
char nome[50];
fgets(nome, sizeof(nome), stdin);
````

✅ Vantagens:
Captura espaços.

Evita estouro de memória.

Adiciona \0 automaticamente.

Mantém o \n (Enter), que pode ser removido manualmente:
```c
int i = 0;
while (nome[i] != '\0') {
    if (nome[i] == '\n') {
        nome[i] = '\0';
        break;
    }
    i++;
}
````
2️⃣ gets() ⚠️ NÃO RECOMENDADO
````c
char nome[50];
gets(nome); // ⚠️ NÃO RECOMENDADO
````
❌ Desvantagens:
Não verifica o tamanho do vetor.

Pode causar falhas de segurança (buffer overflow).

Foi removida do padrão C11.

3️⃣ scanf("%s", ...)
```c
3️⃣ scanf("%s", ...)
````
⚠️ Limitações:
Não captura espaços (apenas a primeira palavra).

Pode causar estouro se o usuário digitar mais do que o vetor comporta.

## 🏁 Comparativo entre funções

| Função        | Captura espaços | Verifica tamanho | Segurança  | Recomendação   |
|---------------|------------------|------------------|------------|----------------|
| `fgets()`     | ✅ Sim           | ✅ Sim           | ✅ Alta     | ⭐ Recomendada  |
| `gets()`      | ❌ Não           | ❌ Não           | ❌ Baixa    | 🚫 Evitar       |
| `scanf("%s")` | ❌ Não           | ❌ Não           | ⚠️ Média    | ⚠️ Limitada     |



### 🧾 Exemplo de declaração:

```c
int numeros[5];     // vetor de 5 inteiros
char nome[50];      // vetor de 50 caracteres
float notas[10];    // vetor de 10 números reais
````

### Exemplo de captura de nome e exibição com SCANF, 
⚠️ Importante:
O scanf("%s", nome); não captura espaços. Se o usuário digitar Leandro Silva, apenas Leandro será armazenado.

Para capturar nomes completos com espaços, o ideal continua sendo fgets().

```c
#include <stdio.h>

int main() {
    char nome[50];
    int i = 0;

    printf("Digite seu nome (sem espaços): ");
    scanf("%s", nome);  // Captura apenas até o primeiro espaço

    printf("Seu nome é: ");
    while (nome[i] != '\0') {
        printf("%c", nome[i]);
        i++;
    }

    return 0;
}

````

## Capturar e exibir nome completo, utilizando FOR e Vetor
```c
#include <stdio.h>

int main() {
    char nome[50];
    int i;

    printf("Digite seu nome completo: ");
    fgets(nome, sizeof(nome), stdin); // Captura com espaços

    printf("Seu nome é: ");
    for (i = 0; nome[i] != '\0'; i++) {
        printf("%c", nome[i]);
    }

    return 0;
}
````
## Capturar e exibir número inteiro, utilizando FOR e Vetor
```c
#include <stdio.h>

int main() {
    int inteiros[5];
    float reais[5];
    int i;

    printf("Digite 5 números inteiros:\n");
    for (i = 0; i < 5; i++) {
        printf("Inteiro %d: ", i + 1);
        scanf("%d", &inteiros[i]);
    }

    printf("Digite 5 números reais:\n");
    for (i = 0; i < 5; i++) {
        printf("Real %d: ", i + 1);
        scanf("%f", &reais[i]);
    }

    printf("\nNúmeros digitados:\n");
    for (i = 0; i < 5; i++) {
        printf("Inteiro %d: %d | Real %d: %.2f\n", i + 1, inteiros[i], i + 1, reais[i]);
    }

    return 0;
}

````
# Capturar, exibir e alterar nome, utilizando FOR e Vetor
```c
#include <stdio.h>
#include <string.h>

int main() {
    char nome[50];
    int i;

    printf("Digite seu nome: ");
    fgets(nome, sizeof(nome), stdin);

    printf("Nome original: ");
    for (i = 0; nome[i] != '\0'; i++) {
        printf("%c", nome[i]);
    }

    // Alterando o nome
    strcpy(nome, "Nome Alterado");

    printf("\nNome após alteração: ");
    for (i = 0; nome[i] != '\0'; i++) {
        printf("%c", nome[i]);
    }

    return 0;
}

````

## Acessando elementos com For, utilizando FOR e Vetor
```c
for (int i = 0; i < 5; i++) {
    printf("%d\n", numeros[i]);
}
````

## Capturar e exibir nome com, utilizando While e Vetor
```c
#include <stdio.h>

int main() {
    char nome[50];
    int i = 0;

    printf("Digite seu nome completo: ");
    fgets(nome, sizeof(nome), stdin); // Captura com espaços

    printf("Seu nome é: ");
    while (nome[i] != '\0') {
        printf("%c", nome[i]);
        i++;
    }

    return 0;
}

````
## Capturar e exibir números inteiros e reais, utilizando While e Vetor
```c

````
##  Capturar, exibir e alterar nome, utilizando While e Vetor
```c
#include <stdio.h>
#include <string.h>

int main() {
    char nome[50];
    int i = 0;

    printf("Digite seu nome: ");
    fgets(nome, sizeof(nome), stdin);

    printf("Nome original: ");
    while (nome[i] != '\0') {
        printf("%c", nome[i]);
        i++;
    }

    // Alterando o nome
    strcpy(nome, "Nome Alterado");

    i = 0;
    printf("\nNome após alteração: ");
    while (nome[i] != '\0') {
        printf("%c", nome[i]);
        i++;
    }

    return 0;
}


````



