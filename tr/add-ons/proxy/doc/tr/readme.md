# NVDA için proxy desteği

* Yazar: José Manuel Delicado
* NVDA uyumluluğu: 2021.3 ve sonrası
* [Kararlı sürümü indirin][1]

Bu eklenti, NVDA ekran okuyucusunun bir veya daha fazla proxy sunucusu aracılığıyla İnternet'e bağlanmasına olanak tanır. Bunu mümkün kılmak için, standart Python kitaplığına çeşitli yamalar uygular veya seçilen konfigürasyona bağlı olarak belirli ortam değişkenlerini değiştirir. NVDA'yı ve eklentilerini kurumsal ortamınızdan otomatik olarak güncelleyebilecek ve hatta kuruluş proxy sunucunuzun izin vermesi koşuluyla uzak oturumlar gerçekleştirebileceksiniz.  

## Özellikler:

* Çeşitli proxy sunucu türleri için destek: http, socks4 ve socks5.
* Tüm trafiği proxy sunucusu veya yalnızca belirli trafik (http, https, ftp) üzerinden yeniden yönlendirme yeteneği.
* Tüm trafiği bir proxy sunucusu üzerinden yeniden yönlendirme ve ardından belirli trafiği diğer sunucular (iç içe geçmiş proxy'ler) üzerinden yeniden yönlendirme yeteneği.
* Profil değiştirme ve yapılandırma sıfırlama farkında: genellikle NVDA'nın taşınabilir bir kopyasıyla çalışıyorsanız, farklı ortamlar (ev, iş, ofis1, ofis2) için çeşitli profiller oluşturabilir ve bunları manuel olarak etkinleştirebilirsiniz.

## kullanım:

Bu eklenti, NVDA ayarları iletişim kutusuna "Proxy" adlı yeni bir kategori ekler. Bu kategoride dört ayar grubu bulacaksınız. İlki, tüm trafik için genel bir proxy yapılandırmanıza izin verir. Diğer gruplar, proxy sunucularını yalnızca belirli protokoller için yapılandırmanıza izin verir. Tüm gruplar aşağıdaki alanlara sahiptir:

* Ana bilgisayar: proxy sunucusunun ana bilgisayar adı veya ip adresi. Söz konusu proxy'yi devre dışı bırakmak için boş bırakın.
* Bağlantı noktası: sunucu bağlantı noktası.
* Kullanıcı adı: isteğe bağlı. Sunucu yetkilendirmesi için kullanıcı adı.
* Şifre: isteğe bağlı. Sunucu yetkilendirmesi için parola. Soock4 sunucuları için şifre gerekmediğini unutmayın.

Önceki alanlara ek olarak, ilk ayarlar grubunda aşağıdaki seçenekler mevcuttur:

* SOCKS proxy tipi: socks4, socks5 veya http seçilebilir.
* Mümkünse dns istekleri için proxy kullanın: Bu onay kutusu işaretlendiğinde, ana bilgisayar adları veya alan adları doğrudan proxy sunucusuna gönderilir ve burada çözümlenir. İşareti kaldırıldığında, isimler yerel olarak çözülecek ve sunucu sadece hedef ip adresini alacaktır. Tüm stock4 proxy sunucularının bu seçeneği desteklemediğini unutmayın.

Tipik olarak, çoğu kullanıcının yalnızca ilk ayar grubunu yapılandırması gerekir. Proxy ayrıntılarınızı bilmiyorsanız, daha fazla bilgi için kuruluşunuzdaki ağ yöneticinize danışın.

## sınırlamalar:

* Çok sınırlı IPV6 desteği.
* UDP trafiği tüm proxy sunucularında desteklenmez.
* Harici DLL kitaplıkları bu eklentide yapılandırılan ayarlara uymaz.
* http proxy sunucuları için yalnızca temel yetkilendirme desteklenir. Özet yetkilendirme desteklenmiyor.
* Tüm trafiği (https bağlantıları dahil) bir http proxy üzerinden yeniden yönlendirmek için sunucunun http bağlantı yöntemini desteklemesi gerekir.
* Bir "doğrudan bağlantı" modu yapılandırılamaz. Belirli bir proxy'yi devre dışı bırakırsanız, bunun yerine sistem varsayılanı kullanılır.

## değişiklik günlüğü

### Sürüm 1.1

* NVDA 2022.1 ile uyumludur.
* Güvenlik nedeniyle minimum NVDA sürümü 2021.3 olarak ayarlanmıştır.
* Patch socket.getaddrinfo işlevi, "Mümkünse dns istekleri için proxy kullan" onay kutusu işaretlendiğinde ve genel bir proxy yapılandırıldığında.
* Çeviriler güncellendi.

### Sürüm 1.0

* İlk sürüm.

[[!tag dev stable]]

[1]: https://addons.nvda-project.org/files/get.php?file=nvdaproxy
