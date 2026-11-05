# Teknik yaklaşımım

[Profile dön](README.md) · [Çalışma notları](notes/README.md)

İlgimi çeken işler, saha veya masa başındaki bir gereksinimin yazılım kuralına dönüştüğü noktada başlıyor. Bir çizgideki köşeyi düzenlemek, bir tablodan CAD nesnesi üretmek ve bir ajana sınırlı işlem yaptırmak farklı araçlar gerektiriyor. Üçünde de girdinin ne olduğunu, neyin değişeceğini ve sonucun nasıl inceleneceğini açık tutmak gerekiyor.

## Alan bilgisi ile geometriyi birleştirmek

Elektrik çiziminde yakın nesneler aynı devreye ait olmayabilir. Ölçü üretirken en yakın hedef, pafta açısından en iyi hedef olmayabilir. Bu yüzden koordinat hesabını; katman, cihaz, seçim ve çizim kuralıyla birlikte ele alıyorum.

AutoLISP CAD içindeki küçük ve doğrudan işleri; Python veri işleme, araç servisleri ve otomasyonu; C#/.NET masaüstü ve CAD entegrasyonlarını taşıyor. Rust da çekirdek ve geometri çalışmalarımda yer alıyor. Araç seçimini işin çalışacağı ortama göre yapıyorum.

## İşi uygulanabilir parçalara ayırmak

| Sorumluluk | Tasarımda aradığım açıklık |
| --- | --- |
| Girdi | Hangi dosya, revizyon ve nesneler üzerinde çalışılıyor? |
| Yorum | Kullanıcının isteği hangi somut işleme karşılık geliyor? |
| Plan | Değiştirilecek ve korunacak öğeler neler? |
| Uygulama | Yazma nerede başlıyor; başarısızlıkta ne oluyor? |
| Kontrol | Çıktıda beklenen değişikliği ve korunması gereken alanı nasıl gözlüyorum? |

Bu ayrım hem kullanıcı arayüzünü hem araç sözleşmesini sadeleştiriyor. Özellikle ajan araçlarında, önerilen işlem ile gerçekten uygulanmış işlem farklı durumlarda tutulmalı.

## AI'yı araç zincirine yerleştirmek

Serbest metin, belge yapısı ve görev yorumlama gibi alanlarda AI yararlı. Süre hesabı, nesne kimliği, geometri koşulu veya sayısal sınır kontrolü ise açık kurallarla incelenebilir kalmalı. Modelin önerisini gerçek kaynak ve işlem kapsamına bağlamakla ilgileniyorum.

## Yaratıcı işlerde insanın niyetini korumak

Sesin seviyesini veya spektrumunu ölçmek teknik bir gözlem sağlar. Bir vokalin nasıl hissettireceği ise kişinin istediği sonuca bağlıdır. Müzik araçlarında bu ikisini ayrı ele alıyorum: ölçüm uygulanacak işlemi destekler; yaratıcı tercihi insan tarif eder.

## Açık çalışmalar

[EE-CAD-Agents](https://github.com/moderntanri/EE-CAD-Agents) ürün yaklaşımını açık anlatan CAD çalışmam. [Çalışma notlarında](notes/README.md) ise geometri, işlem doğrulama ve AI araç tasarımını sentetik örneklerle açıyorum. Proje isimleri, müşteriye ait çizimler veya özel kaynak kodu bu sayfada paylaşılmıyor.
