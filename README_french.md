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
Ce dépôt est aussi disponible en <a href="README.md"><img src="https://img.shields.io/badge/🇬🇧-English-red" alt="English"></a>
</p>

<h3 align="center">
Un CLI pour parcourir et regarder des animés depuis <a href="https://anime-sama.fr">anime-sama.fr</a> avec l'interface style <strong>ani-cli</strong>
</h3>

<p align="center">
<strong>✨ Sélection interactive fuzzy • 🚀 Recherche en une commande • 🎯 Support du contenu français</strong>
</p>

<h1 align="center">Démonstration</h1>

<p align="center">
<img src="https://user-images.githubusercontent.com/placeholder/anisama-cli-demo.gif" alt="démo anisama-cli" width="80%">
</p>

## Table des Matières

- [🚀 Installation](#installation)
  - [📦 Arch Linux](#arch-linux)
  - [🐧 Autres Linux](#autres-linux) 
  - [🪟 Windows](#windows)
- [🎯 Utilisation](#utilisation)
- [🗑️ Désinstallation](#désinstallation)
- [📚 Dépendances](#dépendances)
- [❓ FAQ](#faq)
- [🌐 Autres CLI d'animés](#autres-cli-danimés)
- [🤝 Contribuer](#contribuer)

## Installation

### Arch Linux

```bash
# Avec yay (recommandé)
yay -S anisama-cli

# Avec paru
paru -S anisama-cli
```

### Autres Linux

**Prérequis :** Assurez-vous d'avoir `curl`, `python3`, `pip` et `mpv` installés.

```bash
# Cloner le dépôt
git clone https://github.com/karbonedev/anisama-cli.git
cd anisama-cli

# Installer les dépendances
pip install -r requirements.txt

# Rendre exécutable et installer globalement
chmod +x anisama-cli
sudo cp anisama-cli /usr/local/bin/
```

### Windows

Ouvrez PowerShell et exécutez :
```powershell
# Télécharger et installer
iwr -Uri "https://raw.githubusercontent.com/karbonedev/anisama-cli/main/install-windows.ps1" -OutFile "install.ps1"
.\install.ps1
```

## Utilisation

### Commandes de Base

```bash
# Mode interactif
anisama-cli

# Recherche directe
anisama-cli "naruto"

# Version française (recommandé pour anime-sama.fr)
anisama-cli "one piece" --vf 🇫🇷

# Continuer à regarder
anisama-cli -c

# Afficher l'aide
anisama-cli --help
```

### Fonctionnalités de l'Interface

- **🔍 Recherche Floue** : Tapez pour filtrer les résultats en temps réel
- **⌨️ Navigation Clavier** : Utilisez les flèches, Entrée pour sélectionner, Échap pour annuler
- **📺 Sélection Intelligente** : Menus interactifs pour animés, saisons et épisodes
- **🎨 Interface Épurée** : Pas de menus complexes, juste l'essentiel
- **💾 Historique** : Reprenez là où vous vous êtes arrêté

### Options de Commande

| Option | Description |
|--------|-------------|
| `--vf` | Activer la voix/doublage français 🇫🇷 |
| `-c, --continue` | Continuer à regarder depuis l'historique |
| `-h, --help` | Afficher le message d'aide |
| `-v, --version` | Afficher la version |

## Désinstallation

<details>
<summary>📋 Cliquez pour développer les instructions de désinstallation</summary>

### Arch Linux (AUR)
```bash
yay -R anisama-cli
# ou
paru -R anisama-cli
```

### Autres Linux
```bash
sudo rm /usr/local/bin/anisama-cli
rm -rf ~/.local/share/anisama-cli
```

### Windows
```powershell
# Supprimer du PATH et effacer les fichiers
Remove-Item -Recurse -Force "$env:USERPROFILE\anisama-cli"
```

</details>

## Dépendances

### 🐍 Dépendances Python
- **requests** : Bibliothèque HTTP pour les requêtes web
- **beautifulsoup4** : Analyseur HTML/XML pour le scraping d'anime-sama.fr  
- **sqlite3** : Base de données pour l'historique de visionnage (intégré)
- **re, json, sys, os** : Modules de bibliothèque standard (intégrés)

### 🛠️ Dépendances Système
- **python3** : Runtime Python (≥3.6)
- **fzf** : Fuzzy finder pour la sélection interactive
- **mpv** : Lecteur multimédia pour la lecture vidéo
- **curl** : Pour les scripts d'installation
- **git** : Pour le clonage de dépôt

### 📦 Commandes d'Installation

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
<summary>❓ <strong>Questions Fréquemment Posées</strong></summary>

### Questions Générales

**Q : Puis-je changer la langue des sous-titres ou les désactiver ?**  
R : Non, les sous-titres sont intégrés dans les fichiers vidéo d'anime-sama.fr.

**Q : Puis-je regarder avec la voix française ?**  
R : Oui ! Utilisez le flag `--vf` : `anisama-cli "nom anime" --vf` 🇫🇷

**Q : Puis-je changer la langue de doublage vers l'anglais/japonais ?**  
R : Non, anime-sama.fr ne fournit que du contenu français (VF/VOSTFR).

**Q : Puis-je changer la source média ?**  
R : Non, anisama-cli est spécifiquement conçu pour anime-sama.fr.

**Q : Puis-je utiliser VLC au lieu de mpv ?**  
R : Non, seul mpv est pris en charge pour des performances de streaming optimales.

**Q : Est-ce que ça marche sur mobile/Android ?**  
R : Non, anisama-cli est conçu pour les environnements desktop/terminal.

### Questions Techniques

**Q : Pourquoi fzf plutôt que l'interface textuelle originale ?**  
R : fzf offre une recherche plus rapide, une meilleure UX et correspond à l'interface familière d'ani-cli.

**Q : Mon historique de visionnage est-il sauvegardé ?**  
R : Oui, votre progression est sauvegardée localement et vous pouvez continuer avec `-c`.

**Q : Est-ce que ça nécessite une connexion internet ?**  
R : Oui, cela diffuse du contenu depuis anime-sama.fr en temps réel.

</details>

## Autres CLI d'Animés

Vous cherchez des animés dans d'autres langues ? Découvrez ces projets incroyables :

- **🇯🇵 [ani-cli](https://github.com/pystardust/ani-cli)** : Voix japonaise avec sous-titres anglais
- **🇵🇹 [GoAnime](https://github.com/alvarorichard/GoAnime)** : Voix japonaise avec sous-titres portugais  
- **🇵🇱 [doccli](https://github.com/TowarzyszFatCat/doccli)** : Voix japonaise avec sous-titres polonais
- **🇩🇪 [aniworld-cli](https://github.com/Bog13/aniworld-cli)** : Streaming d'animés allemands
- **🇪🇸 [animeflv-cli](https://github.com/usuario/animeflv-cli)** : Streaming d'animés espagnols

## Contribuer

Nous accueillons les contributions ! Voici comment vous pouvez aider :

### 🐛 Rapports de Bug
- Utilisez [GitHub Issues](https://github.com/karbonedev/anisama-cli/issues)
- Incluez les étapes pour reproduire
- Fournissez les infos système (OS, version Python)

### 💡 Demandes de Fonctionnalités  
- Vérifiez d'abord les issues existantes
- Décrivez clairement le cas d'usage
- Considérez la rétrocompatibilité

### 🔧 Pull Requests
- Forkez le dépôt
- Créez une branche de fonctionnalité
- Suivez le style de code existant
- Testez vos changements
- Mettez à jour la documentation si nécessaire

### 📝 Documentation
- Corrigez les fautes de frappe ou améliorez la clarté
- Ajoutez des exemples pour les nouvelles fonctionnalités
- Traduisez vers d'autres langues

---

<p align="center">
<strong>⭐ Étoilez ce projet si vous le trouvez utile !</strong><br>
<em>Construit avec ❤️ par <a href="https://github.com/karbonedev">karbonedev</a></em><br>
<small>Inspiration originale d'<a href="https://github.com/pystardust/ani-cli">ani-cli</a> 🙏</small>
</p>