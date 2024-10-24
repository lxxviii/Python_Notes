## Dosya İşlemleri
Python'da dosya işlemleri için özel komutları bulunur.

### open()
Dosya oluşturmak ve açmak için open() fonksiyonu kullanılır.
Kullanımı : open(dosya_adi, dosya_erisme_modu)
dosya_erisme_modu => dosyayı hangi amaçla açtığımızı belirtir.

'w' (Write) yazma modu. Dosyayı konumda oluşturur. 
            Son yapılan ekleme önceki datayı silerek, sıfırdan dosyaya yazar.

```
file = open("C:/users/sadikturan/desktop/newfile.txt","w")      # Yazma İşlemini Yapar
file.close()                                                    # Boşuna kaynak tüketmemek adına dosya kapatılır

file = open ("newfile.txt","w",encoding='utf-8')
file.write("Test text")
file.close()
```

'a' (Append) ekleme. Dosya konumda yoksa oluşturur.
            Daha önceden eklenen dataya ekleme yapar.

'r' (Read) okuma. Varsayılan. Dosya konumda yoksa hata verir.

'x' (Create) oluşturma. Dosya zaten varsa hata verir.