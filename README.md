# League of Stones

Jeu de cartes multijoueur au tour par tour inspiré de Hearthstone et de l'univers de League of Legends.

Le projet a été réalisé en groupe pendant la Licence 3 MIASHS à l'Université Toulouse - Jean Jaurès. Ce dépôt réunit le frontend développé avec Next.js et le backend Express/MongoDB utilisé par l'application.

## Fonctionnalités

- inscription, connexion et gestion du profil ;
- collection de champions et construction d'un deck de 20 cartes ;
- trois emplacements de sauvegarde locale pour les decks ;
- file d'attente, défis et matchmaking entre deux joueurs ;
- plateau de jeu avec pioche, pose de cartes et attaques ;
- gestion des tours, des points de vie et de la fin de partie ;
- interface responsive pour ordinateur et mobile.

## Règles principales

- chaque joueur commence avec 150 points de vie et quatre cartes ;
- un deck contient exactement 20 cartes ;
- le plateau accepte au maximum cinq cartes ;
- une carte posée doit attendre le tour suivant avant d'attaquer ;
- chaque carte peut attaquer une fois par tour ;
- si le plateau adverse est vide, le joueur peut être attaqué directement.

## Technologies

| Partie | Technologies |
|---|---|
| Frontend | Next.js 16, React 19, CSS Modules |
| État client | Zustand et `localStorage` |
| Communication | API HTTP avec `fetch` |
| Backend | Node.js, Express |
| Données | MongoDB |

## Structure

```text
.
├── leagueofront/       # Application Next.js
│   └── src/
│       ├── components/
│       ├── pages/
│       ├── services/
│       ├── store/
│       └── styles/
├── League-Of-Stones/   # Serveur Express et accès MongoDB
└── Documentation/      # Documents de conception et de suivi
```

## Installation

Prérequis :

- Node.js 18 ou plus récent ;
- npm ;
- MongoDB en fonctionnement sur la machine.

### Backend

```bash
cd League-Of-Stones
npm install
npm start
```

Le serveur écoute sur `http://localhost:3001`.

### Frontend

Dans un second terminal :

```bash
cd leagueofront
npm install
npm run dev
```

L'application est alors disponible sur `http://localhost:3000`.

## Fonctionnement technique

Après l'authentification, le frontend conserve la session dans son store Zustand et dans `localStorage`. Les écrans de matchmaking et de partie interrogent régulièrement le backend pour obtenir l'état le plus récent.

Les appels HTTP sont regroupés dans `leagueofront/src/services/api.js`. Le backend fourni avec le projet expose les routes liées aux utilisateurs, aux cartes, au matchmaking et aux matchs.

## Limites actuelles

- l'adresse du backend est fixée à `http://localhost:3001` dans le frontend ;
- MongoDB doit être lancé séparément ;
- le matchmaking et la partie reposent sur du polling ;
- aucune suite de tests automatisés n'est configurée ;
- le backend utilise des dépendances anciennes et doit être considéré comme un serveur pédagogique local.

## Équipe

- Olti Mjeku
- Asmae Zaloufi
- Mohammed-Ali Chabana
- Karim Saïd
- Hyacinthe Waboe
