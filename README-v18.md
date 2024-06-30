# React Başlangıç Kılavuzu
React v18 Başlangıç Kılavuzu


React v18 Başlangıç Kılavuzu
Hoş geldiniz! Bu kılavuz, React'i yeni başlayanlar için anlaşılır ve adım adım öğrenilebilir şekilde sunmayı amaçlamaktadır. React, modern web uygulamaları geliştirmek için popüler bir JavaScript kütüphanesidir ve kullanıcı arayüzlerini oluşturmak için kullanılır.

Bu dokümantasyon, temel JavaScript bilgisine sahip ancak React'i henüz bilmeyenler için tasarlanmıştır. Sizlerin deneyim seviyelerine uygun olarak, bu kılavuzda React'in temellerini kavrayacak ve etkileyici web uygulamaları oluşturmanıza yardımcı olacak adımları öğreneceksiniz.

React Nedir?
React, Facebook tarafından geliştirilen açık kaynaklı bir JavaScript kütüphanesidir. Web uygulamalarının kullanıcı arayüzlerini oluşturmak için kullanılır ve özellikle tek sayfa uygulamaları (Single Page Applications - SPA) için idealdir. React, bileşen tabanlı bir yapıya sahiptir, bu da uygulamaları küçük ve bağımsız parçalara bölmeyi ve yönetmeyi kolaylaştırır.


