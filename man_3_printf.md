% _Printf Printf 1.0
% Elizabeth Gonzales & Pablo Osorio
% November 2021

#NAME

_Printf - The functions in the printf() family produce output according to a format as described below.

#SYPNOSIS

int _printf(const char *format, ...)

#DESCRIPTION

This function write the output under the control of a format stringthat specifies how subsequent arguments (or arguments accessed via the variable-length argument facilities of stdarg(3)) are converted for output.

FORMAT OF THE FORMAT STRING

The format string is a character string, beginning and ending in itsinit
ial shift state, if any. The format string is compose of zero or more directives: ordinary characters (not %), which are copied unchanged to the output stream; and conversion specifications, each of which results in fetchingzero or more subsequent arguments. Each conversion specification is introduced by the character %, and ends with a converion specifier.

Warning: Without a % identifir, the program return a error.

#OPTIONS

The option %s is used to replace some part of the string with the argument of the same type string.
When we have double %% the function just print one %.

- %c: The option %c is used to replace some part of the string with the argumets of type char.

- %i, %d :The options %i, %d is used to replace some part of the string with the argument of type integer number.

- %s: The option %s is udes to replace some part of string with the argument of type string.


#EXAMPLES

- _printf("this is d\n");
	      In this case we don't use any identifier. output: 'this is d'
- _printf("This is the number: %d\n", -78341);
	      'output This is the number: -78341'
- _printf("%cello\n", 'H');
		  Output: 'Hello'
- _printf("Hello %s\n" , "Miss Smith");
	       Output: 'Hello Miss Smith'

#RETURN

It always return the number of characters printed (excluding the null byte used to end output to strings).

#BUGS

this one doesn't handle conversion specifiers

- b
- u
- o
- x
- X
- p