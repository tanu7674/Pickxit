# Changelog

All notable changes to SnapID Studio are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] — 2026-06-29

### Added

**Core Features**
- ✨ AI-guided photo cropping using Claude vision
- 📸 Support for JPG, PNG, WEBP, BMP formats
- 🌍 50+ countries with pre-loaded document specifications
- 📄 9+ document types (passport, visa, ID, driver's license, etc.)
- 🖨️ 300 DPI print-ready output
- 📋 Print sheet preview (4×6" paper layout)
- 🔒 100% browser-based processing (no server uploads)
- ⚡ Optional Anthropic API key integration
- 💾 Smart auto-crop fallback without API key

**Document Types**
- Passport (all major countries)
- Visa (US, UK, India, UAE, China, Singapore, EU)
- National ID card
- Driver's license
- Residence permit
- Work permit
- Student ID
- Travel documents
- Custom size (user-defined dimensions)

**Countries Supported**
- 🇺🇸 United States
- 🇬🇧 United Kingdom
- 🇮🇳 India
- 🇨🇦 Canada
- 🇦🇺 Australia
- 🇩🇪 Germany
- 🇫🇷 France
- 🇦🇪 UAE
- 🇸🇬 Singapore
- 🇯🇵 Japan
- 🇨🇳 China
- 🇧🇷 Brazil
- 🇿🇦 South Africa
- 🇳🇬 Nigeria
- 🇵🇰 Pakistan
- 🇧🇩 Bangladesh
- 🇵🇭 Philippines
- 🇪🇺 European Union (Schengen)
- Plus 30+ more

**User Interface**
- Dark theme with violet/cyan/green color scheme
- Glassmorphism design elements
- Animated gradient backgrounds
- Responsive layout (desktop & mobile)
- Drag-and-drop file upload
- Side-by-side original/converted preview
- QR codes for desktop app downloads
- Status indicators and progress messages

**Configuration**
- Step-by-step setup wizard
- Pre-loaded country/document combinations
- Custom photo size input
- Optional Anthropic API key field
- API key visibility toggle
- Helpful hints and documentation links

**Export & Sharing**
- Download as JPEG (95% quality)
- Correct filename with spec (e.g., `snapid_passport_US_51x51mm.jpg`)
- Print sheet layout preview
- Download button appears after conversion
- Reset button to start over

**Technical**
- Single-file HTML application
- No build process required
- No external dependencies
- Canvas API for image processing
- Anthropic Messages API integration
- QRCode.js for QR generation (CDN)
- Browser-native fetch API
- CSS Grid & Flexbox responsive layout
- Space Grotesk + Inter typefaces

### Infrastructure

- GitHub repository with MIT license
- Vercel deployment configuration
- GitHub Actions CI/CD workflow
- Comprehensive documentation (README, DEPLOYMENT, CONTRIBUTING)
- Launch checklist for pre/post-launch tasks

### Documentation

- 📖 README.md — Full project overview
- 🚀 DEPLOYMENT.md — Step-by-step deployment guide
- ✅ LAUNCH_CHECKLIST.md — Pre-launch and post-launch tasks
- 🤝 CONTRIBUTING.md — Contribution guidelines
- 📝 CHANGELOG.md — This file

## [Unreleased] — Features in Development

### Planned

**Short Term (v1.1.0)**
- [ ] Batch processing (convert multiple photos at once)
- [ ] PDF print sheet template downloads
- [ ] Mobile app optimizations
- [ ] More language support (French, Spanish, German, Chinese)
- [ ] Keyboard shortcuts for power users

**Medium Term (v1.2.0)**
- [ ] Backend API for integrations
- [ ] Google Drive integration
- [ ] Dropbox integration
- [ ] Automated photo quality checking
- [ ] Face detection confidence indicators
- [ ] Custom background color option

**Long Term (v2.0.0)**
- [ ] Desktop apps (Windows, macOS, Linux)
- [ ] Batch processing with progress tracking
- [ ] Advanced image filters (blur detection, lighting fixes)
- [ ] White-label solution for businesses
- [ ] Team accounts with shared specs
- [ ] Webhook support for automated workflows
- [ ] Enterprise API with rate limiting

### Known Issues

- None yet (v1.0.0 is stable)

### Deprecations

None

---

## Version History

| Version | Date | Status | Download |
|---------|------|--------|----------|
| 1.0.0 | 2026-06-29 | ✅ Live | [snapid.app](https://snapid.app) |

---

## How to Upgrade

Since SnapID Studio is a web app, updates are automatic. Your browser always loads the latest version.

For desktop apps, download the latest version from the website.

---

## Reporting Issues

Found a bug? Report it on [GitHub Issues](https://github.com/yourusername/snapid-studio/issues)

Include:
- What you were doing
- What happened
- What should have happened
- Browser and OS
- Screenshots if helpful

---

## Contributing

Want to help? See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

We welcome:
- Bug reports
- Feature requests
- Pull requests
- Documentation improvements
- Translations

---

## Credits

**Built by:** [Your Name/Team]

**Technologies:**
- [Anthropic Claude](https://anthropic.com) — Vision AI
- [Canvas API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API) — Image processing
- [QRCode.js](https://davidsharp.github.io/QRCode.js/) — QR code generation
- [Vercel](https://vercel.com) — Hosting & deployment

**Inspired by:**
- Government photo requirements worldwide
- User frustration with photo shops and apps

---

## License

MIT License — See [LICENSE](LICENSE) for full text.

---

## Support

- 📧 Email: support@snapid.app (coming soon)
- 🐦 Twitter: [@snapid_studio](https://twitter.com/snapid_studio) (coming soon)
- 💬 GitHub Discussions: [Discussions](https://github.com/yourusername/snapid-studio/discussions)
- 🐛 Bug Reports: [Issues](https://github.com/yourusername/snapid-studio/issues)

---

**Last Updated:** June 29, 2026
