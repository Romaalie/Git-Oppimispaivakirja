# Oppimispäiväkirja: Paikallinen git

__Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet?__

Kaikki oli suhteellisen helppoa, mutta hetki piti miettiä miten pääsen käsiksi tähän päiväkirja haaraan vaikka se lopulta hyvin helppoa olikin. Hyvin jäsennelty ohjeistus antoi tilaisuuden harjoitella uudessa repositoriossa asioita joita en ollut ennen kokeillut kuten committien perumista (git revert) ja aiempien committien tarkastelua (git checkout *commit hash*). Myös git log oli uusi tuttavuus, aiemmin olen tarkastellut commit historiaa vain GitHubin GUI:n avulla.

Ehdin tekemään osan harjoituksista ennen kuin tajusin moodlesta löytyvät ohjeet päiväkirjaan, koska jatkoin vain https://mruonavaara.github.io/git-versionhallinta/ sivustolla eteenpäin tarkistamatta moodlea välissä. Näin ollen osa käytetyistä komennoista tässä päiväkirjassa saattoi jäädä kirjaamatta.

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
| git branch *uuden haaran nimi* | Luo uusi haara annetulla nimellä  |
| git merge *yhdistettävän haaran nimi* | Yhdistää merge toiminnolla nimetyn haaran nykyiseen haaraan  |