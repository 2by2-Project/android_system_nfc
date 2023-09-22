# Casimir

## Introduction

Casimir aims to provide virtual tag discovery and emulation for NFC
applications, in order to unlock NFC capability in various testing
contexes.

Casimir includes a virtual NFCC implementation, and internally emulates
RF communications between multiple connected hosts.

## Dependencies

Packet parsing and serialization depends on the pdlc generator.
It is installed with the following command:

```
cargo install pdl-compiler
```

## Usage

```
$ cargo run -- --help
Usage: casimir [--nci-port <nci-port>] [--rf-port <rf-port>]

Nfc emulator.

Options:
  --nci-port        configure the TCP port for the NCI server.
  --rf-port         configure the TCP port for the RF server.
  --help            display usage information
```

## Supported features

Casimir currently supports a subset of the NFC features described in the
following technical specification documents:

- `[NCI]` NFC Controller Interface Technical Specification Version 2.2
- `[DIGITAL]` Digital Protocol Technical Specification Version 2.3
- `[ACTIVITY]` Activity Technical Specification Version 2.2

Supported technologies: `NFC_A`
Supported protocols: `ISO_DEP`, `NFC_DEP`
Supported RF interfaces: `ISO_DEP`, `NFC_DEP`