$z=\sqrt{ x^{2}+y^{2} }=:|z|$
$\phi=:arg(z), z\neq {0}$
$arg(z)\in[0;2\pi)$ или $(-\pi;\pi]$ или $\dots$
$Arg(z):=arg(z)+2\pi k, \ k\in \mathrm{Z}$

![[im_dec_phi.svg]]
### Алгебраическая форма записи
$z=x+iy$
$\omega=u+iv$
$\zeta=\xi+i\eta$

### Тригонометрическая запись комплексного числа
$z\to r_{1}\phi$
$\omega\to \rho_{1}\psi$

$z=x+iy=r\cos \phi+ir\sin \phi=|z|(\cos \phi+i\sin \phi)$


$$
z_{1}z_{2}=r_{1}(\cos \phi_{1}+i\sin \phi_{1})r_{2}(\cos \phi_{2}+i\sin \phi_{2})=r_{1}r_{2}[(\cos \phi_{1}\cos \phi_{2}-\sin \phi_{1}\sin \phi_{2})+i(\cos \phi_{1}\sin \phi_{2}+\sin \phi_{1}\cos \phi_{2})=r_{1}r_{2}(\cos(\phi_{1}+\phi_{2})+i\sin(\phi_{1}+\phi_{2}))]
$$
$\frac{z_{1}}{z_{2}}=\frac{r_{1}}{r_{2}}(\cos(\phi_{1}-\phi_{2})+i\sin(\phi_{1}-\phi_{2}))$

### Экспоненциальная форма записи комплексного числа
$\boxed{e^{i\alpha}=\cos\alpha+i\sin\alpha}$ при $\alpha \in C$ — Формула Эйлера

$e^z=e^{x+iy}:=e^x(\cos y+i\sin y)$
$e^{z_{1}}e^{z_{2}}=e^{z_{1}+z_{2}}$

$$
\begin{array}{a}
e^{i\alpha}=\cos\alpha+i\sin\alpha \\
e^{-i\alpha}=\cos\alpha -i\sin\alpha
\end{array}\implies
\cos\alpha=\frac{{e^{i\alpha}+e^{-i\alpha}}}{2}, \ \sin\alpha=\frac{{e^{i\alpha}-e^{-i\alpha}}}{2i}
$$
### Формула де Муавра

при $n\in \mathrm{N}$
$\boxed{(\cos\alpha+i\sin\alpha)^n=\cos n\alpha+i\sin n\alpha}$

### bebebe
$$
(\cos\alpha+i\sin\alpha)^3=\cos^3\alpha+3\cos ^{2}\alpha(i\sin\alpha)+3\cos\alpha(i\sin\alpha)^{2}+(i\sin\alpha)^{3}=(\cos ^{3}\alpha-3\cos\alpha \sin ^{2}\alpha)+i(3\cos ^{2}\alpha \sin\alpha-\sin ^{3}\alpha)
$$

### Корень комплексного числа

$n\in \mathrm{N}$
$\sqrt[n]{ z }=\omega=z^{1/n}\implies z=\omega^n$

$z=re^{i\phi}=r(\cos \phi+i\sin \phi)$
$\omega=\rho e^{i\psi}=\rho(\cos \psi+i\sin \psi)$

$r(\cos \phi+i\sin \phi)=\rho^n(\cos n\psi+i\sin n\psi)$
$$
\left\{
\begin{array}{s}
\rho^n=r  \ \text{при} \ \rho>0,r>0 \\
\cos n\psi+i\sin n\psi=\cos\phi +i\sin \phi
\end{array}
\right.
\Longleftrightarrow
\left\{
\begin{array}{a}
\rho=\sqrt[n]{ r } \\
n\psi=\phi+2\pi k, &k\in \mathrm{Z}
\end{array}
\right.
$$


$\boxed{\psi=\frac{\phi}{n}+\frac{2\pi}{n}k}$

![[im_radial.svg]]
