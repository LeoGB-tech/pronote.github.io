# Pronote Plus v7.1

Outil gratuit pour collégiens & lycéens. Calcule ta vraie moyenne, identifie les matières prioritaires, te dit quelle note viser.

## Fichiers

```
index.html      ← page principale + bookmarklet PC + PWA shell
manifest.json   ← config PWA + Web Share Target
sw.js           ← Service Worker (cache offline)
icon-192.png    ← icône PWA (à créer)
icon-512.png    ← icône PWA (à créer)
```

## Déploiement sur GitHub Pages

1. Crée un repo GitHub (ex: `pronote-plus`)
1. Mets tous ces fichiers à la racine
1. Va dans Settings → Pages → Source : `main` / `root`
1. Ton site sera dispo sur `https://tonpseudo.github.io/pronote-plus/`

> ⚠️ HTTPS obligatoire pour la PWA et le Share Target — GitHub Pages le fournit automatiquement.

## Icônes

Tu peux générer les icônes sur https://favicon.io ou https://realfavicongenerator.net

- `icon-192.png` : 192×192px
- `icon-512.png` : 512×512px

## Comment ça marche

### PC / Mac

Bookmarklet : glisser le bouton vert dans la barre de favoris, puis cliquer sur “Notes → Par matière” dans Pronote.

### iOS (Safari)

1. Ouvrir ce site dans Safari → Partager → “Sur l’écran d’accueil”
1. Aller sur Pronote dans Safari → Notes → Par matière
1. Partager → “Pronote Plus” → calcul automatique

### Android (Chrome)

1. Ouvrir ce site dans Chrome → menu ⋮ → “Ajouter à l’écran d’accueil”
1. Aller sur Pronote dans Chrome → Notes → Par matière
1. Partager → “Pronote Plus” → calcul automatique

## Limites

- **Web Share Target** : fonctionne uniquement si la PWA est installée sur l’écran d’accueil
- **CORS** : on ne peut pas fetch le HTML de Pronote directement (bloqué côté serveur). Le Share Target reçoit l’URL ou le texte de la page.
- **App native Pronote** : impossible d’injecter du JS dans une app native iOS/Android. La PWA est la meilleure alternative.

## Licence

Open-source. Non affilié à Index Education / Pronote.
