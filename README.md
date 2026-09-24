<div align="center">

# 🅃🄲 Gujarati Fonts

### *Handcrafted Gujarati typefaces for designers, developers & creators*

![Fonts](https://img.shields.io/badge/Fonts-11-b8390e?style=for-the-badge)
![Format](https://img.shields.io/badge/Format-OTF-1a1a1a?style=for-the-badge)
![License](https://img.shields.io/badge/License-Personal%20Use-6b5b45?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Cross--Platform-2d7d5a?style=for-the-badge)

![All Fonts Preview](samples/all-fonts.png)

</div>

---

## 📖 About

**TC Gujarati Fonts** ek carefully curated collection chhe **11 beautiful Gujarati typefaces** ni — designers, publishers, video editors ane app developers mate. Har font unique personality dharaave chhe — devotional calligraphy thi le ne modern display styles sudhi.

---

## 📑 Table of Contents

- [Font Gallery](#-font-gallery)
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

## 💾 Installation

<details>
<summary><strong>🪟 Windows</strong></summary>

1. `fonts/` folder open karo
2. Badha `.otf` files select karo (`Ctrl + A`)
3. Right-click → **Install** (badha users mate: **Install for all users**)

Ke pachi manually copy karo `C:\Windows\Fonts\` ma.
</details>

<details>
<summary><strong>🍎 macOS</strong></summary>

1. `.otf` files par double-click karo
2. **Font Book** khulshe → **Install Font** button dabao

Ke pachi drag-drop `~/Library/Fonts/` ma.
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

`pubspec.yaml`:

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

Widget ma:

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
// Assets Android/iOS folders ma link karo, pachi:
<Text style={{ fontFamily: 'Bhakti', fontSize: 32 }}>
  ગુજરાતી અક્ષર
</Text>
```
</details>

---

## 🚀 Usage

Live preview joyva mate — local server chalavo:

```bash
python -m http.server 8765
```

Pachi browser ma kholo: [http://localhost:8765/samples/preview.html](http://localhost:8765/samples/preview.html)

---

## 📋 Font Details

| Font | Style | Best For |
|------|-------|----------|
| Bhakti | Devotional / Calligraphic | Religious content, invitations, spiritual posts |
| Dhanush Vadodara | Bold Display | Headlines, banners, thumbnails |
| Dhanush Vadodara Dark | Extra Bold Display | High-impact titles, video thumbnails |
| Kala | Artistic Serif | Cultural content, art projects |
| Kalarav | Playful Script | Kids content, casual designs |
| Patrika | Editorial / News | Magazines, newspapers, articles |
| Sahitya | Literary Serif | Books, poetry, long-form reading |
| Shankar 1 | Traditional Bold | Ceremonial content, temples, events |
| Shlock | Decorative | Quotes, shayari, social posts |
| Sundar | Ornamental Bold | Wedding cards, festive designs |
| Tejas | Modern Bold | UI, apps, contemporary branding |

---

## 📁 Repository Structure

```
TC Gujarati Fonts/
├── fonts/                   # Font source files (.otf)
│   ├── Bhakti.otf
│   ├── Dhanush Vadodara.otf
│   └── ... (11 fonts total)
├── samples/                 # Previews & samples
│   ├── all-fonts.png        # Combined preview image
│   ├── preview.html         # Interactive web preview
│   ├── single.html          # Single-font preview page
│   └── individual/          # Per-font preview PNGs
├── docs/                    # Documentation
├── README.md
└── .gitignore
```

---

## 📜 License

Aa collection ma badha fonts na respective owners/designers pase original copyrights chhe. Personal ane educational use mate free chhe. **Commercial use** pahela original font designers ni permission lo.

---

## 🤝 Contributing

Navi Gujarati fonts add karva chhe? Welcome!

1. Repo fork karo
2. `fonts/` folder ma tamaru font mukho
3. `samples/individual/<font-name>.png` ma preview add karo
4. README table update karo
5. Pull Request kholo

**Format:** `.otf` preferred, `.ttf` accepted. Font ne proper Gujarati Unicode support hovi joiye.

---

## 💌 Contact

**Maintainer:** Tejas Chandivakar
**Email:** tejaschandivakar@gmail.com

---

<div align="center">

**⭐ Aa repo useful lagyu? Star karo!**

*Made with ❤️ for the Gujarati design community*

</div>
