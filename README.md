# Respiratory Lung Tracking — Colab demo

Ovaj repozitorijum sadrži jednu Colab notebook demonstraciju fine-tunovanog
modela za segmentaciju oba plućna krila kroz respiratornu sekvencu.

## Pokretanje u Google Colab-u
Test
[![Open test demo in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/markovich1803/respiratory-lung-tracking/blob/master/lung_tracking_colab.ipynb)

Full train+test
[![Open training workflow in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/markovich1803/respiratory-lung-tracking/blob/master/lung_tracking_training_colab.ipynb)

`lung_tracking_colab.ipynb` ručno prima MP4, jednu PNG/JPG sliku ili ZIP
arhivu PNG frejmova, a u samom notebook-u prikazuje video segmentacije, grafik
i tabelu merenja za levo i desno plućno krilo.

`lung_tracking_training_colab.ipynb` je potpuni trening + test workflow. U
prvoj ćeliji se bira izvor podataka. Za javni izvor korisnik unosi direktan ZIP
link ka zvaničnom COVID Chest X-ray repozitorijumu; notebook zatim preuzima
sirove fajlove, priprema uparene `images/` i `masks/` PNG fajlove, trenira model
i prikazuje istoriju treninga, a potom omogućava isti test workflow. Privatni
V7 export linkovi nisu deo ovog repozitorijuma i po potrebi se ručno unose u
prvoj ćeliji.

Trening slike nisu deo repozitorijuma. Fine-tunovani checkpoint je uključen
isključivo za testiranje i demonstraciju inferencije.
