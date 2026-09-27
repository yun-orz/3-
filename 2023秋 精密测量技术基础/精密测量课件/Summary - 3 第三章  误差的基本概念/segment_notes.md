# 第三章 误差的基本概念 —— 分段精读笔记 (Segment Notes)

## 总体结构与分段映射表 (Segmentation Map)
- **Segment 1 (P1 - P4)**: §3-1 测量的定义与分类（等精度测量 vs 非等精度测量）
- **Segment 2 (P5 - P17)**: §3-2 误差定义与基本表示方法（绝对误差、相对误差、引用误差、真误差与残差、极限误差）
- **Segment 3 (P18 - P38)**: 误差分类体系与统计学定义（系统/随机/粗大误差、数学期望分解、相互转化）
- **Segment 4 (P39 - P49)**: 误差来源与有效数字运算修约规则（标准器误差比例、四舍六入五凑双、运算规则）
- **Segment 5 (P50 - P58)**: §3-3 测量仪器、方法与结果的评价（精密度 vs 准确度、重复性、灵敏度、线性度、分辨力）
- **Segment 6 (P59 - P71)**: §3-4 测量不确定度简介与误差对比（定义、6大核心区别、A类与B类评定、合成与扩展）

---

## Segment 1: §3-1 测量的定义与分类 (P1 - P4)
- **page range covered**: P1 - P4
- **main exam points**: 
  1. 测量的经典定义（将未知被测量与作为测量单位的标准量进行比较，确定其比值）与现代定义（赋值过程，赋予事物特定特性关系的值）[课件 P2]。
  2. 等精度测量 vs 非等精度测量（判断条件四要素：测量人员、仪器精度、环境条件、测量方法）[课件 P4]。
- **core formulas**: 
  - 测量基本方程：$x = q \cdot [u]$（$x$ 为被测量，$q$ 为数值，$[u]$ 为测量单位）。
- **key concepts with English terms**:
  - 测量 (Measurement) [课件 P2]
  - 测量值 (Measured value) [课件 P2]
  - 等精度测量 (Measurement of equal precision / Equal accuracy measurement) [课件 P4]
  - 非等精度测量 (Measurement of unequal precision) [课件 P4]
- **important examples or recurring problem patterns**:
  - 判断某组测量是等精度还是非等精度：如不同实验员在不同温度下使用不同仪器，则为非等精度；数据处理时必须加权处理。
- **problem-solving techniques or pitfalls**:
  - 混淆“等精度”与“等读数”：等精度是指测量条件（人、机、料、法、环）恒定，而非测量结果数值完全相同。
- **figure candidates**: 测量比较过程框图。
- **coverage concerns or uncertainty**: None.

---

## Segment 2: §3-2 误差定义与基本表示方法 (P5 - P17)
- **page range covered**: P5 - P17
- **main exam points**:
  1. 误差的定义：绝对误差 $\delta = x - \mu$（测得值 - 真值）[课件 P7]。
  2. 真值的分类：理论真值（理论公式/几何定理如三角形内角和 $180^\circ$）vs 约定真值（计量基准、国家基准实物）[课件 P8]。
  3. 绝对误差的本质特征：必为一个具有大小和符号的确定数值，绝不可带有正负号（$\pm$）[课件 P9]。带有 $\pm$ 的是误差极限或不确定度，不是单次测量的绝对误差！
  4. 相对误差 $\delta_r = \frac{x-\mu}{\mu} \times 100\%$：反映测量工作的精细程度与质量，消除量纲和量值大小的影响[课件 P11-P13]。
  5. 引用误差 $\gamma = \frac{\Delta}{Y_{\max}} \times 100\%$：用于仪表分级（0.1, 0.2, 0.5, 1.0, 1.5, 2.5, 5.0级）[课件 P14]。
  6. 电表测量范围选择原则：为什么指针应在满量程的 $2/3$ 以上？因为引用误差固定时，示值越小，引起的相对误差越大！
  7. 误差表达变体：真误差 $\delta = x - A_0$、残余误差（残差）$v_i = x_i - \bar{x}$、最大绝对误差 $U$、极限误差 $\delta_{\lim} = 3\sigma$ [课件 P15-P17]。
