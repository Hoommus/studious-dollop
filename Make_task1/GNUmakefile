
NAME=binary

SRC=main.c src.c calc.c
OBJ=$(SRC:.c=.o)

$(NAME): $(OBJ)
	gcc -o $(NAME) $(OBJ)

%.o: %.c
	gcc -o $@ -c $< 

clean:
	rm -f $(OBJ) $(NAME)
