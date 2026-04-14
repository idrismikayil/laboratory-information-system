# LIS Middleware - Laboratoriya İnteqrasiya Sistemi: Sistem Təsviri və Prinsipləri

## 1. Sistemin Təyinatı və Əhatə Dairəsi
**LIS (Laboratory Information System) Middleware**, tibbi analizatorların rəqəmsal ekosistemə inteqrasiyasını təmin edən ixtisaslaşmış proqram təminatıdır. Sistemin əsas məqsədi analizatorlardan alınan xam məlumatların (raw data) avtomatlaşdırılmış şəkildə toplanması, validasiyası və mərkəzi verilənlər bazasına köçürülməsidir. Bu sistem laboratoriya daxili iş axınının rəqəmsallaşdırılması və məlumat bütövlüyünün (data integrity) təmin edilməsi məqsədi daşıyır

## 2. Funksional İmkanlar
Sistem aşağıdakı funksional istiqamətləri əhatə edir:
- **Məlumatların Avtomatlaşdırılmış Qəbulu:** ASTM tərəfindən müəyyən edilmiş beynəlxalq protokollar əsasında cihaz paketlərinin fiziki və məntiqi səviyyədə emalı.
- **Məxfilik və Məlumat Təhlükəsizliyi:** Tibbi məlumatların daxili korporativ standartlara və hüquqi tələblərə uyğun şəkildə qorunması.
- **Vahid Arxivləşdirmə:** Müxtəlif markalı və modelli cihazlardan (Hematoloji, Biokimyəvi və s.) daxil olan nəticələrin vahid struktura malik bazada saxlanılması.
- **Sinxronizasiya:** Emal olunmuş nəticələrin real-vaxt rejimində müvafiq kadrların (həkim və laborator personalların) istifadəçi interfeyslərinə ötürülməsi.

## 3. İstismar və İş Akışı (Operational Workflow)
Sistemin çalışma mexanizmi aşağıdakı ardıcıllıqla reallaşır:
1.  **Mənbə Səviyyəsi:** Analizator tərəfindən test prosesi tamamlanır və məlumatlar kommunikasiya kanalı vasitəsilə Host sistemə translyasiya edilir.
2.  **Emal Səviyyəsi (Middleware):** .NET əsaslı server servisi daxil olan ASTM/HL7 paketlərini analiz edir, sintaksis və məntiqi validasiyadan keçirir.
3.  **Yaddaş Səviyyəsi:** Təsdiq olunmuş məlumatlar PostgreSQL verilənlər bazasında müvafiq xəstə və sifariş (order) ID-ləri ilə əlaqələndirilir.
4.  **Təqdimat Səviyyəsi:** React əsaslı idarəetmə panelində nəticələr rəsmi hesabat formasına uyğun şəkildə əks etdirilir.

## 4. Strateji Üstünlüklər
- **Məhsuldarlığın Artırılması:** Məlumatların daxil edilməsi zamanı insan əməyinin minimuma endirilməsi və laboratoriya personalının peşəkar fəaliyyətinə köklənməsi.
- **Məlumat Dəqiqliyi:** Manual məlumat daxil etmə (data entry) zamanı yaranan texniki və insani xətaların eliminasiyası.
- **İdarəetmə və Nəzarət:** Laboratoriyanın iş yükünün və cihaz performansının mərkəzi monitorinq imkanı.

## 5. Yekun Qeyd
Bu sistem laboratoriya infrastrukturunun modernləşdirilməsi və beynəlxalq standartlara (ISO 15189 və s.) uyğunluğun təmin edilməsi üçün təməl infrastruktur rolunu oynayır.