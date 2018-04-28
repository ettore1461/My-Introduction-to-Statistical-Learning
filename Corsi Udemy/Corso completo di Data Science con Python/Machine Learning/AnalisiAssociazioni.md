## Analisi delle associazioni

l'analisi delle associazione fatta su un paniere di bene può essere fatta su 3 livelli:
* analisi per cliente
* analisi degli scontrini
* analisi degli oggetti acquistati (guardo gli solo gli oggetti e non la loro quantità)

## Regole di associazioni
analizza la probabilità di osservare una determinata correlazione tra i prodotti.

*database transazionale*: contiene le transazioni, registrate come osservazioni

**il supporto**

Analizza l'unione

![Supporto](http://www.sciweavers.org/tex2img.php?eq=%24%0AS_%7BX%2CY%7D%3D%5Cfrac%7B%5C%23%28X%2BY%29%7D%7BN%7D%0A%24&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0)

N: è il numero totale di transazioni

**la Confidenza**

Analizza l'intersezione

![Confidenza](http://www.sciweavers.org/tex2img.php?eq=%24%0AC_%7BX%2CY%7D%3D%5Cfrac%7B%5C%23%28X%20%5Ccap%20Y%29%7D%7B%5C%23%28X%29%7D%0A%24&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0)

### Metodi Ensamble

utilizza tanti classificatori, definiti *classificicatori deboli*, per poi unire le singole predizioni in una predizione più attendibile.
la predizione è unita attraverso un meccanismo di voto.

i metodi più usati sono:
* Bagging
* Boosting
* Random Forest

* #### Random Forest
il random forest permette di raggruppare un insieme di alberi di decisione.
si utilizza quando si ricade nella [**maledizione della dimensionalità**](https://github.com/ettore1461/My-Introduction-to-Statistical-Learning/blob/master/Corsi%20Udemy/Corso%20completo%20di%20Data%20Science%20con%20Python/Machine%20Learning/Note%20Generali.md)


* ### Bagging
il termine deriva da _Bootstrap Aggregation_, utilizza le tecniche di campionamento con bootstrap insieme a un modello predittivo (spesso gli alberi di decisione).
le fasi del bagging sono:
1. Applicare il bootstrapping per estrarre un subset di dati
1. applicare al subset un albero decisionale
1. aggrega i risultati con medie pesate

una volta creato il classificatore, ad ogni osservazione sarà associata una classe più probabile.

* ### Boosting
è un algoritmo che permette di migliorare le performance di alcuni algoritmi predittivi definiti deboli. il più conosciuto è l'_AdaBoost_
Si basa sull'utilizzo di più modelli perdittivi, e ad ogni modello viene poi assegnato un peso.
Il boosting può essere applicato a _un qualunque metodo di classificazione_.
Attua un processo iterativo per ridurre gli errori dei modelli precedenti.
