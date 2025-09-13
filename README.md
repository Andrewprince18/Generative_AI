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
3. [GAN 基礎實作](#3-GAN-基礎實作)  
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
```

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
```

## 3. GAN 基礎實作

**用途**  
本專案示範 **生成對抗網路 (Generative Adversarial Network, GAN)** 的基本原理與簡單實作，說明生成器與判別器如何透過對抗訓練學習模擬真實資料分布。  

**特色**  
- 使用 PyTorch 建立簡單的 **生成器 (Generator)** 與 **判別器 (Discriminator)**。  
- 目標資料：一維常態分布 \(N(2, 0.5^2)\)。  
- 展示 **GAN 對抗損失函數**的數學推導。  
- 訓練過程以圖表顯示分布的收斂情況。  

### ⚙️ 環境需求
- Python 3.8+  
- 套件：`torch`、`numpy`、`matplotlib`、`seaborn`  

### 💻 安裝
```bash
pip install torch numpy matplotlib seaborn
```

## 4. 模型 Prompt 測試基準

**用途**  
本專案進行 **跨模型基準測試**，比較不同大型語言模型 (LLM) 在相同主題與相同 Prompt 條件下的表現，觀察其在知識準確度、邏輯性與表達清晰度的差異。  

**特色**  
- 測試主題：**超現實主義 (Surrealism)**。  
- 參與模型：  
  - ChatGPT  
  - Llama 3.3 70B Specdec (Groq)  
- 設計多個基準問題 (Q1 ~ Q4)，涵蓋：  
  - 超現實主義的概念與解釋  
  - André Breton 的理論語錄  
  - 超現實主義與現實世界的關聯  
  - 如何詮釋與理解藝術作品中的象徵  

### ⚙️ 環境需求
- Python 3.8+  
- Jupyter Notebook  

### 💻 安裝
(無額外套件需求，僅需具備 Notebook 環境)  
