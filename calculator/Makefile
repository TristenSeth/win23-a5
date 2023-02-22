CC := gcc
CFLAGS := -Wall -I$(PWD)
LDFLAGS := # empty

SRC := $(wildcard *.c)
OBJ := $(SRC:.c=.o)
TARGET := calculator

$(TARGET) : $(OBJ)
	$(CC) $(CFLAGS) $(LDFLAGS) $(OBJ) -o $(TARGET)

.PHONY: debug
debug : $(OBJ)
	$(CC) $(CFLAGS) -ggdb -O0 $(LDFLAGS) $(OBJ) -o $(TARGET)

.PHONY: release
release : $(OBJ)
	$(CC) $(CFLAGS) -O3 $(LDFLAGS) $(OBJ) -o $(TARGET)


.PHONY: clean
clean : 
	rm -rf $(OBJ) $(TARGET)

