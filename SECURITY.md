# Security Policy

## Supported Versions

| Version | Status | Support Until |
|---------|--------|----------------|
| 1.0.x | ✅ Actively supported | Current + 1 year |
| < 1.0 | ❌ Unsupported | Not supported |

## Reporting a Vulnerability

**If you discover a security vulnerability, please email it to us rather than using the public issue tracker.**

### Responsible Disclosure

Please report security vulnerabilities to: **security@snapid.app** (placeholder)

Include:
- Description of the vulnerability
- Steps to reproduce
- Potential impact
- Suggested fix (if you have one)

**We will:**
1. Acknowledge receipt within 48 hours
2. Investigate and confirm the issue
3. Develop and test a fix
4. Release an update
5. Credit you in the security advisory (optional)

### Security Considerations

#### What SnapID Studio Does NOT Do

- ✅ **No photos are stored** — All processing happens in your browser
- ✅ **No data collection** — We don't track users
- ✅ **No servers involved** — Images never leave your device
- ✅ **No cookies** — Session data stays local
- ✅ **No analytics on photos** — Your privacy is protected

#### API Key Safety

Users provide their own Anthropic API keys to SnapID Studio.

**Security measures:**
- Keys are stored in browser memory only (not saved to disk)
- Keys are NOT sent to any SnapID servers
- Keys are only used for direct Claude API calls
- Users can revoke keys at any time in Anthropic console
- Each user controls their own spending limits

#### Browser Security

SnapID Studio relies on browser security features:
- **HTTPS-only** — All connections encrypted
- **CORS protection** — Only communicates with approved origins
- **CSP headers** — Vercel enforces strict Content Security Policy
- **No JavaScript injection** — Single-file app with no external scripts except CDN libraries

#### Third-Party Dependencies

Minimal external dependencies:
- **qrcodejs** — QR code generation (from CDN)
- **Anthropic API** — User-provided integration
- Everything else is browser-native APIs

Each CDN library is reviewed for security before use.

## Deployment Security

### Vercel (Hosting)

- ✅ Automatic HTTPS/TLS certificates
- ✅ Global CDN with DDoS protection
- ✅ Automatic security updates
- ✅ Edge function protection (if added)

### GitHub (Source Control)

- ✅ Public repository allows community review
- ✅ Branch protection prevents unauthorized changes
- ✅ Signed commits optional but recommended
- ✅ License file prevents misuse

## Privacy Policy

SnapID Studio does not:
- Collect personal data
- Store photos or user information
- Use cookies or tracking
- Sell data to third parties
- Share data with anyone

**Your privacy is built in — not an afterthought.**

## Compliance

### GDPR
- ✅ No personal data collected
- ✅ No data storage or processing
- ✅ Users own their data (stays in browser)

### CCPA
- ✅ No data sharing
- ✅ No data sales
- ✅ No tracking

### Other Standards
- ✅ Works with accessibility features (keyboard nav, screen readers)
- ✅ Supports dark mode
- ✅ Responsive design for all devices

## Reporting Other Security Concerns

### Indirect Security Issues

If you find issues with documentation or non-code security practices:
- Open a GitHub Issue (public discussion is fine)
- Or email security@snapid.app for sensitive matters

### Examples:
- Misleading privacy claims
- Incorrect documentation
- Accessibility barriers
- Mobile security concerns

## Bug Bounty

SnapID Studio is an open-source project with no formal bug bounty program.

However:
- We deeply appreciate responsible vulnerability reports
- We will credit reporters in security advisories
- Contributors get recognition in README & CHANGELOG

## Security Updates

When security issues are patched:
1. Fix is deployed immediately
2. Security advisory is published
3. README is updated with advisory link
4. Previous version users are notified

## Future Security Enhancements

Planned improvements:
- [ ] Two-factor authentication (if backend added)
- [ ] Rate limiting on API calls
- [ ] Subresource integrity (SRI) for CDN
- [ ] Certificate pinning (if desktop app added)
- [ ] Regular security audits

## Dependency Management

All dependencies are:
- Minimal (only what's necessary)
- Well-maintained
- Regularly updated
- Chosen for security, not just features

**Current dependencies:**
- qrcodejs (QR code generation)
- Anthropic API (vision analysis)

Both are:
- ✅ Open source
- ✅ Widely used
- ✅ Actively maintained
- ✅ Have good security practices

## Questions?

For security questions (non-vulnerability):
- 📧 Email: security@snapid.app
- 🐛 GitHub Issues: [Issues](https://github.com/yourusername/snapid-studio/issues)
- 💬 GitHub Discussions: [Discussions](https://github.com/yourusername/snapid-studio/discussions)

---

**Last Updated:** June 29, 2026

**Version:** 1.0.0

Thank you for helping keep SnapID Studio secure! 🔒
