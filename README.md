# 车晶 MEM 学位论文 — Overleaf LaTeX 编译包

华东师范大学工程管理硕士（MEM）学位论文  
《面向服务质量的普惠金融公司 DMAIC 改进研究——以 P 公司为例》

## 项目结构

```
├── main.tex                # 主文件（封面信息、章节引用）
├── ecnumasterpro.cls       # ECNU MEM 模板类
├── STZHONGS.TTF            # 中文字体
├── Declaration.tex          # 原创性声明
├── Committee.tex            # 答辩委员会名单
├── Abstract_chs.tex         # 中文摘要
├── Abstract_eng.tex         # 英文摘要
├── body/
│   ├── chapter1.tex ~ chapter7.tex   # 第1-7章正文
│   ├── refs.tex                      # 参考文献（51条 GB/T 7714）
│   └── ack.tex                       # 致谢
└── figures/                # 论文图表（PNG 300dpi）
```

## Overleaf 编译指南

1. 将整个项目打包为 `.zip` 上传至 Overleaf
2. 编译器选择 **XeLaTeX**
3. 菜单 → Compiler: XeLaTeX
4. 编译 2 遍（首次编译生成引用编号，二次编译刷新交叉引用）
5. 若 PDF 中缺少中文，确认 `STZHONGS.TTF` 已上传至项目根目录

## 写作规范

- 引用格式：GB/T 7714-2015 顺序编码制
- 脱敏规则：企业名→字母代号，财务数据→量级描述
- 图表规范：表题在上 / 图题在下，编号格式 `表 X-Y` / `图 X-Y`
- 三线表：仅使用 `\toprule` / `\midrule` / `\bottomrule`
- 正文无加粗，仅表头和数据载荷可用 `\textbf{}`

## 参考文献

51 篇，其中中文 23 篇 + 外文 28 篇，期刊论文 ≥ 60%，学位论文 ≤ 10 篇。

## 关联仓库

- 陈虎同模板论文：[chenhu-thesis-overleaf](https://github.com/xiaomi1998/chenhu-thesis-overleaf)
- 苗琳同模板论文：[ecnu-mem-miaolin-thesis](https://github.com/xiaomi1998/ecnu-mem-miaolin-thesis)
