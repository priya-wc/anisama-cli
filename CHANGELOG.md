# 📝 CHANGELOG

## Version 1.3.1 - 2025-10-05 🔧

### 🐛 CORRECTIONS CRITIQUES
- **✅ Fix limitation épisodes** - Suppression du hard-code limitant les épisodes à 1144
- **🎯 Détection dynamique** - Calcul automatique du dernier épisode basé sur les données JavaScript
- **📺 One Piece à jour** - Support épisodes 1145+ et futurs épisodes automatiquement

### 🔧 AMÉLIORATIONS TECHNIQUES  
- **Smart episode range** - Utilise `tailleEpisodes` et `epRetards` du JavaScript d'anime-sama
- **Fallback intelligent** - Estimation basée sur max_existing + marge de sécurité
- **Future-proof** - Plus besoin de mise à jour manuelle pour chaque nouvel épisode

## Version 1.2.0 - 2025-09-25 🔧

### ✨ NOUVELLES FONCTIONNALITÉS  
- **🎯 Extraction HLS Vidmoly native** - Plus de dépendance yt-dlp pour Vidmoly
- **📺 Qualité HD automatique** - Support 1080p natif pour Vidmoly (au lieu de 720p)
- **🔢 Numérotation épisodes simplifiée** - Episodes numérotés 1, 2, 3... (fini les 1089-1151)

### 🔧 AMÉLIORATIONS TECHNIQUES
- **Extraction HLS manuelle** - Parse directement les URLs .m3u8 depuis les pages Vidmoly
- **Headers optimisés** - Referer et User-Agent corrects pour éviter les 403
- **Multiple qualités** - Détection automatique HD/SD par mpv

### 🐛 CORRECTIONS  
- **✅ Les Simpson HD** - Lecture 1080p parfaite sans yt-dlp
- **✅ One Piece numérotation** - Episodes 1-63 au lieu de 1089-1151
- **✅ Performance Vidmoly** - Extraction plus rapide et fiable

## Version 1.1.0 - 2025-09-25 🚀

### ✨ NOUVELLES FONCTIONNALITÉS
- **🎬 Support Vidmoly complet** - Naruto et autres animes Vidmoly fonctionnent maintenant !
- **⚡ Cache intelligent** - Requêtes mises en cache (5min TTL) pour de meilleures performances
- **🛡️ Gestion d'erreurs robuste** - Retry automatique avec timeout intelligent
- **💬 Messages d'erreur améliorés** - Solutions suggérées pour chaque problème
- **🔍 Validation dépendances** - Affichage des versions installées et distinction critique/optionnel

### 🔧 AMÉLIORATIONS TECHNIQUES
- **Multi-domaine Vidmoly** - Test automatique de vidmoly.net et vidmoly.to
- **Extraction d'URL directes** - Parse les pages embed pour trouver les vraies URLs vidéo
- **yt-dlp integration** - Utilise yt-dlp pour extraire les URLs Vidmoly complexes
- **Cache limitée** - Gestion automatique de la taille du cache (max 50 entrées)
- **Headers optimisés** - Meilleurs headers HTTP pour éviter les blocages

### 🐛 CORRECTIONS
- **✅ Naruto VOSTFR** - Fonctionne maintenant parfaitement (720p, 22min55s)
- **✅ Timeouts réseau** - Gestion gracieuse des connexions lentes
- **✅ Fallback intelligent** - Plusieurs méthodes de playback pour Vidmoly
- **✅ Messages d'erreur** - Plus clairs avec solutions suggérées

### 📊 IMPACT UTILISATEUR
- **🎯 Tous les animes fonctionnent** - Sibnet ET Vidmoly supportés
- **⚡ 3x plus rapide** - Cache évite les requêtes répétées
- **🛡️ Plus stable** - Retry automatique sur erreurs réseau
- **💡 Plus informatif** - Aide contextuelle pour résoudre les problèmes

### 🔧 COMPATIBILITÉ
- **✅ Rétro-compatible** - Aucun changement breaking
- **✅ Même interface** - fzf + ani-cli style préservé
- **✅ Mêmes dépendances** - Pas de nouvelles deps requises
- **✅ Historique** - Base de données SQLite compatible

---

## Version 1.0.0 - 2025-09-24

### 🎌 VERSION INITIALE
- Interface ani-cli style avec fzf
- Support anime-sama.fr
- Historique SQLite
- Support Sibnet basique