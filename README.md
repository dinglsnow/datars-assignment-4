# 小组成员

丁俐杉2025303110114
于辛铠2025303110116
成一潇2025303110122
霍晶晶2025303110132

# Reproducible Validation of Air Pollution Retrieval

## 项目背景 (Background)
核心任务是复现论文 *Song et al. (2021)* 中的精度验证环节。

- **参考论文**: Song, Z., Bai, Y., Wang, D., Li, T., & He, X. (2021). *Satellite Retrieval of Air Pollution Changes in Central and Eastern China during COVID-19 Lockdown Based on a Machine Learning Model*. **Remote Sensing**, 13(13), 2525.

## 核心方法：散点密度图 (Scatter Density Plots)
本项目实现了一种用于遥感反演数据精度验证的高级可视化方法：
- **功能**: 绘制预测值 (Model Predicted) 与实测值 (Measured) 的对比散点图。
- **技术细节**: 利用高斯核密度估计 (Kernel Density Estimation) 为散点着色，直观展示数据分布密度。
- **指标计算**: 自动计算并标注 $R^2$、RMSE 和样本量 (N)，这与 Song et al. (2021) 论文中的 Figure 3 完全对标。


## 技术栈 (Technical Stack)
- **环境管理**: [uv]
- **机器学习**: `scikit-learn` (Random Forest Regressor)
- **数据处理**: `pandas`, `numpy`
- **可视化**: `matplotlib`, `seaborn` (用于绘制论文风格的密度散点图和时序变化图)

# Reproducible Validation of Air Pollution Retrieval

# 小组成员

丁俐杉2025303110114
于辛铠2025303110116
成一潇2025303110122
霍晶晶2025303110132

## 项目简介

本项目是“数据驱动与可重复性实验”课程的结业作业，主题为**空气污染遥感反演数据的精度验证与可视化复现**。

项目参考 Song et al. (2021) 中关于空气污染反演结果验证的思路，使用 PM2.5 相关数据，对反演值或模型预测值与地面观测值进行对比分析，并通过散点密度图展示两类数据之间的关系。

本项目并不重点关注复杂模型的重新构建，而是围绕一个较为完整的数据分析流程展开，重点体现课程中强调的**数据驱动分析、结果解释和实验可重复性**。

本项目主要完成以下工作：

- 整理并读取 PM2.5 数据；
- 对地面观测值和反演值进行对比；
- 计算相关系数、偏差、均方根误差等评价指标；
- 绘制普通散点图和散点密度图；
- 对结果进行解释；
- 将代码、数据和输出结果整理为可复现的 GitHub 仓库。

## 项目背景

PM2.5 是评价空气污染程度的重要指标之一。传统的地面监测站点可以提供较准确的观测数据，但监测站点在空间分布上通常有限，难以全面反映区域尺度上的污染变化情况。

遥感反演方法可以利用卫星观测数据估算空气污染物浓度，从而在更大空间范围内补充地面观测数据。但是，遥感反演结果是否可靠，需要通过地面实测数据进行验证。

因此，本项目选取 PM2.5 反演值与地面观测值之间的关系作为分析对象，通过统计指标和可视化图像判断反演结果的精度表现。

## 参考文献

Song, Z., Bai, Y., Wang, D., Li, T., & He, X. (2021).  
*Satellite Retrieval of Air Pollution Changes in Central and Eastern China during COVID-19 Lockdown Based on a Machine Learning Model.*  
Remote Sensing, 13(13), 2525.

## 数据说明

本项目使用的数据文件为：

```text
pm25.csv
