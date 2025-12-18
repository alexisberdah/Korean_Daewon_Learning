# Guide : Utiliser Cursor via CLI depuis iPad (SSH)

## 🎯 La Solution : Cursor Agent CLI

**Cursor Agent** est la solution parfaite pour utiliser Cursor via SSH depuis votre iPad ! C'est un agent CLI qui vous donne accès à toutes les fonctionnalités de Cursor directement dans le terminal.

---

## 🚀 Installation et Configuration Initiale

### Étape 1 : Vérifier que Cursor Agent est Installé

Depuis votre machine Linux (ou via SSH) :
```bash
cursor agent --version
```

Si ce n'est pas installé, il s'installera automatiquement lors de la première utilisation.

### Étape 2 : Authentification

La première fois, vous devez vous authentifier :
```bash
cursor agent login
```

Cela ouvrira un navigateur pour l'authentification. Si vous êtes en SSH sans interface graphique, utilisez :
```bash
NO_OPEN_BROWSER=1 cursor agent login
```

Vous obtiendrez une URL à ouvrir dans votre navigateur pour vous authentifier.

### Étape 3 : Vérifier l'Authentification

```bash
cursor agent status
# ou
cursor agent whoami
```

---

## 📱 Utilisation depuis iPad via SSH

### Applications Terminal Recommandées pour iPad :

- **Blink Shell** (payant, très puissant, supporte mosh)
- **Termius** (gratuit/premium, interface moderne)
- **Prompt 3** (payant, interface élégante)
- **iTerminal** (gratuit, basique)

### Connexion SSH :

1. Connectez-vous à votre machine : `ssh daewon@192.168.1.44`
2. Naviguez vers votre projet : `cd ~/Documents/Korean_Daewon_Learning`
3. Lancez Cursor Agent : `cursor agent`

---

## 💡 Utilisation de Cursor Agent

### Mode Interactif (Recommandé)

Lancez simplement :
```bash
cursor agent
```

Puis tapez vos questions ou demandes directement. L'agent peut :
- Lire et modifier des fichiers
- Exécuter des commandes
- Créer de nouveaux fichiers
- Rechercher dans le code
- Et bien plus !

### Exemples d'Utilisation :

```bash
# Lancer l'agent en mode interactif
cursor agent

# Avec un prompt initial
cursor agent "Ouvre la leçon Week_01_Day_01 et montre-moi le contenu"

# Dans un workspace spécifique
cursor agent --workspace ~/Documents/Korean_Daewon_Learning "Résume ma progression"

# Mode print (pour scripts)
cursor agent --print "Liste tous les fichiers markdown"
```

### Mode Print (Non-Interactif)

Pour utiliser dans des scripts ou obtenir une sortie directe :
```bash
cursor agent --print "Quelle est ma progression actuelle ?"
```

### Options Utiles :

```bash
# Forcer l'exécution de commandes
cursor agent --force "Exécute cette commande"

# Utiliser un modèle spécifique
cursor agent --model sonnet-4 "Question complexe"

# Activer le support navigateur
cursor agent --browser "Recherche sur le web"
```

---

## 🎓 Cas d'Usage pour Votre Apprentissage Coréen

### Exemples Concrets :

```bash
# 1. Voir votre progression
cursor agent "Montre-moi ma progression actuelle dans STUDENT_PROFILE.md"

# 2. Ouvrir et réviser une leçon
cursor agent "Ouvre Week_01_Day_01.md et montre-moi les exercices"

# 3. Créer une nouvelle leçon
cursor agent "Crée la leçon Week_01_Day_02 basée sur le template"

# 4. Ajouter du vocabulaire
cursor agent "Ajoute ces 10 mots au fichier de vocabulaire de la semaine 1"

# 5. Vérifier les réponses d'exercices
cursor agent "Vérifie mes réponses dans Week_01_Day_01.md"

# 6. Générer des exercices de pratique
cursor agent "Crée 5 exercices de pratique pour les nombres coréens"
```

---

## 🔧 Commandes Avancées

### Gestion des Sessions de Chat

```bash
# Créer un nouveau chat
cursor agent create-chat

# Reprendre le dernier chat
cursor agent resume

# Reprendre un chat spécifique
cursor agent resume <chatId>

# Lister les chats
cursor agent ls
```

### Gestion des Extensions MCP

```bash
# Gérer les serveurs MCP
cursor agent mcp
```

### Mise à Jour

```bash
# Mettre à jour Cursor Agent
cursor agent update
# ou
cursor agent upgrade
```

### Intégration Shell (Optionnel)

Pour une meilleure intégration avec votre shell :
```bash
# Installer l'intégration shell
cursor agent install-shell-integration

# Désinstaller
cursor agent uninstall-shell-integration
```

---

## 📝 Commandes CLI Cursor Utiles (Sans Agent)

En plus de l'agent, vous pouvez utiliser les commandes Cursor CLI directement :

```bash
# Ouvrir un fichier dans Cursor (si interface graphique disponible)
cursor LESSONS/Week_01_Day_01.md

# Ouvrir un fichier à une ligne spécifique
cursor --goto LESSONS/Week_01_Day_01.md:128

# Comparer deux fichiers
cursor --diff file1.md file2.md

# Ajouter un dossier à la fenêtre active
cursor --add ~/Documents/Korean_Daewon_Learning

# Lister les extensions installées
cursor --list-extensions
```

---

## 📱 Configuration Rapide : Terminal SSH sur iPad

### Avec Termius (Gratuit) :

