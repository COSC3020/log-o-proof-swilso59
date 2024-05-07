[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/fbkbKZ5N)
# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

## Proof

- Using the definiton of big $O$ with $\log_{2}n$ we get.
  - $\ T(n) \leq c_1 \times \log_{2}n\space for\space all\space n\space \geq n_1 $
- Now we can express this in terms of $\log_{5}n$ using the change of base formula.
  - $\log_{2}n = \frac{\log_{5}n}{\log_{5}2}$
- This now gives us.
  -  $\ T(n) \leq c_1 \times \frac{\log_{5}n}{\log_{5}2}\space for\space all\space n\space \geq n_1 $
- Next we can pull out the constant variable $\frac{1}{\log_{5}2}$
- This now gives us.
  - $T(n) \leq \frac{c_1}{log_{5}2} \times \log_{5}n\space for\space all\space n \geq n_1$
- Using the definition of Big $O$ we can see that $T(n) \in O(\log_{2}n)$
- This can also be done with $\log_{5}n$ to show us that $T(n) \in O(\log_{5}n)$
- Since we can use the change of base formula for the logarithm and pull out a constant factor it allows us to use either base within the 
  definition of big $O$.

  Reviewed repository from log-o-swilso59, and talked with the TA about correcting proof.
