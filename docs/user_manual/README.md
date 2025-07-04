# **OpenTennisTrainingBot 用户手册** 📖

## **1. 安全须知** ⚠️
- 使用时保持 3 米安全距离
- 勿将手伸入发射区
- 儿童需在成人监督下使用

## **2. 基本操作**
### **开机/关机**
- 长按电源键 3 秒启动
- 急停按钮可立即切断电源

### **控制方式**
1. **手机 App**（Android/iOS）
   - 调整球速、旋转、发射间隔
2. **物理控制面板**
   - 旋钮调节速度
   - 按钮切换模式

### **训练模式**
- **随机模式**：模拟真实对手
- **定点训练**：重复落点练习
- **自定义编程**：通过 Web 界面设置复杂训练方案

## **3. 维护**
- 每周清洁摩擦轮
- 定期检查电池状态
- 固件更新方法：
  ```bash
  pio run -t upload --upload-port /dev/ttyUSB0
