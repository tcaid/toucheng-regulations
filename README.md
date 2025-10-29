# Toucheng Regulations（頭城鎮地方法規資料庫）

本儲存庫用於管理與公開「頭城鎮公有停車場收費管理自治條例」等地方法規之**版本化全文**、**沿革記錄**與**結構化中繼資料**。

## 目標
- 以 **Git** 追蹤每次修法（2011 制定 → 2019 修正第四條 → 2025 再修正第四條）。
- 提供 **metadata.json** 作為機器可讀的沿革索引，便於 Wikidata / 網站前端引用。
- 提供 **diff\_XXXX\_YYYY.md** 作為民眾可讀的差異摘要（輔助 git diff）。

## 結構
```
toucheng-regulations/
├─ manifest.json
└─ toucheng-parking-ordinance/
   ├─ ordinance_2011.md
   ├─ ordinance_2019.md
   ├─ ordinance_2025.md
   ├─ diff_2011_2019.md
   ├─ diff_2019_2025.md
   └─ metadata.json
```

## 操作建議
1. 在 `ordinance_2011.md`、`ordinance_2019.md`、`ordinance_2025.md` 貼上各版**正式條文全文**（UTF-8 編碼）。
2. 於 `metadata.json` 補齊日期（若僅知年份，可先填 `YYYY-01-01` 並在 `date_note` 註記）。
3. 用 `diff_*.md` 以「條次對照」方式整理第四條的差異（亦可附上 git diff 片段）。
4. 完成後可在 Wikidata 條目使用 `P953: full text available at URL` 指向各 `ordinance_YYYY.md` 檔。

## 授權
除非另有標註，條文全文以其原有公部門公眾授權為準，本儲存庫之整理內容建議採用 CC BY 4.0。
