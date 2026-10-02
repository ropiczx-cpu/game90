# Petualangan Dungeon - Legenda Naga Raja

Game RPG teks sederhana (hitam putih) yang berjalan di browser.
Pilih kelas, jelajahi dungeon, berlatih, belanja, lalu kalahkan Naga Raja!

## Fitur
- 4 tingkat kesulitan: Baby, Medium, Hard, Super Hard
- 4 kelas: Pendekar, Penyihir, Pemanah, Tombak (damage, critical, dan skill berbeda)
- HP & MP awal lebih kecil, ditambah stamina yang menguras tiap aksi
- Senjata kayu dan armor kayu bertingkat (Biasa, Ek, Hitam, Pohon Dunia)
- Toko Budak: Pet dan Elf pendamping yang membantu bertarung, plus menu Bicara dengan Budak
- 13 jenis musuh + monster rahasia Nambo Rafif GoG (muncul sangat jarang)
- Boss Naga Raja (level 5) + 3 boss rahasia yang dibuka lewat dialog pendamping
- Kalahkan 3 boss rahasia untuk gelar Raja Segala Raja
- Toko, penginapan, potion, ether, dan roti
- Musik dan efek suara 8-bit (dibuat oleh browser, tanpa file audio)
- Mode seram: layar jadi hitam putih terbalik, berkedip, bergetar, ada musik & suara bisikan/jeritan/detak jantung (boss, Nambo, dan semua pertarungan Super Hard; detak jantung saat HP kritis)
- Super Hard: Critical tidak dikali dua (maksimal x1.5)
- Dialog Budak lebih panjang (3 dialog tambahan tiap pendamping) dan mereka berbisik ketakutan saat pertarungan seram

## Struktur file
```
index.html   <- halaman utama (berisi game)
style.css    <- tampilan hitam putih
hanni.mp3    <- lagu Clara
README.md
```
`index.html` dan `style.css` harus berada di folder paling luar (root) repo,
dengan nama huruf kecil semua.

## Cara menjalankan
Buka `index.html` langsung di browser. Tidak perlu install apa pun.

## Cara unggah ke GitHub
1. Buat repository baru di github.com (boleh Public).
2. Klik **Add file -> Upload files**.
3. Seret **isi** folder ini (`index.html`, `style.css`, `README.md`), bukan folder induknya.
4. Klik **Commit changes**.

## Cara hosting di Vercel
1. Buka vercel.com -> **Add New -> Project**, lalu pilih repository ini.
2. Framework Preset: **Other**.
3. Kosongkan Build Command dan Output Directory, lalu klik **Deploy**.

## Pembaruan terbaru
- Tampilan: bar HP, MP, Stamina, XP ada di samping; tombol Toko Budak, Toko Pandai Besi, dan Jual Beli ada di bawahnya.
- Loot: kerangka -> tulang, orc -> pedang, slime/serigala/dll -> bahan jual, goblin -> uang. Jual di menu Jual Beli (beli potion/ether/roti juga di sana).
- Super Hard: Budak Istimewa Elf Clara (dengan foto) dan last boss Botak Kopral (jurus Kepingan, cutscene tertawa dan "Sou desu ka").

## Pembaruan terbaru (2)
- `hanni.mp3` harus berada di folder yang sama dengan `index.html` (dipakai saat Clara diminta bernyanyi).
- Nama "ropi" = +1000 koin (semua mode). Nama mengandung angka = Petualang Biasa (tinju saja, tanpa skill & armor).
- Job baru: Petarung (tangan kosong). Mode Baby: Mom Spongebob otomatis jadi budak (mencuri 5 koin jika terlalu malas).
- Berlatih hanya memakai stamina. Istirahat selalu 5 koin. Elf bisa dilamar lewat menu Bicara.
- Menaklukkan dungeon: kalahkan Naga Raja + 3 boss rahasia (+ Botak Kopral di Super Hard); setiap budak mengucapkan terima kasih.

## Pembaruan terbaru (3)
- Monster anomali "Arya Gyat DMY": muncul dengan peluang 56% tiap bertemu monster, di semua mode (ubah `PELUANG_ARYA` di index.html untuk mengatur). Fotonya tampil di panel musuh.
- Foto pernikahan tampil saat melamar Clara.
- Tampilan disesuaikan untuk layar HP (tombol besar, toko 3 kolom, log menyesuaikan tinggi layar).

## Pembaruan terbaru (4)
- Nambo Rafif GoG: musik khusus yang sumbang, jumpscare saat muncul, wajahnya muncul acak di seluruh layar tiap beberapa detik dengan suara seram.

## Nama rahasia "ropi" (untuk testing)
Armor Iron Man, +1000 koin, dan tombol [TEST] untuk langsung melawan Nambo Rafif GoG dan Botak Kopral di mode apa pun.

## Pembaruan terbaru (5)
- Save data otomatis (localStorage browser). Tombol "Lanjutkan permainan" muncul di layar awal jika ada data.
- Kalah: tanpa budak = mati sendirian; punya budak = budak direbut goblin (data save dihapus); punya Mom Spongebob = dihidupkan kembali.
- Botak Kopral: tertawa saat kalah, menjatuhkan Emas x10 dan budak Dinda (adik Clara, hanya bisa didapat dari sini).

