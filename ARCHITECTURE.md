# Architecture de mindoscope

Version 1.1.0 · 19-11-2026

## Organisation

Application HTML/CSS/JavaScript vanilla dans mindoscope.html. Aucun framework, service distant, outil de compilation ou module chargé à l’exécution. index.html est une page de présentation indépendante.

## Données

Une collection contient plusieurs cartes et l’identifiant de la carte active. Chaque carte conserve cellules (nodes), liens (links), formes (regions), typographies de niveaux, polices incorporées, disposition et fond.

Une cellule possède un identifiant, un parent principal éventuel, du texte, des notes, un style et éventuellement une image et une position libre. Le parent principal définit le repli et les déplacements de branche. Les liens supplémentaires ne créent pas de nouvelle parenté.

Les liens ont des identifiants et numéros techniques, des extrémités, un type, un style et des précisions facultatives. Les formes conservent géométrie, rotation, opacité, couleur et ordre.

## Rendu et interactions

- HTML pour les cellules et champs de saisie.
- SVG pour les liens, formes et poignées.
- Coordonnées de carte séparées du déplacement et du zoom de la vue.
- Calcul commun des dimensions pour l’affichage, les dispositions et le PDF.
- Événements de pointeur pour déplacement, pincement et redimensionnement.
- Historique par instantanés, propre à chaque carte.
- Cadenas bloquant les modifications, avec exceptions pour navigation et exports. Les boutons contenant les images restent visibles.

## Persistance et compatibilité

IndexedDB conserve la collection ; localStorage conserve préférences et catalogue des polices. Les écritures sont sérialisées et différées après modification.

Conserver l’identifiant historique eigrutel-character-mindmap et la clé eigrutel-character-mindmap-v1 pour retrouver les anciennes données.

L’extension .json transporte du JSON pour une carte ou une collection, reconnue par son contenu. Lire aussi les anciennes extensions .mindo, .mindmap et .mindmaps. La version 1.1.0 accepte les versions de développement 0.1 à 0.28 et les séries 1.0.x et 1.1.x.

## Import et sécurité

Valider types, identifiants, parenté, cycles, profondeur, styles et limites de taille. Convertir séparément Univers, Pop et Markdown. Extraire uniquement les données JSON des diaporamas Univers ; ne pas exécuter leur code.

## Images, polices et PDF

Incorporer les images et les polices dans les sauvegardes. Conserver le cadrage séparément de l’image. Charger les polices via FontFace, avec polices de repli.

Dessiner la carte sur canvas avec son fond, puis incorporer le rendu JPEG dans le PDF. Ajouter les annexes de notes facultatives et les annotations URL. La carte n’est pas exportée en vectoriel.

## Maintenance

Les dictionnaires FR/EN alimentent l’interface. Le mode d’emploi est centralisé dans les deux langues.

Mettre à jour ensemble version, en-tête, compatibilité d’import, page d’accueil et documentation. Après modification, vérifier ajout de cellules, parenté, sauvegarde/réouverture, images, verrouillage, mobile, annulation, sélection et PDF. Compléter les contrôles automatisés par des essais Safari iPad/iPhone et navigateur de bureau.

## English summary

Single-file vanilla HTML/CSS/JavaScript application with a separate landing page. HTML cells and SVG links/shapes share map coordinates; view pan/zoom is separate.

IndexedDB stores collections; localStorage stores preferences. Keep historical application and storage identifiers for compatibility. Validate imports before use. Save JSON maps or collections as .json with embedded images/fonts. Export rasterised PDF pages with URL annotations. No build step is required.

## Import 1.0.1

Préparer et valider toutes les cartes avant de proposer Ajouter/Remplacer. Ne modifier les données existantes qu’après validation explicite, sauf pour la carte initiale vide. Garder le sélecteur de fichiers sans filtre `accept` pour les extensions personnalisées sur iPad ; contrôler les contenus JSON/Markdown/HTML dans le programme. Ajouter le champ optionnel `settings` aux sauvegardes individuelles et collections, sans changer leur schéma historique. Conserver le cadrage lors du changement de vue. Calculer les lignes par mots et réserver la largeur de texte sans compression flex.

## Raccordement Projets 1.1.0

Activer le mode intégré uniquement avec `?projets=1` dans une iframe. Fournir `window.EigrutelApp` et utiliser le canal `eigrutel-projets-v1` avec `appId: mindoscope`. Vérifier origine identique, fenêtre parent et identifiant de session. Le protocole utilise `ready`, `init`, `loaded`, `dirty`, `save`, `ack`, `clean`, `flush`, `save-error` et `error`.

Transporter une collection native `map-collection` avec toutes les cartes et `settings`. Valider les données et les images avant affichage. Attendre un accusé de réception de la révision envoyée ; une réponse ancienne ne marque pas une modification plus récente comme enregistrée. `flush` attend la lecture d’un fichier ou d’une police en cours avant l’instantané.

En mode intégré, ne jamais lire ni écrire IndexedDB ou localStorage de Mindoscope autonome. Projets possède la persistance. Réinitialiser uniquement les données Mindoscope du projet courant. Conserver le fonctionnement et les clés historiques en mode autonome. Le format JSON des collections reste en schéma 1.
