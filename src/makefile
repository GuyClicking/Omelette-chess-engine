CC = gcc

EXE = omelette
DEBUGEXE = omelette_debug

PEXTFLAGS = -DUSE_PEXT -mbmi2
CFLAGS = -std=gnu11 -Wall -O3 -fcommon -flto -g -pthread -lm -DNDEBUG
TFLAGS = -std=gnu11 -Wall -O3 -fcommon -flto -fopenmp -g -pthread -lm -DNDEBUG -DTUNE
PFLAGS = $(CFLAGS) $(PEXTFLAGS)
DFLAGS = -std=gnu11 -Wall -O0 -fcommon -flto -g -pthread -lm
PFLAGS = -std=gnu11 -Wall -O3 -fcommon -flto -g -pthread -lm -DNDEBUG -p -pg

OBJ = *.c fathom/tbprobe.c

.PHONY:	build debug profile tune clean 

build:
	$(CC) $(CFLAGS) -o $(EXE) $(OBJ) -lm

debug:
	$(CC) $(DFLAGS) -o $(EXE) $(OBJ) -lm

profile:
	$(CC) $(CFLAGS) -o $(EXE) $(OBJ) -lm

tune:
	$(CC) $(TFLAGS) -o $(EXE) $(OBJ) -lm

clean:
	-rm *.o

