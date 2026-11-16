# Budget

Gestionnaire de budget par enveloppes, **100 % local** : aucune donnée ne quitte l'appareil, aucune IA externe — toute l'« intelligence » tourne dans ton navigateur.

## Pratique
- **Ajout rapide en langage naturel** : « 12,50 boulangerie hier », « +1850 salaire », « virement 100 livret », « 45 essence vendredi »
- Catégorisation automatique : mémoire des libellés, mots appris, dictionnaire de commerces français
- Opérations récurrentes automatiques, virements entre comptes, import de relevé CSV bancaire (anti-doublons), export CSV
- Report d'enveloppe, budget par défaut, annuler une suppression, recherche, thème sombre, installable (PWA)

## Intelligent
- **Reste à vivre** : solde hors épargne − récurrences à venir, en €/jour
- **Conseils** : enveloppe qui sera vide avant la fin du mois, abonnements détectés, hausse de prix, doublons probables, dépenses inhabituelles
- **Budgets suggérés** d'après tes 3 derniers mois, **simulateur « puis-je me l'offrir ? »**
- **Bilan du mois** rédigé automatiquement + calendrier des dépenses, courbe du solde sur 12 mois

## Ludique (désactivable)
Score de santé du budget /100, objectifs d'épargne avec plan mensuel, série de jours, 10 badges, confettis.

## Publier (GitHub Pages)
`index.html` en minuscules + `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png` à la racine. iPhone : Safari → Partager → « Sur l'écran d'accueil ». Exporte une sauvegarde de temps en temps.

## Correction rapide (v3)
- **Saisie rapide** : après l'ajout, le message propose « Corriger » (9 s) → un tap sur la bonne enveloppe/le bon compte. Avant d'enregistrer, les pastilles de l'aperçu (enveloppe ▾, compte ▾) sont aussi cliquables.
- **Dans la liste** : touche la pastille de compte ou d'enveloppe d'une opération pour la changer en un geste (« ＋ enveloppe » en orange si absente). « Annuler » est toujours proposé ; changer l'enveloppe propose aussi de corriger les autres opérations du même libellé.
- **Sélection multiple** : « ☑ Sélectionner » → cocher → Enveloppe / Compte / Supprimer en lot.
- Filtre « ⚠️ Dépenses sans enveloppe » pour repérer les oublis.

## Espaces Perso / Pro (v4)
- **Interrupteur Tout / 👤 Perso / 💼 Pro** en haut de l'accueil (rappel dans l'en-tête). Chaque espace filtre comptes, enveloppes, opérations, récurrentes et objectifs. Les virements perso ↔ pro apparaissent des deux côtés.
- **Créer l'espace pro** : un compte pro + 24 catégories préétablies inspirées de Sensations Macarons, modifiables (Réglages → « Compléter les catégories pro »).
  - Recettes : ventes marchés, en ligne, commandes & événements, pros/revendeurs, ateliers, autres.
  - Charges fixes : assurance pro, loyer & local, énergie, site web, logiciels, banque, cotisations & impôts, comptable, crédits & leasing.
  - Charges variables : ingrédients, chocolat/crèmes/parfums, colorants & arômes, emballages, étiquettes & rubans, stands & marchés, transport, marketing, équipement, formation, frais de paiement, autres.
- **Tableau de bord pro** : trésorerie, recettes, charges, résultat ; **organigramme de santé** (Santé → Résultat → Marge brute → Recettes / Charges variables, Charges fixes ; Trésorerie et autonomie) avec voyants ✅ ⚠️ ⛔, point mort, détail par catégorie et 6 derniers mois.
- Saisie rapide pro : « +250 marché samedi », « 45 emballage boîtes », « 120 assurance pro » rangent automatiquement dans la bonne catégorie.
- Déplacer une opération d'un compte perso vers un compte pro (pastille compte) propose directement la bonne catégorie.

## Mise à jour v5
- **Enveloppes** : Recettes, Charges variables et Charges fixes sont repliées par défaut ; un chevron ▸/▾ les déplie.
- **Accueil** : les cartes (Solde total / Trésorerie, Revenus / Recettes, Dépenses / Charges, Reste du mois / Résultat) sont cliquables. Le solde ouvre les comptes, les autres ouvrent la liste des opérations du mois correspondantes (filtre retirable par la pastille ×).
