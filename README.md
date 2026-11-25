# Türkiye Konut Fiyatları ve Deprem Haritası

TCMB konut fiyat endeksi ve USGS deprem verisini bölge bazında birleştiren harita analizi.

## Ne yaptım?
- TCMB EVDS API'den 19 istatistiki bölgenin Konut Fiyat Endeksi verisini çektim
- USGS kataloğundan 2010-2026 arası M4.5+ depremleri indirdim (900 kayıt, 550'si Türkiye karasında)
- Depremleri il sınırlarıyla eşleştirip bölge bazında saydım (geopandas)
- Konut fiyatı ve depremleri etkileşimli haritada (folium) birleştirdim

## Öne çıkan bulgular
- Ekim 2026'da konut endeksi en yüksek bölgeler Doğu Anadolu (TRA, TRB), en düşük Akdeniz kıyısı
- Ocak 2023'ten bu yana nominal fiyat artışı en yüksek bölgeler: TRA (%317) ve TRB (%306)
- Deprem sayısı ile fiyat artışı arasındaki korelasyon 0,36 (19 bölge). İlişki zayıf, tek bir bölgeye (TRB) bağlı
- Sonuç: Deprem sayısı tek başına konut fiyat artışını açıklamıyor. Neden-sonuç iddiası yoktur

## Sınırlamalar
- Fiyat artışları nominaldir (enflasyondan arındırılmamıştır)
- Yalnızca 19 bölge var, istatistiksel güç düşük
- Bölgelerin bir kısmı birden fazla ili kapsıyor, il bazlı fiyat yok

## Kullanılan araçlar
Python, pandas, geopandas, folium, matplotlib

## Veri kaynakları
- TCMB EVDS (evds3.tcmb.gov.tr), Konut Fiyat Endeksi
- USGS Earthquake Catalog (earthquake.usgs.gov)
- İl sınırları: alpers/Turkey-Maps-GeoJSON

## Sonraki adımlar
- Streamlit ile canlı uygulama
- Reel fiyat analizi 
