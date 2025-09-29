[![Modern Embedded Software](img/masthead1.jpg)](https://www.state-machine.com)

# Community Contributed Software

This repository contains links and brief descriptions of contributed software realated to [QP/C](https://github.com/QuantumLeaps/qpc), [QP/C++](https://github.com/QuantumLeaps/qpcpp), [QM](https://github.com/QuantumLeaps/qm), or [QTools](https://github.com/QuantumLeaps/qtools).

# Licensing
The contributed software is owned by the respective developers and is *not* licensed by Quantum Leaps. Please see the linked repositories for the licensing terms offered.

## Table of Contents
- [QP/C++ ESP32](#qpc-esp32)
- [Embedded CLI for QP/C++](#embedded-cli-for-qpc-embedded-cli-for-qpcpp)
- [CppUTest for QP/C++](#cpputest-for-qpc-cpputest-for-qpcpp)
- [CppUTest for QP/C](#cpputest-for-qpc-cpputest-for-qpc)
- [QP/C examples running on low end microcontrollers](#qpc-examples-running-on-low-end-microcontrollers)
- [QP/C 'pollfd'-based POSIX Port](#qpc-pollfd-based-posix-port-qpc-posix-fd-port)
- [Licensing](#licensing)<br>


## QP/C++ ESP32
C++ Port for the ESP32 microcontroller from [espressif](https://www.espressif.com/). The port is compatible with the native sdk from espressif, [esp-idf](https://github.com/espressif/esp-idf), and the [arduino sdk](https://github.com/espressif/arduino-esp32). 

- Link: https://github.com/vChavezB/qpcpp/tree/esp32
- License: GPLv3

## Embedded CLI for QP/C++ (embedded-cli-for-qpcpp)

Need a CLI for your firmware project? This project provides a port of the [Embedded CLI](https://github.com/funbiscuit/embedded-cli) 
to a shared active object for QP/C++. Host project provides a concrete character device implementation
to fully enable and start the CLI.

Additional Information:
- License:  MIT
- Adheres to [Shared Active Objects For QP Best Practices](https://github.com/covemountainsoftware/Shared-Active-Objects-For-QP-Best-Practices).
- Link: https://github.com/covemountainsoftware/embedded-cli-for-qpcpp

## CppUTest for QP/C++ (cpputest-for-qpcpp)
[![cpputest-for-qpcpp](img/cpputest-qpcpp-img.jpg)](https://github.com/covemountainsoftware/cpputest-for-qpcpp)

A port of `qpcpp` with additional supporting code to enable and simplify host based unit testing 
of `QActive` objects using CppUTest. Includes examples demonstrating topics such as:  
* Capturing and testing of published events.
* Testing subscribed event behavior.
* Testing direct post behavior.
* Testing interactions with other active objects.
* Testing interactions with a mocked driver.
* An example continuous integration (CI) setup using GitHub Actions.
* And more!

Additional Information:
- License: Default GPLv3, with a commercial license available upon registration.
- Link: https://github.com/covemountainsoftware/cpputest-for-qpcpp

## CppUTest for QP/C (cpputest-for-qpc)
[![cpputest-for-qpc](img/cpputest-qpc-img.jpg)](https://github.com/covemountainsoftware/cpputest-for-qpc)

This port is conceptually the same as `cpputest-for-qpcpp` (noted above) but instead uses QP's C language 
based framework (`qpc`) with CppUTest. See the details on `cpputest-for-qpcpp` above for benefits, which also apply to 
this version.

Additional Information:
- License: Default GPLv3, with a commercial license available upon registration.
- Link: https://github.com/covemountainsoftware/cpputest-for-qpc

## QP/C examples running on low end microcontrollers
1- A QP/C based solution for the Dining Philosopher Problem ported on MSP430G2553 with only 16 KB of flash and 512 bytes of RAM.

[![MSP430 LaunchPad](img/msp430-launchpad.jpg)](https://github.com/ef15c/qpc-msp430.git)

- Link: https://github.com/ef15c/qpc-msp430.git
- License: GPLv3

2- A QP/C port on Arduino/AVR and an example showing a solution for the Dining Philosopher Problem.

[![Arduino UNO](img/arduino-uno.jpg)](https://github.com/ef15c/qpc_avr.git)

- Link: https://github.com/ef15c/qpc_avr.git
- License: GPLv3

## QP/C 'pollfd'-based POSIX Port (qpc-posix-fd-port)

This port is similar to POSIX-QV, but implemented in a single thread using `poll` (or `ppoll` in Linux)
and signaling events through file-descriptors (aka "pipes"). This is NOT a real-time kernel, but offers the ability to
run the QP/C kernel and your application within a broader pollfd event-loop (e.g., reading devices, running
integration tests, etc.). This is primarily intended for verifying the logic or control-flow of an application
in a "hardware-out-of-the-loop" setup on a POSIX system.

Additional Information:
- License: Default GPLv3, with a commercial license available upon registration.
- Link: https://github.com/mikael-s-persson/qpc/tree/feature/posix-fd-port/ports/posix-fd

