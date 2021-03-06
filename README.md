# TCP-example

This 2 programs area part of a simple TCP client/server file transfer system.
For both sides you are allowed to send/receive a file.
The only particularity is: on the server side, it can handle up to 5 connections.

# Technical Specs
Buffer size: 5120 by default

# Requeriments
Might be created the following path on server side: "./files/rcv/".
And only ./files/ on client side.

# How it works:
* A server creates a socket at some port;
* Client tries to reach the server via TCP connection;
* Server is waiting for requests, so it accecpts (through 3-way-handshake)
* Connections will be closed as soon as the client choose the Exit option, or he loses its connection.

Whatever client wants to do (send/receive a file) it will send a message telling the server what operation it is. This message contains a "!" and a letter the represents the operation:

| Message  | Meaning |
| ------ | ------ |
| !s | Send a file to server |
| !r | Receive a file from server |
| !x | Exit |


# Plus
This is a program based on most basic concepts of networking, in this case I used "Computer Networking: A Top-Down Approach" (James F. Kurose).
I used an older edition (5th) of his book which has some code in it, but is in Java. I know that some newer editions includes python codes. So feel free to check it.

