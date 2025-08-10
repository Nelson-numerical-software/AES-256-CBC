# AES-256-CBC Encrypt / Decrypt Web Tool with PBKDF2

A simple HTML/JavaScript web page for encrypting and decrypting text using AES-256-CBC with PBKDF2 key derivation — fully client-side in the browser, no server required.

## Features

- Encrypt plaintext using AES-256-CBC with PBKDF2 (100,000 iterations, SHA-256)
- Decrypt ciphertext encrypted with OpenSSL-compatible format (including `Salted__` prefix)
- Supports single-line and multiline text input (exclusive — only one active at a time)
- Live-updating OpenSSL command line reminder, dynamically showing commands for current input and password
- Copy-to-clipboard buttons for output and both OpenSSL commands with visual feedback
- Uses Web Crypto API for cryptographic operations (modern browsers only)
- No external dependencies or libraries

## Usage

1. Open `encryption-tools.html` in a modern browser (Chrome, Firefox, Edge).

2. Enter text to encrypt or the base64 ciphertext to decrypt.  
   - Use **either** the single-line input **or** the multiline input (the other will be cleared automatically).

3. Enter your password/key.

4. Click **Encrypt** or **Decrypt**.

5. The result will appear in the **Output** box.

6. The corresponding OpenSSL command lines for encrypting or decrypting the data are shown below for convenience and reproducibility.

7. Use the **Copy** buttons to copy results or commands to your clipboard.

## Compatibility

- Tested on latest versions of Chrome, Firefox, and Edge.
- Requires browser support for [Web Crypto API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Crypto_API).

## Security Notice

- The tool runs entirely client-side in your browser.
- The password and data are not transmitted over the internet.
- PBKDF2 uses 100,000 iterations with SHA-256 for key derivation.
- This tool is intended for educational or light personal use — do **not** use for sensitive production encryption without expert review.

## Development

- The project is a single HTML file: `encryption-tools.html`.
- Uses standard Web Crypto API primitives.
- Styling and UX are minimal and focused on functionality.

## License

BSD 3-Clause License

---

*Created by nelson.numerical.computation@gmail.com*  
*Feel free to open issues or contribute!*
