# ES6+ 

### Apa itu ES6 ?

- ES6 atau ECMASCRIPT 2015 merupakan bagian penting dari Javascript . 
- Hampir semua akar pembelajaran javascript library dan framework asalnya dari ES6 +.

### Apa saja Fitur yang dibawa ES6 ?

•	Arrow Functions
•	Promises
•	Block-Scoped Constructs Let and Const
•	Modules
•	Classes ES6
•	Template Literals
•	Destructuring Assignment
•	Multi-line Strings
•	Enchanced Object Literals

### Apa itu Babel ?

- Babel adalah Javascript Transpilers (Package / Bundle / Webpack) yang menjadi standar industri pada JavaScript.

- Babel membuat kita dapat menulis code ES6 yang kemudian menkonversinya ke pre-ES6 JavaScript sehingga membuat browser support .

### Apa itu Webpack ?

- Webpack adalah opensource JavaScript module Bundler yang akan menyiapkan segala dependencies yang dibutuhkan .

- Webpack mengubah HTML , CSS dan Images menjadi bundler yang akan digunakan pada front-end assets .


### Apa itu Constants ?

- Constants atau const biasanya ditulis dalam JavaScript adalah variable yang tidak dapat diubah .
```
const name =”ABC”
```
- Constants pada ES6 membuat proteksi tersendiri , mengubah nilai , optimisasi performa dan clean code yang di improv daripada JavaScript versi sebelumnya .

### Apa itu Template Literals pada ES6 ?

- Template Literals merupakan string dengan embed code dan variable didalam nya .

- Template Literals membuat struktur code , rangkaian dan penyisipan menjadi lebih efisien untuk dibaca dibandingkan dengan ECMAScript versi sebelumnya.
```
let firstname = “Budi”;
let lastname = “React”;
const fullname = `${firstname} ${lastname}`;
console.log(fullname);
```
hasilnya adalah Budi React.


### Apa itu Rest Operator pada ES6 ?

- Rest Operator adalah sekumpulan element yang berada pada array .
- Rest operator memiliki nama lain yaitu Destructuring Array .
```
let name = [“React”,”Pram”,”Budi”];
const [firstName,...lastName] = name;

console.log(firstName);
console.log(lastName);
```
hasil dari element yang dituju adalah 
```
firstName = React
lastName = [“Pram”,”Budi”]
```

### Apa itu Spread Operator pada ES6 ?

- Spread Operator mengizinkan untuk mengubah dan menambah argumen yang tersedia pada array .
- Spread Operator biasanya digunakan ketika ingin mendapat sebuah hasil lebih dari 1 array yang dibutuhkan .

- Code Syntax Spread Operator mungkin terlihat sama dengan Rest Operator , tetapi nyatanya hal ini berlainan .
```
let arr1 = [1,2,3];
let arr2 = [4,5,6];

const arr = [...arr1,...arr2];
```
hasilnya adalah [1,2,3,4,5,6]

### Apa itu Destructuring Assignment pada ES6 ?

- Destructuring Assignment atau Object Destructuring mengizinkan kita untuk men-ekstrak data dari array dan objects untuk dijadikan Variable secaara terpisah .

- Pada ES6 Destructuring Assignment ini di improvisasi dari versi sebelumnya .
- Berikut adalah perbandingan antara Object Destructuring dengan Array Destructuring
```
// Object Destructuring
const person ={
    firstname: “Budi”,
    lastname: “React”,
    country: “Indonesia”
};

const {firstname, lastname, country } = person;
console.log(firstname, lastname, country);

// hasilnya adalah Budi React Indonesia
```
atau
```
// Array Destructuring

const name = [“Aniket”, “Nagapure”];
const [FirstName , LastName ] = name;
console.log(FirstName , LastName);

// hasilnya adalah Budi, React
```


### Apa itu Set pada ES6 ?

- Set merupakan sebuah Object type yang mengizinkan kita untuk membuat sekumpulan nilai.

- Nilai yang di set dapat berisi strings (“huruf”)  atau integers(angka)

- Object spesifik seperti Object Literals dan Array pun dapat dimasukan menjadi set.

```
let numbers = new Set();
numbers.add(1)
numbers.add (2)
console.log(numbers.size)

// hasilnya adalah 2
```

### Apa itu Let pada ES6 ?

- Let adalah bagian dari deklarasi variable yang membatasi penggunaan blockscope . 
- Sehingga bagian terluar tidak dapat memanggil apa yang ada pada block scope .

Dibawah ini adalah blockscope pada let
```
{
  let x = 2;
}
// x tidak dapat digunakan disini
```
Perbedaan antara var dan let adalah var dapat melakukan scoping secara global .


### Apa itu Arrow Function ?

### Apa itu Generator Function ?

### Apa itu yield pada Generator ?

- Yield pada generator digunakan untuk membuat jeda dan memulai kembali pada generator function.
```
function* foo(index) {
    while (index <2) {
       yield index++;
   }
}

const iterator = foo(0);

console.log(iterator.next().value);
// hasilnya adalah 0

console.log(iterator.next().value);
// hasilnya adalah 1
```

