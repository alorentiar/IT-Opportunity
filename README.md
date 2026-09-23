# IT-Opportunity

Kurasi peluang di bidang IT: **ide bisnis, sinyal pasar, dan tren teknologi** yang
dikumpulkan otomatis dari sumber publik.

## Apa isinya

Folder [`opportunities/`](opportunities/) berisi satu file per hari
(`YYYY-MM-DD.md`). Setiap file punya:

- **tabel ringkas** — waktu, skor, judul, sumber, tautan
- **detail per jam** — konteks kenapa sebuah sinyal dianggap menarik

File yang sama di-append setiap jam, jadi satu file = seluruh peluang hari itu.

## Dari mana datanya

| Sumber | Sinyal yang diambil |
| --- | --- |
| **Ask HN** | Apa yang sedang orang-orang kesusahan |
| **Show HN** | Apa yang sedang dibangun dan dapat perhatian |
| **RemoteOK** | Skill yang sedang dibayar perusahaan |
| **ArbeitNow** | Permintaan kerja lebih luas |
| **GitHub trending** | Ke mana perhatian developer bergerak |

Semuanya API publik tanpa key.

## Bagaimana skornya dihitung

Setiap sinyal diberi skor 0–100 dari lima fakta yang bisa diukur:

| Sinyal | Bobot | Arti |
| --- | --- | --- |
| Demand | 35 | Seberapa ramai dibicarakan |
| Momentum | 25 | Seberapa baru, turun separuh tiap 3 hari |
| Spesifisitas | 20 | Seberapa konkret masalahnya |
| Market | 12 | Apakah perusahaan membayar untuk ini |
| Kebaruan | 8 | Belum pernah muncul sebelumnya |

**Tidak ada LLM dalam proses ini.** Penilaian murni aritmetika atas data yang
terukur, jadi hasilnya bisa direproduksi dan biayanya nol.

## Cara membaca file

Contoh entri:

```markdown
| Waktu | Skor | Peluang | Sumber | Tautan |
| --- | --- | --- | --- | --- |
| 14:00 | 72 | Show HN: Self-hosted analytics for small teams | Show HN | [buka](...) |
```

Skor tinggi berarti **bukti kuat bahwa ada kebutuhan nyata** — bukan jaminan
pasar. Skor rendah bukan berarti buruk, hanya bukti pendukungnya lebih sedikit.

## Repositori terkait

Kode dan arsip lengkapnya ada di
[business-idea-radar](https://github.com/alorentiar/business-idea-radar).

## Catatan

Repositori ini diperbarui otomatis setiap jam. Tidak ada kontribusi manual yang
diharapkan, tapi kalau ada tautan mati atau usulan sumber baru, silakan buka
issue.
