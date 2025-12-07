# Oppimispäiväkirja: Paikallinen git

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
