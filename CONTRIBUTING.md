# Contributing to SnapID Studio

Thank you for your interest in contributing! This document outlines guidelines and processes for contributing to SnapID Studio.

## Code of Conduct

We are committed to providing a welcoming and inclusive environment for all contributors. Please be respectful and constructive in all interactions.

## How to Contribute

### Report a Bug

1. **Search existing issues** — Check if someone already reported it
2. **Create an issue** — Use the bug report template
3. **Provide details:**
   - What browser/OS you're using
   - Steps to reproduce
   - Expected vs actual behavior
   - Screenshots if applicable

### Suggest an Enhancement

1. **Search discussions** — See if it's been discussed
2. **Open an issue** — Describe the feature clearly
3. **Explain the use case** — Why would this be useful?
4. **Examples** — Link to similar features in other apps

### Submit a Pull Request

#### Setup

```bash
# Fork the repository on GitHub, then:
git clone https://github.com/yourusername/snapid-studio.git
cd snapid-studio
```

#### Make Changes

1. **Create a branch** — `git checkout -b feature/your-feature-name`
2. **Edit files** — Only `index.html` contains code
3. **Test locally** — `python -m http.server 8000` then visit `http://localhost:8000`
4. **Keep it minimal** — One feature per PR

#### Submit PR

1. **Commit** — `git commit -m "Add: description of change"`
2. **Push** — `git push origin feature/your-feature-name`
3. **Create Pull Request** — Include description and testing notes
4. **Wait for review** — Maintainers will provide feedback

## Development Guide

### Project Structure

```
snapid-studio/
├── index.html          # Single-file app (all HTML, CSS, JS)
├── README.md           # Project documentation
├── LICENSE             # MIT license
├── DEPLOYMENT.md       # Deployment instructions
└── vercel.json         # Vercel config
```

### No Build Step Required

SnapID Studio is intentionally a **single-file, zero-dependency** application. There's no build process, bundler, or framework. This makes it:
- Easy to understand
- Fast to deploy
- Simple to self-host
- Lightweight to download

### Making Changes

**All code is in `index.html`** — one file containing:
- HTML structure (lines 1–200ish)
- CSS styling (lines 200–1000ish)
- JavaScript logic (lines 1000+)

**Before editing:**
1. Back up the file
2. Test locally in a browser
3. Use browser DevTools to debug

**Common changes:**
- **Add a country** — Find `PHOTO_SPECS` object, add entries
- **Change colors** — Edit CSS variables at `:root`
- **Update UI text** — Find the string, change it
- **Add a document type** — Expand `PHOTO_SPECS`

### Testing

**Local test:**
```bash
python -m http.server 8000
# Visit http://localhost:8000 in browser
```

**What to test:**
- Photo upload works (JPG, PNG, WEBP, BMP)
- Conversion with and without API key
- Preview shows correctly
- Download generates correct file
- Responsive on mobile
- Works in Chrome, Firefox, Safari

### API Integration

The app uses **Anthropic Claude 3.5 Sonnet** for AI-powered face detection.

**Important:** Direct browser-to-API calls require:
```javascript
headers: {
  'x-api-key': apiKey,
  'anthropic-dangerous-direct-browser-access': 'true'
}
```

This header is intentionally verbose — it signals that direct browser access is a security decision, not an accident.

## Areas We Need Help

### High Priority
- [ ] Add more country specifications (passport, visa, ID specs)
- [ ] Improve mobile UI/UX
- [ ] Add more document types
- [ ] Write tests for image processing logic

### Medium Priority
- [ ] Add keyboard shortcuts
- [ ] Implement batch processing UI
- [ ] Create print sheet templates (PDF)
- [ ] Add accessibility improvements (ARIA labels)

### Low Priority
- [ ] Performance optimizations
- [ ] CSS theme improvements
- [ ] Documentation translations
- [ ] SEO meta tags

## Pull Request Guidelines

### Before Submitting
- [ ] Code is tested locally
- [ ] No breaking changes
- [ ] File size isn't significantly increased
- [ ] Changes solve exactly one issue

### What We Look For
- ✅ Clear, descriptive commit messages
- ✅ Minimal, focused changes
- ✅ Proper testing
- ✅ No external dependencies added
- ✅ Follows existing code style

### What We Don't Accept
- ❌ Changes that break existing functionality
- ❌ Major external dependencies
- ❌ Changes requiring a build process
- ❌ Unrelated commits mixed together

## Documentation

Help improve docs:
- [ ] Fix typos in README
- [ ] Add screenshots/GIFs
- [ ] Improve API documentation
- [ ] Write deployment guides
- [ ] Translate to other languages

## Questions?

- **GitHub Issues** — For bugs and features
- **GitHub Discussions** — For questions and ideas
- **Email** — support@snapid.app (add later)

## Recognition

Contributors will be:
- Thanked in the README
- Listed in CONTRIBUTORS.md
- Credited in release notes

Thank you for helping make SnapID Studio better! 🙏

---

## License

By contributing, you agree that your contributions will be licensed under the MIT License.
