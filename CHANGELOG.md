# Changelog

## 1.1.0 · 19-11-2026

### Français

- Raccorder Mindoscope au protocole de sauvegarde Projets, avec confirmation d’écriture et attente avant navigation.
- Isoler chaque projet de l’espace autonome : aucune lecture ni écriture du stockage autonome en mode intégré.
- Conserver toutes les cartes, leur ordre, les images, notes, styles de liens, formes, polices et réglages dans le JSON Projets.
- Importer aussi les cartes Mindoscope depuis un JSON Projets, en usage autonome ou intégré, avec choix Ajouter/Remplacer.
- Préserver les correctifs 1.0.1 et les imports historiques.

### English

- Connect Mindoscope to Projets with acknowledged saving and a flush before navigation.
- Isolate project workspaces from standalone storage.
- Keep the whole map collection, order, images, notes, links, shapes, fonts and settings in project JSON.
- Recover native Mindoscope maps from Projets exports in standalone or embedded mode, with Add/Replace.
- Retain 1.0.1 fixes and legacy imports.

## 1.0.1 · 19-11-2026

### Français

- Revenir aux sauvegardes .json ; conserver la lecture des anciens .mindo et retirer le filtre bloquant du sélecteur iPad.
- Conserver le cadrage au changement de vue.
- Éviter les coupures à l’intérieur des mots et harmoniser le calcul de largeur des cellules, avec espace suffisant pour les commandes.
- Proposer Ajouter ou Remplacer après validation complète de l’import ; remplacer automatiquement la carte de démarrage vide.
- Sauvegarder et restaurer les réglages, la langue et le thème ; conserver les styles de liens.
- Utiliser le trait simple par défaut pour les nouvelles branches.
- Réordonner les cartes depuis le bas des réglages, avec application ou annulation.
- Récupérer ensemble les cartes Univers et Pop! d’un export Projets, sans créer de carte Pop! vide.

### English

- Save as .json; retain legacy .mindo support and remove the restrictive iPad file-picker filter.
- Preserve framing when switching views.
- Avoid splitting words and harmonise cell sizing while leaving room for controls.
- Offer Add or Replace after validating the whole import; automatically replace the empty starting map.
- Save and restore settings, language and theme; preserve link styles.
- Default new branches to a solid line.
- Reorder maps at the bottom of settings, with Apply or Cancel.
- Import both Univers and Pop! maps from a Projects export, skipping empty Pop! data.

## 1.0.0 · 17-11-2026

Première version stable / First stable release.

### Français

- Cartes multiples, cellules indépendantes, dispositions automatiques et placement libre.
- Images recadrables, notes, liens multiples personnalisés et formes de regroupement.
- Typographies par niveau, polices importées, couleurs, transparence et style du parent.
- Sélection et modification groupées, recherche, annulation/rétablissement et verrouillage.
- Sauvegardes .mindo et compatibilité avec les versions de développement.
- Imports Univers, Pop et Markdown ; PDF avec notes visibles et URL cliquables.
- Interface FR/EN, mode nocturne, fond par carte et mode d’emploi actualisé.
- Correction des images masquées sous cadenas et du dossier invisible sur téléphone.
- Nettoyage et commentaires du code ; tests fonctionnels et analyse statique.
- Ajout de la page d’accueil et de la documentation.

### English

- Multiple maps, independent cells, automatic layouts and free placement.
- Cropped images, notes, multiple custom links and grouping shapes.
- Per-level typography, custom fonts, colours, transparency and parent styles.
- Bulk editing, search, undo/redo and editing lock.
- .mindo backups compatible with development versions.
- Univers, Pop and Markdown imports; PDF with visible notes and clickable URLs.
- French/English interface, night mode, per-map background and updated guide.
- Fixed images hidden by the lock and the missing folder icon on phones.
- Code cleanup, comments, functional tests and static analysis.
- Landing page and repository documentation.

## Avant 1.0.0 / Before 1.0.0

Versions de développement 0.1 à 0.28. Conserver leurs identifiants de stockage et accepter leurs sauvegardes.
Development versions 0.1 to 0.28. Storage identifiers and backup compatibility are preserved.
