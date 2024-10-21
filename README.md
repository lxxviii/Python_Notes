
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

```
def arrayList = [startingIndex:EndingIndex]
```

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
print(key, value)
```

### range()
```
for item in range(50,100,20)    # (Start Value, Stop Value, Step Value)

list ()                         # Liste Haline Getir
print(list(range(50,100,20)))   # [50,70,90]

Örnek Code :    myString = 'Hello'
                years = [1990, 2000, 2010, 2020]
        numbers = [x for x in range(10) if x%3==0 ]             # [0 9 36 81]
                = [x if x%2 ==0 else 'Tek' for in range(1,4)]   # ['Tek', 2, 'Tek']
                = [(x,y) for x in range(2) for y in range(2)]   # [(0,0),(0,1),(1,0),(1,1)]
        myList = [letter for letter in myString]                # ['H','e','l','l','o']
        ages = [2030 - year for year in years]                  # [40, 30, 20, 10]
```

### enumarate()
```
for index, item in enumatare (gretting):
    print(f'index : {index}, letter : {item}')    # item => greetting[Index]
```

### zip() dikey listelerden yatay listeler oluşturma işlemi için kullanılır
```
for a,b,.... in zip(list1, list2, ......)
    print(a,b .....)
```
### Fonksiyonlar

**random()**
random.randint(startValue, EndValue) => random.randint(1,10)

**sum()**
n sayıda parametrenin (*) toplanması işlenmesi hazır fonksiyonunu yerine getirir.
```
def add(*params):
    print(type(*params))
    return sum((params))
```
n sayıda parametrenin (**) işlenmesi, dictionary yapısını oluşturarak fonksiyonunu sonucunu döndürür.
```
def displayUser(**params):
    print(type(**params))
    return for key, value in params.items()
        print('{} is {} '.format(key, value))
```
Lambda Expressions
```
#Normal Yöntem
def square(num): return num**2
numbers = [1,3,5,9]
result = list(map(square, numbers))
for item in map (square, numbers)
    print(item)
print(result)

#Lambda Yöntemi-1
numbers = [1,3,5,9]
result = list (map (lambda num : num **2, numbers))
print(result)

#Lambda Yöntemi-2
numbers = [1,3,5,9]
square = lambda num : num **2
result = list (map (square, numbers))
print(result)

#Lambda Fonksiyon Olarak Kullanma
result = square(3)
print(result)

#Lambda Fonksiyon Filter Olarak Kullanma
numbers = [1,3,5,9,10,4]
def checkEven(num): return num%2==0
result = list(filter(checkEven, numbers))


#Lambda Gömülü Fonksiyon Oluşturma
def checkEven(num): return num%2 ==0
result = checkEven(numbers[2])
result = list (filter (lambda num : num%2 ==0, numbers))
```

### Fonksiyonlar Kapsama Alanı
``` 
#Global Scope
x = 'Global X'

def function():
    #Local Scope
    x = 'Local X'

function()
print(x) 
```

### Global Etkili Scope Oluşturmak İçin
``` 
x=50
def test()
    global x #bu şekilde x değişkeni global x=50 değişkeninin olduğu value 'ye atanır
    print(f'x : {x}')

    x=100
    print(f'Changed x to {x}')
test()
print(x)
```

### Class Yapıları
```
class Person():
    def __init__(self, fname, lname):
        self.firstName = fname
        self.lastName = lname
        print('Person Created')
    def eat(self):
        print('Person Eat')

class Student(Person):
    def __init__(self, fname, laname):
        Person.__init__(self, fname, lname)    # inherit işlemi için eklene initialize   veya   # super.__init__(fname, laname)
        print('Student Created')

p1 = Person('P1FName','P1LName')
s1 = Student('S1FName','P1LName')
[Self Özelliği için Link](https://www.informit.com/)
```
