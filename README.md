# Computer Networks Understanding Socket API 

The Socket API
Sockets work very similar to file operations.

● open() socket() → Open a socket
● read() → Read / receive data from a socket (aka recv)
● write() → Write / send data to a socket (aka send)
● close() → Close the socket
In addition to this, we have:
● bind() → Associate socket with a port number
● listen() →Mark socket as ‘listener’
● accept() →Accept new connections as a listener socket


## Server Recipe
Here is how a server would use sockets:
● socket() →Create a socket
● bind(port number) →Bind the socket to a particular port number
● listen() →Mark the socket as a listening socket
● accept() → Block and listen for connections
○ If a connection is established, the call will return a new socket corresponding to the
connection.
Once a connection is established, we can use read / write calls to receive / send data.



## Reads / Writes to sockets read(n: bytecnt, data_addr: pointer)
● Reads upto n bytes from the network stack into data_addr
● Returns the number of bytes actually read upon completion
● This call blocks until there is something to read!
write(n: bytecnt, data_addr: pointer)
● Sends upto n bytes to the network stack from data_addr
● Returns the number of bytes actually written
● This call blocks if the network stack is busy until it is free
