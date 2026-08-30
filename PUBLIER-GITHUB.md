# Publier gratuitement sur GitHub Pages — version « tout à la racine »

Aucun sous-dossier dans ce paquet : vous sélectionnez TOUS les fichiers et vous les glissez,
point final. Impossible de casser l'arborescence.

## 1. Compte GitHub gratuit
https://github.com/signup (votre pseudo deviendra l'adresse du site).

## 2. Nouveau dépôt
github.com → « + » → **New repository** → nom : `indian-mood` → **Public** →
ne cochez rien → **Create repository**.

## 3. Upload (le geste important)
1. Dézippez le paquet et **ouvrez le dossier** extrait.
2. **Ctrl+A** (Cmd+A sur Mac) pour tout sélectionner, puis glissez le tout dans la zone
   d'upload de GitHub (lien « uploading an existing file » sur le dépôt vide).
3. Vérifiez la liste proposée : ~37 fichiers, puis bouton vert **Commit changes**.

## 4. Activer Pages
Dépôt → **Settings** → **Pages** → Source : `Deploy from a branch` → `main` + `/ (root)` → **Save**.
~1 minute après, rechargez : bandeau vert « Your site is live at
`https://PSEUDO.github.io/indian-mood/` ».

## 5. Renseigner l'adresse réelle (Google)
Le site contient l'adresse fictive `www.indian-mood-rennes.fr`. Ouvrez chaque fichier sur
github.com (crayon ✏️) et remplacez par `https://PSEUDO.github.io/indian-mood` :
- `index.html` : 8 occurrences (Ctrl+F : « indian-mood-rennes ») — canonical, og:, twitter:, JSON-LD.
- `robots.txt` : ligne `Sitemap:`.
- `sitemap.xml` : balise `<loc>`.

## Redirections déjà gérées
- `/indian-mood` → `/indian-mood/` → `index.html` : natif GitHub Pages.
- Toute adresse mal tapée (`/indian-mood/menu`, typo…) → `404.html` vous renvoie à l'accueil.
- Pas besoin de fichier `.nojekyll` : aucun nom de fichier ne commence par « _ ».

## Modifier le site plus tard
Sur github.com → `index.html` → crayon ✏️ → éditez prix/horaires/textes (balises `img-*` = vos
images) → Commit changes. En ~1 min c'est en ligne. Si vous remplacez une image, gardez le MÊME
nom de fichier (ex. `img-t-butter-chicken.jpg`) : rien d'autre à changer.

## Déclarer à Google (recommandé)
search.google.com/search-console → « Préfixe de l'URL » → votre adresse → vérification par
« Fichier HTML » (téléchargez-le, glissez-le dans le dépôt) → menu Sitemaps → `sitemap.xml`.
