# Guide de Configuration SSH pour Accès depuis iPad

## Étape 1 : Installer OpenSSH Server

Si SSH n'est pas encore installé sur votre machine Linux, exécutez :

```bash
sudo apt update
sudo apt install openssh-server -y
```

## Étape 2 : Démarrer et Activer le Service SSH

```bash
sudo systemctl start ssh
sudo systemctl enable ssh
```

## Étape 3 : Vérifier le Statut

```bash
sudo systemctl status ssh
```

Vous devriez voir "active (running)" en vert.

## Étape 4 : Obtenir l'Adresse IP de Votre Machine

Votre adresse IP actuelle est : **192.168.1.44**

Pour vérifier à nouveau :
```bash
hostname -I
```

## Étape 5 : Configuration du Pare-feu (si nécessaire)

Si vous avez un pare-feu actif, autorisez SSH :

```bash
sudo ufw allow ssh
# ou
sudo ufw allow 22/tcp
```

## Étape 6 : Se Connecter depuis l'iPad

### Option A : Utiliser l'App Terminal sur iPad

1. Installez une app terminal sur votre iPad (ex: **Termius**, **Blink Shell**, **Prompt 3**, ou **iTerminal**)
2. Créez une nouvelle connexion SSH avec :
   - **Host**: `192.168.1.44` (ou le nom d'hôte de votre machine)
   - **Port**: `22`
   - **Username**: `daewon` (votre nom d'utilisateur)
   - **Authentication**: Mot de passe ou clé SSH

### Option B : Utiliser l'App Files avec SFTP

Vous pouvez aussi accéder aux fichiers via SFTP dans l'app Files de l'iPad.

## Étape 7 : Sécurité (Recommandé)

### Créer une Clé SSH (plus sécurisé que le mot de passe)

Sur votre machine Linux :
```bash
ssh-keygen -t ed25519 -C "ipad-access"
```

Copiez la clé publique vers votre iPad, ou utilisez une clé partagée.

### Désactiver la connexion par mot de passe (optionnel)

Éditez `/etc/ssh/sshd_config` :
```bash
sudo nano /etc/ssh/sshd_config
```

Changez :
```
PasswordAuthentication no
PubkeyAuthentication yes
```

Puis redémarrez SSH :
```bash
sudo systemctl restart ssh
```

## Notes Importantes

1. **Même réseau WiFi** : Votre iPad et votre machine Linux doivent être sur le même réseau WiFi pour que l'adresse IP locale fonctionne.

2. **Adresse IP dynamique** : L'adresse IP peut changer. Pour une solution permanente :
   - Configurez une adresse IP statique sur votre routeur
   - Ou utilisez le nom d'hôte de votre machine (si votre réseau le supporte)

3. **Accès depuis l'extérieur** : Pour accéder depuis l'extérieur de votre réseau local, vous devrez configurer le port forwarding sur votre routeur (non recommandé pour la sécurité).

## Applications Terminal Recommandées pour iPad

- **Termius** (gratuit, avec version premium)
- **Blink Shell** (payant, très puissant)
- **Prompt 3** (payant, interface élégante)
- **iTerminal** (gratuit, basique)

## Test de Connexion

Une fois configuré, testez depuis votre iPad :
```bash
ssh daewon@192.168.1.44
```

## Utilisation avec Cursor/AI Assistant

Une fois connecté via SSH depuis votre iPad, vous pouvez :
- Naviguer dans vos fichiers
- Utiliser git
- Exécuter des scripts
- Modifier des fichiers avec nano/vim

**Note** : L'assistant AI (moi) fonctionne dans l'environnement Cursor sur votre machine. Pour interagir avec moi via SSH, vous devriez utiliser Cursor via SSH, ou utiliser des outils CLI qui peuvent interagir avec l'API de Cursor (si disponible).

