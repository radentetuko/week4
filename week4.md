# Materi Week 4

## 1. JavaSripct Intermediate - Asynchronous

- ### Perbedaan Synchronous dan asynchronous

  Synchronous adalah yang paling umum dan mudah di mengerti. Setiap perintah di eksekusi satu persatu sesuai urutan kode yang kita tuliskan. Sedangkan Asynchronous hasil eksekusi atau output tidak selalu berdasarkan urutan kode, tetapi berdasarkan waktu proses. Eksekusi dengan asynchronous tidak akan membloking atau menunggu suatu perintah sampai selesai. Daripada menunggu, asynchronous akan mengeksekusi perintah selanjutnya.

- ### JavaSripct Intermediate - Asynchronous - Async/Await

  Async/await adalah fitur yang hadir sejak ES2017. Fitur ini mempermudah kita dalam menangani proses asynchronous.Async/Await merupakan sebuah syntax khusus yang digunakan untuk menangani Promise agar penulisan code lebih efisien dan rapih.
  Async/Await terbagi menjadi Async dan Await, mari kita lihat contohnya.

  ```javascript
  const getAllUser = async () => {
    const data = await getUser();
    console.log(data);
  };
  ```

  Pada contoh diatas, pertama kita memiliki function dengan menambahkan async didepan function yang mana berfungsi untuk menjadikan function tersebut asynchronous, dan await berfungsi menunda eksekusi hingga proses asynchronous selesai, dari kode di atas berarti console.log(data) tidak akan di eksekusi sebelum proses getUser() selesai. await juga bisa digunakan berkali-kali di dalam function.

- ### Error Handling Async/Await

  Untuk menghandle error Async/Await kita dapat menggunakan try catch di dalam function yang kita buat, sehingga jika terjadi error kita dapat menangkap errornya dalam block catch, berikut contoh penggunaannya.

  ```javascript
  const getAllUser = async () => {
    try {
      const result = await getUser();
      console.log(result);
    } catch (error) {
      console.log(error);
    }
  };
  ```

- ### JavaSripct Intermediate - Asynchronous - Fetch

  Fetch API pada javascript adalah kegiatan untuk meminta/request layanan ke endpoint/letak url yang akan menerima request pada website secara local maupun public, untuk mengambil response resource / sumber daya berupa data berformat json atau text yang biasa dilakukan programmer untuk membangun website yang membutuhkan data dari website lain ataupun website yang membutuhkan konsep microservice didalamnya.

- ### Fetch dengan Promise

  Berikut ini contoh request data dengan fetch() menggunakan promise:

  ```javascript
  fetch("https://jsonplaceholder.typicode.com/posts")
    .then(function (response) {
      return response.json();
    })
    .then(function (post) {
      console.log(post);
    });
  ```

- ### Fetch dengan async/await

  Berikut contoh request data dengan fetch() menggunakan async/await:

  ```javascript
  const tesFetchAsync = async () => {
    let response = await fetch("https://jsonplaceholder.typicode.com/posts");
    response = await response.json();
    console.log(response);
  };
  tesFetchAsync();
  ```

## 2. Git & GitHub Lanjutan

- ### Cara membuat branch
  Perintah untuk membuat cabang adalah git branch, kemudian diikuti dengan nama cabangnya.
  ```Bash
  git branch halaman_login
  ```
- ### Cara pindah branch
  Coba kita pindah ke cabang yang baru saja kita buat dengan perintah:
  ```Bash
  git checkout halaman_login
  ```
- ### Cara menambahkan file
  Cara Menambahkan file kita bisa menggunakan git add.
  ```Bash
  git add login.html
  ```
- ### Cara meng-commit
  Cara Meng-commit file yang sudah kita tambahkan.
  ```Bash
  git commit -m "membuat file login.html"
  ```
- ### Cara menggabungkan cabang
  Cara Menggabungkan cabang kita bisa menggunakan git merge.
  ```Bash
  git merge halaman_login
  ```
- ### Cara menggabungkan cabang
  Cara Menggabungkan cabang kita bisa menggunakan git merge.
  ```Bash
  git merge halaman_login
  ```
- ### Cara menghapus cabang
  Cara menghapus cabang kita bisa menggunakan git branch -d.
  ```Bash
  git branch -d halaman_login
  ```

## 3. Responsive Web Design

- ### Apa itu Responsive Web Design?
  Responsive web design atau desain web responsif adalah sebuah teknik atau metode bagi web designer untuk membuat suatu layout website yang dapat menyesuaikan diri sesuai dengan ukuran layar pengguna.
- ### Prinsip responsive web design

  Untuk memiliki desain web yang responsif, maka pastikan bahwa website-mu memiliki prinsip-prinsip berikut:

  - #### Fluid Grid

    Maksud dari fluid grid adalah sebuah grid atau garis-garis batas yang menentukan letak suatu komponen dalam desain, namun dapat berubah-ubah sesuai dengan ukuran tampilannya.

    Hal ini karena satuan yang digunakan adalah satuan yang relatif seperti persen, atau em (satuan dipakai dalam tipografi).

  - #### Media Queries

    Adanya media query memungkinkan desainmu lebih sesuai dengan berbagai ukuran layar.

    Media query memungkinkan website untuk dapat mengambil data mengenai ukuran layar yang digunakan untuk menampilkan konten.

  - #### Responsive Media

    Prinsip selanjutnya yang harus diperhatikan dalam membuat responsive web design adalah media yang responsif.

    Seperti pada poin pertama, yaitu kamu harus memastikan bahwa media seperti foto dan video dapat ditampilkan dengan baik di berbagai ukuran layar.

    Oleh karenanya, dibandingkan dengan menggunakan ukuran tampilan berupa pixel, maka pastikan ukuran dari media yang ditampilkan dalam bentuk persentase.

    Sangat disarankan untuk memberikan pengukuran dari media sebesar 100%, agar media yang ditampilkan dalam tampilan yang maksimal.

- ### Keuntungan
  - #### Dapat diakses oleh berbagai device dengan ukuran layar berbeda-beda
  - #### Lebih hemat biaya
  - #### Kemudahan dalam maintenance
  - #### Halaman yang lebih cepat dibuka
