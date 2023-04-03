CC = clang

CFLAGS = -Wall -Wpedantic -Werror -Wextra -g


all: wordle

hw5: wordle.c
	$(CC) $(CFLAGS) hw5.c -o hw5

clean:
	rm -f hw5

format:
	clang-format -i -style=file *.[ch]
