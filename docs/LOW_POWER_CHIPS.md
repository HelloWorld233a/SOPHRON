# 自動開啟低效能模式嘅處理器清單 · Chips that start in low-power mode

SOPHRON 喺 Android 開啟時會讀取部機嘅處理器名稱，如果屬於以下任何一類，低效能模式就會預設開啟。
呢個只係**起始值**：你喺首次設定或者書枱設定入面自己揀過之後，就以你揀嘅為準。

**原則：**

- 2019 年或以前推出嘅處理器全部計入（包括當年嘅旗艦）；
- 中低階處理器計到 2021 年；
- 入門系列（Snapdragon 4／6、Helio A／P／G、Unisoc 等）任何年份都計入；
- **換咗名嘅「馬甲」晶片（新名、舊矽片）一律當舊晶片計**。系統有時俾型號（MT6833），有時俾市場名（Dimensity 6020），所以兩種寫法都認。

另外兩個條件都會令佢自動開：

- Android 版本低過 10；
- 處理器唔喺清單入面，但部機明顯細：記憶體 3 GB 或以下，或者最快嘅核心慢過 1.9 GHz，或者只有 4 個核心或以下。


## Qualcomm

| 系列 Family | 型號 Chips |
| --- | --- |
| Snapdragon 2xx | 200, 205, 208, 210, 212, 215 (MSM8909, MSM8905, QM215) |
| Snapdragon 4 series | 400, 410, 412, 415, 425, 427, 429, 430, 435, 439, 450, 460, 480, 480+, 4 Gen 1, 4 Gen 2, 4s Gen 2 (MSM8916/8917/8920/8929/8937/8940, SDM429/439/450, SM4250, SM4350, SM4375, SM4450, SM4635) |
| Snapdragon 6 series | 610, 615, 616, 617, 625, 626, 630, 632, 636, 650, 652, 653, 660, 662, 665, 670, 675, 678, 680, 685, 690, 695, 6 Gen 1, 6s Gen 3 (MSM8939/8952/8953/8956/8976, SDM630/632/636/660/670, SM6115, SM6125, SM6150, SM6225, SM6350, SM6375, SM6450) |
| Snapdragon platforms (board code names) of the 4 and 6 series | trinket (665), bengal (460/662), khaje (680/685), holi (480/695), blair (695/4 Gen 1), parrot (6 Gen 1/4 Gen 2), talos (675) |
| Old Snapdragon 8 series and earlier | S4, 600, 800, 801, 805, 808, 810, 820, 821, 835 (MSM8960/8974/8084/8992/8994/8996/8998, APQ8064/8084/8096) |
| Snapdragon 7 series up to 2021 | 710, 712, 720G, 730, 730G, 732G, 750G, 765, 765G, 768G, 778G, 778G+, 780G, 782G (SDM710, SDM712, SM7125, SM7150, SM7225, SM7250, SM7325, SM7350; platforms atoll, lito, yupik) |
| Snapdragon names of the renamed chips (when the system gives the marketing name) | 680 / 685 (SM6225), 695 = 6s Gen 3 (SM6375, Qualcomm confirmed), 480+ / 4 Gen 1 (SM4375), 6 Gen 1, 4 Gen 2 / 4s Gen 2, 778G / 778G+ / 782G (one SM7325 family; the 782G only clocks higher) |
| Snapdragon 8 series of 2018–2019 | 845, 850 (SDM845, SDM850), 855, 855+, 860 (SM8150; platform msmnile) |

## MediaTek

