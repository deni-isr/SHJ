# Kirjoituskonekauppa Pärnänen & Pojat - CMS-testaus

Tämä projekti on toteutettu osana julkaisujärjestelmien kurssia. Tarkoituksena oli testata ja rakentaa **Headless CMS** -ratkaisu, jossa taustajärjestelmä (backend) ja käyttöliittymä (frontend) on täysin erotettu toisistaan. 

Valitsin julkaisujärjestelmäksi **Strapin** (versio 5).

## 🛠 Tekniikat
* **Backend (CMS):** Strapi v5 (Node.js)
* **Tietokanta:** SQLite (lokaali testiympäristö)
* **Frontend:** Vanilla HTML, CSS (iOS-tyylinen moderni design) ja JavaScript (Fetch API).

## 🗂 Tietorakenne (Content Types)
Strapiin on mallinnettu dynaaminen tietorakenne:
* **Single Types (Yksittäiset rakenteet):**
  * `Etusivu` (Sivuston otsikko, esittelyteksti ja Hero-kuva)
  * `Yhteystiedot` (Yrityksen tarina ja yhteystiedot)
* **Collection Types (Kokoelmat):**
  * `Palvelu` (Pääkategoriat: Huolto, Myynti, Entisöinti. Sisältää nimen ja kuvauksen.)
  * `Tuote` (Yksittäiset kirjoituskoneet, esim. Olympia SM3 ja Remington. Yhdistetty **relaatiolla** (Relation) `Palvelu`-kategoriaan.)

## 🖥 Frontend-toteutus
Koska Strapi on Headless CMS, se ei tarjoa valmista ulkoasua, vaan jakaa datan JSON-muodossa REST API:n kautta. Tein projektia varten kolme HTML-sivua, jotka hakevat ja esittävät tämän datan dynaamisesti:
1. `index.html` - Etusivu (Hero-osio, palveluiden pikanäkymä ja yhteystiedot).
2. `palvelut.html` - Palvelukatalogi (Dynaaminen listaus kategorioista ja niihin linkitetyistä tuotteista).
3. `tuote.html` - Yksittäisen tuotteen/palvelun tarkempi esittelysivu (hakee datan URL-parametrin ID:n perusteella).

## 🎥 Esittelyvideo ja kuvakaappaukset
Katso projektin esittelyvideo ja demonstrointi tästä:
👉 [LISÄÄ LINKKI YOUTUBE-VIDEOON TAI GOOGLE DRIVEEN TÄHÄN]

*(Vaihtoehtoisesti voit lisätä kuvakaappauksia Strapin hallintapaneelista tähän alle)*

## 🚀 Käyttöönotto (lokaali testi)
1. Käynnistä Strapi-palvelin komennolla `npm run develop` projektin juuressa (varmista, että portti 1337 on auki).
2. Avaa `index.html` selaimessa. Frontend hakee datan automaattisesti lokaalista API:sta ja renderöi sivuston.
