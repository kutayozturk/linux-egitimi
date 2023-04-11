# Linux Disk Yönetimi ve Dosya Sistemi

Linux işletim sisteminde hem taşınır hem de sabit diskler /dev dizini altında bulunur. 

- Dosya Yönetimi; verilerin sabit ve harici depolama birimlerine nasıl saklanacağı, organize edileceği ve buna bağlı olarak nasıl erişileceğini tanımlar. Linux işletim sisteminde en çok kullanılan dosya sistemi ext2 ve onun geliştirilmiş versiyonu olan ext3'tür.

- Dizin Yapısı; farklı Linux dağıtımlarında kısmi farklılıklar göstermekle birlikte hemen hemen tüm Linux dağıtımlarında aşağıdaki şemaya benzer bir dizin yapısı mevcuttur.

![ldr](https://user-images.githubusercontent.com/94574681/230855991-f0c43b1a-ca78-4bdc-bd22-51af64ed1693.jpg)

***Şemada yer alan dizinlerden bazılarının görevlerini bir tabloyla özetleyebiliriz.***

![Dizin](https://user-images.githubusercontent.com/94574681/230856117-e3e927df-e7d1-484c-a4ee-6ab388d6be73.png)

## Kullanıcı İşlemleri ve Hakları

Linux işletim sisteminde birden çok ve farklı yetkilerde kullanıcılar oluşturulabilir. Bu kullanıcılar aynı anda veya farklı zamanlarda sisteme bağlanıp yetkileri çerçevesinde kendi işlemlerini yürütebilirler. Tüm kullanıcılar arasında hiçbir kısıtlamaya tabii olmayan tek kullanıcı root kullanıcısıdır. Çok kullanıcılı sistemlerde belirli kullanıcı politikaları oluşturmanın diğer bir yolu da grup kurmaktır. Dosya ve dizinleri yazma/okuma ve çalıştırma işlemleri grup bazında da yapılabilir.

Sistemde tanımlı her kullanıcı her dosyaya erişemez. Zira herkes her yere erişecekse farklı kullanıcılar oluşturmanın bir anlamı kalmaz. Linux bir dosyaya erişimi 3 sınıfa ayırır:
- Okuma hakkı
- Yazma hakkı
- Çalıştırma hakkı

Böyle bir sınıflandırma sayesinde kullanıcıların "ya hep ya hiç" yerine kısmi haklarla erişimine imkan sağlamış olunur.

 
## Kaynak Kodlarından Program Derleme ve Kurma    

Linux bize geniş bir çalışma alanı sunar ve bu alanda diğer programlama dillerinden de faydalanabilmemize olanak tanır. Linux ortamında çalışan bir çok program C ve C++ dillerinde yazılmaktadır. Ancak bu durum Linux kullanmak için bu dilleri bilmemiz gerektiği anlamına gelmez. Farklı programlama dillerinde yazılmış kodların sisteme ait merkezi işlemci tarafından anlaşılabilmesi için, onun anlayabileceği makine kodlarına çevrilmesi gerekir. Bu işi bizim için derleyiciler (compiler) yaparlar.

Linux ortamında kullanılan derleyicilerden biri GCC'dir. Başlangıçta sadece C dilinde yazılmış programları derlemek için tasarlanan GCC nin adı GNU C Compiler kelimesinden gelmektedir. Ancak zamanla C++, Foltran, Pascal, Java gibi dilleri de desteklemesiyle açık adı GNU Compiler Collection olarak değiştirilmiştir. Böylece GCC, Linux için standartlaşmış bir derleyici haline gelmiştir.

 
## Paket Yönetim Sistemleri

Paket, bir programın derlenmiş kodu olarak tanımlanabilir. Paket yönetim sistemi (PMS: Packet Management System) ise, paketlenmiş uygulamaları kurma, güncelleme ve kaldırma işlemlerini yönetir. Dolayısıyla her paket kendini yönetecek PMS'nin anlayacağı başlıklar taşır. Bu başlıklar sayesinde PMS, paketlerin güncellik bilgisi, diğer uygulamalara ve bileşenlere bağımlılığı gibi bilgileri denetler. PMS, uygulamaların kurulması, kaldırılması ve güncellenmesi işlemlerini ne kadar kolay ve başarılı yapabiliyor ise, o PMS kullanıcı açısından ciddi bir tercih nedeni olmaya başlar. 


## Yazılım Depoları (Software Repository/Repo)
İnternet ortamında birçok yazılım paketini üzerinde bulunduran yazılım depoları bulunmaktadır. Örneğin, YUM/APT gibi otomatik paket kuran ve güncelleyen programlari kendilerine tanımlı olan yazılım depolarına sırayla bakarak kullanıcının o an kurmak veya güncellemek istediği yazılımı arar. Ancak her zaman her türlü yazılımın burada olacağını beklemek mümkün değildir. 

Her Linux dağıtımının kendine has kullandığı bir PMS bulunur. Red Hat, Centos, Fedora RPM'i kullanırken Ubuntu, Knoppix DEB kullanır. Yerli işletim sistemimiz olan Pardus ise PiSi adlı paket yönetim sistemini kullanır. 

 
## Ağ Denetimi
 
Linux ağ dünyasında kendini kanıtlamış bir işletim sistemidir. Üzerinde birden fazla ağ arayüzü bulunan bir Linux makineyi bir yönlendirici (router) veya güvenlik duvarı (firewall) olarak yapılandırmak ve kullanmak mümkündür. Piyasadaki bir çok ticari yönlendirici ve güvenlik duvarlarında Linux işletim sisteminin kullanıldığını görmekteyiz. 

Linux; ATM, X.25, ISDN ve çevirmeli ağ bağlantı arayüzlerini desteklemekle birlikte, günümüzde tüm bu bağlantı tipleri önemini yitirmiştir. Öte yandan ethernet arayüzü, artık herkes tarafından desteklenen ve benimsenen standart bir ağ arayüzü haline gelmiştir. Linux içinde ağ denince, TCP/IP ağlarını; ağ bağlantı arayüzü denince ethernet kartını anlamalıyız.
