0x10. C - printf
Description This team project is part of the first year curriculum of Holberton School. _printf replicates the C standard library printf() function.

Authors
Musa Muhammad - @techbone and Ada Uchechi - @ucheadaeze

What you should learn from this project:

How to use git in a team setting Applying variadic functions to a big project The complexities of printf Managing a lot of files and finding a good workflow Prototype int _printf(const char *format, ...);

Usage Prints a string to the standard output, according to a given format All files were created and compiled on Ubuntu 14.04.4 LTS using GCC 4.8.4 with the command gcc -Wall -Werror -Wextra -pedantic *.c All files were linted for syntax and style with Betty Returns the number of characters in the output string on success, -1 otherwise Call it this way: _printf("format string", arguments...) where format string can contain conversion specifiers and flags, along with regular characters Examples _printf("Hello, Holberton\n") prints "Hello, Holberton", followed by a new line _printf("%s", "Hello") prints "Hello" _printf("This is a number: %d", 98) prints "This is a number: 98" Tasks These are all the tasks of this project, the ones that are completed link to the corresponding files.

I'm not going anywhere. You can print that wherever you want to. I'm here and I'm a Spur for life Write a function that produces output according to format. Prototype: int _printf(const char *format, ...); Returns: the number of characters printed (excluding the null byte used to end output to strings) write output to stdout, the standard output stream format is a character string. The format string is composed of zero or more directives. See man 3 printf for more detail. You need to handle the following conversion specifiers: c : converts input into a character s : converts input into a string
Education is when you read the fine print. Experience is what you get if you don't Handle the following conversion specifiers: d : converts input into a base 10 integer i : converts input into an integer
Just because it's in print doesn't mean it's the gospel Create a man page for your function
With a face like mine, I do better in print Handle the following conversion specifiers: b : the unsigned int argument is converted to binary alex@ubuntu:~/c/printf$ cat main.c #include "holberton.h"
/**

main - Entry point
Return: Always 0 */ int main(void) { _printf("%b\n", 98); return (0); } alex@ubuntu:/c/printf$ gcc -Wall -Wextra -Werror -pedantic main.c alex@ubuntu:/c/printf$ ./a.out 1100010
What one has not experienced, one will never understand in print Handle the following conversion specifiers: u : converts the input into an unsigned integer o : converts the input into an octal number x : converts the input into a hexadecimal number X : converts the input into a hexadecimal number with capital letters
Nothing in fine print is ever good news Use a local buffer of 1024 chars in order to call write as little as possible.
My weakness is wearing too much leopard print Handle the following custom conversion specifier: S : prints the string Non printable characters (0 < ASCII value < 32 or >= 127) are printed this way: \x, followed by the ASCII code value in hexadecimal (upper case - always 2 characters) alex@ubuntu:~/c/printf$ cat main.c #include "holberton.h"
/**

main - Entry point
Return: Always 0 */ int main(void) { _printf("%S\n", "Holberton\nSchool"); return (0); } alex@ubuntu:/c/printf$ gcc -Wall -Wextra -Werror -pedantic main.c alex@ubuntu:/c/printf$ ./a.out Holberton\x0ASchool
How is the world ruled and led to war? Diplomats lie to journalists and believe these lies when they see them in print Handle the following conversion specifier: p : int input is converted to a pointer address
The big print gives and the small print takes away Handle the following flag characters for non-custom conversion specifiers:
: adds a + in front of signed positive numbers and a - in front of signed negative numbers space : same as +, but adds a space (is overwritten by +)
: adds a 0 in front of octal conversions that don't begin with one, and a 0x or 0X for x or X conversions
Sarcasm is lost in print Handle the following length modifiers for non-custom conversion specifiers: l : converts d, i, u, o, x, X conversions in short signed or unsigned ints h : converts d, i, u, o, x, X conversions in long signed or unsigned ints
Print some money and give it to us for the rain forests Handle the field width for non-custom conversion specifiers.
The negative is the equivalent of the composer's score, and the print the performance Handle the precision for non-custom conversion specifiers.
It's depressing when you're still around and your albums are out of print Handle the 0 flag character for non-custom conversion specifiers.
Every time that I wanted to give up, if I saw an interesting textile, print what ever, suddenly I would see a collection Handle the - flag character for non-custom conversion specifiers.
Print is the sharpest and the strongest weapon of our party Handle the following custom conversion specifier: r : prints the reversed string
The flood of print has turned reading into a process of gulping rather than savoring Handle the following custom conversion specifier: R : prints the rot13'ed string
All the above options work well together. Authors
