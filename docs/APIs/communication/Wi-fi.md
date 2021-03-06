# Wi-Fi

The [WifiInterface](https://docs.mbed.com/docs/mbed-os-api/en/mbed-os-5.2/api/classWiFiInterface.html) provides a simple C++ API for connecting to the internet over a Wi-Fi device.

There are multiple Wi-Fi components that implement the WiFiInterface class. For the example below,
the [ESP8266Interface](https://github.com/armmbed/esp8266-driver) is used.

## API

[![View code](https://www.mbed.com/embed/?type=library)](https://docs.mbed.com/docs/mbed-os-api/en/mbed-os-5.3/api/classWiFiInterface.html)

## Usage

To bring up the network interface:

1. Instantiate an implementation of the WiFiInterface class (for example the [ESP8266Interface](https://github.com/armmbed/esp8266-driver)).
1. Call the ``connect`` function with an SSID and password for the Wi-Fi network. 
1. Once connected, the WiFiInterface can be used as a target for opening [network sockets](network_sockets.md).

## Example

Here is an example of an HTTP client program. The program brings up an ESP8266 as the underlying network interface, and uses it to perform an HTTP transaction over a TCPSocket:

[![View code](https://www.mbed.com/embed/?url=https://github.com/ARMmbed/mbed-os-example-wifi/)](https://github.com/ARMmbed/mbed-os-example-wifi/blob/master/main.cpp)
