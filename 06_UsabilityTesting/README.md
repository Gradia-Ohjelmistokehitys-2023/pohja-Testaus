# Käytettävyystestaus 

Arviointimenetelmä, jonka tarkoituksena on kehittää testattavan tuotteen käytettävyyttä.

Kuinka hyvin tuotetta pystytään käyttämään käyttöympäristössä loppukäyttäjän näkökulmasta. 

Käytettävyystestauksen osa-alueet: 

* testin suunnittelu 

* testin suorittaminen 

* analysointi ja raportointi 

Testin suunnittelussa luodaan kirjallinen testaussuunnitelma, jonka voi suorittaa henkilö joka ei ole aiemmin tutustunut testattavaan palveluun. 
 
Analysointi vaiheessa testin tulokset käydään läpi ja havaitut virheet raportoidaan ylös. Yleensä käytetään viisiportaista käytettävyysongelmien luokitteluasteikkoa:  

0 = Kyseessä ei ole käytettävyysongelma  
1 = Kosmeettinen käytettävyysongelma – korjataan, mikäli ylimääräistä aikaa   
2 = Vähäinen käytettävyysongelma – korjaamisella matala prioriteetti  
3 = Merkittävä käytettävyysongelma – korjaamisella korkea prioriteetti  
4 = Katastrofaalinen käytettävyysongelma – välttämätöntä korjata ennen kuin tuote julkaistaan  

Lue seuraavat artikkelit: 
- https://www.nngroup.com/articles/usability-test-checklist/ 
- https://www.nngroup.com/articles/task-scenarios-usability-testing/
- https://www.nngroup.com/articles/usability-testing-101/

  ### Esimerkki
### Käytettävyystesti Apple.com-sivustolle

**Tavoite**: Arvioida käyttäjäkokemusta ja navigoinnin helppoutta Apple.com-sivustolla, keskittyen keskeisiin tehtäviin, kuten tuotteiden selaamiseen, tukitietojen löytämiseen ja ostoksen tekemiseen.

---

#### **Osallistujaprofiili**
- **Demografia**: Osallistujat ovat tuttuja verkkoselailun ja verkko-ostosten tekemisen kanssa. Ikäjakauma on 18-60 vuotta, ja heillä on vaihtelevasti kokemusta Apple-tuotteista.
- **Tekninen osaaminen**: Sekalainen osaamistaso, aloittelijoista asiantuntijoihin.
- **Laitteet**: Testataan sekä työpöytä- että mobiililaitteilla.

---

#### **Scenario 1: Tuotteiden selaaminen**

**Tehtävä 1**: Etsi uusin iPhone-malli.

- **Ohjeet**: Navigoi sivustolla löytääksesi tietoja uusimmasta iPhone-mallista.
- **Onnistumiskriteerit**: Osallistuja löytää helposti iPhone-sivun ja tunnistaa tärkeät tiedot. Löytää tiedot:
  - Hinta
  - Pääkameran tarkkuus
  - Vesitiiviyden taso   
   
- **Havainnot**:
  - Kuinka nopeasti osallistuja löytää iPhone-osaston?
  - Onko mallien välillä navigoiminen vaikeaa?
  - Ovatko tuotetiedot selkeitä ja helposti ymmärrettäviä?

**Tehtävä 2**: Vertaa uutta iPhonea toiseen malliin.

- **Ohjeet**: Vertaa uusinta iPhone-mallia johonkin toiseen iPhone-malliin.
- **Onnistumiskriteerit**: Osallistuja löytää ja käyttää vertailutyökalua tehokkaasti. Osallistuja pystyy nimeämään kolme mielestään tärkeintä eroa.
- **Havainnot**:
  - Löytääkö osallistuja helposti vertailutoiminnon?
  - Kuinka intuitiivinen vertailuprosessi on?
  - Esitetäänkö tiedot päätöksenteon kannalta hyödyllisellä tavalla?

---

#### **Scenario 2: Tukitietojen löytäminen**

**Tehtävä 3**: Etsi tukisivu ja löydä ohjeet Apple ID -salasanan nollaamiseen.

- **Ohjeet**: Kuvittele, että olet unohtanut Apple ID -salasanasi. Navigoi sivustolla löytääksesi ohjeet salasanan nollaamiseen.
- **Onnistumiskriteerit**: Osallistuja löytää onnistuneesti ohjeet Apple ID -salasanan nollaamiseen ja seuraa niitä.
- **Havainnot**:
  - Kuinka helposti osallistuja löytää tukiosion?
  - Ovatko tukisisällöt hyödyllisiä ja helppoja seurata?
  - Onko hakutoiminto tehokas, jos sitä käytetään?

---

**Mittarit**:
- **Tehtävään käytetty aika**: Kuinka kauan kunkin tehtävän suorittaminen kestää.
- **Virheiden määrä**: Tehtävien aikana tehdyt virheet.
- **Tehtävien onnistumisprosentti**: Osallistujien prosenttiosuus, joka suorittaa tehtävät onnistuneesti.
- **Käyttäjätyytyväisyys**: Mitataan testin jälkeisellä kyselyllä.

---

**Lopulliset tuotokset**:
- Yhteenveto havainnoista.
- Parannusehdotukset tunnistettujen käytettävyysongelmien perusteella.
- Ehdotettu korjausten priorisointi käyttäjävaikutusten perusteella.


## Tehtävä: 

1. Tee käytettävyystestaus valitsemastastasi www-palvelusta. Mieti ainakin

    1. Mitä testataan 

    2. Miten testataan 

    3. Raportoi yksityiskohtaisesti löydetyt havainnot (Aihe, ongelma, korjaus) 

    4. Vastaavat www-palvelut (esittele kilpailijoiden palvelua) 

    5. Tee Yhteenveto .md tiedostona githubiin (lyhyesti omat löydökset / prioriteetti / ehdotettu korjaus)  

2. Tee käyttävyystestaus mobiilisovelluksesta. Voit valita valitsemasi www-sivun mobiilisovelluksen tai vapaavalintaisen sovelluksen.

   1. Mitä testataan 

   2. Miten testataan 

   3. Raportoi yksityiskohtaisesti löydetyt havainnot (Aihe, ongelma, korjaus) 

   4. Vastaavat www-palvelut (esittele kilpailijoiden palvelua) 

   5. Tee Yhteenveto .md tiedostona githubiin (lyhyesti omat löydökset / prioriteetti / ehdotettu korjaus)  
