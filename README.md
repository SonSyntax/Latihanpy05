<P>NAMA : MOHAMAD SONY HIDAYATULLAH</P>
<p>NIM : 312410290</p>
<P>KELAS : TI 24 A 4</P>
<p>MATKUL : BAHASA PEMROGRAMAN</p>

# Praktikum 4
## List dan tuple
List dan tuple adalah tipe data dalam Python yang berfungsi untuk menampung sekumpulan data.

## Element List
```Python
list = [34, 56, 76, 38, 10] 

# Akses List
list = [34, 56, 76, 38, 10] 
print(list [2]) 
print(list [1:4]) 
print(list [-1])

# Ubah element list
list = [34, 56, 76, 38, 10]
list [3] = 80 
print(list)
list [3] = list [-1] 
print(list)

#Tambah element list
list = [34, 56, 76, 38, 10]

list_a = [34, 56, 76]
list_b = [38, 10]
list_b.append("monster")
print(list_b)
list_b.extend([1, 37, 9])
print(list_b)
list_a.extend(list_b)
print(list_a)
````
![image](https://github.com/user-attachments/assets/0fcf6e8e-07a7-4597-86df-ab78546eaf9a)

```Python
list = [34, 56, 76, 38, 10] 
````

Buat sebuah list sebanyak 5 elemen dengan nilai bebas

## Akses Element

```Python
print(list [2])  # tampilkan elemen ke 3
````

menampilkan elemen ke 3

```Python
print(list [1:4]) # ambil nilai elemen ke 2 sampai elemen ke 4
````

ambil nilai elemen ke 2 sampai elemen ke 4

```Python
print(list [-1]) # ambil elemen terakhir
````

 ambil elemen terakhir

## Ubah Element List

```Python
list [3] = 80 # ubah elemen ke 4 dengan nilai lainnya
print(list)
````

ubah elemen ke 4 dengan nilai lainnya

```Python
list [3] = list [-1] # ubah elemen ke 4 sampai dengan elemen terakhir
print(list)
````

ubah elemen ke 4 sampai dengan elemen terakhir

## Tambah element list

```Python
list_a = [34, 56, 76]
list_b = [38, 10] #ambil 2 bagian dari list pertama (A) dan jadikan list ke 2 (B)
````

ambil 2 bagian dari list pertama (A) dan jadikan list ke 2 (B)

```Python
list_b.append("monster")
print(list_b) #tambah list B dengan nilai string
````

tambah list B dengan nilai string

```Python
list_b.extend([1, 37, 9])
print(list_b) #tambah list B dengan 3 nilai
````

tambah list B dengan 3 nilai

```Python
list_a.extend(list_b)
print(list_a) #gabungkan list B dengan list A
````
gabungkan list B dengan list A

## Pembuatan List
```Python
def hitung_nilai_akhir(nilai_tugas, nilai_uts, nilai_uas):
    return (nilai_tugas * 0.3) + (nilai_uts * 0.35) + (nilai_uas * 0.35)

def tambah_data():
    data_mahasiswa = []
    while True:
        nama = input("Nama : ")
        nim = input("NIM : ")
        nilai_tugas = float(input("Nilai Tugas : "))
        nilai_uts = float(input("Nilai UTS : "))
        nilai_uas = float(input("Nilai UAS : "))
        nilai_akhir = hitung_nilai_akhir(nilai_tugas, nilai_uts, nilai_uas)
        
        data_mahasiswa.append({
            "nama": nama,
            "nim": nim,
            "nilai_tugas": nilai_tugas,
            "nilai_uts": nilai_uts,
            "nilai_uas": nilai_uas,
            "nilai_akhir": nilai_akhir
        })
        
        tambah_lagi = input("Tambah data(y/t)?")
        if tambah_lagi.lower() != 'y':
            break
        
    if tambah_lagi.lower() == 't':
        return data_mahasiswa
    else:
        print("perintah tidak valid, program dihentikan")
        exit()

def tampilkan_data(data_mahasiswa):
        print("\n==================================================================================")
        print("| No | Nama                           | NIM       | Tugas | UTS   | UAS   | Akhir |")
        print("|====|================================|===========|=======|=======|=======|=======|")
        for i, mahasiswa in enumerate(data_mahasiswa, start=1):
            print(f"| {i:<2} | {mahasiswa['nama']:<30} | {mahasiswa['nim']:<9} | {mahasiswa['nilai_tugas']:<5} | {mahasiswa['nilai_uts']:<5} | {mahasiswa['nilai_uas']:<5} | {mahasiswa['nilai_akhir']:<5.2f} |")
        print("==================================================================================")
