# Microprocessor Final Project

### 組長: 陳帛愛
### 組員: 郭沛蓉、黃友枚、孫以瑭

# 平交道模擬系統專題動機
### 專題動機
- 組員在搭火車回家路上討論專題主題，靈機一動提出可以做平交道模擬系統，經組員們討論後，發現課堂上學過的知識都可以應用在這個系統上，所以決定實作此系統作為期末專題內容。

### 系統功能與原理說明
- 系統功能: 模擬平交道系統，火車經過時護欄關閉，火車離開後護欄打開
- 原理說明: 利用紅外線，偵測火車是否已經離開，並搭配LED和timer計時並以七段顯示器顯示
- 利用UART顯示平交道系統狀態

### 系統使用環境及對象
- 系統使用環境: MPLAB v5.20
- 語言: C
- 編譯器: XC8 v2.40
- 燒錄器: pickit4
- 晶片: PIC18F4520

### 系統完整架構圖、流程圖、電路圖、設計
- 系統完整架構圖
<img width="725" alt="Screenshot 2024-01-07 at 1 51 54 AM" src="https://github.com/Esther2002-soon/FinalProject_Microprocessor/assets/106828044/388dcf71-c4e6-4918-8b2a-e97ed51d99f7">

- 流程圖
<img width="812" alt="Screenshot 2024-01-07 at 2 11 47 AM" src="https://github.com/Esther2002-soon/FinalProject_Microprocessor/assets/106828044/5b9c9370-7a23-4e0c-baf5-8d29534068a1">

- 電路圖

- 設計
1. 通知火車即將抵達：按按鈕後倒數5秒，5秒後火車經過
2. 模擬平交道的安全護欄放下：利用伺服馬達控制
3. 警示燈於欄杆放下期間閃爍，放下後恆亮燈：利用 LED 燈控制
4. 感測火車，待火車通過後護欄升起：利用紅外線及超音波感測器
5. 紅綠燈：利用 timer 的設定切換，並透過七段顯示器顯示紅綠燈秒數
6. 緊急按鈕：利用 interrupt 放下護欄並亮起特殊燈況告知

### 系統開發工具、材料及技術
- 開發工具、材料: 
    - PIC18F4520
    - PICKIT 4
    - 紅外線障蔽傳感器 MH-B
    - 七段顯示器 C-583Q-12 BVN-7572SR4
    - button
    - LED
    - server motor
    - UART

- 系統開發技術
    - 單元項目
        - interrupt
        - timer
        - UART
        - server motor
        - seven segment display
    - 進階項目 
        - 紅外線障蔽傳感器

<!-- ### 周邊接口或Library 及API使用說明 -->
