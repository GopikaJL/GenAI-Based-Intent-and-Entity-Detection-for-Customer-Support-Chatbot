# GenAI-Based-Intent-and-Entity-Detection-for-Customer-Support-Chatbot


## **Project Overview**
This repository demonstrates the development of a **Generative AI-based Intent and Entity Detection** model tailored for Schneider Electric's customer support chatbot. The project focuses on utilizing **Meta's LLaMA** and **Gemini AI** as the primary Large Language Models (LLMs) alongside smaller models like fine-tuned BERT and GPT-2. These models enable precise detection of user requests and extraction of relevant entities to enhance chatbot performance. The methodology was focused on advanced prompt engineering for LLMs and fine-tuning for smaller models due to the size of the dataset.


## **Comparative Analysis of Models**
| **MODEL**        | **GEMINI-1.5-FLASH** | **META LLAMA-3.2-13B** | **BERT**               | **GPT-2**            |
|-------------------|----------------------|-------------------------|-------------------------|----------------------|
| **Architecture**  | Multimodal           | Unidirectional Decoder  | Bidirectional Encoder   | Unidirectional Decoder |
| **Token Capacity**| 1 million tokens     | 8,192 tokens            | 512 tokens              | 1024 tokens          |
| **Primary Feature** | Advanced multimodal | Open-source architecture| Bidirectional context   | Autoregressive       |
| **Learning Capabilities** | Reasoning capabilities | Instruction-following capabilities | Transfer learning | Text generation       |




## **Key Objectives**
1. **Intent and Entity Detection:** Design models capable of identifying user intents and relevant entities with high precision.
2. **Zero-Shot and Non-Zero-Shot Learning:** Compare model performance in handling unseen (zero-shot) and trained (non-zero-shot) intents and entities.
3. **Comparative Study of LLMs:** Evaluate and compare Meta's LLaMA and Gemini AI based on performance metrics like accuracy, F1-Score, Recall and Precision.
4. **Training :** Prompt= Engineering and Fine-Tuning.
5. **Documentation:** Present findings through comprehensive documentation and visualizations.



## **Results and Observations**
- **Meta LLaMA** achieved superior accuracy for zero-shot tasks but had higher latency and computational cost.
- **Gemini AI** provided a balanced approach with moderate accuracy and faster inference times, making it suitable for real-time applications.
- **Fine-Tuned BERT and GPT-2** performed well in non-zero-shot scenarios with minimal resource requirements but lacked flexibility for unseen intents.

### Gemini AI Results
| **Intent**           | **Accuracy** | **Recall** | **F1-Score** |
|----------------------|--------------|------------|--------------|
| CatalogSelection     | 0.90         | 0.82       | 0.90         |
| OrderStatus          | 1.00         | 1.00       | 1.00         |
| PriceAndAvailability | 1.00         | 1.00       | 0.92         |
| ProductReplacement   | 0.80         | 0.84       | 0.87         |

### Meta LLaMA Results
| **Intent**           | **Accuracy** | **Recall** | **F1-Score** |
|----------------------|--------------|------------|--------------|
| PriceAndAvailability | 0.91         | 0.92       | 0.85         |
| ProductReplacement   | 0.83         | 0.83       | 0.91         |
| OrderStatus          | 0.92         | 0.93       | 0.93         |
| CatalogSelection     | 0.78         | 0.79       | 0.85         |



### **Visualization Highlights**
- Accuracy comparison across models:
  - LLaMA: 87.5% (zero-shot)
  - Gemini AI: 92% (zero-shot)
  
- Inference time per query:
  - LLaMA: ~800ms
  - Gemini AI: ~400ms
  - Fine-Tuned BERT: ~100ms

---

## **How to Run**

### **Prerequisites**
- Python 3.8+
- Install dependencies using:
  ```bash
  pip install -r requirements.txt
  ```

### **Steps to Run**
1. Clone the repository:
   ```bash
   git clone https://github.com/your-profile/GenAI-Intent-Entity-Detection.git
   cd GenAI-Intent-Entity-Detection
   ```
2. Run Jupyter notebooks:
   - Open `GeminiAI_Prompt.ipynb` for Gemini-specific experiments.
   - Open `final-output.ipynb` for LLaMA vs. Gemini comparative study.
3. For BERT fine-tuning:
   ```bash
   cd models/bert_fine_tuning
   python train_bert.py
   ```

---

## **Future Enhancements**
- Expand to additional LLM platforms like AWS Bedrock or Anthropic Claude.
- Introduce multilingual support for intent and entity detection.
- Optimize deployment pipelines with Docker and FastAPI.




