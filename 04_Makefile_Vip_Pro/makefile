PROJECT_NAME = lean_makefile

SRC_DIR = source
INC_DIR = include
OBJ_DIR = output
BIN_DIR = bin

SRC = $(wildcard $(SRC_DIR)/*.c)
OBJ = $(SRC:$(SRC_DIR)/%.c=$(OBJ_DIR)/%.o)
EXE = $(BIN_DIR)/$(PROJECT_NAME)

run: build
	./$(EXE)

build: $(EXE)

$(EXE): $(OBJ)
	gcc $^ -o $@

$(OBJ_DIR)/%.o: $(SRC_DIR)/%.c
	gcc -I $(INC_DIR) -Wall -c $< -o $@

.PHONY: clean
clean:
	@rm $(BIN_DIR)/* $(OBJ_DIR)/*
