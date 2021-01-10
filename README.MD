This is an example of configuration file for NGINX to balance a load between 2 or more servers.
In this case we used least_conn balacing mechanism. In this mechanism request is sent to the server with the least number of active connections with server weights taken into account:

But there are other methods to implement

Round Robin – All requests are distributed evenly across the servers, with server weights taken into consideration.
IP Hash – The server to which a request is sent is determined from the client IP address. In this case, either the first three octets of the IPv4 address or the whole IPv6 address are used to calculate the hash value. The method guarantees that requests from the same address get to the same server unless it is not available.
