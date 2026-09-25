# Déploiement Cloudflare Pages — Multicoaching Canada

## Architecture

Site statique sans build, dépendance payante, base de données ou serveur. Le dossier `outputs/` est directement publiable comme répertoire de production.

## Avant publication

1. Ajouter `assets/MULTICOACHINGLOGO.jpeg` et `assets/koloplus.png`.
2. Remplacer le formulaire de démonstration par un fournisseur vérifié (Formspree ou une Cloudflare Pages Function), puis mettre à jour le message de confidentialité si nécessaire.
3. Vérifier les URLs sociales et le profil LinkedIn réel d’Aulida Valery.

## Étapes Cloudflare Pages

1. Pousser le contenu vers un dépôt GitHub.
2. Dans Cloudflare, ouvrir **Workers & Pages → Create application → Pages → Connect to Git**.
3. Choisir le dépôt et configurer le projet en site statique.
4. Utiliser les paramètres Cloudflare Pages suivants :
   - Framework preset : `None`
   - Production branch : `main`
   - Build command : `exit 0`
   - Build output directory : `outputs`
5. Après le premier déploiement, ouvrir **Custom domains** et ajouter `multicoaching.ca`, puis `www.multicoaching.ca`.
6. Suivre exactement les enregistrements DNS affichés par Cloudflare. Ne pas deviner les cibles et ne pas modifier GoDaddy avant cette étape.
7. Vérifier le certificat HTTPS, la redirection choisie entre domaine nu et `www`, puis tester les deux URLs.

## DNS et HTTPS

Cloudflare affichera les enregistrements exacts requis selon la configuration actuelle du domaine. Cette documentation n’en invente aucun. Le domaine reste enregistré chez GoDaddy; seul le DNS sera éventuellement délégué ou mis à jour après validation.
