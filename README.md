# 🪄 poshpicker

![poshpicker demo](https://raw.githubusercontent.com/jakemorgangit/poshpicker/main/poshpicker.gif)


**poshpicker** is an interactive terminal tool for Linux that lets you preview, favourite, and apply **Oh My Posh** themes directly from your shell — no manual editing or guessing required.

It automatically installs itself and fetches all official Oh My Posh themes on first run.

---

## ✨ Features

- 🎨 Instant **live theme previews** 
- ⚡ **Single-key navigation**
- 💾 **Save & apply instantly** (updates your `.bashrc`)
- ⭐ **Favourites system** – mark themes you like and cycle through them later
- 🧠 **Self-installing** – copies itself to `/usr/local/bin` so it’s globally available
- 🔄 **Automatic theme bootstrap** – clones the official theme set if missing
- 💻 Works great on **Ubuntu**, **Debian**, and **WSL**

Big shout out to the ohmyposh dev: [JanDeDobbeleer](https://github.com/JanDeDobbeleer)


---

## 🛠️ Installation

Just copy and paste the following commands:

```bash
curl -sSL https://raw.githubusercontent.com/jakemorgangit/poshpicker/main/poshpicker -o ~/poshpicker
chmod +x ~/poshpicker
~/poshpicker
```

It will:

1. Install itself into `/usr/local/bin/poshpicker` (requires sudo once)
2. Download the official Oh My Posh theme set if not already present
3. Launch the theme picker immediately

After installation, you can simply run:

```bash
poshpicker
```

from any terminal.

---

## 🎮 Usage

When running `poshpicker`, you’ll see a live preview of each theme and can navigate with:

| Key | Action |
|-----|---------|
| **n** | Next theme |
| **p** | Previous theme |
| **f** | Toggle favourite |
| **v** | View favourites only |
| **s** | Save & apply selected theme (and quit) |
| **q** | Quit without saving |

---

## 🪩 Apply your new prompt

After saving a theme, your `.bashrc` is automatically updated.

To apply the prompt immediately, run:

```bash
source ~/.bashrc
```

Your new Oh My Posh prompt will appear straight away.

---

## 🗂️ Theme location

Themes are stored under:

```
~/.local/share/poshpicker/poshthemes
```

If this directory doesn’t exist, `poshpicker` will automatically clone and install them for you.

---

## 💾 Favourites

`poshpicker` remembers your favourite themes between sessions.

They’re stored in:

```
~/.poshpicker_favs
```

Press **`v`** at any time to toggle between viewing *all* themes and *favourites only*.


---

## 🧰 Requirements

- **bash** (tested on Ubuntu 22.04+ and WSL)
- **oh-my-posh** binary available in your `$PATH`

If you haven’t yet installed Oh My Posh, run:

```bash
sudo wget https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/posh-linux-amd64 -O /usr/local/bin/oh-my-posh
sudo chmod +x /usr/local/bin/oh-my-posh
```


---

## 🧹 Uninstall

To remove `poshpicker`:

```bash
sudo rm /usr/local/bin/poshpicker
rm -rf ~/.local/share/poshpicker
rm -f ~/.poshpicker_favs
```

---

## 🐙 Contributing

Pull requests are welcome - improvements to interactivity, shell detection (bash/zsh/fish), or additional quality-of-life features are encouraged.

---

## 📄 Licence

MIT Licence © [Jake Morgan](https://github.com/jakemorgangit)
