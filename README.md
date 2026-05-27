# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
```
Client
import socket
s=socket.socket()
s.connect(('localhost',8005))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())

Server
import socket
s=socket.socket()
s.bind(('localhost',8005))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
 ```
## OUTPUT
Client

<img width="666" height="139" alt="Screenshot 2026-05-27 054427" src="https://github.com/user-attachments/assets/d1f4fbfd-14da-4479-ae01-1a73a5c35435" />

Server

<img width="746" height="148" alt="Screenshot 2026-05-27 054439" src="https://github.com/user-attachments/assets/aff2f162-50b8-47bb-a689-12fac92dffce" />


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
