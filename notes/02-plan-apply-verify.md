# Bir işlemin tamamlandığını doğrulamak

[Notlar](README.md) · [Profil](../README.md)

Bir toplu çizim işleminde beş nesne seçildiğini düşünelim. Üç nesne için plan üretilebiliyor; iki nesnenin hedefi belirsiz. Bu senaryoda “beş nesne tamamlandı” demek hem planı hem belirsizliği yanlış anlatır.

## Durumları ayrı saymak

| Aşama | Bu sentetik örnekte bildiğim şey |
| --- | --- |
| Seçim | 5 nesne görev kapsamında |
| Plan | 3 uygulanabilir aday, 2 belirsiz aday |
| Yazma | Kaç adayın gerçekten işlendiği ayrıca okunmalı |
| Kayıt | Çıktı dosyasının oluştuğu ayrıca gözlenmeli |
| Yeniden açma | Beklenen değişiklik ve kapsam dışı nesneler kontrol edilmeli |

Üç plan üretilmiş olması, üç değişikliğin dosyada bulunduğunu kanıtlamaz. İşlemin yanıtı kaybolduysa aynı komutu tekrar göndermek de tek başına doğru bir kurtarma yöntemi değildir; ilk işlemin durumu bilinmiyor olabilir.

## Karşılaştırmayı önceden tarif etmek

Yazmadan önce kaynak revizyonunu, seçimi ve beklenen değişikliği belirlerim. Ayrı dosyaya kayıt sonrasında yalnız “dosya açıldı” kontrolüyle yetinmem: hedeflerin beklenen duruma gelip gelmediğini ve kapsam dışı nesnelerin korunup korunmadığını incelerim.

Sonuç raporu da bu ayrımı taşımalı: seçilen, planlanan, uygulanan, kaydedilen, doğrulanan ve çözülemeyen öğeler. Hangi adımda durduğum okunabilir olduğunda, bir sonraki işlem kalan işi doğru yerden devralabilir.

## English summary

A plan, an applied edit and a saved, reopened result are different states. Record the source revision and expected change before writing. Verify both the intended edits and preserved objects after reopening. An unknown response is a reason to inspect operation state before retrying.
