# system-security-analysis
Düzce Üniversitesi Sistem Güvenliği dersi güvenlik analizi projesi.
# Sistem Güvenliği Analizi

Düzce Üniversitesi Sistem Güvenliği dersi kapsamında, kontrollü bir
ev ağı ortamında yaptığım güvenlik analizi projesi. Çalışmada hem
saldırgan hem savunmacı rolü üstlenildi.

## Yapılanlar
- Ping ve Nmap ile hedef sistemin erişilebilirliği ve açık portları belirlendi
- 135 (MSRPC), 139 (NetBIOS) ve 445 (SMB) portlarının açık olduğu tespit edildi
- Wireshark ile HTTP ve TLS trafiği karşılaştırıldı
- Bulgular risk seviyelerine göre değerlendirildi
- Windows Defender Güvenlik Duvarı'nda riskli portlar için engelleme kuralları oluşturuldu

## Kullanılan Araçlar
PowerShell, Nmap, Wireshark, curl, Windows Defender Güvenlik Duvarı

## Önemli Bulgular
- HTTP trafiği şifresiz olduğu için paket içeriği okunabiliyor, TLS trafiğinde okunamıyor
- Güvenlik duvarı ICMP yanıtlarını engelleyince Nmap hedefi "host down" gösterebiliyor (-Pn ile aşılabiliyor)

## Not
Tüm testler izinli ve kontrollü, eğitim amaçlı bir ağ ortamında yapılmıştır.

## Rapor
Detaylı rapor için: [Sistem_Guvenligi_Raporu.pdf](Sistem_Guvenligi_Raporu.pdf)
