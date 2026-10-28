# Guide Utilisateur — Lasmium Pulse

Bienvenue sur **Lasmium Pulse**, votre visualiseur Twitch moderne sans publicité avec support Multi-Vue jusqu'à 4 écrans.

---

## 1. Lancer un ou plusieurs streams à partir d'un lien

Vous pouvez ouvrir un stream de plusieurs façons :
1. **Coller un lien Twitch** dans la barre principale ou la barre supérieure :
   - Lien de chaîne classique : `https://www.twitch.tv/kamet0` ou `twitch.tv/caedrel`
   - Lien mobile ou lecteur : `https://m.twitch.tv/inoxtag`
   - Lien de rediffusion (VOD) : `https://www.twitch.tv/videos/123456789`
   - Plusieurs liens d'un coup (séparés par un espace) : `twitch.tv/kamet0 twitch.tv/caedrel`
2. **Bouton « Coller »** : Cliquez directement sur le bouton **Coller** dans la barre du haut pour ajouter instantanément le lien copié dans votre presse-papiers.
3. **Recherche en direct** : Tapez simplement le nom d'un streamer dans la barre du haut pour voir s'il est en direct et l'ajouter en un clic.
4. **Top France / Monde** : Cliquez sur n'importe quelle carte de la section **En Direct en ce moment** ou sur le bouton **Regarder le Top 4 en même temps**.

---

## 2. Gérer la Multi-Vue (jusqu'à 9 écrans)

- **Nombre d'écrans** : 4 par défaut, jusqu'à 9 dans **Réglages → Lecture**. Au-delà de 4, le navigateur travaille beaucoup : baissez la qualité des écrans secondaires si ça saccade.
- **Modes d'affichage** (barre supérieure, touche `L` pour passer de l'un à l'autre) :
  - **Grille** : Affiche vos streams à taille égale (2×2, 3×2, 3×3 selon le nombre).
  - **Focus** : Place un stream en grand écran principal à gauche et les autres en colonne à droite. Cliquez sur le bouton **Focus** en haut d'un écran secondaire pour le passer en écran principal : son son et son chat le suivent (si **Solo** est activé).
  - **Théâtre** : Écran principal en haut, les autres en bandeau en dessous.
  - **Colonnes** : Tous les écrans côte à côte.
  - **Studio (Cinéma)** : Masque le chat et maximise la surface vidéo.
- **Réorganiser** : attrapez le badge **CH.0X** d'un écran et déposez-le à la place d'un autre. Au clavier : focus sur le badge, **Espace**, flèches, **Espace**. Un lien Twitch glissé depuis un autre onglet et **déposé sur la grille** ouvre un nouvel écran.
- **Qualité des écrans secondaires** : quand plusieurs lives tournent, les écrans non sélectionnés sont plafonnés (720p par défaut, badge `↓720p`), ce qui divise la bande passante. Réglable dans **Réglages → Lecture** ; choisir une qualité à la main dans le menu d'un écran lève le plafond.
- **Gestion du son (Audio Solo)** :
  - Lorsque le bouton **Solo** est activé dans la barre supérieure, cliquer sur un écran coupe automatiquement le son des autres streams et active uniquement celui que vous regardez.
  - Désactivez **Solo** pour écouter plusieurs streams à la fois (activez le son de chaque écran avec son bouton). Le réactiver ne garde que le son de l'écran sélectionné.
  - Vous pouvez aussi régler le volume ou couper le son manuellement au bas de chaque vidéo.
