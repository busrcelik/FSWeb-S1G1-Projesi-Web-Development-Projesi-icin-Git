# Araştırma Soruları

Artık yeni iş yerindeki ilk görevini gerçekleştirmek için hazırsın! Kullandığımız araçları biraz daha iyi anlama zamanı. Yapman istenilen şey, bu dokümanı güncelleyerek, aşağıdaki soruları soruları cevaplaman. Böylece Git yapısına biraz daha aşina olmaya başlayacaksın.

Soruları cevaplarken takıldığın yerlerde [GitHub docs](https://docs.github.com/en)'u kullanabilirsin. Docs, (ingilizce documentation'ın kısaltılmış halidir) bir programı veya dilin nasıl kullanılacağını anlatan dokümandır. Yazılım dünyasında sıkça kullanılır. Bir yazılımcı olarak _zamanınızın büyük çoğunluğu da bu tarz dokümanları okumakla ve üzerinde çalışmakla geçecek_.

![READ THE DOCS](https://github.com/Workintech/FSWeb-S1G1-Projesi-Web-Development-Projesi-icin-Git/blob/main/read-the-docs-wit.gif?raw=true)

Eğer aradığın soruların cevapları GitHub docs'ta yoksa, Google'lama becerileriniz size yardımcı olacak. Google'ı iyi kullanabilmek de aslında büyük bir dikkat ve çalışma gerektiriyor. Zamanla bu konuda da daha iyileştiğini göreceksin :)

## Sorular

1. Git nedir?

Git, yazılım geliştirme süreçlerinde kullanılan bir versiyon kontrol sistemidir. Projenin değişikliklerini izler, farklı versiyonları kaydeder, dallar oluşturmanıza ve değişiklikleri birleştirmenize olanak tanır. İşbirliği yapmayı ve projeleri etkili bir şekilde yönetmeyi sağlar. Git, açık kaynak yazılım geliştirmesinde yaygın olarak kullanılır ve çeşitli çevrimiçi platformlarla entegre edilebilir, örneğin GitHub, GitLab, ve Bitbucket gibi.

2. Git ile GitHub arasında ne fark var?

Git yerel versiyon kontrolünü sağlar, GitHub ise Git tabanlı projelerin çevrimiçi olarak yönetilmesi ve işbirliği yapılmasını sağlayan bir platformdur. GitHub, Git'in gücünü çevrimiçi bir ortamda işbirliği yapmak için kullanılabilir hale getirir.

3. Neden bir branch oluşturuyoruz?

Branch oluşturmak, Git'te aynı anda farklı özellikler veya değişiklikler üzerinde çalışmayı sağlayan bir yöntemdir. Bu, paralel geliştirme, risk yönetimi, işbirliği, versiyon yönetimi, hata düzeltme ve eş zamanlı çalışma gibi avantajlar sağlar. Her bir branch, bağımsız bir geliştirme yolunu temsil eder, ve daha sonra bu dallar birleştirilerek ana projeyi güncellenir. Bu, projenin düzenli ve etkili bir şekilde geliştirilmesine olanak tanır.

4. Pull Request'in amacı nedir?

Pull Request, bir geliştiricinin yaptığı değişiklikleri diğer ekip üyelerine önerdiği ve incelemelerini sağladığı bir mekanizmadır. Bu, kod kalitesini artırmak, hataları tespit etmek, işbirliği yapmak ve değişiklikleri güvenli bir şekilde ana projeye entegre etmek için kullanılır.

5. Bir Branchten diğerine geçmek için kullandığın KOMUT nedir? Mesela `isim-soyisim` branch'inde çalıştığını hayal et ve main branch'ine geçmek istiyorsun, ne yaparsın?

Branch'ten diğerine geçmek için Git'te kullanılan komut git checkout veya daha yeni versiyonlarda git switch komutlarıdır.

git checkout main
git switch main

6. `git fetch`, `git merge` ve `git pull` arasındaki farklıarı açıklayınız. Bu konutlar ne yapar açıklayınız.

git fetch:
Bu komut, uzak depodan (örneğin, GitHub) projenin güncel durumu hakkında bilgi alır, ancak yerel çalışma alanınızı değiştirmez.
Yereldeki branch'leri güncellemez, sadece uzak depodaki değişiklikleri görmek için kullanılır.
Güncelleme alırken, uzak depodaki branch'lerin bilgilerini alır, ancak yereldeki branch'leri güncellemez.
'git fetch origin'

git merge:
Bu komut, iki branch'ın veya commit'in birleştirilmesini sağlar.
Özellikle, yereldeki bir branch'teki değişiklikleri diğer bir branch ile birleştirmek için kullanılır.
Birleştirme işlemi otomatikleşebilir, ancak çakışmalar (conflicts) çıkabilir, bu durumda çözümleme işlemi gerekebilir.
'git merge isim-soyisim'

git pull:
Bu komut, git fetch ve git merge işlemlerini bir araya getirir. Yani, uzak depodaki değişiklikleri alır (git fetch) ve sonra yereldeki branch'i günceller (git merge).
Hızlı bir şekilde uzak depodaki güncellemeleri almak ve yereldeki çalışma alanını güncellemek için kullanılır.
'git pull origin main'

Kısaca, git fetch sadece bilgi alır, git merge iki branch'ı birleştirir, ve git pull ise uzak deponun güncel durumunu alarak yerel branch'i günceller.

7. Merge conflict nedir?

Merge conflict (birleştirme çakışması), Git'te iki farklı branch veya commit'in aynı satırlarda çelişen değişikliklere sahip olduğu durumu ifade eder. Bu durumda, Git otomatik olarak birleştirmeyi gerçekleştiremez çünkü hangi değişikliklerin korunması gerektiği belirsizdir. Geliştiricinin çakışmayı elle çözmesi ve ardından birleştirme işlemini tamamlaması gerekmektedir.

8. Merge conflict'i nasıl çözeriz?

1. Conflict'leri Belirleme:
   Git birleştirme işlemi sırasında bir conflict tespit ettiğinde, çakışan dosyaları işaretler.

1. Conflict'li Dosyaları Düzenleme:
   Çakışan dosyaları elle düzenleyerek, hangi değişikliklerin korunacağını belirle.

1. Conflict'in Çözüldüğünü Belirtme:
   Dosyaları düzenledikten sonra, çözümü işaretleyerek (mark as resolved) Git'e conflict'in çözüldüğünü bildir.

1. Commit Yapma:
   Conflict'leri çözdükten sonra, yeni bir commit yaparak birleştirme işlemini tamamla.

Bu adımlar, çakışan değişiklikleri açıklayarak ve düzenleyerek çözümlemenize yardımcı olur. Çözümü tamamladıktan sonra, projenizi güncel bir duruma getirmiş olursunuz.
