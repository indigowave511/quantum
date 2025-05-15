# Quantum Information Study Note
## John's Vector and Spinor

Vertically polarized EM wave is transverse, $E^y(t,x,y,z) = E^y(t,z) = A^y \cos(\omega t - k z + \phi)$. 

$k\over 2\pi$: density  in space

$\omega\over 2\pi$: density  in time

Complex EM wave: 
 $E^y = A^y \cos(\omega t - k z + \phi) + i A^y \sin(\omega t - k z + \phi) = A^y e^{\omega t - k z + \phi}$

 $\vec{E} = \begin{bmatrix} A^x e^{\phi_x}\\ A^y e^{\phi_y}\\ 1\end{bmatrix}  e^{\omega t - k z}$

John's vector: 
 $\vec{J} = \begin{bmatrix}  A^x e^{\phi_x}\\ A^y e^{\phi_y} \end{bmatrix} =  A^x e^{\phi_x}  |H\rangle + A^y e^{\phi_y} |V\rangle$ 
### H/V basis : Same frequency, same phase, but different Projections to x, y axis
* $|H\rangle = \begin{bmatrix}1 \\ 0\end{bmatrix}$
* $|V\rangle = \begin{bmatrix}0 \\ 1\end{bmatrix}$

#### 🔸 Why H/V can’t Capture everything needed
$$
|\psi\rangle = \frac{1}{\sqrt{2}} (|H\rangle + |V\rangle) \quad \text{vs.} \quad |\psi\rangle = \frac{1}{\sqrt{2}} (|H\rangle - |V\rangle)
$$

* In both cases, measurement in $H/V$ yields 50% for each.
* But they are **orthogonal** quantum states — totally distinguishable!

---

### D/A basis : Constructive and Destructive interference (Integer phase)
  $$
  |D\rangle  = \frac{1}{\sqrt{2}}(|H\rangle + |V\rangle) = \frac{1}{\sqrt{2}}\begin{bmatrix}1 \\ 1\end{bmatrix},\\
  |A\rangle = \frac{1}{\sqrt{2}}(|H\rangle - |V\rangle) = \frac{1}{\sqrt{2}}\begin{bmatrix}1 \\ -1\end{bmatrix}
  $$
In both cases, measurement in 
𝐻
/
𝑉
H/V yields 50% for each.

But they are orthogonal quantum states — totally distinguishable!
In $|D\rangle$ basis, EM wave is maximally constructive(Even Integer).
$$
E^x(t) = E_0 \cos(\omega t) \\
E^y(t) = E_0 \cos(\omega t)
$$
Likewise in $|A\rangle$ basis, EM wave is maximally destructive(Odd Integer).
$$
 E^x(t) = E_0 \cos(\omega t) \\
 E^y(t) = -E_0 \cos(\omega t) = E_0 \cos(\omega t + \pi)
$$
### 🧮 Superposition of Two Waves
Suppose two EM waves **coherent** (same frequency and same amplitude), having 
**relative phase difference** $\phi$.:

$$
E_1(t) = E_0 \cos(\omega t) \\
E_2(t) = E_0 \cos(\omega t + \phi)
$$
$$
E_{\text{total}}(t) = E_1(t) + E_2(t) = E_0 \cos(\omega t) + E_0 \cos(\omega t + \phi)
$$
Using,
$$
\cos A + \cos B = 2 \cos\left(\frac{A + B}{2}\right)\cos\left(\frac{A - B}{2}\right)
$$

$$
E_{\text{total}}(t) = 2 E_0 \cos\left( \frac{\phi}{2} \right) \cos\left(\omega t + \frac{\phi}{2} \right)
$$

So the **amplitude** becomes:

$$
\text{Amplitude} \propto \cos\left(\frac{\phi}{2}\right)
$$

| Phase Difference | $\cos(\phi/2)$ | Interference Type      |
| ---------------- | -------------- | ---------------------- |
| $0, 2\pi, 4\pi$  | $\pm 1$        | Constructive (max)     |
| $\pi, 3\pi$      | 0              | Destructive (min/null) |
---

