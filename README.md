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
[https://raw.githubusercontent.com/YOUR_GITHUB_NAME/MangoBlock-Arduino-Core/main/package_mangoblock_index.json](https://raw.githubusercontent.com/YOUR_GITHUB_NAME/MangoBlock-Arduino-Core/main/package_mangoblock_index.json)