- **Clips** : le bouton **Clip** en haut d'un écran (ou la touche `X`) crée un clip Twitch des dernières secondes du live depuis votre compte. Un bouton **Ajuster sur Twitch** ouvre ensuite la page d'édition de Twitch pour choisir le passage exact et le titre. Nécessite d'être connecté à Twitch (une session ouverte avant l'ajout des clips demande de se reconnecter une fois).
- **Latence** : chaque écran se cale à environ 4 s du direct et rattrape seul son retard (lecture légèrement accélérée) ; le badge **LAT** indique le retard actuel.
- **Fermer un écran par erreur** : un message **Annuler** apparaît quelques secondes en bas de l'écran et remet l'écran à sa place.
- **Fin d'un live** : quand un stream se termine, l'écran affiche **LIVE TERMINÉ** avec la durée du live, un bouton **Fermer l'écran** et un lien vers les **Rediffusions**, et un message vous prévient. Une chaîne ajoutée hors ligne affiche **HORS LIGNE**. Dans les deux cas, l'écran redémarre tout seul si le live reprend.
- **Son après un rechargement** : les navigateurs interdisent le son automatique à l'ouverture d'une page. Le live démarre donc en muet avec le bandeau « Cliquez pour activer le son » : un clic n'importe où (y compris sur le bouton son) rétablit le son. Pour éviter ce clic : Edge → `edge://settings/content/mediaAutoplay` (autoriser le site), Firefox → icône à gauche de l'adresse → *Lecture automatique*.
- **Qualité vidéo & Lecteur** (boutons en bas de chaque vidéo, visibles au survol) :
  - Résolution (**AUTO**, **1080p60**, **720p60**, **480p**, etc.), **Picture-in-Picture** et plein écran.
  - 🎵 **Audio seul** : plus d'image, moins de données ; pratique pour écouter un stream en fond.
  - 📈 **Statistiques** : résolution réelle, débit, bande passante, tampon, latence, images perdues, vitesse.
  - 📷 **Capture d'écran** : image PNG enregistrée sur votre ordinateur et copiée dans le presse-papiers.
  - 🎞️ **Clip local** : enregistre les dernières secondes (60 s par défaut) **sur votre ordinateur**, sans rien publier sur Twitch. Format **brut** immédiat (fichier `.ts` ou `.mp4` fragmenté, lisible avec VLC) ou **MP4 standard** converti dans le navigateur (ffmpeg.wasm, ~30 Mo téléchargés la première fois). Durée, format et mémoire réservée se règlent dans **Réglages → Lecture**.
  - 🪟 **Fenêtre flottante** (Chrome, Edge, application de bureau) : sort l'écran dans une petite fenêtre toujours au premier plan ; **Ramener ici** le remet dans la grille.
- **Retour arrière** : le live lu reste en mémoire (2 minutes par défaut). Glissez la barre fine en haut des contrôles pour revenir en arrière, ou **⏪ −10 s** ; le bouton **LIVE** (qui affiche le retard, ex. `−0:42`) ramène au direct. Avec plusieurs angles d'un même événement, **Aligner** (barre du haut) donne à tous les écrans le décalage de l'écran sélectionné.
- **Fin d'un live** : si une chaîne suivie est en direct, le message de fin propose de la **regarder à la place** sur le même écran.

---

## 3. Utiliser le Chat en direct

