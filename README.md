# wisata_banyuwangi

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://flutter.dev/docs/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://flutter.dev/docs/cookbook)

For help getting started with Flutter, view our
[online documentation](https://flutter.dev/docs), which offers tutorials,
samples, guidance on mobile development, and a full API reference.

### Membuat Mobile App Wisata Banyuwangi
1. Klik ctrl + shift + p -> pilih flutter : New Project  -> Pilih folder kemudian pilih nama aplikasi (saya menggunakan nama aplikasi wisata_banyuwangi).
2. Kemudian akan kita hapus aplikasi counter bawaan dari flutter ketika instal di awal tadi. 
3. Lalu kita akan membuat aplikasi dengan struktur widget seperti ![gambar](https://d17ivq9b7rppb3.cloudfront.net/original/academy/20200615123022ba51f3071b1abe12d3704a7ce5db8b4d.png)
4. Buat class dengan nama DetailScreen menggunakan StatelesWidget dengan return Scaffold()
      1. Gunakan widget Text, untuk menampilkan text
      2. Tampilan masih belum bagus, maka kita bungkus dengan Container(). dengan memberikan margin dan menaruh Text didalam child
         ```dart
         body: Column(
            children: <Widget>[
                Container(
                    margin: EdgeInsets.only(top: 16.0),
                    child: Text('Wisata Banyuwangi'),
                    )
                ],
            ),
        );
        ``` 
      3. untuk memudahkan dalam mengatur margin, bisa menggunakan SafeArea
         ```dart
        body: SafeArea(
            child: Column(
                children: <Widget>[
                Container(
                    margin: EdgeInsets.only(top: 16.0),
                    child: Text('Wisata Banyuwangi',),
                )
                ],
            ),
        );
        ```
      4. Buat tulisan Wisata Banyuwangi di tengah dengan menambahkan parameter textAlign pada widget Text
       ```dart
        body: SafeArea(
            child: Column(
                crossAxisAlignment: CrossAxisAlignment.stretch,
                children: <Widget>[
                Container(
                    margin: EdgeInsets.only(top: 16.0),
                    child: Text(
                    'Wisata Banyuwangi',
                    textAlign: TextAlign.center,
                    style: TextStyle(fontSize: 30, fontWeight: FontWeight.bold),
                    ),
                )
                ],
            ),
        )
       ``` 

      7. Selanjutnya, kita buat informasi terkait tempat wisata. Dengan menyusun widget secara vertikal dan horizontal. Dengan menambahkan child kedua dari column dr sebuah container.
        ```dart
        body: SafeArea(
            child: Column(
                crossAxisAlignment: CrossAxisAlignment.stretch,
                children: <Widget>[
                Container(....),
                Container(
                    margin: EdgeInsets.symmetric(vertical: 16.0),
                    child: Row(
                        children: <Widget>[
                            // kode untuk bikin column
                        ]
                    )
                )
                )
                ],
            ),
        )
       ```  
      8. Kemudian di dalam <Widget>[...] kita buat column utk disusun icon dan text. Kode untuk container yang ke dua
         ```dart
            Container(
            margin: const EdgeInsets.symmetric(vertical: 16.0),
            child: Row(
              mainAxisAlignment: MainAxisAlignment.spaceEvenly,
              children: <Widget>[
                Column(
                  children: const <Widget>[
                    Icon(Icons.calendar_today),
                    SizedBox(height: 8.0),
                    Text('Buka Setiap Hari')
                  ],
                ),
                Column(
                  children: const <Widget>[
                    Icon(Icons.access_alarm),
                    Text('09.00 - 18.00 WIB')
                  ],
                ),
                Column(
                  children: const <Widget>[
                    Icon(Icons.money),
                    Text('Rp 20,000')
                  ],
                )
              ],
            ),
          ),
         ``` 
      9.  Kemudian, kita buat lagi untuk deskrips. Dengan menambahkan Container baru. 
        ```dart
        ...
        Container(
            padding: const EdgeInsets.all(16.0),
            child: const Text(
              'Berada di jalur utama Banyuwangi, Kabupaten Banyuwangi menjadi pilihan tepat sebagai  objek wisata yang tidak pernah sepi pengunjung. Selain karena letaknya strategis, kawasan ini juga menghadirkan nuansa wisata khas Eropa. Semua itu diterapkan dalam bentuk spot swafoto Instagramable.',
              textAlign: TextAlign.justify,
              style: TextStyle(fontSize: 15, fontStyle: FontStyle.normal),
            ),
          )
        ....

        ```
      10. fd
      11. fd