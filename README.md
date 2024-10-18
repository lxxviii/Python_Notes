
### VALUES
```x=10  x // 3         # 3 Değerini alacaktır```

### IDENTITY OPERATOR (IS)
Referans Değerlerde == Value'ye bakar. === kontrolü için Identity Operatörü olan 'is' Kullanılır.
```
x = y = [ 1 , 2 , 3 ]
    z= [ 1, 2, 3 ]
print ( x == y )  # True
print ( x == z )  # True
print ( x is y )  # True    'is not' da kullanılabilir
print ( x is z )  # False   'is not' da kullanılabilir
```
### MEMBERSHIP OPERATOR (IN)

array = ['test1', 'test2']
for ( arr in array):        # True  or 'not in'

string = 'Test'
for ( s not in string):     # True  or 'not in'

### TUPLES
``` 
values = (1,2,3,4,5) veya values = 1,2,3,4,5  print(values) print(type(values))
```
Tuple formatında Destruct işlemi yapılabilir. JS de [...] olarak tanımlanmış alanda, * kullanılarak, işlem gerçekleştirilir.
```
Örnek olarak : values = 1,2,3,4,5  x, y, *z = values  print(x,y,z)
```

### STRING
```
message = "lor LOR Lor lOR"
```

```
resultMessage = message.upper()               #  UPPERCASE  
resultMessage = message.lower()               #  lowercase
resultMessage = message.title()               #  Title (Sadece Başharfini büyük karakter yapar)
resultMessage = message.capitalize()          #  Capitalize
```

```
resultMessage = message.strip()               # Space Remover Trimming lstrip and rstrip
resultMessage = message.split()               # ['Lor', 'lor', 'lor', 'lor']
resultMessage = '      '.join(message)        # Lor      lor      lor      lor
resultMessage = message.find('arananText')    # find bulunan ilk harfin index numarasını geri döndürür, yoksa -1 döndürür
```

```
resultMessage  = message.count('o')            # count(result = number) Not in 0  
resultMessage  = message.count('o',0,10)       # count(result = number) Not in 0
```

```
resultMessage  = message.find('o')              # count(result = number) included in 0
resultMessage  = message.find('o',0,10)         # count(result = number) included in 0
resultMessage  = message.rfind('o',0,10)        # count(result = number) included in 0
```

```
resultMessage  = message.index('o')             # count(result = number) included in 0
resultMessage  = message.index('o',0,10)        # count(result = number) included in 0
resultMessage  = message.rindex('o',0,10)       # count(result = number) included in 0  '''  not found find == -1 => not found index == throw error '''
```

```
resultMessage = message.startswith('abc')      # boolean check first Chacter  resultMessage = message.endswith('abc')         # boolean check last Chacter
```

```
resultMessage = message.isalpha()               # boolean Alfabetic check
resultMessage = 'Hello'.isalpha()               # true
resultMessage = message.isdigit()               # boolean Digit check
resultMessage = '123'.isdigit()                 # true
```

```
resultMessage = 'Contents'.center(50, '*')      # Contents ifadesini satırda 50 kararkter ortasına yerleştirip ortasına * ekler  
resultMessage = 'Contents'.ljust(50, '*')       # Contents ifadesini satırda 50 kararkter başına yerleştirip sağına * ekler
resultMessage = 'Contents'.rjust(50, '*')       # Contents ifadesini satırda 50 kararkter sonuna yerleştirip soluna * eklemek
```

```
resultMessage = message.replace(' ', '-')       # Boşluk kararkterini kaldırıp yerine - kararkteri atar  resultMessage = message.replace(' ', '-', 5)
```

### ARRAYS         
 **len(arrayName)**
```arrayName[0-len(arrayName) or -1]    SET arrayName[setArrayNameIndex or -1 => lastNumber] = 'Setlenecek Array Value'Return boolean = 'Searhing Array Value' in arrayName => Return True / FalseArrayName [ Starting Array Index Value : Ending Array Index Value ]```

**Silmek için del kullanılabilir**
```
del ArrayName[SilmekIstenilenArrayDegeriIndexi]
```
**Ecma Script'teki ``, (f'') komutu ile karşılanır**
```
String Value = f('')
```
**(includes) Dizi İçinde Aranan Eleman Var mı?**
'ArananDiziDeğeri' in arrayName => return true/false

**Fonksiyonlar**
min(), max(), number.sort(), letter.sort(), 
reverse(*Listeyi Tersine Çevir*),

len() **length**, arrayName.count('Aranacak Nitelik') **Dizi içinde Kaç tane Aranacak Nitelik var**

insert(Add Index, Add Value) *Add Index Character*, append(Add Value) *Sonuna Ekler*, 
pop(Delete Index) *Belirtilen İndex Noktasını Siler*, remove(Delete Value) *Seçilen Değeri Siler*, clear() *Tüm Diziyi Siler*,

### TUPLE
Dizi yapılarının [] paranteze alınmamış halidir. Genelde Paranteze alınır ancak alınması zorunlu değildir.
```
tuple = 1, 'iki, 3
```
*Atama İşlemi Yapıldıktan Sonra Değerler Değiştirilemez ancak yeni bir Tuple ataması yapılabilir*
*Tuple'dan Array'e atama yapılabilir*
*Index ve Count Dışında Herhangi Bir Fonksiyon Çalışmayacaktır*

### DICTIONARY
**KEY - VALUE** yapısı ile setlenir
```
dictionary = { 'k1':1, 'k2':2, 'k3':3 }
for key, value in dictionary.items():
```