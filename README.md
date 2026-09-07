# bot-onboarding

🤖 Bot Onboarding HRD Restoran (Local RAG + Groq API)

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Groq API](https://img.shields.io/badge/AI-Groq%20API-orange)
![Telegram](https://img.shields.io/badge/Bot-Telegram-blueviolet)

Asisten digital berbasis Telegram yang dirancang untuk mengotomatisasi proses onboarding karyawan baru di jaringan restoran secara instan. Sistem ini memanfaatkan Local RAG (Retrieval-Augmented Generation) agar AI membaca dokumen SOP internal restoran dan tidak mengarang bebas (*hallucination*).

---

🌟 Fitur Utama

- Pangkas Waktu HRD: Mengubah proses manual puluhan menit menjadi hitungan detik via Telegram.
- Kepatuhan SOP Strict: Mengikat AI agar 100% patuh pada aturan dokumen internal `sop_restoran.txt`
- Cakupan Multi-Posisi: Mendukung instruksi spesifik untuk Store Manager, Kasir, Line Cook/Koki, Waitstaff, dan Admin Logistik.
- **Output Instan Siap Pakai:**
  - 💬 Draf pesan sambutan WhatsApp (tinggal *copy-paste* ke karyawan).
  - 📋 Checklist dokumen administrasi untuk manajer.
  - 👔 Panduan aturan seragam (termasuk standar sepatu anti-slip dapur).
  - 📅 Jadwal rinci hari pertama kerja (*Day-1 Schedule*).

---

## 🛠️ Arsitektur & Teknologi

| Komponen | Teknologi | Deskripsi |
| :--- | :--- | :--- |
| **Interface** | `pyTelegramBotAPI` | Antarmuka chat interaktif antara HR/Manager & Bot |
| **LLM Engine** | Groq API (`llama-3.3-70b-versatile`) | Pemrosesan teks super cepat & efisien |
| **Data Logic** | Local RAG (`sop_restoran.txt`) | *Knowledge base* eksternal untuk menjaga akurasi SOP |

---

## 🚀 Cara Menjalankan Project

### 1. Clone Repository
```bash
git clone [https://github.com/Alden-rts/bot-onboarding.git](https://github.com/Alden-rts/bot-onboarding.git)
cd bot-onboarding


