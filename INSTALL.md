# Installation & Usage Guide

Complete guide for installing and using SnapID Studio.

## Quick Start (30 seconds)

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/snapid-studio.git
cd snapid-studio

# 2. Start a local server
python -m http.server 8000

# 3. Open in browser
# Visit http://localhost:8000
```

Done! ✅

---

## System Requirements

### For Users
- ✅ Any modern web browser (Chrome, Firefox, Safari, Edge)
- ✅ 50 MB free disk space (for downloaded photos)
- ✅ Internet connection (optional if using auto-crop)

### For Developers
- ✅ Git (for version control)
- ✅ Python 3.x or Node.js (for local server)
- ✅ Text editor (VS Code, Sublime, etc.)
- ✅ Terminal/Command Prompt

---

## Installation Methods

### Method 1: Clone from GitHub (Recommended)

```bash
# Clone the repository
git clone https://github.com/yourusername/snapid-studio.git

# Navigate to directory
cd snapid-studio

# Start server (choose one)
python -m http.server 8000          # Python 3
python -m SimpleHTTPServer 8000      # Python 2
npx http-server                      # Node.js (if installed)

# Open http://localhost:8000 in browser
```

### Method 2: Download ZIP

1. Go to [GitHub](https://github.com/yourusername/snapid-studio)
2. Click **Code** → **Download ZIP**
3. Extract the ZIP file
4. Open `index.html` in browser

### Method 3: Fork & Deploy

1. Fork the repository on GitHub
2. Go to [Vercel](https://vercel.com)
3. Import your fork
4. Deploy (automatic)

---

## Configuration

### API Key Setup

#### Getting an API Key

1. Visit [console.anthropic.com](https://console.anthropic.com)
2. Sign up or log in
3. Go to **API Keys**
4. Click **Create Key**
5. Copy the key (starts with `sk-ant-`)

#### Using in SnapID Studio

1. Go to [snapid.app](https://snapid.app) or local version
2. Paste API key in the "Anthropic API Key" field
3. Click **Convert Photo**
4. Done! Claude will analyze your photo

#### Security Notes
- ✅ Key stays in your browser only
- ✅ Never sent to SnapID servers
- ✅ Safe to enter in the app
- ✅ Can be revoked anytime in Anthropic console

### Customization

#### Change Colors
Edit the CSS variables in `index.html`:

```css
:root{
  --bg:#06070d;           /* Dark background */
  --violet:#7c6af7;       /* Accent color */
  --cyan:#22d3ee;         /* Secondary color */
  --green:#34d399;        /* Success color */
  /* Change these to customize */
}
```

#### Add Countries
Find the `PHOTO_SPECS` object in `index.html`:

```javascript
passport:{
  US:[{
    id:'us_pp',
    name:'US Passport',
    dims:'51×51mm',
    w:51,
    h:51,
    dpi:300,
    note:'White or off-white background.'
  }],
  // Add your country here
}
```

#### Change UI Text
Search for text strings and update them:
- Hero section: "Perfect Document Photos in Seconds"
- Button labels: "Convert Photo", "Download"
- Placeholders: "Drop your photo here"

---

## Local Development

### File Structure

```
snapid-studio/
├── index.html              # Single-file app
├── README.md               # Documentation
├── DEPLOYMENT.md           # Deployment guide
├── CONTRIBUTING.md         # Contributing guidelines
├── CODE_OF_CONDUCT.md      # Community standards
├── SECURITY.md             # Security policy
├── PRIVACY.md              # Privacy policy
├── TERMS.md                # Terms of service
├── CHANGELOG.md            # Version history
├── LICENSE                 # MIT license
├── vercel.json             # Vercel config
├── .gitignore              # Git ignore rules
└── .github/                # GitHub configuration
    ├── workflows/
    │   └── test.yml        # CI/CD workflow
    ├── ISSUE_TEMPLATE/
    │   ├── bug_report.md
    │   └── feature_request.md
    └── pull_request_template.md
```

### Testing Locally

```bash
# Start server
python -m http.server 8000

# Open in browser
open http://localhost:8000    # macOS
start http://localhost:8000   # Windows
xdg-open http://localhost:8000 # Linux

# Test features
# 1. Upload a photo (JPG, PNG, WEBP, BMP)
# 2. Select document type and country
# 3. Click Convert Photo
# 4. Download and verify
```

### Browser DevTools

Press `F12` to open DevTools:

**Console Tab:**
- Check for errors
- Test JavaScript
- View API responses

**Network Tab:**
- Monitor API calls
- Check request/response
- Verify headers

**Elements Tab:**
- Inspect HTML
- Debug CSS
- Check classes

---

## Using the App

### Step 1: Upload Photo

1. Click upload zone or drag-drop
2. Select JPG, PNG, WEBP, or BMP
3. Photo appears in preview

### Step 2: Configure

1. Select **Document Type** (Passport, Visa, etc.)
2. Select **Country** (US, UK, India, etc.)
3. Select **Photo Size** (appears after country)
4. (Optional) Add API key for AI enhancement

### Step 3: Convert

1. Click **Convert Photo**
2. AI analyzes photo (if API key provided)
3. Photo is cropped and resized
4. Result appears in preview

### Step 4: Download

1. Click **Download Converted Photo**
2. File saves as `snapid_[type]_[country]_[size].jpg`
3. Print or submit as needed

---

## Features Explained

### AI-Guided Cropping (With API Key)

When you provide an API key:
- Claude detects your face
- Analyzes lighting and positioning
- Adjusts brightness if needed
- Centers face in frame
- Optimizes for document specs

**Result:** Professional-quality photos

### Smart Auto-Crop (Without API Key)

Without an API key:
- Center-crops the image
- Adjusts to document ratio
- Applies white background
- Resizes to 300 DPI

**Result:** Good enough for most uses

### Print Sheet Preview

Shows how many photos fit on 4×6" paper:
- Calculates photo grid
- Shows layout preview
- Tells you exact count
- Help with printing

### QR Codes

For desktop app downloads:
- Click "Scan QR code"
- Scan with phone
- Get download link
- Supports Windows & macOS

---

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl/Cmd + U` | Upload file |
| `Ctrl/Cmd + D` | Download result |
| `Ctrl/Cmd + R` | Reset/start over |
| `Escape` | Close QR panel |

