# Branching Strategies

## Apa itu Branching Strategies

Branching Strategies adalah strategi yang diterapkan oleh tim pengembangan perangkat lunak saat menulis, menggabungkan, dan menerapkan kode saat menggunakan sistem kontrol versi. Ini pada dasarnya adalah seperangkat aturan yang dapat diikuti pengembang untuk menentukan bagaimana mereka berinteraksi dengan basis kode bersama.

<img src= https://i.ytimg.com/vi/Bg8tiOLZw4A/maxresdefault.jpg>

Branching memungkinkan tim pengembang untuk berkolaborasi dengan mudah di dalam satu basis kode pusat. Ketika pengembang membuat cabang, sistem kontrol versi membuat salinan basis kode pada titik waktu tersebut. Perubahan pada cabang tidak mempengaruhi pengembang lain dalam tim

Strategi ini sangat penting dalam siklus hidup pengembangan perangkat lunak karena memungkinkan tim untuk bekerja secara paralel pada fitur yang berbeda tanpa mengganggu pekerjaan orang lain. Ini juga memfasilitasi proses seperti code review, integrasi terus menerus (CI), dan penyebaran terus menerus (CD) yang merupakan bagian penting dari praktik pengembangan perangkat lunak modern.

Dengan strategi branching yang efektif, tim dapat mengelola dan mengontrol perubahan kode dengan lebih baik, meminimalkan risiko bug dan konflik, dan pada akhirnya menghasilkan produk perangkat lunak yang lebih stabil dan berkualitas tinggi.

