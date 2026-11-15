# nabail.xoic.space — portofolio video editor

Website statis (tanpa build) untuk Cloudflare Pages. Isi website dibaca dari folder `content/`,
jadi kamu cukup mengubahnya lewat panel `/admin` tanpa menyentuh kode.

```
index.html             halaman utama
admin/                 panel admin (login pakai token GitHub)
content/works.json     semua karya (urutan = urutan tampil)
content/site.json      kontak, intro hero, testimonial, milestones, harga
videos/                file video (maks 25 MB per file)
thumbs/                thumbnail video
img/                   foto, cover, gambar social media
```

## Cara update

1. Buka `https://nabail.xoic.space/admin/`
2. Tempel token GitHub, klik **Sign in**
3. **Works** — tambah/hapus karya, upload video (thumbnail dan durasi terisi otomatis),
   atur urutan dengan drag. **Site settings** — kontak, testimonial, angka, harga.
4. Klik **Publish**. Cloudflare men-deploy ulang sekitar 1 menit.

## Token admin (sekali saja)

GitHub → Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token
- Repository access: **Only select repositories** → repo ini
- Repository permissions → **Contents: Read and write**

Simpan token di password manager. Jangan dibagikan.

## Batas file

Cloudflare Pages: maksimal **25 MB per file**. Video lebih besar harus dikompres dulu
(720p, bitrate lebih rendah). Panel admin menolak file di atas batas ini.
