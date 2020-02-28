## Définition

Bien qu'il n'existe pas de consensus absolu sur la définition du terme « algorithme », nous tâcherons d'en proposer une. Celle-ci s'inspire du sens proposé par Donald E. Knuth (Donald E. Knuth, Algorithmes, Stanford, CSLI Publications, 2011, 510 p.).

Nous définirons donc un algorithme comme un ensemble d**'instructions** agissant sur des **données d'entrée** (en informatique, des chaînes de 0 et de 1) pour produire des **données de sortie**. Celles-ci sont interprétées par un **système d'exécution** mis en œuvre par un **utilisateur**.

```sequence
Utilisateur->Système d'exécution: Données d'entrée
Note right of Système d'exécution: Algorithme
Système d'exécution->Utilisateur: Données de sortie
```

## Instructions

Les instructions d'un algorithme doivent être **explicites**, de manière à pouvoir être interprétées directement par le système d'exécution :

-   « Multiplier la valeur entière **a** par 2 » est une instruction explicite ;
-   « Déterminer une valeur **b** telle que **b** ÷ 2 = **a** » n'est pas une instruction explicite.

Elles doivent également être rigoureuses et sans ambiguïté :

-   Avec **a** et **b** deux valeurs booléenes, l'instruction « b = a ou b et b » est ambigüe ;
-   L'instruction « assigner à **b** la valeur de la racine carrée de  **a** » n'est pas rigoureuse. Quid du cas où **a** est négatif ?

Enfin, les instructions doivent pouvoir être exécutées en un temps fini par un système adapté.

## Implantation

Pour permettre l'exécution d'un algorithme, il faut disposer d'un système d'exécution capable d'interpréter l'algorithme et traduire l'algorithme dans un langage adapté à ce système.

**Exemples de paires **

##### Exemple : algorithme de calcul du prix d'une liste de courses

-   Données d'entrée : liste des articles avec leur prix ;
-   Données de sortie : prix total des articles de la liste de courses ;
-   Algorithme :
    1.  Initialiser une valeur **somme** à 0 ;
    2.  Pour chaque article de la liste de courses, ajouter son prix à la valeur **somme** ;
    3.  Renvoyer la valeur de sortie **somme**.