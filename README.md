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
```python
CLIENT:
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode()) 

```
```python
SERVER:
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
### Client:
<img width="1352" height="325" alt="image" src="https://github.com/user-attachments/assets/03e03cb9-161b-4e55-8cdd-ba23955fa7af" />
Server:
<img width="1373" height="322" alt="image" src="https://github.com/user-attachments/assets/c4a10478-5b94-4d73-b6a9-a32a84a2a932" />


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
