# Anonymous API Credits

WIP, but want to get early feedback to see if this is worth pursuing.

A privacy-preserving approach for anonymous, paid usage of web APIs.


## Disclaimer

This is a personal proposal and does not represent the views of my employer, Google.

## Overview

This project proposes a cryptographic approach that allows users to purchase API credits and spend them anonymously within the same service. By implementing these cryptographic operations directly in the browser, we can prevent side-channel attacks and provide stronger privacy guarantees for users accessing APIs like LLMs, while maintaining security for API providers.

### Key Features

- **True Anonymity**: Service providers cannot correlate different transactions to the same user
- **Double-Spend Prevention**: Ensures credits can only be spent once
- **Credit Conservation**: Total credits issued always ≥ credits spent
- **Browser-Based Security**: Cryptographic operations handled securely by the browser

## How It Works

The system uses BBS signatures to create anonymous credentials:

1. **KeyGen**: The API provider generates a BBS keypair
2. **Issue**: When a user purchases credits, the browser generates blinding factors and receives a signed token
3. **Spend**: When using credits, the browser creates zero-knowledge proofs to spend credits without revealing identity

## Documentation & Feedback

We're actively seeking feedback on this proposal from web developers, browser implementers, and privacy experts. Your input will help shape this technology:

- **Design Document**: [View the full design proposal](https://docs.google.com/document/d/1F4BN-SJnXt9hlk0Ay5iDQPSS88yMBD_3l6GKMC5ydQg/edit?tab=t.0)
- **Project Website**: [Anonymous API Credits](http://samuelschlesinger.github.io/anoncreds)
- **Feedback**: Please open an issue in this repository with your questions, suggestions, or concerns

## Current Status

This project is in the early proposal stage. We welcome community input on the design, potential use cases, and implementation approaches.

## License

Currently, all rights are reserved. Please give feedback on this proposal directly rather than forking it.
