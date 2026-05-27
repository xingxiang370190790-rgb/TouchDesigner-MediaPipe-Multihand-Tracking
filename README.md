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



