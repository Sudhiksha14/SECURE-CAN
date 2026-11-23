# AES-128 Protected CAN Communication for PLC-to-Actuator Systems

## Overview

This project explores a security retrofit for Classical CAN-based industrial communication systems using STM32 microcontrollers.

Traditional CAN communication provides reliable message transmission between electronic control units but does not inherently provide message authentication, confidentiality, or replay attack protection.

This project aims to introduce security mechanisms into a CAN-based communication system while evaluating the additional computational and communication overhead.

## Objectives

- Implement AES-128 encryption for protecting CAN application data.
- Implement AES-CMAC for message authentication and integrity verification.
- Incorporate rolling-counter-based replay attack detection.
- Preserve standard CAN identifiers for message identification.
- Implement a secure communication framework using STM32 microcontrollers.
- Evaluate communication latency, memory usage, and security-related overhead.

## System Architecture

The prototype consists of two STM32-based nodes connected through a Classical CAN bus.

- **Transmitter Node:** Generates application commands, applies the security mechanism, and transmits CAN frames.
- **Receiver Node:** Receives frames, performs security verification and replay checks, and processes valid commands.
- **CAN Bus:** Provides communication between the two nodes using Classical CAN.

## Security Features

- AES-128-based data protection
- AES-CMAC-based message authentication
- Rolling-counter-based replay detection
- CAN message validation

## Hardware

- STM32 microcontrollers[STM32F103C8T6]
- CAN transceivers[SN65HVD230]
- Supporting power supply and wiring

## Communication

The system uses Classical CAN communication. CAN identifiers are retained for message identification, while the security mechanism is incorporated into the application-level data handling.

## Performance Evaluation

The system will be evaluated based on:

- Communication latency
- Processing overhead
- Memory usage
- Successful message transmission and reception
- Replay detection behavior

## Future Work

- Expand security testing
- Evaluate performance under different communication loads
- Investigate additional CAN security mechanisms
- Explore scalability for multi-node networks

---

*This project is developed as an academic engineering project exploring security enhancements for industrial CAN communication.*
