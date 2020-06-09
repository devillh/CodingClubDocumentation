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

### Les Majuscules et les espaces

La [snake case](https://en.wikipedia.org/wiki/Snake_case) convention à été évoquée

Ce qui signifie que les espaces sont remplacés par des "_" et tout est écrit en minuscules par exemple :

`Hello World` deviendra `hello_world`

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

Ce genre de "forêt de if" est peu recommandé et ne devrait etre utilisé qu'en dernier recours

Il à été aussi évoqué que faire trop de if s'imbriquant les uns sur les autres doivent etre évités et minimisés a 3 imbrications :

```python
if condition:
    if condition:
        if condition:
            faire_beaucoup_de_lignes_ensuites
```

Ceci n'est pas très beau est recommandé il serait plus propre de généralement le diviser par une fonction comme ceci : 

```python
def pour_faire_plusieurs_trucs():
    if condition == False:
        return None
    faire_100_lignes_ensuites
    

if condition:
    if condition:
        pour_faire_plusieurs_trucs()
```

De plus si vous avez beaucoup de if imbriqués cela peut donner à des choses extrememnts complexes du genre : 

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
Cela peut semble exagéré mais croyez moi cela n'est clairement pas un cas inconnu et peut se retrouver dans de nombreux code en ligne illisiblent de plus qu nous n'avons pas encore ajouter d'opérateurs `or` ou `and`

### Les operateurs or et and

A venir...

### Comment eviter tant conditions ?

Il peut arriver que souvent les fonctions et les operateurs and et or ne sont pas la solution !

Il y a juste trop de possibilités et sa reviendrait a créer plus dizaines de petites fonctions et des conditions que l'on peut eviter

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