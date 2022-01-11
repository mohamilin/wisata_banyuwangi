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
      7. fd
      8. f
      9. fd
      10. fd