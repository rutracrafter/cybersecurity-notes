As data gets passed down the [[OSI Model]], each layer adds more information to the data that is being transmitted pertaining to that layer's purpose (e.g. the Network layer adding source and destination IP addresses, or the Transport layer adding information about the chosen protocol).

The name of the process of adding this additional data at each layer is Encapsulation.

In the OSI Model's Application, Presentation, and Session layer, the data is just referred to as data. In the Transport layer, the data is referred to by a name depending on the protocol, segments if the protocol is TCP and datagrams if the protocol is UDP. In the Network layer the data is referred to as packets. In the Data Link layer the data is referred to as frames and in the Physical layer, the data is reffered to as bits because at that point it is binary data.

All layers except the Physical layer add a header to the data, the Data Link layer also adds a tail to the data, and the Physical layer only converts the data from the Data Link layer into binary data.

When the receiving machine receives the data, the data travels back up the OSI model (starting in the Physicial layer and ending in the Application layer) to get back to its original form before encapsulation.

The process that was just described is called De-encapsulation.

The importance of Encapsulation and De-encapsulation is that it gives us a standardized way of sending and receiving data. This means that any network enabled device can send or receive data to other reachable network enabled devices as long as it adheres to this standardized way of transmitting information no matter which manufacturer made it, operating system it runs on, or other factors.