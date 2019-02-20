# Nordpoolin tunnittaisen spot-hinnan ennustaminen Suomessa

## Muuttujat

* Yhdistetty yhteen dataframeen: Spot-hinnat, lämpötilamittaukset(HEL,JKL,ROV), sähkönsiirto, sähkönkulutus, tuulivoima, ydinvoima, vesivoima, kivihiilen hinta, öljyn (BRENT) hinta
* Puuttuu: Ruotsin ydinvoima ja tuulivoima. Päästöoikeuksien hinnat.


Ennustustuloksia:

| Menetelmä | RMSE | MAE |
| --- | --- | --- |
| LSTM verkko pelkällä Spot-hinnan historiatiedolla (testi: tammikuu 2019) | 9,86 | 7,79 |
| CNN-LSTM verkko pelkällä Spot-hinnan historiatiedolla (testi: tammikuu 2019) | 18,04 | 13,60 |
| ConvLSTM verkko pelkällä Spot-hinnan historiatiedolla | - | - |
| FBProphet additiivinen malli pelkällä Spot-hinnan historiatiedolla (testi: tammikuu 2019) | 10,46 | 6,81 |   
| LSTM verkko usealla muuttujalla (testi: vuosi 2018) | 6,18 | 3,61 |
| CNN-LSTM verkko usealla muuttujalla | - | - |
| ConvLSTM verkko usealla muuttujalla | - | - |