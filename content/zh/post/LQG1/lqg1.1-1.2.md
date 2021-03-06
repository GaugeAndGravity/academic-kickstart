---
title: 圈量子引力1.1-1.2
summary: ADM形式
tags:
- lqg
date: "2019-08-21T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

# image:
#   caption: by大喵
#   focal_point: Smart

links:
#- icon: twitter
#  icon_pack: fab
#  name: Follow
#  url: https://twitter.com/georgecushen
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

share: false
profile: false

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

## Chapter-1 正则引力

本章是圈量子系列笔记的第一章，介绍正则引力理论。

### 1.1 ADM 形式

为了研究时间演化及对引力进行量子化，我们需要考虑广义相对论的哈密顿描述。我们主要依照文献 [[1](#ref-wald1989),[2](#ref-liang3),[3](#ref-Thiemann2007)] 展开。在拉格朗日描述下，考虑 $n$ 维光滑可定向流形 $M$ ，记 $M$ 上的洛伦兹度规的集合为 $\mathrm{Lor}(M)$， 由于微分同胚不变性的规范对称性，广义相对论的位型空间为 ${\mathcal{S}(M)} := {\mathrm{Lor}(M)}/{\mathrm{Diff}(M)}$。理论的拉氏量为
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=\mathbf{\mathscr{L}}_{\text{EH}}[j^2 g] := \frac{1}{2\kappa} \mathcal{R}(j^2 g) \mathbf{\varepsilon},\\\\">
其中 $\kappa = 8\pi \mathrm{G}$ 是耦合常数，$j^2 g$ 是场 $g$ 的 2-jet，$\mathcal{R}[j^2 g]$ 是标量曲率，$\mathbf{\varepsilon}$ 是与 $g$ 适配的体元。也可采用标量密度 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\tilde{\mathscr{L}}_{\text{EH}}"> 表示，
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=\mathbf{\mathscr{L}}_{\text{EH}}[j^2 g] = \tilde{\mathscr{L}}_{\text{EH}} \mathbf{\epsilon},\\ \tilde{\mathscr{L}}_{\text{EH}} = \frac{1}{2\kappa} f \mathcal{R}(j^2 g),\\\\">
其中 $\mathbf{\epsilon}$ 是任意定向相容体元，$f$ 是满足 $\mathbf{\varepsilon} = f \mathbf{\epsilon}$ 的正函数。例如，在局部坐标系 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\left\{ x^\mu \right\}"> 下，若坐标系为右手系，即 $n$ 形式 $\,\mathrm{d}{x^1} \wedge \cdots \wedge \,\mathrm{d}{x^n}$ 与定向相容，则可取定 $\mathbf{\epsilon} = \,\mathrm{d}{x^1} \wedge \cdots \wedge \,\mathrm{d}{x^n}$，此时 $f=\sqrt{-\det g}$，其中 $\det g$ 指坐标系下 $ \left( g_{\mu\nu} \right) $ 的行列式。于是此时有

$$
\tilde{\mathscr{L}}_{\text{EH}} = \frac{1}{2\kappa} \sqrt{-\det g} \mathcal{R}(j^2 g).
$$

易证明，Einstein-Hilbert 作用量

$$ S_{\text{EH}}[g] = \frac{1}{2\kappa} \int_M \mathcal{R}[g] $$

的运动方程为真空 Einstein 方程

$$
Ric - \frac{1}{2} \mathcal{R} g = 0,
$$

或采取抽象指标形式，写作
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=R_{ab} - \frac{1}{2} \mathcal{R} g_{ab}^{\phantom{a}} = 0.\\\\">
以下张量全部采用抽象指标记号，改用 $g_{ab}^{\phantom{a}}$ 表示度规张量，而 $g$ 表示其行列式。

现在考虑哈密顿描述，这要求我们把时间从时空中分离出来。
设时空 $\left( M, g \right)$ 整体双曲，则对时空有拓扑上的要求： $M \cong \mathbb{R} \times {\mathcal{S}}$，其中 ${\mathcal{S}}$ 是 $3$ 维流形[<sup>[1]</sup>](#ref-wald1989)。设有微分同胚 $\phi \colon M \rightarrow \mathbb{R} \times {\mathcal{S}}$，称为一个分层（foliation）。注意到任取 $\psi \in {\mathrm{Diff}(M)}$，$\phi \circ \psi$ 依然是分层，分层的集合与 ${\mathrm{Diff}(M)}$ 一一对应。记
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex={\mathcal{S}}_t := \phi^{-1}(\left\{ t \right\} \times {\mathcal{S}}),\\\\">
这是类空超曲面，称为 $t$ 时刻的空间。记自然投影 $\pi \colon \mathbb{R} \times {\mathcal{S}} \rightarrow \mathbb{R}$, $\pi_{{\mathcal{S}}} \colon \mathbb{R} \times {\mathcal{S}} \rightarrow {\mathcal{S}}$，则有时间函数 $t := \pi \circ \phi \colon M \rightarrow \mathbb{R}$。此时 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex={\mathcal{S}}_t"> 就是等 $t$ 面。$\pi_{{\mathcal{S}}} \circ \phi$ 可以将 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\mathrm{T}\!{{\mathcal{S}}}"> 拖回到 $M$ 上，其元素称为空间矢量，截面称为空间矢量场；进而可以定义空间张量丛和空间张量场。[^1]另外，超曲面族 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\left\{ {\mathcal{S}}_t \right\}"> 还定义了法余矢丛，其中每个余矢量正比于该点的 $ \,\mathrm{d}{t} $。

[^1]: 我们之后不区分 ${\mathcal{S}}$ 上的张量和将它拖回到 $M$ 上得到的 $M$ 上的空间张量。

考虑 $g$ 的 $3+1$ 分解。我们记 $n_a$ 是单位法余矢场，即 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=n^a n_a = -1">，则可以验证
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=h_{ab} := g_{ab}^{\phantom{a}} %2B n_a n_b\\\\">
是空间对称张量，且它是 $g$ 在 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\mathrm{T}\!{{\mathcal{S}}_t}"> 上的限制，我们称其为 $g$ 所诱导的空间度规，这是我们引入的第一个空间量。再考虑“时间部分”，我们引入矢量场
$$
t^a := \left( \pi \circ \phi \right)^* \left( \frac{\partial}{\partial t} \right)^a,
$$
其中 $\left( \partial/\partial t \right)^a$ 是 $\mathbb{R}$ 中的自然坐标基矢场。则有
<img class=displaymath id="eqt" style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=t^a \nabla_{a} t = -1,\tag{1}">
$t^a$ 的积分曲线汇（作为观测者世界线）标志了在微分同胚 $\phi$ 下不同时空点如何“对齐”为“同一空间点”，它们定义了一个参考系。在每点 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=p\in {\mathcal{S}}_t"> 作直和分解
<img class=displaymath id="eqtsplit" style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=t^a=Nn^a%2BN^a,\quad%20N%3E0,\quad%20n^a\in\mathrm{T}_p{{\mathcal{S}}_t},\tag{2}\\\\" alt="t^a=Nn^a+N^a"/>
称 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=N"/> 为时移函数（lapse function），<img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=N^a"> 为位移矢量（shift vector）场，这是我们引入的第2、3个空间量。由 [(1)](#eqt) 容易算得
<img class=displaymath id="eqn" style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=n_a = - N \nabla_{a} t.\\\\">

现在我们来说明，给定 $\phi$，即有了 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\left\{ {\mathcal{S}}_t \right\}">、$t$ 和 $t^a$ 的条件下，空间量 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\left( h_{ab} , N, n_a \right)"> 和 时空量 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=g_{ab}^{\phantom{a}}"> 互相确定，因而 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\left( h_{ab} , N, n_a \right)"> 可以作为位型变量。由 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=g_{ab}^{\phantom{a}}"> 给出 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\left( h_{ab} , N, n_a \right)"> 的过程已经在上面写出，而给定 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\left( h_{ab} , N, n_a \right)"> 后，首先将空间张量 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=h_{ab}"> 视作 ${\mathcal{S}}$ 上的度量张量，取逆再拖回到 $M$ 上得空间张量 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=h_{ab}">。由 [(2)](#eqtsplit) 知
$$
n^a = \frac{1}{N} \left( t^a - n^a \right),
$$
其中 $n^a = h^{ab} n_b$ 。则
$$
g^{ab} = -n^a n^b + h^{ab} = - \frac{1}{N^2} \left( t^a - n^a \right) \left( t^b - n^b \right) + h^{ab}.
$$

描述每张超曲面 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex={\mathcal{S}}_t"> 的除了描述内蕴几何的 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=h_{ab}"> 之外还有描述它如何嵌入 $M$ 的外曲率 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=K_{ab}">，定义为
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=t^a = K_{ab} := h_{a}^{\phantom{a}c} \nabla_{c} n_b,\\\\">
我们即将看到它与 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=h_{ab}"> 的共轭动量的联系。这从以下命题即可初见端倪：

<div class="property">
<div class="property-title">命题</div>
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=K_{ab} = \frac{1}{2} \mathcal{L}_{n} h_{ab},\\\\">
其中 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\mathcal{L}_{n}"> 表示沿 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=n^a"> 的李导数。
</div>

这里略去证明，可参见[[1](#ref-wald1989),[2](#ref-liang3),[3](#ref-Thiemann2007)] 等任何相关教材。

还需定义空间量的时间导数，沿 $t^a$ 的李导数是好的候选者，但空间张量的李导数未必还是空间张量，为此定义 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\tilde{\mathcal{L}}_{v} T^{a\cdots}_{\phantom{a\cdots}b\cdots}"> 为 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\mathcal{L}_{v} T^{a\cdots}_{\phantom{a\cdots}b\cdots}"> 的空间投影，即
<img class=displaymath id="eq-spaceLd" style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=\tilde{\mathcal{L}}_{v} T^{a_1\cdots a_k}_{\phantom{a_1 \cdots a_k}b_1 \cdots b_l} := {h}^{a_1}_{\phantom{a_1}c_1} \cdots {h}^{a_k}_{\phantom{a_1}c_k} {h}^{d_1}_{\phantom{d_1}b_1} \cdots {h}^{d_l}_{\phantom{d_l}b_l} \mathcal{L}_{v} {T}^{c_1 \cdots c_k}_{\phantom{c_1 \cdots c_k}d_1 \cdots d_l},\\\\">
然后即可定义
<img class=displaymath id="eq-timedot" style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex={\dot{T}}^{a_1 \cdots a_k}_{\phantom{a_1 \cdots a_k}b_1 \cdots b_l} := \tilde{\mathcal{L}}_{t} T^{a_1\cdots a_k}_{\phantom{a_1 \cdots a_k}b_1 \cdots b_l} = N \tilde{\mathcal{L}}_{n} T^{a_1\cdots a_k}_{\phantom{a_1 \cdots a_k}b_1 \cdots b_l} %2B \tilde{\mathcal{L}}_{N} T^{a_1\cdots a_k}_{\phantom{a_1 \cdots a_k}b_1 \cdots b_l},\\\\">
则得到
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=\dot{h}_{ab} = 2N K_{ab} %2B 2 D_{{(a}} {N}_{b)},\\\\">
其中 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=D_{a}"> 是 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex={\mathcal{S}}_t"> 上与 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=h_{ab}"> 相容的联络。

现在，我们把 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\tilde{\mathscr{L}}_{\text{EH}} = \frac{1}{2\kappa} \sqrt{- \det g} \mathcal{R}"> 用空间量表示。需要借助 Gauss 方程
<img class=displaymath id="eq-gauss" style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=\mathcal{R}_{abc}^{\phantom{abc}d} = {h}_a^{\phantom{a}k} {h}_b^{\phantom{b}l} {h}_c^{\phantom{c}m} {h}_n^{\phantom{n}d} \mathcal{R}_{klm}^{\phantom{klm}n} - 2 {K}{_{c[a}} {K}_{b]}^{\phantom{b]}d},\\\\">
其中 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\mathcal{R}_{abc}^{\phantom{abc}d}"> 是3维流形 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex={\mathcal{S}}_t"> 上空间度规 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=h_{ab}"> 对应的曲率；<img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex={T}_{[\cdots]}"> 表示对张量 $T$ 反称化。略去所有计算过程，我们得到
<img class=displaymath id="eq-L_split" style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=\tilde{\mathscr{L}} = \frac{1}{2\kappa} \sqrt{h} N \left( \mathcal{R} - K^2 %2B K_{ab} {K}^{ab} \right),\tag{3}">
其中 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=h"> 是 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=h_{ab}"> 的分量矩阵的行列式， <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\mathcal{R}"> 是 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\mathcal{S}_t"> 上的标量曲率，由 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=h_{ab}"> 及其二阶空间导数确定，而 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=K_{ab}"> 通过
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=K_{ab} = \frac{1}{2N} \left( {\dot{h}}_{ab} - 2 {D}_{(a} {N}_{b)} \right)\\\\">
由 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex={\dot{h}}_{ab}, N, n_a, D_{a}"> 决定，并有 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=K = h^{ab} K_{ab}">。这说明 [3](#eq-L_split) 的确是位型变量 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\left( h_{ab} , N, n_a \right)"> 及其时间导数及空间导数的函数。可求得共轭动量
<img class=displaymath id="eq-constrain12" style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=\pi_N=\frac{\partial\tilde{\mathscr{L}}}{\partial\dot{N}}=0,\quad\pi^a=\frac{\partial\tilde{\mathscr{L}}}{\partial\dot{N}_a}=0,\tag{4}%20\\%20\pi^{ab} = \frac{\partial\tilde{\mathscr{L}}}{\partial {\dot{h}}_{ab}} = \frac{1}{2\kappa} \sqrt{h} \left( K^{ab} - K h^{ab} \right),\\\\">
其中 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\pi_{N}">, $\pi^a$, $\pi^{ab}$ 分别是与 $N$, <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=n_a">, <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=h_{ab}"> 共轭的动量。[(4)](#eq-constrain12) 给出两个初级约束。去掉一些边界项后，有哈密顿量
<img class=displaymath id="eq-ADM_H" style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=H[N,n_a, h_{ab}, \pi^{ab}] = \frac{1}{2\kappa} \int_{{\mathcal{S}}} \,\mathrm{d}^3{x} \left( N C %2B n_a V^a \right),\\\\">
其中
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=C := - \frac{\sqrt{h}}{2\kappa} \mathcal{R} %2B \frac{2\kappa}{\sqrt{h}} \left( \pi_{ab} \pi^{ab} - \frac{1}{2} \pi^2 \right),\\V^a := -2 D_{b} \pi^{ab}.\\\\">
对 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=N">，<img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=n_a"> 变分给出两个次级约束，称为标量约束和矢量约束
<img class=displaymath id="eq-constrain34" style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=C = 0 ,\quad V^a = 0,\tag{5}\\\\">
可以证明 [(4)](#eq-constrain12), [(5)](#eq-constrain34) 已经穷尽了所有约束。

定义smeared 约束
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=C(f) := \int_{{\mathcal{S}}} \,\mathrm{d}^3{x} C f  ,\quad V ({v}) := \int_{{\mathcal{S}}} \,\mathrm{d}^3{x} V_a v^a,\\\\">
其中 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=f\in C^\infty({\mathcal{S}}), v\in \Gamma(\mathrm{T}\!{{\mathcal{S}}})"> 满足适当的边界条件，可以算得泊松括号
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=\begin{align}\left\{V({u}),V({v})\right\}%26=2\kappa%20V(\mathcal{L}_{{u}}%20{v}),\\%20\left\{V({v}),C(f)\right\}%26=2\kappa%20C(v(f)),\\%20\left\{C(f),C(f')\right\}%26=2\kappa%20V(fD^af'-f'D^af),\end{align}\\\\">
又因
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=H = \frac{1}{2\kappa} \left( C(N) %2B V(\mathbf{N}) \right),\\\\">
知 $H,C,V$ 两两泊松括号弱等于零（在约束面上为零），并且是约束的线性组合，故 ADM 形式的广义相对论是第一类约束系统。

### 1.2 Quantum Geometrodynamics(QGD)

接下来对上一节得到的广义相对论的哈密顿表述进行正则量子化，得到量子几何动力学（Quantum Geometrodynamics）。但由于体现规范对称性的两个第一类约束的存在，我们需要先介绍这样的约束系统的量子化方法。

第一类约束哈密顿系统的量子化最早由狄拉克发展\cite{dirac2001lectures}，其核心是先连同规范自由度一起量子化得到 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\mathcal{H}_{\text{kin}}">，然后将经典约束方程 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\{ C_I = 0 \}_{I \in \mathcal{I}}"> 变为物理状态应满足的方程 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\left\{ \hat{C}_I \left|\psi\right\rangle = 0 \right\}_{I \in \mathcal{I}}">，即定义物理态空间 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\mathcal{H}_{\text{phy}}"> 是所有 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\mathrm{ker}\, \hat{C}_I"> 之交。

对于 ADM 形式的广义相对论来说，$N$ 和 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=N_a"> 只是拉氏乘子，位型变量为 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=h_{ab}">，即空间几何的动力学。可选择 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\mathcal{H}_{\text{kin}}"> 为某种 “<img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=L^2(\mathrm{Riem}{\mathcal{S}})">”，其中 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\mathrm{Riem}{\mathcal{S}}"> 表示 $\mathcal{S}$ 上黎曼度规的集合，并采用标准的 Schrödinger 表示
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=\begin{align}\hat{h}_{ab} \left|\psi\right\rangle %26\leftrightarrow h_{ab} \psi(h),\\%20\hat{\pi}^{ab} \left|\psi\right\rangle %26 \leftrightarrow - \mathrm{i} \hbar \frac{\delta}{\delta%20h_{ab}} \psi(h).\end{align}\\\\">
$V^a \left|\psi\right\rangle =0$ 定义了空间微分同胚不变的态空间 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\mathcal{H}_{\text{Diff}}">，再通过哈密顿约束
<img class=displaymath id="eq-WDeq" style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=\hat{C} \left|\psi\right\rangle =0\tag{6}\\\\">
得到物理态空间。这便是量子几何动力学，方程 [(6)](#eq-WDeq) 即为著名的 Wheeler DeWitt 方程。

但这一方法存在很多问题，例如一开始 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\mathcal{H}_{\text{kin}}"> 就难以定义；在标准 Schrödinger 表示下 $\hat{C}$ 是否是定义良好的算符也不清楚。当经典层面已经有了高度对称性约化，例如宇宙学的情况下，才能很好地使用 Wheeler DeWitt 方程。

## 参考文献

- <div id="ref-wald1989">[1] Wald R M. General relativity. Chicago: The University of Chicago Press, 1989.</div>
- <div id="ref-liang3">[2] 梁灿彬. 微分几何入门与广义相对论: 下册. 2 版. 北京: 科学出版社, 2009.</div>
- <div id="ref-Thiemann2007">[3] Thiemann T. Cambridge monographs on mathematical physics: Modern Canoni­cal Quantum General Relativity. Cambridge: Cambridge University Press, 2007. DOI: <a href="http://doi.org/10.1017/CBO9780511755682">10.1017/CBO9780511755682</a>.</div>
- <div id="ref-Thiemann2007">[4] P.A.M.Dirac. Belfer graduate school of science, monograph series: Lectures on quantum mechanics. Dover Publications, 2001. <a href="https://books.google.com.hk/books?id=GVwzb1rZW9kC">https://books.google.com.hk/books?id=GVwzb1rZW9kC</a>.</div>
