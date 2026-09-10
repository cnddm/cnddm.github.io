# Ma page de liens (LittleLink)

Page unique qui regroupe tous mes liens (Facebook, Instagram, YouTube...).
Site 100 % statique : aucun serveur, aucune base de donnees, aucun cout.

Base sur [LittleLink](https://littlelink.io) v3.11.0 (licence MIT).

---

## 1. Modifier mes liens

Tout se passe dans **`index.html`**. Les endroits a personnaliser sont marques
par `<<< A REMPLIR >>>`.

Pour chaque bouton, remplacez `href="#"` par le vrai lien :

```html
<a class="button button-instagram" href="https://instagram.com/monpseudo" ...>Instagram</a>
```

- **Supprimer un reseau** : effacez la ligne `<a ...>...</a>` correspondante.
- **Ajouter un reseau** : copiez-collez la ligne depuis `index.original.html`,
  qui contient les ~100 boutons disponibles (Discord, Spotify, Twitch, Telegram,
  Snapchat, Threads, PayPal, Signal, GitHub...).
- **Changer la photo** : remplacez `images/avatar.png` (128x128 px) et
  `images/avatar@2x.png` (256x256 px).
- **Theme** : ligne 15, `theme-auto` (suit le systeme), `theme-light` ou `theme-dark`.

Apres modification : ouvrez `index.html` dans un navigateur pour verifier,
puis publiez (voir section 3).

## 2. Mise en ligne (gratuite, via GitHub Pages)

L'hebergement choisi est **GitHub Pages** : gratuit, sans carte bancaire,
sans limite de trafic raisonnable, et l'adresse suit le compte.

1. Creer un compte GitHub avec l'adresse Proton dediee.
2. Creer un depot **public** nomme exactement `PSEUDO.github.io`
   (ou `PSEUDO` est le nom du compte GitHub).
3. Pousser ce dossier dedans (commandes en section 3).
4. Sur GitHub : **Settings > Pages > Source : Deploy from a branch >
   branche `main`, dossier `/ (root)`** puis *Save*.
5. Au bout de 1 a 2 minutes, le site est en ligne sur `https://PSEUDO.github.io`.

## 3. Publier une modification

```bash
git add -A
git commit -m "Mise a jour des liens"
git push
```

Le site se met a jour tout seul en une a deux minutes.

## 4. Passation a un nouveau proprietaire

Le compte GitHub a ete cree avec une adresse **Proton Mail dediee**.
Transmettre le projet revient donc a transmettre ce compte :

1. Donner l'adresse Proton + son mot de passe, et le mot de passe GitHub.
2. Le nouveau proprietaire change les deux mots de passe.
3. Il verifie qu'aucune double authentification n'est restee sur un
   ancien telephone (GitHub : *Settings > Password and authentication*).

**Avantage decisif de cette methode : l'URL `https://PSEUDO.github.io` ne
change pas.** Tous les liens deja partages (bio Instagram, QR codes, cartes
de visite) continuent de fonctionner.

Variante si l'on prefere garder son compte GitHub : ajouter la personne en
collaborateur (*Settings > Collaborators*), ou transferer le depot
(*Settings > General > Transfer ownership*). Attention : dans ce dernier cas
**l'URL change** puisqu'elle contient le nom du compte.

## 5. Nom de domaine personnalise (optionnel, payant)

Pour une adresse du type `monnom.fr` (environ 10 EUR par an) :
acheter le domaine, puis GitHub *Settings > Pages > Custom domain*.
Le HTTPS est fourni gratuitement par GitHub.

## Structure du projet

| Fichier / dossier      | Role                                              |
|------------------------|---------------------------------------------------|
| `index.html`           | **La page a editer**                              |
| `index.original.html`  | Version d'origine : catalogue de tous les boutons |
| `privacy.html`         | Page de confidentialite (a adapter ou supprimer)  |
| `css/brands.css`       | Couleurs officielles de chaque marque             |
| `images/icons/`        | Logos SVG                                         |
| `images/avatar.png`    | Photo de profil                                   |
| `docker/`, `wrangler.toml` | Hebergements alternatifs, inutiles ici        |
