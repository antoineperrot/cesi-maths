# Lois de probabilité discrètes

# Introduction aux Variables Aléatoires Discrètes

Une **variable aléatoire discrète** est une variable qui peut prendre un nombre fini ou dénombrable de valeurs distinctes. Par exemple, considérons le lancer d'un dé. Les valeurs possibles sont {1, 2, 3, 4, 5, 6}.

> On considèrera des variables aléatoire sur $\mathbb{N}$ ou des sous-ensembles de $\mathbb{N}$.

## Caractérisation d'une variable aléatoire discrète
Ici, on considère l'ensemble discret $E \subset \mathbb{N}$.

### Fonction de Masse de Probabilité (FMP)
Soit $E$ un ensemble discret, $f$ est une fonction de masse de probabilité sur $E$ si $f$ vérifie :
1. $\forall x \in E, f(x)) \geq 0$
2. $\sum_{x \in E} f(x) = 1$

Alors, $f$ définie une loi de probabilité sur $E$.

> $X$ est une variable aléatoire suivant la loi induite par $f$ si $\mathbb{P}(X = x) = f(x)$
### Fonction de distribution cumulative sur $\mathbb{N}$
Soit $F: \mathbb{N} \mapsto \mathbb{R}$. $F$ induit une loi de probabilité sur $E$ si
1. $\forall n \in \mathbb{N}, F(n)) \geq 0$
2. $F$ est croissante
3. $\lim_{n \to \infty} F(n) = 1$

> $X$ est une variable aléatoire suivant la loi induite par $F$ si $\mathbb{P}(X <= x) = F(x)$
## Espérance et variance 
[Formule variance](https://www.nagwa.com/fr/explainers/893163473169/#:~:text=D%C3%A9finition%20%3A%20Variance%20d'une%20variable,%C3%A9cart%2Dtype%20de%20la%20variable.)
## Loi de Bernouilli
- introduction
- calculer esperance
- calculer variance

Donner des exemples de la vie courante qui correspondent à la loi de Bernouilli
## Intro loi binomiale
> Rappel formule du binôme de Newton
Exo intro :
- une usine fabrique des roues en inox. Un boulon est défectueux avec proba $p$.

Les roues sont vendues par lots de $n$.
Soit $X$ le nombre de roues défectueuses dans un lot.
- dire quelles valeurs prend $X$
- modéliser X en fonction de plusieurs variables IID Bernoulli
- calculer la probabilité d'avoir aucune piece d'effectueuse
  - 1
  - toutes
  - k pieces defectueuses, 0 <= k <= n

- calculer espérance de x
- variance de x

## Loi géométrique
Une personne cherche à rencontrer l'ame soeur via un site de rencontres et participe à des dates.
On note $p$ la probabilité d'un match lors d'un date.
On note $X$ le numéro du date correspondant à la rencontre de l'ame soeur.
- (Ecrire $X$ en fonction de variables de Bernouilli)
- Calculer la probabilité de rencontrer l'ame soeur au 1er date, au 2eme date, au 3eme date, au n-eme date ?
- Calculer le nombre moyen de dates pour rencontrer l'ame soeur
- Calculer la variance
- Calculer la fonction de distribution cumulative


## Loi de Poisson
Donner la formule de la loi de poisson.

- Vérifier que la somme de f(x) fait bien 1.
- Calculer l'espérance de la loi de poisson
- la variance

> La loi de Poisson permet par exemple de modéliser des durées entre deux événements.

## Mêler Loi géométrique et loi de poisson
On fait l'hypothèse qu'après une rupture, le temps moyen avant de se sentir prêt à rencontrer quelqu'un d'autre suit une loi de Poisson de paramètre $\mu$.
On considère que le temps écoulé en jours entre deux dates suit la loi de poisson de paramètre $\lambda$.
Modéliser le temps écoulé avant la rencontre de l'âme soeur par une variable aléatoire $T$ de votre composition.

$$
T = R + \sum_{i=1}^X Z_i
$$



avec $R \sim \mathcal{P}(\mu), Z_i \sim \mathcal{P}(\lambda)$ et $X \sim \mathcal{G}(p)$ 

1. Calculer l'espérance de $T$.

## Jupyter notebook
1. Coder une fonction simulant renvoyant $n$ variables de Bernouilli
2. Coder une fonction simulant une variable binomiale
3. Coder une fonction simulant une variable géométrique
4. Coder une fonction simulant la variable $T$. -> Fixer des paramètres pour les valeurs lambda, mu et p
5. Calculer empiriquement l'espérance de $T$. Vérifier que cela concorde avec l'espérance théorique.

    
