![](https://www.alxafrica.com/)
## Description
This team project is part of the first year curriculum of ALX School.
_printf replicates the C standard library printf() function.

What you should learn from this project:

* How to use git in a team setting
* Applying variadic functions to a big project
* The complexities of printf
* Managing a lot of files and finding a good workflow

---

## printf()
The printf project is a collaboration between Jonathan Abayie Boahene - [Abayie](https://github.com/Abayie) and Degbor Johnson - [jo-dev123](https://github.com/jo-dev123), actual students of Software Engineering at ALX School, where a function named "_printf" imitates the actual "printf" command located in the stdio.h library. It contains some of the basic features and functions found in the manual 3 of "printf".
	
_printf() is a function that performs formatted output conversion and print data. Its prototype is the following:

	int _printf(const char *format, ...)

Where **format** contains the string that is printed. As _printf() is variadic function, it can receives n arguments that replace by n tags written inside the string.

The format tags prototype is the following:

	%[flags][length]specifier
	
If the program runs successfully, the **return value** is the amount of chars printed.
	
| Specifier | Output |
| ------------- | ------------- |
| c  | Character  |
| d or i | Signed decimal integer |
| s  | String of characters  |
| b  | Signed binary  |
| o  | Signed octal  |
| u  | Unsigned integer  |
| x  | Unsigned hexadecimal  |
| X  | Unsigned hexadecimal (uppercase)  |
| p  | Pointer address  |
| r  | Reverse string of characters |
| R  | ROT13 translation of string |
| S  | String with special chars replaced by their ASCII value  |
| %  | Character  |

| Flags | Description | Specifiers |
| ------------- | ------------- | ------------- | 
| +  | Prints a plus sign (+) when the argument is a positive number. In other case, prints a minus sign (-). | i, d |
| (space) | Prints a blank space if the argument is a positive number | i, d |
| #  | Prints 0, 0x and 0X for o, x and X specifiers, respectively. It doesn't print anything if the argument is zero | o, x, X |

| Length | Description | Specifiers |
| ------------- | ------------- | ------------- | 
| l | Prints a long int or unsigned long int | i, d, o, u, x and X |
| h | Prints a short int or unsigned short int | i, d, o, u, x and X |

------------

## Usage
* Prints a string to the standard output, according to a given format
* All files were created and compiled on Ubuntu 20.04.4 LTS using GCC 9.3.0 with the command ```gcc -Wall -Werror -Wextra -pedantic *.c```
* Returns the number of characters in the output string on success, -1 otherwise
* Call it this way: ```_printf("format string", arguments...)``` where ```format string``` can contain conversion specifiers and flags,
along with regular characters


## Examples

1. Printing the string of chars "Hello, Holberton":
	+ Use: `_printf("Hello Hol%s.", "berton");`
	+ Output: `Hello Holberton.`
	
2. Printing an integer number:
	+ Use: `_printf("10 + 10 is equal to %d.", 20);`
	+ Output: `10 + 10 is equal to 20.`
	
3. Printing a binary, octal and hexadecimal:
	+ Use: `_printf("10 in binary is [%b], in octal is [%o] and in hexadecimal is [%x]", 5, 5, 5);`
	+ Output: `10 in binary is [1010], in octal is [12] and in hexadecimal is [A]`
	
4. Printing a string codified in ROT13:
	+ Use: `_printf("Hello in ROT13 is %R", "Hello");`
	+ Output: `Hello in ROT13 is Urybb`

Using flags and length tags:

5. Printing the string of chars "Hello, Holberton":
	+ Use: `_printf("2 * 2 = %+d and 5 * -5 = %+i", 4, -25);`
	+ Output: `2 * 2 = +4 and 5 * -5 = -25`
	
6. Printing a long integer number and short integer number:
	+ Use: `_printf("1 million as a long int is %ld, but as a short int is %hd", 1000000, 1000000);`
	+ Output: `1 million as a long int is 1000000, but as a short int is 16960`


------------

## File Functions

### _printf.c
Own Printf Function That Performs Formatted Output Conversion And Print Data.

------------

### main.h
Header File Where All Prototypes Are Saved.

------------

### [0. I'm not going anywhere. You can print that wherever you want to. I'm here and I'm a Spur for life](./_printf.c)
* Write a function that produces output according to format.
  - c : converts input into a character
  - s : converts input into a string
------------

### [1. Education is when you read the fine print. Experience is what you get if you don't](./print_nums.c)
* Handle the following conversion specifiers:
  - d : converts input into a base 10 integer
  - i : converts input into an integer

------------

### [2. Just because it's in print doesn't mean it's the gospel](./man_3_printf)
* Create a man page for your function

------------

### [3. With a face like mine, I do better in print](./print_bases.c)
* Handle the following conversion specifiers:
  - b : the unsigned int argument is converted to binary

------------

### [4. What one has not experienced, one will never understand in print](./print_bases.c)
* Handle the following conversion specifiers:
  - u : converts the input into an unsigned integer
  - o : converts the input into an octal number
  - x : converts the input into a hexadecimal number
  - X : converts the input into a hexadecimal number with capital letters

------------


### [5. Nothing in fine print is ever good news](./write_funcs.c)
* Use a local buffer of 1024 chars in order to call write as little as possible.


------------

### [6. My weakness is wearing too much leopard print](./print_custom.c)
* Handle the following custom conversion specifier:
  - S : prints the string
  - Non printable characters (0 < ASCII value < 32 or >= 127) are printed this way: \x, followed by the ASCII code value in hexadecimal (upper case - always 2 characters)

------------

### [7. How is the world ruled and led to war? Diplomats lie to journalists and believe these lies when they see them in print](./print_address.c)
* Handle the following conversion specifier:
  - p : int input is converted to a pointer address


------------

### [8. The big print gives and the small print takes away](./get_flag.c)
* Handle the following flag characters for non-custom conversion specifiers:
  - \+ : adds a \+ in front of signed positive numbers and a \- in front of signed negative numbers
  - space : same as \+, but adds a space (is overwritten by \+)
  - \# : adds a 0 in front of octal conversions that don't begin with one, and a 0x or 0X for x or X conversions

------------

### [9. Sarcasm is lost in print]
* Handle the following length modifiers for non-custom conversion specifiers:
  - l : converts d, i, u, o, x, X conversions in short signed or unsigned ints
  - h : converts d, i, u, o, x, X conversions in long signed or unsigned ints

------------

### [10. Print some money and give it to us for the rain forests]
* Handle the field width for non-custom conversion specifiers.

------------

### [11. The negative is the equivalent of the composer's score, and the print the performance]
* Handle the precision for non-custom conversion specifiers.

------------

### [12. It's depressing when you're still around and your albums are out of print]
* Handle the 0 flag character for non-custom conversion specifiers.
------------

### [13. Every time that I wanted to give up, if I saw an interesting textile, print what ever, suddenly I would see a collection]
* Handle the - flag character for non-custom conversion specifiers.
------------

### [14. Print is the sharpest and the strongest weapon of our party](./print_custom.c)
* Handle the following custom conversion specifier:
  - r : prints the reversed string

------------

### [15. The flood of print has turned reading into a process of gulping rather than savoring](./print_custom.c)
* Handle the following custom conversion specifier:
  - R : prints the rot13'ed string


------------
### [16. * ]

* All the above options work well together.


------------

### Authors
**Jonathan Abayie Boahene** [Abayie](https://github.com/Abayie)
**Degbor Johnson.** [jo-dev123](https://github.com/jo-dev123)

------------

### End
