# Terres & Troupeau — installation simple

## Le plus simple sur Android (recommandé)

1. Téléchargez `terres-troupeau-pwa.zip` et décompressez-le.
2. Déposez le contenu du dossier sur **GitHub Pages** ou **Netlify Drop** (gratuit). Vous obtenez une adresse web.
3. Ouvrez cette adresse dans Chrome Android.
4. Dans le menu ⋮ de Chrome, choisissez **Ajouter à l'écran d'accueil** / **Installer l'application**.
5. Ouvrez ensuite l'application depuis l'icône. Elle reste utilisable sans réseau après le premier chargement.

> Pour le mode hors-ligne complet, il faut ouvrir l'application depuis une adresse HTTPS. Une simple ouverture de `index.html` peut fonctionner pour la saisie, mais Chrome ne garantit pas le service worker hors ligne depuis un fichier local.

## Sur ordinateur ou réseau local

Dans le dossier décompressé, lancez un petit serveur local :

- Windows : installer Python, puis dans le dossier : `python -m http.server 8000`
- Linux/macOS : `python3 -m http.server 8000`

Ouvrez `http://localhost:8000`. Pour un téléphone sur le même Wi-Fi, utilisez l'adresse IP de l'ordinateur, par exemple `http://192.168.1.20:8000`.

## Données et sauvegardes

- Les données sont stockées sur l'appareil dans le navigateur (IndexedDB, avec une copie de secours locale).
- Utilisez régulièrement **Réglages → Exporter JSON** et conservez le fichier hors du téléphone.
- Pour restaurer : **Réglages → Importer une sauvegarde JSON**.
- CSV et Excel `.xls` sont des exports simples, ouvrables dans LibreOffice ou Excel.
- Effacer les données du navigateur peut supprimer les données : exportez avant toute réinitialisation.

## Ce qui est préchargé

- 76 parcelles issues du classeur PAC 2026, pour 109,58 ha admissibles.
- 32 lignes nommées de l'historique d'assolement, surface source 55,88 ha, campagnes 2020 à 2026 conservées quand renseignées.
- Codes et cultures provenant des classeurs fournis.
- Aucun produit, teneur d'effluent ou conseil agronomique n'est inventé : les référentiels sont à compléter et à valider.

## Fonctionnalités

Tableau de bord par campagne, journal d'interventions (semis, sol, fertilisation, traitements bio/phyto, récolte, irrigation, épandage), parcelles, assolement/historique, plan de fumure N/P/K, référentiels éditables, export/import JSON, export CSV et Excel `.xls`, interface mobile en français, PWA installable et cache hors ligne.

## À valider avant usage réglementaire

Les calculs du plan de fumure sont uniquement ceux permis par les teneurs saisies dans le catalogue : dose (t/ha) × teneur (kg/t) × surface apportée. Ils ne remplacent ni un conseil agronomique, ni une analyse de sol, ni la vérification des règles applicables en agriculture biologique, nitrates et registre phyto. Complétez notamment les besoins N/P/K par culture, reliquats, analyses, coefficients d'efficacité et produits avec leurs fiches/étiquettes.
