####1. TCP-Client-Server-DES_Algorithm
#####Reliable Transfer through TCP using DES Encrption Algorithm
#####DES Algorithm
######Data Encryption Standard (DES) encrypts blocks of size 64 bit. 
######It uses Block Ciphers and small key length of 56 bit.
######This pdf was used for understanding and implementing the encryption algorithm.http://www.cs.ucsb.edu/~koc/ns/docs/slides/03-des.pdf


##### Java_Client_Server_Application
A distributed networking application in Java consisting of a transmitter and a receiver that can ensure reliable data transfer and cryptographic authentication

#####The Following rules were used to write the program
The data packet should have the following fields (‘h’ stands for hexadecimal):
• Packet type (1 byte): This field describes the type of the packet. Its possible values are: 55h : Data packet with additional packet(s) to be sent later aah : Last data packet (the payload contains the last part of the data) 
• Sequence number (4 bytes): The ordinal number of the first sent byte in the payload of the current data packet. (The protocol counts bytes, and not packets.) It should start from a random value previously agreed by the transmitter and the receiver and be incremented based on the number of sent bytes for each sent packet. 
• Length field (1 byte): The length of the data (payload) in bytes. 
• Data (variable length): The carried payload as a sequence of bytes. 
• Integrity check field (4 bytes): The integrity check value provides error detection and authentication ability. Its value should be calculated as described later. 
The acknowledgment packet should have the following fields: 
• Packet type (1 byte): This field describes the type of the packet. It should be set to ffh.
• Acknowledgment number (4 bytes): The ordinal number of the next expected byte from the sender. The protocol uses cumulative acknowledgments, so this means that all data bytes with sequence numbers up to, but not including this acknowledgment number have been received correctly.  
• Integrity check field (4 bytes): The integrity check value provides error detection and authentication ability. Its value should be calculated as described later. The integrity check calculation is based on the RC4 encryption algorithm
