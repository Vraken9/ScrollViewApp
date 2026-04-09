## Ringkasan Proyek

Dalam mengemas gulungan panjang selayaknya gulungan kertas prasejarah, halaman 
artikel perawatan bunga mempekerjakan asisten utama pembungkus `<ScrollView>` di
`6_ScrollViewApp`. Keterbatasan layar diakali secara cerdas; ScrollView wajib
sifatnya dipersenjatai semata-mata dengan satu balok pendamping utama selongsong
tambat (dalam hal ini `LinearLayout`), di mana elemen satu-satunya tersebut memeluk
hancurnya kepingan serentetan jalinan baris teks cerita, barisan ikon stempel, serta 
sisipan foto raksasa secara utuh. Properti pendorongnya, yaitu `fillViewport="true"`,
ditancapkan menyelamatkan muka layar guna meregangkan pelat kosong memblok peranti 
batas akhir bila konten ternyata melengkung surut atau kehabisan durasi pemanjangan.

## Dokumentasi Teknis

### 1. Penjelasan File Resource Pendukung

Menjejaring antarmuka yang membosankan membedah estetika artikel majalah bertumpu
pada perbendaharaan silsilah tabung *color index* yang memadai.

-   **Fungsinya:** Diarahkan memberi patokan palet hitam kepucatan (`text_dark`), 
    bayang abu seia sekata (`text_light`), membelah bilah penyekat (`divider_color`)
    serta merekam corak kekosongan gambar selagi jaringan tumpul melambat 
    (`img_placeholder`). Pemisahan strata ini menyangkut kesehatan membaca audiens.
-   **Mengapa dipisah?:** Dokumentasi literatur acap kali mengandalkan kelembutan
    kombinasi beralih fasa antar rezim Gelap Terang Mode Ponsel (*Dark / Light*). 
    Mempertebal penempatan pigmen sentral mencegah rutinitas pembantaian kodingan 
    yang menjemukan jika terjadi migrasi fasa malam tanpa mencederai tatanan teks.

### 2. Penjelasan Logika Layout Utama (`activity_main.xml`)

Kecongkakan posisi View manapun akan terlucuti habis saat menabrak batas ubin pixel
bagian kaki hp, maka dipanggil sebuah payung penyapu batas, the **ScrollView**.

-   **Peraturan Ketat Hukum Tunggal (Single Child Policy)**: ScrollView itu makhluk
    bisu penggulung, ia tidak mendikte ruang melainkan cangkangnya. Aturan kodrati
    mewajibkan: jangan pernah menjejalkan 2 pelopor ke dalamnya, bungkuslah semuanya
    dengan wadah tas plastik tunggal berupa balok vertikal pendistribusi (*LinearLayout*).
    Penembusan aturan ini berganjar remuknya layar secara prematur bertajuk *Crash*.
-   **`android:fillViewport="true"`**: Andai artikel hampa tanpa tulisan, cangkang 
    gulung layu memendek mengerut berantakan secara kodrati. Suntikkan pelicin *line*
    ini merapal keajaiban merenggang memaksa karet perekat menyentuh lantai mentok 
    menahan sisa-sisa pelat latar belakang warna gading di layarnya tetap megah berkelas.

### 3. Alur Visual

Arus mengantarkan bahtera tatapan membentangi kanvas artikel secara mendalam:

1.  **Kanopi Foto Pelopor**: Langit dibelah mendadak hantaman rongga kosong tiruan 
    *(Image Placeholder)* membawakan cuplikan pesona kuncup rimbun mencuri tatapan 
    tiga puluh persen daratan paling utara layar gawai.
2.  **Identitas Penulis Lintas Jalur**: Mendadak muncul nama kebanggaan majalah, 
    tanggal rilis tinta, dan logo penulis yang mematah rute silang membentang tegak 
    horizontal bersanding kawan (dijaga elemen balok penyerap *LinearLayout* kecil).
3.  **Tsunami Huruf Spasi Udara**: Melampaui sekat batas tipis *divider*, meluncurlah
    banjir lahar tulisan artikel panjang menjejali layar, diatur berspasi sela 
    napasan legah (`lineSpacingExtra`) supaya irigasi membaca manusia pelan 
    dinikmati dengan nyaman dan estetis, sesekali dibentur tiang lampu pijar kutipan
    para ahli dalam keranjang berbingkai abu murni.
4.  **Tembakan Akhir Halaman**: Guliran merangkak jauh menuju peluit pungkas, ditaburi
    bintang kelap-kelip pualam kepuasan perawi ulasan, ditutup tombol palang pintu "Ayo Beli Koleksinya". Menuntaskan perjalanan panjang seluncur tak berhingga!
