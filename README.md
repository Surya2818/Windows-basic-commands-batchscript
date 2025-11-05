# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"

## COMMAND AND OUTPUT

```cmd
mkdir my-folder
```
<img width="703" height="160" alt="image" src="https://github.com/user-attachments/assets/6b6d191c-0f4a-4018-a5ab-b1cad19ee46c" />

Remove the directory "my-folder"

## COMMAND AND OUTPUT

```bat
rmdir my-folder
```
<img width="547" height="52" alt="image" src="https://github.com/user-attachments/assets/cb37d4ca-ec90-4606-b03b-754ad306980d" />

Create the file Rose.txt

## COMMAND AND OUTPUT

```bat
COPY CON Rose.txt
dir Rose.txt
```

<img width="751" height="417" alt="image" src="https://github.com/user-attachments/assets/bb107f02-e446-4201-bca1-61873a4f0b11" />

Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT

```bat
echo "hello world" > hello.txt
type hello.txt
```
<img width="707" height="106" alt="image" src="https://github.com/user-attachments/assets/4c264ef9-4301-4a7b-82f2-e7c6571fcce1" />

Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT

```bat
copy hello.txt hello1.txt
hello1.txt
type hello1.txt
```
<img width="732" height="183" alt="image" src="https://github.com/user-attachments/assets/b76850c2-63b7-4537-b27e-de74034c9a04" />

Remove the file hello1.txt

## COMMAND AND OUTPUT

```bat
del hello1.txt
```
<img width="706" height="235" alt="image" src="https://github.com/user-attachments/assets/96456b5e-a057-461e-9726-a8347b7e0948" />

List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT

```bat
dir hello1.txt
```

<img width="706" height="235" alt="image" src="https://github.com/user-attachments/assets/ccd2756a-e854-4911-81eb-930cdffaae29" />

List out all the associated file extensions 

## COMMAND AND OUTPUT

```bat
assoc | more
```

<img width="602" height="1120" alt="image" src="https://github.com/user-attachments/assets/4f316e6d-07d6-4964-8c7c-1621e047d039" />



Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT

```bat
fc hello.txt Rose.txt
```

<img width="641" height="236" alt="image" src="https://github.com/user-attachments/assets/5de8c274-d41e-4165-888f-2310120230f5" />

## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="Pravesh" and display as "Hello, Pravesh".


## SCRIPT AND OUTPUT

```bat
@echo off
set name=Pravesh
echo Hello, %name%!
pause
```
<img width="627" height="447" alt="image" src="https://github.com/user-attachments/assets/7bd73f28-1e2c-42d7-9d14-752ad0b740f8" />

<img width="491" height="116" alt="image" src="https://github.com/user-attachments/assets/cd265d25-38ad-4a29-99d6-5765d4b171fa" />


Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.



## SCRIPT AND OUTPUT

```bat
@echo off
:main
set /p number=Enter a number: 
rem Calculate remainder when divided by 2
set /a remainder=%number% %% 2
if %remainder%==1 (
    echo %number% is an odd number.
) else (
    echo %number% is not an odd number.
)
:choice
set /p continue=Do you want to check another number? (Y/N): 
if /i "%continue%"=="Y" goto main
if /i "%continue%"=="N" goto end
echo Invalid choice, please enter Y or N.
goto choice
:end
echo Thank you for using the odd number checker!
pause
```

<img width="627" height="447" alt="image" src="https://github.com/user-attachments/assets/7bd73f28-1e2c-42d7-9d14-752ad0b740f8" />


<img width="680" height="235" alt="image" src="https://github.com/user-attachments/assets/b3742ceb-ccef-4729-b79a-5c8cbc6fabde" />


Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.



## OUTPUT

```bat
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause
```

<img width="357" height="187" alt="image" src="https://github.com/user-attachments/assets/e9dfce57-9099-458e-b343-e1fb9f66e542" />

<img width="597" height="178" alt="image" src="https://github.com/user-attachments/assets/82e3f22b-677f-4ff5-993e-e80a21979e47" />



Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):

## OUTPUT

```bat
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
```
<img width="392" height="222" alt="image" src="https://github.com/user-attachments/assets/768d8eb5-3b93-4ed4-a67d-254834ef001f" />

<img width="478" height="97" alt="image" src="https://github.com/user-attachments/assets/07e2c6e7-a886-4ea9-84d7-204e6da6c119" />

Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.


## OUTPUT

```bat
@echo off
:menu
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option: 
if "%choice%"=="1" goto hello
if "%choice%"=="2" goto createfile
if "%choice%"=="3" goto end

:hello
echo Hello, World!
goto menu

:createfile
echo Creating a file...
echo This is a new file > newfile.txt
goto menu
:end
echo Goodbye!
pause
```

<img width="559" height="483" alt="Screenshot 2025-11-05 103419" src="https://github.com/user-attachments/assets/c20cde4c-9e8f-4afb-b72b-b95ff03ed5d9" />


# RESULT:
The commands/batch files are executed successfully.

