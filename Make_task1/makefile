NAME=binary

SRC=main.c src.c calc.c
OBJ=$(SRC:.c=.o)

$(NAME): src calc main
	gcc $(OBJ) -o $(NAME)

main:
	gcc -c main.c -o main.o

src:
	gcc -c src.c -o src.o

calc:
	gcc -c calc.c -o calc.o

clean:
	rm -f $(OBJ) $(NAME)
