# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## CLIENT
 ```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## SERVER
```
 
import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
            ClientMessage=c.recv(1024).decode() 
            print("Client > ",ClientMessage) 
            msg=input("Server > ") 
            c.send(msg.encode())
```
## OUPUT
## CLIENT
![Screenshot 2025-05-11 073826](https://github.com/user-attachments/assets/234583ec-b6ed-42c7-8d56-9c065da5d451)


## SERVER

![Screenshot 2025-05-11 073840](https://github.com/user-attachments/assets/aeeb5df0-2a3d-4af2-9bdb-327bbb3d5b75)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
