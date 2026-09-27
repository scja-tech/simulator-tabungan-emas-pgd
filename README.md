# Simulator Integrasi Tabungan Emas Pegadaian × N-Digi

Prototipe interaktif aplikasi mobile banking (N-Digi) sebagai *collecting agent* produk Tabungan Emas Pegadaian, lengkap dengan inspector API untuk melihat request/response di setiap langkah.

**Semua data adalah data tiruan (mock).** Simulator tidak terhubung ke server Pegadaian mana pun; respons dibuat oleh mock server di dalam halaman.

## Isi repositori

| File | Keterangan |
|---|---|
| `index.html` | Simulator siap pakai (dibuka langsung di browser / GitHub Pages) |
| `source.jsx` | Kode sumber sebelum dikompilasi, untuk dibaca atau dikembangkan |

## Fitur

- Alur buka rekening, top up, jual (buyback), transfer, cetak emas, riwayat, dan penautan rekening
- Panel skenario negatif SIT (rekening blokir, EOD, timeout + cek status & reversal, dll.)
- Panel presenter untuk memulai sesi nasabah baru
- Masking PII di inspector

## Struktur kode

1. **Mock server Pegadaian** — data & aturan sisi Pegadaian
2. **API client** — `API_MODE = "mock"`; mode `"dev"` disiapkan untuk proxy server-side
3. **Komponen UI** — satu komponen per layar
