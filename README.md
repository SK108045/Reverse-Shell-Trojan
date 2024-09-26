# Reverse-Shell-Trojan
##  Obfuscated Reverse Shell Trojan using Invoke-PSObfuscation Too

![AI Tweet Bot Logo](https://sk10codebase.online/images/Red.png)

This repository contains a reverse shell script written in Visual Basic SCRIPT , as well as its obfuscated counterpart. The purpose of this project is purely educational—to demonstrate how reverse shells work and to explore the use of obfuscation techniques to avoid detection by common security measures. Use this information responsibly.

## Files in this Repository
   1. Original Script (OriginalVBS.vbs)
   2. Obfuscated Script (ObfuscatedVBS.vbs)

### Original VBScript Reverse Shell
  - The original script is a basic reverse shell that uses PowerShell to connect to a remote server (in this case, 34.90.173.235 on port 8888). 
    Once connected, it allows the remote server to execute commands on the target machine and send the results back to the remote server. 
  - A TCP connection is made using System.Net.Sockets.TCPClient.The script reads data from the remote server, executes it using iex (Invoke- 
    Expression), captures the output, and sends it back to the remote server.The process repeats until the connection is closed.
    
### Obfuscated Reverse Shell
  In order to make the reverse shell harder to detect by anti-virus software, we obfuscate the script using the Invoke-PSObfuscation tool. This 
  tool targets PowerShell scripts and transforms them into a more complex and encoded format, reducing the chances of detection by most 
  signature-based security tools.

#### Obfuscation Process
If you want to obfuscate the VBScript yourself, follow these steps:

1. Install the Invoke-PSObfuscation tool from GitHub:  
   `git clone https://github.com/gh0x0st/Invoke-PSObfuscation.git`
2. Feed the original VBScript or PowerShell code into the tool.
3. Run the obfuscation commands to generate the obfuscated script.
4. The resulting script will be similar to the `ObfuscatedVBS.vbs` file included in this repository.

#### Connecting to the affected machine
While in the server use a tool like nc (Netcat) to listen on the port you specified in the script

```bash
nc -lvp 8888
```

### Credits
Special thanks to [gh0x0st](https://github.com/gh0x0st) for creating the [Invoke-PSObfuscation](https://github.com/gh0x0st/Invoke-PSObfuscation) tool, which was used in this project to obfuscate the VBScript and PowerShell code.
   




  
