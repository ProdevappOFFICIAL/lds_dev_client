# lds_dev_client

[![npm version](https://img.shields.io/npm/v/lds_dev_client.svg)](https://www.npmjs.com/package/lds_dev_client)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A lightweight utility package that extracts the hostname and port from the current URL.

## Installation

```bash
npm install lds_dev_client
```

## Usage

```javascript
// ES6 import
import { HostAddress, HostPort } from 'lds_dev_client';

// Example: If the page URL is "https://localhost:3000"
console.log(HostAddress); // Outputs: "localhost"
console.log(HostPort);    // Outputs: 3000

// If the page URL is "https://example.com/"
console.log(HostAddress); // Outputs: "example.com"
console.log(HostPort);    // Outputs: 443 (default HTTPS port)

// If the page URL is "http://localhost/"
console.log(HostAddress); // Outputs: "localhost"
console.log(HostPort);    // Outputs: 80 (default HTTP port)
```

You can also use the functions directly for more flexibility:

```javascript
import { getHost, getPort } from 'lds_dev_client';

const host = getHost();
const port = getPort();
```

## License

MIT

## Author

Your Name

## Examples

Here's a simple example showing how to use the package in a React application:

```jsx
import React from 'react';
import { HostAddress, HostPort } from 'lds_dev_client';

function ServerInfo() {
  return (
    <div className="server-info">
      <h3>Server Information</h3>
      <p>Connected to: {HostAddress}</p>
      <p>Port: {HostPort}</p>
    </div>
  );
}

export default ServerInfo;
```

## API Reference

### Constants

| Name | Type | Description |
|------|------|-------------|
| `HostAddress` | String | The hostname from the current URL (e.g., "localhost", "example.com") |
| `HostPort` | Number | The port number from the URL, or default port (80 for HTTP, 443 for HTTPS) |

### Functions

| Name | Return Type | Description |
|------|-------------|-------------|
| `getHost()` | String | Function to get the hostname dynamically |
| `getPort()` | Number | Function to get the port dynamically |

## Browser Compatibility

This package is designed for browser environments and has been tested with:

- Chrome 85+
- Firefox 80+
- Safari 14+
- Edge 85+

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
