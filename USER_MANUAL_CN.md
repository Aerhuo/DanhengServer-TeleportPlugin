### **多功能传送插件 (TeleportPlugin) v1.0.0 用户手册**

#### **一、 插件简介**

欢迎使用“多功能传送插件”！这是一个强大的游戏“优化”工具，提供了三种不同的传送和定位指令，让你在游戏中的移动和探索变得前所未有的方便。

本插件包含以下核心功能：
*   **获取当前坐标**: 精准定位你所在的位置。
*   **绝对坐标传送**: 像GM一样，瞬间移动到世界上的任何一个角落。
*   **相对位移传送**: 记录一个空间位移，并将这个位移应用到任何地方，适合应用在复杂场景的传送中。

#### **二、 指令列表速查**

| 指令 | 功能 |
| :--- | :--- |
| **/getpos** | 获取并显示你当前的坐标。 |
| **/tp `<x> <y> <z>`** | 传送到指定的绝对坐标。 |
| **/offsettp `<子命令>`**| 执行复杂的相对位移传送（详情见下文）。 |

#### **三、 详细指令用法**

##### **1. 获取坐标 (`/getpos`)**

当你想知道自己精确的位置时，使用此指令。

*   **功能**: 显示你当前所在位置的X, Y, Z坐标。
*   **用法**:
    ```
    /getpos
    ```
*   **示例**:
    你在游戏中输入 `/getpos`，聊天框会收到类似如下的回复：
    `当前位置: X=152, Y=88, Z=-1234`

##### **2. 绝对坐标传送 (`/tp`)**

当你想直接前往一个已知的坐标点时，使用此指令。

*   **功能**: 将你立即传送到一个指定的世界坐标。
*   **用法**:
    ```
    /tp <X坐标> <Y坐标> <Z坐标>
    ```
*   **示例**:
    输入 `/tp 0 100 0`，你将会被瞬间传送到世界的中心点（X=0, Z=0）上空100米的位置。

##### **3. 相对位移传送 (`/offsettp`)**

这是本插件最强大的功能。它不是让你传送到一个固定的点，而是记录一个“位移”或“偏移量”，然后将这个位移应用到你当前的位置。

**这有什么用？** 想象一下，当你在匹诺康尼的任务中遇到了难以解决的触发问题，面前的大门在完成拼图解谜后才会出现，但我们的DanhengServer还没有修复这个问题，此时你用尽了一切办法想解决这个问题，但仍然没有解决，这时你才会想到有一个可以进行相对位移传送的指令有多好，你不知道你确切地需要传到什么坐标，你只是想穿过那扇没有出现的门，这时使用该指令，模拟一段你朝门方向走路的过程，执行两次set最后执行一次go，然后你就成功地穿过了那扇难以逾越的门！

*   **功能**: 记录、计算并执行一次空间位移传送。
*   **用法**: 此指令包含多个子命令，你需要按顺序使用它们。

    *   `/offsettp set1`
        **记录起点**: 将你当前站立的位置，标记为位移的“坐标点1”。

    *   `/offsettp set2`
        **记录终点**: 将你当前站立的位置，标记为位移的“坐标点2”。

    *   `/offsettp go`
        **执行传送**: 计算从“坐标点1”到“坐标点2”的偏移量，然后将这个偏移量应用到你**当前**的位置，把你传送到最终的目的地。

    *   `/offsettp status`
        **查看状态**: 显示你当前已记录的“坐标点1”和“坐标点2”的信息。

    *   `/offsettp clear`
        **清除记录**: 删除为你保存的所有坐标点，以便开始一次新的记录。

*   **使用场景示例**:
    假设你想穿过一段障碍。

    1.  首先，走到障碍的一旁，输入：
        `/offsettp set1`
        *(系统回复：坐标点1已记录...)*

    2.  然后，走近障碍，输入：
        `/offsettp set2`
        *(系统回复：坐标点2已记录...)*

    3.  现在，你已经成功记录了“从障碍的一旁到障碍位置”的这个精确位移。

    4.  现在是时候逾越这个不可承受之重了。

    5.  输入：
        `/offsettp go`

    6.  **完成！** 你会被瞬间传送到障碍的身后，好耶！

希望这份手册能帮助你更好地解决游戏过程中遇到的BUG！如果你有任何问题或建议，欢迎随时反馈。
