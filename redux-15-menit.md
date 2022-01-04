### Apa itu Redux ?

Redux adalah open-source Javascript library untuk mengatur penggunaan state .

Redux merupakan library yang ringan , yang di desain untuk mengetahui alur state menjadi sebuah container agar rute dan penggunaannya lebih teratur .

Singkatnya Redux mengatur bagaimana state (data) bekerja dan respond terhadap interaksi user .

Redux dibuat oleh Dan Abramov dan Andrew Clark , 2015 .

### Apa itu konsep Single Source of Truth pada Redux ?

Yaitu dengan menggunakan state yang tersimpan pada object tree pada seluruh aplikasi .

Hal ini membuat state menjadi lebih teratur , teroptimisasi dan dapat digunakan pada function lain tanpa ekstra code .

### Apa itu action pada Redux ?

Action adalah objek yang mempunyai property spesifik yang nantinya dibawa ke container lain.

Action dikirim melalui props store.dispatch()


### Apa saja pilar-pilar cakupan Redux ?

1. Single Source of Truth , artinya State diimpan pada pohon object (object tree) yang dapat digunakan di seluruh implementasi aplikasi .

2. State is read-only , artinya satu-satu nya cara untuk mengubah sebuah state (data) adalah dengan melakukan prosedur action dan object . Action dan object akan mengizinkan untuk membuat write pada interaksi user tanpa membuat default state terubah .

3. Perubahan dengan pure function , artinya anda menulis setiap action yang akan digunakan sebagai reducers .
Reducers digunakan untuk mengambil state sebelumnya pada function yang kemudian menggunakan action sebagai parameter yang kemudian lanjut ke sesi state berikutnya .


### Apa itu mapStateToProps() ?

mapStateToProps membuat state baru dari yang asli melalui reducer sehingga dapat dijadikan props pada component .

mapStateToProps di perbarui setiap kali dipanggil .

### Apa itu map DispatchToProps () ?

mapDispatchToProps ditugaskan untuk mengeksekusi function ketika akan ter trigger melalui reducer .

props tidak hanya berupa object , function juga bisa termasuk props.

Contoh dari mapDispatchToProps adalah tombol click yang akan men-trigger refresh dan saat itu otomatis data ter mount

### Apa itu connect() function pada redux ?

connect() pada redux digunakan untuk membuat sambungan dari react component ke redux store.


