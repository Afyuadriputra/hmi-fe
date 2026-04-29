# PRD Frontend SI-HMI Pekanbaru & Integrasi API

## Ringkasan

Frontend publik React untuk SI-HMI Pekanbaru yang dibangun dengan Vite, TypeScript, Tailwind CSS, dan TanStack Query.

## Sistem Desain: "Editorial Intelektual"

- **Tipografi:** Newsreader (Judul), Inter (Isi).
- **Warna:** Hijau Tua (#00450d), Hijau Rimba (#1b5e20), Aksen emas, Permukaan netral.
- **Filosofi:** Editorial premium, tata letak Golden Ratio, ruang kosong luas, dan glassmorphism.

## Strategi Integrasi API

- URL Dasar: `http://127.0.0.1:8000`
- Client: Axios/Fetch wrapper in `src/lib/api.ts`.
- Manajemen State: TanStack Query for caching and server state.
- Formulir: React Hook Form + Zod.

## Roadmap Halaman

1. **Beranda:** `/api/v1/home/` - Hero multi-bagian, ringkasan berita, dan agenda.
2. **Organisasi:** Profil, kepengurusan, dan sejarah ketua umum.
3. **Program & Agenda:** Daftar dan halaman detail berbasis slug.
4. **Berita & Galeri:** Daftar berkategori dan halaman detail.
5. **Pendaftaran:** Direktori formulir yang terhubung ke Google Form.
6. **Interaksi:** Form kontak dan pengajuan upload berita dengan pelacakan.

## Cakupan Layar Statis

| Static Screen                              | Kontrak API Backend                                                      | Status      |
| ------------------------------------------ | ------------------------------------------------------------------------ | ----------- |
| `halaman_beranda/index.html`               | `GET /api/v1/home/`                                                      | Tersedia    |
| `profil_organisasi/code.html`              | `GET /api/v1/organization/profile/`                                      | Tersedia    |
| `kepengurusan_cabang/code.html`            | `GET /api/v1/organization/management/`                                   | Tersedia    |
| `sejarah_ketua_umum/code.html`             | `GET /api/v1/organization/chairmen/`                                     | Tersedia    |
| `direktori_program/code.html`              | `GET /api/v1/programs/`                                                  | Tersedia    |
| `detail_program/code.html`                 | `GET /api/v1/programs/:slug/`                                            | Ditambahkan |
| `direktori_agenda/code.html`               | `GET /api/v1/events/`                                                    | Tersedia    |
| `detail_agenda/code.html`                  | `GET /api/v1/events/:slug/`                                              | Ditambahkan |
| `arsip_berita/code.html`                   | `GET /api/v1/news/`, `GET /api/v1/news/categories/`                      | Tersedia    |
| `detail_artikel_berita/code.html`          | `GET /api/v1/news/:slug/`                                                | Tersedia    |
| `halaman_galeri/code.html`                 | `GET /api/v1/gallery/`, `GET /api/v1/gallery/categories/`                | Ditambahkan |
| `direktori_formulir_pendaftaran/code.html` | `GET /api/v1/registration-forms/`                                        | Tersedia    |
| `halaman_kontak/code.html`                 | `POST /api/v1/contact-messages/`                                         | Ditambahkan |
| `pengajuan_upload_berita/code.html`        | `POST /api/v1/news-requests/`, `POST /api/v1/news-requests/:id/payment/` | Tersedia    |
| `lacak_pengajuan_berita/code.html`         | `GET /api/v1/news-requests/track/:tracking_code/`                        | Ditambahkan |

## Catatan Mapping Field API

- Navigation must map from `home.navigation`: `title`, `url`, `location`, `sort_order`.
- Program detail must map: `title`, `slug`, `category`, `description`, `content`, `image`, `icon`, `button_text`, `button_link`, `registration_form_url`.
- Event detail must map: `title`, `slug`, `description`, `content`, `image`, `location`, `start_date`, `end_date`, `start_time`, `end_time`, `registration_form_url`.
- News archive filters must map from `news/categories`: `id`, `name`, `slug`, `description`.
- Gallery filters must map from `gallery/categories`: `id`, `name`, `slug`, `description`.
- Pendaftaran buttons must use `google_form_url`, never `href="#"` in final React implementation.
- News request success must show backend `tracking_code` UUID, not a handcrafted code.

## Status Navigasi Statis

Semua layar statis `code.html` sudah terhubung dengan path HTML relatif untuk navigasi prototipe. Tidak ada placeholder `href="#"` tersisa. Tombol Google Form eksternal memakai placeholder sementara `https://forms.google.com` dan harus diganti dengan `google_form_url` / `registration_form_url` dari backend saat dikonversi ke React.
