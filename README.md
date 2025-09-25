# Anime-Sama CLI - ani-cli Style Interface

Ce projet est une version modifiée d'`anime-sama.py` avec une interface utilisateur inspirée d'[ani-cli](https://github.com/pystardust/ani-cli), offrant une expérience plus fluide et intuitive.

## 🌟 Améliorations Principales

### Interface fzf Intégrée
- **Sélection interactive** : Utilise `fzf` (fuzzy finder) pour toutes les sélections
- **Recherche rapide** : Tapez pour filtrer les résultats en temps réel
- **Navigation au clavier** : Flèches haut/bas, Entrée pour valider, Échap pour annuler
- **Interface unifiée** : Même style pour tous les menus (anime, saisons, épisodes)

### Workflow Simplifié
- **Recherche directe** : `./anime-sama-cli naruto` lance directement la recherche
- **Prompts colorés** : Interface claire avec codes couleur cohérents
- **Messages d'état** : Feedback visuel pour chaque étape
- **Gestion d'erreurs** : Messages d'erreur clairs et informatifs

### Compatibilité ani-cli
- **Syntaxe familière** : Options similaires à ani-cli (`-c`, `--vf`, etc.)
- **Comportement cohérent** : Logique de sélection et navigation identique
- **Interface minimale** : Pas de menus complexes, juste l'essentiel

## 📋 Comparaison avec l'Original

| Fonctionnalité | anime-sama.py (original) | anime-sama-cli (nouveau) |
|---|---|---|
| Interface principale | Menu textuel numéroté | fzf avec recherche interactive |
| Sélection d'anime | Liste numérotée (1, 2, 3...) | Fuzzy finder avec filtrage |
| Navigation | Input manuel de numéros | Flèches + Entrée |
| Recherche | Input séparé | Intégrée dans fzf |
| Historique | Liste simple | Interface fzf interactive |
| Gestion d'erreurs | Messages basiques | Fonction `die()` avec formatage |

## 🚀 Installation et Usage

### Prérequis
```bash
# Ubuntu/Debian
sudo apt install fzf mpv python3-pip
pip install requests beautifulsoup4

# Arch Linux
sudo pacman -S fzf mpv python-requests python-beautifulsoup4

# macOS (avec Homebrew)
brew install fzf mpv
pip install requests beautifulsoup4
```

### Usage
```bash
# Recherche interactive
./anime-sama-cli

# Recherche directe
./anime-sama-cli "one piece"

# Recherche VF uniquement
./anime-sama-cli --vf "dragon ball"

# Continuer depuis l'historique
./anime-sama-cli -c

# Mode debug
./anime-sama-cli --debug "naruto"

# Aide
./anime-sama-cli -h
```

## 🎯 Fonctionnalités Conservées

Toutes les fonctionnalités de base de l'original sont conservées :
- ✅ **Streaming vidéo** : Lecture avec mpv en plein écran
- ✅ **Historique** : Sauvegarde automatique des épisodes regardés
- ✅ **Multi-saisons** : Support des différentes saisons et versions
- ✅ **VF/VOSTFR** : Choix de la version française ou sous-titrée
- ✅ **Base de données** : Stockage local dans `~/.local/share/animesama-cli/`

## 🔧 Améliorations Techniques

### Architecture
- **Code modulaire** : Fonctions séparées pour chaque type de sélection
- **Gestion d'erreurs** : Fonction centralisée `die()` pour les erreurs fatales
- **Interface cohérente** : Fonction `fzf_select()` réutilisable
- **Prompts interactifs** : `search_prompt()` avec gestion des interruptions

### Style ani-cli
- **Couleurs ANSI** : Codes couleur identiques à l'original mais utilisés de manière cohérente
- **Formatage des messages** : Style uniforme pour tous les retours utilisateur
- **Navigation intuitive** : Logique de sélection inspirée d'ani-cli
- **Simplicité d'usage** : Interface minimaliste et efficace

## 🎨 Exemple d'Interface

```
╔══════════════════════════════════════════════════════╗
║     🎌 ANIME-SAMA CLI - ani-cli style 🎌          ║
║  📺 Streaming + MPV + fzf interface               ║
║  ⚡ Powered by iamlaz + ani-cli UI                ║
╚══════════════════════════════════════════════════════╝

🔍 Checking dependencies...
✓ All dependencies found! 🚀

Search anime: one piece
🔍 Searching for: one piece

📋 SEARCH RESULTS:
> 1. One Piece
  2. One Piece Film: Red
  3. One Piece: Stampede
  [Interface fzf interactive]
```

## 🛠️ Développement

Le code est structuré de manière modulaire avec :
- **Fonctions utilitaires** : `fzf_select()`, `die()`, `search_prompt()`
- **Classes métier** : `AnimeDownloader` (identique à l'original)
- **Fonctions d'interface** : `display_history()`, `main()`
- **Configuration** : Variables globales pour couleurs et headers

## 📝 Notes

- Compatible avec l'historique de l'original `anime-sama.py`
- Nécessite `fzf` pour l'interface interactive
- Conserve toute la logique de scraping originale
- Interface inspirée mais pas identique à ani-cli (adaptation pour anime-sama.fr)

## 🙏 Crédits

- **anime-sama.py original** : Code de base pour le scraping d'anime-sama.fr
- **ani-cli** : Inspiration pour l'interface utilisateur et l'UX
- **fzf** : Outil de sélection interactive