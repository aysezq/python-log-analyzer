# log_analyzer.py

def analyze_log(file_path):
    """
    Belirtilen log dosyasını okur ve her satırı işler.
    """
    try:
        # 'with open' kullanmak, dosya işi bittiğinde otomatik kapatılmasını sağlar.
        with open(file_path, 'r') as file:
            print(f"[{file_path}] dosyası analiz ediliyor...")
            line_number = 0
            
            # Dosyayı satır satır okuma döngüsü
            for line in file:
                line_number += 1
                
                # Geçici olarak her satırı ekrana basalım (Test amaçlı)
                # print(f"Satır {line_number}: {line.strip()}")
                
                # --- BURAYA KRİTİK KELİME KONTROL KODUMUZ GELECEK ---
                
    except FileNotFoundError:
        print(f"HATA: {file_path} bulunamadı. Lütfen dosya yolunu kontrol edin.")

# Script'i çalıştırmak için ana kısım
if __name__ == "__main__":
    # Analiz edilecek örnek dosya yolu (Bu dosyayı depo içine ekleyeceğiz)
    LOG_FILE = "sample.log"
    analyze_log(LOG_FILE)
