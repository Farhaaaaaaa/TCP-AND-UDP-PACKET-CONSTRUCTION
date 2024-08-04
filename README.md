# TCP-AND-UDP-PACKET-CONSTRUCTION
<P> To understand the construction of TCP and UDP packets we need to understand what a TCP and UDP packet looks like</P>
<h2>TCP PACKET</h2>

![Screenshot 2024-07-30 105652](https://github.com/user-attachments/assets/a78a9c99-e801-4cc9-a8a7-a51f78377296)
<h2>Let us analyze this TCP packet completely</h2>
<B>Source Port (16 bits):</B>
The port number of the source.
<br>

![image](https://github.com/user-attachments/assets/23d214b7-11f9-427d-a37c-5a773b891fd0)
<p>suppose 50001 is the port number given to the application of the source and 80 is the port  number of the destination</p>
<b>Destination Port (16 bits):</b>
The port number of the receiving application.
<br>
Sequence Number (32 bits):

The sequence number of the first byte in this packet. If the SYN flag is set, this is the initial sequence number.
Acknowledgment Number (32 bits):

The next expected sequence number from the other side. This field is only valid if the ACK flag is set.
Data Offset (4 bits):

Specifies the size of the TCP header in 32-bit words. It indicates where the data begins. The minimum value is 5 (for a 20-byte header), and the maximum value is 15 (for a 60-byte header).
Reserved (3 bits):

Reserved for future use and should be set to 0.
Flags (9 bits):

Various control flags:
NS (1 bit): ECN-nonce - concealment protection (experimental).
CWR (1 bit): Congestion Window Reduced flag.
ECE (1 bit): ECN-Echo flag, indicates ECN capability.
URG (1 bit): Urgent pointer field significant.
ACK (1 bit): Acknowledgment field significant.
PSH (1 bit): Push Function.
RST (1 bit): Reset the connection.
SYN (1 bit): Synchronize sequence numbers (used to initiate a connection).
FIN (1 bit): No more data from the sender (used to terminate a connection).
Window Size (16 bits):

<br>
<b>Checksum (16 bits):</b>
Used for error control.
<br>
<B>Urgent Pointer (16 bits):</b>
Tells us the range of data which is urgent.
<br>
<b>Options and padding :</b>
If we want to send some extra datan we can send them through options and padding.
<br>
<h2>UDP PACKET</h2>

![phptBFP20](https://github.com/user-attachments/assets/a4da21fc-0a6a-43f0-aa19-5359e0569295)





