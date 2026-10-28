<div align="center">

<img src="./public/favicon.svg" alt="Lasmium Pulse Logo" width="84" height="84" />

# LASMIUM *Pulse* `04`

**Visualiseur Twitch moderne • Multi-vue jusqu'à 9 écrans • Bloqueur de publicités HLS • Chat hybride • Compte Twitch**

[![Dernière version](https://img.shields.io/github/v/release/lasme-ephrem/lasmium-pulse-releases?style=flat-square&label=Derni%C3%A8re%20version&color=1EC988)](https://github.com/lasme-ephrem/lasmium-pulse-releases/releases/latest)
[![Téléchargements](https://img.shields.io/github/downloads/lasme-ephrem/lasmium-pulse-releases/total?style=flat-square&label=T%C3%A9l%C3%A9chargements&color=141413)](https://github.com/lasme-ephrem/lasmium-pulse-releases/releases)
[![Windows · macOS · Linux](https://img.shields.io/badge/Windows%20%C2%B7%20macOS%20%C2%B7%20Linux-141413?style=flat-square)](#télécharger)
[![Licence : AGPL-3.0](https://img.shields.io/badge/Licence-AGPL--3.0-F4F1EA?style=flat-square&labelColor=141413&color=FF3E1D)](LICENSE)

<p align="center">
  <em>Tous vos lives Twitch sans interruption publicitaire, jusqu'à 9 écrans simultanés, dans une interface éditoriale inspirée du design industriel (clair, sombre, OLED).</em>
</p>

<p align="center"><a href="README.md">🇬🇧 English version</a></p>

</div>

---

Ce dépôt héberge les **versions de bureau officielles** de Lasmium Pulse (Windows, macOS, Linux), le flux de mise à jour automatique de l'application, le journal des versions et la documentation. C'est aussi ici que vous pouvez [signaler un bug ou proposer une fonctionnalité](https://github.com/lasme-ephrem/lasmium-pulse-releases/issues/new/choose). Le code source est développé dans un dépôt séparé.

Lasmium Pulse tourne sur votre propre machine. Il n'est **pas affilié à Twitch**. Filtrer les publicités va à l'encontre des conditions d'utilisation de Twitch : utilisez-le à vos risques, et abonnez-vous aux streamers que vous voulez soutenir.

## <img src="docs/icons/rocket.svg" width="24" height="24" alt="" align="absmiddle"> Télécharger

**[Récupérer la dernière version →](https://github.com/lasme-ephrem/lasmium-pulse-releases/releases/latest)**

| Système | Fichier à télécharger | Remarques |
| :--- | :--- | :--- |
| **Windows** 10 / 11 (64 bits) | `Lasmium-Pulse-x.y.z-win-x64.exe` | Installeur ; vous choisissez le dossier. Raccourcis sur le bureau et dans le menu Démarrer. |
| **macOS** Apple Silicon (M1 et suivants) | `Lasmium-Pulse-x.y.z-mac-arm64.dmg` | Ouvrez le DMG et glissez l'application dans *Applications*. |
| **macOS** Intel | `Lasmium-Pulse-x.y.z-mac-x64.dmg` | Idem. |
| **Ubuntu / Debian** et dérivées | `Lasmium-Pulse-x.y.z-linux-amd64.deb` | `sudo apt install ./Lasmium-Pulse-x.y.z-linux-amd64.deb` : installe l'entrée de menu et l'icône du dock. |
| **Autres Linux** (64 bits) | `Lasmium-Pulse-x.y.z-linux-x86_64.AppImage` | `chmod +x` puis lancez. Intégrez-la avec [Gear Lever](https://github.com/mijorus/gearlever) ou AppImageLauncher pour avoir l'entrée de menu et l'icône ; lancée telle quelle, elle garde une icône générique. |

Les autres fichiers d'une release (`.zip`, `.blockmap`, `latest*.yml`) servent à la mise à jour automatique : vous n'en avez pas besoin.

Tout est embarqué : aucun terminal, aucun Node.js à installer. L'application garde la session Twitch dans le coffre du système et affiche une icône dans la zone de notification pour rouvrir la fenêtre ou quitter.

### Premier lancement

Les paquets ne sont pas encore signés, chaque système affiche donc un avertissement la première fois :

- **Windows** SmartScreen : *Informations complémentaires* → *Exécuter quand même*.
- **macOS** Gatekeeper : clic droit (ou Ctrl-clic) sur l'application → *Ouvrir*, une seule fois.
- **Linux** : rien à faire.

La connexion Twitch ne demande aucune configuration : cliquez sur **Se connecter avec Twitch** dans la barre latérale, puis saisissez le code affiché sur `twitch.tv/activate`. Chacun se connecte avec son propre compte ; l'application utilise le Device Code Flow officiel de Twitch et ne voit jamais votre mot de passe.

### Mises à jour

L'application vérifie s'il existe une nouvelle version au lancement puis toutes les 24 heures (Windows : aussi via *Aide* → *Rechercher des mises à jour…*). Une fois téléchargée, un message **Mise à jour prête** propose de **Redémarrer** ; sinon elle s'installe au prochain lancement. Seule la dernière version est maintenue.

## <img src="docs/icons/package.svg" width="24" height="24" alt="" align="absmiddle"> Docker (auto-hébergement)

Pour accéder à Lasmium Pulse depuis plusieurs appareils (téléphone compris) sur votre réseau ou votre propre serveur, utilisez [compose.yml](compose.yml) avec l'image publiée sur GHCR à chaque version :

```bash
PULSE_SECRET='une-longue-chaine-aleatoire' PULSE_PASSWORD='choisissez-un-mot-de-passe' docker compose up -d
# → http://<machine>:3001
```

| Variable | Rôle |
| :--- | :--- |
| `PULSE_SECRET` | Clé (16 caractères minimum) qui chiffre la session Twitch sur le volume. Obligatoire. |
| `PULSE_PASSWORD` | Mot de passe (8 caractères minimum) demandé par le navigateur avant tout accès. Indispensable dès qu'une autre machine peut atteindre le serveur. |
| `TWITCH_APP_CLIENT_ID` | Optionnel : le Client ID de votre propre application Twitch « Public » à la place de celle fournie avec l'application. |
| `PULSE_ALLOWED_HOSTS` | Optionnel : noms d'hôte supplémentaires par lesquels joindre l'application (ex. `pulse.local`). |

Image : `ghcr.io/lasme-ephrem/lasmium-pulse:<version>` (`latest` suit la dernière release). Le navigateur propose ensuite **Installer Lasmium Pulse** comme application web, qui s'ouvre dans sa propre fenêtre.

## <img src="docs/icons/sparkles.svg" width="24" height="24" alt="" align="absmiddle"> Ce que vous obtenez

- **Lecture sans publicité PulseShield™** : un proxy local retire les segments publicitaires du flux en direct, en temps réel.
- **Multi-vue jusqu'à 9 écrans** avec 5 dispositions (Grille, Spotlight, Théâtre, Colonnes, Studio), glisser-déposer, plafond de qualité sur les écrans secondaires, **solo audio** en un clic.
- **Retour en arrière dans le live**, décalage par écran avec un bouton **Aligner**, clips locaux des dernières secondes, captures d'écran, fenêtre flottante toujours au premier plan.
- **Chat hybride** : mode rapide avec les emotes Twitch + 7TV / BTTV / FFZ, un onglet **Mix** qui fusionne tous les chats, filtres, alertes de mention, fiches spectateur et outils de modération, messages envoyés avec votre compte ; ou le chat officiel Twitch en un clic.
- **Compte Twitch** : chaînes suivies en direct, recommandations, **notifications de live**, raids, changements de titre et de catégorie en temps réel, clips Twitch.
- **Rediffusions (VOD)** avec chapitres et replay du chat synchronisé avec la vidéo ; catégories et clips les plus vus dans l'application.
- **Multi-vues enregistrées**, historique de session, liens partageables, palette de commandes (`Ctrl+K`), raccourcis clavier personnalisables.
- Interface **français / anglais**, thèmes clair, sombre et noir OLED, 8 couleurs d'accent.

Le [guide utilisateur](docs/GUIDE_UTILISATEUR.md) complet détaille chaque fonctionnalité.

## <img src="docs/icons/lock.svg" width="24" height="24" alt="" align="absmiddle"> Confidentialité & sécurité

Votre session Twitch ne quitte jamais votre machine (ou votre serveur) : elle est chiffrée sur le disque, et le serveur local ne répond qu'à votre propre navigateur (écoute locale uniquement, vérification de `Host` / `Origin`, jeton de session par lancement). Les rapports d'erreurs sont **désactivés par défaut** et ne contiennent jamais d'identifiant, de jeton ni de nom de chaîne. Détails et procédure de signalement d'une vulnérabilité : [SECURITY.md](SECURITY.md).

## <img src="docs/icons/book-open.svg" width="24" height="24" alt="" align="absmiddle"> Aide & retours

- <img src="docs/icons/book-open.svg" width="18" height="18" alt="" align="absmiddle"> **[Guide utilisateur](docs/GUIDE_UTILISATEUR.md)** · **[Notes techniques](docs/ARCHITECTURE.md)**
- <img src="docs/icons/history.svg" width="18" height="18" alt="" align="absmiddle"> **[Journal des versions](CHANGELOG.md)** : ce qui change à chaque version
- <img src="docs/icons/flag.svg" width="18" height="18" alt="" align="absmiddle"> **[Signaler un bug / proposer une fonctionnalité](https://github.com/lasme-ephrem/lasmium-pulse-releases/issues/new/choose)**
- <img src="docs/icons/scale.svg" width="18" height="18" alt="" align="absmiddle"> **[Licence AGPL-3.0](LICENSE)**

Construit avec Electron, React, HLS.js et Node.js.
