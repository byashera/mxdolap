<div align="center">

# 📦 MX IT Dolap & Envanter Yönetim Sistemi (v4.0)

**IT Donanım, Sarf Malzeme, Arka Depo, Barkod Okuyucu ve Personel Zimmet Otomasyonu**

[![Son Sürüm](https://img.shields.io/badge/S%C3%BCr%C3%BCm-v4.0-2563EB?style=for-the-badge&logo=windows&logoColor=white)](https://github.com/byashera/mxdolap/releases/latest)
[![Mimari](https://img.shields.io/badge/Mimari-Tek%20Dosya%20(.EXE)-10B981?style=for-the-badge&logo=python&logoColor=white)](https://github.com/byashera/mxdolap/releases/latest)
[![Veritabanı](https://img.shields.io/badge/Veritaban%C4%B1-SQLite3%20%2B%20Flask%20LAN-0EA5E9?style=for-the-badge&logo=sqlite&logoColor=white)](https://github.com/byashera/mxdolap)
[![İmza](https://img.shields.io/badge/Dijital%20%C4%B0mza-SHA256%20Verified-7C3AED?style=for-the-badge&logo=letsencrypt&logoColor=white)](https://github.com/byashera/mxdolap/releases/latest)

<br />

[**📥 Son Sürümü İndir (v4.0 .EXE)**](https://github.com/byashera/mxdolap/releases/latest) • [**🚀 Sürüm Notları**](https://github.com/byashera/mxdolap/releases) • [**🐞 Sorun Bildir**](https://github.com/byashera/mxdolap/issues)

</div>

---

## 🎯 Ne Amaçla Kullanılabilir?

> **MX IT Dolap Yönetimi**, bilgi işlem (IT) departmanlarındaki dolap ve arka depolarda bulunan donanım ile sarf malzemelerin stok kontrolünü sizin yerinize otomatik olarak yapar. Barkod okuyucu desteğiyle ürün giriş-çıkışlarını ve personel zimmetlerini anlık takip eder; hangi ürünlerin kritik stok seviyesine düştüğünü veya hangi departman/personel tarafından daha çok talep edildiğini analiz ederek tek tıkla renkli **Excel (`.xlsx`)** raporu sunar.

---

## ✨ Öne Çıkan Özellikler (v4.0)

| Özellik | Açıklama |
| :--- | :--- |
| ⚡ **Akıllı Barkod Motoru** | Barkod tabancasıyla okutulan ürünleri milisaniyeler içinde yakalar. **1. Barkod** ve **2. Alternatif Barkod** desteğiyle aynı ürünü farklı kutu barkodlarıyla tanır. |
| 🔄 **Giriş (+1) & Çıkış (-1) Modu** | Dolap kapağına yapıştırılan özel **`REMOVE_MODE_999`** barkodu okutulduğunda ekrana dokunmadan **Çıkış Moduna** geçer, stoktan düşer ve otomatik zimmet kaydı açar. |
| 🏢 **Ana Dolap & Arka Depo** | Aktif kullanımdaki malzemeleri **DOLAP**, yedek kolileri ise **DEPO (Arka)** rozetleriyle ayrı sekmelerde ve KPI kartlarında takip eder. |
| 📋 **Personel Zimmet & Talep** | Stoktan düşülen her malzemenin hangi departmana, hangi personele ve hangi IT çalışanı tarafından teslim edildiğini kayıt altına alır. |
| 🌐 **Yerel Ağ (LAN) Web Paneli** | Dahili Flask sunucusu sayesinde aynı ağdaki diğer bilgisayarlardan veya mobil cihazlardan tarayıcı üzerinden envantere ve zimmet ekranına erişim sağlar. |
| 📥 **3 Adımlı Veri İçeri Aktarma** | Standart Excel listelerini, `IT_Dolap_Stok_Raporu.xlsx` raporlarını, JSON yedeklerini ve eski `.db` dosyalarını çakışma çözümüyle (Üzerine Ekle / Yaz / Atla) içeri aktarır. |
| 🔔 **Otomatik Güncelleme (OTA)** | Uygulama açılışında ve ayarlar menüsünde GitHub üzerinden yeni sürüm kontrolü yapar; veritabanını koruyarak tek tıkla kendini günceller. |

---

## 💻 Gereksinimler & Kurulum

* **Ek Program Gerektirmez:** Bilgisayarınızda Python veya herhangi bir ek kütüphane yüklü olmasına ihtiyaç duymaz.
* **Tek Dosya (`IT_Dolap_Yonetimi.exe`) Mimarisi:** Yan klasörlere ihtiyaç duymadan **Tıkla-Çalıştır** olarak görev yapar. Veritabanını (`veri_tabani.db`) ve ayarlarını bulunduğu klasörde otomatik oluşturur.

> 🛡️ **Windows Güvenlik & Dijital İmza Bilgisi:**
> Uygulama **SHA256 Dijital Sertifika** ile imzalanmıştır. İlk kez çalıştırılan bilgisayarlarda Windows SmartScreen uyarısı görürseniz **"Ek Bilgi -> Yine de Çalıştır"** seçeneğine tıklayabilir veya Releases sayfasındaki `.cer` sertifikasını **Güvenilen Kök Sertifika Yetkilileri** deposuna yükleyebilirsiniz.

---

## 🏷️ Özel Barkod Kısayolu (`REMOVE_MODE_999`)

Dolap kapağına aşağıdaki barkod kodunu etiket olarak yapıştırarak, klavye veya fareye dokunmadan yalnızca barkod okuyucu tabanca ile **Stok Çıkışı (-1)** yapabilirsiniz:

```text
Barkod Kodu       : REMOVE_MODE_999
TR-Q Okuyucu Kodu : REMOVE?MODE?999

1 - Barkod tabancasıyla REMOVE_MODE_999 kodunu okutun (Uygulama Çıkış Moduna geçer).
2 - Ardından dolaptan aldığınız ürünün barkodunu okutun (Stoktan 1 adet düşülür ve Bekleyen Zimmet kaydı açılır).

```


🖼️ Uygulama Ekran Görüntüleri(Eski Yenilenecek)
1. İlk Kurulum Sihirbazı

<img width="420" alt="Kurulum Sihirbazı" src="https://github.com/user-attachments/assets/fdae5a1e-84f1-4fa2-86e0-9393534526c7" />

2. Masaüstü Uygulama Ana Ekranı
<img width="900" alt="Uygulama Ana Ekranı" src="https://github.com/user-attachments/assets/35d02213-4ef4-4cba-b95d-68ad6bd3c693" />

3. Yerel Ağ (LAN) Web Paneli (Farklı Bilgisayar / Mobil Erişim)
<img width="900" alt="Web Paneli" src="https://github.com/user-attachments/assets/715cc44b-658d-43d8-9008-434d5bd08568" />

4. Masaüstü ve Web Senkronize İşlem Logları
<img width="900" alt="İşlem Logları" src="https://github.com/user-attachments/assets/aa75f053-c7a8-4298-84db-7733fad0c443" />

5. Sistem Ayarları, IP/Port Yönetimi ve OTA Güncelleme
<img width="900" alt="Sistem Ayarları" src="https://github.com/user-attachments/assets/a3e3b02b-9789-4ae9-8fe8-bd7e54ed5257" />

6. Otomatik Renkli Excel (.xlsx) Stok ve Popüler Ürün Raporu
<img width="900" alt="Excel Raporu" src="https://github.com/user-attachments/assets/d4340d2e-f74a-4b19-84a9-01056a9eaa1e" />


<div align="center">
IT Sistem & Otomasyon Ekibi • MX IT Dolap Yönetimi v4.0
</div>