## Pembaruan terbaru (6)
- **Gacha item & uang**: tiap pemain dapat 1 Tiket Gacha di awal permainan, dan +1 tiket setiap mengalahkan Arya Gyat DMY. Buka lewat tombol "Gacha" di panel Toko. Peluang: Biasa 55%, Langka 30%, Epik 12%, Legendaris 3% (hadiah: potion, ether, roti, gold, Emas, dan permata stat permanen). Save lama otomatis dapat 1 tiket.
- **Siang & malam**: jam game berjalan sendiri (1 menit game tiap 3 detik) dan maju saat beraksi (jelajah, latihan, istirahat tidur 8 jam, dll). Malam = 18:00-04:59: tampilan berbalik jadi gelap, musuh +35% HP/ATK tapi XP & gold +25%, monster gelap (Vampir, Hantu, Serigala, Kerangka) lebih sering muncul, duduk lebih berisiko. Siang: duduk memulihkan +10 stamina.
- **Jam di atas layar** (seperti status bar HP): menampilkan jam, hari ke-, fase (Pagi/Siang/Sore/Malam), dan ikon matahari/bulan.
- **Animasi pembuka** "Selamat Datang di Dunia Fantasi" (bintang, huruf muncul satu per satu). Ketuk layar untuk memulai (sekaligus menyalakan musik).
- **Nama rahasia "ropi" diperbarui**: HP, MP, Stamina, ATK, dan Critical TANPA BATAS (tampil ∞), koin TANPA BATAS, Armor Iron Man, menu [TEST] tetap ada. (Menggantikan aturan lama "+1000 koin".)

## Pembaruan terbaru (7)
- **Foto Mom Spongebob** diganti dengan foto baru. **Boss rahasia Spongebob** (anak Mom Spongebob): buka dengan mengajak bicara Mom 3x (khusus mode Baby, tempat Mom jadi budak), butuh Level 6. Menang: 2 Potion Kebugaran 2 + 300 gold. Tidak wajib untuk menaklukkan dungeon.
- **Malam lebih sulit di semua mode**: musuh biasa +35% HP & ATK (hadiah XP/gold +25%). Saat menjelajah malam ada 30% peluang menemukan **Bar Dungeon** (ubah `PELUANG_BAR`) untuk membeli Alkohol.
- **Mabuk**: Minum Alkohol saat bertarung (tidak memakai giliran). 3 aksi berikutnya GRATIS (tanpa stamina/MP), tetapi stamina, MP, dan DEF jadi 0. Setelah 3 aksi (atau pertarungan selesai) kembali normal dan HP berkurang 20% (tidak sampai mati).
- **Rem** (maid yang ditinggalkan tuannya): hanya dari Gacha dengan peluang 0,1% (Mitos). Menyerang 40 damage tiap giliran, memberi 3 Roti + 4 Alkohol saat bergabung dan tiap kamu istirahat di penginapan. Bisa diajak bicara dan dilamar (foto gaun pengantin). Jika kamu mati: Rem kabur dengan "Maafkan tuan, sepertinya aku mencari tuan baru."
- **Subcus** (monster rahasia): menyerap 10 stamina tiap giliran, HP 30. Peluang muncul 10% siang / 75% malam (`PELUANG_SUBCUS_SIANG`, `PELUANG_SUBCUS_MALAM`). Selalu menjatuhkan **Potion Kebugaran 2**: stamina 100%, HP & MP +25%, ATK/DEF/Critical +25% selama 3 pertarungan (`DROP_KEBUGARAN` untuk mengatur peluang drop).
- Nama "ropi": menu [TEST] bertambah (Subcus, Spongebob, Bar, Panggil Rem).

## Pembaruan terbaru (8)
- **Ending animasi** saat dungeon ditaklukkan (bintang, teks muncul perlahan; ketuk layar untuk melanjutkan, tombol "Lewati" tersedia):
  - Semua mode: teks "Selamat atas perjuangannya", lalu kelanjutan hidup tiap budak yang dimiliki (tanpa budak = langsung ke kredit).
  - **Super Hard + punya Elf Clara**: tambahan adegan foto kenangan di bukit (kelopak berjatuhan, efek zoom pelan) dengan kata-kata romantis bahwa mereka kini hidup bebas dan tak terikat dungeon lagi. Jika sudah menikah dengan Clara, ada tambahan baris cincin. Jika punya Dinda, ia ikut muncul.
  - **Kredit akhir**: "Game ini dibuat oleh ROPI - Creator".
  - Menu "Putar ulang ending" muncul setelah dungeon ditaklukkan.
- **Album Foto Secret** (tombol "Album" di bagian atas, tersimpan di browser lintas permainan): 16 foto yang terbuka saat mendapatkan secret, yaitu Clara, pernikahan Clara, Dinda, Rem, pernikahan Rem, Mom Spongebob, Spongebob, Nambo, Arya, Subcus, Botak Kopral, Naga Raja, 3 boss rahasia, dan foto Kebebasan (ending Super Hard + Clara). Foto baru muncul sebagai notifikasi kecil. Klik foto untuk memperbesar.
- **Musik diganti ke fantasi retro** (gaya JRPG 8/16-bit, tetap dibuat dengan kode): menu/jelajah, pertarungan, dan boss memakai melodi + arpeggio harpa + bass baru; ada lagu ending. Musik seram (Nambo, mode horor, sedih) tidak diubah.
- Tulisan "(Klik di mana saja untuk menyalakan musik & suara)" dihapus.
- Nama "ropi": menu [TEST] bertambah "Lihat Ending Biasa" dan "Lihat Ending Super Hard + Clara".
