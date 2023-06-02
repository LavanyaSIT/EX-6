# EX-6 IMPLEMENTATION OF PING COMMAND
# DATE :13-04-2023
# AIM :

To write the python program for simulating ping command
# ALGORITHM :

    start the program.
    Include necessary package in java.
    To create a process object p to implement the ping command.
    declare one Buffered Reader stream class object.
    Get the details of the server
    length of the IP address.
    time required to get the details.
    send packets, receive packets and lost packets.
    minimum, maximum and average times.
    print the results.
    Stop the program.

# PROGRAM :
# Client:

# Developed by :Lavanya S
# Register Number : 212221220030
```
import socket
from pythonping import ping
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
hostname=c.recv(1024).decode()
try:
c.send(str(ping(hostname, verbose=False)).encode())
except KeyError:
c.send("Not Found".encode())
```

# Server:

# Developed by : Lavanya S
# Register Number : 212221220030
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
ip=input("Enter the website you want to ping ")
s.send(ip.encode())
print(s.recv(1024).decode())
```

# OUTPUT :
# Client:

![image](https://github.com/LavanyaSIT/EX-6/assets/130207418/71e9d469-3f5f-4311-b088-42bda3a4c750)

# Server:

![image](https://github.com/LavanyaSIT/EX-6/assets/130207418/1f5063b1-e803-46d0-bb52-bafa947e6bec)

# RESULT :

Thus, the python program for simulating ping command was successfully executed.


