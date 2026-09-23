# Devis carrelage & fiche chantier

Outil autonome, un seul fichier (`index.html`). Aucune dépendance serveur : tout tourne dans le navigateur (formulaire, calculs, export Word). Rien n'est enregistré nulle part — tu remplis, tu exportes le devis et la fiche technique en .docx, puis "Nouveau devis" pour repartir de zéro sur le suivant.

## Héberger gratuitement (choisis une option)

### Option A — Ligne de commande (git push), le plus direct
Ce dossier contient déjà un dépôt git initialisé avec un premier commit. Il ne manque que le lien vers GitHub :

1. Sur github.com : **New repository** → donne-lui un nom (ex. `devis-carrelage`) → **ne coche ni "Add a README" ni ".gitignore"** (le dépôt doit rester vide) → Create repository.
2. Dans un terminal, à la racine de ce dossier décompressé :
   ```
   git remote add origin https://github.com/TON-NOM-UTILISATEUR/devis-carrelage.git
   git push -u origin main
   ```
   (remplace l'URL par celle affichée sur la page de ton nouveau dépôt GitHub, bouton "Code" → HTTPS)
3. Dans le dépôt sur github.com : **Settings → Pages** → Source : **Deploy from a branch**, branche `main`, dossier `/ (root)` → Save.
4. Après 1-2 minutes, ton outil est en ligne à `https://TON-NOM-UTILISATEUR.github.io/devis-carrelage/`.

Besoin de Git installé sur ta machine (`git --version` pour vérifier ; sinon [git-scm.com](https://git-scm.com/downloads)).

### Option B — Glisser-déposer sur github.com (sans rien installer)
1. Crée un compte GitHub si tu n'en as pas (gratuit).
2. Crée un nouveau dépôt (repository), par exemple `devis-carrelage`.
3. Mets `index.html` à la racine du dépôt (glisser-déposer sur github.com fonctionne, pas besoin de ligne de commande).
4. Dans le dépôt : **Settings → Pages → Source : Deploy from a branch**, branche `main`, dossier `/root`. Enregistre.
5. Après 1-2 minutes, ton outil est en ligne à une adresse du type :
   `https://TON-NOM-UTILISATEUR.github.io/devis-carrelage/`
6. Ajoute cette adresse à l'écran d'accueil de ton téléphone pour l'ouvrir comme une app.

Pas de mise en veille, pas de limite de trafic gênante pour un usage perso.

### Option C — Netlify (glisser-déposer, encore plus rapide)
1. Va sur netlify.com, crée un compte gratuit.
2. "Add new site" → "Deploy manually" → glisse le dossier contenant `index.html`.
3. Ton site est en ligne immédiatement sur une adresse `....netlify.app`.

### Option D — Vercel
Même principe que Netlify : compte gratuit, importer le dossier ou connecter un dépôt GitHub, déploiement automatique.

## Fonctionnement

Aucune donnée n'est conservée d'un devis à l'autre : le formulaire ne garde les informations qu'en mémoire pendant la saisie. Une fois les deux documents .docx exportés (devis client + fiche technique pour l'exécutant), clique sur "Nouveau devis" pour vider le formulaire et passer au suivant.
