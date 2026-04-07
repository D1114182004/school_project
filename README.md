# 📘 README.md

## 📌 專案名稱

**Adaptive Filter 演算法說明（LMS / NLMS）**

---

## 📖 專案簡介

*本專案說明一種常見的自適應濾波演算法，透過迭代更新權重向量 ĥ(n)，使輸出誤差最小化。*

---

## 🖼️ 附圖內容說明

以下為演算法流程的文字重點整理：

> Initialization: $\hat{h}(0) = zeros(p)$
> Computation: For $n = 0,1,2,\dots$
>
> $\mathbf{x}(n) = [x(n), x(n-1), \dots, x(n-p+1)]^T$
>
> $e(n) = d(n) - \hat{h}^H(n)\mathbf{x}(n)$
>
> $\hat{h}(n+1) = \hat{h}(n) + \frac{\mu e^*(n)\mathbf{x}(n)}{\mathbf{x}^H(n)\mathbf{x}(n)}$

---

## 🧠 核心概念

* **輸入向量**：由當前與過去訊號組成
* **誤差計算**：實際輸出與預測輸出差值
* **權重更新**：依據誤差動態調整

---

## 🔧 使用方法

```bash
# 假設使用 Python
python adaptive_filter.py
```

---

## 📂 專案結構

```
project/
│── README.md
│── adaptive_filter.py
│── data/
```

---

## 📊 公式重點

* 誤差公式：`e(n) = d(n) - h^H(n)x(n)`
* 更新公式：`h(n+1) = h(n) + μ * e*(n)x(n) / (x^H(n)x(n))`

---

## 💡 範例說明

假設：

* 步長 $\mu = 0.01$
* 濾波器長度 $p = 4$

則系統會逐步收斂至最佳解。

---

## ⚠️ 注意事項

* 步長過大可能導致發散
* 步長過小收斂速度慢

---

## 📎 參考資料

* Adaptive Signal Processing
* LMS / NLMS 演算法

---

## 🏷️ 標籤

`Adaptive Filter` `Signal Processing` `LMS` `NLMS`

---