*(Currently not implemented; planned for v1.1)*

---

## Troubleshooting

### Upload Won't Work

**Problem:** Can't upload photos  
**Solution:**
1. Check file format (JPG, PNG, WEBP, BMP only)
2. Verify file size (should be < 20 MB)
3. Try a different browser
4. Clear browser cache and reload

### Conversion Fails

**Problem:** Getting an error during conversion  
**Solution:**
1. Make sure document type and country are selected
2. Check API key is valid (if using AI)
3. Try without API key (auto-crop)
4. Check console (F12) for error message

### Downloaded File is Corrupted

**Problem:** Downloaded file won't open  
**Solution:**
1. Try downloading again
2. Use a different browser
3. Check file extension (.jpg)
4. Try opening with different app

### API Key Error

**Problem:** "API Error" or invalid key  
**Solution:**
1. Verify key starts with `sk-ant-`
2. Check it's copied completely (no extra spaces)
3. Confirm key is active in Anthropic console
4. Try creating a new key
5. Try without key (auto-crop works)

### Slow Performance

**Problem:** App is slow or laggy  
**Solution:**
1. Close other browser tabs
2. Restart browser
3. Try a different browser
4. Check internet connection
5. Reduce photo size (smaller file = faster)

---

## Advanced Usage

### Batch Processing (Planned)

*Coming in v1.1.0*

Convert multiple photos at once:
```
1. Upload folder of photos
2. Select document type
3. Auto-convert all
4. Download ZIP with all results
```

### Programmatic Usage (Future)

*Planned for v2.0.0*

```javascript
// Example API usage (not yet available)
const snapid = new SnapID({
  apiKey: 'your-api-key',
  documentType: 'passport',
  country: 'US'
});

snapid.convert(photoFile)
  .then(result => console.log(result.url));
```

### Integrations (Future)

*Coming in future versions*

- Google Drive integration
- Dropbox sync
- Slack integration
- Webhook support

---

## Performance Tips

### For Best Results

1. **Good lighting** — Clear, well-lit photos
2. **Face forward** — Look straight at camera
3. **Clear background** — Plain white or light background
4. **Center framed** — Face should fill most of frame
5. **Recent photo** — Within 6 months if official use

### Optimization

1. **Smaller photos** — Crop before uploading
2. **JPG format** — Smaller file size
3. **No glasses** — Some countries prohibit them
4. **Natural expression** — Slight smile or neutral

---

## Privacy & Security

### Your Photos
- ✅ Never stored on SnapID servers
- ✅ Never sent to SnapID servers
- ✅ Only sent to Claude if you provide API key
- ✅ Deleted from browser after download

### Your API Key
- ✅ Stays in your browser only
- ✅ Never sent to SnapID servers
- ✅ Only used for Claude API calls
- ✅ Can be revoked anytime

### Your Downloads
- ✅ Downloaded to your device
- ✅ You own the files
- ✅ Use however you like

---

## FAQ

**Q: Is this secure?**  
A: Yes. All processing happens in your browser. No data is stored or transmitted to SnapID servers.

**Q: Will photos be rejected?**  
A: Photos generated by SnapID Studio meet official specifications, but acceptance depends on the specific agency. Always verify current requirements.

**Q: Can I use it offline?**  
A: Yes, without API key. AI features require internet for Claude API calls.

**Q: How much does it cost?**  
A: Free! You only pay for Anthropic API calls if you use them (they provide a free tier).

**Q: Can I use for passport/visa applications?**  
A: Yes, as long as specifications are current. Verify with the official agency first.

**Q: How do I report bugs?**  
A: [GitHub Issues](https://github.com/yourusername/snapid-studio/issues)

**Q: How do I suggest features?**  
A: [GitHub Discussions](https://github.com/yourusername/snapid-studio/discussions)

---

## Support

### Getting Help

- 📖 **Documentation:** README.md
- 🐛 **Bug Reports:** GitHub Issues
- 💬 **Discussions:** GitHub Discussions
- 🤝 **Contributing:** CONTRIBUTING.md
- 🔒 **Security:** SECURITY.md

### Contact

Email: **support@snapid.app** (placeholder)

Response time: 24-48 hours

---

## Next Steps

- [ ] Upload your first photo
- [ ] Get an Anthropic API key
- [ ] Try with and without AI
- [ ] Download your result
- [ ] Share feedback
- [ ] Contribute improvements

---

**Happy converting! 📸**

*For more, see README.md and other documentation files.*
