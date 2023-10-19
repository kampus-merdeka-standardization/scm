# Versioning

## Semantic Versioning

Pembuatan versi semantik (juga dikenal sebagai SemVer) adalah sistem pembuatan versi yang sedang meningkat selama beberapa tahun terakhir. Ini selalu menjadi masalah bagi pengembang perangkat lunak, manajer rilis, dan konsumen. Memiliki cara universal untuk membuat versi proyek pengembangan perangkat lunak adalah cara terbaik untuk melacak apa yang terjadi dengan perangkat lunak saat plugin, add-on, perpustakaan, dan ekstensi baru dibuat hampir setiap hari. Masalah ini dapat diatasi dengan Pembuatan Versi Semantik. Singkatnya, ini adalah cara untuk memberi nomor pada rilis perangkat lunak.

Jadi SemVer berbentuk Major.Minor.Patch.

![Semantic](https://media.geeksforgeeks.org/wp-content/uploads/semver.png)

Semantic Versioning merupakan bilangan 3 komponen dalam format X.Y.Z, dimana :
- X adalah singkatan dari versi **Major**. Angka paling kiri menunjukkan versi mayor. Saat Anda menambah nomor versi mayor, Anda menambahnya satu tetapi Anda menyetel ulang versi patch dan versi minor ke nol. Jika versi saat ini adalah 2.6.9 maka upgrade berikutnya untuk versi mayor adalah 3.0.0. Tingkatkan nilai X ketika 
- Y adalah singkatan dari versi **Minor**. Ini digunakan untuk merilis fungsionalitas baru dalam sistem. Ketika Anda meningkatkan versi minor, Anda menambahnya satu tetapi Anda harus mengatur ulang versi patch ke nol. Jika versi saat ini adalah 2.6.9 maka upgrade berikutnya untuk versi minor adalah 2.7.0. Tingkatkan nilai Y ketika mengimplementasikan fitur baru yang kompatibel dengan versi sebelumnya.
- Z adalah singkatan dari Versi **Patch**: Versi patch digunakan untuk perbaikan bug. Tidak ada perubahan fungsionalitas pada peningkatan versi patch. Jika versi saat ini adalah 2.6.9 maka versi berikutnya untuk peningkatan patch adalah 2.6.10. Tidak ada batasan untuk angka-angka ini. Tingkatkan nilai Z saat memperbaiki bug

Pengidentifikasi yang valid ada di set [A-Za-z0-9] dan tidak boleh kosong. Metadata pra-rilis diidentifikasi dengan menambahkan tanda hubung di akhir urutan SemVer. Jadi pra-rilis untuk versi 1.0.0 bisa jadi 1.0.0-alpha.1. Lalu jika diperlukan build lain, menjadi 1.0.0-alpha.2, dan seterusnya. Perhatikan bahwa nama tidak boleh berisi angka nol di depannya, namun tanda hubung diperbolehkan dalam nama untuk pengidentifikasi pra-rilis. 

![versioning](https://media.geeksforgeeks.org/wp-content/uploads/20201021010157/SemanticVersioning.png)

![possible version upgrades](https://media.geeksforgeeks.org/wp-content/uploads/20201021015029/WINWORD3DROTliALc.png)

### Kelebihan

- Anda dapat melacak setiap transisi dalam fase pengembangan perangkat lunak.
- Pembuatan versi dapat menjelaskan kepada pengembang tentang jenis perubahan apa yang telah terjadi dan kemungkinan pembaruan yang harus dilakukan pada perangkat lunak.
- Membantu menjaga segala sesuatunya tetap bersih dan bermakna.
- Membantu orang lain yang mungkin menggunakan proyek Anda sebagai ketergantungan.

### Poin yang perlu diingat

- Versi pertama dimulai pada 0.1.0 dan bukan pada 0.0.1, karena tidak ada perbaikan bug yang dilakukan, kami memulai dengan serangkaian fitur sebagai draf pertama proyek.
- Sebelum 1.0.0 hanyalah Fase Pengembangan, di mana Anda fokus menyelesaikan sesuatu. Tahap ini diperuntukkan bagi pengembang dimana sistem sedang dikembangkan.
- SemVer tidak mencakup perpustakaan yang diberi tag 0. * . *. Versi stabil pertama adalah 1.0.0.2

### Referensi

- [Introduction to Semantic Versioning](https://www.geeksforgeeks.org/introduction-semantic-versioning/)

## Calendar Versioning

CalVer, atau Calendar Versioning, adalah skema pembuatan versi populer lainnya yang semakin banyak diadopsi selama beberapa tahun terakhir. Daripada menggunakan nomor sembarangan, CalVer memilih untuk menggunakan nomor yang cocok dengan informasi kalender versi tertentu yang dirilis, misalnya. 2020–05, 2020.05, 20.05 (semuanya menunjukkan waktu rilis Mei 2020).

Mirip dengan SemVer, CalVer dapat terdiri dari beberapa segmen angka dan pengubah. Segmen pertama biasanya memuat informasi tahun, yang dapat berupa tahun penuh (YYYY), tahun pendek (YY), atau *zero-padded year* (0Y, relatif terhadap tahun 2000). Segmen kedua dapat berupa informasi kalender lainnya (misalnya bulan — MM/0M), atau nomor rilis tambahan pada tahun tersebut.

![calver parts](https://miro.medium.com/v2/resize:fit:1100/format:webp/0*djbnhOT72Kp0NG8D.png)

Dalam contoh di atas, segmen pertama adalah nomor tahun penuh, diikuti dengan nomor rilis tahun ini (segmen ke-2), nomor build rilis (segmen ke-3), dan status rilis (segmen ke-4). Anda mungkin memperhatikan bahwa versi ini sebenarnya menggunakan skema campuran yang menyertakan karakteristik CalVer dan SemVer.

CalVer biasanya dipilih oleh proyek jika mereka ingin mengatur irama yang stabil dan ekspektasi pengguna untuk waktu rilis versi mendatang. Pembuatan versi proyek Ubuntu adalah contoh yang baik dari CalVer, yang tidak hanya mudah untuk mengetahui kapan versi tertentu dirilis, tetapi juga apakah versi tersebut merupakan versi *Long-term support* (LTS), cukup dengan mengacu pada digit terakhir versi tersebut.

### Referensi 

- [SemVer and CalVer](https://nehckl0.medium.com/semver-and-calver-2-popular-software-versioning-schemes-96be80efe36)

## Build Number

Build number versioning adalah salah satu metode untuk mengelola versi perangkat lunak, terutama perangkat lunak yang dikembangkan secara iteratif. Metode ini biasanya digunakan dalam pengembangan perangkat lunak untuk memantau perubahan dan pembaruan yang terjadi pada setiap versi perangkat lunak. Sistem build number versioning sering digunakan bersamaan dengan versi perangkat lunak dan nomor revisi.

Contoh build number versioning: 1.2.345
- "1" adalah versi utama (Major Version).
- "2" adalah nomor revisi (Minor Version).
- "345" adalah nomor build.

Versi Perangkat Lunak (Major Version): Versi perangkat lunak adalah nomor utama yang menunjukkan perubahan besar atau fitur utama baru dalam perangkat lunak. Ketika ada perubahan signifikan dalam perangkat lunak, nomor versi utama ini akan ditingkatkan. Contohnya, perubahan dari versi 1.0 ke 2.0 mungkin menandakan perubahan besar dalam perangkat lunak tersebut.

Nomor revisi mengacu pada perubahan kecil atau perbaikan dalam perangkat lunak. Ketika ada pembaruan yang memperbaiki bug atau menambahkan perbaikan kecil, nomor revisi akan ditingkatkan. Contohnya, perubahan dari versi 1.1 ke 1.2 mungkin menandakan adanya perbaikan bug atau pembaruan kecil lainnya.

Nomor build adalah bagian dari sistem build number versioning yang paling sering berubah. Setiap kali perangkat lunak dikompilasi (dibangun) dari kode sumbernya, nomor build akan ditingkatkan. Ini biasanya mencakup perubahan yang sangat kecil, seperti perubahan kosmetik, perubahan konfigurasi, atau perubahan kecil lainnya yang tidak memengaruhi fungsionalitas utama perangkat lunak.

Sistem build number versioning membantu tim pengembang melacak evolusi perangkat lunak dan memberikan pemahaman yang lebih baik tentang apa yang telah berubah dalam setiap iterasi. Ini juga memudahkan pengembang dalam melacak dan memecahkan masalah, karena mereka dapat merujuk ke nomor build tertentu untuk memahami riwayat perubahan dan menemukan penyebab masalah.