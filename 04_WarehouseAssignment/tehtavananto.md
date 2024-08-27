# Warehouse

Tee jokaiselle metodille alla olevat testit. Koita miettiä laajasti erilaisia testitapauksia.

## Tee alla olevat yksikkötestit:
Sivuuta tässä vaiheessa metodien sisältö ja sen mahdolliset virheet, vaan kirjoita testit niin kuin ne sinusta olisi järkevä toimia. 
Kun kaikki testit on tehty, niiden ei pitäisi mennä läpi, koska koodissa on epäjohdon mukaisuuksia. Korjaa seuraavaksi koodia niin että se toimii sinun testien määrittämällä tavalla. [Test first](https://www.soapui.org/learn/functional-testing/test-first/) Lopussa kaikkien testien pitäisi mennä läpi.  
 Keksitkö metodeille nyt uusia testejä joista se ei vielä pääse läpi. 

AddToStock:

- Lisää esine, jolla on määränä kunnollinen positiivinen arvo.   
- Lisää esine, jolla on määränä arvo nolla.
  - _Assert vaihtoehdot:_
    - _esine löytyy listalta ja määrä on nolla_  
    - _esinettä ei lisätä listaan_
   Eli tässä kohti määrittelet kuinka valmiin sovelluksen kuuluisi toimia tässä tilanteessa.   
- Lisää esine, jolla on negatiivinen arvo.
  - Assert: virhe, määränä nolla tms...   
- Lisää esine, jolla on mielestäsi kohtuuttoman suuri arvo.

InStock:

- Tarkista onko esinettä varastossa positiivinen määrä.
- Tarkista onko varastossa esine määrällä nolla.
- Tarkasta voiko esinettä olla varastossa negatiivinen määrä.
  - Tuotetta on lisätty negatiivinen määrä
  - Tuotetta on otettu varastosta enemmän kuin sitä on

TakeFromStock:

- Ota oikeanlainen määrä esineitä varasosta.
- Ota viimeinen esine varastosta.
- Ota isompi määrä kuin varastossa on tavaraa.
- Ota varastosta negatiivinen määrä.
- Ota varastosta tavara, jota ei ole olemassa.
- Ota varastosta nolla esinettä.

StockCount:

- Tarkista esineiden lukumäärä esineeltä, jota on positiviinen määrä.
- Tarkista esineiden määrä, joita on nolla kappaletta.
- Tarkista esineiden lukumäärä, joita on negatiivinen määrä.

## Funktionaaliset testit
Tee omia testejä, joilla varmistat, että asiat toimivat yhdessä. Alla esimerkkejä:

- Tee testi, joka testaa, että jos samaa esinettä lisätään uudestaan, niin esineitä on oikea määrä.
- Tee testi, jossa lisäät varastoon esineen ja varmista, että liian isolla määrällä metodi heittää poikkeuksen.
- Tee testi, jossa lisäät esineen varastoon, katsot, että esine on varastossa, poistat esineen ja varmistat, että kaikki meni oikein.

