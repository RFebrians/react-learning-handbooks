# React dalam 15 menit

### Bagaimana Virtual DOM Bekerja pada React ?
Virtual DOM adalah improvisasi dari Javascript Object yang memanfaatkan layer virtual dari Real DOM .
### Apa itu DOM ?
Document Object Model (DOM) adalah sebuah antarmuka pemrograman (programing interface) untuk HTML, XML dan SVG yang bersifat lintas platform dan language-independent , atau singkatnya ini yang membuat sebuah website menjadi Dinamis dengan penggunaan Javascript.
### Bagaimana Virtual DOM Bekerja ?
- Virtual DOM Bekerja dengan menggunakan struktur elemen yang kemudian attribute dan content digunakan sebagai Object dan Properties 
- Pada Virtual DOM React me-render struktur function di luar React Component . Hal ini membuat sebuah perubahan data (state management) dan sebuah keamanan serta performa efisien dari sebuah aksi-reaksi (action) yang telah ditentukan  .
- Kesimpulan dari Virtual DOM 
Virtual DOM setidaknya memiliki 3 langkah umum yang dapat kita ketahui ,
1.	Setiap pemuatan (loading) dan perubahan data seluruh UI di render pada Virtual DOM
2.	Berkat Virtual DOM perbedaan antara pemuatan sebelumnya dan yang akan datang dapat di perhitungkan (state management)
3.	Setelah proses pemuatan telah selesai , Implementasi Real DOM mengikuti hasil akhir dari Virtual DOM

 
### Functional Component
Functional Component ( Tanpa Hook) adalah Syntax asli Javascript Function yang menerima props object sebagai parameter pertama yang kemudian di return ke React Elements
Functional Component ini lebih simple ketimbang Class Component untuk membuat Component .
Awalnya function component ini tidak menerima state sebagaimana class . Kemudian pada tahun 2018 , React mengeluarkan useState sebagai state untuk Function Component , yang akan membuat code lebih simple dan dapat dipahami .

### Class Component

- Class Component merupakan bagian kelas dari ES6 .

- Class Component ini lebih kompleks dari function component karena meliputi constructors , life-cycle methods , render() function dan state(data) management .
- Class ini dapat menerima props pada constructor dengan metode render() yang kemudian di return menjadi React Element (JSX) atau bahkan null.

- Dan pada awalnya state hanya digunakan pada Class

### Apa itu State ?

- State adalah objek untuk Components . State ini menyimpan sebuah perubahan yang telah ditentukan secara realtime .

- Penggunaan terbaik untuk State adalah kita harus selalu membuat rute atau alur state secara simple dan meminimalisir stateful components (banyaknya penggunaan state). 


### Apa itu Props dalam React ?

- Props adalah input untuk Components . Props digunakan sebagai value yang akan di passing ke Components .
- Props ini dapat di passing dari Parent Components ke Child Components

 
### Bagaimanakah cara men-update state (versi Class) ?
```
// salah
this.state.message = ‘hello world’
```
- Contoh diatas adalah salah , hal ini tidak akan me-render Component .
- Melainkan kita menggunakan setState () pada Class Component . Seperti berikut 
```
// benar
this.setState({message:’hello world’})
```

### Apa itu ‘Key’ dalam props dan apa manfaatnya untuk digunakan sebagai array sebuah elements ?

- Key merupakan special string attribute yang harus digunakan ketika membuat array elements .
- Key membantu React mengidentifikasi item yang berubah , ditambah maupun dihapus .

### Apa itu Controlled Component ?

- Controlled Component adalah Component yang mengontrol sebuah input pada form masukan setelah terjadinya user input .
- Maksudnya adalah setiap state mempunyai batasan dalam function , dalam implementasi ini misal contohnya , form nomor hp tidak dapat dimasukan alfabet atau ketika terjadinya error handling .

- Contoh lain adalah ketika kita ingin merubah semua huruf menjadi uppercase atau kapital maka kita gunakan  handleChange sebagai berikut 
```
handleChange(event){
this.setState({
value:event.target.value.toUpperCase()})
}
```

### Apa itu Uncontrolled Component ?

- Uncontrolled Component merupakan lawan dari Controlled Component .
- Jika Controlled Component  di handle pada React Component , maka Uncontrolled Component ini di handle langsung oleh DOM .

- Uncontrolled Component ini menyimpan state secara tersendiri dan di query pada DOM menggunakan ref untuk mencari value yang di perlukan . Dengan kata lain ini berjalan pada  bagian terluar .


