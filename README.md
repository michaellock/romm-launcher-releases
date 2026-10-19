# RomM Launcher

Application Windows et macOS pour jouer à la bibliothèque d'un serveur [RomM](https://github.com/rommapp/romm)
(version 5.4 ou plus récente) : elle installe et lance les jeux PC et les ROMs, et synchronise les
sauvegardes avec le serveur.

**[Télécharger la dernière version](https://github.com/michaellock/romm-launcher-releases/releases/latest)**
(Windows : `RomM.Launcher_x.y.z_x64-setup.exe` ; Mac Apple Silicon : `RomM.Launcher_x.y.z_aarch64.dmg`).

## Installation

1. Lance l'installateur téléchargé.
2. L'application n'est pas signée : Windows SmartScreen peut afficher « Windows a protégé votre
   ordinateur ». Clique sur **Informations complémentaires**, puis **Exécuter quand même**.
3. Les mises à jour suivantes s'installent depuis l'application, sans cet avertissement.

## Installation sur Mac (Apple Silicon)

1. Ouvre le fichier `.dmg` et glisse **RomM Launcher** dans Applications.
2. L'application n'est pas certifiée par Apple : au premier lancement macOS la bloque. Ouvre
   Réglages Système > Confidentialité et sécurité, puis clique sur **Ouvrir quand même** en bas
   de la page (une seule fois).
3. Les mises à jour suivantes s'installent depuis l'application.

**Jeux Windows sur Mac** : installe [CrossOver](https://www.codeweavers.com/crossover) (payant,
essai gratuit, le plus compatible) ou [Whisky](https://frankea.github.io/Whisky/) (gratuit), puis
choisis-le dans Réglages > Jeux PC. L'application prépare elle-même un environnement Windows
dédié et y installe tes jeux.

## Premier lancement

1. Saisis l'adresse de ton serveur RomM (par exemple `https://romm.exemple.com`).
2. L'application affiche un code : valide-le dans RomM depuis le navigateur (bouton
   « Ouvrir dans le navigateur »). Aucun mot de passe n'est saisi dans l'application.
3. Choisis le dossier de la bibliothèque, où seront installés les jeux.
4. L'application propose les émulateurs trouvés sur le PC : valide ceux à utiliser.

## Ce que fait l'application

- **Bibliothèque** : jeux par plateforme, collections et favoris RomM, recherche et tri.
- **Jeux PC** : un clic installe le jeu, qu'il s'agisse d'une archive prête à jouer ou d'un
  installateur. L'installation peut être silencieuse (sans questions) ou personnalisée (tu choisis
  les options). L'exécutable du jeu et son désinstalleur sont détectés automatiquement.
- **ROMs** : téléchargement puis lancement avec l'émulateur associé à la plateforme. Préréglages
  pour RetroArch, mGBA, Eden, Ryujinx, PCSX2 et RPCS3 ; tout autre émulateur peut être ajouté.
- **Sauvegardes** : envoyées au serveur après chaque partie et récupérées avant la suivante, pour
  reprendre sur un autre PC. Un emplacement de sauvegarde choisi à la main est retenu avec la
  sauvegarde et repris sur tes autres ordinateurs. En cas de conflit, l'application te demande quelle version garder ;
  l'autre reste en copie de secours.
- **Temps de jeu** : envoyé à RomM et affiché sur la fiche du jeu.
- **Installation à distance** : un jeu demandé depuis l'interface web de RomM s'installe sur le PC.
- **Mode TV** : interface plein écran pilotable à la manette (voir ci-dessous).
- **Jeux 18+** : masqués par défaut ; Réglages > Application pour les afficher.
- **Plateformes synchronisées** : choisis dans Réglages > Sauvegardes celles dont les sauvegardes
  sont envoyées au serveur.
- **Notifications** quand une installation se termine ou échoue, application en arrière-plan.

## Mode TV

Pour y entrer : bouton **Mode TV** en haut de l'application, bouton **Menu** de la manette maintenu
une seconde, réglage **Démarrer en mode TV**, ou raccourci lancé avec l'argument `--tv` (pratique
dans Steam Big Picture).

| Manette | Clavier | Action |
|---|---|---|
| Croix ou stick gauche | Flèches | Se déplacer |
| A | Entrée | Choisir |
| B | Échap | Retour |
| Y | F | Ajouter aux favoris |
| LB / RB | Page préc. / Page suiv. | Rangée ou plateforme précédente / suivante |
| View | / | Rechercher |
| Menu | M | Téléchargements, quitter le mode TV |

## Problèmes

- **Un installateur ne se ferme pas** : la fiche du jeu propose de l'afficher ou de l'arrêter.
- **Le bouton Favori affiche une erreur** : clique sur **Déconnexion** en haut de l'application,
  puis reconnecte-toi : l'appareil reçoit alors le droit de modifier les collections.
- **Autre souci** : Réglages > Journaux > **Exporter les journaux**, puis joins le fichier à ta
  demande. Les journaux ne contiennent ni mot de passe ni jeton.
