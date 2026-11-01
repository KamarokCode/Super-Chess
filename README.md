# Super Chess — application Android

Échecs avec pouvoirs, événements, vue 3D, et parties en ligne entre comptes.

## Installer l'application
1. Ouvrez la page **Releases** de ce dépôt depuis votre téléphone Android.
2. Téléchargez le fichier `SuperChess-1.0.X.apk` de la dernière version.
3. Ouvrez-le. Android demandera d'autoriser l'installation depuis le navigateur : acceptez pour cette fois.
4. Les versions suivantes s'installent par-dessus, sans perdre votre compte.

## Comment ça se compile
Chaque envoi sur la branche `main` lance le workflow **Compiler l'APK** (onglet *Actions*),
qui publie l'APK dans *Releases*. On peut aussi le relancer à la main depuis cet onglet.

## Comptes et jeu en ligne (Firebase)
- `app/src/main/assets/www/firebase-config.js` : identifiants publics du projet Firebase.
- `firestore.rules` : règles de sécurité, à coller dans *Firestore Database › Règles*.
- Authentification : **E-mail/Mot de passe** activée.

## Organisation
- `app/src/main/assets/www/index.html` : le jeu complet (moteur, pouvoirs, événements, 3D, en ligne).
- `app/src/main/java/.../MainActivity.java` : la WebView qui affiche le jeu.
- `keystore/superchess.keystore` : clé de signature (mot de passe `superchess`), commune à toutes les versions
  pour que les mises à jour s'installent par-dessus.
