# Hotel-Cancellations
# Gerekli kütüphaneyi yükle
library(readxl)

# Veriyi filtrele
h_filtered <- h %>%
  filter(arrival_date_month %in% c('April', 'May', 'June'),
         arrival_date_year == "2017",
         market_segment == "Online TA")

# Filtrelenmiş veriyi CSV dosyasına yaz
write.csv(h_filtered, file = "otel1.csv", row.names = FALSE)

# Benzersiz değerleri kontrol et
unique(h_filtered$market_segment)
unique(h_filtered$meal)
![image](https://github.com/arazgarayev/Hotel-Cancellations/assets/124186024/eb90a001-234f-4c24-924e-6742ffa52ada)

