# Laravel Log Analyzer

Bu Python script'i, Laravel log dosyalarını analiz eder ve çeşitli formatlarda raporlar oluşturur.

## Özellikler

- Laravel log dosyalarını okuma ve ayrıştırma
- Hata kayıtlarını JSON, Text, Excel veya PDF ( Yakında aktif olacak PDF) formatlarında raporlama
- İşlenen log dosyalarını isteğe bağlı olarak silme

## Gereksinimler

Script'i çalıştırmak için aşağıdaki Python kütüphanelerine ihtiyacınız vardır:

- openpyxl
- fpdf

Bu kütüphaneleri şu komutla yükleyebilirsiniz:

```
pip install openpyxl fpdf
```

## Kullanım

1. Log dosyalarınızı `errors` adlı bir klasöre yerleştirin. Bu klasör, script ile aynı dizinde olmalıdır.

2. Terminalde script'in bulunduğu dizine gidin ve aşağıdaki komutu çalıştırın:

   ```
   python main.py
   ```

3. Script çalıştığında, çıktı formatını seçmeniz istenecektir:
   - 1 : JSON
   - 2 : Text
   - 3 : Excel
   - 4 : PDF (Henüz tam olarak uygulanmamış)

4. Seçiminizi yapın ve Enter tuşuna basın.

5. Script, log dosyalarını işleyecek ve raporları `output` klasörüne kaydedecektir.

6. Her log dosyası için, dosyanın silinip silinmeyeceğini soran bir komut göreceksiniz:
   - 1 : Dosyayı sil
   - 2 : Dosyayı silme (varsayılan)

7. Seçiminizi yapın ve Enter tuşuna basın.

## Çıktı

Oluşturulan raporlar `output` klasöründe saklanacaktır. Her rapor, orijinal log dosyasının adını taşıyacak ve seçtiğiniz formata göre bir uzantıya sahip olacaktır (örneğin, `report_laravel.json`).

## Notlar

- Script, `.log` uzantılı tüm dosyaları işleyecektir.
- Hata durumunda, script hatayı gösterecek ve diğer dosyaları işlemeye devam edecektir.
- PDF çıktısı henüz tam olarak uygulanmamıştır.

## Hata Giderme

Eğer script çalışırken herhangi bir hata ile karşılaşırsanız, lütfen gerekli kütüphanelerin doğru şekilde yüklendiğinden emin olun ve log dosyalarınızın doğru formatta olduğunu kontrol edin.
