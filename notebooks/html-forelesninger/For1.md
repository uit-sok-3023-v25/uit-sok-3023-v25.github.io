# **Forelesning 1 - Introduksjon**


# Om kurset
Hovedpensum i dette faget blir disse Notebook-ene, som er lagd for å brukes i [Google Colab](https://colab.google/). Sammen med notebook'en vil vi også gjennomgå en del matematikk og maskinlæringskonsepter i de fysiske forelesningene.

I dette kurset har vi ikke pensumbok, men vi har lagd en kompendium som skal være støttelitteratur for forelesningene og inneholder en del teori som dere kan bruke i prosjektoppgaven. I tillegg, vil dere kunne bli testa i pensum fra kompendiet på muntlige eksamen.

Informasjon om semesteroppgave, forelesninger, innlevering og muntlig eksamen finner dere på GitHub siden (**eller Canvas - hva tenker du Øystein?**).



# Eksamen og vurdering
| <h2>Vurderingsform        | <h2>Andel  | <h2>Arbeidsform           | <h2>Beskrivelse |
|-----------------------|--------|-----------------|-------------|
| <h4>Semesteroppgave        | <h4>50%    | <h4>1-2 stk     | <h4>Gjennomføre et maskinlæringsprosjekt i Google Colab. |
| <h4>Muntlig eksamen        | <h4>50%    | <h4>Individuelt     | <h4>10 minutter presentasjon av prosjektet. <br> **20** minutter spørsmål til prosjekt OG resterende pensum. |

# Hvorfor Google Colab
Colab er en vertstjeneste for Jupyter Notebook som ikke krever noe oppsett for å bruke og gir gratis tilgang til databehandlingsressurser, inkludert GPU-er og TPU-er. Colab er spesielt godt egnet for maskinlæring, datavitenskap og vil derfor brukes aktivt gjennom kurset. Tensorflow, som er maskinlæringsrammeverket vi kommer til å bruke mye, er også utviklet av Google - noe som gjør det enkelt å kjøre i Google Colab.

![](https://media.dev.to/cdn-cgi/image/width=1000,height=420,fit=cover,gravity=auto,format=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fmns81frj4ziq82o2fea5.jpg)

Når det er sagt, er det mange måter å skrive Python-kode på. Dere står fritt til å velge akkurat det dere vil, et annet eksempel er Visual Studio Code (VSCode) - men forelesningene vil foregå i Colab.

# Hvordan hente forelesningsnotatene

#### **Manuell nedlastning**
Forelesningene vil dere finne her (Insert github-lenke til notebooks). De kan dere laste ned manuelt inne fra GitHub.

Det gjør dere inn i repositorie hvor disse **.ipynb**-filene ligger, samt datasett vi bruker og andre filer.

#### **Alternativ henting av forelesningsnotatene**
Dere kan også bruke et utviklerverktøy for å hente forelesningsnotatene, men dette er ikke et krav. Særlig dere på samfunnsøkonomi vil bruke ```git``` en del. Da kan dere følge denne oppskriften.

### 1. Installere git
**Windows:**

1. Gå til [installasjonsiden for git](https://git-scm.com/downloads)
4. Last ned for windows og installer for alle brukere (krever elevering/admin login)

**Mac:**

Åpne Terminal-appen og skriv `git`. Du blir spurt om du vil installere utviklerverktøy. Takk ja, og installer:-)
* (Hvis det ikke funker: gå til gå til [installasjonsiden for git](https://git-scm.com/downloads))

### 2. Hente kursmateriell fra Github

For å hente filene til Jupyter  åpner du kommanovinduet på nytt, men denne gangen UTEN Å HØYREKLIKKET, siden du nå skal arbeidet på ditt hjemmeområde. Videre gjør du slik:

1. Naviger til dit du ønsker å ha kursmappen din. Om du for eksempel har en mappe `Documents` på maskinen din, og du vil ha kursmappen under den, så skriver du
```cd Documents```

2. Lag en mappe der du ønsker å ha kursfilene dine ved å skrive inn i terminalvinduet

```mkdir sok-3023```

3. Gå så inn i den mappen du har laget ved å skrive

```cd sok-3023```
        
4. Last ned kursmateriellet ved å kopiere inn følgende kommando i kommandovinduet:

```git clone https://github.com/uit-sok-1003-h24/notebooks/```<br>
[https://github.com/uit-sok-1003-h24/notebooks/](https://github.com/uit-sok-1003-h24/notebooks/)

(OBS: Steg 4 må oppdateres med nye lenker til faget.)



# Hvorfor Python?
Python er et høynivå kodespråk, altså at det er enklere for oss å forstå hva vi faktisk skriver enn i lavnivå kodespråk som C#. I tillegg, har Python muligheten til å lage objekter og klasser, noe som er mye vanskeligere i f.eks. RStudio.

Python et av de mest veldokumenterte kodespråkene, hvertfall når det kommer til fagfeltet maskinlæring og kunstig intelligens. Derfor er det Python vi velger å bruke i dette introduksjonskurset til maskinlæring.

Jeg vil anbefale at arbeid dere gjør, og særlig prosjektet, lagres i et personlig repositorie på GitHub - det kan brukes i f.eks. jobbsøknad, for å vise deres breddekompetanse som økonomer.

# Andre læringsressurser
Som følge av koding og datavitenskapens egenart, er det mange småproblemer man kan støte på underveis. Likevel, har vi utallige nettsteder vi kan søke hjelp til, som
* Google
* YouTube
* ChatGPT

Husk å bruke kunstig intelligens med måte, da den (ironisk nok) kan *hallusinere* når det kommer til kompliserte kodespørsmål om ML/AI.


# **La oss begynne med det faglige**

# **Introduksjon til ML/AI**
* Kunstig intelligens er *intelligens* til maskiner, i motsetning til naturlig intelligens hos mennesker/dyr/levende liv.
* Maskiner kan også *etterligne* menneskelige kognitive funksjoner som *læring* og *problemløsning*.
  * Egentlig handler det om trender i data.
* Maskinlæring og AI trekker tråder fra biologi, psykologi, datavitenskap, statistikk (!!), ingeniørvitenskap osv.
  * Faktisk er statistikk **grunnmuren** for mange av de kjente maskinlæringsteknikkene vi har, og dette kurset kommer derfor til å gi dere en kort introduksjon til noen av de viktigste matematiske prinsippene bak (uten at vi skal gå alt for mye i dybden, selv om det er der det morsomme er).
* Kunstig intelligens er med andre ord et bredt begrep som monner mye, under viser noen av dens sentrale bestanddeler.

![AI's bestanddeler](https://miro.medium.com/v2/resize:fit:2000/format:webp/1*TSfbVZfzkLTDFT46U4-wbQ.png)

# AI er gammelt!
Deler av kunstig intelligens, som nevrale nettverk, er ikke ny teori. Nevrale nettverk hadde god bakgrunnteori allerede på 40 tallet!

## Grunnen til at det har eksplodert de siste årene er hovedsakelig
1. Utvikling av **nye** matematiske/statistiske modeller.
2. Økning i **tilgjengelig data**.
3. Økning i **GPU**'er (muligheten for å prosessere data).
4. Kostnadene av **datalagring** er minket betydelig.

# **Maskinlæring i økonomi og finans**
* Fordeler med bruk av AI/ML i finans
  * **Finansielle operasjoner** (f.eks. trading) er noen ganger basert på *forhåndsdefinerte regler*. ML/AI kan automatisere denne prosessen, og dermed **redusere kost og tidsbruk**.
  * **Finansielle beslutninger** (f.eks. innvilgning av lån, invisteringer etc.) krever ofte hurtig og fakta-baserte beslutninger - hvor maskinlæring kan være et verktøy i denne prosessen.
  * Til forskjell fra en økonom som forvalter et fond, krever ikke maskinlæring og kunstig intelligens **økonomisk kunnskap**, men finner mønster og trender i data - som kan potensielt hjelpe økonomer i deres jobb.
  * **Deteksjon** av svindel/hvitvasking/økonomisk kriminalitet.


## Veiledet læring
**Veiledet læring** og **ikke-veiledet læring** er to sentrale tilnærminger innen maskinlæring. Veiledet læring involverer bruk av et merket (eng: *labeled*) datasett, der hver input-data har en tilsvarende output (eller merking). Modellen lærer å forutsi output'et basert på input'et. Eksempler på veiledet læring inkluderer regresjon og klassifikasjon. På den annen side benytter ikke-veiledet læring datasett uten merking, hvor målet er å finne mønstre eller strukturer i dataene. Denne tilnærmingen brukes ofte i clustering og dimensjonsreduksjon. Valget mellom veiledet og ikke-veiledet læring avhenger av problemet og tilgjengeligheten av merkede data.

### Sammenligning av Veiledet og Ikke-veiledet Læring

| Egenskap                   | Veiledet Læring                             | Ikke-veiledet Læring                     |
|----------------------------|--------------------------------------------|------------------------------------------|
| **Datasett**               | Merket datasett med inngangs- og utgangsdata | Umerket datasett uten merking            |
| **Mål**                    | Forutsi utgang basert på innganger        | Finne mønstre, grupper eller strukturer  |
| **Algoritmer**             | Lineær regresjon, logistisk regresjon, NN | K-means, hierarkisk clustering, PCA     |
| **Bruksområder**          | Klassifikasjon, regresjon, prediksjon     | Clustering, datavisualisering            |
| **Eksempler**              | Spam-deteksjon, ansiktsgjenkjenning       | Segmentering av kunder, anomalideteksjon |
| **Dataforberedelse**      | Krever omfattende dataforberedelse med merking | Mindre dataforberedelse nødvendig         |

## Et introduksjonseksempel
I statistikk-kurs, så brukes ofte et datasett kalt 'iris' for å lære seg databehandling. Det ble brukt av den britiske statistikeren og biologen Ronald Fisher.

```python
# Importerer pandas for å laste datasettet
import pandas as pd

iris = pd.read_csv('https://raw.githubusercontent.com/mwaskom/seaborn-data/master/iris.csv')
```

Dette datasettet gir variabelene ```sepal_length```, ```sepal_width```, ```petal_length```, ```petal_width``` og ```species```. Tabellen under forklarer hva disse er:

| **Variabelnavn**     | **Beskrivelse**                                           | **Enhet**       | **Type**    |
|----------------------|-----------------------------------------------------------|-----------------|-------------|
| **sepal length (cm)** | Lengden på begerbladet (sepal) på blomsten                | Centimeter (cm) | Numerisk    |
| **sepal width (cm)**  | Bredden på begerbladet (sepal) på blomsten                | Centimeter (cm) | Numerisk    |
| **petal length (cm)** | Lengden på kronbladet (petal) på blomsten                 | Centimeter (cm) | Numerisk    |
| **petal width (cm)**  | Bredden på kronbladet (petal) på blomsten                 | Centimeter (cm) | Numerisk    |
| **species**           | Blomstens art: Setosa, Versicolor eller Virginica         | Kategorisk (blomst-art) | Kategorisk  |

Nå skal vi bruke *lineær regresjon* for å predikere blomst-art, basert på de forrige variablene.



```python
import pandas as pd

iris = pd.read_csv('https://raw.githubusercontent.com/mwaskom/seaborn-data/master/iris.csv')
iris
```





  <div id="df-7543fb53-2b5e-45a1-aece-04591e4a185d" class="colab-df-container">
    <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>sepal_length</th>
      <th>sepal_width</th>
      <th>petal_length</th>
      <th>petal_width</th>
      <th>species</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>5.1</td>
      <td>3.5</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4.9</td>
      <td>3.0</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>2</th>
      <td>4.7</td>
      <td>3.2</td>
      <td>1.3</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4.6</td>
      <td>3.1</td>
      <td>1.5</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5.0</td>
      <td>3.6</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>145</th>
      <td>6.7</td>
      <td>3.0</td>
      <td>5.2</td>
      <td>2.3</td>
      <td>virginica</td>
    </tr>
    <tr>
      <th>146</th>
      <td>6.3</td>
      <td>2.5</td>
      <td>5.0</td>
      <td>1.9</td>
      <td>virginica</td>
    </tr>
    <tr>
      <th>147</th>
      <td>6.5</td>
      <td>3.0</td>
      <td>5.2</td>
      <td>2.0</td>
      <td>virginica</td>
    </tr>
    <tr>
      <th>148</th>
      <td>6.2</td>
      <td>3.4</td>
      <td>5.4</td>
      <td>2.3</td>
      <td>virginica</td>
    </tr>
    <tr>
      <th>149</th>
      <td>5.9</td>
      <td>3.0</td>
      <td>5.1</td>
      <td>1.8</td>
      <td>virginica</td>
    </tr>
  </tbody>
</table>
<p>150 rows × 5 columns</p>
</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-7543fb53-2b5e-45a1-aece-04591e4a185d')"
            title="Convert this dataframe to an interactive table."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"/>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-7543fb53-2b5e-45a1-aece-04591e4a185d button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-7543fb53-2b5e-45a1-aece-04591e4a185d');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


<div id="df-fb93460b-9eb5-43a9-9d8f-35db23036afa">
  <button class="colab-df-quickchart" onclick="quickchart('df-fb93460b-9eb5-43a9-9d8f-35db23036afa')"
            title="Suggest charts"
            style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
     width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"/>
    </g>
</svg>
  </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

  <script>
    async function quickchart(key) {
      const quickchartButtonEl =
        document.querySelector('#' + key + ' button');
      quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
      quickchartButtonEl.classList.add('colab-df-spinner');
      try {
        const charts = await google.colab.kernel.invokeFunction(
            'suggestCharts', [key], {});
      } catch (error) {
        console.error('Error during call to suggestCharts:', error);
      }
      quickchartButtonEl.classList.remove('colab-df-spinner');
      quickchartButtonEl.classList.add('colab-df-quickchart-complete');
    }
    (() => {
      let quickchartButtonEl =
        document.querySelector('#df-fb93460b-9eb5-43a9-9d8f-35db23036afa button');
      quickchartButtonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';
    })();
  </script>
</div>

  <div id="id_2f254bc4-c0bb-4875-90f2-ebb7b2240e6c">
    <style>
      .colab-df-generate {
        background-color: #E8F0FE;
        border: none;
        border-radius: 50%;
        cursor: pointer;
        display: none;
        fill: #1967D2;
        height: 32px;
        padding: 0 0 0 0;
        width: 32px;
      }

      .colab-df-generate:hover {
        background-color: #E2EBFA;
        box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
        fill: #174EA6;
      }

      [theme=dark] .colab-df-generate {
        background-color: #3B4455;
        fill: #D2E3FC;
      }

      [theme=dark] .colab-df-generate:hover {
        background-color: #434B5C;
        box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
        filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
        fill: #FFFFFF;
      }
    </style>
    <button class="colab-df-generate" onclick="generateWithVariable('iris')"
            title="Generate code using this dataframe."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
       width="24px">
    <path d="M7,19H8.4L18.45,9,17,7.55,7,17.6ZM5,21V16.75L18.45,3.32a2,2,0,0,1,2.83,0l1.4,1.43a1.91,1.91,0,0,1,.58,1.4,1.91,1.91,0,0,1-.58,1.4L9.25,21ZM18.45,9,17,7.55Zm-12,3A5.31,5.31,0,0,0,4.9,8.1,5.31,5.31,0,0,0,1,6.5,5.31,5.31,0,0,0,4.9,4.9,5.31,5.31,0,0,0,6.5,1,5.31,5.31,0,0,0,8.1,4.9,5.31,5.31,0,0,0,12,6.5,5.46,5.46,0,0,0,6.5,12Z"/>
  </svg>
    </button>
    <script>
      (() => {
      const buttonEl =
        document.querySelector('#id_2f254bc4-c0bb-4875-90f2-ebb7b2240e6c button.colab-df-generate');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      buttonEl.onclick = () => {
        google.colab.notebook.generateWithVariable('iris');
      }
      })();
    </script>
  </div>

    </div>
  </div>





```python
# Importer nødvendige biblioteker
import numpy as np
from sklearn.linear_model import LinearRegression
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import LabelEncoder
from sklearn.metrics import accuracy_score

# Konverter arten til numeriske verdier
label_encoder = LabelEncoder()
iris['species'] = label_encoder.fit_transform(iris['species'])

# Definer features og targetvariable
X = iris.drop('species', axis=1)  # Funksjoner: sepallengde, sepalbredde, petallengde, petalbredde
y = iris['species']               # Målvariabel: art

# Split datasettet i trenings- og testsett
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=42)

# Definer lineær regresjonsmodellen
model = LinearRegression()

# Tren modellen på treningsdata
model.fit(X_train, y_train)

# Gjør prediksjoner på testdata
y_pred = model.predict(X_test)

print(y_pred)

# Siden resultatet er kontinuerlige verdier, avrunder vi til nærmeste heltall
y_pred_rounded = np.round(y_pred).astype(int)

# Evaluer nøyaktigheten
accuracy = accuracy_score(y_test, y_pred_rounded)
print(f"Accuracy: {accuracy * 100:.2f}%")

# Print noen eksempler på prediksjoner
for i in range(10):
    print(f"True species: {y_test.iloc[i]}, Predicted species: {y_pred_rounded[i]}")

```

    [ 1.24069097 -0.04537609  2.24501083  1.35143666  1.29775083  0.01024241
      1.05031173  1.82525399  1.37084413  1.06699186  1.70363485 -0.08712067
     -0.165166   -0.07724353 -0.03380619  1.40167699  2.00651252  1.04725931
      1.28368327  1.97600474  0.01782354  1.59952875  0.079732    1.92307532
      1.8621986   1.8790815   1.80251247  2.04196713  0.01873817  0.01291496
     -0.15365607 -0.08046738  1.18506728 -0.00461982 -0.02934265  1.68665136
      1.29088786 -0.07995434 -0.09076782 -0.16795331  1.75520461  1.37514144
      1.3174234  -0.07193336 -0.1131512 ]
    Accuracy: 100.00%
    True species: 1, Predicted species: 1
    True species: 0, Predicted species: 0
    True species: 2, Predicted species: 2
    True species: 1, Predicted species: 1
    True species: 1, Predicted species: 1
    True species: 0, Predicted species: 0
    True species: 1, Predicted species: 1
    True species: 2, Predicted species: 2
    True species: 1, Predicted species: 1
    True species: 1, Predicted species: 1


## Fordeler og ulemper med lineær regresjon for klassifikasjon

### Fordeler:
- Enkel implementasjon: Lineær regresjon er en av de enkleste modellene å forstå og implementere. Dette gjør den til et godt valg for å illustrere grunnleggende konsepter eller som et utgangspunkt.

- Lav beregningskompleksitet: Lineær regresjon er rask å trene og predikere med, spesielt på små datasett som Iris. Det er derfor en effektiv modell for rask testing og prototyping.

- Gir en numerisk forståelse av klassifiseringsproblemet: Ved å bruke lineær regresjon på et klassifiseringsproblem, kan man få en intuitiv følelse av hvordan forskjellige funksjoner (features) påvirker målet i form av kontinuerlige utfall.

### Ulemper:
- Ikke designet for klassifisering: Lineær regresjon er en modell for regresjon, ikke for klassifisering. Klassifisering er en oppgave hvor resultatet er en kategori (som for eksempel 0, 1, 2 for artene i Iris-datasettet), mens regresjon gir kontinuerlige prediksjoner. Ved å bruke lineær regresjon må du etterpå runde resultatene for å tilordne en klasse, noe som ikke nødvendigvis alltid fungerer like godt.

- Kan gi dårlige prediksjoner på klasser som ikke er ordnet: Lineær regresjon antar at de numeriske verdiene er ordnet i en lineær sammenheng, noe som ikke stemmer for klassifikasjon hvor klassene ikke nødvendigvis har en slik ordning. For eksempel, her er det ingen naturlig rekkefølge mellom artene setosa, versicolor og virginica. Ved å bruke lineær regresjon kan modellen feilaktig anta at avstanden mellom klassene er kontinuerlig og proporsjonal, noe som kan føre til dårlige prediksjoner.

- Prediksjoner utenfor rekkevidde: Lineær regresjon kan predikere verdier utenfor klasserommene (for eksempel predikere -0.5 eller 3.0), noe som er meningsløst for klassifikasjonsproblemer der klassene er diskrete og begrenset (her mellom 0, 1 og 2).

- Rundingsproblemer: Når du runder prediksjoner til nærmeste heltall, kan det være stor risiko for feilklassifisering, spesielt hvis prediksjonene er nær grensen mellom to klasser. Små feil i lineære prediksjoner kan føre til feilklassifisering.

### Når kan det være nyttig?
Lineær regresjon kan være nyttig som en enkel baseline-modell. Ved å kjøre lineær regresjon kan du sammenligne resultatene med mer avanserte klassifiseringsmodeller for å se hvor mye mer nøyaktighet du oppnår med de riktige verktøyene for klassifikasjon. Det er også nyttig for forståelse av de grunnleggende sammenhengene mellom funksjoner og prediksjoner, selv om det ikke nødvendigvis gir den beste ytelsen - derfor har vi tatt det med her, bare for eksempelhetens skyld.

## Alternative modeller som passer bedre til klassifisering:
- **Logistisk regresjon**: Passer bedre til binær og multiklassifisering enn lineær regresjon fordi den gir sannsynligheter for hver klasse.
- **Decision Trees**: Kan klassifisere data på en ikke-lineær måte og håndtere komplekse beslutningsregler.
- **Random Forest**: En ensemble-modell som kombinerer flere beslutningstrær for bedre prediksjoner.
- **K-nearest neighbors (KNN)**: En enkel, men ofte effektiv klassifiseringsmetode som bruker nærhet til andre data.

**Disse går vi ikke gjennom eksplisitt i kurset, men er læringsteknikker dere kan ta i bruk på prosjektet i kurset. Særlig decision trees og random forests, på grunn av deres brukervennlighet.**

## La oss teste ut decision trees


```python
# Importer nødvendige biblioteker
import numpy as np
import pandas as pd
from sklearn.tree import DecisionTreeClassifier
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score, confusion_matrix

# Last ned iris-datasettet - på nytt for å ikke gjøre unødvendig encoding
iris = pd.read_csv('https://raw.githubusercontent.com/mwaskom/seaborn-data/master/iris.csv')

# Definer features og targetvariable
X = iris.drop('species', axis=1)  # Funksjoner: sepallengde, sepalbredde, petallengde, petalbredde
y = iris['species']               # Målvariabel: art (ingen behov for LabelEncoder)

# Split datasettet i trenings- og testsett
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=42)

# Definer Decision Tree Classifier
model = DecisionTreeClassifier(random_state=42)

# Tren modellen på treningsdata
model.fit(X_train, y_train)

# Gjør prediksjoner på testdata
y_pred = model.predict(X_test)

# Evaluer nøyaktigheten
accuracy = accuracy_score(y_test, y_pred)
print(f"Accuracy: {accuracy * 100:.2f}%")

# Print noen eksempler på prediksjoner
for i in range(10):
    print(f"True species: {y_test.iloc[i]}, Predicted species: {y_pred[i]}")
```

    Accuracy: 100.00%
    True species: versicolor, Predicted species: versicolor
    True species: setosa, Predicted species: setosa
    True species: virginica, Predicted species: virginica
    True species: versicolor, Predicted species: versicolor
    True species: versicolor, Predicted species: versicolor
    True species: setosa, Predicted species: setosa
    True species: versicolor, Predicted species: versicolor
    True species: virginica, Predicted species: virginica
    True species: versicolor, Predicted species: versicolor
    True species: versicolor, Predicted species: versicolor



```python
# Calculate confusion matrix
conf_matrix = confusion_matrix(y_test, y_pred)

# Print confusion matrix
print("Confusion Matrix:")
print(conf_matrix)
```

    Confusion Matrix:
    [[19  0  0]
     [ 0 13  0]
     [ 0  0 13]]


# **Tensorflow** skal bli vår venn :-)
TensorFlow er et gratis og åpen kildekode-programvarebibliotek for maskinlæring og kunstig intelligens. Det kan brukes til en rekke oppgaver, men har et spesielt fokus på trening og inferens av dype nevrale nettverk. Det er utviklet og brukt av Google. Opprinnelig ble det laget som en del av Google's Brain Team, og 9. november 2015 ble TensorFlow gjort tilgjengelig under Apache 2.0 open source-lisensen.
[Les mer om Tensorflow her!](https://www.tensorflow.org/)

## Hva er en *tensor*?
En **tensor** er en generell betegnelse på en dataenhet i maskinlæring og numerisk databehandling. Den kan betraktes som en utvidelse av skalarer, vektorer og matriser til høyere dimensjoner.
*Tensor* har spesifikke matematiske definisjoner basert på kontekst, som for eksempel i fysikken, så bruker vi en definisjon som er relevant mot maskinlæring, fra *Deep Learning* (Goodfellow, Bengio, and Courville, 2016):
**In the general case, an array of numbers arranged on a regular grid with a variable number of axes is known as a tensor.**

## Typer av Tensor
En tensor er en generalisering av matriser og vektorer til høyere dimensjoner og er en grunnleggende datastruktur i maskinlæring, spesielt i rammeverk som PyTorch og TensorFlow.
1. **Skalar** (rank-0 tensor)
   - En enkeltverdi, for eksempel et tall som $3$ eller $7.5$.

2. **Vektor** (rank-1 tensor)
   - En rekke av verdier, for eksempel en liste med tall $[1, 3, 5, 7]$.

3. **Matriser** (rank-2 tensor)
   - En matrise med nxn-dimensjoner, for eksempel $\begin{bmatrix}
3 & 5 & 7 \\
2 & 6 & 1 \\
8 & 4 & 9
\end{bmatrix}$.

4. **Rank-3 tensor** og høyere
  - En flerdimensjonal generalisering av matriser. For eksempel en 3D-tensor kan tenkes som en "kubelignende" struktur med flere matriser stablet sammen.



## *Hvordan skrive tensorer i Python*

### **0-rank tensor**


```python
# Først må vi importere tensorflow i Python. Det gjøres slik:
import tensorflow as tf
```


```python
# En vanlig skalar vil vanligvis skrives;
skalar = 3
print(3)

# Skal vi skrive en rank-0 tensor, gjør vi følgende;
zero_tensor = tf.constant(3)
print(zero_tensor)
```

    3
    tf.Tensor(3, shape=(), dtype=int32)



```python
# Vi kan nå se på typene
print(type(skalar))

print(type(zero_tensor))
```

    <class 'int'>
    <class 'tensorflow.python.framework.ops.EagerTensor'>


Her ser vi at variabelen *skalar* tilhører en annen klasse enne *zero_tensor*, dette vil være viktig senere i kurset.

### La oss gjøre det samme for **rank-1 tensor** og **rank-2 tensor**.


```python
import numpy as np

# Eksempel på en vektor ved bruk av numpy (knallbra bibliotek for matematiske operasjoner med vektorer)
vector = np.array([1, 2, 3, 4, 5])
print(vector)

# rank 1 tensor
rank_1_tensor = tf.constant([1, 2, 3, 4, 5])
print(rank_1_tensor)

# Vi kan nå se på typene
print(type(vector))

print(type(rank_1_tensor))
```

    [1 2 3 4 5]
    tf.Tensor([1 2 3 4 5], shape=(5,), dtype=int32)
    <class 'numpy.ndarray'>
    <class 'tensorflow.python.framework.ops.EagerTensor'>



```python
# Eksempel på matrise ved bruk av numpy
matrix = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
print(matrix)

# rank 2 matrix
rank_2_tensor = tf.constant([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
print(rank_2_tensor)
```

    [[1 2 3]
     [4 5 6]
     [7 8 9]]
    tf.Tensor(
    [[1 2 3]
     [4 5 6]
     [7 8 9]], shape=(3, 3), dtype=int32)


## **En matematisk presentasjon av tensorer kan være følgende**
1. Rank-0 Tensor, Skalar, $ℝ$
2. Rank-1 Tensor, Vektor, $ℝ^n$
3. Rank-2 Tensor, Vektor, $ℝ^n × ℝ^m$
4. Rank-3 Tensor, Vektor, $ℝ^n × ℝ^m × ℝ^p$

Det viktigste å forstå her er at når vi snakker om en *tensor* og vi snakker om dens *dimensjoner* som **rank** til tensoren, så må dette **ikke** forveksles med dimensjonene til matrisen!

![Forklarende bilde av tensorer](https://hkilter.com/images/7/7a/Tensors.png)


### **Når får man bruk for rank-3 tensorer?**
* Et gråskalabilde (enkanals) er vanligvis en tensor av rank 2, representert som en 2D-matrise (høyde × bredde) med pikselverdier.
* Et fargebilde har derimot flere kanaler (vanligvis tre: rød, grønn og blå). Det representeres derfor som en 3D-matrise (høyde × bredde × kanaler), hvor hver kanal lagrer pikselverdier som tilsvarer én farge. Dette kommer vi mer inn på senere i kurset.

# **Noen fundamentale konsepter i maskinlæring**





## **Prediksjon vs inferens**
Fra tidligere matematikk- og statistikk-kurs har dere være lært om *lineær regresjon*. Da har vi en kvantitativ response $Y$ og $p$ ulike prediktorer, disse kan skrives $X = (X_1, X_2, \ldots, X_p)$. Sammenhengen uttrykkes da som

$$Y=f(X)+ϵ$$

hvor $f$ er en ukjent funksjon av $X$ og $ϵ ∼ N(0, σ^2)$. Hvor i lineær regresjon, hvor vi prøver å estimere $Y$, vil det kunne skrives som

\begin{align}
\hat{Y} &= \hat{f}(x) \\
&= \beta_0 + \beta_1 \cdot X_1 + \cdots + \beta_p \cdot X_p,
\end{align}

her ser dere at $ϵ$ er borte, det er fordi $E[ϵ]=0$, mens $\beta_0$ representerer **konstantleddet** (intercept) og $\beta_i, i=1,\ldots,p$ representerer **regresjons koeffisientene**.

Under her har vi et eksempel på *enkel* lineær regresjon.

![Lineær regresjon](https://media.licdn.com/dms/image/D4D12AQFLzVNzsxPLvA/article-cover_image-shrink_423_752/0/1698421969894?e=1728518400&v=beta&t=VogREEr5ZeblblSFt2Bkz90On1qDdGno_-2R6mn8JQs)

Dette leder oss inn på hva **prediksjon** er. Ofte kan vi finne $X$ verdiene, men output'et $Y$ er ikke alltid like lett. Derfor prøver vi å predikere $Y$ som
$$\hat{Y}=\hat{f}(X)$$
hvor også her $\epsilon$ er satt til $0$, som følge av forventningsverdien. $\hat{f}$ er vårt estimat av $f$ og $\hat{Y}$ representerer vår prediksjon av $Y$.

Prediksjon handler jo (selvfølgelig) om å predikere noe, men da er det nettopp det vi er interssert i - som følge av det behandler vi ofte $\hat{f}$ som en *svart boks* (black-box principle, noe vi kommer til å snakke mye om).

### Inferens
Inferens handler om når vi vil se og forstå sammenhengen mellom $Y$ og disse $X$'ene ($X_1, X_2, \ldots, X_p$).
Derfor er ikke hovedmålet å estimere $f$, og derfor kan vi heller ikke behandler $\hat{f}$ som en *svart boks*.

For eksempel, hvis vi har ulike prediktorer, og responsen er solgte PC'er. Da er salgsteamet interssert i **hvilke** prediktorer har mest å si for salget, i både positiv og negativ retning! Eller de kan gjennomføre hypotese-testing, estimering av koeffisientene (f.eks. $\beta_0$).

## **Irreducible og reducible error**
Fra statistikken har dere lært om **forventningsverdi** og **varians**. I tillegg har dere lært om **Mean Squared error (MSE)**. Her er den matematiske definisjonen av disse termene:

### **Definisjon av forventningsverdi**
La $X$ være en tilfeldig vriabel med sannsynlighetsfordeling $f(x)$. **Forventningsverdien** av $X$ er

$$E[X]= \sum_{x}x \cdot f(x)$$

hvis $X$ er diskret, og

$$E[X]=\int_{-\infty}^{∞}x \cdot f(x) \; dx$$

hvis $X$ er kontinuerlig.

### **Definisjon av varians**
La $X$ være en tilfeldig variabel med sannsynlighetsfordeling $f(x)$. **Variansen** til $X$ er

$$\sigma^2 = E[(X-\mu)^2]=\sum_{x}(x-\mu)^2 \cdot f(x),$$

hvis $X$ er diskret, og

$$\sigma^2 = E[(X-\mu)^2]=\int_{-\infty}^{\infty}(x-\mu)^2 \cdot f(x) \; dx,$$

hvis $X$ er kontinuerlig.

## **MSE**
Hvis en vektor av $n$ prediksjoner er generert fra et utvalg med $n$ datapunkter, og $Y$ er den observerte verdien, og $\hat{Y}$ er den predikerte verdien, da er **Mean Squared Error**

$$MSE = \frac{1}{n}\sum_{i=1}^n \left(Y_i - \hat{Y_i}\right)^2$$

Disse verdiene over kan vi bruke til å forklare et av de fundamentale konseptene i maskinlæring.

*Prediksjon* er ofte et mål i maskinlæring, og hvis vi lar $Y$ representere den faktiske *avhengige variabelen* (også kalt response) og $\hat{Y}$.  Når man driver med prediksjon vil man ikke alltid kunne treffe $100$% på virkeligheten, derfor velger vi å se på forventningsverdien av differansen mellom $Y$ (observert response) og $\hat{Y}$ (predikert response), i andre. Disse kan uttrykkes matematisk på følgende vis:

$$Y = f(X) + ϵ$$
og
$$\hat{Y} = \hat{f}(X)$$

hvor sannheten $Y$ alltid inneholder litt noise/støy, nemlig $ϵ$ (på engelsk kalt, *irreducible error*). Med følgende egenskaper:

$$E[ϵ]=0$$
og
$$Var[ϵ]=σ^2$$

Dette gjør at vi kan gjøre følgende:

$$
\begin{align}
E[(Y - \hat{Y})^2] &= E[(f(X) + \epsilon - \hat{Y})^2] \\
&= [f(X)-\hat{f}(X)]^2 + Var(ϵ)
\end{align}
$$

Differansen mellom $f(X)$ og $\hat{f}(X)$ **kan** man gjøre noe med (f.eks. med bedre modell, feature selection, bruk av domene-kunnskap osv.) og kalles **reducible error**, mens $Var(\epsilon)$ kan man ikke gjøre noe med, derfor **irreducible error**.



## **Oppgave**
Utled $E[(f(X) + \epsilon - \hat{Y})^2]$ for å vise at det er lik $[f(X)-\hat{f}(X)]^2 + Var(ϵ)$.

## **Regresjon versus klassifikasjon**
I *maskinlæring* er det viktig å skille mellom **regresjon** og **klassifikasjon**, da disse tilnærmingene er designet for å håndtere ulike typer prediksjonsproblemer.

Regresjon brukes når målet er å forutsi en **kontinuerlig variabel**. For eksempel kan vi bruke regresjon for å estimere boligpriser basert på ulike egenskaper som størrelse og beliggenhet. I regresjonsproblemer er den avhengige variabelen en kontinuerlig verdi som kan ta et uendelig antall verdier innenfor et bestemt område. Matematiske modeller i regresjon er designet for å minimere avviket mellom de predikerte verdiene og de faktiske verdiene. For eksempel, når vi estimerer en boligpris, kan modellen forsøke å forutsi en pris i en konkret skala, som $300,000, som representerer en spesifikk, kontinuerlig verdi.

Klassifikasjon, derimot, handler om å forutsi en **kategorisk variabel**. Dette innebærer å tilordne hver observasjon til en av et begrenset antall kategorier eller klasser. For eksempel kan vi bruke klassifikasjon for å bestemme om en e-post er spam eller ikke, eller for å identifisere håndskrevne sifre i en bildedatabase. Klassifikasjonsproblemer resulterer i diskrete utfall, hvor hver observasjon tilhører en av et sett med definerte klasser. Matematiske modeller i klassifikasjon gir en sannsynlighet for hvert av de mulige utfallene og tildeler den mest sannsynlige klassen basert på disse sannsynlighetene. For eksempel, i en e-postklassifikator, kan modellen gi en sannsynlighet på $90$% for at en e-post er spam og $10$% for at den ikke er spam, og dermed klassifisere e-posten som spam.

## **Trening, validering og testdata**

I maskinlæring er det avgjørende å dele datasettet i tre distinkte deler: *trening*, *validering* og *testdata*. Trening av modellen skjer på treningsdataene, hvor målet er å lære de underliggende mønstrene og sammenhengene i dataene. Under denne prosessen justeres modellens parametere for å minimere feilen mellom de predikerte og de faktiske verdiene.

Deretter evalueres modellen på valideringsdataene. Valideringsdataene brukes ikke til trening, men til å optimalisere modellvalg og hyperparametere, som for eksempel *læringsrate* (eng: *learning rate*) eller antall *noder* (eng: *nodes*) i et nevralt nettverk. Dette hjelper til med å unngå *overtilpasning* (eng: *overfitting*, som vil diskuteres lenger ned i dokumentet), hvor modellen tilpasser seg treningsdataene for godt og dermed mister evnen til å generalisere til nye data.

Til slutt brukes testdataene, som modellen ikke har sett tidligere, for å gi en endelig evaluering av modellens generaliseringsevne.

For en økonom kan dette være særlig viktig ved for eksempel prediksjon av finansielle indikatorer, hvor en godt generalisert modell kan ha direkte praktiske implikasjoner i beslutningsprosesser.

![Eksempel på to ulike måter å splitte data på](https://upload.wikimedia.org/wikipedia/commons/thumb/b/bb/ML_dataset_training_validation_test_sets.png/800px-ML_dataset_training_validation_test_sets.png?20201206114522)

Her skal vi se på eksempel på hvordan vi splitter opp et datasett, og bruker det til noe fornuftig.


```python
# Hvis vi importerer data, kan vi splitte det opp på følgende vis
import pandas as pd

# Importerer datasettet
df = pd.read_csv('Fraud.csv')
df.head()
```





  <div id="df-5a5441da-02b8-4839-8c51-d02437853b62" class="colab-df-container">
    <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Unnamed: 0</th>
      <th>step</th>
      <th>type</th>
      <th>branch</th>
      <th>amount</th>
      <th>nameOrig</th>
      <th>oldbalanceOrg</th>
      <th>newbalanceOrig</th>
      <th>nameDest</th>
      <th>oldbalanceDest</th>
      <th>newbalanceDest</th>
      <th>unusuallogin</th>
      <th>isFlaggedFraud</th>
      <th>Acct type</th>
      <th>Date of transaction</th>
      <th>Time of day</th>
      <th>isFraud</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>1</td>
      <td>PAYMENT</td>
      <td>Indonesia</td>
      <td>9839.64</td>
      <td>C1231006815</td>
      <td>170136.0</td>
      <td>160296.36</td>
      <td>M1979787155</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>9</td>
      <td>0</td>
      <td>Current</td>
      <td>3/1/2018</td>
      <td>Morning</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>PAYMENT</td>
      <td>India</td>
      <td>1864.28</td>
      <td>C1666544295</td>
      <td>21249.0</td>
      <td>19384.72</td>
      <td>M2044282225</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>10</td>
      <td>0</td>
      <td>Savings</td>
      <td>5/1/2018</td>
      <td>Morning</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>1</td>
      <td>TRANSFER</td>
      <td>India</td>
      <td>181.00</td>
      <td>C1305486145</td>
      <td>181.0</td>
      <td>0.00</td>
      <td>C553264065</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>2</td>
      <td>0</td>
      <td>Current</td>
      <td>7/1/2018</td>
      <td>Morning</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
      <td>1</td>
      <td>CASH_OUT</td>
      <td>Australia</td>
      <td>181.00</td>
      <td>C840083671</td>
      <td>181.0</td>
      <td>0.00</td>
      <td>C38997010</td>
      <td>21182.0</td>
      <td>0.0</td>
      <td>1</td>
      <td>0</td>
      <td>Current</td>
      <td>6/1/2018</td>
      <td>Afternoon</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4</td>
      <td>1</td>
      <td>PAYMENT</td>
      <td>Australia</td>
      <td>11668.14</td>
      <td>C2048537720</td>
      <td>41554.0</td>
      <td>29885.86</td>
      <td>M1230701703</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>17</td>
      <td>0</td>
      <td>Current</td>
      <td>6/1/2018</td>
      <td>Morning</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-5a5441da-02b8-4839-8c51-d02437853b62')"
            title="Convert this dataframe to an interactive table."
            style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"/>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-5a5441da-02b8-4839-8c51-d02437853b62 button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-5a5441da-02b8-4839-8c51-d02437853b62');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


<div id="df-7a256f2d-4de4-4a0f-bbc2-211eb7c831fd">
  <button class="colab-df-quickchart" onclick="quickchart('df-7a256f2d-4de4-4a0f-bbc2-211eb7c831fd')"
            title="Suggest charts"
            style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
     width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"/>
    </g>
</svg>
  </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

  <script>
    async function quickchart(key) {
      const quickchartButtonEl =
        document.querySelector('#' + key + ' button');
      quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
      quickchartButtonEl.classList.add('colab-df-spinner');
      try {
        const charts = await google.colab.kernel.invokeFunction(
            'suggestCharts', [key], {});
      } catch (error) {
        console.error('Error during call to suggestCharts:', error);
      }
      quickchartButtonEl.classList.remove('colab-df-spinner');
      quickchartButtonEl.classList.add('colab-df-quickchart-complete');
    }
    (() => {
      let quickchartButtonEl =
        document.querySelector('#df-7a256f2d-4de4-4a0f-bbc2-211eb7c831fd button');
      quickchartButtonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';
    })();
  </script>
</div>

    </div>
  </div>





```python
### Kvitter oss med kolonnene vi ikke bruker ###
df = df.drop(['nameOrig', 'nameDest', 'Unnamed: 0', 'Date of transaction', 'type', 'branch', 'Acct type', 'Time of day'], axis = 1)
```


```python
import numpy as np

# Sjekker etter NAN verdi i vår response.
nan_indices = np.isnan(df['isFraud'])

# Summer antall NAN verdier
num_nan_values = np.sum(df['isFraud'])

# Print resultatet
if num_nan_values > 0:
    print(f"There are {num_nan_values} nan values in df['isFraud'].")
else:
    print("There are no nan values in df['isFraud'].")
```

    There are 68.0 nan values in df['isFraud'].



```python
### Kvitter oss med NAN values ###

# Finn indeksene av rader med NAN verdier i responsen
nan_indices = np.isnan(df['isFraud'])

# Kvitter oss med disse radene
df = df[~nan_indices]
```


```python
# Ser på hvilke features vi har nå
df.columns
```




    Index(['step', 'amount', 'oldbalanceOrg', 'newbalanceOrig', 'oldbalanceDest',
           'newbalanceDest', 'unusuallogin', 'isFlaggedFraud', 'isFraud'],
          dtype='object')




```python
# Fjern rader med NaN-verdier fra hele DataFrame
df = df.dropna()
```


```python
### Gjør om type-format til variabelen til modellen Random Forests liker:-) ###

df.loc[:, 'step'] = df['step'].astype(int)
#df.loc[:, 'type'] = df['type'].astype('category')
#df.loc[:, 'branch'] = df['branch'].astype('category')
df.loc[:, 'amount'] = df['amount'].astype(float)
df.loc[:, 'oldbalanceOrg'] = df['oldbalanceOrg'].astype(float)
df.loc[:, 'newbalanceOrig'] = df['newbalanceOrig'].astype(float)
df.loc[:, 'oldbalanceDest'] = df['oldbalanceDest'].astype(float)
df.loc[:, 'newbalanceDest'] = df['newbalanceDest'].astype(float)
df.loc[:, 'unusuallogin'] = df['unusuallogin'].astype(int)
df.loc[:, 'isFlaggedFraud'] = df['isFlaggedFraud'].astype(int)
# Fill NaNs with a placeholder value
#df['Acct type'].fillna('Unknown', inplace=True)
#df['Time of day'].fillna('Unknown', inplace=True)

# Convert 'Acct type' and 'Time of day' to category
#df['Acct type'] = df['Acct type'].astype('category')
#df['Time of day'] = df['Time of day'].astype('category')

df.loc[:, 'isFraud'] = df['isFraud'].astype(int)
```


```python
# Her deler vi opp data i uavhengig og avhengig variabler
X = df.drop(columns=['isFraud'])  # Ta bort responsen fra uavhengig variabelen
y = df['isFraud']                 # Avhengig variabel/responsen, Fraud (1) eller NotFraud (0)

# sklearn inneholder bibliotek, gode for å splitte data inn i test og treningsdata
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
```


```python
# La oss se på fordelingen av antall svindel i datasettet (i både trening og test settet.)
import matplotlib.pyplot as plt

# Create subplots
fig, (ax1, ax2) = plt.subplots(1, 2, figsize=(16, 6))

# Plot histogram of y_train
ax1.hist(y_train, bins=10, alpha=0.75, color='blue')
ax1.set_title('Distribution of y_train')
ax1.set_xlabel('Classes')
ax1.set_ylabel('Frequency')
ax1.grid(True)

# Plot histogram of y_test
ax2.hist(y_test, bins=10, alpha=0.75, color='green')
ax2.set_title('Distribution of y_test')
ax2.set_xlabel('Classes')
ax2.set_ylabel('Frequency')
ax2.grid(True)

# Show plot
plt.show()
```


    
![png](For1_files/For1_45_0.png)
    


## **Hjemmeoppgave**
Som vi ser fra plottet over har vi det som kalles *ubalansert* eller *skjevt* datasett (eng: **imbalanced dataset**), og referer til situasjonen der klasser i datasettet har betydelig ulik forekomst/antall observasjoner. For dette eksempelet, som er et binært klassifiseringsproblem, ser vi at $1$ ("isFraud") skjer mye sjeldnere i vårt datasett enn verdien $0$.

En mulighet er å legge til flere eksempler i minoritetsklassen, for eksempel ved hjelp av teknikker som SMOTE (Synthetic Minority Over-sampling Technique). Under er et eksempel!

```python
# Prøv å fikse problemet med ubalansert datasett vha SMOTE
from imblearn.over_sampling import SMOTE

smote = SMOTE(sampling_strategy='minority')
X_resampled_train, y_resampled_train = smote.fit_resample(X_train, y_train)
```

Her ser vi at det er en klar overvekt i antall **ikke-svindel** hendelser.


```python
y_test.value_counts()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>count</th>
    </tr>
    <tr>
      <th>isFraud</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0.0</th>
      <td>2010</td>
    </tr>
    <tr>
      <th>1.0</th>
      <td>14</td>
    </tr>
  </tbody>
</table>
</div><br><label><b>dtype:</b> int64</label>



### Under er eksempelbruk av maskinlæringsteknikken **XGBOOST**
Vi kommer ikke til å bruke tid på å gå inn på teorien bak XGBoost, vit at *boosting* (*boosted trees*) er en ofte brukt teknikk, som har en fordel at de er relativt lett å programmere. Denne teknikken kan dere velge å bruke i prosjektet i kurset.


```python
import xgboost as xgb
from sklearn.metrics import classification_report, confusion_matrix

# Lag en Boosting model - ved å bruke XGBoost.
model = xgb.XGBClassifier(use_label_encoder=False, eval_metric='logloss', enable_categorical=True)

# Trene modellen
model.fit(X_train, y_train)

# Gjøre prediksjoner
y_pred = model.predict(X_test)
```

    /usr/local/lib/python3.10/dist-packages/xgboost/core.py:158: UserWarning: [08:29:43] WARNING: /workspace/src/learner.cc:740: 
    Parameters: { "use_label_encoder" } are not used.
    
      warnings.warn(smsg, UserWarning)



```python
conf_mat_boosting = confusion_matrix(y_test, y_pred)
conf_mat_boosting
```




    array([[2010,    0],
           [   7,    7]])




```python
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.metrics import confusion_matrix

# Finner confusion matrix. som eksempel over
conf_mat_nice = confusion_matrix(y_test, y_pred)

# Plot confusion matrix
plt.figure(figsize=(6, 4))
sns.heatmap(conf_mat_nice, annot=True, fmt='d', cmap='Blues', xticklabels=['Predicted Negative', 'Predicted Positive'], yticklabels=['Actual Negative', 'Actual Positive'])
plt.xlabel('Predicted')
plt.ylabel('Actual')
plt.title('Confusion Matrix')
plt.show()
```


    
![png](For1_files/For1_52_0.png)
    


Over her ser vi det vi kaller en *confusion matrix*, og dette kan vi bruke til å si noe om hvor godt/dårlig vår modell har gjort det.

Her har vi ikke brukt noe valideringsdata, kun training og test-sett. Det kommer av at her brukte vi *boosting* (en teknikk som bruker *beslutningstrær*) som har færre *hyperparametere* enn for eksempel nevrale nettverk.

**Tenkte å forklare kort hva vi har gjort i mer detalj her!**

# Mer om confusion matrix - og metrikker vi kan få ut av det

## Nøyaktighet (Accuracy)
Formel: $\frac{TP + TN}{TP + TN + FP + FN}$

Tolkning: Totalt antall korrekte prediksjoner delt på totalt antall observasjoner.

---

## Presisjon (Precision)
Formel: $\frac{TP}{TP + FP}$

Tolkning: Andel av positive prediksjoner som er korrekte.

---

## Gjenkalling (Recall/Sensitivitet)
Formel: $\frac{TP}{TP + FN}$

Tolkning: Andel av faktiske positive tilfeller som korrekt er identifisert som positive.

---

## F1-Score
Formel: $2 \cdot \frac{\text{Precision} \cdot \text{Recall}}{\text{Precision} + \text{Recall}}$

Tolkning: Harmonisk gjennomsnitt av presisjon og gjenkalling.

---

## Spesifisitet (Specificity)
Formel: $\frac{TN}{TN + FP}$

Tolkning: Andel av faktiske negative tilfeller som korrekt er identifisert som negative.

---

## Falsk positiv rate (FPR)
Formel: $\frac{FP}{FP + TN}\$

Tolkning: Andel av faktiske negative tilfeller som feilaktig er klassifisert som positive.

---

## Falsk negativ rate (FNR)
Formel: $\frac{FN}{FN + TP}$
  
Tolkning: Andel av faktiske positive tilfeller som feilaktig er klassifisert som negative.






# Oppgave
Så med disse metrikkene over - er egentlig vår modell bra her?

## **Overfitting**
$\textit{Overfitting}$ eller over-tilpasning skjer når en maskinlæringsmodell "lærer" noise og tilfeldige fluktasjoner i treningsdata'en - og ikke den **underliggende** mønsteret i data'en. Dette gjør at modellen kan være fryktelig god på treningsdata'en, men generaliserer dårlig til ny, ikke-sett data. Dette vil kunne bli problem hvis man skal ta i bruk maskinlæringsmodeller i den virkelige verden.

### Viktige konsepter:
1. **Underfitting**: Når modellen er for *simpel* til å fange data'en underliggende struktur. F.eks. å bruke lineær regresjon for å predikere været.

2. **Overfitting**: Når modeller er for *kompleks* og fanger opp noise i treningsdataen.

3. **Generalisering**: Handler om modellens evne til å gjøre det bra på ny, ikke-sett data (test-sett).

![Eksempel](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*_7OPgojau8hkiPUiHoGK_w.png)

## Eksempel på overfitting
Hvis vi prøver å lage en confusion matrix av modellen vår, hvor vi tester modellen på **treningsdataen**.

### Før du kjører de neste to cellene, hva forventer du at utfallet er?


```python
# Gjøre prediksjoner, men denne gang på treningsdata'en (ikke test-data'en)
y_pred_on_train = model.predict(X_train)
```


```python
conf_mat_boosting = confusion_matrix(y_train, y_pred_on_train)
conf_mat_boosting
```




    array([[8042,    0],
           [   1,   53]])



## **Hvorfor er denne confusion matrixen så "bra"?**
Skriv hva du tror her:

## **Årsaker til overfitting**
* **Kompleks modell**: Det er mange måter en modell kan være for kompleks på, men for mange variabler (features), dype nettverk og høy-ordens polynomer er noen årsaker.
* **Mangel på data**: Begreset mengde data gjør det lettere for en model å *memorisere*, i steden for å *generalisere*.
* **Mangel på regularisering**: Hvis man mangler teknikker for å straffe (eng: *penalize*) veldig komplekse modeller.
* oooog, mange fler. Dette skal vi få sett mer hands-on på gjennom kurset.

### **Hvordan kan vi spotte overfitting?**
* **Stor varians i resultat**:
  * Store forskjell mellom trening og validering/test-sett sin nøyaktighet (eng: *accuracy*).
  * Hvis man bruker ulike *random.seed's* og får veeeldig ulike outputs.

## **Teknikker for å forhindre overfitting**
* **Kryss-validering**: Gjør for en mer robust modell ved å validere over flere delmengder (subsets) av datasettet.
![](https://www.mathworks.com/discovery/cross-validation/_jcr_content/mainParsys/image.adapt.full.medium.jpg/1718274806179.jpg)

* **Pruning (for decision trees)**: Kvitte seg med *noder* som ikke gir noe særlig informasjon.
![](https://upload.wikimedia.org/wikipedia/commons/thumb/2/23/Before_after_pruning.png/1000px-Before_after_pruning.png)

* **Dropout (for nevrale nettverk)**: Tilfeldig *dropping* av nevroner mens det trenes.
![](https://www.researchgate.net/profile/Amine-Ben-Khalifa/publication/309206911/figure/fig3/AS:418379505651712@1476760855735/Dropout-neural-network-model-a-is-a-standard-neural-network-b-is-the-same-network.png)

* **Early stopping**: Slutt å tren nevrale nettverket når modellen slutter å gjøre det bedre når det testes på validerings-settet.


### **Overfitting i økonomi**
Overfitting er et kjent problem i økonomi, f.eks. i prediksjon av aksjekurser. Har man en modell som passer treningsdata'en perfekt når det gjelder aksjer - er det fort gjort at vi snakker om overfitting.

#### **Praktiske tips**
* Bruk enkle modeller i starten, og gradvis øk kompleksiteten.
  * Hvordan gjøre lineær regresjon det her, deretter ta beslutningstrær, xgboost og nevrale nettverk.
* Bruke *domene-kunnskap* for å velge relevante features.
* Valider modeller, innføre *penalties* og vær kritisk til *for gode* resultater.

---


# **Oppgaver**
Under her er det gitt et par oppgaver. Ingen obligatoriske, men nyttige for egen forståelse av fundamentale konsepter i maskinlæring. I tillegg, ingen dårlig trening mot en muntlig eksamen.

## Oppgave 1
Det er gitt en *hjemmeoppgave* lenger oppe i notebook'en. Den omhandler ubalanserte datasett, og hvordan vi kan takle det ved hjelp av SMOTE. Gjør denne, og jobb gjennom eksempelet med ```Fraud.csv``` datasettet.

## Oppgave 2
Utledningsoppgave lenger oppe i notebook'en.

Utled $$E[(f(X) + \epsilon - \hat{Y})^2]$$ for å vise at det er lik $$[f(X)-\hat{f}(X)]^2 + Var(ϵ)$$

## Oppgave 3
Forklar med egne ord, hva som er forskjellen mellom inferens og prediksjon.

## Oppgave 4
Forklar med egne ord, hva irreducible error er. Gjerne ved hjelp av matematikk.

## Oppgave 5
Hva er forskjellen mellom regresjon og klassifikasjon.

## Oppgave 6
Hva er overfitting, og hvor kan man støte på overfitting-problemer?


```python

```
