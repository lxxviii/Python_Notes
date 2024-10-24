## Dosya İşlemleri
Python'da dosya işlemleri için özel komutları bulunur.

### open()
Dosya oluşturmak ve açmak için open() fonksiyonu kullanılır.
Kullanımı : open(dosya_adi, dosya_erisme_modu)
dosya_erisme_modu => dosyayı hangi amaçla açtığımızı belirtir.

'w' (Write) yazma modu. Dosyayı konumda oluşturur. 
            Son yapılan ekleme önceki datayı silerek, sıfırdan dosyaya yazar.
'a' (Append) ekleme. Dosya konumda yoksa oluşturur.
            Daha önceden eklenen dataya ekleme yapar.

'r' (Read) okuma. Dosya konumda yoksa hata verir.               # Eğer herhangi bir işaret yoksa, varsayılan 'r'  'dir.

'r+'(Update) Dosyayı Açıp içine metin ekleneceğini belirtir.

'x' (Create) oluşturma. Dosya zaten varsa hata verir.

### open().read()
```
file = open("C:/users/sadikturan/desktop/newfile.txt","w")      # Yazma İşlemini Yapar
file.close()                                                    # Boşuna kaynak tüketmemek adına dosya kapatılır

try:
    file = open ("newfile.txt","w",encoding='utf-8')
    print(file) 
    file.write("Test text")
except FileNotFoundError:
   print("dosya okuma hatası")
finally:
    file.close()
    print("dosya kapandı")

    #Result For Döngüsüyle
for i in file:
    print(i, end="")

    # Result read() ile
content = file.read(5)      # 5 Karakter oku
print(content)

file.close()  # Dosya kapatılmadan read işlemi yapılırsa, cursor sona geldiği için yeniden okuma yapmaz. Bu nedenle kapat aç yapılmalıdır.

file.readline() # Her seferinde 1 satır okur
file.readlines() # [] Her Line için  [1Value, 2Value, 3Value, ...] oluşturur.
```
Pratik Kullanım
````
with open ("newFile.txt", "r", encoding="utf-8") as file :
    content = file.read()   # Sentetik dosya adı oluşturur ve close() fonksiyonunu otomatik ekler.
    print(content)
    file.seek(0)            # Cursor'un gideceği index numarası
    print (file(tell()))    # Cursor'un konumunu verir
```

Sayfa Ortasında Güncelleme
````
with open ("newFile.txt, "r+", encoding="utf-8") as file:
    list.file.readline()
    list.insert(1,"EklenecekIsim Soyad\n")
    file.seek(0)
    for i in list:
        file.write(i)

with open("newFile.txt", "r", encoding="utf-8") as file:
    print(file.read())
```

