# MCC — Intranet Consortium

Espace de travail anticipatoire pour la réponse au marché public
« Ma Classe au Cinéma » — coordination nationale des missions d'éducation à l'image.

---

## Structure du dépôt

```
mcc-intranet/
├── index.html          ← shell unique (auth + navigation + iframe)
├── config.json         ← arborescence, statuts, flags admin/partage
├── modules/
│   ├── _placeholder.html   ← page affichée pour un module non encore produit
│   ├── P0-1.html
│   ├── P1-2.html
│   ├── P1-5.html
│   ├── P2-1.html
│   └── ...
└── README.md
```

---

## Déploiement GitHub Pages

1. Créer un dépôt **privé** sur GitHub (ex. `mcc-intranet`)
2. Pousser ce dossier à la racine du dépôt
3. Dans les paramètres du dépôt → Pages → Source : `main` / `/ (root)`
4. L'intranet est accessible à l'URL : `https://[compte].github.io/mcc-intranet/`

> ⚠️ Le dépôt doit rester **privé**. GitHub Pages sur dépôt privé nécessite
> un abonnement GitHub Pro ou Team.

---

## Mots de passe

Les mots de passe sont définis dans `index.html`, variable `PASSWORDS` (ligne ~120).
À modifier avant tout partage.

| Entrée | Accès |
|--------|-------|
| `mcc-admin-2025` | Mode administrateur — modules P0 visibles |
| `mcc-consortium-2025` | Mode consortium — P0 masqués |

---

## Ajouter un module

1. Produire l'artefact HTML dans une conversation Claude dédiée
2. Déposer le fichier dans `modules/` avec le nom exact : `P2-6.html`, `P3-2_A.html`, etc.
3. Mettre à jour `config.json` : changer `"status"` si nécessaire
4. Pousser sur GitHub

**Convention de nommage des fichiers :**
- Module simple : `P2-3.html`
- Module scénarisé : `P3-2_A.html`, `P3-2_B.html`
- Note de terrain : `SRC-archipel-ca.html`

**Convention de nommage storage (dans les modules HTML) :**
- Module simple : `mcc_P2-3`
- Module scénarisé : `mcc_P3-2_A`
- Note de terrain : `mcc_src_[identifiant]`

---

## Mettre à jour un statut

Éditer `config.json` et changer la valeur `"status"` pour l'entrée concernée.
Valeurs valides : `anticipé` · `en cours` · `à réviser` · `stabilisé` · `verrouillé` · `archivé`

---

## Basculement mode partage / admin

Les modules P0 (`"adminOnly": true` dans config.json) sont invisibles en mode consortium.
Le basculement est automatique selon le mot de passe saisi à l'entrée.
Aucune manipulation supplémentaire n'est nécessaire.

---

## Modules produits

| Module | Statut | Fichier |
|--------|--------|---------|
| P0-1 | stabilisé | à déposer |
| P1-2 | stabilisé | à déposer |
| P1-5 | stabilisé | à déposer |
| P2-1 | stabilisé | à déposer |
| … | … | … |