### Apa itu penggunaan reduce() pada ES6 ?

- Metode reduce() mengizinkan untuk melakukan reducer function pada setiap elemen array yang hasil nya dijadikan out dengan nilai tunggal .

Reducer function mempunyai 4 arguments yaitu ;

1.	accumulator (acc)
2.	current value (cur)
3.	current index (idx)
4.	source array (src)
```
const array1 = [1,2,3,4];
const reducer = (accumulator, currentValue) => accumulator + currentValue;

console.log(array1.reduce(reducer));
//hasilnya adalah 10 . Karena 1+2+3+4

console.log(array1.reduce(reducer, 5));
// hasilnya adalah 15. karena 1+2+3+4+5
```

### Apa itu penggunaan map() pada ES6 ?

Map() membuat array baru dengan hasil yang dapat dipanggil pada setiap element array .

```
let numbers = [1,4,9];
let roots = numbers.map(Math.sqrt);

console.log (“root is :”+roots);
//hasilnya adalah roots is : 1,2,3 
```

### Apa itu penggunaan filter() pada ES6 ?

filter() akan menyaring element yang ditentukan yang kemudian membuat array baru melalui implementasi function .
```
const numbers = [1,2,10,15,20];
const result = numbers.filter(number => numbers > 10);

console.log(result);

output => [15,20] 
```

### Apa itu penggunaan find() pada ES6 ?

Find() mencari nilai pada sebuah element yang telah ditentukan .
```
const numbers = [1,2,10,15,20];
const result = numbers.find(number => numbers >10);

console.log(result);

output => [15]
```
### Apa itu penggunaan every() pada ES6 ?

every() adalah metode dimana semua elements di dalam array di seleksi dan di  luluskan / pass yang di implementasikan pada function dan hasilnya adalah Nilai Boolean .

Contoh :
```
const isBelow Threshold =(currentValue) => currentValue < 40;
const array1 = [1,30,39,29,10,13];

console.log(array1.every(isBelowThreshold));

output => true
```

### Apa itu penggunaan some() pada ES6 ?

some() merupakan metode dimana setidaknya satu element di passing melalui function yang akan menjadi Nilai Boolean
```
const array = [1,2,3,4,5]
const even = (element) => element %2 === 0;

console.log(array.some(even));

output => true
```

### Apa itu forEach() method pada ES6 ?

forEach() merupakan metode dimana setiap array element di eksekusi / dijalankan yang akan menjadi Nilai Boolean.
```
const array = [a,b,c];
forEach(element => 
console.log(element))

output => a,b,c
```
### Apa itu Promise ?

- Promise dalam Javascript adalah sebuah object yang akan dipakai sebagai placeholder / reservasi pada sebuah event yang dapat di spekulasi dalam sebuah perhitungan.

- Promise biasanya dipakai ketika waktu aksi tidak dapat ditentukan atau untuk berspekulasi .

- Promise dibentuk menggunakan Promise Constructor .

- Sebuah Promise mempunyai ketentuan reject , pending atau resolve , hampir sama kaya exception atau throw catch
```
const wait = time => newPromise((resolve) => setTimeout(resolve,time));

wait (5000).then(() => console.log(Hello!)); // hasilnya adalah Hello! 
```
```
Keterangan , 
.then akan menangani sebuah nilai .
Code akan menjalankan output Hello dengan interval 5000 (5detik) . 
```
### Apa itu async await pada ES7 ?

- ES 2017 atau ES7 mengeluarkan function baru yaitu Asynchronous atau Async .

- Async Function ini ditujukan untuk membuat code secara singkat pada metode asynchronous .

- Async Function akan me return (render) Promise .
- Jika Function mendapati error , maka Promise akan membuat rejected .
- Jika Function mendapati sebuah nilai/value , maka Promise akan membuat resolved.
```
async function add(x,y){
   return x + y;
```
- Await pada  Async Function dapat digunakan sebagai ekspresi .

- Await berfungsi untuk menunda (pause) async function hingga Promise mendapati resolve untuk sebuah nilai .
```
Function doubleAfter2seconds(x) {
    return new Promise(resolve => {
       resolve(x * 2);
}, 2000);
    PLEASE INSERT CODE
```

### Apa yang baru pada ES8 ?

- Object.values()
Akses semua value dengan objek tanpa terkecuali .
```
const countries = {DE:"Germany", ID:"Indonesia"};

Object.values(countries);

// output ==>  ["Germany","Indonesia"]
```

### Apa itu Object.assign() ?

Object.assign() merupakan metode untuk menyalin semua nilai yang bersangkutan dari properties object ke object target , dan hasil nya akan di return kepada target object .
```
const target = { a:1, b:2 };
const source = {b:4, c:5} 

const returnedTarget = Object.assign(target,source);
```
```
console.log (target);
//output: Object { a:1, b:4, c:5}
```
```
console.log(returnedTarget);
//output: Object { a:1, b:4, c:5}
```