#### Referensi:
- [Branching Strategies](https://www.abtasty.com/blog/git-branching-strategies/)
- [Software Development Branching](https://www.atlassian.com/agile/software-development/branching)

## Jenis-Jenis Branching Strategies

Ada beberapa jenis strategi branching yang umum digunakan dalam pengembangan perangkat lunak, antara lain:

1. **GitFlow**: GitFlow adalah salah satu strategi branching yang paling populer dan banyak digunakan . Strategi ini melibatkan dua cabang utama dengan durasi hidup tak terbatas: `master` dan `develop`. Cabang `master` mencerminkan versi produksi saat ini, sementara cabang `develop` adalah tempat pengembangan aktif berlangsung.

2. **GitHub Flow**: GitHub Flow adalah strategi branching yang lebih sederhana dibandingkan GitFlow . Dalam GitHub Flow, tidak ada cabang `develop`. Sebaliknya, semua perubahan dilakukan di cabang fitur yang dibuat dari `master`, dan kemudian digabungkan kembali ke `master` ketika mereka siap untuk diterapkan.

3. **Trunk Based Development**: Trunk Based Development adalah strategi branching di mana semua pengembangan dilakukan di satu cabang utama (biasanya disebut `trunk` atau `main`), dengan cabang fitur yang digunakan hanya untuk perubahan jangka pendek. Tujuannya adalah untuk mendorong integrasi terus-menerus dan menghindari "merge hell" yang bisa terjadi ketika banyak cabang jangka panjang beroperasi secara simultan.

4. **Release Branching**: Dalam strategi ini, rilis tertentu dikandung sepenuhnya dalam sebuah cabang. Ini berarti bahwa pada akhir siklus pengembangan, manajer rilis akan membuat cabang dari kode utama (misalnya, "cabang pengembangan 1.1"). Semua perubahan untuk rilis 1.1 harus diterapkan dua kali: sekali ke cabang 1.1 dan kemudian ke kode utama.

5. **Feature Branching**: Cabang fitur sering dikaitkan dengan fitur bendera - "toggle" yang mengaktifkan atau menonaktifkan fitur dalam produk. Hal ini memudahkan penyebaran kode ke kode utama dan mengontrol kapan fitur diaktifkan, memudahkan penyebaran kode jauh sebelum fitur terpapar ke pengguna akhir.

Setiap strategi memiliki kelebihan dan kekurangan tersendiri, dan tim harus memilih strategi yang paling sesuai dengan kebutuhan mereka.

#### Referensi:
- [Branching Strategies](https://www.abtasty.com/blog/git-branching-strategies/)
- [Software Development Branching](https://www.atlassian.com/agile/software-development/branching)



## GitFlow

<img src = "https://wac-cdn.atlassian.com/dam/jcr:8f00f1a4-ef2d-498a-a2c6-8020bb97902f/03%20Release%20branches.svg?cdnVersion=1280">

GitFlow adalah salah satu strategi branching yang sangat populer dan banyak digunakan. Strategi ini melibatkan dua cabang utama dengan durasi hidup tak terbatas: `master` dan `develop`. Cabang `master` mencerminkan versi produksi saat ini, sementara cabang `develop` adalah tempat pengembangan aktif berlangsung.

GitFlow adalah pola branching model yang digunakan pada suatu kolaborasi menggunakan version control GIT. Pada setiap branch, nantinya akan disatukan dan menghasilkan suatu produk yang utuh. Model ini dinilai merupakan suatu hal yang cocok untuk melakukan kolaborasi dan mengukur pekerjaan suatu developer team.

GitFlow membagi repo kedalam 2 branch utama, yaitu master dan develop. Branch master adalah branch yang siap atau yang sedang live di production, sedangkan branch develop adalah branch yang masih dalam tahap pengembangan.

GitFlow adalah sebuah fitur dari Git yang digunakan untuk keperluan desain alur kerja, yang dapat digunakan untuk mendefinisikan model percabangan alur kerja secara jelas dan efisien. Gitflow adalah aturan-aturan yang disepakati oleh tim agar selama proses pengerjaan project terbentuk alur yang jelas.

#### Referensi:
- [Konsep dasar Git dan Gitflow](https://medium.com/@antoeldi/konsep-dasar-git-dan-gitflow-71e33cea6a5f)
- [Git dan Gitflow](https://medium.com/@dicky.dwi.r/git-dan-git-flow-6b1f79c4c26c)
- [Keuntungan dan cara kerja Gitflow](https://medium.com/pdb-r/keuntungan-dan-cara-kerja-git-flow-63ab526e5385)
- [Gitflow Workflow](https://medium.com/@rizael.ichigo28/gitflow-workflow-463645732a29)


## Trunk Based Development

<img src="https://statusneo.com/wp-content/uploads/2022/08/tbd_workflow.drawio-1-1.png"/>

Trunk Based Development (TBD) adalah strategi pengembangan perangkat lunak di mana pengembang menggabungkan setiap fitur baru, perbaikan bug, atau perubahan kode lainnya ke satu cabang pusat dalam sistem kontrol versi. Cabang ini disebut "trunk", "mainline", atau dalam Git, "master branch".

TBD adalah strategi pengembangan perangkat lunak di mana para insinyur menggabungkan perubahan yang lebih kecil lebih sering ke basis kode utama dan bekerja dari salinan trunk daripada bekerja pada cabang fitur jangka panjang. Model pengembangan ini sering digunakan sebagai bagian dari alur kerja pengembangan integrasi terus-menerus.

Dalam TBD, setiap pengembang membagi pekerjaan mereka menjadi batch kecil dan menggabungkan pekerjaan tersebut ke trunk setidaknya sekali (dan mungkin beberapa kali) sehari. Perbedaan kunci antara pendekatan ini adalah cakupan. Cabang fitur biasanya melibatkan beberapa pengembang dan membutuhkan hari atau bahkan minggu kerja. Sebaliknya, cabang dalam pengembangan berbasis trunk biasanya tidak bertahan lebih dari beberapa jam, dengan banyak pengembang menggabungkan perubahan individu mereka ke trunk dengan sering.

Salah satu manfaat utama dari pendekatan berbasis trunk adalah bahwa itu mengurangi kompleksitas acara penggabungan dan menjaga kode tetap terkini dengan memiliki sedikit jalur pengembangan dan melakukan penggabungan kecil dan sering.

Referensi:
- [Trunk-based Development | Atlassian.](https://www.atlassian.com/continuous-delivery/continuous-integration/)
- [DevOps tech: Trunk-based development - Google Cloud.](https://cloud.google.com/architecture/devops/)
- [Trunk-Based Development – Glossary – Split](https://www.split.io/glossary/trunk-based-development/)
- [What is trunk-based development? - Optimizely](https://www.optimizely.com/optimization-glossary/trunk-based-development/)

## Kelebihan dan Kekurangan masing-masing Strategi

Berikut adalah tabel yang merangkum kelebihan dan kekurangan dari GitFlow dan Trunk Based Development:

| Strategi | Kelebihan | Kekurangan |
| --- | --- | --- |
| **GitFlow** | - Memudahkan dalam proses Pararell Development.<br>- Fitur branch memudahkan 2 sampai lebih developer untuk berkolaborasi dalam fitur yang sama.<br>- Memiliki branch hotfix, branch yang dibuat dari branch master. | - Tidak berfungsi dengan baik dengan versi multi-produksi.<br>- Prosesnya sulit untuk ditangani dalam model penerapan yang berkelanjutan (atau hampir berkelanjutan). |
| **Trunk Based Development** | - Semua code changes dibuat langsung ke trunk dan langsung tersedia untuk semua developer.<br>- Memungkinkan perubahan kode yang lebih sering dan lebih kecil.<br>- Memudahkan melihat dan melacak perubahan, dan dapat meningkatkan kolaborasi antar anggota tim. | - Memerlukan proses pengujian yang kuat.<br>- Dengan semua developer bekerja pada basis kode yang sama, bisa menjadi tantangan untuk meninjau semua perubahan.<br>- Dengan semua developer bekerja pada basis kode yang sama, konflik lebih mungkin terjadi. |

Referensi:
- [Apa pro dan kontra dari git-flow vs github-flow?](https://qastack.id/programming/18188492/what-are-the-pros-and-cons-of-git-flow-vs-github-flow)
- [Keuntungan dan Cara Kerja Git Flow](https://medium.com/pdb-r/keuntungan-dan-cara-kerja-git-flow-63ab526e5385)
- [GIT dan GITFLOW](https://medium.com/@dicky.dwi.r/git-dan-git-flow-6b1f79c4c26c)
- [Konsep dasar git dan gitflow](https://medium.com/@antoeldi/konsep-dasar-git-dan-gitflow-71e33cea6a5f)
- [Trunk-based Development: Pros, Cons and Why You Should Consider Adopting It](https://medium.com/@sabri.mutlucag/trunk-based-development-pros-cons-and-why-you-should-consider-adopting-it-81cd7c24626c)


## Kapan Cocok Dipakai

### GitFlow
GitFlow cocok digunakan untuk proyek yang memiliki siklus rilis yang terjadwal. Adanya Feature Branch Workflow memberikan peran yang sangat spesifik untuk cabang yang berbeda dan menentukan bagaimana dan kapan mereka harus berinteraksi. GitFlow bekerja dengan baik untuk produk dalam model rilis yang lebih tradisional, di mana rilis dilakukan setiap beberapa minggu sekali. Namun, proses ini rusak secara signifikan saat Anda merilisnya sekali sehari atau lebih.

### Trunk Based Development
Trunk Based Development adalah pendekatan pengembangan perangkat lunak di mana pengembang sering mengintegrasikan perubahan kode mereka ke cabang utama. Pendekatan ini cocok untuk tim yang menerapkan prinsip integrasi terus-menerus dan penyebaran terus-menerus. Dengan Trunk Based Development, pengembang dapat dengan mudah mengintegrasikan kode mereka dengan cabang utama. Ketika mereka menyelesaikan pekerjaan baru, mereka menggabungkan perubahan ke cabang utama. Namun, mereka tidak seharusnya menggabungkan ke cabang utama sampai mereka telah menyelesaikan build yang berhasil.

Referensi:
- [Apa pro dan kontra dari git-flow vs github-flow?](https://qastack.id/programming/18188492/what-are-the-pros-and-cons-of-git-flow-vs-github-flow)
- [Gitflow Workflow. Gitflow Workflow adalah sebuah fitur](https://medium.com/@rizael.ichigo28/gitflow-workflow-463645732a29)
- [A guide to trunk-based development](https://blog.logrocket.com/product-management/a-guide-to-trunk-based-development/)
- [What is Trunk Based Development?](https://www.gitkraken.com/blog/trunk-based-development)
- [Transitioning to Trunk Based Development](https://devcycle.com/solutions/trunk-based-development)
