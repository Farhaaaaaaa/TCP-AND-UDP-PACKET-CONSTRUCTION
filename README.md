# TCP-AND-UDP-PACKET-CONSTRUCTION
<P> <h3>To understand the construction of TCP and UDP packets we need to understand what a TCP and UDP packet looks like</h3></P>
<h2>TCP PACKET</h2>

![Screenshot 2024-07-30 105652](https://github.com/user-attachments/assets/a78a9c99-e801-4cc9-a8a7-a51f78377296)
<h2>Let us analyze this TCP packet completely</h2>
<h3><B>Source Port (16 bits):</B>
The port number of the source.
<br>
<b>Destination Port (16 bits):</b>
The port number of the receiving application.

![image](https://github.com/user-attachments/assets/c973b5ae-91d7-4763-a65d-e3c89d17ee98)
<br>
<B>Sequence Number (32 bits):</B>
 It indicates the position of the first byte of data in the data segment.<br>
 
 ![image](https://github.com/user-attachments/assets/e83cf94f-7338-4172-8e68-7d7be047f447)

<B>Acknowledgment Number (32 bits):</B>
It determines  the sequence number of the next byte of the segment that the sender is expecting to receive..<br>

![image](https://github.com/user-attachments/assets/745a22c4-48d8-4e67-be75-86263168c468)

<b>Data Offset (4 bits):</b>
This field indicates the length of the TCP header in 32-bit words. The minimum value is 5 (for 20 bytes), and the maximum value is 15 (for 60 bytes).<br><br>
<b>Reserved (3 bits):</b>
Reserved for future use and should be set to 0.<br><br>
Flags (9 bits):
Various control flags:
CWR (1 bit):  It is set by the sender to indicate that it received a TCP segment with the ECE flag set.<br>
ECE (1 bit):  It is used to indicate congestion to the sender.<br>
URG (1 bit):  Urgent pointer is said to be 1 if the data contains some urgent data.<br>
ACK (1 bit):  Acknowledgment flag is said to be 1 if it contains acknowledgement that the packet is recieved.<br>
PSH (1 bit):  Push flag is set to be 1 if we want our data to be sent immediately.<br>
RST (1 bit):  Used to reset a connection.<br>
SYN (1 bit):  SYN flag is set to be 1 if we want to establish a connection .<br>
FIN (1 bit):  Used to terminate a connection.<br><br><br>

Window Size (16 bits):It is the total capacity of the user. 
![image](https://github.com/user-attachments/assets/c172fb36-ab4b-4360-8ad6-2a27955de678)
<br>
<b>Checksum (16 bits):</b>
Used for error control.
<br>
<B>Urgent Pointer (16 bits):</b>
Tells us the range of data which is urgent.

![image](https://github.com/user-attachments/assets/a96bc3da-c655-4c6a-8c78-fcd981d66329)

<br>
<b>Options and padding :</b>
If we want to send some extra data we can send them through options and padding.
</h3><br>
<h2>UDP PACKET</h2>

![phptBFP20](https://github.com/user-attachments/assets/a4da21fc-0a6a-43f0-aa19-5359e0569295)





