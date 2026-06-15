# 🖥️ Frontend League of Stones

Interface Next.js du jeu **League of Stones** : authentification, collection, création de decks, matchmaking et plateau de jeu.

![Next.js](https://img.shields.io/badge/Next.js-16-000000?logo=nextdotjs)
![React](https://img.shields.io/badge/React-19-20232A?logo=react)
![Zustand](https://img.shields.io/badge/État-Zustand-443E38)

## 🚀 Lancement

Le backend doit d'abord fonctionner sur `http://localhost:3001`.

```bash
npm install
npm run dev
```

L'interface est disponible sur `http://localhost:3000`.

## 🧰 Commandes

| Commande | Utilité |
|---|---|
| `npm run dev` | Lancer le serveur de développement |
| `npm run build` | Construire la version de production |
| `npm run start` | Lancer la version construite |
| `npm run lint` | Vérifier le code |

## 📂 Repères

- `src/pages/` : écrans de l'application ;
- `src/services/api.js` : appels HTTP ;
- `src/store/authStore.js` : session utilisateur avec Zustand ;
- `src/styles/` : styles globaux et CSS Modules.

> Le README principal du dépôt présente les règles du jeu et le lancement complet.
