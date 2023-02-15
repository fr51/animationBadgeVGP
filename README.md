# animationBadgeVGP

Ceci est une application WPF destin�e � g�n�rer un fichier qui va contenir des s�quences de coloration des diodes des badges VGP

## fichier de sortie

### format

Le fichier de sortie est au format JSON

### structure

1. 1 tableau contenant les �tapes
2. pour chaque �tape,
  1. 3 tableaux (1 par lettre)
  2. un d�lai avant le passage � l'�tape d'apr�s (le dernier est � 0 pour garder une structure homog�ne)
3. pour chaque lettre, 1 couleur par diode

### exemple

```
[
	{
		"V":
		[
			"#FF0000",
			"#FF0000",
			"#FF0000",
			"#FF0000",
			"#FF0000",
			"#FF0000",
			"#FF0000"
		],
		"G":
		[
			"#FF0000",
			"#FF0000",
			"#FF0000",
			"#FF0000",
			"#FF0000",
			"#FF0000"
		],
		"P":
		[
			"#FF0000",
			"#FF0000",
			"#FF0000",
			"#FF0000",
			"#FF0000",
			"#FF0000",
			"#FF0000"
		],
		"d�lai": 500
	},
	{
		"V":
		[
			"#00FF00",
			"#00FF00",
			"#00FF00",
			"#00FF00",
			"#00FF00",
			"#00FF00",
			"#00FF00"
		],
		"G":
		[
			"#00FF00",
			"#00FF00",
			"#00FF00",
			"#00FF00",
			"#00FF00",
			"#00FF00"
		],
		"P":
		[
			"#00FF00",
			"#00FF00",
			"#00FF00",
			"#00FF00",
			"#00FF00",
			"#00FF00",
			"#00FF00"
		],
		"d�lai": 1000
	},
	{
		"V":
		[
			"#0000FF",
			"#0000FF",
			"#0000FF",
			"#0000FF",
			"#0000FF",
			"#0000FF",
			"#0000FF"
		],
		"G":
		[
			"#0000FF",
			"#0000FF",
			"#0000FF",
			"#0000FF",
			"#0000FF",
			"#0000FF"
		],
		"P":
		[
			"#0000FF",
			"#0000FF",
			"#0000FF",
			"#0000FF",
			"#0000FF",
			"#0000FF",
			"#0000FF"
		],
		"d�lai": 0
	}
]
```

## d�pendances

biblioth�que "colorPicker.dll"

## utilisation de l'interface graphique

### 1. nouvelle animation

Dans le menu "Animation", cliquez sur le bouton "Nouvelle". Chaque diode sera blanche

### 2. coloration d'une diode

1. Cliquez sur la diode � colorer
2. Le s�lecteur de couleur va se mettre � jour pour afficher la couleur actuelle de la diode
3. Si besoin, utilisez le s�lecteur de couleur pour d�finir une nouvelle couleur

### 3. d�finition du d�lai

Saisissez dans le champ d�di� la dur�e � attendre avant de passer � la prochaine �tape. Cette dur�e est exprim�e en millisecondes
Attention, dans un souci d'homog�n�it�, le dernier d�lai est impos� et vaudra toujours 0

### 4. s�lection d'une �tape en particulier

Dans la liste des �tapes d�j� cr��es, s�lectionnez celle que vous souhaitez visualiser et modifiez-la au besoin

### 5. fonctionnalit�s

1. actuelles
2. � venir
	1. cr�ation d'une animation
	2. sauvegarde de l'animation dans un fichier
	3. modification de l'ordre des �tapes
	4. chargement d'une animation � partir d'un fichier