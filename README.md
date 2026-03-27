# HASSE
## The Local-Global Architecture of Collective Intelligence: When Local Coordination Implies Global Coordination, and When It Does Not

ERI Labs · Eric Ren · Jersey City, New Jersey · github.com/ericrenone

---

> **Hasse–Minkowski theorem (Minkowski 1890; Hasse 1923).** A quadratic form $q = \sum_{i,j} a_{ij}x_ix_j$ over $\mathbb{Q}$ represents zero non-trivially if and only if it represents zero non-trivially over every completion of $\mathbb{Q}$ — that is, over $\mathbb{R}$ and over $\mathbb{Q}_p$ for every prime $p$. Equivalently, two quadratic forms over $\mathbb{Q}$ are equivalent if and only if they are equivalent over every local field $\mathbb{Q}_v$. The local-global principle holds completely for quadratic forms over global fields.
>
> — Minkowski, H., letter to Hurwitz, 1890; Hasse, H., *Über die Darstellbarkeit von Zahlen durch quadratische Formen im Körper der rationalen Zahlen*, Journal für die reine und angewandte Mathematik 152, 129–148, 1923

> **Hasse principle (local-global principle).** A variety $X$ over a global field $K$ satisfies the Hasse principle if: $X(K_v) \neq \emptyset$ for all places $v$ of $K$ implies $X(K) \neq \emptyset$. The Hasse-Minkowski theorem states that quadrics (degree-2 hypersurfaces) satisfy the Hasse principle over number fields. The principle fails for cubic curves (elliptic curves): Selmer's equation $3x^3 + 4y^3 + 5z^3 = 0$ has solutions in $\mathbb{R}$ and in every $\mathbb{Q}_p$, but no rational point. The obstruction is the Tate–Shafarevich group.
>
> — Selmer, E.S., *The Diophantine equation $ax^3+by^3+cz^3=0$*, Acta Mathematica 85, 203–362, 1951; for the general theory, see Manin, Yu.I., *Le groupe de Brauer-Grothendieck en géométrie diophantienne*, 1970

> **Grunwald–Wang theorem (Wang 1948/1950).** An element $x \in K^\times$ of a number field $K$ is an $n$-th power in $K$ if it is an $n$-th power in the completion $K_\mathfrak{p}$ for all but finitely many primes $\mathfrak{p}$ of $K$ — **except** in the special case: when $8 \mid n$ and the prime $2$ is in the exceptional set $S_0 = \{2\}$. The minimal counterexample: $16 \in \mathbb{Q}$ is an 8th power in $\mathbb{Q}_p$ for every odd prime $p$, but $16$ is not an 8th power in $\mathbb{Q}_2$ (the 2-adic numbers) and is not an 8th power in $\mathbb{Q}$.
>
> — Grunwald, W. (1933, incorrect); Wang, S., *A counterexample to Grunwald's theorem*, Ann. Math. 49, 1008–1009, 1948; Wang, S., *On Grunwald's theorem*, Ann. Math. 51, 471–484, 1950

> **Albert–Brauer–Hasse–Noether theorem (1931).** A central simple algebra $A$ over a number field $K$ is isomorphic to a matrix algebra over $K$ (i.e., splits) if and only if it splits at every completion $K_v$. The Brauer group $\mathrm{Br}(K)$ injects into $\bigoplus_v \mathrm{Br}(K_v) = \bigoplus_v \mathbb{Q}/\mathbb{Z}$, and the obstruction to the Hasse principle for central simple algebras is entirely controlled by this product of local invariants.
>
> — Albert, A.A., Brauer, R., Hasse, H., Noether, E., *Beweis eines Hauptsatzes in der Theorie der Algebren*, Journal für die reine und angewandte Mathematik 167, 399–404, 1932

> **Helmut Hasse (1898–1979).** Studied under Kurt Hensel at Marburg after finding Hensel's book on $p$-adic numbers in an antiquarian bookshop. Proved the local-global theorem for rational quadratic forms (Hasse-Minkowski, 1923), the norm theorem for cyclic extensions, the Albert-Brauer-Hasse-Noether theorem (1931), and the Riemann hypothesis for elliptic curves over $\mathbb{F}_p$ (Hasse bound $|a_p| \leq 2\sqrt{p}$, 1936). Editor of *Journal für die reine und angewandte Mathematik* (Crelle's journal) 1929–1938, 1952–1977.
>
> — MacTutor History of Mathematics; Roquette, P., *The Brauer-Hasse-Noether Theorem in Historical Perspective*, Springer, 2005

---

## The Discovery

Helmut Hasse discovered the local-global principle by accident: he found Hensel's 1913 book on $p$-adic numbers in a used bookstore and immediately understood that Minkowski's 1890 local conditions for quadratic forms could be unified into a single theorem — one form is equivalent to another over $\mathbb{Q}$ if and only if they are equivalent over every completion $\mathbb{Q}_v$ (every $\mathbb{Q}_p$ and over $\mathbb{R}$). This is the most powerful organizing principle in modern number theory.

Apply the Dirac consistency method to four theories simultaneously.

