# PWA Icons

This directory contains PWA icons required for the app to be installable.

## Required Icons

| Icon | Size | Purpose | Status |
|------|------|---------|--------|
| icon-192x192.png | 192x192 | Android/iOS home screen | ⚠️ NEEDED |
| icon-512x512.png | 512x512 | Android/iOS splash screen | ⚠️ NEEDED |

## How to Create Icons

### Option 1: Use Online Tool

1. Go to https://realfavicongenerator.net/ or https://www.pwabuilder.com/imageGenerator
2. Upload a square logo (at least 512x512)
3. Download the generated icons
4. Place them in this directory as `icon-192x192.png` and `icon-512x512.png`

### Option 2: Use ImageMagick (CLI)

```bash
# If you have a source logo.png
magick convert logo.png -resize 192x192 icon-192x192.png
magick convert logo.png -resize 512x512 icon-512x512.png
```

### Option 3: Use Figma/Photoshop

1. Create a 512x512px canvas
2. Design your logo/icon
3. Export as PNG at 192x192 and 512x512 sizes

## Icon Design Guidelines

- **Background**: Use `#3b82f6` (blue accent color) or transparent
- **Foreground**: White or dark text/icon
- **Style**: Simple, clean, recognizable at small sizes
- **Padding**: Include safe margins (20% on all sides)
- **Format**: PNG with transparency (optional)

## Temporary Solution

For testing purposes, you can copy the favicon.ico:

```bash
# This is NOT recommended for production
# Only for initial PWA testing
cp public/favicon.ico src/assets/icons/icon-192x192.png
cp public/favicon.ico src/assets/icons/icon-512x512.png
```

**⚠️ WARNING**: Using favicon.ico as PNG icons will work but will look poor. Create proper PNG icons before production deployment.

## Verification

After creating icons, verify:

1. Build the app: `npm run build`
2. Check dist/STASKK/assets/icons/ contains both icons
3. Test in Chrome DevTools → Application → Manifest
4. Install on mobile device to verify icon appearance

---

**Current Status**: Icons needed - see above for creation options
