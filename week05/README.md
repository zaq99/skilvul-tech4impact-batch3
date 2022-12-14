![Image Banner!](assets/react-banner.png "Javascript")

# **React js Dasar**

## apa itu React js ?

> react.js adalah library javascript yg berkonsep komponen base, yang sangat memudahkan kita dalam development terutama pada sisi FrontEnd

## Install React js

-   Install **node js**, download disini https://nodejs.org/en/
-   Install **react js**, download disini https://reactjs.org/

### install React Js from Vite

download disini https://vitejs.dev/guide/

-   install

    -   npm create vite@latest my-react-app --template react
    -   pilih react, pilih javacript
    -   cd react-app
    -   npm install

-   run
    -   npm run dev

![Image Banner!](assets/component.png "React.js")

### Perbedaan Class Component VS Function Component

> -   Functional component hanya bisa menggunakan props itu sebabnya function component disebut stateless component atau biasa digunakan juga sebagai UI Component (komponen yang menangani tampilan).
> -   sedangkan Class component dapat menggunakan state dan props.

### Styling CSS in React Js

> replace **class** to **className**

### Install Bootstrap in React JS

-   can use react bootstrap
-   can use bootstrap
    -   use CDN
    -   drop link in index.html
    -   use Install bootsrap
    -   https://blog.logrocket.com/using-bootstrap-with-react-tutorial-with-examples/

### Perbedaan props vs state

> props adalah singkatan dari properties yang berfungsi sebagai parameter untuk menangkap data dari state, sedangkan state berfungsi untuk mengirim data

-   state site

    ```
          function App() {
          return (
              <>
              <Nav />
              <Kartu foto={'https://i.pinimg.com/originals/5a/74/dc/5a74dc1edc469d9a6d985338f1cdd230.jpg'} nama={'Patrick'} keterangan={'teman spongebob'} />

              </>
          );
      }
    ```

-   props site

    ```
      const Kartu = (props) => {
          return (
              <>
                  {/* styling menggunakan bootstrap */}
                  <div className="container d-flex gap-2">
                      <div>
                          {/* styling menggunakan ekternal css */}
                          <img className="image-kartu" src="https://play-lh.googleusercontent.com/ZqSUbqjoUmb-2MpPNkzvh9O0jBiOffhdocrZRwZ2Jliwy3TJ8DawPvjZx_AonSiw7e5p" alt="" />
                      </div>
                      <div>
                          <h4>{props.nama}</h4>
                          <p>Orang yang jenius</p>
                      </div>
                  </div>

              </>
          )
      }
    ```

-   props after defracture

    ```
      const Kartu = ({ foto, nama, keterangan }) => {
          return (
              <>
                  {/* styling menggunakan bootstrap */}
                  <div className="container d-flex gap-2">
                      <div>
                          {/* styling menggunakan ekternal css */}
                          <img className="image-kartu" src={foto} alt="" />
                      </div>
                      <div>
                          <h4>{nama}</h4>
                          <p>{keterangan}</p>
                      </div>
                  </div>

              </>
          )
      }
    ```

### Lifecycle

> adalah sebuah siklus dari element, dari ia muncul, ada perubahan, dan menghilang
> mount, update, unmount

### UseState

> variabel untuk menyimpan data yg datanya berubah dalam react

-   example

    ```
    const [name, setName] = useState('zaq')
    const [age, setAge] = useState('21')
    ```

    ### noted

    -   '<>...</> = react fragment, digunakan untuk menggantikan div atau menuliskan multiple kode pada return

    -   **tittle case**
        diawali dengan huruf besar, untuk memberitau react jika itu adalah
        component milik kita bukan component bawaan.

        -   example : HomePage
        -   example default component : h1, header, table, dsb.
        -   example **camel case** : homePage
