# Analiza podatkov s programom R, 2020/21

Repozitorij z gradivi pri predmetu APPR v študijskem letu 2020/21

* [![Shiny](http://mybinder.org/badge.svg)](http://mybinder.org/v2/gh/jaanos/APPR-2020-21/master?urlpath=shiny/APPR-2020-21/projekt.Rmd) Shiny
* [![RStudio](http://mybinder.org/badge.svg)](http://mybinder.org/v2/gh/jaanos/APPR-2020-21/master?urlpath=rstudio) RStudio

## Tematika

V svojem projektu bom analizirala poroke in razveze v Sloveniji. Nekatere pridobljene podatke, bom primerjala tudi z Evropskimi.

Viri podatkov:
* Statistični urad Republike Slovenije (https://pxweb.stat.si/SiStat/sl/Podrocja/Index/100/prebivalstvo) in 
* EUROSTAT (https://ec.europa.eu/eurostat/home)

Analizirala bom:

(1) Število sklenjenih zakonskih zvez letno v Sloveniji in primerjava z drugimi Evropskimi državami 

Ob začetku moje analize me bo zanimalo kako se število porok skozi leta spreminja. Podatke iz Slovenije pa bom primerjala tudi s podatki iz izbranih Evropskih držav. Za analizo podatkov iz Slovenije se bom sprva omejila na podatke med letoma 1990 in 2019. Ob primerjavi z drugimi državami, pa se bom morala zaradi pomankanja podatkov omejiti, le med letoma 2009 in 2019.

TABELA 1:
https://pxweb.stat.si/SiStatData/pxweb/sl/Data/-/05M1002S.px
Zasnova tabele: Meritve, Leto

TABELA 2:
https://ec.europa.eu/eurostat/databrowser/view/demo_nind/default/table?lang=en
Zasnova tabele: Država, Leto

(2) Število sklenjenih zakonskih zvez letno, glede na statitične regije v Sloveniji

Predstavila bom tudi skupno število sklenjenih porok glede na posamezno regijo. Zanimalo me bo v kateri regiji je letno največ porok in ali se trend lokacije skozi leta sreminja. 

 TABELA 3:
https://pxweb.stat.si/SiStatData/pxweb/sl/Data/-/05M2004S.px
Zasnova tabele: Kohezijska regija, Meritve, Leto

(3) Sklenitve prvih zakonskih zvez po starosti in spolu. 

(3.1) Iz tabele 4 bom pridobila podatek pri kateri starosti največkrat neveste in ženini prvič vstopijo v zakonsko zvezo. Tabela podaja podatke na leto, kar mi bo omogočilo razbrati, kako se skozi leta delež porok glede na posamezne starostne skupine spreminja, omejila se bom na podatke med letoma 1990 in 2019. Poleg te tabele sem na spletu zasledila tudi tabelo, ki vsebuje povprečno starost mladoporočencev drugod po svetu, te podatke bom primerjala s podatki v Sloveniji, zanimalo me bo predvsem kakšna so odstopanja v različnih državah. 

TABELA 4:
https://pxweb.stat.si/SiStatData/pxweb/sl/Data/-/05M1004S.px/table/tableViewLayout2/
Zasnova tabele: starostna skupina, leto, ženin/nevesta

TABELA 5:
https://ec.europa.eu/eurostat/databrowser/view/tps00014/default/table?lang=en (od leta 2007 do 2018)

TABELA 6:
https://en.wikipedia.org/wiki/List_of_countries_by_age_at_first_marriage (od leta 2008 do 2019)

(3.2) Število otroških porok od leta 2013 do leta 2019

TABELA 7:
https://data.unicef.org/topic/child-protection/child-marriage/


(4)Sklenitve zakonskih zvez po vrstnem redu sklenitve zakonske zveze ženina in neveste.

S pomočjo te tabele bom pridobila podatke, katere vrste porok (glede na vrstni red) je bilo v posameznem letu največ, oz. ali je delež katerih od teh skozi leto naraščal/ padal, to bom povezala z drugim delom analize, ki se tiče razvez v Sloveniji. Omejila se bom na podatke med letoma 1990 in 2019.

TABELA 5:
https://pxweb.stat.si/SiStatData/pxweb/sl/Data/-/05M1010S.px
Zasnova tabele: sklenitve zakonske zveze ženina/ neveste, leto

(4)Osnovni podatki o razvezah zakonskih zvez, Slovenija, letno.

Tabela zajema različne meritve razvez. Pri svoji analizi se bom omejila na število razvez zakonskih zvez z otrokom in brez in na skupno število razvez glede na leto.

TABELA 6: 
https://pxweb.stat.si/SiStatData/pxweb/sl/Data/-/05M3002S.px
Zasnova tabele: leto, meritve

Cilj mojega projekta je pridobiti vpogled, kako se število novih sklenjenih porok in razvez spreminja skozi leta. 


## Program

Glavni program in poročilo se nahajata v datoteki `projekt.Rmd`.
Ko ga prevedemo, se izvedejo programi, ki ustrezajo drugi, tretji in četrti fazi projekta:

* obdelava, uvoz in čiščenje podatkov: `uvoz/uvoz.r`
* analiza in vizualizacija podatkov: `vizualizacija/vizualizacija.r`
* napredna analiza podatkov: `analiza/analiza.r`

Vnaprej pripravljene funkcije se nahajajo v datotekah v mapi `lib/`.
Podatkovni viri so v mapi `podatki/`.
Zemljevidi v obliki SHP, ki jih program pobere,
se shranijo v mapo `../zemljevidi/` (torej izven mape projekta).

## Potrebni paketi za R

Za zagon tega vzorca je potrebno namestiti sledeče pakete za R:

* `knitr` - za izdelovanje poročila
* `rmarkdown` - za prevajanje poročila v obliki RMarkdown
* `shiny` - za prikaz spletnega vmesnika
* `DT` - za prikaz interaktivne tabele
* `rgdal` - za uvoz zemljevidov
* `rgeos` - za podporo zemljevidom
* `digest` - za zgoščevalne funkcije (uporabljajo se za shranjevanje zemljevidov)
* `readr` - za branje podatkov
* `rvest` - za pobiranje spletnih strani
* `tidyr` - za preoblikovanje podatkov v obliko *tidy data*
* `dplyr` - za delo s podatki
* `gsubfn` - za delo z nizi (čiščenje podatkov)
* `ggplot2` - za izrisovanje grafov
* `mosaic` - za pretvorbo zemljevidov v obliko za risanje z `ggplot2`
* `maptools` - za delo z zemljevidi
* `tmap` - za izrisovanje zemljevidov
* `extrafont` - za pravilen prikaz šumnikov (neobvezno)

## Binder

Zgornje [povezave](#analiza-podatkov-s-programom-r-202021)
omogočajo poganjanje projekta na spletu z orodjem [Binder](https://mybinder.org/).
V ta namen je bila pripravljena slika za [Docker](https://www.docker.com/),
ki vsebuje večino paketov, ki jih boste potrebovali za svoj projekt.

Če se izkaže, da katerega od paketov, ki ji potrebujete, ni v sliki,
lahko za sprotno namestitev poskrbite tako,
da jih v datoteki [`install.R`](install.R) namestite z ukazom `install.packages`.
Te datoteke (ali ukaza `install.packages`) **ne vključujte** v svoj program -
gre samo za navodilo za Binder, katere pakete naj namesti pred poganjanjem vašega projekta.

Tako nameščanje paketov se bo izvedlo pred vsakim poganjanjem v Binderju.
Če se izkaže, da je to preveč zamudno,
lahko pripravite [lastno sliko](https://github.com/jaanos/APPR-docker) z želenimi paketi.

Če želite v Binderju delati z git,
v datoteki `gitconfig` nastavite svoje ime in priimek ter e-poštni naslov
(odkomentirajte vzorec in zamenjajte s svojimi podatki) -
ob naslednjem zagonu bo mogoče delati commite.
Te podatke lahko nastavite tudi z `git config --global` v konzoli
(vendar bodo veljale le v trenutni seji).
