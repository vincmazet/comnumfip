# COMNUMFIP

**Comnumfip** est un module Python pour les TP de communications numériques
à [Télécom Physique Strasbourg](http://www.telecom-physique.fr/).
Il est associé au cours de [Communications numériques](https://vincmazet.github.io/comnum/).


## Installation

Téléchargez le code en cliquant sur le bouton _Code_ ci-dessus, puis _Download ZIP_.
Décompressez les fichiers dans votre dossier de travail.


## Documentation


### eyediag

`eyediag(t, x, T, alpha=.5, color="tab:blue")`

Diagramme de l'oeil.

Entrées :
* **t** (array) : temps
* **x** (array) : signal
* **T** (scalar) : durée d'un symbole
* **alpha** (scalar) : transparence (0,5 par défaut)

Sortie :
* aucune


### randmary

`randmary(N,p)`

Génération d'une séquence M-aire.

Entrées :
> N (scalar) : taille de la séquence (nombre de symboles)
>
> P (array)   : probabilité des symboles (sa taille correspond à la taille de l'alphabet)

Sortie :
> c (array) : séquence aléatoire M-aire où M = len(P).

Exemples :

```
# séquence binaire de taille 1000, symboles équiprobables :
c1 = randmary(1000,[0.5, 0.5])

# séquence binaire de taille 100, p("0") = 0.3, p("1") = 0.7 :
c2 = randmary(100,[0.3, 0.7])

# séquence 4-aire de taille 10, symboles équiprobables :
c3 = randmary(10,np.ones(4)/4)
```


### bin2mary

`bin2mary(x,M)`

Convertit une séquence binaire en séquence M-aire.
Si la taille de x n'est pas multiple de log2(M), des "0" sont rajoutés à la fin de x.

Entrées :
> x (array)  : séquence binaire
>
> M (scalar) : taille de l'alphabet de la séquence traduite (M est une puissance de 2)
    
Sortie :
> y (array) : séquence M-aire



### mod_a, mob_b, mod_c, mod_d, mod_e

`mod_a(x, v, d)`

`mod_b(x, v, d)`

`mod_c(x, v, d)`

`mod_d(x, v, d)`

`mod_e(x, v, d)`

Modulations mystères A, B, C, D et E.

Entrées :
> x (array)    : séquence binaire
>
> v (scalaire) : amplitude de la forme d'onde
>
> d (scalaire) : durée de la forme d'onde
    
Sorties :
> t (array) : vecteur temps
>
> y (array) : signal modulé


## Licence

Ce programme est distribué sous licence CeCILL-B (www.cecill.info).
Copyright Université de Strasbourg 2021.
Contributeur : vincent.mazet@unistra.fr.