> Pada tutorial ini kita belum akan membahas tentang fitur di es6 / es2015

# Fungsi (Function)

Pada javascript fungsi adalah hal yang aneh dan agak sulit untuk dimengerti, khususnya bagi pemula yang baru berkenalan dengan javascript. Karna fungsi di javascript juga turunan dari Object (dan *context* jika kita bicara object) juga [scope](Scope.md). 

Tapi tenang, disini saya akan mencoba menjelaskan dengan bahasa yang mudah dipahami (setidaknya menurut saya, haha :smile: ) dan perlahan - lahan (asal selamat).

Mungkin bagi anda yang sudah mengenal fungsi di javascript secara baik, malah akan menganggap bahwa ini adalah hal yang indah dan elegan. Dimana fungsi bisa disimpan di dalam variabel, dipanggil dari dalam fungsi lain, dikirim sebagai argumen pada fungsi lainnya, dll.
Bahkan dalam perkembangannya banyak orang menggunakan javascript lebih condong ke arah konsep functional programming.

*Fungsi* secara umum digunakan agar kode yang ditulis bisa digunakan berulang kali, tanpa membuat kode tersebut berulang - ulang (code reuse).
*Ingat dibuat cukup sekali namun bisa digunakan berkali - kali, bukannya setiap kali dibutuhkan 

> Fungsi adalah turunan dari *Function.prototype* dan *Function.prototype* adalah turunan dari *Object.prototype*. Jadi fungsi juga merupakan turunan dari Object.

Langsung aja yah kita coba untuk mulai membahas fungsi secara teknis.

## Pembuatan fungsi pada javascript.

```javascript
function penjumlahan(x, y) {
	return x + y
}
penjumlahan(5, 5);
```

Pada contoh di atas adalah contoh dari pembuatan fungsi, dimana dari contoh diatas terdapat 2 bagian :

- Deklarasi fungsi
```javascript
function penjumlahan(x, y) {
	return x + y
}
```
- Pemanggilan fungsi
```javascript
penjumlahan(5, 5);
```

### Function expression
Selain pembuatan fungsi dengan cara diatas, fungsi juga bisa dibuat dengan function expression. Yaitu pembuatan sebuah fungsi tanpa nama (anonymous function) yang dimasukkan kedalam sebuah variabel.  
Contoh : 
```javascript
var penjumlahan = function(x, y) {
	return x + y;
}
penjumlahan(5,5); //outputnya 10
```

## Constructor Functions