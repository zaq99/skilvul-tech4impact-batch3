![Image Banner!](assets/js-banner-intermediate.png "Javascript")
# **Javascript Intermediate**
## Javascript Modules
> adalah cara untuk memisahkan kode ke file yg berbeda

### Apa keuntungan menggunakan module ?
- mudah untuk mengelola kode
- kode ga numpuk di 1 file

### Bagaimana cara import dan eksport ?
   - cara import
     - pada file js gunakan :
     ```
     import {variable} from "direct file.js"
     ```
   
   - pada file html tambahkan
   ```type="module"```
     > example : 
     ``` 
     <script src="script.js" type="module"></script>
     ```

   - jika ingin ubah nama variable form export, gunakan as
     > example : 
     
     ```
     import{varibale as newVariable} form 'direct file.js'
     console.log(newVariable)
     ```

   - cara eksport
   pada file js gunakan :
   ```export pada variabel/object/func/array``` yg ingin di eksport
      > example : 
      ``` 
      exsport let motor = ['honda','yamaha']
      ```
   
   - ekport default
      > - eksport bawaan dan tidak menggunakan kurung kurawal
      >  - ! hanya bisa digunakan 1x
      > example : 
        ```
        export default motor
        ```
   ![Image Banner!](assets/modules.png "Javascript")

### **Noted**
- file yg sudah ada dalam html hanya bisa import tidak dapat melakukan eksport
- selain file utama yg tertanam di html, jika sudah di eksport maka tidak bisa import
---
## Recursive
> adalah function yang memanggil dirinya sendiri sampai kondisi tertentu
![Image Banner!](assets/recursive.png "Javascript")
>
> example :
>    ```
>      function recursive (){
>         recursive()
>      }
>    ```

### kenapa perlu recursive ?
> recursive digunakan untuk perhitungan matematika yang cukup rumit

example :
   ```
      function deretAngka(x) {
         //base case
         if(x == 1){
            console.log(x)
         } else {
            // recursvive case
            deretAngka(x - 1)
            console.log(x)
         }   
      }

   deretAngka(5)
   ------------------------------
   // output :
   1
   2
   3
   4
   5

   ```
---
## Asyncrhonous 
> Asynchronous adalah proses yang dijalankan secara tidak berurutan

### Bagaimana Proses dalam Javascript ?
![Image Banner!](assets/async.png "Javascript")

### Simulasi proses js
![Image Banner!](assets/js-proses.png "Javascript")
### Terdapat 3 Kunci Utama dalam Async 
- callback
  > adalah sebuah function yg dijadikan argumen
  ```
  callback(() => { 
	console.log("B")
   })
   ```

- promise
  > seperti sebuah janji, dia akan bejalan kode yg dipunya namun mengunggu semua kode dijalankan, lalu cek kondisi kode mana yg akan di jalankan  
   ```
   let makanPromise = new Promise((reslove, reject) => {
    reslove('jadi makan') // berhasil
    reject('ga jadi makan') //gagal
   })

   // eksekusi prosess ....

   console.log("a")

   makanPromise
   // then untuk menangkap relosve (jika berhasil)
   .then(result => {
      console.log(result)
   })
   // catch untuk menangkap reject (jika gagal)
   .catch((err) => {
      console.log(err)
   })

   console.log("B")

    ------------------------------
   // output :
   a
   b
   'jadi makan'
   ```
   - ```.then``` untuk menangkap jika berhasil
   - ```.catch``` untuk menangkap jika gagal


- Asynchronous Fetch
   ```
     fetch("https://pokeapi.co/api/v2/pokemon/pikachu/", {
  method: "GET"
  })
   .then(async (response) => {
  let convertData = await response.json();
  console.log(convertData);
  })
  .catch((error) => {
  console.log(error);
  });
   ```
- Asynchronous promise
   ```
      function GetUser(id) {
      return new Promise((resolve, reject) => {
      if (id !== "" && id !== undefined) {
      resolve (id);
      } else {
      reject ("ID Harus di Isi");
      }
      });
   }
   
   GetUser( ) // memanggil fungsinya GetUser
   .then((response) => {
      console.log(response);
      })
   .catch((error) => {
   console.log(error);
   });
   ```
---
## Git & Github lanjutan
1. membuat branch baru  
   ```git branch branchName```

2. pindah branch   
   ```git switch brancName```
   or  
   ```git checkout brancName```
3. menggabungkan isi branch  
   ```git merge brancName```
   
----

## Responsive WEB Design 
### Apa itu responsive WEB Design ?
> adalah design yang tetap terlihat bagus menyesuaikan ukuran layar pengguna

### Beberapa cara setting Design WEB menjadi responsive
1. Add viewport in html
   ```
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```
2. Use max width
    ```
    <img src='skilvul.png' max-widht='100%' alt='logo skilvul'>
    ```
3. Use element responsive with css
   > - %
   > - rem
   > - em
   > - vh
   > - media query
   > 

4. Use media query
![Image Banner!](assets/css-media.png "media query")



----
![Image Banner!](assets/bst-banner.png "Bootstrap")
# **Bootstrap**
### Apa itu bootstrap ?
> bootstrap adalah sebuah framework css yang memudahkan kita untuk styling menjadi lebih mudah, rapih, cepat dan responsive

### Cara memasang bootstrap
1. online
   > buat meta tag di head. Cara memanggil css bootstrap dengan menggunakan href lalu mengganti link href css lokal dengan link boostrap online.

2. offline
   > download dan ekstrak bootstrap, lalu satukan dalam satu folder html. hubungkan file :
   > - bootstrap.min.css
   > - bootstrap.min.js
   

### Breakpoints pada bootstrap :
- sm
- md
- lg
- xl
- xxl

### Cara penggunaan bootstrap
> caranya sangat mudah, hanya dengan memberi class pada element html yang ingin kita styling, penamaan class pun sangat relevan 
>
>  ```
>   <p class='text-danger'>Skilvul.com</p>
> ```

