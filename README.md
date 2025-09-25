# Hello Brieux!

Une petite application web permettant de générer automatiquement des lignes formatées à partir d’adresses e-mail.

---

## Objectif
Transformer une liste d’emails en lignes respectant le format suivant :

```
PR|FR|<Courtier>|||||<email>||||FR|CRG|<Date>|True||False||<Date>
```

- `<Courtier>` : le courtier saisi par l’utilisateur.
- `<email>` : chaque adresse e-mail saisie.
- `<Date>` : la date choisie (toujours au format AAAA-MM-JJ).

---

##  Utilisation

1. Ouvrir [l’application déployée sur GitHub Pages](https://<ton-compte>.github.io/hello-brieux/) (après avoir activé Pages).
2. Remplir :
   - **Date** (au format AAAA-MM-JJ).
   - **Courtier** (obligatoire, aucune valeur par défaut).
   - **Emails** (plusieurs emails possibles, séparés par retour à la ligne, virgule, point-virgule ou espaces).
3. Cliquer sur **Générer les lignes**.
4. Copier le résultat ou télécharger le fichier `ouptut.txt`.

---

## ✅ Fonctionnalités
- Nettoyage automatique des doublons et espaces.
- Validation de base des emails.
- Génération d’un fichier texte prêt à l’emploi.
- Interface simple, responsive et utilisable depuis un navigateur.

---

## 🛠 Déploiement
1. Créer un dépôt GitHub et y ajouter ce projet.
2. Mettre le fichier `index.html` à la racine.
3. Activer **GitHub Pages** dans **Settings → Pages**.
4. L’application est disponible à l’URL : `https://<ton-compte>.github.io/hello-brieux/`

---

## 📄 Licence
Projet publié sous licence **MIT**. Libre de réutiliser et modifier.
