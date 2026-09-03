# Respiratory Lung Tracking — Colab demo

Ovaj repozitorijum sadrži jednu Colab notebook demonstraciju fine-tunovanog
modela za segmentaciju oba plućna krila kroz respiratornu sekvencu.

## Pokretanje u Google Colab-u

[![Open test demo in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/markovich1803/respiratory-lung-tracking/blob/master/lung_tracking_colab.ipynb)

[![Open training workflow in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/markovich1803/respiratory-lung-tracking/blob/master/lung_tracking_training_colab.ipynb)

`lung_tracking_colab.ipynb` ručno prima MP4, jednu PNG/JPG sliku ili ZIP
arhivu PNG frejmova, a u samom notebook-u prikazuje video segmentacije, grafik
i tabelu merenja za levo i desno plućno krilo.

`lung_tracking_training_colab.ipynb` preuzima skup podataka sa linka koji se
unese u prvoj ćeliji, automatski pronalazi lokalnu `images/` + `masks/`
strukturu, trenira model i zatim omogućava isti test workflow.

Trening slike nisu deo repozitorijuma. Fine-tunovani checkpoint je uključen
isključivo za testiranje i demonstraciju inferencije.
