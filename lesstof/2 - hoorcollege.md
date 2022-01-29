## Hoorcollege

Data types:

* **Structured** - Data met een voorgedefinieerd model zoals databases, tabellen en spreadsheets.
* **Unstructured** - Data zonder een voorgedefinieerde structuur en daarom lastig op te slaan is in tabellen zoals afbeeldingen, geluid, video en tekst.
* **Big Data** - Een dataset welke zeer grote hoeveelheid data bevat en niet in memory van een enkele machine kan passen.

Veel voorkomende data bronnen \& formaten:

* CSV
* XML
* SQL
* JSON
* Protocol Buffers
* APIs

### Variabelen / Features
De variabelen die als input dienen om een andere variabel te voorspellen noemen we de 'independant variables'. De waarde welke voorsped wordt de 'dependant variabel'.

Afhankelijke en onafhankelijke variabelen:

* **Independant Variables** - Variabelen welke gebruikt worden om een ander variabel te voorspellen. Wordt ook wel *input variables* of *features* genoemd.
* **Dependant Variables** - Een eigenschap welke voorspel wordt. Wordt ook wel *output attribute* of *label* genoemd

Continu en discreet:

* **Continuous** - Continue variabelen kunnen oneindig mogelijkheden bevatten.
* **Discrete** - Kunnen slechts een beperkt aantal mogelijkheden bevatten.

Type features:

* **Numerical** - Representeerd een kwantitatieve eenheid. Kan *Continuous* of *Discrete* zijn.
* **Catagorische** - kwalitatieve data zonder wiskundige betekenis. Bijv. Yes/no of Country
* **Ordinal** - Categorische data met een wiskundige betekenis. Zoals een rating van n-sterren op een boek (1 is dus slechter dan 2).

### errors/problems

* **Errors** - Informatie die verloren is gegaan (en niet kan worden hersteld) door bijvoorbeeld electriciteits storing of een server die crashed.
* **Artifiacts** - Systemetische problemen die veroorzaakt zijn in het data cleaning process. Deze problemen kunnen gecorrigeerd worden maar moeten eerst ontdekt worden.

### Data compatibility
Wanneer variabelen met elkaar vergelijkt worden moet ervoor worden gezorgd dat deze *vergelijkbaar* zijn met elkaar, bijvoorbeeld;

* Units (metric / imperial)
* Numbers (decimals / integers)
* Names (John Smith / Smith, John)
* Time/dates (UNIX / UTC / GMT)
* Currency (Type, inflation adjusted, dividends)

### Data Imputation
Het omgaan met missende waardes (`NaN`).

* Drop records met missende gegevens
* **Heuristic-Based** - Maak een schatting gebasseerd op kennis van het domein
* **Mean Value** - Vervang missende data met een gemiddelde
* **Random** - Vervang met Random waarde
* **Interpolation** - Gebruik een methode zoals lineare regressie om de waarde van missende gegevens te voorspellen