# Ma Bibliothèque

Site statique pour GitHub Pages : les livres du dossier `Books/` sont listés automatiquement, avec leur page de couverture (1ʳᵉ page du PDF ou image de couverture de l'EPUB) et un bouton de téléchargement.

## Mise en ligne

1. Créez un dépôt GitHub et envoyez-y `index.html` et le dossier `Books/`.
2. Dépôt → **Settings → Pages** → Source : *Deploy from a branch* → branche `main`, dossier `/ (root)` → Save.
3. Le site sera disponible sur `https://VOTRE-NOM.github.io/NOM-DU-DEPOT/`.

## Ajouter un livre

Déposez simplement le fichier dans `Books/` (via *Add file → Upload files* sur GitHub). La page lit le dossier via l'API GitHub : aucune autre modification n'est nécessaire.

## Notes

- Formats avec couverture : **PDF** et **EPUB**. Les autres formats reçoivent une couverture colorée avec leur titre.
- Si l'API GitHub est indisponible (limite de 60 requêtes/heure par visiteur), créez un fichier `books.json` à la racine : `["Livre 1.pdf", "Livre 2.epub"]`.
- Pour tester en local, ouvrez la page avec `?repo=VOTRE-NOM/NOM-DU-DEPOT` (les livres doivent être servis par un petit serveur, ex. `python -m http.server`).
- Les couvertures PDF utilisent la bibliothèque pdf.js, chargée depuis cdnjs uniquement quand il y a des PDF.
- Limite GitHub : 100 Mo par fichier.
