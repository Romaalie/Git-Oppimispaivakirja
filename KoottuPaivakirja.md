# Tässä yhteen tiedostoon yhdistetty oppimispäiväkirja

Ohjeiden epäselvyyden vuoksi tein tämmöisenkin.

## Oppimispäiväkirja: Paikallinen git

__Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet?__

Kaikki oli suhteellisen helppoa, mutta hetki piti miettiä miten pääsen käsiksi tähän päiväkirja haaraan vaikka se lopulta hyvin helppoa olikin. Hyvin jäsennelty ohjeistus antoi tilaisuuden harjoitella uudessa repositoriossa asioita joita en ollut ennen kokeillut kuten committien perumista (git revert) ja aiempien committien tarkastelua (git checkout *commit hash*). Myös git log oli uusi tuttavuus, aiemmin olen tarkastellut commit historiaa vain GitHubin GUI:n avulla.

Ehdin tekemään osan harjoituksista ennen kuin tajusin moodlesta löytyvät ohjeet päiväkirjaan, koska jatkoin vain https://mruonavaara.github.io/git-versionhallinta/ sivustolla eteenpäin tarkistamatta moodlea välissä. Näin ollen osa käytetyistä komennoista tässä päiväkirjassa saattoi jäädä kirjaamatta.

### Osiossa käyttämäni Git-komennot

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

## Oppimispäiväkirja: Hajautettu git

__Mikä osion tehtävissä oli vaikeaa ja mikä helppoa? Mikä auttoi minua oppimaan? Miten selvitin esteet, jotka vaikuttivat tehtävän suorittamiseen?__

Tämä vaihe oli jälleen melko helppo. Uutena kokeiluna oli `git fetch`:n jälkeen etähaaran muutosten tarkastelu `git checkout origin/master`. Tämänkin olen yleensä tehnyt GitHubista selaimella. Koen tämän vaiheen kuitenkin hiukan syventäneen ymmärrystäni gitin toiminnasta.

### Osiossa käyttämäni Git-komennot

| Komento | Kuvaus |
| --------| ------ |
| git remote *add origin https://github.com/Romaalie/GitPerusteet.git* | Määritä paikalliselle repositoriolle etärepositorio (nimi origin, sijainti url)|
| git remote -v | Näytä etärepositorioiden asetukset "tarkemmin"|
| git push *-u origin master* | Puske nykyinen paikallinen haara etärepositorion origin haaraan master ja aseta tämä oletus etärepositorioksi/haaraksi|
| git branch -r | Näytä etärepositorion haarat|
| git fetch | Hae uusimmat tiedot etärepositoriosta|
| git checkout *origin/master* | Siirry tarkastelemaan etärepositorion origin haaraa master|

## Oppimispäiväkirja: Git projektissa

__Mitä hyötyä voisi olla versionhallinnasta, jos kehität projektia yksin?__

Versionhallinta mahdollistaa mm. aiempien versioiden palauttamisen sekä uusien ominaisuuksien testaamisen turvallisesti (ei rikota aiempaa/voidaan palauttaa).

__Mitä hyötyä voisi olla versionhallinnasta, jos projektissa on useita kehittäjiä?__

Useamman kehittäjän projekteissa versionhallinta helpottaa yhtäaikaista kehittämistä tarjoamalla jokaiselle tekijälle yhtenäisen ja ajantasaisen projektipohjan sekä oman henkilökohtaisen kehitysympäristön. Nämä mahdollistavat eri ominaisuuksien samanaikaisen kehittämisen ja niiden hallitun yhteen tuomisen.  

__Miten järjestäisit projektitiimin versionhallinnan 3-4 hengen ohjelmistoprojektikurssilla? Laadi tiimiläisille lyhyt ohje, miten projektissa toimitaan.__

Sopikaa yhteisistä käytännöistä ja noudattakaa niitä. Seuraavassa hyviä ehdotuksia/aiheita tiimin yhdessä sovittavaksi:

- Kuka tekee ja mitä tekee: voi harmittaa aika paljon jos kaksi ihmistä on hiljaa tehnyt pari päivää samaa ominaisuutta omissa haaroissaan ja sitten tämä huomataan commitoidessa yhteiseen.

- Commit viestien rakenne: tarpeeksi kuvaavat ja tarkat, niistä on helppo jälkikäteen nopeasti seurata mitä on tehty ja milloin.

- Commitoikaa tarpeeksi usein: yksi muutos, yksi commit on oikeasti aika hyvä periaate.

- Committien hierarkia: mihin haaraan commitoidaan ja miten niitä yhdistellään (feature->dev->main vai joku muu?).

- Vaikka versionhallinta on tosi kätevää niin kommunikointi on silti kultaa. Keskustelkaa myös commit viestien ulkopuolella.


__Kommenttini opintojaksosta, esim. sisällöstä, materiaalista, työmäärästä, hyödyllisyydestä, työmäärästä. Mitä toivoisit olevan enemmän, mitä vähemmän?__

Opintojakso toimi minulle hyvänä git refresher kurssina kesän jälkeen ja tarjosi mahdollisuuden kokeilla harvemmin käytettyjä/minulle tuntemattomia gitin perus ominaisuuksia.

Työmäärältään kurssi ohi hyvin kohtuullinen, mutta tarjoaa silti hyvät lähtökohdat git versionhallinnan parissa työskentelyyn yksin ja osana projektitiimiä.

Erityisen hauska osuus oli harjoituksen 6 virtuaalisen tiimikaverin kanssa työskentely, ~~joskaan en ole vielä ihan varma kuinka tarkasti lopputuloksen piti vastata ohjeissa esitettyä [kuvaa](https://mruonavaara.github.io/git-versionhallinta/assets/hei_maailma_lopputulos.png) (kello ja taustakuva).~~ No niin saihan sieltä vihdoin imettyä uuden päivityksen.

[Ulkoinen oppimateriaali](https://mruonavaara.github.io/git-versionhallinta/) imi niin tehokkaasti mukaan, että oppimispäiväkirja tuli hiukan myöhässä mukaan kuvioihin, jos tarkoitus oli tehdä sitä täysin samaan aikaan kuin harjoituksia. Tämä saattoi olla kyllä vain henkilökohtainen ongelma.