# 💡 Catatan Teori: Fondasi Grafika Komputer

## 1. Apa itu Grafika Komputer (Computer Graphics)?
Secara sederhana, Grafika Komputer adalah ilmu dan seni untuk menciptakan, memanipulasi, dan menampilkan gambar (visual) menggunakan komputer.

### Kategori Utama Gambar Digital:
* **Raster (Bitmap):**
    * Terbuat dari jaringan **piksel** (titik-titik warna).
    * Contoh: Foto digital (`.jpg`, `.png`).
    * Kelebihan: Detail warna yang kaya.
    * Kekurangan: **Pecah (pixelated)** jika diperbesar melebihi resolusi aslinya.
* **Vektor:**
    * Terbuat dari **jalur matematis** (garis, kurva, bentuk).
    * Contoh: Logo, ikon (`.svg`, `.ai`).
    * Kelebihan: **Resolusi independen**. Tidak akan pernah pecah, seberapa pun besarnya diperbesar.
    * Kekurangan: Tidak ideal untuk gambar fotorealistik.

**Grafika 3D pada dasarnya adalah bentuk canggih dari Vektor**, yang kemudian di-render menjadi gambar **Raster**.

## 2. Anatomi Objek 3D
Bagaimana komputer "melihat" objek 3D? Melalui tiga komponen inti:
* **Vertex (Titik):** Sebuah titik koordinat di ruang 3D (X, Y, Z).
* **Edge (Garis):** Garis lurus yang menghubungkan dua **Vertex**.
* **Face (Permukaan):** Permukaan datar (biasanya segitiga/segiempat) yang terbentuk dengan menghubungkan tiga atau lebih **Edge**.

Kumpulan dari Vertex, Edge, dan Face ini disebut sebagai **Mesh** atau **Polygon Mesh**. Inilah yang kita manipulasi di Blender.

## 3. Pipeline (Alur Kerja) Produksi 3D
Membuat film animasi 3D bukanlah satu langkah. Ini adalah proses linear yang kompleks (pipeline):

1.  **Konsep & Pre-produksi:** Ide, naskah, *storyboard*, *concept art*.
2.  **Modeling:** Proses "memahat" atau "membangun" bentuk objek 3D (Karakter, properti, lingkungan).
3.  **Texturing & Shading:** Memberi "warna", "material", dan "tekstur" pada model (misal: membuatnya terlihat seperti kayu, logam, atau kulit).
4.  **Rigging:** Memberi "tulang" (armature) pada karakter atau objek agar bisa digerakkan.
5.  **Animation:** Proses menggerakkan objek/karakter yang sudah di-*rig* berdasarkan *timeline*.
6.  **Lighting:** Menata pencahayaan virtual (seperti di studio foto) untuk menciptakan *mood* dan visibilitas.
7.  **Simulation / VFX:** Membuat efek khusus seperti asap, api, air, atau simulasi kain.
8.  **Rendering:** Proses di mana komputer "mengambil foto" adegan 3D dan mengubahnya menjadi gambar 2D (video/gambar) final. Ini bisa memakan waktu lama.
9.  **Compositing & Post-Processing:** Menggabungkan berbagai hasil *render* dan memberikan sentuhan akhir (koreksi warna, *glow*, dll).
