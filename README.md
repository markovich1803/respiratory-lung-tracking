# Respiratory Lung Tracking — Colab demo

Ovaj repozitorijum sadrži jednu Colab notebook demonstraciju fine-tunovanog
modela za segmentaciju oba plućna krila kroz respiratornu sekvencu.

## Pokretanje u Google Colab-u
Test script
[![Open test demo in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/markovich1803/respiratory-lung-tracking/blob/master/lung_tracking_colab.ipynb)

Full train+test script
[![Open training workflow in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/markovich1803/respiratory-lung-tracking/blob/master/lung_tracking_training_colab.ipynb)

`lung_tracking_colab.ipynb` ručno prima MP4, jednu PNG/JPG sliku ili ZIP
arhivu PNG frejmova, a u samom notebook-u prikazuje video segmentacije, grafik
i tabelu merenja za levo i desno plućno krilo.

`lung_tracking_training_colab.ipynb` je potpuni trening + test workflow. U prvoj ćeliji se unosi Google Drive
link ka privatno uploadovanoj `colab_training_dataset.zip` arhivi. Notebook
očekuje tačno 392 image-mask para u sibling `images/` i `masks/` folderima,
prekida rad ako struktura ili broj parova ne odgovaraju, zatim trenira model,
prikazuje istoriju treninga i omogućava isti test workflow.

Trening slike nisu deo repozitorijuma. Fine-tunovani checkpoint je uključen
isključivo za testiranje i demonstraciju inferencije.
