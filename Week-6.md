# Distributed Systems and their Features
## Case Nr. 1
A server program written in one programming language (for example C++) provides the implementation of a BLOB (Binary Large Object) object that is intended to be accessed by clients that may be written in a different language (for example Java). The client and server computers may have different hardware, but all of them are attached to an internet.

###### *Question*
Describe the problems due to each of the five aspects of heterogeneity that need to be solved to make it possible for a client object to invoke a method on the server object.

###### *Answer*
Since computers are connected to the Internet, Internet protocols deal with differences in
networks.Computers can be composed differently.So you have to take into account its differences when representing the data elements in the request and response messages from the clients to the objects.For each type of element to be transmitted, we will set up a standard.
It is also necessary to take into account the different operating systems that do not communicate with the same protocols (messages or requests). To go from one to another there must be a gateway that would translate the object so that it is understandable for the receiver.
there must be different implementors, for example one for C ++ and the other for Java for reciprocity.
conclusion:
- common communication standard.
- set of protocols
- unique standard for the representation of data structures
- calculation standard (different material)



## Case Nr. 2
###### *Let us contunue with a situation from Case Nr. 1*
An open distributed system allows new resource sharing services such as the BLOB object mentioned in Case Nr.1. 
to be added and accessed by a variety of client programs. 
###### *Question*
Discuss in the context of this example, to what extent the needs of openness differ from those of heterogeneity.


###### *Answer*
For an open distributed system it is necessary that, before implementing the object, the standards are decided. Moreover, after being added to the system, the interface with the BLOB must be posted so that the clients are able to access it. The publication of the standards allows different manufacturers to implement parts of the system and work together.


## Case Nr. 3
###### *We are working with a relevance to situation from Case Nr. 1 about BLOB*
Suppose that the operations of the BLOB object are separated into two categories – public
operations that are available to all users and protected operations that are available only to certain
named users. 
###### *Question*
State all of the problems involved in ensuring that only the named users can use a
protected operation. Supposing that access to a protected operation provides information that
should not be revealed to all users, what further problems arise?

###### *Answer*
Any request for access to protected information is followed by the name of the requester:
One of the problems is that one must be sure that the identity given is that of the requestor (false id).
Another problem is that other users should not be able to modify and replay legitimate requests from a user.
In the first place, one must of course define the identities of legitimate users in a list of people who can access protected operations and in the request messages.
Last problem, the information must be encrypted for not to access it.
Information returned as a result of a protected operation must be hidden from unauthorized users.
