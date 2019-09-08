CC	    := gcc
C_FLAGS	    := -Wall -Wextra -fPIC 

BIN	    := bin
SRC	    := src
INCLUDE	    := include
LIB	    := lib

LIBRARIES   := -luser_interface -luser_commands -lncurses

APP_NAME:= server

EXECUTABLE  := $(APP_NAME)

CFILES := $(SRC)/main.c

libs: 
	cd $(LIB) && make && make install

all: $(CFILES)
	$(CC) $(C_FLAGS) -I$(INCLUDE) $(CFILES) -L$(BIN)/$(LIB) $(LIBRARIES) -o $(APP_NAME)

install:
	mv $(EXECUTABLE) $(BIN)

clean:
	-$(RM) $(BIN)/$(EXECUTABLE)

run: all
	./$(BIN)/$(EXECUTABLE)
