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

Server Recipe
Here is how a server would use sockets:
● socket() →Create a socket
● bind(port number) →Bind the socket to a particular port number
● listen() →Mark the socket as a listening socket
● accept() → Block and listen for connections
○ If a connection is established, the call will return a new socket corresponding to the
connection.
Once a connection is established, we can use read / write calls to receive / send data.
