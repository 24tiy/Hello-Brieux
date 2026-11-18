# Hello Brieux!

Convertisseur simple et rapide de fichiers *leads* vers le format interne **INIT_LEADS_PRFR_YYYYMMDD000003.csv**.  
Interface web légère, sans serveur, fonctionnant entièrement dans le navigateur.

---

## ⚙️ Fonctionnalités

- Lecture automatique des exports bruts (souvent en **UTF-16 + tabulations**)  
- Détection du séparateur et conversion vers **UTF-8 | pipe-séparé**  
- Application du même `broker` à toutes les lignes  
- Attribution automatique du téléphone mobile ou fixe (règle FR : 6/7 → mobile)  
- Génération du fichier au format :  
```

INIT_LEADS_PRFR_YYYYMMDD000003.csv

```
- Glisser-déposer du fichier n’importe où sur la page
- Aperçu avant téléchargement : nombre de leads, mobiles / fixes, lignes à vérifier (email manquant, mal formé ou en double, numéro hors +33) — purement informatif, le fichier généré reste identique
- Téléchargement direct, sans envoi de données vers un serveur
- Aucune dépendance externe : une seule page HTML, thème clair et sombre

---

## 🪶 Utilisation

1. Ouvrez [l’application en ligne](https://24tiy.github.io/Hello-Brieux/)
2. Glissez l’export brut (ex. Facebook/Instagram) sur la page, ou choisissez-le
3. Vérifiez le `broker` et la `date` (les codes fixes `PR · FR · FR · CRG` sont repliés)
4. Contrôlez l’aperçu, puis cliquez sur **Télécharger le CSV**
5. Le fichier normalisé est prêt à être utilisé dans vos outils internes DPR.

---

## 📄 Format de sortie

```

brand_code | country_code | partner_name | title | first_name | last_name | birthdate | email | zip_code | mobil_phone | fix_phone | language_code | collected_mode | creation_date | internal_consent | creation_date_internal_consent | partner_consent | creation_date_partner_consent | last_interaction_date

```

Les noms et prénoms sont conservés **tels qu’ils apparaissent** dans le fichier source.

---

## 🧭 Exemple rapide

Entrée :  
```

prénom   nom_de_famille   email                          phone_number
ALEXANDER  FOKINYAO         [mrbeaugosse@yopmail.com](mailto:mrbeaugosse@yopmail.com)  p:+336636666666

```

Sortie :  
```

PR|FR|PAID_LEAD||ALEXANDER|FOKINYAO||[mrbeaugosse@yopmail.com](mailto:mrbeaugosse@yopmail.com)||663666666||FR|CRG|2025-10-17|True||False||2025-10-17

```
---

## 🧑‍💻 Crédits

**Hello Brieux**  
Développé par *24tiy* pour un usage interne au sein de **DPR**.  
Aucune donnée n’est transmise ni stockée : tout s’exécute localement dans votre navigateur.