### L/R basis : Constructive and Destructive interference (Half Integer phase)
$$
|R\rangle = \frac{1}{\sqrt{2}} (|H\rangle - i|V\rangle)
$$
$$
|L\rangle = \frac{1}{\sqrt{2}} (|H\rangle + i|V\rangle)
$$

In electric field terms, **the $i$ or $-i$ introduces a phase shift**:

* $E_x(t) = E_0 \cos(kz - \omega t)$
* $E_y(t) = \pm E_0 \sin(kz - \omega t)$

$$
\cos(\phi \pm \frac{\pi}{2}) = \mp \sin(\phi)
$$
####  **Helicity**

| Component      | $R$ (right circular)                          | $L$ (left circular)                                  |
| -------------- | --------------------------------------------- | ---------------------------------------------------- |
| $E_x(t)$       | $E_0 \cos(kz - \omega t)$                     | $E_0 \cos(kz - \omega t)$                            |
| $E_y(t)$       | $E_0 \sin(kz - \omega t)$                     | $-E_0 \sin(kz - \omega t)$                           |
| Field vector   | $E_x \hat{x} + E_y \hat{y}$                   | $E_x \hat{x} + E_y \hat{y}$                          |
| Time evolution | Rotates **clockwise** as seen along $+z$-axis | Rotates **counterclockwise** as seen along $+z$-axis |
#### 🟡 In all D/A and L/R, 
| **Phase Difference**             | $\cos(\phi/2)$           | **Interference Type**             | **Resulting Rotation**                  |
| -------------------------------- | ------------------------ | --------------------------------- | --------------------------------------- |
| $0, 2\pi, 4\pi$                  | $\pm 1$                  | Constructive (max amplitude)      | Linear polarization (no net rotation)   |
| $\pi, 3\pi$                      | 0                        | Destructive (min/null)            | Cancelled; no field                     |
| $\frac{\pi}{2}, \frac{5\pi}{2}$  | $\pm \frac{1}{\sqrt{2}}$ | Partial constructive (elliptical) | Left-handed (counterclockwise) rotation |
| $\frac{3\pi}{2}, \frac{7\pi}{2}$ | $\pm \frac{1}{\sqrt{2}}$ | Partial constructive (elliptical) | Right-handed (clockwise) rotation       |


### 🔬 Quantum Tomography
Generic complex EM field, or quantum state of a photon:
$$
|\psi\rangle = \alpha |H\rangle + \beta |V\rangle
= |\alpha| e^{i\theta_H} |H\rangle + |\beta| e^{i\theta_V} |V\rangle, \quad  \text{with } |\alpha|^2 + |\beta|^2 = 1
$$
$$
\rho = |\psi\rangle \langle \psi | = \begin{bmatrix}
|\alpha|^2 & \alpha^* \beta \\
\beta^* \alpha & |\beta|^2
\end{bmatrix}
$$
* $|\alpha|, |\beta|$ from H/V basis
* $\text{Re}(\alpha^* \beta)$ from D/A basis
* $\text{Im}(\alpha^* \beta)$ from R/L basis

### Population imbalance between D and A
$$
\Pi_D = |D\rangle\langle D| = \frac{1}{2}
\begin{bmatrix}
1 & 1 \\
1 & 1
\end{bmatrix}, \quad
\Pi_A = |A\rangle\langle A| = \frac{1}{2}
\begin{bmatrix}
1 & -1 \\
-1 & 1
\end{bmatrix}
$$

The probabilities of outcomes $D$ and $A$ are:

$$
P(D) = \langle \psi |D \rangle \langle D |\psi\rangle = \text{Tr}(\rho \Pi_D), \quad
P(A) = \langle \psi |A \rangle \langle A |\psi\rangle = \text{Tr}(\rho \Pi_A)
$$

Let’s compute $P(D) - P(A)$:

$$
P(D) - P(A) = \text{Tr}(\rho (\Pi_D - \Pi_A)) = \text{Tr}(\rho\, \sigma_x)
$$

