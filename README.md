# URL Encoder/Decoder - Privacy-First Developer Tool

[![Stars](https://img.shields.io/github/stars/formatho/url-encoder-decoder?style=social)](https://github.com/formatho/url-encoder-decoder)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Privacy First](https://img.shields.io/badge/Privacy-First%20%F0%9F%94%92-success)](https://formatho.com)
[![Try Online](https://img.shields.io/badge/Try%20Online-Online%20%F0%9F%8C%90-blue)](https://formatho.com/tools/url-encoder)

A fast, secure, and privacy-first URL encoder/decoder that processes data entirely in your browser. No data is ever sent to a server, ensuring complete privacy and security for your sensitive URLs.

## 🚀 Features

- **Instant Encoding/Decoding**: Real-time conversion as you type
- **Privacy-First**: All processing happens client-side in your browser
- **No Tracking**: Zero analytics, zero cookies, zero data collection
- **UTF-8 Support**: Full Unicode and emoji support
- **URL-Safe Encoding**: Support for both standard and URL-safe Base64 variants
- **Batch Processing**: Encode or decode multiple URLs at once
- **One-Click Copy**: Copy results to clipboard instantly
- **History Tracking**: Keep track of recent conversions
- **Responsive Design**: Works perfectly on desktop, tablet, and mobile

## 📖 Why Privacy Matters

Traditional URL encoder/decoder tools send your URLs to remote servers, exposing sensitive information:

- API keys and tokens embedded in URLs
- Session identifiers and authentication tokens
- Personal identifiable information (PII) in query parameters
- Internal application URLs and endpoints
- Database connection strings
- Proprietary business URLs

**Formatho processes everything in your browser** - your URLs never leave your device.

## 🔧 How It Works

### URL Encoding

URL encoding (also called percent encoding) converts special characters into a format that can be transmitted over the Internet. Characters that are not allowed in a URL are replaced with a `%` followed by two hexadecimal digits.

Example:
```
Original: https://example.com/search?q=hello world
Encoded:  https://example.com/search?q=hello%20world
```

### URL Decoding

URL decoding reverses the encoding process, converting percent-encoded characters back to their original form.

Example:
```
Encoded:  https://example.com/search?q=hello%20world
Decoded:  https://example.com/search?q=hello world
```

## 💻 Usage

### Web App

Visit [formatho.com/tools/url-encoder](https://formatho.com/tools/url-encoder) and:

1. **Encode**: Paste or type your URL in the input field
2. **Decode**: Paste an encoded URL in the input field
3. **Copy**: Click the copy button to copy the result
4. **History**: View and reuse recent conversions

### NPM Package

```bash
npm install @formatho/url-encoder-decoder
```

```javascript
import { encodeURL, decodeURL } from '@formatho/url-encoder-decoder';

// Encode a URL
const encoded = encodeURL('https://example.com/search?q=hello world');
console.log(encoded); // https://example.com/search?q=hello%20world

// Decode a URL
const decoded = decodeURL('https://example.com/search?q=hello%20world');
console.log(decoded); // https://example.com/search?q=hello world
```

### Command Line

```bash
# Encode a URL
npx @formatho/url-encoder-decoder encode "https://example.com/search?q=hello world"

# Decode a URL
npx @formatho/url-encoder-decoder decode "https://example.com/search?q=hello%20world"
```

## 🎯 Use Cases

- **API Development**: Encode URL parameters for API requests
- **Debugging**: Decode complex URLs to analyze query parameters
- **Data Migration**: Convert URLs during system migrations
- **Security Testing**: Analyze encoded URLs for security vulnerabilities
- **Web Development**: Test URL encoding/decoding in web applications
- **Data Analysis**: Parse and decode URLs from logs or databases
- **SEO**: Analyze and optimize URL structures
- **Privacy**: Safely encode/decode sensitive URLs without exposing them

## 🔒 Privacy & Security

At Formatho, we believe in privacy-first development:

- **Client-Side Processing**: All encoding/decoding happens in your browser
- **No Server Communication**: Your URLs never leave your device
- **No Analytics**: We don't track how you use this tool
- **No Cookies**: We don't store or use cookies
- **Open Source**: Code is available for security audits
- **MIT License**: Free to use, modify, and distribute

## 📊 Performance

| Operation | Time | Complexity |
|-----------|------|------------|
| Encode URL | < 1ms | O(n) |
| Decode URL | < 1ms | O(n) |
| Batch Processing (100 URLs) | < 50ms | O(n) |

*Benchmarks run on modern browsers (Chrome 120+, Firefox 120+, Safari 17+)*

## 🛠️ Installation

### For Web App

No installation required! Visit [formatho.com/tools/url-encoder](https://formatho.com/tools/url-encoder).

### For NPM Package

```bash
npm install @formatho/url-encoder-decoder
```

### For Command Line

```bash
npm install -g @formatho/url-encoder-decoder
```

## 📚 API Reference

### `encodeURL(url: string): string`

Encodes a URL using percent encoding.

**Parameters:**
- `url` - The URL to encode

**Returns:**
- The encoded URL

**Example:**
```javascript
const encoded = encodeURL('https://example.com/search?q=hello world');
// Returns: 'https://example.com/search?q=hello%20world'
```

### `decodeURL(url: string): string`

Decodes a percent-encoded URL.

**Parameters:**
- `url` - The URL to decode

**Returns:**
- The decoded URL

**Example:**
```javascript
const decoded = decodeURL('https://example.com/search?q=hello%20world');
// Returns: 'https://example.com/search?q=hello world'
```

### `encodeURLSafe(url: string): string`

Encodes a URL using URL-safe Base64 encoding.

**Parameters:**
- `url` - The URL to encode

**Returns:**
- The URL-safe encoded URL

**Example:**
```javascript
const encoded = encodeURLSafe('https://example.com/search?q=hello world');
// Returns: 'https://example.com/search?q=hello+world'
```

## 🤝 Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## 📄 License

This project is licensed under the MIT License - see [LICENSE.md](LICENSE.md) for details.

## 🔗 Related Tools

- [Base64 Encoder/Decoder](https://github.com/formatho/base64-encoder-decoder) - Encode and decode Base64 strings
- [HTML Entity Encoder/Decoder](https://formatho.com/tools) - Encode and decode HTML entities
- [JSON Formatter](https://github.com/formatho/json-formatter) - Format and validate JSON data
- [URL Parser](https://formatho.com/tools/url-parser) - Parse and analyze URLs

## 💬 Support

- **Issues**: [GitHub Issues](https://github.com/formatho/url-encoder-decoder/issues)
- **Discussions**: [GitHub Discussions](https://github.com/formatho/url-encoder-decoder/discussions)
- **Email**: support@formatho.com

## ⭐ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=formatho/url-encoder-decoder&type=Date)](https://star-history.com/#formatho/url-encoder-decoder&Date)

---

**Made with 🔒 by Formatho**

Privacy-first developer tools, 100+ utilities with zero tracking.

[Try Online](https://formatho.com/tools/url-encoder) | [More Tools](https://formatho.com) | [Privacy Policy](https://formatho.com/privacy)
## ⚡ Free API — Cloudflare Worker

This tool is also available as a free, zero-tracking API deployed on Cloudflare Workers:

**Endpoint:** https://url-encoder-formatho.filesformatho.workers.dev

Deploy it yourself: the complete Worker source is in [`worker/`](./worker) — `cd worker && wrangler deploy`. MIT licensed.

## 🔗 Links

- [Online tool](https://formatho.com/tools/url-encoder)
- [Live API](https://url-encoder-formatho.filesformatho.workers.dev)
