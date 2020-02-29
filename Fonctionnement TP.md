# Fonctionnement TP

## Dépôts Git

Deux dépôts Git :

-   le premier, public, permet aux étudiants de cloner les sources. Il est accessible par tous en lecture seule. On y trouve la base de code source à utiliser pour tous les TPs ;
-   le second permet aux étudiants de créer et pousser leur branche de travail. L'étudiant est le seul à avoir accès à sa branche de travail.

La base de code contient :

1.  les squelettes de code de tous les TPs ;
2.  les codes de test et de benchmark ;
3.  les fichiers CMake décrivant :
    1.  les options de compilation ;
    2.  les cibles de test et de benchmark.

Les cibles de test et de benchmark vérifient que les résultats des calculs sont conformes à ceux attendus et produisent des résultats de performances. Ceux-ci permettent de vérifier l'efficacité des implémentations par rapport à un chiffre attendu sur la version de référence dans le dépôt privé.

## 

## 

## 

## 

## 

## Déroulement des TPs

1.  L'étudiant clône le dépot principal. Celui-ci contient les squelettes de code de tous les exercices ainsi que les CMake correspondants qui permettent de compiler et d'exécuter les tests et les benchmarks.
2.  L'étudiant, en travaillent sur l'exercice, peut lancer ses tests et benchmarks à distance sur le PC central de test (si pas un PC de calcul/étudiant). Pour ce faire, il pousse sa branche de travail et lance une requête de test/benchmark sur le PC de test. Jenkins ?
3.  Une fois qu'il est satisfait du résultat, il applique un tag au commit souhaité. Celui-ci fera foi lors de l'évaluation.

## 

## Besoins techniques

-   Un PC connecté au réseau et équipé d'un CPU multi-cœurs raisonnablement puissant et d'un GPU de calcul Nvidia. On y installera une cible Docker qui permettra de faire tourner le serveur de tests et de benchmark.
-   Deux dépôts Git, potentiellement sur le serveur de calcul.