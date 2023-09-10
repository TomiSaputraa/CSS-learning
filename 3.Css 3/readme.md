# 1. Definisi

Kenapa css 3?

- membuat website lebih fleksibel
- Membuat mockup lebih cepat tanpa bantuan scripting
- mengurangi penggunaan gambar = kecepatan load halaman
- penggunaan selector untuk menghindari penggunaan mark up yang boros

# 2. border-radius(px) :

Fungsinya membuat ujung kotak menjadi tumpul

# 3. opacity(RGBa)/(0-1)

sering digunakan untuk transparansi pada elemen
agar child dari parent tidak ikut transparan bisa dengan RGBa dibawah

# 4. RGBa & HSLa

RGBa/RGB (Red, green, blue, alpha/opacity) / (Red, green, blue) digunakan untuk transparansi pada warna
HSLa(hue, saturation, lightness, alpha)

# 5. Box-shadow :

digunakan untuk memberikan bayangan pada elemen yang kita buat

- inset(optional) -> ini akan membuat bayangan didalam box
- x-offset -> kiri kanan negatif untuk ke kiri
- y-offset -> atas bawah negatif untuk ke atas
- blur
- spread(optional) -> untuk menyebar shadow
  -> negatif akan membuat shadow semakin kecil
- color
  multiple shadow bisa ditambahkan setelah warna dengan ","
  multiple shadow bisa dibuat jumlahnya berapa pun

# 6. text-shadow :

- x-offset -> kiri kanan negatif untuk ke kiri
- y-offset -> atas bawah negatif untuk ke atas
- blur
- color
  bisa juga multiple color seperti box-shadow

# 7. linear-gradient

digunakan untuk membuat warna gradiasi pada sebuah elemen
color stop -> digunakan untuk berapa banyak lokasi warna yang akan dibuat

- linear-gradient -> memberikan warna secara garis lurus
  -> bisa untuk background :
  -> bisa untuk background-image :
  -> bisa diberikan multiple color
  -> bisa color stop
- radial-gradient -> properti sama dengan linear
  -> memberikan warna secara melingkar
  -> bisa diberikan multiple color
  -> bisa color stop
  -> tipe : elipse(default), circle

# 8. @font-face

digunakan untuk mengelola font pada css kita
pastikan font yang akan digunakan support web browser
untuk web disarankan menggunakan format .woff karena lebih cepat
untuk mengubah font .ttf menjadi .woff bisa disini :
'https://www.fontsquirrel.com/tools/webfont-generator'
'https://caniuse.com/'
'https://pleeease.iamvdo.me/play/' disini lebih bagus

# 9. Vendor prefix

karena tidak semua browser support css3
sintaks spesifik untuk tiap browser atau vendor
untuk cek apakah perlu prefix atau tidak disini "https://shouldiprefix.com/"

- -webkit-<properti css3> -> chrome,safari, opera versi terbaru
- -moz-<properti css3> -> firefox
- -ms-<properti css3> -> internet explorer
- -o-<properti css3> -> opera terlebih dahulu

# 10. Filter

meberikan efek visual pada gambar, background atau border
filter akan menggunakan hardware jadi akan lebih cepat

- blur(px)
- brightness(angka | %)
- contrast(angka | %)
- saturate(angka | %)
- grayscale(angka | %)
- sepia(angka | %)
- hue-rotate(deg)
- invert(angka | %)
- opacity(angka | %)
- drop-shadow(sama seperti box-shadow) bedanya drop shadow akan memberikan shadow pada objek nya bukan pada kotak/box nya

# 11. transform

yang memungkinkan kita dapat memanipulasi format visual dari elemen html
transform ada 2 jenis : 2D & 3D

- scale (angka) ->memperbesar /kecil
- rotate(deg) -> memutar
- skew (deg) -> membuat condong atau miring
- translate (px,px)-> translate / ubah posisi

# 12. transition

memungkinkan kita dapat mengubah nilai dari properti html secara halus
hanya ada state awal dan state akhir

- property -> all(default) / bisa memilih salah satu properti dalam hover
- duration (wajib) -> s/ms
- fungsi -> ease(default), ease-in(makin akhir makin cepat),ease-out, ease-in-out, linear, cubic-bezier(w,x,y,z) / bisa gunakan tool chrome
- delay -> waktu tunggu sebelum menjalankan posisi nya s/ms

# 13. animation

banyak state degan cara menambahkan keyframe
sebelum memanggil animation harus membuat keyframe

- name(wajib) -> nama dari animasi yang harus sama dengan nama keyframe
- duration -> durasi dari animasi s/ms
- timing-function -> ease,ease-in,ease-out, ease-in-out, linear, cubic-bezier(w,x,y,z)
- delay -> sama dengan transition s/ms
- iteration-count -> angka/infinite, berapa kali diulang/ terus menerus
- direction -> normal/reverse/alternate/alternate-reverse
- fill-mode -> none/forward/backwards/both, akhir dari transisi seperti apa
- play-state -> running(default)/paused, untuk berjalan dan berhenti
  @keyframe [name] {
  from {
  [property css]
  }
  to {
  [property css]
  }
  }
