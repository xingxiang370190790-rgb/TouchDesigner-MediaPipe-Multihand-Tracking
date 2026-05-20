# MediaPipe TouchDesigner - Multi-Hand Extension

This project is a modified version of the popular MediaPipe plugin for TouchDesigner. A huge thank you to **Torin Blankensmith** and **Dom Scott** for their incredible work on the original creator ecosystem!

---

## 📌 Why This Fork?

While using the original plugin, I noticed that it was limited to tracking and transmitting data for a maximum of 2 hands. After seeing other community members reporting the same issue, I decided to modify the **hand_tracking** module. 

This version successfully unlocks the limitation, allowing you to **detect, process, and output motion data for 3 or more hands simultaneously**.

---

## ⚠️ Current Status & Known Issues

* **Work in Progress:** This project is still being refined.
* **Channel Limitation:** I have heavily tested and verified the **`normalized_data`** output channel, as it was the only channel required for my specific interactive project. Other output channels (such as world coordinates or custom overlays) **have not been fully checked and may contain bugs or unexpected behavior**. 

If you encounter issues with other channels, contributions and Pull Requests are more than welcome!

---

## 💡 Practical Recommendation for Interactive Installations

Although this plugin technically enables multi-hand detection (>2 hands) via a single camera, **I still highly recommend using multiple devices/cameras (with each camera dedicated to tracking only 1-2 hands) for real-world interactive art installations.** **Why?**
1. **Limited FOV:** Standard camera capture areas are usually too small to fit multiple people comfortably.
2. **Occlusion & Misidentification:** When 3 or more hands move in the same frame, hands frequently cross or block each other, which drastically increases the rate of tracking loss and misidentification.

---

## ❤️ Contributing & Feedback

I hope this modification helps you with your multi-user interactive projects! If you find bugs or want to help fix the other output channels, feel free to open an Issue or submit a Pull Request.

Happy programming!


# MediaPipe TouchDesigner - 多手识别扩展版

本项目基于在 TouchDesigner 社区中的 MediaPipe 插件进行修改。在此衷心感谢原作者 **Torin Blankensmith** 和 **Dom Scott** 带来的杰出开源贡献！

---

## 📌 为什么开发这个修改版？

在实际使用原版插件时，我发现它最多只能传输 2 只手的数据。同时，我也在社区中看到其他开发者反馈了相同的问题。因此，我对插件底层的 **hand_tracking** 模块进行针对性的修改。

现在它能够**同时检测、处理并输出 3 只手及以上的运动活动数据**。

---

## ⚠️ 当前状态与已知问题

* **完善进行中：** 本项目目前仍处于不断完善的阶段。
* **通道限制：** 目前我仅对 **`normalized_data`（归一化数据）** 输出通道进行了深度测试和验证，因为我自己的交互项目只需要这一个通道。其他输出通道（如世界坐标 world coordinates 或自定义图层叠加 custom overlays）**尚未经过完整测试，可能存在 Bug 或输出异常**。

如果你在测试其他通道时遇到问题，非常欢迎提交 Issue 或直接提交 Pull Request（PR）来一起完善它！

---

## 💡 交互艺术装置落地建议

虽然该插件在技术上实现了通过单摄像头检测多只手（>2只手）的功能，但**在实际的多人交互艺术装置项目中，我依然建议使用“多台设备/多摄像头组合”的方案（即每台摄像头只专门负责检索 1-2 只手）。** **原因如下：**
1. **视场角（FOV）限制：** 普通摄像头的捕捉范围有限，很难在舒适的距离内同时容纳多个人伸高手臂。
2. **遮挡与误识别：** 当 3 只或更多只手在同一个画面中运动时，手势之间极易发生前后交错和遮挡，这会导致视觉算法频繁丢失追踪或发生身份误判（ID 跳变）。

---

## ❤️ 贡献与反馈

希望这次修改能对你的多人交互项目有所帮助！如果你发现了 Bug，或者愿意帮助修复其他未验证的输出通道，请随时提出 Issue 或提交 Pull Request。
