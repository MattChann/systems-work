ifeq ($(DEBUG), true)
	CC = gcc -g
else 
	CC = gcc
endif

all: main.o
	$(CC) -o program main.o

main.o: main.c
	$(CC) -c main.c

val:
	valgrind --leak-check=yes --track-origins=yes ./program

run: 
	./program $(DIR)

clean:
	rm *.o
	rm program