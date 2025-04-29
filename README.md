# 2a_Stop_and_Wait_Protocol
# NAME.- BARATHRAJ K
# REG NO.- 212224230033

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

## PROGRAM

Server
```
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
Client:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    print(s.recv(1024).decode()) 
    s.send("Acknowledgement Recived".encode()) 
```


## OUTPUT:

client
![Screenshot 2025-04-18 212509](https://github.com/user-attachments/assets/1518358e-5f3b-436e-97ed-69d05937b630)

server
![Screenshot 2025-04-18 212621](https://github.com/user-attachments/assets/e215517c-8b52-4bfc-98ab-0af9f6adffb1)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
