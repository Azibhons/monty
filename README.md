# Project_ 0x19. C - Stacks, Queues - LIFO, FIFO

The goal of this project is to create an interpreter for Monty ByteCodes files.

# The Monty language

Monty 0.98 is a scripting language that is first compiled into Monty byte codes (Just like Python). 
It relies on a unique stack, with specific instructions to manipulate it. 
Monty byte code files:Files containing Monty byte codes usually have the .m extension. 

# Compilation & Output

Code will be compiled this way:

* $ gcc -Wall -Werror -Wextra -pedantic -std=c89 *.c -o monty
* Any output must be printed on stdout
* Any error message must be printed on stderr


# Data structures for this project:

/**
 * struct stack_s - doubly linked list representation of a stack (or queue)
 * @n: integer
 * @prev: points to the previous element of the stack (or queue)
 * @next: points to the next element of the stack (or queue)
 *
 * Description: doubly linked list node structure
 * for stack, queues, LIFO, FIFO
 */
typedef struct stack_s
{
        int n;
        struct stack_s *prev;
        struct stack_s *next;
} stack_t;

/**
 * struct instruction_s - opcode and its function
 * @opcode: the opcode
 * @f: function to handle the opcode
 *
 * Description: opcode and its function
 * for stack, queues, LIFO, FIFO
 */
typedef struct instruction_s
{
        char *opcode;
        void (*f)(stack_t **stack, unsigned int line_number);
} instruction_t;

# AUTHORS

* Nathan Azibabhonomeni

* Ilyas Ettourach

