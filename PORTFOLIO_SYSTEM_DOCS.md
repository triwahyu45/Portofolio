# 🚀 PORTFOLIO SYSTEM & MAINTENANCE DOCUMENTATION
**Tri Wahyu Handoyo (NIM 22518241023) - S1 Pendidikan Teknik Mekatronika UNY**
*Official Web Portfolio Maintenance & AI Agent Guidelines*

---

## 🌟 1. FITUR UTAMA & FITUR TERUJI (HARUS DIPERTAHANKAN)

Berikut adalah komponen utama web yang sudah diuji secara teliti dan **WAJIB DIPERTAHANKAN** pada setiap update mendatang:

### A. Performa & Arsitektur Mobile Anti-Lag (Smooth 60 FPS)
- **Lazy 3D Mode (Default OFF)**: Tampilan 3D WebGL Three.js **SELALU MATI secara default** pada saat pertama kali web dimuat untuk menjamin kecepatan *fast-response* < 1 detik.
- **1-Click 3D Toggle Switch**: Disediakan tombol saklar `#toggle3DMode` di Sidebar & Hero Banner untuk mengaktifkan rendering Three.js hanya ketika diminta pengunjung.
- **Video Preload Optimization**: Seluruh elemen `<video>` wajib menggunakan `preload="none"` untuk menghemat kuota dan mencegah throttling GPU di smartphone.
- **Backdrop Blur Mobile Tweak**: Pada layar HP (`@media max-width: 768px`), filter `backdrop-filter: blur(6px)` dan `transform-style: flat` dikunci agar scroll tetap 60 FPS.

### B. Kartu Profil Hero Atas (Mobile-First Hero Avatar Card)
- **Posisi Paling Atas (`#about`)**: Kartu profil Hero berisi Foto Avatar (`assets/tri_wahyu_avatar.jpg`), NIM, Program Studi S1 Pendidikan Teknik Mekatronika UNY, serta badge tim **Abhinaya UNY** & **Maestro EVO UNY** agar langsung muncul di HP tanpa perlu scroll.

### C. Logo & Timeline Resmi Tim Robotika UNY
- **Tim Abhinaya UNY**:
  - *2023–2024*: Programmer Utama KRTMI BPTI Puspresnas.
  - *2026*: Finalis Transporter Robot Technocorner UGM 2026 (Senior Support & Technical Advisor).
- **Tim Maestro EVO UNY**:
  - *2025*: Software & Hardware System Developer (KRAI Puspresnas - Demisioner).
- **Efek Stroke Putih Logo**: Seluruh logo tim (`logo_abhinaya_transparent.png` & `logo_maestro_evo.png`) dilengkapi efek CSS `filter: drop-shadow(0 0 2px #ffffff) drop-shadow(0 0 6px rgba(255, 255, 255, 0.7))` agar tampil tajam dan kontras di latar hitam.

### D. Audit Presisi Sertifikat Puspresnas KRI (2023 & 2024)
- **🏆 Juara 2 KRTMI 2024 (Tingkat Nasional)**: Gambar HD asli `Abhinaya_2024_Juara_2_Nasional_Tri_Wahyu_Handoyo_1.png` + Metadata BPTI Puspresnas.
- **🏆 Juara 1 KRTMI 2024 (Tingkat Regional I Wilayah)**: Gambar HD asli `Abhinaya_2024_Juara_1_Wilayah_Tri_Wahyu_Handoyo_1.png` + PDF.
- **🏅 Finalis KRI KRTMI 2023 (Tingkat Nasional - USM Semarang)**: PDF & Gambar `cert_krtmi_2023_nasional` (21–26 Juni 2023 di USM Semarang, ditandatangani Kepala BPTI Asep Sukmayadi, M.Si.).
- **🚩 Peserta KRI KRTMI 2023 (Tingkat Wilayah)**: PDF & Gambar `cert_krtmi_2023_wilayah` (28 Mei – 5 Juni 2023).

### E. Integrasi 7 Perancangan CAD Autodesk Inventor (.iam) Asli
- **1. INESCO 2025**: `Robot Inesco.iam` (Render HD: `assets/cad/render_inesco.png`)
- **2. PANCO UNY**: `KapalPembersihLaut Seaware.iam` (Render HD: `assets/cad/render_seaware.png`)
- **3. HIMEPA Untan**: `SmartTrash Tinggi.iam` (Render HD: `assets/cad/render_smarttrash.png`)
- **4. FKMPI Fair**: `Robot Humanoid.iam` (Render HD: `assets/cad/render_humanoid.png`)
- **5. PodComfest**: `Robot PodComFest.iam` (Render HD: `assets/cad/render_podcomfest.png`)
- **6. Robot TAMA**: `KapalPembersihLautSeacraft.iam` (Render HD: `assets/cad/render_seacraft.png`)
- **7. Technocorner UGM**: `Robot Transporter.iam` (Render HD: `assets/cad/render_transporter_technocorner.png`)

### F. Aturan Privasi & Keamanan Data (100% Strict)
- **Tidak Boleh Memuat Nomor Telepon / WA Personal**: Seluruh tombol kontak WA/telepon dilarang dipasang di repo publik. Gunakan Instagram resmi `@detronics.id` atau Linktree.

---

## 🛠️ 2. OPSI PENINGKATAN MENDATANG (WHAT CAN BE IMPROVED)

Jika ada pengembangan portofolio berikutnya, berikut poin-poin yang bisa ditingkatkan:

1. **Export 3D Binary GLTF (`.glb`) untuk 7 CAD Assembly**:
   - Mengekspor ke-7 file `.iam` Inventor menjadi format `.glb` agar mesh 3D di Three.js memiliki tekstur warna material logam & warna komponen yang persis seperti di Autodesk Inventor.
2. **Penyimpanan Tema Dark/Light (localStorage)**:
   - Menambahkan `localStorage.setItem('theme', ...)` agar preferensi Dark Mode / Light Mode tersimpan saat pengunjung membuka kembali web.
3. **Embed Live Wokwi Simulation**:
   - Memasang iframe modal live simulator Wokwi untuk penguji sirkuit mikrokontroler ESP32/STM32 secara *real-time*.

---

## 📁 3. STRUKTUR ASET PENTING

```text
Portofolio/
├── index.html                  # Main Web Markup & Integrated JS Engine
├── style.css                   # Cyberpunk Glassmorphism Design System
├── PORTFOLIO_SYSTEM_DOCS.md    # Documentation & Maintenance Guide
├── README.md                   # Repository Overview
└── assets/
    ├── logo_abhinaya.png       # Abhinaya UNY Official HD Logo
    ├── logo_maestro_evo.png    # Maestro EVO UNY Official Logo (with White Stroke)
    ├── tri_wahyu_avatar.jpg    # Primary Hero Profile Avatar
    ├── cad/                    # Optimized CAD Renders (render_*.png)
    ├── certificates/           # HD Certificate Images & PDFs
    ├── docs/                   # Original High-Res Document Archives
    └── documentation/          # Field & Competition Photos
```

---
*Dokumen ini dibuat secara resmi untuk menjadi panduan pengembang & agen AI dalam memelihara kualitas portofolio Tri Wahyu Handoyo.* 🚀⚡🔥
