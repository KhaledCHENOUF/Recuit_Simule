# Recuit_Simule

Introduction
Les problèmes NP-complets d'optimisation combinatoire sont caractérisés par une complexité exponentielle ou factorielle, par conséquent ; il est impossible d'énumérer toutes les solutions possibles car cela dépasse la capacité de calcul de n'importe quel ordinateur. Il est donc très difficile de trouver la solution optimale. Pour palier à ces problèmes, les chercheurs ont introduit des méthodes approchées appelées heuristiques, elles présentent l'avantage d'un temps de calcul réduit mais ne donnent aucune information sur la qualité de la solution trouvée, de plus elles ne sont en général applicables qu'a un seul type de problèmes, parmi ces méthodes heuristiques nous allons intéresser à l’algorithme de recuit simulé.
Algorithmes recuit simulé
Le recuit simulé applique itérativement l’algorithme de Metropolis, pour engendrer une séquence de configurations qui tendent vers l'équilibre thermodynamique :
1) Choisir une température de départ T=T0 et une solution initiale S=S0 ;
2) générer une solution aléatoire dans le voisinage de la solution actuelle ;
3) comparer les deux solutions selon le critère de Metropolis ;
4) répéter 2 et 3 jusqu'à ce que l'équilibre statistique soit atteint ;
5) décroitre la température et répéter jusqu'a ce que le système soit gelé.
Dans un premier temps, T étant généralement choisi très grand, beaucoup de solutions - même celles dégradant la valeur de f - sont acceptées, et l'algorithme équivaut à une visite
aléatoire de l'espace des solutions. Mais à mesure que la température baisse, la plupart des solutions augmentant l'énergie sont refusés, et l'algorithme se ramène à une amélioration itérative classique.
A température intermédiaire, l'algorithme autorise de temps en temps des transformations qui dégradent la fonction objective. Il laisse ainsi une chance au système de s'extraire d'un minima local.
Notons aussi que si la température est égale à 0, seules les solutions optimisant f sont acceptées. L'algorithme se comportera donc comme la méthode de la descente du gradient.

