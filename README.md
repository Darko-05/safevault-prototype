# SafeVault – Prototype interactif

Prototype de cours (IHM) : déposer et partager un document confidentiel en trois écrans.
Site statique : un seul fichier `index.html`, aucune installation, aucun serveur.

## Contenu

- `index.html` : le prototype (HTML, CSS et JavaScript)
- `favicon.svg` : l'icône de l'onglet
- `vercel.json` : réglages de déploiement (URL propres, en-têtes de sécurité)

## Tester en local

Ouvrir `index.html` dans un navigateur. Il n'y a rien d'autre à lancer.

## Déployer sur Vercel

Le projet est un site statique : pas de commande de build, pas de dossier de sortie.

### Option A : avec GitHub (sans terminal)

1. Créer un dépôt GitHub et y envoyer ces fichiers (bouton « Add file » puis « Upload files »).
2. Sur vercel.com, choisir « Add New… » puis « Project », et importer le dépôt.
3. Laisser « Framework Preset » sur **Other**, ne rien mettre dans « Build Command » ni « Output Directory ».
4. Cliquer sur « Deploy ». Vercel donne une adresse en `.vercel.app` à partager aux autres groupes.

### Option B : avec la ligne de commande

```bash
npm install -g vercel
cd safevault-prototype
vercel login
vercel --prod
```

Répondre aux questions avec les valeurs par défaut (projet nouveau, dossier courant, pas de build).

## Récupérer les retours des testeurs

À la fin du test, chaque testeur obtient un résumé (durée, erreurs rencontrées, droits choisis, note de facilité, remarques) à copier.
Pour recevoir ces résumés dans un formulaire en ligne, renseigner son adresse dans `index.html`, tout en haut du script :

```js
var FEEDBACK_URL = 'https://…';
```

Un bouton « Envoyer à l'équipe » apparaît alors. Laissé vide, il reste masqué.

## À savoir

- Aucun e-mail n'est envoyé et aucun fichier ne quitte l'appareil du testeur : tout est simulé dans le navigateur.
- Les polices (Bricolage Grotesque, IBM Plex Sans) se chargent depuis Google Fonts. Hors connexion, le texte utilise une police du système.
