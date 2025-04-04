# Sans Rendez-Vous Express

Une application de prise de rendez-vous médicaux développée avec Next.js et Supabase.

## Fonctionnalités principales

- Système d'authentification avec Supabase (inscription, connexion, récupération de mot de passe)
- Interface en français et en anglais
- Recherche de rendez-vous médicaux par code postal
- Système de paiement avec Stripe pour les abonnements
- Interface d'administration pour les médecins et cliniques
- Gestion de profils familiaux pour les utilisateurs

## Configuration technique

### Prérequis

- [Bun](https://bun.sh/) (recommandé) ou Node.js 18+
- Compte Supabase (gratuit pour commencer)
- Compte Stripe (optionnel, pour les paiements)

### Configuration de Supabase

1. Créez un compte sur [Supabase](https://supabase.com)
2. Créez un nouveau projet
3. Dans les paramètres du projet, copiez l'URL du projet et la clé anon
4. Créez un fichier `.env.local` à la racine du projet et ajoutez-y les variables suivantes:

```
NEXT_PUBLIC_SUPABASE_URL=votre-url-supabase
NEXT_PUBLIC_SUPABASE_ANON_KEY=votre-clé-anon-supabase
NEXT_PUBLIC_URL=http://localhost:3000
```

5. Dans Supabase, allez dans Authentication > Settings et configurez les options suivantes:
   - Activez "Email auth" dans les providers
   - Configurez les URL de redirection pour qu'elles pointent vers `http://localhost:3000/auth/callback`
   - Désactivez "Email confirmations" pour les tests (optionnel)