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
### Client.py:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
### Server.py:
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
### Client.py:
<img width="840" alt="3b-client py" src="https://github.com/Ganesh23013987/3b_CHAT_USING_TCP_SOCKETS/assets/147473768/c9d595a7-57e1-4792-9a58-11262cb0bd83">

### Server.py:
<img width="840" alt="3b-server py" src="https://github.com/Ganesh23013987/3b_CHAT_USING_TCP_SOCKETS/assets/147473768/59cab92d-a1b6-441b-80a5-4168bd547aed">

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
