---
layout: page   页面布局:
title: "Movie Profit Mining | 电影盈利因素挖掘"Title: "Movie Profit Mining | Uncovering Factors for Film Profitability"Title: "Movie Profit Mining | Uncovering Factors for Film Profitability"
date: 2025-10-13   日期:2025-10-13   日期:2025-10-13
description: "K-Means cluster 5 043 movies to find the golden formula of profitability"描述：“通过 K-Means 聚类算法对 5043 部电影进行分类，以找出盈利的黄金法则”描述：“通过 K-Means 聚类算法对 5043 部电影进行分类，以找出盈利的黄金法则”
img: assets/img/movie_02_scatter.png图片：assets/img/movie_02_scatter.png图片：assets/img/movie_02_scatter.png
importance: 1   重要性:1
category: work   类别:工作
---

## 1 项目背景
国内电影年备案上千部，真正盈利的不足 30 %。借助数据挖掘，把“拍脑袋”决策变成可量化的成功率评估。

## 2 数据与字段
- 公开数据集：Kaggle “The Movies” 5 043 条记录
- 核心字段：budget、worldwide_gross、IMDb_score、is_profitable
- 衍生字段：ROI、profit_level（均在 SPSS Modeler 节点完成）

## 3 关键步骤
① 数据清洗  
缺失 budget 6 条 → 敏感性检验后整行删除，保证分布不偏。

② 聚类建模  
K-Means，K=5 由肘部法则 + 轮廓系数 0.52 双重锁定；80/20 分区验证。

③ 可视化  
gross vs IMDb 散点按簇着色，一眼锁定“高票房+高口碑”黄金象限。

## 4 结果亮点
| Cluster | 盈利概率 | 特征简述 |
|---|---|---|
| Cluster-4 | 91 % | 高预算、高评分、暑期/感恩档期 |
| Cluster-2 | 6 % | 低预算、低评分、冷门档期 |

## 5 可复现
模型流 + 清洗后数据 + 本报告已打包，下载后双击 `.str` 文件即可一键复现。

### 下载区
- [📄 完整报告 PDF](https://github.com/YOYO03/YOYO03.github.io/raw/main/blockchain_survey_report_2025-10-13.pdf)
- [📊 清洗数据 CSV](https://github.com/YOYO03/YOYO03.github.io/raw/main/movie_clean.csv)
- [💻 模型流文件](https://github.com/YOYO03/YOYO03.github.io/raw/main/movie_k5.str)

### 图注
① 数据流全景  
![Pipeline](assets/img/movie_01_pipeline.png)

② 聚类散点：预算-口碑-盈利三维空间  
![Scatter](assets/img/movie_02_scatter.png)散点图
