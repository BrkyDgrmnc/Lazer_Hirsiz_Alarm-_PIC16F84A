05/2/2016 

LAZER IŞIK KONTROLLÜ ALARM DEVRESİ NEDİR ?

Lazer ışık kontrollü alarm devresi üzerindeki 3 ayrı LDR sayesinde 3 ayrı odanın güvenlik kontrolünü sağlayan sistemdir. Alarm devresi aktif hale geldikten sonra lazer ışığının önünden geçilirse hem görsel hem de ses olarak alarm verir. Alarm  (eğer lazer ışığının önünde engel yoksa) yaklaşık 4sn çalmaya devam eder, 4sn sonra alarm kapanır.

ÇALIŞMA PRENSİBİ:

PİC 16F84A mikro denetleyicisine yazılmış kod sayesinde devre çalışır. Devrede 3 adet ışığa göre direnci değişen direnç (LDR) kullanılmıştır. Bu elemanın üzerine ışık düşürüldüğünde doğru orantılı olarak direncide düşer, karanlık ortamda ise direnci artar. Devrede mikro -denetleyiciye “0” sinyali gidince çalışması istendiği için pull-down direnç kullanılmıştır. LDR’ler pull-down dirençleri ile birlikte mikrodenetleyicinin “a” portuna bağlanmıştır, bu sayede lazer ışını LDR’nin üzerine düşürüldüğünde mikrodenetleyiciye “1” sinyali gidecek, LDR üzerinde ışık olmadığında ise mikrodenetleyiciye “0” sinyali giderek içinde yazılmış olan programla B0.0 portundaki buzzer’i çalıştıracak ve B0.1 B0.2 B0.3 portlarındaki ilgili led’i yakacaktır. Birinci LDR birinci led’i, ikinci LDR ikinci led'i, üçüncü LDR üçüncü led’i yakar. LDR’lerin önünden engel çekildikten 4sn sonra alarm durur, önüne tekrar engel geçince alarm çalmaya başlar.

![devre şeması](https://user-images.githubusercontent.com/57718277/151841806-027b05d9-8785-45e5-98e5-0c4268736b29.PNG)
  
![3d](https://user-images.githubusercontent.com/57718277/151841708-78c23627-ce76-474d-a4dd-5199df396c8b.PNG)
