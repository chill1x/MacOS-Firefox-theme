# 🎨 MacOS Firefox Theme

🇬🇧 English | **[🇷🇺 Русский](README.md)**

---

Minimalist Firefox theme with macOS-style window control buttons **on the left**.

---

## 📑 Table of Contents

- [✨ Features](#-features)
- [📦 What's Included](#-whats-included)
- [🚀 Installation](#-installation)
- [🎯 Result](#-result)
- [🔧 Customization](#-customization)
- [❓ Troubleshooting](#-troubleshooting)
- [🎨 Compatibility](#-compatibility)
- [📝 Technical Details](#-technical-details)
- [🤝 Support](#-support)
- [📜 Project Information](#-project-information)

---

## ✨ Features

- 🔴🟢🟡 **Buttons on the left** (just like macOS)
- 🎨 **Correct order**: Red (close) → Green (maximize) → Yellow (minimize)
- 🌓 **Light and dark theme support**
- ✨ **Smooth animations** on hover and click
- 🖱️ **Fully functional** - all buttons are clickable

---

## 📦 What's Included

```
MacOS-Firefox-theme/
├── customChrome.css          # Main styles
├── MacTahoe/                 # Theme resources
│   ├── titlebuttons/         # SVG button files (30+ files)
│   ├── colors/               # Color schemes
│   ├── parts/                # UI components
│   └── ...
├── README.md                 # Instructions (Russian)
└── README_EN.md              # Instructions (English)
```

---

## 🚀 Installation

### Step 1: Find Your Firefox Profile Folder

1. Open **Firefox**
2. Type in the address bar: **`about:support`**
3. Find the **"Profile Directory"** row
4. Click **"Open Directory"** / **"Show in Finder"**

### Step 2: Create chrome Folder

In your profile folder:
1. Create a new folder named **`chrome`** (lowercase!)
2. Open the `chrome` folder

### Step 3: Copy Theme Files

1. Copy **all contents** from `MacOS-Firefox-theme` into the `chrome` folder
2. You should have this structure:

```
[Firefox Profile]/
└── chrome/
    ├── customChrome.css
    ├── MacTahoe/
    ├── README.md
    └── README_EN.md
```

### Step 4: Create or Edit userChrome.css

In the `chrome` folder, create **`userChrome.css`** and add:

```css
/* MacOS Window Controls Theme */
@import "MacTahoe/theme.css";
@import "customChrome.css";
```

💡 **If the file already exists** - just add:
```css
@import "customChrome.css";
```

### Step 5: Enable Custom Styles Support

1. Type in the address bar: **`about:config`**
2. Click **"Accept the Risk and Continue"**
3. Search for: **`toolkit.legacyUserProfileCustomizations.stylesheets`**
4. Set the value to **`true`** (double-click)

### Step 6: Restart Firefox

1. **Completely close Firefox** (all windows)
2. Open Firefox again
3. **Done!** 🎉

[⬆️ Back to top](#-table-of-contents)

---

## 🎯 Result

After installation, you'll see:

**🔴 Red button** → Close window  
**🟢 Green button** → Maximize/Restore window  
**🟡 Yellow button** → Minimize window

[⬆️ Back to top](#-table-of-contents)

---

## 🔧 Customization

### Change Distance from Left Edge

Open `customChrome.css` and find:
```css
#nav-bar {
  padding-left: 96px !important;  /* ← Change this value */
}
```

- Smaller (`70px`) - buttons closer to edge
- Larger (`120px`) - buttons further from edge

### Change Spacing Between Buttons

```css
#nav-bar .titlebar-buttonbox-container {
  gap: 4px !important;  /* ← Spacing between buttons */
}
```

[⬆️ Back to top](#-table-of-contents)

---

## ❓ Troubleshooting

### Theme Not Working?

✅ Check path: `[Profile]/chrome/customChrome.css`  
✅ Verify: `toolkit.legacyUserProfileCustomizations.stylesheets` = `true`  
✅ Fully restart Firefox (all windows)  
✅ Check `userChrome.css`: must contain `@import "customChrome.css";`

### Buttons Still on the Right?

✅ Check import order in `userChrome.css`  
✅ `@import "customChrome.css";` must be **after** `@import "MacTahoe/theme.css";`  
✅ Fully restart Firefox

### Want to Revert to Default?

Comment out in `userChrome.css`:
```css
/* @import "customChrome.css"; */
```

[⬆️ Back to top](#-table-of-contents)

---

## 🎨 Compatibility

| Component | Support |
|-----------|---------|
| **Firefox** | 69+ |
| **OS** | Windows, macOS, Linux |
| **Themes** | Light and Dark |
| **Base Theme** | MacTahoe (any version) |

[⬆️ Back to top](#-table-of-contents)

---

## 📝 Technical Details

### What's Modified

1. **customChrome.css** - left positioning, correct button order
2. **All states**: normal, hover, active, inactive window
3. **Both themes**: light and dark

### Modified Files

**Close button (red):**
- `titlebutton-close.svg` / `titlebutton-close-dark.svg`
- `titlebutton-close-hover.svg` / `titlebutton-close-hover-dark.svg`
- `titlebutton-close-active.svg` / `titlebutton-close-active-dark.svg`
- `titlebutton-close-backdrop.svg` / `titlebutton-close-backdrop-dark.svg`

**Maximize button (green):**
- `titlebutton-maximize-*.svg` / `titlebutton-unmaximize-*.svg`
- All variants: normal, hover, active, backdrop (light + dark)

**Minimize button (yellow):**
- `titlebutton-minimize-*.svg`
- All variants: normal, hover, active, backdrop (light + dark)

[⬆️ Back to top](#-table-of-contents)

---

## 🤝 Support

**Having installation issues?**

1. Re-read the instructions carefully
2. Check error console: **Ctrl+Shift+J**
3. Make sure Firefox is completely restarted

[⬆️ Back to top](#-table-of-contents)

---

## 📜 Project Information

**Modifications:**
- Window control buttons moved to the left
- Correct macOS-style button order

[⬆️ Back to top](#-table-of-contents)

---

## ⭐ Like This Theme?

Share it with your friends! 🚀

---

**[🇷🇺 Читать на русском](README.md)**
