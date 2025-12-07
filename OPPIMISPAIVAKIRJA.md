# Oppimispäiväkirja – kooste

Tämä tiedosto kokoaa kaikki oppimispäiväkirjan osat yhdeksi kokonaisuudeksi.

---

## Oppimispäiväkirja 1 – Paikallinen Git

__Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet?__

Helppoa minulle oli Git:in peruskomennot ja niiden käyttäminen, koska olen git:tiä käyttänyt ohjelmistoprojekti 1 aikana todella paljon ja perusteet on siinä tullut hyvin esille. Myös uuden repositorion luominen ja yksinkertaisten tiedostojen tekeminen sujui melko helposti kiitos jo opitun tiedon.

Vaikeinta oli aluksi komentorivin käyttäminen ja hakemistoissa liikkuminen. Myös tietyt komennot oli uusia, mutta git onneksi neuvoo ja antaa ohjeet, että mitä ne tekee ja milloin niitä kanntattaa käyttää. Opin paljon lukemalla Gitin virheilmoituksia rauhassa, kokeilemalla uudestaan ja etsimällä syytä siihen, miksi komento ei toiminut.  Näin aloin hahmottaa paremmin muun muassa, että mikä on “working directory”, mikä on “staging”.

## Osiossa käyttämäni Git-komennot

| Komento | Kuvaus |
| --------| ------ |
| `git init` | Luo uuden Git-repositorion nykyiseen hakemistoon. |
| `git status` | Näyttää tiedostojen tilan: mitkä ovat muuttuneet, mitkä menossa seuraavaan commit:iin jne. |
| `git add tiedosto` | Lisää tiedoston muutokset staging-alueelle seuraavaa commit:ia varten. |
| `git commit -m "viesti"` | Tallentaa staged-muutokset versionhallintaan annetulla viestillä. |
| `git log` | Näyttää commit-historian. |
| `git clone URL` | Kloonaa olemassa olevan repositorion (esim. oppimispäiväkirjarepon) omalle koneelle. |
| `git branch` | Näyttää olemassa olevat haarat ja mikä haara on aktiivinen. |
| `git switch haara` | Vaihtaa toiseen haaraan (esim. master → tyylit tai main → paivakirja1). |
| `git reset` | Poistaa tiedostoja staging-alueelta (peruu `git add` -komennon vaikutuksen). |
| `git restore tiedosto` | Palauttaa tiedoston työtilassa viimeisimmän commitin mukaiseen tilaan. |
| `git revert <commit>` | Tekee uuden commitin, joka peruu jonkin aiemman commitin muutokset rikkomatta historiaa. |

---

## Oppimispäiväkirja 2 – Hajautettu Git ja GitHub

__Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet, jotka vaikuttivat tehtävän suorittamiseen?__

Helppoa oli ymmärtää perusajatus siitä, että GitHub toimii etäpalvelimena ja paikallinen repositorio voidaan “työntää” sinne `git push` komennolla. Myös uuden etärepositorion lisääminen komennolla `git remote add origin ...` oli helppoa. Näitäkin käytiin läpi ohjelmistoprojekti kurssilla ja myös sen yhteydessä git ja github on tullut erittäin tutuksi.

Vaikeinta oli aluksi hahmottaa, mitä eroa on komennoilla `git fetch`, `git pull`. Yleensä ollaan vaan käytetty `git pull`. 

Oppimista auttoi Gitin virheilmoitukset. Myös se, että tarkistin usein `git status`-komennolla tilanteen, auttoi ymmärtämään, milloin haarani oli jäljessä etäreposta ja milloin ajan tasalla.

## Osiossa käyttämäni Git-komennot

| Komento | Kuvaus |
| --------| ------ |
| `git clone <url>` | Kloonaa etärepositorion (esim. GitHubista) omalle koneelle paikalliseksi repositorioksi. |
| `git remote add origin <url>` | Lisää etärepositorion ja antaa sille nimen `origin`. |
| `git remote -v` | Näyttää määritellyt etärepositoriot ja niiden URL-osoitteet (fetch/push). |
| `git push -u origin main` | Työntää paikallisen master-haaran commitit GitHubin origin-repoon ja asettaa seurantahaaraan. |
| `git fetch` | Hakee uudet commitit etärepositoriosta, mutta ei vielä yhdistä niitä paikallisiin haaroihin. |
| `git checkout origin/main` | Siirtyy katsomaan etärepositorion master-haaran tilannetta (detached HEAD -tila). |
| `git switch main` | Palaa paikalliseen master-haaraan. |
| `git merge origin/main` | Yhdistää etärepon master-haaran muutokset paikalliseen master-haaraan. |
| `git status` | Näyttää repositorion tilanteen: onko muutoksia, onko haara jäljessä tai edellä etäreposta jne. |