- **core formulas**:
  - 绝对误差：$\delta = x - \mu$；示值误差：$\Delta = x_{\text{示}} - x_{\text{真}}$ [课件 P7]
  - 相对误差：$\delta_r = \frac{\delta}{\mu} \times 100\% \approx \frac{\delta}{x} \times 100\%$ [课件 P11]
  - 引用误差：$\gamma = \frac{\Delta}{Y_{\max}} \times 100\%$ [课件 P14]
  - 仪表准确度等级：$K = |\gamma_{\max}| \times 100$（去掉百分号）
  - 仪表实际测量的最大相对误差界：$\delta_{r,\max} = \pm \frac{K\% \cdot Y_{\max}}{x} = \pm K\% \cdot \frac{Y_{\max}}{x}$ [作业 3-3]
  - 残差：$v_i = x_i - \bar{x}$，满足 $\sum_{i=1}^n v_i = 0$ [课件 P15]
  - 极限误差：$\delta_{\lim} = 3\sigma$（正态分布置信概率 99.73%）[课件 P17]
- **key concepts with English terms**:
  - 绝对误差 (Absolute error) [课件 P7]
  - 示值误差 (Error of indication) [课件 P7]
  - 真值 (True value) [课件 P7]
  - 理论真值 (Theoretical true value) [课件 P8]
  - 约定真值 (Conventional true value) [课件 P8]
  - 相对误差 (Relative error) [课件 P11]
  - 引用误差 (Fiducial error) [课件 P14]
  - 标称值 / 测量范围上限 (Nominal value / Upper limit of measuring range) [课件 P14]
  - 残余误差 / 残差 (Residual error) [课件 P15]
  - 极限误差 (Limiting error) [课件 P17]
- **important examples or recurring problem patterns**:
  - 频率计测量实例（100 kHz 测得 101 kHz，误差 1 kHz，$\delta_r = 1\%$；1 MHz 测得 1.001 MHz，误差 1 kHz，$\delta_r = 0.1\%$）[课件 P12-P13]。
  - 作业 3-2：检定 2.5 级、量程 100V 电压表，50V 处示值误差 2V，是否合格？（允许最大误差 $\Delta_{\max} = 100 \times 2.5\% = 2.5\text{V} > 2\text{V}$，故合格）。
  - 作业 3-3：电表 2/3 量程使用理由推导：相对误差 $\delta_r \le \frac{K\% \cdot Y_m}{x}$，若 $x < \frac{2}{3} Y_m$，相对误差将急剧放大超过 $1.5 K\%$。
- **problem-solving techniques or pitfalls**:
  - 混淆“绝对误差”与“误差的绝对值”：绝对误差有量纲、有正负号；误差绝对值无负号。
  - 混淆“最大绝对误差 $U$”与“极限误差 $\delta_{\lim} = 3\sigma$”：$U$ 是确定性界限（上确界），$\delta_{\lim}$ 是基于正态分布的统计概率界限。
- **figure candidates**: 仪表不同刻度下的相对误差变化曲线。
- **coverage concerns or uncertainty**: None.

---

## Segment 3: 误差分类体系与统计学定义 (P18 - P38)
- **page range covered**: P18 - P38
- **main exam points**:
  1. 传统误差分类：系统误差、随机误差、粗大误差三类特征机理 [课件 P18-P28]。
  2. 系统误差 (Systematic error)：在重复性条件下保持恒定或按可预见规律变化；修正值 $b = -\varepsilon$；已定系统误差 vs 未定系统误差；恒定 vs 变值（线性、周期、复杂）[课件 P19-P24]。
  3. 随机误差 (Random error)：按不可预见方式变化；单个无规律，总体服从统计分布；具有“抵偿性”，不能通过修正值消除，只能通过统计估计 [课件 P25-P26]。
  4. 粗大误差 (Gross error / Outlier)：超出正常分布范围的异常值，由失误产生，必须剔除 [课件 P27-P28]。
  5. 现代统计学数学定义：$\delta = x - \mu = [x - E(x)] + [E(x) - \mu] = \eta + \varepsilon$ [课件 P29-P36]：
     - 随机误差分量 $\eta = x - E(x)$，$E(\eta) = 0$
     - 系统误差分量 $\varepsilon = E(x) - \mu$，$E(\delta) = \varepsilon$
  6. 误差分类的相对性与相互转化：在特定条件下，系统误差与随机误差可以相互转化（如一批零件加工尺寸的系统误差，在装配环节表现为随机误差；标准仪器的随机误差在用于校准次级仪器时转变为次级仪器的系统误差）[课件 P38]。
