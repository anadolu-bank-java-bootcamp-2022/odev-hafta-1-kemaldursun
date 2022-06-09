# Liskov Prensibi

Bu ilke, bir üst sınıfın nesnelerinin, uygulamayı bozmadan alt sınıflarının nesneleri ile değiştirilebileceğini tanımlar. Yani alt sınıfların nesnelerinin, üst sınıfın nesneleri gibi davranmasını gerektirir. Liskov prensibini, B. Meyer tarafından tanımlanan sözleşmeye göre tasarım(design by contract) konseptine oldukça benzeyen birkaç kuralı takip ederek başarabilirsiniz. Sözleşme bir anlaşmadır. Design by contract'ın ana fikri, bir yazılım sisteminin öğelerinin karşılıklı yükümlülükler ve faydalar temelinde birbirleriyle nasıl işbirliği yaptığına dairdir. Liskov prensibi “sözleşmeye göre tasarımla” yakın planda yer alır. Çünkü kendisi de hiyerarişide uyumlu bir anlaşmalar silsilesini vurgular ve ister.

Liskov prensibi ilk ağızdan: “S, T'nin bir alt türüyse, programı bozmadan T türündeki nesneler S türündeki nesnelerle değiştirilebilir” ya da “Alt türler, temel türleri için davranışsal olarak ikame edilebilir olmalıdır” şeklinde tanımlanmıştır.

Alt sınıfın override edilmiş bir metotu, üst sınıfın metoduyla aynı giriş parametre değerlerini kabul etmelidir. Bunun anlamı daha az kısıtlayıcı doğrulama kuralları uygulayabilirsiniz, ancak alt sınıfınızda daha katı kuralları zorlayamazsınız. Aksi takdirde, üst sınıfın bir nesnesi üzerinde bu yöntemi çağıran herhangi bir kod, alt sınıfın bir nesnesiyle çağrılırsa bir hataya(exception) neden olabilir. Yani birbirinin yerine geçmede problem yaratır bu da bahse konu prensibe aykırıdır.

Benzer kurallar, metodun dönüş değeri için de geçerlidir. Alt sınıfın bir metodunun dönüş değerinin, üst sınıfın metodunun dönüş değeriyle aynı kurallara uymasını gerektirir. 

<ins>Yararları</ins>

LSP izlenirse, alt sınıflar sınıflardaki öğeler yani istemciler sınıf hiyerarşisindeki değişikliklerden habersiz kalabilir. Daha rahat kod yazılmasını sağlar. Arayüzde herhangi bir değişiklik olmadığı sürece, mevcut herhangi bir kodu değiştirmek için hiçbir sebep olmamalıdır. Bu nedenle LSP, hem open/close(açık/kapalı) ilkesinin hem de single responsibility(tek sorumluluk) ilkesinin uygulanmasına yardımcı olur.  

SOLID’in ortasında yer alan bu örüntü, bize iyi kalıtım hiyerarşilerini karakterize etmenin bir yolunu verir. Açık-kapalı ilkesine uymayan hiyerarşiler oluşturmamıza neden olacak tuzaklar hakkında farkındalığımızı artırır.

Kaynaklar:  
https://stackify.com/solid-design-liskov-substitution-principle/  
Adaptive Code Via C#, Agile coding with design patterns and SOLID prenciples, Microsoft, Gary Mclean Hall