[1-) React Proje Kurulumu](https://github.com/MercanX/react-documentation#1--react-proje-kurulumu)

[2-) React Projenin Çalıştırılması](https://github.com/MercanX/react-documentation#2--react-projenin-%C3%A7al%C4%B1%C5%9Ft%C4%B1r%C4%B1lmas%C4%B1)

[3-) Projenin Temiz Hale Getirilmesi](https://github.com/MercanX/react-documentation#3--projenin-temiz-hale-getirilmesi)

[4-) Dosya içeriklerinin temizlenmesi](https://github.com/MercanX/react-documentation#4--dosya-i%C3%A7eriklerinin-temizlenmesi)

[5-) Modül Yükleme](https://github.com/MercanX/react-documentation#5--mod%C3%BCl-y%C3%BCkleme)

[6-) Components Oluşturma](https://github.com/MercanX/react-documentation#6--components-olu%C5%9Fturma)

[7-) Componenti App.js Ekleme](https://github.com/MercanX/react-documentation#7--componenti-appjs-ekleme)

[8-) useState Kullanımı](https://github.com/MercanX/react-documentation#8--usestate-kullan%C4%B1m%C4%B1)

[Tools](https://github.com/MercanX/react-documentation#tools)


<br><br>
### 1-) React Proje Kurulumu

```terminal
yarn create react-app myapp
```
bulunduğunuz dizine "myapp" klasörü açarak dosyaları bu klasöre yükler. 
<br><br>
Eğer bulundusğunu dizine yükleme yapmak isterseniz ise aşağıdaki kodu kullanmanız gerekmektedir.

```terminal
yarn create react-app ./
```
<br><br>
### 2-) React Projenin Çalıştırılması

```terminal
yarn start
```
<br><br>
### 3-) Projenin Temiz Hale Getirilmesi

##### 3.1-) public Klasörüde sadece aşağıdakiler olacak diğerleri silinecek

index.html
<br><br>
##### 3.2-) src Klasörüde sadece aşağıdakiler olacak diğerleri silinecek

App.css

App.js

index.css

index.js
<br><br>
### 4-) Dosya içeriklerinin temizlenmesi

##### 4.1-) public/index.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <meta name="theme-color" content="#000000" />
    <meta name="description" content="Web site created using create-react-app" />
    <title>React App</title>
  </head>
  <body>
    <noscript>You need to enable JavaScript to run this app.</noscript>
    <div id="root"></div>
  </body>
</html>
```
<br><br>
##### 4.2-) src/App.css

İçersi tamamen silinecek
<br><br>
##### 4.3-) src/App.js

App.js
```javascript
import './App.css';

function App() {
  return (
    <div>
      React Project
    </div>
  );
}

export default App;
```
<br><br>
##### 4.4-) src/index.css

İçersi tamamen silinecek
<br><br>
##### 4.5-) src/index.js

```javascript
import React from 'react';
import ReactDOM from 'react-dom/client';
import './index.css';
import App from './App';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
```
<br><br>
### 5-) Modül Yükleme
İki Türlüde modül yükleyebiliriyoruz

##### Komut
```terminal
yarn add modulunAdı
```
<br><br>
##### Örnek
```terminal
yarn add bootstrap
```

App.js
```javascript
import './App.css';
import 'bootstrap/dist/css/bootstrap.min.css'

function App() {
  return (
    <div>
      React Project
    </div>
  );
}

export default App;
```
Bu örnekde bootsrap modülünü uygulamamıza ve App.js ye dahil ettik.
<br><br>
### 6-) Components Oluşturma

React bileşenleri, bir web uygulamasının arayüzünün farklı parçalarını oluşturmak için kullanılan bağımsız ve yeniden kullanılabilir JavaScript fonksiyonları veya sınıflarıdır. React bileşenleri, uygulamadaki belirli parçaların sorumluluklarını ve davranışlarını düzenlemeye yardımcı olur.


##### 6.1) Arrow Fonksiyonlu Bileşenler (Arrow Function Components):
Arrow fonksiyonlu bileşenler, fonksiyon bileşenlerinin bir başka kısa ve okunaklı şeklidir. Fonksiyon bileşenlerinde olduğu gibi, props parametresini alır ve JSX içinde kullanılabilir. State yönetimi için React kancalarını kullanabilirsiniz. Daha çok bunu kullanıyoruz.
<br><br>
##### Örnek1
Lesson.jsx dosyası oluşturuyoruz. Dosyayı açtıktan sonra VSCode da aşağıdaki kodu yazdığımızda otamatik oluşuyor.
Not: Dosyanın ilk harfi Büyük olacak.

```terminal
rafce
```

```javascript
import React from 'react';

const Lesson = () => {
  return (
    <div>
      React Project
    </div>
  );
}

export default Lesson;

```
<br><br>
##### Örnek2 props ile kullanımı
Lesson.jsx dosyası oluşturuyoruz. Dosyayı açtıktan sonra VSCode da aşağıdaki kodu yazdığımızda otamatik oluşuyor. Aşağıdaki örnekdede görüldüğü gibi Propsları biz de içersine ekliyoruz. 
Not: Dosyanın ilk harfi Büyük olacak.

```terminal
rafce
```

```javascript
import React from 'react';

const Lesson = (props) => {
  return (
    <div>
      <h1>{props.title}</h1>
      <p>{props.description}</p>
    </div>
  );
}

export default Lesson;

```
<br><br>
##### 6.2) Fonksiyon Bileşenleri (Function Components):
Fonksiyon bileşenleri, React 16.8 sürümü ve sonrasında fonksiyonel bileşenler adıyla da bilinen basit ve temiz bir bileşen tanımlama yöntemidir. Bir fonksiyon bileşeni, props (özellikler) parametresini alır ve JSX içinde kullanılabilir. State yönetimi için useState gibi React kancalarını (hooks) kullanabilirsiniz.
<br><br>
##### Örnek1
Lesson.jsx dosyası oluşturuyoruz. Dosyayı açtıktan sonra VSCode da aşağıdaki kodu yazdığımızda otamatik oluşuyor
Not: Dosyanın ilk harfi Büyük olacak.

```terminal
rafc
```


Lesson.jsx
```javascript
import React from 'react';

function Lesson() {
  return (
    <div>
      React Project
    </div>
  );
}

export default Lesson;
```
<br><br>
##### Örnek2 props ile kullanımı
Lesson.jsx dosyası oluşturuyoruz. Dosyayı açtıktan sonra VSCode da aşağıdaki kodu yazdığımızda otamatik oluşuyor. Aşağıdaki örnekdede görüldüğü gibi Propsları biz de içersine ekliyoruz. 
Not: Dosyanın ilk harfi Büyük olacak.

```terminal
rafc
```

Lesson.jsx
```javascript
import React from 'react';

function Lesson(props) {
  return (
    <div>
      <h1>{props.title}</h1>
      <p>{props.description}</p>
    </div>
  );
}

export default Lesson;
```
<br><br>
### 7-) Componenti App.js Ekleme

##### Örnek1
Lesson.jsx dosyasındaki bileşeni oluşturduktan sonra, bu bileşeni App.js dosyasına ekleyebilirsiniz. Bunu yapmak için import ifadesini kullanarak oluşturduğunuz bileşeni içeri aktarmanız gerekir.


Lesson.jsx 
```javascript
import React from 'react';

function Lesson() {
  return (
    <div>
      React Project
    </div>
  );
}

export default Lesson;
```


App.js
```javascript
import './App.css';
import Lesson from './components/Lesson';

function App() {
  return (
    <div>
      <Lesson/>
    </div>
  );
}

export default App;

```
<br><br>
##### Örnek2 props ile kullanımı

Lesson.jsx dosyasındaki bileşeni oluşturduktan sonra, bu bileşeni App.js dosyasına ekleyebilirsiniz. Bunu yapmak için import ifadesini kullanarak oluşturduğunuz bileşeni içeri aktarmanız gerekir.


Lesson.jsx
```javascript
import React from 'react';

function Lesson(props) {
  return (
    <div>
      <h1>{props.title}</h1>
      <p>{props.description}</p>
    </div>
  );
}

export default Lesson;
```


App.js
```javascript
import './App.css';
import Lesson from './components/Lesson';

function App() {
  return (
    <div>
      <Lesson title="Bileşen Başlık" description="Bileşen Açıklama" />
    </div>
  );
}

export default App;

```
<br><br>
### 8-) useState Kullanımı
 `useState` kancası (hook), React uygulamalarında durum yönetimi için kullanılan bir fonksiyondur. React'ta state (durum), bir bileşenin içindeki verileri depolamak ve bu verileri güncellemek için kullanılır.
 
<br><br>
Kullanışı:
```javascript
const [count, setCount] = useState(0);
```
`count` adlı değişkeni tanımladık ve başlangıç değeri olarak 0 verdik. `setCount` ile değişkeni güncellemek için kullanılan fonksiyonu tanımladık.

<br><br>
 `useState` kancasını ve bileşeninizi oluşturmak için import ifadesine eklenmesi gerekmektedir.
 ```javascript
import React, { useState }  from 'react';
```
<br><br>
Lesson.jsx
```javascript
import React, { useState }  from 'react';

function Lesson() {

  const [count, setCount] = useState(0);

  const azalt =()=>{
    setCount(count-1)
  }

  return (
    <div>
      <h1>Sayac: {count}</h1>
      <button onClick={() => setCount(count + 1)}>Artır</button>
      <button onClick={azat}>Azalt</button>
    </div>
  );
}

export default Lesson;
```

Örnekte, `count` adlı değişkeni tanımladık ve başlangıç değeri olarak 0 verdik. Ardından, `setCount` ile değişkeni güncellemek için kullanıyoruz.

Bu örnekte, 
Arttır butonuna tıklandığı zaman `count` değişkenini 1 arttırıyoruz ve `setCount` ile `count` değişkenini güncelliyoruz.
Azalt  butonuna tıklandığı zaman `azalt` fonksiyonunu çağırıyoruz, `count` değişkenini 1 azaltıyoruz ve `setCount` ile count değişkenini güncelliyoruz.

Not: Burada kısa yolu ve fonksiyon yazarak her iki durumuda görmüş olduk.

<br><br>
### Tools

##### 01- Html to jsx
Html yapıyı Jsx Yapıya dönüştürmeyi sağlıyor. Oldukca Kullanışlı bir site

[https://transform.tools/html-to-jsx](https://transform.tools/html-to-jsx)

