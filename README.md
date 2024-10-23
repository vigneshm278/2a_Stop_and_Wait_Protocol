# Ex. No:2a Stop and Wait Protocol
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
```py
import time
# Function to simulate sending frame and receiving ACK
def send_frame(frame):
    print("Sending frame:", frame)
    time.sleep(1) # Simulating transmission delay
    ack_received = False
    while not ack_received:
        ack = input("Enter ACK (1 for success, 0 for failure): ")
        if ack == '1':
            print("ACK received for frame:", frame)
            ack_received = True
        else:
            print("NACK received for frame:", frame)
            print("Resending frame:", frame)
            time.sleep(1) # Simulating retransmission delay
def main():
    frame_size = int(input("Enter frame size: "))
    frames = [i for i in range(frame_size)]
    for frame in frames:
        send_frame(frame)
    print("All frames sent successfully.")
if _name_ == "_main_":
    main()
```
## OUTPUT
![image](https://github.com/Prajeeth17/2a_Stop_and_Wait_Protocol/assets/120513885/b0c1861d-a895-4e09-b773-89d1acf7c42d)

## RESULT
Thus python program to perform stop and wait protocol was successfully executed.
