# coop-poc
# Missing COOP Header — Security POC

A proof-of-concept demonstrating the impact of a missing `Cross-Origin-Opener-Policy` (COOP) HTTP response header.

## Overview

When a web application does not set the `Cross-Origin-Opener-Policy` header, an attacker can open it in a new browser window and silently navigate the victim away to a malicious page — without any visible warning.

## Repository Structure
├── index.html   # Customer-facing security advisory
└── poc.html     # Proof-of-concept exploit page

## Usage
https://<your-username>.github.io/<repo-name>/poc.html?target=https://<target>
> ⚠️ Only test against systems you own or have explicit written permission to test.

## The Fix

Add the following HTTP response header to the target application:
Cross-Origin-Opener-Policy: same-origin

## References

- [MDN — Cross-Origin-Opener-Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cross-Origin-Opener-Policy)
- [web.dev — Why you need COOP & COEP](https://web.dev/why-coop-coep/)

## Disclaimer

This repository is intended for **security research and awareness purposes only**.  
The author is not responsible for any misuse of the code or techniques demonstrated here.
