
- ### JVM nedir? Ne işe yarar?
  JVM, yani Java Virtual Machine java kodlarının herhangi bir platforma bağlı kalmadan çalışmasını sağlar. Windows, MacOS, Linux gibi Farklı platformlarda aynı kodun, aynı şekilde çalışmasını sağlayan sistemdir.
  - ### JVM Nasıl Çalışır
    JVM yazılan java kodunu "bytecode" denilen bir ara dilin kodlarına çevirir ve bu şekilde her platformda çalıştırılabilir bir hale getirir. Sonrasında ise istenildiği zaman çalıştırılır.

    ![](images/java-derleme-sureci.png)

***

- ### JDK nedir? Ne işe yarar?
  
  Java Development Kit java üzerinde bir proje geliştirirken ihtiyacımız olan kütüphanelerin genelini barındıran pakettir. Java ile yapacağımız projelerde kolaylık sağlar.

***
- ### Garbage Collector nedir? Nasıl Çalışır?
  Garbage collector java dilinde bir nesnenin işi bittiğinde bellekte ona ayrılan yeri boşaltmak için kullanılan araçtır. Garbage collector kod çalıştırıldığında kodu takip ederek bellekte yer işgal eden nesneleri belirler ve onları yok eder.
***
- ### ".jar" Formatı Nedir?
  Açılımı "Java ARchive" olan bu dosya formatı ".zip" dosya sistemiyle aynı şekilde çalışır. Java ile hazırlanmış uygulamaların ve projelerin bileşenlerini saklayan arşivdir.
***
- ### ".java" ile ".class" Arasındaki Fark Nedir?
  - ".java" java dili ile yazdığımız kodun bulunduğu dosya türüdür.
  - ".class" java ile yazdığımız kodu derlediğimizde JVM ile birlikte "bytecode" formatına dönüştürdüğümüz kodu saklar.
***
- ### Abstract Class Nedir?
  Abstract class, kod yazarken tekrar tekrar yazmamız gereken nesne tanımlamalarını tek bir yerde yapmamızı  sağlayan classlardır. Genel olarak nesneler için bir şablon özelliği görür. Kodları sonrasında tekrar yazmak yerine tek bir kaynaktan alırız ve bu kod tekrarına düşmemizi engeller. İçerisinde somut bir nesne oluşturulamaz. Extends ederek farklı sınıflarda kullanabiliriz. Her extends ettiğimiz sınıfta, soyut sınıfların özellikleri kullanılarak farklı sonuçlar üretilir.

  #### Bir örnekte inceleyelim:  



  ```java

      abstract class Araba
    {
        public string Marka { get; set; }
        public int VitesSayisi { get; set; }
        // Oluşturacağımız bir araba classına dair özellikleri tanımlıyoruz

        public abstract void MaximumHiz();
        // Override edilecek methodumuz. Sonrasında override edeceğimiz zaman değiştirebilicez
    }

    
    /// Ferrari'yi Araba sınıfımızdan inherit alıyoruz.
    class Ferrari : Araba
    {
        /// Maximum hız bilgimizi override ediyoruz ve Araba abstract sınıfımızın sahip olduğu tüm özelliklere sahip oluyor.

        public override void MaximumHiz()
        {
            Console.WriteLine("Ferrari'nin maximum hızı: 300");
        }
    }

  ```
 
