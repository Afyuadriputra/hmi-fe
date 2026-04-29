Kesimpulan: sekarang kontrak API frontend static sudah selaras dengan public API backend Django untuk kebutuhan setup React nanti.

Saya juga memperbaiki mismatch kecil di halaman pengajuan_upload_berita/code.html:

requester_name
requester_email
requester_phone
title
category
content
image
attachment
payment_method
payment_proof
Sekarang halaman itu sudah jelas mengarah ke:

POST /api/v1/news-requests/
POST /api/v1/news-requests/:id/payment/
Coverage frontend static sekarang:

Beranda -> GET /api/v1/home/
Profil -> GET /api/v1/organization/profile/
Kepengurusan -> GET /api/v1/organization/management/
Sejarah Ketua Umum -> GET /api/v1/organization/chairmen/
Program -> GET /api/v1/programs/
Detail Program -> GET /api/v1/programs/:slug/
Agenda -> GET /api/v1/events/
Detail Agenda -> GET /api/v1/events/:slug/
Wacana/Arsip -> GET /api/v1/news/, GET /api/v1/news/categories/, filter category
Detail Artikel -> GET /api/v1/news/:slug/
Galeri -> GET /api/v1/gallery/, GET /api/v1/gallery/categories/, filter category
Form Pendaftaran -> GET /api/v1/registration-forms/
Kontak -> POST /api/v1/contact-messages/
Ajukan Berita -> request + payment proof
Lacak Pengajuan -> GET /api/v1/news-requests/track/:tracking_code/
Validasi:

NO_BROKEN_RELATIVE_LINKS
OpenAPI backend: Errors: 0
Ada 1 warning enum status dari drf-spectacular, tidak mengganggu API. Itu hanya nama enum schema karena beberapa model sama-sama punya field status.
Catatan penting: frontend ini masih static HTML prototype, belum fetch API sungguhan. Tapi sebagai acuan setup React/Vite nanti, endpoint, payload, dan field utamanya sudah cocok dengan backend.