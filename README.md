#  Suppression File ... Ignore Mac Internal Library Leaks -- 42 School Mac


##  What is Supression File : 

A suppression file is a file that tells Valgrind to ignore certain errors or leaks that are not caused by your program but by some external library or system call. This can help you focus on the errors that are relevant to your code and avoid false positives.


## Why is it required ?
Valgrind reads the leaks from the readline library itself and finding leaks in your project (Ex: So long, Minishell)  difficult. 
See the first picture which creates huge line of leaks due to macos. At times it wastes time to find the actual one. 
Then after using the suppression with the command above you will see the output with your actual leaks in your function.


![image](https://github.com/mdabir1203/Valgrind_Suppression_MacOs/assets/66947064/66e43070-2811-4998-a863-6dc456bfd2f8)
![image](https://github.com/mdabir1203/Valgrind_Suppression_MacOs/assets/66947064/4baa4a40-ace0-4b86-985e-f999bb5fc46c)


Pasted image 20230517114825.png]]

## How to Run ?
- Clone the repo
- Copy the `ignore_readline.supp` file to your Project folder 
- run ```valgrind --leak-check=full --show-leak-kinds=all --track-origins=yes --suppressions=ignore_readline.supp -s ./program_name```
- Check the output


## Feedbacks 

If you face bugs or want to add something to this let us know :) 
