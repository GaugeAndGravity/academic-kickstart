---
title: 圈量子引力1.3
summary: Palatini 作用量
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

### 1.3 Palatini 作用量和 Holst 作用量

Palatini作用量是 Hilbert 作用量的改写，在流形上引入标架来替代度规。<sup>[[1](#ref-Baez1994),[2](#ref-Ashtekar2004)]</sup>

设 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\left(V,\eta_{IJ}^{\phantom{I}}\right)"> 是一个带有选定洛伦兹度规的四维矢量空间，称为内部空间（internal space），其中 $I,J,\cdots$ 是 $V$ 上的抽象指标，以与 $M$ 上的区分。我们考虑 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\mathrm{T}\!{M}"> 的平凡化，设有矢量丛同构 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=e\colon%20M\times%20V\rightarrow\mathrm{T}_{x}{M}">，$e(x) := e(x,\cdot)$ 是从 $V$ 到 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\mathrm{T}_{x}{M}"> 的线性同构。按照抽象指标记号，将它记为 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=e^{a}_{\phantom{a}I}(x)">，称为 $M$ 上的标架场（frame field，4维情况又特别地称为tetrads）。逐点取逆得到丛同构 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=e^{-1}\colon\mathrm{T}\!{M}\rightarrow%20M\times%20V">，$e^{-1}(x) := e^{-1}(x,\cdot)$ 按照抽象指标记号写为 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=e^{I}_{\phantom{I}a}(x)">，称为对偶标架场，则有
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=e^{a}_{\phantom{a}I} e^I_{\phantom{I}b} = \delta^a_{\phantom{a}b} ,\quad e^{I}_{\phantom{I}a} e^{a}_{\phantom{a}J} = \delta^{I}_{\phantom{I}J}.\\\\">
若满足
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=g_{ab}^{\phantom{a}} = \eta_{IJ}^{\phantom{a}} e^{I}_{\phantom{I}a} e^J_{\phantom{J}b},\\\\">
则称标架场是正交归一的。

我们可以选择 $V$ 上的基底 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\left\{ \xi^I_{\phantom{I}\mu} \right\}"> 及其对偶基 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\left\{ \xi^\mu_{\phantom{\mu}I} \right\}">，其中 $\mu=0,1,2,3$，使得 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\eta_{IJ}^{\phantom{a}} := \eta_{\mu\nu}^{\phantom{a}} \xi^\mu_{\phantom{\mu}I} {\xi}^\nu_{\phantom{\nu}J} = -\xi^0_{\phantom{0}I} \xi^0_{\phantom{0}J} %2B \sum_i \xi^i_{\phantom{i}I} \xi^i_{\phantom{i}J}">，其中 $i=1,2,3$，并定义
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=e^{a}_{\phantom{a}\mu} := \xi^I_{\phantom{I}\mu} e^{a}_{\phantom{a}I},\\\\">
则 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\left\{ e^{a}_{\phantom{a}\mu} \right\}"> 构成 $M$ 上每点的正交基底。

正交归一标架丛 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\mathrm{F}\!{M}"> 上的联络等价于其伴丛上的联络。将 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\xi^I_{\phantom{I}\mu}"> 视为 $\mathrm{SO}(3,1)$ 矢量丛 $E = M \times V$ 上截面的基底，将任意截面展开为 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=v^I = v^\mu \xi^I_{\phantom{I}\mu}">，定义标准平直联络
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=\partial_{a}^{\phantom{a}} v^I := \left( \partial_{a}^{\phantom{a}} v^\mu \right) \xi^I_{\phantom{I}\mu},\\\\">
任何联络（或称协变导数）可表为
<img class=displaymath id="eq-spin_connection" style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=\nabla_{a}^{\phantom{a}}v^I = \partial_{a}^{\phantom{a}} v^I %2B \omega_{a\phantom{I}J}^{\phantom{a}I} v^J,\tag{1}\\\\">
其中 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\omega_{a\phantom{I}J}^{\phantom{a}I}"> 是 $\mathrm{so}(3,1)$ 值一形式，称为 spin connection。设 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\mathrm{T}\!{M}"> 上的联络为
<img class=displaymath id="eq-ChristoffelSymbol" style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=\nabla_{a}^{\phantom{a}} v^b = \partial_{a}^{\phantom{a}} v^b %2B \Gamma^b_{\phantom{b}ac} v^c,\tag{2}\\\\">
<img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=e^{I}_{\phantom{I}a}"> 可视为 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=E \otimes \mathrm{T}^*\!{M}"> 上的截面，规定取坐标基底和截面基底 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\xi^I_{\phantom{I}\mu}"> 下分量定义偏导算符，而协变导数通过满足莱布尼兹律的方式推广到各种张量积丛，有
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=\nabla_{a} v^I = e^I_{\phantom{I}b} \nabla_{a} v^b %2B v^b \nabla_{a} e^I_{\phantom{I}b},\\\\">
由 [(1)](#eq-spin_connection),[(2)](#eq-ChristoffelSymbol) 可得
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=\nabla_{a}^{\phantom{a}} e^I_{\phantom{I}b} = \partial_{a}^{\phantom{a}} e^I_{\phantom{I}b} - \Gamma^c_{\phantom{c}ab} e^I_{\phantom{I}c} %2B \omega_{a\phantom{I}J}^{\phantom{a}I} e^J_{\phantom{J}b}.\\\\">
对矢量值一形式 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=v^I_{\phantom{I}a}">，定义外微分
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=\mathrm{d}_a^{\phantom{a}} {v^I_{\phantom{I}b}} := 2 \partial_{{[a}}^{\phantom{a}} v^I_{\phantom{I}b]} \equiv \xi^I_{\phantom{I}\mu} \mathrm{d}_a^{\phantom{a}} {v^\mu_{\phantom{\mu}b}},\\\\">
以及协变外微分
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=D_a^{\phantom{a}}v^I_{\phantom{I}b}:=2\nabla_{{[a}}^{\phantom{a}}v^I_{\phantom{I}b]}\equiv\mathrm{d}_a^{\phantom{a}}v^I_{\phantom{I}a}%2B%20\omega_{a\phantom{I}J}^{\phantom{a}I}\wedge v^J_{\phantom{J}b},\\\\">
其中 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\omega_{a\phantom{I}J}^{\phantom{a}I}\wedge%20v^J_{\phantom{J}b} := 2 \omega_{[a\phantom{I}|J|}^{\phantom{[a}I} v^J_{\phantom{J}b]}">。定义挠率形式为
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=T^I_{\phantom{I}ab} := D_a^{\phantom{a}} e^I_{\phantom{I}b} = \mathrm{d}_a^{\phantom{a}} e^I_{\phantom{I}b} %2B \omega_{a\phantom{I}J}^{\phantom{a}I} \wedge e^J_{\phantom{J}b},\\\\">
及曲率二形式
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=F_{abI}^{\phantom{abI}J} := 2D_{[a}^{\phantom{a}} \omega_{b]I}^{\phantom{b]I}J} = \mathrm{d}_a^{\phantom{a}} \omega_{bI}^{\phantom{bI}J} %2B \omega_{aI}^{\phantom{aI}K} \wedge \omega_{bJ}^{\phantom{bJ}K}.\\\\">

定义 Palatini作用量
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=S_{\text{Palatini}}[e,\omega] := \frac{1}{4\kappa} \int_M \varepsilon_{IJKL}^{\phantom{a}} e^{I}_{\phantom{I}a} \wedge e^J_{\phantom{J}b} \wedge {F}_{cd}^{\phantom{cd}KL},\\\\">
其中 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\varepsilon_{IJKL}^{\phantom{a}}"> 是 $V$ 上与 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\eta_{IJ}^{\phantom{a}}"> 适配的体元。对 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\omega_{a\phantom{I}J}^{\phantom{a}I}"> 变分可得
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=D_a^{\phantom{a}}e^I_{\phantom{I}b}=0,\\\\">
此运动方程即要求联络无挠，此条件由 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=e^{I}_{\phantom{I}a}"> 唯一确定了相容联络 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\omega_{a\phantom{I}J}^{\phantom{a}I}">。当无挠条件满足时，容易验证 Palatini 作用量变回 Hilbert-Einstein 作用量
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=S_{\text{Palatini}}[e,\omega(e)] = \frac{1}{2\kappa}\int_M R[e],\\\\">
其中
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=R[e] = R[g(e)] = F_{ab}^{\phantom{ab}IJ} e^{a}_{\phantom{a}I} e^b_{\phantom{b}J},\\\\">
故无需详细计算即知对 $e$ 变分可得 Einstein 场方程。

注意到 Palatini 作用量引入了一个 $\mathrm{SO}(3,1)$ 局域规范对称性
<img class=displaymath style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=\left( e^{I}_{\phantom{I}a}, \omega_{a\phantom{I}J}^{\phantom{a}I} \right) \mapsto \left( \Lambda_J^{\phantom{J}I} e^J_{\phantom{J}a}, \Lambda_K^{\phantom{K}I} \omega_{a\phantom{K}L}^{\phantom{a}K} \Lambda^L_{\phantom{L}J} %2B \Lambda_K^{\phantom{K}I} \mathrm{d}_a^{\phantom{a}} \Lambda_K^{\phantom{K}J} \right),\\\\">
或更紧凑地写为
$$
(e,\omega) \mapsto \left( \Lambda^{-1} e, \Lambda^{-1} \omega \Lambda + \Lambda^{-1} \,\mathrm{d}{\Lambda} \right),
$$
这引入一个第二类约束。

在圈量子引力中十分重要的是 Palatini 作用量的 Holst 修正
<img class=displaymath id="eq-Holst_action" style="margin-top:0.7em;margin-bottom:0" src="https://www.zhihu.com/equation?tex=\begin{aligned}S_{\text{Holst}}%26:=S_{\text{Palatini}} - \frac{1}{2\kappa} \int_M \frac{1}{\beta} e^{I}_{\phantom{I}a} \wedge e^J_{\phantom{J}b} \wedge F_{cdIJ}^{\phantom{a}}\\%26= - \frac{1}{2\kappa} \int_M \,\mathrm{tr}\left[\left( *\left( e \wedge e \right) %2B \frac{1}{\beta} \left( e \wedge e \right) \right) \wedge F\right],\end{aligned}\\\\">
容易验证后一项是拓扑项，不改变运动方程。$\beta$ 称为 Barbero-Immiriz 参数。

## 参考文献

- <div id="ref-Baez1994">[1] Baez J, Muniain J P. Series on knots and everything: Gauge fields, knots and gravity. Singapore: World Scientific, 1994. <a url="https://www.worldscientific.com/doi/abs/10.1142/2324">https://www.worldscientific.com/doi/abs/10.1142/2324</a>.</div>
- <div id="ref-Ashtekar2004">[2] Ashtekar A, Lewandowski J. Background Independent Quantum Gravity: A Status Report. <i>Class. Quant. Grav.</i>, 2004, 21:R53. DOI: <a url="http://doi.org/10.1088/0264­9381/21/15/R01">10.1088/0264­9381/21/15/R01</a>.</div>