---

## Oppimispäiväkirja 3 – Git projektissa

__Mitä hyötyä voisi olla versionhallinnasta, jos kehität projektia yksin?__

Versionhallinta on hyödyllinen myös kun teet yksin projektia. Saan talteen selkeän “aikajanan” siitä, miten projekti on kehittynyt sekä voin palata aiempiin versioihin, jos jokin muutos rikkookin sovelluksen. Eri kokeiluja voi tehdä omissa haaroissaan ilman pelkoa, että koko projekti menee sekaisin. Commit-viestit toimivat samalla päiväkirjana. Lisäksi varmuuskopio GitHubissa tai muussa etäpalvelussa suojaa tilanteelta, jos esimerkiksi oma kone hajoaa.

__Mitä hyötyä voisi olla versionhallinnasta, jos projektissa on useita kehittäjiä?__

Jos projektissa on useampi kehittäjä, versiohallinta melkein pakollinen. Se mahdollistaa kaikkien työskentelyn samaan aikaan eri osissa järjestelmää ilman, että he tallovat toistensa varpaille. Haarojen avulla voidaan kehittää uusia ominaisuuksia erillään main koodista ja yhdistää ne vasta testien jälkeen. GitHubin pull requestit tuovat mukaan myös koodikatselmoinnin: toinen tiimiläinen voi tarkistaa muutokset ennen kuin ne viedään päähaaraan. Lisäksi on aina selkeä näkyvyys siihen, kuka on tehnyt mitäkin ja milloin.

__Miten järjestäisit projektitiimin versionhallinnan 3–4 hengen ohjelmistoprojektikurssilla? Laadi tiimiläisille lyhyt ohje, miten projektissa toimitaan.__

***Lyhyt ohje tiimille:***

1. **Haarat**
   - Päähaara on `main` (tai `master`). Sinne viedään vain valmiiksi testattuja ominaisuuksia.
   - Yhteinen kehityshaara on `develop`. Uudet ominaisuudet yhdistetään ensin developiin.
   - Jokainen tekee oman työnsä **feature-haaroissa**, esim. jarik haara.
2. **Työskentelytapa**
   - Kun aloitat uuden tehtävän:
     - Varmista, että `develop` on ajan tasalla:  
       `git switch develop` → `git pull`
     - Luo uusi haara:  
       `git switch -c jarik
   - Tee muutokset, commitoi usein selkeillä viesteillä.
   - Puske haara GitHubiin:  
     `git push -u origin jarik

3. **Pull requestit ja koodikatselmointi**
   - Tee GitHubissa **pull request** haarasta `jari` haaraan `develop`.
   - Kirjoita lyhyt kuvaus siitä, mitä muutos tekee.
   - Vähintään yksi tiimiläinen käy läpi muutokset (code review) ja kommentoi tarvittaessa.

4. **Konfliktien ratkaisu**
   - Jos `git pull` aiheuttaa konflikteja, ratkaise ne tiedostossa (poista `<<<<<<<`, `=======`, `>>>>>>>` -rivit) ja keskustele tiimin kanssa, jos et ole varma.
   - Älä commitoi puolivalmista konfliktiratkaisua.

5. **Yhteiset pelisäännöt**
   - Sovitaan etukäteen nimeämiskäytännöt (haarojen ja commit-viestien tyyli).
   - Ei suoria muutoksia `main`-haaraan, ainoastaan pull requestien kautta.
   - Pidetään `develop` aina ajokuntoisena (ei rikkinäistä koodia).

__Kommenttini opintojaksosta, esim. sisällöstä, materiaalista, työmäärästä, hyödyllisyydestä. Mitä toivoisit olevan enemmän, mitä vähemmän?__

Kurssin sisältö on ollut käytännönläheinen ja hyödyllinen. Git tulee vastaan lähes kaikissa oikeissa projekteissa. Harjoitukset on rakennettu loogisesti: ensin peruskomennot, sitten haarat, etärepo ja lopuksi tiimityö ja pull requestit.

Materiaalit (esimerkit, ohjeet ja komentolistat) ovat tukeneet hyvin tekemistä, erityisesti kun tuli virheitä ja piti selvittää, mitä Git oikeasti tarkoittaa. Ihan perusasioiden toistoa voisi hieman tiivistää loppua kohti, kun samat komennot alkavat tulla selkärangasta. Kokonaisuutena kurssi on tuntunut hyödylliseltä ja käytännönläheiseltä.

---
