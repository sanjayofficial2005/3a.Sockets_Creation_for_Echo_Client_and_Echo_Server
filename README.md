# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS

## Developed By : SANJAY M
## Register No  : 212223230187
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM:
## client.py:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```

## server.py:
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
## client:
![Screenshot 2024-04-11 143346](https://github.com/sanjayofficial2005/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/148048602/c3232dc0-c6c0-4dad-b70f-f0194e1866cc)
## server:
![Screenshot 2024-04-11 143357](https://github.com/sanjayofficial2005/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/148048602/77e6e228-3c13-49ce-9285-94f5ccd12aa3)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
