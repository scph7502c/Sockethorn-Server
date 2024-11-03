# Sockethorn Server

This repository contains the server-side code for the Sockethorn chat application. The server is written in C and designed to handle secure, anonymous messaging for Android clients connecting through the TOR network.

## Project Structure

```
server/
├── src/              # Server source code
│   ├── main.c        # Main entry point
│   ├── sockets.c     # Socket handling for client connections
│   ├── encryption.c  # Message encryption module
│   ├── tor.c         # TOR integration
│   └── rooms.c       # Chat room management
├── include/          # Header files
├── tests/            # Unit tests
├── scripts/          # Build and deployment scripts
└── Makefile          # Build configuration
```

## Requirements

- **C Compiler**: GCC or Clang recommended.
- **TOR**: Required for anonymous connections.
- **OpenSSL**: For message encryption.

## Installation and Setup

1. **Clone the repository**:
   ```bash
   git clone https://github.com/scph7502c/sockethorn-server.git
   cd sockethorn-server/server
   ```

2. **Install dependencies**:
   - Make sure TOR and OpenSSL are installed on your server.
   - For Debian-based systems:
     ```bash
     sudo apt update
     sudo apt install tor openssl
     ```

3. **Build the server**:
   - Use `make` to compile the source code:
     ```bash
     make
     ```

4. **Run the server**:
   - Start the server application:
     ```bash
     ./server_app
     ```

## Usage

The server listens for incoming connections from Android clients. All communication is routed through the TOR network to ensure anonymity and security.

## Contributing

If you'd like to contribute to the project, feel free to fork the repository, make changes, and submit a pull request. Issues and feature requests are also welcome.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
