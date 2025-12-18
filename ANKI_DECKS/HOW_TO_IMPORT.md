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


