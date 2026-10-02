# Petualangan Dungeon - Legenda Naga Raja

Game RPG teks sederhana (hitam putih) yang berjalan di browser.
Pilih kelas, jelajahi dungeon, berlatih, belanja, lalu kalahkan Naga Raja!

## Fitur
- 4 kelas: Pendekar, Penyihir, Pemanah, Tombak (damage, critical, dan skill berbeda)
- Aksi berlatih dan stat critical
- 13 jenis musuh + boss Naga Raja (muncul di level 5)
- Toko, penginapan, potion, dan ether
- Musik dan efek suara 8-bit (dibuat oleh browser, tanpa file audio)

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
