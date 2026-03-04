# Contributory Rebalancer

每月 DCA 再平衡計算器。輸入持倉市值和本月預算，自動算出該買哪幾檔、各買多少。

- 支援 USD / TWD 雙幣別（0050 台幣輸入，其餘美金）
- 貢獻式再平衡：資金按缺口比例分配給低配標的，超配標的自動跳過
- 目標比例可自訂、標的可排除
- 零依賴單一 HTML 檔，離線可用

## 部署到 GitHub Pages

```bash
# 1. 建立 repo
gh repo create rebalancer --public --clone
cd rebalancer

# 2. 複製 index.html 進去
cp /path/to/index.html .

# 3. 推上去
git add .
git commit -m "init: contributory rebalancer v1.2"
git push origin main

# 4. 開啟 GitHub Pages
#    Settings → Pages → Source: Deploy from a branch → Branch: main / root → Save
#    幾分鐘後就能在 https://<username>.github.io/rebalancer/ 看到
```

## 本地使用

直接用瀏覽器開啟 `index.html` 即可，不需要任何伺服器。

## 更新配置

直接編輯 `index.html` 裡的 `TARGET_ALLOCATION` 陣列即可調整標的和預設目標比例。
