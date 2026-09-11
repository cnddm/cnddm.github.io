# Chœur Notre-Dame du Magnificat — page de liens

Page unique regroupant tous les liens du chœur, à partager en une seule adresse.

### 👉 https://cnddm.github.io

Le site est gratuit et n'expire pas. Il n'y a rien à payer, rien à renouveler.

---

## Pour modifier la page : l'application

Tout se fait avec le programme **« Ma page de liens »** — un seul fichier à
ouvrir, rien à installer. Il permet de changer les textes, le logo, l'image de
fond, d'ajouter ou retirer des boutons, puis d'envoyer le tout en ligne.

Demandez-le au responsable précédent : il ne se télécharge pas depuis cette
page, pour des raisons de sécurité.

> ### ⚠️ Ne modifiez pas les fichiers de ce dépôt à la main
>
> `index.html` et `privacy.html` sont **reconstruits automatiquement** par
> l'application à partir du fichier `contenu.json`. Une correction faite ici
> avec le crayon ✏️ serait **effacée sans prévenir** à la prochaine
> publication. Passez toujours par l'application.

Après un envoi, comptez une à deux minutes. Si le changement n'apparaît pas,
appuyez sur **Ctrl + Maj + R** : c'est presque toujours l'ancienne version
gardée en mémoire par le navigateur.

## En cas d'erreur

Rien n'est jamais perdu. L'onglet **Commits**, en haut de la liste des
fichiers, conserve l'historique de toutes les versions et permet de revenir
en arrière.

---

## Changer de responsable

Ce site est rattaché à un **compte GitHub dédié**, créé avec une **adresse
Proton Mail dédiée** (`choeurnddm@proton.me`). Rien d'autre n'est lié à ce
compte : le transmettre suffit.

1. L'ancien responsable transmet l'adresse Proton et les deux mots de passe
   (Proton et GitHub), **ainsi que le programme « Ma page de liens »**.
2. Le nouveau responsable change immédiatement les deux mots de passe.
3. Il vérifie qu'aucune double authentification ne pointe encore vers
   l'ancien téléphone : *Settings → Password and authentication*.

**L'adresse du site ne change pas.** Les liens déjà imprimés ou publiés
— bio Instagram, QR codes, affiches — continuent de fonctionner.

### Si l'application refuse de publier

Elle utilise un jeton d'accès GitHub qui peut expirer, être révoqué, ou être
supprimé par GitHub après un an sans usage. Dans l'application :
**4. Publier → Remplacer le jeton…**, et collez-en un neuf créé depuis le
compte du chœur (*Settings → Developer settings → Personal access tokens*,
avec le droit d'écriture sur ce dépôt).

---

<details>
<summary>Informations techniques (pour un développeur)</summary>

Site statique basé sur [LittleLink](https://littlelink.io) v3.11.0 (licence MIT).
Aucun serveur, aucune base de données, aucun script côté serveur.

**Hébergement** — GitHub Pages, dépôt public nommé `cnddm.github.io`,
*Settings → Pages → Deploy from a branch → `main` / `(root)`*.

**Le HTML est généré, pas écrit.** `contenu.json` est la source de vérité ;
`index.html` en est reconstruit intégralement à chaque publication, à partir
d'un gabarit. Le code de l'application et les gabarits ne sont pas dans ce
dépôt : ils vivent à part, l'exécutable contenant un jeton d'accès.

| Fichier | Rôle |
|---|---|
| `contenu.json` | Textes, liens et réglages — **la seule chose à modifier** |
| `index.html` | Page publiée, **générée automatiquement** |
| `privacy.html` | Page de confidentialité, **générée automatiquement** |
| `css/custom.css` | Fond, couleurs et boutons propres au chœur |
| `css/brands.css` | Couleurs officielles des marques (LittleLink, ne pas modifier) |
| `fonts/edosz.woff2` | Police du titre, Edo SZ |
| `images/` | Logo, image de fond et icônes des marques |

**Police du titre** — Edo SZ, de Vic Fieger (2008), sous licence
[1001Fonts Free For Commercial Use](https://www.1001fonts.com/licenses/ffc.html).
Usage personnel et commercial gratuit ; l'article 6 autorise explicitement
l'incorporation dans un site web et l'article 4 la conversion en WOFF2, tant
que la police n'est pas modifiée. Seule interdiction : revendre ou
redistribuer le fichier de police en tant que tel.

**Domaine personnalisé** (optionnel, ~10 €/an) — *Settings → Pages → Custom
domain*. Le HTTPS est fourni gratuitement par GitHub.

</details>
