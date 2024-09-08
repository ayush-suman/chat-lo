# chat-lo

## Description
`chat-lo` is a simple C-based UDP communication system that allows for message exchange between two local addresses using multi-threading to handle concurrent tasks such as receiving and sending messages. This project implements two separate communication modules to demonstrate the basic principles of UDP networking, socket programming, and multi-threading in C.

## Table of Contents
1. [Installation](#installation)
2. [Usage](#usage)
3. [Features](#features)
4. [Architecture](#architecture)

## Installation
To compile the source files, you'll need to have a C compiler installed on your system. You can use GCC (GNU Compiler Collection) to compile the programs.

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/chat-lo.git
   ```
2. Navigate to the project directory:
   ```
   cd chat-lo
   ```
3. Compile the C files:
   ```
   gcc -pthread chatside1.c -o chatside1
   gcc -pthread chatside2.c -o chatside2
   ```

## Usage
1. Start `chatside1` in one terminal window:
   ```
   ./chatside1
   ```
2. Start `chatside2` in another terminal window:
   ```
   ./chatside2
   ```
3. Now, you can send and receive messages between the two terminals.

## Features
- **UDP Communication:** Set up basic UDP client and server for message exchange.
- **Multi-threading:** Utilizes pthreads to concurrently handle message receiving and user input.
- **Local Addressing:** Communicates between two specified local addresses.

## Architecture
The repository consists of two main C files, each implementing a UDP communication module:

### chatside1.c
- Implements a UDP client.
- Sets up two socket addresses for the client and server.
- Uses threads to manage message receiving and user input concurrently.
- Binds the client's address and initializes the sockets.

### chatside2.c
- Implements UDP communication between two local addresses.
- Creates and binds a socket for the local address.
- Uses threads for concurrent receiving and sending of messages.
- Continuously listens for and prints incoming messages, while sending user-input messages to the specified address.

This setup allows smooth and effective message flow management using multi-threading and provides a basic understanding of socket programming in C.