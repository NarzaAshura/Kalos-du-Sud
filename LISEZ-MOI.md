# Atlas de Kalos du Sud

Site statique pour GitHub Pages. Tout le contenu est dans `data.json` ; `index.html` ne contient que l'affichage et l'éditeur.

## Mettre en ligne (une fois, propriétaire du dépôt)

1. Sur github.com : **New repository**, public, par exemple `kalos-du-sud`.
2. **Add file → Upload files** : glisser tout le contenu de ce dossier (y compris `img`, `portraits`, `sprites` et `.nojekyll`), puis **Commit changes**.
3. **Settings → Pages → Source : Deploy from a branch → main / (root) → Save**.
4. Une à deux minutes plus tard, le site est à `https://PSEUDO.github.io/kalos-du-sud/`.

## Comptes des modérateurs (pseudo + mot de passe)

Le propriétaire du site fait ceci une seule fois :

1. Créer une clé GitHub réservée au site : photo de profil → **Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**.
   - **Repository access** : *Only select repositories* → choisir le dépôt du site.
   - **Permissions → Repository permissions → Contents** : *Read and write*.
   - Choisir une durée, **Generate token**, copier la clé (`github_pat_…`).
2. Sur le site : **Accès modérateur**, coller la clé, **Se connecter**.
3. Dans la barre du bas : **Comptes des modérateurs**. Pour chaque modérateur, saisir son pseudo et un mot de passe d'au moins 12 caractères, puis **Créer le compte**.
4. Donner à chacun son pseudo et son mot de passe. Il clique sur **Accès modérateur**, les saisit, et peut ensuite changer son mot de passe avec **Mon mot de passe**.

À savoir :

- Chaque mot de passe verrouille une copie chiffrée de la clé, rangée dans `data.json`. Un mot de passe court pourrait être deviné par essais : les choisir longs.
- Le pseudo du compte signe les modifications dans le journal.
- **Retirer** un compte bloque ses prochaines connexions. Une personne déjà connectée garde l'accès sur son appareil tant que la clé n'est pas remplacée : pour une coupure immédiate, supprimer la clé sur GitHub, en créer une nouvelle (étapes 1 et 2) et recréer les comptes.
- Quand la clé expire, même manœuvre.

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
- Sprites : les formes delta de Pokémon Insurgence s'affichent d'elles-mêmes. Pour un delta maison ou une fusion, utiliser le champ **Sprite personnalisé** du Pokémon.
