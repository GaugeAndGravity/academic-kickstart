---
title: 圈量子引力1.4
summary: Ashtekar 联络
tags:
- lqg
date: "2020-05-28T00:00:00Z"

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

本文由 $\LaTeX$ 源码粘贴，尚未完成格式化，因此公式暂时都是乱的。

## Chapter-1 正则引力

本章是圈量子系列笔记的第一章，介绍正则引力理论。

### 1.1 -1.3

见前文。

### 1.4 Ashtekar 变量

Abhay Ashtekar 在1986年给出了广义相对论的一组新的正则变量\cite{Ashtekar1986,Ashtekar1987}，使约束表达式得到了大幅简化，便于考虑量子引力，后来成为了圈量子引力 的基础。以下参照 \inlinecite{Ashtekar2004} 予以简单介绍，相关内容也可参考\cite{liang3,Thiemann2007,Baez1994}。

从 Holst 作用量出发，我们考虑 $3+1$ 分解，其含义与之前 1.1 节中相同，即选择时空的分层 $\phi \colon M \rightarrow \mathbb{R} \times {\mathcal{S}}$，将物理量分解。每点的直和分解 <img class=inlinemath style="margin:0" src="https://www.zhihu.com/equation?tex=\mathrm{T}\\_{x}{M}=\operatorname{Span}\left\{n^a(x)\right\}\oplus\mathrm{T}_x{{\mathcal{S}}}"> 被 $\tensor{e}{^I_a}$ 映为 $V = \Span\left\{ \tensor{n}{^I}(x) \right\} \oplus V_{{\mathcal{S}}}(x)$，其中 $\tensor{n}{^I} = \tensor{e}{^I_a} \tensor{n}{^a}$。注意到法矢场 $\tensor{n}{^a}$ 仅与 $\phi$ 和 $\tensor{g}{_a_b}$ 有关，而同一个 $\tensor{g}{_a_b}$ 对应的 $\tensor{e}{^I_a}$ 还存在 $\SO{3,1}$ 规范自由度，为了方便可以部分固定规范，即固定内部矢量场 $\tensor{n}{^I}$，例如本文中取为第零基矢 $\tensor{\xi}{^I_0}$。则规范群约化为 $\SO{3}$ 。每点的 $V_{{\mathcal{S}}}$ 同构于一固定的三维线性空间 $W$，于是在标架 $\tensor{e}{^a_I}$ 将 $\TB{M}$ 平凡化为 $E=M\times V$ 后，时空的 $3+1$ 分解又将其（局部地）直和分解为 $\left( M \times \mathbb{R} \right) \oplus \left( M \times W \right)$。用 $i,j,k,\cdots$ 作为 $W$ 上的抽象指标，记 $\tensor{q}{^i_I}(x)$ 为 $V_{{\mathcal{S}}}$ 到 $W$ 的同构映射。记 $\tensor{h}{^I_J} = \tensor{\delta}{^I_J} + \tensor{n}{^I} \tensor{n}{_J}$ 为 $V$ 到 $V_{{\mathcal{S}}}$ 的投影映射，$\tensor{h}{_I_J} = \tensor{\eta}{_I_K} \tensor{h}{^K_J}$ 即 $V_{{\mathcal{S}}}$ 上的诱导黎曼度规，它等于 $\tensor{e}{^a_I} \tensor{e}{^b_J} \tensor{h}{_a_b}$。我们知道 $\tensor{\vol}{_a_b_c} \definedby \tensor{n}{^d} \tensor{\vol}{_d_a_b_c}$ 给出 ${\mathcal{S}}$ 上的诱导体元，其标架版本为 $\tensor{\vol}{_I_J_K} \definedby \tensor{n}{^L} \tensor{\vol}{_L_I_J_K}$。通过同构 $\tensor{q}{^i_I}$ 及其逆 $\tensor{q}{^I_i}$ 有 $\tensor{h}{^i_I} \definedby \tensor{q}{^i_J} \tensor{h}{^J_I}$ 及 $W$ 上的度规 $\tensor{h}{_i_j} \definedby \tensor{q}{^I_i} \tensor{q}{^J_j} \tensor{h}{_I_J}$ 与体元 $\tensor{\vol}{_i_j_k} \definedby \tensor{q}{^I_i} \tensor{q}{^J_j} \tensor{q}{^K_k} \tensor{\vol}{_I_J_K}$。