### Apa saja Tahapan Lifecycle pada React (Class) ?

Mounting : Ketika user masuk ke dalam Web , maka mounting akan mempersiapkan proses ini .Persiapan Component untuk di mount pada browser DOM . 
Setidaknya pada tahap ini lifecyclenya terdiri dari 
-	Constructor() , 
-	getDerivedStateFromProps(),
-	render(), dan 
-	componentDidMount().



Updating : Component dapat men-update perubahan dari interaksi melalui 2 cara yaitu
-	Mengirim state baru pada props kemudian men-update nya
-	Kemudian men-update state dari setState() atau forceUpdate()

Pada tahapan ini lifecyclenya terdiri dari 
-	getDerivedStateFromProps(),
-	shouldComponentUpdate(),
-	render(),
-	getSnapshotBeforeUpdate(),dan
-	componentDidUpdate(),

Unmounting : User meninggalkan halaman , dan semuanya kembali ke nilai default atau di set tertentu .
Pada tahap ini tidak diperlukan sebuah interaksi Component tambahan .
Lifecycle yang berada pada unmounting antara lain 
-	componentWillUnmount()

### Apa itu High Order Components ?

- High Order Components merupakan function yang akan menerima component dan membuat component baru .
- HOC ini dapat digabung pada component child namun tidak mengubah hasil atau 
```
//NEED REVISI HOC
```


### Apa itu React Fragments ?

React Fragment digunakan untuk men-wrap components dan dapat di return pada multiple elements .
Anda dapat menggunakan 
```
<React.Fragment>
// code
</React.Fragment>
```
Atau cukup
```
 <> 
 // code
</>
```
### Apakah div dan fragment itu sama ?
- Div adalah Container pada DOM .
- Sedangkan Fragment adalah Container dari React itu sendiri tentunya pada DOM juga .

Fragment mempunyai kelebihan antara lain , 
-	lebih cepat pemuatan 
-	Struktur yang lebih rapi saat inspeksi DOM
-	Dan mekanisme CSS seperti Flexbox atau CSS Grid yang dapat mempermudah layout

### Apa itu Validation Props ?

- Pada dasarnya Validation props digunakan seiring development . 
- Validation lebih berguna ke arah Developer ketimbang User .
- Secara default Validation props pada Production akan di disable .

- React akan mencoba menge-check setiap props ketika dijalankan , dan menampilkan validasi nya ketika ada error. 
- Jika ada yang salah , maka akan ditampilkan pada console .
- Berikut adalah beberapa list prop type yang biasa di check
```
-	PropTypes.number
-	PropTypes.string
-	PropTypes.array
-	PropTypes.object
-	PropTypes.funct
-	PropTypes.node
-	PropTypes.element
-	PropTypes.bool
-	PropTypes.symbol
-	PropTypes.any
```
### Apa keuntungan menggunakan React ?

-	Mengoptimisasi performa dengan penggunaan Virtual DOM.
-	JSX membuat code dapat dibaca dan terstruktur
-	Dapat di render secara client side dan serverside rendering (SSR)
-	Compatible terhadap framework lainnya , karena React merupakan Library
-	Dapat ditulis menggunakan unit , integration test dan test-test lainnya menggunakan Jest atau React Testing Library

### Apa kelemahan dalam React ?

-	React adalah Library , bukan Framework
-	Learning Curve dalam React cukup menengah
-	Integrasi React ke Tradisional MVC framework membutuhkan konfigurasi lebih lanjut
-	Tingkat kerumitan code bertambah seiring waktu ketika menggunakan component lainnya 

### Apa itu Ajax Call dalam React ?

- AJAX merupakan metode , yang kepanjangannya Asynchronous Javascript And XML.
- Dengan metode AJAX kita dapat mengambil data dari server.

- AJAX dalam react menggunakan fetch atau libraries tambahan seperti Axios dan Jquery AJAX .

### Apa itu Hooks dalam React ?

- Hooks di perkenalkan dalam React pada versi 16.8 

- Hooks mengizinkan kita untuk menggunakan state pada React tanpa harus menggunakan Class.
- Hooks pada React antara lain 
```
-	useState()
-	useEffect()
-	useContext()
-	useReducer()
-	useCallback()
-	useMemo()
-	useRef()
-	useImperativeHandle()
-	useLayoutEffect()
-	useDebugValue()
```
### Apa itu useState() Hook ?

- useState merupakan bagian dari Function Component . 
- useState mengizinkan kita untuk melakukan perubahan state (status,data,perubahan bentuk,dsb) pada Function Component dengn beberapa peraturan , antara lain ;

