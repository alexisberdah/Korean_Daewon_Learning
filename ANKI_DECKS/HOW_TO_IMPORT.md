# 📥 COMMENT IMPORTER LES CARTES ANKI

## Méthode Rapide d'Import

### Étape 1: Télécharger le Fichier CSV
Le fichier est déjà créé: `Week_01_Day_01_Import.csv`

### Étape 2: Ouvrir Anki
1. Lancez Anki
2. Sélectionnez votre deck "Korean_Week_01_Foundation"

### Étape 3: Importer
1. **Fichier → Importer** (ou `Ctrl+Shift+I` / `Cmd+Shift+I`)
2. Naviguez vers: `/home/daewon/Documents/Korean_Daewon_Learning/ANKI_DECKS/`
3. Sélectionnez: `Week_01_Day_01_Import.csv`

### Étape 4: Configurer l'Import

Dans la fenêtre d'import, configurez:

**Type**: Basic (and reversed card) OU Basic
**Deck**: Korean_Week_01_Foundation
**Fields separated by**: Pipe (|)
**Allow HTML in fields**: ✓ (IMPORTANT!)

**Field mapping**:
- Field 1 → Front
- Field 2 → Back
- Field 3 → Tags

### Étape 5: Importer
1. Cliquez sur "Import"
2. Anki devrait confirmer: "30 notes added"
3. C'est fait! ✅

---

## Format du Fichier CSV

Le format utilisé:
```
Front | Back | Tags
```

- **Front**: Phrase coréenne avec mot cible
- **Back**: Traduction + détails + exemples (avec HTML pour le formatage)
- **Tags**: Mots-clés pour filtrer (week1, day1, etc.)

---

## 📱 IMPORT DEPUIS L'APPLICATION MOBILE

### Pour AnkiMobile (iOS - iPhone/iPad)

#### Méthode 1: Synchronisation via AnkiWeb (RECOMMANDÉE)

1. **Sur votre ordinateur**:
   - Importez le CSV dans Anki Desktop (voir instructions ci-dessus)
   - Fichier → Synchroniser (ou cliquez sur le bouton Sync)
   - Connectez-vous avec votre compte AnkiWeb

2. **Sur votre iPhone/iPad**:
   - Ouvrez AnkiMobile
   - Appuyez sur le bouton Sync (⟳) en haut à droite
   - Attendez que la synchronisation se termine
   - Vos nouvelles cartes apparaîtront automatiquement! ✅

#### Méthode 2: Import Direct via iTunes/Fichiers

1. **Transférer le fichier CSV**:
   - Envoyez-vous le fichier `Week_01_Day_01_Import.csv` par email OU
   - Utilisez AirDrop depuis votre Mac OU
   - Placez-le dans iCloud Drive

2. **Dans AnkiMobile**:
   - Ouvrez le fichier CSV (depuis Mail, Fichiers, etc.)
   - Choisissez "Ouvrir avec AnkiMobile"
   - AnkiMobile s'ouvrira automatiquement

3. **Configurer l'Import**:
   - Sélectionnez le deck: "Korean_Week_01_Foundation"
   - Type: "Basic" ou "Basic (and reversed card)"
   - Field separator: Pipe (|)
   - Allow HTML: ON (important!)
   - Confirmez l'import

---

### Pour AnkiDroid (Android)

#### Méthode 1: Synchronisation via AnkiWeb (RECOMMANDÉE)

1. **Sur votre ordinateur**:
   - Importez le CSV dans Anki Desktop (voir instructions plus haut)
   - Synchronisez avec AnkiWeb

2. **Sur votre téléphone Android**:
   - Ouvrez AnkiDroid
   - Appuyez sur l'icône de synchronisation (deux flèches circulaires)
   - Vos nouvelles cartes seront téléchargées automatiquement! ✅

#### Méthode 2: Import Direct depuis le Téléphone

1. **Transférer le fichier CSV sur votre téléphone**:
   - Par email (téléchargez la pièce jointe)
   - Via Google Drive, Dropbox, etc.
   - Connexion USB vers `/Android/data/com.ichi2.anki/files/`
   - Placez le CSV dans le dossier `AnkiDroid` ou `Downloads`

2. **Dans AnkiDroid**:
   - Ouvrez AnkiDroid
   - Appuyez sur ☰ (menu hamburger)
   - Sélectionnez "Importer un fichier"
   - Naviguez vers votre fichier CSV
   - Sélectionnez `Week_01_Day_01_Import.csv`

3. **Configurer l'Import**:
   - Deck: "Korean_Week_01_Foundation"
   - Type de note: "Basic" ou "Basic (inverser)"
   - Séparateur de champs: Pipe (|)
   - Autoriser HTML: ✓ (activé)
   - Appuyez sur "Importer"

---

## ⚡ Quelle Méthode Choisir?

| Méthode | Avantages | Inconvénients |
|---------|-----------|---------------|
| **Sync AnkiWeb** | • Automatique<br>• Garde tout synchronisé<br>• Pas de manipulation de fichiers | • Nécessite compte AnkiWeb (gratuit)<br>• Besoin d'internet |
| **Import Direct Mobile** | • Pas besoin d'ordinateur<br>• Fonctionne hors ligne | • Plus de manipulations<br>• Transfert de fichiers nécessaire |

**Recommandation**: Utilisez la synchronisation AnkiWeb! C'est de loin le plus simple et vous gardera tous vos appareils à jour. 🎯

---

## Pour les Prochains Jours

Je créerai des fichiers CSV pour chaque jour:
- `Week_01_Day_02_Import.csv`
- `Week_01_Day_03_Import.csv`
- etc.

Vous n'aurez qu'à répéter le processus d'import! 🚀

---

## Vérifier l'Import

Après l'import:
1. Allez dans votre deck "Korean_Week_01_Foundation"
2. Cliquez "Étudier maintenant"
3. Vérifiez que les cartes s'affichent correctement
4. Si le HTML ne s'affiche pas bien, activez "Allow HTML" dans les paramètres d'import

---

## Problèmes Courants

### "Les balises HTML s'affichent comme du texte"
→ Réimportez avec "Allow HTML in fields" ✓

### "Les caractères coréens ne s'affichent pas"
→ Vérifiez que votre système supporte UTF-8

### "Duplicate found"
→ Normal si vous réimportez. Choisissez "Update" ou "Skip"

---

**Gain de temps: ~45 minutes par jour! 🎉**

Au lieu de créer 30 cartes manuellement (1-2 min/carte), import en 30 secondes!


