# AI ile kurallı araçları birlikte kullanmak

[Notlar](README.md) · [Profil](../README.md)

“Seçtiğim nesneleri mevcut düzeni koruyarak bağla” isteğinde iki farklı iş var: kullanıcının neyi kastettiğini anlamak ve hangi nesnelere hangi işlemin uygulanabileceğini belirlemek.

Dil modeli ilk işi yorumlamaya yardımcı olabilir. İkinci iş gerçek nesne kimliklerini, seçim kapsamını, güncel revizyonu ve geometri koşullarını gerektirir. İyi yazılmış bir metin, bu verilerin yerine geçmez.

## Öneriyi uygulanabilir işleme çevirmek

| Alan | İşlemden önce netleşmesi gereken bilgi |
| --- | --- |
| Kaynak | Üzerinde çalışılan belge ve revizyon |
| Hedef | Gerçek nesne kimlikleri ve izin verilen seçim |
| Değişiklik | Desteklenen işlem ve açık parametreleri |
| Koruma | Değişmeyecek nesneler veya özellikler |
| Sonuç | İşlem kimliği, tamamlanma durumu ve kontrol bulguları |

Örneğin sentetik bir görevde yalnız `A` ve `B` nesnelerinin seçilmiş olması, modele `C` nesnesini düzenleme yetkisi vermez. Model daha geniş bir plan önerirse uygulayıcı kapsamı genişletmek yerine bu uyumsuzluğu bildirmelidir.

## Hangi katman neyi kararlaştırır?

Model, kullanıcının tarifini desteklenen araçlara eşleyen bir öneri oluşturabilir. Araç katmanı ise giriş biçimini, hedefleri ve işlem koşullarını denetler. Sayısal hesaplar ve geometri kontrolleri açık kodda tutulduğunda yanlış öneri incelenebilir bir noktada durdurulabilir.

MCP gibi araç arayüzleri bu ayrımı farklı istemcilere taşımak için kullanışlıdır. Aracın bulunması, her görevi doğru tamamlayabileceği anlamına gelmez; yetenek ve kapsam her görevde güncel tutulmalıdır.

## English summary

Use models to interpret intent and propose supported actions. Bind every action to the actual document revision, object identities and permitted scope. The execution layer checks targets, parameters and conditions. A model proposal does not expand its authority over the source.
