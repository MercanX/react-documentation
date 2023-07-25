# React Başlangıç Kılavuzu
React Başlangıç Kılavuzu


React Başlangıç Kılavuzu
Hoş geldiniz! Bu kılavuz, React'i yeni başlayanlar için anlaşılır ve adım adım öğrenilebilir şekilde sunmayı amaçlamaktadır. React, modern web uygulamaları geliştirmek için popüler bir JavaScript kütüphanesidir ve kullanıcı arayüzlerini oluşturmak için kullanılır.

Bu dokümantasyon, temel JavaScript bilgisine sahip ancak React'i henüz bilmeyenler için tasarlanmıştır. Sizlerin deneyim seviyelerine uygun olarak, bu kılavuzda React'in temellerini kavrayacak ve etkileyici web uygulamaları oluşturmanıza yardımcı olacak adımları öğreneceksiniz.

React Nedir?
React, Facebook tarafından geliştirilen açık kaynaklı bir JavaScript kütüphanesidir. Web uygulamalarının kullanıcı arayüzlerini oluşturmak için kullanılır ve özellikle tek sayfa uygulamaları (Single Page Applications - SPA) için idealdir. React, bileşen tabanlı bir yapıya sahiptir, bu da uygulamaları küçük ve bağımsız parçalara bölmeyi ve yönetmeyi kolaylaştırır.


[React Proje Kurulumu](https://github.com/MercanX/react-documentation/README.md#5--components-olu%C5%9Fturma)


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


##### 4.2-) src/App.css

İçersi tamamen silinecek

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


##### 4.4-) src/index.css

İçersi tamamen silinecek


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


### 5-) Modül Yükleme
İki Türlüde modül yükleyebiliriyoruz

##### Komut
```terminal
yarn add modulunAdı
```

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


### 5-) Components Oluşturma

React bileşenleri, bir web uygulamasının arayüzünün farklı parçalarını oluşturmak için kullanılan bağımsız ve yeniden kullanılabilir JavaScript fonksiyonları veya sınıflarıdır. React bileşenleri, uygulamadaki belirli parçaların sorumluluklarını ve davranışlarını düzenlemeye yardımcı olur.


##### 5.1) Arrow Fonksiyonlu Bileşenler (Arrow Function Components):
Arrow fonksiyonlu bileşenler, fonksiyon bileşenlerinin bir başka kısa ve okunaklı şeklidir. Fonksiyon bileşenlerinde olduğu gibi, props parametresini alır ve JSX içinde kullanılabilir. State yönetimi için React kancalarını kullanabilirsiniz. Daha çok bunu kullanıyoruz.

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

##### 5.2) Fonksiyon Bileşenleri (Function Components):
Fonksiyon bileşenleri, React 16.8 sürümü ve sonrasında fonksiyonel bileşenler adıyla da bilinen basit ve temiz bir bileşen tanımlama yöntemidir. Bir fonksiyon bileşeni, props (özellikler) parametresini alır ve JSX içinde kullanılabilir. State yönetimi için useState gibi React kancalarını (hooks) kullanabilirsiniz.

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

### 6-) Componenti App.js Ekleme

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
