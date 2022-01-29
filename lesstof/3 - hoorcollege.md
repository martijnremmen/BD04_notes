## Hoorcollege

### Statistical Analysis
Bij statistische analyze wordt slechts een kleinere *sample* van een *populatie* geobserveerd. Middels statistische inferentie kunnen we deduceren wat de eigenschappen van de *populatie* zijn gegeven dat we een *sample* hebben geobserveerd.

### Regression Analysis
Regressie modelering wordt gebruikt voor *predictive modelling* en onderzoekt een relatie tussen de afhankelijke (target) en onafhankelijke (predictor) variabelen.

Dit helpt dus bij het begrijpen van hoe de dependant variabelen verandert naarmate één van de onafhankelijke variabelen wordt aangepast (terwijl eventuele andere variabelen hetzelfde blijven).

Binnen *Regression Analysis* kennen we de volgende variabelen:

* De onbekende parameters $\beta_i$
* De onafhankelijke variabelen $x_i$
* De afhankelijke variabelen $y$

Regressie types:

* **Linear Regression** - Vindt een relatie tussen afhankelijke en een of meer onafhankelijk variabelen door een rechte lijn te trekken (de *best fit* lijn)
* **Logistic Regression** - Wordt gebruikt om de probability te vinden van een 'Success' event. Kan worden gebruikt wanneer de dependant variabelen binair is.
* **Polynomial Regression** - Wanneer de beste lijn niet recht is

Formeel gezien wat een model doet: $Y = f(\textbf{X}) + \epsilon$

* Waar $\textbf{X} = (X_{1}, X_{2} ...X_p)$ representeerd de input variabelen (onafhankelijke)
* $\epsilon$ Representeerd random error, bestaat uit:
    * *Reducible Error*: Error die potentieel verkleind kan worden door een leertechniek toe te passen dat $f$ beter schat.
    * *Irreducible Error*: Error dat niet verkleind kan worden onafhankelijk van hoe goed we $f$ inschatten. Dit type is onbekend en onmeetbaar.
* $Y$ representeerd de output variabelen (afhankelijke)

*Statistical Learning* bevat methodes om deze $f(\textbf{X})$ in te schatten.

Waarom proberen we $f(\textbf{X})$ te schatten?

* **Prediction** - Wanneer we een goede estimate hebben van $\hat{f}(\textbf{X}$ kunnen we deze gebruiken om voorspellingen te maken op nieuwe data. We gebruiken $\hat{f}$ als een *black box*. We geven er niet om hoe of waarom het werkt, zolang de uitkomst redelijk accuraat is.
* **Inferentie** - We willen begrijpen wat de relatie is tussen $\textbf{X}$ en $Y$. We behandelijk $\hat{f}$ niet langer als een *black box*. We willen begrijpen hoe $Y$ verandert ten opzichte van $\textbf{X}$



* *underfitting* - Betekent dat er een hoge *bias* is en het model niet helemaal klopt
* *Overfitting* - Betekent dat het model te veel is afgestemd op de trainingsset
