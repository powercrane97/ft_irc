# IRC Server

## Description

This project is a C++ implementation of an IRC (Internet Relay Chat) server.

## Features

*   Supports common IRC commands:
    *   `INVITE <nickname> <#channel>` - Invites a user to a channel.
    *   `JOIN <#channel>` - Allows a client to join a channel.
    *   `KICK <#channel> <nickname> [:<reason>]` - Removes a user from a channel.
    *   `MODE <#channel>|<nickname> <modes> [parameters]` - Sets or unsets channel or user modes.
        *   Channel modes examples: `MODE #channel +i` (invite-only), `MODE #channel +t` (topic protection by operators).
        *   User modes examples: `MODE yournick +o` (operator status, if permitted).
    *   `PART <#channel> [:<reason>]` - Allows a client to leave a channel.
    *   `PRIVMSG <target> :<message>` - Sends a private message to a user or a channel.
        *   Example to user: `PRIVMSG nickname :Hello there!`
        *   Example to channel: `PRIVMSG #channel :This is a message to the channel.`
    *   `QUIT [:<reason>]` - Disconnects a client from the server.
    *   `TOPIC <#channel> [:<newtopic>]` - Sets or views the topic of a channel.
*   Channel management
    *   Creating and deleting channels
    *   Joining and leaving channels
    *   Setting and unsetting channel modes (e.g., invite-only, topic protection)
    *   Listing available channels
    *   Displaying channel user lists
*   Client handling

## Getting Started

### Prerequisites

*   A C++ compiler (e.g., c++)
*   Make

### Building

1.  Clone the repository:
    ```bash
    git clone <repository-url>
    cd irc
    ```
2.  Build the project using Make:
    ```bash
    make
    ```

## Usage

After building, you can run the server executable.

To run the server:
```bash
./ircserv <port> <password>
```

To connect to the server using an IRC client (e.g., irssi):
Connect to `localhost` on the specified `<port>` with the given `<password>`.

For example, if you started the server with `./ircserv 6667 secret`, you would connect to `localhost:6667` with the password `secret`.

### Recommended Client

For the best experience and compatibility, it is recommended to use [irssi](https://irssi.org/) as your IRC client.

## Reference

These IRC [docs](https://modern.ircdocs.horse) were used for reference. 

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.