- useState digunakan untuk 1 argument yang akan menjadi awalan nilai dari pada permulaan state
- useState membutuhkan 2 array untuk di return
- Array yang pertama adalah nama state , dan array yang kedua adalah function yang akan membuat state menjadi update . 
```
const [ mobil , updateMobil ] = useState(0);
```
atau
```
const [mobil , setMobil ] = useState(0);
```
function array yang kedua digunakan untuk men-update state pertama , dan ingat ditulis secara camelCase .

### Apa itu useEffect() Hook ?

- useEffect adalah Hook yang memegang kendali pada life cycle atau disebut juga efek.

useEffect dapat digunakan untuk 2 argument sekaligus .
- Argumen pertama adalah effect (proses pada background) yang akan dijalankan. Ini sama seperti componentDidMount atau componentDidUpdate pada Class
- Argumen kedua merupakan opsional . useEffect pada argumen kedua mengizinkan untuk di re-run pada keadaan yang berbeda .
Jika argumen kedua tidak hadir , maka useEffect akan berjalan terus setiap kali di render pada React Component . 

### Apa itu useReducer() Hook ?

- useReducer Hook digunakan untuk memanagement state . Sama seperti useState , namun lebih kompleks .

- Perbedaan pada useState dan useReducer adalah useReducer mengupdate state dengan passing function ketimbang memanggil function update itu sendiri .

- Ini seperti cara Redux bekerja . Reducer merupakan pure function dari Javascript yang akan dilaksanakan sesuai dengan event yang ditentukan secara berurutan.

- UseReducer menerima argument dari reducer function .

- Reducer function itu sendiri mengharuskan memiliki state dan action yang kemudian berjalan sesuai urutan event .

Apa itu useContext() Hook ?

- useContext Hook memiliki semua kesamaan pada Context API pada React Class Component.
- useContext ini dikemas secara simple mengizinkan anda dapat menggunakannya dalam Function component.

- Context menggunakan metode consumer dan provider . 

- Yang spesial dari useContext , kita dapat memahami bahwa useContext menyimpan value dan dapat di passing ke seluruh context object , tidak hanya consumer atau provider .

- Lihat perbedaannya syntaxnya seperti berikut ini , 
- kita membuat object Context pada React menggunakan Context API , yaitu React.CreateContext seperti berikut
```
const AppContext = React.createContext({foo : bar});
```
sedangkan useContext 
```
const context = useContext(AppContext);
```

### Apa itu useMemo() Hook ?

- useMemo hampir sama seperti useCallback , hanya saja perbedaannya ada pada optimisasi performa disini kita menyebutnya memoization (untuk useMemo).

- useMemo menerima setiap function dan kemudian siap dipanggil ketika ada value yang dibutuhkan .

- useMemo cukup baik untuk peningkatan performa saat memproses data secara bulk (banyak) . 

- useMemo akan dijalankan pertama kali ketika me-render , yang kemudian membuat sebuah cache sementara dan akan kembali lagi ke cache setiap kali render di lakukan .

### Apa itu useRef() Hook ?

- useRef Hook adalah function return yang berinteraksi dengan object yang tidak tetap (mutable) yang kemudian dapat di passing ke argumen berikutnya .

- Objek yang telah di return akan menjadi permanen.

Contoh penggunaan useRef
```
const refContainer = useRef(initialValue);
```
Setidaknya ada dua cara penggunaan useRef :
- Akses menuju DOM atau React Element
- Membuat object tidak tetap (mutable) menjadi variable (fixed)


### Apa itu ReactTestUtils ?

- React Test Utils adalah Test Utilities yang disediakan React untuk mengetes dan mensimulasikan DOM yang bertujuan sebagai Unit Testing .

### Apa itu Jest ?

- Jest atau kepanjangannya adalah JavaScript Unit Testing merupakan Framework Testing yang dibuat oleh Facebook berdasarkan Jasmine yang menyediakan automated mock creation dan Fake DOM (jsdom) environment .

- Jest biasa ditujukan sebagai Testing Components.

### Apa Kelebihan Jest sebagai Testing Framework ?

- Tugas otomatis dalam menjalankan test pada code .
- Mocks dalam dependencies ketika menjalankan test
- Dapat melakukan async test yang diperlukan ketika dibutuhkan sebuah koneksi untuk mengambil data (fetch)
- Testing dijalankan pada fake DOM (jsdom) dan dapat dijalankan pada Command Line
- Testing dilakukan secara berurutan sesuai perintah.
