# OF Tracker — MK AERO

Outil de suivi journalier des OF's : compare le fichier client et l'export ERP,
calcule les indicateurs (nouveaux OF, progressés, stagnants, terminés, urgents,
multi-lots). 100% client-side — aucune donnée n'est envoyée à un serveur.

## Structure du projet

```
of-tracker/
└── index.html      <- l'application complète (HTML + CSS + JS, un seul fichier)
```

## Étape 1 — Créer le dépôt sur GitHub

1. Va sur [github.com](https://github.com) et connecte-toi (ou crée un compte gratuit)
2. Clique sur **"New repository"** (bouton vert, en haut à droite)
3. Nom du dépôt : `of-tracker` (ou ce que tu veux)
4. Laisse "Public" sélectionné (nécessaire pour GitHub Pages gratuit)
5. Ne coche **rien** d'autre (pas de README, pas de .gitignore — on les a déjà)
6. Clique **"Create repository"**

GitHub va t'afficher une page avec des commandes — garde-la ouverte, on va s'en servir.

## Étape 2 — Ouvrir le projet dans VS Code

1. Installe [VS Code](https://code.visualstudio.com/) si tu ne l'as pas déjà
2. Installe [Git](https://git-scm.com/downloads) si tu ne l'as pas déjà
3. Crée un dossier sur ton PC, ex: `Documents/of-tracker`
4. Mets le fichier `index.html` dedans
5. Ouvre ce dossier dans VS Code : `Fichier > Ouvrir le dossier...`

## Étape 3 — Envoyer sur GitHub (depuis le terminal intégré de VS Code)

Dans VS Code : `Terminal > Nouveau terminal`, puis colle ces commandes une par une
(remplace `TON_USERNAME` par ton nom d'utilisateur GitHub) :

```bash
git init
git add .
git commit -m "Premier envoi de l'outil OF Tracker"
git branch -M main
git remote add origin https://github.com/TON_USERNAME/of-tracker.git
git push -u origin main
```

Si Git te demande de t'identifier, connecte-toi avec ton compte GitHub
(VS Code ouvre normalement une fenêtre de connexion automatiquement).

## Étape 4 — Activer GitHub Pages (avoir le lien du site)

1. Sur GitHub, va dans ton dépôt `of-tracker`
2. Clique sur **Settings** (en haut du dépôt)
3. Dans le menu de gauche, clique sur **Pages**
4. Sous "Build and deployment" → "Branch", choisis **main** et le dossier **/ (root)**
5. Clique **Save**
6. Attends 1-2 minutes, puis rafraîchis la page — ton lien apparaît en haut :
   `https://TON_USERNAME.github.io/of-tracker/`

C'est ce lien que tu utilises chaque jour, depuis n'importe quel appareil.

## Mettre à jour le site plus tard

Si tu modifies `index.html` (ou si je t'envoie une nouvelle version) :
```bash
git add .
git commit -m "Mise à jour"
git push
```
Le site se met à jour automatiquement en 1-2 minutes.

## Note sur les données

- Les fichiers (client + export ERP) sont traités **entièrement dans le
  navigateur** — rien n'est envoyé à GitHub ni à aucun serveur.
- Le dépôt GitHub étant **public**, n'importe qui connaissant le lien peut
  ouvrir l'outil (mais il aura besoin de tes fichiers pour voir tes données).
- Si la confidentialité de l'outil lui-même est un sujet chez toi, tu peux
  créer un dépôt **privé** — dans ce cas GitHub Pages gratuit ne fonctionne
  pas directement (il faut GitHub Pro, ou héberger ailleurs). Vérifie avec ton
  IT si besoin.

## L'historique (mémoire jour à jour)

Stocké dans le navigateur (`localStorage`) — reste tant que tu utilises le
même navigateur sur le même PC. Utilise les boutons "Exporter l'historique" /
"Importer l'historique" dans l'appli pour le sauvegarder ou le transférer sur
un autre appareil.