because:

$$
\Pi_D - \Pi_A = 
\frac{1}{2}
\left[
\begin{bmatrix}
1 & 1 \\
1 & 1
\end{bmatrix}
-
\begin{bmatrix}
1 & -1 \\
-1 & 1
\end{bmatrix}
\right]
=
\frac{1}{2}
\begin{bmatrix}
0 & 2 \\
2 & 0
\end{bmatrix}
=
\begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix}
= \sigma_x
$$


$$
\text{Tr}(\rho\, \sigma_x)
=
\text{Tr}
\left(
\begin{bmatrix}
|\alpha|^2 & \alpha \beta^* \\
\alpha^* \beta & |\beta|^2
\end{bmatrix}
\begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix}
\right)
=
\text{Tr}
\left(
\begin{bmatrix}
\alpha \beta^* & |\alpha|^2 \\
|\beta|^2 & \alpha^* \beta
\end{bmatrix}
\right)
= \alpha \beta^* + \alpha^* \beta
= 2 \,\text{Re}(\alpha^* \beta)
$$

---


### Population imbalance between R and L
$$
\Pi_R = |R\rangle\langle R| = \frac{1}{2}
\begin{bmatrix}
1 & -i \\
i & 1
\end{bmatrix}, \quad
\Pi_L = |L\rangle\langle L| = \frac{1}{2}
\begin{bmatrix}
1 & i \\
-i & 1
\end{bmatrix}
$$
$$
P(R) - P(L) = \text{Tr}(\rho (\Pi_R - \Pi_L)) = \text{Tr}(\rho\, \sigma_y)
 =
\text{Tr}\left(
\begin{bmatrix}
|\alpha|^2 & \alpha \beta^* \\
\alpha^* \beta & |\beta|^2
\end{bmatrix}
\begin{bmatrix}
0 & -i \\
 i & 0
\end{bmatrix}
\right)
 = 2\, \text{Im}(\alpha^* \beta)
$$

$$
\boxed{\text{Tr}(\rho\, \sigma_y) = 2\, \text{Im}(\alpha^* \beta)}
$$
---

# Stern-Gerlach Experiment
* Beam split
* Splitted beams are projective: Orthogonality along the same axis orthogonal.
* Zero expectation on perpendicular axis

## Quantum Discrimination


* **Alice** prepares one of two known pure states:

  $$
  |0\rangle \quad (\text{label } L_0) \quad \text{or} \quad |\Psi\rangle = \psi_0 |0\rangle + \psi_1 |1\rangle \quad (\text{label } L_\Psi)
  $$
, where
$$
|0\rangle = \begin{bmatrix} 1 \\ 0 \end{bmatrix}, \quad |\Psi\rangle = \begin{bmatrix} \psi_0 \\ \psi_1 \end{bmatrix}
$$
with $|\psi_0|^2 + |\psi_1|^2 = 1$.

For $|0\rangle$:
$$
\rho_0 = |0\rangle \langle 0| = \begin{bmatrix} 1 \\ 0 \end{bmatrix} \begin{bmatrix} 1 & 0 \end{bmatrix} = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}
$$
For $|\Psi\rangle = \psi_0 |0\rangle + \psi_1 |1\rangle$:
$$
\rho_\Psi = |\Psi\rangle \langle \Psi| = \begin{bmatrix} \psi_0 \\ \psi_1 \end{bmatrix} \begin{bmatrix} \psi_0^* & \psi_1^* \end{bmatrix} = \begin{bmatrix} |\psi_0|^2 & \psi_0 \psi_1^* \\ \psi_0^* \psi_1 & |\psi_1|^2 \end{bmatrix}
$$

* **Alice** makes probabilistic arrangement of two states:
$$
 q_0 |0\rangle + q_1 |\Psi\rangle, \quad \text{where } q_0 + q_1 = 1
$$
Bob has to do to **specify the labels $L_0$ and $L_\Psi$** when trying to discriminate Alice’s two states.

