# Shell_C
This is the First project of COM S 352-Operating System course

## Overview
This project consists of designing a C program to serve as a shell interface that accepts user commands and then executes each command in a separate process. The implementation will support input and output redirection, as well as pipes and backgroudprocess. Completing this project will involve using the Linux fork(), exec(), wait(), dup2(), and pipe() system calls.

A shell interface gives the user a prompt, after which the next command is entered. The example below illustrates the prompt osh> and the user’s next command: cat prog.c. (This command displays the file prog.c on the terminal using the UNIX cat command.)

## Running the shell 

run `make` to generate the executable

run `./shell` to run the shell

run `exit` to exit the shell

## FEATURES

#### Foreground processes
- The shell waits for the current process to execute

#### Background processes
- Use '&' at the end of any command to invoke a background process
- The process will then run in the background. 
- The status of the background process will be checked and when exited, a message will be displayed. 
  
#### File redirection
- Use '<' in the command to redirects input from a file to a command
- Use '>' in the command to redirects output form the command to a file.
- Assume commands contain either one input or one output and not both.

#### Pipes
- Use '|' in the command to connects the stdout of one process to the stdin of another.
- Assume commands contain no more than one pipe.

#### Job control commands
- **jobs** - prints a list of all background processes

- **CTRL+C** - sends a SIGINT signal to the foreground jobs of the shell and stop the currently running foreground command.

- **bg job_id** - resumes a stopped command.

#### exit command
- `exit` - exit the shell. The shell exits only when quit is typed
