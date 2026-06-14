# MD→LaTeX 章节转换规范 v1.0
## 适用: 车晶论文 05_LaTeX/body/chapter1-7.tex

## 核心规则（来源于12轮Overleaf编译修复经验）

### 1. 表格 — 三线表强制规范
```latex
\begin{table}[htbp]
  \centering
  \small
  \caption{表题（不写"表X-Y："前缀，LaTeX自动编号）}
  \begin{tabularx}{\textwidth}{X X X X}
    \toprule
    \textbf{表头1} & \textbf{表头2} & \textbf{表头3} & \textbf{表头4} \\
    \midrule
    数据行... \\
    \bottomrule
  \end{tabularx}
\end{table}
```
- 禁止: \hline、竖线|、\footnotesize（用\small代替）
- 表注: {\footnotesize 注：...} 花括号包裹，放在\end{table}之前
- 宽表超\textwidth: 用 \scalebox{0.85}{...} 包裹整个tabularx

### 2. 插图
```latex
\begin{figure}[htbp]
  \centering
  \includegraphics[width=0.85\textwidth]{figures/图X-Y_描述.png}
  \caption{图题（不写"图X-Y："前缀）}
  \label{fig:X-Y}
\end{figure}
```

### 3. 加粗规则（严格）
- ✅ 表格表头: \textbf{...}
- ✅ EFA因子载荷≥0.7: \textbf{...}
- ❌ 正文段落: 禁止\textbf{...}
- ❌ 研究结论: 禁止\textbf{...}
- ❌ 表格数据单元格: 禁止\textbf{...}

### 4. 引用格式
- Markdown [N] → LaTeX \cite{refN}
- 连续引用: [1][2][3] → \cite{ref1,ref2,ref3}

### 5. 章节结构
```latex
\chapter{第X章标题}
\section{小节标题}
\subsection{子小节标题}
```
- 段落结尾加 \par
- 列表用 \begin{itemize} \item ... \end{itemize}

### 6. 字符规范
- 中文引号: "内容"
- 箭头: A → B（前后空格）
- P公司: 无空格
- 百分号: 51.4\%
- 省略号: \ldots
- 波折号: ——
- 粗体强调: 仅用\textbf{}在表头

### 7. 公式
- 核心公式: \begin{equation} ... \end{equation}
- 行内变量: $...$
- α/β/χ²: $\alpha$, $\beta$, $\chi^2$

### 8. 图片映射表
| 图号 | 文件名 |
|------|--------|
| 图1-4 | 图1-4_技术路线图.png |
| 图1-4(2) | 图1-4_DMAIC研究框架图.png |
| 图3-1 | 图3-1_P公司服务流程图.png |
| 图3-2 | 图3-2_客户投诉类型分布.png |
| 图4-1 | 图4-1_IPA四象限分析矩阵.png |
| 图4-2 | 图4-2_SERVQUAL改良评价指标模型.png |
| 图4-3 | 图4-3_期望感知差距雷达图.png |
| 图5-1 | 图5-1_服务质量短板鱼骨图.png |
| 图6-1 | 图6-1_改进方案实施路线图.png |
| 图6-2 | 图6-2_持续控制闭环图.png |
| 图6-3 | 图6-3_改进前后指标对比.png |
