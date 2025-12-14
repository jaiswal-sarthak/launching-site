# Launch Pad - Vercel Deployment

A production-ready rocket launch page with countdown and automatic redirect to payload URL.

## 🚀 Quick Start

### Deploy to Vercel

1. Push your code to GitHub
2. Import project in Vercel
3. Deploy - that's it!

The `vercel.json` file is already configured for optimal routing.

## 📝 Usage

### Basic Usage

Simply add the payload URL as a query parameter:

```
https://your-domain.vercel.app/launching.html?payload=https://example.com
```

### Supported Parameter Names

You can use any of these parameter names:
- `payload` (recommended)
- `url`
- `target`
- `dest`
- `destination`

### Examples

```
# Full URL with protocol
?payload=https://google.com

# Domain only (https:// will be added automatically)
?payload=github.com

# URL encoded (handled automatically)
?payload=https%3A%2F%2Fexample.com

# Using different parameter name
?url=https://stackoverflow.com
```

## 🔒 Security Features

- ✅ XSS prevention (blocks `javascript:`, `data:`, etc.)
- ✅ URL validation and sanitization
- ✅ Protocol enforcement (HTTP/HTTPS only)
- ✅ Input encoding/decoding
- ✅ Secure redirect (prevents back navigation)

## 🎯 How It Works

1. User visits the page with `?payload=URL` in the URL
2. System extracts and validates the payload
3. Destination is displayed on screen
4. User clicks "LAUNCH NOW"
5. Countdown begins (5 seconds)
6. After countdown, redirects to the payload URL

## 📋 Requirements

- Modern browser with JavaScript enabled
- No backend required (pure client-side)

## 🛠️ Customization

The payload can also be provided via:
- URL hash: `#payload=https://example.com`
- Data attribute: `<body data-payload="https://example.com">`
- Meta tag: `<meta name="payload" content="https://example.com">`

URL query parameter is the primary method and recommended for Vercel deployment.
