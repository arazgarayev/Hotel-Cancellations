# Hotel-Cancellations
Gerekli kütüphaneyi yükluyoruz

attach(h)

library(readxl)

 Veriyi filtrelemek gerekli burada
unique(h_filtered$arrival_date_month)
unique(h_filtered$meal)
h_filtered <- h %>%
  filter(arrival_date_month %in% c('April', 'May', 'June'),
         arrival_date_year == "2017",
         market_segment == "Online TA")

değerleri kontrol et
unique(h_filtered$market_segment)
unique(h_filtered$meal)
Filtrelenmiş veriyi CSV dosyasına yaziyoruz
write.csv(h_filtered, file = "otel1.csv")
![image](https://github.com/arazgarayev/Hotel-Cancellations/assets/124186024/eb90a001-234f-4c24-924e-6742ffa52ada)

