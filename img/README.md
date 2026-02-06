# Portfolio Professionnel

Portfolio minimaliste et épuré, optimisé pour GitHub Pages.

## 🎨 Caractéristiques

- **Design Moderne** : Dark mode professionnel avec accents cyan
- **Responsive** : Parfaitement optimisé pour tous les appareils
- **Performant** : Pas de dépendances externes lourdes
- **Accessible** : Sémantique HTML proper et navigation claire
- **GitHub Pages Ready** : Déploiement direct depuis ton repo

## 📁 Structure

```
portfolio/
├── index.html       # Page principale
├── styles.css       # Styles optimisés
├── script.js        # Interactions & animations
└── README.md        # Ce fichier
```

## 🚀 Installation Locale

1. Clone le repo
```bash
git clone https://github.com/ton-username/portfolio.git
cd portfolio
```

2. Ouvre `index.html` dans ton navigateur
```bash
# macOS
open index.html

# Linux
xdg-open index.html

# Windows
start index.html
```

Ou utilise un serveur local :
```bash
python3 -m http.server 8000
# Puis visite http://localhost:8000
```

## 📦 Déploiement sur GitHub Pages

### Option 1 : Depuis la branche main (Recommended)

1. **Pousse le code sur GitHub**
```bash
git add .
git commit -m "Ajoute portfolio"
git push origin main
```

2. **Active GitHub Pages**
   - Va dans les **Settings** de ton repo
   - Scroll jusqu'à **GitHub Pages**
   - Sélectionne `main` comme branche source
   - Clique sur **Save**

3. **Accède à ton portfolio**
```
https://ton-username.github.io/portfolio/
```

### Option 2 : Depuis une branche `gh-pages`

```bash
# Crée une branche gh-pages
git checkout --orphan gh-pages

# Ajoute et pousse les fichiers
git add .
git commit -m "Deploy portfolio"
git push origin gh-pages
```

## ✏️ Personnalisation

### 1. Mettre à jour les informations

**Dans `index.html`**
- Remplace les liens GitHub par tes vrais liens
- Modifie l'email dans la section Contact
- Change les URLs LinkedIn et autres réseaux

```html
<a href="https://github.com/ton-username" class="contact-link" target="_blank">
    <span class="contact-icon">⚡</span>
    GitHub
</a>
```

### 2. Ajouter tes propres projets

**Section Projects** :
```html
<article class="project-card">
    <div class="project-header">
        <h3>Ton Projet</h3>
        <p class="project-date">2024</p>
    </div>
    <p class="project-description">
        Description de ton projet...
    </p>
    <div class="project-tags">
        <span class="tag">Technologie1</span>
        <span class="tag">Technologie2</span>
    </div>
    <a href="https://github.com/lien" class="project-link" target="_blank">
        Voir sur GitHub <span class="arrow">→</span>
    </a>
</article>
```

### 3. Modifier les couleurs

**Dans `styles.css`** (section `:root`):
```css
:root {
    --bg-primary: #0f1419;
    --accent: #00d9ff;      /* Couleur principale */
    --success: #4ade80;      /* Couleur secondaire */
    /* ... */
}
```

### 5. Modifier ton CV

**Section Formation** (dans `index.html`):
```html
<div class="cv-entry">
    <div class="cv-entry-header">
        <h5>Ton Diplôme</h5>
        <span class="cv-date">Année - Année</span>
    </div>
    <p class="cv-location">Établissement, Ville</p>
    <p class="cv-description">
        Description de ta formation...
    </p>
</div>
```

**Section Expérience**:
```html
<div class="cv-entry">
    <div class="cv-entry-header">
        <h5>Ton Titre</h5>
        <span class="cv-date">2024</span>
    </div>
    <p class="cv-location">Entreprise/Projet</p>
    <ul class="cv-achievements">
        <li>Accomplissement 1</li>
        <li>Accomplissement 2</li>
    </ul>
</div>
```

**À propos** (section `.cv-about`):
```html
<div class="cv-about">
    <h3>À propos</h3>
    <p>Ton texte de présentation personnelle...</p>
</div>
```

### 6. Ajouter une image de profil (optionnel)

Ajoute au début du hero:
```html
<img src="assets/profile.jpg" alt="Profil" class="profile-image">
```

## 🎯 Fonctionnalités Principales

### Téléchargement CV en PDF
Le portfolio intègre une fonctionnalité de **génération et téléchargement automatique du CV en PDF**.

- **Bouton cliquable** dans la section CV
- **Formatage automatique** adapté à l'impression
- **Données synchronisées** avec la section CV affichée
- **Aucune dépendance externe** requise (librairie chargée à la demande)

**Comment ça marche** :
1. L'utilisateur clique sur le bouton "Télécharger mon CV"
2. La librairie `html2pdf.js` est chargée depuis CDN
3. Un PDF formaté est généré automatiquement
4. Le fichier `CV-Developpeur.pdf` est téléchargé

## 📋 Sections Principales

### Hero
- Titre accrocheur avec gradient
- Appels à l'action (CTA)
- Description claire du profil

### Projets
- Cards responsives
- Tags technologiques
- Liens vers GitHub

### Stack Technique
- Langages maîtrisés
- Frameworks & outils
- Concepts & méthodes

### CV
- **À propos** : Résumé professionnel
- **Formation** : Diplômes et formations académiques
- **Expérience** : Projets et travaux réalisés
- **Téléchargement PDF** : Bouton pour exporter ton CV en PDF

### Contact
- Liens rapides (GitHub, Email, LinkedIn)
- Design cohérent

## 🎨 Tipps de Customisation

### Changer la police d'affichage
Dans `index.html` (ligne 10) :
```html
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;600;700&display=swap" rel="stylesheet">
```

Puis dans `styles.css` :
```css
--font-display: 'Space Grotesk', sans-serif;
```

### Ajouter des animations personnalisées
- Modifie la section `@keyframes` dans `styles.css`
- Utilise `animation` sur tes éléments
- Test avec Developer Tools (F12)

## 🚨 Troubleshooting

### Les images ne s'affichent pas
- Vérifie le chemin des images
- Les chemins doivent être relatifs (ex: `assets/image.jpg`)

### GitHub Pages ne met pas à jour
- Vide le cache (Ctrl+Shift+Del)
- Attends quelques minutes (max 1 minute généralement)
- Vérifie les Settings > Pages

### Style cassé après déploiement
- S'assure que `styles.css` et `script.js` sont au même niveau que `index.html`
- Vérifie les chemins relatifs des assets

## 📊 Performance

- Lighthouse Score: **95+**
- Temps de chargement: **< 1s**
- Pas de dépendances NPM
- Pur HTML/CSS/JavaScript

## 📝 Licence

Libre d'utilisation pour ton portfolio personnel.

## 💡 Conseil

Mets à jour ton portfolio régulièrement :
- Ajoute tes nouveaux projets
- Met à jour tes compétences
- Améliore les descriptions

---

**Questions ?** Consulte la [documentation GitHub Pages](https://docs.github.com/en/pages)
