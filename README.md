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
4. [Prompt 測試基準](#4-模型-Prompt-測試基準)  
5. [互動式對話機器人](#5-互動式對話機器人)
6. [進階版互動式對話機器人](#6-進階版互動式對話機器人)
7. [RAG 音樂推薦系統](#7-RAG-音樂推薦系統)
8. [AI Agent (CoT任務)](#8-AI-Agent-(CoT任務))
9. [AI 圖像生成](#9-AI-圖像生成)
10. [Stable Diffusion 插畫生成器](#10-Stable-Diffusion-插畫生成器)
11. [Fooocus Workflow 圖像生成創作](#11-Fooocus-Workflow-圖像生成創作)
12. [健康知識與症狀導引系統](#12-健康知識與症狀導引系統)
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

## 5. 互動式對話機器人

**用途**  
本專案示範如何透過 **Groq API** 建立一個連接大型語言模型 (LLM) 的對話機器人，並提供互動式網站介面，讓使用者能與自訂角色進行對話。  

**特色**  
- 使用 **Groq API** 連接 Llama3 70B 模型。  
- 可讀取並設定 API 金鑰以確保安全存取。  
- 自訂對話機器人角色（此案例為「最Chill的Doggy style」）。  
- 建立簡易網站介面，支援即時對話互動。  

### ⚙️ 環境需求
- Python 3.8+  
- 套件：`requests`、`os`、`matplotlib`、`pandas`  
- Groq API 金鑰  

### 💻 安裝
```bash
pip install requests matplotlib pandas
```

## 6. 進階版互動式對話機器人

**用途**  
本專案示範如何使用 **Ollama** 與 OpenAI API 建立一個進階版對話機器人，支援 **持續對話功能**，可保留上下文訊息，讓回覆更自然流暢。  

**特色**  
- 使用 **Ollama** 安裝與執行本地模型伺服器。  
- 採用 `gemma3:4b` 模型。  
- 支援 **持續對話 (contextual conversation)**，能保留對話歷史。  
- 可於 **Google Colab** 環境執行。  
- 結合 **OpenAI API**，提供混合式聊天體驗。  

### ⚙️ 環境需求
- Python 3.8+  
- 工具：Ollama、Colab  
- 套件：`requests`、`os`、`matplotlib`、`pandas`  

### 💻 安裝與設定
安裝 **Ollama**：  
   ```bash
   curl -fsSL https://ollama.ai/install.sh | sh
   nohup ollama serve &
   ollama pull gemma3:4b
   ```

## 7. RAG 音樂推薦系統

**用途**  
本專案是一套基於 **Spotify 播放清單資料**的音樂推薦系統。  
使用者只需輸入心情描述或偏好條件，系統即可從預先抓取的播放清單資料中檢索並推薦符合情境的歌曲，打造個人化的聆聽體驗。  

**特色**  
- 使用 Spotify API 搜尋並爬取播放清單與歌曲資料。  
- 建立以 **心情關鍵字 + 音樂類型** 為基礎的檢索資料集。  
- 利用 **RAG (Retrieval-Augmented Generation)** 架構，提升推薦的準確性與相關性。  
- 支援多樣化的輸入，例如：  
  - 「放鬆」  
  - 「想提振精神」  
  - 「悲傷的台灣流行歌」  

### 系統架構圖
<img src="7_RAG/rag_Image.png" alt="RAG 架構" width="60%"/>


---

### ⚙️ 環境需求
- Python 3.9+  
- 套件：`spotipy`、`pandas`、`faiss`、`numpy`、`matplotlib`  

### 💻 安裝
```bash
pip install spotipy pandas faiss-cpu numpy matplotlib
```

### ▶️ 使用流程

1. **資料蒐集**  
   - 使用 `misuc_data_crawling.ipynb`，透過 **Spotify API** 搜尋並爬取播放清單與歌曲資訊。  
   - 匯出歌曲資料為 **CSV 檔**，作為後續檢索資料來源。  

2. **建立向量資料庫**  
   - 使用 `RAG_create_database.ipynb`，將歌曲資訊轉換為文本並嵌入向量空間。  
   - 建立 **FAISS 資料庫**，並儲存於 `faiss_db/`，後續查詢會依此檢索。  

3. **查詢與推薦**  
   - 使用 `RAG_query_system.ipynb`，輸入使用者需求（心情或音樂風格）。  
   - 系統會從向量資料庫中找到最相關的歌曲，並輸出推薦清單。  

## 8. AI Agent (CoT任務)

**用途**  
本專案設計了一個基於 **Chain-of-Thought (CoT) 思考流程** 的 AI 任務，模擬「NBA 2024-2025 賽季」總冠軍預測。  
透過兩階段的推理與輸出，讓模型能夠在分析球隊奪冠機率時更具邏輯性與說服力。  

**特色**  
- **system_planner (分析階段)**  
  - 輸入：球隊名稱  
  - 輸出：該隊可能奪冠的 **三個優勢**  
  - 分析面向：球員實力、陣容組合、戰術風格、核心球星狀態、教練策略、季後賽經驗  
  - 注意事項：使用保守語氣，避免假設最新轉會或傷病資訊  
- **system_writer (撰寫階段)**  
  - 從分析階段的三點中挑選最具說服力的一點  
  - 以條列式文字輸出，語氣清晰、具邏輯說服力  
  - 適合用來說服支持其他球隊的球迷  

### ⚙️ 環境需求
- Python 3.9+  
- 套件：`transformers`、`openai`、`langchain`、`pandas`  

### 💻 安裝
```bash
pip install transformers openai langchain pandas
```

### 📊 範例輸出

**輸入：「洛杉磯湖人」**

- **system_planner →**
  - 若核心球員保持健康，進攻火力可持續輸出
  - 陣容深度改善後，替補貢獻更均衡
  - 球隊具備豐富的季後賽經驗與冠軍心態

- **system_writer →**

  - 湖人：如果核心球員保持健康，將是球隊爭奪總冠軍的重要優勢

### 📘 方法說明

- **Chain-of-Thought 兩階段架構**
  - 分析 (planner) → 說服 (writer)
  - 透過分階段推理強化邏輯性，避免單一步驟輸出造成推理缺漏

- **Reflection 機制**
  - 檢視並修正前一輪輸出，使結果更貼近需求與事實


## 9. AI 圖像生成

本部分實作一個基於提示詞的 AI 繪圖任務，主要探索「柔和寫實手繪風格」的生成方式。

### 🎨 生圖使用的風格
**柔和寫實手繪風格**  
結合了手繪插畫、復古童書、柔和水彩、細緻線條和自然比例，創造出一個溫暖且具有細膩表情的插畫風格。  
特點：
- 避免誇張的卡通式五官  
- 帶有紙張紋理質感  
- 保持自然比例與細膩表情  

### 📂 相關檔案
- **9_AI_Image_create.ipynb**：執行 AI 繪圖流程的 Notebook，主要負責提示詞設定與圖像生成。  

## 10. Stable Diffusion 插畫生成器

**用途**  
本專案示範如何使用 **Stable Diffusion** 模型 `gsdf/Counterfeit-V2.5`，進行高品質插畫生成。  
透過多組輸入/輸出圖像比較，展示提示詞 (prompt) 與風格對生成結果的影響。  

**特色**  
- 採用 **Counterfeit V2.5** 模型，適合插畫與二次元風格圖像。  
- 支援輸入提示詞與設定參數，生成符合需求的插畫。  
- 多組生成結果 (輸入/輸出)，便於比較不同 prompt 與設定的影響。  
- 可在 Colab 上快速啟動 Web App，進行互動式繪圖。  

### ⚙️ 環境需求
- Python 3.9+  
- 套件：`diffusers`、`transformers`、`accelerate`、`safetensors`、`gradio`  

### 💻 安裝
```bash
pip install diffusers transformers accelerate safetensors gradio
```

### 🧠 主要參數說明：

| 參數名稱        | 說明 |
|------------------|------|
| `prompt`         | 使用者輸入的主提示詞，建議使用英文 |
| `enhance_text`   | 高品質增強詞，例如：masterpiece、ultra-detailed 等 |
| `negative_text`  | 排除元素的提示詞，避免錯誤結構或低畫質內容 |
| `height/width`   | 輸出影像尺寸，需為 8 的倍數（如：512、768）|
| `steps`          | 推理步數，越多越精緻但花費時間越長 |
| `num_images`     | 一次生成幾張圖片 |
| `seed`           | 可固定隨機種子，以利重現相同結果 |

## 11. Fooocus Workflow 圖像生成創作
**用途**  
本專案紀錄使用 **Fooocus** 進行多種圖像生成實驗，探索不同風格設定、Faceswap、人像生成，以及圖片延展 (Outpaint) 的效果。  

**特色**  
- **風格生成對照實驗**  
  - 預設風格 → 輸出寫實風格的小青蛙舞蹈場景  
  - MK Color Sketchnote 風格 → 插畫化、色彩飽和，帶有漫畫式細節  
- **Faceswap 測試**  
  - 僅丟入圖片 → 生成結果與原圖人物差異大  
  - 加入 prompt 與 Faceswap 功能 → 人物五官與風格更接近原圖  
- **圖片延展 (Outpaint)**  
  - 測試案例：黑色 Mazda RX7  
  - Fooocus 成功延伸背景 (天空、公路、地平線)，保持主體一致性  

### ⚙️ 環境需求
- Fooocus 圖像生成工具  
- GPU 環境 (建議至少 8GB VRAM)  

### ▶️ 使用方式
1. 啟動 Fooocus，選擇模型與風格設定  
2. 輸入文字 Prompt 或上傳圖片  
3. 可選擇功能：  
   - **生成插畫/寫實圖片**  
   - **Faceswap**：提升人像相似度  
   - **Outpaint**：延展圖片背景與場景  

### 📊 實驗結果摘要
- **文字生成**：不同風格下的青蛙插畫對照  
- **Faceswap**：透過 prompt + faceswap，生成更接近原始人物的影像  
- **Outpaint**：成功延展場景並保持主體穩定  

### 📘 使用心得
- Fooocus 在文字生成與 Outpaint 上表現自然，生成結果具延續性  
- Faceswap 能顯著提升人像相似度，但僅靠圖片輸入時結果不穩定  
- 適合用於 **創意嘗試** 與 **風格比較**，上手容易，靈活度高  

## 12. 健康知識與症狀導引系統

**用途**  
本專案建立一套具備 **中文語意理解** 的健康資訊查詢系統，整合 RAG 架構與 2-Stage CoT 推理機制，能夠依據使用者輸入的症狀或健康問題，提供條列式或邏輯化的建議回應。  

**使用模型**  
- **向量嵌入模型**：`intfloat/multilingual-e5-small`  
  - 支援多語言語意理解  
  - 將症狀敘述與知識段落轉為可比對的向量  
- **語言生成模型**：`llama3-70b-8192`  
  - 提供高品質中文生成回應  
  - 支援條列式摘要與推理型回覆  
- **RAG 架構**  
  - 使用 LangChain、FAISS、HuggingFace Embeddings  
  - 提升知識檢索與問答的準確度  

---

### 🎯 專案目標
- 建立一個中文健康知識查詢系統  
- 架設從 **資料擷取 ➜ 文本轉換 ➜ 向量建構 ➜ 問答生成** 的完整流程  
- 支援多樣化回覆模式（條列式、2-Stage CoT 推理）  
- 提升回覆的 **邏輯清晰度** 與 **上下文理解力**  

---

### 🔑 專案重點與流程
1. **資料準備與轉換**  
   - 從 MedlinePlus 等來源自動下載 XML 檔案  
   - 解析並轉為 JSON、TXT 文字檔  
   - 包含部分手動下載的補充資料  

2. **資料嵌入與索引**  
   - 使用 HuggingFace Embeddings 將文本轉換為向量  
   - 透過 **FAISS** 建立向量資料庫  

3. **系統整合與 API 設置**  
   - 引入 **Groq API** 作為語言模型執行核心  
   - 覆蓋預設 proxy 行為，確保回應穩定性  

4. **多樣化 Prompt 模板**  
   - 設計多組 Prompt，支援不同互動邏輯  
   - 例如：引導型對話、條列式摘要、推理型回應  
   - 因自動判斷準確性不足 → 最終改為 **使用者自行切換模式**  

5. **互動介面**  
   - 使用 **Gradio** 打造簡易 UI  
   - 支援輸入症狀描述並選擇回覆模式（條列式 / CoT 推理）  

6. **推理機制**  
   - **2-Stage CoT**：先進行逐步推理，再總結建議  
   - 回覆更具邏輯性與可信度  

---

### ✅ 最終成果
- 建立整合 **健康主題 / 維生素 / 礦物質** 等多來源的向量資料庫  
- 完整實作 **RAG + LLM 問答**，提供自然語言互動  
- 成功導入 **2-Stage CoT** 與 **條列式回應**，滿足多樣查詢需求  
- 具擴充性，可接入更多資料來源，應用於其他領域的語意問答  

---

### ⚙️ 環境需求
- Python 3.10+  
- 套件：`langchain`、`faiss`、`transformers`、`gradio`、`openai`、`pandas`  

### 💻 安裝
```bash
pip install langchain faiss-cpu transformers gradio openai pandas
```