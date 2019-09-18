# Reading-Task-RPC-Message-Protocol
_Reading task in system integration_

**DESCRIPTION**

_**According the Remote Procedure Call (RPC) model of distributed computing a client makes a remote procedure call to a network server and receives a reply containing the results of the procedure's execution.
In our demonstrative class exercises, we always assumed that both the call and reply messages have been transported without any errors, but this is not always the case.**

**Actually, RPC implements RPC message protocol, which defines the format of the call message and the reply message.**

**Being familiar with this format enables developers to control the validity of the messages, which the client and the server exchange. For example, if we know what is the RPC reply message that the client has received from a server, we can identify any reason for potential lack of expected result.**

**Your task is to search Internet for the answer of the following questions about the RPC message protocol:
If the request message has been accepted by the server, which information does the reply message provide?**_

The structure of a RPC message is as followed:

<img src="https://github.com/JonasManley/Reading-Task-RPC-Message-Protocol/blob/master/Pictures/RPC%20message%201.PNG" height="auto" width="auto" style="max-width:100%;">

The msg_type is the indicator of weather the message is a replay or call

<img src="https://github.com/JonasManley/Reading-Task-RPC-Message-Protocol/blob/master/Pictures/RPC%20message%202.PNG" alt="UML" height="auto" width="auto" style="max-width:100%;">


Replay message from an accepted request: 

<img src="https://github.com/JonasManley/Reading-Task-RPC-Message-Protocol/blob/master/Pictures/replay%20message%201.PNG" alt="UML" height="auto" width="auto" style="max-width:100%;">

<img src="https://github.com/JonasManley/Reading-Task-RPC-Message-Protocol/blob/master/Pictures/replay%20message%202.PNG" alt="UML" height="auto" width="auto" style="max-width:100%;">

Which status code will the server generate, if it can not 'understand' the parameters, sent by the client?

There’s 5 different status codes the server can use:

<img src="https://github.com/JonasManley/Reading-Task-RPC-Message-Protocol/blob/master/Pictures/status%201.PNG" alt="UML" height="auto" width="auto" style="max-width:100%;">

Based on the code above we can see that se status code generated would be: GARBAGE_ARGS  = 4


_source list for assignment_
https://en.wikipedia.org/wiki/Remote_procedure_call
http://ps-2.kev009.com/tl/techlib/manuals/adoclib/aixprggd/progcomc/rpcmsg.htm 
https://www.geeksforgeeks.org/remote-procedure-call-rpc-in-operating-system/_
