# Guide de Compilation des Diagrammes UML

## Prérequis

Pour compiler les diagrammes PlantUML, vous avez plusieurs options :

### Option 1 : PlantUML en ligne (Recommandé pour simplicité)
1. Allez sur http://www.plantuml.com/plantuml/uml/
2. Copiez le contenu de chaque fichier `.puml`
3. Collez dans l'éditeur en ligne
4. Téléchargez l'image PNG générée

### Option 2 : Installation locale
```bash
# Installer Java (requis)
sudo apt-get install default-jre

# Télécharger PlantUML
wget http://sourceforge.net/projects/plantuml/files/plantuml.jar/download -O plantuml.jar

# Compiler un diagramme
java -jar plantuml.jar diagramme.puml
```

### Option 3 : Extension VS Code
1. Installer l'extension "PlantUML" dans VS Code
2. Ouvrir un fichier `.puml`
3. Utiliser `Ctrl+Shift+P` puis "PlantUML: Export Current Diagram"

## Fichiers à compiler

Dans le dossier `diagrammes/`, vous trouverez :

1. **use_case_diagram.puml** → `use_case_diagram.png`
   - Diagramme de cas d'utilisation
   - Montre les interactions entre acteurs et système

2. **sequence_reservation.puml** → `sequence_reservation.png`
   - Diagramme de séquence pour la réservation
   - Flux complet de réservation avec paiement

3. **sequence_inscription_prestataire.puml** → `sequence_inscription_prestataire.png`
   - Diagramme de séquence pour l'inscription prestataire
   - Processus en 2 étapes avec validation OTP

4. **class_diagram.puml** → `class_diagram.png`
   - Diagramme de classes des modèles de données
   - Relations entre entités

5. **activity_diagram.puml** → `activity_diagram.png`
   - Diagramme d'activité du processus de réservation
   - Flux de décision et actions

6. **architecture_diagram.puml** → `architecture_diagram.png`
   - Vue d'ensemble de l'architecture système
   - Composants et leurs interactions

7. **state_diagram.puml** → `state_diagram.png`
   - Diagramme d'états d'un rendez-vous
   - Cycle de vie complet

## Instructions pour Overleaf

1. **Créer le projet Overleaf :**
   - Nouveau projet → Blank Project

2. **Ajouter le fichier principal :**
   - Copier le contenu de `rapport_projet.tex`
   - Coller dans le fichier `main.tex` d'Overleaf

3. **Créer le dossier diagrammes :**
   - Clic droit dans Overleaf → New Folder → `diagrammes`

4. **Ajouter les images :**
   - Compiler chaque fichier `.puml` en PNG
   - Upload chaque PNG dans le dossier `diagrammes/` d'Overleaf
   - Noms des fichiers : `use_case_diagram.png`, `sequence_reservation.png`, etc.

5. **Compiler le rapport :**
   - Cliquer sur "Recompile" dans Overleaf
   - Le PDF sera généré avec tous les diagrammes

## Résolution recommandée

Pour une qualité optimale dans le PDF :
- Exporter les diagrammes en PNG avec une résolution de 300 DPI
- Taille recommandée : 1200px de largeur minimum

## Dépannage

Si les images ne s'affichent pas :
1. Vérifier que les noms de fichiers correspondent exactement
2. S'assurer que les images sont dans le bon dossier `diagrammes/`
3. Vérifier que les extensions sont bien `.png` (en minuscules)

## Structure finale dans Overleaf

```
Projet Overleaf/
├── main.tex (contenu de rapport_projet.tex)
└── diagrammes/
    ├── use_case_diagram.png
    ├── sequence_reservation.png
    ├── sequence_inscription_prestataire.png
    ├── class_diagram.png
    ├── activity_diagram.png
    ├── architecture_diagram.png
    └── state_diagram.png
```