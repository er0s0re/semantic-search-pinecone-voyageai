# 🚀 Semantic Search with Pinecone & Voyage AI

Yoo, wazzup! 👋 Ini adalah proyek keren buat nge-handle **pencarian semantik** pake embedding teks dari dokumen PDF. Basically, kita bikin teks jadi vektor, terus nyari teks yang mirip-mirip gitu. Tech stack-nya? Nih:

*   **Voyage AI**: Buat ngeubah teks jadi embedding (alias vektor keren).
*   **Pinecone**: Database vektor buat nyimpen dan nyari embedding.
*   **PDFPlumber**: Buat nge-extract teks dari PDF.

Buat yang mau cobain, langsung gas aja!🔥

---

## ️🛠️ Cara Install & Jalankan

1.  **Clone Repo Ini**:

    ```bash
    git clone [https://github.com/er0s0re/semantic-search-pinecone-voyageai.git](https://github.com/er0s0re/semantic-search-pinecone-voyageai.git)
    cd semantic-search-pinecone-voyageai
    ```

2.  **Install Dependencies**:

    ```bash
    pip install -r requirements.txt
    ```

3.  **Siapin API Keys**:

    *   Buat file `.env` di folder project, terus isi kayak gini:

        ```
        VOYAGE_API_KEY=your_voyage_api_key
        PINECONE_API_KEY=your_pinecone_api_key
        PINECONE_ENVIRONMENT=your_pinecone_environment
        ```

4.  **Jalankan Notebook**:

    *   Buka `embedding.ipynb` pake Jupyter Notebook atau VS Code.
    *   Run semua cell buat nge-extract teks, bikin embedding, dan upload ke Pinecone.

5.  **Coba Pencarian Semantik**:

    *   Pake fungsi `semantic_search` buat nyari teks yang mirip-mirip. Contoh:

        ```python
        results = semantic_search("Anak saya lahir di luar negeri, gimana cara bikin akta kelahiran?")
        for match in results["matches"]:
            print(f"ID: {match['id']}, Skor: {match['score']}, Metadata: {match['metadata']}")
        ```

---

## 🤔 Kenapa Harus Pake Ini?

*   **Cepet Banget**: Pake Pinecone, nyari teks yang mirip cuma hitungan milidetik.
*   **Akurat**: Embedding pake Voyage AI bikin hasil pencarian lebih relevan.
*   **Gampang Dipake**: Udah dibikin simpel, tinggal copas aja kodenya.

---

## 🧠 Gimana Cara Kerjanya?

1.  **Extract Teks**: Ambil teks dari PDF pake `PDFPlumber`.
2.  **Bikin Chunk**: Potong teks jadi bagian-bagian kecil biar gampang di-process.
3.  **Embedding**: Ubah teks jadi vektor pake Voyage AI.
4.  **Simpan di Pinecone**: Upload embedding ke Pinecone biar bisa di-query.
5.  **Semantic Search**: Cari teks yang mirip pake embedding.

---

## ️🖼️ Visualisasi Data

Kita juga bisa liat visualisasi embedding pake t-SNE. Cek aja di notebook buat liat grafiknya! 

---

## 🙏 Credits

* 📝 Buat yang mau belajar lebih lanjut, cek dokumentasi resminya:
    *   [Voyage AI](https://docs.voyageai.com/)
    *   [Pinecone](https://docs.pinecone.io/)
    *   [PDFPlumber](https://github.com/jsvine/pdfplumber)

---

##  License

Proyek ini open-source under MIT License. Mau dipake buat apa aja, silakan! 

---
