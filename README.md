# Duruş Bozukluğu Tespiti İçin Transformatör Model Eğitimi 
*Transformatör modeli, doğal dil işleme (NLP) ve bilgisayarla görme gibi alanlarda kullanılan modern bir derin öğrenme mimarisidir. 2017 yılında "Attention is All You Need" makalesiyle tanıtılmıştır. Bu model, dikkat mekanizmasını (attention mechanism) kullanarak, girdiler arasındaki uzun vadeli ilişkileri öğrenmede ve paralel hesaplama yapmada yüksek performans sağlar. ViT, Swin, BEiT ve DeiT gibi popüler modeller transformatör mimarisi üzerine inşa edilmiştir.* </br>
### Kullanılan Modeller: </br>
`ViT: Vision Transformer ` </br>
`Swin: Shifted Window Transformer ` </br>
`BEiT: BERT Pre-Training of Image Transformers ` </br> </br>

# ViT </br> 
![image](https://github.com/user-attachments/assets/4f8847fa-d13d-454f-b231-22ab93676849) </br>
*Son epoch'ta eğitim doğruluğu %91,03, doğrulama doğruluğu ise %78,95 olarak gözlemlenmiştir. Benzer şekilde, eğitim kaybı başlangıçta 1,7818 iken, son epoch'ta 0,2428'e düşmüştür. Doğrulama kaybı ise 1,4029'dan 0,6786'ya kadar azalmıştır. Bu sonuçlar, modelin eğitim sırasında hem eğitim hem de doğrulama veri kümesine başarılı bir şekilde adapte olduğunu göstermektedir.* </br> </br>
## Modeli Test Etme </br>
![image](https://github.com/user-attachments/assets/e21af01c-ada5-4cc9-a74a-b3dc12a3b594) </br>
*Yukarıdaki görüntüler ile modelimizi test ettik.* </br> </br>
**1.Görsel: PEKTUS KARİNATUM** </br>
**2.Görsel: POLAND SENDROMU** </br>
**3.Görsel: KİFOZ** </br>
**4.Görsel: PEKTUS EKSKAVATUM** </br>
**5.Görsel: SKOLYOZ** </br> </br>
*Bu modelimiz beş resimden dördünü doğru bilmiştir (1.görsel hatalı). Çıkan sonuç ise şu şekildedir:* </br> </br>
![image](https://github.com/user-attachments/assets/0c064e3f-0fd6-4ec9-a792-9ce9f1b86e8a) </br> </br> 
# Swin </br>
![image](https://github.com/user-attachments/assets/18731854-1a77-46ef-b1bd-5567dd934f30) </br>
*İlk epoch'ta doğruluk %20.27 iken, ilerleyen epoch'larda modelin öğrenme başarısı artarak 14. epoch'ta doğruluk %71.11 seviyesine ulaşmıştır. Ancak, validasyon doğruluk değerlerinin (val_accuracy) eğitim doğruluğuna oranla düşük olduğu ve zamanla dalgalanma gösterdiği fark edilmektedir.* </br> </br>
## Modeli Test Etme </br>
![image](https://github.com/user-attachments/assets/5be3a16c-4339-4a3f-a966-0e9b3d3e1147) </br> 
*ViT model testinde kullandığımız görüntü verileri ile modeli test ettiğimizde karşımıza çıkan sonuç bu şekildedir. Model beş resim üzerinden iki tanesini doğru tahmin etmiştir.* </br> </br>
# BEiT </br>
![image](https://github.com/user-attachments/assets/494e054c-042b-4a61-a467-071e59b891c7) </br>
*14. epoch sonunda doğrulama doğruluğu %33.90'a ulaşmıştır. Eğitim kaybı sürekli düşüş göstermiştir; ancak doğrulama kaybında tam bir iyileşme gözlenmemiştir, bu da modelin doğrulama kümesinde genelleme yapma yeteneğinin sınırlı olduğunu gösterir. Toplam eğitim süresi 1788.80 saniyedir.* </br> </br>
## Modeli Test Etme </br>
![image](https://github.com/user-attachments/assets/8b50fa20-5659-48d8-990e-d218bc7af26f) </br>
*ViT model testinde de kullandığımız görüntüler ile BeiT modelini test ettik. Beş görüntüden ikisini doğru bildi. Sonuçlar modelin sınıfları ayırt etme zorluk çektiğini ve daha fazla optimizasyon gerektiğini gösteriyor.*
