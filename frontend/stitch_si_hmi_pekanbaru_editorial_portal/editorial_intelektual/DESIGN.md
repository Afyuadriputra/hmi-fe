---
name: Editorial Intelektual
colors:
  surface: '#fcf9f8'
  surface-dim: '#dcd9d9'
  surface-bright: '#fcf9f8'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f6f3f2'
  surface-container: '#f0eded'
  surface-container-high: '#eae7e7'
  surface-container-highest: '#e5e2e1'
  on-surface: '#1c1b1c'
  on-surface-variant: '#41493e'
  inverse-surface: '#313030'
  inverse-on-surface: '#f3f0f0'
  outline: '#717a6d'
  outline-variant: '#c0c9bb'
  surface-tint: '#2e6b2f'
  primary: '#002c06'
  on-primary: '#ffffff'
  primary-container: '#00450d'
  on-primary-container: '#74b46e'
  inverse-primary: '#95d78e'
  secondary: '#705d00'
  on-secondary: '#ffffff'
  secondary-container: '#fce17e'
  on-secondary-container: '#766307'
  tertiary: '#705d00'
  on-tertiary: '#ffffff'
  tertiary-container: '#c5aa3c'
  on-tertiary-container: '#4c3f00'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#b0f3a7'
  primary-fixed-dim: '#95d78e'
  on-primary-fixed: '#002203'
  on-primary-fixed-variant: '#135219'
  secondary-fixed: '#fce17e'
  secondary-fixed-dim: '#dfc566'
  on-secondary-fixed: '#221b00'
  on-secondary-fixed-variant: '#544600'
  tertiary-fixed: '#ffe16e'
  tertiary-fixed-dim: '#e1c554'
  on-tertiary-fixed: '#221b00'
  on-tertiary-fixed-variant: '#544600'
  background: '#fcf9f8'
  on-background: '#1c1b1c'
  surface-variant: '#e5e2e1'
typography:
  display-lg:
    fontFamily: Newsreader
    fontSize: 64px
    fontWeight: '400'
    lineHeight: '1.1'
    letterSpacing: -0.02em
  display-md:
    fontFamily: Newsreader
    fontSize: 48px
    fontWeight: '400'
    lineHeight: '1.1'
  headline-lg:
    fontFamily: Newsreader
    fontSize: 32px
    fontWeight: '500'
    lineHeight: '1.2'
  headline-md:
    fontFamily: Newsreader
    fontSize: 24px
    fontWeight: '500'
    lineHeight: '1.3'
  body-lg:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.6'
  body-md:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.6'
  label-lg:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '600'
    lineHeight: '1.2'
    letterSpacing: 0.05em
  label-sm:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '500'
    lineHeight: '1.2'
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  base: 8px
  section-gap: 80px
  golden-ratio-thin: 38.2%
  golden-ratio-wide: 61.8%
  gutter: 24px
  margin: 32px
---

## Brand & Gaya

Sistem desain ini mewujudkan **Garda Intelektual**, yaitu perpaduan antara wibawa institusi historis dan energi intelektual anak muda modern. Sistem ini dibangun sebagai lembar editorial digital untuk wacana ilmiah dan kepemimpinan komunitas.

Estetikanya condong pada gaya **Editorial Premium**. Fokus utamanya adalah kejernihan, wibawa, dan kekuatan kata. Hal ini dicapai melalui fondasi minimalis, glassmorphism yang halus, serta komposisi asimetris yang memecah pola layout korporat standar. Tujuannya adalah menghadirkan rasa seperti membaca jurnal premium, tempat setiap informasi terasa dikurasi dengan niat dan ketelitian.

## Warna

Palet warna berakar pada hijau tua yang terasa ilmiah, melambangkan pertumbuhan dan warisan institusi.

