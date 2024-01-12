# Lab Report 1

## cd

1. `cd` with no arguments: 
```
[user@sahara ~/lecture1]$ cd
```
Working Directory: `lecture 1`  
There is no output because the `cd` command does not ouput anything. When the `cd` command has no arguments, it default changes the directory back to the home directory.  
The output is not an error.  

2. `cd` with a path to a directory:
```
[user@sahara ~]$ cd /home/lecture1/messages
```
Working Directory: `lecture 1`  
There is no output because the `cd` command does not ouput anything. The working directory was changed to messages because the argument for the change directory command was the path for the messages directory.  
The output is not an error.  

3. `cd` with a path to a file:
```
[user@sahara ~/lecture1]$ cd /home/lecture1/messages/en-us.txt
bash: cd: /home/lecture1/messages/en-us.txt: Not a directory
```
Working Directory: `lecture 1`  
We got this output because `en-us.txt` is a file and not a directory and we asked to change the directory to a file given by `/home/lecture1/messages/en-us.txt`.  
The output is an error because the `cd` command requires an argument that is a directory, not a file.  

## ls

1. `ls` with no arguments:
```
[user@sahara ~/lecture1]$ ls
Hello.class  Hello.java  messages  README
```
Working Directory: `lecture1`  
The `ls` command with no arguments lists all the files in the current directory and since we are in the lecture1 directory, the output is a list of all the files in the lecture1 directory.  
The output is not an error.  

2. `ls` with a path to a directory:
```
[user@sahara ~/lecture1]$ ls /home/lecture1
Hello.class  Hello.java  messages  README
```
Working Directory: `lecture1`  
When you provide a directory as an argument to the `ls` command, the output is a list of the files in the directory that is inputted.  
The output is not an error.  

3. `ls` with a path to a file:
```
[user@sahara ~/lecture1]$ ls /home/lecture1/messages/en-us.txt
/home/lecture1/messages/en-us.txt
```
Working Directory: `lecture1`  
When you provide a file as an argument to the `ls` command, the output is the path of that file.  
The output is not an error.  

## cat

1. `cat` with no arguments:
```
[user@sahara ~/lecture1]$ cat

```
Working Directory: `lecture1`  
There is no output because there were no arguments provided to the cat command.  
The output is an error because there is nothing to concatenate resulting in an infinite loop that breaks the terminal.  

2. `cat` with a path to a directory:
```
[user@sahara ~/lecture1]$ cat /home/lecture1/messages
cat: /home/lecture1/messages: Is a directory
```
Working Directory: `lecture1`  
The output states that the given path is a directory because the expected inputs are files.  
The output is not an error.  

3. `cat` with a path to a file:
```
[user@sahara ~/lecture1]$ cat /home/lecture1/messages/en-us.txt
Hello World!
```
Working Directory: `lecture1`  
The output is the contents of the text file en-us.txt because the file concatenated with nothing is just the file.  
The output is not an error.  
