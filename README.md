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
### client
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())

```
### server
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
## OUTPUT
### client
![Screenshot 2024-04-29 133648](https://github.com/karthik-2106/3b_CHAT_USING_TCP_SOCKETS/assets/150319557/60345f1a-5695-44fa-ac8b-b3645500ca9a)

### server
![Screenshot 2024-04-29 133959](https://github.com/karthik-2106/3b_CHAT_USING_TCP_SOCKETS/assets/150319557/3d2e7bdb-c11e-4d5c-86b0-23e99a960c04)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