称 $\tensor{e}{^a_i} \definedby \tensor{h}{^a_b} \tensor{e}{^b_I} \tensor{q}{^I_i}$ 为空间标架。接下来分解 $\tensor{\omega}{_a^I^J}$，定义
\begin{equation}
\tensor{K}{^I_a} \definedby \tensor{h}{^b_a} \tensor{n}{_J} \tensor{\omega}{_b^I^J} \qc \tensor{K}{^i_a} \definedby \tensor{q}{^i_I} \tensor{K}{^I_a},
\end{equation}
及
\begin{equation}
\tensor{\omega}{^I_a} \definedby \tensor{h}{^b_a} \tensor{n}{_J} \tensor[^\star]{\omega}{_b^I^J} \qc \tensor{\omega}{^i_a} \definedby \tensor{q}{^i_I} \tensor{\omega}{^I_a},
\end{equation}
其中 $\star$ 是 $V$ 上的 Hodge 对偶，
\begin{equation}
\tensor[^\star]{\omega}{_a^I^J} = \frac{1}{2} \tensor{\vol}{^I^J^K^L} \tensor{\omega}{_a_K_L}.
\end{equation}

\begin{Remark}
取 $\tensor{\xi}{^i_\alpha} := \tensor{q}{^i_I} \tensor{\xi}{^I_\alpha}$, $\alpha=1,2,3$ 为 $W$ 上的基底。令 $( \tensor{\tau}{_\alpha} )\tensor{{}}{^i_j} := \tensor{\vol}{^i_k_j} \tensor{\xi}{^k_\alpha}$，则三个 $\tensor{{\tau}}{_\alpha^i_j}$ 是 $\so{3}$ 的基底，$\tensor{\tau}{_i^j_k} := \tensor{\tau}{_\alpha^j_k} \tensor{\xi}{^\alpha_i}$ 是从 $W$ 到 $\so{3}$ 的同构。则 $\tensor{\omega}{_a^i_j} = \tensor{\omega}{^k_a} \tensor{\tau}{_k^i_j}$ 是 $\so{3}$ 值联络。
\end{Remark}

\begin{Property}
当 $\tensor{\omega}{_a^I_J}$ 是与 $\tensor{e}{^I_a}$ 相容的洛伦兹联络时，$\tensor{\omega}{^k_a} \tensor{\tau}{_k^i_j} = \tensor{\vol}{^i_k_j}\tensor{\omega}{^k_a}$ 是与 $\tensor{e}{^i_a}$ 相容的 $\so{3}$ 值联络，$\tensor{K}{^i_a} = \tensor{e}{^i_d} \tensor{h}{^c_a} \tensor{h}{^d_b} \Nabla{c} \tensor{n}{^b}$ 是外曲率的标架形式。
\end{Property}

定义 Ashtekar 联络
\begin{equation}
\tensor{A}{^i_a} \definedby \tensor{\omega}{^i_a} + \beta \tensor{K}{^i_a},
\end{equation}
可以算得
\begin{Property}
以 Ashtekar 联络为位型变量，相应的共轭动量为
\begin{equation}
\tensor{\tilde{P}}{^a_i} \definedby \frac{1}{\gkappa \beta} \tensor{\tilde{E}}{^a_i},
\end{equation}
其中
\begin{equation}
\tensor{\tilde{E}}{^a_i} = \sqrt{\abs{\det h}} \tensor{e}{^a_i} = \det(e) \tensor{e}{^a_i}
\end{equation}
是权为1的密度化的 3 标架。
\end{Property}

