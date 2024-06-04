## Student Collaboration Chat Protocol Implementation using QUIC in GO

## Overview
The Student Collaboration Chat Protocol Application is a network-based chat application designed to facilitate communication among students. It uses the QUIC protocol for secure, reliable communication and supports both server and client modes. This project is implemented in Go.

## Team Members
- **Rohit Annasaheb Ragde**: [rar369@drexel.edu](mailto:rar369@drexel.edu)
- **Disha Yadav**: [dcy26@drexel.edu](mailto:dcy26@drexel.edu)

## QUIC Features in Chat Protocol

#### Real-Time Messaging

- **Basic Messaging:** Implement basic functionality for sending and receiving messages between clients.
- **QUIC Protocol:** Utilizes the `quic-go` library to handle QUIC sockets for efficient and reliable communication.
- **Message Encoding/Decoding:** Custom PDU (Protocol Data Unit) format is used for message encoding and decoding to ensure efficient data transmission.
- **Emoji Support:** Supports sending and receiving messages with emojis as part of the Unicode standard.

#### User Management

- **Username Handling:** Users can join the chat with a specified username.
- **User Join/Leave Notifications:** Notifies all users when someone joins or leaves the chat.

#### Broadcast Messaging

- **Message Broadcasting:** Sends messages to all connected clients, ensuring everyone in the chat room receives the messages.

#### Active Users Listing

- **List Active Users:** Allows users to request a list of active users in the chat room.

#### Authentication

- **TLS for Secure Connections:** Incorporated TLS to secure connections. The client uses a certificate file for authentication, ensuring that only authorized clients can connect to the server. If a certificate file is not provided, the client defaults to using a basic TLS configuration.

#### Multi-client Support

- **Handling Multiple Clients:** The server can handle multiple clients simultaneously. Each client initiates a connection and opens a stream to communicate with the server. The server can manage multiple streams concurrently, allowing multiple clients to communicate at the same time.

#### Error Handling

- **Error Logging:** Error handling is critical in our protocol. Both the client and server log any errors encountered during communication. If an error occurs, such as an issue with reading from a stream or decoding a PDU, it is logged.

#### Chat Messages from Client to Server

- **Initial Handshake and Message Exchange:** Clients can send chat messages to the server. This is part of the initialization handshake, where the client sends a "hello from client" message. The server responds with a menu of video options for the client to choose from.

  






