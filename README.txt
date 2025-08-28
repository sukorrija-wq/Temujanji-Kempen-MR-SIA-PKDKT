Temujanji MR SIA – PKD Kuala Terengganu (Pakej Lengkap)
=============================================================

Fail dalam ZIP ini:
- index.html — Web app siap guna (GitHub Pages / mana-mana hosting statik)
- Code.gs     — Apps Script backend (copy ke Extensions → Apps Script)
- README.txt  — Fail ini

Apa yang ditambah (mengikut permintaan anda):
✓ Kunci tarikh ikut pilihan hari (bekerja = Ahad–Khamis, cuti = Jumaat–Sabtu)  
✓ Cegah rekod berganda (telefon+tarikh) — client & server-side  
✓ Auto-setup helaian: header, freeze row 1, filter, lebar kolum asas  
✓ Butang “Salin WhatsApp” dan “Muat turun CSV”  
✓ Retry offline: jika gagal hantar, data disimpan ke outbox (localStorage) dan dicuba semula bila online

Cara pasang (ringkas):
1) Google Sheet → Extensions → Apps Script → paste **Code.gs** → Deploy → Web app  
   - Execute as: Me  
   - Who has access: Anyone with link  
   - Salin URL `/exec`.
2) index.html sudah diisi URL anda:
   https://script.google.com/macros/s/AKfycbxx-p5Oit0R8a116e207P93GyYkKzQQUKBSYQDq8lUKKBXbO57ovJlvBz3VoB8kbb1D/exec
   (Jika menukar deployment, cari `WEB_APP_URL` dalam index.html dan tukar.)
3) Upload **index.html** ke GitHub Pages → cuba submit → semak Google Sheet (tab “Data”).

Struktur kolum di Google Sheet:
[
  "Server Timestamp",
  "Client Timestamp ISO",
  "Unique Key (tel|tarikh)",
  "Nama",
  "Telefon (normalized)",
  "Tempat Bertugas",
  "Bil Anak",
  "Umur1 (bulan)",
  "Umur2 (bulan)",
  "Umur3 (bulan)",
  "Umur (gabung)",
  "Pilihan Hari",
  "Tarikh Appt",
  "Masa",
  "Lokasi",
  "Catatan"
]
