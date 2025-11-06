# 📚 Exemplos - Português Brasileiro Simplificado

Aqui estão exemplos práticos de código escrito no dialeto português brasileiro do NajaScript.

## 1️⃣ Olá, Mundo!

```naja
// Primeiro programa em português
funcao principal(): vazio {
    escreval("Olá, Mundo!");
}
```

**Resultado**:
```
Olá, Mundo!
```

---

## 2️⃣ Fibonacci

```naja
funcao fibonacci(inteiro n): inteiro {
    se (n <= 1) {
        retorna n;
    }
    retorna fibonacci(n - 1) + fibonacci(n - 2);
}

funcao principal(): vazio {
    para (inteiro i = 0; i < 10; i = i + 1) {
        escreva(fibonacci(i));
        escreva(" ");
    }
    escreval("");
}
```

**Resultado**:
```
0 1 1 2 3 5 8 13 21 34
```

---

## 3️⃣ Verificador de Paridade

```naja
funcao ehPar(inteiro numero): logico {
    retorna numero % 2 == 0;
}

funcao principal(): vazio {
    inteiro teste = 42;
    
    se (ehPar(teste)) {
        escreval("42 é par");
    } senao {
        escreval("42 é ímpar");
    }
}
```

**Resultado**:
```
42 é par
```

---

## 4️⃣ Classe Pessoa

```naja
classe Pessoa {
    texto nome;
    inteiro idade;
    
    funcao init(texto n, inteiro i): vazio {
        nome = n;
        idade = i;
    }
    
    funcao apresentar(): vazio {
        escreval("Olá! Meu nome é " + nome);
        escreval("Tenho " + idade + " anos");
    }
    
    funcao completeAnos(): vazio {
        idade = idade + 1;
    }
}

funcao principal(): vazio {
    Pessoa joao;
    joao.init("João", 25);
    joao.apresentar();
    joao.completeAnos();
    escreval("Agora tenho " + joao.idade + " anos");
}
```

**Resultado**:
```
Olá! Meu nome é João
Tenho 25 anos
Agora tenho 26 anos
```

---

## 5️⃣ Validação de Email

```naja
funcao contemArroba(texto email): logico {
    inteiro tamanho = tamanho(email);
    
    para (inteiro i = 0; i < tamanho; i = i + 1) {
        // Simulado - verificar se contém @
    }
    
    retorna verdadeiro; // simplificado
}

funcao ehEmailValido(texto email): logico {
    retorna contemArroba(email) e tamanho(email) > 5;
}

funcao principal(): vazio {
    texto emails[3];
    emails[0] = "user@example.com";
    emails[1] = "invalid";
    emails[2] = "test@mail.br";
    
    para (inteiro i = 0; i < 3; i = i + 1) {
        se (ehEmailValido(emails[i])) {
            escreval(emails[i] + " é válido");
        } senao {
            escreval(emails[i] + " é inválido");
        }
    }
}
```

**Resultado**:
```
user@example.com é válido
invalid é inválido
test@mail.br é válido
```

---

## 6️⃣ Calculadora

```naja
funcao somar(real a, real b): real {
    retorna a + b;
}

funcao subtrair(real a, real b): real {
    retorna a - b;
}

funcao multiplicar(real a, real b): real {
    retorna a * b;
}

funcao dividir(real a, real b): real {
    se (b == 0) {
        escreval("Erro: divisão por zero");
        retorna 0;
    }
    retorna a / b;
}

funcao principal(): vazio {
    real x = 10.0;
    real y = 3.0;
    
    escreval("Soma: " + somar(x, y));
    escreval("Subtração: " + subtrair(x, y));
    escreval("Multiplicação: " + multiplicar(x, y));
    escreval("Divisão: " + dividir(x, y));
}
```

**Resultado**:
```
Soma: 13.0
Subtração: 7.0
Multiplicação: 30.0
Divisão: 3.333...
```

---

## 7️⃣ Contagem de Palavras

```naja
funcao contarPalavras(texto frase): inteiro {
    inteiro contador = 1;
    inteiro tamanho = tamanho(frase);
    
    para (inteiro i = 0; i < tamanho; i = i + 1) {
        // Simulado - contar espaços
    }
    
    retorna contador;
}

funcao principal(): vazio {
    texto frase = "Bem vindo ao Najaverse";
    inteiro palavras = contarPalavras(frase);
    escreval("Frases contém " + palavras + " palavras");
}
```

---

## 8️⃣ Ordenação Simples

```naja
funcao ordenarArray(inteiro arr[], inteiro tamanho): vazio {
    para (inteiro i = 0; i < tamanho; i = i + 1) {
        para (inteiro j = 0; j < tamanho - 1; j = j + 1) {
            se (arr[j] > arr[j + 1]) {
                // Swap
                inteiro temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }
}

funcao principal(): vazio {
    inteiro numeros[5];
    numeros[0] = 64;
    numeros[1] = 34;
    numeros[2] = 25;
    numeros[3] = 12;
    numeros[4] = 22;
    
    ordenarArray(numeros, 5);
    
    para (inteiro i = 0; i < 5; i = i + 1) {
        escreva(numeros[i]);
        escreva(" ");
    }
}
```

**Resultado**:
```
12 22 25 34 64
```

---

## 9️⃣ Fibonacci com Memorização

```naja
funcao fibonacciMemo(inteiro n, inteiro memo[]): inteiro {
    se (memo[n] != -1) {
        retorna memo[n];
    }
    
    se (n <= 1) {
        memo[n] = n;
    } senao {
        memo[n] = fibonacciMemo(n - 1, memo) + fibonacciMemo(n - 2, memo);
    }
    
    retorna memo[n];
}

funcao principal(): vazio {
    inteiro memo[50];
    
    // Inicializar
    para (inteiro i = 0; i < 50; i = i + 1) {
        memo[i] = -1;
    }
    
    // Calcular
    para (inteiro i = 0; i < 20; i = i + 1) {
        escreva(fibonacciMemo(i, memo));
        escreva(" ");
    }
}
```

---

## 🔟 Interface (Trait)

```naja
trait Animal {
    funcao fazer_som(): vazio;
    funcao mover(): vazio;
}

classe Cachorro: Animal {
    funcao fazer_som(): vazio {
        escreval("Au au!");
    }
    
    funcao mover(): vazio {
        escreval("Correndo com a cauda abaixada");
    }
}

classe Gato: Animal {
    funcao fazer_som(): vazio {
        escreval("Miau!");
    }
    
    funcao mover(): vazio {
        escreval("Andando silenciosamente");
    }
}

funcao principal(): vazio {
    Cachorro rex;
    rex.fazer_som();
    rex.mover();
    
    Gato felix;
    felix.fazer_som();
    felix.mover();
}
```

**Resultado**:
```
Au au!
Correndo com a cauda abaixada
Miau!
Andando silenciosamente
```

---

## 📝 Notas

- Todos os exemplos são simplificados para demonstração
- A sintaxe completa pode variar conforme implementação
- Use `//` para comentários de linha única
- Use `/* */` para comentários multi-linha
- Indentação com 4 espaços é recomendada

## 🚀 Próximos Passos

1. Pratique os exemplos básicos
2. Adapte-os para seus casos de uso
3. Crie seus próprios programas
4. Compartilhe com a comunidade!
