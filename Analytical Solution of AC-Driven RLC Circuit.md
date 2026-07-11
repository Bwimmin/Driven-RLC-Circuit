
The second-order differential equation of current for an AC-driven RLC circuit is,
$$\begin{eqnarray}
I''+ \frac{R}{L}I'+\frac{1}{LC}I=\frac{V_{0}}{L}\omega \cos \omega t
\end{eqnarray}$$
$\text{let } \alpha=\frac{R}{2L}, \quad\omega_{0}=\frac{1}{\sqrt{LC}}, \quad F_{0}=\frac{V{0}}{L}\omega$
$$\boxed{I''+2\alpha I'+\omega_{0}^{2}I=F_{0}\cos \omega t}\tag{1}$$
**Complimentary Solution :** 
 let $I''+2\alpha I'+\omega_{0}^{2}I=0$$$I=e^{ mx}, \quad I'=me^{ mx }, \quad I''=m^{2}e^{mx}$$$$\begin{eqnarray}
 m^{2}e^{ mx }+2\alpha (me^{ mx })+\omega_{0}^{2}e^{ mx }&=&0\\
 m^{2}+2\alpha m+\omega_{0}^{2}&=&0
 \end{eqnarray}$$ $$\begin{eqnarray}
 m_{1,2}&=& \frac{-2\alpha\pm \sqrt{(2\alpha)^{2}-4(1)(\omega^{2})}}{2(1)}\\&=& -\alpha\pm \sqrt{\alpha^{2}-\omega_{0}^{2}}
 \end{eqnarray}$$ We are interested in underdamped cases ($\omega_{0}>\alpha$)
 $$\begin{eqnarray}
 m_{1,2}&=&-\alpha \pm \sqrt{-(\omega_{0}^{2}-\alpha^{2})}=-\alpha\pm i\sqrt{\omega_{0}^{2}-\alpha^{2}} \\ &=& -\alpha\pm i\omega_{d}
 \end{eqnarray}$$ where $\omega_{d}=\sqrt{\omega_{0}^{2}-\alpha^{2}}$

 The roots are complex, therefore the complimentary solution is given as
$$I_{c}=e^{ -\alpha t}(A_{1}\cos \omega_{d} t+A_{2}\sin \omega_{d} t)$$
 

**Particular Solution :** 
$$\begin{eqnarray}
F_{0}\cos(\omega t) \Rightarrow I_{p}&=& B_{1}\cos \omega t+B_{2}\sin \omega t\\I'_{p}&=&-B_{1}\omega\sin \omega t+B_{2}\omega\cos \omega t\\ I_{p}'' &=&-B_{1}\omega^{2}\cos \omega t -B_{2}\omega^{2}\sin \omega t
\end{eqnarray}$$
Substitute into the differential equation (1)
$$\begin{eqnarray}
-B_{1}\omega^{2}\cos \omega t -B_{2}\omega^{2}\sin \omega t+2\alpha (-B_{1}\omega\sin \omega t+B_{2}\omega\cos \omega t)+\omega_{0}^{2}(B_{1}\cos \omega t+B_{2}\sin \omega t)= F_{0}\cos \omega t
\end{eqnarray}$$
comparing coefficients of $\color{blue}\cos \omega t$
$$\begin{eqnarray}
-B_{1}\omega^{2}+2\alpha \omega B_{2}+\omega_{0}^{2}B_{1}&=&F_{0}\\B_{1}(\omega_{0}^{2}-\omega^{2})+2\alpha \omega B_{2}&=&F_{0} \tag{2}
\end{eqnarray}$$
comparing coefficients of $\color{blue}\sin \omega t$
$$\begin{eqnarray}
-B_{2}\omega^{2}-2\alpha \omega B_{1}+\omega_{0}^{2}B_{2} &=& 0\\B_{2}(\omega_{0}^{2}-\omega^{2})-2\alpha \omega B_{1}&=&0 \\B_{1}&=&\frac{B_{2}(\omega_{0}^{2}-\omega^{2})}{2\alpha \omega}\tag{3}
\end{eqnarray}$$
substitute (3) into (2)

$$\begin{eqnarray}
\left( \frac{B_{2}(\omega_{0}^{2}-\omega^{2})}{2\alpha \omega} \right)(\omega_{0}^{2}-\omega^{2})+2\alpha \omega B_{2}&=&F_{0} \\ 
B_{2}\left(\frac{(\omega_{0}^{2}-\omega^{2})^{2}}{2\alpha \omega}+2\alpha \omega\right)&=&F_{0}\\ B_{2}\left(\frac{(\omega_{0}^{2}-\omega^{2})^{2}+(2\alpha \omega)^{2}}{2\alpha \omega}\right)&=&F_{0}\\ B_{2}&=& \frac{F_{0}(2\alpha \omega)}{(\omega_{0}^{2}-\omega^{2})^{2}+(2\alpha \omega)^{2}}
\end{eqnarray}$$
let $D=(\omega_{0}^{2}-\omega^{2})^{2}+(2\alpha \omega)$
$$\boxed{B_{2}=\frac{F_{0}(2\alpha \omega)}{D}}\tag{4}$$

Substitute (4) into (3)
$$\begin{eqnarray}
B_{1}&=&\frac{(\frac{F_{0}(2\alpha \omega)}{D})(\omega_{0}^{2}-\omega^{2})}{2\alpha \omega}\\
\end{eqnarray}$$ $$\boxed{B_{1}=\frac{F_{0}(\omega_{0}^{2}-\omega^{2})}{D}} \tag{5}$$
>[!danger] Particular Solution
>$$\therefore I_{p}=B_{1}\cos \omega t+B_{2}\sin \omega t$$where
>$D_{1}=(\omega_{0}^{2}-\omega^{2})^{2}-(2\alpha \omega)^{2}$
>$B_{1}=\frac{F_{0}(\omega_{0}^{2}-\omega^{2})}{D_{1}}$
>$B_{2}=\frac{F_{0}(2\alpha \omega)}{D_{1}}$

The Full solution of equation (1) is given by
$$\begin{eqnarray}
I&=&I_{c}+I_P\\&=& e^{ -\alpha t}(A_{1}\cos \omega_{d} t+A_{2}\sin \omega_{d} t)+B_{1}\cos \omega t+B_{2}\sin \omega t
\end{eqnarray}$$
Initial Values : $I(0)=0$
$$\begin{eqnarray}
0&=&A_{1}+B_{1}\\A_{1}&=& -B_{1}
\end{eqnarray}$$

$$I'=-\alpha e^{ -\alpha t }(A_{1}\cos \omega_{d}t+A_{2}\sin \omega_{d}t)+e^{-\alpha t}(-A_{1}\omega_{d} \sin \omega_{d} t+A_{2}\omega_{d} \cos \omega_{d} t)-\omega B_{1}\sin \omega t+B_{2}\omega \cos \omega t$$
Initial Values : $I'(0)=0$
$$\begin{eqnarray}
0&=&-\alpha A_{1}+A_{2}\omega_{d}+\omega B_{2}\\ &=&\alpha B_{1}+A_{2}\omega_{d}+\omega B_{2}\\ A_{2}&=&\frac{-\alpha B_{1}-\omega B_{2}}{\omega_{d}}
\end{eqnarray}$$

>[!success] Equation of current (I)
>$$\therefore I=e^{ -\alpha t }\left[ -B_{1}\cos \omega_{d} t-\left( \frac{\alpha B_{1}+\omega B_{2}}{\omega_{d}} \right) \sin \omega_{d}t\right]+B_{1}\cos \omega t+B_{2}\sin \omega t$$ where
>$D_{1}=(\omega_{0}^{2}-\omega^{2})^{2}-(2\alpha \omega)^{2}$
>$B_{1}=\frac{F_{0}(\omega_{0}^{2}-\omega^{2})}{D_{1}}$
>$B_{2}=\frac{F_{0}(2\alpha \omega)}{D_{1}}$

---
The second-order differential equation of current for an AC-driven RLC circuit is,
$$\begin{eqnarray}
Q''+ \frac{R}{L}Q'+\frac{1}{LC}Q=\frac{V_{0}}{L} \sin \omega t
\end{eqnarray}$$
$\text{let } \alpha=\frac{R}{2L}, \quad\omega_{0}=\frac{1}{\sqrt{LC}}, \quad F_{0}=\frac{V{0}}{L}\omega$
$$\boxed{Q''+2\alpha Q'+\omega_{0}^{2}Q=\frac{F_{0}}{\omega}\sin \omega t}$$
**Complimentary Solution :** $$Q_{c}=e^{ -\alpha t}(R_{1}\cos \omega_{d} t+R_{2}\sin \omega_{d} t)$$ where $\omega_{d}=\sqrt{\omega_{0}^{2}-\alpha^{2}}$

**Particular Solution :** $$Q_{p}=S_{1}\cos \omega t+S_{2}\sin \omega t$$where
$D_{2}=(\omega_{0}^{2}-\omega^{2})^{2}+(2\alpha \omega)^{2}$
$S_{1}=-\frac{F_{0}(2\alpha \omega)}{D_{2}}$
$S_{2}=\frac{F_{0}(\omega_{0}^{2}-\omega^{2})}{D_{2}\omega}$
$$\boxed{\therefore Q=e^{ -\alpha t }\left[ S_{1}\cos \omega_{d} t+\left( \frac{\alpha S_{1}-\omega S_{2}}{\omega_{d}} \right) \sin \omega_{d}t\right]+S_{1}\cos \omega t+S_{2}\sin \omega t}$$
