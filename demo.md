# Continuité d'une Fonction

## Définition

Une fonction $f$ est **continue** en un point $a$ si :

$$\lim_{x \to a} f(x) = f(a)$$

Cela signifie que trois conditions doivent être satisfaites :
1. $f(a)$ est défini
2. $\lim_{x \to a} f(x)$ existe
3. $\lim_{x \to a} f(x) = f(a)$

---

## Exemple 1 : Fonction Continue

### Fonction : $f(x) = x^2 + 2x - 1$

Démontrons que $f$ est continue au point $a = 1$.

**Étape 1** : Calculer $f(1)$
$$f(1) = 1^2 + 2(1) - 1 = 1 + 2 - 1 = 2$$

**Étape 2** : Calculer $\lim_{x \to 1} f(x)$
$$\lim_{x \to 1} (x^2 + 2x - 1) = 1^2 + 2(1) - 1 = 2$$

**Conclusion** : Puisque $\lim_{x \to 1} f(x) = f(1) = 2$, la fonction est **continue** en $a = 1$.

---

## Exemple 2 : Fonction Discontinue

### Fonction définie par morceaux :

$$f(x) = \begin{cases}
x + 1 & \text{si } x < 2 \\
5 & \text{si } x = 2 \\
x + 2 & \text{si } x > 2
\end{cases}$$

Étudions la continuité au point $a = 2$.

**Étape 1** : $f(2) = 5$ ✓

**Étape 2** : Limite à gauche
$$\lim_{x \to 2^-} f(x) = \lim_{x \to 2^-} (x + 1) = 3$$

**Étape 3** : Limite à droite
$$\lim_{x \to 2^+} f(x) = \lim_{x \to 2^+} (x + 2) = 4$$

**Conclusion** : Puisque $\lim_{x \to 2^-} f(x) \neq \lim_{x \to 2^+} f(x)$, la fonction n'est **pas continue** en $a = 2$.

---

## Exemple 3 : Continuité avec Epsilon-Delta

### Démonstration rigoureuse

Soit $f(x) = 3x + 2$ au point $a = 1$.

Pour tout $\epsilon > 0$, trouvons $\delta > 0$ tel que :
$$|x - 1| < \delta \implies |f(x) - f(1)| < \epsilon$$

**Calcul** :
- $|f(x) - f(1)| = |3x + 2 - 5| = |3x - 3| = 3|x - 1|$
- Si $|x - 1| < \delta$, alors $|f(x) - f(1)| = 3|x - 1| < 3\delta$
- Nous voulons $3\delta = \epsilon$, donc $\delta = \frac{\epsilon}{3}$

**Conclusion** : Pour tout $\epsilon > 0$, en posant $\delta = \frac{\epsilon}{3}$, on a la continuité au sens d'Epsilon-Delta.

---

## Propriétés Importantes

| Propriété | Description |
|-----------|-------------|
| **Somme** | $f + g$ continue si $f$ et $g$ continues |
| **Produit** | $f \cdot g$ continue si $f$ et $g$ continues |
| **Quotient** | $\frac{f}{g}$ continue si $g \neq 0$ |
| **Composition** | $f \circ g$ continue si $f$ et $g$ continues |

---

## Graphique Conceptuel

```
Fonction Continue          Fonction Discontinue
     |                           |
    /                           /|
   /                           / |
  /____                      /  |___
 |    \                     |
```
