# Atlas de Kalos du Sud

Site statique pour GitHub Pages. Tout le contenu est dans `data.json` ; `index.html` ne contient que l'affichage et l'éditeur.

## Mettre en ligne (une fois, propriétaire du dépôt)

1. Sur github.com : **New repository**, public, par exemple `kalos-du-sud`.
2. **Add file → Upload files** : glisser tout le contenu de ce dossier (y compris `img`, `portraits`, `sprites` et `.nojekyll`), puis **Commit changes**.
3. **Settings → Pages → Source : Deploy from a branch → main / (root) → Save**.
4. Une à deux minutes plus tard, le site est à `https://PSEUDO.github.io/kalos-du-sud/`.

## Accès des modérateurs par mot de passe

Le propriétaire du site fait ceci une seule fois :

1. Créer une clé GitHub réservée au site : photo de profil → **Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**.
   - **Repository access** : *Only select repositories* → choisir le dépôt du site.
   - **Permissions → Repository permissions → Contents** : *Read and write*.
   - Choisir une durée (un an au maximum conseillé), **Generate token**, copier la clé (`github_pat_…`).
2. Sur le site : **Accès modérateur**, coller la clé, **Se connecter**.
3. Dans la barre du bas : **Mot de passe des modérateurs**, choisir un mot de passe d'au moins 12 caractères, enregistrer.
4. Donner ce mot de passe aux modérateurs. Ils cliquent sur **Accès modérateur**, tapent leur pseudo et le mot de passe.

À savoir :

- La clé est rangée chiffrée dans `data.json`. Sans le mot de passe elle est illisible, mais un mot de passe court pourrait être deviné par essais : le choisir long.
- Toute personne qui a le mot de passe peut modifier le site. Le pseudo saisi signe le journal sur la bonne foi.
- Changer de mot de passe : refaire l'étape 3. Couper l'accès à tout le monde : supprimer la clé sur GitHub.
- Quand la clé expire, en créer une nouvelle et refaire les étapes 2 et 3.

## Modifier le site

- En mode modérateur, des boutons **✎ Modifier** et **+ Ajouter** apparaissent sur les fiches et les sections.
- Remplir le formulaire, écrire le **compte rendu** (obligatoire), **Enregistrer**.
- Le changement est visible tout de suite pour le modérateur, et sous une minute environ pour les lecteurs.
- Dans le journal, le bouton **Annuler cette modification** rétablit l'état précédent (30 dernières modifications).
- Chaque enregistrement est inscrit dans la section **Journal des modifications** (auteur, date, fiche, champs touchés, compte rendu) et dans l'historique GitHub du dépôt, qui permet de revenir en arrière.

### Formats de saisie

- Listes : un élément par ligne. Pour les « Informations », laisser une ligne vide entre deux éléments.
- Tableaux : une ligne par rangée, cellules séparées par ` | ` ; la première ligne donne les titres.
- Liens : `Libellé | https://…`, un par ligne.
- Épisodes : `Episode 441 | lien du message | repère | lien du repère` (les deux derniers sont facultatifs).
- Pokémon en texte libre : un par ligne ; le sprite est trouvé d'après le nom français.
- Portraits : bouton **Choisir une image** (l'image est recadrée en carré et envoyée dans `portraits/`), ou coller une adresse d'image.
- Sans divulgâchage : commencer une ligne ou un paragraphe par `{153}` le masque aux lecteurs qui n'ont pas atteint l'épisode 153. Le champ « Visible à partir de l'épisode » fait de même pour une fiche entière.
- Rubriques libres : une ligne `# Titre`, puis le texte en dessous.
- Relations : `Nom du personnage | lien`, une par ligne.
- Menu, images de la carte et de la couverture, catégories : bouton **Modifier l'accueil**.
