# Petualangan Dungeon - Legenda Naga Raja

Game RPG teks sederhana (hitam putih) yang berjalan di browser.
Pilih kelas, jelajahi dungeon, berlatih, belanja, lalu kalahkan Naga Raja!

## Fitur
- 4 tingkat kesulitan: Easy, Medium, Hard, Super Hard
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
