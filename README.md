# Budget

Gestionnaire de budget par enveloppes, **100 % local** : aucune donnée ne quitte l'appareil.

## Fonctionnalités
- Comptes, enveloppes (budget mensuel par défaut, report du solde au mois suivant), opérations (dépense, revenu, **virement** entre comptes)
- Opérations **récurrentes** (loyer, salaire, abonnements) créées automatiquement
- Mémorisation libellé → enveloppe, recherche, annuler une suppression
- Graphiques : répartition des dépenses, revenus vs dépenses sur 6 mois, « reste par jour »
- **Import de relevé bancaire CSV** (détection des colonnes, anti-doublons), export CSV (Excel)
- Sauvegarde / restauration JSON, thème clair/sombre, installable sur l'écran d'accueil (PWA)

## Fichiers
`index.html` (l'appli, fonctionne seule), `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png` (installation + mode hors ligne).

## Publier sur GitHub Pages
1. Le fichier doit s'appeler `index.html` **en minuscules**.
2. Settings → Pages → Branch `main` / racine.
3. iPhone : Safari → Partager → « Sur l'écran d'accueil ».

Les données sont dans le `localStorage` du navigateur : exporte une sauvegarde de temps en temps.
