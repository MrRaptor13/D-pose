# D-pose

**Dossiers clients, tâches et documents déposés, au même endroit.**

D-pose est un gestionnaire de tâches par dossier client avec dépôt de documents. Il tient dans **un seul fichier HTML** (`d-pose.html`), sans serveur ni bibliothèque externe, et s’intègre dans un site Google Sites.

---
## Test de fonctionalités
Le test utilise des entreprise et taches fictives.
https://sites.google.com/view/d-pose/accueil

---

## Fonctionnalités

- **Dossiers clients** : création, modification, suppression, recherche par numéro ou par nom.
- **Tâches et sous-tâches** : intitulé, description, priorité (Faible, Normal, Élevé, Urgent), échéance, statut.
- **Statut modifiable directement dans la liste** : À faire, En cours, En attente, Terminé.
- **Dépôt de documents** : un ou plusieurs fichiers par tâche ou sous-tâche, téléchargement et suppression.
- **Suivi** : compteurs (à réaliser, terminées, en retard), alerte visuelle des tâches en retard, avancement des sous-tâches (« 2 / 3 terminées »).
- **Filtres et tris** : par statut, priorité, retard ; tri par échéance, priorité, statut ou date de création.
- **Affichage adapté** : ordinateur, tablette et téléphone ; fenêtres de saisie qui défilent si la zone intégrée est petite.

---

## Intégration dans Google Sites

1. Ouvrez votre site en modification.
2. Menu **Insérer** puis **Intégrer**, onglet **Code intégré**.
3. Ouvrez `d-pose.html` dans un éditeur de texte, copiez **tout** son contenu et collez-le dans la zone.
4. Validez, puis agrandissez le bloc : une hauteur d’au moins 700 px est conseillée. La page défile à l’intérieur du bloc.
5. Publiez le site.

### Ce qui a été corrigé pour Google Sites

Le fichier d’origine était incomplet : le balisage de la page (en-tête, listes, fenêtres de saisie) et la majeure partie des styles étaient remplacés par des « existing code », donc rien ne pouvait s’afficher correctement. La page est reconstruite en entier, avec :

- une structure HTML complète et un affichage adaptatif (aucune hauteur d’écran imposée) ;
- un **repli en mémoire** si le navigateur bloque le stockage dans le bloc intégré, avec un bandeau d’avertissement au lieu d’une erreur à chaque action ;
- aucune ressource externe (polices, scripts, images).

---

## Limites à connaître

- **Données locales à chaque navigateur.** Tâches et documents sont enregistrés dans le navigateur de la personne qui les saisit (stockage local et IndexedDB). Ils ne sont **pas partagés** entre collaborateurs ni entre appareils.
- **Stockage bloqué dans certains sites intégrés.** Si le bandeau orange apparaît, les données ne survivent pas à la fermeture de la page. Ouvrir la page dans son propre onglet règle le problème.
- **Sauvegarde.** Vider les données du navigateur efface tâches et documents. Gardez les documents importants ailleurs.
- **Non testé dans Google Sites même.** Le fonctionnement a été vérifié dans un navigateur simulé (création, statut rapide, filtres, dépôt de fichier, stockage bloqué). Vérifiez le dépôt et le téléchargement de fichiers une fois la page intégrée, car certains sites intégrés restreignent les fenêtres de sélection de fichier.

Pour un usage collaboratif réel (plusieurs personnes, mêmes données), il faut une base de données partagée, comme dans le projet D-lai.

---

## Données d’exemple

Au premier lancement, deux dossiers et cinq tâches d’exemple sont créés pour montrer le fonctionnement. Supprimez-les depuis l’interface.
