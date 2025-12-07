# Oppimispäiväkirja: Git projektissa

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