- **core formulas**:
  - 误差正交/线性分解：$\delta = \eta + \varepsilon$ [课件 P29]
  - 修正值关系：$b = -\varepsilon$，$x_{\text{修}} = x + b = x - \varepsilon$ [课件 P22]
  - 统计期望性质：$E(\eta) = 0$，$E(x) = \mu + \varepsilon$ [课件 P30, P34]
- **key concepts with English terms**:
  - 系统误差 (Systematic error) [课件 P19]
  - 随机误差 (Random error) [课件 P25]
  - 粗大误差 / 过失误差 (Gross error / Parasitic error / Outlier) [课件 P27]
  - 修正值 (Correction value) [课件 P22]
  - 已定系统误差 (Determined systematic error) [课件 P23]
  - 未定系统误差 (Undetermined systematic error) [课件 P23]
  - 抵偿性 (Compensating property) [课件 P26]
  - 数学期望 (Mathematical expectation) [课件 P29]
- **important examples or recurring problem patterns**:
  - 砝码偏差为系统误差，可通过修正值消除；环境微小波动引起的读数跳动为随机误差；读错刻度为粗大误差。
  - 阐述系统误差与随机误差的辩证关系与转化条件（经典论述题）。
- **problem-solving techniques or pitfalls**:
  - 区分未定系统误差与随机误差：未定系统误差大小符号未知但在一次测量中恒定不变；随机误差在每次测量中跳变且具有抵偿性。
- **figure candidates**: 概率密度曲线 $f(x)$，标出真值 $\mu$、数学期望 $E(x)$、系统误差 $\varepsilon$、随机误差 $\eta$、置信区间 $\pm 3\sigma$ 及奇异值粗大误差。
- **coverage concerns or uncertainty**: None.

---

## Segment 4: 误差来源与有效数字运算修约规则 (P39 - P49)
- **page range covered**: P39 - P49
- **main exam points**:
  1. 测量误差四大来源：测量装置误差（原理、制造、装配、校准、磨损老化、量化误差等）、环境误差、方法误差、人员误差 [课件 P39-P41]。
  2. 标准器选用准则：标准器件的误差应占总误差的 $1/3 \sim 1/10$ [课件 P41]。
  3. 有效数字定义：绝对误差界为末位半个单位的近似数位数 [课件 P44-P45]。
  4. 有效数字位数与相对误差的关系：有效数字位数直接反映相对误差的大小，与小数点位置无关（2位有效数字 $Er \in \pm [1\%, 10\%]$；3位 $\pm [0.1\%, 1\%]$；4位 $\pm [0.01\%, 0.1\%]$）[课件 P47]。
  5. 数字修约规则：“四舍六入五凑双”（五后非零则进一；五后全零看奇偶，奇进偶不进；严禁连续修约！）[课件 P48-P49]。修约误差是不超过末位半个单位的均值为 0 的随机误差。
  6. 数据运算规则：加减运算按小数点后位数最少（绝对误差最大）的保留；乘除运算按有效数字位数最少（相对误差最大）的保留 [作业 3-4]。
- **core formulas**:
  - 有效数字绝对误差限：$\Delta \le \frac{1}{2} \times 10^{-m}$（$m$ 为末位所在位）[课件 P44]
  - 相对误差范围估算：$\frac{0.5}{10} \le \delta_r \le \frac{0.5}{1}$ 即 $5\% \sim 50\%$（首位数字为 1 到 9 时的规律）[课件 P47]
  - 加减法有效位数规则：以小数点后位数最少者为准
  - 乘除法有效位数规则：以有效数字位数最少者为准
- **key concepts with English terms**:
  - 有效数字 (Significant figures / digits) [课件 P44]
  - 数字修约 / 舍入 (Rounding off / Numerical rounding) [课件 P48]
  - 四舍六入五凑双 (Round half to even / Bankers rounding) [课件 P48]
  - 舍入误差 (Rounding error) [课件 P49]
  - 量化误差 (Quantization error) [课件 P41]
