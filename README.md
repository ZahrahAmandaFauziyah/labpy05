# labpy05

Latihan 1
Soal

Buat Dictionary daftar kontak ( Nama sebagai key, dan nomor sebagai value )
Tampilkan kontaknya Ari
Tambah kontak baru dengan nama Riko, nomor 087654544
Ubah kontak Dina dengan nomor baru 088999776
Tampilkan semua Nama
Tampilkan semua Nomor
Tampilkan daftar Nama dan nomornya
Hapus kontak Dina.

Kode Python

    # 1. Buat Dictionary daftar kontak
    daftar_kontak = {
    "Arza": "085678799450",
    "Duta": "082462094567",
    "Ara" : "086390215444"
    }

    # 2. Tampilkan kontaknya Arza
    print("Kontak Arza:", daftar_kontak.get("Arza"))

    # 3. Tambah kontak baru dengan nama Duta, nomor 082462094567
    daftar_kontak["Duta"] = "082462094567"
    print("Kontak Duta telah ditambahkan.")

    # 4. Ubah kontak Ara dengan nomor baru 086390215444
    daftar_kontak["Ara"] = "086390215444"
    print("Kontak Ara telah diubah.")

    # 5. Tampilkan semua Nama
    print("Semua Nama:", list(daftar_kontak.keys()))

    # 6. Tampilkan semua Nomor
    print("Semua Nomor:", list(daftar_kontak.values()))

    # 7. Tampilkan daftar Nama dan nomornya
    print("Daftar Nama dan Nomornya:")
    for nama, nomor in daftar_kontak.items():
    print(f"{nama}: {nomor}")

    # 8. Hapus kontak Ara
    if "Dina" in daftar_kontak:
    del daftar_kontak["Ara"]
    print("Kontak Ara telah dihapus.")
    else:
    print("Kontak Ara tidak ditemukan.")

![Cuplikan layar 2024-11-21 111659](https://github.com/user-attachments/assets/757a5f7c-185f-4aa8-bb17-6434860527ae)
![Cuplikan layar 2024-11-21 111711](https://github.com/user-attachments/assets/5cd79186-0dc9-430f-8c84-0c495324253d)

Penjelasan : 

1. Membuat Dictionary Daftar Kontak ( Di sini, sebuah dictionary bernama daftar_kontak dibuat. Kunci (key) dari dictionary ini adalah nama-nama kontak (Arza, Duta, Ara), dan nilainya (value) adalah nomor telepon yang sesuai. )
2. Menampilkan Kontak Arza ( Menggunakan metode get(), kode ini menampilkan nomor telepon yang terdaftar untuk kontak "Arza". Jika "Arza" tidak ada dalam dictionary, get() akan mengembalikan None tanpa menghasilkan error. )
3. Menambahkan Kontak Baru ( Di sini, kontak baru dengan nama "Duta" dan nomor "082462094567" ditambahkan ke dalam dictionary. Jika nama tersebut sudah ada, nilainya akan diperbarui. )  Secara keseluruhan, kode ini menunjukkan bagaimana cara membuat, mengubah, menampilkan, dan menghapus data dalam sebuah dictionary yang digunakan untuk menyimpan daftar kontak.
4. Mengubah Kontak Ara ( Kontak "Ara" diubah dengan nomor baru "086390215444". Jika "Ara" tidak ada, maka kontak baru akan ditambahkan. )
5. Menampilkan Semua Nama (digunakan untuk mendapatkan semua kunci (nama) dari dictionary, yang kemudian diubah menjadi list untuk ditampilkan)
6. Menampilkan Semua Nomor (digunakan untuk mendapatkan semua nilai (nomor telepon) dari dictionary, yang juga diubah menjadi list untuk ditampilkan.)
7. Menampilkan Daftar Nama dan Nomornya (digunakan untuk mendapatkan pasangan kunci-nilai dari dictionary. Dalam loop, setiap nama dan nomor ditampilkan dalam format yang rapi.) 8.Menghapus Kontak Ara


   Praktikum 5
   
Buat program sederhana yang akan menampilkan daftar nilai mahasiswa, dengan ketentuan : 
1. Program dibuat dengan menggunakan Dictionary
2. Tampilkan menu pilihan: (Tambah Data, Ubah Data, Hapus Data, Tampilkan Data, Cari Data)
3. Nilai Akhir diambil dari perhitungan 3 komponen nilai (tugas: 30%, uts: 35%, uas: 35%)
4. Buat flowchart dan penjelasan programnya

   Kode Python

       # Pastikan dictionary mahasiswa sudah didefinisikan
        mahasiswa = {}

        def tambah_data():
        print("\n=== TAMBAH DATA MAHASISWA ===")
        nama = input("Masukkan Nama: ")
    
        if nama in mahasiswa:  # Cek apakah nama sudah ada
        print("Data mahasiswa sudah ada!")
        return
    
        try:
        # Input nilai
        tugas = float(input("Nilai Tugas (0-100): "))
        uts = float(input("Nilai UTS (0-100): "))
        uas = float(input("Nilai UAS (0-100): "))
        
        # Validasi rentang nilai
        if not (0 <= tugas <= 100 and 0 <= uts <= 100 and 0 <= uas <= 100):
            print("Nilai harus berada dalam rentang 0-100!")
            return
        
        # Hitung nilai akhir
        nilai_akhir = (tugas * 0.3) + (uts * 0.35) + (uas * 0.35)
        
        # Simpan ke dictionary
        mahasiswa[nama] = {
            "tugas": tugas,
            "uts": uts,
            "uas": uas,
            "nilai_akhir": nilai_akhir
        }
        print("Data berhasil ditambahkan!")
    
        except ValueError:
        print("Input tidak valid! Pastikan untuk memasukkan angka.")

        # Contoh pemanggilan fungsi
        tambah_data()

![Cuplikan layar 2024-11-21 112747](https://github.com/user-attachments/assets/764198a7-5add-4b26-a623-9c5355664644)
![Cuplikan layar 2024-11-21 112800](https://github.com/user-attachments/assets/2df20d3b-7d6e-45dd-964b-a6d4e02e7bc5)
![flowchart pemrograman](https://github.com/user-attachments/assets/a5fa97d8-ffff-45cc-8001-aab0a2ddb8c6)




