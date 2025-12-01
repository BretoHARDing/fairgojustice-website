# 📸 Media Upload Guide - Fair Go Justice

## 🎵 Your Aussie Hip Hop Tracks

Your AI-assisted Aussie hip hop tracks are a powerful asset for the movement! Here's how to add them:

### Music File Structure

```
media/
└── music/
    ├── fair-go-anthem.mp3        # Featured track
    ├── system-breakdown.mp3      # Track 1
    ├── voice-of-the-people.mp3   # Track 2
    ├── scales-of-truth.mp3       # Track 3
    ├── stand-together.mp3        # Track 4
    ├── parliament-steps.mp3      # Track 5
    └── hope-rising.mp3           # Track 6
```

### How to Upload Music

1. **Prepare your files:**
   - Format: MP3 (recommended) or WAV
   - Bitrate: 192kbps or higher for quality
   - File size: Keep under 10MB per track for web

2. **Rename files** to match the placeholders in `music.html`:
   - Use lowercase, hyphens instead of spaces
   - Example: `Fair Go Anthem.mp3` → `fair-go-anthem.mp3`

3. **Upload to repository:**
   ```bash
   cd media/music/
   # Copy your files here
   git add .
   git commit -m "Add Aussie hip hop tracks"
   git push
   ```

4. **Update track info** in `music.html`:
   - Change track titles to your actual song names
   - Update descriptions
   - Add your artist/producer credits

---

## 📷 Your Images

### Image Folder Structure

```
images/
├── hero/           # Homepage hero images
│   ├── hero-main.jpg
│   ├── hero-mobile.jpg
│   └── hero-overlay.png
│
├── stories/        # Story submission photos
│   ├── story-1.jpg
│   ├── story-2.jpg
│   └── story-3.jpg
│
├── team/           # Team/founder photos
│   ├── founder.jpg
│   └── team-group.jpg
│
├── icons/          # UI icons and logos
│   ├── logo.svg
│   ├── logo-white.svg
│   ├── favicon.ico
│   └── pillar-icons/
│
├── social/         # Social media share images
│   ├── og-image.jpg        # 1200x630px
│   ├── twitter-card.jpg    # 1200x600px
│   └── music-share.jpg
│
├── graphics/       # Campaign graphics
│   ├── petition-badge.png
│   ├── signature-counter.png
│   └── infographics/
│
└── music/          # Album artwork
    ├── featured-track.jpg
    ├── track-1.jpg
    └── track-2.jpg
```

### Image Specifications

| Type | Size | Format | Notes |
|------|------|--------|-------|
| Hero (Desktop) | 1920x1080px | JPG/WebP | Compress to <500KB |
| Hero (Mobile) | 768x1024px | JPG/WebP | Portrait orientation |
| Story Photos | 800x600px | JPG | Compress to <200KB |
| Social Share (OG) | 1200x630px | JPG | Facebook/LinkedIn |
| Twitter Card | 1200x600px | JPG | Twitter/X |
| Album Artwork | 500x500px | JPG/PNG | Square format |
| Logo (Full) | 400x100px | SVG/PNG | Transparent BG |
| Favicon | 32x32px, 180x180px | ICO/PNG | Multiple sizes |

### How to Optimize Images

**Quick optimization:**
```bash
# Using ImageMagick (install: brew install imagemagick)
convert input.jpg -resize 1200x630 -quality 85 output.jpg

# Using squoosh-cli
npx @aspect/squoosh-cli input.jpg -d output/ --webp
```

**Online tools:**
- [Squoosh.app](https://squoosh.app) - Best for web images
- [TinyPNG](https://tinypng.com) - Batch compression
- [Canva](https://canva.com) - Resize and edit

---

## 🎨 Adding Images to Pages

### Homepage Hero

Edit `index.html`:
```html
<!-- Replace the placeholder -->
<section class="hero" style="background-image: url('images/hero/hero-main.jpg');">
```

### Story Cards

Edit `stories.html` or `index.html`:
```html
<div class="story-card">
    <img src="images/stories/story-1.jpg" alt="John's story about justice reform">
    <!-- ... -->
</div>
```

### Music Artwork

Edit `music.html`:
```html
<div class="track-artwork">
    <img src="images/music/track-1.jpg" alt="System Breakdown Album Art">
    <!-- Remove the placeholder icon -->
</div>
```

---

## 🎵 Adding Music to the Player

### Single Track

```html
<audio controls>
    <source src="media/music/your-track.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
</audio>
```

### With Multiple Formats (best compatibility)

```html
<audio controls>
    <source src="media/music/your-track.mp3" type="audio/mpeg">
    <source src="media/music/your-track.ogg" type="audio/ogg">
    <source src="media/music/your-track.wav" type="audio/wav">
    Your browser does not support the audio element.
</audio>
```

---

## 📱 Social Media Sharing

### Open Graph Images

For best social sharing, add these meta tags to each page:

```html
<meta property="og:image" content="https://fairgojustice.org/images/social/og-image.jpg">
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="630">
```

### Twitter Cards

```html
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:image" content="https://fairgojustice.org/images/social/twitter-card.jpg">
```

---

## ✅ Upload Checklist

### Music Files
- [ ] Converted to MP3 format
- [ ] Compressed to reasonable size (<10MB each)
- [ ] Named using lowercase-with-hyphens.mp3
- [ ] Placed in `media/music/` folder
- [ ] Updated `music.html` with correct titles and descriptions
- [ ] Tested audio playback in browser

### Image Files
- [ ] Resized to correct dimensions
- [ ] Compressed for web (under 500KB for large images)
- [ ] Named descriptively (lowercase-with-hyphens.jpg)
- [ ] Placed in correct `/images/` subfolder
- [ ] Added alt text in HTML for accessibility
- [ ] Updated page HTML to reference new images

### After Upload
- [ ] Run `git add .` and `git commit -m "Add media files"`
- [ ] Push to repository
- [ ] Test on live site
- [ ] Check mobile display
- [ ] Verify social sharing previews

---

## 🎤 Music Credits Template

Add to your music page or about page:

```html
<section class="music-credits">
    <h3>Music Credits</h3>
    <p><strong>Production:</strong> AI-Assisted with [Your Directives]</p>
    <p><strong>Lyrics:</strong> Fair Go Justice Team</p>
    <p><strong>Vocals:</strong> [Artist Name]</p>
    <p><strong>Mix/Master:</strong> [Studio/Producer]</p>
    <p>© 2025 Fair Go Justice. Free for advocacy use.</p>
</section>
```

---

## 📞 Need Help?

If you have questions about uploading media:
- **Email:** bretharding69@gmail.com
- **GitHub Issues:** Open an issue in the repository

---

**Your images and music are powerful tools for the movement!** 🇦🇺✊🎵
