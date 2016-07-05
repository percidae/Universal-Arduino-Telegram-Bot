#Universal Telegram Bot Library

An Arduino IDE library for using Telegram Bot API. It's designed to be used with multiple Arduino architectures.

Forked from [ESP8266-TelegramBot](https://github.com/Gianbacchio/ESP8266-TelegramBot) & inspired by [TelegramBot-Library](https://github.com/CasaJasmina/TelegramBot-Library)


## Introduction

This library provides an interface for [Telegram Bot API](https://core.telegram.org/bots/api).

Telegram is a instant messaging app that allows for the creation of bots. Bots can be configured to send and receive messages. This is useful for Arduino projects as you can receive updates from your project or issue it commands via your Telegram app.

As mentioned, this is a library forked from [one library](https://github.com/Gianbacchio/ESP8266-TelegramBot) and inspired by [another](https://github.com/CasaJasmina/TelegramBot-Library)

Each library only supported a single type of Arduino and had different features implemented. The only thing that needs to be different for each board is the actual sending of requests to Telegram so I thought a library that additional architectures or boards could be configured easily would be useful, although this springs to mind:

![alt text](https://imgs.xkcd.com/comics/standards.png "standards")


## Installing

The downloaded code can be included as a new library into the IDE selecting the menu:

     Sketch / include Library / Add .Zip library

You also have to install the ArduinoJson library written by [Benoît Blanchon](https://github.com/bblanchon).
Available [here](https://github.com/bblanchon/ArduinoJson).

Include UniversalTelegramBot in your project:

    #include <UniversalTelegramBot.h>

and pass it a Bot token and a SSL Client (See the examples for more details)

    #define BOTtoken "XXXXXXXXX:XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
    WiFiClientSecure client;
    UniversalTelegramBot bot(BOTtoken, client);

*NOTE:* This library has not been tested with the 101 boards as I do not have a compatible board. If you can help please let me know!

## Getting started

View the last released Telegram API documentation at: https://core.telegram.org/bots/api.

To generate your new Bot, you need an Access Token. Talk to [BotFather](https://telegram.me/botfather) and follow a few simple steps described [here](https://core.telegram.org/bots#botfather).

For full details, see "[Bots: An introduction for developers](https://core.telegram.org/bots)".


## Examples

Here are listed some examples to help you to build your own Bot:

- EchoBot : replies echoing your messages.

- FlashLedBot : Reacts to your command switching ON/OFF a GPIO.

- EchoBotWithPost : same as EchoBot but using post to commincate with Telegram.

- CustomKeyboard : Same as FlashLedBot but also uses a replyKeyboard



## License

You may copy, distribute and modify the software provided that modifications are described and licensed for free under [LGPL-3](http://www.gnu.org/licenses/lgpl-3.0.html). Derivatives works (including modifications or anything statically linked to the library) can only be redistributed under [LGPL-3](http://www.gnu.org/licenses/lgpl-3.0.html), but applications that use the library don't have to be.