- **Primary & Container:** Dipakai untuk identitas utama dan elemen UI dengan prioritas tinggi. Gradien di antara dua hijau ini menciptakan kedalaman tanpa bergantung pada shadow berat.
- **Aksen Emas:** Warna emas gelap dan terang dipakai untuk penanda keunggulan, seperti penghargaan, tag penting, atau kontribusi ilmiah yang disorot.
- **Netralitas:** Charcoal (#5f5e5e) menjadi warna utama body text untuk mengurangi lelah mata, sementara Surface Low (#f3f3f3) memberi lapisan pemisah halus untuk konten sekunder.
- **Interaksi:** Perubahan state sebaiknya memakai opacity halus atau pergeseran background ke arah Primary Container, bukan menambah hue baru.

## Tipografi

Sistem desain ini memakai pasangan tipografi berkontras tinggi untuk memberi kesan otoritas intelektual.

- **Newsreader:** Typeface serif ini menjadi suara institusi. Gunakan untuk display text dan headline. Ukurannya harus cukup lega agar bentuk klasik dan detail elegannya terasa.
- **Inter:** Typeface fungsional dan netral untuk UI serta body copy panjang. Keterbacaannya menyeimbangkan karakter ekspresif headline serif.
- **Aturan Hirarki:** Jaga ritme vertikal yang jelas. Headline perlu ruang atas yang lebih besar daripada ruang bawah untuk membentuk alur editorial. Label sering memakai uppercase dan tracking ringan agar metadata UI berbeda dari konten utama.

## Layout & Spasi

Filosofi layout menolak grid simetris standar dan memilih **Asimetri Terarah** yang dipandu Golden Ratio.

- **Pembagian 38/62:** Layout utama membagi ruang horizontal menjadi 38% kolom pendukung dan 62% kolom konten. Ini menciptakan titik fokus alami yang terasa dirancang, bukan sekadar ditempatkan.
- **Whitespace Luas:** Konten tidak boleh terasa padat. Gunakan `section-gap` untuk jarak vertikal antar tema besar agar pengguna punya ruang memahami informasi.
- **Margin & Gutter:** Grid fluida 12 kolom dipakai untuk penempatan komponen internal, sementara wrapper halaman tetap memakai margin lebar agar terasa seperti lembar editorial cetak.

## Elevasi & Kedalaman

Kedalaman dalam sistem ini dicapai lewat efek atmosferik, bukan pembatas fisik yang keras.

- **Glassmorphism:** Navbar sticky memakai backdrop blur 12-20px dengan fill putih semi-transparan (#ffffff90). Ini menjaga konteks scroll tetap terasa ringan dan modern.
- **Ambient Shadow:** Shadow harus sangat lembut, memakai warna Primary (#00450d) pada opacity 4-8%. Hindari shadow abu-abu generik agar profil warna Garda Intelektual tetap kuat.
- **Tingkatan Surface:** Gunakan lapisan tonal dari Surface ke Surface Low untuk membangun hirarki. Border hitam 1px tidak boleh dipakai; jika batas benar-benar dibutuhkan, gunakan stroke #1b5e20 pada opacity 10%.

## Bentuk

Bahasa bentuk dikendalikan, halus, dan matang.

- **Corner Radius:** Radius dasar 0.25rem dipakai untuk elemen kecil seperti tag atau input. Elemen lebih besar seperti card dan button memakai `rounded-xl` (0.75rem) untuk melembutkan kesan intelektual dengan energi muda.
- **Bobot Visual:** Elemen harus terasa seperti stationery berkualitas. Card tidak perlu border; cukup gunakan perubahan background halus dari White ke Surface Low saat hover untuk memberi sinyal interaksi.

## Komponen

### Tombol
Tombol utama memakai **gradien 135 derajat** dari Primary (#00450d) ke Primary Container (#1b5e20). Radius wajib **0.75rem**. Tipografi tombol memakai Inter Bold, uppercase, 14px.

### Cards
Card adalah kontainer putih bersih dengan ambient shadow. Saat hover, card mengalami perubahan background halus atau sedikit penguatan shadow, tetap dengan radius 0.75rem.

### Sticky Navbar
Navbar menempel di atas dengan efek glassmorphism. Blur radius harus 12-20px. Link navigasi memakai Inter 14px Medium dengan underline emas gelap yang halus untuk state aktif.

### Field Input
Input bersifat minimalis, memakai Surface Low (#f3f3f3) sebagai warna isi dan radius 0.25rem. State focus mengganti tampilan borderless dengan glow lembut warna Primary.

### Aksen Editorial
Gunakan kutipan tarik dengan Newsreader Italic dan divider vertikal mengikuti garis pembagian 38/62 untuk memperkuat tema editorial.
