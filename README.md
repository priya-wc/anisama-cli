<p align=center>
<br>
<a href="#Linux"><img src="https://img.shields.io/badge/os-linux-90ee90"></a>
<a href="#Windows"><img src="https://img.shields.io/badge/os-windows-90ee90"></a>
<a href="https://aur.archlinux.org/packages/anisama-cli"><img src="https://img.shields.io/aur/version/anisama-cli?style=flat&logo=archlinux&color=1793D1"></a>
<br>
<h1 align="center">🎌 anisama-cli</h1>
<br>
<a href="https://github.com/karbonedev"><img src="https://img.shields.io/badge/owner-karbonedev-ff6344"></a>
</p>

<p align="center">
This repository is also available in <a href="README_french.md"><img src="https://img.shields.io/badge/🇫🇷-French-blue" alt="French"></a>
</p>

<h3 align="center">
A CLI to browse and watch anime from <a href="https://anime-sama.fr">anime-sama.fr</a> with <strong>ani-cli</strong> style interface
</h3>

<p align="center">
<strong>✨ Interactive fuzzy finder • 🚀 One-command search • 🎯 French content support</strong>
</p>

<h1 align="center">Showcase</h1>

[ani-cli-demo.webm](https://user-images.githubusercontent.com/44473782/224679247-0856e652-f187-4865-bbcf-5a8e5cf830da.webm)


## Table of Contents

- [🚀 Install](#install)
  - [📦 Arch Linux](#arch-linux)
  - [🐧 Other Linux](#other-linux) 
  - [🪟 Windows](#windows)
- [🎯 Usage](#usage)
- [🗑️ Uninstall](#uninstall)
- [📚 Dependencies](#dependencies)
- [❓ FAQ](#faq)
- [🌐 Other Language CLI](#other-language-cli)
- [🤝 Contributing](#contributing)

## Install

### Arch Linux

```bash
# Using yay (recommended)
yay -S anisama-cli

# Using paru
paru -S anisama-cli
```

### Other Linux

**Prerequisites:** Ensure you have `curl`, `python3`, `pip`, and `mpv` installed.

```bash
# Clone repository
git clone https://github.com/karbonedev/anisama-cli.git
cd anisama-cli

# Install dependencies
pip install -r requirements.txt

# Make executable and install globally
chmod +x anisama-cli
sudo cp anisama-cli /usr/local/bin/
```

### Windows

Open PowerShell and run:
```powershell
# Download and install
iwr -Uri "https://raw.githubusercontent.com/karbonedev/anisama-cli/main/install-windows.ps1" -OutFile "install.ps1"
.\install.ps1
```

## Usage

### Basic Commands

```bash
# Interactive mode
anisama-cli

# Direct search
anisama-cli "naruto"

# French dub (recommended for anime-sama.fr)
anisama-cli "one piece" --vf 🇫🇷

# Continue watching
anisama-cli -c

# Show help
anisama-cli --help
```

### Interface Features

- **🔍 Fuzzy Search**: Type to filter results in real-time
- **⌨️ Keyboard Navigation**: Use arrow keys, Enter to select, Escape to cancel
- **📺 Smart Selection**: Interactive menus for anime, seasons, and episodes
- **🎨 Clean Interface**: No complex menus, just the essentials
- **💾 History**: Resume where you left off

### Command Options

| Option | Description |
|--------|-------------|
| `--vf` | Enable French voice/dub 🇫🇷 |
| `-c, --continue` | Continue watching from history |
| `-h, --help` | Show help message |
| `-v, --version` | Show version |

## Uninstall

<details>
<summary>📋 Click to expand uninstall instructions</summary>

### Arch Linux (AUR)
```bash
yay -R anisama-cli
# or
paru -R anisama-cli
```

### Other Linux
```bash
sudo rm /usr/local/bin/anisama-cli
rm -rf ~/.local/share/anisama-cli
```

### Windows
```powershell
# Remove from PATH and delete files
Remove-Item -Recurse -Force "$env:USERPROFILE\anisama-cli"
```

</details>

## Dependencies

### 🐍 Python Dependencies
- **requests**: HTTP library for web requests
- **beautifulsoup4**: HTML/XML parser for anime-sama.fr scraping  
- **sqlite3**: Database for watch history (built-in)
- **re, json, sys, os**: Standard library modules (built-in)

### 🛠️ System Dependencies
- **python3**: Python runtime (≥3.6)
- **fzf**: Fuzzy finder for interactive selection
- **mpv**: Media player for video playback
- **curl**: For installation scripts
- **git**: For repository cloning

### 📦 Installation Commands

<details>
<summary>🐧 Ubuntu/Debian</summary>

```bash
sudo apt update
sudo apt install python3 python3-pip mpv fzf curl git
pip3 install requests beautifulsoup4
```
</details>

<details>
<summary>🎩 Fedora</summary>

```bash
sudo dnf install python3 python3-pip mpv fzf curl git
pip3 install requests beautifulsoup4
```
</details>

<details>
<summary>🦎 openSUSE</summary>

```bash
sudo zypper install python3 python3-pip mpv fzf curl git
pip3 install requests beautifulsoup4
```
</details>

<details>
<summary>🍎 macOS</summary>

```bash
brew install python mpv fzf curl git
pip3 install requests beautifulsoup4
```
</details>

## FAQ

<details>
<summary>❓ <strong>Frequently Asked Questions</strong></summary>

### General Questions

**Q: Can I change subtitle language or turn them off?**  
A: No, the subtitles are embedded in the video files from anime-sama.fr.

**Q: Can I watch with French voice?**  
A: Yes! Use the `--vf` flag: `anisama-cli "anime name" --vf` 🇫🇷

**Q: Can I change dub language to English/Japanese?**  
A: No, anime-sama.fr only provides French content (VF/VOSTFR).

**Q: Can I change the media source?**  
A: No, anisama-cli is specifically designed for anime-sama.fr.

**Q: Can I use VLC instead of mpv?**  
A: No, only mpv is supported for optimal streaming performance.

**Q: Does it work on mobile/Android?**  
A: No, anisama-cli is designed for desktop/terminal environments.

### Technical Questions

**Q: Why fzf over the original textual interface?**  
A: fzf provides faster searching, better UX, and matches ani-cli's familiar interface.

**Q: Is my watch history saved?**  
A: Yes, your progress is saved locally and you can continue with `-c`.

**Q: Does it require internet connection?**  
A: Yes, it streams content from anime-sama.fr in real-time.

</details>

## Other Language CLI

Looking for anime in other languages? Check out these amazing projects:

- **🇯🇵 [ani-cli](https://github.com/pystardust/ani-cli)**: Japanese voice with English subtitles
- **🇵🇹 [GoAnime](https://github.com/alvarorichard/GoAnime)**: Japanese voice with Portuguese subtitles  
- **🇵🇱 [doccli](https://github.com/TowarzyszFatCat/doccli)**: Japanese voice with Polish subtitles
- **🇩🇪 [aniworld-cli](https://github.com/Bog13/aniworld-cli)**: German anime streaming
- **🇪🇸 [animeflv-cli](https://github.com/usuario/animeflv-cli)**: Spanish anime streaming

## Contributing

We welcome contributions! Here's how you can help:

### 🐛 Bug Reports
- Use [GitHub Issues](https://github.com/karbonedev/anisama-cli/issues)
- Include steps to reproduce
- Provide system info (OS, Python version)

### 💡 Feature Requests  
- Check existing issues first
- Describe the use case clearly
- Consider backward compatibility

### 🔧 Pull Requests
- Fork the repository
- Create a feature branch
- Follow existing code style
- Test your changes
- Update documentation if needed

### 📝 Documentation
- Fix typos or improve clarity
- Add examples for new features
- Translate to other languages

---

<p align="center">
<strong>⭐ Star this project if you find it useful!</strong><br>
<em>Built with ❤️ by <a href="https://github.com/can-oktay404">Can Oktay</a></em><br>
<small>Original inspiration from <a href="https://github.com/pystardust/ani-cli">ani-cli</a> 🙏</small>
</p>
