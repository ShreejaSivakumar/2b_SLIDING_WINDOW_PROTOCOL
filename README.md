# 2b IMPLEMENTATION OF SLIDING WINDOW PROTOCOL

# EX.NO : 2B
# DATE : 22/05/26
# NAME : SHREEJA R S
# REF.NO : 25017561

## AIM

To implement a simple **Stop-and-Wait Protocol** using Python socket programming, where the client sends frames one by one and waits for an acknowledgment (ACK) from the server before sending the next frame.

## ALGORITHM:
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM

SERVER : -

```
import socket

s = socket.socket()
s.bind(('localhost', 8000))
s.listen(1)

print("Waiting for connection...")
conn, addr = s.accept()
print("Connected to", addr)

while True:
    data = conn.recv(1024).decode()
    if not data:
        break

    print("Frame received:", data)
    conn.send("ACK".encode())

conn.close()
```

CLIENT : -
```
import socket

s = socket.socket()
s.connect(('localhost', 8000))

n = int(input("Enter number of frames: "))

for i in range(n):
    msg = input("Enter frame: ")
    s.send(msg.encode())

    ack = s.recv(1024).decode()
    print("Received:", ack)
s.close()
```
## OUTPUT

<img width="741" height="930" alt="Screenshot 2026-05-22 082528" src="https://github.com/user-attachments/assets/e393fb7b-bfe6-4303-ad3a-c16a686e8f45" />

<img width="757" height="903" alt="Screenshot 2026-05-22 082547" src="https://github.com/user-attachments/assets/acb12512-336e-4dac-82e4-d1ab7052f743" />

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed




































































.
.
.
.
.
.
.




































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.



































































.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
..
.
..
.

.
..
.
.
.

