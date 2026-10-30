# Compilador — Analisador Léxico e Sintático

Projeto da disciplina de **Compiladores (UNIFEI)**: front-end de um compilador para uma
linguagem imperativa simples, construído em Python com a biblioteca
[PLY](https://www.dabeaz.com/ply/) (implementação de Lex e Yacc).

## ⚙️ O que foi implementado

- **Analisador léxico** — reconhece identificadores, números inteiros e de ponto flutuante,
  operadores aritméticos, relacionais e lógicos, delimitadores e palavras reservadas;
  reporta caracteres inválidos
- **Tabela de símbolos** — registra palavras reservadas e identificadores encontrados
- **Analisador sintático (LALR)** — valida o programa segundo a gramática da linguagem e
  monta uma árvore sintática em forma de tuplas
- **Tratamento de erros** de sintaxe, indicando o token onde ocorreu o problema

## 📝 A linguagem

| Recurso | Sintaxe |
|---|---|
| Tipos básicos | `int`, `char`, `bool` |
| Arrays (multidimensionais) | `int[10][5] matriz;` |
| Registros | `record { int id; char nome; } r;` |
| Atribuição | `x = expressao;` |
| Condicional | `if (cond) comando else comando` |
| Repetição | `while (cond) comando` · `do comando while (cond);` |
| Entrada e saída | `read(x);` · `print(expressao);` |
| Controle | `break;` |
| Operadores | `+ - * /` · `== != < <= > >=` · `&& \|\| !` |

Todo programa é um bloco `{ declarações comandos }`, e blocos podem ser aninhados.

## ▶️ Como executar

```bash
pip install ply
python principal.py
```

Digite o código linha por linha e finalize com `.` em uma linha separada. O programa
imprime a árvore sintática resultante ou as mensagens de erro.

## 🛠️ Tecnologias

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
PLY (Python Lex-Yacc)
