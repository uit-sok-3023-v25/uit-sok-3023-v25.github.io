{% include navbar.html %}{% include top-box.html %}
# Prosjekt - Maskinlæring for økonomer
I dette kurset skal vi ha et maskinlæringsprosjekt, hvor dere vil bli utfordret på å lage egne maskinlæringsmodeller. Dere skal gjennomføre arbeidet **enten** alene, eller i gruppe på to.

## Oppgave 🎯📊
Dere skal utforske og sammenligne maskinlæringsmodeller på et selvvalgt eller anbefalt datasett. Målet er å analysere hvordan ulike teknikker presterer på problemstillingen dere velger.  

### 🔍 Maskinlæringsteknikker  
Dere skal bruke minst én **dyplæringsteknikk** som:  
- Nevrale nettverk  
- CNN (Convolutional Neural Networks)  
- LSTM (Long Short-Term Memory)  
- Whisper-modellen 
  
Alle teknikkene over, går under feltet *dyplæring*. Dyplæring **skal** inkluderes i prosjektet. 

I tillegg kan dere sammenligne disse med enklere modeller:  
- Lineær regresjon  
- Logistisk regresjon  
- Beslutningstrær (Decision Trees, Random Forests, Boosting)
- Dere har lov til å introdusere andre teknikker dere finner på egen hånd, **om dere vil**.

**Husk:** Mer komplekse modeller er ikke alltid best! Dere skal evaluere modellene basert på deres ytelse og relevans for problemstillingen.  

### Krav til prosjektet
Jeg har funnet frem en del eksempel-datasett dere *kan* (les kan, **ikke må**) bruke. De finner dere lenke til nederst på siden her.

Dere står fritt til å velge datasett selv, som dere finner på Internett. Det kan f.eks. være fra Yahoo finance, Kaggle, SSB eller andre sider som har data. Uansett hvilke data dere bruker, så **må** dere oppgi dets kilde!

Det er ganske åpne rammer for oppgaven, men oppgaven har følgende krav:

1. **Datasett og problemstilling**
   - Velg et datasett (selv eller fra gitte eksempel-datasett).
   - Beskriv datasettet, dets kilde og hva dere ønsker å analysere.
    
2. **Dataforståelse og preprosessering**  
   - Utforsk datasettet (statistikk, visualiseringer).  
   - Gjør nødvendige transformasjoner (håndtere manglende verdier, normalisering, etc.).  

3. **Implementasjon av modeller**  
   - Bruk minst én dyplæringsteknikk og sammenlign gjerne med andre modeller.  
   - Koden skal være godt kommentert og forklart!!!  

4. **Evaluering av modellene**  
   - Bruk relevante evalueringsmetrikker som MSE, RMSE, Accuracy, F1-score, etc.
       * Her er lista lang, og opp til dere hvilke metrikk som gir mest mening å benytte seg av.  
   - Sammenlign modellene basert på ytelse og generaliseringsevne.  

5. **Matematisk beskrivelse av modellene**  
   - Bruk LaTeX i Markdown for å forklare de matematiske konseptene.  
   - For eksempel kan input-lag til første skjulte lag i et nevralt nettverk beskrives noe som dette:  
     $\mathbf{a^{(1)}} = \sigma(\mathbf{W} \mathbf{a^{(0)}} + \mathbf{b})$

6. **Konklusjon og refleksjon**  
   - Hvilken modell presterte best? Hvorfor?  
   - Hvordan kan modellen forbedres?  
   - Hva kan resultatene brukes til i praksis?  

7. **Format og innlevering**  
   - Prosjektet skal leveres som en **Jupyter Notebook (`.ipynb`)**.  
   - Det skal kunne kjøres i **Google Colab** uten eksterne avhengigheter.  
   - Husk å oppgi en **kildeliste** for datasett og litteratur.  

* God beskrivelse av datasettet deres, og hvor det kommer fra (kilde).
* Kode, som er kommentert og at dere forklarer hva den gjør.
* Dere skal ha en problemstilling knyttet til et datasett. 
* Gjerne bruk flere læringsteknikker, for å se hvilke som gjør det best - ved å se på ulike evalueringsmetrikker.
* Dere **må** ha med noe *dyplæring*, altså nevrale nettverk, CNN, LSTM, ... 
* Det forventes at dere skriver LaTeX i Markdown delen av Google Colab (eller VSCode etc.), for å forklare hvilke modeller dere bruker. Dette skal ha et matematisk/statistisk fundament, slik kurset har, for at dere skal vise forståelse av modellen(e) dere bruker. I tillegg, at dere viser forståelse av hva output'et av modellen betyr, og hva det har å si for problemstillingen deres.
* Det er bare positivt om dere trekker inn andre læringsteknikker, metrikker etc. fra litteraturen.
* Oppgaven skal leveres i format av en ipynb (Jupyter Notebook), som skal kunne kjøres i Google Colab.
* Kildeliste skal oppgis.

### Vurdering av oppgaven
Denne semesteroppgaven teller 50% av karakteren. Dere vil få karakter A-F, og det vurderes ut i fra følgende:

* Forståelse av maskinlæring, teknikkene dere bruker, hva dere har gjort og hvordan dette **formidles** i oppgaven.
* Hvordan problemstillingen er besvart.
* Struktur og tydelig kommunikasjon
* Å vise breddeforståelse for fagfeltet maskinlæring, som gjerne trekker inn samfunnsøkonomi, teller positivt.
* Det er lov å bruke AI som et hjelpemiddel, for å få hjelp med koding, forståelse etc. - men ting **skal** være formidlet med egne ord. For det første er det juks, og for det andre, hvis man blir tatt, kan det føre til utestengelse. 

Lykke til! 🚀

### Datasett
Vi har en rekke datasett som er lastet opp eller linket til på GitHub, det finner dere [her](https://github.com/uit-sok-3023-v25/uit-sok-3023-v25.github.io/blob/main/data/README.md).
