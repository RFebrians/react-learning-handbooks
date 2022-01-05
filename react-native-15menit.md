### Apa itu React Native ?
- React Native adalah Framework open-source untuk mobile Application dibuat oleh Facebook dan berdasarkan React .
- Keunggulan React Native antara lain dapat me re-use code antar web dan mobile
- React Native pertama kali di rilis secara stabil pada 26 Maret 2015

### Apa Saja kelebihan pada React Native ?
- Cara kerja React Native sangat mirip dengan react yang memungkinkan anda hanya perlu belajar web dan ES6
- Kompatible dengan berbagai mobile dan web framework , seperti React Native CLI dan Expo
- Menggunakan JSX dan TSX
- React Native membuat mobile app secara cepat dan fleksibel

### Apa itu StyleSheet pada React Native ?
- Stylesheet adalah module React Native untuk membuat style
- Cara kerjanya hampir sama dengan CSS

```
const styles = StyleSheet.create({
  container: {
    flex: 1,
    padding: 24,
    backgroundColor: "#eaeaea"
  },
  ```
 
 ### Apakah React Native support pada multi platform ?
 - React Native merupakan framework crossplatform yang ditujukan untuk membangun aplikasi Android dan IOS 

  ### Apa itu Gesture Responder pada React Native ?
  - Gesture Responder System bekerja menangani setiap interaksi user dengan touch screen 
  - Sebagai contoh tap dan scroll akan di respons oleh Gesture Responder
  - React Native Gesture Responder merupakan library powerful yang digunakan sebagai standar untuk scrolling , single tap , double tap , zoom in/out distance 
  
  ### Bagaimana cara store data pada AsyncStorage di React Native ?
  Async Storage pada React Native merupakan localstorage pada reactJS
   4 tahapan yang kita perlu pahami dalam menggunakan Async Storage
   
   ```
   import { AsyncStorage } from 'react-native';
   ```
### Apa saja database yang digunakan untuk React Native ?
- SQLite
- Firebase
- RealM
- Watermelon DB
- PouchDB
- MongoDB

### Apa itu FlatList component ?
- FlatList efisien terhadap bentuk layar pada scrolling list data
- data dan renderItem merupakan dua props primer yang dibutuhkan untuk FlatList
- prop data akan mengambil array data. Membuat nya sebagai list dan variasi object.
- prop renderItem akan mengambil elemen secara individual dari data array yang kemudian merender nya menjadi component

### Apa itu Expo dan hubungannya pada React Native ?
- Expo merupakan framework dan platform pada Aplikasi React
- Expo terdiri dari serangkaian tools yang menyediakan development , build dan deploy untuk IOS dan Android menggunakan Javascript atau Typescript
- Expo mempunyai cukup banyak API untuk digunakan dibandingkan React Native CLI
- Tetapi Expo juga mempunyai batasan tertentu ketimbang React Native CLI :
```
- Tidak semua API pada IOS dan Android tersedia
- Ukuran Aplikasi yang tergolong besar saat production
- Minimal Supported Version adalah Android 5.0 dan IOS 10
```

### Apa itu Hermes ?
- Hermes merupakan open-source Javascript Engine Optimized untuk React Native pada Android.
- Hermes digunakan untuk improvisasi app pada start-up time , memory reduction dan kompresi ukuran app

### Apa itu Animated API ?
- Animated API dari React Native di design secara variasi untuk membuat sebuah gerakan animasi pada sebuah component .
- Animated berfokus pada inputs dan outputs yang dapat di konfigurasi melalui control time-based animation
- Animated API men-ekspor animasi component yaitu : View , Text , Image , Scrollview , FlatList dan SectionList 
- Kita juga dapat membuat Animated API sendiri menggunakan Animated.createAnimatedComponent()

### Apa perbedaan antara React dan React Native ?
- React atau React JS adalah Javascript Library untuk membangun Web Application pada HTML5
- React Native adalah Framework crossplatform React yang digunakan untuk membangun Aplikasi pada Android dan IOS .


### Bagaimana React Native Apps dijalankan saat Development ?
- Yaitu dengan menggunakan Emulator atau Real Device.
- React Native CLI dan Expo CLI menyediakan emulator pada saat development dengan hot reload (live).
- Pada React Native CLI anda dapat menggunakan Android ADB dan Android Studio Kit untuk connect pada Real Device dengan USB .
- Sedangkan pada Expo anda dapat men-scan QR kode pada saat development .

### Apa itu Flexbox pada React Native ?
- Flexbox di design untuk menyesuaikan layar device pada React Native .
- Flexbox bersifat konsisten dan absolut .
- Pada dasarnya cara kerja Flexbox sama dengan CSS , dan tujuannya memang untuk Styling Component .
- seperti contoh flex :1 akan selalu berada di tengah-tengah layar .

### Apa itu ScrollView ?
- ScrollView adalah sebuah scrolling container yang dapat mencakup components dan views.
- Item yang berada pada ScrollView dapat diatur vertical dan horizontal .

### Apa itu Dimension API ?
- React Native menggunakan DPI atau DOts Per Inch untuk mengatur segala urusan pada UI di layar
- Hal ini membuat pengukuran pada DPI terlihat sama meski berbeda ukuran layar dan pixel .
- Sepenuhnya anda juga dapat mengatur ukuran ini pada React Native dengan Dimension API
```
Dimensions.get('window').height;
```
```
Dimension.get('window').width;
```
### Apa saja batasan dari React Native ?
- Dependencies pada third party libraries mungkin saja tidak support .
- Tidak support untuk Aplikasi yang membutuhkan Multi Processing.
- Dibutuhkan konfigurasi lebih lanjut untuk deployment pada IOS
