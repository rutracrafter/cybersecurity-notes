The OSI Model is made up of seven layers:
- Application
- Presentation
- Session
- Transport
- Network
- Data Link
- Physical

Here is a brief overview of each of the seven layers:

## Application
This layer interacts directly with the programs running on a computer. It provides these programs with the necessary interfaced for these programs to trasmit data.

The data from this layer is then passed on to the Presentation layer.

## Presentation
This layer receives data from the Application layer and converts it to a standardized format, as well as performs other transformations to the data such as compression or encryption.

From here, the data moves on to the Session layer.

## Session
Upon receiving the correctly formatted data, the Session layer tries to set up a connection with the other computer that it is trying to connect to. If this connection isn't successful, an error occurs and the proccess ends here. If a session is established however, the Session layer's job is to mantain the connection and co-operate with the Session layer of the computer that it is connected to in order to synchronise communications.

Each session created by the Session layer is individual/unique to the communication in question. This is why many requests can be made to diffent endpoints at the same time without the data getting all mixed up (e.g. opening two browser tabs at the same time = two individual connections established and communicating at the same time)!

If this layer succeeds in connecting with the machine that we are trying to communicate with, then the data is then sent to the Transport layer.

## Transport
This layer is very important. Firstly, it is responsible for choosing which protocol will be used to trasmit the data. The two most common protocols are [[TCP]] (Transmission Control Protocol) and [[UDP]] (User Datagram Protocol).

Via TCP, a connection is established and maintained, which means there is reliable transmission of data and the connection can be used to ensure that all the packets get to the right place. Via UDP, the connection is not maintained, this is like throwing the packets at the receiving machine in the hopes that it will be able to keep up, however, if it isn't then that is its problem.

By the desciptions of the previously mentioned protocols, TCP is usually chosen for situations where the data's integrity/fidelity is prioritized over the transfer speed, whereas UDP prioritizes transfer speed. This is why things such as file tranfer, or loading a webpage are done via TCP, and things such as video streaming are done via UDP.

After choosing a protocol, the Transport layer then breaks up the data into bite-sized pieces (called segments over TCP, and datagrams over UDP) to make transmission easier.

## Network
This layer finds the destination of the request (and the best route) via the destination's IP address. IP addresses work via Logical Addressing which is still software controlled. Logical addresses provide order to networks be categorising them, and making them easier to sort and search them. The most common form of logical addressing is the IPV4 format (192.168.1.1 is a common address for a home router).

Now let us move on to the Data Link layer!

## Data Link
This layer focuses on the physical addressing of trasmission. It takes the packets that it reveices from the Network layer and adds in the physical (MAC) address of the receiving endpoint. Every network enable computer contains a NIC (Network Interface Card) which comes with a unique identification known as a MAC (Media Access Control) address.

MAS addresses are set by the manufacturer (burned onto the card) and so they cannot be changed, but they can be spoofed.

The MAC address allows the proccess of trasmission of data to know exactly which machine to send the information to on a network.

This layer is also responsible for presenting the data in a format that the Physical layer can trasmit.

This layer also does one other very important thing which is checking the received data to make sure that it hasn't been corrupted during transmission.

Now for the next layer!

## Physical
This layer is the closes to the hardware as it operates on the binary data that make up the information we are sending or receiving. This layer both converts binary data into electrical pulse signals that then are transmitted to and received by the receiving endpoint and converted back into binary data.

Alas! This is the last layer of the OSI Model!