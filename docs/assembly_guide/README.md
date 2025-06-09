# OpenTennisTrainingBot 组装指南 🛠️

本指南将帮助你完成 OpenTennisTrainingBot 的硬件组装和初始设置。

## **1. 所需工具**
- **3D 打印部件**（STL 文件位于 `hardware/mechanical_design/`）
- **螺丝刀套装**（十字/一字）
- **电烙铁 & 焊锡**
- **万用表**（用于电路检查）
- **钳子 & 剪线钳**
- **锂电池（24V, 3000mAh 或更高）**

## **2. 机械组装**
### **步骤 1：打印框架**
- 打印 `hardware/mechanical_design/frame/` 下的所有部件
- 使用 PLA+ 或 PETG 材料（ABS 可选，但需封闭打印环境）

### **步骤 2：安装驱动轮**
1. 将电机安装到电机支架上
2. 固定摩擦轮，确保间距可调（参考 `hardware/mechanical_design/wheel_assembly.pdf`）
3. 用皮带连接电机和驱动轮

### **步骤 3：装配球仓**
- 安装储球漏斗
- 确保送球机构顺畅（测试手动送球）

## **3. 电子系统安装**
### **步骤 1：焊接控制板**
- 按照 `hardware/electronics/schematic.pdf` 焊接 PCB
- 安装 ESP32 主控、电机驱动模块（如 DRV8871）

### **步骤 2：连接传感器**
- 限位开关（检测球仓状态）
- 光电传感器（检测球速）

### **步骤 3：供电系统**
- 连接 24V 锂电池
- 安装电源开关和急停按钮

## **4. 首次启动 & 校准**
1. 通电后，检查电机是否运转正常
2. 使用 `firmware/calibration_tool.py` 校准发射角度和速度
3. 测试不同旋转模式（上旋/下旋/侧旋）

---

## **2. 贡献指南 (`.github/CONTRIBUTING.md`)**
```markdown
# **欢迎贡献 OpenTennisTrainingBot！** 👋

我们非常欢迎社区贡献，无论是代码、文档、测试还是反馈！

## **1. 报告问题**
- 使用 [Issue 模板](.github/ISSUE_TEMPLATE/bug_report.md) 提交 Bug
- 提供复现步骤、硬件配置和错误日志

## **2. 提交代码**
1. **Fork 本项目**
2. **创建分支**（如 `feature/add-bluetooth` 或 `fix/motor-driver-issue`）
3. **提交代码**
   ```bash
   git commit -m "feat: 添加蓝牙控制支持"
