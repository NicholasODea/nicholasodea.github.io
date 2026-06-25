# Two-slit interference: identical bosons

## First-quantized view: one boson vs. two bosons

I'll pose a question about the interference of identical particles, and sketch a solution. The question and solution are both elementary, but I like this problem as it emphasizes certain funny things about identical particles (when and whether identical particles can interfere, with a focus on single-body observables in this note). Special thanks to Samuel Alipour-fard and Danial Shadmany for enjoyable conversations about these topics. 

I'm considering a two-slit problem with a detecting screen, and to really emphasize the problem, I will take two disjoint canals behind the slits, and imagine initializing various states with various numbers of particles from within one or both of the canals. I find it easiest to first state the problem in first quantized language (indeed, in the position basis), before going to second quantized language (which is more natural for the solution). This is a little unfair on my part, as number-uncertain states will play a prominent role in the solution.

Let the single-particle wavefunctions at the left and right slits be $u_L(x), u_R(x)$.  Note that these states are orthogonal, as their supports are disjoint. (Note that we can even imagine the wavefunctions at an initial time before there is any support on the slits at all; these initial wavefunctions definitely have disjoint supports, as one starts entirely in the canal preceding the left slit and the other in the canal preceding the right slit.) We'll consider a closed system, and by unitarity, the orthogonality will persist under the time evolution, so that $u_L(x,t)$ and $u_R(x,t)$ remain orthogonal at all times. 

It is easiest to *not* think about the time that the particles arrive at the detecting screen, as different paths contributing to the path integral may reach the detector at a variety of times; let us imagine that the system can be well-approximated by these single particle states arriving at the detecting screen near some time $t_f$ with high probability. Furthermore, let's suppose that the detector "detects" by making a dot at the location a particle is detected, and that this detection occurs with probability density $n(x)=|\psi(x,t_f)|^2$ for a particle whose wavefunction is $\psi(x,t)$. 

More generally, for a many-body problem described by some wavefunction $\Psi$, the detector will see the density 
$n(x) = \sum_i \int d^dx_1...d^dx_{i-1}d^dx_{i+1}..d^dx_{N}|\Psi(x_1,...x_{i-1}, x, x_{i+1},...,x_N,t_f)|^2$.

To keep the notation marginally lighter, I'll call $u_L(x,t_f) = f_L(x)$ and $u_R(x,t_f) = f_R(x)$; as noted above $f_L(x)$ and $f_R(x)$ are orthogonal by virtue of unitarity and the orthogonality of $u_L(x)$ and $u_R(x)$.
## One boson

