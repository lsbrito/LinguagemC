# 📥 Entrada e 📤 Saída de Dados em C

Em C, a **entrada e saída** são feitas principalmente com as funções `scanf` (entrada) e `printf` (saída), ambas da biblioteca `<stdio.h>`.  
Elas são as nossas ferramentas para interagir com quem está usando o programa — como um bate-papo entre o computador e o usuário. 😄

---

## 📥 Recebendo dados com `scanf`

```c
int idade;
printf("Digite sua idade: ");
scanf("%d", &idade);
```
## 🔍 Entenda linha por linha:

```c
printf("Digite sua idade: ");
````

Exibe a mensagem pedindo a idade do usuário.
→ Tudo entre aspas é texto literal a ser exibido.

```c
scanf("%d", &idade);
````

Lê o que o usuário digitou e guarda na variável idade.

### 🧠 Por que tem `%` e `&`?

- `%` é um **especificador de formato**:

  - `%d` = espera um número inteiro  
  - `%f` = espera um número com casas decimais  
  - `%c` = espera um único caractere  
  - `%s` = espera uma sequência de caracteres (string)

- `&` é o **endereço da variável**:

  O `scanf` precisa saber onde guardar o valor.  
  Usamos `&idade` para dizer: "guarde aqui dentro da variável idade".

> ⚠️ **Não usamos `&` com strings porque o nome do array já é um ponteiro!** 🧵

## 📤 Exibindo dados com printf

```c
printf("Você tem %d anos.\n", idade);
````

### 🔍 Entenda

A string `"Você tem %d anos.\n"` é exibida exatamente como está.  
O `%d` será substituído pelo valor da variável `idade`.  
O `\n` pula uma linha (como apertar Enter).

---

### 🧪 Tabela de Especificadores

| Tipo de dado | Especificador | Exemplo de uso no `scanf`         |
|--------------|----------------|-----------------------------------|
| `int`        | `%d`           | `scanf("%d", &idade);`            |
| `float`      | `%f`           | `scanf("%f", &altura);`           |
| `char`       | `%c`           | `scanf("%c", &letra);`            |
| `string`     | `%s`           | `scanf("%s", nome);`              |

> ⚠️ **Ordem Importa!**  
> No `scanf`, a ordem dos especificadores deve combinar com a ordem das variáveis.

````c
int x;
float y;
scanf("%d %f", &x, &y);  // Primeiro lê um int, depois um float
````

Se inverter os formatos ou esquecer o &, o programa pode funcionar errado — ou nem funcionar! 💥

## 💡 Dicas Rápidas
Sempre use & no scanf, exceto com strings.

Para limpar a tela (em alguns sistemas), use: system("clear"); ou system("cls");.

Use \n no printf para quebrar linha e deixar a saída mais limpa.

## 🎯 Desafio
Crie um programa que:

Pergunta o nome e a idade do usuário.

Imprime uma frase como:
👉 Olá João, você tem 25 anos!

````c
#include <stdio.h>

int main() {
    char nome[50];
    int idade;

    printf("Digite seu nome: ");
    scanf("%s", nome);

    printf("Digite sua idade: ");
    scanf("%d", &idade);

    printf("Olá %s, você tem %d anos!\n", nome, idade);

    return 0;
}
