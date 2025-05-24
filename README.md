
# 3a.ECHO CLIENT AND SERVER USING TCP SOCKETS
NAME Hemanath S
REG NO 212224230094
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
### client.py
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
### server.py
```python
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
## OUPUT
### client.py
![Screenshot 2025-05-24 132244](https://github.com/user-attachments/assets/7c04dbc0-c89b-4e67-bc17-7999f890eb00)


### server.py
![Screenshot 2025-05-24 132252](https://github.com/user-attachments/assets/04b6da66-f23d-4c6d-9563-6f7d3b513ad4)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
