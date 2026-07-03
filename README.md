# SnapID Studio

**AI-Powered Document Photo Resizing & Optimization**

Convert any portrait into a print-ready official document photo in seconds. SnapID Studio uses Claude's vision AI to analyze, crop, and resize photos to meet government specifications for 50+ countries.

**[🚀 Launch App](https://snapid.app)** | **[📱 Download Desktop](https://snapid.app#download)** | **[🔑 Get API Key](https://console.anthropic.com)**

---

## Features

✨ **AI-Guided Cropping** — Claude vision detects face position, centers it perfectly, and adjusts brightness  
🌍 **50+ Countries** — Pre-loaded specs for US, UK, India, EU, UAE, Singapore, Japan, and more  
📄 **9+ Document Types** — Passport, visa, national ID, driver's license, work permits, student IDs, and custom sizes  
🖨️ **Print-Ready Output** — 300 DPI at exact mm dimensions with print-sheet preview  
🔒 **100% Private** — All processing happens in your browser; no photos uploaded to any server  
⚡ **No Login Required** — Provide your own Anthropic API key; instant results  
💰 **Free to Use** — No subscription; you only pay for the Claude API calls you make  

---

## Quick Start

### Online
Visit **[snapid.app](https://snapid.app)** and:
1. Upload a portrait photo (JPG, PNG, WEBP, BMP)
2. Select document type and country
3. Click "Convert Photo"
4. Download print-ready image

### Desktop
Download the native app for macOS or Windows from the website for offline use and batch processing.

---

## How It Works

```
Your Photo (Browser)
    ↓
Claude Vision Analysis (Optional — with API key)
    ├─ Detects face position
    ├─ Measures brightness & contrast
    └─ Optimizes for spec requirements
    ↓
Smart Crop Engine
    ├─ Centers face in frame
    ├─ Adjusts to exact document ratio
    └─ Applies white background
    ↓
Resize to DPI & Dimensions
    ├─ 300 DPI for print quality
    ├─ Exact mm size (e.g., 35×45mm for passports)
    └─ JPEG export
    ↓
Your Download ✓
```

**Key Point:** Without an API key, the app uses smart center-crop — still produces professional results. With a key, Claude enhances it with AI analysis.

---

## API Requirements

### Get an Anthropic API Key (Free)
1. Visit [console.anthropic.com](https://console.anthropic.com)
2. Sign up or log in
3. Go to **API Keys** → **Create Key**
4. Copy the key (starts with `sk-ant-`)
5. Paste into SnapID Studio

### Free Tier
- $5 free credit per month for API usage
- Claude 3.5 Sonnet: ~$3 per 1M input tokens, ~$15 per 1M output tokens
- Typical photo analysis: ~0.01¢ per conversion

### Optional
The app works **without** an API key using built-in smart crop — ideal for quick testing.

---

## Supported Document Types & Countries

### Document Types
- **Travel:** Passport, Visa, Travel Documents
- **Identity:** National ID, Driver's License, Residence Permit
- **Employment/Study:** Work Permit, Student ID, Employment Pass
- **Custom:** Any size you specify

### Countries (50+)
🇺🇸 US · 🇬🇧 UK · 🇮🇳 India · 🇨🇦 Canada · 🇦🇺 Australia · 🇩🇪 Germany · 🇫🇷 France · 🇦🇪 UAE · 🇸🇬 Singapore · 🇯🇵 Japan · 🇨🇳 China · 🇧🇷 Brazil · 🇿🇦 South Africa · 🇳🇬 Nigeria · 🇵🇰 Pakistan · 🇧🇩 Bangladesh · 🇵🇭 Philippines · 🇪🇺 EU (Schengen)

---

## Deployment

### Self-Host (Recommended for First Launch)

#### Vercel (Free, Recommended)
```bash
git push origin main
# Visit vercel.com, connect GitHub, auto-deploy
```

#### GitHub Pages
```bash
# Repo name: yourusername.github.io
git push origin main
# Live at yourusername.github.io
```

#### Netlify / Cloudflare Pages
Similar setup — connect GitHub repo, auto-deploy on push.

### Custom Domain
Point your domain DNS to your hosting provider and set it in their dashboard.

---

## Development

### Local Testing
```bash
# Clone this repo
git clone https://github.com/yourusername/snapid-studio.git
cd snapid-studio

# Open in browser (no build step needed)
open index.html
# or
python -m http.server 8000
# Visit http://localhost:8000
```

### File Structure
```
snapid-studio/
├── index.html          # Single-file app (all HTML, CSS, JS)
├── README.md           # This file
├── LICENSE             # MIT license
└── .gitignore          # Git ignore rules
```

### Tech Stack
- **Frontend:** Vanilla HTML5 + CSS3 + JavaScript
- **Image Processing:** Canvas API (browser-native)
- **AI Backend:** Anthropic Claude 3.5 Sonnet (via API)
- **No build tools, no dependencies, no backend server**

---

## Privacy & Security

✅ **Your photos stay private:**
- All image processing happens in your browser
- Photos are never sent to SnapID servers
- Only your optional Anthropic API key connects to Claude
- No cookies, no tracking, no logins

✅ **Your API key is secure:**
- Stored only in your browser's memory (not saved)
- Never transmitted to SnapID infrastructure
- You control the key — add spending limits in Anthropic console

✅ **GDPR & Compliance:**
- No personal data collection
- No analytics on your photos
- You maintain 100% control

---

## Troubleshooting

### "API Error" or "Cannot reach Claude"
- Verify your API key is correct
- Check Anthropic console for spending limits
- Ensure your network allows CORS requests to api.anthropic.com
- Try without API key (uses smart auto-crop fallback)

### Photo quality is off
- Use good lighting and clear face visibility
- Try a photo taken head-on (not angled)
- Ensure face fills at least 50% of the frame
- With API key, Claude will optimize; without, auto-crop is applied

### Download doesn't work
- Check your browser's download settings
- Ensure JavaScript is enabled
- Try a different browser
- Clear browser cache and reload

---

## Roadmap

### Short Term (0–1 month)
- [ ] Batch processing (upload multiple photos)
- [ ] Print template downloads (PDF for various sheet sizes)
- [ ] Mobile-optimized UI
- [ ] Download history / recent specs

### Medium Term (1–3 months)
- [ ] Backend API for integrations
- [ ] Zapier / Make.com automation
- [ ] Google Drive / Dropbox integration
- [ ] More countries & document types

### Long Term (3–6 months)
- [ ] Webhook support for automated workflows
- [ ] Enterprise API with rate limits
- [ ] Team accounts with shared specs
- [ ] iOS & Android native apps

---

## Contributing

Contributions welcome! Areas where help is needed:
- Adding more country/document specifications
- UI/UX improvements
- Bug fixes and performance tweaks
- Documentation and translations

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## License

MIT License — free to use, modify, and distribute. See [LICENSE](LICENSE) file.

---

## Support

- 🆘 **Issues:** [GitHub Issues](https://github.com/yourusername/snapid-studio/issues)
- 💬 **Discussions:** [GitHub Discussions](https://github.com/yourusername/snapid-studio/discussions)
- 📧 **Email:** support@snapid.app (add this later)
- 🐦 **Twitter:** [@snapid_studio](https://twitter.com/snapid_studio) (add this later)

---

## Disclaimer

SnapID Studio helps prepare document photos, but **you are responsible for verifying current requirements** with the issuing authority (passport office, visa center, etc.). Photo specifications change and vary by region. Always check official requirements before submitting official photos.

---

## Built With

- **Claude 3.5 Sonnet** (Anthropic) — AI vision & analysis
- **HTML5 Canvas** — Image processing
- **Vanilla JavaScript** — No frameworks, pure JS
- **CSS3 Grid/Flexbox** — Responsive layout
- **QRCode.js** — QR code generation for downloads

---

**Made by [Your Name/Team]** | [Website](https://yoursite.com) | [Twitter](https://twitter.com/yourhandle)

---

**Last Updated:** June 2026 | v1.0.0
