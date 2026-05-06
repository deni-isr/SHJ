# Kirjoituskonekauppa Pärnänen & Pojat 

Tämä projekti on toteutettu osana julkaisujärjestelmien kurssia. Tarkoituksena oli testata ja rakentaa **Headless CMS** -ratkaisu, jossa taustajärjestelmä (backend) ja käyttöliittymä (frontend) on täysin erotettu toisistaan. 

Valitsin julkaisujärjestelmäksi **Strapin** (versio 5).

## Tekniikat
* **Backend (CMS):** Strapi v5
* **Tietokanta:** SQLite
* **Frontend:** Vanilla HTML, CSS ja JavaScript

## Tietorakenne (Content Types)
Strapiin on mallinnettu dynaaminen tietorakenne:
* **Single Types (Yksittäiset rakenteet):**
  * `Etusivu` (Sivuston otsikko, esittelyteksti ja Hero-kuva)
  * `Yhteystiedot` (Yrityksen tarina ja yhteystiedot)
* **Collection Types (Kokoelmat):**
  * `Palvelu` (Pääkategoriat: Huolto, Myynti, Entisöinti. Sisältää nimen ja kuvauksen.)
  * `Tuote` (Yksittäiset kirjoituskoneet, esim. Olympia SM3 ja Remington. Yhdistetty **relaatiolla** (Relation) `Palvelu`-kategoriaan.
