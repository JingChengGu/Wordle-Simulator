CC = clang

CFLAGS = -Wall -Wpedantic -Werror -Wextra -g


all: wordle

hw5: wordle.c
	$(CC) $(CFLAGS) wordle.c -o wordle

clean:
	rm -f wordle

format:
	clang-format -i -style=file *.[ch]
