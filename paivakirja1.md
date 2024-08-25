# Oppimispäiväkirja: Paikallinen git

__Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet?__

Kaikki oli suhteellisen helppoa. Hyvin jäsennelty ohjeistus antoi kuitenkin tilaisuuden harjoitella uudessa repositoriossa asioita joita en ollut ennen kokeillut kuten committien perumista (git revert) ja aiempien committien tarkastelua (git checkout *commit hash*). Myös git log oli uusi tuttavuus, aiemmin olen tarkastellut commit historiaa vain GitHubin GUI:n avulla.

## Osiossa käyttämäni Git-komennot

| Komento | Kuvaus |
| --------| ------ |
| git init | Luo uusi git repositorio/lisää nykyinen hakemisto git versionhallintaan. |
| git clone *etärepon osoite* | kloonaa kyseisestä etärepositoriosta paikallinen versio. |
| git add *lisättävä tiedosto/hakemisto*/ *.* | Lisää määritelty sisältö rekursiivisesti nykyisen repositorion git versionhallintaan ja valmiiksi talletusta varten. |
| git status | Näytä työtilan tiedostojen tilanne git versionhallinnan suhteen. |
| git commit *-m "commit viesti"* | Tallentaa valmistellut muutokset git versiohallintaan committina. Viesti vapaaehtoinen joskin vahvasti toivottu ja mieluiten kuvaava." |
| git log *--stat*| Näytä repositorion commit historia. Tehdyt muutokset saa näkymään historiaan lisäkomennolla --stat. |
| git checkout *haara/commit* | Siirry määriteltyyn haaraan/committiin. |
| git switch - | Palaa haaraan, josta checkout tehtiin. |
| git reset --staged *poistettavan tiedoston/hakemiston nimi* | Peruuta git add -komennolla tehty talletuksen valmistelu määritellylle kohteelle. |
| git revert *commitin hash* | Tee käänteinen commit kyseisestä commitista eli peruuta se. |