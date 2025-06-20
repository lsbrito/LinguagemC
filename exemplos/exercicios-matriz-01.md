## 🌿 Lista de Exercícios – Matrizes em Linguagem C

#### 📚 Utilize apenas if, else, for, while e matriz.
#### 💡 Evite o uso de funções externas, ponteiros, structs ou bibliotecas além de stdio.h.

✅ Questão 1 (Resolvida)
Tabuleiro de Números Ímpares:
Crie uma matriz 3x3 e preencha com os 9 primeiros números ímpares em ordem crescente. Em seguida, imprima a matriz na tela no formato de tabela.

```c
#include <stdio.h>

int main() {
    int matriz[3][3];
    int valor = 1; // Primeiro número ímpar

    // Preencher a matriz com números ímpares
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            matriz[i][j] = valor;
            valor += 2; // Próximo número ímpar
        }
    }

    // Exibir a matriz
    printf("Matriz de Números Ímpares:\n");
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            printf("%2d ", matriz[i][j]);
        }
        printf("\n");
    }

    return 0;
}
```
✅ Questão 2 (Resolvida)
Contagem de Números Pares em uma Matriz:
Leia os valores de uma matriz 4x4 e conte quantos números pares ela possui. Exiba a matriz e o total de números pares encontrados.

```c
#include <stdio.h>

int main() {
    int matriz[4][4];
    int pares = 0;

    // Leitura da matriz
    printf("Digite os valores da matriz 4x4:\n");
    for (int i = 0; i < 4; i++) {
        for (int j = 0; j < 4; j++) {
            scanf("%d", &matriz[i][j]);
            if (matriz[i][j] % 2 == 0) {
                pares++;
            }
        }
    }

    // Impressão da matriz
    printf("Matriz digitada:\n");
    for (int i = 0; i < 4; i++) {
        for (int j = 0; j < 4; j++) {
            printf("%3d ", matriz[i][j]);
        }
        printf("\n");
    }

    printf("Quantidade de números pares: %d\n", pares);

    return 0;
}
```

📝 Questões 3 - Caminho do Robô Explorador:
Um robô explora um terreno representado por uma matriz 5x5 com valores 0 (livre) ou 1 (obstáculo). Conte quantos caminhos livres existem.

📝 Questões 4 - Espelho Vertical:
Leia uma matriz 3x4 e crie uma nova matriz que seja o espelho vertical da original.

📝 Questões 5 - Maior Elemento da Diagonal Principal:
Leia uma matriz quadrada 4x4 e encontre o maior valor da diagonal principal.

📝 Questões 6 - Soma das Bordas da Matriz:
Leia uma matriz 4x4 e calcule a soma dos elementos que estão nas bordas (primeira/última linha e coluna).

📝 Questões 7 - Temperatura Média Semanal:
Uma matriz 7x4 armazena a temperatura de 7 dias em 4 horários diferentes. Calcule a média de temperatura de cada dia.

📝 Questões 8 - Jogo da Velha (Início):
Preencha uma matriz 3x3 com os valores 0 (vazio), 1 (X), 2 (O). Conte quantos X e quantos O existem.

📝 Questões 9 - Imagem em Preto e Branco:
Uma imagem P&B é representada por uma matriz 10x10 com valores 0 (preto) e 255 (branco). Conte quantos pixels brancos há na imagem.

📝 Questões 10 - Verificador de Linhas Iguais:
Leia uma matriz 3x3 e verifique se existe alguma linha com todos os elementos iguais.

📝 Questões 11 - Soma de Colunas Pares:
Dada uma matriz 5x5, calcule a soma dos elementos das colunas pares (índices 0, 2, 4).

📝 Questões 12 -Detectando Calor Extremo:
Matriz 5x7 armazena temperaturas. Marque com 1 as posições onde a temperatura ultrapassa 40°C e com 0 caso contrário.

📝 Questões 13 - Contador de Números Negativos:
Leia uma matriz 6x6 com inteiros e conte quantos são negativos.

📝 Questões 14 - Notas de Alunos:
Matriz 5x3 com notas de 5 alunos em 3 provas. Calcule a média de cada aluno e diga se foi aprovado (média ≥ 7).

📝 Questões 15 - Transformar Matriz em Triangular Superior:
Zere os valores abaixo da diagonal principal de uma matriz 4x4.

📝 Questões 16 - Troca de Linhas:
Leia uma matriz 4x4 e troque a 1ª linha com a última.

📝 Questões 17 - Soma de uma Linha Específica:
Dada uma matriz 5x5, some todos os elementos da linha 2 (índice 1).

📝 Questões 18 - Matriz Identidade Falsa:
Crie uma matriz 4x4 com 1 na diagonal principal e 0 no restante. (Matriz identidade).

📝 Questões 19 - Jogo de Batalha Naval (Visualização):
Matriz 10x10 com valores 0 (água) e 1 (barco). Mostre a matriz com ~ para água e # para barco.

📝 Questões 20 - Quantos Três?:
Leia uma matriz 4x4 e diga quantas vezes o número 3 aparece.

📝 Questões 21 -Soma das Duas Diagonais:
Em uma matriz 5x5, calcule a soma da diagonal principal e diagonal secundária.

📝 Questões 22 - Tabuleiro Numérico com Zonas de Impacto:
Crie uma matriz 5x5 com valores aleatórios entre 1 e 20. Imprima a matriz e marque com * as posições que têm valor maior que 15.
