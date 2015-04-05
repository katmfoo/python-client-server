## Client-Server Network
A basic example of a TCP client/server network using Python's socket and threading library. The server uses instances of a client object and individual threads to listen to incoming data from each client while listening for new connections.

### Running
* Download the `server.py` and `client.py` python files for Python 3.
* Run `server.py`. You will be prompted for a host and port for the server. If you are going to run the client on the same computer or local network as the server, use `localhost` as the host name. If you are going to run the client on a different network, use the computer's local IP address (the IP address that resembles [one of these](http://en.wikipedia.org/wiki/Reserved_IP_addresses)). The port can be any 16 bit number (lower than 65535), but must be forwarded on your router if the client will be on a different network.
* Run `client.py`. If the server is running on the same computer, use `localhost` as the host. If the server is running on a different computer, but the same local network, use the local IP address of the computer that the server is running on. If the server is running on a different network, use the external IP address of the network that the server is running under (google [what is my ip](https://www.google.com/search?q=what%20is%20my%20ip)).

### Usage
The client should successfully connect to the server. Each time the server accepts a new connection, it will print the connection information to the server console. When the server receives a message from any of the clients, it will print the message to the server console and bounce the messsage to all other clients (not the client that sent it).

On the client, just type in a message and hit enter to send it to the server. Due to the way the console works, if a message is sent to you while you are typing a message yourself, it will interrupt your typing.