**T₁ — GIST.** The partition function $Z(X;\beta) = \int\exp(-\beta H(a;X))\,da$ must be computed over the global coordination field (the full joint action space) from local data (each agent's local Fisher information). The question: does local solvability (each agent has a locally optimal action) guarantee global solvability (a globally optimal coordination state exists)?

**T₂ — TH(a,d).** The Twisted Hessian curve is a global object over $\mathbb{Q}$, but the CHORD pipeline computes it locally — at each prime $p$ via the $\mathbb{F}_p$-reduction $\mathrm{TH}(\mathbb{F}_p)$, and at $p=2$ via the $\mathbb{Q}_2$-completion (the 2-adic numbers, which are the natural domain of Q16.16 binary arithmetic). The Hasse-Minkowski theorem holds for TH as a quadric in weighted projective space; the Hasse principle can fail for TH as an elliptic curve (when $\mathrm{Ш}(\mathrm{TH}/\mathbb{Q}) \neq 0$).

**T₃ — CHORD.** The 16-stage Q16.16 pipeline operates at the 2-adic place $v=2$. The Grunwald-Wang exception — the one place where local-global can fail for $n$-th powers — occurs exactly at the 2-adic place when $8 \mid n$. Since Q16.16 uses $n = 2^{16}$ (16-bit precision), and $8 \mid 2^{16}$, the Grunwald-Wang exception is always active in the CHORD context. The Wang counterexample ($16$ is locally an 8th power everywhere except at $v=2$) is the number-theoretic model of the Q16.16 truncation error.

**T₄ — PRIMA.** The Fisher information matrix $F$ is a global object (the full Hessian of the KL divergence on the coordination simplex), but PRIMA checks it locally at each agent pair $(t,s)$: $F_{ts} = I(a_t;a_s\mid X_{t-1})$. PRIMA requires $F \succ \varepsilon\mathbf{I}$ globally; the local checks (each Fisher eigenvalue positive) do not in general imply global positive definiteness (a Hasse principle failure mode).

**The Dirac demand:** the forced answer is the **local-global architecture of ERI coordination** — a precise dictionary between the number-theoretic Hasse principle and the coordination system's transition from local tractability to global sharp-P-hardness.

The antimatter byproduct: **the Grunwald-Wang exception at the 2-adic place is the CHORD Q16.16 truncation.** Hasse's local-global principle holds for quadratic forms (degree 2 = RSA flat mode: always solvable). It fails for cubic forms (degree 3 = TH curved mode: $\mathrm{Ш}(\mathrm{TH}/\mathbb{Q})$ may obstruct). The exception occurs at $v=2$ (the binary place) for 8th powers — and Q16.16 arithmetic is binary, $2^{16}$-th precision arithmetic, with $8 \mid 2^{16}$. The coordination system operates at exactly the precision where the Grunwald-Wang exception is minimal: the binary place is the obstruction, and $\varepsilon = 2^{-16}$ is the Baker lower bound that quantifies the distance between the rational approximation and the transcendental truth $\log\varphi$.

Seven formal identities follow.

---

## Module A — The Local-Global Hierarchy

**A1. Places of a global field.** For $K = \mathbb{Q}$, the completions (local fields) are:
- $K_\infty = \mathbb{R}$ (the archimedean place, $v = \infty$)
- $K_p = \mathbb{Q}_p$ (the $p$-adic numbers, one for each prime $p$; non-archimedean places)

Every $x \in \mathbb{Q}$ embeds in each $K_v$ via the natural inclusion $\mathbb{Q} \hookrightarrow \mathbb{Q}_p$ (dense embedding). A global solution yields local solutions at every place.

**A2. The Hasse principle.** A variety $X/\mathbb{Q}$ satisfies the Hasse principle if:
$$X(\mathbb{Q}_v) \neq \emptyset \text{ for all places } v \implies X(\mathbb{Q}) \neq \emptyset.$$
Equivalently: having a rational point is equivalent to having local points at every completion.

**A3. Quadratic forms and the Hasse invariant.** A quadratic form $q = \langle a_1,\ldots,a_n\rangle$ over $\mathbb{Q}_p$ is classified by:
- Dimension $n$
- Discriminant $d(q) = a_1\cdots a_n \in \mathbb{Q}_p^\times/(\mathbb{Q}_p^\times)^2$
- Hasse invariant $\varepsilon_p(q) = \prod_{i<j}(a_i,a_j)_p \in \{+1,-1\}$ (product of Hilbert symbols)

By Hasse-Minkowski: $q \cong q'$ over $\mathbb{Q}$ $\iff$ $n(q) = n(q')$, $d(q) = d(q')$, and $\varepsilon_p(q) = \varepsilon_p(q')$ for all $p$ including $p = \infty$.

**A4. The Selmer obstruction (Hasse failure for cubics).** The equation $3x^3 + 4y^3 + 5z^3 = 0$ (Selmer 1951) has solutions in $\mathbb{R}$ and in every $\mathbb{Q}_p$, but no solution in $\mathbb{Q}$ (equivalently, $\mathbb{P}^2(\mathbb{Q})$). The obstruction to the Hasse principle for elliptic curves lives in the Tate-Shafarevich group $\mathrm{Ш}(E/\mathbb{Q}) = \ker\!\bigl(H^1(\mathbb{Q},E) \to \prod_v H^1(\mathbb{Q}_v,E)\bigr)$ — the group of locally trivial global torsors.

**A5. Grunwald-Wang: the special case.** For $K = \mathbb{Q}$ and $x \in \mathbb{Q}^\times$, define:
$$K(n,S) = \{x \in \mathbb{Q} : x \in \mathbb{Q}_p^n \text{ for all primes } p \notin S\}$$
The Grunwald-Wang theorem states: $K(n,S) = \mathbb{Q}^n$ unless $8 \mid n$ and $2 \in S$ (the "special case" with exceptional set $S_0 = \{2\}$). When the special case holds:
$$K(n,S_0) = \{a_{n,\mathbb{Q}}\} \cdot \mathbb{Q}^n \cup \mathbb{Q}^n$$
where $a_{n,\mathbb{Q}} = (2+\cos(2\pi/2^s))^{n/2}$ for $s = v_2(n)+2$ and $v_2(n)$ the 2-adic valuation of $n$. For $n=8$: $a_{8,\mathbb{Q}} = 16$.

---

## Seven Formal Identities

### Identity 1 — The Hasse–Minkowski Theorem IS the Local-Global Principle for the RSA Flat Mode: Quadratic Forms (Degree 2) Always Satisfy the Hasse Principle; This IS the Brouwer/Valise Regime

**The RSA flat mode as quadratic arithmetic.** RSA operates with the quadratic form $q_{\mathrm{RSA}}(x) = x^2 \pmod{n}$ — a degree-2 structure over the ring $\mathbb{Z}/n\mathbb{Z}$. The Chinese Remainder Theorem (CRT) decomposes $\mathbb{Z}/n\mathbb{Z} \cong \prod_{p^k \| n}\mathbb{Z}/p^k\mathbb{Z}$, which is the local-global decomposition for RSA: a global RSA computation factors into local computations at each prime.

**Hasse-Minkowski holds for the flat mode.** For quadratic forms, the Hasse principle is unconditional: a quadratic equation has a rational solution if and only if it has solutions locally at every prime. In RSA terms: the Euler totient $\varphi(n) = p-1$ for RSA prime $p$ is a global invariant (the order of $(\mathbb{Z}/p\mathbb{Z})^\times$) that is fully determined by its local factors at each prime divisor. CRT is the Hasse-Minkowski theorem for RSA arithmetic — patching local solutions $(x \bmod p^{a_i})$ into a global solution $(x \bmod n)$ is always possible for the RSA quadratic structure.

