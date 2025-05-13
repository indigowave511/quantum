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



