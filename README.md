# lx-remote-command

Ce dépôt contient des **commandes distantes** utilisables par `lx` pour le déploiement automatisé de services.

---

## Commandes disponibles

### `pull`

Effectue un `git pull` dans le répertoire du service afin de récupérer les dernières modifications du dépôt.

---

### `start`

Déploie une application **Node.js** en utilisant **PM2**.
A utiliser pour le premier déploiement.

---

### `Reload`

Redéploie une application **Node.js** en utilisant **PM2**. 
A utiliser pour les déploiements après avoir effectué le premier déploiement    avec start.

---


## Activation des commandes

Pour qu’une commande soit exécutable par `lx`, son nom doit être ajouté dans le fichier :

```text
.local/commands_enabled
```

Sans cette étape, la commande sera ignorée, même si le script existe.

---

## Notes

* Les commandes sont exécutées dans un **shell restreint**
* Seules les commandes listées dans `commands_enabled` sont autorisées
* Chaque commande peut être chaînée via GitHub Actions (`[cmd:pull][cmd:deploy]`)