* **Bob** knows:

  * The exact definitions of $|0\rangle$ and $|\Psi\rangle$ as well as $q_0$ and $q_1$.
  * His goal: when he gets a quantum system from Alice, perform a **measurement** whose result lets him assign the correct label.

---

### What Bob Needs to Do

Bob must design a measurement that gives him **information** to tell apart the two states.

There are two approaches:

---

#### (1) **Projective Measurement**

* Bob picks two basis $\{ |X_0\rangle, |X_\Psi\rangle \}$ such that:

  * $|X_0\rangle$ is the direction “most aligned” to $|0\rangle$.
  * $|X_\Psi\rangle$ is the direction “most aligned” to $|\Psi\rangle$.

* He builds projectors to "perfectly" discriminate the lables:

  $$
  \Pi_0 = |X_0\rangle \langle X_0|, \quad \Pi_\Psi = |X_\Psi\rangle \langle X_\Psi|
  $$
🔸 There are photons from $\Psi$ label to be detected on $\Pi_0$, aren't there?  
✅ However, when Bob receives a quantum state:

* Apply the measurement $\{ \Pi_0, \Pi_\Psi \}$.
* If outcome = $\Pi_0$, **guess label $L_0$**.
* If outcome = $\Pi_\Psi$, **guess label $L_\Psi$**.

There are photons that **do not match** either projection.
$$
\Pi_{\perp} = I - \Pi_0 - \Pi_\Psi
$$
This represents the **“lost” events** — photons that:
* Are absorbed,
* Pass through undetected,
* Or get scattered into unmeasured directions.


---

#### (2) **Optimal POVM (Helstrom Measurement)**

* For **minimum error discrimination**, the mathematically optimal approach is:

  * Calculate the Helstrom projector onto the **positive part** of $\rho_0 - \rho_\Psi$ (the difference of density matrices).

This gives:

* $E_0$ (positive outcome region) → assign $L_0$.
* $E_\Psi$ (negative outcome region) → assign $L_\Psi$.

This strategy **maximizes the probability** of correct labeling.

✅ If the overlap $|\langle 0 | \Psi \rangle| \neq 0$, it means there’s **nonzero confusion**, but the optimal measurement minimizes this error.
 
✅ Perfect overlap: $|\langle 0 | \Psi \rangle| = 1$.  This only happens if:
$$
|\Psi\rangle = e^{i\phi} |0\rangle
$$
That is, the states are **identical up to a global phase**.

* Bob **cannot** tell the difference.
* No measurement can help.
* His best bet is to **guess randomly**, with success probability $\frac{1}{2}$.

This is the **maximum possible confusion** case.

✅ Zero overlap $|\langle 0 | \Psi \rangle| = 0$.
$$
|\Psi\rangle = |1\rangle
$$
That is, the states are **orthogonal**.

* Bob can perfectly discriminate them.
* He can apply the projective measurement(1) $\{|0\rangle, |1\rangle\}$.
* He can also apply Helstrom Measurment, where success probability = 1.

Let's see why the last is true. 

Bob's measurement basis in general:
$$
|X\rangle = \begin{bmatrix} a \\ b \end{bmatrix}, \quad \text{with} \quad |a|^2 + |b|^2 = 1
$$
and the corresponding **projector**:
$$
\Pi_X = |X\rangle \langle X| = \begin{bmatrix} a \\ b \end{bmatrix} \begin{bmatrix} a^* & b^* \end{bmatrix} = \begin{bmatrix} |a|^2 & a b^* \\ a^* b & |b|^2 \end{bmatrix}
$$
✅ $\det{\Pi_X} = 0$, since **factorized matrix determinant is zero**.
$$
\begin{aligned}
1
&=\Pr(\text{send }0)\;
                 [\Pr(\text{outcome }0 \mid \text{send }0) + \Pr(\text{outcome }\Psi \mid \text{send }0)]\\[2pt]
&\quad + \Pr(\text{send }\Psi)\;
                 [\Pr(\text{outcome }0 \mid \text{send }\Psi) + \Pr(\text{outcome }\Psi \mid \text{send }\Psi)]\\[2pt]
