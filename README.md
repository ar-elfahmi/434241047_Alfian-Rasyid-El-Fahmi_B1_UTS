# E-Ticketing Helpdesk

Aplikasi mobile helpdesk untuk pelaporan, monitoring, dan penyelesaian tiket layanan IT.

## Fitur Utama

- Multi role: User, Helpdesk, Admin
- Autentikasi login dan registrasi berbasis dummy repository
- Dashboard statistik tiket dan daftar tiket terbaru
- Manajemen tiket: list, filter, search, detail, timeline, komentar
- Create tiket baru dengan kategori, prioritas, dan lampiran dummy
- Notifikasi update tiket
- Profil pengguna + toggle dark/light mode

## Arsitektur

Project menerapkan Feature-First + Provider + Repository Pattern:

- core:
  - constants, theme, services, reusable widgets
- features:
  - auth, dashboard, ticket, notification, profile
  - tiap fitur memiliki data dan presentation layer
- data layer:
  - abstract repository interface + implementasi dummy

Semua provider bergantung ke interface repository, sehingga migrasi backend ke Supabase cukup mengganti implementasi repository pada injection di main.

## Menjalankan Project

1. Install dependency

   flutter pub get

2. Jalankan aplikasi

   flutter run

3. Analisis code

   flutter analyze

4. Jalankan test

   flutter test

## Akun Demo

- User: user / password123
- Helpdesk: helpdesk / password123
- Admin: admin / password123

## Struktur Penting

- lib/main.dart
- lib/app.dart
- lib/core/
- lib/features/

## Catatan

- Data saat ini masih dummy data in-memory.
- Rencana migrasi backend Supabase mengikuti implementation plan pada phase berikutnya.
# -E-Ticketing-Helpdesk
