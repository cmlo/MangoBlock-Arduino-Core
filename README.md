<img width="400" height="400" alt="logo" src="https://github.com/user-attachments/assets/acf6da42-8a64-4222-8289-2c37ed5d893c" />

# MangoBlock X4-RP2350B Arduino 開發板安裝指南

歡迎使用 **MangoBlock X4-RP2350B**！這是一塊專為 **Spatial-AI FPV System** 與新世代科技教育設計的強大機器人主板。

透過本安裝包，您與學生將能在 Arduino IDE 中體驗到「一鍵就緒」的極致開發環境。**無需另外下載任何繁瑣的感測器或螢幕函式庫**，安裝完畢後，所有硬體驅動與教學範例都會自動內建於您的 IDE 中！

---

## ✨ 硬體特色
- **核心算力**：Raspberry Pi RP2350B 雙核心微控制器 (預設時脈 150MHz)
- **超大儲存**：16MB Flash 記憶體 (支援分割儲存空間)
- **全端控制**：板載 4 組直流馬達與編碼器介面、專屬總線舵機 (UART1) 連接埠
- **空間感知**：內建 I2C 介面支援 6 軸 IMU 姿態解算
- **物聯網整合**：預留 RM2 Wi-Fi/BLE 模組腳位
- **視覺回饋**：內建 TFT 顯示器高速 SPI 腳位與 WS2812B 全彩光效

---

## 🚀 3 分鐘快速安裝步驟

### 步驟一：新增開發板網址
1. 打開 **Arduino IDE 2.x**。
2. 點擊左上角選單：`檔案 (File)` ➔ `偏好設定 (Preferences)`。
3. 在視窗下方的 **「額外的開發板管理員網址 (Additional boards manager URLs)」** 欄位中，將以下兩行網址**完整複製並貼上**（若原本已有其他網址，請用逗號 `,` 或換行隔開）：

```text
[https://github.com/earlephilhower/arduino-pico/releases/download/global/package_rp2040_index.json](https://github.com/earlephilhower/arduino-pico/releases/download/global/package_rp2040_index.json),
[https://raw.githubusercontent.com/cmlo/MangoBlock-Arduino-Core/main/package_mangoblock_index.json](https://raw.githubusercontent.com/cmlo/MangoBlock-Arduino-Core/main/package_mangoblock_index.json)
```

(圖例：建議在此處放一張 IDE 偏好設定貼上網址的截圖)

### 步驟二：安裝底層核心與 MangoBlock 套件
點擊 IDE 左側邊欄的 「開發板管理員 (Boards Manager)」 圖示。

在搜尋框中輸入 rp2040。

找到由 Earle F. Philhower, III 提供的 Raspberry Pi Pico/RP2040，點擊 「安裝」。（檔案較大，請耐心等待下載完成）

接著，在搜尋框中改輸入 MangoBlock。

找到 MangoBlock Boards，點擊 「安裝」。

(圖例：建議在此處放一張搜尋 MangoBlock 並點擊安裝的截圖)

### 步驟三：選擇開發板
點擊 IDE 上方的開發板選擇下拉選單，選擇 選擇其他開發板與連接埠 (Select other board and port)。

搜尋並選擇 MangoBlock X4-RP2350B。

將開發板接上電腦的 USB，勾選對應的 COM Port。

🎉 恭喜！您已經完成所有設定！

📚 內建函式庫與教學範例
本套件已將 MangoBlock 專屬函式庫與底層繪圖/燈光依賴套件完美打包。學生只需在程式碼第一行輸入：

C++
#include <MangoBlock.h>
即可透過 Mango.begin(); 喚醒所有硬體。

如何開啟教學範例？
請點擊選單：檔案 (File) ➔ 範例 (Examples)，往下捲動找到 MangoBlock，裡面已依據課程難度為您準備好一系列的教學講義碼：

01.Basics: 基礎燈光與按鈕控制

02.Motor_Control: 帶有編碼器計數的馬達巡線基礎

03.Display: TFT 螢幕繪製與文字顯示

04.MangoBlock_System: 整合姿態感測與 Wi-Fi 的進階機器人應用

🛠 常見問題 (FAQ)
Q: 按下上傳時，需要手動按板子上的按鈕嗎？
A: 不需要！本套件已支援 USB 自動重置燒錄功能，只要在 IDE 點擊「上傳」，板子會自動進入燒錄模式並重新啟動。

Q: 編譯時出現 Adafruit_GFX.h 找不到的錯誤？
A: 本套件已經內建所需依賴。若發生此錯誤，請檢查是否選錯了開發板型號，請確保選擇的是 MangoBlock X4-RP2350B。
