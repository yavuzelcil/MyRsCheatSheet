MyRs Cheat Sheet (LaTeX)
========================

Bu proje, A4 üzerinde dikey olarak ikiye bölünmüş (iki sütun) küçük puntolu bir "cheat sheet" düzeni sağlar. Kod blokları sütunlar arasında bölünmez.

Hızlı Başlangıç
---------------
- Derlemek için `MyRsCheatSheet` klasöründe:
  - `make pdf` → `cheatsheet.pdf` üretir (iki sütun, tek sayfa düzeni).
  - `make pdf-2up` → `two-up.pdf` üretir (1. sayfa solda, 2. sayfa sağda görünecek şekilde 2-up düzeni).
- Sisteminizde `latexmk` yoksa `pdflatex` veya `tectonic` ile otomatik olarak derlenir.

Düzen Ayrıntıları
-----------------
- İki sütunlu A4 (`extarticle[8pt, a4paper, twocolumn]`).
- Dar kenar boşlukları ve küçük yazı boyutu (8pt) ile yoğun bilgi için optimize.
- `listings` yapılandırması ile kod bloklarında otomatik satır kırma (`breaklines=true`).
- `Code` ortamı (\`samepage\`) sayesinde kod örnekleri diğer sütuna/sonraki sayfaya bölünmez.

Nasıl Düzenlersiniz?
--------------------
- İçeriği `cheatsheet.tex` dosyasında doğrudan düzenleyin.
- Bölüm başlıkları ve listeler kısa ve yoğun olmalı (boşluklar azaltıldı).
- Kod örnekleri için:

```
\begin{Code}
// Kodunuzu buraya yazın
\end{Code}
```

Gerçek "Sol=Sayfa1, Sağ=Sayfa2" Görünümü
-----------------------------------------
- `two-up.pdf` dosyası, `cheatsheet.pdf` içeriğini sayfaları yan yana yerleştirerek (2-up) gösterir.
- Yazıcıda “yan yana iki sayfa” baskısı için uygundur (broşür benzeri görünüm).

Notlar
-----
- Türkçe heceleme ve karakterler için `babel[turkish]`, `inputenc[utf8]`, `fontenc[T1]` etkin.
- Eğer `listings` içinde Rust anahtar kelimeleri tanınmazsa, dosyadaki Rust dil tanımı devreye girer (taşınabilirlik için eklendi).

