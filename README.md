# 🔍 Détecteur de caractère GS1

Outil de diagnostic standalone pour identifier le caractère GS1 généré par les douchettes scanner lors de la lecture de datamatrix.

## 🎯 Objectif

Certaines douchettes génèrent des caractères différents pour le séparateur GS1 dans les codes datamatrix. Cet outil permet d'identifier facilement quel caractère clavier est produit par le driver de votre douchette.

## 📱 Utilisation

1. **Ouvrir la page** : Ouvrez `index.html` dans votre navigateur
2. **Scanner le datamatrix** : Utilisez votre douchette pour scanner le code affiché sur la page
3. **Voir le résultat** : L'outil affiche automatiquement :
   - Le caractère généré
   - Le code de touche (keyCode)
   - Le nom de la touche
   - Le code ASCII
4. **Copier le résultat** : Cliquez sur "Copier le résultat" pour copier les informations

## 🔧 DataMatrix de test

Le datamatrix de test contient la séquence :
```
010123456789012817261030110ABCD1234[GS1]17654
```

Où `[GS1]` est le caractère séparateur à identifier.

## 📋 Format de sortie

Le résultat copié contient :
```
Caractère GS1 détecté:
Caractère: [caractère ou nom]
Code de touche: [keyCode]
Nom de la touche: [nom technique]
Code ASCII: [code ASCII]

Généré par l'outil de détection GS1
```

## 🌐 Déploiement

Pour héberger sur GitHub Pages :

1. Créer un repository sur GitHub
2. Uploader le fichier `index.html`
3. Activer GitHub Pages dans les paramètres du repository
4. Partager l'URL générée

## 🛠️ Fonctionnalités

- ✅ Détection automatique du scan (basée sur la vitesse de frappe)
- ✅ Interface intuitive avec feedback visuel
- ✅ Affichage des caractères de contrôle (TAB, CR, LF, etc.)
- ✅ Copie automatique des résultats
- ✅ Compatible avec tous les navigateurs modernes
- ✅ Aucune dépendance externe

## 🔍 Caractères GS1 courants

Les caractères GS1 les plus fréquents selon les douchettes :
- `]C1` (ASCII 29) - Caractère de contrôle GS
- `\t` (ASCII 9) - Tabulation
- ` ` (ASCII 32) - Espace
- `\x1E` (ASCII 30) - Record Separator

## 🐛 Dépannage

**Le scan n'est pas détecté :**
- Vérifiez que la page a le focus
- Essayez de cliquer sur la zone de scan avant de scanner
- Vérifiez que votre douchette est configurée pour envoyer un retour à la ligne

**Caractère non affiché correctement :**
- L'outil gère automatiquement les caractères de contrôle
- Consultez la section debug pour plus d'informations

## 📄 Licence

Outil libre d'utilisation pour diagnostic technique.
