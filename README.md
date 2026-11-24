# Jodus調節效果互動實驗室

以「外送平台：同樣晚到 10 分鐘，熟客和新客一樣生氣嗎？」為情境的調節效果（moderation）互動教學網頁。60 筆訂單記錄外送延遲、會員身分、每月訂購次數與滿意度，學生可以在散布圖上新增、拖曳、刪除訂單，看兩條迴歸線何時不再平行；也能用滑桿移動調節變數，看簡單斜率即時改變、在 3D 圖中旋轉扭曲的預測面，並學會用階層迴歸與 APA 格式把調節效果寫進論文。

🔗 **線上使用：** https://jodusocnncwiy.github.io/moderation-lab/

## 適用對象

- 研究所多變量分析：調節效果、交互作用單元
- 先備知識：複迴歸，可先使用 [Jodus複迴歸互動實驗室](https://jodusocnncwiy.github.io/multiple-regression-lab/)
- 各頁的「研究所延伸」區塊預設收起，需要時再展開

## 單元內容（8 頁）

| 頁次 | 主題 | 重點 |
|---|---|---|
| 1 | 先猜一猜 | 延遲對會員與非會員的打擊一樣大嗎？兩群人分色、分形狀呈現，猜完再揭曉 |
| 2 | 兩條線 | 名目調節變數：兩組各一條迴歸線，比較斜率差；不分組的線會把差異平均掉 |
| 3 | 交互作用項 | ŷ = b₀ + b₁X + b₂W + b₃XW；代入 W = 0、1 得到兩條線，b₃ 就是斜率差；Δ<i>R</i>² 與階層迴歸第 2 步（*F* = *t*²） |
| 4 | 連續調節 | 每月訂購次數當調節變數：滑桿移動 W 看簡單斜率；−1SD／平均／+1SD 三條線；3D 扭曲平面；名目與連續調節變數的處理方式對照表；研究所延伸：Johnson–Neyman 顯著區間 |
| 5 | 中心化 | 中心化前後對照：b₁、b₂ 意義改變、VIF 下降，b₃ 與它的 *t*、*R*² 不變 |
| 6 | 條件與迷思 | 檢定力模擬（主效果 vs. 交互作用，n = 30～240，可切換效果大小）；調節 vs. 中介；常見迷思（比較兩個 *p* 值、中位數切組、非線性） |
| 7 | 論文怎麼寫 | APA 第七版兩階段階層迴歸表、簡單斜率表、交互作用圖與結果段落（隨資料即時改寫）；找錯練習；控制變數的三步驟排法 |
| 8 | 自我檢測 | 6 題選擇題，作答後立即顯示解析 |

## 操作方式

**散布圖（第 1～4 頁）**

- **點空白處**：新增訂單（第 1～3 頁可先在工具列選「會員／非會員」；第 4 頁的訂購次數取目前滑桿值）
- **拖曳**：移動資料點
- **點兩下**：刪除資料點；第 1～3 頁在觸控裝置可以改用「刪除模式」
- **資料表**（第 1、4 頁）：可以直接修改數字

**連續調節（第 4 頁）**

- **滑桿**：選擇每月訂購次數 W，桃紅色虛線即時顯示這個 W 的簡單斜率
- **平面圖／立體圖**：切換 2D 簡單斜率圖與 3D 扭曲預測面；立體圖可拖曳旋轉，並有斜上方、正面、側面、俯視四種視角

**其他頁面**

- **第 2、3 頁**：顯示不分組的一條線；比較拿掉交互作用項（強迫平行）的模型
- **第 6 頁**：選擇交互作用的真實大小（b₃ = 0.09 或 0.03），按「模擬」重複抽樣 400 次，比較不同樣本數的檢定力
- **第 7 頁**：點表格或段落中的任何數字，可以看到它的出處頁次並一鍵前往；「先猜一猜」在一段結果敘述中找出 4 句寫錯的地方

**預設資料（每頁下方）**：會員／非會員、沒有交互作用（平行）；每月訂購次數、沒有交互作用

**全螢幕**：按 F 鍵或右上角的按鈕。網頁以 16:9 投影畫面設計，會依視窗大小自動縮放；在手機或直式螢幕上會改成上下排列。

## 技術說明

- 單一 HTML 檔（`index.html`），使用原生 JavaScript 與 SVG，不需要安裝或建置；3D 圖以 SVG 自行投影繪製，不使用外部 3D 函式庫
- 外部資源：Google Fonts（Noto Sans TC）、KaTeX（公式排版，透過 CDN 載入）
- 所有統計量都在瀏覽器端即時計算，包括迴歸係數、標準誤、*t*、*p*、信賴區間、Δ*R*² 與 *F* 改變量、簡單斜率與其標準誤、Johnson–Neyman 分界點、中心化前後的 VIF；檢定力以固定亂數種子的蒙地卡羅模擬計算
- 離線使用：下載 `index.html` 後用瀏覽器開啟即可；沒有網路時，字型與公式排版會改用系統預設

## 資料說明

外送平台 60 筆訂單的外送延遲、會員身分、每月訂購次數與滿意度為**教學用虛構資料，僅供課堂示範**；「熟客對延遲比較寬容」為教學設定。資料以固定亂數種子產生，每次開啟都相同。

## 參考文獻

Aiken, L. S., & West, S. G. (1991). *Multiple regression: Testing and interpreting interactions*. Sage.

American Psychological Association. (2020). *Publication manual of the American Psychological Association* (7th ed.). https://doi.org/10.1037/0000165-000

Baranger, D. A. A., Finsaas, M. C., Goldstein, B. L., Vize, C. E., Lynam, D. R., & Olino, T. M. (2023). Tutorial: Power analyses for interaction effects in cross-sectional regressions. *Advances in Methods and Practices in Psychological Science, 6*(3), 1–13. https://doi.org/10.1177/25152459231187531

Bauer, D. J., & Curran, P. J. (2005). Probing interactions in fixed and multilevel regression: Inferential and graphical techniques. *Multivariate Behavioral Research, 40*(3), 373–400. https://doi.org/10.1207/s15327906mbr4003_5

Castillo, A., Miller, J. D., Vize, C., Baranger, D. A. A., & Lynam, D. R. (2026). When do interaction/moderation effects stabilize in linear regression? *Advances in Methods and Practices in Psychological Science, 9*(1), 1–14. https://doi.org/10.1177/25152459251407860

Finsaas, M. C., & Goldstein, B. L. (2021). Do simple slopes follow-up tests lead us astray? Advancements in the visualization and reporting of interactions. *Psychological Methods, 26*(1), 38–60. https://doi.org/10.1037/met0000266

Hayes, A. F. (2022). *Introduction to mediation, moderation, and conditional process analysis: A regression-based approach* (3rd ed.). Guilford Press.

MacCallum, R. C., Zhang, S., Preacher, K. J., & Rucker, D. D. (2002). On the practice of dichotomization of quantitative variables. *Psychological Methods, 7*(1), 19–40. https://doi.org/10.1037/1082-989X.7.1.19

Simonsohn, U. (2024). Interacting with curves: How to validly test and probe interactions in the real (nonlinear) world. *Advances in Methods and Practices in Psychological Science, 7*(1), 1–22. https://doi.org/10.1177/25152459231207787

## 版本紀錄

- **v03**：首次上線（8 頁）

## 製作

Jodus｜Jodus 互動實驗室系列
