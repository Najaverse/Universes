# Exemplos Najapt

## 1. Olá, Mundo!

O programa mais simples em Najapt:

```portuguese
função principal(): vazio {
    escrever("Olá, Mundo!\n");
}
```

**Compilar e executar:**
```bash
najapt olá.pt
./olá
```

**Saída:**
```
Olá, Mundo!
```

---

## 2. Variáveis e Tipos

Declarando variáveis com tipos explícitos:

```portuguese
função principal(): vazio {
    idade: inteiro = 25;
    nome: texto = "João Silva";
    salário: decimal = 3500.50;
    ativo: booleano = verdadeiro;
    
    escrever("Nome: " + nome + "\n");
    escrever("Idade: " + idade + "\n");
    escrever("Salário: R$ " + salário + "\n");
    escrever("Ativo: " + ativo + "\n");
}
```

---

## 3. Operações Matemáticas

Calculando e imprimindo resultados:

```portuguese
função principal(): vazio {
    x: inteiro = 10;
    y: inteiro = 3;
    
    escrever("x = " + x + "\n");
    escrever("y = " + y + "\n");
    escrever("x + y = " + (x + y) + "\n");
    escrever("x - y = " + (x - y) + "\n");
    escrever("x * y = " + (x * y) + "\n");
    escrever("x / y = " + (x / y) + "\n");
    escrever("x % y = " + (x % y) + "\n");
}
```

---

## 4. Estruturas Condicionais

Usando `se`, `senão_se` e `senão`:

```portuguese
função classificarNota(nota: inteiro): vazio {
    se (nota >= 90) {
        escrever("Nota A - Excelente!\n");
    } senão_se (nota >= 80) {
        escrever("Nota B - Muito bom!\n");
    } senão_se (nota >= 70) {
        escrever("Nota C - Bom!\n");
    } senão_se (nota >= 60) {
        escrever("Nota D - Satisfatório!\n");
    } senão {
        escrever("Nota F - Insuficiente!\n");
    }
}

função principal(): vazio {
    classificarNota(95);
    classificarNota(75);
    classificarNota(55);
}
```

---

## 5. Loops com For

Iterando com `para`:

```portuguese
função principal(): vazio {
    escrever("Números de 1 a 10:\n");
    
    para (i: inteiro = 1; i <= 10; i = i + 1) {
        escrever(i + " ");
    }
    
    escrever("\n\nTabuada do 7:\n");
    
    para (i: inteiro = 1; i <= 10; i = i + 1) {
        resultado: inteiro = 7 * i;
        escrever("7 x " + i + " = " + resultado + "\n");
    }
}
```

---

## 6. Loops com While

Usando `enquanto`:

```portuguese
função principal(): vazio {
    contador: inteiro = 1;
    
    escrever("Contando até 5:\n");
    
    enquanto (contador <= 5) {
        escrever(contador + "\n");
        contador = contador + 1;
    }
    
    escrever("Fim!\n");
}
```

---

## 7. Funções

Definindo e chamando funções:

```portuguese
função quadrado(numero: inteiro): inteiro {
    retornar numero * numero;
}

função saudacao(nome: texto): vazio {
    escrever("Olá, " + nome + "!\n");
}

função principal(): vazio {
    saudacao("Maria");
    saudacao("Carlos");
    
    para (i: inteiro = 1; i <= 5; i = i + 1) {
        resultado: inteiro = quadrado(i);
        escrever(i + "² = " + resultado + "\n");
    }
}
```

---

## 8. Fibonacci Recursivo

Função recursiva calculando Fibonacci:

```portuguese
função fibonacci(n: inteiro): inteiro {
    se (n <= 1) {
        retornar n;
    }
    retornar fibonacci(n - 1) + fibonacci(n - 2);
}

função principal(): vazio {
    escrever("Sequência de Fibonacci:\n");
    
    para (i: inteiro = 0; i < 10; i = i + 1) {
        resultado: inteiro = fibonacci(i);
        escrever(resultado + " ");
    }
    
    escrever("\n");
}
```

---

## 9. Números Pares e Ímpares

Usando operador módulo:

```portuguese
função principal(): vazio {
    escrever("Números pares de 1 a 20:\n");
    
    para (i: inteiro = 1; i <= 20; i = i + 1) {
        se (i % 2 == 0) {
            escrever(i + " ");
        }
    }
    
    escrever("\n\nNúmeros ímpares de 1 a 20:\n");
    
    para (i: inteiro = 1; i <= 20; i = i + 1) {
        se (i % 2 != 0) {
            escrever(i + " ");
        }
    }
    
    escrever("\n");
}
```

---

## 10. Classe Simples

Definindo uma classe com propriedades e métodos:

```portuguese
classe Retangulo {
    largura: inteiro;
    altura: inteiro;
    
    função área(): inteiro {
        retornar este.largura * este.altura;
    }
    
    função perímetro(): inteiro {
        retornar 2 * (este.largura + este.altura);
    }
}

função principal(): vazio {
    ret: Retangulo = novo Retangulo();
    ret.largura = 5;
    ret.altura = 3;
    
    escrever("Retângulo: " + ret.largura + "x" + ret.altura + "\n");
    escrever("Área: " + ret.área() + " unidades²\n");
    escrever("Perímetro: " + ret.perímetro() + " unidades\n");
}
```

---

## 11. Estrutura de Dados

Usando estruturas para agrupar dados:

```portuguese
estrutura Pessoa {
    nome: texto;
    idade: inteiro;
    cpf: texto;
}

função exibirPessoa(p: Pessoa): vazio {
    escrever("Nome: " + p.nome + "\n");
    escrever("Idade: " + p.idade + "\n");
    escrever("CPF: " + p.cpf + "\n");
}

função principal(): vazio {
    pessoa: Pessoa;
    pessoa.nome = "Ana Silva";
    pessoa.idade = 28;
    pessoa.cpf = "123.456.789-00";
    
    exibirPessoa(pessoa);
}
```

---

## 12. Break e Continue

Controlando loops com `quebra` e `continua`:

```portuguese
função principal(): vazio {
    escrever("Números até encontrar 7:\n");
    
    para (i: inteiro = 1; i <= 10; i = i + 1) {
        se (i == 7) {
            quebra;
        }
        escrever(i + " ");
    }
    
    escrever("\n\nNúmeros exceto 5:\n");
    
    para (i: inteiro = 1; i <= 10; i = i + 1) {
        se (i == 5) {
            continua;
        }
        escrever(i + " ");
    }
    
    escrever("\n");
}
```

---

## Como Compilar os Exemplos

1. Salve o código em um arquivo `.pt` (ex: `exemplo.pt`)
2. Compile com o Najapt:
   ```bash
   najapt exemplo.pt
   ```
3. Execute o programa gerado:
   ```bash
   ./exemplo
   ```

Para mais exemplos e documentação, visite https://najapt.dev
