# LEVELUP — levelup.mu

Site vitrine de **LEVELUP**, cabinet de transformation d'équipes fondé par **Diane Maigrot**, basé à l'île Maurice. Ateliers design thinking, sprints d'innovation IA et coaching qui ancrent le changement dans la durée.

**Production : [levelup.mu](https://levelup.mu)** — déployé automatiquement via Vercel à chaque push sur `main`.

---

## Stack technique

- **Un seul fichier** : `index.html` — HTML, CSS et JS inline, aucune dépendance ni build.
- **Bilingue FR/EN** : chaque texte porte des attributs `data-fr` / `data-en` ; la fonction `setLang()` bascule la langue et la préférence est persistée en `localStorage`.
- **Sécurité** : les injections HTML passent par `safeSetHTML()` (allowlist : `em|strong|sup|sub|span|br`).
- **SEO** : title/meta orientés "Design Thinking / Coaching Innovation / Ile Maurice", données structurées JSON-LD (`ProfessionalService`).
- **Polices** : Manrope (titres) + chargement non bloquant Google Fonts.
- **Responsive** : breakpoints 980px (tablette), 600px et 390px (mobile). Le visuel hero est masqué sur mobile.

### Palette

| Variable | Valeur | Usage |
|---|---|---|
| `--magenta` | `#E0185C` | Couleur principale (logo, CTA) |
| `--magenta-dk` | `#B81249` | Hover CTA |
| `--marigold` | `#FFB300` | Accents (points, badge) |
| `--ink` | `#111111` | Texte |
| `--cream` | `#F5F1EA` | Fonds doux |
| Dégradé icône | `#FFE4EE` → `#E0185C` → `#8C0030` | 3 chevrons du logo, repris sur les cartes Services |

---

## Structure de la page

1. **Nav** — liens ancres, bascule FR/EN, burger mobile.
2. **Hero** — H1 « Transformer vos équipes en moteurs d'innovation. », CTA « Réserver mon diagnostic offert », photo à droite (`hero-create.jpg`).
3. **Approche** (`#approche`) — comparatif « L'approche classique » (carte blanche) vs « Notre approche » (carte noire).
4. **Services** (`#services`) — 3 cartes colorées aux teintes du logo :
   - **1. Ateliers Design Thinking** (rose clair) — 1 à 3 jours, 8–40 personnes, sur-mesure.
   - **2. Sprints Innovation Produit ou Service** (magenta, « le plus demandé ») — 5 jours, 6–12 personnes.
   - **3. L'Innovation Challenge** (magenta foncé) — 3 à 6 mois, 5–6 équipes, bimensuel.
5. **Méthode** (`#methode`) — 4 étapes : Diagnostic → Ateliers → Accompagnement (3 à 6 mois) → Suivi.
6. **Fondatrice** (`#fondatrice`) — portrait (`diane-portrait.jpg`), bio, tags, LinkedIn. Texte centré verticalement avec la photo.
7. **Programmes** (`#programmes`) — les 6 ateliers (voir `docs/ATELIERS.md`), chacun avec CTA devis `mailto:hello@levelup.mu`.
8. **Cas clients** (`#cas-clients`) — 3 témoignages au format avant/après.
9. **Contact** (`#contact`) — « Prêt à faire grandir vos équipes ? / Ready to grow with your team? ».
10. **CRO** — CTA flottant (desktop) + barre sticky (mobile), libellé unifié « Réserver mon diagnostic offert ».

## Fichiers

| Fichier | Rôle |
|---|---|
| `index.html` | Tout le site |
| `hero-create.jpg` | Photo hero actuelle (« Create Change ») |
| `hero-bulb.jpg`, `hero-sign.png`, `team-photo.jpg` | Anciennes photos hero (conservées) |
| `diane-portrait.jpg` | Portrait de la fondatrice |
| `docs/ATELIERS.md` | Contenu détaillé bilingue des 6 ateliers |
| `docs/HISTORIQUE.md` | Décisions éditoriales & design prises pendant la construction |

---

## Déploiement & domaine

- **Vercel** : projet lié à ce repo, déploiement auto sur push `main`. URL de secours : `levelup-mu-tan.vercel.app`.
- **Domaine OVH** : `levelup.mu`
  - A `@` → `76.76.21.21`
  - CNAME `www` → `cname.vercel-dns.com.`
  - Après modification DNS : bouton **Refresh** sur Vercel → Settings → Domains. Certificat SSL généré automatiquement (jusqu'à 24 h de propagation).

## Modifier le site

1. Éditer `index.html` (chaque texte existe en `data-fr` **et** `data-en` — toujours mettre à jour les deux).
2. Commit + push sur `main` → Vercel déploie en quelques secondes.
3. Pour une nouvelle photo hero : ajouter le fichier au repo et changer le `src` de `.hv-photo`.
