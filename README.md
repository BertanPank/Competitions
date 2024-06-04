Competition Name: WiDS Datathon 2024 Challenge #2
Competition Link: https://www.kaggle.com/competitions/widsdatathon2024-challenge2/overview
Result: 26th/542

[TR]  
Problem: Hastaların kanser tanısı konmasının ne kadar sürdüğünün tahmin edilmesi.

Yaklaşımım: Veri seti 13200 gözlem ve 152 özelliğe sahip. Yani oldukça kısıtlı gözlemimiz ve çok fazla özelliğimiz var.
Overfit etmekten çekindiğim için şu stratejiyi izledim:

-Feature selection: Sadece 8 feature seçerek modellerimi bu featurelar ile eğittim.

-PCA: Birbirleriyle korele olduğunu düşündüğüm featureları PCA'ledim. Oluşan 4 featuredan 1'i skoru geliştirmeme yardımcı oldu.

-Kategorik featureların kardinalitesini olabildiğince düşürdüm.

-2 ila 4 derinlikli ağaçlar eğittim. Yarışmanın sonunda bunun aslında fazla düşük olduğunu farkettim. Eğer 6 derinliğe kadar çıksaydım istikrarlı şekilde ilk 5'e giren modeller eğitebiliyordum.

Geliştirilebilecek yönler:

-Autogluon'a ek olarak kendi modellerimi de manuel olarak eğitip HPO sonrası ensemble etsem çok yüksek ihtimalle kazanan çözüme sahip olunabilir.

----------------------------------------------------

[EN]
Problem: Predict the duration of time it takes for patients to receive a cancer diagnosis.

My approach: The dataset contains 13,200 observations and 152 features. This means we have a relatively small number of observations and a large number of features.

To avoid overfitting, I followed this strategy:

-Feature selection: I selected only 8 features and trained my models with these features.

-PCA: I performed PCA on features I thought were correlated. One of the 4 resulting features helped improve the score.

-I reduced the cardinality of categorical features as much as possible.

-I trained trees with depths ranging from 2 to 4. By the end of the competition, I realized this was too shallow. If I had gone up to a depth of 6, I could have consistently trained models that ranked in the top 5.

Areas for improvement:

In addition to AutoGluon, if I had manually trained my own models and performed HPO before ensembling, it is highly likely I could have achieved a winning solution.
