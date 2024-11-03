# js-minimum-relay-coverage

## Overview

`js-minimum-relay-coverage` is a web application that helps users find the minimum set of Nostr relays needed to cover all their contacts. Users can input their Nostr public key in npub format, and the application will query multiple relays to determine the optimal relay set.

## Features

- **NIP-07 Extension Support**: Automatically fetch the public key from a NIP-07 extension if available.
- **Relay Querying**: Query multiple relays to fetch contacts and their associated relays.
- **Minimum Relay Set Calculation**: Compute the minimum set of relays needed to cover all contacts using a greedy algorithm.
- **User-Friendly Interface**: Simple and intuitive interface for entering public keys and displaying results.

## Usage

1. Open the `index.html` file in a web browser.
2. Enter your Nostr public key in npub format in the input field.
3. Click the "Find Relays" button to start the process.
4. Optionally, click "get from extension" to fetch the public key from a NIP-07 extension.
5. The results will be displayed in a table showing the minimum relay set and their coverage.

## Code Structure

- **HTML**: The main structure of the web application.
- **CSS**: Basic styling for the application.
- **JavaScript**: Contains the logic for querying relays, fetching contacts, and computing the minimum relay set.

## Dependencies

- [nostr-tools](https://cdn.skypack.dev/nostr-tools@1.8.2): A library for interacting with Nostr relays.

## Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Nostr Relay Finder</title>
    <style>
        /* CSS styles here */
    </style>
</head>
<body>
    <h1>Nostr Relay Finder</h1>
    <p>Enter your Nostr public key in npub format (or <a href="#" id="getFromExtension">get from extension</a>)</p>
    <input type="text" id="pubkey" placeholder="npub1..." />
    <button id="findRelays">Find Relays</button>
    <div id="output"></div>
    <script type="module">
        import { relayInit, nip19 } from 'https://cdn.skypack.dev/nostr-tools@1.8.2';
        // JavaScript code here
    </script>
</body>
</html>
```

## License

This project is licensed under the MIT License.

