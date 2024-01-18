# utility-scripts
Vous avez une collection de scripts utiles destinés à simplifier le processus de développement de projets en langage C et en utilisant Git. Voici une description de chaque script et de son utilité :

-**__addc (Ajout de fichier C)__**:

Utilité : Cette commande vous permet de créer facilement un fichier source en langage C avec des préconfigurations. Le fichier résultant inclura un "main" prêt à l'emploi, le EpiHeader (qui semble être un en-tête standard), et la syntaxe de base.
Syntaxe : ```addc nomdufichier```

-**__addh (Ajout de fichier d'en-tête)__** :

Utilité : Cette commande vous aide à créer un fichier d'en-tête en langage C avec des configurations de base. Le fichier créé contiendra le EpiHeader et la directive "pragma once" (pour éviter les inclusions multiples).
Syntaxe : ```addh nomdufichier```

-**__adds (Ajout de fichier shell)__** :

Utilité : Cette commande simplifie la création d'un fichier shell en ajoutant automatiquement le shebang (ligne d'interpréteur) pour les scripts shell.
Syntaxe : ```adds nomdufichier```

-**__addt (Ajout de fichier de test unitaire)__** :

Utilité : Cette commande vous permet de générer un fichier de test unitaire pour vos projets. Le fichier résultant contiendra le EpiHeader, les inclusions nécessaires, ainsi qu'une fonction de test.
Syntaxe : ```addt nomdufichier```

-**__push (Envoi de code vers GitHub)__** :

Utilité : Cette commande automatise le processus de mise à jour de votre code sur GitHub. Elle effectue un "git add," "git commit," et "git push" en une seule commande, vous permettant de soumettre facilement vos modifications.
Syntaxe : ```push "le contenu du commit"```

-**__getlib (Récupération d'une bibliothèque depuis GitHub)__** :

Utilité : Cette commande vous permet de récupérer une bibliothèque à partir de son référentiel GitHub si vous avez renseigné l'URL du référentiel. Elle simplifie le processus de gestion des dépendances en clonant automatiquement la bibliothèque.
Syntaxe : ```getlib "votre commit"```

-**__genmake (Génération de Makefile)__** :

Utilité : Cette commande vous permet de générer un Makefile depuis le dossier où vous vous trouver.
Syntaxe : ```genmake [-d] [-f folder_path]"```

Ces scripts visent à accélérer le processus de développement en automatisant les tâches courantes liées à la création de fichiers source, d'en-tête, de scripts shell, de tests unitaires, et à la gestion des modifications via Git. Ils vous permettent de gagner du temps et de maintenir une structure cohérente dans vos projets.
