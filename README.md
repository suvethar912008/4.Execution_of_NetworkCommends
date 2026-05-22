# 4.Execution_of_NetworkCommands
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>

## Program:

server:

```
import socket
import subprocess

s = socket.socket()

s.bind(("localhost", 5000))

s.listen(1)

print("Server waiting for connection...")

c, addr = s.accept()

print("Connected with:", addr)

host = c.recv(1024).decode()

result = subprocess.getoutput("ping " + host)

c.send(result.encode())


c.close()
s.close()
```
client:

```
import socket


c = socket.socket()


c.connect(("localhost", 5000))


host = input("Enter website/IP: ")

c.send(host.encode())

print(c.recv(4096).decode())

c.close()

```

Index:

```

import subprocess

target = input("Enter website or IP: ")

subprocess.run(["tracert", target])

```
## Output

Server:

<img width="425" height="180" alt="Screenshot 2026-05-22 143559" src="https://github.com/user-attachments/assets/31ffd43a-d21b-405b-bb03-d9523a9c107f" />

Client:

<img width="576" height="354" alt="Screenshot 2026-05-22 143614" src="https://github.com/user-attachments/assets/5749f51a-caf4-479c-8f10-a5a6cc81f916" />

index:

<img width="523" height="312" alt="Screenshot 2026-05-22 143624" src="https://github.com/user-attachments/assets/a4c5ff8d-58b8-4cf5-8b10-8ec8a32ede88" />


## Result
Thus Execution of Network commands Performed 
