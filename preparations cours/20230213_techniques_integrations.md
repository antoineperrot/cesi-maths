# Cours Techniques d'intégration (6h)

cours du 13 et 20 février 2023 au CESI.

## 1. Intégrale de Riemann
Inférieure             | Supérieure
:-------------------------:|:-------------------------:
![](https://raw.githubusercontent.com/antoineperrot/cesi-maths/main/ets/data/Riemann_Integration_and_Darboux_Lower_Sums.gif)  |  ![](https://raw.githubusercontent.com/antoineperrot/cesi-maths/main/ets/data/Riemann_Integration_and_Darboux_Upper_Sums.gif)

__Définition:__

[Pages 1 et 2](https://github.com/antoineperrot/cesi-maths/blob/main/notes%20de%20cours/methodes_numeriques.pdf)


$\varepsilon$


## 2. Changement de variable

__Objectif:__ On cherche à calculer 
$\int_a^bf(x)dx$

### 2.1 Cours
__Théorème du changement de variable:__
Soit la fonction $varphi$ admettant une dérivée continue sur l'intervalle $[t_1, t_2]$ définit par $t_1 = \varphi^{-1}(a)$ et $t_2 = \varphi^{-1}(b)$, alors

$$
\color{red}\int_a^bf(x)dx=\int_{\varphi^{-1}(a)}^{\varphi^{-1}(b)}f[\varphi(t)]\varphi'(t)dt
$$

> __Intérêt :__ Si $\varphi$ est bien choisie, la nouvelle intégrale est  potentiellement plus simple que celle de départ.

### 2.2 Exercices

#### Exo 1

Calculer les intégrales suivantes en utilisant un changement de variable

1. $$\int_1^4\frac{1-\sqrt t}{\sqrt t}dt$$
1. $$\int_0^{\pi}\frac{\sin t}{1+\cos^2 t}dt$$
1. $$\int_1^e \frac{dt}{2t\ln (t)+t}$$

[Exercices supplémentaires (faire exo 3)](https://www.i2m.univ-amu.fr/perso/clothilde.melot/_media/enseignement:correction_complete_integration.pdf)
## 3. Intégration par parties

## 4. Intégration numérique

### 4.1 Formules de quadratures
### 4.2 Ordre des formules de quadrature



