# monty - Stacks, Queues - LIFO, FIFO 🥞  
#### monty functions as a Monty byte code interpreter. Monty 0.98 is a scripting language that is first compiled into Monty byte codes (Just like Python). It relies on a unique stack, with specific instructions to manipulate it.  
  
  
## SYNOPSIS  
monty is a simple byte code interpreter in accordance with Holberton School standards and expectations. This project's purpose was to introduce students to working with the `stack` which is [**LIFO** (last in first out)]([https://en.wikipedia.org/wiki/Stack_(abstract_data_type)](https://en.wikipedia.org/wiki/Stack_(abstract_data_type))) and the `queue`, which is [**FIFO** (first in first out)]([https://en.wikipedia.org/wiki/FIFO_(computing_and_electronics)](https://en.wikipedia.org/wiki/FIFO_(computing_and_electronics))).  
  
  
  
  
  
  
## INSTALLATION AND USAGE  
Please use GCC 4.8.4 compiler or later.  
  
```  
$ git clone [repository link]  
$ gcc -Wall -Werror -Wextra -pedantic *.c -o monty  
$ ./monty file_name.m  
```  
  
  
  
## SYNTAX OVERVIEW AND EXAMPLES  
  
  
Below are some examples of using monty with bytecode files:  
  
```  
vagrant@vagrant-ubuntu-trusty-64:~/0x19-stacks_queues_lifo_fifo$ cat -e bytecodes/00.m  
push 1$  
push 2$  
push 3$  
pall$  
vagrant@vagrant-ubuntu-trusty-64:~/0x19-stacks_queues_lifo_fifo$ ./monty bytecodes/00.m  
3  
2  
1  
vagrant@vagrant-ubuntu-trusty-64:~/0x19-stacks_queues_lifo_fifo$  
```  
```  
vagrant@vagrant-ubuntu-trusty-64:~/0x19-stacks_queues_lifo_fifo$ cat bytecodes/09.m  
push 1  
push 2  
push 3  
pall  
swap  
pall  
vagrant@vagrant-ubuntu-trusty-64:~/0x19-stacks_queues_lifo_fifo$ ./monty bytecodes/09.m  
3  
2  
1  
2  
3  
1  
vagrant@vagrant-ubuntu-trusty-64:~/0x19-stacks_queues_lifo_fifo$  
```  
## opcodes 

Listed below are the opcodes to can be used in monty:  
  
opcode | Function  
--------|---------------  
push | Pushes an element to the stack  
pall | Prints all the values on the stack, starting from the top of the stack  
pint| prints the value at the top of the stack, followed by a new line  
pop| Removes the top element of the stack  
swap | Swaps the top two elements of the stack  
 add | Adds the top two elements of the stack  
 nop| Doesn’t do anything 
  
  
  
  

## File Descriptions  
  
Listed below are the descriptions of the files in this repo:  
  
File | Description  
--------|---------------  
helperfuncs.c | Includes functions for string manipulation.  
main.c| Contains parser and main monty interpreter.  
free_list.c | Contains function to print doubly linked list    
monty.c | Contains functions for opcodes 
monty1.c | Contains functions for opcodes 
monty.h | Contains function prototypes and data structures.  
  
  
  
  
  
  
## Authors  
  
*Faizan Khan* :zap:  
  
  
*Christian Williams* :musical_note:  
  
## Data Structures and Functions  Used
  
```  
typedef struct stack_s

{
int n;
struct stack_s *prev;
struct stack_s *next;
} stack_t;

typedef struct instruction_s

{
char *opcode;
void (*f)(stack_t **stack, unsigned int line_number);
} instruction_t;

void add(stack_t **stack, unsigned int line_num);
void swap(stack_t **stack, unsigned int line_num);
void pop(stack_t **stack, unsigned int line_num);
stack_t *push(stack_t **stack, unsigned int line_num, int n);
void pall(stack_t **stack, unsigned int line_num);
stack_t *push(stack_t **stack, unsigned int line_num, int n);
void swap(stack_t **stack, unsigned int line_num);
void free_dlistint(dlistint_t *head);
int _strcmp(char *s1, char *s2);


```
