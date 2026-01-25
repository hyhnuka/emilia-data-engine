
# EMILIA Data Engine 

**EMILIA (Emotional Intelligence & Mental Health Innovative AI Solution)** adalah teknologi AI yang dirancang untuk memahami kompleksitas emosi manusia serta mendukung penanganan masalah kesehatan mental melalui pendekatan berbasis teknologi.

Repository ini berisi **Data-Centric Development Pipeline** yang digunakan untuk mengembangkan, mengevaluasi, dan menguji kualitas dataset EMILIA.

## Dataset Information
Dataset yang digunakan adalah dataset Q&A sintetis bertema psikologi yang digenerate dengan model GROK3 dan GPT dengan panduan dokumen psikologi.
* **Dataset Name:** [Emilia-Indonesian-Psychology-QnA-7K](https://huggingface.co/datasets/hnuka/Emilia-Indonesian-Psychology-QnA-7K)
* **Size:** ~7,500 Question-Answer pairs.
* **Sources:** Diolah dari 18 dokumen psikologi.
* **Generation:** Menggunakan LLMs (GROK-3 & ChatGPT) dengan teknik *Prompt Engineering*.

---

## Repository Structure

Proyek ini dibagi menjadi dua bagian utama: Analisis Konten dan Evaluasi Kualitas.

### 1. Analysis (`/Analysis`)
Berfokus pada pemahaman distribusi data dan topik untuk memastikan keberagaman konten.
* **`BERTopic.ipynb`**: Implementasi *Topic Modeling* menggunakan BERTopic untuk memetakan klaster diskusi psikologi dalam dataset, memastikan cakupan materi yang luas (dari kecemasan, hubungan, hingga pengembangan diri).

### 2. Evaluation (`/Evaluation`)
Menggunakan pendekatan *LLM-as-a-Judge* dan inferensi bahasa alami untuk menjamin validitas data.
* **`NLI.ipynb`**: Menggunakan *Natural Language Inference* untuk mengecek konsistensi logika antara konteks dokumen sumber dengan jawaban yang dihasilkan (Entailment vs Contradiction).
* **`coba-prometheus2-answer-relevance.ipynb`**: Evaluasi menggunakan model **Prometheus 2** untuk mengukur seberapa relevan jawaban AI terhadap instruksi/pertanyaan pengguna.
* **`coba-prometheus2-hallucination.ipynb`**: Deteksi halusinasi menggunakan **Prometheus 2** dengan membandingkan jawaban terhadap referensi dokumen sumber untuk memastikan fakta yang akurat.

---





**Apakah kamu ingin saya bantu membuat "Score Rubric" khusus untuk evaluasi Prometheus di README-nya?** (Ini biasanya sangat disukai rekruter karena menunjukkan kamu punya standar penilaian yang jelas).
