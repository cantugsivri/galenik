# Galenik – EMP Cihazı Eczaneleri

FAGRON LAB. PRO&EMP Homojenizatör cihazı bulunan eczanelerin il → ilçe → mahalle
sırasıyla listelendiği, mobil uyumlu tek sayfalık uygulama.

- Tek dosya: `index.html` (dış script, sunucu, veritabanı veya form yok).
- Eczane verisi sayfanın içine gömülüdür; listeyi güncellemek için `index.html`
  dosyasındaki `DATA` dizisi değiştirilir.
- QR kodu `https://galenik.vercel.app/` adresine yönlendirir.
- **Önemli:** `index.html` içindeki `<meta http-equiv="Content-Security-Policy">`
  etiketi script'i `sha256-...` hash'iyle sınırlar. `<script>` içeriği (örneğin
  `DATA`) her değiştiğinde bu hash de yeniden hesaplanıp güncellenmelidir; aksi
  halde tarayıcı script'i engeller ve sayfada il listesi görünmez.
