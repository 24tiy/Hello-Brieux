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
- Téléchargement direct, sans envoi de données vers un serveur

---

## 🪶 Utilisation

1. Ouvrez [l’application en ligne](https://<votre-nom>.github.io/hello-brieux/)  
2. Déposez votre fichier CSV brut (ex. export Facebook/Instagram)  
3. Renseignez si besoin le `broker` et la `date`  
4. Cliquez sur **Convertir & Télécharger**  
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
EVELYNE  BERTRAND         [eveelynebertrand75@hotmail.fr](mailto:eveelynebertrand75@hotmail.fr)  p:+33663697077

```

Sortie :  
```

PR|FR|PAID_LEAD||EVELYNE|BERTRAND||[eveelynebertrand75@hotmail.fr](mailto:eveelynebertrand75@hotmail.fr)||663697077||FR|CRG|2025-10-17|True||False||2025-10-17

```

---

## 🪩 Design

Inspiré de l’esthétique [air.inc](https://air.inc) :  
interface claire, fluide et sans surcharge, pensée pour un usage interne.

---

## 🧑‍💻 Crédits

**Hello Brieux**  
Développé par *24tiy* pour un usage interne au sein de **DPR**.  
Aucune donnée n’est transmise ni stockée : tout s’exécute localement dans votre navigateur.
```