| 系列 Family | 型號 Chips |
| --- | --- |
| Older phone chips (MT65xx, MT67xx up to Helio P25) | MT6580, MT6582, MT6592, MT6735, MT6737, MT6738, MT6739, MT6750, MT6752, MT6753, MT6755 (P10), MT6757 (P20/P25), MT6795, MT6797 (X20–X27) |
| Helio A, P and G (entry level) | A20/A22/A25 (MT6761/MT6762), P22/P35, G25/G35/G36/G37 (MT6762/MT6765), P23/P30 (MT6763), P60/P70 (MT6771), P65, G70/G80/G85/G88 (MT6768/MT6769) |
| Tablet chips (MT81xx, MT83xx, MT87xx) | MT8121, MT8127, MT8135, MT8151, MT8161, MT8163, MT8165, MT8166, MT8167, MT8168, MT8173, MT8175, MT8176, MT8183 (Kompanio 500), MT8321, MT8382, MT8735, MT8765, MT8766, MT8768, MT8783, MT8786, MT8788 |
| Helio X30, P90, G90, G95 and G96 (up to 2021) | X30 (MT6799), P90 (MT6779), G90, G90T, G95 (MT6785), G96 (MT6781) |
| Dimensity mid-range of 2020–2021, and the chips renamed from them | 700 / 810 = 6080 (MT6833; 6020 is the 7 nm 700 under a new name), 6100+ / 6300 (MT6835, 6 nm), 720 / 800U (MT6853), 930 = 7020 (MT6855), 800 (MT6873), 820 (MT6875), 900 / 920 / 1080 = 7050 (MT6877). Left out on purpose: 8020 (= 1100, a 2021 upper-mid chip) |
| Dimensity names of the renamed chips (when the system gives the marketing name, not the model number) | Dimensity 700, 720, 800, 800U, 810, 820, 900, 920, 930, 1080, 6020, 6080, 6100+, 6300, 7020, 7050 (also written D6020 …) |

## Unisoc (Spreadtrum)

| 系列 Family | 型號 Chips |
| --- | --- |
| SC series and Tiger T3xx / T6xx | SC7731E, SC9832E, SC9850, SC9863A, T310, T606, T610, T612, T615, T616, T618, T619, T620, T700, T710, T740, T760, T770; renamed: T7200 = T606, T7225 = T612, T7250 = T615, T7255 = T616, T7280 = T620 (also reported as sp9863a, ums312, ums512, ums9230) |

## Samsung

| 系列 Family | 型號 Chips |
| --- | --- |
| Exynos 5, 7 and older 8 / 9 series | 5410–5433, 7420, 7570, 7580, 7870, 7872, 7880, 7884, 7885, 7904, 850, 8890, 8895, 9609, 9610, 9611 (also s5e3830, universal7870…) |
| Exynos 9 series of 2018–2019, and mid-range of 2019–2020 | 9810, 9820, 9825, 880, 980 |

## HiSilicon

| 系列 Family | 型號 Chips |
| --- | --- |
| Kirin 6xx, 710 and old 9xx | 620, 650, 655, 658, 659, 710, 710A, 710F, 910, 920, 925, 930, 935, 950, 955, 960 (hi6210, hi6220, hi6250, hi6260, hi3630, hi3635, hi3650, hi3660) |
| Kirin 810, 820 and 970–990 (2017–2020) | 810, 820, 820E, 970, 980, 990, 990 5G, 990E (hi6280, hi3670, hi3680, hi3690) |

## Rockchip

| 系列 Family | 型號 Chips |
| --- | --- |
| All tablet chips before RK3588 | RK3026, RK3066, RK3126, RK3128, RK3188, RK3228, RK3288, RK3326, RK3328, RK3368, RK3399, RK3562, RK3566, RK3568, PX30 |

## Allwinner

| 系列 Family | 型號 Chips |
| --- | --- |
| A series | A13, A23, A33, A50, A64, A83T, A100, A133, A523 (sun8i, sun50i…) |

## Amlogic

| 系列 Family | 型號 Chips |
| --- | --- |
| S and A series | S805, S905 (all), S912, S922, A311D |

## 馬甲對照（上網核實過） · Renamed chips, checked online

| 新名 | 實際係 | 可信度 |
| --- | --- | --- |
| 天璣 6080 | 天璣 810（MT6833，只係相機支援較高） | 多個來源一致 |
| 天璣 6020 | 天璣 700 嗰類 7nm 晶片 | 來源冇明確講係換名，只確認同為 7nm；你指出係馬甲，已計入 |
| 天璣 6100+、6300 | 6100+ 被報道係天璣 700 嘅小改款（MT6835，6nm）；6300（MT6835T）同 6080 好似 | 只有一個明確來源，6300 嘅說法來自評論，唔算權威 |
| 天璣 7020 | 天璣 930（MT6855，6nm） | 多個來源一致 |
| 天璣 7050 | 天璣 1080（MT6877） | 來源描述為換名 |
| 天璣 8020 | 天璣 1100（2021 中高階） | 一個對照表；**我刻意冇計入**，因為 1100 唔算低端 |
| 天璣 7030 | 天璣 1050（2022） | 一個來源；冇計入 |
| Helio G35 | Helio P35（MT6765） | 多個來源一致 |
| 驍龍 6s Gen 3 | 驍龍 695（SM6375-AC） | **高通自己確認** |
| 驍龍 782G | 驍龍 778G+（同屬 SM7325，頻率較高 2.7GHz） | 同一代晶片，唔係完全相同 |
| 展訊 T7200／T7225／T7250／T7255／T7280 | T606／T612／T615／T616／T620 | 規格資料庫列出；未見 Unisoc 官方說明 |
| Kirin 710F | Kirin 710（只係封裝唔同） | Notebookcheck；710A 係另一個製程（14nm），計入但唔係純換名 |

