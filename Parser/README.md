# Instructions to run the program:

## Run the commands yourself

- Run the following in a shell:
  - `lex lexer.l`
  - `yacc -d parser.y`
  - `gcc lex.yy.c y.tab.c`
- This will create an executable file "./a.out" which can then be run

Write a parser to identify the following grammar:

stmts : stmts stmt
      | epsilon

stmt  : ;
      | expr ;
      | if (expr) stmt
      | if (expr) stmt else stmt
      | for (expr ; expr ; expr ) stmt
      | { stmts }