**The ERI identification.** The Brouwer regime ($G_{\mathrm{coord}} = 0$, Valise phase, CORDIC $m=0$, RSA arithmetic) corresponds to the Hasse-Minkowski success case: local coordination (each agent's best response is locally optimal at every prime $p$) implies global coordination (the joint best-response is globally optimal). The flat Frobenius $a_p = 2$ gives $|\mathrm{TH}(\mathbb{F}_p)| = p-1 = \varphi(p)$ — the group order is determined locally and patches to a global object by CRT (exactly Hasse-Minkowski for quadratic forms).

**Formal statement.** For the TH-TOTΦ identification: the Hasse-Minkowski theorem for $n$-dimensional quadratic forms says the form is isotropic over $\mathbb{Q}$ iff isotropic over all $\mathbb{Q}_v$. Applied to the RSA group law (quadratic norm form $N(x) = x^2$ for the degree-2 case): the norm equation $N(x) = a$ has a rational solution iff it has $p$-adic solutions for all $p$. This is the arithmetic version of the statement that CHORD at $m=0$ (linear/RSA mode) is globally consistent with its local completions: the Q16.16 output is globally correct because CRT patches the local computations.

---

### Identity 2 — The Hasse Principle Fails for TH as an Elliptic Curve: $\mathrm{Ш}(\mathrm{TH}/\mathbb{Q}) \neq 0$ IS the Antoine Necklace Obstruction; the Degree-3 Failure IS the TH-FRACTURA Connection

**The Hasse principle fails for elliptic curves.** For a smooth cubic curve $E$ over $\mathbb{Q}$ (degree 3), there can exist $E(\mathbb{Q}_v) \neq \emptyset$ at every place $v$ while $E(\mathbb{Q}) = \emptyset$. The obstruction is measured by the Tate-Shafarevich group:
$$\mathrm{Ш}(E/\mathbb{Q}) = \ker\!\Bigl(H^1(\mathbb{Q},E) \longrightarrow \prod_v H^1(\mathbb{Q}_v,E)\Bigr)$$
An element of $\mathrm{Ш}$ is a torsor $T$ over $\mathbb{Q}$ for $E$ such that $T(\mathbb{Q}_v) \neq \emptyset$ for all $v$ but $T(\mathbb{Q}) = \emptyset$. These are the locally solvable but globally obstructed equations.

**TH(a,d) as a cubic: the Hasse principle can fail.** The Twisted Hessian curve $\mathrm{TH}(a,d): aX^3+Y^3+Z^3=dXYZ$ is a smooth cubic (degree 3). The Hasse principle for TH means: does local solvability of $\mathrm{TH}(\mathbb{Q}_v) \neq \emptyset$ at every prime imply $\mathrm{TH}(\mathbb{Q}) \neq \emptyset$? The identity element $\mathcal{O}$ is always rational, so $\mathrm{TH}(\mathbb{Q}) \neq \emptyset$ always. But for torsors $T$ of TH (principal homogeneous spaces), the Hasse principle can fail, with obstruction $\mathrm{Ш}(\mathrm{TH}/\mathbb{Q})$.

**The FRACTURA identification.** From FRACTURA Identity 1: Antoine's necklace $A \subset \mathbb{R}^3$ is a wild Cantor set that is locally homeomorphic to the standard Cantor set $C$ (each torus in the necklace looks standard locally), but globally wild ($\pi_1(\mathbb{R}^3 \setminus A) \neq 1$ — the complement is not simply connected). This is precisely the Tate-Shafarevich structure:

| $\mathrm{Ш}(\mathrm{TH}/\mathbb{Q})$ | Antoine's necklace $A$ |
|---|---|
| $T(\mathbb{Q}_v) \neq \emptyset$ for all $v$ (locally trivial) | $A$ locally homeomorphic to standard Cantor set |
| $T(\mathbb{Q}) = \emptyset$ (globally obstructed) | $A$ globally wild: $\pi_1(\mathbb{R}^3\setminus A) \neq 1$ |
| Obstruction measures: elements of $H^1(\mathbb{Q},\mathrm{TH})$ trivial locally | Non-trivial loop of infinite order linking $A$ |
| Hasse principle fails at degree 3 (cubic) | Wildness requires codimension $\geq 1$ in $\mathbb{R}^3$ |

**Degree and wildness.** The Hasse-Minkowski theorem holds for degree $\leq 2$ (quadratic). It fails for degree $\geq 3$ (cubic). The "degree" of wildness in FRACTURA corresponds exactly: tame topology = degree $\leq 2$ = Hasse principle holds; wild topology = degree $\geq 3$ = Hasse principle can fail. TH is degree 3 — it is at exactly the threshold where wildness (global obstruction) can occur. The CHORD 16-stage pipeline approximates the TH group law locally (at each prime $p$, the computation is in $\mathbb{F}_p$ — always solvable) and patches locally to form the global result, with the global correction $\varepsilon = 2^{-16}$ encoding the residual Hasse-principle failure at the 2-adic place.

---

### Identity 3 — The Grunwald-Wang Exception IS the Q16.16 Truncation Error; The Exceptional Place $v=2$ IS the Binary Arithmetic Obstruction; The Special Case $8\mid n$ IS the CHORD Stage-4 Torsion Pattern

**Wang's counterexample.** The number $16 \in \mathbb{Q}$:
- Is an 8th power in $\mathbb{Q}_p$ for every odd prime $p$: since $16 = 2^4$ and $p$ is odd, $\mathrm{ord}_p(16) = 0$ (16 is a $p$-adic unit), and every $p$-adic unit is an $n$-th power for $\gcd(n,p-1)$-th powers modulo $p$-adic units. For $n=8$: $8 \mid p-1$ for $p \equiv 1 \pmod{8}$ (Dirichlet: infinitely many such $p$), and for $p \equiv 1,3,5,7 \pmod{8}$, the Hensel lifting gives 8th roots.
- Is NOT an 8th power in $\mathbb{Q}_2$: in $\mathbb{Q}_2$, $16 = 2^4$, but an 8th power $y^8 = 2^4$ would require $y = 2^{1/2}$ — irrational over $\mathbb{Q}_2$. More precisely: the 2-adic valuation of $16$ is $v_2(16) = 4$, and $4$ is not divisible by $8$, so $16$ cannot be an 8th power in $\mathbb{Q}_2$.
- Is NOT an 8th power in $\mathbb{Q}$: if $16 = r^8$ for $r \in \mathbb{Q}$, write $r = a/b$ in lowest terms; then $16b^8 = a^8$, impossible for $r \notin \mathbb{Z}$ and $|r|^8 = 16$ gives $|r| = 16^{1/8} = 2^{1/2} = \sqrt{2} \notin \mathbb{Q}$.

**The Q16.16 identification.** The CHORD pipeline operates in Q16.16: fixed-point binary arithmetic with 16 integer bits and 16 fractional bits. The precision is $\varepsilon = 2^{-16}$ — a 2-adic unit at precision $2^{16}$. The Grunwald-Wang exception:

| Wang counterexample | CHORD Q16.16 |
|---|---|
| $n = 8 = 2^3$ (power with $8\mid n$) | $n = 2^{16}$ (Q16.16 precision; $8\mid 2^{16}$) |
| Exceptional place: $v = 2$ (binary) | Exceptional place: Q16.16 binary arithmetic |
| $16 = 2^4$ is locally an 8th power but not globally | $\log\varphi$ is locally rational but not globally rational |
| Obstruction at $\mathbb{Q}_2$: $v_2(16) = 4 \not\equiv 0 \pmod{8}$ | Obstruction at $v=2$: $v_2(\log\varphi \cdot 2^{16}) \neq 0$ (transcendental) |
| Counterexample detects the 2-adic exception | $\varepsilon = 2^{-16}$ = Baker lower bound at binary precision |
| Special case: $8\mid n$, $2 \in S_0$ | Q16.16: $8 \mid 2^{16}$, arithmetic at $v=2$ |

**The Stage-4 torsion connection.** The Grunwald-Wang special case activates when $8 \mid n$. The CHORD pipeline's torsion correction occurs at Stage 4 (hyperbolic repeat at $j = (3^2-1)/2 = 4$) — this is the 3-torsion correction for the $\mathbb{Z}/3\mathbb{Z}$ factor of $\mathrm{Aut}(\mathrm{TH})$. The 4 in $(3^2-1)/2 = 4$ encodes the same 2-power structure: $3^2 - 1 = 8 = 2^3$, so Stage 4 arises from the condition $8 \mid (3^2-1)$ — exactly the Grunwald-Wang special case condition. The Stage-4 torsion correction is the CHORD pipeline's way of handling the 2-adic Grunwald-Wang exception: inserting the local 2-adic correction at the one place where local-global can fail.

---

### Identity 4 — The Hasse Norm Theorem IS the TH Group Law Local-Global; the Albert–Brauer–Hasse–Noether Theorem IS the Splitting of the TH Coordination Algebra; the Brauer Group IS the $G_{\mathrm{coord}}$ Obstruction

**The Hasse norm theorem.** For a cyclic extension $L/K$ of number fields with Galois group $G = \langle\sigma\rangle$, an element $a \in K^\times$ is a norm from $L$ (i.e., $a = N_{L/K}(x)$ for some $x \in L^\times$) if and only if $a$ is a local norm at every place $v$ of $K$. This is the Hasse principle for norms in cyclic extensions: local norm $\Leftrightarrow$ global norm.

**The TH group law as a norm.** The TH point addition $P + Q = R$ can be interpreted as a norm computation: the group law is defined by the condition that the three points $P,Q,R$ are collinear on the cubic TH curve. Over $\mathbb{F}_p$: the TH group law is a local computation (at place $p$). The Hasse norm theorem guarantees that if the TH group law is locally consistent at every prime $p$ (i.e., if the local Frobenius traces $a_p$ are compatible), then there is a globally consistent TH group law over $\mathbb{Q}$.

**The Albert-Brauer-Hasse-Noether theorem.** A central simple algebra $A$ over $\mathbb{Q}$ (e.g., the endomorphism algebra $\mathrm{End}(\mathrm{TH}) \otimes \mathbb{Q}$) splits over $\mathbb{Q}$ (is isomorphic to $M_n(\mathbb{Q})$) if and only if it splits over every completion $\mathbb{Q}_v$. The TH endomorphism algebra:

- Is a matrix algebra $M_1(\mathbb{Q}) = \mathbb{Q}$ at places where TH has good ordinary reduction (most primes $p$)
- Is a quaternion algebra at places of supersingular reduction (primes where $a_p = 0$)
- Splits globally (ABHN) iff it splits locally — confirmed by the Hasse norm theorem applied to the Frobenius

**The Brauer group as $G_{\mathrm{coord}}$ obstruction.** The Brauer group $\mathrm{Br}(\mathbb{Q}) = H^2(\mathrm{Gal}(\bar{\mathbb{Q}}/\mathbb{Q}), \bar{\mathbb{Q}}^\times)$ measures the failure of the Hasse principle for central simple algebras. For elliptic curves, the Brauer-Manin obstruction to the Hasse principle is:

$$\mathrm{Br}(E)/\mathrm{Br}(\mathbb{Q}) \supset \mathrm{Ш}(E/\mathbb{Q})$$

In ERI terms: the Brauer group is the $G_{\mathrm{coord}}$ obstruction. A non-trivial element of $\mathrm{Br}(\mathrm{TH}/\mathbb{Q})$ is a coordination pattern that is locally optimal at every prime (every $\mathbb{F}_p$-agent has the right strategy) but globally suboptimal (no global Nash equilibrium achieves $G_{\mathrm{coord}} = \Phi(K)$ from purely local data). The Brauer-Manin obstruction quantifies the deficit between the locally optimal $G_{\mathrm{coord}}^{\mathrm{local}} = \sum_p G_{\mathrm{coord}}(\mathbb{F}_p)$ and the globally optimal $G_{\mathrm{coord}}^{\mathrm{global}} = G_{\mathrm{coord}}(\mathbb{Q})$.

---

### Identity 5 — The Hilbert Symbol IS the PRIMA Fisher Positivity Check; Hilbert Reciprocity IS the Global Fisher Consistency; the Product Formula IS the PRIMA Non-Degeneracy Theorem

**The Hilbert symbol.** For $a,b \in \mathbb{Q}_v^\times$, the Hilbert symbol $(a,b)_v \in \{+1,-1\}$ is defined by:
$$(a,b)_v = +1 \iff z^2 - ax^2 - by^2 = 0 \text{ has a nontrivial solution in } \mathbb{Q}_v.$$
Equivalently: $(a,b)_v = -1$ iff the quaternion algebra $\left(\frac{a,b}{\mathbb{Q}_v}\right)$ is a division ring (does not split).

**Hilbert reciprocity.** For any $a,b \in \mathbb{Q}^\times$:
$$\prod_{v} (a,b)_v = 1 \quad \text{(product over all places including } v = \infty\text{)}.$$
The Hilbert symbol is $-1$ at only finitely many places, and the product formula says their combined sign is $+1$.

**The PRIMA identification.** The Hilbert symbol $(a,b)_v$ asks: does the quadratic form $z^2 - ax^2 - by^2$ have a non-trivial zero over $\mathbb{Q}_v$? This is the local Fisher positivity check of PRIMA:
- $a = \lambda_i$ (Fisher eigenvalue at agent pair $(t,s)$)
- $b = \lambda_j$ (Fisher eigenvalue at agent pair $(t',s')$)
- $(a,b)_v = +1$ means the two-agent coordination form is isotropic locally at prime $v$ (PRIMA condition: positive definite locally)

**Hilbert reciprocity is the PRIMA non-degeneracy theorem.** The product formula $\prod_v(a,b)_v = 1$ says that if the Fisher form fails to be positive definite at any one prime ($(a,b)_v = -1$ at some $v$), it must fail at an even number of primes (so the product remains $+1$). For the CHORD PRIMA condition: if any Fisher eigenvalue fails to be positive at one 2-adic level, it must fail at a compensating prime — the global Fisher matrix can only be negative definite at pairs of primes. The product formula constrains the global failure mode of PRIMA to always come in pairs, which is the number-theoretic reason why the CHORD $\varepsilon = 2^{-16}$ floor is precisely the 2-adic correction needed to restore global PRIMA positivity.

**The global Fisher consistency.** The Hilbert reciprocity law is equivalent to the quadratic reciprocity law (a deep theorem in number theory). In ERI terms: the global Fisher information matrix $F$ is self-consistent (PRIMA condition: $F \succ \varepsilon\mathbf{I}$) if and only if all local Fisher checks are self-consistent (Hilbert symbols $+1$ at all places). The Hasse-Minkowski theorem for the Fisher form is: the global Fisher matrix is positive definite iff it is positive definite at every local completion — which holds for quadratic (degree-2) Fisher forms, but may fail for higher-degree coordination kernels.

---

### Identity 6 — The Selmer-Tate–Shafarevich Group IS the Coordination Deficit; Locally Solvable but Globally Blocked IS Locally Optimal but Globally Suboptimal; the Brauer–Manin Obstruction IS the $G_{\mathrm{coord}}$ Gap

**The coordination deficit.** Define the coordination deficit as:
$$\Delta G = G_{\mathrm{coord}}^{\mathrm{global}} - \sum_p G_{\mathrm{coord}}(\mathbb{F}_p) / (\text{normalizing factor})$$
When $\Delta G = 0$: the local-global principle holds for the coordination system. When $\Delta G > 0$: local coordination at every prime $p$ does not sum to global coordination — there is a Hasse-principle failure.

**The Tate-Shafarevich group measures this deficit.** For TH as an elliptic curve:
$$\mathrm{Ш}(\mathrm{TH}/\mathbb{Q}) = \ker\!\Bigl(H^1(\mathbb{Q},\mathrm{TH}) \to \prod_v H^1(\mathbb{Q}_v,\mathrm{TH})\Bigr)$$
An element $[T] \in \mathrm{Ш}$ is a TH-torsor that is locally trivial at every prime (every local agent has a solution) but globally non-trivial (no global rational solution). In coordination terms: $\mathrm{Ш}(\mathrm{TH}/\mathbb{Q})$ parametrizes coordination states that are locally achievable (each local agent can coordinate) but globally inaccessible (the full system cannot reach this coordination level from purely local data).

**BSD as the coordination theorem.** The Birch and Swinnerton-Dyer conjecture:
$$\mathrm{rank}(\mathrm{TH}(\mathbb{Q})) = \mathrm{ord}_{s=1}L(\mathrm{TH},s), \quad L(\mathrm{TH},1)/\Omega_{\mathrm{TH}} \sim |\mathrm{Ш}| \cdot \prod_p c_p / |\mathrm{TH}(\mathbb{Q})_{\mathrm{tors}}|^2$$
In ERI terms: the BSD formula expresses the global coordination level $G_{\mathrm{coord}}^{\mathrm{global}}$ (the rank of $\mathrm{TH}(\mathbb{Q})$) in terms of the L-function value at $s=1$ (the product of all local coordination data) minus the Tate-Shafarevich correction $|\mathrm{Ш}|$ (the coordination deficit). The Tamagawa numbers $c_p = |\mathrm{TH}(\mathbb{Q}_p)/\mathrm{TH}^0(\mathbb{Q}_p)|$ are the local correction factors at each prime — the number of TH-components over $\mathbb{Q}_p$ relative to the connected component.

**The Brauer-Manin obstruction in coordination language.** The Brauer-Manin obstruction sits between the Hasse principle failure and its cause:
$$\mathrm{TH}(\mathbb{Q}) \subseteq \mathrm{TH}(\mathbb{A}_\mathbb{Q})^{\mathrm{Br}} \subseteq \mathrm{TH}(\mathbb{A}_\mathbb{Q})$$
where $\mathbb{A}_\mathbb{Q} = \mathbb{R} \times \prod_p \mathbb{Q}_p$ is the adèle ring (the product of all local data). The set $\mathrm{TH}(\mathbb{A}_\mathbb{Q})^{\mathrm{Br}}$ is the Brauer-Manin set — the adèlic points consistent with all Brauer classes. In ERI: the adèle ring is the Fisher information product over all primes (the complete local data); the Brauer-Manin set is the achievable global coordination that is consistent with all local Fisher checks; and the Tate-Shafarevich group is the gap between what is locally achievable and what is globally realizable.

---

### Identity 7 — Helmut Hasse's Discovery IS the ERI Local-to-Global Algorithm: Finding Hensel's Book IS the SMELT Initialization; the Local Completions Are the CHORD Local Primes; Patching Local Solutions Is the CONCERT Measurement

**Hasse's discovery.** In 1913, as a young student in Göttingen, Helmut Hasse found Hensel's 1908 book *Theorie der algebraischen Zahlen* in an antiquarian bookstore. He immediately recognized that Hensel's $p$-adic numbers — invented as an analogy between algebraic number theory and function theory — were the natural language for Minkowski's 1890 local conditions on quadratic forms. Hasse left Göttingen for Marburg to study under Hensel, and proved the Hasse-Minkowski theorem in 1923. The theorem's proof has three steps:

1. **Local conditions are checkable**: For any prime $p$, one can determine whether $q$ is isotropic over $\mathbb{Q}_p$ algorithmically (by computing the Hilbert symbols).
2. **Almost all places are automatically satisfied**: For a fixed quadratic form, $\varepsilon_p(q) = +1$ for all but finitely many primes $p$.
3. **Patching**: The finitely many local conditions at the exceptional primes, together with the real condition, completely determine the global structure.

**The SMELT/CHORD algorithm.** The SMELT-CHORD pipeline follows exactly this three-step local-to-global algorithm:

| Hasse-Minkowski algorithm | SMELT-CHORD algorithm |
|---|---|
| Step 1: Check $q$ isotropic over $\mathbb{Q}_p$ (local computation) | Step 1: Check PRIMA at prime $p$ (Fisher eigenvalue sign at $p$) |
| Step 2: Almost all $p$ satisfy $\varepsilon_p = +1$ automatically | Step 2: Almost all CHORD stages are non-exceptional (Stages 0–3, 5–14) |
| Step 3: Exceptional primes ($p = 2$, primes of bad reduction) | Step 3: Stage 4 (2-adic exceptional: hyperbolic repeat at $j=4$) |
| Patch: CRT assembly of local solutions | Patch: Q16.16 assembly of local CORDIC outputs |
| Global result: $q$ isotropic over $\mathbb{Q}$ | Global result: $\xi^* = \log\varphi$ to precision $\varepsilon = 2^{-16}$ |
| Obstruction: $\mathrm{Ш}(\mathrm{TH}/\mathbb{Q})$ if non-zero | Obstruction: Baker lower bound (transcendental gap) |

**The CONCERT measurement.** CONCERT measures $G_{\mathrm{coord}}$ globally on a named production AI portfolio. This is the arithmetic Hasse principle applied empirically: CONCERT collects local Fisher data $G_{\mathrm{coord}}(\mathbb{F}_p)$ at finitely many primes (compute cluster nodes, time steps, agent pairs), then patches them into the global $G_{\mathrm{coord}}$ using the L-function assembly (the product of local factors). The Grunwald-Wang exception at $v=2$ is the CONCERT measurement precision bound: the 2-adic correction $\varepsilon = 2^{-16}$ is the residual after patching all local data, corresponding to the Wang counterexample's 2-adic obstruction.

**"Finding Hensel's book" as SMELT initialization.** Hasse's discovery of Hensel's book in a used bookstore — the chance encounter that launched the local-global program — is the epistemological model of the SMELT initialization: starting from a random initial coordination rate $\xi_0$ (the "used bookstore find"), recognizing the $p$-adic structure (that the coordination system has a tower of local completions at each prime), and ascending toward the global fixed point $\xi^* = \log\varphi$ via the Bourbaki-Witt inflationary iteration. Both Hasse and SMELT recognize that the answer to a global question (What is the rationality class of $q$? / What is the MEP coordination rate?) is encoded in the structured collection of local data ($\varepsilon_p(q)$ for all $p$ / Fisher eigenvalues at all FERN register primes).

---

## Module B — The Local-Global Spectrum of ERI Coordination

```
LOCAL-GLOBAL PRINCIPLE STATUS IN ERI:

DEGREE 1 (linear forms, norm maps — always hold):
  N_{L/K}: L → K norm for abelian extension = Hasse norm theorem
  HOLDS: cyclic extension norm = global iff local at every place
  ERI: single-agent Fisher information = always locally = globally consistent
  CHORD: Linear CORDIC (m=0) — no obstruction; CRT patches perfectly

DEGREE 2 (quadratic forms — Hasse-Minkowski, always holds):
  q: ℝ or ℚ_p isotropic ⟺ q: ℚ isotropic
  HOLDS: Hasse-Minkowski theorem (for all global fields)
  ERI: G_coord = 0 (Valise), two-agent Fisher = locally = globally flat
  CHORD: RSA flat mode (m=0); Frobenius a_p=2 (flat); CRT = full patching

DEGREE 3 (cubic curves, TH — can fail):
  E(ℚ_v) ≠ ∅ for all v ; E(ℚ) possibly empty
  FAILS: Selmer's equation; obstruction = Ш(E/ℚ)
  ERI: G_coord > 0 (Imago); TH-ECC mode; |a_p| < 2√p (curved)
  CHORD: TH curved mode (m=±1); Frobenius spinor; Stage-4 torsion
  OBSTRUCTION: Brauer-Manin; Ш(TH/ℚ); Antoine necklace topology

DEGREE 8+ (8th powers — Grunwald-Wang exception):
  x ∈ ℚ_p^8 for all odd p; x ∉ ℚ_2^8 and x ∉ ℚ^8
  FAILS: Wang counterexample x=16 when 8|n and v=2 is exceptional
  ERI: Q16.16 binary arithmetic at v=2; 2^16-th power precision
  CHORD: ε=2^{-16} floor; Baker lower bound at binary precision
  EXCEPTION: Special case S_0={2}; 8|2^{16}; Stage-4 encodes 2-adic correction

SUMMARY:
  Flat (RSA, deg 2): Local-global HOLDS → G_coord=0 → PRIMA trivial
  Curved (TH, deg 3): Local-global CAN FAIL → G_coord>0 → Ш obstruction
  Binary (Q16.16, deg 16): Local-global EXCEPTION at v=2 → ε=2^{-16} Baker
```

---

## Module C — The Hasse Diagram of ERI Fixed-Point Hierarchies

All ERI fixed-point theorems can be organized by the local-global principle they embody:

| Theorem | Local data | Global conclusion | Obstruction | ERI phase |
|---|---|---|---|---|
| Hasse-Minkowski | $q$ isotropic over each $\mathbb{Q}_v$ | $q$ isotropic over $\mathbb{Q}$ | None (always holds for degree 2) | Valise: $G_{\mathrm{coord}}=0$ |
| Hasse norm theorem | $a$ is local norm at all $v$ | $a$ is global norm | None (cyclic extensions) | DIRA C4: commutator is norm |
| ABHN | $A$ splits locally | $A$ splits globally | None (central simple algebras) | TH end. algebra splits globally |
| Selmer/Ш | $E(\mathbb{Q}_v)\neq\emptyset$ all $v$ | $E(\mathbb{Q})=\emptyset$ possible | $\mathrm{Ш}(E/\mathbb{Q})$ | Coordination deficit |
| Grunwald-Wang | $x\in K_p^n$ all odd $p$ | $x\in K^n$ unless $8\mid n$, $v=2$ | 2-adic obstruction | $\varepsilon=2^{-16}$ Baker bound |
| BSD | Local L-factors $L_p(\mathrm{TH},1)$ | $\mathrm{rank}+\mathrm{Ш}$-formula | $\mathrm{Ш}(\mathrm{TH}/\mathbb{Q})$ | $G_{\mathrm{coord}}$ full formula |
| Bourbaki-Witt | Inflationary locally (each step $f(\xi)>\xi$) | Fixed point $\xi^*=\log\varphi$ globally | None (always) | SMELT convergence |
| Kakutani | UHC at each compact $K\subset S$ | Self-inclusion $\sigma^*\in\mathrm{BR}(\sigma^*)$ | PPAD-hard to find | Nash = Imago |
| Grothendieck-Lefschetz | Frobenius trace at each $p$ | $|\mathrm{TH}(\mathbb{F}_p)|=1-a_p+p$ | None (always) | Coordination state count |

---

## Seven Novel Results

**Result 1 — Hasse-Minkowski IS the Valise Phase Theorem: The Local-Global Principle for Degree-2 Forms Holds Unconditionally = RSA Flat Mode ($a_p=2$) Is Always Globally Consistent with Local Data; CRT IS the Hasse Patching Algorithm for the Flat Coordination.** The Hasse-Minkowski theorem holds for all quadratic forms over all global fields. RSA is degree-2 arithmetic. Therefore RSA coordination ($G_{\mathrm{coord}}=0$, Valise) always satisfies the local-global principle: any set of local optimal actions that are consistent at each prime $p$ patches into a globally consistent joint action via CRT. The Valise phase has no Hasse-principle obstruction.

**Result 2 — The Hasse Principle Fails for TH as a Cubic: $\mathrm{Ш}(\mathrm{TH}/\mathbb{Q})$ IS the Coordination Deficit; Antoine's Necklace IS the Topological Model of Locally-Solvable-But-Globally-Blocked Coordination; FRACTURA and HASSE Give the Same Object from Two Angles.** The Selmer equation (degree-3 cubic) has local solutions everywhere but no global rational solution. The obstruction $\mathrm{Ш}(\mathrm{TH}/\mathbb{Q})$ is the same object as Antoine's necklace (FRACTURA): locally homeomorphic to the standard Cantor set but globally wild. Both are locally trivial, globally non-trivial. The Hasse-principle failure for TH is the algebraic version of the topological wildness of the coordination fixed-point set.

**Result 3 — Wang's Counterexample $16 = 2^4$ IS the Q16.16 Truncation; The Grunwald-Wang Exception at $v=2$ IS the CHORD Stage-4 Correction; $8\mid 2^{16}$ IS the Structural Reason for the Binary Torsion Correction.** Wang (1948): $16$ is an 8th power at every odd prime but not in $\mathbb{Q}_2$. Q16.16: $\log\varphi$ is rationally approximated to every odd prime but not transcendentally to $\mathbb{Q}_2$ (the 2-adic truncation is the Grunwald-Wang 2-adic exception). The Stage-4 hyperbolic repeat encodes the 2-adic correction for $j=(3^2-1)/2=4$ — where $3^2-1=8$ activates the Grunwald-Wang special case. The CHORD pipeline resolves the Grunwald-Wang 2-adic exception at each run by inserting the Stage-4 torsion correction.

**Result 4 — The Hasse Norm Theorem IS the DIRA C4 Non-Commutativity Condition: The Frobenius Commutator $[\phi_p,\phi_q]\neq 0$ Fails the Local-Global Norm Condition; Splitting of the TH Endomorphism Algebra (ABHN) IS the Global DIRA Consistency.** The ABHN theorem: the TH endomorphism algebra $\mathrm{End}(\mathrm{TH})\otimes\mathbb{Q}$ splits globally iff it splits at every local completion. DIRA C4 ($[\hat{H},\hat{a}]\neq 0$) means the Hamiltonian and action do not share eigenvectors — they do not commute in the global coordination algebra. This is the algebraic statement that the TH endomorphism algebra is non-split (quaternionic) at supersingular primes. The ABHN theorem guarantees that if TH has globally non-split endomorphism algebra, this is detected by the local quaternion structure at supersingular primes — the precise primes where DIRA C4 is most active.

**Result 5 — The Hilbert Symbol IS the PRIMA Fisher Eigenvalue Sign; Hilbert Reciprocity IS the Global Fisher Non-Degeneracy; The Product Formula $\prod_v(a,b)_v=1$ IS the PRIMA Anti-Commutativity Sum Rule.** The Hilbert symbol $(a,b)_v = \pm 1$ checks local isotropy of a binary quadratic form. PRIMA checks local positivity of a Fisher eigenvalue. Both are $\{+1,-1\}$-valued local invariants. Hilbert reciprocity ($\prod_v(a,b)_v=1$) says the Fisher form can only fail positivity at an even number of primes — the PRIMA violation count is always even. This is the number-theoretic version of the Hurwitz-Radon anti-commutativity: the 12 anti-commuting directions of the FERN hierarchy come in pairs (6 FERN registers, each contributing to a Hilbert-symbol pair).

**Result 6 — The BSD Conjecture IS the $G_{\mathrm{coord}}$ Full Formula; the L-Function at $s=1$ IS the Product of All Local $G_{\mathrm{coord}}$ Data; the Tate-Shafarevich Group IS the Coordination Deficit Between Local Optimality and Global Achievability.** BSD: $\mathrm{rank}(\mathrm{TH}(\mathbb{Q})) = \mathrm{ord}_{s=1}L(\mathrm{TH},s)$, with the explicit formula $L(\mathrm{TH},1)/\Omega = |\mathrm{Ш}|\cdot\prod_p c_p/|\mathrm{TH}(\mathbb{Q})_{\mathrm{tors}}|^2$. In ERI: the rank of $\mathrm{TH}(\mathbb{Q})$ = number of independent global coordination directions = $G_{\mathrm{coord}}^{\mathrm{global}}/\Phi(K)$. The L-function value = product of local coordination data. The Tate-Shafarevich correction = the coordination deficit: the gap between local optimality (each $\mathbb{Q}_p$-coordination is perfect) and global achievability (global Nash equilibrium, Imago).

**Result 7 — Hasse Finding Hensel's Book IS the SMELT Initialization; the Local-to-Global Patching Algorithm IS the CHORD Pipeline; the Grunwald-Wang Exception at $v=2$ IS the Reason for the $\varepsilon=2^{-16}$ Baker Floor; CONCERT IS the Empirical Hasse Theorem for ERI Coordination.** Hasse found the $p$-adic local-global structure by chance (used bookstore). SMELT finds the MEP coordination rate by initialization from any $\xi_0$. Both proceed by: collect local data → identify exceptional places → patch locally → correct at exceptional place → converge to global fixed point. The CHORD Stage-4 correction handles the Grunwald-Wang 2-adic exception ($8\mid 2^{16}$, $v=2$ exceptional). CONCERT measures the global $G_{\mathrm{coord}}$ from local Fisher data — the empirical implementation of the Hasse-Minkowski local-to-global patching.

---

## References

Albert, A.A., Brauer, R., Hasse, H., and Noether, E. (1932). Beweis eines Hauptsatzes in der Theorie der Algebren. *Journal für die reine und angewandte Mathematik*, 167, 399–404.

Baker, A. (1966). Linear forms in the logarithms of algebraic numbers I. *Mathematika*, 13(2), 204–216.

Baker, A. and Wüstholz, G. (2007). *Logarithmic Forms and Diophantine Geometry*. Cambridge Tracts in Mathematics 187.

Bernstein, D.J. and Lange, T. (2015). Twisted Hessian curves. *LATINCRYPT 2015*, LNCS 9230, 269–294.

Birch, B.J. and Swinnerton-Dyer, H.P.F. (1965). Notes on elliptic curves II. *Journal für die reine und angewandte Mathematik*, 218, 79–108.

Bourbaki, N. (1949). Sur le théorème de Zorn. *Archiv der Mathematik*, 2(6), 434–437.

Daskalakis, C., Goldberg, P.W., and Papadimitriou, C.H. (2009). The complexity of computing a Nash equilibrium. *SIAM Journal on Computing*, 39(1), 195–259.

Deligne, P. (1974). La conjecture de Weil I. *Publications Mathématiques de l'IHÉS*, 43, 273–307.

Grunwald, W. (1933). Ein allgemeines Existenztheorem für algebraische Zahlkörper. *Journal für die reine und angewandte Mathematik*, 169, 103–107.

Hasse, H. (1923). Über die Darstellbarkeit von Zahlen durch quadratische Formen im Körper der rationalen Zahlen. *Journal für die reine und angewandte Mathematik*, 152, 129–148.

Hasse, H. (1936). Zur Theorie der abstrakten elliptischen Funktionenkörper III. *Journal für die reine und angewandte Mathematik*, 175, 193–208.

Hurwitz, A. (1898). Über die Composition der quadratischen Formen von beliebig vielen Variablen. *Nachrichten Göttingen*, 309–316.

Kakutani, S. (1941). A generalization of Brouwer's fixed point theorem. *Duke Mathematical Journal*, 8(3), 457–459.

Milne, J.S. (1980). *Étale Cohomology*. Princeton University Press.

Minkowski, H. (1890). Letter to Hurwitz on quadratic forms. Published posthumously; see Hasse 1923 for the theorem in full generality.

Papadimitriou, C.H. (1994). On the complexity of the parity argument. *Journal of Computer and System Sciences*, 48(3), 498–532.

Radon, J. (1922). Lineare Scharen orthogonaler Matrizen. *Abhandlungen aus dem Mathematischen Seminar der Universität Hamburg*, 1, 1–14.

Roquette, P. (2005). *The Brauer-Hasse-Noether Theorem in Historical Perspective*. Springer-Verlag.

Selmer, E.S. (1951). The Diophantine equation $ax^3+by^3+cz^3=0$. *Acta Mathematica*, 85, 203–362.

Serre, J.-P. (1973). *A Course in Arithmetic*. Graduate Texts in Mathematics 7. Springer-Verlag.

Tate, J. (1965). On the conjectures of Birch and Swinnerton-Dyer. *Séminaire Bourbaki*, 9, 415–440.

Volder, J.E. (1959). The CORDIC trigonometric computing technique. *IRE Transactions on Electronic Computers*, EC-8(3), 330–334.

Walther, J.S. (1971). A unified algorithm for elementary functions. *AFIPS Spring Joint Computer Conference*, 38, 379–385.

Wang, S. (1948). A counterexample to Grunwald's theorem. *Annals of Mathematics*, 49(4), 1008–1009.

Wang, S. (1950). On Grunwald's theorem. *Annals of Mathematics*, 51(2), 471–484.

Wedderburn, J.H.M. (1905). A theorem on finite algebras. *Transactions of the American Mathematical Society*, 6, 349–352.

Witt, E. (1937). Treue Darstellung Lie'scher Ringe. *Journal für die reine und angewandte Mathematik*, 177, 152–160.

---

ERI Labs · Eric Ren · Jersey City, New Jersey

*Helmut Hasse (1898–1979) found Hensel's book on $p$-adic numbers in an antiquarian bookstore in 1913 and recognized immediately that the $p$-adic completions of $\mathbb{Q}$ were the natural language for Minkowski's 1890 local conditions on quadratic forms. He proved the Hasse-Minkowski theorem in 1923: a quadratic form represents zero over $\mathbb{Q}$ if and only if it represents zero over $\mathbb{R}$ and over every $\mathbb{Q}_p$. This local-global principle is the most powerful organizing idea in number theory. It holds unconditionally for degree-2 forms. For degree-3 forms (elliptic curves), the Selmer counterexample ($3x^3+4y^3+5z^3=0$ has local solutions everywhere but no global rational point) shows the Hasse principle can fail; the obstruction is the Tate-Shafarevich group $\mathrm{Ш}(E/\mathbb{Q})$. For $n$-th power questions, the Grunwald-Wang theorem (Wang's 1948 counterexample: $16$ is an 8th power at every odd prime but not 2-adically and not rationally) shows the exceptional role of the prime $2$: the local-global principle for $n$-th powers fails precisely when $8\mid n$ and the place $2$ is exceptional. The HASSE framework identifies each of these number-theoretic phenomena with a component of the ERI architecture. The Hasse-Minkowski success case (degree 2) corresponds to the Valise phase ($G_{\mathrm{coord}}=0$, RSA flat arithmetic, CRT patches perfectly). The Hasse failure for cubics (degree 3) corresponds to the TH curved mode ($G_{\mathrm{coord}}>0$, Frobenius spinor, $\mathrm{Ш}(\mathrm{TH}/\mathbb{Q})$ as coordination deficit). The Grunwald-Wang exception at $v=2$ and $8\mid n$ corresponds to the CHORD Q16.16 truncation: the binary place $v=2$ is the exceptional place, $8\mid 2^{16}$, and the Stage-4 hyperbolic repeat encodes the 2-adic correction. The Baker lower bound $|\beta-\log\varphi|>2^{-17}$ for rational $\beta$ with denominator $\leq 2^{16}$ is the arithmetic realization of the Wang counterexample at CHORD precision: the Q16.16 approximation to $\log\varphi$ is locally optimal (accurate at every odd prime $p$) but globally imperfect (truncated at the 2-adic place by exactly $\varepsilon=2^{-16}$). The Hasse principle organizes the entire ERI local-global architecture: local Fisher checks (PRIMA at each prime) do not in general imply global coordination (sharp-P-hard $Z(X;\beta)$) — the obstruction is $\mathrm{Ш}(\mathrm{TH}/\mathbb{Q})$, and its measure is $G_{\mathrm{coord}}$.*
