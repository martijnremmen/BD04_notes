## Hoorcollege

### Decision Trees

Decision trees hebben de volgende **voordelen**:

* Non-linearity
* Support for categorical variables
* Easy to interpret
* Application to regression

**Nadelen**:

* Prone to overfitting
* Instable (not rebust to noise)
* High variance
* Low bias

Decision Trees worden gemaakt op ongeveer de volgende manier (recursive partitioning steps):

1. Kies een predictor $X_i$
2. Kies een waarde $S_i$ uit $X_i$ welke de waardes in 2 splits (niet perse gelijk)
3. Meet hoe *puur* deze splitsing is. Puur = wanneer deze splitsing perfect classificeert
4. Met een algoritme worden verschillende waardes van $X_i$ en $S_i$ vergeleken om de *puurheid* te maximaliseren op de eerste split.
5. Wanneer deze *maximale puurheid* behaalt is wordt hetzelfde process doorlopen voor een tweede splits enzovoorts.

Meten van puurheid ($m$ is het aantal categorieën):


* Gini Index
    * Waarde tussen $0,0$ en $1 - 1 / m$
    * Volledig puur wanneer $I(A) = 0$
* Entropy
    * Volledige puur wanneer $ Ent(A) = 0 $

**Pruning**

* CART (*'Classification and Regression Trees'*) laat de tree volledig tot stand komen (deze is dus overfit)
* Probeer het punt te vinden waar de validatie error begint op te lopen
* Genereer steeds kleinere trees door leaves te prunen
* Op elk pruning moment zijn er meerdere verschillende mogelijkheden
* Gebruik een *cost complexity* functie om de beste tree te kiezen

**Regression Trees for Prediction**

* Wordt gebruikt bij *continue* uitkomst variabelen (afhankelijke)
* Vergelijkbare procedure als een classification tree
* Veel splits worden geprobeerd, kies de split welke impurity minimaliseerd
* Voorspelling is het gemiddelde van het numerische doelvariabelen in de vierkant (Bij Classification Trees is het een majority vote)
* impuurheid gemeten door de som van deviatie in het kwadraat
* Performance gemeten door RMSE (root mean squared error)

### Ensemble

Ensemble learning is een strategie waarbij meerdere verschillende classifiers/models in één model worden gecombineerd. Dit reduceert *variantie* in de voorspelling. Er zijn verschillende Ensemble methodes:

* **Bagging** - Er worden meerdere instanties van hetzelfde model gebouwd elk getrained op een verschillende subset van de originele dataset. Staat voor *"Bootrstrapping and Aggregating"*
* **Random Forests** - Een methode specifiek voor Decision Trees. Werkt voort op dezelfde basis als **bagging** alleen wordt willekeurig een aantal features gekozen voor elke knoop.
* **Boosting** - Verbeterd een model door informatie te gebruiken van vorige classifiers.

Samengevat:

1. Presteren over het algemeen beter dan individuele modellen
2. Hebben vele varianten (averaging, weighted avereging, voting, medians, resampling)
3. Bevorderd "parallel processing"
4. Helpt tegen overfitting (but does not cure it)
5. Zijn black-box modellen met hoge transparantie verliezen dit wanneer ensembled