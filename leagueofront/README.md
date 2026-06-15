# Frontend League of Stones

Interface Next.js du jeu League of Stones.

## Lancement

Le backend doit d'abord être lancé sur `http://localhost:3001`.

```bash
npm install
npm run dev
```

Ouvrir ensuite `http://localhost:3000`.

## Commandes

```bash
npm run dev
npm run build
npm run start
npm run lint
```

Le code de l'interface se trouve dans `src/`. Les appels au backend sont regroupés dans `src/services/api.js` et l'état d'authentification est géré avec Zustand dans `src/store/authStore.js`.
