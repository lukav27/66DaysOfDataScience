# 66DaysOfDataScience
66 DAYS OF DATA SCIENCE

**Knjige:**
1. [Marcos Lopez de Prado: Advances in Financial Machine Learning](https://www.amazon.com/Advances-Financial-Machine-Learning-Marcos/dp/1119482089)  

**Članci:**  
1. [Information-driven bars for financial machine learning: imbalance bars](https://towardsdatascience.com/information-driven-bars-for-financial-machine-learning-imbalance-bars-dda9233058f0)  
2. [Information-Driven Bars for Finance](https://towardsdatascience.com/information-driven-bars-for-finance-c2b1992da04d)

**Dan 1** *(15. veljače 2021.)*  
Pročitao prvo poglavlje knjige "Advances in Financial Machine Learning" (str. 50/393)

**Dan 2** *(16. veljače 2021.)*  
"Advances in Financial Machine Learning" poglavlje 2:  
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
   - cilj im je češće uzorkovanje u trenutcima kad nove informacije dolaze na tržište -> donošenje odluka prije nego cijene dosegnu novu ravnotežu   

Napomene:  
   + FIX poruke (Financial Information eXchange) -protokol za trgovanje i komuniciranje informacija o prodaji/kupnji  
   + BWIC (Bid Wanted In Competition) - formalni zahtjev za ponudu na paket osiguranja, institucijonalni investitor šalje trgovcima osiguranja kako bi dobio sliku tržišta, kontaktira najviše ponuditelje da finalizira dogovor  
   + heteroskedastičnost -pojava kada je standardna pogreška neke varijable promatrana u određenom vremenu nekonstantna (kondicionalna i nekondicionalna) 

**Dan 3** *(17. veljače 2021.)*  
članak: Information-driven bars for financial machine learning: imbalance bars (1)
članak: Information-Driven Bars for Finance (2)
"Advances in Financial Machine Learning" poglavlje 2:

-Information driven bars:  
   + Tick imbalance bars 
     - lista tickova (-1, 0, 1)  
     - 
   + Volume/Dollar bars  
   + Ticks Runs Bars  
   + Volume/Dollar runs bars  














   
