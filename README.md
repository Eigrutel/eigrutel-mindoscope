# mindoscope

**Version 1.0.0 · 17-11-2026**

Application de cartes mentales conçue et développée par **Simon Léturgie** dans le cadre d’**Eigrutel BD Academy** et d’**Eigrutel Lab - Atelier d’outils libres pour la bande dessinée**.

[Ouvrir l’application](https://eigrutel.github.io/eigrutel-mindoscope/mindoscope.html) · [Présentation](https://eigrutel.github.io/eigrutel-mindoscope/) · [Télécharger](https://github.com/Eigrutel/eigrutel-mindoscope/releases/latest)

## Français

### Présentation

Créer plusieurs cartes mentales avec du texte, des images, des notes, des liens et des formes. Utiliser une application web autonome FR/EN, sans compte, serveur applicatif ni dépendance distante nécessaire à son fonctionnement.

### Fonctionnalités

- Cartes multiples et cellules reliées ou indépendantes.
- Placement libre et dispositions automatiques dans plusieurs directions.
- Déplacement et repli des branches, annulation/rétablissement, deux vues et une troisième compacte facultative.
- Images recadrables et notes de cellules.
- Liens multiples avec styles, flèches, précisions et images.
- Typographies des niveaux 1 à 5, import et retrait de polices personnalisées.
- Couleurs, transparence, fond par carte et mode nocturne.
- Sélection et modification groupées des cellules et des liens.
- Formes : rectangles, ovales, nuages et accolades, avec poignées et rotation.
- Transmission du style du parent, avec ou sans typographie.
- Recherche dans l’ensemble des cartes et des notes.
- Verrouillage des modifications, en conservant navigation, sauvegardes et exports.
- Import des formats pris en charge d’Univers, de Pop et de Markdown, ainsi que des diaporamas HTML d’Univers.
- Export PDF avec notes visibles facultatives et URL cliquables ; export Markdown.

### Lancer

1. Télécharger et décompresser l’archive.
2. Conserver mindoscope.html et le dossier favicon côte à côte.
3. Ouvrir mindoscope.html dans un navigateur moderne, ou utiliser la version hébergée.
4. Sur iPhone/iPad, privilégier Safari avec l’adresse hébergée plutôt que l’aperçu de l’application Fichiers.
5. Ouvrir « i » pour consulter le mode d’emploi.

[Mode d’emploi français](docs/UTILISATION.md)

### Sauvegarder

Utiliser la disquette pour enregistrer la carte active ou toutes les cartes dans un fichier **.mindo**. Le fichier contient des données JSON, les images et les polices importées. Le bouton dossier permet de l’ouvrir en ajoutant les cartes à celles déjà présentes.

Continuer à ouvrir les anciens fichiers .mindmap et .mindmaps. Les identifiants de stockage des versions de développement sont conservés.

La mémorisation locale utilise IndexedDB ; les préférences utilisent localStorage. Elle dépend du navigateur et de l’origine du site, ne se synchronise pas entre appareils et peut disparaître lors d’un effacement des données. Conserver régulièrement des sauvegardes .mindo en dehors du navigateur.

### PDF et limites

Exporter la vue de la carte avec son fond, y compris nocturne, et les liens en gris. Ajouter facultativement les notes des éléments visibles contenant du texte ou une image. Exclure les descendants masqués par une branche repliée.

Le PDF incorpore une image de la carte et des annotations URL cliquables ; ce n’est pas un dessin vectoriel éditable. Une carte très étendue peut produire des textes petits sur une seule page.

Limites par carte : 1 000 cellules, 40 niveaux, 4 000 liens et 200 formes. Les images et polices volumineuses augmentent l’utilisation de mémoire.

### Vie privée

Aucun compte, suivi ou envoi des cartes à un serveur. Les données restent sur l’appareil ; les liens externes sont ouverts à la demande. Aucune synchronisation distante intégrée.

## English

### Overview

A standalone bilingual mind-mapping application designed and developed by Simon Léturgie for Eigrutel BD Academy and Eigrutel Lab. No account, application server or remote runtime dependency is required.

Create multiple maps with connected or independent cells, cropped images, notes, custom links and shapes. Use free placement or automatic layouts, fold branches, search across maps, edit multiple elements, import custom fonts, use night mode and lock editing.

Import supported Univers and Pop files, Univers HTML slideshows and Markdown. Export PDF with optional visible notes and clickable URLs, or Markdown text.

### Launch and save

Open mindoscope.html in a modern browser, keeping the favicon folder alongside it, or use the hosted application. On iPhone/iPad, prefer the hosted page in Safari to a file-manager preview.

Use the disk button to save one map or all maps as **.mindo** JSON files, including images and fonts. Use the folder to open files without replacing existing maps. Legacy .mindmap and .mindmaps backups remain supported.

Maps are stored locally in IndexedDB and preferences in localStorage. Browser data is not synchronised across devices and may be removed by clearing storage. Keep regular file backups outside the browser.

[English user guide](docs/USAGE.md)

### PDF and limits

PDF maps are rasterised with clickable URL annotations, not editable vector artwork. Optional notes include visible elements containing text or an image, excluding descendants hidden by folded branches.

Per-map limits: 1,000 cells, 40 levels, 4,000 links and 200 shapes. Large maps, images and fonts may consume significant browser memory.

## Fichiers / Files

| Fichier | Rôle / Purpose |
| --- | --- |
| mindoscope.html | Application autonome / Standalone app |
| index.html | Présentation FR/EN / Landing page |
| favicon/favmind.png | Icône / Icon |
| docs/UTILISATION.md, docs/USAGE.md | Modes d’emploi / User guides |
| ARCHITECTURE.md | Organisation technique / Technical architecture |
| CHANGELOG.md | Historique / Changelog |
| LICENSES/ | Textes complets des licences / Full licence texts |
| LICENSE.md, NOTICE.md | Licences et attribution / Licences and attribution |

Aucune compilation, aucun dossier vendor ni script d’installation requis. / No build step, vendor folder or installation script is required.

## Licences

Copyright © 2026 Simon Léturgie.

- Code : GNU AGPL v3.0 ou version ultérieure / or later.
- Documentation et modèles / Documentation and templates : CC BY-SA 4.0, sauf mention contraire / unless otherwise noted.
- Marques, logos et signes distinctifs Eigrutel / Eigrutel Lab / Eigrutel BD Academy : réservés / reserved.

Consulter [LICENSE.md](LICENSE.md) et [NOTICE.md](NOTICE.md).
