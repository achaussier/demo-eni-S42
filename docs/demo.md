# Présentation du markdown

## La syntaxe de base

### Les citations

> Linux c'est le bien :)
> 
> Et windows non ;)

### Texte simple

C'est un language de balisage qui permet de prendre des notes ...

Un super contenu.

### Les listes

#### Des checkbox

- [x] Pwet
- [ ] Pouet

#### Non ordonnées

Ma semaine :

- Le réseau

    Mon super contenu

- Les sous réseaux
- Le binaire
    - (dès le matin ...)

#### Ordonnées

Comment faire ...

1. Je pleure
2. Je comprends
   1. (un peu)
   2. ...


```bash
# Git commit from https://github.com/docker/docker-install when
# the script was uploaded (Should only be modified by upload job):
SCRIPT_COMMIT_SHA="${LOAD_SCRIPT_COMMIT_SHA}"
```

### Mise en forme

Je peux mettre **en gras**, *en italique* ou ~~barré~~, <span style="text-decoration: underline;">souligné c'est plus compliqué</span> !

Pour lister les lichiers, j'utilise `ls` avec l'option `-h`.

```bash
# Git commit from https://github.com/docker/docker-install when
# the script was uploaded (Should only be modified by upload job):
SCRIPT_COMMIT_SHA="${LOAD_SCRIPT_COMMIT_SHA}"

# strip "v" prefix if present
VERSION="${VERSION#v}"

# The channel to install from:
#   * stable
#   * test
#   * edge (deprecated)
#   * nightly (deprecated)
DEFAULT_CHANNEL_VALUE="stable"
if [ -z "$CHANNEL" ]; then
	CHANNEL=$DEFAULT_CHANNEL_VALUE
fi

DEFAULT_DOWNLOAD_URL="https://download.docker.com"
if [ -z "$DOWNLOAD_URL" ]; then
	DOWNLOAD_URL=$DEFAULT_DOWNLOAD_URL
fi

DEFAULT_REPO_FILE="docker-ce.repo"
if [ -z "$REPO_FILE" ]; then
	REPO_FILE="$DEFAULT_REPO_FILE"
fi

mirror=''
DRY_RUN=${DRY_RUN:-}
while [ $# -gt 0 ]; do
	case "$1" in
		--channel)
			CHANNEL="$2"
			shift
			;;
		--dry-run)
			DRY_RUN=1
			;;
		--mirror)
			mirror="$2"
			shift
			;;
		--version)
			VERSION="${2#v}"
			shift
			;;
		--*)
			echo "Illegal option $1"
			;;
	esac
	shift $(( $# > 0 ? 1 : 0 ))
done

```

### Les liens

- [Google](https://google.fr)
- [Administration Linux](./linux-admin.md)
- [Les citations](#les-citations)
- ![Tux rambo](https://cursowebnuevo.files.wordpress.com/2010/02/tux_rambo.png)
- [![Tux matrix](./images/matrix.png)](https://fr.wikipedia.org/wiki/Matrix_(film))


## Les tableaux

| Commande | Description |
| --- | --- |
| `ls` | Liste les fichiers |
| `mkdir` | Crée un répertoire |
