MAKES=foo.mk bar.mk foobar.mk
OBJ=main.o foo.o bar.o foobar.o

NAME=hello

all: $(NAME)

$(NAME): $(OBJ)
	gcc $(OBJ) -o $(NAME)

main.o: main.c
	gcc -o $@ -c $<

%.o: %.c
ifeq ($(METHOD), exec)
	$(MAKE) -f $(@:.o=.mk)
else
include $(MAKES)
endif

clean:
	rm $(OBJ) $(NAME)

.PHONY:clean
