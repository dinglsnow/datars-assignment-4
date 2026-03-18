# 小组成员

丁俐杉2025303110114
于辛铠2025303110116
成一潇2025303110122

# datars-assignment-4
# Reproducible Machine Learning Pipeline for Satellite-based Air Pollution Retrieval

## 项目背景 (Background)
本实验旨在复现并建立一个类似于以下研究的大气污染预测机器学习流程：

- **参考论文**: Song, Z., Bai, Y., Wang, D., Li, T., & He, X. (2021). *Satellite Retrieval of Air Pollution Changes in Central and Eastern China during COVID-19 Lockdown Based on a Machine Learning Model*. **Remote Sensing**, 13(13), 2525.

本项目重点在于利用 Python 机器学习工具链，复现论文中提到的**地理随机森林 (Geographical Random Forest, RF)** 建模思路，并确保该研究环境在不同计算平台上的高度可重复性。

## 核心方法论 (Methodology)
参考 Song et al. (2021) 的研究，本项目模拟了以下数据处理与建模流程：
1. **多源数据整合**: 结合卫星遥感数据（如 AOD 气溶胶光学厚度）、ERA5 气象重分析数据（温度、湿度、风速等）以及地面监测站观测数据。
2. **机器学习建模**: 使用随机森林 (Random Forest) 算法构建非线性回归模型，预测 PM2.5、PM10、O3 和 CO 的浓度分布。
3. **可重复性实现**: 通过 `uv` 环境管理器锁定依赖版本，确保模型训练和验证结果在不同环境下的一致性。

## 技术栈 (Technical Stack)
- **环境管理**: [uv]
- **机器学习**: `scikit-learn` (Random Forest Regressor)
- **数据处理**: `pandas`, `numpy`
- **可视化**: `matplotlib`, `seaborn` (用于绘制论文风格的密度散点图和时序变化图)

