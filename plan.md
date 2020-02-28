# Algorithmes (3h ?)

Rappel, éléments préliminaires.

## Définition (5 min., cours)

Proposition d'une définition.

## Instructions (10 min., cours)

Précisions sur le concept d'instruction de manière très générale.

## Implantation (15 min., cours)

Concept d'implantation, code machine, langage compilé/interprété/intermédiaire.

## Exemple d'algorithme (10 min., cours)

## TD (2h ?)

Proposer un exemple de système d'exécution/jeu d'instruction et faire réaliser quelques implémentations sur papier.

Référence à TIS-100.

## Travail à réaliser (noté)

L'exemple du TD est dispo sur GitHub, mettre en pratique les implémentations du TD et aller plus loin.

# Architecture CPU (10h ?)

## Processeur généraliste GPP (30 min ?, cours)

Notions d'architecture matérielle des microprocesseurs. ALU.

Registres, FLOPS.

Référence à NAND Game.

## Mode scalaire/séquentiel (1h ?, cours)

Performances en mode scalaire/séquentiel : fréquence, prédiction de branches, cache.

Loi de Moore sur la fréquence. Limites de la loi de Moore.

Courbes de fréquence des CPU avec le temps. Chute des fréquences au moment du passage au multi-cœurs sans chute de FLOPS. Pourquoi ?

Éventuellement, montrer un exemple sur le PC avec variation de la fréquence.

## Parallélisme (8h)

### Bases (20 min ?, cours)

Pourquoi le parallélisme ? Intéret. Top 500.

Intérêt, loi d'Amhdal.

### TPs dirigés (notés avec rapport + code à rendre sur GitHub)

On essaiera de faire avancer les TPs autour d'un algorithme qui jouera le rôle de fil conducteur. Idéalement, un algo orienté blockchain tel que du calcul de hash.

#### Premiers exemples de // en C++ (1h ?)

-   Utilisation des std::thread.
-   Exemples basiques.
-   Premier algo // pour voir de meilleurs performances = résultat cool, fait monter la hype.
-   Notion de *embarassingly parallel*.
-   Notions de facteur de mise à l'échelle ==> fil conducteur.

#### Problèmes de parallélisation (pour faire chuter la hype) (2h ?)

On s'intéresse à un algorithme pas facilement parallélisable.

-   Lecture/écriture concurrente ==> mutex ==> performances pourries. (30 min. ?)

-   Lecture/écriture concurrente ==> mutex ==> deadlock. (15 min. ?)

-   Lecture écriture concurrente ==> std::atomic ==> limites. (15 min. ?)

-   Lecture/écriture concurrente ==> patterns de parallélisation avancés, sans TBB (1h ?)

    À chaque étape, on mesure le scaling. Conclusions.

#### TBB (2h ?)

-   Introduction aux lambdas (30 min. ?)
-   OpenMP et tbb::parallel_for (30 min. ?) ==> WHAT ?! On pouvait faire tout ça aussi simplement ?!
-   Autres patterns de parallélisation (1h max, aller aussi loin que possible)
-   Exercice facultatif : résultats sympa, genre fractale.

#### SIMD (facultatif, à voir… 2h)

-   Bases avec Intel Intrinsics Guide,
-   VCL ou autre bibliothèque du genre.

#### Travail à réaliser indépendamment (noté)

Implémentation d'un algorithme orienté blockchain :

-   Séquentiel,
-   Parallèle simple (méthode au choix),
-   Parallèle avec SIMD si abordé (méthode au choix).

Mesures de performances et mise à l'échelle.

## Conclusions sur le CPU (20 min., moment de cours interactif)

-   Relativement simple à paralléliser en SIMT, moins en SIMD.
-   Très versatile.
-   Rapport FLOPS/W et FLOPS/€.

# Architecture GPU