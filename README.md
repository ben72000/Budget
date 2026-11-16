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

## Mise à jour v6
- **Date de fin de récurrence** : dans la fiche d'une récurrence, champ « Jusqu'au (optionnel) ». Vide = répétition indéfinie ; sinon la dernière occurrence est celle qui tombe au plus tard à cette date (« Sans fin » pour l'effacer). La liste affiche « sans fin », « jusqu'au … » ou « terminée le … », et les prévisions ignorent les occurrences après la date de fin.
- **Livraison** : tout est dans un seul dossier `budget-app` (zip) — décompresse-le et garde les fichiers ensemble.

## Mise à jour v7
- **Jauges d'enveloppe bidirectionnelles** (Enveloppes, accueil, catégories pro) : le zéro est au milieu. Le vert part vers la droite quand il reste de l'argent, le rouge vers la gauche en cas de dépassement ; une enveloppe à zéro reste sans couleur. Pleine jauge = tout le budget disponible (vert) ou 100 % du budget dépassé (rouge).

## Mise à jour v8 — Scan de tickets et factures
- **Où** : bouton 📷 dans la barre d'ajout rapide, bouton « 📷 Scanner » dans Opérations, entrée « Scanner un ticket » dans Plus.
- **Comment** : photo (ou image de la galerie) → lecture du texte sur l'appareil → écran « Vérifier le ticket » : commerçant, date, espace (👤 Perso / 💼 Pro), compte, et chaque ligne avec son enveloppe (modifiable). L'enregistrement crée une dépense par enveloppe (case à décocher pour une seule dépense) ; « Annuler » reste disponible.
- **Intelligence** : espace détecté d'après le commerçant (Metro, Promocash, Rajapack… → pro ; cinéma, supermarché… → perso) et les articles ; factures HT : les lignes sont ramenées au total TTC ; écart avec le total signalé ; l'appli retient tes corrections (article → enveloppe, commerçant → espace).
- **Moteur de lecture** : Tesseract.js, téléchargé depuis Internet à la première utilisation (connexion requise ce jour-là), puis exécuté localement : l'image ne quitte jamais l'appareil. Sans connexion : « Coller le texte du ticket » (iPhone : appui long sur le texte de la photo → Texte en direct → copier).

## Mise à jour v9
- **Enveloppes → « Dépensé » cliquable** (souligné, avec ›) : ouvre les lignes de l'enveloppe pour le mois affiché. Chaque ligne se modifie sur place (libellé, montant, date, compte), se supprime (× avec « Annuler ») ou s'ouvre en fiche complète (✎). Une zone « + Ajouter une ligne » en bas crée une dépense dans l'enveloppe (Entrée sur le montant pour valider). Pour une enveloppe de recettes, le raccourci s'appelle « Encaissé ».

## Version 10 — Transferts entre enveloppes & Historique

- **⇄ Transférer** (Enveloppes, icône ⇄ sur chaque ligne, menu Plus) : déplace du budget d'une enveloppe à une autre (même espace perso/pro), avec montant, « tout le disponible », date et motif. Bloqué si le disponible est insuffisant. Modifiable, supprimable, annulable.
- Le transfert s'applique au budget du mois de sa date ; un tag ⇄ s'affiche sur l'enveloppe et la feuille « Dépensé » liste les transferts du mois.
- **🕘 Historique** (Plus, ou bouton dans Enveloppes) : journal daté de toutes les opérations et transferts, avec l'origine de chacune (saisie, saisie rapide, scan, récurrence, import, ajustement) et la date/heure de création. Filtres et recherche.
- Les opérations antérieures sont classées par origine déduite (récurrence, scan, ajustement, sinon saisie).

## Version 11 — Calendrier prévisionnel

- **📅 Prévisionnel** (menu Plus, ou bouton dans Récurrentes) : calendrier visuel des opérations récurrentes et des opérations datées dans le futur.
- Espace au choix : 👤 Perso, 💼 Pro ou Perso + Pro combinés. Horizon : 1, 3 ou 6 mois.
- Synthèse : solde d'aujourd'hui, solde projeté, point bas (alerte s'il passe sous 0), total des revenus et dépenses prévus, courbe d'évolution du solde.
- Chaque jour est coloré (vert = entrée, rouge = sortie) avec le net du jour ; toucher un jour affiche son détail.
- Simulation : décocher une récurrence pour voir le solde sans elle, ou ajouter un événement fictif (🧪) — rien n'est écrit dans tes vrais comptes. « Réinitialiser » remet tout à zéro.
- Le solde porte sur les comptes courants (hors épargne) de l'espace choisi.

## Version 12 — Refonte design (principes Apple HIG)

Refonte visuelle selon les règles du skill « apple-design-skill » (Human Interface Guidelines) ; aucune fonctionnalité modifiée.
- **Couleurs** : 6 jetons nommés clair/sombre, tous ≥ 4,5:1 (texte 17:1, accent framboise 6,7:1). Une couleur = un sens : framboise = action, vert = entrée/disponible, rouge = sortie/dépassement, ambre = vigilance. Espace pro : accent violet.
- **Typographie** : texte 17 px, titres de page 28 px, aucun texte sous 12 px.
- **Cibles tactiles** : 44 px par défaut (36 px minimum pour les actions secondaires).
- **Matériaux** : effet verre uniquement sur l'en-tête et la barre d'onglets (désactivé si « réduire la transparence »).
- **Feuilles** : poignée, coins arrondis larges. **Mouvement** réduit si demandé ; **contraste renforcé** pris en charge ; anneau de focus visible.
- Mode sombre sur vrai noir, couleurs adaptées.

## Version 13 — Récurrences projetées sur les mois à venir

- Correction : une opération récurrente n'était créée qu'à son échéance, donc les mois futurs (ex. décembre) n'affichaient rien.
- Désormais chaque occurrence à venir (jusqu'à 24 mois, en respectant la date de fin et les récurrences en pause) est comptée en **« prévu »** : dans le « Dépensé » et le « Disponible » de l'enveloppe, dans les totaux Revenus/Dépenses du mois, et dans le tableau de bord pro.
- La mention « dont X € prévu » s'affiche ; la feuille « Dépensé » liste les récurrentes à venir.
- Le report d'enveloppe tient compte du prévu. Les soldes de comptes restent inchangés (réels).
- À l'échéance, l'occurrence devient une vraie opération, sans double compte.
