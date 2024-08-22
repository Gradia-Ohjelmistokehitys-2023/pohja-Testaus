

## Tehtävä 2

1. Toistaiseksi esitellyt testit ovat ns. hyvän päivän testejä (fair weather tests). Ne testaavat metodien toimintaa kun syötteet ovat kunnossa. Mitä jos vaikkapa Debit-funktiota kutsutaankin negatiivisella saldolla. Funktion pitäisi heittää keskeytys tässä tilanteessa. Kirjoita yksikkötesti joka yrittää syöttää negatiivisen saldon Debit funktiolle ja tarkistaa, että funktio heittää ArgumentOutOfBounds keskeytyksen.

Vinkki: Etsi esimerkkiä "Assert.ThrowsException"-tarkistuksesta.

Linkki:
https://docs.microsoft.com/en-us/visualstudio/test/walkthrough-creating-and-running-unit-tests-for-managed-code?view=vs-2022


Siirry seuraavaksi **[tehtävän toiseen vaiheeseen - Refaktorointi](2_Refaktorointi.md)**



