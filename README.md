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
prvoj ćeliji se bira izvor podataka. Preporučeni izbor je zvanični Montgomery
County CXR ZIP, sa 138 slika i ručno nacrtanim levim/desnim maskama pluća.
Notebook preuzima sirove fajlove, spaja leve i desne maske u standardni
`images/` + `masks/` raspored, trenira model i prikazuje istoriju treninga, a
potom omogućava isti test workflow. Podržan je i javni COVID Chest X-ray izvor,
kao i opcioni privatni V7 export.

Trening slike nisu deo repozitorijuma. Fine-tunovani checkpoint je uključen
isključivo za testiranje i demonstraciju inferencije.
