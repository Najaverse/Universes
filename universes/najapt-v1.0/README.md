# Najapt - Programação em Português

Najapt é um dialeto do NajaScript que permite programar **100% em português**, mantendo toda a performance e recursos do compilador original.

## O que é Najapt?

Najapt é um transpilador que converte código escrito em português para NajaScript, que é então compilado para binários nativos otimizados.

### Características

✅ **Sintaxe 100% em Português** - Use `função`, `classe`, `se`, `enquanto` naturalmente  
✅ **Performance Máxima** - Compila para código nativo com otimizações O3  
✅ **Compilador Standalone** - Não precisa de dependências externas  
✅ **Compatível com NajaScript** - Pode usar bibliotecas e módulos Naja  
✅ **Multiplataforma** - Windows, Linux, macOS  
✅ **Sem Runtime** - Gera executáveis puros  

## Instalação

### Opção 1: Baixar o compilador pré-compilado

Acesse o site de downloads e baixe `najapt` para sua plataforma.

### Opção 2: Via Najaverse

```bash
naja universes install najapt-v1.0
```

## Quickstart

### 1. Criar seu primeiro programa

Crie um arquivo `olá.pt`:

```portuguese
função principal(): vazio {
    escrever("Olá, Mundo!");
}
```

### 2. Compilar

```bash
najapt olá.pt
```

### 3. Executar

```bash
./olá
```

## Mapeamento de Palavras-chave

| Português | Naja | Descrição |
|-----------|------|-----------|
| `função` | `fun` | Declaração de função |
| `classe` | `class` | Declaração de classe |
| `estrutura` | `struct` | Declaração de estrutura |
| `se` | `if` | Condicional if |
| `senão` | `else` | Condicional else |
| `senão_se` | `else if` | Condicional else if |
| `enquanto` | `while` | Loop while |
| `para` | `for` | Loop for |
| `quebra` | `break` | Break loop |
| `continua` | `continue` | Continue loop |
| `retornar` | `return` | Return statement |
| `novo` | `new` | Criar nova instância |
| `nulo` | `null` | Valor nulo |
| `verdadeiro` | `true` | Booleano true |
| `falso` | `false` | Booleano false |
| `constante` | `const` | Constante imutável |
| `genérico` | `<T>` | Genéricos |
| `importar` | `import` | Importar módulo |
| `exportar` | `export` | Exportar símbolo |
| `async` | `async` | Função assíncrona |
| `aguardar` | `await` | Aguardar promise |
| `tentar` | `try` | Bloco try/catch |
| `pegar` | `catch` | Pegar exceção |
| `finalmente` | `finally` | Bloco finally |

## Tipos de Dados

| Português | Naja | Descrição |
|-----------|------|-----------|
| `inteiro` | `int` | Inteiro 32-bit |
| `grande_inteiro` | `long` | Inteiro 64-bit |
| `decimal` | `float` | Número decimal |
| `texto` | `string` | Cadeia de caracteres |
| `booleano` | `bool` | Valor booleano |
| `nulo` | `null` | Tipo nulo |
| `qualquer` | `any` | Tipo dinâmico |
| `matriz` | `array` | Array de elementos |
| `dicionário` | `map` | Mapa chave-valor |
| `vazio` | `void` | Sem retorno |

## Exemplos

### Fibonacci

```portuguese
função fibonacci(n: inteiro): inteiro {
    se (n <= 1) {
        retornar n;
    }
    retornar fibonacci(n - 1) + fibonacci(n - 2);
}

função principal(): vazio {
    para (i: inteiro = 0; i < 10; i = i + 1) {
        escrever(fibonacci(i));
        escrever(" ");
    }
    escrever("\n");
}
```

### Classe e Métodos

```portuguese
classe Pessoa {
    nome: texto;
    idade: inteiro;
    
    função saudação(): vazio {
        escrever("Olá, meu nome é " + este.nome);
    }
}

função principal(): vazio {
    pessoa: Pessoa = novo Pessoa();
    pessoa.nome = "João";
    pessoa.idade = 25;
    pessoa.saudação();
}
```

### Loop e Condicional

```portuguese
função principal(): vazio {
    para (i: inteiro = 1; i <= 5; i = i + 1) {
        se (i % 2 == 0) {
            escrever(i + " é par\n");
        } senão {
            escrever(i + " é ímpar\n");
        }
    }
}
```

## Comandos do Compilador

```bash
# Compilar e gerar executável
najapt arquivo.pt

# Compilar com otimizações máximas
najapt arquivo.pt --release

# Compilar em modo debug com símbolos
najapt arquivo.pt --debug

# Especificar nome do executável
najapt arquivo.pt -o meu_programa

# Modo verbose (mostra detalhes)
najapt arquivo.pt --verbose

# Verificar sintaxe sem compilar
najapt arquivo.pt --check
```

## Limitações Atuais

- Macros não suportadas (planejado para v2.0)
- Genéricos básicos apenas (sem tipos variádicos)
- Sem suporte a múltiplas threads (planejado)

## Suporte e Comunidade

- Documentação: https://najapt.dev
- GitHub: https://github.com/Najaverse/najapt
- Reportar bugs: https://github.com/Najaverse/najapt/issues
- Discord: Comunidade Najaverse

## Licença

MIT - Sinta-se livre para usar, modificar e distribuir!

---

**Desenvolvido com ❤️ para a comunidade portuguesa de programação**
