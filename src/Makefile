CFLAGS=-g -O3

all: main

	cc -o main tokenizer.o history.o main.o



tokenizer.o: tokenizer.h tokenizer.c

main.o: main.c tokenizer.h history.h

history.o: history.h history.c tokenizer.h

main: tokenizer.o  history.o main.o
	cc -o $@ $^ $(CFLAGS)


clean:
	rm -f *.o main
