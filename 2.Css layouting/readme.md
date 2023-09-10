# 1. Display

setiap tag pada elemen html berada dalam sebuah KOTAK.
properti display mengatur perilaku dari KOTAK tersebut.

- <div> : default display adalah block
- <span> : default display adalah inline
  value display :
- inline -> block akan membuat elemen dibaris yang sama/row
  -> elemen html secara default tidak akan menambahkan baris baru ketika dibuat
  -> Lebar dan tinggi elemennya sebesar kontent yang ada di dalamnya
  -> kita tidak dapat mengatur tinggi dan lebar
  -> margin dan padding hanya mempengaruhi elemen secara horizontal, tidak vertikal
- inline-block -> tidak ada elemen default memiliki inline-block
  -> kita harus ubah manual properti tersebut
  -> perilaku dasarnya sama dengan inline
  -> kita dapat mengatur lebar dan tinggi
- block -> block akan otomatis membuat baris baru/column
  -> jika tidak di atur maka lebar default akan memenuhi lebar dari parent/browser
  -> kita dapat mengatur tinggi dan lebar dari elemen block
  -> didalam elemen block, kita dapat menyimpan tag dengan elemen di atas maupun block lagi
- none -> menghilangkan sebuah elemen

# 2. Dimensi & overflow

- Dimensi -> width & height
- overflow -> visible,auto,hidden dan scroll

# 3. Box model

- setiap elemen berada didalam box/kotak
- kita bisa mengatur width dan height dan posisi kotak tersebut
- bisa diberi warna background
- terdiri dari MARGIN,padding, BORDER dan content

# 4. margin

- overlaping ->
  margin vertikal akan memilih margin yang paling besar.
  margin horizontal akan menambahkan margin.
- negatif ->
- auto -> nilai khusus untuk kiri dan kanan
- shorthand -> margin: atas kanan bawah kiri

# 5. padding,border & box-sizing

- padding -> tidak bisa auto, tidak bisa negatif & menambah ukuran elemen
- border -> border: width style color;
- box-sizing -> digunakan agar padding & border tidak menambah ukuran box secara otomatis

# 6. reset

digunakan untuk mereset properti default elemen seperti body,h1-h6,p dll

# 7. Float

untuk mengatur posisi sebuah elemen.
sebuah elemen dapat dipaksa untuk berada di sebelah kiri atau kanan dari parentnya
normal nya elemen adalah normal flow, sedangkan dengan float dibuat secara out of flow
makanya dibutuhkan clear dibawah untuk fix out of flow tersebut.

- none
- left
- right

# 8. clear

berfungsi untuk menghentikan / membersihkan float.
clear digunakan untuk mengatasi float yang keluar dari container

- left
- right
- both
  menggunakan properti overflow: auto
  atau lebih bagus dengan -> micro clearfix(google)

# 9. position

Jika kita tidak memberikan properti position pada elemen maka default properti nya static.

- static -> nilai default tiap elemen ketika tidak di berikan position
  -> elemen yang diberikan position selain static(non static) dapat menggunakan properti top,left,right,bottom
- relative -> elemen akan maju 1 Dimensi
  -> ketika menggerakan(top,left dll) ruang yang di tempati masih ada
  -> jika memberi elemen top:0; dan left:0; maka elemen tidak akan berubah posisinya
- absolut -> ketika menggerakan posisinya ruang yang ditempati oleh elemen tersebut dianggap tidak ada
  -> berbeda dengan relative, absolut akan bergerak relatif terhadap parentnya >
  selama posisi parent nya juga non static
- fixed -> ketika diberi properti left/right dll maka posisi nya akan relatif terhadap parent(browsernya)
  -> biasanya sering digunakan untuk membuat navbar

# 10. Z-index & dll (dari position)

- hanya berlaku pada elemen non static
- kita bisa membuat lebar,tinggi,kanan & kiri container dengan menggunakan properti left,right dll
  contohnya :
  top: 100px;
  left: 100px;
  bottom: 100px;
  right: 100px;
  Maka akan membentuk kotak karna setiap value nya akan saling menarik
