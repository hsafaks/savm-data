# savm-data

Savm uygulamasının internetten okuduğu herkese açık veriler. Gizli bilgi içermez.

## fitre.json

Kişi başı fitre (aynı zamanda günlük fidye) tutarı. Uygulama bu dosyayı yaklaşık 7 günde bir ve "Güncel tutarı al" düğmesiyle okur.

Her yıl Diyanet İşleri Başkanlığı Din İşleri Yüksek Kurulu yeni tutarı açıkladığında (genellikle Ocak, https://kurul.diyanet.gov.tr):

1. `fitre.json` dosyasını düzenleyin:
   - `year`: tutarın geçerli olduğu Ramazan yılı (ör. 2027)
   - `fitre`: kişi başı tutar, TL (50–5000 arası olmalı)
   - `source`: kararın kaynağı ve tarihi (ör. "Din İşleri Yüksek Kurulu 08.01.2027")
   - `updated`: karar tarihi, YYYY-AA-GG
2. Kaydedip ana dala (main) gönderin. Uygulamalar en geç bir hafta içinde yeni tutarı görür.

Elle tutar girmiş kullanıcıların değeri kendiliğinden değişmez; uygulama onlara yeni tutarı kullanmak isteyip istemediklerini sorar.