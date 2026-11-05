# Kesişim ile bağlantı arasındaki fark

[Notlar](README.md) · [Profil](../README.md)

Bir yatay çizgi `(0, 0)` ile `(10, 0)` arasında; bir dikey çizgi de `(5, -5)` ile `(5, 5)` arasında uzansın. İkisi `(5, 0)` noktasında kesişir. Bu, geometrik bir gözlemdir.

Aynı şekil elektrik çiziminde farklı anlamlar taşıyabilir: iki hattın bağlantısı, bağlantısız bir geçiş veya farklı sistemlere ait üst üste çizilmiş nesneler. Koordinat hesabı bunlardan hangisinin doğru olduğunu tek başına söylemez.

## Eksik bilgiyi görünür tutmak

| Gözlenen bilgi | Söyleyebileceğim şey |
| --- | --- |
| Segmentlerin ortak noktası var | Geometrik kesişim var |
| Devre kimlikleri farklı | Bunları birleştirmek devre kimliğini değiştirir |
| Uç/port rolleri ve çizim kuralı biliniyor | Bağlantı adayı alan kurallarıyla incelenebilir |
| Bağlantı anlamı belirlenemiyor | Adayı belirsiz bırakıp ek bilgi istemek gerekir |

Mesafe toleransını büyütmek eksik devre kimliğini sağlamaz. Daha çok geometriyi “yakın” kabul etmiş olurum. Bu yüzden tolerans, bağlantı anlamının yerine kullanılmamalı.

## İşlem tasarımına etkisi

Önce geometri adaylarını toplarım. Sonra seçim kapsamını, sistem/devre bilgisini ve nesnenin bağlantı rolünü kontrol ederim. Alan bilgisi yetmeyen adayı ayrı raporlarım. Böylece algoritmanın bulduğu her yakınlık otomatik olarak çizim değişikliğine dönüşmez.

Bu yaklaşımın ürün bağlamı, [EE-CAD-Agents iş akışında](https://github.com/moderntanri/EE-CAD-Agents/blob/main/docs/WORKFLOWS.md) anlatılan seçim, planlama ve istisna raporlamayla ilişkilidir.

## English summary

Two segments can intersect without representing an electrical connection. Geometry identifies candidates; circuit identity, terminal roles and drawing conventions determine whether a connection is meaningful. Increasing a distance tolerance cannot replace missing semantic information. Ambiguous candidates should remain explicit.
