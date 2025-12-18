# 🚀 Guide Rapide : Cursor Agent via SSH (iPad)

## Première Utilisation

### 1. Connectez-vous en SSH depuis votre iPad
```bash
ssh daewon@192.168.1.44
```

### 2. Authentifiez-vous (une seule fois)
```bash
cursor agent login
```
Si pas d'interface graphique : `NO_OPEN_BROWSER=1 cursor agent login`

### 3. Vérifiez votre statut
```bash
cursor agent status
```

---

## Utilisation Quotidienne

### Option A : Simple
```bash
# 1. SSH
ssh daewon@192.168.1.44

# 2. Aller dans le projet
korean

# 3. Lancer l'agent
cursor agent
# ou simplement
ca
```

### Option B : Avec tmux (Recommandé)
```bash
# 1. SSH
ssh daewon@192.168.1.44

# 2. Démarrer/Reprendre session tmux
tmux new -s korean
# ou si déjà existante
tmux attach -t korean

# 3. Dans tmux
korean
ca
```

---

## Commandes Essentielles

### Alias Disponibles :
- `korean` → Va dans votre projet
- `ca` ou `cagent` → Lance Cursor Agent
- `cai` → Lance Cursor Agent directement dans le projet
- `ll` → Liste détaillée des fichiers

### Dans Cursor Agent :
- Tapez vos questions directement
- `exit` ou `quit` pour quitter
- `Ctrl+C` pour annuler/interrompre

---

## Exemples de Questions

```
> Montre-moi ma progression actuelle
> Ouvre la leçon Week_01_Day_01
> Crée 10 exercices de pratique pour les nombres coréens
> Ajoute ces mots au vocabulaire de la semaine 1
> Vérifie mes réponses dans les exercices
> Résume ce que j'ai appris cette semaine
```

---

## Aide

- Guide complet : `cat CURSOR_SSH_GUIDE.md`
- Statut agent : `cursor agent status`
- Aide agent : `cursor agent --help`

