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
