$$\begin{aligned}
              &\int_\Omega u_{tt}(h(x)\cdot \nabla u){\mathop{}\!\mathrm{d}} x\\
               =&\frac{{\mathop{}\!\mathrm{d}}}{{\mathop{}\!\mathrm{d}} t}\int_\Omega u_t(h(x)\cdot \nabla u){\mathop{}\!\mathrm{d}} x-\int_\Omega u_t (h(x)\cdot \nabla u){\mathop{}\!\mathrm{d}} x\\
                =&\frac{{\mathop{}\!\mathrm{d}}}{{\mathop{}\!\mathrm{d}} t}\int_\Omega u_t(h(x)\cdot \nabla u){\mathop{}\!\mathrm{d}} x-\frac12 \int_\Omega h(x)\cdot \nabla |u_t|^2 {\mathop{}\!\mathrm{d}} x.
              \end{aligned}$$
              由于$\int_a^b f(x) {\mathop{}\!\mathrm{d}} x=F(b)-F(a)$, 于是
              $$\begin{aligned}
              &\int_\Omega h(x)\cdot \nabla |u_t|^2{\mathop{}\!\mathrm{d}} x=\sum_i^N\int_\Omega h_i\frac{\partial}{\partial x_i}|u_t|^2 {\mathop{}\!\mathrm{d}} x\\
              =&\sum_i^N\int_{\partial\Omega}h_i |u_t|^2 \nu_i{\mathop{}\!\mathrm{d}} S-\sum_i^N\int_\Omega |u_t|^2 \frac{\partial h_i}{\partial x_i}{\mathop{}\!\mathrm{d}} x\\
              =&0-\int_\Omega (\nabla \cdot h)|u_t|^2 {\mathop{}\!\mathrm{d}} x,
              \end{aligned}$$
              所以最终有
              $$\begin{aligned}
              &\int_\Omega u_{tt}(h(x)\cdot \nabla u){\mathop{}\!\mathrm{d}} x\\
              =&\frac{{\mathop{}\!\mathrm{d}}}{{\mathop{}\!\mathrm{d}} t}\int_\Omega u_t(h(x)\cdot \nabla u){\mathop{}\!\mathrm{d}} x+\frac12 \int_\Omega (\nabla \cdot h)|u_t|^2 {\mathop{}\!\mathrm{d}} x.
              \end{aligned}$$

由于在$\partial \Omega$ 上$u=0$, 所以$\frac{\partial u}{\partial x_i}=\frac{\partial u}{\partial \nu}\nu_i$, 即
    $$\nabla u=\frac{\partial u}{\partial \nu}\nu\quad \textrm{并且}\quad |\nabla u|^2=\left|\frac{\partial u}{\partial \nu}\right|^2.$$
    一方面,
    $$\begin{aligned}
    A_1&=-\int_{\partial \Omega}(h(x)\cdot \nabla u)(\nabla u\cdot \nu ){\mathop{}\!\mathrm{d}} S\\
    &=-\int_{\partial \Omega}\left(h(x)\cdot \frac{\partial u}{\partial \nu}\nu\right)\frac{\partial u}{\partial \nu}{\mathop{}\!\mathrm{d}} S\\
    &=-\int_{\partial \Omega}\left|\frac{\partial u}{\partial \nu}\right|^2(h(x)\cdot \nu){\mathop{}\!\mathrm{d}} S.
    \end{aligned}$$
    另一方面, 
    $$\begin{aligned}
    A_2&=\int_\Omega \nabla u\cdot \nabla (h(x)\cdot \nabla u){\mathop{}\!\mathrm{d}} x\\
    &=\sum_i^N\sum_j^N \int_\Omega \frac{\partial u}{\partial x_i}\frac{\partial}{\partial x_i}\left(h_j\frac{\partial u}{\partial x_j}\right){\mathop{}\!\mathrm{d}} x\\
    &=\sum_i^N\sum_j^N \int_\Omega \left[\frac{\partial u}{\partial x_i}\frac{\partial h_j}{\partial x_i}\frac{\partial u}{\partial x_j}+\frac{\partial u}{\partial x_i}\frac{\partial}{\partial x_j}\left(\frac{\partial u}{\partial x_i}\right)h_j\right]{\mathop{}\!\mathrm{d}} x\\
    &=\sum_i^N\sum_j^N \left(\int_\Omega \frac{\partial u}{\partial x_i}\frac{\partial h_j}{\partial x_i}\frac{\partial u}{\partial x_j} {\mathop{}\!\mathrm{d}} x +\frac12 \int_\Omega h_j \frac{\partial}{\partial x_j}\left(\left|\frac{\partial u}{\partial x_i}\right|^2\right){\mathop{}\!\mathrm{d}} x \right)\\
    &=\sum_i^N\sum_j^N \int_\Omega \frac{\partial u}{\partial x_i}\frac{\partial h_j}{\partial x_i}\frac{\partial u}{\partial x_j} {\mathop{}\!\mathrm{d}} x+\frac12 \int_\Omega h\cdot \nabla (|\nabla u|^2){\mathop{}\!\mathrm{d}} x\\
    &=\sum_i^N\sum_j^N \int_\Omega \frac{\partial u}{\partial x_i}\frac{\partial h_j}{\partial x_i}\frac{\partial u}{\partial x_j} {\mathop{}\!\mathrm{d}} x +\frac12 \int_{\partial\Omega}\left|\frac{\partial u}{\partial \nu}\right|^2(h(x)\cdot \nu){\mathop{}\!\mathrm{d}} S \\
    &-\frac12 \int_\Omega |\nabla u|^2(\nabla \cdot h){\mathop{}\!\mathrm{d}} x.
    \end{aligned}$$
    所以
    $$\begin{aligned}
    &-\int_\Omega {\mathop{}\!\mathrm{d}} u(h(x)\cdot \nabla u){\mathop{}\!\mathrm{d}} x\\
    =&-\frac12 \int_\Omega (\nabla \cdot h)|\nabla u|^2{\mathop{}\!\mathrm{d}} x-\frac12 \int_{\partial\Omega}\left|\frac{\partial u}{\partial \nu}\right|^2(h(x)\cdot \nu){\mathop{}\!\mathrm{d}} S+\sum_{i,j}^N u_{x_i}u_{x_j}\frac{\partial}{\partial x_i}h_j(x){\mathop{}\!\mathrm{d}} x.
    \end{aligned}$$