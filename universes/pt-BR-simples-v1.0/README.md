# 🇧🇷 Português Brasileiro Simplificado

Um dialeto NajaScript simplificado com palavras-chave em português natural, ideal para educação e projetos brasileiros.

## 🎯 Objetivo

Tornar a programação mais acessível para falantes de português, especialmente para fins educacionais, mantendo compatibilidade com NajaScript.

## ✨ Features

- ✅ Palavras-chave em português natural
- ✅ Suporte a OOP com português
- ✅ Traits e Generics
- ✅ Modularização
- ✅ Compatível com NajaScript v0.5+

## 🗂️ Estrutura

```
funcao principal(): vazio {
    escreval("Olá, Mundo!");
}
```

## 📚 Exemplos de Sintaxe

### Variáveis
```naja
inteiro numero = 42;
texto mensagem = "Olá";
logico verdadeiro = verdadeiro;
```

### Funções
```naja
funcao saudacao(texto nome): texto {
    retorna "Olá, " + nome;
}
```

### Controle de Fluxo
```naja
se (numero > 0) {
    escreval("Positivo");
} senao {
    escreval("Negativo ou zero");
}

para (inteiro i = 0; i < 10; i = i + 1) {
    escreval(i);
}

enquanto (condicao) {
    // fazer algo
}
```

### Classes
```naja
classe Pessoa {
    texto nome;
    inteiro idade;
    
    funcao apresentar(): vazio {
        escreval("Meu nome é " + nome);
    }
}
```

## 📦 Instalação

```bash
naja universes install pt-BR-simples-v1.0
```

## 🚀 Uso

```bash
# Compilar programa em português
naja compile programa.pt --dialect pt-BR-simples-v1.0

# Executar
naja run programa.pt --dialect pt-BR-simples-v1.0
```

## 📖 Documentação Completa

Para aprender mais sobre esse universo, consulte `EXAMPLES.md`.

## 📝 Licença

MIT - Aberto para todos

## 👥 Criador

NajaScript Team - Comunidade Najaverse
