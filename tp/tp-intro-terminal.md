## TP: Initiation au Terminal Linux

<blockquote>
    <h3>Prérequis</h3>
    <p>Aucune connaissance préalable du terminal n'est nécessaire, mais une familiarité avec les concepts de base de l'informatique est utile.</p>
</blockquote>

<blockquote>
    <h3>Objectif</h3>
    <p>Apprendre à naviguer dans le système de fichiers, gérer les fichiers et les répertoires via le terminal Linux.</p>
</blockquote>

---

### Partie 1: Introduction au Terminal

1. **Ouverture du Terminal**
   - Ouvrez le terminal via le menu des applications ou avec le raccourci clavier (souvent Ctrl+Alt+T).

2. **Découverte du Prompt**
   - Identifiez les parties du prompt : l'utilisateur, le nom de la machine, et le répertoire courant.

---

### Partie 2: Navigation dans le Système de Fichiers

1. **Afficher le Répertoire Courant**
   - Tapez `pwd` pour voir le chemin absolu du répertoire dans lequel vous vous trouvez.

2. **Changement de Répertoire**
   - Entrez `cd /` pour aller à la racine du système de fichiers.
   - Utilisez `pwd` pour confirmer le changement de répertoire.
   - Naviguez vers le répertoire personnel en tapant `cd ~` ou simplement `cd`.
   - Confirmez à nouveau avec `pwd`.

3. **Lister les Contenus d'un Répertoire**
   - Dans votre répertoire personnel, listez les fichiers et dossiers en utilisant `ls`.
   - Pour une vue complète, y compris les fichiers cachés et les détails comme les permissions, utilisez `ls -la`.

---

### Partie 3: Création et Gestion des Fichiers et Répertoires

1. **Création d'un Nouveau Répertoire**
   - Créez un répertoire nommé `TP_Linux` avec `mkdir TP_Linux`.

2. **Navigation et Exploration**
   - Naviguez dans `TP_Linux` avec `cd TP_Linux`.
   - Affichez votre emplacement avec `pwd`.
   - Listez le contenu (qui devrait être vide) avec `ls -la`.

3. **Création de Fichiers**
   - Dans `TP_Linux`, créez un fichier appelé `exercice1.txt` avec `touch exercice1.txt`.
   - Listez à nouveau le contenu pour voir le fichier nouvellement créé en utilisant `ls -la`.

4. **Manipulation de Fichiers**
   - Créez un sous-répertoire dans `TP_Linux` nommé `Dossier_Test` avec `mkdir Dossier_Test`.
   - Déplacez `exercice1.txt` dans `Dossier_Test` avec `mv exercice1.txt Dossier_Test/`.
   - Naviguez dans `Dossier_Test` et utilisez `ls -la` pour confirmer la présence de `exercice1.txt`.

---

### Partie 4: Écriture dans les Fichiers et Recherche de Contenu

1. **Écriture dans un Fichier**
   - Naviguez vers le répertoire `TP_Linux/Dossier_Test`.
   - Pour ajouter des noms de fruits dans `liste.txt`, utilisez `nano liste.txt`. Saisissez quelques noms de fruits, un par ligne (par exemple, Pomme, Banane, Cerise).
   - Sauvegardez le fichier et quittez `nano` avec `Ctrl + O`, `Enter` pour sauvegarder, puis `Ctrl + X` pour quitter.

2. **Vérification du Contenu**
   - Utilisez `cat liste.txt` pour afficher le contenu du fichier et vérifier l'ajout des noms de fruits.

3. **Recherche Simple avec `grep`**
   - Recherchez le mot "Pomme" dans le fichier avec `grep 'Pomme' liste.txt`.

---

### Partie 5: Affichage de Contenu de Fichier

1. **Utilisation de `cat`, `head`, et `tail`**
   - Affichez le contenu complet du fichier avec `cat liste.txt`.
   - Pour voir les premières lignes, utilisez `head liste.txt`, et pour les dernières, `tail liste.txt`.

---

### Partie 6: Création et Utilisation des Alias

Les alias permettent de créer des raccourcis pour des commandes longues ou utilisées fréquemment, rendant ainsi votre travail dans le terminal plus rapide et plus efficace.

1. **Création d'un Alias Temporaire**
   - Pour créer un alias temporaire (qui ne persiste que pour la session de terminal actuelle), utilisez la commande `alias`. Par exemple, pour raccourcir la commande `ls -la` en `ll`, tapez `alias ll='ls -la'`.
   - Essayez votre nouvel alias en tapant `ll`. Vous devriez voir le résultat de `ls -la`.

2. **Création d'un Alias Permanent**
   - Pour rendre un alias permanent, vous devez l'ajouter au fichier de configuration de votre shell, souvent `.bashrc` ou `.zshrc`, situé dans votre répertoire personnel. Ouvrez ce fichier avec `nano ~/.bashrc` (remplacez `.bashrc` par `.zshrc` si vous utilisez Zsh).
   - À la fin du fichier, ajoutez la ligne de l'alias que vous souhaitez rendre permanent, par exemple `alias ll='ls -la'`.
   - Sauvegardez et fermez le fichier. Pour que les changements prennent effet, rechargez le fichier de configuration en tapant `source ~/.bashrc` ou fermez et rouvrez votre terminal.

3. **Suppression d'un Alias**
   - Si vous souhaitez supprimer un alias temporaire durant votre session actuelle, utilisez `unalias [nom_de_l'alias]`. Par exemple, `unalias ll` supprimera l'alias `ll`.


### Résumé des Commandes

- `pwd` : Affiche le chemin du répertoire courant.
- `cd [chemin]` : Change le répertoire courant.
- `ls`, `ls -l`, `ls -a`, `ls -la` : Liste les fichiers et dossiers, avec `-l` pour le format long, `-a` pour inclure les cachés, et `-la` pour les deux.
- `mkdir [nom_dossier]` : Crée un nouveau répertoire.
- `touch [nom_fichier]` : Crée un nouveau fichier vide.
- `mv [source] [destination]` : Déplace ou renomme des fichiers ou dossiers.
- `nano [nom_fichier]` : Ouvre l'éditeur de texte nano.
- `cat [nom_fichier]` : Affiche le contenu d'un fichier.
- `head [nom_fichier]`, `tail [nom_fichier]` : Affichent les premières/dernières lignes d'un fichier.
- `grep 'texte' [nom_fichier]` : Recherche une chaîne de caractères dans un fichier.
- `alias [nom_de_l'alias]='commande'` : Crée un alias temporaire pour une commande.
- `unalias [nom_de_l'alias]` : Supprime un alias temporaire.
- `~/.bashrc` ou `~/.zshrc` : Fichiers de configuration pour Bash ou Zsh où ajouter des alias permanents.

