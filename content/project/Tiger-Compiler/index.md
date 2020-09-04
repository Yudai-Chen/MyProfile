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

Please check the [Tiger Language Manual](tiger.pdf).

## 1. Lexical Analysis

The main task of lexical analysis is to break the input into individual tokens, and keep the position of every token. To achieve a lexical analyzer, we use Lex, an automatic lexical analyzer generator, to translate regular expressions into a DFA. 

There are two kinds of input words to deal with: one is the lexical tokens, including reserved words and punctuation symbols; the other is the special character sequences, such as string constants, comments, escape sequences and so on. To process the former kind, we write regular expression to specify the lexical tokens; while for the latter one, we use state machines to deal with them. 

## 2. Syntax Analysis

The main task for syntax analysis is to parse the phrase structure of the program. To achieve a syntax parser, I use Yacc, a classic and widely used parser generator, to complete LR parsing for me.

## 3. Semantic Analysis

After the syntax analysis, we get an abstract tree. This tree will be transmitted to "Semant" module to do the semantic analysis whose main tasks are to construct environment tables and type check. In Semant module, we will call the Translate module to generate the intermediate code.

## 4. Trace Produce

After a few previous steps, we finally got a Intermediate Representation Tree. What’s more has to be done is to convert the Intermediate Representation Tree to assembly language or machine language. However, there are certain aspects of the Tree language that do not correspond exactly with machine languages, and some aspects of the Tree language interfere with compile-time optimization analyses. 

To deal with this problem, we should perform an extra step, to translate the original Tree to another form, which is easy to translate to machine language. 

## 5. Target Code Generation

I implemented the Maximal Munch algorithm to generate x86 instructions. For each of the abstract assembly-language types, I attached it with an instruction. 

## 6. Performance Tests

For more information, please refer to the PDF attached to this page.