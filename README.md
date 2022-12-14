<h1> KÜMELEME ALGORİTMASI </h1>
  <u1>
  <li>Veri kümesindeki elemanların yakınlık, uzaklık ve benzerlik gibi ölçütlere göre analiz edilerek kendi arasında gruplandırmaya kümeleme denir.</li>
  <li>Temelde veriler kendi aralarındaki benzerlik ve farklılıklar analiz edilerek gruplandırılır.</li>
  <li>Kümeleme algoritmalarında kaç küme oluşması gerektiğine kullanıcı veya algoritma karar verir. Küme sayısı ile ayrıntı düzeyi belirlenir.</li>
  <br /><br />
  
  ![image](https://user-images.githubusercontent.com/56221025/207609850-0a5bf27a-adcd-4505-84dd-74a07915a78b.png)


  
  </u1>
  <h2>Kümeleme Algoritması Kullanım Alanları</h2>
  <h3>1-)Müşteri Segmentasyonu</h3>
  <li>Müşterilerin verileri ön tanımsız olarak makineye  verilir. Makine ortak özelliklere göre sınıflandırma yapar. Müşterilerin geçmiş verilerine bakılarak veya kendisine benzer kişilerin davranışlarına bakılarak ürün tavsiye edilir. Kişilere özel kampanyalar yapılır.</li><br /><br />
  
  ![image](https://user-images.githubusercontent.com/56221025/207609651-0b088c7c-e921-4b2e-8913-fdd7579aecdd.png)



  
  <h3>2-)Pazar Segmentasyonu</h3>
  <li>Pazar araştırması kapsamında yaş grupları, kazanç dilimleri, kentsel, kırsal veya banliyö konumu gibi kategorileri belirlemek için kullanılabilir.  Pazarlamada, farklı müşteri gruplarının en alakalı mesajlarla hedeflenebilmesinde küme analizi kullanılır. Satın alma kalıplarına göre müşteri gruplarını karakterize edilir.</li><br /><br />
  
  ![image](https://user-images.githubusercontent.com/56221025/207609158-417ad080-71a0-4e5f-97d7-a8e126551ed2.png)


  
  <h3>3-)Sağlıkta Kümeleme</h3>
  <li>Özellikle görüntü işlemede kümele çok kullanılır. Makine görüntüyü alıp analiz eder ve ardından kümele yapar.</li><br />
  
  ![image](https://user-images.githubusercontent.com/56221025/207609330-3a157428-463b-4dca-899c-d024e1dbf1d7.png)
  
  <h2>K-Means Kümeleme Algoritması</h2>
  <li>K-Means kümeleme algoritması yinelemeli bir kümeleme algoritmasıdır.</li>
  <li>"K" değeri kaç kümeye ayıracağımızı  belirleyen faktördür.</li>
  <li>K değeri her yinelemede en yüksek değeri bulmaya yardım eder.</li>
  <li>Başlangıçta K bizim tarafımızdan belirlenebilir. Sonrasında seçilen K değerine göre veriler K tane merkez noktada kümelenir.</li>
  <li>Kararlı hale gelinceye kadar merkez bulma döngüsü devam eder.</li><br />
  
  ![image](https://user-images.githubusercontent.com/56221025/207610083-981a86c4-2c2c-44c1-b7ec-3dc9debb5b2e.png)

  
  <h2>K-Means Kümeleme Algoritması Adımları</h2>
  <h3>Adım 1:</h3>
  <li>Kümeler için bir merkez noktası rastgele seçilir.</li><br /><br />
  
  ![image](https://user-images.githubusercontent.com/56221025/207611188-09a8f798-6215-4ce0-9cf8-b856ccf736de.png)
  
  <h3>Adım 2:</h3>
  <li>Merkez eleman dışındakiler en yakın merkez noktasına göre kümelenir. Bunun için her bir elemanın merkez noktalara olan uzaklıkları ölçülür.</li><br /><br />
  
  ![image](https://user-images.githubusercontent.com/56221025/207611348-5935372b-992d-4206-b845-01618136be25.png)
  
  <h3>Adım 3:</h3>
  <li>Kümelenen elemanlarımız şöyle bir hal alır.</li><br /><br />
  
   ![image](https://user-images.githubusercontent.com/56221025/207611392-3daba49e-e725-4cea-a6b5-bfa55ce9a76d.png)
   
  <h3>Adım 4:</h3>
  <li>Ardından aynı kümeler içerisinde tekrar bir merkez noktası hesaplanır.</li><br /><br />
  
  ![image](https://user-images.githubusercontent.com/56221025/207611443-cb5e2830-cc9d-45a8-af31-b7642180a61c.png)
  
  <h3>Adım 5:</h3>
  <li>Daha sonra merkez noktası kararlı hale gelinceye kadar ilk iki adım tekrarlanır.</li><br /><br />
  
  ![image](https://user-images.githubusercontent.com/56221025/207611501-9a1ef55f-590b-4157-8e98-1e2b68580e5a.png)
  
  <h2>K-Means Kümeleme Algoritması Sorunları</h2>
  <li>K-Means algoritmasının bazı problemleri vardır. Yapılan örnekte küme sayısını üç olarak aldık. Fakat küme sayısını kullanıcı belirleyeceği için bu sayı her zaman optimum olmayabilir.</li>
  <li>Başka bir problem ise başlangıçta rastgele olarak atanan merkez noktaları her zaman başarılı bir kümeleme işlemi başlatmayabilir. Çünkü algoritmanın gidişatı başlangıçta rastgele olarak atanan bu merkez noktalarına göre şekillenmektedir.  Başlangıçta atanan bu rastgele noktalar için K-Means++ algoritması mevcuttur.</li>
  <li>Optimum küme sayısını belirlemek için de WCSS (within-cluster sums of squares) yöntemi kullanılmaktadır.</li>
  <h3>WCSS Yöntemi</h3>
  <li>Amaç her bir küme için o kümedeki noktaların  merkez noktalarına olan uzaklıklarının karelerini hesaplamak.</li>
  <li>Kümeleme algoritmasında küme elemanları arasındaki mesafe minimum, her küme arasındaki mesafe ise maksimum ise o küme başarılı bir kümedir. </li><br />
  
  ![image](https://user-images.githubusercontent.com/56221025/207612507-b17c9911-f1a7-4805-861b-cdfa829bed3b.png)
  
  <br />
  <li>Eğer küme sayısını olabildiğince artırıp küme içindeki her bir eleman arası mesafeyi azaltırsak WCSS değeri o kadar azalır ve başarılı bir kümeleme gerçekleştirmiş oluruz. Fakat küme sayısını artırmanın da bir limiti vardır. Eğer küme sayısını her bir eleman ayrı bir küme olacak şekilde yaparsak küme elemanları arasındaki mesafe 0 olur ve WCSS de 0 olur. Fakat bu durumda modelimiz overfitting yani ezberleme durumuna uğrar. Onun için optimum küme sayısını WCSS grafiğindeki ani eğim değişimi olan yere göre belirlemeliyiz. Bu grafikteki en uygun değer 3'tür.</li><br />
  
  ![image](https://user-images.githubusercontent.com/56221025/207612115-48e9fa95-a683-4651-b428-d864fbee0995.png)
  
<h2>K-Means Kümeleme Algoritması Kullanım Alanları</h2>
<b>Belge Sınıflandırılması :</b>Belgeleri etiketlere, konulara ve belgenin içeriğine göre birden fazla kategoride kümeleyin. Bu standart sınıflandırma problemi K-Means ile çözülebilir.<br /><br />
<b>Suç Yerlerinin Belirlenmesi :</b>Bir  şehirdeki belirli bölgelerde mevcut olan suçlarla ilgili veriler, suç kategorisi, suç alanı ve ikisi arasındaki ilişki, bir şehirdeki ya da bölgedeki suça eğilimli alanlara ilişkin kaliteli bilgiler verebilir.<br /><br />
<b>BT Uyarılarının Otomatik Kümelenmesi :</b>Ağ, depolama veya veritabanı gibi büyük BT altyapı teknoloji bileşenleri büyük hacimli uyarı mesajları içerir. Uyarı mesajları potansiyel olarak operasyonel sorunlara işaret ettiğinden sonraki işlemler için  önceliklendirmenin manuel olarak taranmaları gerekir. Verilerin kümelenmesi uyarı kategorileri hakkında bilgi verebilir. Böylece ortalama onarım süresinin azalmasına tahminlerde yardımcı olarak katı sağlar.<br /><br />
<b>Görüntü Tanıma</b><br /><br />
<b>Oyuncu Analizi</b><br /><br />
<b>Çağrı Kaydı Detay Analizi</b><br /><br />
<b>Dolandırıcılık Tespiti</b><br /><br />
<h2>KAYNAKÇA</h2>
https://medium.com/machine-learning-t%C3%BCrkiye/ad%C4%B1m-ad%C4%B1m-makine-%C3%B6%C4%9Frenmesi-b%C3%B6l%C3%BCm-3-denetimsiz-%C3%B6%C4%9Frenme-nedir-f890ada49a40
<br>https://yavuz.github.io/denetimsiz-ogrenme/
<br>https://www.youtube.com/watch?v=CMbLMiJAx_g
<br>https://samed-harman.medium.com/makine-%C3%B6%C4%9Frenmesi-clustering-k%C3%BCmeleme-teknikleri-bd1b59a0a177 
<br>https://www.btkakademi.gov.tr/portal/course/player/deliver/python-ile-makine-oegrenmesi-11800 
<br>https://samed-harman.medium.com/makine-%C3%B6%C4%9Frenmesi-clustering-k%C3%BCmeleme-teknikleri-bd1b59a0a177
<br>https://www.google.com/imgres?imgurl=https%3A%2F%2Fwww.veribilimiokulu.com%2Fwp-content%2Fuploads%2F2019%2F10%2FKumeleme_Notlari_4_K-Ortalamalar_Python_Uygulama_Kumeler_grafik_gosterim.png&imgrefurl=https%3A%2F%2Fwww.veribilimiokulu.com%2Fkumeleme-notlari-4-k-ortalamalar-python-uygulama%2F&tbnid=lQsiD7CoJHQi2M&vet=12ahUKEwjl2PLH__b7AhXdIMUKHU-XAp0QMyhgegUIARCxAQ..i&docid=0P8fBezONugU3M&w=398&h=281&q=k%20means%20k%C3%BCmeleme%20algoritmas%C4%B1%20k%20mean&hl=tr&ved=2ahUKEwjl2PLH__b7AhXdIMUKHU-XAp0QMyhgegUIARCxAQ0
