# 生成式 AI 專案集

這個資料庫收錄了多個與 **生成式 AI** 有關的程式實作與實驗。  
內容涵蓋自然語言處理、影像生成、資料模擬以及互動應用等主題。  
每個專案皆以獨立模組呈現，目標在於：

- 探索生成式模型的核心概念  
- 提供可重現、可實際操作的程式範例  
- 展示生成式 AI 在不同領域的應用可能性  

---

## 目錄 (Table of Contents)

1. [函數圖形繪製](#1-函數圖形繪製)  
2. [DNN 手寫數字辨識](#2-DNN-手寫數字辨識)  
3. [專案 3：xxxx]  
4. [專案 4：xxxx]  
⋮  

---

## 1. 函數圖形繪製

**用途**：  
本專案示範如何利用 Python 視覺化 **Beta 分配** 的機率密度函數，並比較在不同參數條件下的分布形狀。  

**特色**：  
- 使用 `scipy.stats.beta` 建立 Beta 分配的 PDF。  
- 將參數設定為 \(a=b\)，觀察分布的對稱性與集中性。  
- 顯示不同參數下的圖形變化，從均勻分布到集中於 0.5 附近的尖峰分布。  

### 環境需求
- Python 3.8+  
- 套件：`numpy`、`pandas`、`matplotlib`、`seaborn`、`scipy`

### 安裝
```bash
pip install numpy pandas matplotlib seaborn scipy


## 2. DNN 手寫數字辨識

**用途**：  
本專案利用 **深度神經網路 (Deep Neural Network, DNN)** 訓練與測試 MNIST 手寫數字資料集，並提供互動式介面，讓使用者可以即時手寫數字並進行辨識。  

**特色**：  
- 採用 4 層全連接神經網路：  
  - 第一層：256 個神經元  
  - 第二層：128 個神經元  
  - 第三層：64 個神經元  
  - 第四層：32 個神經元  
- 使用 **MNIST 資料集**進行訓練與測試。  
- 提供 **Gradio 互動式介面**，可直接手寫輸入數字並辨識結果。  
- 使用 `TensorFlow/Keras` 架構，程式結構清晰。  

### 環境需求
- Python 3.8+  
- 套件：`tensorflow`、`numpy`、`matplotlib`、`PIL`、`gradio`、`ipywidgets`

### 安裝
```bash
pip install tensorflow numpy matplotlib pillow gradio ipywidgets