\nomenclature{$\tensor{A}{^i_a}$}{Ashtekar 联络}
\nomenclature{$\tensor{\tilde{P}}{^a_i}$}{与 Ashtekar 联络共轭的动量}
\nomenclature{$\tensor{\tilde{E}}{^a_i}$}{权为1的密度化的 3 标架}

联络 $\tensor{A}{^i_a}$ 或 $\tensor{A}{_a^i_j} = \tensor{\vol}{^i_k_j} \tensor{A}{^k_a}$ 对应新的导数算子 $\AD{a}$，记其曲率为
\begin{equation}
\begin{split}
\tensor{F}{_a_b_i^j} &\definedby \tensor{\vol}{_i_k^j} \tensor{\dd{}}{_a} \tensor{A}{^k_b} + \left( \tensor{\vol}{_i_l^k} \tensor{A}{^l_a} \right) \wedge \left( \tensor{\vol}{_k_m^j} \tensor{A}{^m_b} \right)\\
&= \tensor{\vol}{_i_k^j} \tensor{\dd{}}{_a} \tensor{A}{^k_b} + \tensor{A}{^j_a} \wedge \tensor{A}{_i_b},
\end{split}
\end{equation}
或
\begin{equation}
\tensor{F}{^i_a_b} = \tensor{\dd{}}{_a} \tensor{A}{^i_b} + \tensor{\vol}{^i_j_k} \tensor{A}{^j_a} \wedge \tensor{A}{^k_a}.
\end{equation}

\nomenclature{$\AD{a}$}{Ashtekar 联络对应的协变导数}
\nomenclature{$\tensor{F}{^i_a_b}$}{Ashtekar 联络对应的曲率}

\begin{Property}
在Ashtekar 变量下，Holst 作用量改写为
\begin{equation}
S = \int_{\mathbb{R}} \dd{t} \int_{{\mathcal{S}}_t} \dd[3]{x} \left( \tensor{\tilde{P}}{^a_i} \tensor{\dot{A}}{^i_a} - \Had(\tensor{A}{^i_a}, \tensor{\tilde{P}}{^a_i}, N, \tensor{N}{^a}, \tensor{\Lambda}{^i}) \right),
\end{equation}
哈密顿量
\begin{equation}
H = \int_{{\mathcal{S}}} \dd[3]{x} \Had := \int_{{\mathcal{S}}} \dd[3]{x} \left( \tensor{\Lambda}{^i} \tensor{G}{_i} + \tensor{N}{^a} \tensor{V}{_a} + N C \right),
\end{equation}
其中三个约束
\begin{equation}
\begin{split}
\tensor{G}{_i} &= \AD{a} \tensor{\tilde{P}}{^a_i} = \Partial{a} \tensor{\tilde{P}}{^a_i} + \tensor{\vol}{_i_j^k} \tensor{A}{^j_a} \tensor{\tilde{P}}{^a_k},\\
\tensor{V}{_a} &= \tensor{\tilde{P}}{^b_i} \tensor{F}{^i_a_b} - \frac{1+\beta^2}{\beta} \tensor{K}{^i_a} \tensor{G}{_i},\\
C &= \frac{\gkappa \beta^2}{2\sqrt{\abs{\det h}}} \tensor{\tilde{P}}{^a_i} \tensor{\tilde{P}}{^b_j} \left[ \tensor{\vol}{^i^j_k} \tensor{F}{^k_a_b} - \left( 1+ \beta^2 \right) \tensor{K}{^i_a} \wedge \tensor{K}{^j_b} \right]\\
& \qquad + \gkappa \left( 1 +\beta^2 \right) \tensor{G}{^i} \Partial{a} \left( \frac{\tensor{\tilde{P}}{^a_i}}{\sqrt{\abs{\det h}}} \right)\label{eq-constrains_in_Ashtekar_connection}
\end{split}
\end{equation}
是 Gauss 约束（规范对称引入的新约束）、矢量约束、标量约束，而
\begin{equation}
\tensor{\Lambda}{^i} := \tensor{q}{^i_I} \tensor{t}{^a} \tensor{n}{_J} \tensor[^\star]{\omega}{_a^I^J}
\end{equation}
和 $\tensor{N}{^a},N$ 是拉氏乘子。
\end{Property}