1. **Installez Termius** depuis l'App Store
2. **Créez un nouveau host** :
   - Alias : `Korean Learning Machine`
   - Hostname : `192.168.1.44`
   - Port : `22`
   - Username : `daewon`
   - Password : (votre mot de passe Linux)
3. **Connectez-vous**
4. **Naviguez** : `cd ~/Documents/Korean_Daewon_Learning`

### Commandes Essentielles pour Votre Projet :

```bash
# Aller dans votre projet
cd ~/Documents/Korean_Daewon_Learning

# Voir la structure
tree -L 2  # ou ls -R si tree n'est pas installé

# Ouvrir une leçon
nano LESSONS/Week_01_Day_01.md

# Voir votre profil
cat STUDENT_PROFILE.md

# Voir le vocabulaire
cat VOCABULARY/Week_01_Vocabulary.md
```

---

## 🤖 Interagir avec l'Assistant AI via SSH

**Avec Cursor Agent**, vous avez un accès complet à l'assistant AI directement depuis votre terminal SSH !

### Comment ça fonctionne :

1. **Connectez-vous en SSH** depuis votre iPad
2. **Lancez Cursor Agent** : `cursor agent`
3. **Posez vos questions** directement dans le terminal
4. L'agent peut lire, modifier, créer des fichiers et exécuter des commandes

### Différence avec l'Assistant dans Cursor Desktop :

- **Cursor Desktop** : Interface graphique avec moi (l'assistant intégré)
- **Cursor Agent CLI** : Même intelligence, mais via terminal - parfait pour SSH !

Les deux utilisent la même technologie, donc vous obtenez les mêmes capacités.

---

## 🔧 Configuration Avancée

### Alias Utiles pour Cursor Agent

Ajoutez ces alias à votre `~/.bashrc` pour faciliter l'utilisation :

```bash
# Alias pour Cursor Agent
alias ca='cursor agent'
alias cagent='cursor agent'
alias cai='cursor agent --workspace ~/Documents/Korean_Daewon_Learning'

# Alias pour votre projet (déjà configuré)
alias korean='cd ~/Documents/Korean_Daewon_Learning'
alias ll='ls -lah'
```

Puis rechargez : `source ~/.bashrc`

### Améliorer l'Expérience Terminal sur iPad :

1. **Installer des outils utiles** :
```bash
# Tree pour voir la structure
sudo apt install tree

# Bat (meilleur que cat)
sudo apt install bat

# Fzf pour la recherche
sudo apt install fzf
```

2. **Utiliser tmux ou screen** (pour les sessions persistantes) :
```bash
sudo apt install tmux
# Puis : tmux new -s korean
# Cela permet de garder votre session Cursor Agent active même si la connexion SSH se coupe
```

### Workflow avec tmux (Recommandé pour SSH) :

```bash
# 1. Démarrer une session tmux
tmux new -s korean

# 2. Dans tmux, aller dans votre projet
korean

# 3. Lancer Cursor Agent
cursor agent

# 4. Si la connexion SSH se coupe, reconnectez-vous et :
tmux attach -t korean
# Votre session Cursor Agent sera toujours active !
```

---

## 🚀 Démarrage Rapide

Une fois connecté en SSH depuis votre iPad :

```bash
# 1. Aller dans votre projet
cd ~/Documents/Korean_Daewon_Learning
# ou utilisez l'alias
korean

# 2. Lancer Cursor Agent
cursor agent

# 3. Dans l'agent, demandez :
# "Montre-moi ma progression actuelle"
# "Ouvre la leçon Week_01_Day_01"
# "Crée des exercices de pratique pour les nombres"
# etc.
```

### Workflow Typique :

```bash
# Connexion SSH
ssh daewon@192.168.1.44

# Aller dans le projet
korean

# Lancer l'agent
cursor agent

# Interagir avec l'agent
> Montre-moi où j'en suis dans mon apprentissage
> Ouvre la leçon d'aujourd'hui
> Crée 10 exercices de pratique pour le vocabulaire de la semaine 1
```

---

## ❓ Questions Fréquentes

**Q : Puis-je utiliser l'assistant AI depuis le terminal SSH ?**  
R : **Oui !** Utilisez `cursor agent` pour avoir accès à l'assistant AI directement dans le terminal. C'est la solution parfaite pour SSH.

**Q : Quelle app terminal recommandez-vous ?**  
R : **Blink Shell** est excellent mais payant. **Termius** est gratuit et très bon. Les deux fonctionnent parfaitement avec Cursor Agent.

**Q : Dois-je me ré-authentifier à chaque fois ?**  
R : Non, l'authentification est sauvegardée. Vous n'avez besoin de vous connecter qu'une seule fois avec `cursor agent login`.

**Q : Puis-je utiliser git depuis le terminal SSH ?**  
R : Oui, absolument ! Git fonctionne parfaitement via SSH. Vous pouvez aussi demander à Cursor Agent d'exécuter des commandes git pour vous.

**Q : Comment quitter Cursor Agent ?**  
R : Tapez `exit` ou `quit`, ou utilisez `Ctrl+C`.

**Q : Puis-je utiliser Cursor Agent dans des scripts ?**  
R : Oui ! Utilisez `cursor agent --print "votre demande"` pour une utilisation non-interactive.

**Q : Quelle est la différence entre Cursor Desktop et Cursor Agent ?**  
R : Cursor Desktop est l'interface graphique complète. Cursor Agent est la version CLI - même intelligence, mais accessible via terminal (parfait pour SSH).

---

## 📞 Besoin d'Aide ?

Si vous avez des questions ou des problèmes, dites-moi simplement ce que vous voulez faire et je vous guiderai !

