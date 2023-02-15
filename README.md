# animationBadgeVGP

Ceci est une application WPF destinée à générer un fichier qui va contenir des séquences de coloration des diodes des badges VGP

## fichier de sortie

### format

Le fichier de sortie est au format JSON

### structure

1. 1 tableau contenant les étapes
2. pour chaque étape,
  1. 3 tableaux (1 par lettre)
  2. un délai avant le passage à l'étape d'après (le dernier est à 0 pour garder une structure homogène)
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
		"délai": 500
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
		"délai": 1000
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
		"délai": 0
	}
]
```

## dépendances

bibliothèque "colorPicker.dll"

## utilisation de l'interface graphique

### 1. nouvelle animation

Dans le menu "Animation", cliquez sur le bouton "Nouvelle". Chaque diode sera blanche

### 2. coloration d'une diode

1. Cliquez sur la diode à colorer
2. Le sélecteur de couleur va se mettre à jour pour afficher la couleur actuelle de la diode
3. Si besoin, utilisez le sélecteur de couleur pour définir une nouvelle couleur

### 3. définition du délai

Saisissez dans le champ dédié la durée à attendre avant de passer à la prochaine étape. Cette durée est exprimée en millisecondes
Attention, dans un souci d'homogénéité, le dernier délai est imposé et vaudra toujours 0

### 4. sélection d'une étape en particulier

Dans la liste des étapes déjà créées, sélectionnez celle que vous souhaitez visualiser et modifiez-la au besoin

### 5. fonctionnalités

1. actuelles
2. à venir
	1. création d'une animation
	2. sauvegarde de l'animation dans un fichier
	3. modification de l'ordre des étapes
	4. chargement d'une animation à partir d'un fichier