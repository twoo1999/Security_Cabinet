CORSS =
CC=$(CORSS)gcc

EXE=main

DEFINES=
LDFLAGS = -lpthread -lwiringPi
CFLAGS=-g -I./include $(DEFINES)

C_SRC=$(wildcard *.c)
CPP_SRC = $(wildcard *.cpp)
CC_SRC = $(wildcard *.cc)
SRC = $(C_SRC) $(CPP_SRC) $(CC_SRC)
OBJ = $(C_SRC:.c=.o) $(CC_SRC:.cc=.o) $(CPP_SRC:.cpp=.o)

defualt : $(EXE) clean

all : $(EXE)
	echo complete!!

$(EXE) : $(OBJ)
	$(CC) $(CFLAGS) -o $@ $^ $(LDFLAGS)
	strip $@
	
clean:
	rm *.o
