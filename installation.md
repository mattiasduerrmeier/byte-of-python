# Installation {#installation}

Lorsque nous nous r�f�rons � "Python 3" dans ce livre, nous ferons r�f�rence � toute version de Python �gale ou sup�rieure � la version Python [Python 3.6.0](https://www.python.org/downloads/).

## Installation sous Windows

Visitez https://www.python.org/downloads/ et t�l�chargez la derni�re version. Au moment d'�crire ces lignes, c'�tait Python 3.5.1
L'installation est comme n'importe quel autre logiciel bas� sur Windows.

Notez que si votre version de Windows est ant�rieure � Vista, vous devez [t�l�charger Python 3.4 uniquement](https://www.python.org/downloads/windows/) car les versions ult�rieures n�cessitent des versions plus r�centes de Windows.

ATTENTION: Assurez-vous de cocher l'option `Ajouter Python 3.5 au PATH`.

Pour changer l'emplacement d'installation, cliquez sur `Personnaliser l'installation`, puis sur `Suivant` et entrez `C:\python35` (ou un autre emplacement appropri�) comme emplacement d'installation.

Si vous n'avez pas coch� l'option `Ajouter Python 3.5 au PATH` plus t�t, cochez `Ajouter Python aux variables d'environment`. Cela fait la m�me chose que `Ajouter Python 3.5 au PATH` sur le premier �cran d�installation.

Vous pouvez choisir d'installer Launcher pour tous les utilisateurs ou non, peu importe. Launcher est utilis� pour basculer entre diff�rentes versions de Python install�es.

Si votre chemin n'a pas �t� d�fini correctement (en cochant les options `Ajouter Python 3.5 au PATH` ou `Ajouter Python aux variables d'environment`), suivez les �tapes d�crites dans la section suivante (`Invite de commandes DOS )` pour y rem�dier. Sinon, allez � la section `Lancer l'invite de commandes Python sous Windows` de ce document.

REMARQUE: Si vous connaissez d�j� la programmation et que vous �tes familiers avec Docker consultez [Python dans Docker](https://hub.docker.com/_/python/) et [Docker sous Windows](https://docs.docker.com/windows/).

### Invite de commandes DOS {#dos-prompt}

Si vous voulez pouvoir utiliser Python � partir de la ligne de commande Windows, c'est-�-dire � l'invite de commande DOS, vous devez d�finir la variable PATH de mani�re appropri�e.

Pour Windows 2000, XP, 2003, cliquez sur `Panneau de configuration` -> `Syst�me` -> `Avanc�` -> `Variables d�environnement`. Cliquez sur la variable nomm�e `PATH` dans la section _Variables syst�me_, puis s�lectionnez `Modifier` et ajoutez � la fin de ce qui est d�j� l� `;C:\Python36` (veuillez v�rifier que ce dossier existe, il sera diff�rent pour les versions plus r�centes de Python). Bien s�r, utilisez le nom de r�pertoire appropri�.

<!-- Le r�pertoire doit correspondre � la variable pythonVersion de book.json -->
Pour les versions plus anciennes de Windows, ouvrez le fichier `C:\AUTOEXEC.BAT` et ajoutez la ligne`PATH=%PATH%;C:\Python36` et red�marrez le syst�me. Pour Windows NT, utilisez le fichier `AUTOEXEC.NT`.

Pour Windows Vista:

- Cliquez sur D�marrer et choisissez `Panneau de configuration`
- Cliquez sur Syst�me. � droite, vous verrez "Afficher les informations de base sur votre ordinateur".
- A gauche, une liste de t�ches dont la derni�re est `Param�tres syst�me avanc�s`. Cliquez dessus.
- L'onglet `Avanc�` de la bo�te de dialogue `Propri�t�s syst�me` est affich�. Cliquez sur le bouton `Variables d'environnement` en bas � droite.
- Dans la zone inf�rieure intitul�e `Variables syst�me`, faites d�filer jusqu'� "PATH" et cliquez sur le bouton `Modifier`.
- Modifiez votre chemin au besoin.
- Red�marrez votre syst�me. Sur mon ordinateur, Vista n'a pas pris en compte la modification de la variable d'environnement avant mon red�marrage.

Pour Windows 7 et 8:

- Cliquez avec le bouton droit sur Ordinateur de votre bureau et s�lectionnez `Propri�t�s` ou cliquez sur `D�marrer` et choisissez `Panneau de configuration` -> `Syst�me et s�curit�` -> `Syst�me`. Cliquez sur `Param�tres syst�me avanc�s` sur la gauche, puis sur l'onglet `Avanc�`. En bas, cliquez sur "Variables d'environnement" et sous "Variables syst�me", recherchez la variable `PATH`, s�lectionnez-la, puis appuyez sur `Modifier`.
- Allez � la fin de la ligne sous `Valeur de la variable` et ajoutez `;C:\Python36` (veuillez v�rifier que ce dossier existe, il sera diff�rent pour les versions les plus r�centes de Python) � la fin de ce qui existe d�j�. Bien s�r, utilisez le nom de dossier appropri�.
- Si la valeur �tait `%SystemRoot%\system32;` il deviendra maintenant `%SystemRoot%\system32;C:\Python36` <!-- Le r�pertoire doit correspondre � la variable pythonVersion de book.json -->
- Cliquez sur `OK` et vous avez termin�. Aucun red�marrage n'est requis, mais vous devrez peut-�tre fermer et rouvrir la ligne de commande.

Pour Windows 10:

- Menu D�marrer de Windows> `Param�tres` > `� propos de` > `Informations syst�me` (tout � droite) > `Param�tres syst�me avanc�s` > `Variables d�environnement` (vers le bas) > Choisissez `Variable Path` et cliquez sur `Modifier`)> `New` > (tapez le lieu de votre emplacement python. Par exemple, `C:\Python36\`)

### Lancer l'invite de commandes Python sous Windows

Pour les utilisateurs Windows, vous pouvez ex�cuter l'interpr�teur en ligne de commande si vous avez d�fini [la variable `PATH` de mani�re appropri�e](#DOS-prompt).

Pour ouvrir le terminal sous Windows, cliquez sur le bouton D�marrer, puis sur Ex�cuter. Dans la bo�te de dialogue, tapez `cmd` et appuyez sur la touche`[Entr�e]`.

Ensuite, tapez `python` et assurez-vous qu'il n'y a pas d'erreur.

## Installation sous Mac OS X

Pour les utilisateurs de Mac OS X, utilisez [Homebrew](http://brew.sh): `brew install python3`.

Pour v�rifier, ouvrez le terminal en appuyant sur les touches `[Commande + Espace]` (pour ouvrir la recherche Spotlight), tapez `Terminal` et appuyez sur la touche `[Entr�e] `. Maintenant, lancez `python3` et assurez-vous qu'il n'y a pas d'erreur.

## Installation sous GNU/Linux

Pour les utilisateurs GNU / Linux, utilisez le gestionnaire de paquets de votre distribution pour installer Python 3, par exemple. sur Debian et Ubuntu: `sudo apt-get update && sudo apt-get install python3`.

Pour v�rifier, ouvrez le terminal en ouvrant l�application `Terminal` ou en appuyant sur `Alt + F2` et en entrant `gnome-terminal`. Si cela ne fonctionne pas, reportez-vous � la documentation de votre distribution GNU/Linux. Ensuite, lancez `python3` et assurez-vous qu'il n'y a pas d'erreur.

Vous pouvez voir la version de Python � l'�cran en lan�ant:

<!-- The output should match pythonVersion variable in book.json -->
```
$ python3 -V
Python 3.6.0
```

NOTE: `$` est l'invite du shell. Ce sera diff�rent pour vous selon le param�trage du syst�me d'exploitation de votre ordinateur, par cons�quent, je vais indiquer l'invite uniquement par le symbole `$`.

ATTENTION: la sortie peut �tre diff�rente sur votre ordinateur, selon la version du logiciel Python install� sur votre ordinateur.

## R�capitulatif

A partir de maintenant, nous supposerons que Python est install� sur votre syst�me.

Ensuite, nous �crirons notre premier programme Python.
