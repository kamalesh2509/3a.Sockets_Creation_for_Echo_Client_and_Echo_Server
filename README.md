# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.

## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
   
## PROGRAM
```
Name : E Kamalesh
Reg no : 212222100019
```
## CLIENT
~~~
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
~~~
## SERVER
~~~
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
~~~

## OUPUT
## CLIENT
![echo client](https://github.com/23006111/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/145981696/c2a483c9-e14f-4682-8349-a66c3dcb51fb)
## SERVER
![echo server](https://github.com/23006111/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/145981696/ac44bd8a-ba1d-44d9-a23f-9c7cabb6947f)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.

