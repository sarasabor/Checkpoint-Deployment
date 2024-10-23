# Checkpoint-Deployment

Déployer une application MERN sur Microsoft Azure implique plusieurs étapes. Voici un guide détaillé basé sur vos instructions :

###1. Préparer votre application MERN- Développement Local: Assurez-vous que votre application MERN (MongoDB, Express.js, React, Node.js) fonctionne correctement en local.

Connectivité: Vérifiez que le backend (Node.js/Express) est correctement connecté à votre base de données MongoDB.
###2. Créer un compte Microsoft Azure- Inscription: Si vous n’avez pas de compte, rendez-vous sur Microsoft Azure et créez un compte.

Accès au Portail: Connectez-vous au portail Azure et accédez à votre tableau de bord.
###3. Configurer MongoDB Atlas- Création de l'instance: Si vous n'avez pas encore de base de données, créez un compte sur MongoDB Atlas et configurez une nouvelle base de données.

Connexion: Copiez la chaîne de connexion MongoDB et sauvegardez-la pour plus tard.
###4. Préparer votre application pour le déploiement- Variables d'environnement: Mettez à jour votre application pour utiliser des variables d'environnement pour les données sensibles, comme les informations de connexion à MongoDB.

Construire le front-end: Dans votre dossier React, exécutez la commande suivante pour créer une version optimisée de votre application :
bash npm run build
###5. Créer un service Azure Web App- Créer une ressource: Dans le portail Azure, cliquez sur "Créer une ressource" > "Web" > "Web App".

Détails de l'application: Remplissez les informations nécessaires comme le nom de l'application, le groupe de ressources (ou en créer un) et la region.
Choix du prix: Sélectionnez le niveau de prix souhaité en fonction de vos besoins.
###6. Configurer la source de déploiement- Centre de déploiement: Dans les paramètres de l'Azure Web App, accédez à "Deployment Center".

Source de déploiement: Choisissez votre méthode de déploiement (Local Git, GitHub, etc.).
###7. Déployer votre application MERN- Cloner le dépôt (si Local Git est choisi) :

Copier les fichiers de build: Collez vos fichiers construits (généralement dans le dossier build de React) dans un dossier de votre projet backend, comme server/public.
Commit et Push: Exécutez les commandes suivantes pour envoyer vos fichiers au dépôt Azure :


bash
git commit -m "Déploiement de l'application MERN"  
git push ```  

Azure détectera automatiquement ces changements et déploiera votre application.  

###8. Configurer les variables d'environnement- **Paramètres**: Dans le portail Azure, allez à "Configuration" et ajoutez les variables d'environnement nécessaires, y compris la chaîne de connexion MongoDB.  

###9. Tester votre application déployée- **Accès**: Utilisez l'URL fournie par Azure pour accéder à votre application et vérifiez que toutes les fonctionnalités fonctionnent comme prévu.  
- **Diagnostic**: Si vous rencontrez des problèmes, vérifiez les journaux d'erreurs dans le portail Azure pour diagnostiquer les problèmes de déploiement ou de connectivité.  

### ConclusionVous avez maintenant déployé avec succès votre application MERN sur Microsoft Azure. Assurez-vous de surveiller l'application et d'ajuster les configurations ou les ressources selon vos besoins.
