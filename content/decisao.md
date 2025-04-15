# 🔀 Estruturas de Decisão

As **estruturas de decisão** permitem que o programa faça **escolhas** com base em condições, ou seja, ele executa diferentes blocos de código dependendo do valor ou estado de uma variável. Essa capacidade é essencial para construir programas interativos e dinâmicos.

### 📌 Por que usar estruturas de decisão?
Sem estruturas de decisão, o código seria executado de forma linear e sem flexibilidade, impossibilitando a implementação de funcionalidades mais complexas, como menus, validações e decisões baseadas no comportamento do usuário.

---

## 🧪 Exemplo com `if` e `else`

O `if` é a estrutura de decisão mais básica e permite que o programa execute um bloco de código se uma condição for verdadeira, e outro caso contrário.

```c
#include <stdio.h>

int main() {
    int idade = 18;

    if (idade >= 18) {
        printf("Maior de idade\n");
    } else {
        printf("Menor de idade\n");
    }

    return 0;
}
````
### Explicação:

O `if` verifica a condição `idade >= 18`. Se for verdadeira, o código dentro do bloco `if` é executado.

Caso contrário, o código dentro do bloco `else` é executado.

O programa exibirá "Maior de idade" ou "Menor de idade", dependendo do valor de `idade`.

---

### 🧠 Dicas:

**Operadores de comparação**: O `>=` é um operador de comparação. Outros operadores comuns são:

- `==` (igual)
- `!=` (diferente)
- `>` (maior que)
- `<` (menor que)
- `<=` (menor ou igual)

---

### 🎯 Exemplo com `switch`

O `switch` é utilizado quando você tem várias opções e quer verificar a igualdade de uma variável com diferentes valores possíveis. Ele é útil para simplificar o código quando há muitas condições `if-else`.

````c
#include <stdio.h>

int main() {
    int opcao = 2;

    switch(opcao) {
        case 1:
            printf("Novo jogo\n");
            break;
        case 2:
            printf("Carregar jogo\n");
            break;
        default:
            printf("Opção inválida\n");
    }

    return 0;
}
````
### Explicação:

O `switch` verifica o valor de `opcao`. Se for igual a 1, executa o código do `case 1`; se for igual a 2, executa o código do `case 2`; caso contrário, executa o código do `default`.

O `break` é importante para terminar a execução do `switch` após a correspondência com um `case`. Se você não usar o `break`, o código pode continuar a executar os outros casos mesmo sem uma correspondência.

---

### 🧠 Dicas:

- O `default` é opcional, mas é útil para capturar qualquer valor que não tenha sido previsto nos `case`.
- O `switch` é geralmente mais eficiente do que vários `if-else` aninhados quando se tem muitas opções.

---

### 🚀 Novo Exemplo com `if` e operadores lógicos

Exemplo com múltiplas condições usando operadores lógicos:

````c
#include <stdio.h>

int main() {
    int idade = 22;
    char cidadania = 'B'; // B para Brasileiro, E para Estrangeiro

    if (idade >= 18 && cidadania == 'B') {
        printf("Você pode votar no Brasil.\n");
    } else {
        printf("Você não pode votar no Brasil.\n");
    }

    return 0;
}
````
### Explicação:

O operador lógico `&&` significa "e". A condição só será verdadeira se ambas as subcondições forem verdadeiras.

- A expressão `idade >= 18` verifica se a idade é maior ou igual a 18 anos.
- A expressão `cidadania == 'B'` verifica se a pessoa é brasileira.

Combinando essas condições, o programa verifica se a pessoa pode votar no Brasil (maior de 18 anos e brasileira).

---

### 🧠 Dicas:

Outros operadores lógicos úteis:

- `||` (ou): A condição será verdadeira se pelo menos uma das subcondições for verdadeira.
- `!` (não): Inverte o valor lógico de uma condição.

---

### 📚 Resumo:

- **if**: Executa um bloco de código se a condição for verdadeira; opcionalmente, executa outro bloco de código se a condição for falsa (`else`).
- **switch**: Verifica múltiplas opções e executa o bloco correspondente ao valor de uma variável.
- **Operadores lógicos**: Permitem combinar várias condições (por exemplo, `&&`, `||`, `!`).

Essas estruturas são fundamentais para controlar o fluxo do seu programa, permitindo que você escreva códigos mais interativos e dinâmicos. Pratique criando seus próprios exemplos!

---

### 💡 Dica Extra:

A utilização de estruturas de decisão torna seu código muito mais flexível e dinâmico, permitindo que ele se ajuste de acordo com o comportamento do usuário ou de variáveis internas. Lembre-se de usar a estrutura que mais se adequa ao problema que você está resolvendo!

