# 01 MS Test Pankki

## Ms Test - Yksikkötestaus

Yksikkötestauksella tarkoitetaan lähdekoodiin kuuluvien yksittäisten osien kuten luokkien ja niiden tarjoamien metodien testaamista. Luokkien ja metodien rakenteen suunnittelussa käytettävän ohjesäännön — jokaisella metodilla ja luokalla tulee olla yksi selkeä vastuu — noudattamisen tai siitä poikkeamisen huomaa testejä kirjoittaessa. Mitä useampi vastuu metodilla on, sitä monimutkaisempi testi on. Jos laaja sovellus on kirjoitettu yksittäiseen metodiin, on testien kirjoittaminen sitä varten erittäin haastavaa ellei jopa mahdotonta. Vastaavasti, jos sovellus on pilkottu selkeisiin luokkiin ja metodeihin, on testienkin kirjoittaminen suoraviivaista.

## Tehtävä 1

1. Tee alla olevan linkin ohjeiden mukaan pankkisovellus ja siihen testi. Varmista että ymmärrät mitä kopioimasi koodi tekee. Korjaa lopuksi ohjeiden mukaan koodiin tahallisesti kirjoitettu virhe.
2. Credit-metodia ei testata lainkaan. Lisää yksikkötesti joka tarkistaa että Credit-metodi toimii oletetulla tavalla.

* https://learn.microsoft.com/en-us/visualstudio/test/walkthrough-creating-and-running-unit-tests-for-managed-code?view=vs-2022.

  Kyseistä tehtävää jatkokehitetään tehtävässä kaksi.

### Dokumentaatiota
* https://learn.microsoft.com/en-us/visualstudio/test/unit-test-basics?view=vs-2022#write-your-tests
* https://learn.microsoft.com/en-us/dotnet/core/testing/unit-testing-best-practices

*Huom!* Voit tehdä tehtävät yksi ja kaksi samaan solutiooniin. Nimeä Program luokka uudelleen esimerkiksi MathOperations luokaksi. Tee jokaiselle eri operaatiolle oma metodi. Lisää solutioniin MS-test projekti, johon lisäät referenssiksi alkuperäisen projektisi.

Kun teet metodiin testejä, niin testaa yhtä asiaa kerrallaan. Jos löydät toisen tapauksen, niin tee sille uusi testi.
Testaa tehtävissä seuraavia asioita:
Hyvän päivän "ns. good weather" tapaus eli, jos ohjelma laskee yhteen 2+2, niin testin oletustulos on 4 ja testit menevät läpi.
Huono tapaus eli "ns. bad weather", jos lasketaan 2-3 = -5, niin tulee virhe."Ei ole oikein."
Testaa lukujen rajat, koska esimerkiksi neliöjuuri ei voi olla negatiivisesta luvusta. 

Tee tehtäviin 1-2 VÄHINTÄÄN 3 testitapausta per kohta ja löytyykö tiedostojen käsittelyyn neljättä testitapausta. Tee tehtävän kaikki metodit samaan projektiin.

## 1. Lukujen testaamista
 1. Tee metodi, joka ottaa parametrina kaksi kokonaislukua(int), vähentää ne toisistaan ja palauttaa lopputuloksen. Luvut voivat olla negatiivisia. Tee ohjelmalle yksikkötestit.
 2. Tee metodi, joka ottaa syötteenä kokonaisluvun. Sallituin suurin parametrin arvo, jonka ohjelma käsittelee on 100. Ohjelma palauttaa luvun toisen potenssin (n^2). Tee ohjelmalle yksikkötestit.
 3. Tee metodi, joka ottaa parametrinä kokonaisluvun. Ohjelma palauttaa luvun neliöjuuren. Tee ohjelmalle yksikkötestit.

## 2. Etsi pienin, suurin, laske keskiarvo

1. Tee metodi, joka etsii double tyyppisestä listasta (List<double>) pienimmän arvon ja palauttaa sen. Tee itse pienimmän arvon etsiminen. List.Min metodin käyttö on kielletty. Tee ohjelmalle yksikköstestit.
2. Tee metodi, joka etsii int tyyppisestä listasta (List<int>) suurimman arvon ja palauttaa sen. Tee itse suurimman arvon etsiminen. List.Max metodin käyttö on kielletty. Tee ohjelmalle yksikköstestit. 
3. Tee metodi, joka laskee float tyyppissen listan (List<float>) lukujen keskiarvon ja palauttaa sen. Tee ohjelmalle yksikköstestit. 

## 3. Tiedostojen testaaminen

Lisää prjektiin uusi luokka File.
Tehtävänäsi on suunnitella kaksi testiä lisää alla olevalle ohjelmalle. Nyt testataan, onko listassa yhtään alkiota. Mitä muita testejä keksit?
```c#

using System.Reflection;

namespace TestFiles
{
    public class File
    {

        public static void Main(string[] args)
        {
        }

        private static void PrintFile(List<string> systemConfig)
        {
            foreach (var item in systemConfig)
            {
                Console.WriteLine(item);
            }
        }

        public static List<string> ReadFile(List<string> fileContent, string directory, string filePath)
        {
       
            StreamReader reader = new StreamReader(directory + filePath);
            try
            {
                do
                {
                    fileContent.Add(reader.ReadLine());
                }
                while (reader.Peek() != -1);
            }
            catch (FileNotFoundException e)
            {
              throw;
            }

            finally
            {
                reader.Close();
            }
            return fileContent;
        }
    }
}
Mallitesti:

using Microsoft.VisualStudio.TestPlatform.TestHost;
using TestFiles;
namespace FileTests
{
    [TestClass]
    public class FileUnitTests
    {
        [TestMethod]
        public void ReadFile_ReturnsListOfSettings_IfFileIsNotEmpty()
        {
            //Arrange
            List<string> systemConfig;
            string winDir = "C:\\Windows";
            string path = "\\system.ini"
            //Act
            systemConfig = Files.ReadFile(systemConfig, windir, path);
            //Assert
            Assert.IsTrue(systemConfig.Count < 0); //tarkoituksella väärin. Korjaa.

        }

    }
}
```