\end{aligned}
$$ 
The probability for Bob's correct labels:
$$
\begin{aligned}
P_{\text{succ}}
&=\sum_{k\in\{0, \Psi\}}\Pr(\text{send }k)\;
                 \Pr(\text{outcome }k \mid \text{send }k) \\[2pt]
&=\sum_{k\in\{0, \Psi\}}q_k \langle \Psi_k \mid X_k \rangle \langle X_k \mid \Psi_k \rangle \\
&=\sum_{k\in\{0, \Psi\}}q_k \operatorname{Tr}(\rho_k \Pi_k).
\end{aligned}
$$
If Bob's measurement basis($\Pi := \Pi_X$) is complete(,which is not the case in projective discrimination), 
$$
\Pi + \Pi_{\bot} = \mid X \rangle \langle X \mid + \mid X_{\bot} \rangle \langle X_{\bot} \mid = I  
$$
$$
\begin{aligned}
P_{\text{succ}}
&=q_\Psi \operatorname{Tr}(\rho_\Psi) + \operatorname{Tr}([q_0\rho_0 - q_\Psi \rho_\Psi]\Pi)\\
&=q_\Psi + \operatorname{Tr}([q_0\rho_0 - q_\Psi \rho_\Psi]\Pi) \\
&=q_\Psi + \operatorname{Tr}(\Pi \,\Gamma) 
\end{aligned}
$$
The Helstrom operator:
$$
\boxed{\;
\Gamma := q_0 \rho_0 - q_\Psi \rho_\Psi
\;}
$$

Write $\Gamma$ in its spectral decomposition:

$$
\Gamma=\sum_{i}\lambda_i |v_i\rangle\!\langle v_i|
      =\underbrace{\sum_{\lambda_i>0}\lambda_i |v_i\rangle\!\langle v_i|}_{\displaystyle\Gamma_{+}}
       \;-\;
       \underbrace{\sum_{\lambda_j<0}|\lambda_j| |v_j\rangle\!\langle v_j|}_{\displaystyle\Gamma_{-}} ,
$$
so that $\Gamma_{+}\ge0,\;\Gamma_{-}\ge0$ and $\Gamma=\Gamma_{+}-\Gamma_{-}$.

The task is to choose projection $\Pi$ on $\Gamma$ to maximize $\operatorname{Tr}(\Pi \Gamma)$, which is obviously the seggregation of positive eigenvalues. 
$$
\Pi = \Gamma_+ 
$$
$$
\max_{0\le\Pi\le I}\;
        \operatorname{Tr}\bigl(\Pi \,\Gamma\bigr)
      =\!\!\sum_{\lambda_i>0}\!\!\lambda_i 
$$

**Trace norm** is called the 1-norm of its spectrum
$$
\boxed{\;
\lVert\Gamma\rVert_1
      =\sum_i|\lambda_i|
      =\operatorname{Tr}\Gamma_{+}+\operatorname{Tr}\Gamma_{-}.
\;}
$$
Choosing the optimal $\Pi_0 = \Gamma_+$ and using trace norm:
$$
\begin{aligned}
P_{\text{succ}}^{\max}
   &=q_\Psi+\operatorname{Tr}\Gamma_{+}  \\[2pt]
   &=q_\Psi+\tfrac12\bigl(\lVert\Gamma\rVert_1+\operatorname{Tr}\Gamma\bigr) \\
   &=q_\Psi+\tfrac12\bigl(\lVert\Gamma\rVert_1+(q_0 - q_\Psi)\bigr) \\
   &=\tfrac12\bigl(\lVert\Gamma\rVert_1+1\bigr)
\end{aligned}
$$


## Trace Norm Algebra
### Singular(Non-negative) Value Decompostion
For **every** matrix $A\in\mathbb C^{m\times n}$ **(real or complex, square or rectangular)** there are

