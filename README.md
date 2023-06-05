# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER
## DATE :26-04-2023

## AIM :
To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.
## ALGORITHM :
```
1.Import the necessary modules in python
2.Create a socket connection to using the socket module.
3.Send message to the client and receive the message from the client using the 
  Socket module in server.
4.Send and receive the message using the send function in socket.
```
## PROGRAM :
```
Developed By: Yashaswi Mitta
Reg No: 212221230062
```
### client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
### server:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
## OUTPUT:
![cn 8-1](https://github.com/yashaswimitta/EX-8/assets/94619247/dc5d9fe6-c822-4ec7-90da-41a2471f0829)





## RESULT:
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.

