# 2a_Stop_and_Wait_Protocol
# NAME:KEERTHIKA M P
# REG NO:212223240071
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
```
Client Side:

import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
  i=input("Enter a data: ")
  c.send(i.encode())
  ack=c.recv(1024).decode()
  if ack:
    print(ack)
    continue
  else:
    c.close()
    break
```

```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   print(s.recv(1024).decode())
   s.send("Acknowledgement Recived".encode())

```

## OUTPUT

![Screenshot 2024-10-19 091804](https://github.com/user-attachments/assets/36837d30-9bae-41b1-a7ca-eab3dc9eff10)

![Screenshot 2024-10-19 091827](https://github.com/user-attachments/assets/3232f8c7-3421-4378-acde-d9d1feb3aefd)



## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
