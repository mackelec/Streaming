# Streaming Arduino Library README

## Introduction

The `Streaming` library is an Arduino library that introduces an intuitive way to send multiple types of data sequentially to the Serial port or any other `Print` class, using the familiar "streaming" << operator, similar to C++ iostream. It reduces the need to write repetitive `Serial.print()` statements.

## Features

- Simplified syntax for sending data to the Serial port using the << operator.
- Integrated support for different base conversions like HEX, DEC, OCT, and BIN.
- Support for sending bytes.
- Enhanced floating point precision support (for Arduino 0018 and later).
- Endline support with `endl`.

## Basic Usage

To use the library, include the `Streaming.h` header:

```
#include <Streaming.h>
```

Examples of the simplified syntax:

```
Serial << "This is an example" << endl;
Serial << "A is " << lettera << "." << endl;
```

## Modifiers

Modifiers allow you to specify the format of the data:

- **_BYTE(x)**: Prints `x` as a byte.
- **_HEX(x)**: Prints `x` in hexadecimal format.
- **_DEC(x)**: Prints `x` in decimal format.
- **_OCT(x)**: Prints `x` in octal format.
- **_BIN(x)**: Prints `x` in binary format.

For example:

```
Serial << _BYTE(lettera) << " is " << _HEX(lettera) << " in hex. " << endl;
```

## Installation

1. Download the ZIP of the library.
2. Open Arduino IDE.
3. Go to Sketch -> Include Library -> Add .ZIP Library.
4. Locate the downloaded ZIP and click open.

## Example

The `streaming_example.pde` provides a brief demonstration of the library's capabilities:

```
#include <Streaming.h>

void setup() {
    // ... setup code ...
    Serial << "A is " << lettera << "." << endl;
    // ... rest of the example ...
}
```

## License

This library is distributed under the GNU Lesser General Public License v2.1. For more information, check the source code header.

## Acknowledgments

- **Mikal Hart** for creating the library.
- Arduino forum users **Ben Combee**, **Michael Margolis**, and **Paul V.** for their valuable suggestions and contributions.

## Contributions

Feel free to contribute to this library by submitting pull requests or raising issues on GitHub.

## Version

The current version of the Streaming library is 5.

