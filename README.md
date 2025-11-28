# CENG543_Midterm_290201005

# CENG 543 - Midterm Examination
**Student ID:** 290201005

## Project Structure
This repository contains the solution for the Take-Home Midterm. The project is organized by question:

* **`Question1.ipynb`**: Comparison of Bi-LSTM/Bi-GRU with GloVe/BERT embeddings (IMDb).
* **`Question2_3.ipynb`**: Sequence-to-Sequence models (Attention Mechanisms) and Transformer implementation (Multi30k).
* **`Question4.ipynb`**: Retrieval-Augmented Generation (RAG) pipeline (HotpotQA).
* **`Report.pdf`**: The final comprehensive report generated from LaTeX.
* **`outputs/`**: Contains generated plots and visualization figures.

## How to Reproduce Results

1.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    python -m spacy download en_core_web_sm
    python -m spacy download de_core_news_sm
    ```

2.  **Run Notebooks:**
    Each notebook is self-contained. You can open them in Jupyter or Google Colab and run all cells sequentially. Data downloading is handled automatically within the notebooks.

    * *Note for Q3:* The Transformer training includes an ablation study that may take time on CPU. GPU is recommended.

## Key Findings
* **Q1:** Static embeddings (GloVe) with GRUs outperformed fine-tuned BERT on the small IMDb dataset due to overfitting constraints.
* **Q2:** Scaled Dot-Product attention proved superior to Multiplicative attention, validating the importance of the scaling factor.
* **Q3:** Transformers demonstrated high sensitivity to hyperparameters (learning rate) compared to the robust baseline RNNs.
* **Q4:** Dense Retrieval + Instruction-Tuned Generation (FLAN-T5) was identified as the only viable RAG configuration.
