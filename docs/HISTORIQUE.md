# Historique des décisions — LEVELUP.MU

Résumé des choix éditoriaux et design faits pendant la construction du site (sessions Claude Code, 2026). Permet de reprendre le travail sans l'historique de chat.

## Identité & contenu

- **Fondatrice** : Diane Maigrot — *8 ans* à la tête de La Turbine (incubateur de référence à l'île Maurice), 120+ équipes transformées depuis 2016, 20+ ans d'expérience entrepreneuriale. Ligne éditoriale : « l'humain au cœur » de chaque projet.
- **Tags fondatrice** : Innovation · Coaching individuel ou d'équipes · Transformation · Leadership (le tag « Design Thinking » a été retiré).
- **Citation Mandela** (« It always seems impossible until it's done. ») : d'abord en overlay sur le portrait, puis en encadré sous la bio, finalement **supprimée**.
- **H1 hero** : « Je vous accompagne vers une transformation positive et durable. » (a remplacé « Transformer vos équipes en moteurs d'innovation. », lui-même choisi contre une variante urgence « en 90 jours »). Sous-titre : « Offrez-vous, ainsi qu'à vos équipes, les outils et le support nécessaires pour devenir des acteurs engagés de votre organisation. »
- **CTA principal unifié partout** : « Contactez-moi ! » / « Contact me! » — hero, CTA flottant desktop, barre sticky mobile (a remplacé « Réserver mon diagnostic offert »).
- **Bio fondatrice** (sept. 2026) : reformulée — « l'une… l'autre », « avant de prendre la tête de La Turbine » (sans gras sur La Turbine), « Elle place l'humain, le partage et le respect au cœur de chaque projet. »
- **Contact EN** : « Ready to grow with your team? ».
- **H2 promesse** : « La formation classique ? 80 % oublié en 48h. Notre approche change cela. »
- **H2 services** : « Nos offres de transformation d'équipes à l'île Maurice. »

## Sections retirées (à ne pas réintroduire sans demande)

- Section stats d'impact (« Des résultats qui tiennent »).
- Section logos partenaires / confiance.
- Quiz interactif avec soft gate email + Brevo (l'URL du formulaire Brevo existe : `https://7c675398.sibforms.com/v2/serve/MUIFALiVm_…`).
- Prix des programmes — remplacés par des CTA « Demander un devis » (`mailto:contact@levelup.mu`).
- Titres « Ce qu'on évite » / « Ce qu'on construit avec vous » dans le comparatif, ainsi que les lignes séparatrices des deux cartes.

## Visuel hero — itérations

1. Carte magenta avec chevrons animés → statiques → 2 grands chevrons.
2. Photo d'équipe au coucher de soleil (`team-photo.jpg`).
3. Ampoule tenue à la main (`hero-bulb.jpg`).
4. Panneau « Turning Point » détouré (`hero-sign.png`, détourage via rembg).
5. **Actuel** : plateau « CREATE CHANGE » (`hero-create.jpg`), `object-fit: cover`, aligné avec le texte.

## Cartes Services — couleurs du logo

Les 3 cartes reprennent le dégradé des chevrons de l'icône LEVELUP :
1. Rose clair `#FFE4EE` (bordure `#FFD0E4`, texte magenta)
2. Magenta `#E0185C` (texte blanc) — « Le plus demandé »
3. Magenta foncé `#8C0030` (texte blanc)

## Témoignages

3 cartes au format **avant/après** (mesures à 6 mois) : Camille Roux (Directrice Innovation, Groupe Aurelia), Sarah Permal (DRH, Groupe Métis), Marc Lavoie (CEO, Sereno Group). *Ces témoignages sont des exemples rédigés — à remplacer par de vrais clients.*

## Domaine & infra

- Repo GitHub : `dianemaigrot7-cloud/levelup.mu`, branche de prod : `main`.
- Vercel déploie `main` automatiquement ; domaine `levelup.mu` (OVH) : A `@` → `76.76.21.21`, CNAME `www` → `cname.vercel-dns.com.` (un TXT `www` en conflit a dû être supprimé chez OVH).
- Email de contact : `contact@levelup.mu`.
- `robots.txt` + `sitemap.xml` ajoutés (sept. 2026) ; images inutilisées (photos Unsplash, anciens visuels hero, ancien `LEVELUP Landing.html`) supprimées du dépôt — les GIF de signature email sont conservés.

## Conventions

- Tout texte visible existe en double : `data-fr` + `data-en`.
- Pas de framework — un seul `index.html`.
- Mobile : visuel hero masqué < 600px ; grille programmes 2 colonnes en tablette, 1 colonne en mobile.