A single boson prepared in a coherent superposition of the two paths has
$$
\psi(x,t=0) = c_L u_L(x) + c_R u_R(x).
$$
The single-particle detection rate is (throughout, I'll use superscripts to denote the system we are considering)
$$
n^{(1)}(x)
=
|\psi(x,t_f)|^2
=
|c_L|^2 |f_L(x)|^2
+
|c_R|^2 |f_R(x)|^2
+
2\operatorname{Re}
\left[
c_L^* c_R f_L^*(x)f_R(x)
\right].
$$
Thus the one-particle interference term is
$$
n^{(1)}_{\mathrm{int}}(x)
=
2\operatorname{Re}
\left[
c_L^* c_R f_L^*(x)f_R(x)
\right].
$$
In comparison, a single particle in the incoherent mixture
$$
\rho_{x,x'}
=
|c_L|^2 u_L(x)u_L^*(x')
+
|c_R|^2 u_R(x)u_R^*(x')
$$
instead gives
$$
n^{(1,\,\rm inc)}(x)
=
|c_L|^2 |f_L(x)|^2
+
|c_R|^2 |f_R(x)|^2,
$$
with no interference term.
## Two identical bosons, one from each slit

Now consider two identical bosons, with one occupying the left slit mode and one occupying the right slit mode. The symmetrized first-quantized wavefunction is
$$
\Psi(x_1,x_2)
=
\frac{1}{\sqrt{2}}
\left[
f_L(x_1)f_R(x_2)
+
f_R(x_1)f_L(x_2)
\right].
$$
The one-particle density is (using symmetry to simplify slightly)
$$
n^{(2)}(x)
=
2\int dx_2\, |\Psi(x,x_2)|^2.
$$
The integral over $x_2$ is quite important. Crossterms that could lead to a $f_L^*(x) f_R(x)$ term are weighted by $\int dx_2\, f_R^*(x_2)f_L(x_2)$ which vanishes by orthogonality:
$$
\int dx'\, f_L^*(x')f_R(x') = 0,
$$
That is,
$$
n^{(2)}(x)
=
|f_L(x)|^2
+
|f_R(x)|^2.
$$
So the two-identical-boson state, one starting in the left canal and one starting in the right canal, has no ordinary one-body interference, as the detector is only sensitive to $n(x)$. 

This is very different from the coherent single particle case; another way of thinking about it is that the reduced density matrix for a single particle corresponds to the incoherent mixture with parameter values $|c_L|^2=|c_R|^2=1/2$.

This concept (roughly, that symmetric superpositions of products of orthogonal states have the same symmetrized-but-linear-in-single-particles observables as the unsymmetrized product of orthogonal states) is noted in Griffiths' undergraduate quantum textbook.

## Why it might feel a little strange

Identical particles can and do interfere with one another. 

They really have to: consider, for example, two spatially separated phase-locked monochromatic lasers. Treating the output beam of the lasers classically, the light shows an interference pattern where the laser beams overlap. 

More broadly, we expect spatially separated classical sources that have a well-defined phase to emit waves that can interfere with one another. 
 
If we imagine quantum sources that are spatially separated, then it seems a little odd at first blush that the seemingly analogous problem lacks any interference pattern (at least on our detector screen).

The simple resolution is just that the case of two particles is not analogous to the classical problem; the usual mantra is that bosonic *coherent states* are the right objects to compare to classical waves, and the above comparison with two particles is not quite apples to apples. I thank Samuel Alipour-fard for emphasizing this point to me in a conversation on the topic.

At first, it is also not obvious that introducing states with indefinite numbers of particles is quite the right thing to do. It is clearly necessary to have indefinite $(N_L,N_R)$; if we have a definite number $N_L$ bosons in $u_L(x)$ and a definite number $N_R$ bosons in $u_R(x)$, then there is still no interference because crossterms will again vanish. But is it obvious that an indefinite number of particles is sufficient?
## Detection density

Before proceeding, it's useful to rephrase things in a second quantized language, as coherent states made of states of differing numbers of particles are much more natural in this language. 

Write the mode annihilation operators $a_L,a_R$ and the annihilator
$$
\hat\psi(x,t)=u_L(x,t)a_L+u_R(x,t)a_R .
$$
The one-particle detection rate is
$$
n(x)=\langle \hat\psi^\dagger(x,t_f)\hat\psi(x,t_f)\rangle
$$
so
$$
n(x)
=|f_L(x)|^2\langle N_L\rangle+|f_R(x)|^2\langle N_R\rangle
+2\operatorname{Re}(f_L^*(x)f_R(x)\langle a_L^\dagger a_R\rangle).
$$
This is a nice form that works for all sorts of superpositions of Fock states, and it shows that relatively little information about the initial state is needed to characterize the interference pattern. In particular, only the occupation expectation values and the cross term $\langle a^\dagger_L a_R\rangle$ are needed to characterize the interference pattern.
## Single particle revisited

In this language, it's easy to see that neither $N_L$ nor $N_R$ have definite values. The initial state is
$$
|\psi_1\rangle=\left(c_L a_L^\dagger+c_R a_R^\dagger\right)|0\rangle .
$$
with 
$$
\langle N_L\rangle=|c_L|^2\quad \langle N_R\rangle=|c_R|^2,
\qquad
\langle a_L^\dagger a_R\rangle=c_L^*c_R.
$$
Therefore
$$
n^{(1)}(x)
=|c_L|^2|f_L(x)|^2+|c_R|^2|f_R(x)|^2
+2\operatorname{Re}(c_L^*c_R f_L^*(x)f_R(x)).
$$
which thankfully agrees with the single-quantized example.
## Two identical bosons, one in each slit mode

State:
$$
|\psi_2\rangle=|1_L,1_R\rangle=a_L^\dagger a_R^\dagger|0\rangle .
$$
Occupancies and coherence:
$$
\langle n_L\rangle=\langle n_R\rangle=1,
\qquad
\langle a_L^\dagger a_R\rangle=0
$$
Therefore
$$
n^{(2)}(x)=|f_L(x)|^2+|f_R(x)|^2 .
$$
## Pair of coherent states

State:
$$
|\alpha_L\rangle_L|\alpha_R\rangle_R,
\qquad
 a_L|\alpha_L\rangle=\alpha_L|\alpha_L\rangle,
\qquad
 a_R|\alpha_R\rangle=\alpha_R|\alpha_R\rangle .
$$
Occupancies and coherence:
$$
\langle n_L\rangle=|\alpha_L|^2,
\qquad
\langle n_R\rangle=|\alpha_R|^2,
\qquad
\langle a_L^\dagger a_R\rangle=\alpha_L^*\alpha_R.
$$
Therefore
$$
n^{(\alpha)}(x)
=|\alpha_L|^2|f_L(x)|^2+|\alpha_R|^2|f_R(x)|^2
+2\operatorname{Re}(\alpha_L^*\alpha_R f_L^*(x)f_R(x)).
$$
Thus, with $\alpha_L=c_L$ and $\alpha_R = c_R$, we perfectly reproduce the interference pattern seen in the case of a single particle that started in a superposition of the canal states! It is also nice to note that we can increase the brightness of our coherent-state bulbs by taking $\alpha_L = \lambda c_L$ and $\alpha_R = \lambda c_R$ for some large factor $\lambda$ without changing the interference pattern. 

Roughly, I like to imagine this as that we have two spatially separated sources that separately produce coherent states of the same kind of boson, and the fact that we have a system of identical bosons means that these coherent states can interfere. More prosaically, these quantum sources replicate the behavior (at least through single-body observables) of phase-locked monochromatic classical sources. 
