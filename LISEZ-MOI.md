# Atlas de Kalos du Sud

Site statique pour GitHub Pages. Tout le contenu est dans `data.json` ; `index.html` ne contient que l'affichage et l'éditeur.

## Mettre en ligne (une fois, propriétaire du dépôt)

1. Sur github.com : **New repository**, public, par exemple `kalos-du-sud`.
2. **Add file → Upload files** : glisser tout le contenu de ce dossier (y compris `img`, `portraits`, `sprites` et `.nojekyll`), puis **Commit changes**.
3. **Settings → Pages → Source : Deploy from a branch → main / (root) → Save**.
4. Une à deux minutes plus tard, le site est à `https://PSEUDO.github.io/kalos-du-sud/`.

## Donner l'accès à un modérateur (propriétaire)

**Settings → Collaborators → Add people** : saisir le pseudo GitHub du modérateur. Il reçoit une invitation à accepter.

## Devenir modérateur (chaque modérateur, une fois)

1. Créer un compte gratuit sur github.com et donner son pseudo au propriétaire ; accepter l'invitation reçue par mail.
2. Créer une clé d'accès : photo de profil → **Settings → Developer settings → Personal access tokens → Tokens (classic) → Generate new token (classic)**.
   Donner un nom, choisir une durée, cocher la case **repo**, puis **Generate token**. Copier la clé (elle commence par `ghp_`) : elle n'est affichée qu'une fois.
3. Sur le site : **Accès modérateur**, vérifier le nom du dépôt (`PSEUDO/kalos-du-sud`), coller la clé, **Se connecter**.

La clé reste dans le navigateur de l'appareil utilisé. Sur un ordinateur partagé, cliquer sur **Quitter** après usage.

## Modifier le site

- En mode modérateur, des boutons **✎ Modifier** et **+ Ajouter** apparaissent sur les fiches et les sections.
- Remplir le formulaire, écrire le **compte rendu** (obligatoire), **Enregistrer**.
- Le changement est visible tout de suite pour le modérateur, et sous une minute environ pour les lecteurs.
- Chaque enregistrement est inscrit dans la section **Journal des modifications** (auteur, date, fiche, champs touchés, compte rendu) et dans l'historique GitHub du dépôt, qui permet de revenir en arrière.

### Formats de saisie

- Listes : un élément par ligne. Pour les « Informations », laisser une ligne vide entre deux éléments.
- Tableaux : une ligne par rangée, cellules séparées par ` | ` ; la première ligne donne les titres.
- Liens : `Libellé | https://…`, un par ligne.
- Épisodes : `Episode 441 | lien du message | repère | lien du repère` (les deux derniers sont facultatifs).
- Pokémon en texte libre : un par ligne ; le sprite est trouvé d'après le nom français.
- Portraits : bouton **Choisir une image** (l'image est recadrée en carré et envoyée dans `portraits/`), ou coller une adresse d'image.
