The TCP-IP Model is made up of 4 (sometimes 5 depending whether the author decided to split the Network Interface layer up into the Data Link and the Physical layer) layers:
- Application
- Transport
- Internet
- Network Interface

Even though the [[OSI Model]] is not used in the real world, it is still of importance to use because since it is less condensed and more rigid, it allows us to break networking theory down into more bite sized pieces that are easier to learn.

The correspondence in the layers of the OSI Model and the TCP-IP model are as follows:
| OSI | TCP-IP |
|-----|--------|
| Application, Presentation, Session | Application|
| Transport | Transport |
| Network | Internet |
| Data Link, Physical | Network Interface |

[[Encapsulation]] works exactly the same way in the TCP-IP Model as it does in the OSI Model.

Now, it is fine to think of the TCP-IP Model as a layered model, however, it is much more realistically represented as a suite of protocols, or sets of rules, that define how actions are carried out. TCP-IP gets its name from the two most important of these mentioned protocols: the Transmission Control Protocol (TCP, which is briefly explained in the [[OSI Model]]) that controls the flow of data between two endpoints, and the Internet Protocol (IP) which controls how packets are addressed and sent. Keep in mind that there are many more protocols that make up the TCP-IP suite, TCP and IP are just two of the many.

TCP is a connection-based protocol. This means that a stable connection must be established between the two endpoints in order for data to be transitted and received. In order to form this connection, a proccess occur called the three-way handshake.

## Three-Way Handshake
To establish a connection, the trasmitting machine will send a request to the receiving machine, this request is called a SYN (Synchronize) bit. The receiving machine will then reply back with a SYN-ACK packet containing the SYN bit that it received, and an ACK (Acknowledgement) bit. Finally, to confirm the connection, the transmitting machine will reply to the SYN-ACK packet with just an ACK bit. This establishes that the connection was successful.

With the three-way handshake complete, data can now be reliably transferred between both enpoints. Any data that is lost or corrupted over the transmission proccess is re-sent, which leads to a connection that appears to be lossless.

**Visual Representation:**
Transmitting machine -------(SYN)------> Receiving machine

Transmitting machine <---(SYN/ACK)---- Receiving machine

Transmitting machine -------(ACK)------> Receiving machine