- **important examples or recurring problem patterns**:
  - 连续修约错误：$15.4546 \to 15$，绝不可 $15.4546 \to 15.455 \to 15.46 \to 15.5 \to 16$ [课件 P49]。
  - 作业 3-4 计算：
    (1) $3151.0 + 65.8 + 7.326 + 0.4162 + 152.28 = 3376.8$。
    (2) $28.13 \times 0.037 \times 1.473 = 1.5$。
- **problem-solving techniques or pitfalls**:
  - 0 的有效性判断：$0.0050$ 中前三个 0 定位，后一个 0 是有效数字（共 2 位）；$500$ 歧义，应写为 $5.00 \times 10^2$。
- **figure candidates**: None needed.
- **coverage concerns or uncertainty**: None.

---

## Segment 5: §3-3 测量仪器、方法与结果的评价 (P50 - P58)
- **page range covered**: P50 - P58
- **main exam points**:
  1. 精密度 (Precision)：多次重复测量观测值之间的离散程度，表征随机误差大小 [课件 P50]。
  2. 准确度 (Accuracy)：测量结果与真值的一致程度，主要与系统误差关联，定性概念 [课件 P51]。
  3. 精密度 vs 准确度关系（打靶模型）[课件 P52-P53]；期末真题考点：精度 vs 准确度哪一个优先？为什么？（精密度优先！因为精密度好说明随机误差小，离散度小，系统误差可以通过标定和修正消除；若精密度差，随机波动大，即便平均值靠近真值也无法通过单次测量修正得到可靠结果）。
  4. 重复性 (Repeatability)：同条件、同人员、同仪器、短时间内的一致性，$R_N = \frac{\sigma_r}{Y_m} \times 100\%$ [课件 P54-P55]。
  5. 重现性 (Reproducibility)：不同条件、不同实验室、不同人员在改变了的测量条件下的测量结果一致性 [课件 P54]。
  6. 灵敏度 (Sensitivity)：输出增量与输入增量之比 $S = \frac{\Delta y}{\Delta x}$（非线性时为导数 $\frac{dy}{dx}$）[课件 P56]。
  7. 线性度 (Linearity)：实际校准曲线与理论拟合直线的最大偏差与满量程之比 $L_N = \frac{\Delta L_{\max}}{Y_m} \times 100\%$ [课件 P57]。
  8. 分辨力 (Resolution)：能引起输出量产生可察觉变化的最小输入增量，相对指标 $\delta = \frac{\Delta x_{\min}}{x_{\max}} \times 100\%$ [课件 P58]。
- **core formulas**:
  - 重复性指标：$R_N = \frac{\sigma_r}{Y_m} \times 100\%$ [课件 P55]
  - 灵敏度：$S = \lim_{\Delta x \to 0} \frac{\Delta y}{\Delta x} = \frac{dy}{dx}$ [课件 P56]
  - 线性度（非线性误差）：$L_N = \frac{\Delta L_{\max}}{Y_m} \times 100\%$ [课件 P57]
  - 分辨力相对指标：$\delta_{\text{res}} = \frac{\Delta x_{\min}}{x_{\max}} \times 100\%$ [课件 P58]
- **key concepts with English terms**:
  - 精密度 (Precision) [课件 P50]
  - 准确度 (Accuracy) [课件 P51]
  - 重复性 (Repeatability) [课件 P54]
  - 重现性 / 复现性 (Reproducibility) [课件 P54]
  - 灵敏度 (Sensitivity) [课件 P56]
  - 线性度 / 非线性误差 (Linearity / Non-linearity error) [课件 P57]
  - 分辨力 / 分辨率 (Resolution) [课件 P58]
- **important examples or recurring problem patterns**:
  - 打靶四象限对比：高精密度低准确度（密集偏离靶心）、低精密度高准确度（分散包围靶心）、高精密度高准确度（密集靶心）、低精密度低准确度（分散偏离靶心）。
  - 名词辨析与优先选用问答（期末试卷第一大题 10 分）。
- **figure candidates**: 打靶图（TikZ 实现）与灵敏度/线性度特性曲线。
- **coverage concerns or uncertainty**: None.

---

