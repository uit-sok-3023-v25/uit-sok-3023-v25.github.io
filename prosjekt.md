{% include navbar.html %}{% include top-box.html %}
# Prosjekt
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

I tillegg, kan dere sammenligne dyplæring med mindre komplekse modeller som:  
- Lineær regresjon  
- Logistisk regresjon  
- Beslutningstrær (Decision Trees, Random Forests, Boosting)
- Dere har lov til å introdusere andre maskinlæringsteknikker dere finner på egen hånd, **om dere vil**.

**Husk:** Mer komplekse modeller er ikke alltid best! Dere skal evaluere modellene basert på deres ytelse og relevans for problemstillingen.  

### 📂 Krav til prosjektet
Jeg har funnet frem en del eksempel-datasett dere *kan* (les kan, **ikke må**) bruke. De finner dere lenke til nederst på siden her.

Dere står fritt til å velge datasett selv, som dere finner på Internett. Det kan f.eks. være fra Yahoo finance, Kaggle, SSB eller andre sider som har data. Uansett hvilke data dere bruker, så **må** dere oppgi dets kilde!

Det er ganske åpne rammer for oppgaven, men oppgaven har følgende krav:

1. **Datasett og problemstilling**
   - Velg et datasett (selv eller fra gitte eksempel-datasett).
   - Beskriv datasettet, dets kilde og hva dere ønsker å analysere.
    
2. **Dataforståelse og preprosessering**  
   - Utforsk datasettet (statistikk, visualiseringer, etc.).  
   - Gjør nødvendige transformasjoner (håndtere manglende verdier, normalisering, etc.).  

3. **Implementasjon av modeller**  
   - Bruk minst én dyplæringsteknikk og sammenlign gjerne med andre modeller (som nevnt over).
       * Det er bare positivt om dere gjør egne valg, og gjør en grundig analyse.  
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
   - Også videre, også videre. 

7. **Format og innlevering**  
   - Prosjektet **skal** leveres som en **Jupyter Notebook (`.ipynb`)**.  
   - Det skal kunne kjøres i **Google Colab** uten eksterne avhengigheter.
   - Legg ved datasettet!
   - Husk å oppgi en **kildeliste** for datasett og litteratur, bruk APA 7 referansestil. 

### 🎙️ Presentasjon av prosjektbeskrivelse
Dere skal presentere prosjektet før det starter ordentlig. Dette er for å demonstrere hva dere har tenkt til å gjennomføre, fremdriftsplan og hvilke data dere velger å se på. Dette skjer fredag 28. februar 2025, mellom 08.15-14.00 (Skulle noen ønske *tidligere*, så ta det opp med fagansvarlig i forelesning/mail).

- Presentasjonen skal være i 5-10 minutter, etterfulgt av 5 minutter med spørsmål/diskusjon.
- Dere skal vise frem valgte data, problemstilling og initielle tanker for prosjektet. Dette kan presenteres ved hjelp av Notebooks, PowerPoint eller en kombinasjon av PowerPoint/Notebooks.
- Målet med presentasjonen er at dere har satt dere et passende mål, problemstilling, datasett og eventuelle spørsmål.
- Vurderes som Godkjent/Ikke-godkjent.

### 📚 Vurdering av oppgaven
Denne semesteroppgaven teller 50% av karakteren. Dere vil få karakter A-F, og det vurderes ut i fra følgende:

* Forståelse av maskinlæring, teknikkene dere bruker, hva dere har gjort og hvordan dette **formidles** i oppgaven.
* Hvordan problemstillingen er besvart.
* Struktur og tydelig kommunikasjon
* Å vise breddeforståelse for fagfeltet maskinlæring, som gjerne trekker inn samfunnsøkonomi, teller positivt.
* Det er lov å bruke AI som et hjelpemiddel, for å få hjelp med koding, forståelse etc. - men ting **skal** være formidlet med egne ord. For det første er det juks, og for det andre, hvis man blir tatt, kan det føre til utestengelse.
* Dere har god tid på prosjektet, og skal leveres 7. mai kl. 14:00 på WiseFlow (lenke kommer).

**Husk:** Det er ikke om accuracy til modellen er 100% eller ikke, som bestemmer om dere har levert en god oppgave. Det er ikke alltid mulig å få det til på test data, da vi ikke alltid har perfekt data. En god oppgave tar hensyr til kravene, viser forståelse, refleksjon og at dere tar i bruk maskinlæring på en fornuftig måte.

Lykke til! 🚀

### Datasett
Vi har en rekke datasett som er lastet opp eller linket til på GitHub, det finner dere [her](https://github.com/uit-sok-3023-v25/uit-sok-3023-v25.github.io/blob/main/data/README.md).
