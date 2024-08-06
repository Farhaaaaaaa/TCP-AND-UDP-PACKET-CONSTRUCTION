<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TCP and UDP Packet Construction</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
        }
        h2, h3 {
            color: #333;
        }
        img {
            display: block;
            margin: 10px 0;
        }
        p {
            margin: 10px 0;
        }
    </style>
</head>
<body>
    <h3>To understand the construction of TCP and UDP packets, we need to understand what a TCP and UDP packet looks like</h3>

    <h2>TCP Packet</h2>

    <img src="https://github.com/user-attachments/assets/a78a9c99-e801-4cc9-a8a7-a51f78377296" alt="TCP Packet Diagram">

    <h2>Let us analyze this TCP packet completely</h2>

    <h3>
        <b>Source Port (16 bits):</b>
        The port number of the source.
    </h3>

    <h3>
        <b>Destination Port (16 bits):</b>
        The port number of the receiving application.
    </h3>

    <img src="https://github.com/user-attachments/assets/c973b5ae-91d7-4763-a65d-e3c89d17ee98" alt="TCP Packet Source and Destination Ports">

    <h3>
        <b>Sequence Number (32 bits):</b>
        It indicates the position of the first byte of data in the data segment.
    </h3>

    <img src="https://github.com/user-attachments/assets/e83cf94f-7338-4172-8e68-7d7be047f447" alt="TCP Packet Sequence Number">

    <h3>
        <b>Acknowledgment Number (32 bits):</b>
        It determines the sequence number of the next byte of the segment that the sender is expecting to receive.
    </h3>

    <img src="https://github.com/user-attachments/assets/745a22c4-48d8-4e67-be75-86263168c468" alt="TCP Packet Acknowledgment Number">

    <h3>
        <b>Data Offset (4 bits):</b>
        This field indicates the length of the TCP header in 32-bit words. The minimum value is 5 (for 20 bytes), and the maximum value is 15 (for 60 bytes).
    </h3>

    <h3>
        <b>Reserved (3 bits):</b>
        Reserved for future use and should be set to 0.
    </h3>

    <h3>
        <b>Flags (9 bits):</b> Various control flags:
        <ul>
            <li><b>CWR (1 bit):</b> It is set by the sender to indicate that it received a TCP segment with the ECE flag set.</li>
            <li><b>ECE (1 bit):</b> It is used to indicate congestion to the sender.</li>
            <li><b>URG (1 bit):</b> Urgent pointer field significant.</li>
            <li><b>ACK (1 bit):</b> Acknowledgment field significant.</li>
            <li><b>PSH (1 bit):</b> Push function.</li>
            <li><b>RST (1 bit):</b> Reset the connection.</li>
            <li><b>SYN (1 bit):</b> Synchronize sequence numbers.</li>
            <li><b>FIN (1 bit):</b> No more data from sender.</li>
        </ul>
    </h3>

    <h3>
        <b>Window Size (16 bits):</b> It is the total capacity of the receiver.
    </h3>

    <img src="https://github.com/user-attachments/assets/c172fb36-ab4b-4360-8ad6-2a27955de678" alt="TCP Packet Window Size">

    <h3>
        <b>Checksum (16 bits):</b> Used for error control.
    </h3>

    <h3>
        <b>Urgent Pointer (16 bits):</b> Indicates the end of the urgent data.
    </h3>

    <img src="https://github.com/user-attachments/assets/a96bc3da-c655-4c6a-8c78-fcd981d66329" alt="TCP Packet Urgent Pointer">

    <h3>
        <b>Options and Padding:</b> If we want to send some extra data, we can send it through options and padding.
    </h3>

    <h2>UDP Packet</h2>

    <img src="https://github.com/user-attachments/assets/a4da21fc-0a6a-43f0-aa19-5359e0569295" alt="UDP Packet Diagram">
</body>
</html>