* a unitary $U\in\mathbb C^{m\times m}$
* a unitary $V\in\mathbb C^{n\times n}$
* a diagonal matrix $\Sigma\in\mathbb R^{m\times n}$ whose only non-zero entries are non-negative numbers
  $\sigma_1\ge\sigma_2\ge\dots\ge\sigma_r>0$ on its main diagonal ($r=\operatorname{rank}A$)

such that
$$
A \;=\; U\,\Sigma\,V^{\dagger}.
$$
💡🤩 **Meanwhile $A$ is a generic matrix, $A^{\dagger}A$ is an $n\times n$ Hermitian, positive-semidefinite matrix.**

$$\begin{array}{}
V^{\dagger}(A^{\dagger}A)V = \Lambda
            = \operatorname{diag}\!\bigl(\sigma_1^{2},\dots,\sigma_n^{2}\bigr), 
\\
 (V^{\dagger}A^{\dagger}U )( U^{\dagger}AV)= \sqrt\Lambda \sqrt\Lambda = \Sigma \Sigma = \Sigma^{\dagger} \Sigma = \operatorname{diag}\!\bigl(|\sigma_1|,\dots,|\sigma_n|\bigr)^2
\end{array}
$$
It is a good guess that $\Sigma = U^{\dagger}AV $. Let's verify if it indeed is true. 

$U \Sigma = U U^{\dagger}AV \Rightarrow U = AV \Sigma^{-1} \Rightarrow U \Sigma V^{\dagger} = A V \Sigma^{-1}\Sigma V^{\dagger} = A.$
#### Example: square vs rectangular case

1️⃣ If $A$ is square (e.g., $2 \times 2$):

* SVD gives $A = U \Sigma V^\dagger$ with $\Sigma$ diagonal $2 \times 2$, nonnegative singular values.
* Eigenvalue diagonalisation (if possible) gives $A = S D S^{-1}$ with $D$ diagonal, possibly complex eigenvalues (can be negative or even nonreal).

2️⃣ If $A$ is rectangular (e.g., $3 \times 2$):

* Only SVD applies; there’s **no** eigenvalue diagonalisation.
* $\Sigma$ will be a $3 \times 2$ diagonal matrix with zeros off the main diagonal, nonnegative entries.
---
## No Cloning Theorem
Show that for two non-orthogonal pure qubit states

$$
\rho = |\psi\rangle\!\langle\psi|,\qquad
\sigma = |\phi\rangle\!\langle\phi|,\qquad
0 < s:=|\langle\psi|\phi\rangle| < 1,
$$

the trace distance **increases** if an ideal cloner $\rho\mapsto\rho^{\otimes 2}$ is applied to both inputs:

$$
D(\rho^{\otimes 2},\sigma^{\otimes 2}) \;>\; D(\rho,\sigma).
$$
---
Proof: 
For any kets $|\psi\rangle,|\phi\rangle$ the trace distance is

$$
\boxed{\;D\bigl(|\psi\rangle,|\phi\rangle\bigr)
      =\sqrt{1-\bigl|\langle\psi|\phi\rangle\bigr|^{2}}\;} .
$$

In the basis $\{|e_1\rangle=|\psi\rangle,\;|e_2\rangle\}$ with
$|\phi\rangle = s|e_1\rangle+\sqrt{1-s^{2}}\,|e_2\rangle$,
the matrix $\rho-\sigma$ has eigenvalues $\pm\sqrt{1-s^{2}}$;
the trace norm $||\rho-\sigma||_1$ is twice that number, and
$D=\tfrac12||\rho-\sigma||_1=\sqrt{1-s^{2}}$.


  Let
   $|u\rangle:=|\psi\psi\rangle,\;|v\rangle:=|\phi\phi\rangle$.
   Because $|u\rangle$ and $|v\rangle$ are generally not parallel but lie in the huge $4$-qubit Hilbert space, the span $\mathcal S=\operatorname{span}\{|u\rangle,|v\rangle\}$ is at most 2-D.
   Outside $\mathcal S$ both projectors act as zero, so the spectrum of
   $\Delta=\rho^{\otimes2}-\sigma^{\otimes2}$ is completely determined by its $2\times2$ representation on $\mathcal S$.

  Concretely, choose an orthonormal basis of $\mathcal S$:

   $$
     |e_1\rangle := |u\rangle, \qquad
     |e_2\rangle := \frac{|v\rangle-\alpha|u\rangle}{\sqrt{1-\alpha^{2}}},
     \quad\text{with}\;
     \alpha:=\langle u|v\rangle=s^{2}\in(0,1).
   $$

