# 1131437_frmBeepPlayer
A C# practice about BeepPlayer.

# 簡易電子琴 (Simple Beep Piano)

## 專案簡介 (Description)
本專案為一個使用 C# Windows Forms 開發的「簡易電子琴」應用程式。
程式透過呼叫系統底層的 Windows API (`kernel32.dll` 中的 `Beep` 函式)，來驅動電腦發出指定頻率的聲音，模擬出 Do、Re、Mi、Fa、Sol、La、Si、Do 八個基本音階。同時，專案實作了視窗動態縮放功能，當使用者調整視窗大小時，內部的琴鍵按鈕會依比例自動縮放，確保良好的使用者體驗。

## 功能特色 (Features)
* **音效播放**：使用 `DllImport` 匯入系統 API，點擊對應按鈕即可發出不同頻率的音階。
* **共用事件處理**：使用單一 Click 事件處理所有琴鍵的發聲邏輯，透過按鈕的 `TabIndex` 屬性來對應頻率陣列。
* **動態 UI 縮放**：監聽表單的 `SizeChanged` 事件，並記錄控制項的初始位置與大小，計算比例以動態調整介面配置。

## 執行說明 (How to Run)
1. 請確認電腦已安裝 .NET Framework 執行環境。
2. 透過 Visual Studio 開啟本專案。
3. 點擊上方的「開始」按鈕（或按 `F5`）編譯並執行應用程式。
4. 程式開啟後，點擊畫面上的音階按鈕即可聽到對應的琴聲。
5. 可嘗試拖曳視窗邊緣改變視窗大小，確認琴鍵大小會隨之動態調整。

## 程式執行截圖 (Screenshot)
<img width="501" height="153" alt="螢幕擷取畫面 2026-05-13 075824" src="https://github.com/user-attachments/assets/9f3c3958-3280-4ab7-9cd7-dbf6967cb311" />