由于 $\tensor{A}{^i_a}$ 和 $\tensor{\tilde{P}}{^a_i}$ 是共轭变量，其泊松括号为
\begin{equation}
\left\{ \tensor{A}{^i_a}(x) , \tensor{\tilde{P}}{^b_j}(y) \right\} = \tensor{\delta}{^i_j} \tensor{\delta}{^b_a} \delta(x,y),
\end{equation}
定义 smeared 约束
\begin{equation}
G(\Lambda) := \int_{{\mathcal{S}}} \dd[3]{x} \tensor{\Lambda}{^i} \tensor{G}{_i},\label{eq-smeared_Gauss_constrain}
\end{equation}
它是局部 $\SO{3}$ 规范变换
的生成元，即
\begin{Property}
\begin{equation}
\left\{ \tensor{A}{^i_a}, G(\Lambda) \right\} = - \AD{a} \tensor{\Lambda}{^i} \qc \left\{ \tensor{\tilde{P}}{^a_i}, G(\Lambda) \right\} = \tensor{\vol}{_i_j^k} \tensor{\Lambda}{^j} \tensor{\tilde{P}}{^a_k}.
\end{equation}
\end{Property}
$\tensor{V}{_a}$ 和 $C$ 都包含一部分 $\SO{3}$ 规范变换，一种方便的做法是重新定义 smeared 微分同胚约束
\begin{equation}
C_{\text{Diff}}(v) := \int_{{\mathcal{S}}} \dd[3]{x} \left( \tensor{v}{^a} \tensor{\tilde{P}}{^b_i} \tensor{F}{^i_a_b} - \tensor{v}{^a} \tensor{A}{^i_a} \tensor{G}{_i} \right)
\end{equation}
代替矢量约束，可以算得
\begin{Property}
\begin{equation}
\left\{ \tensor{A}{^i_a} , C_{\text{Diff}}(v) \right\} = \Ld{v} \tensor{A}{^i_a} \qc \left\{ \tensor{\tilde{P}}{^a_i}, C_{\text{Diff}}(v) \right\} = \Ld{v} \tensor{\tilde{P}}{^a_i},
\end{equation}
\end{Property}
并在 smeared 标量约束中去掉 $\tensor{G}{_i}$ 项，即
\begin{equation}
C(f) = \int_{{\mathcal{S}}} \dd[3]{x} f(x) \tilde{C}(x) := \frac{\gkappa \beta^2}{2} \int_{{\mathcal{S}}} \dd[3]{x} f \frac{\tensor{\tilde{P}}{^a_i} \tensor{\tilde{P}}{^b_j}}{\sqrt{\abs{\det h}}} \left[ \tensor{\vol}{^i^j_k} \tensor{F}{^k_a_b} - \left( 1+ \beta^2 \right) \tensor{K}{^i_a} \wedge \tensor{K}{^j_b} \right],
\end{equation}
常称为哈密顿约束，有如下约束代数
\begin{Property}
\begin{equation}
\begin{split}
\left\{ G(\Lambda), G(\Lambda') \right\} &= G\left( \left[ \Lambda, \Lambda' \right] \right),\\
\left\{ G(\Lambda), C_{\text{Diff}}(v) \right\} &= - G(\Ld{v} \Lambda),\\
\left\{ G(\Lambda), C(f) \right\} &= 0,\\
\left\{ C_{\mathrm{Diff}}(u), C_{\text{Diff}}(v) \right\} &= C_{\text{Diff}}([u,v]),\\
\left\{ C_{\text{Diff}}(v), C(f) \right\} &= - C(v(f)),\\
\left\{ C(f), C(f') \right\} &= - C_{\text{Diff}}(S(f,f')) - G\left(\tensor{S}{^a}(f,f') \tensor{A}{^i_a} \right)\\
&\qquad\qquad - \left( 1+\beta^2 \right) G\left( \frac{\left[ \tilde{P}(f), \tilde{P}(f') \right]}{\abs{\det q}} \right),\label{eq-constrain_algebra}
\end{split}
\end{equation}
其中
\begin{equation}
\tensor{S}{^a}(f,f') := f \tensor{D}{^a} f' - f' \tensor{D}{^a} f,
\end{equation}
而 $\tilde{P}(f)$ 指的是 $\tensor{\tilde{P}}{^a_i} \tensor{D}{_a} f$。
\end{Property}

\nomenclature{$G(\Lambda)$}{smeared 高斯约束}
\nomenclature{$C_{\text{Diff}}(v)$}{smeared 微分同胚约束}

至此，我们基本构建了 Ashtekar 变量下的哈密顿理论，以 Ashtekar 联络 $\tensor{A}{^i_a}$ 和动量 $\tensor{\tilde{P}}{^a_i}$ 为正则变量，约束方程加上（为哈密顿量补上边界项的）哈密顿方程即等价于 Einstein 场方程。于是，广义相对论被改写为了一个具有紧致规范群的规范理论，可以参考非阿贝尔规范理论已有的工具进行量子引力的探索，这就是圈量子引力的由来。

最早 Ashtekar 于 1986 年所发表的 Ashtekar 变量\cite{Ashtekar1986}是选择 $\beta = -\ii$ 的情况，此时可以注意到约束的表达式极为简洁：
\begin{equation}
\begin{split}
\tensor{G}{_i} &= \AD{a} \tensor{\tilde{P}}{^a_i},\\
\tensor{V}{_a} &= \tensor{\tilde{P}}{^b_i} \tensor{F}{^i_a_b},\\
C &= \frac{\gkappa \beta^2}{2\sqrt{\abs{\det h}}} \tensor{\tilde{P}}{^a_i} \tensor{\tilde{P}}{^b_j} \tensor{\vol}{^i^j_k} \tensor{F}{^k_a_b},\label{eq-remannian_constrain}
\end{split}
\end{equation}
但缺点是要引入复联络，相当于考虑复化的广义相对论。为了得到物理的信息，需要引入“实性条件”，即把物理状态限制在复相空间中的一个截面上，以保证由 Ashtekar 变量诱导的 $\tensor{h}{_a_b}$ 和 $\tensor{K}{_a_b}$ 为实张量。在研究过程中物理学家们发现，实性条件给量子化带来了大量困难，于是 1994 年 Barbero 引入了上文所述的实值 Barbero-Immiriz 参数 $\beta$ 代替 $-\ii$，于是有了实变量理论。实 Ashtekar 变量理论与复 Ashtekar 变量理论相比，虽然约束表达式多出了被称为“Lorentz 项”的附加项，复杂了一些，但消除了实性条件，综合来看要更简洁方便一些，因此普遍采用实变量理论。

## 参考文献

<table border="0" text-align="center" vertical-align="top">
    <tr>
        <td>[1]</td>
        <td>Ashtekar A. New Variables for Classical and Quantum Gravity. Phys. Rev. Lett., 1986, 57:2244­2247. <a url="http://doi.org/10.1103/PhysRevLett.57.2244">10.1103/PhysRevLett.57.2244</a>.</td>
    </tr>
</table>
[1]<div id="ref-Ashtekar1986">Ashtekar A. New Variables for Classical and Quantum Gravity. Phys. Rev. Lett., 1986, 57:2244­2247. DOI: [10.1103/PhysRevLett.57.2244](http://doi.org/10.1103/PhysRevLett.57.2244).</div>
