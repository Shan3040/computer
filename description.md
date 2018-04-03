# computer
Description:
**Symbol table***
Lexical analyzer reads token by token and puts it in symbol table.
compilation:
           lex block.l
           yacc -d block.y
           g++ lex.yy.c 
           ./a.out
           
***ifelse***
Embed else with null statement to satisfy ifelse.
compilation:
           lex n.l
           yacc n.y
           gcc -o n lex.yy.c
           ./n
           
***while loop***
Convert for and do while loop to while loop
compilation:
           lex loop.l
           yacc -dy loop.y
           gcc lex.yy.c y.tab.c -o loop
           ./loop
           
***syntaxtree***
Displays syntax tree for given expression.
compilation:
           lex syntree.l
           yacc -dy syntree.y
           g++ lex.yy.c y.tab.c -ll
           ./a.out
           
***3-address***
Outputs 3 address statement for given expression.
            
***backpatch***
Backpatches if else statement,array of statement or block of statement.

[for 3-address ad backpatch same compilation like syntax tree...]

***Basic block***
Displays three address,Basic block,control flow.
            flex threeaddr.l
            bison threeaddr.y
            g++ lex.yy.c threeaddr.tab.c -ll
            ./a.out
            
***labelled tree***
Displays DAG for the given expression.
            lex syntree.l
            yacc syntree.y
            g++ lex.yy.c syntree.tab.c -ll
            ./a.out
