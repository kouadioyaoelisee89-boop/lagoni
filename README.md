# 🛍️ Lagoni Boutique — Gestion des ventes & inventaire

Application mono-fichier HTML de gestion boutique pour Lagoni (Côte d'Ivoire).

## 🚀 Déploiement GitHub + Vercel

### Étape 1 — Créer le dépôt GitHub

1. Aller sur [github.com/new](https://github.com/new)
2. Nom du dépôt : `lagoni-boutique` (ou autre nom)
3. Visibilité : **Privé** recommandé (données boutique)
4. Cliquer **Create repository**

### Étape 2 — Pousser les fichiers sur GitHub

```bash
git init
git add .
git commit -m "🛍️ Lagoni Boutique — déploiement initial"
git branch -M main
git remote add origin https://github.com/VOTRE_PSEUDO/lagoni-boutique.git
git push -u origin main
```

### Étape 3 — Connecter Vercel

1. Aller sur [vercel.com](https://vercel.com) → **Sign in with GitHub**
2. Cliquer **Add New Project**
3. Sélectionner votre dépôt `lagoni-boutique`
4. Framework Preset : **Other** (pas Next.js, pas Vite)
5. Build settings :
   - Build Command : _(vide)_
   - Output Directory : _(vide ou `.`)_
   - Install Command : _(vide)_
6. Cliquer **Deploy** ✅

### Résultat

Votre app sera accessible à : `https://lagoni-boutique-XXXX.vercel.app`

---

## ⚙️ Architecture technique

| Composant | Technologie |
|-----------|-------------|
| App | HTML mono-fichier (11 000+ lignes) |
| Styles | CSS inline + variables |
| Synchronisation cloud | Firebase Realtime Database (REST pure) |
| Stockage local | IndexedDB (primaire) + localStorage (secours) |
| Génération PDF | jsPDF 2.5.1 (CDN Cloudflare) |
| Polices | Google Fonts (Cormorant Garamond + Outfit) |
| PWA | Service Worker + Manifest (Blob URLs) |
| Hébergement | Vercel (CDN mondial) |

## 🔥 Firebase — Configuration

La base de données est déjà configurée :
- **URL** : `https://lagoni-boutique-470f8-default-rtdb.firebaseio.com`
- **Nœud** : `lagoni_boutique/data`

> ⚠️ **Sécurité** : Les règles Firebase sont en lecture/écriture ouverte.
> Pour sécuriser, aller dans Firebase Console → Realtime Database → Rules
> et ajouter une authentification ou restriction IP.

## 📱 Installation comme PWA

Sur Android Chrome, après ouverture de l'URL Vercel :
1. Menu Chrome (⋮) → **Ajouter à l'écran d'accueil**
2. Ou attendre la bannière automatique **"Installer Lagoni"**

## 🔄 Mises à jour

Pour mettre à jour l'application :
```bash
# Modifier lagoni-boutique-inventaire.html
git add lagoni-boutique-inventaire.html
git commit -m "✨ Mise à jour : [description]"
git push
```
Vercel redéploie automatiquement en ~30 secondes.

## 📁 Structure du projet

```
lagoni-boutique/
├── lagoni-boutique-inventaire.html  ← Application principale
├── index.html                        ← Redirection vers l'app
├── vercel.json                       ← Configuration Vercel
├── .gitignore                        ← Fichiers ignorés par Git
└── README.md                         ← Ce fichier
```

---

*Lagoni Boutique — Côte d'Ivoire 🇨🇮 | Contact : +225 07 792 297 74*
