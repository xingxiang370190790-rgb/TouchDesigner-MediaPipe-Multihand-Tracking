<details open>
<summary><b>🌐 Click to collapse / expand English Version (点击收起/展开英文版)</b></summary>
<br>

# MediaPipe TouchDesigner - Multi-Hand Recognition Extension

This project is modified based on [MediaPipe in the TouchDesigner community](https://github.com/torinmb/mediapipe-touchdesigner). Thanks to the original authors for their plugin development!

To use this modified version, you can download the compressed package from the Release. The folder contains the plugin file in `.tox`, as well as a project demonstration file.(`.toe`)

The plugin I provide can **recognize and output the dynamic data of up to 4 hands**. The later text shows how I modified and the reasons why I only made the upper limit 4 hands, but if needed, you can continue to **increase the number of recognized hands through the steps** provided later.

Other usage methods are consistent with the original project.

The project demonstration file is also provided by the original plugin authors. I have only made certain modifications to the hand gesture recognition part of the plugin!

---

## 1. Development Purpose

When using the original plugin, I found that it could only transmit data for **a maximum of 2 hands**. Even if the option to recognize more hands was turned on, it could not output the results correctly.
【Picture】
Therefore, I made a brief modification to the hand recognition part.

---

## 2. Effect Demonstration
【Video】

---

## 3. Modification Steps

In this section, I will describe my modification method. If you need data for more than 4 hands, you can refer to the steps:

1. In the MediaPipe options settings, change the "Maximum number of recognized hands" to the number you want.
【Picture】

2. After entering the MediaPipe module, select the part boxed in the picture, then copy and paste it.
【Picture】

3. Enter the selected module and confirm whether the following content corresponds to the number.
【Picture】

---

## 4. Usage Recommendations

⚠️ Although the plugin can technically achieve the recognition of more hands, in actual interactive projects, because the **capture range of the camera** is limited, hands are prone to cross-occlusion within the designated range, leading to **target loss**. Moreover, MediaPipe **limits the input pixel** value of the camera, and when the pixels occupied by the hand are too low, MediaPipe will **choose not to recognize it**. 

Therefore, it is **very difficult to capture 5 or more hands in the frame.**

If your project requires the recognition of more hands, in my personal idea, increasing the number of camera devices might be a more feasible solution.

---

## Acknowledgments... Acknowledgments I guess (?)

I have currently only modified the hand recognition part, and I have only verified whether the output of normalized_data and the gesture part is correct. However, I think the modification methods for other modules should be very similar? If there are related needs in the future, maybe I will modify them again.

If you find a bug, or are willing to help fix other unverified output channels, please raise an issue directly! 

Thank you very much!

</details>

<br>
<hr>
<br>

<details>
<summary><b>🌐 点击展开 / 收起 简体中文版本 (Click to expand / collapse Chinese Version)</b></summary>
<br>

# MediaPipe TouchDesigner - 多手识别扩展版

本项目基于[在 TouchDesigner 社区中的 MediaPipe ](https://github.com/torinmb/mediapipe-touchdesigner)进行修改。感谢原作者们的插件开发！

要使用这个修改后的版本，您可以直接下载Release中的压缩包并解压，文件夹中含有'.tox'格式的插件文件，以及一个工程示意文件。

我提供的插件 **最多可以识别并输出4只手的动态数据** ，后文提供了我修改的具体步骤和我只做了上限为4只手识别的原因，但如果需要，你可以继续通过后文中提供的方法，提高手的识别数量。

其他使用方法与原项目一致。

工程示意文件同样为插件原作者提供，我只对插件的手势识别部分进行了一定修改！

---

## 1.开发目的

在使用原版插件时，我发现它最多只能传输 2 只手的数据，即使打开识别更多手的选项，也无法正确输出结果。

【图片】

因此我对手识别的部分进行了简要的修改

---

## 2.效果演示

【视频】

---

## 3.修改步骤

在本段，我将叙述我的修改方式，如果你需要4只手以上的数据，可以参考步骤：

1.在MediaPipe的选项设置，更改“最大识别手的数量”至你想要的数量

【图片】

2.点入MediaPipe的模块后，选择图中框出的部分，复制粘贴

【图片】

3.点入选中的模块，确认以下内容是否与数字对应

【图片】

---

## 4.使用建议

 ⚠️尽管插件在技术上能够实现更多手的识别，但是在实际的交互项目中，由于摄像头的捕捉范围有限，手在指定范围内容易发发生交错遮挡，导致目标丢失，且MediaPipe限制了摄像头输入的像素值，而当手占的像素过低时MediaPipe不会选择识别，因此，画面里很难捕捉到5个及以上数量的手。
  
 如果你的项目需要对更多的手的识别，我认为**增加摄像头设备数量**也许是更具可行性的方案。

---

## 致谢...致谢吗（？）

我目前仅修改了手部识别的部分，也只检验了normalized_data和手势部分的输出是否正确，但是我认为其他模块的修改方式应该非常相似？如果未来有相关需求，也许我会再改一下。
  
如果你发现了 Bug，或者愿意帮助修复其他未验证的输出通道，请直接提issue！非常感谢！

</details>
