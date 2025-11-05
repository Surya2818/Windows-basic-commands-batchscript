# Ex08-Windows-basic-commands-batchscript

## Name : SURYA D
## REG NO: 212224220115

## AIM:
To execute Windows basic commands and batch scripting



## DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




## WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"
## COMMAND AND OUTPUT
```
mkdir my-folder
```
<img width="1063" height="235" alt="01" src="https://github.com/user-attachments/assets/1031cc3f-93c6-4759-954f-15c04c9c3c30" />


Remove the directory "my-folder"
## COMMAND AND OUTPUT
```
rmdir my-folder
```
<img width="898" height="308" alt="02" src="https://github.com/user-attachments/assets/9ad92637-79bf-47d9-ba4f-576a52de6b9f" />


Create the file Rose.txt
## COMMAND AND OUTPUT
```
COPY CON Rose.txt
dir Rose.txt
```
<img width="708" height="396" alt="03" src="https://github.com/user-attachments/assets/db6b8c48-c210-4c71-bfa1-1aaf429b58e2" />


Create the file hello.txt using echo and redirection
## COMMAND AND OUTPUT
```
echo “hello world” > hello.txt
type hello.txt
```
<img width="837" height="101" alt="04" src="https://github.com/user-attachments/assets/049c49c4-01be-4948-93d0-ef4fe9544bb2" />


Copy the file hello.txt into the file hello1.txt
## COMMAND AND OUTPUT
```
copy hello.txt hello1.txt
```
<img width="801" height="125" alt="05" src="https://github.com/user-attachments/assets/b951d5bd-ac4a-4651-b178-bf163fc709fb" />



Remove the file hello1.txt
## COMMAND AND OUTPUT
```
del hello1.txt
```
<img width="801" height="125" alt="05" src="https://github.com/user-attachments/assets/616f3e1f-19a5-47cf-84a1-7df2e67ece49" />



List out the file hello1.txt in the current directory
## COMMAND AND OUTPUT
```
dir hello1.txt
```

<img width="688" height="177" alt="06" src="https://github.com/user-attachments/assets/2f56b5cc-ceb9-46d7-8a78-a63aa7bfe1a7" />


List out all the associated file extensions 
## COMMAND AND OUTPUT
```
assoc | more
```
<img width="638" height="492" alt="07" src="https://github.com/user-attachments/assets/f986e531-250c-4605-8d05-e5aff4375256" />



Compare the file hello.txt and rose.txt
## COMMAND AND OUTPUT
```
fc hello.txt Rose.txt
```
<img width="713" height="280" alt="08" src="https://github.com/user-attachments/assets/cc55ecba-ceed-42b0-9460-c5ebcc8049c9" />


## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".





## OUTPUT

<img width="672" height="162" alt="09" src="https://github.com/user-attachments/assets/bf6f17e0-e07e-4942-bad8-0648fdd54ae2" />


Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.



## OUTPUT

<img width="583" height="165" alt="10" src="https://github.com/user-attachments/assets/d1cd5844-0d94-4761-9a90-727ae05d1b34" />



Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.




## OUTPUT

<img width="627" height="208" alt="11" src="https://github.com/user-attachments/assets/05ef6178-55e1-4a50-bc19-536271ee4ef9" />



Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):

## OUTPUT
<img width="827" height="247" alt="12" src="https://github.com/user-attachments/assets/f43d5a99-dbc9-4949-a6a4-e119a9eadbc3" />


Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.


## OUTPUT
<img width="662" height="412" alt="13" src="https://github.com/user-attachments/assets/0d76467f-4e98-4c6b-be41-ea7bc647767e" />



# RESULT:
The commands/batch files are executed successfully.
