# 🤖 Bot Onboarding HRD Restoran (Local RAG + Groq API)

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Groq API](https://img.shields.io/badge/AI-Groq%20API-orange)
![Telegram](https://img.shields.io/badge/Bot-Telegram-blueviolet)

Asisten digital berbasis Telegram yang dirancang untuk mengotomatisasi proses onboarding karyawan baru di jaringan restoran secara instan. Sistem ini memanfaatkan Local RAG (Retrieval-Augmented Generation) agar AI membaca dokumen SOP internal restoran dan tidak mengarang bebas (*hallucination*).

---

## 🌟 Fitur Utama

- **Pangkas Waktu HRD:** Mengubah proses manual puluhan menit menjadi hitungan detik via Telegram.
- **Kepatuhan SOP Strict:** Mengikat AI agar 100% patuh pada aturan dokumen internal `sop_restoran.txt`.
- **Cakupan Multi-Posisi:** Mendukung instruksi spesifik untuk Store Manager, Kasir, Line Cook/Koki, Waitstaff, dan Admin Logistik.
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
| **LLM Engine** | Groq API (`openai/gpt-oss-120b`) | Pemrosesan teks super cepat & efisien |
| **Data Logic** | Local RAG (`sop_restoran.txt`) | *Knowledge base* eksternal untuk menjaga akurasi SOP |

---

## 🚀 Cara Menjalankan Project

### 1. Clone Repository
```bash
git clone https://github.com/Alden-rts/bot-onboarding.git
cd bot-onboarding

```

### 2. Install Dependency

```bash
pip install pyTelegramBotAPI groq python-dotenv

```

### 3. Siapkan File SOP (`sop_restoran.txt`)

Buat file `sop_restoran.txt` di direktori yang sama dengan `main.py`. Berikut contoh struktur isinya:

```text
SOP RESTORAN - FRENCH ASIAN FUSION (INTERNAL)

1. POSISI: KASIR (Front of House)
- Seragam: Kemeja hitam, celemek coklat, dilarang memakai aksesoris berlebihan.
- Jadwal Hari Pertama: 08:00 - Pengenalan mesin kasir, 10:00 - Latihan melayani pelanggan.
- Pesan WA: Harus ramah, panggil pelanggan "Kakak".

2. POSISI: KOKI (Line Cook / Kitchen Staff)
- Seragam: Baju chef putih, topi dapur, WAJIB sepatu anti-slip.
- Jadwal Hari Pertama: 07:00 - Pengenalan stasiun masak, 09:00 - Standar Food Safety (HACCP).
- Pesan WA: Profesional, tegas pada kebersihan.

```

### 4. Konfigurasi Environment Variable (`.env`)

Buat file bernama `.env` di folder root project, lalu isi dengan API key milikmu:

```env
TELEGRAM_BOT_TOKEN="MASUKKAN_TOKEN_BOT_TELEGRAM_DISINI"
GROQ_API_KEY="MASUKKAN_API_KEY_GROQ_DISINI"

```

### 5. Jalankan Bot

```bash
python main.py

```

---

## 💡 Contoh Penggunaan di Telegram

### Input dari HR / Manager:

> `Onboard staf baru: Arnold, posisi Line Cook, mulai jam 7 pagi.`

### Output Otomatis dari Bot Telegram:

> **📩 Draf WA Karyawan Baru:**
> "Halo Arnold! Selamat bergabung di tim kitchen kami. Kamu dijadwalkan mulai kerja besok jam 07:00 pagi. Harap gunakan baju chef putih, topi dapur, dan WAJIB memakai sepatu anti-slip demi keselamatan kerja. Sampai bertemu!"
> **📋 Checklist Manager & Jadwal Hari Pertama:**
> * **Dokumen Required:** KTP, Rekening Bank, Formulir Biodata.
> * **07:00:** Pengenalan stasiun masak & perkenalan tim.
> * **09:00:** Briefing standar Food Safety (HACCP) & kebersihan dapur.
> 
> 
