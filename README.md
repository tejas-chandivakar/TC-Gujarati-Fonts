<div align="center">

<img src="assets/logo.png" alt="TC Logo" width="120" />

# TC Gujarati Fonts

### *Gujarati typefaces for designers, developers & creators*

![Fonts](https://img.shields.io/badge/Fonts-11-b8390e?style=for-the-badge)
![Format](https://img.shields.io/badge/Format-OTF-1a1a1a?style=for-the-badge)
![License](https://img.shields.io/badge/License-Personal%20Use-6b5b45?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Cross--Platform-2d7d5a?style=for-the-badge)

![All Fonts Preview](samples/all-fonts.png)

</div>

---

## 📖 About

**TC Gujarati Fonts** is a carefully curated collection of **11 beautiful Gujarati typefaces** for designers, publishers, video editors, and app developers. Each font brings its own personality — from devotional calligraphy to modern display styles — perfect for headlines, posters, invitations, thumbnails, and festive layouts.

> ✨ **Now with full long-text support!** The repo also bundles **Noto Sans Gujarati** (SIL OFL, Google Fonts) as a companion body font, so you can pair a decorative display font with a fully Unicode-shaping body font for paragraphs, articles, and books. See [Long Text Support](#-long-text-support).

---

## 📑 Table of Contents

- [Font Gallery](#-font-gallery)
- [Long Text Support](#-long-text-support)
- [Compatibility & Limitations](#-compatibility--limitations)
- [Installation](#-installation)
- [Usage](#-usage)
- [Font Details](#-font-details)
- [Repository Structure](#-repository-structure)
- [License](#-license)
- [Contributing](#-contributing)

---

## 🎨 Font Gallery

| # | Font | Preview |
|---|------|---------|
| 1 | **Bhakti** | ![Bhakti](samples/individual/bhakti.png) |
| 2 | **Dhanush Vadodara** | ![Dhanush Vadodara](samples/individual/dhanush-vadodara.png) |
| 3 | **Dhanush Vadodara Dark** | ![Dhanush Vadodara Dark](samples/individual/dhanush-vadodara-dark.png) |
| 4 | **Kala** | ![Kala](samples/individual/kala.png) |
| 5 | **Kalarav** | ![Kalarav](samples/individual/kalarav.png) |
| 6 | **Patrika** | ![Patrika](samples/individual/patrika.png) |
| 7 | **Sahitya** | ![Sahitya](samples/individual/sahitya.png) |
| 8 | **Shankar 1** | ![Shankar](samples/individual/shankar-1.png) |
| 9 | **Shlock** | ![Shlock](samples/individual/shlock.png) |
| 10 | **Sundar** | ![Sundar](samples/individual/sundar.png) |
| 11 | **Tejas** | ![Tejas](samples/individual/tejas.png) |

---

## 📝 Long Text Support

The display fonts in `fonts/` are optimized for short headings and posters. For **paragraphs, articles, and books**, this repo bundles the **Noto Sans Gujarati** family (Regular, Medium, Bold) — Google's professionally engineered Gujarati font with full Unicode coverage, proper OpenType Indic shaping, and support for all complex conjuncts (`ક્ષ`, `જ્ઞ`, `ત્ર`, `ર્ક`, `સ્ત્ર`, etc.).

Bundled body fonts live in [`fonts/body/`](fonts/body/):

- `NotoSansGujarati-Regular.ttf`
- `NotoSansGujarati-Medium.ttf`
- `NotoSansGujarati-Bold.ttf`
- `OFL.txt` (SIL Open Font License)

### ✨ Recommended Pairing Pattern

Use a **display font for headings** and **Noto for body text**. The result:

![Long Text Preview](samples/long-text-preview.png)

> 🎯 Live demo: open `samples/long-text.html` after starting the local server.

### 🎨 Ready-to-use Font Stacks

<details open>
<summary><strong>CSS</strong></summary>

```css
@font-face {
  font-family: 'Bhakti';
  src: url('fonts/Bhakti.otf') format('opentype');
}
@font-face {
  font-family: 'Noto Sans Gujarati';
  src: url('fonts/body/NotoSansGujarati-Regular.ttf') format('truetype');
  font-weight: 400;
}
@font-face {
  font-family: 'Noto Sans Gujarati';
  src: url('fonts/body/NotoSansGujarati-Bold.ttf') format('truetype');
  font-weight: 700;
}

h1, h2 { font-family: 'Bhakti', 'Noto Sans Gujarati', sans-serif; }
p, li  { font-family: 'Noto Sans Gujarati', system-ui, sans-serif;
         line-height: 1.75; font-size: 17px; }
```
</details>

<details>
<summary><strong>Flutter</strong></summary>

```yaml
# pubspec.yaml
flutter:
  fonts:
    - family: Bhakti
      fonts:
        - asset: assets/fonts/Bhakti.otf
    - family: NotoSansGujarati
      fonts:
        - asset: assets/fonts/body/NotoSansGujarati-Regular.ttf
        - asset: assets/fonts/body/NotoSansGujarati-Bold.ttf
          weight: 700
```

```dart
// Headline uses display font, body uses Noto
Text('શ્રી ગણેશાય નમઃ',
  style: TextStyle(fontFamily: 'Bhakti', fontSize: 36)),
Text('ગુજરાતી ભાષા વિશ્વની સૌથી પ્રાચીન ભાષાઓમાંની એક છે...',
  style: TextStyle(fontFamily: 'NotoSansGujarati', fontSize: 16, height: 1.7)),
```
</details>

<details>
<summary><strong>Microsoft Word / Google Docs</strong></summary>

1. Install both the display font (e.g. `Bhakti.otf`) and `NotoSansGujarati-Regular.ttf`
2. Apply the display font to your **Heading 1** / **Heading 2** styles
3. Apply **Noto Sans Gujarati** to your **Normal / Body** style
4. Write long paragraphs — all conjuncts and matras render correctly
</details>

### 🧩 Which display font pairs best with body Noto?

| Body font | Recommended display pairing | Vibe |
|-----------|-----------------------------|------|
| Noto Sans Gujarati | **Bhakti** | Religious, devotional |
| Noto Sans Gujarati | **Sundar** | Wedding, festive |
| Noto Sans Gujarati | **Patrika** | News, editorial, magazine |
| Noto Sans Gujarati | **Tejas** | Modern apps, tech blogs |
| Noto Sans Gujarati | **Shankar 1** | Traditional, ceremonial |

---

## ⚠️ Compatibility & Limitations

Before installing, please understand what these fonts can and cannot do.

### 📊 Font Encoding Summary

| Type | Fonts | What it means |
|------|-------|---------------|
| ✅ **Unicode-mapped** | 10 fonts — Bhakti, Dhanush Vadodara, Dhanush Vadodara Dark, Kala, Patrika, Sahitya, Shankar 1, Shlock, Sundar, Tejas | Direct Gujarati Unicode text (`ગુજરાતી`) renders correctly in Word, browsers, apps, and design tools |
| ⚠️ **Legacy ASCII-only** | **Kalarav** | Contains **no Gujarati Unicode glyphs**. You must type English letters using a legacy keyboard mapping to produce Gujarati output. Pasting Unicode Gujarati will show blanks or fallback font |

### 🖥️ Platform Compatibility

| Platform | Installation | Rendering | Notes |
|----------|--------------|-----------|-------|
| **Windows** 10/11 | ✅ Works | ✅ Works in Word, PowerPoint, browsers, Photoshop | Best supported |
| **macOS** | ✅ Works | ✅ Works via Font Book | Fully supported |
| **Linux** | ✅ Works | ✅ Works | Requires modern HarfBuzz / libraqm (present on most 2020+ distros) |
| **Web / CSS** | ✅ `@font-face` | ✅ Works | Verified — see `samples/preview.html` |
| **Android / iOS apps** | ✅ Works | ✅ Works | Recommended for display text only |
| **Flutter** | ✅ Works | ✅ Works | Use for headings and titles, not paragraphs |

### 🚫 Known Limitations

These are **display / decorative fonts**, not general-purpose text fonts. Please note:

1. **Limited character set** — each font contains only ~76 basic Gujarati Unicode characters (consonants, vowels, digits). Rare characters may fall back to the system font.
2. **Complex conjuncts may not shape correctly** — characters like `ક્ષ`, `જ્ઞ`, half-letters (`ર્ક`), and stacked matras rely on OpenType Indic shaping (GSUB / GPOS tables). These fonts have limited shaping support.
3. **Best used for:**
   - Headlines, titles, banners
   - Wedding cards, invitations, festival posters
   - YouTube thumbnails, social media graphics
   - Logos and short display text
4. **Not recommended for:**
   - Long body text (articles, books, ebooks)
   - Legal or official documents requiring perfect script rendering
   - Screen readers / accessibility-critical contexts
5. **For long-form Gujarati content**, use the bundled **Noto Sans Gujarati** in [`fonts/body/`](fonts/body/) — see [Long Text Support](#-long-text-support). Alternatives: Shruti, Lohit Gujarati, Rasa (all free).

### 🎹 Special Note on Kalarav (Legacy Font)

Kalarav uses **ASCII-based glyph mapping** (a common convention for older Indian fonts). To type Gujarati with it:

- Install a legacy Gujarati keyboard layout (e.g. **Shree-Lipi**, **Terafont**, or a custom .klc keyboard file)
- Type English letters — the font maps them to Gujarati glyphs visually
- Copy-pasting the visible "Gujarati" text elsewhere without the font will appear as garbled English

If you need Kalarav-style output as real Gujarati Unicode, you'll need a converter tool.

---

## 💾 Installation

<details>
<summary><strong>🪟 Windows</strong></summary>

1. Open the `fonts/` folder
2. Select all `.otf` files (`Ctrl + A`)
3. Right-click → **Install** (or **Install for all users** for system-wide access)

Alternatively, copy the files manually into `C:\Windows\Fonts\`.
</details>

<details>
<summary><strong>🍎 macOS</strong></summary>

1. Double-click any `.otf` file
2. **Font Book** will open → click **Install Font**

Or drag them into `~/Library/Fonts/`.
</details>

<details>
<summary><strong>🐧 Linux</strong></summary>

```bash
mkdir -p ~/.fonts
cp fonts/*.otf ~/.fonts/
fc-cache -fv
```
</details>

<details>
<summary><strong>🌐 Web (CSS)</strong></summary>

```css
@font-face {
  font-family: 'Bhakti';
  src: url('fonts/Bhakti.otf') format('opentype');
  font-display: swap;
}

.gujarati-heading {
  font-family: 'Bhakti', serif;
  font-size: 48px;
}
```
</details>

<details>
<summary><strong>📱 Flutter</strong></summary>

Add to your `pubspec.yaml`:

```yaml
flutter:
  fonts:
    - family: Bhakti
      fonts:
        - asset: assets/fonts/Bhakti.otf
    - family: Tejas
      fonts:
        - asset: assets/fonts/Tejas.otf
```

Use in a widget:

```dart
Text(
  'ગુજરાતી અક્ષર',
  style: TextStyle(fontFamily: 'Bhakti', fontSize: 32),
)
```
</details>

<details>
<summary><strong>📱 React Native</strong></summary>

```js
// Link the assets under Android/iOS folders, then use:
<Text style={{ fontFamily: 'Bhakti', fontSize: 32 }}>
  ગુજરાતી અક્ષર
</Text>
```
</details>

---

## 🚀 Usage

To view live previews locally, start a simple HTTP server:

```bash
python -m http.server 8765
```

Then open in your browser: [http://localhost:8765/samples/preview.html](http://localhost:8765/samples/preview.html)

---

## 📋 Font Details

| Font | Encoding | Style | Best For |
|------|----------|-------|----------|
| Bhakti | Unicode | Devotional / Calligraphic | Religious posters, invitations |
| Dhanush Vadodara | Unicode | Bold Display | Headlines, banners, thumbnails |
| Dhanush Vadodara Dark | Unicode | Extra Bold Display | High-impact titles, video thumbnails |
| Kala | Unicode | Artistic Serif | Cultural posters, art projects |
| Kalarav | ⚠️ Legacy ASCII | Playful Script | Casual designs (requires legacy keyboard) |
| Patrika | Unicode | Editorial Display | Magazine headlines, article titles |
| Sahitya | Unicode | Literary Serif | Book covers, poetry titles |
| Shankar 1 | Unicode | Traditional Bold | Ceremonial content, temples, events |
| Shlock | Unicode | Decorative | Quotes, shayari, social posts |
| Sundar | Unicode | Ornamental Bold | Wedding cards, festive designs |
| Tejas | Unicode | Modern Bold | UI headings, app branding |

> All 11 display fonts above are intended for **short display text** (titles, headings, posters). For long-form Gujarati body text, use the bundled **Noto Sans Gujarati** in [`fonts/body/`](fonts/body/) — see [Long Text Support](#-long-text-support).

---

## 📁 Repository Structure

```
TC Gujarati Fonts/
├── fonts/
│   ├── *.otf                # 11 display fonts (Bhakti, Sundar, Tejas, ...)
│   └── body/                # Body font for long text (SIL OFL)
│       ├── NotoSansGujarati-Regular.ttf
│       ├── NotoSansGujarati-Medium.ttf
│       ├── NotoSansGujarati-Bold.ttf
│       └── OFL.txt
├── samples/
│   ├── all-fonts.png        # Combined display-font preview
│   ├── long-text-preview.png# Display + body pairing demo
│   ├── preview.html         # Interactive gallery
│   ├── long-text.html       # Long-text pairing demo
│   ├── single.html          # Single-font preview page
│   └── individual/          # Per-font preview PNGs
├── docs/
├── README.md
└── .gitignore
```

---

## 📜 License

- **Display fonts** (in `fonts/`): retain the original copyrights of their respective owners and designers. Free for personal and educational use. For **commercial use**, please obtain permission from the original designers.
- **Noto Sans Gujarati** (in `fonts/body/`): licensed under the **SIL Open Font License 1.1** — free for personal and commercial use. Full license text is bundled in `fonts/body/OFL.txt`.

---

## 🤝 Contributing

Have a Gujarati font you'd like to add? Contributions are welcome!

1. Fork the repository
2. Add your font file to the `fonts/` folder
3. Add a preview image to `samples/individual/<font-name>.png`
4. Update the gallery table in the README
5. Open a Pull Request

**Format:** `.otf` preferred, `.ttf` also accepted. The font must support proper Gujarati Unicode characters.

---

## 💌 Contact

**Maintainer:** Tejas Chandivakar
**Email:** tejaschandivakar@gmail.com
**GitHub:** [@tejas-chandivakar](https://github.com/tejas-chandivakar)

---

<div align="center">

**⭐ Found this useful? Please star the repo!**

*Made with ❤️ for the Gujarati design community*

</div>
