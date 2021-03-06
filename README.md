# 66 DAYS OF DATA SCIENCE

## **Knjige:**
1. [Marcos Lopez de Prado: Advances in Financial Machine Learning, 2018](https://www.amazon.com/Advances-Financial-Machine-Learning-Marcos/dp/1119482089)  
2. [Peter Bruce, Andrew Bruce and Peter Gedeck: Pratical statistics for data scientists, 2020](https://www.amazon.com/Practical-Statistics-Data-Scientists-Essential/dp/149207294X)

## **Članci:**  
1. [Information-driven bars for financial machine learning: imbalance bars](https://towardsdatascience.com/information-driven-bars-for-financial-machine-learning-imbalance-bars-dda9233058f0)  
2. [Information-Driven Bars for Finance](https://towardsdatascience.com/information-driven-bars-for-finance-c2b1992da04d)  
3. [Christopher J. Pannucci and Edwin G. Wilkins: Identifying and Avoiding Bias in Research](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2917255/)  

## **Stranice:**  
1. [Konstruiranje boxplota](https://www.oswego.edu/~srp/stats/bp_con.htm)  
2. [Kernel density estimation](https://mathisonian.github.io/kde/) 
3. [Zavaravajući grafovi](https://en.wikipedia.org/wiki/Misleading_graph)  
4. [Kaggle: Use Cases for Model Insight](https://www.kaggle.com/dansbecker/use-cases-for-model-insights)  
5. [Kaggle: Permutation Importance](https://www.kaggle.com/dansbecker/permutation-importance)  
6. [Kaggle: Permutation Importance (exercise)](https://www.kaggle.com/lukavaljin/exercise-permutation-importance)  
7. [Kaggle: Partial Plots](https://www.kaggle.com/dansbecker/partial-plots)  
8. [Kaggle: Partial Plots (exercise)](https://www.kaggle.com/lukavaljin/exercise-partial-plots)  
9. [Kaggle: SHAP Values](https://www.kaggle.com/dansbecker/shap-values)  
10. [Kaggle: SHAP Values (exercise)](https://www.kaggle.com/lukavaljin/exercise-shap-values) 
11. [Kaggle: Advanced Uses of SHAP Valuess](https://www.kaggle.com/dansbecker/advanced-uses-of-shap-values)  
12. [Kaggle: Advanced Uses of SHAP Values (exercise)](https://www.kaggle.com/lukavaljin/exercise-advanced-uses-of-shap-values)  
13. [simulacija distribucije frekvencije](https://onlinestatbook.com/stat_sim/sampling_dist/)   

## **Dan 1** *(15. veljače 2021.)*  
Pročitao prvo poglavlje knjige "Advances in Financial Machine Learning" (str. 50/393)

## **Dan 2** *(16. veljače 2021.)*  
*"Advances in Financial Machine Learning" poglavlje 2:*  
-Esencijalni tipovi financijskih podataka:  
1. Fundamentalni podatci  
   + poslovna analitika, većinom podatci računovodstva  
   + treba utvrditi kada su točno podatci objavljeni i pravilno indeksirati podatke, kraj perioda izvještavanja nije datum objave podataka  
   + treba paziti na podatke koji su obnovljeni i podatke koji su popunjeni iako je prava vrijednost tih podataka nepoznata  
2. Tržišni podatci  
   + uključuje svu aktivnost trgovine na nekom području  
   + idealno 'raw feed' -> nestrukturirane informacije (npr.: FIX poruke, BWIC¸odgovori...)
   + svaki sudionik na tržištu ostavlja karakterističan otisak -> predviđanje ponašanja  
3. Analitika  
   + podaci izvedeni iz originalnih, procesuirani  
   + pozitivno: već ekstrahirano znanje iz podataka  
   + negativno: skupo, nismo sigurni u kvalitetu, drugi korisnici?  
4. Alternativni podatci  
   + primarne informacije koje nisu stigle u druge izvore (npr.: podatci poslovnih procesa, podatci sa senzora, vijesti i mediji...)  
   + teško za procesiranje  
   + visok trošak i brige oko privatnosti

-Grafovi stupaca (bars):  
   1. Sandardni grafovi:  
   -transformiranje serija podataka koji stižu u nepravilnim frekvencijama
      + time bars (vremenski) - loša statistička svojstva i različito od stvarnog funkcioniranja  
      + tick bars (definiriani broj transakcija) - treba biti svjestan iznimaka (*outliers*)  
      + volume bars (količina)  
      + dollar bars (tržišna vrijednost) - otpornije na promjene broja dionica  
   2. Information-driven bars  
   -cilj im je češće uzorkovanje u trenutcima kad nove informacije dolaze na tržište -> donošenje odluka prije nego cijene dosegnu novu ravnotežu   

Napomene:  
   + FIX poruke (Financial Information eXchange) -protokol za trgovanje i komuniciranje informacija o prodaji/kupnji  
   + BWIC (Bid Wanted In Competition) - formalni zahtjev za ponudu na paket osiguranja, institucijonalni investitor šalje trgovcima osiguranja kako bi dobio sliku tržišta, kontaktira najviše ponuditelje da finalizira dogovor  
   + heteroskedastičnost -pojava kada je standardna pogreška neke varijable promatrana u određenom vremenu nekonstantna (kondicionalna i nekondicionalna) 

## **Dan 3** *(17. veljače 2021.)*  
*članak: Information-driven bars for financial machine learning: imbalance bars (1)  
članak: Information-Driven Bars for Finance (2)  
"Advances in Financial Machine Learning" poglavlje 2:*

Information driven bars:  
   + Tick imbalance bars 
     + lista tickova (-1, 0, 1)  
     + ![formula 1](https://user-images.githubusercontent.com/59167006/108177118-18cf2000-7103-11eb-9ecb-3b4eb79062e6.jpeg)  
     + ![1_MhKo-iXHA6l_D6Fy2jc-SQ](https://user-images.githubusercontent.com/59167006/108177466-9430d180-7103-11eb-8f22-f223306cfd0e.jpeg)  
     + određivanje praga - EWMA  
     + formula za dobivanje očekivane neravnoteže na početku svake svijeće u grafu:  
     + ![1_82PKW_r7HbHqccQgAtVvyA](https://user-images.githubusercontent.com/59167006/108182619-7d8d7900-7109-11eb-81f6-d0a5c5959a4c.jpeg)  
     + procjenjujemo broj tickova po svijeći koristeći EWMA stvarnih tickova (T) u prethodnim svijećama  

   + Volume/Dollar bars  
   + Ticks Runs Bars  
   + Volume/Dollar runs bars  

Napomene:  
   + EWMA (Exponentially Weighted Moving Average) - EWMA(t) = a * x(t) + (1-a) * EWMA(t-1), svi prethodni rezultati utječu na rezultat, što su dalji imaju manji utjecaj  
   
## **Dan 4** *(18. veljače 2021.)*
*"Pratical statistics for data scientists" poglavlje 1*  

Tipovi podataka:  
   + brojčani  
      + kontinuirani  
      + diskretni  
   + kategorički  
      + binarni
      + ordinalni  

Mjere položaja:  
   + prosjek (*mean*, *average*)  
   + težinski prosjek (*weighted mead*, *weighted average*) - suma svih vrijednosti pomnoženih sa težinom kroz zbroj težina  
   + medijan (*median*, *50th percentile*)  
   + percentil (*percentile*) - P posto podataka je ispod te vrijednsti  
   + težinski medijan (*weighted median*) - polovina zbroja težina se nalazi iznad i ispod  
   + podrezani *?* prosjek (*trimmed mean*, *truncated mean*) - prosjek nakon izbacivanja određenog broja ekstremnih vrijednost  
   + robustan (*robust*, *resistant*) - neosjetljiv na ekstremne vrijednosti  
   + iznimka (*outlier*, *extreme*) vrijednost podatka koja se bitno razlikuje od ostalih vrijednosti  

Mjere varijabilnosti:  
   + devijacija (*deviation*, *error*, *residual*)- razlika izmeđe procjenjenih i promatranih vrijednosti  
   + varijanca (*variance*, *mean-squared-error*) - prosječna suma kvadrata odstupanja vrijednosti obilježja (veličine) od aritmetičke sredine  
   + standarna devijacija (*standard deviation*) - kvadratni korjen varijance  
   + srednja apsolutna devijacija (*mean absolute deviation*, *L1 norm*, *Manhattan norm*) - prosjek odstupanja vrijednosti od prosjeka  
   + medijan absolutne devijacije od medijana (*median absolute deviation from the median*)  
   + raspon (*range*) - razlika najveće i najmanje vrijednosti u datasetu  
   + statistike redosljeda (*order statistics*, *ranks*) - metrike bazirane na vrijednostima podataka poredanim od najmanje do najveće  
   + interkvartil (*interquartile range*, *IQR*) - razlika između 75. i 25 interkvartila  

## **Dan 5** *(19. veljače 2021.)*  
*"Pratical statistics for data scientists" poglavlje 1*   
*[Konstruiranje boxplota](https://www.oswego.edu/~srp/stats/bp_con.htm)*  
*[Kernel density estimation](https://mathisonian.github.io/kde/)*  

Istraživanje distirbucije podataka:  
   + boxplot (*box and whiskers plot*)  
   + tablica frekvencija (*frequency table*)  
   + histogram
   + graf gustoće (*density plot*)

Istraživanje kategoričkih podataka:  
   + mod (*mode*)  
   + očekivana vrijednost (*expected value*) - izračunava se kad kategorije mogu biti povezane s numeričkom vrijednošću, prosiječna vrijednost bazirana na vjerojatnosti pojavljivanja neke kategorije (*težinski prosijek*)  
   + stupčasti grafikoni (*bar chart*)  
   + pita grafioni (*pie chart*)  

## **Dan 6** *(20. veljače 2021.)*   
[zavaravajući grafovi](https://en.wikipedia.org/wiki/Misleading_graph)  

## **Dan 7** *(21. veljače 2021.)*
*"Pratical statistics for data scientists" poglavlje 1*
Korelacija:  
   + koeficijent korelacije (*correlation coefficient*) - mjera povezanost između numeričkih varijabli 
     ![pearson-correlation-coefficient-formula](https://user-images.githubusercontent.com/59167006/108747621-ecba0180-753d-11eb-83ed-bd3741ecf133.png)
   + matrica korelacija (*correlation matrix*) - tablica u kojoj su varijable i retci i stupci a ćelije su korelacije među varijablama  
   + dijagram raspršenosti (*scatterplot*) - svaka os predstavlja vrijednosti jedne varijable  

## **Dan 8** *(22. veljače 2021.)*  
ponavljanje  

## **Dan 9** *(23. veljače 2021.)*
*"Pratical statistics for data scientists" poglavlja 1 i 2*
Istraživanje dvije ili više varijabli:  
   + kontigencijska talica (*contingency table*) - zbroj slučajeva dvije ili više kategoričkih varijabli  
   + heksagonalno svrstavanje (*hexagonal binning*) - graf dvije numeričke varijable sa zapisima svrstanim u heksagone  
   + dijagram kontura (*contour plot*) - graf koji pokazuje gustoću dvije muneričke varijable u obliku topografske mape  
   + *violin plot* - sličan boxplotu ali prikazuje procjenu gustoće  

**Podatci i distribucije uzorkovanja**  
slučajno uzorkovanje (*random sampling*) - proces u kojem svaki član populacije ima jendaku šansu biti izabran svaki krug -> jednostavan slučajni uzorak  
   + uzorak je podset podataka iz većeg seta podataka (u statistici populacija)  
   + N (n) - veličina populacije  
   + nadomještavanje (*replacment*) -  kad se neka stavka izabere ne izbacuje se iz populacije -> može biti ponovno odabrana  
   + stratificirano uzorkovanje (*stratified sampling*) - djeljenje podataka na particije nakon čega se slučajno uzorkuje iz svake particije  
   + particija (*stratum*, *strata*) - homogena podgrupa populacije sa zajedničkim karakteristikama  
   + pristranost (*bias*) - sistematska pogreška
   + pristrani uzorak (*sample bias*) - uzorak koji pogrešno predstavlje populaciju  

## **Dan 10** *(24. veljače 2021.)*  
Kaggle course "Machine Learning Explainability"  
[Kaggle: Use Cases for Model Insight](https://www.kaggle.com/dansbecker/use-cases-for-model-insights)

## **Dan 11** *(25. veljače 2021.)*  
Kaggle course "Machine Learning Explainability"  
[Kaggle: Permutation Importance](https://www.kaggle.com/dansbecker/permutation-importance)  
[Kaggle: Permutation Importance (exercise)](https://www.kaggle.com/lukavaljin/exercise-permutation-importance)

## **Dan 12** *(26. veljače 2021.)*  
Kaggle course "Machine Learning Explainability"  
[Kaggle: Partial Plots](https://www.kaggle.com/dansbecker/partial-plots)  
[Kaggle: Partial Plots (exercise)](https://www.kaggle.com/lukavaljin/exercise-partial-plots)  

## **Dan 13** *(27. veljače 2021.)*  
Kaggle course "Machine Learning Explainability"  
[Kaggle: SHAP Values](https://www.kaggle.com/dansbecker/shap-values)  
[Kaggle: SHAP Values (exercise)](https://www.kaggle.com/lukavaljin/exercise-shap-values)  

## **Dan 14** *(28. veljače 2021.)*  
Kaggle course "Machine Learning Explainability"  
[Kaggle: Advanced Uses of SHAP Valuess](https://www.kaggle.com/dansbecker/advanced-uses-of-shap-values)  
[Kaggle: Advanced Uses of SHAP Values (exercise)](https://www.kaggle.com/lukavaljin/exercise-advanced-uses-of-shap-values)  
   
## **Dan 15** *(1. ožujka 2021.)*  
*"Pratical statistics for data scientists" poglavlje 2"*  
+ pristranosti odabira (*selection bias*) - pristranost koja je rezultat načina na koji se biraju opažanja  
+ njuškanje po podatcima (*data snooping*) - opsežna pretraga po podatcima u potrazi za nečim zanimljivim  
+ efekt golemog pretraživanja (*vast search efect*) - pristranost ili nereproduktivnost kao rezultat višestrukog modeliranja podataka ili podataka s velikim brojem prediktora   
+ regresija na srednju vrijednost (*regression to the mean*) - fenomen varijabli da ekstremne vrijednosti nastoje pratiti centralne vrijednosti  

## **Dan 16** *(2. ožujka 2021.)*
[Christopher J. Pannucci and Edwin G. Wilkins: Identifying and Avoiding Bias in Research](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2917255/)  

## **Dan 17** *(3. ožujka 2021.)*
*"Pratical statistics for data scientists" poglavlje 2"*
Distribucija uzoraka (*sammpling distribution*) - distribucija neke statistike uzoraka dobivene iz više uzoraka koji se odnose na istu populaciju  
  + statistika uzoraka (*sample statistic*) - metrike izračunate iz uzoraka  
  + distribucija podataka (*data distribution*) - učestalost distribucije pojedinih vrijednosti u u skupu podataka  
  + teorem centralnog limita (*central limit theorem*) - tendencija distribucije uzoraka da zauzima normalan oblik porastom veličine uzorka    
  + standardna pogreška (*standard error*, *square root of n rule*) - varijabilnost statistike uzoraka s obzirom na veći broj uzoraka (ne miješati sa standardnom devijacijom!)  
[simulacija distribucije frekvencije](https://onlinestatbook.com/stat_sim/sampling_dist/)  

## **Dan 18** *(4. ožujka 2021.)*  
*"Pratical statistics for data scientists" poglavlje 2"*  
+ bootstrap uzorak (*bootstrap sample*) - uzorak uzet s nadomještavanjem iz promatranog skupa podataka  
+ ponovljeno uzorkovanje (*resampling*) - proces uzimanja ponovljenih uzoraka iz promatranog skupa podataka, uključuje bootstrap i permutaciju  

Algoritam za bootstrap:  
1. izvlačimo vrijednost iz uzorka, zabilježimo je i nadomjestimo  
2. ponovimo to *n* puta  
3. zabilježimo prosijek *n* zabilježenih vrijednosti  
4. ponovimo korake od 1 do 3 *R* puta  
5. koristimo *R* rezultata da bi:  
   + izračunali standardnu devijaciju - procijenjuje srednju standardnu pogrešku uzorka  
   + izradili histogram ili boxplot  
   + pronašli interval pouzdanosti  

Nappomene:
+ Permutacija - zadani poredak elemenata nekog skupa  

## **Dan 19** *(5. ožujka 2021.)*  
*"Pratical statistics for data scientists" poglavlje 2"*  
+ interval pouzdanosti (*confidence interval*) - raspon mogućih vrijednosti unutar kojega s izvjesnom vjerojatnošču nalazi ta statistička mjera populacije  
+ krajnje točke intervala (*interval endpoints*) - vrh i dno intervala pouzdanosti  

interval pouzdanosti računamo nakon bootstrapa tako da za x% željene pouzdanosti odredimo ((100-x)/2)% od R rezultata uzorkovanja sa svakog kraja distribucije kao točke podrezivanja

## **Dan 20** *(6. ožujka 2021.)*  
*"Pratical statistics for data scientists" poglavlje 2"*  
Normalna distribucija (Gaussova distribucija):  
![normalna distribucija](https://user-images.githubusercontent.com/59167006/110205045-9ec6c700-7e76-11eb-8692-1ae2a537ccec.png)  
+ standardizacija (standardization) - proces oduzimanja prosjeka i podjele sa standardnom devijacijom  
+ z-score - rezultat standardizacije jedne točke podatka  
+ standardna normalna distribucija (standard normal) - normalna distribucija sa prosjekom 0 i standardnom devijacijom 1  
+ QQ-graf (QQ-Plot) - graf za vizualizaciju blizine distribucije uzorka i neke druge specifične distribucije  

