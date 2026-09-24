CC = cc
LEX = flex

# Ejercicio a compilar/correr. Uso: make run EJE=eje3
EJE ?= eje1

scanner: main.c lex.yy.c
	$(CC) main.c lex.yy.c -o scanner

lex.yy.c: $(EJE)/scanner.l
	$(LEX) -o lex.yy.c $(EJE)/scanner.l

.PHONY: run clean
run: scanner
	./scanner < $(EJE)/input.txt

clean:
	rm -f scanner lex.yy.c
