# Concepts

## Networking

### OSI Model

[Wikipedia - OSI Model](<https://en.wikipedia.org/wiki/OSI_model>)

A conceptual model that "provides a common basis for the coordination of [ISO] standards development for the purpose of systems interconnection". The communications between a computing system are split into seven abstraction layers: Physical, Data Link, Network, Transport, Session, Presentation, and Application.

| Layer             | Function |
| ----------------- | ------------- |
| 7 - Application   | (Data) High-level protocols for resource sharing or remote file access. Responsible for loading resources to make a site work. E.g. Loading an application (website) and setting headers and cookies.  |
| 6 - Presentation  | (Data) Translate data between network service and an application. Encoding, data compression, encryption/dexryption |
| 5 - Session       | (Data) Duration a connection from a sender to reciever remains open. Manage communication sessions and checkpoints. E.g. sending a 500mb file. Session can verify the file can be uploaded and chackpoint can check after each 10mb increment. If upload fails, checkpoint can be used to pickup where upload left. |
| 4 - Transport     | (Segment data) Break down data and assign source and destination ports with TCP or UDP. |
| 3 - Network       | (Packet) Further breakdown data and prepare packets from segments. Add source and destination IPs to packets. |
| 2 - Data link     | (Frame) Further breakdown data (packet from layer 3) and prepare frames. Attach source and destination MAC address. |
| 1 - Physical      | (Bit) Physical equipment (cables, hubs, switches). Data (frames) get converted to bit stream (1s and 0s). |

#### Example Using Below Layers (Sending a Slack Message)

Sender

- Application layer picks HTTP protocol and prepares the request (Slack message)
- Presentation layer prepares the message by encyrpting it (HTTPS) and compressing if needed
- Session with create a session needed to transport the data
- Transport layer breaks down data into smaller segments and assign ports to segments
- Network layer breaks down the segments into packets and will assign source/destination IPs
- Data link layer breaks down packets to frames and will attach MAC address
- Physical layer will convert frames to 1s and 0s (completes sender OSI process)

Reciever
- Physical layer will convert 1s and 0s to frames
- Data link layer will convert frames to packets
- Network layer will convert packets into segments
- Transport layer will convert segments into a single data piece
- Session layer will close session if needed
- Presentation layer will decrypt, decompress, and decode as needed
- Application layer will feed data to application and can be shown to the user.

## POSIX

## Sockets

## Proceses

## I/O Management

## Virtualization

## Memory/Storage

## File Systems
