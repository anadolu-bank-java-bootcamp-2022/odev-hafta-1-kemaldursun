# Decomposition

Decomposition tekniklerine genellikle böl ve yönet(divide and conquer) stratejileri denir. Buradaki ana fikir, tek bir problemi, onu oluşturan alt problemlere ayırarak(bölerek) yaklaşmak ve sonra her bir alt problemi ayrı ayrı çözmektir. Konuya göre bu süreç defalarca kez tekrarlanabilir.
Alt problemler yeni ve biricik bireysel problemler olarak da düşünülebilir ve strateji onları bölmek ve fethetmek(çözümlemek) için tekrarlanabilir.

Sorunu, senaryoyu ya da konuyu organize etmeyi sağlar, bunların ana hatları da bu sayede oluşturulmuş olur. 

Böl ve yönet stratejileri eski zamanlardan, en eski askeri stratejilerden beri kullanılmakta olup hem konuya hakimiyeti artırır hem de detayların ayrıştırılmasını sağlar. Aynı zamanda yazılım açısından algoritmaların daha sağlıklı geliştirilmesine olanak tanır.

Sınıfların, nesnelerin, metotların vb. ayrıştırılması ile daha sağlıklı kod yazılmasına ve kendisine yakın duran Single Responsibility(Tek Sorumluluk) prensibi gibi diğer patternlerle(örüntülerle) uyum içinde çalışılmasına kapı aralamış olur.

Decomposition Uygulama Teknikleri

Decomposition, genellikle <p><ins>anahatlarını çıkarma(outlining)</ins></p> olarak bilinen bir yazma tekniği olarak öğretilir. Yazılım geliştiriciler tarafından kullanılan bu tasarım tekniğine yukarıdan aşağıya tasarım denir. Üst düzeydeki tasarım, problemin birkaç talimattan oluşan bir algoritmaya ayrıştırılması, dönüştürülmesidir. 

<p><ins>Ardışık prototipleme</ins></p> ile tasarım ise, aşamalı olarak nihai bir çalışma programına yol açan bir dizi bireysel prototipten oluşur. Çoklu görev olarak da bilinen birden fazla yazılım parçasının aynı anda yürütülmesi fikri, yazılımın ayrıştırılmasını gerektirir.

Ancak özü, bir uygulamanın mimarisinin, onun parçalara (öğeler) ve bu parçalar arasındaki ilişkilere (ilişkilere) ayrıştırılmasıdır. Ayrışma birkaç nedenden dolayı önemlidir: İş ve bilgi paylaşımını kolaylaştırır. Muhtemelen uzmanlık bilgisine sahip birden fazla kişinin (veya birden çok ekibin) bir uygulama üzerinde birlikte verimli bir şekilde çalışmasını sağlar. Yazılım öğelerinin nasıl etkileşime girdiğini tanımlar. Uygulamanın özelliklerini belirleyen, parçalara ayrıştırma ve bu parçalar arasındaki ilişkilerdir.

<p><ins>4+1 Mimari görünüm modeli(architectural view model)</ins></p> ile de uygulanabilir. Bu modelin ana kalemleri alttaki gibidir.  
Mantıksal görünüm—Geliştiriciler tarafından oluşturulan yazılım öğeleridir. Nesne yönelimli dillerde bu öğeler sınıflar ve paketlerdir. Aralarındaki ilişkiler; kalıtım, dernekler ve bağımlılar dahil olmak üzere sınıflar ve paketler arasındaki ilişkilerdir.
Uygulama görünümü—Yapı sisteminin çıktısıdır. Bu görünüm, paketlenmiş kodu temsil eden modüllerden ve bir veya daha fazla modülden oluşan yürütülebilir veya konuşlandırılabilir birimler olan bileşenlerden oluşur. Örneğin Java'da bir modül bir JAR dosyasıdır ve bir bileşen tipik olarak bir WAR dosyası veya yürütülebilir bir JAR dosyasıdır. Aralarındaki ilişkiler, modüller arasındaki bağımlılık ilişkilerini ve bileşenler ve modüller arasındaki kompozisyon ilişkilerini içerir.
Süreç görünümü—Çalışma zamanındaki bileşenlerdir. Her öğe bir süreçtir ve süreçler arasındaki ilişkiler süreçler arası iletişimi temsil eder.
Dağıtım—Süreçlerin makinelerle nasıl eşleştirildiği ile ilgilenir. Bu görünümdeki öğeler (fiziksel veya sanal) makinelerden ve süreçlerden oluşur. Makineler arasındaki ilişkiler ağ oluşturmayı temsil eder. Bu görünüm aynı zamanda süreçler ve makineler arasındaki ilişkiyi de açıklar.
Senaryolar: Bir mimarinin tanımı, dört artı bir yani beşinci bir görünüm haline gelen küçük bir dizi kullanım senaryosu veya senaryosu kullanılarak gösterilmektedir. Senaryolar, nesneler ve süreçler arasındaki etkileşim dizilerini tanımlar. Mimari öğeleri tanımlamak ve mimari tasarımı örneklemek ve doğrulamak için kullanılırlar. Ayrıca bir mimari prototipin testleri için bir başlangıç noktası görevi görürler. Bu görünüm, kullanım durumu görünümü olarak da bilinir.

Kaynaklar:
Computationalthinking for the modern problem solver, Chapman & Hall Book, David D. Riley, Kenny A. Hunt  
Microservices Patterns, Manning, Chris Richardson
