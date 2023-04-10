# Lab Report 1

## Step 1: Download VScode

[Vscode](https://code.visualstudio.com/download)

<img width="835" alt="Screen Shot 2023-04-05 at 4 48 53 PM" src="https://user-images.githubusercontent.com/110417599/230238137-d9137d34-b96b-4ee7-a47d-bd2c20ef3697.png">

After opening it should look like this:
(![image](https://user-images.githubusercontent.com/110417599/231013705-bd82b39f-3d27-452c-a9e2-6f8e106b9a01.png))

## Step 2: Remotely Connecting

To connect to the server we would want to use 'ssh' by oepning a 'terminal' in VScode (command + `) (MAC)

After the terminal is open, enter this command 'ssh cs15lsp23zz@ieng6.ucsd.edu' but replace 'zz' with your account letters.

If the terminal asks 'are you sure you want to continue connecting (yes/no/[fingerprint])?' 

Say yes

Next, They will want you to input your password and after your screeen should look like this:

(![image](https://user-images.githubusercontent.com/110417599/231014453-111893f3-dd0a-47db-a824-89d206153696.png)

## Step 3: Running commands 

You are now ready to run some commands. 
Here are some to try:
* cd ~
* cd
* ls -lat
* ls -a
* ls <directory> 
* cp /home/linux/ieng6/cs15lsp23/public/hello.txt ~/
* cat /home/linux/ieng6/cs15lsp23/public/hello.txt
