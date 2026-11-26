# Atelier IA · Claude × Gemini

Ma page perso pour poser une question et l'envoyer au bon assistant, Claude ou Gemini, depuis l'iPhone, l'iPad ou l'ordinateur.

## Deux modes

- **Apps** (par défaut) : la page choisit Claude ou Gemini, affine la demande, la copie et ouvre l'app. Tout passe par mes abonnements Claude Pro et Gemini Pro, sans frais en plus. Si le champ de l'app reste vide, il suffit de coller.
- **Ici** : la réponse s'affiche directement dans la page, en direct. Il faut une clé API (réglages ⚙️) :
  - Gemini : clé gratuite (avec limites) sur https://aistudio.google.com/apikey
  - Claude : clé payante à l'usage sur https://console.anthropic.com/settings/keys (séparée de l'abonnement Pro)

  Les clés restent dans le navigateur de l'appareil (localStorage) et ne partent que vers Anthropic et Google. Sans clé, la page ouvre l'app à la place.

## Routage automatique

En mode **Auto**, la page envoie vers :
- **Gemini** : actualités et recherche web, lieux et trajets, YouTube, images et vidéos à créer, Gmail / Drive / Agenda, recherche approfondie (Deep Research).
- **Claude** : rédaction (emails, lettres, CV), analyse et décisions, organisation, explications, code, traduction, longs textes.

On peut toujours forcer Claude, Gemini ou ChatGPT (version gratuite, ouverture dans l'app seulement) avec le sélecteur.

## Sécurité

- Le site ne contient aucun secret : c'est une page statique, sans serveur ni compte.
- Les clés API sont facultatives et restent sur l'appareil. Avec un **code de verrouillage** (réglages), elles sont chiffrées (AES-256, clé dérivée du code par PBKDF2) et le code est demandé une fois par session.
- L'historique reste sur chaque appareil, il n'est pas synchronisé.

## Installer sur l'iPhone / l'iPad

1. Ouvrir la page dans Safari.
2. Bouton Partager → **Sur l'écran d'accueil**.
3. L'Atelier s'ouvre ensuite en plein écran comme une app.

## Astuces

- `https://<page>/?q=ma question` préremplit la demande, et `&to=gemini` ou `&to=claude` force l'assistant. Pratique avec l'app Raccourcis d'iOS.
- « Mon utilisation » ouvre le tableau de bord de consommation Claude × Gemini.

## Publication

Site statique, publié avec GitHub Pages (branche `main`, dossier racine). Aucun serveur, aucune dépendance.
