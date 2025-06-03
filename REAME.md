# Fast Command Project (FCP) - README

Ce document explique chaque commande du toolkit Fast Command Project et comment les utiliser efficacement.

## Table des Matières

- Installation
- Commandes de Création de Fichiers
- Contrôle de Version
- Construction de Projet
- Style de Codage
- Gestion des Fonctions
- Commandes Utilitaires

## Installation

### [`FCP-Installer`](./FCP-Installer)
Installateur automatisé pour le toolkit Fast Command Project. Cet installateur télécharge tous les scripts nécessaires, configure votre environnement et prépare votre système pour l'utilisation de FCP.

```bash
# Télécharger l'installateur
curl -O https://raw.githubusercontent.com/lagie-marin/utility-scripts-manager/main/download.ptr

# Le rendre exécutable
chmod +x FCP-Installer

# Exécuter l'installateur
./FCP-Installer
```

### [`fcp-setup`](fcp-setup)

Configure l'environnement FCP en créant les répertoires nécessaires et en mettant à jour votre .bashrc.
```bash
fcp-setup
```

### [`script-manager`](script-manager)

Met à jour et installe les scripts FCP depuis le dépôt.
```bash
script-manager                 # Mettre à jour tous les scripts
script-manager command1 cmd2   # Mettre à jour des scripts spécifiques
```

## Commandes de Création de Fichiers
### [`addc`](addc)
Crée un fichier C avec l'en-tête Epitech et vous permet d'inclure des fichiers d'en-tête.
```bash
addc [-u] nomfichier        # -u pour mettre à jour le script
```
### [`addh`](addh)
Crée un fichier d'en-tête avec l'en-tête Epitech et les gardes d'inclusion appropriées.
```bash
addh [-u] nomfichier        # -u pour mettre à jour le script
```
### [`adds`](adds)
Crée un script shell avec les permissions appropriées.
```bash
adds [-u] nomfichier        # -u pour mettre à jour le script
```
### [`addt`](addt)
Crée un fichier de test pour les tests unitaires Criterion.
```bash
addt [-u] nomfichier        # -u pour mettre à jour le script
```

## Version Control
### [`push`](push)
Wrapper pour les commandes git add, commit et push.
```bash
push [-u] [-f nomfichier] "message de commit"   # -u pour mettre à jour, -f pour spécifier un fichier
```

## Construction de Projet
### [`genmake`](genmake)
Génère un Makefile automatiquement basé sur la structure du projet.

```bash
genmake [-l] [-n nom] [-f dossier] [-i dossier_à_ignorer]
  -l              # Générer pour une bibliothèque
  -n nom          # Définir le nom du binaire
  -f dossier      # Définir le dossier source
  -i dossier/fichier  # Ignorer des dossiers spécifiques
  -force          # Forcer l'inclusion d'autres Makefiles
  -u              # Mettre à jour le script
```

### [`getlib`](getlib)
Clone et gère les bibliothèques pour votre projet.
```bash
getlib [-u]       # -u pour mettre à jour le script
```

## Style de Codage
### [`csr`](csr)
Affiche la documentation pour les codes d'erreur de style de codage.
```bash
csr              # Vérifier le style de codage
```
### [`doc_csr`](doc_csr)

Affiche la documentation pour les codes d'erreur de style de codage.
```bash
doc_csr -e CODE             # Afficher la documentation pour un code d'erreur
doc_csr -l                  # Lister tous les codes d'erreur
doc_csr -r fichier.pdf      # Enregistrer un PDF de référence
```
### [`translate_csr`](translate_csr)
Traduit les codes d'erreur de style de codage en descriptions lisibles.
```bash
translate_csr -e CODE       # Traduire un code d'erreur
translate_csr -r fichier.pdf # Enregistrer un PDF de référence
translate_csr -u            # Mettre à jour le script
```

## Gestion des Fonctions
### [`fexport`](fexport)
Exporte des fonctions et des macros de votre projet vers JSON pour réutilisation.
```bash
fexport -init langage       # Initialiser pour un langage
fexport -macros             # Exporter toutes les macros
fexport nom_fonction        # Exporter une fonction spécifique
fexport -u                  # Mettre à jour le script
```
### [`fimport`](fimport)
Importe des fonctions précédemment exportées dans votre projet.
```bash
fimport fonction1 fonction2  # Importer des fonctions avec leurs dépendances
fimport -u                   # Mettre à jour le script
```

## Utility Commands

### [`get_config`](get_config)
Obtient les valeurs de configuration du fichier de configuration FCP.
```bash
get_config CLE_CONFIG       # Obtenir une valeur de configuration
```

### func
Bibliothèque de fonctions communes utilisées par d'autres scripts (généralement non utilisé directement).

### [`help_emacs`](help_emacs)
Affiche les raccourcis clavier d'Emacs.
```bash
help_emacs
```
### [`mr_clean`](mr_clean)
Nettoie les fichiers temporaires et générés de votre projet.
```bash
mr_clean
```
## Configuration
FCP stocke sa configuration dans config.ptr. Les paramètres clés incluent:

- LIB - Activer/désactiver les fonctionnalités de bibliothèque
- CODING_STYLE_RULES - Commande pour les vérifications de style de codage
- EPI_HEADER - Format pour l'en-tête Epitech

Pour modifier les configurations, utilisez get_config pour lire les valeurs et modifiez directement le fichier pour les changer.

## Requirements

- jq (processeur JSON)