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




