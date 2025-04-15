#### 📄 `constantes.md`
```md
# 🧱 Constantes em C

Constantes são valores que **nunca mudam** depois de definidos.

## 🔐 Como declarar:
```c
#define PI 3.14
const int MAX_USUARIOS = 100;
```

## 💡 Exemplo:
```c
#define DESCONTO 0.10
float precoFinal = precoOriginal * (1 - DESCONTO);
```

## ✅ Dica de ouro
Use constantes para representar valores que fazem sentido no contexto do seu programa.