In this basis

   $$
     \rho^{\otimes2}=
     \begin{pmatrix}1&0\\0&0\end{pmatrix},\qquad
     \sigma^{\otimes2}=
     \begin{pmatrix}\alpha^{2}&\alpha\sqrt{1-\alpha^{2}}\\
                     \alpha\sqrt{1-\alpha^{2}}&1-\alpha^{2}\end{pmatrix}.
   $$

**Compute the eigenvalues in that $2\times2$ block.**

   $$
     \Delta = \rho^{\otimes2}-\sigma^{\otimes2}
            =\begin{pmatrix}
                 1-\alpha^{2} & -\alpha\sqrt{1-\alpha^{2}}\\
                 -\alpha\sqrt{1-\alpha^{2}} & -\!(1-\alpha^{2})
              \end{pmatrix}.
   $$
Its eigenvalues are easily found to be $\pm\sqrt{1-\alpha^{2}}$.
   (Check: the trace is zero, the determinant is $-\!(1-\alpha^{2})$.)

**Trace norm and trace distance.**
   The trace norm is twice the positive eigenvalue:

   $$
      \|\Delta\|_{1}=2\sqrt{1-\alpha^{2}},
      \qquad
      D(\rho^{\otimes2},\sigma^{\otimes2})
        =\tfrac12\|\Delta\|_{1}
        =\sqrt{1-\alpha^{2}}
        =\sqrt{1-s^{4}}.
   $$

5. **Compare with the single-copy distance.**
   Before cloning, $D(\rho,\sigma)=\sqrt{1-s^{2}}$.
   Because $0<s<1\Rightarrow s^{4}<s^{2}$, we indeed have

   $$
     \sqrt{1-s^{4}}\;>\;\sqrt{1-s^{2}}.
   $$


---
#### Assume a universal cloner exists then compute how far *apart* the ideal clones would be
$$
\begin{aligned}
D(\rho,\sigma)          &=\sqrt{1-s^{2}},\\[4pt]
D(\rho\otimes\rho,\;\sigma\otimes\sigma)
                         &=\sqrt{1-s^{4}}
                          =\sqrt{1-(s^{2})^{2}}\;>\;\sqrt{1-s^{2}}
                          =D(\rho,\sigma).
\end{aligned}
$$
Once the maximum discrimination was the trace norm $D(\rho,\sigma)$, no other operator trace norm can not be greater than this.

Therefore, hypothetical cloner violates the maximality of discrimination.∎

---
## Schmidt Decomposition(To measure degree of entanglement)

Let $\mathcal H_A$ and $\mathcal H_B$ be finite-dimensional Hilbert spaces with dimensions $d_A$ and $d_B$.
For **every *normalised* bipartite pure state**

$$
\lvert\psi\rangle\in\mathcal H_A\otimes\mathcal H_B,\qquad
\langle\psi\vert\psi\rangle=1,
$$

there exist

* non-negative real numbers (Schmidt coefficients) $\{\lambda_k\}_{k=1}^{r}$ satisfying $\sum_{k=1}^{r}\lambda_k^{2}=1$

* orthonormal sets $\{\lvert u_k\rangle\}_{k=1}^{r}\subset\mathcal H_A$ and $\{\lvert v_k\rangle\}_{k=1}^{r}\subset\mathcal H_B$,

such that

$$
\boxed{\;
\lvert\psi\rangle=\sum_{k=1}^{r}\lambda_k\,\lvert u_k\rangle\otimes\lvert v_k\rangle
\;}
$$

