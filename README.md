# React Todo

Bu uygulamada React kullanarak bir Todo application'ı yazacağız. Todo app, bir yapılacaklar listesidir. 

## Pratik yapılacak yetenekler

- Sıfırdan bileşenler oluşturma
- State'i en üst bileşende depolama ve proplar yardımıyla alt bileşenlerde kullanma
- `change` ve `submit` event handlerları oluşturma

## Giriş

Bu projede `yapılacaklar listesine` eleman eklenmesine, tamamlandı olarak işaretlenmesine ve viewden kaldırılmasına izin veren bir uygulama oluşturacaksınız.
Uygulama şunları içermelidir:

- Şu dosyadaki [gif](./todo.gif) örneği ilham alarak projenizi DOM'a aktarın.
- Tüm yapılacaklar stateini `App.js` bileşeninde depolayın. State'in içeriği aşağıdaki gibi olmalıdır:

  ```js
  [
    {
      isim: 'Yemekleri Pişir',
      id: 1528817077286, // farklı görünüyor olabilir, bunu oluşturmak için timestamp(zaman damgası) kullanabilirsiniz
      tamamlandi: false
    },
    {
      isim: 'Bake Cookies',
      id: 1528817084358,
      tamamlandi: false
    }
  ]
  ```

- `yapılacaklar` elemanının üzerine tıklanması halinde state'indeki "tamamlandı" durumunu toogle(aç/kapa) şeklinde dizayn edin.
- Todo form bileşeni submit edildiğinde listeye yeni bir "todo" elemanı eklensin.
- Tamamlananlar butonuna tıklandığında "tamamlandı" durumları true olanları listeden kaldırsın.

## Talimatlar

### Görev 1: Proje kurulumu

- Forklayın, klonlayın, ve `npm install`.
- Projeyi çalıştırmak için `npm run dev` komutunu kullanın.
- `http://localhost:3000` adresinden uygulamana ulaşabilirsin.

### Görev 2: Project Gereksinimleri

- **Tüm bileşenleri oluşturun. Dosyaları `frontend/components` klasöründe bulabilirsin.**
- **Stillere odaklanmana gerek yok. Bugün form yerine fonksiyonlara önem vermeni istiyoruz.**
- Yapılacaklar listende yeni bir todo eklemek için bir text input, bir gönder butonu, bir tamamlananları göster butonu bulunmalıdır.
- `<App />` proje için gerekli bütün dataları depolamalı.
  - Bütün uygulama verileri burada tutulmalı `<App />`.
  - Tüm `handler` fonksiyonları burada bulunmalı `<App />`.
- `<TodoList />` yapılacaklar dizisini alıp, listedeki elemanları yineleyerek `<Todo />` bileşeniyle tüm elemanlar için bir view oluşturacak.
- `<Todo />` `yapılacaklar` dizisinden elemanları alıp ekrana yazdıran bileşendir.
- `<Form />` bileşeni inputlarınızın barındığı bileşendir, bir text input, `Yapılacak Ekle` ve `Tamamlananları Kaldır` butonları.
  - Text inputunuz kullanıcının girdiği veriyi almalı ve `Enter` tuşuna basıldığında veya `Yapılacak Ekle` butonuna basıldığında listeye yeni girdiyi ekleyebilecek şekilde tasarlanmalıdır.
  - Yeni yapılacak elemanı eklendiğinde, re-render edilmeli ve eklenen eleman ekrana yazdırılmalıdır.
