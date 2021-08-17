# library to enter and validate data in C Language

//----------english

Hi there! This is a C library of functions for keyboard inputs and validations in C Language.
This project was started on a Windows10 OS with Code Blocks and ended on Linux(Ubuntu) with Eclipse.


For using it
First of all you need a C development environment. To set up a C-Environment visit https://www.tutorialspoint.com/cprogramming/c_environment_setup.htm
In your code editor (I'been using Eclipse and CodeBlocks) you must to create a New C Console Project
and add the first line: #include "utn.h"


Note: function's names and documentation are incomplete and in spanish (or spanglish in some cases like 'getNumero'). Sorry. But don't worry, I'll try to explain the basic usage of this library in the following lines. And you will learn one or two words in spanish, so have fun :)


IMPLEMENTATIONS

Usable functions names are like "utn_getSOMETHING"
Eg: Let's supose you have to ask for a Integer Positive Number (an age for example).
You will need to use the utn_getNumero() function.

Here's function's prototype: 
int utn_getNumero(int* pResultado, char* mensaje, char* mensajeError,int minimo,int maximo,int reintentos)

Wich in english would be like:
int utn_getNumber(int* pointerToResult, char* messageToAskForANumber, char* errorMessage,int minimunAccepted,int maximumAccepted
,int retries)

A possible implementation:
utn_getNumero(*pResult, "enter your age: ", "Error: out of range, or null pointer given\n", 0, 110, 3);
If something went wrong you will see errorMessage as a console output.


Other possible implementations

//ask for an Integer Possitive Number (negative and float not allowed)
int utn_getNumero(int* pResultado, char* mensaje, char* mensajeError, int minimo, int maximo, int reintentos);

//ask for an Integer Number (possitive, negative and zero allowed. floats not allowed)
int utn_getNumeroConSigno(int* pResultado,char* mensaje, char* mensajeError,int minimo, int maximo, int reintentos);

//ask for a real number (positive, negative, zero and float allowed)
int utn_getNumeroReal(float* pResultado,char* mensaje, char* mensajeError,float minimo, float maximo, int reintentos);

//ask for text input
int utn_getTexto(char* pTexto,int tamBuffer, char* mensaje);
eg: utn_getTexto(*pointerToString , bufferSize, "Write some text and press Return: ");

//ask for a char.
int utn_getLetra(char* pResultado, char* mensaje, char* mensajeError, char minimo, char maximo, int reintentos);
//Note: In Spanish 'letra' means 'character', not 'letter'(for letter we say 'carta', eg: 'love letter' is 'carta de amor' <3

//ask for a phone number
int utn_getTelefono(char* pResultado,char* mensaje, char* mensajeError, int reintentos);
eg:
int retries = 3 ;
utn_getTelefono(*pointerToPhoneNumber, "Phone Number: ", "error message", retries )



//----------spanish

Hola :) 
Esta es una blioteca con funciones de ingreso por teclado y validación de datos en Lenguaje C.
Se desarrollaron funciones para, entre otras cosas, evitar que se desborde el buffer de entrada, validar strings, convertir strings a numeros.

Fueron hechas como parte de un curso básico de programación en C.
Se comenzaron a desarrollar en CodeBlocks en Windows10.
Se terminaron de desarrollar en Eclipse en Ubuntu.

Saludos. Gracias por leer :)
