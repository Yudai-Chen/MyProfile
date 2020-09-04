---
title: Tiger Compiler
summary: A simple toy complier.
date: "2018-06-10T00:00:00Z"
external_link: ""

image:
  caption: Yudai Chen
  focal_point: Smart
  
slides: example
---
 A toy compiler that includes lexical analysis, parsing, AST generation, code generation, and GUI. It supports comments, basic data types / operations, and function calls. 

Tiger language:

Please check the `{{% staticref "files/tiger.pdf" %}}Tiger Language Manual{{% /staticref %}}`.

## 1. Lexical Analysis

The main task of lexical analysis is to break the input into individual tokens, and keep the position of every token. To achieve a lexical analyzer, we use Lex, an automatic lexical analyzer generator, to translate regular expressions into a DFA. 

There are two kinds of input words to deal with: one is the lexical tokens, including reserved words and punctuation symbols; the other is the special character sequences, such as string constants, comments, escape sequences and so on. To process the former kind, we write regular expression to specify the lexical tokens; while for the latter one, we use state machines to deal with them. 

## 2. Syntax Analysis



