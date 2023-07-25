# React Başlangıç Kılavuzu
React Başlangıç Kılavuzu


React Başlangıç Kılavuzu
Hoş geldiniz! Bu kılavuz, React'i yeni başlayanlar için anlaşılır ve adım adım öğrenilebilir şekilde sunmayı amaçlamaktadır. React, modern web uygulamaları geliştirmek için popüler bir JavaScript kütüphanesidir ve kullanıcı arayüzlerini oluşturmak için kullanılır.

Bu dokümantasyon, temel JavaScript bilgisine sahip ancak React'i henüz bilmeyenler için tasarlanmıştır. Sizlerin deneyim seviyelerine uygun olarak, bu kılavuzda React'in temellerini kavrayacak ve etkileyici web uygulamaları oluşturmanıza yardımcı olacak adımları öğreneceksiniz.

React Nedir?
React, Facebook tarafından geliştirilen açık kaynaklı bir JavaScript kütüphanesidir. Web uygulamalarının kullanıcı arayüzlerini oluşturmak için kullanılır ve özellikle tek sayfa uygulamaları (Single Page Applications - SPA) için idealdir. React, bileşen tabanlı bir yapıya sahiptir, bu da uygulamaları küçük ve bağımsız parçalara bölmeyi ve yönetmeyi kolaylaştırır.


<br><br>
### 1-) React Proje Kurulumu

```javascript
yarn create react-app myapp
```
bulunduğunuz dizine "myapp" klasörü açarak dosyaları bu klasöre yükler. 
<br><br>

Eğer bulundusğunu dizine yükleme yapmak isterseniz ise aşağıdaki kodu kullanmanız gerekmektedir.

```javascript
yarn create react-app ./
```
<br><br>

### 2-) React Projenin Çalıştırılması

```javascript
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
```javascript
yarn add modulunAdı
```

##### Örnek
```javascript
yarn add bootstrap
```
Bu örnekde bootsrap modülünü uygulamamıza dahil ettik.



