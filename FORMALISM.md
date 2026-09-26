# Formalism

## 1. Observer-world recursion

\[
\begin{aligned}
o_t &= O(x_t,a_{t-1})+\epsilon_t,\\
m_t &= M(m_{t-1},o_t),\\
h_t &= \Pi(h_{t-1},o_t,m_t),\\
a_t &= \pi(h_t,m_t),\\
x_{t+1} &= F(x_t,a_t,\eta_t).
\end{aligned}
\]

## 2. Coherence vector

\[
\mathbf C_t=(C_s,C_\tau,C_o,C_m,C_c)_t\in[0,1]^5.
\]

\[
D_t=1-\mathbf w^\top\mathbf C_t,
\qquad \mathbf w\ge0,
\qquad \mathbf 1^\top\mathbf w=1.
\]

## 3. Surprise and model revision

\[
I_t=-\log p(o_t\mid h_{t-1}).
\]

\[
I_t>\theta_I\Rightarrow
p_t(h)=\frac{p(o_t\mid h)p_{t-1}(h)}{\sum_{h'}p(o_t\mid h')p_{t-1}(h')}.
\]

## 4. Anti-premature-coherence rule

\[
\Gamma_t=
\frac{p_t(h_{(1)})}{p_t(h_{(2)})}.
\]

\[
\Gamma_t<\theta_\Gamma
\Rightarrow
\operatorname{output}=\text{UNCERTAIN/VERIFY}.
\]

## 5. Invariant search

\[
\mathcal I_\varepsilon=
\{q:\sup_{g\in G}\mathbb E\|q(gx)-q(x)\|\le\varepsilon\}.
\]

## 6. Narrative Backrooms criterion

For interval \([a,b]\):

\[
B_{a:b}=\frac{1}{b-a+1}\sum_{t=a}^{b}D_t.
\]

\[
B_{a:b}>\theta_B
\land
\frac1{b-a}\sum_{t=a+1}^{b}d(h_t,h_{t-1})>\theta_R
\Rightarrow
\operatorname{BACKROOMS}(a,b)=1.
\]
