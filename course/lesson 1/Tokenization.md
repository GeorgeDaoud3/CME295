# Lecture 1: Tokenization

Goto [Home page](/README.md)

## Overview
How to cut the text to pass it to the model

### Types:
1. Arbitrary:
   > $\color{DarkGreen}{\text{A}}$ $\color{Red}{\text{cute}}$ $\color{Brown}{\text{teddy bear}}$ $\color{Blue}{\text{is}}$ $\color{Orange}{\text{reading}}$
2. Word-level:
   > $\color{DarkGreen}{\text{A}}$ $\color{Red}{\text{cute}}$ $\color{Brown}{\text{teddy}}$ $\color{green}{\text{bear}}$ $\color{Blue}{\text{is}}$ $\color{Orange}{\text{reading}}$
   
   Cons: bear & bears will be considered two different entities ( as well; read, reads, and readings)
3. Subword-level:
   > $\color{DarkGreen}{\text{A}}$ $\color{Red}{\text{cute}}$ $\color{Brown}{\text{ted}}$ $\color{DarkRed}{\text{-dy}}$ $\color{green}{\text{bear}}$ $\color{Blue}{\text{is}}$ $\color{Orange}{\text{read}}$ $\color{DarkYellow}{\text{-ing}}$
   
   Cons: Sequence is longer (make model more complicated)

### summary 
|      Method     |    Pros   | Cons |
| --------------- | -------- | -------- |
| Word-level      | simple | Risk of OOV (out of Vocabulary)   |
|                 | Interpretable | Does not leverage knowledge of root |
| Subword-level   | Leverage common prefixe & suffixes   | Risk of OOV (less than word-level) |
|                 | Learned from the data   | |
| Character-level | Small chances of OOV| slower|
||Robust to casing and misspellings|Not interpretable|

## Token Representation 
Convert text to numerics

### Types:
1. Naiive (one-hot encoding):
   Ex:
   soft=(1,0,0)
   book=(0,1,0)
   teddy bear=(0,1,1)

   Cosine similarity fails as
   <soft, book>=0
   <Teddy bear, book>=0
   <soft, Teddy bear>=0
   
2. Learned embedding
   Ex:
   soft=(0.95,0.32,0.01)
   <Teddy bear, book> $ \approx $ 0
   <soft, Teddy bear> $ \approx $ 1

### How to get the leaened embedding?
[word2vec](/Script/word2vec/index.md)

Goto [Home page](/README.md)
