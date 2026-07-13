# Lecture 1: Tokenization

Goto [Home page](/README.md)

## Overview
How to cut the text to pass it to the model

## Types:
1. Arbitrary:
   > $\color{DarkGreen}{\text{A}}$ $\color{Red}{\text{cute}}$ $\color{Brown}{\text{teddy bear}}$ $\color{Blue}{\text{is}}$ $\color{Orange}{\text{reading}}$
2. Word-level:
   > $\color{DarkGreen}{\text{A}}$ $\color{Red}{\text{cute}}$ $\color{Brown}{\text{teddy}}$ $\color{green}{\text{bear}}$ $\color{Blue}{\text{is}}$ $\color{Orange}{\text{reading}}$
   
   Cons: bear & bears will be considered two different entities ( as well; read, reads, and readings)
3. Subword-level:
   > $\color{DarkGreen}{\text{A}}$ $\color{Red}{\text{cute}}$ $\color{Brown}{\text{ted}}$ $\color{DarkRed}{\text{-dy}}$ $\color{green}{\text{bear}}$ $\color{Blue}{\text{is}}$ $\color{Orange}{\text{read}}$ $\color{DarkYellow}{\text{-ing}}$
   
   Cons: Sequence is longer (make model more complicated)

## summary 
|      Method     |    Pros   | Cons |
| --------------- | -------- | -------- |
| Word-level      | Cell 2   | Cell 3   |
| Subword-level   | Cell 5   | Cell 6   |
| Character-level | ||

Goto [Home page](/README.md)
