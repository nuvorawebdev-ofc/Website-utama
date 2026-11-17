# Nuvora.webdev — Website Project

Situs statis satu halaman untuk Nuvora.webdev dengan identitas editorial yang sudah ada: Gray 900 `#141411`, aksen lime, portrait pengguna, logo Nuvora, navigasi responsif, pilihan Bahasa Indonesia/English, dan tiga demo portfolio dengan screenshot autentik.

Katalog layanan saat ini berfokus pada desain/pengembangan website, landing page, dan desain ulang website. Tarif paket yang sudah ada tetap dipertahankan. Halaman tambahan di luar paket dikenakan **Rp389.000 per halaman**.

## Isi project

```text
NUVORA-WEBSITE/
├── index.html
├── README.md
└── assets/
    ├── favicon.png
    └── images/
        ├── *.png          # PNG originals retained
        └── *.webp         # exact-pixel, lossless WebP used by the site
```

`index.html` berisi HTML, CSS, dan JavaScript mandiri. Gambar memakai path project-relative dari folder `assets`; situs menyajikan salinan WebP lossless (piksel, proporsi dan transparansi tetap sama), sementara PNG sumber asli tetap disertakan. Situs mempertahankan metadata halaman, markup semantik, tata letak responsif dan FAQ praktik teknis website. Tidak ada framework atau paket build yang diperlukan.

## Preview di Android

1. Unduh `NUVORA-WEBSITE.zip` dan ekstrak dengan Files atau aplikasi pengelola arsip Android.
2. Buka folder `NUVORA-WEBSITE` hasil ekstraksi.
3. Buka `index.html` menggunakan browser yang mendukung file lokal. Bila browser membatasi file lokal, gunakan aplikasi server/editor web lokal Android dan buka alamat localhost yang ditampilkan.
4. Pertahankan folder `assets` di sebelah `index.html`; jangan memisahkan file HTML dari asetnya.

## Ekstrak ZIP

Di Android, pilih file ZIP di Files lalu tekan **Ekstrak**. Di komputer gunakan menu Extract bawaan atau `unzip NUVORA-WEBSITE.zip`. Setelah ekstraksi, folder hasilnya berisi semua aset yang diperlukan.

## Deploy ke GitHub Pages

1. Buat repository GitHub dan unggah seluruh isi folder `NUVORA-WEBSITE` ke root repository, termasuk `assets/` dan README.
2. Buka **Settings → Pages** pada repository.
3. Pilih **Deploy from a branch**, branch `main`, folder `/ (root)`, lalu simpan.
4. Tunggu GitHub Pages menerbitkan situs dan buka URL yang ditampilkan pada pengaturan Pages.

Project juga dapat diunggah utuh ke layanan static hosting lain. Build step, framework, backend, dan dependency eksternal tidak diperlukan.

## Portfolio dan aset

Urutan kartu: West Coffee — [Demo Website 01](https://nuvorawebdev-ofc.github.io/Demo-website-by-Nuvora-01/); D'Rasa Indonesian Restaurant — [Demo Website 02](https://nuvorawebdev-ofc.github.io/Demo-website-02/); Assyifa Dental Clinic — [Demo Website 03](https://nuvorawebdev-ofc.github.io/Demo-website-03/). Setiap kartu memakai screenshot asli dari halaman demo yang bersangkutan, membuka URL yang sesuai di tab baru, dan diberi label sebagai demo—bukan klaim pekerjaan klien atau hasil komersial.

Portrait dan logo berasal dari aset yang diberikan pengguna dan tetap disimpan dalam project; identitas visualnya tidak diganti. Favicon lokal berasal dari logo project. Semua PNG asli tetap dipertahankan; salinan WebP untuk logo, portrait dan screenshot telah diverifikasi identik per piksel/dimensi sebelum dipakai pada halaman. Screenshot demo menampilkan halaman awal pada viewport desktop saat inspeksi; situs demo pihak ketiga dapat berubah atau tidak tersedia sewaktu-waktu.

## Kualitas dan aksesibilitas

Website mempertahankan navigasi desktop/mobile, active-section indicator, menu mobile yang menutup sesudah memilih bagian, FAQ `<details>` yang dapat dioperasikan dengan keyboard, pengalih bahasa, CTA WhatsApp, target anchor internal, dan dukungan `prefers-reduced-motion`. Harga tambahan dan bagian layanan tersedia dalam Bahasa Indonesia maupun English.

---

Untuk arsip aset saja, gunakan `NUVORA-ASSETS.zip` di project root. Arsip situs lengkap yang diminta adalah `NUVORA-WEBSITE.zip`.


## QA akhir

- Pemeriksaan statis: 3 kartu demo sesuai URL, 11 FAQ, semua anchor lokal valid, semua gambar project-relative tersedia; JavaScript lolos `node --check`; endpoint `/` dan `/manus-routes.json` merespons.
- Pemeriksaan browser: pilihan Bahasa Indonesia/English untuk 81 elemen konten di layanan, harga, tambahan, dan FAQ; metadata/label aksesibel/CTA WhatsApp; navigasi aktif dan menu mobile; FAQ dibuka dengan Enter dan ditutup dengan Space. Semua gambar WebP tampil, semua tautan eksternal demo memakai target baru dan rel aman; tidak terlihat error console.
- Pemeriksaan visual: ponsel 320×780 dan 390×844, tablet 768×1024, serta halaman penuh desktop. Ukuran layout browser yang diperiksa tidak melewati viewport.
- Kelima WebP lossless diuji identik per piksel dengan PNG asli, mempertahankan dimensi dan transparansi; total byte gambar yang dilayani turun 35,6%. PNG sumber tetap disertakan.
- Arsip ZIP lengkap lulus uji integritas dan folder output statis berisi seluruh path aset. Situs **belum di-deploy atau dipublikasikan**.