## Segment 6: §3-4 测量不确定度简介与误差对比 (P59 - P71)
- **page range covered**: P59 - P71
- **main exam points**:
  1. 测量不确定度的定义（VIM 3）：根据所用到的信息，表征赋予被测量量值分散性的非负参数 [课件 P59-P60]。
  2. 测量结果完整表达形式：$y \pm U$（最佳估计值 $\pm$ 扩展不确定度，给出包含因子 $k$ 或置信水平 $p$）[课件 P61-P62]。
  3. 测量误差 vs 测量不确定度的本质区别（课件 P63-P64 核心表格，期末与作业重中之重！）：
     - 定义与符号：误差是有正负符号的偏离量；不确定度是无符号的非负离散性参数。
     - 参照基准：误差以“真值”为基准（向心）；不确定度以“测得值/结果”为中心评定区间（向外）。
     - 客观性 vs 认识性：误差是客观存在的客观物理状态；不确定度与评定者掌握的信息和认知水平有关。
     - 可知性：真值不可知导致真误差不可求；不确定度可根据实验和信息实际定量评定。
     - 分类哲学：误差分为随机误差与系统误差（理想概念）；不确定度分量按评定方法分为 A 类和 B 类，不强行区分误差性质。
     - 修正功能：已知系统误差可用于修正测得值；不确定度不能用于修正，修正值自身不完善会引入新的不确定度。
  4. 测量不确定度的 10 大来源（方法、仪器、环境、人员、对象）[课件 P65-P66]。
  5. A 类评定 vs B 类评定：
     - A 类：基于统计学分析，通过对观测列求均值和贝塞尔公式实验标准差 $s(\bar{x}) = \frac{s}{\sqrt{n}}$ [课件 P67-P68]。
     - B 类：基于非统计方法（利用仪器检定证书、技术规范、经验先验概率分布如正态、均匀、三角分布等确定标准不确定度 $u = \frac{a}{k}$）[课件 P67-P68]。
  6. 体系架构：标准不确定度（A类 $u_A$、B类 $u_B$）$\to$ 合成标准不确定度 $u_c = \sqrt{\sum c_i^2 u_i^2}$ $\to$ 扩展不确定度 $U = k \cdot u_c$（通常 $k=2$ 或 $3$）[课件 P69]。
- **core formulas**:
  - 测量结果区间：$Y = y \pm U$ [课件 P61]
  - A 类标准不确定度：$u_A = s(\bar{x}) = \frac{s}{\sqrt{n}} = \sqrt{\frac{\sum_{i=1}^n (x_i - \bar{x})^2}{n(n-1)}}$ [课件 P68]
  - B 类标准不确定度：$u_B = \frac{a}{k}$（$a$ 为半宽，$k$ 为包含因子，如均匀分布 $k=\sqrt{3}$，正态分布 $k=3$）
  - 合成标准不确定度（不相关输入量）：$u_c = \sqrt{\sum_{i=1}^m \left(\frac{\partial f}{\partial x_i}\right)^2 u^2(x_i)}$
  - 扩展不确定度：$U = k \cdot u_c$ [课件 P69]
- **key concepts with English terms**:
  - 测量不确定度 (Measurement uncertainty) [课件 P59]
  - 最佳估计值 (Best estimate) [课件 P62]
  - 标准不确定度 (Standard uncertainty) [课件 P69]
  - A 类评定 (Type A evaluation of measurement uncertainty) [课件 P67]
  - B 类评定 (Type B evaluation of measurement uncertainty) [课件 P67]
  - 合成标准不确定度 (Combined standard uncertainty) [课件 P69]
  - 扩展不确定度 (Expanded uncertainty) [课件 P69]
  - 包含因子 (Coverage factor $k$) [课件 P69]
- **important examples or recurring problem patterns**:
  - 论述题：“论述测量误差与测量不确定度的区别与联系”（课件作业 P71，期末 10 分必考）。
  - 计算题：均匀分布落在 $[-\sqrt{2}\sigma, +\sqrt{2}\sigma]$ 中的概率（作业 3-5）。
- **problem-solving techniques or pitfalls**:
  - 严禁说“误差等于不确定度”或“不确定度就是最大误差”。
  - 测量结果表达规范：必须写明包含因子 $k$ 或置信概率 $p$。
- **figure candidates**: 不确定度体系层次结构图与误差 vs 不确定度区间对比图。
- **coverage concerns or uncertainty**: None.
