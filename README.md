# Kirjoituskonekauppa Pärnänen & Pojat - CMS-testaus

Tämä projekti on tehty osana julkaisujärjestelmien kurssia. Valitsin testattavaksi järjestelmäksi **Strapin**, joka on suosittu avoimen lähdekoodin Headless CMS.

## Testiympäristö
- **CMS:** Strapi v4 (Node.js)
- **Tietokanta:** SQLite (lokaali testiympäristö)
- **Käyttöönotto:** Asennettu lokaalisti `npx create-strapi-app`-komennolla.

## Toteutus
Strapiin on luotu tehtävänannon mukainen tietorakenne (Content Types):
- **Single Types:** Etusivu (Hero-osio) ja Yhteystiedot (Footer-tiedot).
- **Collection Types:** Palvelut (Huolto, Myynti, Entisöinti).

Koska kyseessä on Headless CMS, järjestelmä ei generoi valmista HTML-sivua, vaan tarjoaa datan REST API:n kautta JSON-muodossa mitä tahansa frontend-sovellusta (esim. React, Vue) varten.

## Kuvakaappaukset
*(Lisää tähän kuvakaappaukset Strapin admin-paneelista ja selaimen API-näkymästä)*
