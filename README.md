# lds_dev_client

A lightweight utility package for getting the hostname for LearningDeck Client Web.

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

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
