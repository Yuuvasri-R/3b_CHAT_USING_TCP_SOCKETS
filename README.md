# 3b) CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM

Developed by : **Yuuvasri R**

Reg no : **212225230313**

### Client 
```python
import socket
s = socket.socket()
s.connect(('localhost', 8080))
while True:
    msg = input("Client > ")
    s.send(msg.encode())
    server_reply = s.recv(1024).decode()
    if not server_reply:
        break
    print("Server >", server_reply)
s.close()
```

### Server
```python
import socket
s = socket.socket()
s.bind(('localhost', 8080))
s.listen(5)
print("Waiting for connection...")
c, addr = s.accept()
print("Connected to:", addr)
while True:
    client_message = c.recv(1024).decode()
    if not client_message:
        break
    print("Client >", client_message)
    msg = input("Server > ")
    c.send(msg.encode())
c.close()
s.close()
```
## OUPUT
<img width="946" height="942" alt="Screenshot 2026-05-19 161741" src="https://github.com/user-attachments/assets/ae3c9eb0-af98-4647-8b1e-43c7d65f9392" />
<img width="943" height="925" alt="Screenshot 2026-05-19 161719" src="https://github.com/user-attachments/assets/d1aa901c-7106-45d6-8358-f30e9c303869" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.



















































.















































.










































.
