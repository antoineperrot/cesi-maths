# Organisation de la journée 
## 1. 1h30 de cours magistral
## 2. Répartition en deux salles. 2 x 1h30 exercices/TP matrices - implémentation d'un modèle numérique
## 3. Retour au Cours magistral. Bilan de la journée. Correction collective. Parcours d'une méthode de résolution.

# 1) 1h30 CM
1. __Méthode num :__ Rappel des formules de quadrature et de leur ordre.
2. __Schémas temporels__: Rappel des schémas temporels présentés la semaine dernière et présentation RK4 (donné sans explications).
3. __Système dynamiques :__ présentation du modèle de Lotka-Volterra. Justification des équations.

# 2) Exercices et TP en autonomie


## A. __Matrices : maximum 45min/1h__.

Faire exercice 3 de la feuille d'exos.

Si déjà fait faire exo 4.

N'hésitez pas à me demander quand vous êtes bloqués.
## B. __Méthodes numériques :__ 

__Priorité absolue :__
Faire une prévision du système de Lotka-Volterra avec la méthode d'Euler explicite. Plotter les résultats :
1. Les séries temporelles : càd l'évolution des populations au cours du temps
2. Le portrait de phase : plotter la trajectoire dans le temps du point $X(t) = \left(x(t), y(t) \right)$ dans le plan $\mathbb{R}^2$. Vous devez normalement obtenir une orbite.

__Puis :__
Implémenter les schémas temporels RK2 et RK4. Faire 3 prévisions en faisant varier seulement le schéma temporel utilisé, en considérant un pas de temps "assez grand". Plotter sur un même graphe les 3 prévision (séries temporelles ou portrait de phase au choix). Comparer.

### Approfondissement (que je vous invite à continuer chez vous !)


__1)__ Si vous maîtrisez les classes en Python, ré-arrangez votre code en créant une classe "Model" générique.

Cette classe doit obligatoirement disposer 
- d'un attribut "trend" (noté $f$ dans le cours sur les systèmes dynamiques) indéfini (None) pour la classe générique Model, et qui sera ensuite écrasé lors de la création de classes héritières.
-  d'une méthode de prévision "forecast" ayant pour paramètres (x0, t_final, dt)

Vous créérez ensuite une classe héritière de Model que vous appelerez "LotkaVolterra", sur laquelle vous redéfinirez/complèterez le constructeur et la l'attribut "trend", afin de rendre possible les simulations du système de Lotka-Volterra.

__2) Vérification numérique de l'ordre des schémas temporels__

Pour vérifier l'ordre d'un schéma temporel, on compare, pour un problème dont on connaît la solution analytique, l'approximation numérique fournie par le schéma temporel avec le résultat théorique attendu. 

On considère donc par exemple le problème suivant : $x'(t) = - x(t)$ avec $x(0)=1$, qui a pour solution analytique $x(t) = e^{-t}$.

L'erreur numérique associée à une prévision numérique se calcule de la façon suivante :

$\varepsilon = \max_{1 \leq i \leq n} || x(t_n) - x_n ||$, où $x_n \simeq x(t_n)$ est l'approximation numérique de $x(t_n)$.

Pour un schéma temporel donné :
1. Réaliser une prévision en conservant toujours le même temps final $t_f$ et en ne faisant varier que la taille du pas de temps.
2. Plotter l'erreur en fonction du pas de temps.

Pour __Euler explicite__ par exemple, vous devriez obtenir une droite avec une pente de 1 : lorsque le pas de temps est divisé par 10, l'erreur est également divisée par 10.

Pour __Runge-Kutta 2__ par exemple, vous devriez obtenir une droite avec une pente de 2 : lorsque le pas de temps est divisé par 10, l'erreur est également divisée par 10^2.


# Retour CM

## A) Correction exo matrice

## B) Parcours d'un notebook de "correction".