# Bot Sosmed Twitter (botsosmedtwitter)

Selamat datang di Bot Sosmed Twitter, sebuah solusi otomatisasi canggih yang dirancang untuk mengubah topik trending dari Google Trends menjadi konten tweet yang menarik secara otomatis. Bot ini menggunakan riset dari GNews dan kecerdasan buatan dari Google Gemini untuk membuat setiap tweet relevan dan berpotensi viral.

<br>

[**➡️ Beli Lisensi Anda di Sini ⬅️**](https://link-pembelian-anda.com)

<br>

---

## 1. Fungsi & Keunggulan

* ✅ **Otomatisasi Penuh 24/7**: Diatur untuk berjalan secara mandiri menggunakan GitHub Actions. Cukup atur sekali dan biarkan bot bekerja untuk Anda.
* ✅ **Konten dari Google Trends**: Mengambil topik paling relevan langsung dari Google Trends sesuai negara yang Anda targetkan.
* ✅ **Riset Konten Otomatis**: Melakukan riset singkat melalui GNews untuk mendapatkan konteks berita terkait topik trending.
* ✅ **Teks Tweet Berbasis AI**: Menggunakan **Google Gemini** untuk menulis teks tweet yang menarik, informatif, dan memancing interaksi berdasarkan hasil riset.
* ✅ **Pencarian Gambar Otomatis**: Secara otomatis mencari gambar yang relevan dengan topik dari artikel berita asli, memastikan setiap tweet memiliki visual yang kuat.
* ✅ **Manajemen Hashtag Cerdas**: Menggabungkan hashtag utama dari topik, hashtag populer dari `trends24.in`, dan hashtag manual dari konfigurasi Anda.
* ✅ **Anti-Duplikat**: Bot mengingat topik yang sudah pernah diposting untuk memastikan konten yang dihasilkan selalu baru.
* ✅ **Konfigurasi Eksternal**: Semua pengaturan penting dikelola melalui satu file `config.json` yang mudah dipahami.

---

## 2. Struktur File

Pastikan repositori Anda memiliki struktur file berikut untuk fungsionalitas penuh:

```
/
├── .github/
│   └── workflows/
│       └── twitter_bot.yml        (atau nama file workflow .yml Anda)
│
├── config.json             # File Konfigurasi Utama
├── botsosmedtwitter.py                  # Skrip Utama Bot
├── requirements.txt        # Daftar library Python yang dibutuhkan
├── processed_topics.log    # File log untuk mencegah duplikat (dibuat otomatis)
└── README.md
```

---

## 3. Panduan Instalasi Lengkap

Untuk menjalankan bot ini di akun GitHub Anda, ikuti langkah-langkah berikut:

#### **A. Dapatkan Lisensi**
Bot ini memerlukan lisensi untuk aktif. Dapatkan lisensi Anda melalui link di atas. Lisensi Anda akan terikat pada alamat email yang Anda gunakan saat pembelian.

#### **B. Fork Repositori**
Buat salinan proyek ini ke akun GitHub Anda dengan mengklik tombol **"Fork"** di pojok kanan atas halaman repositori ini.

#### **C. Atur GitHub Secrets**
Ini adalah langkah paling penting. Buka repositori Anda, lalu pergi ke **Settings > Secrets and variables > Actions**. Klik **"New repository secret"** dan buat semua *secrets* berikut:

* **`BOT_LICENSE_EMAIL`**: **(Wajib)** Isi dengan email waktu pembelian license.
* **`GEMINI_API_KEY`**: **(Wajib)** Kunci API dari Google AI Studio.
* **`TWITTER_API_KEY`**: Kunci API Twitter Anda.
* **`TWITTER_API_SECRET`**: Kunci rahasia API Twitter Anda.
* **`TWITTER_ACCESS_TOKEN`**: Token akses Twitter Anda.
* **`TWITTER_ACCESS_TOKEN_SECRET`**: Token rahasia akses Twitter Anda.

#### **D. Aktifkan dan Jalankan Workflow**
1.  Di repositori Anda, klik tab **Actions**.
2.  Jika ada peringatan, klik tombol hijau untuk mengaktifkan workflow.
3.  Di sisi kiri, klik nama workflow (misal: `Bot Auto-Tweet (Google Trends)`).
4.  Klik **"Run workflow"** untuk menjalankan bot secara manual atau biarkan berjalan otomatis sesuai jadwal.

---

## 4. Panduan Edit Konfigurasi `config.json`

Semua perilaku bot diatur dari file `config.json`. Buka file tersebut dan sesuaikan nilainya:

```json
{
  "GEMINI_SETTINGS": {
    "model": "gemini-1.5-flash-latest",
    "temperature": 0.8
  },
  "GOOGLE_TRENDS_CONFIG": {
    "geo": "ID",
    "hl": "id",
    "hours": 4,
    "category": "h"
  },
  "GNEWS_CONFIG": {
    "language": "id",
    "country": "ID"
  },
  "TRENDS24_CONFIG": {
    "scrape_url": "[https://www.trends24.in/indonesia/](https://www.trends24.in/indonesia/)",
    "trending_limit": 4
  },
  "TWITTER_CONFIG": {
    "traffic_link": "[https://LINK-WEBSITE-ANDA.com](https://LINK-WEBSITE-ANDA.com)",
    "manual_hashtags": ["#beritaviral", "#infoterkini"]
  },
  "GEMINI_PROMPTS": {
    "generate_tweet": "Anda adalah seorang social media manager viral. Berdasarkan topik utama '{topic}' dan rangkuman berita '{news_context}', buat satu tweet yang sangat menarik (maksimal 150 karakter) yang membuat orang penasaran untuk mencari tahu lebih lanjut. JANGAN gunakan hashtag dalam jawabanmu."
  }
}
```
* **`GOOGLE_TRENDS_CONFIG`**: Ubah `geo`, `hours`, atau `category` untuk menargetkan tren yang berbeda.
* **`TRENDS24_CONFIG`**: Ubah `scrape_url` untuk target negara lain dan `trending_limit` untuk jumlah hashtag tambahan.
* **`TWITTER_CONFIG`**: Masukkan link website Anda di `traffic_link` dan hashtag default Anda di `manual_hashtags`.
* **`GEMINI_PROMPTS`**: Sesuaikan instruksi untuk AI Gemini jika Anda ingin gaya penulisan yang berbeda.

---

## 5. Kebijakan Lisensi

* Lisensi berlaku selama **satu tahun** sejak tanggal pembelian.
* Satu lisensi dapat Anda gunakan untuk mengotomatisasi akun-akun Twitter dalam jumlah **tidak terbatas**.
* Lisensi ini **tidak dapat dipindahtangankan**, dibagikan, atau dijual kembali kepada pihak lain. Pengembang berhak menonaktifkan lisensi jika terdeteksi adanya pelanggaran.

<br>
<hr>
<br>

# Bot Sosmed Twitter (botsosmedtwitter) - English

Welcome to Bot Sosmed Twitter, a sophisticated automation solution designed to turn trending topics from Google Trends into engaging, automated tweets. This bot utilizes research from GNews and artificial intelligence from Google Gemini to make every tweet relevant and potentially viral.

<br>

[**➡️ Buy Your License Here ⬅️**](https://your-purchase-link.com)

<br>

---

## 1. Function & Features

* ✅ **24/7 Full Automation**: Configured to run autonomously using GitHub Actions. Set it up once and let the bot work for you.
* ✅ **Google Trends Content**: Fetches the most relevant topics directly from Google Trends based on your target country.
* ✅ **Automated Content Research**: Performs a quick search via GNews to get news context related to the trending topic.
* ✅ **AI-Powered Tweet Text**: Leverages **Google Gemini** to write engaging, informative, and interaction-driven tweet text based on the research.
* ✅ **Automatic Image Search**: Automatically finds a relevant image from the original news article, ensuring every tweet is visually strong.
* ✅ **Smart Hashtag Management**: Combines the main topic hashtag, popular hashtags from `trends24.in`, and your manual hashtags from the configuration.
* ✅ **Anti-Duplicate**: The bot remembers which topics have been posted to ensure the generated content is always new.
* ✅ **External Configuration**: All critical settings are managed through a single, easy-to-understand `config.json` file.

---

## 2. File Structure

Ensure your repository has the following file structure for full functionality:

```
/
├── .github/
│   └── workflows/
│       └── twitter_bot.yml        (or your workflow .yml file name)
│
├── config.json             # Main Configuration File
├── botsosmedtwitter.py                  # Main Bot Script
├── requirements.txt        # List of required Python libraries
├── processed_topics.log    # Log file to prevent duplicates (auto-generated)
└── README.md
```

---

## 3. Complete Installation Guide

To run this bot on your own GitHub account, follow these steps:

#### **A. Get a License**
This bot requires a license to be activated. Get your license from the link above. Your license will be bound to the email address you use at checkout.

#### **B. Fork the Repository**
Create your own copy of this project by forking it to your GitHub account using the **"Fork"** button at the top-right corner of this repository's page.

#### **C. Set Up GitHub Secrets**
This is the most critical step. Go to your repository's **Settings > Secrets and variables > Actions**. Click **"New repository secret"** and create all of the following secrets:

* **`BOT_LICENSE_EMAIL`**: **(Required)** Fill with the email used at the time of license purchase.
* **`GEMINI_API_KEY`**: **(Required)** Your API Key from Google AI Studio.
* **`TWITTER_API_KEY`**: Your Twitter API Key.
* **`TWITTER_API_SECRET`**: Your Twitter API Secret Key.
* **`TWITTER_ACCESS_TOKEN`**: Your Twitter Access Token.
* **`TWITTER_ACCESS_TOKEN_SECRET`**: Your Twitter Access Token Secret.

#### **D. Enable and Run the Workflow**
1.  In your repository, click the **Actions** tab.
2.  If there is a warning, click the green button to enable workflows.
3.  On the left, select the workflow (e.g., `Bot Auto-Tweet (Google Trends)`).
4.  Click **"Run workflow"** to trigger the bot manually or let it run automatically on its schedule.

---

## 4. Guide to Editing `config.json`

All of the bot's behaviors are controlled from the `config.json` file. Open the file and adjust the values:

```json
{
  "GEMINI_SETTINGS": {
    "model": "gemini-1.5-flash-latest",
    "temperature": 0.8
  },
  "GOOGLE_TRENDS_CONFIG": {
    "geo": "ID",
    "hl": "id",
    "hours": 4,
    "category": "h"
  },
  "GNEWS_CONFIG": {
    "language": "id",
    "country": "ID"
  },
  "TRENDS24_CONFIG": {
    "scrape_url": "[https://www.trends24.in/indonesia/](https://www.trends24.in/indonesia/)",
    "trending_limit": 4
  },
  "TWITTER_CONFIG": {
    "traffic_link": "[https://YOUR-WEBSITE-LINK.com](https://YOUR-WEBSITE-LINK.com)",
    "manual_hashtags": ["#breakingnews", "#viralinfo"]
  },
  "GEMINI_PROMPTS": {
    "generate_tweet": "You are a viral social media manager & content strategist. Based on the main topic '{topic}' and the news summary '{news_context}', create one very engaging tweet (max 150 characters) that makes people curious to learn more. DO NOT use hashtags in your answer."
  }
}
```
* **`GOOGLE_TRENDS_CONFIG`**: Change `geo`, `hours`, or `category` to target different trends.
* **`TRENDS24_CONFIG`**: Change `scrape_url` for other countries and `trending_limit` for the number of extra hashtags.
* **`TWITTER_CONFIG`**: Insert your website link in `traffic_link` and your default hashtags in `manual_hashtags`.
* **`GEMINI_PROMPTS`**: Adjust the instruction for Gemini AI if you want a different writing style.

---

## 5. License Policy

* The license is valid for **one year** from the date of purchase.
* A single license can be used to automate an **unlimited** number of your own Twitter accounts.
* This license is **non-transferable** and may not be shared or resold. The developer reserves the right to deactivate a license if a violation is detected.
