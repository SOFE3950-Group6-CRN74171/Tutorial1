# SOFE 3950U: Operating Systems

## TUTORIAL #1: Introduction to Linux

- **TA:** Omar Hemied
- **CRN:** 74171

### Objectives
- Learn the fundamentals of Linux
- Gain a better understanding of the terminal
- Simple programming using the shell (bash)

### Important Notes
- Work in groups of three students
- All reports must be submitted as a PDF on Canva. If source code is included, submit everything as an archive (e.g. zip, tar.gz). Also, bring your output screenshot.
- Save the file as `<tutorial_name><GroupName>.pdf` (e.g. tutorial1_Group1.pdf)

### Conceptual Questions

1. Write a brief summary of Linux and why you believe it has become so popular in the years since its inception. Provide some examples where the Linux operating system has been used.
   
2. What does it mean for software to be considered "Free" or Open Source, why is this significant?
   
3. What are the benefits of Open Source software, and what are the drawbacks?
   
4. Name an open-source license.
   
5. Name the three standard streams, their numeric value, and their purpose.

### Application Questions

- If you do not have Linux configured on your system, you can use the following online terminal, you can write scripts by using the option “File → Create File” to open an editor that you can use to create the script.

  [Online Terminal](http://www.tutorialspoint.com/execute_bash_online.php)

1. Write the terminal commands to do the following:
   - Create a directory named tutorials
   - Create an empty file called tutorial1
   - Copy the file as a new file called tutorial_1
   - Delete the old file, tutorial1

2. Write the terminal commands to change to the home directory and create a symbolic link named tutorial_1 to the file ~/work/tutorials/tutorial_1

3. Write the terminal commands to search recursively for the word “stdin” in all of the files within the tutorials directory (~/work/tutorials/)

4. Write the terminal command to search for all files starting with “tutorial” (hint you will need to look up bash wildcards) and redirect all of the errors (error stream) to a file named “errors.log”.

5. Terminal commands can be written as scripts for later reuse, use the following example as a starting point to create your own script that does the following.
   - Accepts the first argument (this is $ARG1 in the template) and checks if it is equal to “loop” and if so prints (hint use echo) the word “loop”
   - Loops 5 times and each time it concatenates the current index (1 to 5) to the file count.log
   - Saves the list of processes (hint use ps) to a file named processes.log

  You will need to consult online sources, the following are very helpful.
   - [Bash Programming Introduction](http://tldp.org/HOWTO/Bash-Prog-Intro-HOWTO.html)
   - [Bash by Example](https://www.ibm.com/developerworks/library/l-bash/)
   - [Learn Bash in Minutes](http://learnxinyminutes.com/docs/bash/)

  ```bash
  #!/bin/bash
  ARG1="$1"

  for i in {1..5}
  do
    echo $ARG1
  done
```
-To run this example script, open a new file in an editor (e.g. gedit, sublime text, vim, etc.) and paste the example in and save the file as question_5.sh, then in your terminal navigate to the directory/location where you saved the file and execute the following commands to make the file executable (so you can run it) and to run the file with an argument, which it will then print out 5 times.
```bash
cd <directory where file is saved>
chmod +x question_5.sh
./question_5.sh hello     (this will print hello 5 times)
```
