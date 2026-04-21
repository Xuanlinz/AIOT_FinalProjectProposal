### 智慧城市交通安全：基於邊緣運算之智慧疲勞駕駛偵測系統Smart Fatigue Driving Detection System based on Edge AI
## 📌 專案背景
在智慧城市與 AIoT 設備普及的趨勢下，智慧交通與安全駕駛已成為城市治理的核心 。然而，儘管車輛硬體不斷升級，疲勞與分心駕駛仍佔重大交通事故的近 20% 。本專案旨在突破傳統監控設備的技術瓶頸，如：反應延遲： 捨棄雲端傳輸，採用邊緣運算實現毫秒級防護 。環境限制： 解決低光源環境辨識失效問題 。成本壁壘： 透過平價 AIoT 設備，讓一般大眾車款也能享有高階車載 DMs 的安全監控 。
## 🛠️ 技術架構:本系統採用三層架構設計，確保從影像擷取到預警觸發的高效能表現 ：資料蒐集層 (Data Collection)： 利用內建或 USB 鏡頭擷取駕駛面部影像，維持高幀率（High FPS）輸入 。核心模型層 (Single-Model Core)： 採用單階段 YOLOv8-Pose 輕量化網絡，同步進行臉部定位與關鍵點（上下眼瞼、嘴角）座標提取 。智能判定層 (Smart Decision)： 基於時序特徵進行 Rule-based 數學運算，觸發即時警報 。
## 🧠 核心演算法：YOLOv8-Pose + 數學建模我們將複雜的視覺資訊量化為雙重疲勞指標 ：眼睛閉合比 (EAR - Eye Aspect Ratio)： 精準提取上下眼瞼座標，計算眼睛開合程度，排除光影干擾 。打哈欠狀態 (MAR - Mouth Aspect Ratio)： 同步攝取嘴角關鍵點，量化嘴部張合張力 。防誤報機制系統設有嚴格的時序追蹤邏輯，非僅憑單一畫面判定。當 EAR/MAR 連續低於或超過特定閾值（如：連續 1.5 秒）時，才會觸發警報 。
## 📊 系統規格與效能目標硬體平台： PC/Laptop 邊緣運算終端 。訓練資料集： NTHU-DDD (Driver Drowsiness Detection) 。偵測精度目標： $mAP > 85\%$ 。系統特性： 高吞吐量、低延遲、毫秒級預警 。
## 👥 團隊成員 (第五組)朱軒麟 - 電資四 (學號：4111064206) 徐宛禾 - 電資四 (學號：4111064237) 
## 🌟 願景我們致力於落實智慧城市「零傷亡 (Vision Zero)」的全球趨勢，透過技術普及化，讓每一次毫秒級的成功預警，都能守護一個家庭的完整 。
## 📝 參考文獻[1] 江秉穎等 (2022)。《現行國際疲勞駕駛監測科技資料蒐集彙整》。交通部運輸研究所 。
[2] Maleki Varnosfaderani, S., et al. (2025). A Comprehensive Review of Unobtrusive Biosensing in Intelligent Vehicles. Bioengineering (Basel) 。
