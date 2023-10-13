### A little background on *q*-state Potts

The *q*-state [Potts model](https://en.wikipedia.org/wiki/Potts_model)
describes a lattice of classical spins *σ* = {1, 2, ..., *q*} and has
Hamiltonian

*H* =  − ∑<sub> &lt; *i**j*&gt;</sub>*δ*<sub>*σ*<sub>*i*</sub> = *σ*<sub>*j*</sub></sub>
Note that the model has an *S*<sub>*q*</sub> global symmetry
corresponding to permuting the states of the spins; a permutation *τ* on
{1, 2, ..., *q*} will yield a global symmetry operation
{*σ*<sub>*i*</sub>} → {*τ*(*σ*<sub>*i*</sub>)}. There are also several
spatial symmetries corresponding to reflections and translations.

I’ll be imagining a 2d square lattice throughout the following. At a
finite temperature, the model above is known for having continuous phase
transitions for *q* ≤ 4 and suffering from first-order phase transitions
for *q* &gt; 4. For *q* just slightly larger than 4 the correlation
length actually becomes quite large near the first-order transition,
which sounds reasonable because of the “proximity” to a continuous
transition at smaller *q* and real coupling with diverging correlation
length. A description and discussion of this large correlation length in
terms of proximity to fixed points at *q* &gt; 4 for complex coupling is
given in [this](https://arxiv.org/abs/1807.11512)
[pair](https://arxiv.org/abs/1808.04380) of papers.

Consider the continuous phase transition for *q* ≤ 4. The phase
transition is in fact described by a conformal field theory which is
rational for *q* = 2, 3, 4 with corresponding central charges
$c=\frac{1}{2}, \frac{4}{5}, 1$.

### Perturbing the 3-state Potts model on the square lattice

If I explicitly break the *S*<sub>3</sub> symmetry of the standard
3-state Potts model down to a ℤ<sub>3</sub> symmetry in a sufficiently
gentle way, will the finite-temperature symmetry-breaking phase
transition stay in the 3-state Potts universality class? In particular,
my gently perturbed Hamiltonian will now be

*H*(*λ*) =  − ∑<sub> &lt; *i**j*&gt;</sub>*δ*<sub>*σ*<sub>*i*</sub> = *σ*<sub>*j*</sub></sub> + *λ*∑<sub> &lt; *i**j**k*&gt;</sub>*δ*<sub>*σ*<sub>*i*</sub> = (*σ*<sub>*j*</sub>+1) = *σ*<sub>*k*</sub></sub>

where ∑<sub> &lt; *i**j**k*&gt;</sub> sums over all sets of three
adjacent spins in a row and three adjacent spins in a column. I imagine
*λ* to be small and positive. This perturbation explicitly breaks
*S*<sub>3</sub> down to the ℤ<sub>3</sub> subgroup of cyclic
permutations of the states 1, 2, 3. Note I’m being a little loose with
notation in that indicator functions are meant by my Kronecker deltas
and *σ*<sub>*i*</sub> = (*σ*<sub>*j*</sub>+1) = *σ*<sub>*k*</sub> is to
be understood mod 3.

The *λ* term has the following physical effect. For *λ* = 0, at very low
temperatures, my symmetry-broken state will look like small bubbles of
excitations on top of an otherwise uniform state. For example, if my
symmetry-broken state favors 1s, I’ll have mostly 1s with a sprinkle of
small bubbles of 2s and 3s on top. For *λ* &gt; 0 and small, I’m now
additionally penalizing one of the two kinds of bubbles. For example, if
my symmetry-broken state favors 1s, the small bubbles of 3s will be
penalized.

Note that *λ* has little effect on the energy cost of big, rounded
bubbles of 3s in a background of 1s – e.g. a perfectly horizontal domain
wall between 1s and 3s will only get an energy cost from the usual Potts
term and will be unaffected energy-wise by the *λ* term.

### Universality class of the perturbed model’s phase transition

The model *H*(*λ*&gt;0) will undergo a symmetry-breaking phase
transition at a finite temperature, but will it be in the same
universality class as the 3-state Potts *H*(*λ*=0) transition?

I’m leaning on the side that though the model explicitly breaks the
*S*<sub>3</sub> symmetry down to ℤ<sub>3</sub>, its phase transition
remains in the same universality class as the 3-state Potts model. From
conversations with friends, it seems like the thing to do would be to
somehow identify the *λ* term with an appropriate Potts CFT operator and
to check the dimension of that operator at the Potts CFT (i.e. check
whether or not it’s a relevant perturbation). I look forward to learning
whether and how one can make these identifications of lattice operators
with CFT operators.

Heuristic arguments for changing the universality class:

1.  The perturbation changes the symmetry of the model, and symmetries
    are part of what determines universality classes.

2.  It seems like there are other models that explicitly break an
    *S*<sub>*n*</sub> symmetry down to ℤ<sub>*n*</sub> – a quantum one
    of interest is the [chiral](https://arxiv.org/abs/1502.05049)
    [clock](https://arxiv.org/abs/1806.01867)
    [model](https://arxiv.org/pdf/1808.07056.pdf)
    *H* =  − ∑<sub>*i*</sub>*Z*<sub>*i*</sub><sup>†</sup>*Z*<sub>*i* + 1</sub>*e*<sup>*i**θ*</sup> − *h*∑<sub>*i*</sub>*X*<sub>*i*</sub>*e*<sup>*i**ϕ*</sup> + *h*.*c*.
    where *Z* and *X* are [Weyl-Heisenberg-Sylvester
    unitaries](https://en.wikipedia.org/wiki/Generalizations_of_Pauli_matrices#Sylvester's_generalized_Pauli_matrices_(non-Hermitian))
    generalizing the Pauli matrices to higher dimensions and satisfying
    *Z**X* = *ω**X**Z* where *ω* is an *n*-th principal root of unity.
    In the three-state case of interest, *ω* = *e*<sup>2*π**i*/3</sup>.
    When at least one of *θ* and *ϕ* are not equal to zero, it appears
    this ℤ<sub>3</sub> model undergoes phase transitions that are *not*
    in the 3-state Potts universality class. When both *θ* = *ϕ* = 0,
    the model indeed has *S*<sub>3</sub> symmetry and enjoys a
    transition in the 3-state Potts class.

Heuristic counterpoints:

1.  There are cases of irrelevant explicit-symmetry-breaking operators,
    so perhaps the model will regain its larger symmetry group in the IR
    at the critical point.

2.  The chiral clock models with *S*<sub>3</sub> explicitly broken down
    to *Z*<sub>3</sub> additionally explicitly break a number of other
    discrete symmetries. The chiral clock models with *θ* ≠ 0 are not
    symmetric under spatial inversion (reflection about a bond or a
    spin). The chiral clock models with *ϕ* ≠ 0 are not symmetric under
    complex conjugation. I suspect that in a classical model, the
    equivalent operations would be reflection about a column and
    reflection about a row respectively, so that my model above actually
    maintains more symmetries than these chiral models do (and hence
    might not be perturbed by the analogous relevant operators).

### Thoughts for proceeding

I could make a quick check of the properties of a quantum version of my
classical model above, such as by adding the same *λ* perturbation to
the ℤ<sub>3</sub> clock model (the clock model is really
*S*<sub>3</sub>-symmetric before the perturbation). I’d be tempted to
start with exact diagonalization (Lanczos for a few low-lying states)
and finding the critical point and *z* via finding where curves for
different *L* of the scaled gap *Δ**L*<sup>*z*</sup> against *h* cross.
I’d also be curious about the ground state entanglement entropy as a way
for extracting *c*. DMRG would also be useful to push to larger sizes.
DMRG may also be useful in probing the properties of the transfer matrix
of the classical model – a number of classical models have compact MPO
representations of their transfer matrices.

It may also be that the answer already lies in some of the
[chiral](https://arxiv.org/abs/1502.05049)
[clock](https://arxiv.org/abs/1806.01867)
[model](https://arxiv.org/pdf/1808.07056.pdf) papers above.