def main():
    data_mahasiswa = tambah_data()
    tampilkan_data(data_mahasiswa)

if __name__ == "__main__":
    main()
````
Program ini diperuntukan untuk mengumpulkan list, berupa data str, maupun int, dengan ketentuan yang ada

```Python
def hitung_nilai_akhir(nilai_tugas, nilai_uts, nilai_uas):
    return (nilai_tugas * 0.3) + (nilai_uts * 0.35) + (nilai_uas * 0.35)
````

menaruh fungsi `hitung_nilai_akhir` di dalam def, dengan para meter (nilai tugas, niai uts, nilai uas), yang akan ber proses (Nilai tugas di kalikan 30%) di tambah (nilai uts dikalikan 35%) ditambah (nilai uas dikalikan 35%)

```Python
def tambah_data():
    data_mahasiswa = []
````

menaruh fungsi `tambah_data()` di dalam def, yang berproses ke fungsi `data_mahasiswa = []` yang artinya list kosong,

```Python
while True:
        nama = input("Nama : ")
        nim = input("NIM : ")
        nilai_tugas = float(input("Nilai Tugas : "))
        nilai_uts = float(input("Nilai UTS : "))
        nilai_uas = float(input("Nilai UAS : "))
        nilai_akhir = hitung_nilai_akhir(nilai_tugas, nilai_uts, nilai_uas)
````

Masih di dalam fungsi `tambah_data()`, yang berproses ke fungsi `while` yang mengoperasikan perulangan ke fungsi `input()`, dan akan berproses ke variable (nilai_akhir)

```Python
data_mahasiswa.append({
            "nama": nama,
            "nim": nim,
            "nilai_tugas": nilai_tugas,
            "nilai_uts": nilai_uts,
            "nilai_uas": nilai_uas,
            "nilai_akhir": nilai_akhir
        })
````
masih di fungsi `tambah_data()` fungsi `append()` ini menambahkan list ke fungsi `data_mahasiswa = []` yaitu list kosong

```Python
 tambah_lagi = input("Tambah data(y/t)?")
        if tambah_lagi.lower() != 'y':
            break
        
    if tambah_lagi.lower() == 't':
        return data_mahasiswa
    else:
        print("perintah tidak valid, program dihentikan")
        exit()
````
desision ini masih berada di fungsi `tambah_data()` yang mengoperasikan pernyataan (y/t) jika y akan berproses ke fungsi `break` yang artinya berhenti, dan melakukan perulangan ke while true, jika t akan berproses ke fungsi selanjutnya dengan parameter yaitu `data_mahasiswa`, jika tidak sesuai dengan ada di perintah maka pogram di hentikan.

```Python
def tampilkan_data(data_mahasiswa):
        print("\n==================================================================================")
        print("| No | Nama                           | NIM       | Tugas | UTS   | UAS   | Akhir |")
        print("|====|================================|===========|=======|=======|=======|=======|")
        for i, mahasiswa in enumerate(data_mahasiswa, start=1):
            print(f"| {i:<2} | {mahasiswa['nama']:<30} | {mahasiswa['nim']:<9} | {mahasiswa['nilai_tugas']:<5} | {mahasiswa['nilai_uts']:<5} | {mahasiswa['nilai_uas']:<5} | {mahasiswa['nilai_akhir']:<5.2f} |")
        print("==================================================================================")
````

Menarung fungsi `tampilkan_data()` ke dalam def, dengan parameter (data_mahasiswa), yang akan berproses mencetak suatu design list, dan perulangan `for` yang berisi data_mahasiswa yang berada di fungsi `data_mahasiswa = []` list kosong.

```Python
def main():
    data_mahasiswa = tambah_data()
    tampilkan_data(data_mahasiswa)
````
menaruh fungsi `Main()` kedalam def guna mengaktifkan fungsi" def diatas, dengan proses yang ditentukan

<p>berikut hasil program tersebut</p>

![hasil soal2](https://github.com/user-attachments/assets/5ac03298-3ca9-4b6a-af7d-2d5b9bc6494f)

<p>Eksekusi program tersebut</p>

![eksekusi 2](https://github.com/user-attachments/assets/7bb6caef-1293-48da-9b7d-5939e55c0adc)

<p>dan berikut Flowchartnya</p>

![flochart list](https://github.com/user-attachments/assets/19cb9c77-f6e8-427f-bbd7-87d9d0ef6b6f)










