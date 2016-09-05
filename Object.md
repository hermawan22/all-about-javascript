> Pada tutorial ini kita belum akan membahas tentang fitur di es6 / es2015

# Object

Apa yang anda bayangkan pertama kali jika mendengar kata Object?
Jika anda pernah berkutat dengan bahasa pemorgraman yang kental dengan konsep Object Oriented Programming (OOP), seperti Java, C#, atau bahkan PHP. Saya dapat menebak bahwa anda berfikir bahwa Object di javascript juga sama, yaitu *blueprint* dari sebuah class.  
Di javascript *Object* bukan merupakan class based melainkan prototype based, yang berarti tidak memerlukan sebuah class dan menginisialisasinya atau dengan constructor untuk mendapatkan sebuah Object.

- contoh di pemrograman yang berkonsep OOP :
```php
// deklarasi kelas
public class Hewan {
    public int $jumlahKaki;
    // properti lain
}

// penggunaan kelas
var singa = new Hewan();

// gunakan kelas...
singa.jumlahKaki = 4;
```

- contoh di javascript :
```javascript
var Hewan = {
	jumlahKaki : 4,
	//properti lain
}
```

### Penulisan properti dan pengaksesan nilai properti di object
#### Penulisan properti
Untuk cara penulisan properti di object terdapat dua jenis penulisan, yaitu legal dan ilegal (nah, lo ilegal :smile:).

- Contoh penulisan properti ilegal :
```javascript
var Hewan = {
	jumlah-kaki : 4
}
```
Di javascript tanda "-" dan spasi, merupakan ilegal dalam penulisan properti. Maka jika anda paksakan seperti itu akan error.  
Cara agar tidak error adalah dengan menggunakan tanda kutip ("") pada properti yang cara penulisannya ilegal, contoh :  
```javascript
var Hewan = {
	'jumlah-kaki' : 4,
	'warna badan' : 'coklat'
}
```

- Untuk penulisan properti yang legal adalah penulisan selain dengan tanda "-" atau spasi, contoh : 
```javascript
var Hewan = {
	jumlahKaki : 4,
	warnabadan : "coklat"
}
```

#### Pengaksesan nilai properti
Selain penulisannya, cara pemanggilan properti ilegal dan legal di object juga berbeda.

- Contoh pengaksesan nilai properti yang ilegal :
```javascript
Hewan.["jumlah-kaki"];
Hewan.["warna badan"];
```  
Jadi harus menggunakan kurung siku [] untuk mengakses nilai dari property yang namanya ilegal.

- Contoh pengaksesan nilai properti yang legal :
```javascript
Hewan.jumlahKaki;
Hewan.jumlahkaki;
```  
Menggunakan tanda titik (.) untuk dapat mengakses nilai dari property yang namanya legal.

