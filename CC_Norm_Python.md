# Coder en Python à la norme python du Coding Club

### Mon Code je le formate comment ?

A voir... UTF-8, Unicode etc..

### Tabs ou espaces ?

|Choix | Pourquoi ?|
|----|-----|
|Tabs | sûreté de l’indentation |
|Espaces | conversion des tabs en espace une fois le code terminé |

Préférence choisie le : 08/06/2020 pour les tabs

### Code en français ou en Anglais ?

Le code en anglais semble préféré

### Nom des variables, fonctions :

Le code étant en anglais, les noms de variables et fonctions doivent être en anglais explicite, en minuscule, et avec des _ pour représenter les espaces entre mots.

Attention !

Pour bien faire les choses nous avons mit en place des exceptions :

Pour les cordonnées : x y z sont autorisés
Pour les boucles for : i et e sont autorisés
Pour préciser des cordonnées x différente, on rajoute un nom explicite devant exemple : map_x, guy_x
 
### Nom des class :

Tout mots dans le nom de la class doivent commencer par une majuscule : ex MyClassIsBeautiful(self,...)
### Les Majuscules et les espaces

La [snake case](https://en.wikipedia.org/wiki/Snake_case) convention à été évoquée

Ce qui signifie que les espaces sont remplacés par des "_" et tout est écrit en minuscules par exemple :

`Hello World` deviendra `hello_world`

### Nombre de caractère par ligne : 

Pour ne pas avoir des lignes trop longues qui dépasseraient l'écran, nous vous conseillons de limiter 80 caractères par lignes.


### If Else Elif

Pas trop de branches if/elif/else 
(Généralement on est pas censé avoir besoin de plus de  5 else/if/elif pour faire UNE action) : 

```python
if condition1:
    fait_tel_chose
elif conditiion2:
    fait_ça
elif condition3:
    fait_cela
elif condition4:
    fait_ceci
else:
    bah_fait_ça
```

Ce genre de "forêt de if" est peu recommandé et ne devrait être utilisé qu'en dernier recours

Il à été aussi évoqué que faire trop de if s'imbriquant les uns sur les autres doivent être évités et minimisés a 3 imbrications :

```python
if condition:
    if condition:
        if condition:
            faire_beaucoup_de_lignes_ensuite
```

Ceci n'est pas très beau est recommandé il serait plus propre de généralement le diviser par une fonction comme ceci : 

```python
def pour_faire_plusieurs_trucs():
    if condition == False:
        return None
    faire_100_lignes_ensuite
    

if condition:
    if condition:
        pour_faire_plusieurs_trucs()
```

De plus si vous avez beaucoup de if imbriqués cela peut donner à des choses extrêmement complexes du genre : 

```python
if condition1:
    if condition2:
        if condition3:
            dothat()
        elif condition5:
            dothat2()
        elif condition9:
            dothat3()
    elif condition7:
        if condition 8:
            dothat9()
    else:
        dothat10()
elif:
    dothat11()
    if condition12:
        dothat11()
else:
    exit
```
Cela peut semble exagéré mais croyez moi cela n'est clairement pas un cas inconnu et peut se retrouver dans de nombreux code en ligne illisible de plus qu nous n'avons pas encore ajouter d'opérateurs `or` ou `and`

### Les opérateurs or et and

Comme pour les lignes de code "basiques", si votre condition dépasse 80 caractères les opérateurs or ou and se place en fin de ligne.
```python

if Vore > Eino and Helife > Stan or
Eino >= Stan:
	ton_actionblablablablabla
``` 

### Comment éviter tant conditions ?

Il peut arriver que souvent les fonctions et les operateurs and et or ne sont pas la solution !

Il y a juste trop de possibilités et sa reviendrait a créer plus dizaines de petites fonctions et des conditions que l'on peut éviter

Dans ce genre de cas on peut faire des tableaux ou dictionnaires : 

```python
#Dictionaires

dictionary = {
    "surname": "Eino",
    "name": "Sorcière",
    "year": 1992
}

for x in dictionary: #print le dictionnaire un a un
    print(dictionary[x]) 

if "name" in dictionary: #Retourne une valeur True car name existe
    print("Yes")

#Arrays

names = ["Eino", "JC", "Jarod"] #names[0] = Eino, names[1] = JC, names[2] = Jarod, names[3] n'existe pas !

x = len(names) #Sera égal à 3

for x in names: #Print tous les noms un à un
  print(x) 
```

Avec tout ceci vous devriez pouvoir gérer presque tous les cas et si meme cela n'est pas assez il existe aussi les tableaux a deux dimensions !

### Tableaux et Dico :

Les Tableaux et dictionnaires sont différents, donc nous avons décidé de différencier les deux.

Les éléments de tableau se feront les uns à côté des autres : ['Eino','Vore','Stan','Ade','Helife']


Quant aux dictionnaires, les éléments se feront les uns en dessous des autres :

```python

dictionary = {
	"surname": "Eino",
	"age": "40",
	"job": "Reconfiné",

	"surname": "Stan",
	"age"; "29",
	"job": "Chasseur de carapuce"

}


```

### Opérateur binaire ( + , - , *...) :

Les opérateur à l'inverse des or et and se placent en début de ligne et non les uns après les autres.

```python
resultat = moyenne_math
	   + moyenne_fr
	   - moyenn_total
```

#### Fonction

### Nombre de ligne par fonction :

Il est normal d'avoir des fonctions dans tout langage de programmation, mais il faut savoir limiter les actions d'une fonction.

En effet, beaucoup de fonctions exécute du code inutile ou plutôt qui pourrait être mit dans une autre fonction.

C'est pour cela que nous recommandons 45 lignes maximum par fonction.

### Nombre de fonction par fichier :

Il est important de ne pas avoir un fichier qui déborde de fonction et code inutile, c'est pour cela que nous posons une limite de 10 fonctions par fichier

### Nombre de ligne blanche entre fonctions :

Pour avoir un code lisible par tous, il est important de le laisser respirer, 1 ligne entre fonction sera suffisant pour rendre votre code lisible

### Nombre de ligne blanche entre class et fonction :

Comme pour les lignes blanches entre fonctions, il est important de laisser de la place et de dissocier la class et les fonctions.

Nous recommandons 2 lignes entre class et fonction.



