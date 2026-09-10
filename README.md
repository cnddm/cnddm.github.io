# Ma page de liens

Une page unique qui regroupe tous mes liens (Facebook, Instagram, YouTube…),
à partager en une seule adresse.

### 👉 Adresse du site : https://PSEUDO.github.io

Le site est gratuit et n'expire pas. Il n'y a rien à payer, rien à renouveler.

---

## Modifier un lien

**Aucun logiciel à installer.** Tout se fait depuis cette page GitHub, dans le navigateur.

1. Dans la liste de fichiers ci-dessus, cliquez sur **`index.html`**
2. En haut à droite du fichier, cliquez sur le crayon **✏️**
3. Cherchez la ligne du réseau concerné, par exemple Instagram :

   ```
   <a class="button button-instagram" href="#" ...>Instagram</a>
   ```

4. Remplacez le `#` par votre lien, **en gardant les guillemets** :

   ```
   <a class="button button-instagram" href="https://instagram.com/mon-compte" ...>Instagram</a>
   ```

5. Bouton vert **`Commit changes…`** en haut à droite, puis **`Commit changes`**
6. Attendez 1 à 2 minutes, puis rechargez le site. C'est en ligne.

> ⚠️ Ne touchez qu'à ce qui est **entre les guillemets** après `href=`.
> Le reste de la ligne fait fonctionner le bouton et son logo.

## Supprimer un réseau

Même méthode (étapes 1 à 2), puis effacez la ligne entière du réseau,
de `<a` jusqu'à `</a>`. Enregistrez comme à l'étape 5.

## Ajouter un réseau

Le fichier **`index.original.html`** contient une centaine de boutons tout prêts
(Discord, Spotify, Twitch, Telegram, Snapchat, Threads, PayPal, WhatsApp…).
Ouvrez-le, copiez la ligne du réseau voulu, collez-la dans `index.html`
au milieu des autres boutons, puis remplacez le `#` par votre lien.

## Changer le nom, la phrase ou la photo

Dans `index.html`, tout ce qui est personnalisable est signalé par un
commentaire **`<<< A REMPLIR >>>`** juste au-dessus.

Pour la photo : remplacez les fichiers `images/avatar.png` (128 × 128 pixels)
et `images/avatar@2x.png` (256 × 256 pixels) en gardant exactement ces noms.

## En cas d'erreur

Rien n'est jamais perdu : l'onglet **`Commits`** (en haut de la liste de fichiers)
garde l'historique de toutes les modifications, et permet de revenir en arrière.

---

## Changer de propriétaire

Ce site est rattaché à un **compte GitHub dédié**, créé avec une **adresse Proton Mail
dédiée**. Rien d'autre n'est lié à ce compte : le transmettre suffit.

1. L'ancien responsable transmet l'adresse Proton et les deux mots de passe
   (Proton et GitHub).
2. Le nouveau responsable **change immédiatement les deux mots de passe**.
3. Il vérifie qu'aucune double authentification ne pointe encore vers l'ancien
   téléphone : sur GitHub, *Settings → Password and authentication*.

**L'adresse du site ne change pas.** Les liens déjà imprimés ou publiés
(bio Instagram, QR codes, affiches, cartes de visite) continuent de fonctionner.

---

<details>
<summary>Informations techniques (pour un développeur)</summary>

Site statique basé sur [LittleLink](https://littlelink.io) v3.11.0 (licence MIT).
Aucun serveur, aucune base de données, aucun script.

**Hébergement** — GitHub Pages, dépôt public nommé `PSEUDO.github.io`,
*Settings → Pages → Deploy from a branch → `main` / `(root)`*.

**En local**

```bash
git clone https://github.com/PSEUDO/PSEUDO.github.io.git
cd PSEUDO.github.io
python -m http.server 8123   # puis http://localhost:8123
```

**Publier**

```bash
git add -A && git commit -m "Mise à jour des liens" && git push
```

| Fichier | Rôle |
|---|---|
| `index.html` | La page publiée |
| `index.original.html` | Catalogue LittleLink complet des boutons |
| `privacy.html` | Page de confidentialité |
| `css/brands.css` | Couleurs officielles des marques |
| `images/icons/` | Logos SVG |
| `docker/`, `wrangler.toml` | Hébergements alternatifs, non utilisés |

**Domaine personnalisé** (optionnel, ~10 €/an) — *Settings → Pages → Custom domain*.
HTTPS fourni gratuitement par GitHub.

</details>
