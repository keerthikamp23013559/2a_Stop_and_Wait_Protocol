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
![Screenshot 2024-10-26 215435](https://github.com/user-attachments/assets/ac724a3e-a48f-4982-aa29-b64520c4ee48)
![Screenshot 2024-10-26 215428](https://github.com/user-attachments/assets/2ded20f9-a02b-4a8f-abc4-5c08a7504b77)



## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
