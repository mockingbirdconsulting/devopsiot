# DevOps IoT

This is a reference repository for bringing the tooling part of DevOps to the Internet of Things.

## Setup Guide

This repository assumes you are working with Jenkins CI.

Install the Arduino IDE, and then on each of your build-slaves switch to the Jenkins user and run `arduino --install-boards <board_type>` where `<board_type>` is one of the valid instruction sets.

### Example

To setup Jenkins to build for the "standard" ATMEL/AVR boards, run `arduino --install-boards arduino:avr`, for the SAMD-based boards such as the Zero or the Exen Mini, run `arduino --install-boards arduino:samd`.
