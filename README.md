# 📈 Simulateur ROI — PWA

Simulateur d'investissement mensuel avec intérêts composés, montants et taux variables dans le temps. Fonctionne **100% hors-ligne** une fois installé.

## Fonctionnalités

- Définir une durée d'investissement (1–50 ans)
- Graphique interactif du **montant mensuel** : ajouter/déplacer/supprimer des points, interpolation linéaire
- Graphique interactif du **taux annuel** : même logique
- Simulation mois par mois avec **intérêts composés**
- Graphique de résultats : capital investi, gains cumulés, gains annuels
- Table récapitulative année par année
- **PWA** : installable sur mobile et desktop, fonctionne hors-ligne

---

## 🚀 Déploiement sur GitHub Pages

### 1. Créer le dépôt

```bash
git init
git add .
git commit -m "feat: simulateur ROI PWA"
```

### 2. Pousser sur GitHub

```bash
# Créez un dépôt sur github.com, puis :
git remote add origin https://github.com/VOTRE_USERNAME/VOTRE_REPO.git
git branch -M main
git push -u origin main
```

### 3. Activer GitHub Pages

Dans votre dépôt GitHub :
- Aller dans **Settings → Pages**
- Source : **Deploy from a branch**
- Branch : `main` / `/ (root)`
- Cliquer **Save**

Votre app sera disponible à :
```
https://VOTRE_USERNAME.github.io/VOTRE_REPO/
```

> ⚠️ GitHub Pages requiert HTTPS, ce qui est nécessaire pour que le Service Worker fonctionne. Tout est compatible automatiquement.

---

## 📂 Structure des fichiers

```
├── index.html       → Application principale
├── manifest.json    → Manifeste PWA (nom, icônes, couleurs)
├── sw.js            → Service Worker (cache offline)
├── icons/
│   ├── icon-192.png → Icône PWA 192×192
│   └── icon-512.png → Icône PWA 512×512
└── README.md
```

---

## 📱 Installation en tant qu'app

**Sur mobile (iOS/Android)** :
- Ouvrir l'URL dans Safari / Chrome
- iOS : bouton Partager → « Sur l'écran d'accueil »
- Android : bannière automatique ou menu → « Installer l'application »

**Sur desktop (Chrome/Edge)** :
- Icône d'installation dans la barre d'adresse

---

## 🛠️ Développement local

Aucune dépendance, aucun build requis. Un simple serveur HTTP suffit :

```bash
# Python
python3 -m http.server 8080

# Node.js
npx serve .

# VS Code
# Utiliser l'extension Live Server
```

Puis ouvrir `http://localhost:8080`

> Note : le Service Worker ne fonctionne qu'en HTTPS ou `localhost`.