**核實後我改正咗嘅錯誤：** 之前我寫「驍龍 4 Gen 1 係 680 嘅馬甲」，來源顯示 4 Gen 1 係 480+ 嘅後繼（亦有一個來源話佢係 695 嘅換名，互相矛盾），已經拎走呢個說法（4 Gen 1 照樣計入低端）；「6 Gen 1 係馬甲」亦唔啱（佢係 695 嘅後繼，唔係換名）；「Exynos 1330 係 1280 嘅馬甲」搜尋後發覺唔成立（1330 係另一粒 5nm 晶片），所以冇計入。

**未能核實：** Helio G80／G70 同 MT6769 嘅關係、天璣 810 嘅確切型號（MT6833P 定 MT6833V）、Kirin 820E／810 有冇換名，搜尋冇答案。

## 唔會自動開嘅例子 · Not on the list

2021 年之後嘅中高階處理器，以及 2020 年之後嘅旗艦：Snapdragon 865／888 或以上、7 Gen 1 或以上、8 Gen 系列；MediaTek Helio G99（2022）、天璣 1000 系列（1100、1200、1300 等）、7200、8000 系列、9000 系列；Exynos 990、1280／1330／1380、2100／2200；Kirin 985、9000 系列；Rockchip RK3588；Google Tensor。
呢啲機一樣可以手動開低效能模式。

## 資料來源 · Sources

- [Notebookcheck：Dimensity 6080](https://www.notebookcheck.net/MediaTek-Dimensity-6080-Processor-Benchmarks-and-Specs.825250.0.html)、[6300](https://www.notebookcheck.net/Mediatek-Dimensity-6300-Processor-Benchmarks-and-Specs.900284.0.html)、[6020](https://www.notebookcheck.net/MediaTek-Dimensity-6020-Processor-Benchmarks-and-Specs.743863.0.html)
- [TechWiser：MediaTek 命名方式](https://techwiser.com/mediatek-processor-naming-scheme-explained/)
- [Unbox.ph：新 MediaTek 晶片係舊款換名](https://unbox.ph/editorials/some-new-mediatek-chips-are-renamed-versions-of-old-models/)
- [Notebookcheck：Dimensity 7020 對 Helio G99／7050／1080](https://www.notebookcheck.net/Dimensity-7020-vs-Helio-G99-vs-Dimensity-7050_15104_14649_15080.247596.0.html)
- [Beebom：驍龍 6s Gen 3 係換名嘅 695](https://beebom.com/snapdragon-6s-gen-3-launched-rebranded-snapdragon-695)
- [GSMArena：高通承認 6s Gen 3 係 695 嘅加強版](https://m.gsmarena.com/newscomm-63308.php)
- [TechInsights：驍龍 6 Gen 1](https://www.techinsights.com/ja/node/49260)
- [GSMArena：驍龍 782G 取代 778G+](https://m.gsmarena.com/snapdragon_782g_is_here_as_a_sd778g_replacement-news-56620.php)
- [Notebookcheck：Unisoc T606／T612／T610 對照](https://www.notebookcheck.net/T606-vs-T612-vs-T610_14018_14386_14014.247596.0.html)
- [Notebookcheck：Unisoc T7280／T620](https://www.notebookcheck.net/UNISOC-T7280-T620-Processor-Benchmarks-and-Specs.930518.0.html)
- [Beebom：Helio G35 係換名嘅 P35](https://beebom.com/mediatek-helio-g35-essentially-seems-rebadged-helio-p35)
- [Notebookcheck：Kirin 710A 對 710](https://www.notebookcheck.net/Kirin-710A-vs-Kirin-710_12945_10172.247596.0.html)
- [Notebookcheck：Exynos 1330](https://www.notebookcheck.net/Samsung-Exynos-1330-Processor-Benchmarks-and-Specs.945355.0.html)

註：搜尋結果大部分係發燒友網站同規格資料庫，唔係晶片廠商文件，所以「可信度」欄只供參考。
