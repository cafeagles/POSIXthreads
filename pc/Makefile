CC = gcc
CCOPTS = -Wall -pedantic -c
LINKOPTS = -lpthread

all: pc

pc: pc.o 
	$(CC) $(LINKOPTS) -o $@ $^

pc.o: pc.c
	$(CC) $(CCOPTS) -o $@ $<

clean:
	rm -rf *.o pc *~

