# Oppimispäiväkirja: Hajautettu git

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