where $r=\operatorname{rank}(\psi)\le\min(d_A,d_B)$ is the **Schmidt rank**.
The set $\{\lambda_k\}$ and $r$ are unique (up to degeneracy-phase conventions).

Proof: 

* Write $\lvert\psi\rangle = \sum_{i=1}^{d_A}\sum_{j=1}^{d_B} C_{ij}\lvert i\rangle_A\otimes\lvert j\rangle_B$ in chosen product bases.

* View the coefficients $C$ as a $d_A\times d_B$ matrix.
Perform an SVD: $C = U\Lambda V^\dagger$ with diagonal $\Lambda=\mathrm{diag}(\lambda_1,\dots,\lambda_r)$.
* Defining $\lvert u_k\rangle=\sum_i U_{ik}\lvert i\rangle_A$ and $\lvert v_k\rangle=\sum_j V^{*}_{jk}\lvert j\rangle_B$ yields the boxed form above.

#### Key properties

* Invariance of Schmidt coefficients $\lambda_k$ 

 $
(U_A\!\otimes\!V_B)\lvert\psi\rangle
=\sum_{k}\lambda_k\,(U_A\lvert u_k\rangle_A)\otimes(V_B\lvert v_k\rangle_B)
        \;=\sum_{k}\lambda_k\,\lvert u'_k\rangle_A\otimes\lvert v'_k\rangle_B .
$
Explanation: 

*For $A$,   $\rho_A=\operatorname{Tr}_B\lvert\psi\rangle\langle\psi\rvert$:*

$$
\rho_A'=\operatorname{Tr}_B\!\bigl[(\mathbb I\!\otimes\!U_B)\,
        |\psi\rangle\langle\psi|\,
        (\mathbb I\!\otimes\!U_B^{\dagger})\bigr]
      =\operatorname{Tr}_B\!\bigl[|\psi\rangle\langle\psi|\bigr]
      =\rho_A .
$$
  $$
  \rho_A \;\xrightarrow{\,U_A\otimes\mathbb I\,}\; U_A\rho_A U_A^{\dagger}
  \quad\Longrightarrow\quad
  \text{same eigenvalues }(\lambda_k^{2}).
  $$

*For $B$,*

$$
\rho_B'=\operatorname{Tr}_A|\psi'\rangle\langle\psi'|
      =U_B\,\rho_B\,U_B^{\dagger},
$$





| Quantity                             | Meaning                                                                                                                                 |
| ------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------- |
| **Schmidt coefficients** $\lambda_k$ | “Weights’’ of each correlated pair; invariant under local unitaries.                                                                    |
| **Schmidt rank** $r$                 | Minimum number of product terms; $r=1$ ⇔ state is *separable*.                                                                          |
| **Reduced states**                   | $\rho_A=\operatorname{Tr}_B\lvert\psi\rangle\langle\psi\rvert=\sum_k\lambda_k^2\lvert u_k\rangle\langle u_k\rvert$ (similarly for $B$). |
| **Entropy of entanglement**          | $S(\rho_A)= -\sum_k\lambda_k^2\log\lambda_k^2$.                                                                                         |
| **Contracted overlaps**              | Inner product of two pure states equals the dot product of their Schmidt vectors $(\lambda_k)$.                                         |

---

#### Examples:

1️⃣. **Bell state**

   $$
   \lvert\Phi^+\rangle=\tfrac1{\sqrt2}\bigl(\lvert00\rangle+\lvert11\rangle\bigr)
   =\sum_{k=1}^{2}\tfrac1{\sqrt2}\,{\lvert k\rangle\!}_A\otimes{\lvert k\rangle\!}_B 
   $$

   Schmidt coefficients $\lambda_{1,2}=1/\sqrt2$; rank $r=2$ ⇒ maximally entangled (entropy = 1 bit).

2️⃣. **Product state**
   $\lvert\psi\rangle=\lvert0\rangle_A\otimes(\alpha\lvert0\rangle+\beta\lvert1\rangle)_B$ has one non-zero coefficient ($\lambda_1=1$), hence $r=1$ and no entanglement.

