<h1 align="center">🃏 League of Stones</h1>

<p align="center">
  <strong>Construisez votre deck, trouvez un adversaire et prenez le contrôle du plateau.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next.js">
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React">
  <img src="https://img.shields.io/badge/Zustand-443E38?style=for-the-badge" alt="Zustand">
  <img src="https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express">
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB">
</p>

## 🎮 Le jeu

League of Stones est un jeu de cartes multijoueur au tour par tour inspiré de Hearthstone et de l'univers de League of Legends.

Deux joueurs s'affrontent avec leur propre deck de champions. Il faut gérer sa main, poser les bonnes cartes, attaquer au bon moment et faire tomber les **150 points de vie** de l'adversaire.

Ce projet a été réalisé en groupe pendant la **Licence 3 MIASHS** à l'Université Toulouse - Jean Jaurès.

## ✨ Fonctionnalités

- 🔐 inscription, connexion et gestion du profil ;
- 🦸 collection de champions ;
- 🧩 création d'un deck de exactement 20 cartes ;
- 💾 trois emplacements de sauvegarde locale ;
- 🔎 file d'attente et recherche d'adversaires ;
- ⚔️ envoi et acceptation de défis ;
- 🎴 pioche, pose de cartes et attaques ;
- ❤️ gestion des points de vie et de la fin de partie ;
- 📱 interface adaptée aux ordinateurs et aux mobiles.

## 📜 Règles principales

| Élément | Règle |
|---|---|
| Points de vie | 150 par joueur |
| Main de départ | 4 cartes |
| Deck | Exactement 20 cartes |
| Plateau | 5 cartes maximum |
| Attaque | Une fois par carte et par tour |
| Nouvelle carte | Doit attendre le tour suivant |
| Attaque directe | Possible si le plateau adverse est vide |

## 🧱 Architecture

```text
.
├── leagueofront/       # Application Next.js
│   └── src/
│       ├── components/ # Composants partagés
│       ├── pages/      # Écrans du jeu
│       ├── services/   # Appels au backend
│       ├── store/      # État Zustand
│       └── styles/     # CSS Modules
├── League-Of-Stones/   # Serveur Express et MongoDB
└── Documentation/      # Conception et suivi du projet
```

## 🛠️ Technologies

| Partie | Technologies |
|---|---|
| Frontend | Next.js 16, React 19, CSS Modules |
| État client | Zustand et `localStorage` |
| Communication | API HTTP avec `fetch` |
| Backend | Node.js et Express |
| Données | MongoDB |

## 🚀 Lancer une partie en local

### 1. Démarrer le backend

MongoDB doit être lancé sur la machine.

```bash
cd League-Of-Stones
npm install
npm start
```

Le serveur écoute sur `http://localhost:3001`.

### 2. Démarrer le frontend

Dans un second terminal :

```bash
cd leagueofront
npm install
npm run dev
```

Ouvrir ensuite `http://localhost:3000`.

## ⚙️ Fonctionnement technique

Après la connexion, le frontend conserve la session dans Zustand et `localStorage`. Le matchmaking se rafraîchit périodiquement pour découvrir les joueurs disponibles, puis l'écran de partie interroge régulièrement le backend afin d'afficher le nouvel état du match.

Les appels HTTP sont centralisés dans `leagueofront/src/services/api.js`. Le backend expose les routes nécessaires aux utilisateurs, aux cartes, au matchmaking et aux combats.

## 🚧 Limites actuelles

- l'adresse du backend est fixée à `http://localhost:3001` ;
- MongoDB doit être lancé séparément ;
- le matchmaking et les parties utilisent du polling ;
- aucune suite de tests automatisés n'est configurée ;
- le backend possède des dépendances anciennes et reste destiné à un usage pédagogique local.

## 👥 Équipe

- Olti Mjeku
- Asmae Zaloufi
- Mohammed-Ali Chabana
- Karim Saïd
- Hyacinthe Waboe

<p align="center"><em>Un projet de groupe où développement web et stratégie de jeu se rencontrent. ⚔️</em></p>
