# Hesap Makinesi Projesi (Motoko)

## Proje Hakkında
Bu proje **Motoko Playground IDE** kullanarak yapılan bir hesap makinesi projesidir. **Motoko** dili kullanılarak oluşturulmuştur. Çarpma, bölme, toplama ve çıkarma gibi temel matematik işlemlerini gerçekleştirir. Ek olarak **Temizle()** fonksiyonu ile sonuç değeri sıfırlanabilir.

## Proje Bağlantısı
Projeyi **Motoko Playground IDE** platformu üzerinden çevrimiçi olarak incelemek için bağlantıyı kullanabilirsiniz.

[Proje Bağlantısı](https://m7sm4-2iaaa-aaaab-qabra-cai.raw.ic0.app/?tag=3269391765)

## Kod Satırları  

```motoko
actor hesap_makinesi{
var hucre: Int = 0;
  
  // Toplama İşlemi Fonksiyonu
  public func toplama(s: Int) : async Int{
    hucre += s;
    hucre
  };

  // Çıkarma İşlemi Fonksiyonu
  public func cikarma(s: Int) : async Int{
    hucre -= s;
    hucre
  };

  // Çarpma İşlemi Fonksiyonu
  public func carpma(s: Int) : async Int{
    hucre *= s;
    hucre
  };

  // Bölme İşlemi Fonksiyonu
  public func bolme(s: Int) : async ?Int{
    if (s == 0) {
      null
    }else {
      hucre /= s;
      ?hucre
    };
  };

//Sonucu Sıfırlama
  public func temizle() : async () {
    hucre := 0;
  };
};
