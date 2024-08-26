# Oppimispäiväkirja: Hajautettu git

__Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet, jotka vaikuttivat tehtävän suorittamiseen?__

Tämä vaihe oli jälleen melko helppo. Uutena kokeiluna oli `git fetch`:n jälkeen etähaaran muutosten tarkastelu `git checkout origin/master`. Tämänkin olen yleensä tehnyt GitHubista selaimella. Koen tämän vaiheen kuitenkin hiukan syventäneen ymmärrystäni gitin toiminnasta.

## Osiossa käyttämäni Git-komennot

| Komento | Kuvaus |
| --------| ------ |
| git remote *add origin https://github.com/Romaalie/GitPerusteet.git* | Määritä paikalliselle repositoriolle etärepositorio (nimi origin, sijainti url)|
| git remote -v | Näytä etärepositorioiden asetukset "tarkemmin"|
| git push *-u origin master* | Puske nykyinen paikallinen haara etärepositorion origin haaraan master ja aseta tämä oletus etärepositorioksi/haaraksi|
| git branch -r | Näytä etärepositorion haarat|
| git fetch | Hae uusimmat tiedot etärepositoriosta|
| git checkout *origin/master* | Siirry tarkastelemaan etärepositorion origin haaraa master|