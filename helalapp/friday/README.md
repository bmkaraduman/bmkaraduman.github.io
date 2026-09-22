# Helal App — Cuma kartı arka planları

Uygulama `manifest.json`'ı çekip listeyi buradan alıyor. Yeni görsel eklemek için:

1. Görseli `.webp` (ya da `.jpg`) olarak bu klasöre koy. Kart 4:5 dikey
   (1080×1350); yatay görseller ortadan kırpılır. 1024–1600 px uzun kenar yeterli.
2. Küçük önizlemesini `thumbs/<id>.jpg` olarak koy (240 px genişlik):
   `sips -s format jpeg -s formatOptions 70 --resampleWidth 240 X.webp --out thumbs/X.jpg`
3. `manifest.json`'a bir satır ekle: `{"id": "...", "file": "...", "thumb": "thumbs/...", "free": false}`
4. Commit + push. Uygulama kataloğu günde bir tazeliyor; sıralama manifest sırası.

`"free": true` olanlar herkese açık, diğerleri Pro.
