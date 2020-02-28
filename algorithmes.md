# Algorithmes

## Définition

Bien qu'il n'existe pas de consensus absolu sur la définition du terme « algorithme », nous tâcherons d'en proposer une. Celle-ci s'inspire du sens proposé par Donald E. Knuth [1].

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

Pour permettre l'exécution d'un algorithme, il faut disposer d'un système d'exécution capable d'interpréter l'algorithme. Pour ce faire, il est nécessaire de traduire l'algorithme dans un langage adapté à ce système, dit **langage machine**. On dit alors qu'on **implante** l'algorithme.

**Exemples de paires système d'exécution/langage machine :**

-   Le métier Jacquard, inventé en 1801 par Joseph Marie Jacquard, est un des premiers exemples de systèmes programmables. Il exploitait des cartes perforées pour tisser des motifs de tissage complexes ;
-   Le pianola, instrument de musique capable de reproduire une partition écrite sur deux rouleaux de papier perforés ;
-   Un joueur de Rubik's Cube peut lire des séries d'instructions représentant des mouvements, par exemple : FRUR'U'F' ;
-   Un microprocesseur exploite des instructions au format binaire qui correspondent à des opérations élémentaires (logiques, arithmétiques, mémoire…) ;
-   Un interpréteur Python applique des instructions directement écrites dans le langage Python : il transforme à la volée le code au format texte en code binaire exploitable par un microprocesseur.

Les langages interprétés tels que le C, l'ADA ou le Fortran ne sont pas des langages machine : ils requièrent une phase de compilation pour transformer le code écrit en binaire.

Enfin, il existe des langages qualifiés d'intermédaires tels que Java, Scala. Ceux-ci exploitent une machine virtuelle qui se charge d'exécuter à la volée des instructions en un code machine spécifique en les transformant en langage machine binaire pour le microprocesseur.

## Exemple : algorithme de calcul du prix d'une liste de courses

-   Données d'entrée : liste des articles avec leur prix ;

-   Données de sortie : prix total des articles de la liste de courses ;

-   Algorithme :
    1.  Initialiser une valeur **somme** à 0 ;
    2.  Pour chaque article de la liste de courses, ajouter son prix à la valeur **somme** ;
    3.  Renvoyer la valeur de sortie **somme**.
    
    

[1] Donald E. Knuth, *Algorithmes*, Stanford, CSLI Publications, 2011, 510 p.