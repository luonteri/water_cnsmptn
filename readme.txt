Käyttöveden lämmitys aiheutuu epälineaarisesti vedenkulutuksesta.
Uusissa asuinrakennuksissa vedenkulutusta seurataan asuntokohtaisesti,
mutta tutkittavassa taloyhtiössä on yksi vesimittari, joka mittaa 
taloyhtiön kokonaisvedenkulutusta. Tämän vuoksi ajatuksena on tutkia 
voidaanko saada aikaan aikasarjaan perustuva ennuste veden kulutukselle. 
Jos ennuste on riittävän tarkka voitaisiin lämpimän käyttövesiverkoston kierrätys
pysäyttää hetkellisesti milloin vedenkulutus on nolla tai lähes nolla. (käytetään vain kylmää vettä)
Tämä edellyttää ennustemallilta riittävää tarkkuutta, jotta toisaalta asumismukavuus 
ei vaarannu ja toisaalta kustannukset eivät kasva toista kautta kuten esim. veden kulutuksen lisääntymisenä.

Pohjadata on kerätty Afry Oy:n ylläpitämästä tietokannasta. perusdata löytyy tiedostosta vededkulutus.xlsx.

Ennusteen laatimisessa käytetään FaceBookin kehittämää aikasarjaalgoritmia Prophet.

Laskenta suoritetaan ts_vedenkulutus.ipynb tiedostossa.

ts_vedenkulutus_iterointi.ipynb tiedostoa käytetään hyperparametrien arvojen testaamiseen. Vaihtamalla 
hypeparametien arvoja pyritään saavuttamaan mahdillisimman korkea ennustettavuus.
Nämä tulokset kerättiin tiedostoon prophet_results_collection.xlsx. 

Koska aika-sarja algoritmi ei tuottanut riittävän hyvää tarkkuutta testattiin data lisäksi seuraavilla algoritemeilla:
- Gradient Boosting (M3_grad_boost.ipynb)
- Logistic regression (M3_log_reg.ipynb)

Näillä algoritmeilla saatiin hieman parempi tulos, mutta tarkkuus tavoitetta 95% ei kuitenkaan saavutettu.