- **Changement automatique de salon** : Par défaut, cliquer sur l'un de vos streams affiche automatiquement son chat à droite (vous pouvez verrouiller/déverrouiller cette synchronisation via l'icône de chaîne à droite des onglets du chat).
- **Mode Rapide vs Mode Officiel** :
  - **Rapide** : Affiche les messages instantanément avec les badges et toutes les emotes Twitch + 7TV + BTTV + FFZ, avec une barre de recherche pour filtrer les messages. Si la connexion au chat tombe, elle se rétablit toute seule.
  - **Mix** : Avec plusieurs écrans ouverts, l'onglet **Mix** fusionne tous les chats en un seul fil ; chaque message est étiqueté avec le nom de sa chaîne.
  - **Écrire depuis le mode Rapide** : une fois connecté à Twitch (barre latérale), un champ de saisie apparaît en bas du chat. Les messages partent avec votre compte et réapparaissent dans le chat comme ceux des autres. Si Twitch refuse un message (mode abonnés, mode lent, AutoMod…), la raison s'affiche sous le champ. En mode **Mix**, le message part vers la chaîne de l'onglet sélectionné.
  - **Mentionner quelqu'un** : tapez `@` puis le début d'un pseudo : les viewers récents du chat sont proposés (flèches pour choisir, `Tab` ou `Entrée` pour valider). Un clic sur un pseudo dans le chat l'ajoute aussi au message.
  - **Répondre à un message** : survolez-le et cliquez sur la flèche **Répondre**. Un bandeau « Réponse à @… » apparaît au-dessus du champ (`Échap` ou ✕ pour annuler) ; la réponse part en fil Twitch, comme sur le chat officiel, même depuis l'onglet Mix. Les réponses des autres viewers affichent le message d'origine au-dessus.
  - **Emotes** : le bouton 😊 du champ ouvre le **sélecteur d'emotes** (récentes, vos emotes Twitch si vous êtes connecté, celles de la chaîne, les globales, et 7TV / BTTV / FFZ, avec recherche). Tapez `:` puis deux lettres (`:kap`) pour l'autocomplétion.
  - **Vos messages** sont surlignés ; un message qui **vous mentionne** est surligné en ambre, avec en option un **son** et une **notification** quand l'onglet est en arrière-plan (réglages → Chat → Mentions).
  - **Événements** : abonnements, cadeaux, raids et annonces apparaissent en lignes dédiées ; les bits sont signalés ; un message supprimé par un modérateur devient « Message supprimé » (cliquez pour le lire) ; les expulsions (timeouts), bans et vidages du chat sont indiqués. Les **liens** sont cliquables (http/https seulement, ouverture dans un nouvel onglet).
  - **Fiche d'un viewer** : cliquez sur un pseudo : avatar, date de création du compte, followers, **Mentionner**, **Répondre**, **Copier le pseudo**, ouvrir sur Twitch, **Masquer ses messages** (dans l'app seulement) et **Bloquer sur Twitch** (liste de blocage de votre compte). Sur une chaîne dont vous êtes **modérateur** (ou votre propre chaîne), la fiche propose aussi **Supprimer le message**, **Pause 1 / 10 min / 1 h**, **Bannir** et **Débannir**, chaque action demandant une confirmation.
  - **Viewers** : le bouton 👥 liste les viewers qui ont écrit récemment ; sur une chaîne que vous modérez, la liste complète fournie par Twitch s'affiche aussi.
  - **Chat détaché** : le bouton ⧉ ouvre le chat seul dans une petite fenêtre (pratique sur un second écran). La fenêtre suit les mêmes réglages.
  - **Filtres** (réglages → Chat → Filtres) : masquer les bots connus, les commandes `!…`, les messages composés uniquement d'emotes, des **mots** et des **pseudos** (localement). Les utilisateurs bloqués sur votre compte Twitch sont masqués d'office.
  - **Officiel** : le chat Twitch d'origine intégré (iframe) : vrais badges, sondages, prédictions et points de chaîne, mais sans emotes 7TV/BTTV/FFZ ni Mix. Pour y écrire, il faut être connecté à twitch.tv dans le navigateur.
  - Le mode Rapide affiche les messages reçus depuis l'ouverture de l'écran (180 par chaîne par défaut, jusqu'à 1 000 ; la liste est virtualisée donc un long historique reste fluide). En option, les **50 derniers messages** peuvent être chargés à l'ouverture d'une chaîne via le service tiers recent-messages.robotty.de (désactivé par défaut : ce service voit alors le nom des chaînes que vous ouvrez).
  - **Sondages, prédictions, hype train** : Twitch ne les expose pas aux viewers par ses API officielles (ils exigent l'autorisation du streamer) ; ils restent visibles dans le chat **Officiel**.

---

## 4. Mode Clair / Mode Sombre & Anti-Pub

- **Thème Clair / Sombre** : Cliquez sur le bouton **Clair / Sombre** en haut à droite pour passer du thème *Papier d'Atelier* au thème *Carbone Sombre*. Votre préférence est sauvegardée automatiquement.
- **Panneau Anti-Pub** : Cliquez sur le bouton **Anti-Pub** dans la barre supérieure pour consulter le nombre de flux protégés et de coupures publicitaires bloquées pendant votre session.

- **Stratégies anti-pub** : *Multi-Couches* (recommandé) bascule sur un flux de secours pendant la pub ; *Jeton Embed* se contente de retirer les segments publicitaires ; *Purge stricte* retire tout, quitte à figer l'image quelques secondes au lieu d'afficher la pub. Les statistiques sont conservées entre deux redémarrages et peuvent être remises à zéro.

---

## 5. Vos chaînes suivies & les recommandations

- **Prochain live** : sous une chaîne suivie hors ligne, l'heure de son prochain live apparaît quand le streamer a publié un planning sur Twitch.
- **Cloche par chaîne** : survolez une chaîne suivie et cliquez sur la cloche pour ne plus être prévenu de ses lives (la cloche barrée reste visible ; un nouveau clic rétablit). L'historique des notifications reçues est dans Réglages → Notifications, avec un bouton **Regarder**.
- **Temps réel** : une fois connecté, le titre et la catégorie des écrans ouverts se mettent à jour instantanément, la fin d'un live est détectée en quelques secondes, et un **raid** lancé par un streamer que vous regardez propose de **Suivre le raid**. Twitch limite ce canal à une dizaine d'abonnements : les écrans ouverts passent en premier, le reste continue d'être vérifié toutes les minutes.

La barre latérale gauche reprend celle de Twitch, pour ne plus faire d'aller-retour entre les deux :

- **Chaînes suivies** : cliquez sur **Se connecter avec Twitch**, puis validez le code affiché sur `twitch.tv/activate`. Vos chaînes en direct apparaissent, triées par spectateurs (l'icône ⇅ trie par début de live), suivies des chaînes hors ligne via **Afficher plus**. Un clic ajoute la chaîne à la multi-vue.
- **Chaînes live** : des chaînes recommandées dans les catégories que regardent vos chaînes suivies.
- **Catégories recommandées** : un clic ouvre le répertoire des directs filtré sur cette catégorie.
- **Notifications** : l'icône 🔔 en bas de la barre active une notification du navigateur quand une chaîne suivie lance un live. Un message apparaît aussi dans l'app avec un bouton **Regarder**.
- **Afficher plus / Afficher moins** sous chaque section déplie ou replie la liste.
- La barre se replie (icône « » ou touche **B**) pour ne garder que les avatars.

> La première connexion demande une configuration unique (création d'une application Twitch, ≈ 3 min) : voir la section *Connexion Twitch* du README.

---

## 6. Session, partage & raccourcis

- **Accueil** : un clic sur le logo **Lasmium Pulse** ramène à l'accueil sans couper vos streams (ils continuent en arrière-plan) ; le bandeau **Revenir à la multi-vue** vous y ramène.
- **Session conservée** : vos écrans et la disposition sont restaurés après un rafraîchissement de la page.
- **Lien partageable** : le bouton **Partager** copie l'adresse de la multi-vue (`?c=chaine1,chaine2&layout=spotlight`). L'ouvrir recrée exactement les mêmes écrans.
- **Synchronisation du direct** : le retard de chaque écran est affiché (`LAT 3.2s`). Le bouton **Sync** (ou **R**) ramène tous les écrans au plus près du direct.
- **Raccourcis clavier** (aide complète avec **?**, touches modifiables dans **Réglages → Raccourcis**) :

| Touche | Action |
| :--- | :--- |
| `1` – `4` | Sélectionner un écran |
| `M` / `S` | Couper le son / écoute solo de l'écran sélectionné |
| `F` | Plein écran de l'écran sélectionné |
| `L` | Changer de disposition |
| `R` | Resynchroniser tous les écrans sur le direct |
| `X` | Créer un clip de l'écran sélectionné |
| `,` | Ouvrir les réglages |
| `C` / `B` / `D` | Chat / barre des chaînes / répertoire des directs |
| `Échap` | Fermer les fenêtres ouvertes |

---

## 7. Langue de l'interface

- **Détection automatique** : au premier lancement, l'application s'affiche dans la langue de votre navigateur si elle est disponible (français ou anglais), sinon en anglais.
- **Changer de langue** : bouton **FR / EN** dans la barre du haut. Votre choix est mémorisé et prime ensuite sur la détection.
- La langue s'applique aussi aux nombres (« 32,3 k » / « 32.3K »), aux heures du chat, et aux noms des catégories Twitch.
- **Langue des streams** : le filtre **Top** du répertoire et les recommandations montrent par défaut les streams dans la langue de l'interface. La flèche à côté de **Top** permet d'en choisir une autre (par exemple l'interface en anglais avec le Top français) ; ce choix est mémorisé.

---

## 8. Réglages

Le bouton ⚙️ de la barre du haut (ou la touche `,`) ouvre un panneau unique. Tout y est mémorisé dans votre navigateur.

- **Général** : langue de l'interface (automatique ou fixée), **thème** (Système, Clair, Sombre, Noir OLED), couleur d'accent, langue des streams du Top, transitions animées, et **Revoir la visite guidée** du premier lancement.
- **Lecture** : Audio Solo, nombre d'écrans maximum, qualité des écrans secondaires, latence visée, segments annoncés à l'avance (expérimental), mémoire de retour arrière, durée / format / mémoire des clips locaux.
- **Chat** : mode Rapide ou Officiel, chat affiché au démarrage, chat qui suit l'écran sélectionné ; **affichage** (taille du texte, densité, horodatage, lignes alternées, badges, messages conservés par chaîne) ; **mentions** (son, notification) ; **filtres** (bots, commandes, emotes seules, mots et pseudos masqués) ; **historique** tiers à l'ouverture d'une chaîne (désactivé par défaut).
- **Notifications** : notifications du navigateur pour les lives des chaînes suivies, avec l'état de l'autorisation.
- **Anti-pub** : état, compteurs, stratégie et journal du bloqueur (anciennement dans sa propre fenêtre).
- **Raccourcis** : cliquez sur une touche puis appuyez sur la nouvelle. Les chiffres (écrans) et Échap sont réservés ; une touche déjà prise est signalée.
- **Données** : **exporter** un fichier JSON (réglages, écrans ouverts, chaînes récentes, presets et préférences par chaîne) et le **réimporter** sur un autre navigateur ou après une réinstallation ; réinitialiser les réglages ; effacer les données locales.
- **À propos** : version de l'app et du serveur, licence, et le rappel que l'app n'est pas affiliée à Twitch.

L'onglet du navigateur affiche la chaîne sélectionnée et son nombre de spectateurs (`🔴 kamet0 +1 · 46 k`), et le favicon porte le nombre d'écrans en direct.

---

## 9. Multi-vues enregistrées & reprise

- Le bouton **Presets** (🔖) de la barre du haut enregistre la multi-vue en cours (chaînes, disposition, volumes) sous un nom, puis la relance d'un clic. Les presets sont conservés par le serveur local (bibliothèque SQLite) et compris dans l'export des données.
- L'accueil affiche une section **Reprendre** : vos presets et les dernières multi-vues ouvertes (historique des sessions), à relancer d'un clic.

## 10. Palette de commandes

`Ctrl+K` (ou le bouton ⌘ de la barre du haut) ouvre une zone de saisie unique : tapez un nom de chaîne (chaînes suivies en direct, chaînes récentes, puis recherche Twitch) ou une action (dispositions, Solo, chat, barre latérale, répertoire, accueil, synchronisation, alignement, lien de partage, presets, réglages, raccourcis, tout fermer). `>` au début limite aux actions. Flèches pour choisir, `Entrée` pour lancer.

## 11. Catégories & clips

- Sur l'accueil, la section **Catégories** présente les plus regardées et une recherche ; cliquer sur une catégorie filtre le répertoire des directs. Le bouton **Afficher plus de directs** élargit la liste (jusqu'à 60).
- L'onglet **Clips** du répertoire montre les clips les plus vus d'une chaîne ouverte, d'une chaîne suivie en direct ou de la catégorie choisie, sur 24 h, 7 jours, 30 jours ou depuis toujours. Un clic ouvre le lecteur de clip de Twitch dans l'app ; le lien **Ouvrir sur Twitch** reste disponible.

## 12. Rediffusions (VOD)

Collez un lien `twitch.tv/videos/…` comme pour un live. L'écran propose en plus : la **vitesse** (0,5× à 2×), les **chapitres** (changements de jeu) pour sauter directement à un moment, une **barre de position** et le temps écoulé. Dans le panneau de chat, l'onglet **VOD** rejoue le **chat de la rediffusion** synchronisé avec la vidéo (lecture seule : les messages apparaissent au moment où ils ont été écrits, et suivent vos sauts dans la vidéo).

---

## 13. Installer l'application

- **Application de bureau** (Windows, macOS, Linux) : téléchargez l'installeur de la dernière release GitHub. Tout est embarqué : aucun terminal, aucun Node.js à installer. L'icône dans la zone de notification permet de rouvrir la fenêtre ou de quitter. Sur Windows, la barre de titre aux couleurs de l'app porte les menus **Affichage** (plein écran, zoom, recharger) et **Aide** (raccourcis clavier, guide, signaler un problème, **Rechercher des mises à jour…**, À propos). Quand une mise à jour est téléchargée, un message **Mise à jour prête — Redémarrer** apparaît ; elle s'installe aussi au prochain lancement. La connexion Twitch ne demande aucune configuration : **Se connecter avec Twitch** dans la barre latérale, puis le code sur `twitch.tv/activate` (chacun avec son propre compte). Les paquets ne sont pas signés : acceptez l'avertissement de Windows (« Informations complémentaires → Exécuter quand même ») ou, sur macOS, faites un clic droit → Ouvrir la première fois. Sur Ubuntu / Debian, préférez le `.deb` (`sudo apt install ./Lasmium-Pulse-x.y.z-linux-amd64.deb`) : il installe l'entrée de menu et l'icône du dock. L'AppImage fonctionne aussi mais, lancée telle quelle, GNOME lui donne une icône générique ; intégrez-la avec Gear Lever ou AppImageLauncher pour retrouver l'icône et l'entrée de menu.
- **Docker / serveur maison** : `docker compose up -d` avec `PULSE_SECRET` (chiffrement de la session) et `PULSE_PASSWORD` (mot de passe demandé par le navigateur). L'application est alors accessible depuis vos autres appareils, téléphone compris.
- **Navigateur** : depuis une installation Docker ou `npm start`, le menu du navigateur propose **Installer Lasmium Pulse** (application web installable) ; elle s'ouvre dans sa propre fenêtre, sans barre d'adresse. Sur téléphone, les écrans s'empilent et le chat occupe le bas de l'écran.
- **Depuis les sources** : voir le README.

## 14. Confidentialité

- Votre session Twitch ne quitte jamais votre machine (ou votre serveur) ; elle est chiffrée sur le disque (coffre du système dans l'application de bureau, `PULSE_SECRET` ailleurs).
- Les **rapports d'erreurs anonymes** (Réglages → Données) sont désactivés par défaut et n'existent que si la personne qui héberge le serveur a configuré un service Sentry. Activés, ils transmettent la pile d'erreur technique, la version et le navigateur, sans identifiant, jeton ni nom de chaîne. Le choix est partagé par tous les navigateurs de la même installation.
- L'historique tiers du chat (Réglages → Chat) est le seul service externe à Twitch que l'application peut contacter, et il est désactivé par défaut.
