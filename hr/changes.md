# ﻿Što je novo u NVDA

## 2024.3

Add-on store će vas obavijestiti o dostupnosti ažuriranja dodataka prilikom pokretanja NVDA.

Dodane su opcije za primjenu unicode normalizacije na govor i brajicu.
To može biti korisno pri čitanju znakova koji su nepoznati određenoj govornoj jedinici ili ne postoje u određenoj brajičnoj tablici. Takvi znakovi mogu imati kompatibilnu alternativu, poput podebljanih ili kosih slova koja se uobičajeno koriste na društvenim mrežama.
Ta opcija također omogućuje čitanje jednadžbi u Microsoft Word uređivaču jednadžbi.

Help Tech Activator Pro brajični redci su sada podržani.

Dodane su nedodijeljene geste za pomicanje kotačića miša vertikalno ili horizontalno.

Ispravljeno je nekoliko pogrešaka, prije svega u Windows 11 emoji panelu i povijesti međuspremnika.
Dodane su ispravke u web preglednicima za čitanje poruka o pogreškama, figure, crteže, oznake tablica te potvrdne okvire i izborne gumbe.

Liblouis je nadograđen sa dodanom podrškom za srpsku ćirilicu, Jidiš, nekoliko drevnih jezika, turski i međunarodnu fonetsku abecedu.
eSpeak je nadograđen sa dodanom podrškom za karakalpački.
Unicode CLDR je također nadograđen.

### nove značajke

* Novi tipkovnički prečaci:
  * Dodani su prečaci za vertikalno i horizontalno pomicanje kotačića miša, kako bi se unaprijedilo kretanje u nekim aplikacijama i na nekim web stranicama čiji se sadržaj osvježava, kao što je to na primjer Dism++. (#16462, @Cary-Rowen)
* Dodana podrška za Unicode normalizaciju za govor i brajicu. (#11570, #16466 @LeonarddeR).
  * To može biti korisno kada je određeni znak nepoznat za govornu jedinicu ili ne postoji u brajičnoj tablici, ali ima kompatibilnu alternativu kao što su to na primjer podebljani ili kosi znakovi koji se uobičajeno koriste na društvenim mrežama.
  * To također omogućuje čitanje jednadžbi u Microsoft Word uređivaču jednadžbi. (#4631)
  * Ovu značajku možete uključiti za govor i brajicu u dijaloškom okviru postavki u pripadajućim kategorijama.
* Od sada ćete biti podrazumijevano obavješteni o novim ažuriranjima dodataka prilikom pokretanja NVDA. (#15035)
  * To se može isključiti u "Add-on Store" kategoriji u postavkama.
  * NVDA provjerava svakodnevno za ažuriranje NVDA dodataka.
  * Provjeravat će se ažuriranja samo za jedan kanal (na primjer instalirani beta dodaci će biti provjeravani iz beta kanala).
* Dodana podrška za Help Tech Activator Pro brajične redke. (#16668)

### Izmjene

* nadogradnje komponenata:
  * eSpeak NG je nadograđen na inačicu 1.52-dev commit `54ee11a79`. (#16495)
    * Dodan novi jezik: karakalpački.
  * Nadograđen Unicode CLDR na inačicu 45.0. (#16507, @OzancanKaratas)
  * Nadograđen fast_diff_match_patch (koristi se za otkrivanje izmjena u naredbenom redku i drugom dinamičkom sadržaju) na inačicu 2.1.0. (#16508, @codeofdusk)
  * Nadograđen LibLouis brajični prevoditelj na inačicu [3.30.0](https://github.com/liblouis/liblouis/releases/tag/v3.30.0). (#16652, @codeofdusk)
    * nove brajične tablice:
      * Srpski ćirilica.
      * Jidiš.
      * Nekoliko drevnih jezika: biblijski hebrejski, akadski, sirijski, ugaricki te transliterirani klinopis.
      * Turski kratkopis. (#16735)
      * Međunarodna fonetska abeceda. (#16773)
  * Nadograđen NSIS na inačicu 3.10 (#16674, @dpy013)
  * Nadograđen markdown na inačicu 3.6 (#16725, @dpy013)
  * Nadograđen nh3 na inačicu 0.2.17 (#16725, @dpy013)
* Sigurnosna ulazna brajična tablica je jednaka izlaznoj sigurnosnoj brajičnoj tablici, koja je "Unificirani Engleski brajični kod puno pismo". (#9863, @JulienCochuyt, @LeonarddeR)
* NVDA će sada čitati figure bez pristupačnih podređenih objekata, ali sa oznakom i opisom. (#14514)
* Prilikom čitanja po redku  u modusu čitanja, "potpis" se više ne čita pri svakom redku potpisa ili tablice. (#14874)
* U Python konzoli, zadnja neizvršena komanda više neće biti izgubljena prilikom kretanja po povijesti ulaza. (#16653, @CyrilleB79)
* Unikatan anonimni identifikator sada se šalje kao dio neobaveznih statistika korištenja NVDA. (#16266)
* Pri stvaranju prijenosne kopije, podrazumijevano će se automatski stvarati nova mapa.
Od sada će se prikazivati upozorenje ako pokušate pisati unutar mape koja nije prazna. (#16686)

### Ispravke grešaka

* Windows 11 ispravke:
  * NVDA se više neće zaglavljivati prilikom zatvaranja povijesti međuspremnika i emoji panela. (#16346, #16347, @josephsl)
  * NVDA će ponovno izgovarati vidljive kandidate prilikom otvaranja Ime sučelja. (#14023, @josephsl)
  * NVDA više neće dvaput izgovoriti "povijest međuspremnika" pri kretanju stavkama izbornika emoji panela. (#16532, @josephsl)
  * NVDA više neće prekidati govor i brajicu pri pregledu kaomojia i znakova u emoji panelu. (#16533, @josephsl)
* Ispravke u preglednicima:
  * Poruke o pogrešci zabilježene kao `aria-errormessage` sada se izgovaraju u Google Chromeu i Mozilla Firefoxu. (#8318)
  * Ako postoji, NVDA će sada koristiti `aria-labelledby` atribut za  dohvaćanje pristupačnih naziva tablica u Mozilla Firefoxu. (#5183)
  * NVDA će ispravno izgovarati stavke izbornika u obliku izbornih gumbi i potvrdnih okvira prilikom prvog otvaranja podizbornika u Google Chromeu i Mozilla Firefoxu. (#14550)
  * Značajka pretrage u modusu čitanja NVDA čitača zaslona sada je točnija kada stranica sadrži emoji znakove. (#16317, @LeonarddeR)
  * U Mozilla Firefoxu, NVDA sada ispravno čita trenutni znak, trenutnu riječ i trenutni redak kada se kursor nalazi na točki umetanja na kraju redka. (#3156, @jcsteh)
  * NVDA više ne prouzrokuje rušenje poslije zatvaranja dokumenta ili zatvaranja Google Chromea. (#16893)
* NVDA će sada ispravno čitati prijedloge automatskog popunjavanja u Eclipse i drugim okruženjima baziranima na Eclipseu u Windowsima 11. (#16416, @thgcode)
* Unapređena pouzdanost automatskog čitanja teksta, osobito u aplikacijama naredbenog redka. (#15850, #16027, @Danstiv)
* Sada je ponovno moguće pouzdano vratiti konfiguraciju na prethodne vrijednosti. (#16755, @Emil-18)
* NVDA će ispravno izgovarati promjene u označavanju pri uređivanju teksta ćelije u Microsoft Excelu. (#15843)
* U aplikacijama koje koriste Jawa access bridge, NVDA će sada ispravno pročitati zadnji prazan redak teksta umjesto ponavljanja prethodnog redka teksta. (#9376, @dmitrii-drobotov)
* U LibreOffice Writeru (inačica 24.8 i novijim), prilikom uključivanja ili isključivanja oblikovanja teksta (podebljanja, ukošenja, podcrtavanja, indeksa/eksponenta, poravnanja) kada se koriste odgovarajući tipkovnički prečaci, NVDA će izgovoriti novo obilježje oblikovanja (na primjer, "podebljano uključeno", "podebljano isključeno"). (#4248, @michaelweghorn)
* pri kretanju po poljima za uređivanje u aplikacijama koje koriste UI automation, NVDA više ne izgovara krivi znak, krivu riječ, Itd. (#16711, @jcsteh)
* Pri ljepljenju u  Windows 10/11 kalkulator, NVDA sada ispravno čita cijeli broj koji je zalijepljen. (#16573, @TristanBurchett)
* Govor se više ne gubi prilikom ponovnog povezivanja u sesiju udaljene radne površine. (#16722, @jcsteh)
* Dodana je podrška za prečace za pregledavanje teksta za ime objekta u Visual Studio Codeu. (#16248, @Cary-Rowen)
* Zvukovi NVDA sada se reproduciraju i na Mono audiouređajima. (#16770, @jcsteh)
* NVDA će od sada čitati adrese prilikom kretanja po poljima do/kopija/skrivena kopija u prgramu outlook.com i suvremenom Outlooku. (#16856)
* NVDA sada bolje rukuje pogreškama pri instalaciji dodataka. (#16704)

### Changes for Developers

* NVDA now uses Ruff instead of flake8 for linting. (#14817)
* Fixed NVDA's build system to work properly when using Visual Studio 2022 version 17.10 and above. (#16480, @LeonarddeR)
* A fixed width font is now used in Log Viewer and in the NVDA Python Console so that the cursor remains in the same column during vertical navigation.
It is especially useful to read the error location markers in tracebacks. (#16321, @CyrilleB79)
* Support for custom braille tables has been added. (#3304, #16208, @JulienCochuyt, @LeonarddeR)
  * Tables can be provided in the `brailleTables` folder in an add-on package.
  * Table metadata can be added to an optional `brailleTables` section in the add-on manifest or to a `.ini` file with the same format found in the brailleTables subdirectory of the scratchpad directory.
  * Please consult the [braille translation tables section in the developer guide](https://www.nvaccess.org/files/nvda/documentation/developerGuide.html#BrailleTables) for more details.
* When a `gainFocus` event is queued with an object that has a valid `focusRedirect` property, the object pointed to by the `focusRedirect` property is now held by `eventHandler.lastQueuedFocusObject`, rather than the originally queued object. (#15843)
* NVDA will log its executable architecture (x86) at startup. (#16432, @josephsl)
* `wx.CallAfter`, which is wrapped in `monkeyPatches/wxMonkeyPatches.py`, now includes proper `functools.wraps` indication. (#16520, @XLTechie)
* There is a new module for scheduling tasks `utils.schedule`, using the pip module `schedule`. (#16636)
  * You can use `scheduleThread.scheduleDailyJobAtStartUp` to automatically schedule a job that happens after NVDA starts, and every 24 hours after that.
  Jobs are scheduled with a delay to avoid conflicts.
  * `scheduleThread.scheduleDailyJob` and `scheduleJob` can be used to schedule jobs at custom times, where a `JobClashError` will be raised on a known job scheduling clash.
* It is now possible to create app modules for apps hosting Edge WebView2 (msedgewebview2.exe) controls. (#16705, @josephsl)

## 2024.2

Dodana nova značajka način podjeljenog zvuka.
Ta značajka omogućuje postavljanje zvuka NVDA u jedan kanal (npr. lijevi), dok su zvukovi drugih programa usmjereni u  drugi kanal (na primjer desni).

Dodani su novi prečaci za promjenu postavki prstena govorne jedinice, koje omogućuju premještanje od prve do zadnje postavke, te njihovo mijenjanje u većim koracima.
Dodani su novi prečaci brze navigacije, koji omogućuju korisnicima kretanje po: odlomcima, okomito poravnatim odlomcima, tekstu istog stila, tekstu različitog stila, stavkama izbornika, preklopnim gumbima, trakama napredovanja, figurama, te matematičkim formulama.

Dodano je puno novih značajki vezanih uz brajicu, te je ispravljeno puno pogrešaka.
Dodan je novi modus brajice "prikaz govora".
Kada je aktivan, na brajičnom se redku prikazuje točno ono što NVDA izgovara.
Također je dodana podrška za brajične redke BrailleEdgeS2, BrailleEdgeS3.
LibLouis je nadograđen sa dodanim novim brajičnim tablicama sa označavanjem velikih slova za bjeloruski i ukrajinski jezik, brajičnom tablicom za Laoski jezik te brajičnom tablicom za španjolski jezik, predviđena za čitanje starogrčkog teksta.

eSpeak je nadograđensa dodanim novim jezikom Tigrinja.

Ispravljeno je puno pogrešaka u programima, poput Thunderbirda, Adobe Readera, web preglednika, Nudija te Geekbench-a.

### Nove značajke

* Novi tipkovnički prečaci:
  * Novi prečac za brzo kretanje `p` za premještanje na sljedeći/prethodni odlomak teksta u modusu čitanja. (#15998, @mltony)
  * Novi nedodijeljeni prečaci, koji se mogu koristiti za kretanje po slijedećim/prethodnim:
    * figurama (#10826)
    * okomito poravnatim odlomcima (#15999, @mltony)
    * stavkama izbornika (#16001, @mltony)
    * preklopnim gumbima (#16001, @mltony)
    * trakama napredka (#16001, @mltony)
    * matematičkim formulama (#16001, @mltony)
    * tekstovima istog stila (#16000, @mltony)
    * tekstovima različitog stila (#16000, @mltony)
  * Dodan prečac za premještanje između prve postavke, posljednje postavke, za kretanje u naprijed te za kretanje u nazad unutar postavki prstena govorne jedinice. (#13768, #16095, @rmcpantoja)
    * Postavljanje prve ili posljednje postavke prstena govorne jedinice nema dodijeljen prečac. (#13768)
    * Povećavanje ili smanjivanje postavki govorne jedinice u većim koracima (#13768):
      * Prečac za stolna računala: `NVDA+control+pageUp` odnosno `NVDA+control+pageDown`.
      * prečac za prijenosna računala: `NVDA+control+shift+pageUp` ili `NVDA+control+shift+pageDown`.
  * Dodan novi nedodijeljeni prečac za uključivanje ili isključivanje izgovora figura i potpisa. (#10826, #14349)
* brajica:
  * Dodana podrška za brajični redak BrailleEdgeS2, BrailleEdgeS3. (#16033, #16279, @EdKweon)
  * Novi modus brajice "prikaz govora" je dodan. (#15898, @Emil-18)
    * Kada je aktivan, na brajičnom se redku prikazuje točno ono što NVDA izgovara.
    * Može se uključiti pritiskom `NVDA+alt+t`, ili u dijaloškom okviru postavki brajice.
* Način podijeljenog zvuka: (#12985, @mltony)
  * Omogućuje postavljanje NVDA u jednom kanalu (na primjer lijevom) dok su zvukovi drugih programa usmjereni u drugi kanal (na primjer desni).
  * Regulira se uz pomoć prečaca `NVDA+alt+s`.
* Izgovaranje zaglavlja redaka i stupaca u ContentEditable html elementima. (#14113)
* Dodana opcija za isključivanje čitanja figura i potpisa u postavkama oblikovanja dokumenata. (#10826, #14349)
* U Windowsima 11, NVDA će izgovarati upozorenja glasovnog upisivanja i preporučene radnje uključujući glavnu preporučenu radnju prilikom kopiranja podataka poput telefonskih brojeva u međuspremnik (Windows 11 nadogradnja 2022 i novije inačice). (#16009, @josephsl)
* NVDA će držati audiouređaj budnim poslije zaustavljanja govora, kako bi se izbjeglo rezanje sljedeće izgovorene fraze na nekim audiouređajima poput Bluetooth slušalica. (#14386, @jcsteh, @mltony)
* HP Secure Browser je sada podržan. (#16377)

### Izmjene

* Add-on Store:
  * Minimalna verzija i posljednja testirana verzija dodatka sada se prikazuju u području "više detalja". (#15776, @Nael-Sayegh)
  * Radnja "recenzije zajednice" biti će dostupna u pojedinostima u svim karticama svojstava u Add-on storeu. (#16179, @nvdaes)
* Nadogradnje komponenti:
  * Nadograđen LibLouis brajični prevoditelj na inačicu [3.29.0](https://github.com/liblouis/liblouis/releases/tag/v3.29.0). (#16259, @codeofdusk)
    * Nove brajične tablice za bjeloruski i ukrajinski jezik sa podrškom prikazivanja znakova za velika slova.
    * Nova španjolska brajična tablica sa podrškom za čitanje grčkog teksta.
    * Nova brajična tablica za laoski jezik, puno pismo. (#16470)
  * eSpeak NG je nadograđen  na inačicu 1.52-dev commit `cb62d93fd7`. (#15913)
    * Dodan je novi jezik: tigrinya. 
* Promijenjeno je nekoliko prečaca za brajični redke BrailleSense kako bi se izbjegli konflikti sa znakovima francuske brajične tablice. (#15306)
  * `alt+strelicaLijevo` sada je promijenjen na prečac `točkica2+točkica7+razmak`
  * `alt+strelicaDesno` sada je promijenjen u `točkica5+točkica7+razmaknica`
  * `alt+strelicaGore` sada je promijenjen u `točkica2+točkica3+točkica7+razmaknica`
  * `alt+StrelicaDolje` sada je promijenjen u `točkica5+točkica6+točkica7+razmaknica`
* Višetočja koja se često koriste u tablicama sadržaja više se ne čitaju pri niskim razinama interpunkcije. (#15845, @CyrilleB79)

### Ispravke grešaka

* Ispravke vezane uz Windows 11:
  * NVDA će opet izgovarati prijedloge za upisivanje kada se koristi hardverska tipkovnica. (#16283, @josephsl)
  * U inačici 24H2 (nadogradnji za 2024 godinu te Windows Server 2025), miš i dodirnik mogu se koristiti u brzim postavkama. (#16348, @josephsl)
* Add-on Store:
  * Kada se pritisne `ctrl+tab`, fokus se ispravno prebacuje na novi aktualni naslov kartice svojstva. (#14986, @ABuffEr)
  * Ako datoteke predmemorije nisu ispravne, NVDA se više neće ponovno pokretati. (#16362, @nvdaes)
* Ispravke za  preglednike bazirane na Chromiumu kada se korise uz pomoć Uia:
  * Ispravljene greške koje su prouzrokovale zaglavljivanje NVDA. (#16393, #16394)
  * Tipka Backspace sada ispravno radi U poljima za prijavu Gmail a. (#16395)
* Tipka backspace sada ispravno radi kada se koristi program Nudi 6.1 sa postavkom "rukuj tipkama iz drugih programa". (#15822, @jcsteh)
* Ispravljena je pogreška kada se reproduciraju zvučne koordinate kada se program nalazi u stanju mirovanja kada je opcija "Reproduciraj zvučne signale prilikom pomicanja miša" uključena. (#8059, @hwf1324)
* U Adobe Readeru, više se ne ignorira alternativni tekst na formulama u PDF datotekama. (#12715)
* Ispravljena je pogreška koja je onemogućavala čitanje opcija i ribbona u  Geekbenchu. (#16251, @mzanm)
* Ispravljen je rijedak slučaj nemogućnosti spremanja konfiguracije, kada se nisu spremali i konfiguracijski profili. (#16343, @CyrilleB79)
* U Firefoxu i preglednicima baziranima na Chromiumu, NVDA će ispravno aktivirati modus fokusa prilikom pritiska entera kad je fokus na prezentacijskom popisu (ul / ol) unutar sadržaja za uređivanje. (#16325)
* Stanje promjena stupaca kada se označuju stupci za prikaz u popisu poruka u Thunderbirdu sada se ispravno čitaju. (#16323)
* preklopnik u naredbenom redku `-h`/`--help` ponovno ispravno radi. (#16522, @XLTechie)
* NVDA podrška za Poedit softver za prevođenje inačica 3.4 ili novije verzije ispravno radi prilikom prevođenja na jezike sa jednim ili više od dva oblika množine (npr: u kineskom, poljskom). (#16318)

### Changes for Developers

Please refer to [the developer guide](https://www.nvaccess.org/files/nvda/documentation/developerGuide.html#API) for information on NVDA's API deprecation and removal process.

* Instantiating `winVersion.WinVersion` objects with unknown Windows versions above 10.0.22000 such as 10.0.25398 returns "Windows 11 unknown" instead of "Windows 10 unknown" for release name. (#15992, @josephsl)
* Make the AppVeyor build process easier for NVDA forks, by adding configurable variables in appveyor.yml to disable or modify NV Access specific portions of the build scripts. (#16216, @XLTechie)
* Added a how-to document, explaining the process of building NVDA forks on AppVeyor. (#16293, @XLTechie)

## 2024.1

Dodan je novi modus govora čitanja informacija na zahtjev.
Kada je modus govora postavljen da izgovara informacije na zahtjev, NVDA ne čita informacije automatski na primjer prilikom pomicanja kursora, ali još uvijek izgovara informacije i koje se dobivaju uz pomoć prečaca, čiji je cilj izgovaranja određenih informacija na primjer, izgovaranje naslovne trake.
U kategoriji "govor" NVDA postavki, sada je moguće izostavljanje neželjenih modusa govora iz odabira modusa govora (`NVDA+s`).

Novi način kopiranja sa sačuvanim oblikovanjem, koji se poziva uz pomoć prečaca `NVDA+shift+f10` dostupan je na web stranicama u Mozilla Firefoxu.
Kada se uključi, koristit će se izvorno označavanje u Mozilli firefoxu.
Kopiranje teksta uz pomoć prečaca `control+c` biti će proslijeđeno direktno Mozilli firefoxu što znači da će tekst biti kopiran sa sačuvanim oblikovanjem, umjesto čistog teksta bez oblikovanja.

NVDA store sada podržava višestruke radnje na primjer: instaliranje ili uključivanje dodataka tako da se označi više dodataka
Dodana je nova radnja za otvaranje web stranice recenzija za bilo koji označeni dodatak.

Opcije odabira zvučne kartice i načina stišavanja govora su uklonjene iz dijaloškog okvira "odabir govorne jedinice".
Ove se opcije mogu pronaći u novom dijaloškom okviru postavki zvuka koji se poziva prečacem `NVDA+control+u`.

Nadograđeni su eSpeak-NG, LibLouis braille translator, i Unicode CLDR.
Dodane su nove brajične tablice za tajski, filipinski i rumunjski jezik.

Ispravljeno je puno pogrešaka, uglavnom u Add-on Storeu, podršci za brajicu, Libre Officeu, Microsoft Officeu i podršci za zvuk.

### Važne napomene

* Ova inačica narušava kompatibilnost sa postojećim dodacima.
* Windows 7, i Windows 8 više nisu podržani operacijski sustavi.
Windows 8.1 je minimalna verzija operacijskog sustava Windows.

### Nove značajke

* Add-on Store:
  * Add-on Store sada podržava višestruke radnje na primjer instaliranje, uključivanje više dodataka) tako da se odabere više dodataka. (#15350, #15623, @CyrilleB79)
  * Dodana je opcija koja služi za davanje povratne informacije o dodacima putem posebne web stranice za svaki dodatak. (#15576, @nvdaes)
* Dodana podrška za Bluetooth niskonaponske brajične redke. (#15470)
* Dodano je kopiranje sa sačuvanim oblikovanjem (koje se uključuje ili isključuje uz pomoć prečaca `NVDA+shift+f10`) na web stranicama u Mozilla firefoxu.
Kada je uključeno, koristit će se izvorno označavanje u Mozilla firefoxu.
Prilikom kopiranja teksta uz pomoć prečaca `control+c` biti će proslijeđeno izravno Firefoxu, što će kopirati i formatiranje, a ne samo oblikovanje.
Imajte na umu da prilikom kopiranja teksta i njegovim rukovanjem od strane Firefoxa, NVDA neće izgovoriti poruku "kopirano u međuspremnik". (#15830)
* Prilikom kopiranja teksta u Microsoft Wordu sa uključenim načinom čitanja, oblikovanje će se također kopirati.
Posljedica ovoga je da NVDA neće izgovarati poruku "kopirano u međuspremnik" kada se pritisne `control+c` u Microsoft wordu ili Outlooku, zbog toga što aplikacija upravlja kopiranjem., umjesto NVDA. (#16129)
* Dodan je novi modus govora "na zahtjev".
Kada je govor podešen na zahtjev, NVDA neće govoriti automatski (na primjer, prilikom pomicanja kursora) ali govori kada se pozivaju prečaci čiji je cilj čitanje određene informacije (na primjer izgovaranje naslovne trake). (#481, @CyrilleB79)
* U kategoriji govor postavki NVDA, sada je moguće isključiti neželjene moduse govora iz odabira prečacem odabira modusa govora (`NVDA+s`). (#15806, @lukaszgo1)
  * Ako koristite dodatak NoBeepsSpeechMode razmislite o njegovom uklanjanju, i onemogućavanjem "zvučnih signala" "i načina na zahtjev" u postavkama.

### Izmjene

* NVDA više ne podržava Windows 7 i Windows 8.
Windows 8.1 je minimalna podržana verzija sustava Windows. (#15544)
* Nadogradnje komponenata:
  * Nadograđen LibLouis brajični prevoditelj na inačicu [3.28.0](https://github.com/liblouis/liblouis/releases/tag/v3.28.0). (#15435, #15876, @codeofdusk)
    * Dodane nove brajične tablice za Tajski, Rumunjski i Filipinski.
  * eSpeak NG je nadograđen na 1.52-dev commit `530bf0abf`. (#15036)
  * Prijevodi simbola i Emoji znakova su nadograđeni na verziju 44.0. (#15712, @OzancanKaratas)
  * Nadograđena Java Access Bridge na 17.0.9+8Zulu (17.46.19). (#15744)
* Tipkovnički prečaci:
  * Slijedeći tipkovnički prečaci od sada podržavaju dvostruke i trostruke pritiske za slovkanje informacije, te sricanje uz pomoć fonetskog opisa znakova: čitaj označeni tekst, čitaj tekst u međuspremniku i čitaj fokusirani objekt. (#15449, @CyrilleB79)
  * Prečac za uključivanje i isključivanje zaslonske zavjese sada ima podrazumjevani tipkovnički prečac: `NVDA+control+escape`. (#10560, @CyrilleB79)
  * Kada se pritisne četiri puta, prečac za čitanje označenog teksta sada prikazuje označeni tekst u poruci koja se može pročitati. (#15858, @Emil-18)
* Microsoft Office:
  * Kada treba pročitati oblikovanje ćelije u Excelu pozadina i rubovi biti će pročitani samo ako takvo oblikovanje postoji. (#15560, @CyrilleB79)
  * NVDA više neće čitati neoznačene grupe kao što su to u posljednjim inačicama Microsoft Office 365 izbornicima. (#15638)
* Opcija za odabir zvučne kartice i opcije načina stišavanja govora uklonjene su iz dijaloškog okvira "Odabir govorne jedinice".
Možete ih pronaći u panelu postavki zvuka koji se može otvoriti pritiskom prečaca `NVDA+control+u`. (#15512, @codeofdusk)
* Opcija "Izgovori tip objekta kada se nađe pod mišem" u postavkama miša je preimenovan u "Pročitaj objekt kada se nađe pod mišem".
Ova opcija izgovara više relevantnih informacija kada se objekt nađe pod mišem poput stanja: označeno ili pritisnuto ili koordinate ćelija u tablici. (#15420, @LeonarddeR)
* Nove stavke su dodane u izbornik pomoć Pomoć obuka i podrška i NV acces trgovina. (#14631)
* Podrška NVDA za [Poedit](https://poedit.net) je kompletno prepisana za inačicu 3 i novije.
Korisnicima Poedita  1 se preporučuje nadogradnja na Poedit 3 ako žele koristiti unapređenu pristupačnost Poedita, kao što su to prečaci za čitanje bilježaka za prevoditelje i komentara. (#15313, #7303, @LeonarddeR)
* Preglednik brajice i preglednik govora od sada su isključeni u Sigurnom načinu. (#15680)
* Prilikom korištenja objektne navigacije, onemogućeni (nedostupni) objekti više neće biti ignorirani. (#15477, @CyrilleB79)
* Dodan sadržaj u dokument "popis tipkovničkih prečaca". (#16106)

### Ispravke grešaka

* Add-on Store:
  * Ako je status dodatka promijenjen kada se nalazi u fokusu, na primjer promjena iz "preuzimanje" u "preuzeto", osvježena se stavka sada potpuno izgovara. (#15859, @LeonarddeR)
  * Prilikom instalacije dodataka instalacijska pitanja se više ne prekrivaju dijaloškim okvirom ponovnog pokretanja. (#15613, @lukaszgo1)
  * Prilikom reinstalacije nekompatibilnog dodatka isti se neće nasilno onemogućavati. (#15584, @lukaszgo1)
  * Onemogućeni i nekompatibilni dodaci se sada mogu ažurirati. (#15568, #15029)
  * NVDA se sada obnavlja i pokazuje grešku u slučaju neuspješnog preuzimanja dodatka. (#15796)
  * NVDA se više ne pokreće ponovno poslije ponovnog otvaranja i zatvaranja Add'on storea. (#16019, @lukaszgo1)
* Zvuk:
  * NVDA se više ne smrzava kada se zvukovi reproduciraju brzo. (#15311, #15757, @jcsteh)
  * Ako je zvučna kartica postavljena na jednu od onih koja nije podrazumijevana a ta kartica postane dostupna, NVDA će se prebaciti na tu zvučnu karticu. (#15759, @jcsteh)
  * NVDA će sada ponovno reproducirati zvuk ako konfiguracija zvučne kartice bude promijenjena ili druga aplikacija prestane ekskluzivno koristiti zvučnu karticu. (#15758, #15775, @jcsteh)
* Brajica:
  * Višeredni brajični redci više neće dovesti upravljački program BRLTTY do rušenja, te su tretirani kao jedan kontinuirani brajični redak. (#15386)
  * Od sada se na brajičnom redku prikazuju objekti koji sadrže koristan tekst. (#15605)
  * Sada ponovno radi upisivanje brajičnih znakova kada se koristi kratkopis. (#15773, @aaclause)
  * Od sada se brajica osvježava prilikom pomicanja objekta navigatora u više situacija (#15755, @Emil-18)
  * Rezultati izgovora trenutnog fokusa, trenutnog objekta navigatora i trenutnog označavanja sada se prikazuju na brajičnom redku. (#15844, @Emil-18)
  * Albatross upravljački program više ne prepoznaje Esp32 mikrokontroler kao Albatross brajični redak. (#15671)
* LibreOffice:
  * Riječi izbrisane uz pomoć prečaca `control+backspace` sada se također ispravno izgovaraju kada nakon izbrisane riječi slijedi bjelina (razmaci i tabulatori). (#15436, @michaelweghorn)
  * Čitanje trake stanja koristeći tipkovnički prečac `NVDA+end` sada također radi u Libre office dialoškim okvirima u inačicama 24.2 i novijim. (#15591, @michaelweghorn)
  * Svi očekivani atributi teksta sada su podržani U Libreoffice inačicama 24.2 i novijim.
  Ova ispravka omogućuje čitanje pravopisnih pogrešaka prilikom čitanja redaka u Writeru. (#15648, @michaelweghorn)
  * Čitanje razine naslova sada također radi u LibreOfficeu inačicama 24.2 i novijim. (#15881, @michaelweghorn)
* Microsoft Office:
  * U Excelu sa isključenim UIA, brajica se osvježava, a aktivni sadržaj ćelije se izgovara, kada se pritisne `control+y`, `control+z` ili `alt+backspace`. (#15547)
  * U Wordu sa isključenim Uia brajica se osvježava kada se pritisnu `control+v`, `control+x`, `control+y`, `control+z`, `alt+backspace`, `backspace` ili `control+backspace`.
  Također se osvježava kada je UIA omogućen, kada se  upisuje tekst, a brajica je povezana na pregled a pregled prati kursor sustava. (#3276)
  * U Wordu, trenutna ćelija će se izgovoriti koristeći izvorne prečace Worda za navigaciju po tablicama `alt+home`, `alt+end`, `alt+pageUp` and `alt+pageDown`. (#15805, @CyrilleB79)
* Izgovaranje tipkovničkih prečaca je unapređeno. (#10807, #15816, @CyrilleB79)
* SAPI4 govorne jedinice sada pravilno podržavaju promjene glasnoće, brzine i visine ugrađene u govor. (#15271, @LeonarddeR)
* Stanje višerednog objekta sada se pravilno čita u aplikacijama koje koriste Java Access Bridge. (#14609)
* NVDA će sada čitati više sadržaja dijaloških okvira za više Windows 10 i 11 dijaloških okvira. (#15729, @josephsl)
* NVDA će sada čitati novu učitanu stranicu u Microsoft Edgeu prilikom korištenja UI automation. (#15736)
* Prilikom korištenja prečaca za čitanje cijelog teksta ili slovkanja teksta, pauze između rečenica ili znakova više se ne smanjuju postupno tokom vremena. (#15739, @jcsteh)
* NVDA više se ne smrzava prilikom čitanja velike količine teksta. (#15752, @jcsteh)
* Prilikom pristupanja Microsoft Edgeu koristeći UI automation, NVDA sada može aktivirati više kontrola u modusu čitanja. (#14612)
* NVDA će se sada pokretati ispravno kada je konfiguracijska datoteka oštećena, ali će se konfiguracija vratiti na zadane vrijednosti kao što je to bilo i u prošlosti. (#15690, @CyrilleB79)
* Ispravljena podrška za System List view (`SysListView32`) kontrole U Windows forms aplikacijama. (#15283, @LeonarddeR)
* Sada nije više moguće nadpisivanje NVDA povijesti Python konzole. (#15792, @CyrilleB79)
* NVDA će ostati brz i stabilan kada postane preopterećen sa UI automation događajima, na primjer prilikom prikazivanja velike količine teksta u Windows terminalu ili prilikom slušanja glasovnih poruka u  WhatsAppu. (#14888, #15169)
  * Ovo novo ponašanje može se isključiti koristeći opciju "Koristi unapređeno procesuiranje događaja" u NVDA naprednim postavkama.
* NVDA sada ponovno može slijediti fokus u aplikacijama unutar Windows defender application guarda (WDAG). (#15164)
* Izgovoreni tekst se više ne ažurira prilikom pomicanja miša u Pregledniku govora. (#15952, @hwf1324)
* NVDA će se opet prebaciti u modus čitanja prilikom zatvaranja odabirnih okvira koristeći tipku `escape` ili `alt+strelicu gore` u Firefox ili Chrome. (#15653)
* Kretanje strelicama gore ili dolje u iTunesu više se neće prebacivati nazad u modus čitanja. (#15653)

### Changes for Developers

Please refer to [the developer guide](https://www.nvaccess.org/files/nvda/documentation/developerGuide.html#API) for information on NVDA's API deprecation and removal process.

* Note: this is an Add-on API compatibility breaking release.
Add-ons will need to be re-tested and have their manifest updated.
* Building NVDA now requires Visual Studio 2022.
Please refer to the [NVDA docs](https://github.com/nvaccess/nvda/blob/release-2024.1/projectDocs/dev/createDevEnvironment.md) for the specific list of Visual Studio components. (#14313)
* Added the following extension points:
  * `treeInterceptorHandler.post_browseModeStateChange`. (#14969, @nvdaes)
  * `speech.speechCanceled`. (#15700, @LeonarddeR)
  * `_onErrorSoundRequested` (should be retrieved calling `logHandler.getOnErrorSoundRequested()`) (#15691, @CyrilleB79)
* It is now possible to use plural forms in an add-on's translations. (#15661, @beqabeqa473)
* Included python3.dll in the binary distribution for use by add-ons with external libraries utilizing the [stable ABI](https://docs.python.org/3.11/c-api/stable.html). (#15674, @mzanm)
* The `BrailleDisplayDriver` base class now has `numRows` and `numCols` properties to provide information about multi line braille displays.
Setting `numCells` is still supported for single line braille displays and `numCells` will return the total number of cells for multi line braille displays. (#15386)
* Updated BrlAPI for BRLTTY to version 0.8.5, and its corresponding python module to a Python 3.11 compatible build. (#15652, @LeonarddeR)
* Added the `speech.speakSsml` function, which allows you to write NVDA speech sequences using [SSML](https://www.w3.org/TR/speech-synthesis11/). (#15699, @LeonarddeR)
  * The following tags are currently supported and translated to appropriate NVDA speech commands:
    * `Prosody` (`pitch`, `rate` and `volume`). Only multiplication (e.g. `200%` are supported.
    * `say-as` with the `interpret` attribute set to `characters`
    * `voice` with the `xml:lang` set to an XML language
    * `break` with the `time` attribute set to a value in milliseconds, e.g. `200ms`
    * `mark` with the `name` attribute set to a mark name, e.g. `mark1`, requires providing a callback
  * Example: `speech.speakSsml('<speak><prosody pitch="200%">hello</prosody><break time="500ms" /><prosody rate="50%">John</prosody></speak>')`
  * The SSML parsing capabilities are backed by the `SsmlParser` class in the `speechXml` module.
* Changes to the NVDA Controller Client library:
  * The file names of the library no longer contain a suffix denoting the architecture, i.e. `nvdaControllerClient32/64.dll` are now called `nvdaControllerClient.dll`. (#15718, #15717, @LeonarddeR)
  * Added an example to demonstrate using nvdaControllerClient.dll from Rust. (#15771, @LeonarddeR)
  * Added the following functions to the controller client: (#15734, #11028, #5638, @LeonarddeR)
    * `nvdaController_getProcessId`: To get the process id (PID) of the current instance of NVDA the controller client is using.
    * `nvdaController_speakSsml`: To instruct NVDA to speak according to the given SSML. This function also supports:
      * Providing the symbol level.
      * Providing the priority of speech to be spoken.
      * Speaking both synchronously (blocking) and asynchronously (instant return).
    * `nvdaController_setOnSsmlMarkReachedCallback`: To register a callback of type `onSsmlMarkReachedFuncType` that is called in synchronous mode for every `<mark />` tag encountered in the SSML sequence provided to `nvdaController_speakSsml`.
  * Note: the new functions in the controller client only support NVDA 2024.1 and above.
* Updated `include` dependencies:
  * detours to `4b8c659f549b0ab21cf649377c7a84eb708f5e68`. (#15695)
  * ia2 to `3d8c7f0b833453f761ded6b12d8be431507bfe0b`. (#15695)
  * sonic to `8694c596378c24e340c09ff2cd47c065494233f1`. (#15695)
  * w3c-aria-practices to `9a5e55ccbeb0f1bf92b6127c9865da8426d1c864`. (#15695)
  * wil to `5e9be7b2d2fe3834a7107f430f7d4c0631f69833`. (#15695)
* Device info yielded by `hwPortUtils.listUsbDevices` now contain the bus reported description of the USB device (key `busReportedDeviceDescription`). (#15764, @LeonarddeR)
* For USB serial devices, `bdDetect.getConnectedUsbDevicesForDriver` and `bdDetect.getDriversForConnectedUsbDevices` now yield device matches containing a `deviceInfo` dictionary enriched with data about the USB device, such as `busReportedDeviceDescription`. (#15764, @LeonarddeR)
* When the configuration file `nvda.ini` is corrupted, a backup copy is saved before it is reinitialized. (#15779, @CyrilleB79)
* When defining a script with the script decorator, the `speakOnDemand` boolean argument can be specified to control if a script should speak while in "on-demand" speech mode. (#481, @CyrilleB79)
  * Scripts that provide information (e.g. say window title, report time/date) should speak in the "on-demand" mode.
  * Scripts that perform an action (e.g. move the cursor, change a parameter) should not speak in the "on-demand" mode.
* Fixed bug where deleting git-tracked files during `scons -c` resulted in missing UIA COM interfaces on rebuild. (#7070, #10833, @hwf1324)
* Fix a bug where some code changes were not detected when building `dist`, that prevented a new build from being triggered.
Now `dist` always rebuilds. (#13372, @hwf1324)
* A `gui.nvdaControls.MessageDialog` with default type of standard, no longer throws a None conversion exception because no sound is assigned. (#16223, @XLTechie)

#### API Breaking Changes

These are breaking API changes.
Please open a GitHub issue if your Add-on has an issue with updating to the new API.

* NVDA is now built with Python 3.11. (#12064)
* Updated pip dependencies:
  * configobj to 5.1.0dev commit `e2ba4457c4651fa54f8d59d8dcdd3da950e956b8`. (#15544)
  * Comtypes to 1.2.0. (#15513, @codeofdusk)
  * Flake8 to 4.0.1. (#15636, @lukaszgo1)
  * py2exe to 0.13.0.1dev commit `4e7b2b2c60face592e67cb1bc935172a20fa371d`. (#15544) 
  * robotframework to 6.1.1. (#15544)
  * SCons to 4.5.2. (#15529, @LeonarddeR)
  * sphinx to 7.2.6. (#15544)
  * wxPython to 4.2.2a commit `0205c7c1b9022a5de3e3543f9304cfe53a32b488`. (#12551, #16257)
* Removed pip dependencies:
  * typing_extensions, these should be supported natively in Python 3.11 (#15544)
  * nose, instead unittest-xml-reporting is used to generate XML reports. (#15544)
* `IAccessibleHandler.SecureDesktopNVDAObject` has been removed.
Instead, when NVDA is running on the user profile, track the existence of the secure desktop with the extension point: `winAPI.secureDesktop.post_secureDesktopStateChange`. (#14488)
* `braille.BrailleHandler.handlePendingCaretUpdate` has been removed with no public replacement. (#15163, @LeonarddeR)
* `bdDetect.addUsbDevices and bdDetect.addBluetoothDevices` have been removed.
Braille display drivers should implement the `registerAutomaticDetection` class method instead.
That method receives a `DriverRegistrar` object on which the `addUsbDevices` and `addBluetoothDevices` methods can be used. (#15200, @LeonarddeR)
* The default implementation of the check method on `BrailleDisplayDriver` now requires both the `threadSafe` and `supportsAutomaticDetection` attributes to be set to `True`. (#15200, @LeonarddeR)
* Passing lambda functions to `hwIo.ioThread.IoThread.queueAsApc` is no longer possible, as functions should be weakly referenceable. (#14627, @LeonarddeR)
* `IoThread.autoDeleteApcReference` has been removed. (#14924, @LeonarddeR)
* To support capital pitch changes, synthesizers must now explicitly declare their support for the `PitchCommand` in the `supportedCommands` attribute on the driver. (#15433, @LeonarddeR)
* `speechDictHandler.speechDictVars` has been removed. Use `NVDAState.WritePaths.speechDictsDir` instead of `speechDictHandler.speechDictVars.speechDictsPath`. (#15614, @lukaszgo1)
* `languageHandler.makeNpgettext` and `languageHandler.makePgettext` have been removed.
`npgettext` and `pgettext` are supported natively now. (#15546)
* The app module for [Poedit](https://poedit.net) has been changed significantly. The `fetchObject` function has been removed. (#15313, #7303, @LeonarddeR)
* The following redundant types and constants have been removed from `hwPortUtils`: (#15764, @LeonarddeR)
  * `PCWSTR`
  * `HWND` (replaced by `ctypes.wintypes.HWND`)
  * `ULONG_PTR`
  * `ULONGLONG`
  * `NULL`
  * `GUID` (replaced by `comtypes.GUID`)
* `gui.addonGui.AddonsDialog` has been removed. (#15834)
* `touchHandler.TouchInputGesture.multiFingerActionLabel` has been removed with no replacement. (#15864, @CyrilleB79)
* `NVDAObjects.IAccessible.winword.WordDocument.script_reportCurrentHeaders` has been removed with no replacement. (#15904, @CyrilleB79)
* The following app modules are removed.
Code which imports from one of them, should instead import from the replacement module. (#15618, @lukaszgo1)

| Removed module name |Replacement module|
|---|---|
|`azardi-2.0` |`azardi20`|
|`azuredatastudio` |`code`|
|`azuredatastudio-insiders` |`code`|
|`calculatorapp` |`calculator`|
|`code - insiders` |`code`|
|`commsapps` |`hxmail`|
|`dbeaver` |`eclipse`|
|`digitaleditionspreview` |`digitaleditions`|
|`esybraille` |`esysuite`|
|`hxoutlook` |`hxmail`|
|`miranda64` |`miranda32`|
|`mpc-hc` |`mplayerc`|
|`mpc-hc64` |`mplayerc`|
|`notepad++` |`notepadPlusPlus`|
|`searchapp` |`searchui`|
|`searchhost` |`searchui`|
|`springtoolsuite4` |`eclipse`|
|`sts` |`eclipse`|
|`teamtalk3` |`teamtalk4classic`|
|`textinputhost` |`windowsinternal_composableshell_experiences_textinput_inputapp`|
|`totalcmd64` |`totalcmd`|
|`win32calc` |`calc`|
|`winmail` |`msimn`|
|`zend-eclipse-php` |`eclipse`|
|`zendstudio` |`eclipse`|

#### Deprecations

* Using `watchdog.getFormattedStacksForAllThreads` is deprecated - please use `logHandler.getFormattedStacksForAllThreads` instead. (#15616, @lukaszgo1)
* `easeOfAccess.canConfigTerminateOnDesktopSwitch` has been deprecated, as it became obsolete since Windows 7 is no longer supported. (#15644, @LeonarddeR)
* `winVersion.isFullScreenMagnificationAvailable` has been deprecated - use `visionEnhancementProviders.screenCurtain.ScreenCurtainProvider.canStart` instead. (#15664, @josephsl)
* The following Windows release constants has been deprecated from winVersion module (#15647, @josephsl):
  * `winVersion.WIN7`
  * `winVersion.WIN7_SP1`
  * `winVersion.WIN8`
* The `bdDetect.KEY_*` constants have been deprecated.
Use `bdDetect.DeviceType.*` instead. (#15772, @LeonarddeR).
* The `bdDetect.DETECT_USB` and `bdDetect.DETECT_BLUETOOTH` constants have been deprecated with no public replacement. (#15772, @LeonarddeR).
* Using `gui.ExecAndPump` is deprecated - please use `systemUtils.ExecAndPump` instead. (#15852, @lukaszgo1)

## 2023.3.4

Ovo je verzija zakrpe koja ispravlja problem s instalacijom i jedan skgurnosni prropust.
Molimo odgovorno izvještavajte o sigurnosnim propustima prateći [NVDA politiku sigurnosti](https://github.com/nvaccess/nvda/blob/master/security.md).

### Ispravke sigurnosti

* Onemogućeno učitavanje koda prilikom prisilnog uključivanja sigurnog načina.
([GHSA-727q-h8j2-6p45](https://github.com/nvaccess/nvda/security/advisories/GHSA-727q-h8j2-6p45))

### Ispravke grešaka

* Ispravljena greška prilikom koje NVDA proces se nije mogao ispravno prekinuti. (#16123)
* Ispravljena pogreška, prilikom koje ako prethodni NVDA proces NVDA se neuspješno prekine, NVDA instalacija može završiti i stanju neoporavljivosti. (#16122)

## 2023.3.3

Ovo je verzija zakrpe koja ispravlja sigurnosni propust.
Molimo odgovorno prijavljujte probleme sigurnosti u skladu sa NVDA [politikom sigurnosti](https://github.com/nvaccess/nvda/blob/master/security.md).

### Ispravke sigurnosnih propusta

* Prevencija mogućeg povratnog XSS izgrađenog koda koji prouzrokuje arbitrarno izvršavanje koda.
([GHSA-xg6w-23rw-39r8](https://github.com/nvaccess/nvda/security/advisories/GHSA-xg6w-23rw-39r8))

## 2023.3.2

Ovo je verzija zakrpe koja ispravlja sigurnosni propust.
Sigurnosni propust iz verzije 2023.3.1 nije bio implementiran ispravno.
Molimo odgovorno prijavljujte probleme sigurnosti u skladu sa NVDA [politikom sigurnosti](https://github.com/nvaccess/nvda/blob/master/security.md).

### Ispravke sigurnosti

* Sigurnosni propust iz verzije 2023.3.1 nije bio implementiran ispravno.
Prevenira mogući pristup sustavu i arbitrarno pokretanje koda sa privilegijama sustava za neautentificirane korisnike.
([GHSA-h7pp-6jqw-g3pj](https://github.com/nvaccess/nvda/security/advisories/GHSA-h7pp-6jqw-g3pj))

## 2023.3.1

Ovo je verzija zakrpe koja ispravlja sigurnosni propust.
Molimo odgovorno prijavljujte probleme sigurnosti u skladu sa NVDA [politikom sigurnosti](https://github.com/nvaccess/nvda/blob/master/security.md).

### Ispravke sigurnosti

* Prevenira mogući pristup sustavu i arbitrarno pokretanje koda sa privilegijama sustava za neautentificirane korisnike.
([GHSA-h7pp-6jqw-g3pj](https://github.com/nvaccess/nvda/security/advisories/GHSA-h7pp-6jqw-g3pj))

## 2023.3

Ova inačica uključuje poboljšanja stabilnosti i performansi pri izlazu zvuka.
Dodane su opcije za kontrolu glasnoće NVDA zvukova i zvučnih signala, ili ujednačavanja sa glasnoćom glasa koji koristite.

NVDA može s vremena na vrijeme osvježavati rezultate prepoznavanja teksta kada se pojave.
Ovo se može konfigurirati u Windows OCR kategoriji u dijaloškom okviru postavki NVDA.

Dodane su ispravke za brajične redke, uključujući automatsko otkrivanje.
Sada je moguće isključiti upravljačke programe iz procesa automatskog otkrivanjau cilju poboljšanja performansi.
Dodane su također nove komande za Brltty.

Ispravljene su greške u Add-on Storeu, Microsoft Officeu, Microsoft Edge kontekstnim izbornicima i u Windows kalkulatoru.

### Nove značajke

* Unapređeno upravljanje zvukom:
  * Novi panel postavki zvuka:
    * Može se otvoriti tipkovničkim prečacom `NVDA+control+u`. (#15497)
    * Opcija koja omogućuje ujednačavanje glasnoće zvukova sa glasnoćom govorne jedinice koju koristite. (#1409)
    * Opcija za odvojenu konfiguraciju glasnoće NVDA zvukova. (#1409, #15038)
    * Opcije za promjenu zvučne kartice i utišavanje zvukova premještene su u novu kategoriju postavki zvuka iz dijaloškog okvira odabira govorne jedinice.
    Ove će opcije biti uklonjene iz dijaloškog okvira  "odaberi govornu jedinicu" u inačici 2024.1. (#15486, #8711)
  * NVDA will now output audio via the Windows Audio Session API (WASAPI), which may improve the responsiveness, performance and stability of NVDA speech and sounds. (#14697, #11169, #11615, #5096, #10185, #11061)
  * Upozorenje: WASAPI je nekompatibilan sa nekim dodacima.
  Dostupne su kompatibilne nadogradnje tih dodataka, Nadogradite ih prije nadogradnje NVDA.
  Nekompatibilne verzije tih dodataka bit će isključene prilikom nadogradnje NVDA:
    * Tony's Enhancements inačica 1.15 ili starija. (#15402)
    * NVDA global commands extension 12.0.8 ili starija. (#15443)
* NVDA sada može kontinuirano osvježavati rezultat prepoznavanja teksta kada se pojavi novi tekst. (#2797)
  * Kako biste uključili ovu opciju, molimo uključite opciju "S vremena na vrijeme osvježavaj sadržaj prepoznavanja" u kategoriji Windows Ocr u NVDA postavkama.
  * Kada je ova opcija uključena, možete uključiti ili isključiti izgovor novog teksta tako da uključite ili isključite čitanje dinamičkog sadržaja (pritiskom `NVDA+5`).
* Prilikom korištenja automatskog otkrivanja brajičnih redaka, sada je moguće onemogućiti upravljačke programe sa popisa automatski otkrivanih u dijaloškom okviru izbora brajičnog redka. (#15196)
* Nova opcija u opcijama oblikovanja dokumenta, "Ignoriraj prazne redke prilikom čitanja uvlačenja". (#13394)
* Dodana nedodijeljena gesta za kretanje po grupiranjima kartica svojstva u načinu pregleda. (#15046)

### izmjene

* Brajica:
  * Kada se tekst u naredbenom redku promijeni bez promjene fokusa, tekst na brajičnom redku će se također obnoviti kada se nalazite na tom redku.
  Ovo uključuje situacije kada je brajica povezana na pregled. (#15115)
  * Više Brltty prečaca je povezana sa NVDA prečacima (#6483):
    * `learn`: uključi isključi pomoć pri unosu
    * `prefmenu`: otvori nVDA izbornik
    * `prefload`/`prefsave`: učitaj spremi NVDA konfiguraciju
    * `time`: pokaži vrijeme
    * `say_line`: Izgovori redak na kojem se nalazi pregledni kursor
    * `say_below`: Čitaj sve koristeći pregledni kursor
  * BRLTTY upravljački program je dostupan samo kada je Brltty pokrenut sa BRL api. (#15335)
  * Napredna postavka za isključivanje HID brajičnog redka  sada je uklonjena i zamijenjena novom opcijom.
  Sada možete isključiti određene upravljačke programe za automatsko prepoznavanje u dijaloškom okviru brajičnih postavki. (#15196)
* Add-on Store: dodaci će sada biti dostupni na kartici svojstva dostupnih dodataka, ako su dostupni u Add-on storeu. (#15374)
* Osvježeni su neki prečaci u NVDA izborniku. (#15364)

### Ispravke grešaka

* Microsoft Office:
  * Ispravljeno rušenje u Microsoft Word Kada su opcije u postavkama oblikovanja "čitaj naslove" i "čitaj komentare i bilješke" isključene. (#15019)
  * U Wordu i Excelu, poravnanje će biti ispravno pročitano u više situacija. (#15206, #15220)
  * Ispravljeno čitanje nekih prečaca oblikovanja u Excelu. (#15527)
* Microsoft Edge:
  * NVDA se više neće vraćati na prethodnu poziciju u modusu čitanja pri otvaranju kontekstnog izbornika u Microsoft Edgeu. (#15309)
  * NVDA opet može čitati kontekstni izbornik preuzimanja u Microsoft Edgeu. (#14916)
* Brajica:
  * Brajični kursor i pokazivač označenosti bit će ispravno osvježeni poslije uključenja ili isključenja gestom. (#15115)
  * Ispravljena pogreška prilikom koje su se Albatros brajični redci pokušali inicijalizirati čak iako je drugi brajični redak bio spojen. (#15226)
* Add-on Store:
  * Ispravljena greška poslije odznačavanja "uključi nekompatibilne dodatke" koja je prouzrokovala vidljivost nekompatibilnih dodataka. (#15411)
  * Dodaci blokirani zbog nekompatibilnosti bi se sada trebali pravilno osvježavati prilikom sortiranja po statusu uključenosti ili isključenosti. (#15416)
  * Ispravljena pogreška nadpisivanja ili nadogradnje dodataka koristeći ručnu instalaciju. (#15417)
  * Ispravljena pogreška prilikom koje NVDA neće govoriti poslije ponovnog pokretanja i završetka NVDA instalacije. (#14525)
  * Ispravljena pogreška  pri instalaciji dodataka ako je prethodna instalacija ili preuzimanje prekinuto. (#15469)
  * Ispravljene pogreške s rukovanjem nekompatibilnim dodacima pri nadogradnji NVDA. (#15414, #15412, #15437)
* NVDA opet izgovara rezultate računskih operacija u 32-bitnom kalkulatoru za Windows u operacijskim sustavima Server, LTSC i LTSB. (#15230)
* NVDA više ne ignorira izmjene fokusa kada višeslojni prozor (prozor koji se nalazi iznad drugog prozora) postane fokusiran. (#15432)
* Ispravljeno moguće rušenje prilikom pokretanja NVDA. (#15517)

### Changes for Developers

Please refer to [the developer guide](https://www.nvaccess.org/files/nvda/documentation/developerGuide.html#API) for information on NVDA's API deprecation and removal process.

* `braille.handler.handleUpdate` and `braille.handler.handleReviewMove` have been changed in order not to update instantly.
Before this change, when either of these methods was called very often, this would drain many resources.
These methods now queue an update at the end of every core cycle instead.
They should also be thread safe, making it possible to call them from background threads. (#15163)
* Added official support to register custom braille display drivers in the automatic braille display detection process.
Consult the `braille.BrailleDisplayDriver` class documentation for more details.
Most notably, the `supportsAutomaticDetection` attribute must be set to `True` and the `registerAutomaticDetection` `classmethod` must be implemented.  (#15196)

#### Deprecations

* `braille.BrailleHandler.handlePendingCaretUpdate` is now deprecated with no public replacement.
It will be removed in 2024.1. (#15163)
* Importing the constants `xlCenter`, `xlJustify`, `xlLeft`, `xlRight`, `xlDistributed`, `xlBottom`, `xlTop` from `NVDAObjects.window.excel` is deprecated.
Use `XlHAlign` or `XlVAlign` enumerations instead. (#15205)
* The mapping `NVDAObjects.window.excel.alignmentLabels` is deprecated.
Use the `displayString` methods of `XlHAlign` or `XlVAlign` enumerations instead. (#15205)
* `bdDetect.addUsbDevices` and `bdDetect.addBluetoothDevices` have been deprecated.
Braille display drivers should implement the `registerAutomaticDetection` classmethod instead.
That method receives a `DriverRegistrar` object on which the `addUsbDevices` and `addBluetoothDevices` methods can be used. (#15200)
* The default implementation of the check method on `BrailleDisplayDriver` uses `bdDetect.driverHasPossibleDevices` for devices that are marked as thread safe.
Starting from NVDA 2024.1, in order for the base method to use `bdDetect.driverHasPossibleDevices`, the `supportsAutomaticDetection` attribute must be set to `True` as well. (#15200)

## 2023.2

Ova verzija dodaje add-on store koja Zamjenjuje upravljanje dodacima.
U  Add-on storeu možete pregledavati, pretraživati, instalirati i ažurirati dodatke zajednice.
Sada možete ručno ignorirati probleme kompatibilnosti sa zastarjelim dodacima na vlastitu odgovornost.

Dodane su nove funkcije za brajične redke, prečice i novi podržani brajični redci.
Također su dodate nove prečice za OCR i rasklopljeni prikaz kroz objekte.
Navigacija i čitanje oblikovanja u Microsoft Office paketu je poboljšana.

Puno grešaka je ispravljeno, posebno za brajične redke, Microsoft Office, web preglednike i Windows 11.

eSpeak-NG, LibLouis braille translator, i Unicode CLDR su ažurirani.

### Nove značajke

* Add-on store je dodan u NVDA. (#13985)
  * Pregled, pretraga, instalacija i ažuriranje dodataka zajednice.
  * Ručno učitajte nekompatibilne NVDA dodatke.
  * upravitelj dodacima je uklonjen i zamenjen add-on store.
  * za više informacija molimo pročitajte ažurirani korisnički priručnik.
* Novi prečaci:
  * Nova ulazna gesta bez dodijeljenog prečaca za kruženje kroz dostupne jezike za Windows OCR. (#13036)
  * nova ulazna gesta bez dodijeljenog prečaca za kruženje kroz moduse prikazivanja poruka na brajičnom redku. (#14864)
  * Ulazna gesta bez dodijeljenog prečaca za uključivanje ili isključivanje indikacije označavanja. (#14948)
  * Dodani podrazumjevani prečaci na tipkovnice za kretanje na sljedeći ili prethodni objekt u raskropljenom prikazu hierarhije objekata. (#15053)
    * stolno računalo: `NVDA+numerički9` i `NVDA+numerički3` za kretanje na slijedeći ili prethodni objekt.
    * prijenosno računalo: `šift+NVDA+[` i `šift+NVDA+]` za kretanje na prethodni i slijedeći objekt.
* Nove funkcije za brajične retke:
  * Dodana podrška za Help Tech Activator brajični redak. (#14917)
  * Nova opcija za uključivanje ili isključivanje prikazivanja indikacije označenosti (točkice 7 i 8). (#14948)
  * Nova opcija za pomicanje kursora sustava ili fokusa pri promjeni pozicije preglednog kursora gumbima na brajičnom redku. (#14885, #3166)
  * Kada se pritisne `numerički2` tri puta za čitanje brojčane vrijednosti znaka na poziciji preglednog kursora, informacija se također pruža na brajičnom redku. (#14826)
  * Dodata podrška za `aria-brailleroledescription` ARIA 1.3 atribut, koji će dozvoliti autorima web stranica zamjenu vrste elementa koja će se prikazati na brajičnom redku. (#14748)
  * Upravljački program za Baum brajične redke: Dodano nekoliko vezanih brajičnih prečaca za izvršavanje čestih prečica na tastaturi kao što su `windows+d` i `alt+tab`.
  Molimo pogledajte NVDA korisničko uputstvo za potpun popis. (#14714)
* Dodan izgovor Unicode znakova:
  * brajični znakovi kao što su `⠐⠣⠃⠗⠇⠐⠜`. (#14548)
  * Znak za Mac tipku opcije `⌥`. (#14682)
* Dodani prečaci za Tivomatic Caiku Albatross brajične redke. (#14844, #15002)
  * prikaz dijaloškog okvira brajičnih postavki
  * Pristup traci stanja
  * promjena oblika brajičnog kursora
  * promjena modusa prikazivanja poruka
  * Uključivanje i isključivanje brajičnog kursora
  * Uključivanje i isključivanje kursora označavanja na brajičnom redku
  * Promjena opcije "Pomakni kursor sustava prilikom usmjeravanja kursora pregleda ". (#15122)
* Značajke Microsoft Office:
  * Kada se omogući čitanje istaknutog teksta u opcijama oblikovanja dokumenta, boje isticanja se sada čitaju u Microsoft Wordu. (#7396, #12101, #5866)
  * Kada se uključi čitanje boja u opcijama oblikovanja dokumenta, boje pozadine se sada čitaju u Microsoft Wordu. (#5866)
  * Kada se koriste Excel prečaci za uključivanje ili isključivanje opcija oblikovanja poput podebljanih, kosih, podcrtanih i prekriženih slova za ćeliju u Excelu, rezultat se sada čita. (#14923)
* Eksperimentalno poboljšano upravljanje zvukom:
  * NVDA sada može reproducirati zvukove putem standarda Windows Audio Session API (WASAPI), što može poboljšati brzinu, performanse i stabilnost NVDA govora i zvukova.
  * Korištenje WASAPI se može omogućiti u naprednim postavkama.
  Također, ako je WASAPI omogućen, sljedeće napredne postavke se mogu regulirati.
    * Opcija koja prouzrokuje praćenje glasnoće NVDA govornog izlaza i zvučnih signala. (#1409)
    * Opcija za odvojeno postavljanje glasnoće NVDA zvukova. (#1409, #15038)
  * Postoji poznat problem sa povremenim rušenjem kada je WASAPI omogućen. (#15150)
* U preglednicima Mozilla Firefox i Google Chrome, NVDA sada čita ako kontrola otvara dijaloški okvir, mrežu, popis ili stablasti prikaz ako je autor ovo označio uz pomoć `aria-haspopup` atributa . (#14709)
* Sada je moguće koristiti varijable  sustava (poput  `%temp%` ili  `%homepath%`) pri određivanju putanje pri stvaranju NVDA prijenosne kopije. (#14680)
* Dodana podrška za brajični redak Help Tech Activator. (#14917)
* u ažuriranju Windowsa 10 za svibanj 2019 i novijim, NVDA može izgovarati imena virtualnih radnih površina kada se otvaraju, mijenjaju ili zatvaraju. (#5641)
* Dodan je sveopći parametar sustava koji će dozvoliti korisnicima i administratorima sustava prisilno pokretanje NVDA u sigurnom modusu. (#10018)

### Izmjene

* Ažurirane komponente:
  * eSpeak NG je ažuriran na inačicu 1.52-dev commit `ed9a7bcf`. (#15036)
  * Ažuriran LibLouis brajični prevoditelj na inačicu [3.26.0](https://github.com/liblouis/liblouis/releases/tag/v3.26.0). (#14970)
  * CLDR je ažuriran na inačicu 43.0. (#14918)
* Izmjene u LibreOffice paketu:
  * Kada se čita pozicija preglednog kursora, trenutna pozicija kursora se sada čita u odnosu na trenutnu stranicu u programu LibreOffice Writer za LibreOffice inačicu 7.6 i novije, slično čitanju u programu Microsoft Word. (#11696)
  * Kada se prebacite na neku drugu ćeliju u programu LibreOffice Calc, NVDA više neće neispravno izgovarati koordinate prethodno fokusirane ćelije kada se izgovor koordinata ćelija onemogući u NVDA postavkama. (#15098)
  * Izgovor trake stanja (na primjer kada se pritisne `NVDA+end`) radi u paketu LibreOffice. (#11698)
* Promjene za brajične redke:
  * Kada se koristi brajični redak uz pomoć za Hid brajični standard, dpad se sada može koristiti za emuliranje strelica tipkovnice i entera.
Takođe,  `razmaknica+točka1` i `razmaknica+točka4` sada se koriste kao strelice dole i gore. (#14713)
  * Ažuriranja dinamičkog sadržaja na Web stranicama (ARIA žive regije) se sada prikazuju na brajičnom redku.
Ovo se može onemogućiti na panelu naprednih postavki. (#7756)
* Simboli crtica i spojnica će uvijek biti poslani sintetizatoru. (#13830)
* Udaljenost koju Microsoft Word čita će sada poštovati mjernu jedinicu koja je postavljena u naprednim postavkama Worda čak i kada se koristi UIA za pristup Word dokumentima. (#14542)
* NVDA brže reagira kada se pomiće kursor u kontrolama za uređivanje. (#14708)
* Skripta za prijavljivanje odredišta poveznice sada čita sa pozicije kursora ili fokusa umesto objekta navigatora. (#14659)
* Stvaranje prenosne kopije više ne zahtijeva upisivanje slova diska kao dio apsolutne putanje. (#14680)
* Ako je Windows postavljen da prikazuje sekunde na satu područja obavijesti, korištenje prečaca `NVDA+f12` za čitanje vremena sada prati ovo podešavanje. (#14742)
* NVDA će sada prijavljivati grupe bez oznake koje imaju korisne informacijje o poziciji, kakve se mogu pronaći u novijim  inačicama Microsoft Office 365 izbornika. (#14878) 

### Ispravke grešaka

* Brajični redci:
  * Nekoliko poboljšanja u stabilnosti unosa/prikaza na brajičnom redku, što će smanjiti učestalost grešaka i rušenja programa NVDA. (#14627)
  * NVDA se više neće bespotrebno prebacivati na opciju bez brajice više puta u toku automatskog prepoznavanja, što donosi zapisnike i manje opterećenje. (#14524)
  * NVDA će se sada prebacivati na USB ako HID Bluetooth uređaj (kao što je HumanWare Brailliant ili APH Mantis) automatski bude prepoznat i USB veza postane dostupna.
  Ovo je ranije radilo samo za Bluetooth serijske portove. (#14524)
  * Kada nijedan brajični redak nije povezan i preglednik brajičnog redka se zatvori pritiskanjem `alt+f4` ili klikom na gumb zatvori, veličina brajevog podsistema će ponovo biti vraćena na bez ćelija. (#15214)
* Web preglednici:
  * NVDA više neće ponekad izazivati rušenje ili prestanak rada programa Mozilla Firefox. (#14647)
  * U pretraživačima Mozilla Firefox i Google Chrome, upisani znakovi se više ne prijavljuju u nekim poljima za unos teksta čak i kada je izgovor upisanih znakova isključen. (#8442)
  * Sada možete koristiti modus pretraživanja u Chromium umetnutim kontrolama u kojima to ranije nije bilo moguće. (#13493, #8553)
  * U Mozilli Firefox, pomicanje miša do teksta nakon linka sada ispravno čita tekst. (#9235)
  * Odredište linkova na slikama se sada preciznije ispravno čita u većini slučajeva u programima Chrome i Edge. (#14779)
  * Kada pokušavate čitati adresu poveznice bez href atributa NVDA više neće biti bez govora.
  Umesto toga NVDA će prijaviti da poveznica  nema odredište. (#14723)
  * U modusu pretraživanja, NVDA neće neispravno ignorirati pomeranje fokusa na glavnu kontrolu ili kontrolu unutar nje na primer pomicanje sa kontrole na njenu unutrašnju stavku popisa ili ćeliju mreže. (#14611)
   * Napomena međutim da se ova ispravka primenjuje samo kada je opcija "Automatsko postavljanje fokusa na stavke koje se mogu fokusirati" u postavkama modusa pretraživanja isključena (što je podrazumevano postaka).
* Ispravke za Windows 11:
  * NVDA ponovo može izgovarati sadržaj trake stanja u bloku za pisanje. (#14573)
  * Prebacivanje između kartica će izgovoriti ime i poziciju nove kartice u bloku za pisanje i upravitelju datoteka. (#14587, #14388)
  * NVDA će ponovo izgovarati dostupne unose kada se tekst piše na jezicima kao što su Kineski i Japanski. (#14509)
  * Ponovo je moguće otvoriti popis doprinositelja ili licencu iz menija NVDA pomoći. (#14725)
* Microsoft Office ispravke:
  * Kada se brzo krećete kroz ćelije u Excelu, manja je vjerojatnost prijavljivanja pogrešne ćelije ili pogrešnog odabira. (#14983, #12200, #12108)
  * Kada stanete na Excel ćeliju van radnog lista, brajični redak i označavanje fokusa se više neće bespotrebno ažurirati na objekt koji je ranije bio fokusiran. (#15136)
  * NVDA sada uspješno izgovara fokusiranje na polja za lozinke u programima Microsoft Excel i Outlook. (#14839)
* Za simbole koji nemaju opis na trenutnom jeziku, podrazumjevana Engleska razina simbola će se koristiti. (#14558, #14417)
* Sada je moguće koristiti znak obrnuta kosa crta u polju zamjene unosa rječnika, kada tip nije postavljen kao pravilni izraz. (#14556)
* U kalkulatoru u  Windowsima 10 i 11, a prijenosna kopija NVDA će pravilno čitati izraze u kompaktnom načinu. (#14679)
* NVDA se ponovo oporavlja u brojnim slučajevima kao što su aplikacije koje više ne reagiraju, što je ranije izazivalo da NVDA u potpunosti prestane raditi. (#14759) 
* Kada želite prisilno koristitiUIA podršku u određenim Terminalima i konzolama, ispravljena je greška koja je izazivala rušenje i neprestano pisanje podataka  u zapisniku. (#14689)
* NVDA više neće odbijati spremanje konfiguracije nakon vraćanja postavki na tvorničke. (#13187)
* Kada se pokreće privremena kopija iz instalacije, NVDA neće korisnicima davati pogrešne informacije da postavke mogu biti spremljena. (#14914)
* NVDA sada brže reagira na prečace i promjene fokusa. (#14928)
* Prikazivanje OCR postavki više neće biti neuspješno na nekim sistemima. (#15017)
* Ispravljena greška vezana za spremanje i vraćanje NVDA postavki, uključujući promjenu sintetizatora. (#14760)
* Ispravljena greška koja je izazvala da u pregledu teksta pokret "Povlačenje gore" pomiće stranice umjesto prelaska na prethodni redak. (#15127)

### Changes for Developers

Please refer to [the developer guide](https://www.nvaccess.org/files/nvda/documentation/developerGuide.html#API) for information on NVDA's API deprecation and removal process.

* Suggested conventions have been added to the add-on manifest specification.
These are optional for NVDA compatibility, but are encouraged or required for submitting to the Add-on Store. (#14754)
  * Use `lowerCamelCase` for the name field.
  * Use `<major>.<minor>.<patch>` format for the version field (required for add-on datastore).
  * Use `https://` as the schema for the url field (required for add-on datastore).
* Added a new extension point type called `Chain`, which can be used to iterate over iterables returned by registered handlers. (#14531)
* Added the `bdDetect.scanForDevices` extension point.
Handlers can be registered that yield `BrailleDisplayDriver/DeviceMatch` pairs that don't fit in existing categories, like USB or Bluetooth. (#14531)
* Added extension point: `synthDriverHandler.synthChanged`. (#14618)
* The NVDA Synth Settings Ring now caches available setting values the first time they're needed, rather than when loading the synthesizer. (#14704)
* You can now call the export method on a gesture map to export it to a dictionary.
This dictionary can be imported in another gesture by passing it either to the constructor of `GlobalGestureMap` or to the update method on an existing map. (#14582)
* `hwIo.base.IoBase` and its derivatives now have a new constructor parameter to take a `hwIo.ioThread.IoThread`.
If not provided, the default thread is used. (#14627)
* `hwIo.ioThread.IoThread` now has a `setWaitableTimer` method to set a waitable timer using a python function.
Similarly, the new `getCompletionRoutine` method allows you to convert a python method into a completion routine safely. (#14627)
* `offsets.OffsetsTextInfo._get_boundingRects` should now always return `List[locationHelper.rectLTWH]` as expected for a subclass of `textInfos.TextInfo`. (#12424)
* `highlight-color` is now a format field attribute. (#14610)
* NVDA should more accurately determine if a logged message is coming from NVDA core. (#14812)
* NVDA will no longer log inaccurate warnings or errors about deprecated appModules. (#14806)
* All NVDA extension points are now briefly described in a new, dedicated chapter in the Developer Guide. (#14648)
* `scons checkpot` will no longer check the `userConfig` subfolder anymore. (#14820)
* Translatable strings can now be defined with a singular and a plural form using `ngettext` and `npgettext`. (#12445)

#### Deprecations

* Passing lambda functions to `hwIo.ioThread.IoThread.queueAsApc` is deprecated.
Instead, functions should be weakly referenceable. (#14627)
* Importing `LPOVERLAPPED_COMPLETION_ROUTINE` from `hwIo.base` is deprecated.
Instead import from `hwIo.ioThread`. (#14627)
* `IoThread.autoDeleteApcReference` is deprecated.
It was introduced in NVDA 2023.1 and was never meant to be part of the public API.
Until removal, it behaves as a no-op, i.e. a context manager yielding nothing. (#14924)
* `gui.MainFrame.onAddonsManagerCommand` is deprecated, use `gui.MainFrame.onAddonStoreCommand` instead. (#13985)
* `speechDictHandler.speechDictVars.speechDictsPath` is deprecated, use `NVDAState.WritePaths.speechDictsDir` instead. (#15021)
* Importing `voiceDictsPath` and `voiceDictsBackupPath` from `speechDictHandler.dictFormatUpgrade` is deprecated.
Instead use `WritePaths.voiceDictsDir` and `WritePaths.voiceDictsBackupDir` from `NVDAState`. (#15048)
* `config.CONFIG_IN_LOCAL_APPDATA_SUBKEY` is deprecated.
Instead use `config.RegistryKey.CONFIG_IN_LOCAL_APPDATA_SUBKEY`. (#15049)

## 2023.1

Dodana je nova opcija, "stil odlomka" u kategoriji "kretanje po dokumentu".
Ona se može koristiti u tekstualnim editorima koji ne podržavaju nativno kretanje po odlomcima, kao što su to Notepad i Notepad++.

Dodan je novi prečac za čitanje odredišta na koje vodi poveznica, određen kao `NVDA+k`.

Podrška za anotiran web sadržaj (poput komentara i rubnih bilježaka) je unaprijeđena.
Pritišćite `NVDA+d` kako biste se kretali po sadržajima (na primjer "ima komentar, ima rubnu bilješku").

Tivomatic Caiku Albatross 46/80 brajični redci su sada podržani.

Podrška za ARM64 i AMD64 inačica sustava Windows je unapređena.

Ispravljeno je mnoštvo grešaka, među kojima ispravke za Windows 11 čine većinu.

eSpeak, LibLouis, Sonic povećivač brzine i Unicode su ažurirani.
Dodane su nove brajične tablice za gruzijski, Swahili (Kenija) i Chichewa (Malawi).

Upozorenje:
U ovoj inačici narušena je kompatibilnost s postojećim dodacima.
-

### Nove značajke

* Microsoft Excel s sučeljem UI automation: automatsko čitanje zaglavlja i stupaca tablica. (#14228)
  * Upozorenje: ovo se odnosi na tablice oblikovane uz pomoć gumba "tablica" na kratici umetanje na ribbonu.
  "prvi stupac" i "zaglavlje redka" u "opcijama stila tablice" odnose se na zaglavlja redaka i stupaca.
  * Ovo se ne odnosi na specifična zaglavlja čitača zaslona  uz pomoć imenovanih raspona, koje se ne podržavaju uz pomoć UI automation.
* Dodan je nedodijeljen prečac za uključivanje i isključivanje opisa znakova poslije kursora. (#14267)
* Dodana je podrška za čitanje sadržaja naredbenog redka uz pomoć UIA obavijesti, što ima za cilj unađređenje stabilnosti i responsivnosti. (#13781)
  * Kako biste saznali koja su ograničenja ove opcije, molimo pogledajte korisnički vodič za više informacija.
* U Windowsima 11 ARM64, modus pregleda je sada dostupan u AMD64 aplikacijama poput Firefoxa, Google Chromea i 1Passworda. (#14397)
* Nova opcija je dodana, "Stil odlomaka" u kategoriji "kretanje po dokumentu".
Ovo dodaje podršku za kretanje po pojedinačnim prijelomima redka (normalnim) i višerednim prijelomima redka (blokovnim). 
Ovo se može koristiti sa editorima teksta koji ne podržavaju kretanje po odlomcima nativno, kao što su to Notepad i Notepad++. (#13797)
* Izgovarana je prisutnost više anotacija.
`NVDA+d` sada prebacuje između izgovora sadržaja svake ciljne anotacije za izvore sa višestrukim ciljnim anotacijama.
Na primjer, kada tekst sadrži komentar i fusnotu. (#14507, #14480)
* Dodana je podrška za Tivomatic Caiku Albatross 46/80 brajične redke. (#13045)
* Novi globalni prečac: Čitaj odredište poveznice (`NVDA+k`).
Kada se pritisne jednom odredište linka koje se nalazi u objektu navigatora će biti izgovoreno i i prikazano na brajičnom redku.
Kada se pritisne dvaput, poveznica će biti prikazana u prozoru u svrhu detaljnijeg pregleda. (#14583)
* Nova nedodijeljena gesta (u kategoriji alati): je dodana prikaži odredište poveznice u prozoru.
Isto kao pritisak `NVDA+k` dvaput, ali može biti korisnije za korisnike brajice. (#14583)

### Izmjene

* nadograđen LibLouis brajični prevoditelj na  inačicu [3.24.0](https://github.com/liblouis/liblouis/releases/tag/v3.24.0). (#14436)
  * Drastično su osvježene Mađarska, univerzalna engleska, i kineska bopomofo brajična tablica.
  * Podržan je danski brajični standard, koji se promijenio u  2022 godini.
  * Nove brajične tablice za gruzijsku literarnu brajicu, Swahili (Kenija) i Chichewa (Malawi).
* Nadograđena biblioteka Sonic za ubrzanje govora na inačicu `1d70513`. (#14180)
* CLDR je nadograđen na inačicu 42.0. (#14273)
* eSpeak NG je nadograđen na inačicu 1.52-dev commit `f520fecb`. (#14281, #14675)
  * Ispravljeno čitanje velikih brojeva. (#14241)
* Java aplikacije sa kontrolama koje koriste status označenosti će izgovarati kada stavka nije označena umjesto obrnutog. (#14336)

### Ispravke grešaka

* Ispravke koje se primjenjuju u Windowsima 11:
  * NVDA će izgovarati rezultate pretrage prilikom otvaranja izbornika start. (#13841)
  * Na arhitekturi ARM, x64 aplikacije više nisu pogrešno identificirane kao ARM64 aplikacije. (#14403)
  * Stavkama izbornika povijesti međuspremnika poput "prikvači stavku" može se ponovno pristupiti. (#14508)
  * U Windowsima 11 22H2 i novijima, moguće je opet koristiti miš i interakciju dodirom kako bi se moglo koristiti područje obavijesti i dijaloški okvir "otvori sa". (#14538, #14539)
* Izgovaraju se prijedlozi prilikom upisivanja znaka @osvrta u Microsoft Excel komentarima. (#13764)
* U Google Chrome adresnoj traci, kontrole prijedloga (prebaci se na karticu, ukloni prijedlog itd) sada se izgovaraju kada su označene. (#13522)
* Prilikom dohvaćanja informacija o oblikovanju, boje su sada eksplicitno čitane u Wordpadu ili pregledniku zapisnika, umjesto  "podrazumjevana boja". (#13959)
* U  Firefoxu, aktiviranje opcije "Show options" na stranici za github probleme sada pouzdano radi. (#14269)
* Kontroke za odabir datuma u Outlooku 2016 / 365 dijaloškom okviru napredne pretrage sada se izgovaraju zajedno sa svojim vrijednostima. (#12726)
* ARIA switch kontrole sada se točnije izgovaraju kao preklopnici u Firefoxu, Chromeu i Edgeu, umjesto potvrdnih okvira. (#11310)
* NVDA će automatski izgovoriti status razvrstavanja na HTML zaglavlju stupca tablice kada se promjeni, prilikom pritiska unutrašnjeg gumba. (#10890)
* Naziv Orijentira i regije sada će se automatski čitati prilikom skananja u kontrolu ili fokusiranjem kontrole u modusu pregleda. (#13307)
* Kada je uključena opcija reproduciraj zvučni signal ili izgovori  'veliko' za velika slova, sa uključenim opisima znakova poslije kursora, NVDA više ne reproducira zvučni signal, niti ne izgovara  'veliko' dvaput. (#14239)
* Kontrole u tablicama u Java aplikacijama biti će pročitane točnije. (#14347)
* Neke postavke više neće biti neočekivano drugaćije kada se koristi više konfiguracijskih profila. (#14170)
  * Slijedeće postavke su ispravljene:
    * Uvlačenje redka u postavkama oblikovanja dokumenta.
    * Rubovi ćelija u postavkama oblikovanja dokumenta
    * Prikaz poruka u postavkama brajice
    * Povezivanje brajice u postavkama brajice
  * U nekim rijedkim slučajevima, ove postavke korištene u profilima mogu biti neočekivano izmijenjene kada se instalira iva inačica NVDA.
  * Molimo provjerite ove postavke u vašem profilu poslije nadogradnje na ovu inačicu.
* Emoji će se moći čitati na više jezika. (#14433)
* Prisutnost anotacija više ne nedostaje kada se prikazuju na brajičnom redku za neke elemente. (#13815)
* Ispravljena je pogreška u kojoj se izmjene ne spremaju ispravno prilikom izmjene "podrazumjevane" opcije i i vrijednosti "podrazumjevane" opcije. (#14133)
* Prilikom konfiguriranja NVDA uvijek će biti definirana barem jedna tipka kao NVDA modifikacijaka tipka. (#14527)
* Prilikom pristupanja NVDA izborniku preko popisa obavijesti, NVDA neće predložiti nadogradnju koja se očekuje kada isto nije dostupno. (#14523)
* Preostalo, proteklo i ukupno vrijeme sada se točno izgovara za audio datoteke čije trajanje prekoračuje jedan dan u foobar2000 programu. (#14127)
* U preglednicima poput Chromea i Firefoxa, upozorenja kao što su to preuzimanja biti će prikazana i na brajičnom redku. (#14562)
* Ispravljena je greška prilikom kretanja između prvog i zadnjeg stupca u tablici u Firefoxu (#14554)
* Kada je NVDA pokrenut sa parametrom naredbenog redka `--lang=Windows`, sada je ponovo moguće otvoriti prozor općenitih postavki.. (#14407)
* NVDA sada ponovno nastavlja čitanje u programu Kindle for PC poslije okretanja stranice. (#14390)

### Changes for Developers

Note: this is an Add-on API compatibility breaking release.
Add-ons will need to be re-tested and have their manifest updated.
Please refer to [the developer guide](https://www.nvaccess.org/files/nvda/documentation/developerGuide.html#API) for information on NVDA's API deprecation and removal process.

* System tests should now pass when run locally on non-English systems. (#13362)
* In Windows 11 on ARM, x64 apps are no longer identified as ARM64 applications. (#14403)
* It is no longer necessary to use `SearchField` and `SuggestionListItem` `UIA` `NVDAObjects` in new UI Automation scenarios, where automatic reporting of search suggestions, and where typing has been exposed via UI Automation with the `controllerFor` pattern.
This functionality is now available generically via `behaviours.EditableText` and the base `NVDAObject` respectively. (#14222)
* The UIA debug logging category when enabled now produces significantly more logging for UIA event handlers and utilities. (#14256)
* NVDAHelper build standards updated. (#13072)
  * Now uses the C++20 standard, was C++17.
  * Now uses the `/permissive-` compiler flag which disables permissive behaviors, and sets the `/Zc` compiler options for strict conformance.
* Some plugin objects (e.g. drivers and add-ons) now have a more informative description in the NVDA python console. (#14463)
* NVDA can now be fully compiled with Visual Studio 2022, no longer requiring the Visual Studio 2019 build tools. (#14326)
* More detailed logging for NVDA freezes to aid debugging. (#14309)
* The singleton `braille._BgThread` class has been replaced with `hwIo.ioThread.IoThread`. (#14130)
  * A single instance `hwIo.bgThread` (in NVDA core) of this class provides background i/o for thread safe braille display drivers.
  * This new class is not a singleton by design, add-on authors are encouraged to use their own instance when doing hardware i/o.
* The processor architecture for the computer can be queried from `winVersion.WinVersion.processorArchitecture attribute.` (#14439)
* New extension points have been added. (#14503)
  * `inputCore.decide_executeGesture`
  * `tones.decide_beep`
  * `nvwave.decide_playWaveFile`
  * `braille.pre_writeCells`
  * `braille.filter_displaySize`
  * `braille.decide_enabled`
  * `braille.displayChanged`
  * `braille.displaySizeChanged`
* It is possible to set useConfig to False on supported settings for a synthesizer driver. (#14601)

#### API Breaking Changes

These are breaking API changes.
Please open a GitHub issue if your Add-on has an issue with updating to the new API.

* The configuration specification has been altered, keys have been removed or modified:
  * In `[documentFormatting]` section (#14233):
    * `reportLineIndentation` stores an int value (0 to 3) instead of a boolean
    * `reportLineIndentationWithTones` has been removed.
    * `reportBorderStyle` and `reportBorderColor` have been removed and are replaced by `reportCellBorders`.
  * In `[braille]` section (#14233):
    * `noMessageTimeout` has been removed, replaced by a value for `showMessages`.
    * `messageTimeout` cannot take the value 0 anymore, replaced by a value for `showMessages`.
    * `autoTether` has been removed; `tetherTo` can now take the value "auto" instead.
  * In `[keyboard]` section  (#14528):
    * `useCapsLockAsNVDAModifierKey`, `useNumpadInsertAsNVDAModifierKey`, `useExtendedInsertAsNVDAModifierKey` have been removed.
    They are replaced by `NVDAModifierKeys`.
* The `NVDAHelper.RemoteLoader64` class has been removed with no replacement. (#14449)
* The following functions in `winAPI.sessionTracking` are removed with no replacement. (#14416, #14490)
  * `isWindowsLocked`
  * `handleSessionChange`
  * `unregister`
  * `register`
  * `isLockStateSuccessfullyTracked`
* It is no longer possible to enable/disable the braille handler by setting `braille.handler.enabled`.
To disable the braille handler programatically, register a handler to `braille.handler.decide_enabled`. (#14503)
* It is no longer possible to update the display size of the handler by setting `braille.handler.displaySize`.
To update the displaySize programatically, register a handler to `braille.handler.filter_displaySize`.
Refer to `brailleViewer` for an example on how to do this. (#14503)
* There have been changes to the usage of `addonHandler.Addon.loadModule`. (#14481)
  * `loadModule` now expects dot as a separator, rather than backslash.
  For example "lib.example" instead of "lib\example".
  * `loadModule` now raises an exception when a module can't be loaded or has errors, instead of silently returning `None` without giving information about the cause.
* The following symbols have been removed from `appModules.foobar2000` with no direct replacement. (#14570)
  * `statusBarTimes`
  * `parseIntervalToTimestamp`
  * `getOutputFormat`
  * `getParsingFormat`
* The following are no longer singletons - their get method has been removed.
Usage of `Example.get()` is now `Example()`. (#14248)
  * `UIAHandler.customAnnotations.CustomAnnotationTypesCommon`
  * `UIAHandler.customProps.CustomPropertiesCommon`
  * `NVDAObjects.UIA.excel.ExcelCustomProperties`
  * `NVDAObjects.UIA.excel.ExcelCustomAnnotationTypes`

#### Deprecations

* `NVDAObjects.UIA.winConsoleUIA.WinTerminalUIA` is deprecated and usage is discouraged. (#14047)
* `config.addConfigDirsToPythonPackagePath` has been moved.
Use `addonHandler.packaging.addDirsToPythonPackagePath` instead. (#14350)
* `braille.BrailleHandler.TETHER_*` are deprecated.
Use `configFlags.TetherTo.*.value` instead. (#14233)
* `utils.security.postSessionLockStateChanged` is deprecated.
Use `utils.security.post_sessionLockStateChanged` instead. (#14486)
* `NVDAObject.hasDetails`, `NVDAObject.detailsSummary`, `NVDAObject.detailsRole` has been deprecated.
Use `NVDAObject.annotations` instead. (#14507)
* `keyboardHandler.SUPPORTED_NVDA_MODIFIER_KEYS` is deprecated with no direct replacement.
Consider using the class `config.configFlags.NVDAKey` instead. (#14528)
* `gui.MainFrame.evaluateUpdatePendingUpdateMenuItemCommand` has been deprecated.
Use `gui.MainFrame.SysTrayIcon.evaluateUpdatePendingUpdateMenuItemCommand` instead. (#14523)

## 2022.4

U ovoj je inačici dodano nekoliko novih tipkovničkih prečaca, uključujući i prečace za čitanje cijele tablice.
Dodan je odjeljak "Vodič za brzo upoznavanje sa NVDA" u korisnički priručnik.
Ispravljene su također neke pogreške.

Espeak i LibLouis su nadograđeni.
Dodane su nove brajične tablice za jezike: kineski, švedski, Luganda i Kinyarwanda.

### Nove značajke

* Dodan je odlomak "Vodič za brzo upoznavanje" u vodič za korisnike. (#13934)
* Dodan je novi prečac za provjeru tipkovničkog prečaca trenutno fokusirane stavke. (#13960)
  * Za stolna računala: `shift+numerički2`.
  * za prijenosna računala: `NVDA+ctrl+shift+.`.
* Dodani su novi prečaci preglednog kursora za kretanje po stranici gdje to aplikacija podržava. (#14021)
  * Idi na prethodnu stranicu:
    * za stolna računala: `NVDA+pageUp`.
    * Za prijenosna računala: `NVDA+shift+pageUp`.
  * Idi na slijedeću stranicu:
    * Za stolna računala: `NVDA+pageDown`.
    * Za prijenosna računala: `NVDA+shift+pageDown`.
* Dodani su slijedeći prečaci za kretanje po tablicama. (#14070)
  * Čitaj sve u stupcu: `NVDA+control+alt+downArrow`
  * Čitaj sve u redku: `NVDA+control+alt+rightArrow`
  * Čitaj cijeli stupac: `NVDA+control+alt+upArrow`
  * Čitaj cijeli redak: `NVDA+control+alt+leftArrow`
* Microsoft Excel koji se koristi sa UI automation: NVDA sada obavještava o izlazku iz tablice u radnoj knjizi. (#14165)
* Čitanje zaglavlja tablica sada može biti konfigurirano odvojeno redci od stupaca. (#14075)

### Izmjene

* eSpeak NG je nadograđen  na inačicu 1.52-dev commit `735ecdb8`. (#14060, #14079, #14118, #14203)
  * Ispravljeno je čitanje latinice pri korištenju mandarinskog kineskog. (#12952, #13572, #14197)
* Nadograđen je LibLouis brajični prevoditelj na inačicu [3.23.0](https://github.com/liblouis/liblouis/releases/tag/v3.23.0). (#14112)
  * Dodane brajične tablice:
    * Kineska opća brajica (pojednostavljeni kineski znakovi)
    * Kinyarwanda puno pismo
    * Luganda puno pismo
    * švedsko osnovno pismo
    * švedsko puno pismo
    * švedski kratkopis
    * Kineski (Kina, mandarinski) Trenutačni brajični sustav (bez tonova) (#14138)
* NVDA sada uključuje arhitekturu operacijskog sustava kao dio sakupljane korisničke statistike. (#14019)

### Ispravke grešaka

* Prilikom nadogradnje NVDA uz pomoć Windows upravitelja paketa CLI (to jest winget), stabilna inačica se više ne tretira kao novija od bilo koje alpha inačice. (#12469)
* NVDA će sada ispravno čitati grupiranja u java aplikacijama. (#13962)
* Kursor sustava sada točno slijedi tijek "prečaca čitaj sve" u programima poput Bookworm-a, WordPada ili NVDA preglednika zapisnika. (#13420, #9179)
* U programima koji koriste UI automation, polovično odabrani potvrdni okviri sada će biti ispravno pročitani. (#13975)
* Unapređene su performanse i stabilnost u Microsoft Visual Studiu, Windows Terminalu, i drugim programima baziranim na UIA. (#11077, #11209)
  * Ove ispravke se primjenjuju na Windows 11 Sun Valley 2 (inačica 22H2) i novije.
  * Selektivna registracija za događaje UI automation i izmjene svojstava sada je uključena podrazumjevano.
* Čitanje teksta, brajični izlaz i neizgovaranje lozinki sada rade kako je to očekivano u ugrađenoj Windows terminal kontroli u Visual Studiu 2022. (#14194)
* NVDA je sada DPI svjestan pri korištenju više monitora.
Dodano je nekoliko ispravaka za korištenje DPI postavke više od 100% ili pri korištenju više monitora.
Još mogu postojati problemi sa inačicama operacijskog sustava Windows starijih od Windows 10 1809.
Kako bi ove ispravke radile, aplikacije s kojima NVDA ulazi u interakciju  također moraju biti DPI svjesne.
Imajte na umu da postoje problemi sa Chrome i Edge preglednicima. (#13254)
  * Okviri vizualnog označavanja sada će se postavljati ispravno u većini aplikacija. (#13370, #3875, #12070)
  * Interakcija putem dodirnika sada će biti točnija za većinu aplikacija. (#7083)
  * Praćenje miša će sada raditi ispravno za neke aplikacije. (#6722)
* Stanje orijentacije zaslona (okomito/vodoravno) sada se ispravno ignoriraju kada ne postoji izmjena (npr. promjene monitora). (#14035)
* NVDA će obavještavati o spuštanju stavaka na zaslonu kao što su to mjesta premještanja Windows 10 ploćica u izborniku start i virtualnim radnim površinama u Windows 11. (#12271, #14081)
* U naprednim postavkama, opcija opcija "reproduciraj zvuk za zapisane greške" sada se ispravno vraća na svoje podrazumjevane vrijednsti prilikom pritiska gumba "vrati na zadano". (#14149)
* NVDA sada može označavati tekst koristeći `NVDA+f10` tipkovnički prečac u java aplikacijama. (#14163)
* NVDA se više neće zaglavljivati u izborniku pri kretanju strelicama u тематским раѕговорима. (#14355)

### Changes for Developers

Please refer to [the developer guide](https://www.nvaccess.org/files/nvda/documentation/developerGuide.html#API) for information on NVDA's API deprecation and removal process.

* The [NVDA API Announcement mailing list](https://groups.google.com/a/nvaccess.org/g/nvda-api/about) was created. (#13999)
* NVDA no longer processes `textChange` events for most UI Automation applications due to their extreme negative performance impact. (#11002, #14067)

#### Deprecations

* `core.post_windowMessageReceipt` is deprecated, use `winAPI.messageWindow.pre_handleWindowMessage` instead.
* `winKernel.SYSTEM_POWER_STATUS` is deprecated and usage is discouraged, this has been moved to `winAPI._powerTracking.SystemPowerStatus`.
* `winUser.SM_*` constants are deprecated, use `winAPI.winUser.constants.SystemMetrics` instead.

## 2022.3.3

Ovo je mala inačica u kojoj su ispravljeni problemi iz inačica 2022.3.2, 2022.3.1 i 2022.3.
Ova verzija također ispravlja sigurnosnu ranjivost.

### Ispravke sigurnosti

* Onemogućuje pristup za neautentificirane korisnike (npr. NVDA Python konzoli).
([GHSA-fpwc-2gxx-j9v7](https://github.com/nvaccess/nvda/security/advisories/GHSA-fpwc-2gxx-j9v7))

### Ispravke grešaka

* Ispravljena je pogreška, u kojoj je bilo moguće pristupiti korisničkoj radnoj površini kada  se fokus nalazi na zaslonu zaključavanja. (#14416)
* Ispravljena je pogreška u kojoj prilikom smrzavanja NVDA isti se neće ispravno ponašatikao da je uređaj još uvijek zaključan. (#14416)
* Ispravljeni problemi s pristupačnošću s procesima "zaboravio sam pin" i Windows update/iskustvom instalacije. (#14368)
* Ispravljena je pogreška prilikom instalacije NVDA u nekim okruženjima, npr: Windows Server. (#14379)

### Changes for Developers

#### Deprecations

* `utils.security.isObjectAboveLockScreen(obj)` is deprecated, instead use `obj.isBelowLockScreen`. (#14416)
* The following functions in `winAPI.sessionTracking` are deprecated for removal in 2023.1. (#14416)
  * `isWindowsLocked`
  * `handleSessionChange`
  * `unregister`
  * `register`
  * `isLockStateSuccessfullyTracked`

## 2022.3.2

Ova inačica ispravlja regresije u inačici 2022.3.1 te ispravlja sigurnosnu ranjivost.

### Ispravke sigurnosti

* Onemogućen je mogući pristup na razini sustava za neautorizirane korisnike.
([GHSA-3jj9-295f-h69w](https://github.com/nvaccess/nvda/security/advisories/GHSA-3jj9-295f-h69w))

### Ispravke grešaka

* Ispravljena regresija iz inačice 2022.3.1 u kojoj su neke funkcionalnosti bile isključene na sigurnim zaslonima. (#14286)
* Ispravljena regresija iz inačice 2022.3.1 u kojoj su neke funkcije poslije prijave, bile nedostupne ako se NVDA pokrenuo sa zaslona zaključavanja. (#14301)

## 2022.3.1

Ovo je podverzija koja ispravlja nekoliko sigurnosnih propusta.
Molimo odgovorno izvještavajte o sigurnosnim problemima na adresu <info@nvaccess.org>.

### Sigurnosne ispravke

* Ispravljena ranjivost putem koje je bilo moguće podizanja prava sa korisnika na sustav.
([GHSA-q7c2-pgqm-vvw5](https://github.com/nvaccess/nvda/security/advisories/GHSA-q7c2-pgqm-vvw5))
* Ispravljen je sigurnosni propust koji je omogućavao pristpu python konzoli na zaključanom zaslonu preko rizične situacije NVDA pokretanja.
([GHSA-72mj-mqhj-qh4w](https://github.com/nvaccess/nvda/security/advisories/GHSA-72mj-mqhj-qh4w))
* Ispravljena pogreška u kojej je tekst pregledniak govora bio zadržavan prilikom zaključavanja operacijskog sustava Windows.
([GHSA-grvr-j2h8-3qm4](https://github.com/nvaccess/nvda/security/advisories/GHSA-grvr-j2h8-3qm4))

### Ispravke grešaka

* Neautorizirani korisnik biti će spriječen u namjeri spremanja postavki preglednika govora i brajice na zaslonu zaključavanja. ([GHSA-grvr-j2h8-3qm4](https://github.com/nvaccess/nvda/security/advisories/GHSA-grvr-j2h8-3qm4))

## 2022.3

Velikom dijelu ove inačice je doprinijela zajednica NVDA doprinositelja.
Ovo uključuje opise znakove poslije slovkanja i unapređenu podršku Windowsovog naredbenog redka.

Ova inačica uključuje nekoliko ispravaka grešaka.
Primjetno, posljednje inačice Adobe Acrobata/Readera neće se rušiti prilikom čitanja pdf dokumenta.

eSpeak je nadograđen, što znaći da su dodana tri nova jezika: bjeloruski, Luksenburški i Totontepec Mixe.

### Nove značajke

* U hostu Windows naredbenog redka kojeg koristi naredbeni redak, PowerShell i windows podsustav za sustava Linux u Windowsima 11 inačica 22H2 (Sun Valley 2) i novijim:
  * značajno su unapređene performanse i stabilnost. (#10964)
  * Prilikom pritiska prečaca `ctrl+f` za traženje teksta, pozicija preglednog kursora će se obnoviti kako bi pregledni kursor pratio pronađeni pojam. (#11172)
  * Izgovor upisanog teksta koji se ne pojavljuje na zaslonu poput lozinki je podrazumjevano isključen.
Može se uključiti u panelu NVDA Naprednih postavki. (#11554)
  * Tekst koji se pomaknuo izvan zaslona može se pregledavati bez potrebe za pomicanjem prozora naredbenog redka. (#12669)
  * Detaljnije informacije o oblikovanju teksta su dostupne. ([microsoft/terminal PR 10336](https://github.com/microsoft/terminal/pull/10336))
* Dodana je nova opcija za govor koja omogućuje čitanje opisa znaka poslije zadrške. (#13509)
* Dodana je nova brajična opcija koja regulira dali će pomicanje teksta na brajičnom redku naprijed ili nazad prekidati govor. (#2124)

### Izmjene

* eSpeak NG je nadograđen na inačicu 1.52-dev commit `9de65fcb`. (#13295)
  * Dodani jezici:
    * Bjeloruski
    * Luksenburški
    * Totontepec Mixe
* Prilikom korištenja UI Automation za pristup Microsoft Excel proračunskim tablicama, NVDA sada može izgovarati spojene ćelije. (#12843)
* Umjesto izgovora "sadrži detalje" uključen je tip detalja, gdje je to moguće, na primjer "sadrži komentar". (#13649)
* Veličina instalacije NVDA sada se prikazuje u odjeljku programi i funkcije operativnog sustava Windows. (#13909)

### Ispravke grešaka

* Adobe Acrobat / Reader 64 bitne inačice više se neće rušiti prilikom čitanja PDF dokumenata. (#12920)
  * Imajte na umu da je potrebna posljednja inačica Adobe/acrobat readera kako bi se izbjeglo rušenje.
* Mjere veličine fonta su od sada prevedene u  NVDA. (#13573)
* Ignorirani su događaji Java Access Bridge gdje se ne može pronaći uloga prozora za java aplikacije.
Ovo će unaprediti performanse za neke java aplikacije uključujući IntelliJ IDEA. (#13039)
* Izgovor označenih ćelija za LibreOffice Calc je točniji i ne rezultira rušenjem aplikacije Calc prilikom označavanja više ćelija. (#13232)
* Kada se pokreće od drugug korisnika, Microsoft Edge više nije nepristupačan. (#13032)
* Kada je dopojačanje brzine uključeno,, eSpeakova brzina ne pada u međuvrijednost između brzina 99% i 100%. (#13876)
* Ispravljena je greška koja je dozvoljavala dva otvorena dijaloška okvira ulaznih gesti.. (#13854)

### Changes for Developers

* Updated Comtypes to version 1.1.11. (#12953)
* In builds of Windows Console (`conhost.exe`) with an NVDA API level of 2 (`FORMATTED`) or greater, such as those included with Windows 11 version 22H2 (Sun Valley 2), UI Automation is now used by default. (#10964)
  * This can be overridden by changing the "Windows Console support" setting in NVDA's advanced settings panel.
  * To find your Windows Console's NVDA API level, set "Windows Console support" to "UIA when available", then check the NVDA+F1 log opened from a running Windows Console instance.
* The Chromium virtual buffer is now loaded even when the document object has the MSAA `STATE_SYSTEM_BUSY` exposed via IA2. (#13306)
* A config spec type `featureFlag` has been created for use with experimental features in NVDA. See `devDocs/featureFlag.md` for more information. (#13859)

#### Deprecations

There are no deprecations proposed in 2022.3.

## 2022.2.4

Ovo je inačica koja ispravlja sigurnosnu ranjivost.

### Ispravke grešaka

* Ispravljena ranjivost putem koje je bilo moguće otvoriti Python konzolu preko pregledniak zapisnika na sigurnom zaslonu.
([GHSA-585m-rpvv-93qg](https://github.com/nvaccess/nvda/security/advisories/GHSA-585m-rpvv-93qg))

## 2022.2.3

Ovo je verzija koja je izdana u svrhu ispravljanja nekompatibilnosti API sučelja do koje je došlo u inačici 2022.2.1.

### Ispravke grešaka

* Ispravljena greška zbog koje NVDA nije izgovarao "sigurni zaslon" prilikom ulaza u sigurnu radnu površinu.
Ovo je prouzrokovalo nemogućnost NVDA remote da prepoznaje sigurne radne površine. (#14094)

## 2022.2.2

Ovo je verzija sa zakrpom koja ispravlja grešku iz verzije  2022.2.1 sa ulaznim gestama.

### Ispravke grešaka

* Ispravljena greška sa ulaznim gestama koje nisu ispravno radile. (#14065)

## 2022.2.1

Ovo je mala verzija koja ispravlja sigurnosni propust.
Molimo odgovorno prijavljujte sigurnosne propuste na adresu <info@nvaccess.org>.

### Ispravke sigurnosnih propusta

* Ispravljena ranjivost  u kojoj je bilo moguće pokrenuti python konzolu sa zaključanog zaslona. (GHSA-rmq3-vvhq-gp32)
* Ispravljena ranjivost pomoću koje je bilo moguće izaći iz zaključanog zaslona koristeći objektnu navigaciju. (GHSA-rmq3-vvhq-gp32)

### Changes for Developers

#### Deprecations

These deprecations are currently not scheduled for removal.
The deprecated aliases will remain until further notice.
Please test the new API and provide feedback.
For add-on authors, please open a GitHub issue if these changes stop the API from meeting your needs.

* `appModules.lockapp.LockAppObject` should be replaced with `NVDAObjects.lockscreen.LockScreenObject`. (GHSA-rmq3-vvhq-gp32)
* `appModules.lockapp.AppModule.SAFE_SCRIPTS` should be replaced with `utils.security.getSafeScripts()`. (GHSA-rmq3-vvhq-gp32)

## 2022.2

Ova inačica uključuje puno ispravaka grešaka.
Prije svega, značajno je unapređena suradnja sa aplikacijama baziranim na java sučelju, brajičnim redcima i značajkama operacijskog sustava Windows.

Uvedeni su novi prečaci za kretanje po tablicama.
Unicode CLDR je nadograđen.
LibLouis je nadograđen, sa novom dodanom njemačkom brajičnom tablicom.

### Nove značajke

* Podrška za interakciju s Microsoft Loop komponentama u proizvodima Microsoft Officea. (#13617)
* Dodane su nove naredbe za navigaciju u tablicama. (#957)
 * `control+alt+home/end` za skakanje na prvi/zadnji stupac.
 * `control+alt+pageUp/pageDown` za skakanje na prvi/zadnji redak.
* Dodana je nedodijeljena skripta za mijenjanje jezika i dijalekta. (#10253)

### Izmjene

* NSIS je nadograđen na verziju 3.08. (#9134)
* CLDR je nadograđen na verziju 41.0. (#13582)
* Nadograđen LibLouis brajični prevoditelj na verziju [3.22.0](https://github.com/liblouis/liblouis/releases/tag/v3.22.0). (#13775)
  * Nova brajična tablica: Njemački kratkopis (eksperimentalan)
* • Dodana je nova uloga za kontrole "indikatora zauzetosti". (#10644)
* NVDA sada najavljuje kad se NVDA radnja ne može izvesti. (#13500)
  * Ovo uključuje sljedeće:
    * kad se koristi NVDA Windows Store verzija.
    * kad se računalo nalazi na sigurnom zaslonu.
    * kad se čeka na odgovor u modalnom dijaloškom okviru. - - -

### Ispravke grešaka

* Ispravke za aplikacije napisane u java programskom jeziku:
  * NVDAće sada izgovarati status samo za čitanje. (#13692)
  * NVDA će sada ispravno izgovarati stanje uključenosti/isključenosti. (#10993)
  * NVDA će sada izgovarati prečace funkcijskih tipki. (#13643)
  * NVDA sada može reproducirati zvučne signale ili izgovarati trake napredka. (#13594)
  * NVDA više neće neispravno uklanjati tekst sa widgeta kada se isti prikazuje korisniku. (#13102)
  * NVDA će sada izgovarati stanje preklopnih gumbi. (#9728)
  * NVDA će sada prepoznavati prozore u java aplikacijama sa više prozora. (#9184)
  * NVDA će sada izgovarati informacije o poziciji za kontrole kartica. (#13744)
* Ispravke brajice:
  * Ispravljen brajični izlaz u mozillinim kontrolama obogaćenog teksta, kao što je to skiciranje poruka u Mozilla thunderbirdu. (#12542)
  * Kada je brajica povezana automatski a miš se kreće s uključenim praćenjem miša,
   brajični će redak biti obnovljen. (#11519)
  * Sada je moguće pomicati brajični redak po sadržaju poslije korištenja prečaca pregleda teksta. (#8682)
* • NVDA instalacijski program se sada može pokrenuti iz direktorija s posebnim znakovima. (#13270)
* U Firefoxu, NVDA sada uspijeva prijaviti stavke na web stranicama kad su atributi aria-rowindex, aria-colindex, aria-rowcount ili aria-colcount nevažeći. (#13405)
* Kursor više ne mijenja redak ili stupac kad se koristi tablična navigacija za kretanje kroz spojene ćelije. (#7278)
* Prilikom čitanja neinteraktivnih PDF-ova u Adobe Readeru, sada se izvještavaju vrsta i stanje polja obrasca (kao što su potvrdni okviri i izborni gumbi). (#13285)
* "Resetiraj konfiguraciju na tvorničke vrijednosti" sada je dostupno u NVDA izborniku tijekom sigurnog načina rada. (#13547)
* Sve zaključane tipke miša otključat će se kad se NVDA čitač zatvori. Prije je tipka miša ostala zaključana. (#13410)
* Visual Studio sada izvještava o brojevima redaka. (#13604)
  * Da bi izvještavanje o brojevima redaka funkcioniralo, prikazivanje brojeva redaka mora biti aktivirano u Visual Studiju i NVDA-u.
* Visual Studio sada ispravno izvještava o uvlačenju retka. (#13574)
* NVDA će još jednom najaviti detalje rezultata pretraživanja izbornika Start u nedavnim izdanjima sustava Windows 10 i 11. (#13544)
* U kalkulatoru u  Windowsima 10 u inačici 10.1908 i novijim,
NVDA će izgovarati rezultate za više pritisnutih naredbi, poput naredaba iz znanstvenog načina. (#13383)
* U Windowsima 11, sada je opet moguće kretanje i interakcija s elementima korisničkog sučelja ,
poput trake zadataka i pregleda zadataka uz pomoć miša i dodirnika. (#13506)
* NVDA će sada čitati traku stanja u Windows 11 bloku za pisanje. (#13688)
* Označavanje objekta navigatora pokazuje se trenutno poslije aktivacije značajke. (#13641)
* Ispravljeno čitanje jednostupčastih popisa. (#13659, #13735)
* Ispravljeno automatsko prebacivanje jezika prilikom korištenja Espeaka za engleski i francuski vraćajući se na britanski engleski i francuski (Francuska). (#13727)
* Ispravljeno OneCore automatsko prepoznavanje jezika prilikom pokušaja prebacivanja na jezik koji je bio prije instaliran. (#13732)

### Changes for Developers

* Compiling NVDA dependencies with Visual Studio 2022 (17.0) is now supported.
For development and release builds, Visual Studio 2019 is still used. (#13033)
* When retrieving the count of selected children via accSelection,
the case where a negative child ID or an IDispatch is returned by `IAccessible::get_accSelection` is now handled properly. (#13277)
* New convenience functions `registerExecutableWithAppModule` and `unregisterExecutable` were added to the `appModuleHandler` module.
They can be used to use a single App Module with multiple executables. (#13366)

#### Deprecations

These are proposed API breaking changes.
The deprecated part of the API will continue to be available until the specified release.
If no release is specified, the plan for removal has not been determined.
Note, the roadmap for removals is 'best effort' and may be subject to change.
Please test the new API and provide feedback.
For add-on authors, please open a GitHub issue if these changes stop the API from meeting your needs.

* `appModuleHandler.NVDAProcessID` is deprecated, use `globalVars.appPid` instead. (#13646)
* `gui.quit` is deprecated, use `wx.CallAfter(mainFrame.onExitCommand, None)` instead. (#13498)
  -
* Some alias appModules are marked as deprecated.
Code which imports from one of them, should instead import from the replacement module.  (#13366)

| Removed module name |Replacement module|
|---|---|
|azuredatastudio |code|
|azuredatastudio-insiders |code|
|calculatorapp |calculator|
|code - insiders |code|
|commsapps |hxmail|
|dbeaver |eclipse|
|digitaleditionspreview |digitaleditions|
|esybraille |esysuite|
|hxoutlook |hxmail|
|miranda64 |miranda32|
|mpc-hc |mplayerc|
|mpc-hc64 |mplayerc|
|notepad++ |notepadPlusPlus|
|searchapp |searchui|
|searchhost |searchui|
|springtoolsuite4 |eclipse|
|sts |eclipse|
|teamtalk3 |teamtalk4classic|
|textinputhost |windowsinternal_composableshell_experiences_textinput_inputapp|
|totalcmd64 |totalcmd|
|win32calc |calc|
|winmail |msimn|
|zend-eclipse-php |eclipse|
|zendstudio |eclipse|

## 2022.1

Ova verzija uključuje veća poboljšanja za UIA podršku u paketu MS Office.
Za Microsoft Office 16.0.15000 i novije verzije na Windowsu 11, NVDA će podrazumevano koristiti UI Automation za pristup dokumentima programa Microsoft Word.
Ovo pruža značajno poboljšanje brzine u odnosu na stariji način pristupa.

Postoje poboljšanja za upravljačke programe za brajične redke kao što su Seika brajična bilježnica, Papenmeier i  HID brajični standard. 
Takođe su uključene razne ispravke grešaka za Windows 11, u aplikacijama kao što su Kalkulator, naredbeni redak, Terminal, Mail i Emoji panel.

Ažurirani su eSpeak-NG  i LibLouis, tako da su dodane nove Japanske, Nemačke i Katalonske brajične tablice.

Napomena:

 * Ova verzija čini postojeće dodatke nekompatibilnim.

### nove značajke

* Podrška za prijavljivanje napomena u programu MS Excel uz  UI Automation omogućen na Windowsu 11. (#12861)
* U novijim verzijama programa Microsoft Word uz  UI Automation na  Windowsu 11, postojanje markera, nacrta komentara kao i rješenih komentara se sada prijavljuje izgovorom kao i na brajevom redu. (#12861)
* Novi parametar naredbenog redka `--lang` dozvoljava mijenjanje podešenog NVDA jezika. (#10044)
* NVDA će sada upozoriti o parametrima komandne linije koji su nepoznati i a dodaci ih ne koriste. (#12795)
* Kada se pristupa programu Microsoft Word uz UI Automation, NVDA će sada koristiti mathPlayer za kretanje  po matematičkim zadacima i čitanje. (#12946)
  * Kako bi ovo  radilo, morate koristiti Microsoft Word 365/2016 verziju 14326 ili novije. 
    * MathType zadaci se takođe moraju ručno pretvoriti u Office Math izborom svakog od njih, otvaranjem kontekstnog menija, izborom stavke opcije jednadžba, pretvori u  Office Math.
-
* Prijavljivanje kada objekat  "ima detalje " kao i odgovarajuća komanda za prijavljivanje odnosa detalja sada se mogu koristiti u režimu fokusiranja. (#13106)
* Seika brajična bilježnica se sada može automatski prepoznati putem USB i Bluetooth veze. (#13191, #13142)
  * Ovo utiče na sliedeće uređaje: MiniSeika (16, 24 znakova), V6, i V6Pro (40 znakova)
  * Ručno biranje bluetooth COM porta je sada takođe podržano.
* Dodana komanda za uključivanje i isključivanje preglednika brajičnog redka; nema podrazumijevane pridružene prečice. (#13258)
* Dodate komande za uključivanje ili isključivanje više modifikatora u isto vrieme  na brajičnom redku (#13152)
* Dijalog za govorne rečnike sada sadrži gumb "Ukloni sve" koji vam pomaže da očistite cijeli riječnik. (#11802)
* Dodana podrška za Windows 11 kalkulator. (#13212)
* U programu Microsoft Word uz UI Automation omogućen na Windowsu 11, brojevi redaka i sekcija se sada mogu prijaviti. (#13283, #13515)
* Za  Microsoft Office 16.0.15000 i novije na Windowsu 11, NVDA će podrazumijevano koristiti UI Automation za pristup Microsoft Word dokumentima, što pruža značajna poboljšanja u brzini u odnosu na stariji način pristupa. (#13437)
 * Ovo uključuje dokumente u samom programu Microsoft Word, kao i čitanje i pisanje poruka u programu Microsoft Outlook. 

### izmijene

* Espeak-ng je ažuriran na 1.51-dev commit `7e5457f91e10`. (#12950)
* Ažuriran liblouis brajični prevoditelj na [3.21.0](https://github.com/liblouis/liblouis/releases/tag/v3.21.0). (#13141, #13438)
  * Dodana nova brajična tablica: Japanski (Kantenji) literarna brajica.
  * Dodata nova Njemačka šestotočkasta kompjuterska brajična tablica.
  * Dodana brajična tablica Katalonsko puno pismo. (#13408)
* NVDA će izgovarati označavanje i spajanje ćelija u programu LibreOffice Calc 7.3 i novijim. (#9310, #6897)
* Ažuriran Unicode Common Locale Data Repository (CLDR) na 40.0. (#12999)
* ``NVDA+numerička tipka za brisanje `` podrazumjevano prijavljuje lokaciju kursora ili fokusiranog objekta. (#13060)
* `NVDA+šift+numerička tipka za brisanje` prijavljuje lokaciju preglednog kursora. (#13060)
* Dodani podrazumjevani prečaci za uključivanje i isključivanje modifikatorskih tastera na Freedom Scientific brajevim redovima (#13152)
* "Osnovna linija " se više neće izgovarati kada se koristi prečac za prijavljivanje oblikovanja  (`NVDA+f`). (#11815)
* Prijavljivanje dugog opisa više nema postavljenu podrazumjevan prečac. (#13380)
* Prijavljivanje kratkog opisa detalja sada ima podrazumjevan prečac (`NVDA+d`). (#13380)
* NVDA mora ponovo biti pokrenut nakon što se instalira MathPlayer. (#13486)

### Ispravke grešaka

* Okno upravljača privremene memorije više neće neispravno biti fokusirano kada se otvaraju određeni Office programi. (#12736)
* Na sustavima na kojima je korisnik odredio da zamijeni primarni gumb na mišu tako da desni klik aktivira stavke, NVDA više neće otvarati kontekstni meni umesto da aktivira stavku, u aplikacijama kao što su Web pretraživači. (#12642)
* Kada se pregledni kursor pomjera od dna tekstualnih kontrola, kao što su u programu Microsoft Word uz UI Automation, "dno" se ispravno izgovara u više situacija. (#12808)
* NVDA može da pruži ime aplikacije i verziju za binarne datoteke koje se nalaze u system32 kada je pokrenut na 64-bitnoj verziji Windowsa. (#12943)
* Poboljšana dosliednost u čitanju u terminal programima. (#12974)
  * Napomena da će se u određenim situacijama, kada ubacujete ili brišete znakove u sredini redka, znakovi nakon kursora  možda ponovo pročitati.
* MS word uz UIA: Brza navigacija kroz naslove se neće više zaglavljivati na posljednjem naslovu, niti će taj naslov biti prikazan dva puta u listi elemenata. (#9540)
* Na Windowsu 8 i novijim, statusna traka istraživača datoteka se sada može pročitati korištenjem standardnih prečica NVDA+end (desktop) / NVDA+šift+end (laptop). (#12845)
* Dolazne poruke u čavrljanjima aplikacije Skype za biznis se ponovo prijavljuju. (#9295)
* NVDA ponovo može stišavati pozadinske zvukove kada  se koristi SAPI5 sintetizator na Windowsu 11. (#12913)
* U Kalkulatoru Windowsa 10, NVDA će izgovarati oznake za istoriju i stavke popisa memorije. (#11858)
* Prečaci kao što su pomeranje brajevog reda i prebacivanje ponovo rade na HID brajevim uređajima. (#13228)
* Windows 11 Mail: Nakon prebacivanja fokusa između aplikacija, dok se čita duža EMail poruka, NVDA se više neće zaglavljivati na jednom redu poruke. (#13050)
* HID brajevi uređaji: Vezane komande  (na primer  `razmak+točkica4`) se mogu uspešno izvršiti sa brajevog reda. (#13326)
* Ispravljena greška koja je dozvoljavala da se otvori više dijaloga sa postavkama u isto vrieme. (#12818)
* Ispravljen problem koji je izazvao da određeni Focus Blue brajični redci prestanu raditi nakon što probudite računalo iz stanja spavanja. (#9830)
* "Osnovna linija " se više ne izgovara bespotrebno kada je opcija "prijavi indekse i eksponente" omogućena. (#11078)
* U Windowsu 11, NVDA više neće sprečavati navigaciju kroz Emoji panel kada se bira emoji. (#13104)
* Spriječena greška koja izaziva dvostruko prijavljivanje kada se koristi Windows konzola i terminal. (#13261)
* Ispravljeno nekoliko slučajeva u kojima stavke popisa nisu mogle biti prijavljene u 64 bitnim aplikacijama, kao što je REAPER. (#8175)
* U upravljaču preuzimanja programa Microsoft Edge, NVDA će se automatski prebaciti u režim fokusiranja kada stavka liste sa najnovijim preuzimanjem postane fokusirana. (#13221)
* NVDA više neće izazvati rušenje 64-bitnih verzija programa Notepad++ 8.3 i novijih. (#13311)
* Adobe Reader se više ne ruši pri pokretanju ako je njegov zaštićen režim omogućen. (#11568)
* Ispravljena greška koja je izazivala rušenje programa NVDA kada se izabere  Papenmeier upravljački program. (#13348)
* Microsoft word uz UIA: Broj stranice i druge informacije o formatiranju se više ne izgovaraju bespotrebno kada se prebacite iz prazne ćelije tabele u ćeliju sa sadržajem, ili sa kraja dokumenta na postojeći sadržaj. (#13458, #13459)
* NVDA više neće imati problema sa prijavljivanjem naslova stranice i početka automatskog čitanja, kada se stranica učita u programu Google chrome 100. (#13571)
* NVDA se više ne ruši kada se podešavanja vrate na tvorničke vrijednosti uz uključen izgovor komandnih tastera. (#13634)

### Changes for Developers

* Note: this is a Add-on API compatibility breaking release. Add-ons will need to be re-tested and have their manifest updated.
* Although NVDA still requires Visual Studio 2019, Builds should no longer fail if a newer version of Visual Studio (E.g. 2022) is installed along side 2019. (#13033, #13387)
* Updated SCons to version 4.3.0. (#13033)
* Updated py2exe to version 0.11.1.0. (#13510)
* `NVDAObjects.UIA.winConsoleUIA.WinConsoleUIA.isImprovedTextRangeAvailable` has been removed. Use `apiLevel` instead. (#12955, #12660)
* `TVItemStruct` has been removed from `sysTreeView32`. (#12935)
* `MessageItem` has been removed from the Outlook appModule. (#12935)
* `audioDucking.AUDIODUCKINGMODE_*` constants are now a `DisplayStringIntEnum`. (#12926)
  * usages should be replaced with `AudioDuckingMode.*`
  * usages of `audioDucking.audioDuckingModes` should be replaced with `AudioDuckingMode.*.displayString`
* `audioDucking.ANRUS_ducking_*` constants usages should be replaced with `ANRUSDucking.*`. (#12926)
* `synthDrivers.sapi5` changes (#12927):
  * `SPAS_*` usages should be replaced with `SPAudioState.*`
  * `constants.SVSF*` usages should be replaced with `SpeechVoiceSpeakFlags.*`
    * Note: `SVSFlagsAsync` should be replaced with `SpeechVoiceSpeakFlags.Async` not `SpeechVoiceSpeakFlags.lagsAsync`
  * `constants.SVE*` usages should be replaced with `SpeechVoiceEvents.*`
* The `soffice` appModule has the following classes and functions removed `JAB_OOTableCell`, `JAB_OOTable`, `gridCoordStringToNumbers`. (#12849)
* `core.CallCancelled` is now `exceptions.CallCancelled`. (#12940)
* All constants starting with RPC from `core` and `logHandler` are moved into `RPCConstants.RPC` enum. (#12940)
* It is recommended that `mouseHandler.doPrimaryClick` and `mouseHandler.doSecondaryClick` functions should be used to click the mouse to perform a logical action such as activating (primary) or secondary (show context menu),
rather than using `executeMouseEvent` and specifying the left or right mouse button specifically.
This ensures code will honor the Windows user setting for swapping the primary mouse button. (#12642)
* `config.getSystemConfigPath` has been removed - there is no replacement. (#12943)
* `shlobj.SHGetFolderPath` has been removed - please use `shlobj.SHGetKnownFolderPath` instead. (#12943)
* `shlobj` constants have been removed. A new enum has been created, `shlobj.FolderId` for usage with `SHGetKnownFolderPath`. (#12943)
* `diffHandler.get_dmp_algo` and `diffHandler.get_difflib_algo` have been replaced with `diffHandler.prefer_dmp` and `diffHandler.prefer_difflib` respectively. (#12974)
* `languageHandler.curLang` has been removed - to get the current NVDA language use `languageHandler.getLanguage()`. (#13082)
* A `getStatusBarText` method can be implemented on an appModule to customize the way NVDA fetches the text from the status bar. (#12845)
* `globalVars.appArgsExtra` has been removed. (#13087)
  * If your add-on need to process additional command line arguments see the documentation of `addonHandler.isCLIParamKnown` and the developer guide for details.
* The UIA handler module and other UIA support modules are now part of a UIAHandler package. (#10916)
  * `UIAUtils` is now `UIAHandler.utils`
  * `UIABrowseMode` is now `UIAHandler.browseMode`
  * `_UIAConstants` is now `UIAHandler.constants`
  * `_UIACustomProps` is now `UIAHandler.customProps`
  * `_UIACustomAnnotations` is now `UIAHandler.customAnnotations`
* The `IAccessibleHandler` `IA2_RELATION_*` constants have been replaced with the `IAccessibleHandler.RelationType` enum. (#13096)
  * Removed `IA2_RELATION_FLOWS_FROM`
  * Removed `IA2_RELATION_FLOWS_TO`
  * Removed `IA2_RELATION_CONTAINING_DOCUMENT`
* `LOCALE_SLANGUAGE`, `LOCALE_SLIST` and `LOCALE_SLANGDISPLAYNAME` are removed from `languageHandler` - use members of `languageHandler.LOCALE` instead. (#12753)
* Switched from Minhook to Microsoft Detours as a hooking library for NVDA. Hooking with this library is mainly used to aid the display model. (#12964)
* `winVersion.WIN10_RELEASE_NAME_TO_BUILDS` is removed. (#13211)
* SCons now warns to build with a number of jobs that is equal to the number of logical processors in the system.
This can dramatically decrease build times on multi core systems. (#13226, #13371)
* `characterProcessing.SYMLVL_*` constants are removed - please use `characterProcessing.SymbolLevel.*` instead. (#13248)
* Functions `loadState` and `saveState` are removed from addonHandler - please use `addonHandler.state.load` and `addonHandler.state.save` instead. (#13245)
* Moved the UWP/OneCore interaction layer of NVDAHelper [from C++/CX to C++/Winrt](https://docs.microsoft.com/en-us/windows/uwp/cpp-and-winrt-apis/move-to-winrt-from-cx). (#10662)
* It is now mandatory to subclass `DictionaryDialog` to use it. (#13268)
* `config.RUN_REGKEY`, `config.NVDA_REGKEY` are deprecated, please use `config.RegistryKey.RUN`, `config.RegistryKey.NVDA` instead. These will be removed in 2023. (#13242)
* `easeOfAccess.ROOT_KEY`, `easeOfAccess.APP_KEY_PATH` are deprecated, please use`easeOfAccess.RegistryKey.ROOT`, `easeOfAccess.RegistryKey.APP` instead. These will be removed in 2023. (#13242)
* `easeOfAccess.APP_KEY_NAME` has been deprecated, to be removed in 2023. (#13242)
* `DictionaryDialog` and `DictionaryEntryDialog` are moved from `gui.settingsDialogs` to `gui.speechDict`. (#13294)
* IAccessible2 relations are now shown in developer info for IAccessible2 objects. (#13315)
* `languageHandler.windowsPrimaryLCIDsToLocaleNames` has been removed, instead use `languageHandler.windowsLCIDToLocaleName` or `winKernel.LCIDToLocaleName`. (#13342)
* `UIAAutomationId` property for UIA objects should be preferred over `cachedAutomationId`. (#13125, #11447)
  * `cachedAutomationId` can be used if obtained directly from the element.
* `NVDAObjects.window.scintilla.CharacterRangeStruct` has moved to `NVDAObjects.window.scintilla.Scintilla.CharacterRangeStruct`. (#13364)
* Boolean `gui.isInMessageBox` is removed, please use the function `gui.message.isModalMessageBoxActive` instead. (#12984, #13376)
* `controlTypes` has been split up into various submodules. (#12510, #13588)
  * `ROLE_*` and `STATE_*` have been replaced with `Role.*` and `State.*`.
  * Although still available, the following should be considered deprecated:
    * `ROLE_*` and `STATE_*`, use `Role.*` and `State.*` instead.
    * `roleLabels`, `stateLabels` and `negativeStateLabels`, usages like `roleLabels[ROLE_*]` should be replaced with their equivalent `Role.*.displayString` or `State.*.negativeDisplayString`.
    * `processPositiveStates` and `processNegativeStates` should use `processAndLabelStates` instead.
* Excel cell state constants (`NVSTATE_*`) are now values in the `NvCellState` enum, mirrored in the `NvCellState` enum in `NVDAObjects/window/excel.py` and mapped to `controlTypes.State` via _nvCellStatesToStates. (#13465)
* `EXCEL_CELLINFO` struct member `state` is now `nvCellStates`.
* `mathPres.ensureInit` has been removed, MathPlayer is now initialized when NVDA starts. (#13486)

## 2021.3.5

Ovo je manje ažuriranje kako bi se ispravio sigurnosni problem.
Molimo odgovorno prijavite sigurnosne probleme na adresu <info@nvaccess.org>.

### Ispravci sigurnosti

* Ispravljena sigurnosna preporuka `GHSA-xc5m-v23f-pgr7`.
  * Dijalog izgovora znakova interpunkcije i simbola je sada onemogućen u sigurnom načinu rada.

## 2021.3.4

Ovo je manje ažuriranje kako bi se ispravilo nekoliko prijavljenih sigurnosnih problema.
Molimo odgovorno prijavite sigurnosne probleme na adresu  <info@nvaccess.org>.

### Sigurnosni ispravci

* Ispravljena sigurnosna preporuka `GHSA-354r-wr4v-cx28`. (#13488)
  * Uklonjena mogućnost da se NVDA pokrene uz omogućene zapisnike za otklanjanje grešaka kada je NVDA pokrenut u bezbednom načinu rada.
  * Uklonjena mogućnost da se NVDA ažurira kada je pokrenut u sigurnom načinu rada.
* Ispravljena sigurnosna preporuka `GHSA-wg65-7r23-h6p9`. (#13489)
  * Uklonjena mogućnost otvaranja dijaloga ulaznih gesti u bezbednom načinu rada.
  * Uklonjena mogućnost otvaranja podrazumijevanog, privremenog i govornog rječnika u sigurnosnom načinu rada.
* Ispravljena sigurnosna preporuka `GHSA-mvc8-5rv9-w3hx`. (#13487)
  -  wx GUI inspection alat je sada onemogućena u sigurnom načinu rada.
  -

## 2021.3.3

Ova verzija je identična verziji 2021.3.2.
Došlo je do greške u verziji NVDA 2021.3.2 pa se ona identificirala kao 2021.3.1.
Ova verzija se ispravno identificira kao 2021.3.3.

## 2021.3.2

Ovo je manje ažuriranje kako bi se ispravilo nekoliko prijavljenih sigurnosnih problema.
Molimo odgovorno prijavite sigurnosne probleme na adresu  <info@nvaccess.org>.

### Ispravke grešaka

* Sigurnosna ispravka: Sprečavanje objektne navigacije van zaključanog ekrana na Windowsu 10 i Windowsu 11. (#13328)
* Sigurnosna ispravka: Ekran upravljača dodacima je sada onemogućen na sigurnim zaslonima. (#13059)
* Sigurnosna ispravka: NVDA kontekstna pomoć više nije dostupna na sigurnim zaslonima. (#13353)

## 2021.3.1

Ovo je manje ažuriranje kako bi se ispravilo nekoliko grešaka u verziji 2021.3.

### Izmjene

* Novi HID brajični protokol više nije izabran u situacijama kada postoji drugi upravljački program za brajični redak koji se može koristiti. (#13153)
* Novi HID brajični protokol se može onemogućiti korištenjem opcije u panelu naprednih postavki. (#13180)

### Ispravke grešaka

* Orjentiri će ponovo imati skraćenice na brajičnom redku. #13158
* Ispravljjena nestabilnost u automatskom prepoznavanju brajičnih redaka Humanware Brailliant i  APH Mantis Q40 kada se koriste putem  Bluetooth veze. (#13153)

## 2021.3

Ova inačica uvodi podršku za novu HID specifikaciju za brajične retke.
Ova specifikacija ima za cilj standardizaciju podrške za brajične retke bez potrebe za pojedinačnim upravljačkim programima.
Nadograđeni su eSpeak-NG i LibLouis, uključujući nove tablice za ruski i Tshivenda jezike.
Zvuci pogrešaka mogu biti omogućeni u stabilnim inačicama NVDA koristeći novu opciju u naprednim postavkama.
Prečac čitaj sve u Wordu sada prebacuje kako bi trenutna pozicija bila vidljiva.
Učinjeno je mnoštvo poboljšanja pri korištenju Office paketa sa UIA.
Jedna ispravka za UIA je ta da Outlook ignorira više tablica izgleda u porukama.

Važna upozorenja:

Zbog nadogradnje našeg sigurnosnog certifikata, mali broj korisnika dobijaju pogrešku kada NVDA 2021.2 provjerava nadogradnje.
NVDA sada pita operacijski sustav Windows treba li nadograditi sigurnosni certifikat, što znači da će takve greške u budućnosti biti izbjegnute.
Korisnici koji su se susreli sa tom greškom će trebati ručno preuzeti ovu nadogradnju.

### Nove značajke

* Dodan prečac za uključivanje ili isključivanje izgovoraa stila granice rubova. (#10408)
* Podrška nove HID specifikacije za brajične redke koja ima za cilj standardizaciju podrške brajičnih redaka. (#12523)
 * NVDA će automatski prepoznavati uređaje koji podržavaju ovu specifikaciju.
 * Za tehničke detalje o NVDA implementaciji ove specifikacije, pogledajte https://github.com/nvaccess/nvda/blob/master/devDocs/hidBrailleTechnicalNotes.md
* Dodana podrška za  VisioBraille Vario 4 brajični redak. (#12607)
* Obavijesti o pogreškama mogu biti uključene (napredne postavkew) kada se koristi bilo koja inačica NVDA. (#12672)
* Pri korištenju Windowsa 10 i novijih inačica, NVDA će izgovarati broj sugestija prilikom upisivanja upita pretrage u programima poput postavki i Microsoft Storea. (#7330, #12758, #12790)
* Kretanje po tablicama je sada podržana u mrežastim kontrolama koje su stvorene koristeći Out-GridView cmdlet u PowerShellu. (#12928)

### Izmjene

* Espeak-ng je nadograđen na inačicu 1.51-dev commit `74068b91bcd578bd7030a7a6cde2085114b79b44`. (#12665)
* NVDA  će podrazumjevano koristiti eSpeak'ng ako ne postoji niti jedan OneCore glas koji podržava podrazumijevani jezik NVDA. (#10451)
* Ako OneCore glasovi  se ne učitavaju, koristit će se Espeak kao govorna jedinica. (#11544)
* Prilikom čitanja statusne trake koristeći `NVDA+end`, pregledni kursor se neće pomicati na statusnu traku.
Ako vam je ta značajka potrebna molimo dodijelite odgovarajući tipkovnički prečac u kategoriji objektna navigacija u dijaloškom okviru ulazne geste. (#8600)
* Prilikom otvaranja postavki koje su već otvorene, NVDA će postaviti fokus na dijaloški okvir koji je već otvoren što je bolje od prikazivanja pogreške. (#5383)
* Nadograđen liblouis brajični prevoditelj na inačicu [3.19.0](https://github.com/liblouis/liblouis/releases/tag/v3.19.0). (#12810)
 * Nove brajične tablice: ruski kratkopis, Tshivenda puno pismo, Tshivenda kratkopis
* Umjesto "označeni sadržaj" ili "mrkd", "istaknuto" ili "istk." biti će prikazano na brajičnom retku. (#12892)
* NVDA više se neće pokušati isključiti kada se očekuje konkretna izvršena akcija u dijaloškom okviru (eg Confirm/Cancel). (#12984)

### Ispravke grešaka

* Praćenje modifikacijskih tipki poput tipaka Control, ili Insert je robusnije prilikom vraćanja glavnih komponenti u radnu spremnost. (#12609)
* Sada je ponovno moguće provjeravati za nadogradnje na nekim verzijama operacijskog sustava Windows npr. na čistim instalacijama operacijskog sustava Windows. (#12729)
* NVDA ispravno izgovara prazne ćelije tablice u Microsoft Wordu prilikom korištenja sučelja UI automation. (#11043)
* U ARIA ćelijama podatkovne tablice na web stranicama, tipka escape biti će preusmjerena na tablicu a način fokusa se neće bezuvjetno isključiti. (#12413)
* Prilikom čitanja zaglavlja ćelije tablice u Chromeu, ispravljeno je dvostruko čitanje naziva stupca. (#10840)
* NVDA više ne izgovara uzorak numeričke vrijednosti za UIA klizače koji imaju definiranu svoju tekstualnu vrijednost. (UIA ValuePattern je preferiraniji od RangeValuePattern). (#12724)
* NVDA više ne tretira vrijednost UIA klizača kao da su uvijek bazirani na postotcima.
* Izgovaranje pozicije ćelije u Microsoft Excelu kada se koristi sučelje UI Automation ponovno ispravno radi u Windowsima 11. (#12782)
* NVDA više ne postavlja netočne python lokalizacije. (#12753)
* Ako je onemogućeni dodatak deinstaliran a potom ponovno instaliran isti će ponovno biti omogućen. (#12792)
* Ispravljene su pogreške vezane uz nadogradnju i deinstalaciju dodataka gdje je mapa dodatka preimenovana ili su datoteke bile otvorene. (#12792, #12629)
* Prilikom korištenja sučelja UI Automation za pristup  Microsoft Excel kontrolama proračunskih tablica, NVDA više ne izgovara izlišna označavanja ćelija. (#12530)
* Više tekstova dijaloških okvira sada će se čitati u  LibreOffice Writeru, poput dijaloških okvira potvrde. (#11687)
* Kretanje  po dokumentima u Microsoft Wordu koristeći sučelje UI automation sada provjerava vidljivost trenutne pozicije, te da pozicija dokumenta u načinu fokusa je istovjetna sa onom u načinu pregleda. (#9611)
* Prilikom izvođenja prečaca za čitanje cijelog dokumenta u Microsoft Wordu koristeći sučelje UI automation, dokument se sada automatski prebacuje, i pozicija kursora sada se automatski osvježava. (#9611)
* Prilikom čitanja poruka elektroničke pošte u Outlooku kojima NVDA pristupa koristeći sučelje UI automation, neke vrste tablica sada se tretiraju kao tablice izgleda, što znaći da se one neće podrazumjevano izgovarati. (#11430)
* Ispravljena je rijetka pogreška prilikom mijenjanja zvučnih kartica. (#12620)
* Unos koristeći literarne brajične tablice, odnosno tablice punog pisma sada bi trebao biti pouzdaniji prilikom upisivanja u poljima za uređivanje. (#12667)
* Prilikom kretanja po kalendaru u području obavijesti, NVDA izgovara dan u tijednu u potpunosti. (#12757)
* Prilikom korištenja metoda unosa za kineski poput Tajvanski - Microsoft Quick u Microsoft Wordu, prebacivanje brajičnog retka u naprijed ili nazad više ne preskaće neispravno nazad na na izvornu poziciju. (#12855)
* Prilikom pristupanja dokumentima u Microsoft Wordu uz pomoć sučelja UIA, sada je moguće ponovno kretati se po rečenicama koristeći prečace alt+strelica dolje / alt+strelica gore. (#9254)
* Prilikom pristupa MS Wordu koristeći UIA, sad se izgovaraju uvlaćenja odlomaka. (#12899(
* Prilikom pristupa MS Wordu uz pomoć UIA, prečaci za praćenje izmjena i drugi lokalizirani prečaci sada se izgovaraju . (#12904)
* Ispravljena pogreška dvostrukog izgovora i prikaza na brajičnom redku kada se poklapao  'opis' sa 'sadržajem' ili 'nazivom'. (#12888)
* U MS Wordu sa uključenim UIA sučeljem, sada se točnije reproduciraju zvukovi koji označavaju pravopisnu ili gramatičku pogrešku prilikom pisanja. (#12161)
* U Windowsima 11, NVDA više neće izgovarati "prozor" prilikom pritiska Alt+Tab kada se prebacujete između programa. (#12648)
* Nova suvremena  prozor-stranica za komentare sada je podržana u MS Wordu kada se dokumentu ne pristupa koristeći UIA. Press alt+f12 to move between the side track pane and the document. (#12982)

### Changes for Developers

* Building NVDA now requires Visual Studio 2019 16.10.4 or later.
To match the production build environment, update Visual Studio to keep in sync with the [current version AppVeyor is using](https://www.appveyor.com/docs/windows-images-software/#visual-studio-2019). (#12728)
* `NVDAObjects.UIA.winConsoleUIA.WinConsoleUIA.isImprovedTextRangeAvailable` has been deprecated for removal in 2022.1. (#12660)
  * Instead use `apiLevel` (see the comments at `_UIAConstants.WinConsoleAPILevel` for details).
* Transparency of text background color sourced from GDI applications (via the display model), is now exposed for add-ons or appModules. (#12658)
* `LOCALE_SLANGUAGE`, `LOCALE_SLIST` and `LOCALE_SLANGDISPLAYNAME` are moved to the `LOCALE` enum in languageHandler.
They are still available at the module level but are deprecated and to be removed in NVDA 2022.1. (#12753)
* The usage of functions `addonHandler.loadState` and `addonHandler.saveState` should be replaced with their equivalents `addonHandler.state.save` and `addonHandler.state.load` before 2022.1. (#12792)
* Braille output can now be checked in system tests. (#12917)

## 2021.2

Ova inačica sadrži ranu podršku za  Windowse 11.
Iako bi sustav Windows 11 tek trebao biti objavljen, ova je inačica NVDA testirana na predpreglednim inačicama operacijskog sustava Windows 11.
Ovo uključuje važnu ispravku za zaslonsku zavjesu (molimo pogledajte važna upozorenja).
Alat za ispravljanje Com pogrešaka sada može ispraviti više pogrešaka kada je NVDA pokrenut.
Nadograđeni su govorna jedinica eSpeak i brajični prevoditelj LibLouis.
Ova inačica također dolazi sa jako puno poboljšanja, od kojih su najvažnija poboljšanja podrške za brajicu i Windows terminalne programe, kalkulator, emoji panel i povijest međuspremnika.

### Važna upozorenja

Zbog izmjena u Windows API-ju za uvećavanje, funkcija zaslonske zavjese trebala je biti nadograđena kako bi novije inačice operacijskog sustava Windows bile podržane.
Kako biste koristili zaslonsku zavjesu, koristite NVDA 2021.2 sa Windowsima 10 21H2 (10.0.19044) iliji novije inačice operacijskog sustava.
Ovo uključuje Windows 10 insidere i Windows 11.
Iz sigurnosnih razloga, prilikom korištenja novije inačice operacijskog sustava Windows, provjerite radi li zaslonska zavjesa.

### Nove značajke

* Eksperimentalna podrška Aria zabilješki:
  * Dodaje prečac za čitanje detalja objekta koji sadrži aria-details. (#12364)
  * Dodana opcija u naprednim postavkama za izvještavanje o detaljima u načinu pregleda. (#12439) 
* U Windowsima 10 verziji 1909 i novijim (uključujući Windows 11), NVDA će izgovarati broj prijedloga prilikom izvođenja pretrage u eksploreru za datoteke. (#10341, #12628)
* U Microsoft Wordu, NVDA sada čita rezultat prečaca za normalnu i viseću uvlaku pri izvršavanju. (#6269)

### Izmjene

* Espeak-ng je nadograđen na inačicu 1.51-dev commit `ab11439b18238b7a08b965d1d5a6ef31cbb05cbb`. (#12449, #12202, #12280, #12568)
* Ako je članak uključen u korisničkim postavkama oblikovanja dokumenata, NVDA izgovara "članak" poslje sadržaja. (#11103)
* Nadograđen liblouis brajični prevoditelj na inačicu [3.18.0](https://github.com/liblouis/liblouis/releases/tag/v3.18.0). (#12526)
  * Nove brajične tablice: Bugarski puno pismo, Burmansko puno pismo, Burmanski kratkopis, Kazaško puno pismo, Khmersko puno pismo, Sjevernokurdsko osnovno pismo, Sjeverni sotho puno pismo, Sjeverni sotho kratkopis, Južni sotho puno pismo, južni sotho kratkopis, Setswana puno pismo, Setswana kratkopis, tatarsko puno pismo, Vijetnamsko puno pismo, Vijetnamski kratkopis, Južni vijetnamski kratkopis, Xhosa puno pismo, Xhosa kratkopis, Jakutsko puno pismo, Zulu puno pismo, Zulu kratkopis
* Windows 10 OCR je preimenovan u Windows OCR. (#12690)

### Ispravke grešaka

* U Windows 10 kalkulatoru, NVDA će prikazivati izraze kalkulatora na brajičnom redku. (#12268)
* U programima terminala u Windowsima 10 inačica 1607 i novijim, prilikom umetanja ili brisanja teksta u sredini redka, znakovi desno od brisanog znaka nisu više čitani. (#3200)
  * Diff Match Patch sada je uključn podrazumijevano. (#12485)
* Unos brajičnih znakova ponovno radi sa sljedećim tablicama: Arapski kratkopis, Španjolski kratkopis, urdski kratkopis, Kineski (Kina, mandarinski) kratkopis. (#12541)
* Alat za ispravljanje pogrešaka com registracija sada ispravlja više pogrešaka, posebno na 64-bitnim Windowsima. (#12560)
* Ispravke upravljanja gumbima za Seika brajične bilježnice braille tvrtke Nippon Telesoft. (#12598)
* Unapređenja u čitanju  Windows panela emoji i povijesti međuspremnika. (#11485)
* Nadograđeni opisi znakova bengalske abecede. (#12502)
* NVDA izlazi sigurno kada se pokreće novi proces. (#12605)
* Ponovno označavanje Handy Tech upravljačkog progama za brajične redke iz dijaloškog okvira odabira brajičnog redka više ne prouzrokuje greške. (#12618)
* Inačice Windowsa 10.0.22000 ili novije sada se prepoznaju kao Windows 11, a ne kao Windows 10. (#12626)
* Ispravljena je podrška zaslonske zavjese te je ista testirana sa inačicama do 10.0.22000. (#12684)
* Ako nema rezultata ulaznih gesti, dijaloški okvir konfiguracije i dalje radi kako je to očekivano. (#12673)
* Ispravljena pogreška gdje je prva stavka izbornika nije izgovorena u nekim situacijama. (#12624)

### Changes for Developers

* `characterProcessing.SYMLVL_*` constants should be replaced using their equivalent `SymbolLevel.*` before 2022.1. (#11856, #12636)
* `controlTypes` has been split up into various submodules, symbols marked for deprecation must be replaced before 2022.1. (#12510)
  * `ROLE_*` and `STATE_*` constants should be replaced to their equivalent `Role.*` and `State.*`.
  * `roleLabels`, `stateLabels` and `negativeStateLabels` have been deprecated, usages such as `roleLabels[ROLE_*]` should be replaced to their equivalent `Role.*.displayString` or `State.*.negativeDisplayString`.
  * `processPositiveStates` and `processNegativeStates` have been deprecated for removal.
* On Windows 10 Version 1511 and later (including Insider Preview builds), the current Windows feature update release name is obtained from Windows Registry. (#12509)
* Deprecated: `winVersion.WIN10_RELEASE_NAME_TO_BUILDS` will be removed in 2022.1, there is no direct replacement. (#12544)

## 2021.1

Ova inačica sadrži opcionalnu eksperimentalnu podršku za UIA u Excelu i preglednicima baziranima na Chromium platformi.
Dodane su ispravke za neke jezike, te je popravljen način interakciej sa poveznicama koristeći brajični redak.
Nadograđeni su Unicode CLDR, matematički simboli i LibLouis.
Kao i puno ispravaka grešaka i unapređenja, uključujući ispravke grešaka u  Officeu, Visual Studio, te u nekim jezicima.

Upozorenje:

* Ova inačica zahtjeva nadogradnju na novije inačice dodataka.
* Ova inačica također ukida podršku za tehnologiju Adobe flash.

### Nove značajke

* Rana podrška za UIA u preglednicima baziranim na Chromium platformi. (such as Edge). (#12025)
* Rana eksperimentalna podrška za Microsoft Excel koristeći UI Automation. Preporučuje se samo sa Microsoft Excel inačicom 16.0.13522.10000 ili novijom. (#12210)
* Lakše kretanje po rezultatima u NVDA Python konzoli. (#9784)
  * alt+strelice gore/dolje skače na prethodni odnosno sljedeći rezultat (add shift for selecting).
  * control+l briše okno rezultata.
* NVDA sada izgovara kategorije zadataka u Microsoft Outlooku, ako postoje. (#11598)

### Izmjene

* U modusu čitanja, kontrole se mogu aktivirati uz pomoć brajičnog kursora koji se nalazi na opisu kontrole (na primjer. "pvz" za poveznicu). To je korisno za aktivaciju na primjer potvrdnih okvira bez oznaka. (#7447)
* NVDA sada sprječava izvođenje prepoznavanja teksta uz pomoć Windows 10 OCR, ako je zaslonska zavjesa uključena. (#11911)
* Nadograđen repozitorij zajedničkih podataka o lokalizaciju  (CLDR) na inačicu 39.0. (#11943)
* Dodano više matematičkih simbola u rječnik simbola. (#11467)
* Vodič za korisnike, datoteka sa popisom izmjena, i popis tipkovničkih prečaca sada imaju osvježen izgled. (#12027)
* Sada NVDA izgovara"nije podržano" prilikom pokušaja izmjene izgleda u aplikacijama koje to ne podržavaju, kao što je to Microsoft Word. (#7297)
* 'Pokušaj ignoriranja događaja govora koji su istekli' u naprednom panelu postavki je sada podrazumjevano omogućena. (#10885)
  * Ta se opcija može onemogučiti tako da se vrijednost postavi na "Ne".
  * Web aplikacije (npr. Gmail) više ne izgovaraju informacije koje su istekle pri brzom premještanju fokusa.
* Nadograđen Liblouis brajični prevoditelj na inačicu [3.17.0](https://github.com/liblouis/liblouis/releases/tag/v3.17.0). (#12137)
  * Nove brajične tablice: bjeloruska literarna brajica, bjeloruska kompjutorska brajica, Urdsko puno pismo, urdski kratkopis.
* Podrška za Flash sadržaj je uklonjena iz NVDA zbog toga što Adobe ne preporučuje korištenje te tehnologije. (#11131)
* NVDA će se isključiti čak iako su prozori otvoreni, u procesu izlazka iz NVDA zatvaraju se svi prozori NVDA sa njihovim pripadajućim dijaloškim okvirima. (#1740)
* Preglednik govora može biti zatvoren uz pomoć `alt+F4` te sadrži gumb zatvori za lakšu interakciju sa pokazivačkim uređajima. (#12330)
* Preglednik brajice sada posjeduje standardnu tipku zatvori za lakšu interakciju sa pokazivačkim uređajima. (#12328)
* U popisu elemenata, prečac na gumbu "aktiviraj" je uklonjen kako bise izbjegle kolizije za neke jezike sa oznakom izbornog gumba tip elementa. Kada je dostupan, gumb je podrazumjevani u dijaloškom okviru i kao takav se može aktivirati jednostavnim pritiskom tipke enter iz samog popisa elemenata. (#6167)

### Ispravke grešaka

* Popis poruka u Outlooku 2010 je ponovno čitljiv. (#12241)
* U terminalnim programima u  Windows 10 inačici 1607 i novijim, prilikom umetanja ili brisanja znakova usred redka, znakovi sa desne strane se više ne čitaju. (#3200)
  * Ova ispravka treba biti ručno uključena u naprednim korisnicima NVDA tako da se promjeni način čitanja izmjena u terminalnih programima na Diff Match Patch.
* U MS Outlooku, nepotrebno izgovaranje daljine prilikom prelazka iz polja za uređivanje poruke u u polje za upisivanje naslova više se ne bi smjelo događati. (#10254)
* U Python konzoli, sada je podržano unošenje znaka znaka tab za uvlačenje redka, i automatsko dovršavanje. (#11532)
* Informacije o oblikovanju teksta i druge poruke u modusu čitanja više ne pokazuju neočekivane prazne redke kada se isključi izlged ekrana. (#12004)
* Sada je moguće pročitati komentare u MS Wordu sa uključenom podrškom za UIA. (#9285)
* Unapređene su performanse prilikom interakcije sa Visual studio. (#12171)
* Ispravljene su grafičke pogreške kao što su to na primjer izostavljeni elementi kada se NVDA koristi sa jezikom koji se piše s desna na lijevo. (#8859)
* Poštuje se izgled prozora i njegov smjer baziran na jeziku NVDA, umjesto na jeziku sustava. (#638)
  * Poznata pogreška za jezike koji su pisani s desna na lijevo: desni graničnik grupiranja poklapa se sa oznakama/kontrolama. (#12181)
* Jezik pythona sada poštuje jezik namješten u postavkama, te će se isti koristiti prilikom korištenja podrazumjevanog jezika sustava. (#12214)
* TextInfo.getTextInChunks više se ne ruši kada se poziva na kontrolu obogaćenog teksta kao što je to NVAD preglednik zapisnika. (#11613)
* Sada je ponovno moguće koristiti NVDA sa jezicima koji u sebi sadrže znak podvlaka u nazivu jezika kao na primjer de_CH u verzijama operacijskog sustava Windows 10 1803 i 1809. (#12250)
* U WordPadu, podešavanje izgovora indeksa i eksponenata radi kao što je to i očekivano. (#12262)
* NVDA više ne neuspijeva izgovoriti novofokusirani sadržaj na web stranici ako stari fokus nestane i bude zamijenjen novim u na toj istoj poziciji. (#12147)
* Podcrtano, eksponent i indeks sada se izgovaraju za  cijele ćelije u Excelu ako je odgovarajuća opcija uključena. (#12264)
* Ispravljeno je kopiranje konfiguracije tijekom instalacije iz prijenosne kopije kada je odredišna putanja prazna. (#12071, #12205)
* Ispravljen je neispravan izgovor nekih slova sa akcentima ili dijakritičkih znakova kada je opcija 'izgovori veliko prije velikih slova' uključena. (#11948)
* Ispravljena je nemogućnost izmjene visine pri pisanju velikih slova koristeći  SAPI4 govornu jedinicu. (#12311)
* Instalacijski program NVDA sada također poštuje `--minimal` opciju naredbenog redka te ne reproducira zvuk pokretanja, ponašajući se kao prijenosna kopija NVDA izvršne datoteke. (#12289)
* U MS Wordu ili Outlooku, tipke za kretanje poi tablicama sada mogu se koristiti za kretanej po tablicama izgleda ako ej opcija  "uključi tablce izgleda" uključena u postavkama modusa čitanja. (#11899)
* više neće izgovarati "↑↑↑" za emoji znakove u određenim jezicima. (#11963)
* Espeak sada podržava kantonski i mandarinski kineski. (#10418)
* U novom Microsoft Edge pregledniku baziranom na Chromium platformi, tekstualna polja poput adresne trake sada se izgovaraju kada su prazna. (#12474)
* Ispravljen upravljački program za Seika brajične redke. (#10787)

### Changes for Developers

* Note: this is an Add-on API compatibility breaking release. Add-ons will need to be re-tested and have their manifest updated.
* NVDA's build system now fetches all Python dependencies with pip and stores them in a Python virtual environment. This is all done transparently.
  * To build NVDA, SCons should continue to be used in the usual way. E.g. executing scons.bat in the root of the repository. Running `py -m SCons` is no longer supported, and `scons.py` has also been removed.
  * To run NVDA from source, rather than executing `source/nvda.pyw` directly, the developer should now use `runnvda.bat` in the root of the repository. If you do try to execute `source/nvda.pyw`, a message box will alert you this is no longer supported.
  * To perform unit tests, execute `rununittests.bat [<extra unittest discover options>]`
  * To perform system tests: execute `runsystemtests.bat [<extra robot options>]`
  * To perform linting, execute `runlint.bat <base branch>`
  * Please refer to readme.md for more details.
* The following Python dependencies have also been upgraded:
  * comtypes updated to 1.1.8.
  * pySerial updated to 3.5.
  * wxPython updated to 4.1.1.
  * Py2exe updated to 0.10.1.0.
* `LiveText._getTextLines` has been removed. (#11639)
  * Instead, override `_getText` which returns a string of all text in the object.
* `LiveText` objects can now calculate diffs by character. (#11639)
  * To alter the diff behaviour for some object, override the `diffAlgo` property (see the docstring for details).
* When defining a script with the script decorator, the 'allowInSleepMode' boolean argument can be specified to control if a script is available in sleep mode or not. (#11979)
* The following functions are removed from the config module. (#11935)
  * canStartOnSecureScreens - use config.isInstalledCopy instead.
  * hasUiAccess and execElevated - use them from the systemUtils module.
  * getConfigDirs - use globalVars.appArgs.configPath instead.
* Module level REASON_* constants are removed from controlTypes - please use controlTypes.OutputReason instead. (#11969)
* REASON_QUICKNAV has been removed from browseMode - use controlTypes.OutputReason.QUICKNAV instead. (#11969)
* `NVDAObject` (and derivatives) property `isCurrent` now strictly returns Enum class `controlTypes.IsCurrent`. (#11782)
  * `isCurrent` is no longer Optional, and thus will not return None.
    * When an object is not current `controlTypes.IsCurrent.NO` is returned.
* The `controlTypes.isCurrentLabels` mapping has been removed. (#11782)
  * Instead use the `displayString` property on a `controlTypes.IsCurrent` enum value.
    * For example: `controlTypes.IsCurrent.YES.displayString`.
* `winKernel.GetTimeFormat` has been removed - use `winKernel.GetTimeFormatEx` instead. (#12139)
* `winKernel.GetDateFormat` has been removed - use `winKernel.GetDateFormatEx` instead. (#12139)
* `gui.DriverSettingsMixin` has been removed - use `gui.AutoSettingsMixin`. (#12144)
* `speech.getSpeechForSpelling` has been removed - use `speech.getSpellingSpeech`. (#12145)
* Commands cannot be directly imported from speech as `import speech; speech.ExampleCommand()` or `import speech.manager; speech.manager.ExampleCommand()` - use `from speech.commands import ExampleCommand` instead. (#12126)
* `speakTextInfo` will no longer send speech through `speakWithoutPauses` if reason is `SAYALL`, as `SayAllHandler` does this manually now. (#12150)
* The `synthDriverHandler` module is no longer star imported into `globalCommands` and `gui.settingsDialogs` - use `from synthDriverHandler import synthFunctionExample` instead. (#12172)
* `ROLE_EQUATION` has been removed from controlTypes - use `ROLE_MATH` instead. (#12164)
* `autoSettingsUtils.driverSetting` classes are removed from `driverHandler` - please use them from `autoSettingsUtils.driverSetting`. (#12168)
* `autoSettingsUtils.utils` classes are removed from `driverHandler` - please use them from `autoSettingsUtils.utils`. (#12168)
* Support of `TextInfo`s that do not inherit from `contentRecog.BaseContentRecogTextInfo` is removed. (#12157)
* `speech.speakWithoutPauses` has been removed - please use `speech.speechWithoutPauses.SpeechWithoutPauses(speakFunc=speech.speak).speakWithoutPauses` instead. (#12195, #12251)
* `speech.re_last_pause` has been removed - please use `speech.speechWithoutPauses.SpeechWithoutPauses.re_last_pause` instead. (#12195, #12251)
* `WelcomeDialog`, `LauncherDialog` and `AskAllowUsageStatsDialog` are moved to the `gui.startupDialogs`. (#12105)
* `getDocFilePath` has been moved from `gui` to the `documentationUtils` module. (#12105)
* The gui.accPropServer module as well as the AccPropertyOverride and ListCtrlAccPropServer classes from the gui.nvdaControls module have been removed in favor of WX native support for overriding accessibility properties. When enhancing accessibility of WX controls, implement wx.Accessible instead. (#12215)
* Files in `source/comInterfaces/` are now more easily consumable by developer tools such as IDEs. (#12201)
* Convenience methods and types have been added to the winVersion module for getting and comparing Windows versions. (#11909)
  * isWin10 function found in winVersion module has been removed.
  * class winVersion.WinVersion is a comparable and order-able type encapsulating Windows version information.
  * Function winVersion.getWinVer has been added to get a winVersion.WinVersion representing the currently running OS.
  * Convenience constants have been added for known Windows releases, see winVersion.WIN* constants.
* IAccessibleHandler no longer star imports everything from IAccessible and IA2 COM interfaces - please use them directly. (#12232)
* TextInfo objects now have start and end properties which can be compared mathematically with operators such as < <= == != >= >. (#11613)
  * E.g. ti1.start <= ti2.end
  * This usage is now prefered instead of ti1.compareEndPoints(ti2,"startToEnd") <= 0
* TextInfo start and end properties can also be set to each other. (#11613)
  * E.g. ti1.start = ti2.end
  * This usage is prefered instead of ti1.SetEndPoint(ti2,"startToEnd")
* `wx.CENTRE_ON_SCREEN` and `wx.CENTER_ON_SCREEN` are removed, use `self.CentreOnScreen()` instead. (#12309)
* `easeOfAccess.isSupported` has been removed, NVDA only supports versions of Windows where this evaluates to `True`. (#12222)
* `sayAllHandler` has been moved to `speech.sayAll`. (#12251)
  * `speech.sayAll.SayAllHandler` exposes the functions `stop`, `isRunning`, `readObjects`, `readText`, `lastSayAllMode`.
  * `SayAllHandler.stop` also resets the `SayAllHandler` `SpeechWithoutPauses` instance.
  * `CURSOR_REVIEW` and `CURSOR_CARET` has been replaced with `CURSOR.REVIEW` and `CURSOR.CARET`.
* `speech.SpeechWithoutPauses` has been moved to `speech.speechWithoutPauses.SpeechWithoutPauses`. (#12251)
* `speech.curWordChars` has been renamed `speech._curWordChars`. (#12395)
* the following have been removed from `speech` and can be accessed through `speech.getState()`. These are readonly values now. (#12395)
  * speechMode
  * speechMode_beeps_ms
  * beenCanceled
  * isPaused
* to update `speech.speechMode` use `speech.setSpeechMode`. (#12395)
* the following have been moved to `speech.SpeechMode`. (#12395)
  * `speech.speechMode_off` becomes `speech.SpeechMode.off`
  * `speech.speechMode_beeps` becomes `speech.SpeechMode.beeps`
  * `speech.speechMode_talk` becomes `speech.SpeechMode.talk`
* `IAccessibleHandler.IAccessibleObjectIdentifierType` is now `IAccessibleHandler.types.IAccessibleObjectIdentifierType`. (#12367)
* The following in `NVDAObjects.UIA.WinConsoleUIA` have been changed (#12094)
  * `NVDAObjects.UIA.winConsoleUIA.is21H1Plus` renamed `NVDAObjects.UIA.winConsoleUIA.isImprovedTextRangeAvailable`.
  * `NVDAObjects.UIA.winConsoleUIA.consoleUIATextInfo` renamed to start class name with upper case.
  * `NVDAObjects.UIA.winConsoleUIA.consoleUIATextInfoPre21H1` renamed `NVDAObjects.UIA.winConsoleUIA.ConsoleUIATextInfoWorkaroundEndInclusive`
    * The implementation works around both end points being inclusive (in text ranges) before [microsoft/terminal PR 4018](https://github.com/microsoft/terminal/pull/4018)
    * Workarounds for `expand`, `collapse`, `compareEndPoints`, `setEndPoint`, etc

## 2020.4

Ova inačica uključuje novu metodu unosa za kineski, nadogradnja Liblouisa te popis elemenata (NVDA+f7) u modusu fokusa.
Kontekstualna pomoć od sada je dostupna prilikom pritiska F1 u NVDA dijaloškim okvirima.
Unapređenje pravila čitanja simbola, govornih rječnika, brajičnih poruka i letimičnog čitanja.
Ispravke grešaka i unapređenja za Mail u windowsima 10, outlook, Teams, Visual Studio, Azure Data Studio, Foobar2000.
Na web stranicama, unapređenja u Google docs, i veća podrška za ARIA.
te puno drugih važnih ispravaka grešaka  i unapređenja.

### Nove značajke

* Pritiskom tipkovničkog prečaca f1 u dijaloškim okvirima, otvorit će se dio dokumentacije za za određeni dijaloški okvir. (#7757)
* Podrška samodovršavanja (IntelliSense) u Microsoft SQL Server Management Studio i Visual Studio 2017 i novijim inačicama. (#7504)
* Izgovor simbola i interpunkcije: podrška grupiranja u definiciji kompleksnih simbola te podrška za grupne reference u zamjenama čineći ih tako jednostavnijim i moćnijim alatom. (#11107)
* Od sada se korisnik obavještava prilikom pokušaja stvaranja zapisa sa netočnom zamjenom regularnog izraza. (#11407)
  * Točnije otkrivaju se greške prilikom grupiranja.
* Dodana podrška za nove metode unosa Kineski tradicionalni Quick i Pinyin U Windowsima 10. (#11562)
* Zaglavlje kartica od sada se tretiraju kao formulari po kojima se može kretati uz pomoć prečaca "f" za brzu navigaciju. (#10432)
* Dodan prečac za uključivanje ili isključivanje označenog (istaknutog) teksta; Ne postoji podrazumjevana pridjeljena gesta. (#11807)
* Dodan parametar --copy-portable-config koji omogućuje kopiranje konfiguracije u NVDA prijenosnu kopiju. (#9676)
* Za korisnike miša koji koriste brajični preglednik, od sada su dostupne virtualne routing tipke, prijeđite preko ćelije kako biste se na nju usmjerili. (#11804)
* NVDA od sada može automatski otkrivati Humanware Brailliant BI 40X and 20X brajične redke kada su spojeni preko USB ili bluetoth portova. (#11819)

### Izmjene

* Nadograđen liblouis brajični prevoditelj na inačicu 3.16.1:
 * Ispravljena višestruka rušenja
 * Dodana brajična tablica za baškirsko puno pismo
 * Dodana koptska kompjutorska brajična tablica
 * Dodana ruska literarna i ruska literarna sa prikazom velikih slova.
 * Dodana brajična tablica za afrikanersko puno pismo
 * Izbrisana je brajična tablica za rusko staro puno pismo
* Prilikom čitanja cijelog dokumenta u modusu pregleda, prečaci traži sljedeće i traži prethodno više ne zaustavljaju čitanje ako je opcija omogući letimično čitanje uključena; umjesto toga čitanje svega se nastavlja prije prethodnog ili sljedećeg pronađenog termina. (#11563)
* Za HIMS brajične retke kombinacija tipaka F3 je promijenjena u razmaknica + točkice 148. (#11710)
* Unapređenje izgleda opcija "stanka za poruke u milisekundama" i "Pokazuj poruke beskonačno". (#11602)
* U internetskim preglednicima i ostalim aplikacijama koje podržavaju modus čitanja, dijaloški okvir popis elemenata (NVDA+F7) može se otvoriti kada se nalazite u modusu fokusa. (#10453)
* Osvježavanje aria živih regija od sada je utišavano kada je izvještavanje o promjenama dinamičkog sadržaja isključeno. (#9077)
* NVDA će sada izgovoriti "kopirano u međuspremnik" prije kopiranog teksta. (#6757)
* Unapređeno čitanje tablice grafičkog pregleda u upravljanju tvrdim diskovima. (#10048)
* Oznake kontrola su od sada onemogućene (posivljene) kada je kontrola onemogućena. (#11809)
* Nadograđena CLDR anotacija Emoji na inačicu 38. (#11817)
* Ugrađena funkcija "praćenje fokusa" preimenovana je u "vizualno praćenje". (#11700)

### Ispravke grešaka

* NVDA sada ponovno radi u poljima za uređivanje pri korištenju Fast Log Entry programa. (#8996)
* Izgovaranje preostalog vremena u Foobar2000 ako ne postoji ukupno trajanje (NPR. prilikom reproduciranja streama u živo). (#11337)
* NVDA sada poštuje aria-roledescription atribut na elementima u sadržaju koji se može uređivati na web stranicama. (#11607)
* 'popis' se više ne izgovara za svaki redak popisa u Google Docs u otvorenom sadržaju koji se uređuje u Google Chromeu. (#7562)
* Prilikom kretanja kursorskim tipkama po znakovima ili slovima od jedne stavke popisa do druge u sadržaju koji se može uređivati na web stranicama, izgovara se ulazak u novi popis. (#11569)
* NVDA sada čita ispravni redak prilikom izmještanja kursora na kraj poveznice na kraju popisa u Google Docsu ili drugom sadržaju koji se može uređivati na web stranicama. (#11606)
* U Windowsima 7, otvaranje i zatvaranje start izbornika sa radne površine sada postavlja fokus pravilno. (#10567)
* Kada je opcija "pokušaj otkloniti događaje fokusa koji su istekli" omogućena, naslov kartice se sada izgovara ponovno prilikom prebacivanja kartica u Firefoxu. (#11397)
* NVDA više nema probleme poslije upisivanja znakova u popisu prilikom korištenja SAPI5 Ivona glasova. (#11651)
* Sada je ponovno moguće korištenje modusa čitanja prilikom čitanja elektroničke pošte u  Windows 10 Mailu 16005.13110 and later. (#11439)
* Prilikom korištenja SAPI5 Ivona glasova sa stranice harposoftware.com, NVDA sada može spremati svoju konfiguraciju, prebacivati govorne jedinice, te više te se neće utišavati poslije ponovnog pokretanja. (#11650)
* Sada je moguće upisati znamenku  6 koristeći kompjutorsku brajicu sa brajične tipkovnice na Himsovim brajičnim redcima. (#11710)
* Drastično poboljšanje performansi u Azure Data Studiu. (#11533, #11715)
* Sa uključenom opcijom "pokušaj ignoriranja događaja fokusa koji su istekli"  naslov dijaloškog okvira NVDA pretrage ponovno se čita. (#11632)
* NVDA više se ne bi trebao rušiti prilikom buđenja računala i premještanja fokusa u Microsoft edge dokumentu. (#11576)
* Više nije potrebno pritiskati tabulator ili premještati fokus poslije zatvaranja kontekstnog izbornika  kako bi način pregleda bio funkcionalan u MS edgeu. (#11202)
* NVDA sada čita stavke popisa unutar 64-bitnih aplikacija poput Tortoise SVN-a. (#8175)
* Aria mrežaste strukture sada se pokazuju kao normalne tablice u modusu čitanja u Firefoxu i Chromeu. (#9715)
* Obratna pretraga sada može biti započeta uz pomoć komande 'traži prethodno'  NVDA+shift+F3 (#11770)
* NVDA skripta se više ne tretira kao ponovljena ako se dogodi nerelevantni pritisak između dva izvršavanja skripte. (#11388) 
* Strong i emphasis tagovi u Internet exploreru opet mogu biti utišani tako da se isključi opcija izvještavaj o isticanju u postavkama oblikovanja. (#11808)
* Zastoj od nekoliko sekundi koji je iskusio mali broj korisnika a koji se događao prilikom kretanja po ćelijama u Excel više se ne bi trebao događati. (#11818)
* U Microsoft Teams kompilacijama sa brojevima verzija poput 1.3.00.28xxx, NVDA više neće odbijati čitati poruke u čavrljanjima ili kanalima skupine zbog nekorektno fokusiranog izbornika. (#11821)
* Tekst koji je u   Google Chrome označen istovremeno kao pravopisna i gramatička pogreška tako će biti i izgovoren. (#11787)
* Prilikom korištenja Microsoft outlooka na francuskom jeziku, prečac za  akciju 'odgovori svima' (control+shift+R) radi ponovno. (#11196)
* U Visual Studio, IntelliSense alatni savjetnici koji daju više detalja o trenutnoj stavci IntelliSense sada se izgovaraju samo jednom. (#11611)
* U Windows 10 kalkulatoru, NVDA više neće izgovarati tijek izračuna ako je opcija izgovor upisanih znakova isključena. (#9428)
* NVDA više se ne ruši prilikom korištenja Engleskog kratkopisa  za sjedinjene države te proširi riječ na kompjutorsku brajicu pod kursorom , prilikom prikazivanja određenog sadržaja kao pto je to internetska adresa. (#11754)
* Od sada je ponovno moguće čitati informacije o oblikovanju za fokusiranu ćeliju u Excelu koristeći prečac NVDA+F. (#11914)
* Unos sa qwerty tipkovnice na papenmeierovim brajičnim redcima, koji to podržavaju ponovno radi, a NVDA se više ne smrzava u slučajnim situacijama. (#11944)

### Changes for Developers

* System tests can now send keys using spy.emulateKeyPress, which takes a key identifier that conforms to NVDA's own key names, and by default also blocks until the action is executed. (#11581)
* NVDA no longer requires the current directory to be the NVDA application directory in order to function. (#6491)
* The aria live politeness setting for live regions can now be found on NVDA Objects using the liveRegionPoliteness property. (#11596)
* It is now possible to define separate gestures for Outlook and Word document. (#11196)

## 2020.3

Ova inačica uključuje nekoliko velikih unapređenja stabilnosti i performansi u Microsoft Office aplikacijama. Dodane su nove postavke za uključivanje izgovora grafičkih elemenata i podrške ekrana osjetljivih na dodir.
U preglednicima sada se može izgovarati postojanje označenog (obilježenog sadržaja), te dodane su i nove brajične tablice za njemački jezik.

### Nove značajke

* Sada možete uključivati ili isključivati izgovor grafičkih elemenata u postavkama oblikovanja dokumenta. Imajte na umu da isključivanjem ove opcije alternativni tekst će se i dalje čitati. (#4837)
* Sada možete uključivati ili isključivati podršku ekrana osjetljivih na dodir. Dodana je opcija na panel interakcije s ekranima osjetljivim na dodir. Podrazumjevani prečac za ovu opciju je NVDA+control+alt+t. (#9682)
* Dodane nove brajične tablice za njemački jezik. (#11268)
* NVDA sada izvještava o UIA kontrolama UIA koje su samo za čitanje. (#10494)
* Postojanje obilježenog teksta ili sadržaja sada se izgovara i pokazuje na brajičnom retku u web preglednicima. (#11436)
 * Ovo se može uključiti ili isključiti u postavkama oblikovanja dokumenta pomoću nove opcije za obilježavanje.
* Novi emulirani tipkovnički prečaci sada se mogu dadavati koristeći dijaloški okvir ulaznih gesti. (#6060)
  * Kako biste dodali takav prečac, pritisnite gumb dodaj poslje označavanja kategorije emulirani tipkovnički prečaci.
* Sada je podržan Handy Tech Active Braille sa joistickom. (#11655)
* Opcija "automatski način fokusa pri kretanju kursora" sada je kompatibilna sa onemogućavanjem o opcijom "automatski postavi fokus na elemente koji se mogu fokusirati". (#11663)

### Izmjene

* Prečac za izvještavanje o oblikovanju dokumenta (NVDA+f) je izmijenjen tako da izgovara izmjene pod kursorom sustava umjesto preglednog kursora. Kako biste čuli izmjene oblikovanja dokumenta pod preglednim kursorom Sada trebate koristiti prečac NVDA+shift+f. (#9505)
* NVDA više ne postavlja fokus na elemente koji se mogu fokusirati u web preglednicima, što unapređuje stabilnost i brzinu. (#11190)
* CLDR je nadograđen s inačice 36.1 na inačicu 37. (#11303)
* Nadograđen eSpeak-NG na inačicu 1.51-dev, commit 1fb68ffffea4
* Sada možete koristiti tabličnu navigaciju za popise sa označivim stavkama kada taj određen popis ima više stupaca. (#8857)
* U upravitelju dodataka, kada se pojavi pitanje o uklanjanju dodatka, gumb "ne" sada je podrazumjevana opcija. (#10015)
* U Microsoft Excelu, popis elemenata sada pokazuje formule u njihovom prevedenom obliku. (#9144)
* NVDA sada izgovara ispravnu terminologiju za bilješke u MS Excelu. (#11311)
* Kada se koristi prečac "premjesti pregledni kursor na fokus" u načinu pregleda, pregledni se kursor premješta na poziciju virtualnog kursora. (#9622)
* Informacije prikazane u modusu pregleda poput informacija o oblikovanju dokumenata koje se dobiju pritiskom NVDA+F, sada se prikazuju u malo većem prozoru koji se nalazi na sredini zaslona. (#9910)

### Ispravke grešaka

* NVDA sada izgovara simbol prilikom stajanja na riječi i kada znak slijedi poslije bijelog razmaka neovisno od postavke izgovora. (#5133)
* U aplikacijama koje koriste QT 5.11 ili noviji, opisi objekta sada ponovno izgovaraju. (#8604)
* Prilikom brisanja riječi kraticom control+delete, NVDA više ne ostaje tih. (#3298, #11029)
  * sada se izgovara rijeć koja slijedi poslije izbrisane riječi.
* U panelu općih postavki, popis jezika se sada ispravno sortira. (#10348)
* Značajno unapređene performanse u dijaloškom okviru ulaznih gesti prilikom filtriranja. (#10307)(
* Sada možete sa brajičnog retka upisivati Unicode znakove iznad vrijednosti  U+FFFF. (#10796)
* NVDA će sada ispravno čitati sadržaj dijaloškog okvira otvori sa u nadogradnji Windows 10 za svibanj 2020. (#11335)
* Dodana je nova eksperimentalna opcija u  naprednim postavkama (Uključi selektivnu registraciju UIA događaja i izmjena svojstava) koja može unaprijediti performance u Visual studio i drugim UIA automation aplikacijama ako je uključena. (#11077, #11209)
* Za stavke popisa koje se mogu odabrati, stanje označenosti se ne izgovara izlišno, te ako je moguće, umjesto njega se izgovara status neoznačenosti. (#8554)
* U Windowsima 10 nadogradnji za svibanj 2020, NVDA saa prikazuje Microsoft zvučni enumerator u dijaloškom okviru govorna jedinica. (#11349)
* U Internet Exploreru, brojevi se sada točno izgovaraju za parne popise ako popis ne počinje brojem 1. (#8438)
* U Google chromeu, NVDA će sada izgovarati "nije odabrano"  za sve kontrole koje su označive (ne samo za potvrdne okvire) koji su trenutno neoznačeni. (#11377)
* Sada je ponovno moguće kretati se po raznim kontrolama ako je jezik NVDA postavljen na Aragonski. (#11384)
* NVDA više se neće zaglavljivati u Microsoft Wordu prilikom brzog kretanja strelicama ili upisivanja znakova. (#11431, #11425, #11414)
* NVDA više ne dodaje nepostojeći dupli razmak prilikom kopiranja trenutnog objekta navigatora u međuspremnik. (#11438)
* NVDA više ne aktivira profil za čitanje cijelog sadržaja ako ne postoji ništa za čitanje. (#10899, #9947)
* NVDA sada čita popis funkcija u upravitelju internetskih servisa informacija (IIS). (#11468)
* NVDA sada ostavlja otvorenu zvučnu karticu takvim načinom poboljšavajući performanse (#5172, #10721)
* NVDA više se neće smrznuti ili srušiti prilikom pritiska i držanja ctrl+shift+strelica dolje u Microsoft Wordu. (#9463)
* Stanje skupljenosti ili raširenosti mapa na stranici drive.google.com sada je pravilno izgovarano. (#11520)
* Veliko unaprjeđenje performansi u Visual Studio Code. (#11533)

### Changes For Developers

* The GUI Helper's BoxSizerHelper.addDialogDismissButtons supports a new "separated" keyword argument, for adding a standard horizontal separator to dialogs (other than messages and single input dialogs). (#6468)
* Additional properties were added to app modules, including path for the executable (appPath), is a Windows Store app (isWindowsStoreApp), and machine architecture for the app (appArchitecture). (#7894)
* It is now possible to create app modules for apps hosted inside wwahost.exe on Windows 8 and later. (#4569)
* A fragment of the log can now be delimited and then copied to clipboard using NVDA+control+shift+F1. (#9280)
* NVDA-specific objects that are found by Python's cyclic garbage collector are now logged when being deleted by the collector to aide in removing reference cycles from NVDA. (#11499)
 * The majority of NVDA's classes are tracked including NVDAObjects, appModules, GlobalPlugins, SynthDrivers, and TreeInterceptors.
 * A class that needs to be tracked should inherit from garbageHandler.TrackedObject.
* Significant debug logging for MSAA events can be now enabled in NVDA's Advanced settings. (#11521)
* MSAA winEvents for the currently focused object are no longer filtered out along with other events if the event count for a given thread is exceeded. (#11520)

## 2020.2

Novosti u ovoj inačici uključuju podršku za novi brajični redak tvrtke Nattiq, poboljšanu podršku za antivirus eset nod32 te winodws naredbeni redak, unapređenje performanis u programu 1Password, poboljšanja sa sintetizatorom govora One core. Također, u ovu inačicu uvršteni su i puno drugih popravaka grešaka.

### Nove značajke

* Podrška za nove brajične retke:
  * Nattiq nBraille (#10778)
* Dodana mogučnost pridjeljivanja prečaca naredbi otvaranja konfiguracijske mape NVDA (Nema dodjeljene podrazumjevane geste). (#2214)
* Poboljšana podrška za dijaloške okvire ESET antivirusa. (#10894)
* Dodana podrška za Windows terminal. (#10305)
* Dodan prečac za izgovaranje trenutnog konfiguracijskog profila (nije dodjeljen podrazumjevano). (#9325)
* Dodan prečac za uključivanje i isključivanje izgovora eksponenata i indekasa (nema podrazumjevane geste). (#10985)
* Web aplikacije (npr. Gmail) više ne izgovaraju zastarjele informacije prilikom brzog kretanja. (#10885)
  * Ova eksperimentalna ispravka grešaka mora biti ručno uključena uz pomoć opcije 'pokušaj zaustavljanja govora za zastarjele događeje fokusa' na naprednom panelu postavki.
* Puno simbola je dodano u podrazumjevani rječnik simbola. (#11105)

### Izmjene

* Nadograđen liblouis brajični prevoditelj s inačice 3.12 Na inačicu [3.14.0](https://github.com/liblouis/liblouis/releases/tag/v3.14.0). (#10832, #11221)
* Izgovaranje indekasa i eksponenata sada se regulira odvojeno od izgovaranja atributa fonta. (#10919)
* Zbog promjena nastalih u VS Code, NVDA više podrazumjevano je isključuje modus pregleda. (#10888)
* NVDA više ne izgovara "početak" i "kraj" prilikom izravnog kretanja preglednim kursorom na prvi ili zadnji redak objekta navigatora uz pomoć prečaca premjesti se na početak i premjesti se na kraj. (#9551)
* NVDA više ne izgovara  "lijevo" i "desno" prilikom izravnog kretanja kursora pregleda na prvi ili zadnji znak u retku za trenutni objekt navigatora uz pomoć prečaca pomakni se na početak retka i pomoakni se na kraj retka. (#9551)

### Ispravke grešaka

* NVDA se sada ispravno pokreće kada nije moguće stvoriti datoteku zapisnika. (#6330)
* U posljednjim inačicama Microsoft Word 365, NVDA više neće izgovarati "brisanje posljednie riječi" kada je pritisnut prečac ctrl+bacpspace prilikom uređivanja dokumenta. (#10851)
* NVDA će opet izgovarati status uključenosti izmješanosti ili ponavljanja popisa za reprodukciju. (#10945)
* NVDA više nije ekstremno usporen prilikom kretanja po stavkama popisa u 1Passwordu. (#10508)
* Windows OneCore govorna jedinica više ne zastajkuje između izričaja. (#10721)
* NVDA više se ne smrzava prilimom otvaranja kontekstnog izbornika za 1Password u području obavijesti. (#11017)
* U Officeu 2013 i starijim:
  * Riboni se izgovaraju kada se fokus na njima nađe prvi put. (#4207)
  * Stavke kontekstnog izbornika sada se ponovno točno izgovaraju. (#9252)
  * Sekcije ribona sada su točno najavljivane prilikom kretanja po njima uz pomoć prečaca ctrl+strelica lijevo ili desno. (#7067)
* U načinu pregleda u Mozilla firefoxu I Google chromeu, tekst se više ne pojavljuje u jednom retku kada web sadržaj koristi CSS display: inline-flex. (#11075)
* U načinu pregleda sa opcijom Automatsko postavljanje fokusa na fokusirane elemente onemogućenom, sada je moguće aktivirati elemente koje nije moguće fokusirati.
* U načinu pregleda sa isključenom opcijom automatski postavi fokus na fokusirene elemente, sada je moguće aktivirati elemente koji se nalaze pod tabulatorom. (#8528)
* U načinu pregleda sa isključenom opcijom automatski postavi fokus na fokusirane elemente, više se ne događa klikanje na pogrešnu lokaciju. (#9886)
* NVDA zvuci pogreške više se ne reproduciraju prilikom pristupa kontrolama DevExpress. (#10918)
* Alatni savjetnici ikona u polju obavijesti više se ne izgovaraju prilikom kretanja tipkovnicom ako je njihov tekst jednak nazivu ikone, kako bi se izbjeglo duplo izgovaranje. (#6656)
* U načinu pregleda sa isključenom opcijom automatski postavi fokus na fokusirane elemente, prebacivanje modusa fokusa uz pomoć prečaca insert+razmak, sada fokusira element pod kursorom. (#11206)
* Sada je pomovno moguće provjeravati nadogradnje NVDA na nekim sustavima; NPR. čise instalacije Windowsa. (#11253)
* Fokus se ne premješta u Java aplikacijama kada se fokus mijenja u stablu prikaza, tablici ili popisu. (#5989)

### Changes For Developers

* execElevated and hasUiAccess have moved from config module to systemUtils module. Usage via config module is deprecated. (#10493)
* Updated configobj to 5.1.0dev commit f9a265c4. (#10939)
* Automated testing of NVDA with Chrome and a HTML sample is now possible. (#10553)
* IAccessibleHandler has been converted into a package, OrderedWinEventLimiter has been extracted to a module and unit tests added (#10934)
* Updated BrlApi to version 0.8 (BRLTTY 6.1). (#11065)
* Status bar retrieval may now be customized by an AppModule. (#2125, #4640)
* NVDA no longer listens for IAccessible EVENT_OBJECT_REORDER. (#11076)
* A broken ScriptableObject (such as a GlobalPlugin missing a call to its base class' init method) no longer breaks NVDA's script handling. (#5446)

## 2020.1

Novosti u ovoj inačici uključuju podrška novih brajičnih redaka firmi HumanWare i APH, te puno važnih ispravaka grešaka poput ponovnog omogućavanja čitanja matematičkog sadržaja u Microsoft Wordu koristeći MathPlayer / MathType.

### Nove značajke

* Označena stavka se sada ponovno pokazuje u načinu pregleda u Chromeu, slično kao u  NVDA 2019.1. (#10713)
* Sada možete izvoditi desni klik miša na dodirnim uređajima tako da dodirnete i držite jedan prst na ekranu. (#3886)
* Podrška za nove brajične retke: APH Chameleon 20, APH Mantis Q40, HumanWare BrailleOne, BrailleNote Touch v2, and NLS eReader. (#10830)

### Izmjene

* NVDA će spriječiti sustav u pokušaju odlaska u status mirovanja prilikom izvršavanja naredbe čitaj sve. (#10643)
* Podrška za izvanprocesne okvire u Mozilla Firefoxu. (#10707)
* Nadograđen liblouis brajični prevoditelj na inačicu 3.12. (#10161)

### Ispravke grešaka

* Ispravljena pogreška, koja je onemogućavala čitanje znaka za minus (U+2212) (#10633)
* Prilikom instalacije dodataka iz upravitelja dodataka, Imena datoteka i mapa se ne izgovaraju dva puta. (#10620, #2395)
* U Firefoxu, prilikom učitavanja Mastodona sa uključenim naprednim web sučeljem, sve se vremenske osi prikazuju pravilno u načinu čitanja. (#10776)
* U načinu pregleda, NVDA sada izgovara "nije odabrano" za potvrdne okvire u kojima to prethodno nije bilo činjeno. (#10781)
* ARIA kontrole preklopnika više ne izgovaraju zbunjujuće informacije kao što su to "nije pritisnuto odabrano" ili "pritisnuto odabrano". (#9187)
* SAPI4 glasovi više ne odbijaju izgovarati većinu teksta. Bilješka prevoditelja: To se tiče sintetizatora govora koji ne stignu poslati informaciju čitaču zaslona da su primili informaciju o izgovorenom tekstu. (#10792)
* NVDA može ponovno čitati i ulaziti u interakciju sa matematičkim jednadžbama u Microsoft Wordu. (#10803)
* NVDA će od sada izgovarati neoznačeni tekst u modusu pregleda prilikom pritiska strelice kada je tekst označen. (#10731).
* NVDA se više ne isključuje ako postoji greška inicijalizacije Espeaka. (#10607)
* Greške prouzročeneUnicode kodnom stranicom pri prevedenom tipkovničkom prečacu više ne onemogućavaju stvaranje prečaca radne površine, Rješeno tako da će se instalacijski program vratiti na engleski tekst. (#5166, #6326)
* Ulazeći i izlazeći iz popisa i tablica prilikom čitanja svega ili letimičnog čitanja više ne izgovara činjenicu o izlazu iz tablice ili popisa. (#10706)
* Ispravljeno praćenje miša na nekim MSHTML elementima u Internet Exploreru. (#10736)

### Changes for Developers

* Developer documentation is now build using sphinx. (#9840)
* Several speech functions have been split into two. (#10593)
  The speakX version remains, but now depends on a getXSpeech function which returns a speech sequence.
  * speakObjectProperties now relies on getObjectPropertiesSpeech
  * speakObject now relies on getObjectSpeech
  * speakTextInfo now relies on getTextInfoSpeech
  * speakWithoutPauses has been converted into a class, and refactored, but should not break compatibility.
  * getSpeechForSpelling is deprecated (though still available) use getSpellingSpeech instead.
  Private changes that should not affect addon developers:
  * _speakPlaceholderIfEmpty is now _getPlaceholderSpeechIfTextEmpty
  * _speakTextInfo_addMath is now _extendSpeechSequence_addMathForTextInfo
* Speech 'reason' has been converted to an Enum, see controlTypes.OutputReason class. (#10703)
  * Module level 'REASON_*' constants are deprecated.
* Compiling NVDA dependencies now requires Visual Studio 2019 (16.2 or newer). (#10169)
* Updated SCons to version 3.1.1. (#10169)
* Again allow behaviors._FakeTableCell to have no location defined (#10864)

## 2019.3

NVDA 2019.3 je inačica koja sadrži puno značajnih promjena uključujući nadogradnju Pythona 2 na Python 3, te veliko prepisivanje podsistema govora.
Iako ove izmjene stare dodatke čine nekompatibilnima, Nadogradnja na Python 3 bila je nužna radi sigurnosti, a izmjene u podsistemu govora će otvoriti put za nove inovativne mogućnosti u bliskoj budućnosti.
 Ostale izmjene uključuju 64 bitnu podršku za Java virtualne mašine, zaslonsku zavjesu i označitelja fokusa, podrška za puno više brajičnih redaka te novi brajični preglednik, te puno drugih ispravaka grešaka.

### Nove značajke

* Točnost komande "premjesti miš na objekt navigatora", sada je unapređena u tekstualnim poljima u Java aplikacijama. (#10157)
* Dodana podrška za sljedeće Handy Techove brajične retke (#8955):
 * Basic Braille Plus 40
 * Basic Braille Plus 32
 * Connect Braille
* Sve korisnički definirane opcije sada mogu biti uklonjene uz pomoć novog gumba "Vrati na zadane vrijednosti" u dijaloškom okviru ulazne geste. (#10293)
* Izvještavanje o fontu u Microsoft Wordu sada uključuje informaciju o tome jeli tekst skriven. (#8713)
* Dodana komanda za premještavanje kursora pregleda na poziciju označenu kao početni marker za označavanje ili kopiranje: NVDA+shift+F9. (#1969)
* U Internet Exploreru, Microsoft Edgeu i posljednjim inačicama Firefoxa i Chromea, orjentiri su sada izgovoreni u načinu fokusate uz pomoć objektne navigacije. (#10101)
* U Internet Exploreru, Google Chromeu i Mozilla Firefoxu, sada se možete kretati po člancima i grupama koristeći prečace za brzo kretanje. Podrazumjevano ovi prečaci nisu pridjeljeni i mogu se pridjeliti u dijaloškom okviru ulaznih gesti kada je dijaloški okvir otvoren u dokumentu koji koristi način pregleda. (#9227)
 * Figure se također izgovaraju. Iste se smatraju objektima i stoga se po njima može kretati koristeći kraticu brzog kretanja "o".
* U Internet Exploreru, Google Chromeu i Mozilla Firefoxu, članci se sada izgovaraju koristeći objektnu navigaciju, te neobavezno u načinu pregleda ako je opcija uključena u postavkama oblikovanja dokumenta. (#10424)
* Dodana zaslonska zavjesa, koja kada je uključena, zatamnjuje zaslon u Windowsima 8 i novijim. (#7857)
 * Dodan prečac za omogućavanje zaslonske zavjese (do sljedećeg ponovnog pokretanja sa jednim pritiskom, ili uvijek kada je NVDA pokrenut sa dva pritiska). Ovaj prečac nije dodijeljen.
 * Može biti uključeno preko kategorije 'vid' u dijaloškom okviru NVDA postavki.
* Dodana značajka označavanja zaslona u NVDA. (#971, #9064)
 * Označavanje fokusa, objekta navigatora, i kursora u modusu pregleda može biti omogućeno i podešeno preko kategorije vid u dijaloškom okviru NVDA postavki.
 * Napomena: ova je značajka nekompatibilna s dodatkom Focus highlight, međutim, dodatak se moš uvjek može koristiti kada je ugrađeni označivač uključen.
* Dodan brajični preglednik, koji omogućuje prikaz brajice na zaslonu. (#7788)

### Izmjene

* Vodič za korisnike sada opisuje kako koristiti Windowsov naredbeni redak s NVDA. (#9957)
* Pokretanje nvda.exe sada podrazumjevano zamjenjuje već pokrenutu kopiju NVDA. Parametar -r|--replace se još uvijek prihvaća, ali je isti ignoriran. (#8320)
* U Windowsima 8 i novijim, NVDA će sada izgovoriti nazim aplikacije i inačicu za hostane aplikacije poput aplikacija u Microsoft Store-u koristeći informaciju koju je NVDA dobio od aplikacije. (#4259, #10108)
* Prilikom uključivanja praćenja izmjena u Microsoft Wordu putem tipkovnice, NVDA će izgovarati stanje postavke. (#942) 
* NVDA inačica je prva zapisivana u zapisniku. Ovo se događa kada je vođenje zapisnika isključeno u postavkama. (#9803)
* Iz dijaloškog okvira postavki više nije moguće mijenjati razinu vođenja zapisnika, ako je parametar nadpisan preko naredbenog retka. (#10209)
* U Microsoft Wordu, NVDA sada izgovara status pokazivanja znakova koji se ne pokazuju prilikom ispisa kada se pritisne prečac za uključivanje ili isključivanje ove opcije Ctrl+Shift+8. (#10241)
* Nadograđen Liblouis brajični prevoditelj na inačicu 58d67e63. (#10094)
* Kada je uključeno izgovaranje CLDR znakova, uključujući emoji,, oni se izgovaraju neovisno od razine interpunkcije. (#8826)
* Pythonovski paketi treće strane, kao što je to comtypes, sada zapisuju svoje greške i upozorenja u NVDA zapisnik. (#10393)
* Nadograđen opći repozitorij Unicode znakova na inačicu 36.0. (#10426)
* Prilikom fokusiranja grupe u modusu pregleda, sada se izgovara i opis. (#10095)
* Java Access Bridge se sada isporučuje sa NVDA kako bi se omogućio pristup java aplikacijama, uključujući i 64-bitne Java virtualne mašine. (#7724)
* Ako Java Access Bridge nije uključen za korisnika, NVDA automatski ga uključuje pri pokretanju. (#7952)
* Nadograđen eSpeak-NG na inačicu 1.51-dev, commit ca65812ac6019926f2fbd7f12c92d7edd3701e0c. (#10581)

### Ispravci Grešaka

* Emoji i ostali 32-bitni unicode znakovi sada zauzimaju manje mjesta na brajičnom retku kada se pokazuju kao heksadecimalne vrijednosti. (#6695)
* U Windowsima 10, NVDA će izgovarati alatne savjetnike iz univerzalnih aplikacija ako je NVDA podešen da ih izgovara putem dijaloškog okvira prezentacija objekta. (#8118)
* U Windows 10 jubilejnoj nadogradnji i novijim, upisani se tekst izgovara u Mintty. (#1348)
* U Windowsima 10 jubilejnoj nadogradnji i novijim, izlazna informacija u Windows naredbenom retku koja se pojavljuje blizu kursora više se ne slovka. (#513)
* Sada se izgovaraju kontrole kompresora u dijaloškom okviru kompresora u Audacity prilikom kretanja po dijaloškom okviru. (#10103)
* NVDA više ne tretira razmake kao riječi s objektnom navigacijom u Scintilla uređivačima teksta poput Notepadd++. (#8295)
* NVDA će spriječiti sustav da uspava računalo kada se krećemo po tekstu uz pomoć brajičnog retka. (#9175)
* U Windowsima 10, brajica će pratiti uređivanje sadržaja ćelije i drugim UIA kontrolama teksta kada je isti zaostajao. (#9749)
* NVDA će opet izgovarati prijedloge u Microsoft Edge adresnoj traci. (#7554)
* NVDA više nije tih prilikom fokusiranja zaglavlja HTML kontrolne kartice u Internet Exploreru. (#8898)
* U Microsoft Edge baziranom na EdgeHTML, NVDA više neće reproducirati zvuk prijedloga pretrage kada prozor postane maksimiziran. (#9110, #10002)
* ARIA 1.1 odabirni okviri sada su podržani u Mozilla Firefoxu i Google Chromeu. (#9616)
* NVDA više neće izgovarati vizualno skriveni sadržaj stupaca za popise u SysListView32 kontrolama. (#8268)
* Dijaloški okvir postavki više ne pokazuje "info" kao trenutnu razinu zapisnika kada se nalazi u sigurnom načinu. (#10209)
* U izborniku start Windowsa 10 jubilejne nadogradnje i novijim, NVDA će izgovarati detalje rezultata pretrage. (#10232)
* U načinu pregleda, ako kretnja kursora ili brzo kretanje prouzrokuju promjenu dokumenta, NVDA više ne izgovara neispravan sadržaj u nekim situacijama. (#8831, #10343)
* Neka imena točaka su ispravljena u Microsoft Wordu. (#10399)
* U Windowsima 10 nadogradnji za svibanj 2019 i novijoj, NVDA će opet izgovarati prvu stavku na popisu emoji ili element međuspremnika kada se otvori povijest međuspremnika ili emoji panel. (#9204)
* U Poeditu, opet je moguće čitati prijevode za jezike koji se pišu s desna na lijevo. (#9931)
* U postavkama u Windowsima 10 nadogradnji za travanj 2018 i novijim, NVDA više neće izgovarati informaciju o postotcima za metre glasnoće koji se nalaze na stranici zvuk. (#10284)
* Nepravilni regularni izrazi više ne zaustavljaju govor u NVDA. (#10334)
* Prilikom čitanja liste nabrajanja u Microsoft Wordu sa uključenim UIA, sljedeća stavka popisa više se ne izgovara na neželjen način. (#9613)
* Nekoliko rijetkih grešaka sa brajičnim prevođenjem i Liblouis brajičnim prevoditeljem je ispravljeno. (#9982)
* Java aplikacije pokrenute prije NVDA sada se pokreću bez potrebe za ponovnim pokretanjem Java aplikacije. (#10296)
* U Mozilla Firefoxu, kada je fokusirani element označen kao trenutan (aria-current), više se ne izgovara više puta uzastopce. (#8960)
* NVDA će sada tretirati neke sastavne unicode znakove poput e s naglaskom kao jedan znak prilikom kretanja po tekstu. (#10550)
* Spring Tool Suite inačica 4 sada je podržana. (#10001)
* Kada je Aria-labellz unutrašnji element, ozgovor se neće dublirati. (#10552)
* U Windowsima 10 inačici 1607 i novijim, upisani znakovi na brajičnim tipkovnicama sada su izgovoreni u većini situacija ispravno. (#10569)
* Prilikom izmjene izlaznog audio uređaja, zvukovi koje reproducira NVDA sada će se reproducirati na novom uređaju. (#2167)
* U Mozilla Firefoxu, kretanje u modusu pregleda je sada brže. Ovo omogućuje brže kretanje kursorom u puno slučajeva. (#10584)

### Changes for Developers

* Updated Python to 3.7. (#7105)
* Updated pySerial to version 3.4. (#8815)
* Updated wxPython to 4.0.3 to support Python 3.5 and later. (#9630)
* Updated six to version 1.12.0. (#9630)
* Updated py2exe to version 0.9.3.2 (in development, commit b372a8e from albertosottile/py2exe#13). (#9856)
* Updated UIAutomationCore.dll comtypes module to version 10.0.18362. (#9829)
* The tab-completion in the Python console only suggests attributes starting with an underscore if the underscore is first typed. (#9918)
* Flake8 linting tool has been integrated with SCons reflecting code requirements for Pull Requests. (#5918)
* As NVDA no longer depends on pyWin32, modules such as win32api and win32con are no longer available to add-ons. (#9639)
 * win32api calls can be replaced with direct calls to win32 dll functions via ctypes.
 * win32con constants should be defined in your files.
* The "async" argument in nvwave.playWaveFile has been renamed to "asynchronous". (#8607)
* speakText and speakCharacter methods on synthDriver objects are no longer supported.
 * This functionality is handled by SynthDriver.speak.
* SynthSetting classes in synthDriverHandler have been removed. Now use driverHandler.DriverSetting classes instead.
* SynthDriver classes should no longer expose index via the lastIndex property.
 * Instead, they should notify the synthDriverHandler.synthIndexReached action with the index, once all previous audio has finished playing before that index.
* SynthDriver classes must now notify the synthDriverHandler.synthDoneSpeaking action, once all audio from a SynthDriver.speak call has completed playing.
* SynthDriver classes must support the speech.PitchCommand in their speak method, as changes in pitch for speak spelling now depends on this functionality.
* The speech function getSpeechTextForProperties has been renamed to getPropertiesSpeech. (#10098)
* The braille function getBrailleTextForProperties has been renamed to getPropertiesBraille. (#10469)
* Several speech functions have been changed to return speech sequences. (#10098)
 * getControlFieldSpeech
 * getFormatFieldSpeech
 * getSpeechTextForProperties now called getPropertiesSpeech
 * getIndentationSpeech
 * getTableInfoSpeech
* Added a textUtils module to simplify string differences between Python 3 strings and Windows unicode strings. (#9545)
 * See the module documentation and textInfos.offsets module for example implementations.
* Deprecated functionality now removed. (#9548)
 * AppModules removed:
  * Windows XP sound recorder.
  * Klango Player, which is abandoned software.
 * configobj.validate wrapper removed.
  * New code should use from configobj import validate instead of import validate
 * textInfos.Point and textInfos.Rect replaced by locationHelper.Point and locationHelper.RectLTRB respectively.
 * braille.BrailleHandler._get_tether and braille.BrailleHandler.set_tether have been removed.
 * config.getConfigDirs has been removed.
 * config.ConfigManager.getConfigValidationParameter has been replaced by getConfigValidation
 * inputCore.InputGesture.logIdentifier property has been removed.
   * Use _get_identifiers in inputCore.InputGesture instead.
 * synthDriverHandler.SynthDriver.speakText/speakCharacter have been removed.
 * Removed several synthDriverHandler.SynthSetting classes.
   * Previously kept for backwards compatibility (#8214), now considered obsolete.
   * Drivers that used the SynthSetting classes should be updated to use the DriverSetting classes.
 * Some legacy code has been removed, particularly:
  * Support for the Outlook pre 2003 message list.
  * An overlay class for the classic start menu, only found in Windows Vista and earlier.
  * Dropped support for Skype 7, as it is definitely not working any more.
* Added a framework to create vision enhancement providers; modules that can change screen contents, optionally based on input from NVDA about object locations. (#9064)
 * Add-ons can bundle their own providers in a visionEnhancementProviders folder.
 * See the vision and visionEnhancementProviders modules for the implementation of the framework and examples, respectively.
 * Vision enhancement providers are enabled and configured via the 'vision' category in NVDA's settings dialog.
* Abstract class properties are now supported on objects that inherit from baseObject.AutoPropertyObject (e.g. NVDAObjects and TextInfos). (#10102)
* Introduced displayModel.UNIT_DISPLAYCHUNK as a textInfos unit constant specific to DisplayModelTextInfo. (#10165)
 * This new constant allows walking over the text in a DisplayModelTextInfo in a way that more closely resembles how the text chunks are saved in the underlying model.
* displayModel.getCaretRect now returns an instance of locationHelper.RectLTRB. (#10233)
* The UNIT_CONTROLFIELD and UNIT_FORMATFIELD constants have been moved from virtualBuffers.VirtualBufferTextInfo to the textInfos package. (#10396)
* For every entry in the NVDA log, information about the originating thread is now included. (#10259)
* UIA TextInfo objects can now be moved/expanded by the page, story and formatField text units. (#10396)
* External modules (appModules and globalPlugins) are now less likely to be able to break the creation of NVDAObjects. 
 * Exceptions caused by the "chooseNVDAObjectOverlayClasses" and "event_NVDAObject_init" methods are now properly caught and logged.
* The aria.htmlNodeNameToAriaLandmarkRoles dictionary has been renamed to aria.htmlNodeNameToAriaRoles. It now also contains roles that aren't landmarks.
* scriptHandler.isCurrentScript has been removed due to lack of use. There is no replacement. (#8677)

## 2019.2.1

Ovo je mala inačica koja ispravlja nekoliko rušenja u inačici 2019.2. Ispravci uključuju:

* Ispravljeno nekoliko rušenja u Gmail-u uočeno u  Firefoxu i Chromeu prilikom interakcije sa nekim skočnim izbornicima, kao što je to stvaranje filtera ili mijenjanje nekih postavki Gmail-a. (#10175, #9402, #8924)
* U Windowsima 7, NVDA više neće prouzrokovati rušenje Windows upravitelja za datoteke kada se miš koristi u start izborniku. (#9435) 
* Windows Explorer u Windowsima 7 se više ne ruši prilikom pristupa metapodatcima. (#5337) 
* NVDA se više ne ruši prilikom interakcije sa slikama koje sadrže base64 URI u Mozilla Firefoxu ili Google Chromeu. (#10227)

## 2019.2

Novosti u ovoj inačici uključuju  automatsko otkrivanje Freedom Scientific brajičnih redaka, eksperimentalnu postavku u panelu naprednih postavki koja zaustavlja način pregleda da pomiće fokus (što može doprinijeti unapređenim performansama), opciju dodatne vrzine za  Windows OneCore govornu jedinicu kako bise postigle velike brzine govora, i mnogo drugih ispravaka grešaka.

### Nove značajke

* NVDA podrška za Miranda NG radi s novijim inačicama klijenta. (#9053) 
* Sada podrazumjevano možete isključiti način pregleda isključujući opciju "uključi način pregleda pri učitavanju stranice" u postavkama načina pregleda NVDA. (#8716) 
 * Imajte na umu da kada je ova opcija isključena, Još uvjek možete ručno uključiti način pregleda pritiščući tipkovnički prečac nvda+razmak.
* Sada možete filtrirati simbole u dijaloškom okviru izgovora simbola, na sličan način na koji filtriranje radi u popisu elemenata i dijaloškom okviru ulaznih gesti. (#5761)
* Dodana je komanda uz pomoć koje može se promjeniti razlučivost jedinice miša (to jest, kako će tekst biti izgovaran pri pomicanju miša), Ta komanda nema pridjeljen prečac. (#9056)
* windows OneCore govorna jedinica sada podržava opciju dodatne brzine, što omogućava veću regulaciju brzine. (#7498)
* Opcija dodatne brzine sada se može podešavati koristeći prsten govornih jedinica za podržane govorne jedinice. (trenutno su to eSpeak-NG i Windows OneCore). (#8934)
* Konfiguracijski profili sada mogu biti ručno aktivirani uz pomoć gesti. (#4209)
 * Geste mogu biti konfigurirane u dijaloškom okviru "ulazne geste".
* Dodana podrška samodovršavanja u Eclipse uređivaču izvornog koda. (#5667)
 * Dodatno, Javadoc informacija može se pročitati iz uređivača kada ista postoji koristeći NVDA+d.
* Dodana eksperimentalna opcija на panel naprednih postavki koja zaustavlja praćenje fokusa sustava u načinu pregleda (Automatski postavi  način pregleda na elemente fokusa). (#2039) Although this may not be suitable to turn off for all websites, this may fix: 
 * Efekt postranosti: NVDA sporadično poništava posljednih prečac u načinu pregleda preskačući na prethodnu poziciju.
 * Polja za uređivanje uzimaju fokus sustava prilikom kretanja po njima na nekim web stranicama.
 * Prečaci načina pregleda su sporoodzivni.
* Za brajične retke koji to podržavaju, postavke upravljačkog programa se mogu izmjeniti iz kategorije brajičnih postavki U NVDA postavkama. (#7452)
* Automatsko otkrivanje brajičnih redaka sada podržava i Freedom Scientific brajične retke. (#7727)
* Dodana komanda koja prikazuje zamjenu za simbol pod preglednim kursorom. (#9286)
* Dodana eksperimentalna funkcija na panel postavki "napredno", koja omogućuje isprobavanje nove podrške za Windows naredbene retke, koja je još u izradi, koja koristi novi UI Automation API. (#9614)
* U Python konzoli, polje za uređivanje sada podržava ljepljenje više redaka iz međuspremnika. (#9776)

### Izmjene

* Glasnoća govorne jedinice sada se može pojačavati ili smanjivati po svakih pet posto umjesto po svakih deset, koristeći prsten govorne jedinice. (#6754)
* Objašnjen test u NVDA upravitelju dodataka kada je NVDA pokrenut sa zastavicom --disable-add-ons. (#9473)
* Nadograđen repozitorij djeljenog repozitorija anotacija za emoji na inačicu 35.0. (#9445)
* Prečac za polje filtriranja u popisu elemenata u načinu pregleda je promjenjen na alt+y. Bilješka prevoditelja: ista se promjena ne odnosi na hrvatski prijevod NVDA! (#8728)
* Kada je automatski otkriven brajični redak spojen preko Bluetooth veze, NVDA će i dalje tražiti retke povezane preko USB priključka, a koji su podržani od strane istog upravljačkog programa, te će se prebaciti na USB vezu, ako je ista podržana. (#8853)
* Nadograđen eSpeak-NG na inačicu 67324cc.
* Nadograđen liblouis brajični prevoditelj na inačicu 3.10.0. (#9439, #9678)
* NVDA će sada izgovarati riječ  'označeno' poslije trenutnog označenog teksta.(#9028, #9909)
* U Microsoft Visual Studio Code, NVDA se sada podrazumjevano nalazi u načinu fokusa. (#9828)

### Ispravci grešaka

* NVDA se više ne ruši kada je mapa s dodacima prazna. (#7686)
* LTR i RTL znakovi sada se e pokazuju na brajičnom retku ili izgovaraju kada pristupate svojstvima u upravitelju datoteka. (#8361)
* Prilikom preskakanja po formularima u načinu pregleda brzim kretanjem,sada se izgovara cijeli formular umjesto cjijelog retka. (#9388)
* NVDA više se neće utišavati prilikom zatvaranja Windows 10 aplikacije pošta. (#9341)
* NVDA više neće odbijati pokretanje kada su korisničke regionalne postavke podešene na lokalnu postavku koju NVDA ne prepoznaje, poput engleskog (Nizozemska). (#8726)
* Kada je način pregleda uključen u Microsoft excelu i kada se prebacujete između načina pregleda i obratno, status načina pregleda se sada izgovara u skladu sa stvarnim stanjem. (#8846)
* NVDA sada pravilno izzgovara redak pod kursorom u  Notepad++ i drugim Scintilla uređivačima teksta. (#5450)
* U Google Docs (i drugim web baziranim uređivačima teksta), brajica više ne pokazuje sporadično "kr pop" ispred kursora usred stavke popisa. (#9477)
* U Windows 10 nadogradnji za svibanj 2019, NVDA više ne izgovara puno obavijesti o smanjivanju ili povećavanju glasnoće ako se glasnoća mjenja sa hardverskim gumbima kada upravitelj za datoteke je u fokusu. (#9466)
* Pokretanje dijaloškog okvira izgovora simbola i interpunkcije sada je puno brže kada se koriste rječnici simbola koji sadrže preko 1000 zapisa. (#8790)
* U Scintilla kontrolama kao što je to Notepad++, NVDA može sada čitati točan broj retka kada je rastavljanje riječi uključeno. (#9424)
* U Microsoft Excelu, izgovara se pozicija ćelije kada se ista promjeni zbog prečaca shift+enter ili shift+numEnter. (#9499)
* U Visual Studio 2017 novijim, u pregledniku objekata, označena stavka u drvu objekta ili drvu članova sa kategorijama sada se izgovara točno. (#9311)
* Nazivi dodataka koji se razlikuju samo u velikom slovu više se ne tretiraju kao zasebni dodaci. (#9334)
* Za Windows OneCore glasove, brzina koja se postavi u NVDA više ne utjeće na brzinu u Windows 10 uppostavkama govora. (#7498)
* Zapisnik se sada može otvoriti uz pomoć prečaca NVDA+F1 kada ne postoji informacija za razvojne programere za trenutni objekt navigatora. (#8613)
* Sada je opet moguće koristiti NVDA prečace za navigaciju po tablicama u Google Docs, u Firefoxu i Chromeu. (#9494)
* Bumper tipke sada rade ispravno na Freedom Scientific brajičnim recima. (#8849)
* HTCom se sada može koristiti u kombinaciji sa HandyTech brajičnim retcima i NVDA. (#9691)
* U Mozilla Firefoxu, nadogradnje živih regija se ne izgovaraju ako je živa regija u pozadinskoj kartici. (#1318)
* NVDA dijaloški okvir traženja u načinu pregleda više ne odbija poslušnost ako je otvoren dijaloški okvir "o NVDA" u pozadini. (#8566)

### Changes for Developers

* You can now set the "disableBrowseModeByDefault" property on app modules to leave browse mode off by default. (#8846)
* The extended window style of a window is now exposed using the `extendedWindowStyle` property on Window objects and their derivatives. (#9136)
* Updated comtypes package to 1.1.7. (#9440, #8522)
* When using the report module info command, the order of information has changed to present the module first. (#7338)
* Added an example to demonstrate using nvdaControllerClient.dll from C#. (#9600)
* Added a new isWin10 function to the winVersion module which returns whether or not this copy of NVDA is running on (at least) the supplied release version of Windows 10 (such as 1903). (#9761)
* The NVDA Python console now  contains more useful modules in its namespace (such as appModules, globalPlugins, config and textInfos). (#9789)
* The result of the last executed command in the NVDA Python console is now accessible from the _ (line) variable. (#9782)
 * Note that this shadows the gettext translation function also called "_". To access the translation function: del _
 
## 2019.1.1

This point release fixes the following bugs:

* NVDA no longer causes Excel 2007 to crash or refuses to report if a cell has a formula. (#9431)
* Google Chrome no longer crashes when interacting with certain listboxes. (#9364)
* An issue has been fixed which prevented copying a users configuration to the system configuration profile. (#9448)
* In Microsoft Excel, NVDA again uses the localized message when reporting the location of merged cells. (#9471)

## 2019.1

Novosti u ovoj inačici uključuju unapređene performanse u pristupu Microsoft Wordu i Excelu, Poboljšanja u stabilnosti i sigurnosti poput dodataka sa informacijama o inačici, I mnogo drugih ispravaka grešaka.

Imajte na umu, da od ove inačice NVDA, Prilagođeni moduli aplikacija, upravljački programi za brajične retke, te upravljački programi govornih jedinica više se neće pokretati iz vaše mape korisničkih postavki NVDA. 
Isti bi se trebali umjesto načina iznad, instalirati kao NVDA dodaci. Za one, koji razvijaju kod za dodatak, Kod se može razmjestiti u Pješčanik za razvojne programere, specijalnu mapu u mapi NVDA konfiguracije, ako je uključena opcija NVDA scratchpad u naprednom panelu NVDA postavki.
Ove su izmjene nužne, kako NVDA ne bi prestao raditi kada taj novi kod postane nekompatibilan.
Molimo pogledajte izmjene ispod za informacije, kako su bolje označene inačice dodataka.

### Nove značajke

* Nove brajične tablice: Afrikanerski, Arapska kompjutorska brajica, Arapski kratkopis, Španjolski kratkopis. (#4435, #9186)
* Dodana opcija U NVDA postavke miša, koja omogućava kontroliranje aplikacija uz pomoć miša. (#8452) 
 * To će omogućiti kontrolu nad udaljenim računalom uz pomoć aplikacija kao što je to Team viewer.
* Dodana postavka naredbenog retka `--enable-start-on-logon` koja omogućuje tihu instalaciju NVDA sa uključenom ili isključenom podrškom za sigurne zaslone. Ako želite da se poslije tihe instalacije NVDA pokreće na zaslonu za prijavu dodajte argument true  ili false ako ne želite da se pokreće na zaslonima za prijavu. Ako --enable-start-on-logon argument nije specificiran NVDA će se pokretati na zaslonu za prijavu, osim ako u prijašnjoj instalaciji isti nije tako konfiguriran. (#8574)
* Sada je moguće isključiti značajku zapisivanja dnevnika NVDA tako da se razina zapisivanja postavi na "onemogućeno" iz panele općenitih postavki. (#8516)
* Prisutstvo formula u LibreOfficeu i Apache OpenOffice proračunskim tablicama sada se izgovara. (#860)
* U Mozilla firefoxu i Google Chromeu, sada izgovara označeni element u popisima i stablima popisa.
 * Ovo radi u Firefoxu 66 i novijem.
 * Ovo ne radi za neke popise (HTML kontrole označavanja) u Chromeu.
* Rana podrška za aplikacije poput Mozilla Firefoxa na računalima sa ARM64 arhitekturom (na primjer, Qualcomm snapdragon) procesorima. (#9216)
* Nova kategorija naprednih postavki je dodana u NVDA dijaloški okvir postavki, uključujući opciju, koja omogućava isprobavanje pristupa do Word dokumenata uz pomoć Microsoft UI Automation API'ja. (#9200)
* Dodana podrška za grafički pregled u Windows upravljanju diskovima. (#1486)
* Dodana podrška za Handy Tech Connect Braille i Basic Braille 84. (#9249)

### Izmjene

* Nadograđen liblouis brajični prevoditelj na inačicu 3.8.0. (#9013)
* Autori NVDA dodataka sada mogu specificirati minimalnu NVDA inačicu na kojoj će se njihovi dodaci pokretati. NVDA će odbiti pokrenuti ili instalirati dodatak, u čijoj je specifikaciji NVDA inačica viša od predviđene. (#6275)
* Autori dodataka mogu specificirati zadnju testiranu NVDA inačicu u svojim dodacima. Ako je NVDA dodatak testiran sa nižom NVDA inačicom, u tom će trenutku NVDA odbiti instalaciju ili pokretanje dodatka. (#6275)
* Ova će inačica NVDA dopuštati instalaciju i pokretanje NVDA dodataka  koji ne sadrže informacije o minimalnoj i posljednjoj testiranoj inačici ali nadogradnja na novu inačicu NVDA NPR. 2019.2 može izmjeniti tu situaciju.
* Komanda "premjesti miš na objekt navigatora" je dostupna u Microsoft Wordu, kao i u drugim UIA kontrolama, osobito u Microsoft edteu. (#7916, #8371)
* Izvještavanje o tekstu pod mišem radi u Microsoft edgeu i drugim UIA aplikacijama. (#8370)
* Kada je NVDA pokrenut s parametrom naredbenog retka `--portable-path`, dodani put se popunjava prilikom stvaranja prijenosne kopije koristeći NVDA izbornik. (#8623)
* Osvježen put do Norveške kompjutorske brajične tablice, kako bi ista bila aktualna sa standardom iz 2015. godine. (#9170)
* Prilikom kretanja po odlomcima (ctrl+strelica gore ili dolje) ili prilikom kretanja po ćelijama tablice (ctrl+alt+strelice), postojanje pravopisnih grešaka više neće biti najavljivano, pa čak ako je NVDA podešena da iste automatski izgovara. Ovo je zato što odlomci i tablice mogu biti veliki, i otkrivanje pravopisnih grešaka može usporavati rad. (#9217)
* NVDA više ne pokreće prilagođene module aplikacija, globalne dodatke i upravljačke programe brajičnih redaka i govornih jedinica iz mape postavki NVDA. Umjesto toga, taj kod mora biti pakiran kao NVDA dodatak sa ispravnom informacijom o inačici, osiguravajući da se nekompatibilan kod neće pokretati sa trenutnom inačicom NVDA. (#9238)
 * Za razvojne programere koji trebaju testirati kod za vrijeme njegova razvoja,  omogućite mapu bilježnica NVDA razvojnog programera u NVDA postavkama , i kopirajte vaš kod u mapu 'scratchpad' koja se nalazi u NVDA mapi postavki kada je ista uključena.

### Ispravci grešaka

* Prilikom korištenja glasova OneCore u Windowsima 10, nadogradnji za travanj 2018 i novijim, velike pauze se više ne umeću između izričaja. (#8985)
* Prilikom kretanja po znakovima u kontrolama čistog teksta poput bloka za pisanje, ili načinu pregleda, 32'bitni znakovi koji se sastoje od dve kodne točke u utf-16 (poput ðŸ¤¦) sada će se čitati ispravno. (#8782)
* Unapređen dijaloški okvir potvrde o ponovnom pokretanju prilikom promjene jezika. Oznake i gumbi su sada kraći i manje zbunjujući. (#6416)
* Ako se sintetizator treće strane ne uspije pokrenuti, NVDA će se vratiti na Windows OneCore sintetizator govora na windowsima 10, umjesto na Espeak. (#9025)
* Uklonjen upis "dijaloškog okvira dobrodošlice", u NVDA izborniku, kada je NVDA pokrenut na sigurnim zaslonima. (#8520)
* Prilikom tabanja ili korištenja načina pregleda, legende na karticama svojstva sada se dosljednije izgovaraju. (#709)
* NVDA će sada izgovarati izmjene u odabiru za većinu kontrola odabira vremena kao što su to Alarm i sat u Windowsima 10. (#5231)
* U akcijskom centru Windowsa 10, NVDA će izgovarati poruke prilikom uključivanja svjetline zaslona ili focus assist. (#8954)
* U akcijskom centru u Windowsima 10 nadogradnji za listopad 2018 i ranijim, NVDA će prepoznavati gumb svjetline poput gumba umjesto preklopnog gumba. (#8845)
* NVDA će ponovno slijediti pokazivač i izvještavati o izmjenama u Micosoft excel poljima "idi na", i "traži". (#9042)
* Ispravljeno rijetko rušenje u Načinu pregleda u Firefoxu. (#9152)
* NVDA više ne neuspjeva izgovarati neke kontrole u Ribbonima u Microsoft Officeu 2016, kada su isti skupljeni.
* NVDA više ne neuspjeva izgovarati predložene kontakte u  prilikom upisivanje adrese u novim porukama u Outlooku 2016. (#8502)
* Zadnjih nekoliko kursorskih Routing tipki na 80 znakovnim eurobraille brajičnim recima više ne usmjeravaju redak na početak retka ili usred početka retka. (#9160)
* Ispravljena navigacija po tablici u pregledu razgovora u Mozilla Thunderbirdu. (#8396)
* U Mozilla Firefoxu i Google Chromeu, prebacivanje sada radi za većinu popisa i prikaza stabla (kada popis ili drvo nije fokusirajuće ali elementi istih jesu) . (#3573, #9157)
* Način pregleda sada je podrazumijevano uključen pri čitanju poruka u Outlooku 2016/365 kada se koristi Automatska podrška za UIA u Microsoft word dokumentima. (#9188)
* NVDA sada će se rijetko zamrzavati na način koji podrazumijeva samo odjavu iz vaše korisničke sesije. (#6291)
* U Windowsima 10 nadogradnji za listopad 2018 i novijim, prilikom otvaranja oblačnog međuspremnika sa praznim međuspremnikom, NVDA će izgovoriti stanje međuspremnika. (#9103)
* U Windowsima 10 nadogranji za listopad i novijim, prilikom traženja emoji u panelu za emoji, NVDA će izgovarati prvi rezultat pretrage. (#9105)
* NVDA se više ne smrzava u glavnom prozoru Oracle VirtualBox 5.2 i novijima. (#9202)
* Ispravljene performanse u Microsoft excelu  pri kretanju po ćelijama. Podsjetnik: poslje pokretanja Microsoft Worda u dokumentu, isti postavite na izgled predloška. (#9217) 
* U mozilla Firefoxu i Google chromeu, prazne obavjesti se više ne čitaju. (#5657)
* Značajna ubrzanja pri kretanju po ćelijama u Microsoft excelu, osobito u radnim knjigama koje sadrže komentare ili validacijske popise. (#7348)
* Više ne bi smjelo biti potreno isključivati opciju unutarćelijskog uređivanja u opcijama Mocrosoft officea 2016/365, ako se želi uređivati pojedinačna ćelija. (#8146).
* ispravljeno zamrzavanje u Firefoxu ponekad viđeno pri navigaciji po orjentirima, ako se koristi dodatak Enhanced aria. (#8980)

### Changes for Developers

* NVDA can now  be built with all editions of Microsoft Visual Studio 2017 (not just the Community edition). (#8939)
* You can now include log output from liblouis into the NVDA log by setting the louis boolean flag in the debugLogging section of the NVDA configuration. (#4554)
* Add-on authors are now able to provide NVDA version compatibility information in add-on manifests. (#6275, #9055)
 * minimumNVDAVersion: The minimum required version of NVDA for an add-on to work properly.
 * lastTestedNVDAVersion: The last version of NVDA an add-on has been tested with.
* OffsetsTextInfo objects can now implement the _getBoundingRectFromOffset method to allow retrieval of bounding rectangles per characters instead of points. (#8572)
* Added a boundingRect property to TextInfo objects to retrieve the bounding rectangle of a range of text. (#8371)
* Properties and methods within classes can now be marked as abstract in NVDA. These classes will raise an error if instantiated. (#8294, #8652, #8658)
* NVDA can log the time since input when text is spoken, which helps in measuring perceived responsiveness. This can be enabled by setting the timeSinceInput setting to True in the debugLog section of the NVDA configuration. (#9167)

## 2018.4.1

Ova inačica NVDA ispravlja rušenje pri pokretanju, kada je jezik NVDA postavljen na aragonski. (#9089)

## 2018.4

Novosti u ovoj inačici uključuju poboljšanja performansi u zadnjim inačicama Mozilla firefox-a, izgovor emoji sa svim govornim jedinicama, čitanje statusa poruke (prosljeđeno/odgovoreno), u Outlook-u, čitanje udaljenosti od ruba stranice od pokazivača u Microsoft Wordu, te puno ispravaka grešaka.

### Nove značajke

* Nove brajične tablice: Kineski (Kina, Mandarinski) s tonovima i bez tonova. (#5553)
* U popisu poruka, sada se izgovara status poruke odgovoren/proslijeđen. (#6911)
* NVDA sada može čitati opise znakova poput emoji, kao i druge znakove koji su dio općeg Unicode repozitorija znakova. (#6523)
* U Microsoft Wordu, udaljenost kursora od lijevog i gornjeg ruba stranice može se čitati uz pomoć tipkovničkog prečaca insert+delete. (#1939)
* U Google Sheets sa uključenim brajičnim načinom, NVDA više ne izgovara 'označeno' na svakoj ćeliji prilikom pomicanja fokusa. (#8879)
* Dodana podrška za Foxit Reader i Foxit Phantom PDF (#8944)
* Dodana podrška za DBeaver alat za baze podataka. (#8905)

### Izmjene

* Opcija "izvijesti o pomoćnim balončićima" u dijaloškom okviru prezentacija objekta preimenovana je "izgovaraj obavijesti" kako bi uključivala obavijesti u windowsima 8 i novijim. (#5789)
* U NVDA postavkama tipkovnice, potvrdni okviri za izbor NVDA modifikacijskih tipki sada su prikazani u jednom popisu umjesto odvojenog prikaza.
* NVDA više neće prikazivati izlišne informacije pri prikazivanju sata u nekim inačicama Windowsa. (#4364)
* Nadograđen liblouis brajični prevoditelj na inačicu 3.7.0. (#8697)
* Nadograđen eSpeak-NG na commit 919f3240cbb

### Ispravke grešaka

* U Outlooku 2016/365, kategorija i status zastavice sada se izgovaraju za poruke. (#8603)
* Kada je NVDA postavljen na jezike kao što su to  Kirgizijski, Mongolski ili Makedonski, više se ne pojavljuje upozorenje o nepodržanosti jezika od strane operativnog sustava. (#8064)
* Pomičući miš, sada će se isti pomicati točnije u poziciju načina fokusa u Mozilla Firefoxu, Google Chromeu i Acrobat Reader DC. (#6460)
* Interakcija sa odabirnim okvirima na web stranicama u  Firefoxu, Chromeu i Internet Exploreru je poboljšana. (#8664)
* Ako se NVDA pokreće na Japanskoj inačici Windowsa XP ili Viste, upozorenje o nekompatibilnosti sada se prikazuje kako valja. (#8771)
* Povećanje performansi u Mozilla Firefoxu prilikom kretanja po velikim web stranicama sa puno dinamičkog sadržaja. (#8678)
* Karakteristike fonta se više ne pokazuju na brajičnom retku,  ako su iste onemogućene u postavkama oblikovanja dokumenta. (#7615)
* NVDA sada uspjeva pratiti fokus u upravitelju datoteka i drugim aplikacijama koje koriste UI Automation prilikom zauzetosti aplikacije (kao što je to simultana obrada zvuka). (#7345)
* U ARIA izbornicima na webu, tipka escape će biti proslijeđena izborniku kao kontroli i neće više isključivati način fokusa. (#3215)
* U novom Gmailu, kada se koriste tipke brze navigacije u porukama prilikom čitanja, čitavo tijepo poruke više se ne čita poslije elementa do kojeg ste došli. (#8887)
* Poslije nadogradnje NVDA, Preglednici poput Firefoxa i google Chromea više se ne bi trebali rušiti, i način pregleda će ponovo prikazivati osvježavanja u svakom trenutno učitanom dokumentu. (#7641) 
* Prilikom kretanja po klikabilnom sadržaju u načinu pregleda, NVDA više ne čita "klikajući", više puta u jednom retku. (#7430)
* Komande koje su pritisnute na baum Vario 40 brajičnim retcima sada će se normalno izvoditi. (#8894)
* U Google Prezentacijama kada se koristi Mozilla Firefox, NVDA više ne izgovara označeni tekst pri pomicanju na svaku kontrolu fokusa. (#8964)

### Changes for Developers

* gui.nvdaControls now contains two classes to create accessible lists with check boxes. (#7325)
 * CustomCheckListBox is an accessible subclass of wx.CheckListBox.
 * AutoWidthColumnCheckListCtrl adds accessible check boxes to an AutoWidthColumnListCtrl, which itself is based on wx.ListCtrl.
* If you need to make a wx widget accessible which isn't already, it is possible to do so by using an instance of gui.accPropServer.IAccPropServer_impl. (#7491)
 * See the implementation of gui.nvdaControls.ListCtrlAccPropServer for more info.
* Updated configobj to 5.1.0dev commit 5b5de48a. (#4470)
* The config.post_configProfileSwitch action now takes the optional prevConf keyword argument, allowing handlers to take action based on differences between configuration before and after the profile switch. (#8758)

## 2018.3.2

Ovo je mala ispravka, koja ispravlja rušenje u Google Chromeu pri kretanju po tweetovima na [www.twitter.com](http://www.twitter.com). (#8777)

## 2018.3.1

Ovo je ispravka pogreške, koja je prouzrokovala rušenje NVDA, pri pokrenutom pregledniku Mozilla firefox u 32 bitnoj inačici. (#8759)

## 2018.3

Novosti u ovoj inačici uključuju automatsko otkrivanje nekoliko brajičnih redaka, podrška za nove značajke u Windowsima 10, uključujući emoji panel, te mnogo drugih ispravaka grešaka.

### Nove značajke

* NVDA će izvještavati o pravopisnim pogreškama, kada je to točno određeno u Mozilla Firefoxu i Google Chromeu. (#8280)
* Sadržaj koji je označen kao umetnut ili izbrisan na web stranicama sada se čita u Google Chromeu. (#8558)
* Dodana podrška za BrailleNote QT i Apex BT navigacijski kotačić kada se BrailleNote koristi kao brajični redak sa NVDA. (#5992, #5993)
* Dodann prečac za čitanjepreostalog i cjelokupnog vremena trenutne pjesme u Foobar2000. (#6596)
* Simbol Mac komandne tipke (⌘) sada se čita sa bilo kojim sintetizatorom govora prilikom čitanja teksta. (#8366)
* Prilagođene uloge preko aria-roledescription atributa sada su podržane u svim web preglednicima. (#8448)
* Nove brajične tablice: Češki osmotočkasta brajica, Centralni Kurdski, Esperanto, Mađarski, Švedski osmotočkasta kompjutorska brajica. (#8226, #8437)
* Dodana podrška za automatsko otkrivanje brajičnih redaka u pozadini. (#1271)
 * ALVA, Baum/HumanWare/APH/Orbit, Eurobraille, Handy Tech, Hims, SuperBraille i HumanWare BrailleNote i Brailliant BI/B brajični retci su trenutno podržani.
 * Ovu značajku možete uključiti ako da označite opciju automatski u spisku brajičnih redaka u NVDA dijaloškom okviru za odabir brajičnih redaka.
 * Za više informacija, molimo pročitajte korisnički priručnik.
* Dodana podrška za moderne značajke unosa u posljednjim inačicama Windows 10. Iste uključuju emoji panel (zimska nadogradnja za tvorce), diktiranje (zimska nadogradnja za tvorce), prijedlozi unosa na hardverskoj tipkovnici (nadogradnja za travanj 2018), i lijepljenje u oblačnom međuspremniku (nadogradnja za listopad 2018). (#7273)
* Sadržaj označen kao citat koristeći (role blockquote) sada je podržan u Mozilla Firefox 63. (#8577)

### Izmjene

* Spisak dostupnih jezika u NVDA općim postavkama, sada je sortiran po imenima jezika umjesto po iso639 kodovima. (#7284)
* Dodane podrazumijevane geste za Alt+Shift+Tab i Windows+Tab za sve podržane Freedom Scientific brajične redke. (#7387)
* Za ALVA BC680 i pretvornik protokola brajične redke, sada je moguće dodijeliti razne funkcije za lijevi i desni pametni pad, palčane te etouch tipke. (#8230)
* Za ALVA BC6 retke, kombinacija tipaka sp2+sp3 sada će izgovarati trenutni datum i vrijeme, gdje će sp1+sp2 oponašati windows tipku. (#8230)
* Korisnik će biti pitan, jednom kada se NVDA pokrene želi li slati povratne informacije u NV Access prilikom provjere NVDA nadogradnje. (#8217)
* Prilikom provjere nadogradnje, ako je korisnik pristao na slanje statistika u NV Access, NVDA će slati naziv trenutnog brajičnog retka i govorne jedinice, kako bi sam korisnik pomogao u razvoju tih komponenti. (#8217)
* Nadograđen liblouis brajični prevoditelj na inačicu 3.6.0. (#8365)
* Osvježen put do točne ruske osmotočkaste brajične tablice. (#8446)
* Nadograđen eSpeak-ng na 1.49.3dev commit 910f4c2. (#8561)

### Ispravke grešaka

* Dostupne oznake u Google Chromeu sada se isčitavaju u načinu pregleda, kada oznaka se ne pojavljuje kao sadržaj. (#4773)
* Obavijesti su podržane u Zoomu. Na primjer, to uključuje status utišavanja ili ottišavanja zvuka, te izgovaranje pristiglih poruka. (#7754)
* Prebacivanje brajične prezentacije konteksta kada se nalazi u načinu pregleda više ne prouzrokuje prekid izlaza u istom sa pozicije praćenja kursora. (#7741)
* ALVA BC680 brajični redci više ne neuspjevaju se inicijalizirati. (#8106)
* Podrazumijevano, ALVA BC6 brajični redci više ne pokreću tipke na emuliranoj sustavskoj tipkovnici  prilikom pritiska kombinacija koje uključuju sp2+sp3 kako bi se mogle pozivati unutrašnje funkcije. (#8230)
* pritisak sp2 na ALVA BC6 redku kako bi se emulirala tipka alt sada radi kako je i napisano. (#8360)
* NVDA više ne izgovara nepotrebne izmjene tipkovnice. (#7383, #8419)
* Praćenje miša sada je točnije u Notepadu i drugim poljima za uređivanje kada se nalazite u dokumentu koji sadrži više od 65535 znakova. (#8397)
* NVDA će prepoznavati više dijaloških okvira u Windowsima 10 i drugim modernim aplikacijama. (#8405)
* U Windowsima 10 nadogradnji za listopad 2018 te Server 2019 i novijim, NVDA više ne ne uspjeva pratiti fokus sustava kada se program zamrzne ili zablokira sustav sa događajima. (#7345, #8535)
* Korisnik je sada informiran porukom o nemogučnosti kopiranja prazne statusne trake. (#7789)
* Ispravljena pogreška u kojoj stanje "nije označeno" na kontrolama nije izgovoreno govorom ako je ista bila polovično odabrana. (#6946)
* U popisu jezika u NVDA općim postavkama, naziv jezika za burmeški sada se ispravno prikazuje u Windowsima 7. (#8544)
* U Microsoft Edgeu, NVDA će izgovarati obavijesti poput čidostupnog pregleda čitanja te stanja učitavanja stranice. (#8423)
* Pri navigaciji lista na stranici, NVDA će izgovoriti oznaku ako je autor dao istu. (#7652)
* Prilikom pridjeljivanja gesti funkcijama na određenom brajičnom redku, sada se prikazuju kao geste pridjeljene tom brajičnom redku. U prijašnjem stanju, iste su se pokazivale kao geste koje su bile pripisane aktivnom brajičnom redku. (#8108)
* 64-bitna inačica Media Player Classic sada je podržana. (#6066)
* Nekoliko poboljšanja u brajičnoj podršci za Microsoft Word sa uključenim UI Automation:
 * Slično kao u drugim tekstualnim poljima sa više redaka, kada ste pozicionirani na početku dokumenta pomiću brajice, Prvi je znak pozicioniran tako da se nalazi na početku samog brajičnog retka. (#8406)
 * Smanjena prevelika govorna prezentacija fokusa pri otvaranju Wordovih dokumenata. (#8407)
 * Routing tipke sadda ponovno rade u Word dokumentima kada se nalazite u spisku nabrajanja. (#7971)
 * Novoumetnute točkice ili brojevi sada se točno izgovaraju ili prenose u brajicu. (#7970)
* U Windowsima 10 1803 i novijim, sada je moguće instalirati dodatke, ako je značajka "koristi unicode UTF'8 za međunarodnu jezičnu podršku" uključena. (#8599)

### Changes for Developers

* Added scriptHandler.script, which can function as a decorator for scripts on scriptable objects. (#6266)
* A system test framework has been introduced for NVDA. (#708)
* Some changes have been made to the hwPortUtils module: (#1271)
 * listUsbDevices now yields dictionaries with device information including hardwareID and devicePath.
 * Dictionaries yielded by listComPorts now also contain a usbID entry for COM ports with USB VID/PID information in their hardware ID.
* Updated wxPython to 4.0.3. (#7077)
* As NVDA now only supports Windows 7 SP1 and later, the key "minWindowsVersion" used to check if UIA should be enabled for a particular release of Windows has been removed. (#8422)
* You can now register to be notified about configuration saves/reset actions via new config.pre_configSave, config.post_configSave, config.pre_configReset, and config.post_configReset actions. (#7598)
 * config.pre_configSave is used to be notified when NVDA's configuration is about to be saved, and config.post_configSave is called after configuration has been saved.
 * config.pre_configReset and config.post_configReset includes a factory defaults flag to specify if settings are reloaded from disk (false) or reset to defaults (true).
* config.configProfileSwitch has been renamed to config.post_configProfileSwitch to reflect the fact that this action is called after profile switch takes place. (#7598)
* UI Automation interfaces updated to Windows 10 October 2018 Update and Server 2019 (IUIAutomation6 / IUIAutomationElement9). (#8473)

## 2018.2.1

This release includes translation updates due to last-minute removal of a feature which caused problems.

## 2018.2

Novosti u ovoj inačici uključuju Podršku tablica u Kindle za osobna računala, podršku za Humanware Braillenote touch i BI14 Braille brajične retke, unapređenja za OneCore, kao i za sapi5 govorne jedinice, unapređenja u outlooku, i još puno toga.

### Nove značajke

* Širina redka i dužina stupca sada se mogu isčitati uz pomić govora i brajice. (#2642)
* NVDA prečaci za navigaciju u tablicama sada su podržani u  Google Dokumentima (sa uključenim brajičnim načinom). (#7946)
* Mogućnost navigacije po tablicama u Kindleu za osobna računala. (#7977)
* Podrška za BrailleNote touch i Brailliant BI 14 brajične retke preko USB i bluetooth veze. (#6524)
* U Windows 10 zimskoj nadogradnji za tvorce i novijim, NVDA može izgovarati obavijesti iz aplikacija kao što je to KalKulator i Windows Store. (#8045)
* Nove brajične tablice: litavska osmotočkasta, Ukrajinska, Mongolska sa podrškom engleskog kratkopisa. (#7839)
* Dodana skripta za izvještavanje o oblikovanju za tekst koji se nalazi ispod određene brajične ćelije. (#7106)
* Prilikom nadograđivanja NVDA, sada je moguće odgoditi instalaciju nadogradnje za kasnije vrijeme po vašem izboru. (#4263) 
* Novi jezici: Mongolski, Švicarski njemački.
* Sada možete uključivati ili isključivati control, shift, alt, windows i NVDA tipke sa vaše brajične tipkovnice te ih je moguće kombinirati uz brajični ulaz (e.g. press control+s). (#7306) 
 * Možete dodijeliti te modifikatore  koje možete pronaći u kategoriji emulirane tipke sustava u dijaloškom okviru ulazne geste.
* Vraćena podrška za Handy Tech Braillino i Modular brajične retke (sa starim firmwareom). (#8016)
* Datum i vrijeme za podržane Handy Techove uređaje (poput Active Braille i Active Star) će biti automatski sinkronizirano kada nije sinkronizirano više od 5 sekundi. (#8016)
* Sada se može pridijeliti gesta, koja služi za privremeno omogućavanje svih konfiguracijskih profila. (#4935)

### Izmjene

* Stupac statusa je promijenjen tako da će pokazivati je li dodatak omogućen ili onemogućen puno bolje od prijašnjeg obavještenja pokrenut ili suspendiran. (#7929)
* Nadograđen liblouis brajični prevoditelj na inačicu 3.5.0. (#7839)
* Preimenovana je Litavska brajična tablica te sada se zove litavska šestotočkasta, kako bi se izbjegla zbrka sa litavskom osmotočkastom tablicom. (#7839)
* Kanadske francuske brajične tablice su sada uklonjene. Sada će se umjesto kanadskih tablica, koristiti šestotočkasta, te unificirani francuski kratkopis. (#7839)
* Sekundarne routing tipke na Alva BC6, EuroBraille i Papenmeier brajičnim retcima sada izvještavaju o formatiranju teksta pritiskom na routing tipku nad brajičnom ćelijom. (#7106)
* Kratkopisne brajične ulazne tablice vratit će se u punopisni način u slučajevima, kada nije moguće uređivati tekst (npr. pri kontrolama gdje kursor ne postoji ili u načinu pregleda). (#7306)
* NVDA je sada manje pričljiv kada kalendarski termin pokriva cijeli dan. (#7949)
* Sve postavke NVDA sada se nalaze u jednom dijaloškom okviru postavke u istoimenom podizborniku, što znači da dijalozi više nisu raspršeni. (#7302)
* Podrazumijevani sintetizator govora sada je one core, bolje nego espeak. (#8176)

### ispravke grešaka

* NVDA sada uspijeva pročitati fokusirane kontrole u zaslonu za prijavu Microsoft naloga u postavkama poslije upisivanja e-mail adrese. (#7997)
* NVDA sada uspijeva pročitati stranicu kada se vraćate na prethodnu stranicu u  Microsoft Edge. (#7997)
* NVDA više neće pogrešno izgovarati zadnji znak windows 10 pina za prijavu kada se računalo otključava. (#7908)
* Oznake odabirnih okvira i izbornih gumba u Chromeu i Firefoxu više se ne izgovaraju dva put prilikom pritiska tipke tab ili pomicanjem sa strelicama. (#7960)
* Rukovanje aria-current sa vrijednošću false kao false umjesto true (#7892).
* Windows Onecore glasovi više se ne pokreću s greškom ako je prethodni glas bio uklonjem. (#7999)
* Izmjena glasova u Windows Onecore glasovima sada je puno brža. (#7999)
* Ispravljen izobličen brajični prikaz u nekim brajičnim tablicama, uključujući znakove za velika slova u danskom osmotočkastom kratkopisu. (#7526, #7693)
* NVDA sada može izgovarati više vrsta znakova za nabrajanje u Microsoft Wordu. (#6778)
* Pritiskom prečaca za izvještavanje formatiranja više ne premještava reviewPosition te također kada se pritisne više puta, ne nosi neželjene rezultate. (#7869)
* Brajični ulaz više ne dozvoljava korištenje kratkopisa u slučajevima u kojima isti nije podržan (NPR. cijele riječi neće biti poslane u sustav izvan tekstualnog sadržaja te u načinu pregleda). (#7306)
* Ispravljene nestabilnosti u povezivanju za Handy Tech Easy Braille i Braille Wave brajične retke. (#8016)
* U Windowsima 8 i novijim, NVDA više neće izgovarati "nepoznato" prilikom otvaranja izbornika brzog povezivanja )Windows+X) i označavanju stavaka iz tog izbornika. (#8137)
* Specifične geste za modele Na Himsovim retcima sada rade onako, kako su opisane u korisničkom priručniku. (#8096)
* NVDA će sada pokušati ispraviti greške povezane sa sistemskom COM registracijom koje su prouzrokovale da Internet explorer i firefox postanu nepristupačni, pri tom izgovarajući "nepoznato". (#2807)
* Ispravljena greška u upravitelju zadataka, koja je onemogućavala prikaz detaljnog prikaza zadataka. (#8147)
* Noviji Microsoft sapi5 glasovi više ne zaostaju na kraju izgovorene riječi, što ih čini brzim pri kretanju. (#8174)
* NVDA više niti ne izgovara, niti ne prikazuje (LTR i RTL znakove) prilikom pristupanja satu u windowsima 10. (#5729)
* Otkrivanje tipki za pomicanje na Hims Smart Beetle brajičnim retcima sada više nije nepouzdano. (#6086)
* U nekim tekstnim kontrolama, pogotovo u delphi aplikacijama, informacije koje su dane prilikom uređivanja ili kretanja sada su pouzdanije. (#636, #8102)
* U Windowsima 10 RS5, NVDA više ne izgovara suvišne informacije pri prebacivanju aplikacija uz pomoč alt+tab. (#8258)

### Changes for developers

* The developer info for UIA objects now contains a list of the UIA patterns available. (#5712)
* App modules can now force certain windows to always use UIA by implementing the isGoodUIAWindow method. (#7961)
* The hidden boolean flag "outputPass1Only" in the braille section of the configuration has again been removed. Liblouis no longer supports pass 1 only output. (#7839)

## 2018.1.1

Ovo je specijalna stabilna inačica NVDA koja otklanja grešku u OneCore Windows sintetizatoru govora, koja je prouzrokovala da isto govori sa povišenim glasom i povišenom brzinom u Windows 10 Redstone 4 (1803). (#8082)  

## 2018.1

Novosti u ovoj inačici uključuju podršku grafova u Microsoft wordu i Powerpointu, novopodržani brajični retci: Eurobraille i Optelec protocol converter, unapređena podrška za Hims i Optelec brajične retke, poboljšanje performansi u Mozilla Firefox 58 i novijim, i puno više.

### Nove značajke

* Sada je moguće ulaziti u interakciju sa grafovima u Microsoft Wordu i Microsoft PowerPointu, slično kao i kod podrške grafova u Microsoft Excelu. (#7046)
 * U Microsoft Wordu:  kada se nalazite u načinu pregleda, kursorom dođite do grafa i pritisnite enter.
 * U Microsoft PowerPointu prilikom uređivanja slajda: pritišćite tabulator do objekta grafa, i pritisnite enter ili razmak kako biste ušli u interakciju s grafom.
 * Kako biste prestali biti u interakciji s grafom, Pritisnite escape.
* Novi jezik: kirgizki.
* Dodana podrška za VitalSource Bookshelf čitač elektronskih knjiga. (#7155)
* Dodana podrška za Optelec pretvarač protokola, Uređaj koji omogućava korištenje Alvinih Voyager i Satellite brajičnih redaka koristeći noviji ALVA BC6 protokol. (#6731)
* Sada je moguće koristiti brajični unos teksta sa brajičnim retkom ALVA 640 Comfort. (#7733) 
 * NVDA brajični unos može se koristiti sa istim brajičnim retcima, kao i sa  BC6 sa firmware-om 3.0.0 ili novijim.
* Rana podrška za Google Sheets sa uključenim brajičnim načinom. (#7935)
* Podrška za Eurobraille Esys, Esytime i Iris brajične retke. (#7488)

### Izmjene

* upravljački programi za HIMS Braille Sense/Braille EDGE/Smart Beetle i Hims Sync sada su zamijenjeni jednim upravljačkim programom. Ovaj upravljački program bit će automatski aktiviran za stare korisnike syncBraille upravljačkog programa. (#7459) 
 * Neke tipke, točnije tipke za premještanje po redovima su izmijenjene, kako bi pratile konvencije Himsovih proizvoda. Za više detalja, pročitajte vodič za korisnike.
* Prilikom tipkanja na zaslonskoj tipkovnici sa uključenom dodirnom interakcijom, podrazumjevano trebate svaku tipku stisnuti dva puta, kao što aktivirate i druge kontrole. (#7309)
 * Kako biste koristili postojeći način dodirnog unosa, gdje je jedan dodir dovoljan za aktivaciju pojedinačne tipke, omogućite tu opciju u dijaloškom okviru dodirna interakcija kojeg možete naći u izborniku postavke.
* Više nije potrebno ručno prebacivati brajicu na fokus ili pregled, jer će se to događati automatski. (#2385) 
 * imajte na umu, da će se prebacivanje na pregled događati samo kada se koristi pregledni kursor ili prečac objektne navigacije. pomicanje po redovima neće aktivirati ovakav način.

### Ispravke grešaka

* pregledne poruke poput izgovora formatiranja pri pritisku NVDA+f dva puta brzo više neće rezultirati pogreškom, kada je NVDA instaliran na sustavu sa nelatiničnim znakovima. (#7474)
* Fokus se sada vraća ispravno, prilikom vraćanja u Spotify iz drugih aplikacija. (#7689)
* U Windows 10 jesenskoj nadogradnji za tvorce, NVDA će se sada uspjevati nadograditi, kada je uključena opcija kontroliranog pristupa folderima u Windows defenderu. (#7696)
* otkrivanje tipaka za pomicanje napred ' nazad po redku kod hims brajičnih redaka sada više nije nestabilno. (#6086)
* Malo poboljšanje performansi prilikom učitavanja velikog sadržaja u Mozilla Firefox 58 i novijim. (#7719)
* U Microsoft Outlooku, čitanje e-mailova koji sadrže tablice, više ne prouzrokuje greške. (#6827)
* geste brajičnog redka koje emuliraju modifikatore tipki sustava mogu biti kombinirane sa drugim tipkama sustava ako jedna ili više uključenih gesti ovise o modelu. (#7783)
* U Mozilla Firefoxu, način pregleda sada ponovno radi u iskočnim prozorima dodataka poput LastPass i bitwarden. (#7809)
* NVDA se više ne smrzava na svakoj promijeni fokusa u mozilla firefox i chrome preglednicima poput smrzavanja ili rušenja. (#7818)
* U twitter klijentima poput Chicken Nuggeta, NVDA više neće ignorirati zadnjih 20 znakova od 280 znakovnog tweeta prilikom čitanja istog. (#7828)
* NVDA sada koristi ispravan jezik pri označavanju teksta. (#7687)
* U posljednjim inačicama Office 365, sada je moguće ponovo čitati excel grafove sa strelicama gore dole. (#7046)
-  Radi li se o brajičnom ili govornom izlazu, status i tip kontrole bit će predstavljen u istom poredku, neovisno je li pozitivan ili negativan. Ispravlja #7076
* u aplikacijama poput Windows 10 Pošte, NVDA će sada izgovarati izbrisane znakove pritiskom na backspace. (#7456)
* Sve tipke na Hims Braille Sense Polaris brajičnim retcima sada rade kako treba. (#7865)
* NVDA se sada uspješno pokreće na Windows 7 kada se prije pojavljivala greška o unutrašnjem api-ms dll, kada je u aplikaciji instalirana konkretna inačica Visual Studio 2017 redistributivnog paketa. (#7975)

### Changes for developers

* Added a hidden boolean flag to the braille section in the configuration: "outputPass1Only". (#7301, #7693, #7702) 
 * This flag defaults to true. If false, liblouis multi pass rules will be used for braille output.
* A new dictionary (braille.RENAMED_DRIVERS) has been added to allow for smooth transition for users using drivers that have been superseded by others. (#7459)
* Updated comtypes package to 1.1.3. (#7831)
* Implemented a generic system in braille.BrailleDisplayDriver to deal with displays which send confirmation/acknowledgement packets. See the handyTech braille display driver as an example. (#7590, #7721)
* A new "isAppX" variable in the config module can be used to detect if NVDA is running as a Windows Desktop Bridge Store app. (#7851)
* For document implementations such as NVDAObjects or browseMode that have a textInfo, there is now a new documentBase.documentWithTableNavigation class that can be inherited from to gain standard table navigation scripts. Please refer to this class to see which helper methods must be provided by your implementation for table navigation to work. (#7849)
* The scons batch file now better handles when  Python 3 is also installed, making use of the launcher to specifically launch python 2.7 32 bit. (#7541)
* hwIo.Hid now takes an additional parameter exclusive, which defaults to True. If set to False, other applications are allowed to communicate with a device while it is connected to NVDA. (#7859)

## 2017.4

Novosti u ovoj inačici uključuju poboljšanja u web podršci, uključujući podrazumijevani način pregleda za web dijaloge bolje izgovaranje grupa polja u načinu pregleda, Podrška za nove Windows 10 tehnologije Windows 10 zaštitnik aplikacija i windows 10 za ARM64, te automatsko čitanje statusa baterije i orijentacije ekrana.  
Imajte na umu, da ova inačica NVDA ne podržava windows xp ili Windows Vistu. Minimalna podržana inačica operativnog sustava windows je windows 7 sa servisnim paketom 1.

### Nove značajke

* U načinu pregleda, sada je moguće preskakati orjentire koristeći prečac prebacivanja između sadrživaća (zarez/shift+zarez). (#5482)
* U Firefoxu, Chromeu i u Internet Exploreru, brza navigacija do uređivačkih polja i obrazaca sada uključuje tekstualna polja bogatog uređivanja (NPR. contentEditable). (#5534)
* U internet preglednicima, popis elemenata može izlistavati obrasce i gumbe. (#588)
* Prvobitna podrška za Windows 10 na ARM64 platformama. (#7508)
* Rana podrška za čitanje i kretanje po matematičkom sadržaju za Kindle knjige sa pristupačnom matematikom. (#7536)
* Dodana podrška za Azardi čitač elektronskih knjiga. (#5848)
* Prilikom ažuriranja dodataka, sada se izgovara i njihova inačica. (#5324)
* Dodani parametri naredbenog retka koji omogućuju stvaranje prijenosne inačice NVDA. (#6329)
* Podrška za Microsoft edge u windows zaštitniku aplikacija u Windows defenderu, koristeći windows 10 jesensko ažuriranje za tvorce. (#7600)
* Ako je pokrenut na prijenosnom ili tablet računalu, NVDA će sada izgovarati dali je punjač spojen ili odspojen, te promjenu položaja zaslona. (#4574, #4612)
* Novi jezik: Makedonski.
* Nove brajične tablice: Hrvatski puno pismo, Vijetnamski puno pismo. (#7518, #7565)
* Dodana podrška za Handy Tech Actilino brajični redak. (#7590)
* Sada je podržan unos znakova sa brajičnih tipkovnica Handytechovih brajičnih redaka. (#7590)

### Izmjene

* Minimalna podržana inačica operativnih sustava za NVDA sada je Windows 7 sa servisnim paketom 1, ili Windows Server 2008 R2 sa servisnim paketom 1. (#7546)
* Web dijaloški okviri u Firefox i Chrome web preglednicima sada automatski koriste način pregleda, osim ako to nije web aplikacija. (#4493)
* U načinu pregleda, pritiskanje tabulatora i kretanje prečicama za brzo kretanje ne izgovaraju prebacivanje izvan sadrživaća poput popisa i tablica, što čini kretanje bržim. (#2591)
* U načinu pregleda za Firefox i Chrome, Imena grupa polja obrazaca prilikom premještanja po njima sa prečicama za brzo kretanje ili prilikom pritiskanja taba. (#3321)
* U načinu pregleda, prečac za brzo kretanje po ugrađenim objektima (o i shift+o) sada uključuje audio i video playere, kao i elemente s aria atributima application i dialog. (#7239)
* Espeak-ng je nadograđen na inačicu 1.49.2, koja rješava probleme sa kompiliranjem novih verzija. (#7385, #7583)
* prilikom treće aktivacije prečaca 'čitaj statusnu traku', sadržaj izgovoren putem te komande je kopiran u međuspremnik. (#1785)
* Prilikom dodjele prečaca na Baumovom brajičnom redku, sada je moguče ograničiti iste za model na kojem se koriste (npr. VarioUltra ili Pronto). (#7517)
* tipkovni prečac u popisu elemenata u načinu pregleda promijenjen je sa  alt+f na kombinaciju alt+e. Bilješka prevoditelja: ovo ne važi za hrvatsku inačicu NVDA. (#7569)
* Dodana je nedodijeljena gesta koja omogućuje uključivanje / isključivanje tablica izgleda u letu. Ovu komandu možete pronaći u kategoriji način pregleda u dijaloškom okviru ulazne geste. (#7634)
* Nadograđen Liblouis brajični prevoditelj na inačicu 3.3.0. (#7565)
* Tipkovnički prečac za izborni gumb pravilni izrazi u dijaloškom okviru govorni rječnici je zamjenjen sa alt+r na alt+e. Bilješka prevoditelja: ovo ne vrijedi za hrvatsku inačicu čitača zaslona NVDA. (#6782)
* Datoteke glasovnih rječnika su sada verzijonirani i premještene su u mapu 'speechDicts/voiceDicts.v1'. (#7592)
* verzijonirane datoteke (user configuration, voice dictionaries) izmjene nisu spremljene u pokretaču. (#7688)
* Braillino, Bookworm i Modular Handy tech brajični retci (sa starim pogonskim softverom) više nisu podržani direktno. Koristite Handytechov univerzalni pogonski softver i NVDA dodatak kako biste mogli koristiti ove brajične retke s NVDA. (#7590)

### Ispravke grešaka

* Linkovi se sada ispravno prikazuju u aplikacijama poput Microsoft Worda. (#6780)
* NVDA više ne postaje značajno sporiji prilikom otvaranja više kartica u Firefox ili Chrome web preglednicima. (#3138)
* Routing tipka na MDV Lilli brajičnom retku više se ne pomiće neispravno za jednu brajičnu ćeliju u naprijed od one, na kojoj bi kursor trebao stajati. (#7469)
* U Internet Exploreru i drugim MSHTML dokumentima, HTML5 required atribut sada je podržan kako bi slao povratnu informaciju da je polje za upis obvezno. (#7321)
* Brajični retci se sada osvježuju prilikom upisivanja arapskih znakova u lijevo poravnatom WordPad dokumentu (#511).
* Pristupačne oznake za kontrole u Mozilla Firefoxu sada su više izgovarane u načinu pregleda kada oznaka nije prikazana kao sadržaj. (#4773)
* U windows 10 nadogradnji za tvorce, NVDA može ponovno pristupiti Firefoxu poslije ponovnog pokretanja NVDA. (#7269)
* Prilikom ponovnog pokretanja NVDA sa Mozilla Firefox u fokusu, način pregleda će ponovno biti dostupan, međutim, trebalo bi pritisnuti alt tab, da se prebaci na drugu aplikaciju, te ponovno da se vratimo na Firefox. (#5758)
* Sada je moguć pristup matematičkom Sadržaju u Google Chromeu na sustavu bez instaliranog Mozilla Firefox web preglednika. (#7308)
* Operacijski sustav i druge aplikacije trebale bi biti stabilnije neposredno poslije instalacije NVDA prije ponovnog pokretanja, usporedno sa prijašnjim inačicama NVDA čitača zaslona. (#7563)
* Prilikom korištenja prečaca za prepoznavanje sadržaja (npr. NVDA+r), ako objekt navigatora nestane, NVDA izgovara poruku o pogrešci umjesto nikakve poruke. (#7567)
* Popravljeno klizanje unatrag za  freedom Scientific brajične retke kiji imaju lijevi bumper bar. (#7713)

### Changes for Developers

* "scons tests" now checks that translatable strings have translator comments. You can also run this alone with "scons checkPot". (#7492)
* There is now a new extensionPoints module which provides a generic framework to enable code extensibility at specific points in the code. This allows interested parties to register to be notified when some action occurs (extensionPoints.Action), to modify a specific kind of data (extensionPoints.Filter) or to participate in deciding whether something will be done (extensionPoints.Decider). (#3393)
* You can now register to be notified about configuration profile switches via the config.configProfileSwitched Action. (#3393)
* Braille display gestures that emulate system keyboard key modifiers (such as control and alt) can now be combined with other emulated system keyboard keys without explicit definition. (#6213) 
 * For example, if you have a key on your display bound to the alt key and another display key to downArrow, combining these keys will result in the emulation of alt+downArrow.
* The braille.BrailleDisplayGesture class now has an extra model property. If provided, pressing a key will generate an additional, model specific gesture identifier. This allows a user to bind gestures limited to a specific braille display model. 
 * See the baum driver as an example for this new functionality.
* NVDA is now compiled with Visual Studio 2017 and the Windows 10 SDK. (#7568)

## 2017.3

Novosti u ovoj inačici uključuju unos brajevog kratkopisa, podrška za nove Windows OneCore glasove dostupne u Windowsima 10, ugrađenu podršku za Windows 10 OCR, i puno značajnih poboljšanja koje se tiču brajice i weba.

### Nove značajke

* Dodana je postavka u brajičnim postavkama za "vječno prikazivanje poruka". (#6669)
* U Microsoft Outlook popisu poruka, NVDA sada izgovara ako poruka ima zastavicu. (#6374)
* U Microsoft Powerpointu, sada se izgovara točan tip oblika prilikom uređivanja slajda (primjeri uključuju: trokut, krug, video, strelica), bolje nego samo 'oblik'. (#7111)
* Matematički sadržaj (dostupan kao MathML) sada je podržan u Google Chromeu. (#7184)
* NVDA sada može govoriti uz pomoć Windows OneCore glasova (znanih kao mobile glasovi), koji su uključeni u Windowse 10. Pristupate im označavanjem opcije Windows OneCore glasovi u NVDA dijaloškom okviru Govorna jedinica. (#6159)
* NVDA konfiguracijske datoteke sada mogu biti pospremljene korisničkoj mapi application data. To se uključuje u registru. Za više detalja, pogledajte poglavlje 'sistemski parametri' u korisničkom priručniku. (#6812)
* U web preglednicima, NVDA izgovara vrijednosti sadrživača za polja (točnije, aria-placeholder sada je podržan). (#7004)
* U načinu pregleda u Microsoft Wordu, sada je moguće kretati se po pravopisnim pogreškama uz pomoć brze navigacije (w i shift+w) (#6942)
* Dodana podrška za kontrolu odabirnika datuma koja se može pronaći u Microsoft Outlookovom dijaloškom okviru za termine. (#7217)
* Trenutno označeni prijedlog sada se izgovara u Windows 10 pošti u poljima to/cc te u Windows 10 polju uređivanja u Postavkama. (#6241)
* Sada se reproducira zvučni signal, koji izvještava o prisutnosti prijedloga u većini polja za pretragu u Windowsima 10 (NPR. početni zaslon, pretraga u postavkama, polja to/CC u Windows 10 pošti). (#6241)
* NVDA sada automatski čita obavijesti u Skype for Business Desktop, kao kada netko hoće započeti razgovor s vama. (#7281)
* Automatski čita dolazne poruke prilikom Skype for Business razgovora. (#7286)
* Automatsko čitanje obavijesti u Microsoft Edgeu, poput početka preuzimanja.  (#7281)
* Sada možete pisati kratkopisom i punim pismom na brajičnoj tipkovnici vašeg brajevog redka. Pogledajte poglavlje brajični unos u korisničkom vodiču. (#2439)
* Sada možete upisivati Unicode brajične znakove na brajičnoj tipkovnici, označujući Unicode braille kao brajičnu tablicu. (#6449)
* Dodana podrška za SuperBraille brajični redak koji se koristi na Tajwanu. (#7352)
* Nove brajične tablice: danski osmotočkasta kompjutorska brajica, litavski, farsi 8 točkasta kompjutorska brajica, Farsi punno pismo, slovenski osmotočkasta brajica. (#6188, #6550, #6773, #7367)
* Unapređena brajična tablica za engleski (SAD) osmotočkastu kompjutersku brajicu, podrška za znakove nabrajanja, znak za euro i slova sa naglascima. (#6836)
* NVDA sada može koristiti funkcionalnost prepoznavanja teksta uključenu u  Windowse 10 kako bi se mogao prepoznavati tekst sa slika ili iz nepristupačnih aplikacija. (#7361)
 * Jezik može biti postavljen u novom dijalogu windows 10 OCR, koji se nalazi u postavkama, u NVDA izborniku.
 * Kako biste prepoznali tekst u trenutnom objektu navigatora, pritisnite NVDA+r.
 * Za više detalja, pogledajte poglavlje o prepoznavanju teksta u vodiču za korisnike.
* Sada možete izabrati koja će se kontekstna informacija prikazati  kada je objekt u fokusu koristeći novu opciju "prezentacija konteksta fokusa" u dijaloškom okviru brajične postavke. (#217)
 * Na primjer, opcije "popuni redak promjenama konteksta" i "samo kada se redak pomiće u nazad" mogu učiniti kretanje po izbornicima bržim, jer stavke neće mijenjati svoju poziciju na retku.
 * Pogledajte poglavlje o "prezentaciji konteksta fokusa", u korisničkom vodiču za više informacija.
* U Firefoxu i Chromeu, NVDA sada podržava kompleksne dinamičke mreže poput radnih listova u kojima samo neki sadržaj može biti učitan ili prikazan (točnije,  aria-rowcount, aria-colcount, aria-rowindex and aria-colindex atribute uvedene u ARIA 1.1). (#7410)

### Izmjene

* Nedodijeljena komanda (script_restart) je dodana kako bi NVDA mogao biti brzo pokrenut. (#6396)
* Izgled tipkovnice sada može biti odabran iz dijaloškog okvira dobrodošlice. (#6863)
* Puno je više kontrola i stanja skraćeno na brajičnom retku. Orjentiri su također skraćeni. Molimo pogledajte poglavlje "kratice za tipove i stanja kontrola te orjentire" za kompletan popis. (#7188, #3975)
* Espeak-ng je nadograđen na verziju 1.49.1 (#7280).
* Popisi ulaznih i izlaznih brajičnih tablica u dijaloškom okviru brajičnih postavki, sada su sortirani po abecednom redu. (#6113)
* Obnovljen liblouis brajični prevoditelj na verziju 3.2.0. (#6935)
* Podrazumjevana brajična tablica je sada unificirani engleski brajični kod puno pismo. (#6952)
* Podrazumjevano, NVDA prikazuje sada samo djelove kontekstne informacije koja se promjenila na brajičnom retku kada objekt je fokusiran. (#217)
 * Prije je prikazivana cjelovita kontekstna informacija, nezavisno jeste li istu vidjeli prije.
 * Možete vratiti staru postavku  mjenjajući "prezentaciju fokusa konteksta" u brajičnim postavkama kako bi  "uvjek popunjavala redak".
* Prečaci za tablice više nisu dostupni tablice izgleda u načinu pregleda osim ako izgovaranje istih nije uključeno. (#7382)
* U Firefoxu i Chromeu prečaci za brzo kretanje po tablicama sada preskaću skrivene ćelije tablica. (#6652, #5655)
* NVDA logo je nadograđen. NVDA logo je stilizirana mješavina slova NVDA na bijelom, na čvrstoj ljubičastoj podlozi. To osigurava prikaz na svim pozadinskim bojama, i koristi ljubičastu boju iz loga NV Accessa. (#7446)

### Bug Fixes

* Editable div elements in Chrome no longer have their label reported as their value while in browse mode. (#7153)
* Pressing end while in browse mode for an empty Microsoft Word document no longer causes a runtime error. (#7009)
* Browse mode is now correctly   supported in Microsoft Edge where a document has been given a specific ARIA role of document. (#6998)
* In browse mode, you can now select or unselect to the end of the line using shift+end even when the caret is on the last character of the line. (#7157)
* If a dialog contains a progress bar, the dialog text is now updated in braille when the progress bar changes. This means, for example, that the remaining time can now be read in NVDA's "Downloading Update" dialog. (#6862)
* NVDA will now announce selection changes for certain Windows 10 combo boxes such as AutoPlay in Settings. (#6337).
* Pointless information is no longer announced when entering Meeting / Appointment creation dialogs in Microsoft Outlook. (#7216)
* Beeps for indeterminate progress bar dialogs such as the update checker only when progress bar output is configured to include beeps. (#6759)
* In Microsoft Excel 2003 and 2007, cells are again reported when arrowing around a worksheet. (#7243)
* In Windows 10 Creators Update and later, browse mode is again automatically enabled when reading emails in Windows 10 Mail. (#7289)
* On most braille displays with a braille keyboard, dot 7 now erases the last entered braille cell or character, and dot 8 presses the enter key. (#6054)
* In editable text, when moving the caret (e.g. with the cursor keys or backspace), NVDA's spoken feedback is now more accurate in many cases, particularly in Chrome and terminal applications. (#6424)
* The content of the Signature Editor in Microsoft Outlook 2016 can now be read. (#7253)
* In Java Swing applications, NVDA no longer sometimes causes the application to crash when navigating tables. (#6992)
* In Windows 10 Creators Update, NVDA will no longer announce toast notifications multiple times. (#7128)
* In The start menu in Windows 10, pressing Enter to close the start menu after a search no longer causes NVDA to announce search text. (#7370)
* Performing quick navigation to headings in Microsoft Edge is now significantly faster. (#7343)
* In Microsoft Edge, navigating in browse mode no longer skips large parts of certain web pages such as the Wordpress 2015 theme. (#7143)
* In Microsoft Edge, landmarks are correctly localized in languages other than English. (#7328)
* Braille now correctly follows the selection when selecting text beyond the width of the display. For example, if you select multiple lines with shift+downArrow, braille now shows the last line you selected. (#5770)
* In Firefox, NVDA no longer spuriously reports "section" several times when opening details for a tweet on twitter.com. (#5741)
* Table navigation commands are no longer available for layout tables in Browse Mode unless reporting of layout tables is enabled. (#7382)
* In Firefox and Chrome, Browse Mode table navigation commands now skip over hidden table cells. (#6652, #5655)

### Changes for Developers

* Timestamps in the log now include milliseconds. (#7163)
* NVDA must now be built with Visual Studio Community 2015. Visual Studio Express is no longer supported. (#7110)
 * The Windows 10 Tools and SDK are now also required, which can be enabled when installing Visual Studio.
 * See the Installed Dependencies section of the readme for additional details.
* Support for content recognizers such as OCR and image description tools can be easily implemented using the new contentRecog package. (#7361)
* The Python json package is now included in NVDA binary builds. (#3050)

## 2017.2

Novosti u ovoj inačici uključuju punu podršku stišavanja zvuka u Windows 10 nadogradnji za tvorce; ispravke za neke greške pri označavanju u načinu pregleda, uključujući probleme sa prečacom označi sve; značajna unaprjeđenja u podršci za Microsoft edge; i unaprjeđenja na webu kao što su to izvještavanja elemenata koji su označeni kao trenutni (koristeći aria-current).

### Nove značajke

* U Microsoft Excelu sada se mogu izgovarati granice ćelija koristeći `NVDA+f`. (#3044)
* Dodana podrška za aria-current attribute. (#6358)
* Automatsko prebacivanje jezika sada je podržano u Microsoft Edge-u. (#6852)
* Dodana podrška za Windows Kalkulator u Windows 10 Enterprise LTSB (Long-Term Servicing Branch) i Server. (#6914)
* Izvodeći prečicu "čitaj trenutni redak", tri puta brzo sriče redak fonetski. (#6893)
* Novi jezik: Burmanski /Mjanmarski.
* Unicode strelice gore i dolje, te znakovi za razlomke, sada se izgovaraju onako kako bi trebalo. (#3805)

### Izmjene

* Prilikom kretanja uz pomoć jednostavne navigacije u programima koji koriste UI Automation, ignoriraju se bezsadržajni sadržitelji, čineći tako kretanje lakšim. (#6948, #6950) 

### Ispravke grešaka

* Stavke izbornika na web stranicama (stavka izbornika potvrdni okvir i izborni gumbi) sada se mogu aktivirati kada se nalazite u načinu pregleda. (#6735)
* Izgovaranje imena radnog lista je prevedeno. (#6848)
* Pritisak tipke escape, kada je aktivan dijaloški okvir za potvrdu brisanja profila sada zatvara dijaloški okvir. (#6851)
* Ispravljena su neka rušenja u Mozilla Firefoxu i drugim Gecko aplikacijama gdje je uključena značajka višezadačnosti. (#6885)
* Izgovaranje pozadinskih boja u pregledu zaslona sada je točnije kada je tekst crtan sa transparentnom pozadinom. (#6467)
* Unapređena podrška za aria-describedby u Internet Exploreru 11, uključujući podršku u okvirima, te kada su omogućeni višestruki identifikatori. (#5784)
* U Windows 10 nadogradnji za tvorce, NVDA-ovo prigušivanje glasnoće ponovno radi kao i u prijašnjim inačicama NVDA, (TJ. utišavanje sa govorom i zvukom, uvijek utišaj, i bez utišavanja su sve dostupne). (#6933)
* NVDA više neće neuspjevati kretnje ili izgovor većine (UIA) kontrola tamo, gdje tipkovnički prečac nije definiran. (#6779)
* Više se ne dodavaju dva prazna razmaka u informaciji o tipkovničkom prečacu u većini (UIA) kontrola. (#6790)
* Većina kombinacija tipaka na HIMS brajičnim retcima (NPR. razmaknica+točkica4) ne neuspjevaju se izvoditi, tj. ponovno funkcioniraju. (#3157)
* Otklonjena greška, u kojoj je spajanje brajičnih redaka na nekim sustavima i jezicima bilo nemoguće. (#6845)
* Smanjena je šansa oštećenja konfiguracijske datoteke prilikom isključivanja Windowsa. Konfiguracija se zapisuje u privremenu datoteku, prije zamjene iste. (#3165)
* Prilikom pritiska prečaca "slovkaj trenutni redak", tri puta, kako bi se slovkao redak, koristi se ispravan jezik za slovkane znakove. (#6726)
* Kretanje po redku u Microsoft Edgeu sada je tri puta brže u Windows 10 Nadogradnji za tvorce. (#6994)
* NVDA više ne izgovara "Web Runtime grupiranje" kada se fokusiraju Microsoft Edge dokumenti u Windows 10 nadogradnji za tvorce. (#6948)
* Adobe Acrobat Reader se više ne ruši u većini PDF dokumenata, (točnije, dokumente, koji sadrže prazne atribute ActualText). (#7021, #7034)
* Sve postojeće inačice SecureCRT sada su podržane. (#6302)
* U načinu pregleda u Microsoft Edgeu, interaktivne tablice (ARIA grids) više se ne preskaću prilikom kretanja po tablicama pomoću prečaca t i shift+t. (#6977)
* U načinu pregleda, prilikom pritiska shift+home prilikom označavanja u naprijed sada odznačava početak redka kako je to očekivano. (#5746)
* U načinu pregleda, prečac "označi sve", (ctrl+a) više ne neuspjeva označiti cijeli tekst ako kursor nije na početku teksta. (#6909)
* Ispravljeni drugi manji rijetki problemi u načinu pregleda. (#7131)

### Changes for Developers

* Commandline arguments are now processed with Python's argparse module, rather than optparse. This allows certain options such as -r and -q to be handled exclusively. (#6865)
* core.callLater now queues the callback to NVDA's main queue after the given delay, rather than waking the core and executing it directly. This stops possible freezes due to the  core accidentally going to sleep after processing a callback, in the midle of  a modal call such as the desplaying of a message box. (#6797)
* The InputGesture.identifiers property has been changed so that it is no longer normalized. (#6945)
 * Subclasses no longer need to normalize identifiers before returning them from this property.
 * If you want normalized identifiers, there is now an InputGesture.normalizedIdentifiers property which normalizes the identifiers returned by the identifiers property .
* The InputGesture.logIdentifier property is now deprecated. Callers should use InputGesture.identifiers[0] instead. (#6945)
* Removed some deprecated code:
 * `speech.REASON_*` constants: `controlTypes.REASON_*` should be used instead. (#6846)
 * `i18nName` for synth settings: `displayName` and `displayNameWithAccelerator` should be used instead. (#6846, #5185)
 * `config.validateConfig`. (#6846, #667)
 * `config.save`: `config.conf.save` should be used instead. (#6846, #667)
* The list of completions in the autocomplete context menu of the Python Console no longer shows  any object path leading up to the final symbol being completed. (#7023)
* There is now a unit testing framework for NVDA. (#7026)
 * Unit tests and infrastructure are located in the tests/unit directory. See the docstring in the tests\unit\init.py file for details.
 * You can run tests using "scons tests". See the "Running Tests" section of readme.md for details.
 * If you are submitting a pull request for NVDA, you should first run the tests and ensure they pass.

## 2017.1

Novosti u ovoj inačici uključuju Izvještavanje o poglavljima i tekstnim stupcima u Microsoft wordu; podrška za čitanje, kretanje i označavanje knjiga u Kindlu za osobna računala; i unaprjeđena podrška za microsoft edge.

### Nove značajke

* U Microsoft Wordu, vrsta prijeloma poglavlja i brojeva istih sada se izgovara. ovo je omogućeno uz pomoć opcije "izvijesti o brojevima stranica" u dijaloškom okviru oblikovanje dokumenata. (#5946)
* U Microsoft Wordu, tekstni stupci sada se izgovaraju. Ovo je omogućeno uz pomoć opcije "izvijesti o brojevima stranica" u postavkama oblikovanja dokumenata. (#5946)
* Automatsko prebacivanje jezika sada je podržano u  WordPadu. (#6555)
* Prečac za pretragu (NVDA+control+f) sada je podržan u načinu pregleda u Microsoft Edgeu. (#6580)
* Brzo kretanje po gumbima u načinu pregleda (b i shift+b) sada je podržana u Microsoft Edgeu. (#6577)
* Prilikom kopiranja radnog lista u Microsoft Excelu, zaglavlja redaka i stupaca su zapamćena. (#6628)
* Podrška za čitanje i kretanje po knjigama u  Kindlu za osobna računala inačica 1.19, uključujući pristup linkovima, fusnotama, slikama, označenom tekstu i korisničkim bilješkama. Please see the Kindle for PC section of the NVDA User Guide for further information. (#6247, #6638)
* Kretanje po tablicama sada je moguće u  Microsoft Edgeu. (#6594)
* U Microsoft Excelu, prečac izgovori lokaciju preglednog kursora (desktop: NVDA+numDelete, laptop: NVDA+delete) sada izgovara ime radnog lista i poziciju u ćeliji. (#6613)
* Dodana opcija u dijaloški okvir izađi koja omogućuje ponovno pokretanje sa uključenom dijagnostikom. (#6689)

### Izmjene

* Minimalna brzina titranja kursora sada je 200 MS. Ako je ovo prije bilo postavljeno na manju vrijednost, ta vrijednost će se povećati na 200 MS. (#6470)
* U brajične postavke, Dodan je potvrdni okvir koji omogućuje - onemogućuje titranje kursora. Prije je to omogućavala vrijednost 0. (#6470)
* Nadograđen eSpeak NG (commit e095f008, 10 Veljače 2017). (#6717)
* Zbog izmjena u Windows 10 creators nadogradnji, opcija "uvijek stišavaj" više nije dostupna u NVDA glasovnim postavkama. Ali, još uvijek je dostupna u starijim inačicama Windowsa 10. (#6684)
* zbog promjena u   Windows 10 Creators nadogradnji, način "stišavanja zvuka prilikom proizvodnje zvuka i govora" više se ne može uvjeravati u punu stišanost zvuka prije nego što počne govoriti, niti ne može ostaviti audiokanal otvoren  poslije zaustavljanja naglog stišavanja glasnoće. Ove izmjene ne utjeću na starije inačice windows 10 operacijskog sustava. (#6684)

### Ispravke grešaka

* Ispravljeno smrzavanje prilikom kretanje po odlomcima u načinu pregleda. (#6368)
* Tablice koje su kopirane iz Microsoft excela u microsoft word, sada se ne tretiraju kao tablice izgleda i time više se ne ignoriraju. (#5927)
* Prilikom pokušaja pisanja u microsoft excelu u zaštićenom prikazu, NVDA sada takvu situaciju oglašava zvukom, što je bolje od izgovaranja znakova koji nisu upisani. (#6570)
* pritisak escape tipke u Microsoft Excelu Više ne prebacuje korisnika u način pregleda, osiim ako se korisnik izričito nije prebacio u isti sa NVDA+razmak i potom ušao u način fokusa sa enterom na polju obrasca. (#6569) 
* NVDA se više ne smrzava u Microsoft Excelovim gdje se cijeli redak ili stupac spajaju. (#6216)
* Izvještavanje o izrezanom, odnosno tekstu koji ne stane u cijeli redak /stupac sada je točnije u Microsoft Excelu. (#6472)
* NVDA sada izvještava o potvrdnim okvirima koji su samo za čitanje. (#6563)
* NVDA pokretač više neće prikazivati dijaloški okvir upozorenja kada ne može reproducirati zvuk logotipa zbog nedostupnosti audio uređaja. (#6289)
* Kontrole u Microsoft Excel ribbonu koje su nedostupne sada se izvještavaju kao takve. (#6430)
* NVDA više neće izgovarati "ploha" prilikom minimiziranja prozora. (#6671)
* Upisani znakovi sada se izgovaraju u aplikacijama univerzalne windowsowe platforme (UWP) (uključujući Microsoft Edge) u windows 10 Creator nadogradnji. (#6017)
* Praćenje miša sada radi na svim zaslonima na računalima koja imaju više monitora. (#6598)
* NVDA više ne postaje beskoristan poslije isključivanja windows media playera prilikom fokusiranja na kontrolu klizača. (#5467)

### Changes for Developers

* Profiles and configuration files are now automatically upgraded to meet the requirements of schema modifications. If there is an error during upgrade, a notification is shown, the configuration is reset and the old configuration file is available in the NVDA log at 'Info' level. (#6470)

## 2016.4

Poboljšanja u ovoj inačici uključuju unaprjeđenu podršku za Microsoft edge; način pregleda u windows mail e-mail klijentu (windows 10); i značajna poboljšanja u NVDA dijaloškim okvirima.

### Nove značajke

* NVDA sada može izvještavati o poravnanju /uvlaci redka koristeći zvučne signale. Ovo se može konfigurirati koristeći "Izvještavanje o uvlačenju redka" odabirni okvir u NVDA's postavkama oblikovanja dokumenta. (#5906)
* Podrška za Orbit Reader 20 brajični redak. (#6007)
* Opcija koja omogućuje otvaranje preglednika govora pri pokretanju je dodana. Ovo se može uključiti pomoću odabirnog okvira u pregledniku govora. (#5050)
* Prilikom ponovnog otvaranja dijaloškog okvira preglednika govora, Sada će dimenzije biti vrećene. (#5050)
* Polja unakrsnih referenci u Microsoft Word sada se tretiraju poput linkova. One se izgovaraju kao linkovi i mogu se aktivirati. (#6102)
* Podrška za Baum SuperVario2, Baum Vario 340 i HumanWare Brailliant2 brajične retke. (#6116)
* Početna podrška za jubilarnu inačicu Microsoft Edgea. (#6271)
* Način pregleda se sada koristi prilikom čitanja poruka u windows 10 Mail aplikaciji. (#6271)
* Novi jezik: Litavski.

### Izmjene

* Nadograđen liblouis braille translator na inačicu 3.0.0. Ovo uključuje podršku za unificiranu englesku brajicu. (#6109, #4194, #6220, #6140)
* U upravitelju dodataka, gumbi "onemogući dodatak" i omogući dodatak sada imaju tipkovničke prečace (alt+o i alt+m ). (#6388)
* Razni vizualni konflikti su ispravljeni. (#6317, #5548, #6342, #6343, #6349)
* Dijaloški okvir oblikovanje dokumenta sada je prilagođen tako da se sadržaj istog može pomicati. (#6348)
* Prilagođen izgled dijaloškog okvira za izgovor simbola tako da se puna širina dijaloškog okvira koristi za popis simbola. (#6101)
* U načinu pregleda u web preglednicima, komande za polje uređivanja (e i shift+e) i formular (f and shift+f) sada se mogu koristiti kako biste se mogli premještati između uređivačkih polja samo za čitanje. (#4164)
* U postavkama oblikovanja dokumenta, "izvjesti o promjenama oblikovanja poslije kursora" preimenovano je u "izgovori izmjene oblikovanja poslije kursora", zato što ova opcija utjeće kako na govor, tako i na brajicu. (#6336)
* Prilagođen izgled NVDA dijaloškog okvira dobrodošlice. (#6350)
* NVDA dijaloški okviri sada imaju poravnane svoje gumbe "U redu" i "odustani" na desnoj strani  zaslona. (#6333)
* pokretne kontrole sada se koriste za uređivačka polja poput "postotka izmjene visine za velika slova" postavku u dijaloškom okviru glasovnih postavki. You can enter the desired value or use the up and down arrow keys to adjust the value. (#6099)

### Ispravke grešaka

* Ispravljena rijetka greška prilikom isključivanja NVDA kada je preglednik govora otvoren. (#5050)
* Grafički linkovi se sada prikazuju u načinu pregleda u Mozilla Firefoxu. (#6051)
+- Nalazeći se u dijaloškom okviru uređivača rječnika, prilikom pritiska na gumb enter sada se spremaju sve izmjene napravljene tokom uređivanja i zatvara dijaloški okvir. Prije, enter nije radio ništa. (#6206)
* Sada se prikazuju poruke na brajičnom retku prilikom izmjene načina unosa za azijske metode unosa (izvorni unos /alfanumerički, puni oblik/polovičan, itd.). (#5892, #5893)
* Prilikom onemogućavanja a potom ponovnog omogućavanja dodatka, status dodatka sada se ponovno vraća na onu vrijednost na koju je bio postavnjen prije. (#6299)
* Prilikom korištenja Microsoft Worda, brojevi stranica u zaglavjima sada se mogu čitati. (#6004)
* Miš se sada može koristiti za pomicanje fokusa između popisa znakova  i uređivačkih polja u dijaloškom okviru izgovora simbola. (#6312)
* Ispravljena greška koja onemogućuje prikazivanje popisa elemenata kada microsoft wordow dokument sadrži neispravnu hipervezu. (#5886)
* Bio on zatvoren sa alatne trake ili pomoću prečaca alt+f4, stanje odabirnog okvira preglednika govora u nvda izborniku će sada odražavati trenutnu vidljivost prozora. (#6340)
* Komanda za ponovno učitavanje dodataka više ne prouzrokuje probleme  za konfiguracijske profile koji se okidaju, nove dokumente u internetskom pregledniku i pregled zaslona. (#2892, #5380)
* U popisu jezika, u nvda dijaloškom okviru "opće postavke",, jezici poput Aragonskog sada se prikazuju ispravno  u Windowsima 10. (#6259)
* Tipke na tipkovnici koje su emulirane, (npr. gumbi na brajičnom retku koji oponašaju tipku tab) sada se prikazuju u podešenom NVDA jeziku u pomoći ri unosu i u dijaloškom okviru "Ulazne geste". Prije su iste bile prikazane samo na engleskom. (#6212)
* Promjena NVDA jezika (iz dijaloškog okvira za odabir jezika) više se ne primjenjuje sve dok se NVDA ponovno ne pokrene. (#4561)
* Više nije moguće ostavljanje polja za uzorak praznim u novom unosu govornog rječnika. (#6412)
* Ispravljena rijetka greška prilikom skeniranja serijskih priključaka na nekim sustavima koja je rezultirala u neiskoristivosti nekih brajičnih redaka. (#6462)
* U Microsoft Word-u, numerirane liste u ćelijama tablica sada se čitaju prilikom pomicanja po ćeliji. (#6446)
* Way IFrames (dokumenti ugrađeni unutar dokumenata) se sada izgovaraju što je učinilo preciznost između preglednika. IFrames sada se izgovaraju kao "okvir" u Firefox-u. (#6047)
* Sada je moguće dodjeljivati ulazne geste za komande na Handy Tech brajičnom retku u NVDA dijaloškom okviru "ulazne geste. (#6461)
* U Microsoft Excelu, pritisak entera ili numeričkog entera prilikom navigacije u tablici sada se korektno vrši navigacija na slijedeći redak. (#6500)
* iTunes više se ne smrzava prilikom korištenja internetskog preglednika za iTunes trgovinu, Apple glazbu, ITD. (#6502)
* ispravljena rušenja u 64 bitnim Mozilla i Chrome-baziranim aplikacijama. (#6497)
* u Firefoxu sa uključenom višeprocesnošću, način pregleda i tekstualna polja za uređivanje sada funkcioniraju korektno. (#6380)

### Changes for Developers

* It is now possible to provide app modules for executables containing a dot (.) in their names. Dots are replaced with underscores (_). (#5323)
* The new gui.guiHelper module includes utilities to simplify the creation of wxPython GUIs, including automatic management of spacing. This facilitates better visual appearance and consistency, as well as easing creation of new GUIs for blind developers. (#6287)

## 2016.3

Novosti u ovoj inačici uključuju mogučnost onemogučavanja pojedinačnih dodataka; podršku za polja obrazaca u Microsoft excelu; drastična poboljšanja u izvještavanju boja; popravke i unaprjeđenja pri korištenju nekih brajičnih redaka; a također popravci i unaprjeđenja u Microsoft wordu.

### nove značajke

* Način pregleda se sada može koristiti za čitanje PDF dokumenata u Microsoft edge. (#5740)
* Podcrtavanje i dvostruko podcrtavanje se sada izgovara ako je to moguće u Microsoft Wordu. (#5800)
* U Microsoft Wordu, naslov tablice se sada izgovara ako je isti omogućen. Ako postoji opis, istom se može pristupiti koristeći prečac "otvori dugi opis", (Insert+d) in browse mode. (#5943)
* U Microsoft Wordu, NVDA sada izgovara informaciju o poziciji prilikom premještanja između odlomaka (alt+shift+StrelicaDolje i alt+shift+StrelicaGore). (#5945)
* U Microsoft Wordu, proredi se sada izgovaraju preko nvda izprečaca za izvještavanje o oblikovanju, priliko mijenjanja istih uz pomoć raznih pračaca u microsoft wordu, i prilikom premještanja na tekst sa drukčijim proredom ako je uključena opcija izvjesti o proredima u nvda postavkama oblikovanja dokumenata. (#2961)
* U Internet Exploreru, HTML5 strukturni elementi se sada prepoznaju. (#5591)
* Izvještavanje o komentarima, (kao na primjer u Microsoft Wordu) sada se mogu onemogućiti pomoću potvrdnog okvira u nvda  dijaloškom okviru oblikovanje dokumenta. (#5108)
* Sada je moguće onemogućivanje pojedinačnih dodataka. (#3090)
* Dodatni tipkovnički prečaci su dodani za ALVA BC640/680 series brajeve retke. (#5206)
* Sada postoji prečac za premještanje brajičnog retka na trenutan fokus. Trenutno , ALVA BC640/680 series ima prečac pridjeljen toj komandi, ali on se može ručno pridijeliti ručno za druge brajične retke u dijaloškom okviru ulazne geste ako želite. (#5250)
* U Microsoft Excelu, sada možete se koristiti polja obrazaca. You move to form fields using the Elements List or single letter navigation in browse mode. (#4953)
* Sada možete pridijeliti prečac za jednostavan način kretanja koristeći dijaloški obkvir ulazne geste. (#6173)

### Izmjene

* NVDA sada izgovara boje koristeći osnovne dobro razumljive boje koje se sastoje od 9 varijacija boja i 3 sjene, sa svjetlim i tamnim varijacijama. Ovo je bolje od korištenja subjektivnih i malo razumljivih imena boja. (#6029)
* postojeća reakcija NVDA+F9 potom NVDA+F10 je izmjenjena kako bi se mogao označiti tekst na prvi pritisak na F10. kada je F10 pritisnut dva put tekst se kopira u međuspremnik. (#4636)
* Nadograđen eSpeakNG na inačicu Master 11b1a7b (22 lipnja 2016). (#6037)

### Ispravke grešaka

* U načinu pregleda u Microsoft Wordu, kopiranje u međuspremnik sada čuva oblikovanje teksta. (#5956)
* U Microsoft Wordu, nvda sada pravilno čita koristeći wordove prečace za kretanje po tablicama (alt+home, alt+end, alt+pageUp i alt+pageDown) i prečace za označavanje tablica (shift pritisnut sa prečacom za kretanje). (#5961)
* U Microsoft word dijaloškim okvirima, NVDA objektna navigacija je drastično poboljšana. (#6036)
* U nekim aplikacijama poput Visual Studio 2015, prečaci (npr control+c za kopiranje) sada se izgovaraju onako kako se to očekuje. (#6021)
* ispravljena rijetka greška prilikom skeniranja serijskih portova na nekim sustavima, što je činilo večinu brajičnih redaka neupotrebljivim. (#6015)
* Izgovaranje boja u microsoft wordu sada je točnije, jer se i teme u microsoft officeu uzimaju u obzir. (#5997)
* Način pregleda u  Microsoft Edgeu i podrška za prijedloge pretrage u start izborniku, su sada dostupne na Windows 10 verzijama izdanim poslije travnja 2016. (#5955)
* U Microsoft Wordu, automatsko čitanje zaglavlja tablica sada radi bolje pri radu sa spojenim ćelijama. (#5926)
* U Windows 10 aplikaciji "pošta", NVDA više nema problema sa čitanjem sadržaja poruka. (#5635) 
* kada je uključen izgovor tipkovničkih prečaca, tipke poput caps locka, više se ne izgovaraju dva puta. (#5490)
* Dijaloški okviri kontrole korisničkog računa sada se ponovno ispravno čitaju U Windows 10 anniversary nadogradnji. (#5942)
* U Web Conference dodatku (koristi se na out-of-sight.net) NVDA više ne signalizira zvukom i govorom izmjene trake napredovanja koje se odnose na mikrofonski ulaz. (#5888)
* Izvodeći komandu traži prethodno ili traži slijedeće u načinu pregleda će sada ispravno pokretati pretragu osjetljivu na velika slova ako je izvorna pretraga osjetljiva na velika slova. (#5522)
* Prilikom uređivanja upisa u riječnik, sada ćete dobivati povratnu informaciju o nepravilnom regularnom izrazu. NVDA se više ne urušava, ako u datoteci postoji nepravilan regularni izraz. (#4834)
* Ako NVDA ne može komunicirati sa brajičnim retkom (npr. ako je odspojen), automatski će se onemogućiti korištenje istog. (#1555)
* znatno unapređene performanse u popisu elemenata u načinu pregleda u većini slučajeva. (#6126)
* U Microsoft Excelu, imena pozadinskih uzoraka, koje izgovara NVDA sada se poklapaju sa imenima koja se koriste u excelu. (#6092)
* Unaprjeđena podrška za Windows 10 zaslon prijave, uključujući obavještenja o upozorenjima i aktiviranja polja za lozinku uz pomoć dodira. (#6010)
* NVDA sada ispravno detektira sekundarne routing tipke na ALVA BC640/680 series brajičnim redcima. (#5206)
* NVDA može ponovno čitati windowsove obavijesti u posljednjim inačicama windows 10. (#6096)
* NVDA više slučajno ne zaustavlja pritiske tipaka na Baum kompatibilnim i HumanWare Brailliant B brajičnim redcima. (#6035)
* Ako je izgovaranje brojeva redaka uključeno u postavkama oblikovanja dokumenta, isti se sada prikazuju na brajičnom redku. (#5941)
* Kada je način govora isključen, izgovoreni objekti (poput pritiska NVDA+tab za izgovaranje fokusa) sada se pojavljuje u pregledniku govora, kako se to očekuje. (#6049)
* U Outlook 2016 popisu poruka,  pridružena informacija o predlošku više se ne izgovara. (#6219)
* U Google Chrome-u i web preglednicima baziranima na njemu, na jezicima drukćijima od engleskog, način pregleda više ne odbija poslušnost u većini dokumenata. (#6249)

### Changes for Developers

* Logging information directly from a property no longer results in the property  being called recursively over and over again. (#6122)

## 2016.2.1

Ova inačica ispravlja rušenja u Microsoft wordu:

* NVDA više ne prouzrokuje rušenje microsoft worda poslije pokretanja istog. (#6033)
* Uklonjena mogućnost izgovaranja gramatičkih pogrešaka, zato što je to uzrok rušenja Microsoft worda.(#5954, #5877)

## 2016.2

Novosti u ovoj inačici uključuju mogučnost izvještavanja o pravopisnim pogreškama pri pisanju; podrška za izgovaranje gramatičkih pogrešaka u Microsoft Wordu; i unaprjeđenja  i ispravke u podršci za Microsoft office paket.

### Nove značajke

* U načinu pregleda u Internet Exploreru i drugim MSHTML kontrolama, koristeći brzu navigaciju za kretanje po anotacijama (a i shift+a) sada se koristi i za kretanje po umetnutom i izbrisanom tekstu. (#5691)
* U Microsoft Excelu, NVDA sada izgovara razinu grupe ćelija, kao i njihovu proširivost ili skupljivost. (#5690)
* Pritiskom prečaca za izgovor formatiranja teksta (NVDA+f) dva puta, prezentira informaciju u načinu pregleda kako bi se mogla pregledati. (#4908)
* U Microsoft Excelu 2010 i novijem, sjenćanje čelija i njihovo popunjavanje se izgovara. Automatsko izgovaranje možete uključiti u postavkama oblikovanja dokumenta. (#3683)
* Nova brajična tablica: Starogrčki. (#5393)
* u pregledniku zapisnika, sada možete pospremiti zapisnik koristeći prečac ctrl+s. (#4532)
* Ako je izgovor pravopisnih grešaka uključen i podržan u određenoj kontroli, NVDA će reproducirati zvuk kako bi vas upozorio na pravopisnu pogrešku koja je napravljena prilikom pisanja. to se može onemogućiti koristeći "reproduciraj zvuk pri pravopisnim pogreškama" opciju u nvda postavkama tipkovnice. (#2024)
* Gramatičke pogreške se sada izgovaraju u microsoft wordu.. Ovo se može onemogućiti uz pomoć nove opcije "izgovori gramatičke pogreške" u dijaloškom okviru za oblikovanje teksta. (#5877)

### Izmjene

* U načinu pregleda i poljima za uređivanje, NVDA tretira numerički Enter na isti način kao i enter na glavnom dijelu tipkovnice. (#5385)
* NVDA sada koristi eSpeak NG sintetizator govora. (#5651)
* U Microsoft Excelu, NVDA više ne ignorira zaglavlje stupca za ćeliju kada postoji prazan redak između ćelije i zaglavlja. (#5396)
* U Microsoft Excelu, koordinate se sada izgovaraju prije zaglavlja, kako bi se  spriječila višeznačnost zaglavlja i sadržaja. (#5396)

### Ispravke grešaka

* u načinu pregleda, prilikom pokušaja korištenja brzog kretanja kako bi ste se pomakli na element koji nije podržan u dokumentu, nvda izgovara da to nije podržano bolje nego izgovaranje pogrešne informacije o nepostojećem elementu u tom smjeru. (#5691)
* prilikom popisivanja radnih listova u popisu elemenata U Microsoft Excelu, radni listovi koji sadrže samo grafove sada su uključeni. (#5698)
* NVDA više ne izgovara nepotrebne informacije prilikom prebacivanja prozora u java aplikacijama koje imaju višesstruke prozore kao što su to IntelliJ ili Android Studio. (#5732)
* U scintilla'baziranim uređivaćima teksta kao što je to Notepad++, brajica se sada osvježava pravilno pri pomicanju kursora koristeći brajični redak. (#5678)
* NVDA se više ne ruši prilikom odabira brajičnog izlaza. (#4457)
* U Microsoft Wordu, Poravnanje odlomaka sada se izgovara u mjernoj jedinici koju odabire korisnik (NPR. centimetri ili inči). (#5804)
* Pri korištenju brajičnog redka, puno više NVDA poruka koje su se prije samo izgovarale, sada su također ispisane i na brajici. (#5557)
* U pristupačnim Java aplikacijama, razina stavaka stabla sada se izgovara. (#5766)
* Popravljena urušavanja pri korištenju adobe flash'a u nekim slučajevima, koristeći mozilla firefox. (#5367)
* U Google chromeu i chrome-baziranim preglednicima, dokumenti unutar dijaloga ili aplikacije sada se mogu čitati u načinu pregleda. (#5818)
* U Google chromeu i chrome baziranim preglednicima, sada možete prisiliti NVDA da se prebaci u način pregleda u dijaloškim okvirima web sučelja ili aplikacija. (#5818)
* U internet exploreru i drugim MSHTML kontrolama, pomičući fokus do pojedinih kontrola (specifično pri korištenju elementa aria-activedescendant) više se ne prebacuje pogrešno u način pregleda. Ovo se događalo, na primjer, prilikom pomicanja na prijedloge u adresnoj traci prilikom pisanja poruke u gmailu. (#5676)
* U Microsoft Wordu, NVDA se više ne smrzava u velikim tablicama kada je izgovaranje zaglavlja redaka i stupaca uključeno. (#5878)
* U Microsoft wordu, NVDA više ne izgovara pogrešno redak sa uvučenom razinom (ali ne ugrađeni stil razine) kao naslov. (#5186)
* U načinu pregleda u microsoft wordu, pomicanje sa kraja na početak sadrživača (zarez i šift+zarez) sada radi i u tablicama. (#5883)

### Changes for Developers

* NVDA's C++ components are now built with Microsoft Visual Studio 2015. (#5592)
* You can now present a text or HTML message to the user in browse mode using ui.browseableMessage. (#4908)
* In the User Guide, when a <!-- KC:setting command is used for a setting which has a common key for all layouts, the key may now be placed after a full-width colon (：) as well as the regular colon (:). (#5739) -->

## 2016.1

Najvažnije novosti u ovoj inačici uključuju mogućnost neobaveznog smanjivanja glasnoće drugih zvukova; unaprjeđenje brajičnog izlaza i podrške za brajične retke; nekoliko značajnih poboljšanja podrške za Microsoft office; i poboljšanja u načinu pregleda za Itunes.

### Nove značajke

* Nove brajične tablice: poljska kompjutorska brajica, mongolski. (#5537, #5574)
* Možete isključiti brajični pokazivač i izmjeniti njegov oblik koristeći novu opcije prikaži brajični pokazivač i promjeni izgled kursora u dijaloškom okviru brajične postavke. (#5198)
* NVDA se sada može povezati sa  HIMS Smart Beetle brajičnim retkom putem bluetooth veze. (#5607)
* podrška za HumanWare Brailliant BI/B brajične retke kada je protokol postavljen na OpenBraille. (#5612)

### Izmjene

* Sada je zadano isključeno izgovaranje isticanja. (#4920)
* u listi elemenata  u Microsoft excelu, prečac za formule promjenjen je na alt+r tako da je sada različit od prečaca od polja filter (ne važi za hrvatski prijevod). (#5527)
* nadograđen liblouis brajični prevoditelj na inačicu 2.6.5. (#5574)
* Riječ "text" više se ne izgovara kada se pomiće fokus ili ili pregledni kursor na tekstualne objekte. (#5452)

### ispravke grešaka

* U iTunes inačici 12, način pregleda se ispravno osvježava kada se nova stranica otvara u Itunes trgovini. (#5191)
* U Internet Exploreru i drugim MSHTML kontrolama, premještanje do specificirane razine naslova  sa jednoslovnom prečicom ponaša se kako je to očekivano kada je specificirana razina naslova za potrebe pristupačnosti (specifično, kada aria-level nadpisuje razinu h oznake). (#5434)
* U Spotifyju, fokus se više često ne premještava na "nepoznati" objekt. (#5439)
* Fokus je ispravno povraćen prilikom prebacivanja u drugu aplikaciju. (#5439)
* Prilikom prebacivanja iz načina formulara u način pregleda, izmjena načina se izgovara i istovremeno prikazuje na brajičnom retku. (#5239)
* Start gumb na traci zadataka više se ne izgovara kao popis  i/ili) ili kao označen u nekim inačicama sustava windows. (#5178)
* Poruke poput "umetnuto" više se ne izgovaraju prilikom sastavljanja poruka u Microsoft Outlooku. (#5486)
* Pri korištenju brajičnog retka kada je tekst označen na trenutnom retku (npr. prilikom traženja u uređivaću teksta za tekstom koji se pojavljuje u istom retku), brajični redak će se također pomaknuti ako je to potrebno. (#5410)
* NVDA se više ne gasi podmuklo prilikom zatvaranja windows komandne konzole uz pomoć alt+f4 u windowsima 10. (#5343)
* u popisu elemenata u načinu pregleda, prilikom izmjene vrste elementa, polje za filtriranje se sada automatski čisti. (#5511)
* u tekstu koji se može uređivati u Mozilla aplikacijama, pomicanje miša ponovno čita potrebni redak, riječ, itd. Kao što se i očekuje umjesto čitanja cijelog sadržaja. (#5535)
* prilikom pomicanja miša u poljima za uređivanje u mozilla aplikacijama, čitanje se ne zaustavlja na elementima poput linkova u riječi ili retku koji je čitan. (#2160, #5535)
* U internet exploreru, shoprite.com web stranica može se ponovo čitati u načinu pregleda umjesto izgovaranja praznih redova. (točnije, lang atributi se korektno interpretiraju).) (#5569)
* U Microsoft Wordu, lista promjena poput "umetnuto" više se ne izgovara ako oznaka izmjene nije prikazana. (#5566)
* kada je preklopni gumb pritisnut, nvda izgovara izmjenu istog od njegova pritiska do otpuštanja pritiska. (#5441)
* izgovor izgleda pokazivaća miša ponovno radi kako je očekivano. (#5595)
* kada se izgovara poravnanje teksta, nerazdjeljujući razmaci su sada tretirani kao normalni razmaci. Previously, this could cause announcements such as "space space space" instead  of "3 space". (#5610)
* NVDA sada može neobavezno smanjivati glasnoću drugih zvukova kada je instaliran na windowsima 8 i novijim. To može biti konfigurirano koristeći koristeći način manjivanja glasnoće u dijaloškom okviru govorna jedinica ili pritiskom  nvda+shift+d. (#3830, #5575)
* Prilikom zatvaranja moderne liste za upis istočnoazijskih znakova, fokus se vraća na sastavljanje unosa ili na određeni dokument. (#4145)
* U microsoft office 2013 i novijem, kada je ribbon prikazan tako da se prikazuju samo kartice, stavke u ribbonu se izgovaraju ponovno kako je to očekivano kada je kartica aktivirana. (#5504)
-Ispravke u otkrivanju gesti zaslona osjetljivog na dodir. (#5652)
* prelasci po ekranu osjetljivom na dodir više se ne izgovaraju u pomoći pri unosu. (#5652)
* Nvda više ne griješi prilikom izlistavanja komentara u listi elemenata za excel ako je komentar na spojenoj ćeliji. (#5704)
* U vrlo rijetkim slučajevima, nvda više ne neuspjeva čitati sadržaje ćelija u Excelu sa uključenom opcijom izgovaraj zaglavlja redaka i stupaca (#5705)
* U Google chrome, navigacija unutar sastava unosa za istočnoazijske znakove više ne završava greškom. (#4080)
* prilikom pretrage Apple music u iTunesu, način pregleda za rezultate pretrage se sada osvježava kako je to očekivano. (#5659)
* u Microsoft Excelu, pritisak kombinacije shift+f11 za kreiranje nove ćelije sada izgovara vašu novu poziciju umjesto da ne izgovori ništa. (#5689)
* Ispravljeni problemi sa brajičnim izlazom  prilikom upisivanja korejskih znakova.. (#5640)

### Changes for Developers

* The new audioDucking.AudioDucker class allows code which outputs audio to indicate when background audio should be ducked. (#3830)
* nvwave.WavePlayer's constructor now has a wantDucking keyword argument which specifies whether background audio should be ducked while audio is playing. (#3830)
 * When this is enabled (which is the default), it is essential that WavePlayer.idle be called when appropriate.
* Enhanced I/O for braille displays: (#5609)
 * Thread-safe braille display drivers can declare themselves as such using the BrailleDisplayDriver.isThreadSafe attribute. A driver must be thread-safe to benefit from the following features.
 * Data is written to thread-safe braille display drivers in the background, thus improving performance.
 * hwIo.Serial extends pyserial to call a callable when data is received instead of drivers having to poll.
 * hwIo.Hid provides support for braille displays communicating via USB HID.
 * hwPortUtils and hwIo can optionally provide detailed debug logging, including devices found and all data sent and received.
* There are several new properties accessible from touch screen gestures: (#5652)
 * MultitouchTracker objects now contain a childTrackers property which contains the MultiTouchTrackers the tracker was composed of. For example, 2 finger double tap has child trackers for two 2-finger taps. The 2-finger taps themselves have child trackers for two taps.
 * MultiTouchTracker objects now also contain a rawSingleTouchTracker property if the tracker was the result of one single finger doing a tap, flick or hover. The SingleTouchTracker allows access to the underlying ID assigned to the finger by the operating system and whether or not the finger is still in contact at the current time.
 * TouchInputGestures now have x and y properties, removing the need to access the tracker for trivial cases.
 * TouchInputGesturs now contain a preheldTracker property, which is a MultitouchTracker object representing the other fingers held while this action was being performed.
* Two new touch screen gestures can be emitted: (#5652)
 * Plural tap and holds (e.g. double tap and hold)
 * A generalized identifier with finger count removed for holds (e.g. hold+hover for 1finger_hold+hover).

## 2015.4

Novosti u ovoj inačici ukljućuju unaprjeđivanje performansi u windows 10; uključivanje u centar za olakšani pristup u windowsima 8 i novijim; unaprjeđenja za microsoft excel, ukljućujući popisivanje i preimenovanje radnih listova te pristup zaključanim ćelijama u zaštićenim radnim listovima; i podrška za uređivanje teksta u obogaćenog teksta u firefoxu, google chromeu i mozilli thunderbird.

### nove značajke

* NVDA se sada prikazuje u centru za olakšani pristup u windowsima8 i novijim. (#308)
* kada se krećete po ćelijama u excelu, izmjene oblikovanja se sada čitaju ako su odgovarajuće opcije ukljućene u dijaloškom okviru oblikovanje dokumenta. (#4878)
* Opcija izvijesti o isticanju je dodana u NVDA dijaloški okvir oblikovanje dokumenta. podrazumjevano ukljućena, omogućuje nvda  čitanje naglašenog teksta u dokumentima. To je podržano samo u internet exploreru. (#4920)
* Postojanje umetnutog ili izbrisanog teksta sada se izvještava u načinu pregleda za Internet explorer ako je nvda opcija izvijesti o revizijama urednika uključena. (#4920)
* Prilikom pregleda izmjena u nvda popisu elemenata za microsoft word, više informacija poput tog što je brisano ili označenois sada se prikazuje. (#4920)
* Microsoft Excel: popisivanje i preimenovanje radnih listova je moguće iz nvda popisa elemenata (NVDA+f7). (#4630, #4414)
* Sada je moguće podesiti hoće li se trenutni simbol slati govornoj jedinici (npr kako bi prouzročio pauzu - ili promijenio intonaciju) u dijaloškom okviru izgovor simbola. (#5234)
* u microsoft excelu, NVDA izvještava bilo koju ulaznu poruku postavljenu na radni list koju je postavio autor na ćeliju. (#5051)
* podrška za Baum Pronto! V4 i VarioUltra brajične retke preko bluetooth veze. (#3717)
* podrška za uređivanje obogaćenog teksta u mozilla aplikacijama kao što su google dokumenti sa ukljućenom brajičnom podrškom u mozila firefoxu i i html sastavljanju u mozilla thunderbirdu. (#1668)
* podrška za uređivanje obogaćenog teksta u google chrome i Chromepreglednicima baziranim na chromeu poput google docs sa ukljućenom brajičnom podrškom. (#2634)
 * to zahtjeva chrome inačicu 47 i noviju.
* U načinu pregleda u microsoft excelu, Možete se kretati po zakljućanim čelijama u zaštićenim radnim listovima. (#4952)

### Izmjene

* Opcija izvjesti o revizijama urednika u oblikovanju dokumenta sada je uključena zadano. (#4920)
* Premještajući se po znakovima u microsoft wordu sa uključenom opcijom izvjesti o izmjenama urednika, manje se informacija izgovara za izmjene, što olakšava navigaciju i čini je bržom. Kako biste pogledali dodatne informacije, koristite listu izmjena. (#4920)
* Nadograđen liblouis brajični prevoditelj na inačicu 2.6.4. (#5341)
* neki simboli ukljućujući osnovne matematičke simbole, ) premješteni su na razinu ponešto kako bi se zadano izgovarali. (#3799)
* Ako govorna jedinica to podržava, govor će biti zaustavljan za simbole zagrada i en dash (–). (#3799)
* Kada se označava tekst, tekst je čitan prije obavjesti označavanja umjesto poslije. (#1707)

### Ispravke grešaka

* Drastično unaprjeđenje performansi pri navigaciji Outlook 2010/2013 popisa sa porukama. (#5268)
* u grafu u microsoft excelu, kretanje uz pomoć nekih tipaka (poput promjena radnog lista uz pomoć kontrol+page up i kontrol+pageDown) sada ispravno funkcionira. (#5336)
* Ispravljen vizualni izgled  gumbi u dijaloškom okviru upozorenja koji se prikazuje kada želite pregaziti stariju inačicu nvda novijom i obratno. (#5325)
* U windowsima 8 i novijim, NVDA se pokreće puno ranije se kada se prijavljujete u windows. (#308)
* ako ste to omogućili u prijašnjoj inačici nvda, trebate to ponovo iskljućiti i ukljućiti kako bi promjena stupila na snagu. Ispratite slijedeće korake:
Otvorite dijaloški okvir opće postavke.
odznačite odabirni okvir pokreni nvda poslije prijave u windows.
Pritisnite gumb u redu.
Ponovno otvorite dijaloški okvir opće postavke.

1. Odaberite odabirni okvir pokreni nvda prilikom prijave u windows .
1. Pritisnite ok gumb.

* Unaprjeđenja performansi u ui automation uključujući eksplorer za datoteke i task manager. (#5293)
* nvda sada korektno čita kada se dolazi tabom do aria grid kontrola samo za čitanje u načinu pregleda za mozilla firefox i drugim gecko-baziranim kontrolama. (#5118)
* nvda sada korektno izvještava o  "nema prethodnog" umjesto "nema slijedećeg" kada ne postoji više objekata prilikom klizanja u lijevo na zaslonu osjetlijvom na dodir.
* ispravljen problem pri pisanju više rijeći u polju za filtriranje u  dijaloškom okviru ulaznih gesti. (#5426)
* NVDA se više ne smrzava u nekim slućajevima prilikom ponovnog spajanja na humanware BI/B series redak putem usb-a. (#5406)
* u jezicima sa dvojnim znakovima, opisi znakova rade kako treba za engleska velika slova. (#5375)
* nvda se više neće često smrzavati prilikom otvaranja windows 10 izbornika start. (#5417)
* U Skypeu za radnu površinu, obavijesti koje su prikazane prije prethodne obavijesti se sada čitaju. (#4841)
* sada se čitaju obavijesti u  Skypeu za radnu površinu 7.12 i novijim. (#5405)
* NVDA sada ispravno čita fokusiranu stavku prilikom napuštanja kontekstnog izbornika u nekim aplikacijama poput Jart. (#5302)
* U Windowsima 7 i novijim, boja se ponovo čita u većini aplikacija popud Wordpada. (#5352)
* Prilikom uređivanja u  Microsoft PowerPointu, pritiskom entera nvda sada izgovara automatski unešen tekst popud  točkice ili broja. (#5360)

## 2015.3

Novosti u ovoj inačici uključuju početnu podršku za windows 10 operacijski sustav; mogućnost onemogučavanja brzog kretanja u načinu pregleda (korisno za neke web aplikacije); unapređenja u internet exploreru; i popravke grešaka tzv. izmješanog teksta prilikom upisivanja znakova koristeći neke aplikacije sa uključenom brajicom.

### Nove Značajke

* Sada se izgovara postojanje pravopisnih pogrešaka u poljima za uređivanje u internet exploreru i drugim MSHTML kontrolama. (#4174)
* Kada se pojave u tekstu, puno više matematičkih simbola je sada izgovoreno. (#3805)
* Prijedlozi pretrage na početnom zaslonu windowsa 10, sada se izgovaraju (#5049)
* podrška za EcoBraille 20, EcoBraille 40, EcoBraille 80 i EcoBraille Plus brajične retke. (#4078)
* U načinu pregleda sada možete uključivati brzo kretanje pomoću navigacijskih tipki pritiskom kombinacije tipaka NVDA+shift+razmak. Kada je Ova opcija isključena, navigacijske tipke za brzo kretanje počinju se prosljeđivati drugoj aplikaciji /programu, što je korisno za neke web aplikacije poput gmaila, twittera i Facebooka. (#3203)
* Nove brajične tablice: Finski šestotočkasta brajica, irski puno pismo, irski kratkopis, korejsko puno pismo (2006), korejski kratkopis (2006). (#5137, #5074, #5097)
* Sada je podržana qwerty tipkovnica na  Papenmeier BRAILLEX Live Plus brajičnom retku. (#5181)
* Eksperimentalna podrška za Microsoft Edge web preglednik i pregledački mehanizam u Windowsima 10. (#5212)
* Novi jezik: Kanadaški.

### Izmjene

* Nadograđen LibLouis brajični prevoditelj na inačicu 2.6.3. (#5137)
* Prilikom pokušaja instalacije starije inačice NVDA od one koja je trenutno instalirana, sada ćete biti upozoreni da to nije preporučljivo, i da biste trebali ukloniti prethodnu inačicu NVDA prije nastavka instalacije starije inačice. (#5037)

### Ispravke Grešaka

* U načinu pregleda za  Internet Explorer i druge MSHTML kontrole, brza navigacija po poljima obrazaca više ne uključuje prezentacijske stavke popisa. (#4204)
* U firefoxu, NVDA više ne pokušava stvoriti opis za  ARIA tab panele bazirane na all text inside atributu. (#4638)
* U Internet Exploreru i drugim MSHTML kontrolama, tabiranjem u sekcijama, člancima ili dijalozima  više ne izgovara sadržaj nadređenog objekta kao njegovo ime. (#5021, #5025) 
* Pri korištenju Baum/HumanWare/APH brajičnih redaka sa brajičnom tipkovnicom, brajični unos znakova više neće prestati funkcionirati nakon pritiska neke druge tipke  na brajičnom retku. (#3541)
* U windowsima 10, više se ne izgovaraju nepotrebne informacije pri pritisku alt+tab i alt+shift+tab prilikom prebacivanja između aplikacija. (#5116)
* Upisani tekst više nije izmješan pri korištenju nekih aplikacija  poput Microsoft Outlook sa brajičnim retkom. (#2953)
* U načinu pregleda u Internet Exploreru i drugim MSHTML kontrolama, sada se izgovara trenutni sadržaj koji je fokusiran i odma je prebačen fokus. (#5040)
* U načinu pregleda u Microsoft Wordu, brza navigacija osvježava sadržaj na brajičnom retku i pregledni kursor kako je i očekivano. (#4968)
* Pri prikazu brajice, više se ne prikazuju nepotrebni razmaci /bjeline /prazni prostori prije ili poslije oznaka za kontrole i oblikovanje teksta. (#5043)
* Kada program reagira sporo, i kada se prebacujete sa tog programa, NVDA NVDA puno bolje reagira u drugim aplikacijama u većini slučajeva. (#3831)
* Sada se izgovaraju pozadinske obavijesti u windowsima 10. (#5136)
* Sada se izgovara vrijednost koja se mijenja  u nekim (UI Automation) odabirnim okvirima gdje to prije nije radilo.
* u načinu pregleda u internetskim preglednicima, pritiskanje taba se sada ponaša kako je to očekivano poslije tabanja do okvira dokumenta. (#5227)
* windows 10 zaslon zaključavanja može se zatvoriti koristeći zaslon osjetljiv na dodir. (#5220)
* U windowsima 7 i novijim, tekst više nije izmješan kada upisujete tekst u većini aplikacija poput Wordpada i Skypea sa brajičnim retkom. (#4291)
* Na windows 10 zaslonu zaključavanja, više nije moguće čitanje međuspremnika, pristup pokrenutim programima uz pomoć preglednog kursora, izmjena nvda konfiguracije, itd. (#5269)

### Changes for Developers

* You can now inject raw input from a system keyboard that is not handled natively by Windows (e.g. a QWERTY keyboard on a braille display) using the new keyboardHandler.injectRawKeyboardInput function. (#4576)
* eventHandler.requestEvents has been added to request particular events that are blocked by default; e.g. show events from a specific control or certain events even when in the background. (#3831)
* Rather than a single i18nName attribute, synthDriverHandler.SynthSetting now has separate displayNameWithAccelerator and displayName attributes to avoid reporting of the accelerator in the synth settings ring in some languages.
 * For backwards compatibility, in the constructor, displayName is optional and will be derived from displayNameWithAccelerator if not provided. However, if you intend to have an accelerator for a setting, both should be provided.
 * The i18nName attribute is deprecated and may be removed in a future release.

## 2015.2

Nove značajke u ovoj inačici uključuju mogućnost čitanja grafova u microsoft excelu i podršku koja omogućuje čitanje matematičkog sadržaja.

### Nove značajke

* Sada je moguće pomicanje po rečenicama koristeći tipkovničke prečace alt+strelicaGore i alt+strelicaDolje u Microsoft wordu. (#3288)
* Nove brajične tablice za nekoliko indijskih jezika. (#4778)
* U microsoft excelu, NVDA sada izgovara kada je u čeliji sadržaj koji prelazi preko ćelije ili koji je izrezan. (#3040)
* Sada u excelu možete pritisnuti insert f7 kako bi ste se kretali između formula i grafova. (#1987)
* Podrška za čitanje grafova u Microsoft excelu. da biste ovo koristili, pritisnite (NVDA+f7) potom koristite strelice kako biste se kretali između podatkovnih točaka. (#1987)
* koristeći MathPlayer 4 firme Design Science, nvda sada može čitati i biti u interakciji sa matematičkim sadržajem u web preglednicima, microsoft wordu i powerpointu. Molimo pogledajte poglavlje "čitanje matematičkog sadržaja" u korisničkom priručniku". (#4673)
* Sada je moguće pridjeljivanje dodirne geste, tipkovničkog prečaca, ili tipke na brajičnom retku bilo kojem nvda dijaloškom okviru pomoću dijaloškog okvira "ulazne geste". (#4898)

### izmjene

* U NVDA dijaloškom okviru oblikovanje dokumenta, promjenjeni su tipkovnički prečaci za opcije  izvijesti o popisima, izvijesti o linkovima, izvijesti o brojevima redaka i izvijesti o imenu fonta. (#4650)
* U NVDA dijaloškom okviru postavke miša, dodani su tipkovnički prečaci za slijedeće opcije: reproduciraj zvučne koordinate prilikom pomicanja miša i svjetlina kontrolira glasnoću zvuka. (#4916)
* Značajno poboljšano izgovaranje boja. (#4984)
* nadograđen liblouis brajični prevoditelj na inačicu 2.6.2. (#4777)

### Ispravke grešaka

* Opisima znakova se sada ispravno rukuje u slučajevima kada postoje spojni znakovi u nekim jezicima indijskog podkontinenta. (#4582)
* ako je opcija "vjeruj jeziku trenutnog glasa prilikom procesiranja simbola" uključena, dijaloški okvir izgovor simbola interpunkcije sada poštuje taj jezik. također, izgovor za jezik koji se uređuje, sada se prikazuje u naslovnoj traci. (#4930)
-U internet exploreru i drugim mshtml kontrolama, upisani znakovi se više ne izgovaraju nepotrebno u odabirnim okvirima za uređivanje poput google pretrage na Googleovoj web stranici. (#4976)
* kada se označuju boje u aplikacijama Microsoft office uredskog paketa, Imena boja se sada ispravno čitaju. (#3045)
* Danska brajična tablica sada ponovno radi. (#4986)
* Tipke pageUp / pageDown sada se ponovno mogu koristiti kako bi se mijenjali slajdovi u powerpointowom prikazu slajdova. (#4850)
* U Skypeu za radnu površinu 7.2 i novijem, ispravno se izgovaraju obavjesti prilikom pisanja poruke, a također, riješeni su problemi prilikom pomicanja fokusa sa skypeovog prozora čavrljanja. (#4972)
* Ispravljene greške prilikom upisivanja nekih simbola poput zagrada u polje filtriranja u dijaloškom okviru ulazne geste. (#5060)
* u Internet Exploreru i drugim MSHTML kontrolama, pritisak tipkovničkih kombinacija G i shift+G koja služi za kretanje po grafikama sada prikazuje i slike u svrhu pristupačnosti (tj. ARIA role img). (#5062)

### Changes for Developers

* brailleInput.handler.sendChars(mychar) will no longer filter out a character if it is equal to the previous character by ensuring that the key sent is correctly released. (#4139)
* Scripts for changing touch modes will now honor new labeles added to touchHandler.touchModeLabels. (#4699)
* Add-ons can provide their own math presentation implementations. See the mathPres package for details. (#4509)
* Speech commands have been implemented to insert a break between words and to change the pitch, volume and rate. See BreakCommand, PitchCommand, VolumeCommand and RateCommand in the speech module. (#4674)
 * There is also speech.PhonemeCommand to insert specific pronunciation, but the current implementations only support a very limited number of phonemes.

## 2015.1

Unapređenja u ovoj inačici uključuju način pregleda za dokumente u Microsoft Wordu i Outlooku; velika poboljšanja u podršci za Skype za Radnu površinu; i nezamjetne popravke grešaka u Microsoft Internet Exploreru.

### Nove značajke

* Sad možete dodavati nove simbole u dijaloškom okviru za dodavanje novih simbola. (#4354)
* U dijaloškom okviru ulazne geste možete koristiti novu značajku "filtriraj po" da biste prikazali geste koje sadrže samo određene riječi. (#4458)
* NVDA sad automatski čita tekst u aplikaciji mintty. (#4588)
* U dijaloškom okviru načina pregleda moguće je koristiti pretragu osjetljivu na velika slova. (#4584)
* Brzo kretanje (H za naslove itd.) i popis elemenata (NVDA+f7) su sada dostupni i u dokumentima programa Microsoft Word kad uključite način pregleda pomoću prečaca NVDA+razmak. (#2975)
* Čitanje HTML poruka u Microsoft Outlooku 2007 i višim vidno se poboljšalo jer je način pregleda automatski uključen za te poruke. Ako način pregleda nije uključen, što se zna dogoditi u rijetkim situacijama, možete ga prisilno uključiti koristeći prečac NVDA+razmak. (#2975) 
* Zaglavlja stupaca u Microsoft wordu su automatski čitana u tablicama gdje je autor strogo odredio zaglavlje retka pomoću svojstava tablice u microsoft wordu. (#4510) 
 * Međutim, za tablice u kojima su redovi spojeni ovo neće raditi automatski. U tom slučaju još uvijek možete namjestiti zaglavlja stupaca ručno unutar NVDA pomoću prečaca NVDA+shift+c.
* Obavijesti se čitaju uobičajeno u Skypeu za radnu površinu. (#4741)
* U Skypeu za radnu površinu, sada možete čitati i pregledavati zadnje pristigle poruke koristeći prečace NVDA+control+1 do NVDA+control+0; npr. NVDA+control+1 za posljednju poruku i NVDA+control+0 za desetu posljednju. (#3210)
* U razgovoru u programu Skype za radnu površinu, NVDA sada izvještava kada kontakt piše tekst. (#3506)
* NVDA se sada može tiho instalirati preko naredbenog retka bez da se pokreće instalirana kopija nakon instalacije. Kako biste to učinili koristite komandu --install-silent. (#4206)
* Podrška za Papenmeier BRAILLEX Live 20, BRAILLEX Live and BRAILLEX Live Plus brajične retke. (#4614)

### Izmjene

* U dijaloškom okviru oblikovanje dokumenta, opcija izvijesti o pravopisnim pogreškama sada ima tipkovnički prečac (alt+p). (#793)
* NVDA će sad koristiti jezik sintetizatora/glasa za procesiranje znakova i simbola (uključujući imena simbola interpunkcije) u zavisnosti od toga je li automatsko prepoznavanje jezika uključeno. Da biste isključili ovu značajku tako da NVDA ponovno koristi svoj jezik sučelja, odznačite novu opciju u glasovnim postavkama koja se zove Vjeruj jeziku trenutnog glasa kad se procesiraju simboli i znakovi. (#4210)
* Podrška sintetizatora govora Newfon je uklonjena. Newfon je sad dostupan kao dodatak za NVDA. (#3184)
* Za korištenje uz pomoć NVDA zahtjeva se Skype za Radnu površinu 7 ili noviji; Ranije inačice nisu podržane. (#4218)
* Preuzimanje NVDA nadogradnji je sada više sigurnije. (Točnije, informacije o nadogradnjama sada se dobivaju putem https protokola i kontrolni zbroj datoteke se provjerava poslije preuzimanja.) (#4716)
* eSpeak je nadograđen tako da je njegova najnovija inačica 1.48.04 (#4325)

### Ispravke grešaka

* U Microsoft Excelu, rješavanje statusa izgovora kad su ćelije stupaca i redaka spojene. Npr, ako su A1 i B1 spojene, ćelija B2 će pod sobom imati  A1 i  B1 izgovorene kao zaglavlje stupca, bolje nego uopće neizgovoren. (#4617)
* Prilikom uređivanja sadržaja unutar tekstualnog okvira u Microsoft PowerPointu 2003, NVDA će ispravno prikazivati sadržaj u svakom od redaka. U prethodnim inačicama prvi znak unutar svakog retka na početku odlomka nebi bio izgovoren. (#4619)
* Svi se NVDA dijaloški okviri prikazuju na sredini zaslona, povećana urednost vizualne prezentacije i lakše snalaženje (#3148)
* U inačici Skype aplikacije za desktop, prilikom unosa poruke upoznavanja kod dodavanja novog kontakta, kretanje i unos poruke sad rade korektno. (#3661)
* Kad se fokus prebaci na novi element unutar prikaza stabla u aplikacijama kao što su Eclipse ili IDE, ako prethodni element predstavlja potvrdni okvir, isti će sad biti ispravno izgovoren. (#4586)
* U Microsoft Wordu, unutar dijaloškog okvira za provjeru pravopisa, sljedeća greška automatski će biti izgovorena nakon unešenih izmjena na posljednjoj grešci ili u slučaju ignoriranja greške primjenom odgovarajućeg tipkovničkog prečaca.(#1938)
* Tekst se ponovno ispravno može čitati na mjestima kao što su terminal programa Tera Term Pro i dokumenti u Balabolci. (#4229)
* Fokus se ponovno postavlja u dokumentu koji se trenutno uređuje kad se dovršava unos korejskog ili drugih istočnoazijskih jezika, kad se uređuje unutar okvira u INTERNET EXPLORERU i drugim MSHTML dokumentima. (#4045)
* U dijaloškom okviru ulazne geste, kad se označava izgled tipkovnice za tipkovničku gestu koja se dodaje, pritiskom escape tipke, izbornik se zatvara onako kako je očekivano umjesto zatvaranja dijaloškog okvira. (#3617)
* Kad se dodatak uklanja, Mapa koja sadrži određeni dodatak se sada pravilno uklanja. Prije ste NVDA trebali pokretati dva puta. (#3461)
* Ispravljene su velike greške pri korištenju Skype za Radnu površinu 7. (#4218)
* Kada šaljete poruku u skypeu za radnu površinu, ista se više ne čita dvaput. (#3616)
* U Skypeu za Radnu površinu, NVDA više neće sporadično nepravilno čitati više poruka (čak i cijeli razgovor). (#4644)
* Ispravljen problem u kojem NVDA prečac Izgovori datum/vrijeme nije poštivao regionalnu postavku koju je odredio korisnik u nekim slučajevima. (#2987)
* U načinu pregleda, besmisleni tekst (koji ponekada sadrži nekoliko redaka) više se ne prikazuje za većinu slika Kao što se može pronaći na Google grupama. (Specifično, ovo se događalo sa base64 enkodiranim slikama.) (#4793)
* NVDA se više neće smrzavati nakon nekoliko sekundi kad premještate fokus sa metro aplikacija u windowsu 8 kad se suspendiraju. (#4572)
* Atribut aria-atomic na živim regijama u Mozilla Firefoxu je sada uvažen, čak iako se element atomic promijeni. Prije je to utjecalo samo na elemente koji su slijedeći. (#4794) 
* Način pregleda će se osvježavati, žive regije će biti pročitane, za dokumente u načinu pregleda unutar aria aplikacija koje su ugrađene u dokument u Internet Exploreru ili drugim MSHTML kontrolama (#4798)
* Kada je tekst izmijenjen ili dodan u tekstualno relevantnim živim regijama u Internet Exploreru i drugim MSHTML kontrolama, Čita se samo dodan ili pročitan tekst, bolje nego sav tekst koji se nalazi u tom elementu. (#4800)
* Sadržaj koji je označen atributom aria-labelledby na elementima u Internet Exploreru i drugim MSHTML kontrolama ispravno zamjenjuje izvorni sadržaj gdje je to tako dozvoljeno. (#4575)
* Kad se provjerava pravopis u Microsoft Outlooku 2013, neispravno napisana riječ se sada ispravno čita. (#4848)
* U Internet Exploreru i drugim MSHTML kontrolama, sadržaj unutar elemenata koji je skriven sa visibility:hidden više se nepoželjno ne prikazuje u načinu pregleda. (#4839, #3776)
* U Internet Exploreru i drugim MSHTML kontrolama, atribut naslova na kontrolama obrasca više ne uzima prevlast nad drugim pridruženim natpisima]. (#4491)
* U Internet Exploreru i drugim MSHTML kontrolama, NVDA više ne izbjegava fokusiranje na elemente zbog aria-activedescendant attributa. (#4667)

### Changes for Developers

* Updated wxPython to 3.0.2.0. (#3763)
* Updated Python to 2.7.9. (#4715)
* NVDA no longer crashes when restarting after removing or updating an add-on which imports speechDictHandler in its installTasks module. (#4496)

## 2014.4

### Nove mogućnosti

* Novi jezici: Kolumbijski španjolski, Pendžabski.
* Sad je moguće ponovno pokrenuti NVDA, ili ponovno pokrenuti NVDA s isključenim dodacima u NVDA dijaloškom okviru za izlaz. (#4057)
 * NVDA je također moguće pokrenuti s isključenim dodacima uporabom opcije --disable-addons u naredbenom retku.
* U govornim rječnicima sad je moguće odrediti hoće li se uzorak slagati samo ako se radi o cijeloj riječi; npr. ne pojavljuje se kao dio veće riječi. (#1704)

### Promjene

* Ako je objekt na koji ste se pomaknuli uporabom objektne navigacije unutar dokumenta koji radi u načinu pregleda, ali objekt na kojem ste se prethodno nalazili nije bio, način pregleda je automatski postavljen na dokument. Ranije se ovo događalo samo ako je objekt navigatora pomaknut zbog promjene fokusa. (#4369)
* Popisi brajičnih redaka i govornih jedinica u njihovim odgovarajućim dijaloškim okvirima postavki su sad sortirani abecednim redom, svi osim stavke Bez brajice/Bez govora koje se sada nalaze na kraju popisa. (#2724)
* Brajični prevoditelj liblouis je ažuriran na inačicu 2.6.0. (#4434, #3835)
* U načinu pregleda, pritisak na e i shift+e za kretanje po poljima za uređivanje sada uključuje i uređivajuče odabirne okvire. Ovo se odnosi i na okvir za pretraživanje u zadnjoj inačici Google tražilice. (#4436)
* Klik na NVDA ikonu u području obavijesti uporabom lijeve tipke miša sada otvara NVDA izbornik, umjesto da ne napravi ništa. (#4459)

### Ispravke grešaka

* Prilikom premještanja fokusa natrag u dokument koji radi u načinu pregleda (npr. ponavljanja alt+tab naredbe za dolazak do već otvorene web stranice), pregledni kursor je ispravno pozicioniran na virtualnu točku umetanja, a ne više na fokusiranu kontrolu (npr. na obližnji link). (#4369)
* U Powerpoint dijaprojekcijama, pregledni kursor ispravno slijedi virtualnu točku umetanja. (#4370)
* U Mozilla Firefox-u i ostalim preglednicima zasnovanim na Gecko-u, novi sadržaj unutar žive regije će se najaviti čak i ako novi sadržaj ima upotrebljiv ARIA živi tip koji je drugačiji od matične žive regije; npr. kada je sadržaj označen kao pouzdan dodan u živu regiju označenu kao uglađenu. (#4169)
* U Internet Explorer-u i drugim MSHTML kontrolama, neki slućajevi gdje je dokument sadržan unutar drugog dokumenta više ne sprječavaju korisnika da pristupi nekom sadržaju (naročito okviri unutar okvira). (#4418)
* NVDA se više ne ruši prilikom pokušaja korištenja Handy Tech brajičnog retka u nekim slučajevima. (#3709)
* U Windows Vista sustavu, lažan dijaloški okvir "Ulazna točka nije pronađena" više se ne prikazuje u nekoliko slučajeva kao što su pokretanje NVDA preko prečaca na radnoj površini ili putem tipkovnog prečaca. (#4235)
* Ozbiljni problemi sa kontrolama uređivanja teksta unutar dijaloških okvira u nedavnim inačicama Eclipse-a su ispravljeni. (#3872)
* U Outlook-u 2010, premještanje točke umetanja sada funkcionira kako treba u polju za lokaciju kod zahtjeva za sastanke. (#4126)
* Unutar žive regije, sadržaj koji je označen kao neživ (npr. aria-live="off") će se sada ispravno ignorirati. (#4405)
* Prilikom izgovaranja teksta statusne trake koja ima naziv, naziv je sada ispravno odvojen od prve riječi teksta statusne trake. (#4430)
* U poljima za unos lozinke sa omogućenom opcijom za izgovaranje utipkanih riječi, višestruke zvjezdice se neće irelevantno najavljivati kod započinjanja novih riječi. (#4402)
* U Microsoft Outlook popisu poruka, stavke se više neće irelevantno najavljivati kao podatkovne stavke. (#4439)
* Prilikom odabira teksta unutar kontrole za uređivanje koda u Eclipse razvojnom okruženju, više se neće najaviti cjelokupan odabir svaki put kada se odabir promijeni. (#2314)
* Različite inačice Eclipse-a, poput Spring Tool Suite-a i inačice uključene u Android Developer Tools paketu se sada prepoznaju kao Eclipse i njima se postupa na odgovarajući način. (#4360, #4454)
* Praćenje miša i istraživanje dodirom u Internet Explorer-u i drugim MSHTML kontrolama (uključujući mnoge Windows 8 aplikacije) sada je puno preciznije na zaslonima visoke rezolucije ili kada se mijenja uvećanje dokumenta. (#3494) 
* Praćenje miša i istraživanje dodirom u Internet Explorer-u i drugim MSHTML kontrolama će sada najaviti naziv za više gumbi. (#4173)
* Pri korištenju Papenmeier BRAILLEX brajičnog retka sa BrxCom-om, tipke na retku sada rade kako treba. (#4614)

### Changes for Developers

* For executables which host many different apps (e.g. javaw.exe), code can now be provided to load specific app modules for each app instead of loading the same app module for all hosted apps. (#4360)
 * See the code documentation for appModuleHandler.AppModule for details.
 * Support for javaw.exe is implemented.

## 2014.3

### New Features

* The sounds played when NVDA starts and exits can be disabled via a new option in the General Settings dialog. (#834)
* Help for add-ons can be accessed from the Add-ons Manager for add-ons which support this. (#2694)
* Support for the Calendar in Microsoft Outlook 2007 and above (#2943) including:
 * Announcement of the current time when moving around with the arrow keys.
 * Indication if the selected time is within any appointments.
 * announcement of the selected appointment when pressing tab.
 * Smart filtering of the date so as to only announce the date if the new selected time or appointment is on a different day to the last.
* Enhanced support for the Inbox and other message lists in Microsoft Outlook 2010 and above (#3834) including:
 * The ability to silence column headers (from, subject, etc.) by turning off the Report Table row and column headers option in Document Formatting settings.
 * The ability to use table navigation commands (control + alt + arrows) to move through the individual columns. 
* Microsoft word: If an inline image has no alternative text set, NVDA will instead report the title of the image if the author has provided one. (#4193)
* Microsoft Word: NVDA can now report paragraph indenting with  the report formatting command (NVDA+f). It can also be reported automatically when the new Report Paragraph indenting option is enabled in Document Formatting settings. (#4165)
* Report automatically inserted text such as a new bullet, number or tab indent when pressing enter in editable documents and text fields. (#4185)
* Microsoft word: Pressing NVDA+alt+c will report  the text of a comment if the cursor is within one. (#3528)
* Improved support for automatic column and row header reading in Microsoft Excel (#3568) including:
 * Support of Excel defined name ranges to identify header cells (compatible with Jaws screen reader) .
 * The set column header (NVDA+shift+c) and set row header (NVDA+shift+r) commands now store the settings in the worksheet so that they are available the next time the sheet is opened, and will be available to other screen readers that support the defined name range scheme.
 * These commands can also now be used multiple times per sheet to set different headers for different regions.
* Support for automatic column and row header reading in Microsoft Word (#3110) including:
 * Support of Microsoft Word bookmarks to identify header cells (compatible with Jaws screen reader).
 -  set column header (NVDA+shift+c) and set row header (NVDA+shift+r) commands  while on the first header cell in a table allow you to tell NVDA that these headers should be reported automatically.  Settings are stored in the document so that they are available the next time the document is opened, and will be available to other screen readers that support the bookmark scheme.
* Microsoft Word: Report the distance from the left edge of the page when the tab key is pressed. (#1353)
* Microsoft Word: provide feedback in speech and braille for most available formatting shortcut keys (bold, italic, underline, alignment, outline level, superscript, subscript and font size). (#1353)
* Microsoft Excel: If the selected cell contains comments, they can be now reported by pressing NVDA+alt+c. (#2920)
* Microsoft Excel: Provide an NVDA-specific dialog to edit the comments on the currently selected cell when pressing Excel's shift+f2 command to enter comment editing mode. (#2920)
* Microsoft Excel: speech and braille feedback for many more selection movement shortcuts (#4211) including:
 * Vertical page movement (pageUp and pageDown);
 * Horizontal page movement (alt+pageUp and alt+pageDown);
 * Extend selection (the above keys with Shift added); and
 * Selecting the current region (control+shift+8).
* Microsoft Excel: The vertical and horizontal  alignment for cells can now be reported with the report formatting command (NVDA+f). It can also be reported automatically if the Report alignment option in Document Formatting settings is enabled. (#4212)
* Microsoft Excel: The style of a cell can now be reported with the report formatting command (NVDA+f). It can also be reported automatically if the Report Style option in Document formatting settings is enabled. (#4213)
* Microsoft PowerPoint: when moving shapes around a slide with the arrow keys, the shape's current location is now reported (#4214) including:
 * The distance between the shape and each of the  slide edges is reported.
 * If the shape covers or is covered by another shape, then the distance overlapped and the overlapped shape are reported.
 * To report this information at any time without moving a shape, press the report location command (NVDA+delete).
 * When selecting a shape, if it is covered by another shape, NVDA will report that it is obscured.
* The report location command (NVDA+delete) is more context specific in some situations. (#4219)
 * In standard edit fields and browse mode, the cursor position as a percentage through the content and its screen coordinates are reported.
 * On shapes in PowerPoint Presentations, position of the shape relative to the slide and other shapes is reported.
 * Pressing this command twice will produce the previous behaviour of reporting the location information for the entire control.
* New language: Catalan.

### Changes

* Updated liblouis braille translator to 2.5.4. (#4103)

### Bug Fixes

* In Google Chrome and Chrome-based browsers, certain chunks of text (such as those with emphasis) are no longer repeated when reporting the text of an alert or dialog. (#4066)
* In browse mode in Mozilla applications, pressing enter on a button, etc. no longer fails to activate it (or activates the wrong control) in certain cases such as the buttons at the top of Facebook. (#4106)
* Useless information is no longer announced when tabbing in iTunes. (#4128)
* In certain lists in iTunes such as the Music list, moving to the next item using object navigation now works correctly. (#4129)
* HTML elements considered headings because of WAI ARIA markup are now included in the Browse mode Elements list and quick navigation for Internet Explorer documents. (#4140)
* Following same-page links in recent versions of Internet Explorer now correctly moves to and reports the destination position in browse mode  documents. (#4134)
* Microsoft Outlook 2010 and above: Overall access to secure dialogs such as the New profiles and mail setup dialogs has been improved. (#4090, #4091, #4095)
* Microsoft Outlook: Useless verbosity has been decreased in command toolbars when navigating through  certain dialogs. (#4096, #3407)
* Microsoft word: Tabbing to a blank cell in a table no longer incorrectly announces exiting the table. (#4151)
* Microsoft Word: The first character past the end of a table (including a new blank line) is no longer incorrectly considered to be inside the table. (#4152)
* Microsoft Word 2010 spell check dialog: The actual misspelled word is reported rather than  inappropriately reporting just the first bold word. (#3431)
* In browse mode in Internet Explorer and other MSHTML controls, tabbing or using single letter navigation to move to form fields again reports the label in many cases where it didn't (specifically, where HTML label elements are used). (#4170)
* Microsoft Word: Reporting the existence and placement of comments is more accurate. (#3528)
* Navigation of certain dialogs in MS Office products such as Word, Excel and Outlook has been improved by no longer reporting particular control container toolbars which are not useful to the user. (#4198) 
* Task panes such as clipboard manager or File recovery no longer accidentilly seem to gain focus when opening an application such as Microsoft Word or Excel, which was sometimes causing the user to have to switch away from and back to the application to use the document or spreadsheet.  (#4199)
* NVDA no longer fails to run on recent Windows Operating Systems if the user's Windows language is set to Serbian (Latin). (#4203)
* Pressing numlock while in input help mode now correctly toggles numlock, rather than causing the keyboard and the Operating System to become out of sync in regards to the state of this key. (#4226)
* In Google Chrome, the title of the document is again reported when switching tabs. In NVDA 2014.2, this did not occur in some cases. (#4222)
* In Google Chrome and Chrome-based browsers, the URL of the document is no longer reported when reporting the document. (#4223)
* When running say all with the No speech synthesizer selected (useful for automated testing), say all will now complete instead of stopping after the first few lines. (#4225)
* Microsoft Outlook's Signature dialog: The Signature editing field is now accessible, allowing for full cursor tracking and format detection. (#3833)
* Microsoft Word: When reading the last line of a table cell, the entire table cell is no longer read. (#3421)
* Microsoft Word: When reading the first or last line of a table of contents, the entire table of contents is no longer read. (#3421)
* When speaking typed words and in some other cases, words are no longer incorrectly broken at marks such as vowel signs and virama in Indic languages. (#4254)
* Numeric editable text fields in GoldWave are now handled correctly. (#670)
* Microsoft Word: when moving by paragraph with control+downArrow / control+upArrow, it is no longer necessary to press them twice if moving through bulleted or numbered lists. (#3290)

### Changes for Developers

* NVDA now has unified support for add-on documentation. See the Add-on Documentation section of the Developer Guide for details. (#2694)
* When providing gesture bindings on a ScriptableObject via __gestures, it is now possible to provide the None keyword as the script. This unbinds the gesture in any base classes. (#4240)
* It is now possible to change the shortcut key used to start NVDA for locales where the normal shortcut causes problems. (#2209)
 * This is done via gettext.
 * Note that the text for the Create desktop shortcut option in the Install NVDA dialog, as well as the shortcut key in the User Guide, must also be updated.

## 2014.2

### New Features

* Announcement of text selection is now possible in some custom edit fields where display information is used. (#770)
* In accessible Java applications, position information is now announced for radio buttons and other controls that expose group information. (#3754)
* In accessible Java applications, keyboard shortcuts are now announced for controls that have them. (#3881)
* In browse mode, labels on landmarks are now reported. They are also included in the Elements List dialog. (#1195)
* In browse mode, labelled regions are now treated as landmarks. (#3741)
* In Internet Explorer documents and applications, Live Regions (part of the W3c ARIA standard) are now supported, thus allowing web authors to mark particular content to be automatically spoken as it changes. (#1846)

### Changes

* When exiting a dialog or application within a browse mode document, the browse mode document's name and type is no longer announced. (#4069)

### Bug Fixes

* The standard Windows System menu is no longer accidentally silenced in Java applications. (#3882)
* When copying text from screen review, line breaks are no longer ignored. (#3900)
* Pointless whitespace objects are no longer reported in some applications when the focus changes or when using object navigation with simple review enabled. (#3839)
* Message boxes and other dialogs produced by NVDA again cause previous speech to be canceled before announcing the dialog.
* In browse mode, the labels of controls such as links and buttons are now rendered correctly where the label has been overridden by the author for accessibility purposes (specifically, using aria-label or aria-labelledby). (#1354)
* In Browse mode in Internet Explorer, text contained within an element marked as presentational (ARIA role="presentation") is no longer inappropriately ignored. (#4031)
* It is now again possible to type Vietnamese text using the Unikey software. To do this, uncheck the new Handle keys from other applications checkbox in NVDA's Keyboard settings dialog. (#4043)
* In browse mode, radio and check menu items are reported as controls instead of just clickable text. (#4092)
* NVDA no longer incorrectly switches from focus mode to browse mode when a radio or check menu item is focused. (#4092)
* In Microsoft PowerPoint with speaking of typed words enabled, characters erased with backspace are no longer announced as part of the typed word. (#3231)
* In Microsoft Office 2010 Options dialogs, the labels of combo boxes are reported correctly. (#4056)
* In browse mode in Mozilla applications, using quick navigation commands to move to the next or previous button or form field now includes toggle buttons as expected. (#4098)
* The content of alerts in Mozilla applications is no longer reported twice. (#3481)
* In browse mode, containers and landmarks are no longer inappropriately repeated while navigating within them at the same time as page content is changing (e.g. navigating the Facebook and Twitter websites). (#2199)
* NVDA recovers in more cases when switching away from applications that stop responding. (#3825)
* The caret (insertion point) again correctly updates when doing a sayAll command while in editable text drawn directly to the screen. (#4125)

## 2014.1

### New Features

* Support for Microsoft PowerPoint 2013. Note that protected view is not supported. (#3578)
* In Microsoft word and Excel, NVDA can now read the selected symbol when choosing symbols using the Insert Symbols dialog. (#3538)
* It is now possible to choose if content in documents should be identified as clickable via a new option in the Document Formatting settings dialog. This option is on by default in accordance with the previous behavior. (#3556)
* Support for braille displays connected via Bluetooth on a computer running the Widcomm Bluetooth Software. (#2418)
* When editing text in PowerPoint, hyperlinks are now reported. (#3416)
* When in ARIA applications or dialogs on the web, it is now possible to force NVDA to switch to browse mode with NVDA+space allowing document-style navigation of the application or dialog. (#2023)
* In Outlook Express / Windows Mail / Windows Live Mail, NVDA now reports if a message has an attachment or is flagged. (#1594)
* When navigating tables in accessible Java applications, row and column coordinates are now reported, including  column and  row headers if they exist. (#3756)

### Changes

* For Papenmeier braille displays, the move to flat review/focus command has been removed. Users can assign their own keys using the Input Gestures dialog. (#3652)
* NVDA now relies  on the Microsoft VC runtime version 11, which means it can no longer be run on Operating systems older than Windows XP Service Pack 2 or Windows Server 2003 Service Pack 1.
* Punctuation level Some will now speak star (*) and plus (+) characters. (#3614)
* Upgraded eSpeak to version 1.48.04 which includes many language fixes and fixes several crashes. (#3842, #3739, #3860)

### Bug Fixes

* When moving around or selecting cells in Microsoft Excel, NVDA should no longer inappropriately announce the old cell rather than the new cell when Microsoft Excel is slow to move the selection. (#3558)
* NVDA properly handles opening a dropdown list for a cell in Microsoft Excel via the context menu. (#3586)
* New page content in iTunes 11 store pages is now shown properly in browse mode when following a link in the store or when opening the store initially. (#3625)
* Buttons for previewing songs in the iTunes 11 store now show their label in browse mode. (#3638)
* In browse mode in Google Chrome, the labels of check boxes and radio buttons are now rendered correctly. (#1562)
* In Instantbird, NVDA no longer reports useless information every time you move to a contact in the Contacts list. (#2667)
* In browse mode in Adobe Reader, the correct text is now rendered for buttons, etc. where the label has been overridden using a tooltip or other means. (#3640)
* In browse mode in Adobe Reader, extraneous graphics containing the text "mc-ref" will no longer be rendered. (#3645)
* NVDA no longer reports all cells in Microsoft Excel as underlined in their formatting information. (#3669)
* No longer show meaningless characters in browse mode documents such as those found in the Unicode private usage range. In some cases these were stopping more useful labels from being shown. (#2963)
* Input composition for entering east-asian characters no longer fails in PuTTY. (#3432)
* Navigating in a document after a canceled say all no longer results in NVDA sometimes incorrectly announcing that you have left a field (such as a table) lower in the document that the say all never actually spoke. (#3688)
* When using browse mode quick navigation commands  while in say all with skim reading enabled, NVDA more accurately announces the new field; e.g. it now says a heading is a heading, rather than just its text. (#3689)
* The jump to end or start of container quick navigation commands now honor the skim reading during say all setting; i.e. they will no longer cancel the current say all. (#3675)
* Touch gesture names listed in NVDA's Input Gestures dialog are now friendly and localized. (#3624)
* NVDA no longer causes certain programs to crash when moving the mouse over their rich edit (TRichEdit) controls. Programs include Jarte 5.1 and BRfácil. (#3693, #3603, #3581)
* In Internet Explorer and other MSHTML controls, containers such as tables marked as presentation by ARIA are no longer reported to the user. (#3713)
* in Microsoft Word, NVDA no longer inappropriately repeats table row and column information for a cell on a braille display multiple times. (#3702)
* In languages which use a space as a digit group/thousands separator such as French and German, numbers from separate chunks of text are no longer pronounced as a single number. This was particularly problematic for table cells containing numbers. (#3698)
* Braille no longer sometimes fails to update when the system caret is moved in Microsoft Word 2013. (#3784)
* When positioned on the first character of a heading in Microsoft Word, the text communicating it is a heading (including the level) no longer disappears off a braille display. (#3701)
* When a configuration profile is triggered for an application and that application is exited, NVDA no longer sometimes fails to deactivate the profile. (#3732)
* When entering Asian input into a control within NVDA itself (e.g. the browse mode Find dialog), "NVDA" is no longer incorrectly reported in place of the candidate. (#3726)
* The tabs in the Outlook 2013 options dialog are now reported. (#3826)
* Improved support for ARIA live regions in Firefox and other Mozilla Gecko applications:
 * Support for aria-atomic updates and filtering of aria-busy updates. (#2640)
 * Alternative text (such as alt attribute or aria-label) is included if there is no other useful text. (#3329)
 * Live region updates are no longer silenced if they occur at the same time as the focus moves. (#3777)
* Certain presentation elements in Firefox and other Mozilla Gecko applications are no longer inappropriately shown in browse mode (specifically, when the element is marked with aria-presentation but it is also focusable). (#3781)
* A performance improvement when navigating a document in Microsoft Word with spelling errors enabled. (#3785)
* Several fixes to the support for accessible Java applications:
 * The initially focused control in a frame or dialog no longer fails to be reported when the frame or dialog comes to the foreground. (#3753)
 * Unuseful position information is no longer announced for radio buttons (e.g. 1 of 1). (#3754)
 * Better reporting of JComboBox controls (html no longer reported, better reporting of expanded and collapsed states). (#3755)
 * When reporting the text of dialogs, some text that was previously missing is now included. (#3757)
 * Changes to the name, value or description of the focused control is now reported more accurately. (#3770)
* Fix a crash in NVDA seen in Windows 8 when focusing on certain RichEdit controls containing large amounts of text (e.g. NVDA's log viewer, windbg). (#3867)
* On systems with a high DPI display setting (which occurs by default for many modern screens), NVDA no longer routes the mouse to the wrong location in some applications. (#3758, #3703)
* Fixed an occasional problem when browsing the web where NVDA would stop working correctly until restarted, even though it didn't crash or freeze. (#3804)
* A Papenmeier braille display can now be used even if a Papenmeier display has never been connected via USB. (#3712)
* NVDA no longer freezes when the Papenmeier BRAILLEX older models braille display is selected without a display connected.

### Changes for Developers

* AppModules now contain productName and productVersion properties. This info is also now included in Developer Info (NVDA+f1). (#1625)
* In the Python Console, you can now press the tab key to complete the current identifier. (#433)
 * If there are multiple possibilities, you can press tab a second time to choose from a list.

## 2013.3

### New Features

* Form fields are now reported in Microsoft word documents. (#2295)
* NVDA can now announce revision information in Microsoft Word when Track Changes is enabled. Note that Report editor revisions in NVDA's document settings dialog (off by default) must be enabled also for them to be announced. (#1670)
* Dropdown lists in Microsoft Excel 2003 through 2010 are now announced when opened and navigated around. (#3382)
* a new 'Allow Skim Reading in Say All' option in the Keyboard settings dialog allows navigating through a document with browse mode quick navigation and line / paragraph movement commands, while remaining in say all. This option is off by default. (#2766) 
* There is now an Input Gestures dialog to allow simpler customization of the input gestures (such as keys on the keyboard) for NVDA commands. (#1532)
* You can now have different settings for different situations using configuration profiles. Profiles can be activated manually or automatically (e.g. for a particular application). (#87, #667, #1913)
* In Microsoft Excel, cells that are links are now announced as links. (#3042)
* In Microsoft Excel, the existence of comments on a cell is now reported to the user. (#2921)

### Bug Fixes

* Zend Studio now functions the same as Eclipse. (#3420)
* The changed state of certain checkboxes in the Microsoft Outlook 2010 message rules dialog are now reported automatically. (#3063)
* NVDA will now report the pinned state for pinned controls such as tabs in Mozilla Firefox. (#3372)
* It is now possible to bind scripts to keyboard gestures containing Alt and/or Windows keys as modifiers. Previously, if this was done, performing the script would cause the Start Menu or menu bar to be activated. (#3472)
* Selecting text in browse mode documents (e.g. using control+shift+end) no longer causes the keyboard layout to be switched on systems with multiple keyboard layouts installed. (#3472)
* Internet Explorer should no longer crash or become unusable when closing NVDA. (#3397)
* Physical movement and other events on some newer computers are no longer treated as inappropriate key presses. Previously, this silenced speech and sometimes triggered NVDA commands. (#3468)
* NVDA now behaves as expected in Poedit 1.5.7. Users using earlier versions will need to update. (#3485)
* NVDA can now read protected documents in Microsoft Word 2010,  no longer causing Microsoft Word to crash. (#1686)
* If an unknown command line switch is given when launching the NVDA distribution package, it no longer causes an endless loop of error message dialogs. (#3463)
* NVDA no longer fails to report alt text of graphics and objects in Microsoft Word if the alt text contains quotes or other non-standard characters. (#3579)
* The number of items for certain horizontal lists in Browse mode is now correct. Previously it may have been double the actual amount. (#2151)
* When pressing control+a in a Microsoft Excel worksheet, the updated selection will now be reported. (#3043)
* NVDA can now correctly read XHTML documents in Microsoft Internet Explorer and other MSHTML controls. (#3542)
* Keyboard settings dialog: if no key has been chosen to be used as the NVDA key, an error is presented to the user when dismissing the dialog. At least one key must be chosen for proper usage of NVDA. (#2871)
* In Microsoft Excel, NVDA now announces merged cells differently to multiple selected cells. (#3567)
* The browse mode cursor is no longer positioned incorrectly when leaving a dialog or application inside the document. (#3145)
* Fixed an issue where the HumanWare Brailliant BI/B series braille display driver wasn't presented as an option in the Braille Settings dialog on some systems, even though such a display was connected via USB.
* NVDA no longer fails  to switch to screen review when the navigator object has no actual screen location. In this case the review cursor is now placed at the top of the screen. (#3454)
* Fixed an issue which caused the Freedom Scientific braille display driver to fail when the port was set to USB in some circumstances. (#3509, #3662)
* Fixed an issue where keys on Freedom Scientific braille displays weren't detected in some circumstances. (#3401, #3662)

### Changes for Developers

* You can specify the category to be displayed to the user for scripts using the scriptCategory attribute on ScriptableObject classes and the category attribute on script methods. See the documentation for baseObject.ScriptableObject for more details. (#1532)
* config.save is deprecated and may be removed in a future release. Use config.conf.save instead. (#667)
* config.validateConfig is deprecated and may be removed in a future release. Add-ons which need this should provide their own implementation. (#667, #3632)

## 2013.2

### New Features

* Support for the Chromium Embedded Framework, which is a web browser control used in several applications. (#3108)
* New eSpeak voice variant: Iven3.
* In Skype, new chat messages are reported automatically while the conversation is focused. (#2298)
* Support for Tween, including reporting of tab names and less verbosity when reading tweets.
* You can now disable displaying of NVDA messages on a braille display by setting the message timeout to 0 in the Braille Settings dialog. (#2482)
* In the Add-ons Manager, there is now a Get Add-ons button to open the NVDA Add-ons web site where you can browse and download available add-ons. (#3209)
* In the NVDA Welcome dialog which always appears the first time you run NVDA, you can now specify whether NVDA starts automatically after you log on to Windows. (#2234)
* Sleep mode is automatically enabled when using Dolphin Cicero. (#2055)
* The Windows x64 version of Miranda IM/Miranda NG is now supported. (#3296)
* Search suggestions in the Windows 8.1 Start Screen are automatically reported. (#3322)
* Support for navigating and editing spreadsheets in Microsoft Excel 2013. (#3360)
* The Freedom Scientific Focus 14 Blue and Focus 80 Blue braille displays, as well as the Focus 40 Blue in certain configurations that weren't supported previously, are now supported when connected via Bluetooth. (#3307)
* Auto complete suggestions are now reported in Outlook 2010. (#2816)
* New braille translation tables: English (U.K.) computer braille, Korean grade 2, Russian braille for computer code.
* New language: Farsi. (#1427)

### Changes

* On a touch screen, performing a single finger flick left or right when in object mode now moves previous or next through all objects, not just those in the current container. Use 2-finger flick left or right to perform the original action of moving to the previous or next object in the current container.
* the Report layout tables checkbox found in the Browse Mode settings dialog has now been renamed to Include layout tables to reflect that quick navigation also will not locate them if the checkbox is unchecked. (#3140)
* Flat review has been replaced with object, document and screen review modes. (#2996)
 * Object review reviews text just within the navigator object, document review reviews all text in a browse mode document (if any) and screen review reviews text on the screen for the current application.
 * The commands that previously move to/from flat review now toggle between these new review modes.
 * The navigator object automatically follows the review cursor such that it remains the deepest object at the position of the review cursor when in document or screen review modes.
 * After switching to screen review mode, NVDA will stay in this mode until you explicitly switch back to document or object review mode.
 * When in document or object review mode, NVDA may automatically switch between these two modes depending on whether you are moving around a browse mode document or not.
* Updated liblouis braille translator to 2.5.3. (#3371)

### Bug Fixes

* Activating an object now announces the action before the activation, rather than the action after the activation (e.g. expand when expanding rather than collapse). (#2982)
* More accurate reading and cursor tracking in  various input fields for recent versions of Skype, such as chat and search fields. (#1601, #3036)
* In the Skype recent conversations list, the number of new events is now read for each conversation if relevant. (#1446)
* Improvements to cursor tracking and reading order for right-to-left text written to the screen; e.g. editing Arabic text in  Microsoft Excel. (#1601) 
* Quick navigation to buttons and form fields will now locate links marked as buttons for accessibility purposes in Internet Explorer. (#2750)
* In browse mode, the content inside tree views is no longer rendered, as a flattened representation isn't useful. You can press enter on a tree view to interact with it in focus mode. (#3023)
* Pressing alt+downArrow or alt+upArrow to expand a combo box while in focus mode no longer incorrectly switches to browse mode. (#2340)
* In Internet Explorer 10, table cells no longer activate focus mode, unless they have been explicitly made focusable by the web author. (#3248)
* NVDA no longer fails to start if the system time is earlier than the last check for an update. (#3260)
* If a progress bar is shown on a braille display, the braille display is updated when the progress bar changes. (#3258)
* In browse mode in Mozilla applications, table captions are no longer rendered twice. In addition, the summary is rendered when there is also a caption. (#3196)
* When changing input languages in Windows 8, NVDA now speaks the correct language rather than the previous one.
* NVDA now announces IME conversion mode changes in Windows 8.
* NVDA no longer announces garbage on the Desktop when the Google Japanese or Atok IME input methods are in use. (#3234)
* In Windows 7 and above, NVDA no longer inappropriately announces speech recognition or touch input as a keyboard language change.
* NVDA no longer announces a particular special character (0x7f) when pressing control+backspace in some editors when speak typed characters is enabled. (#3315)
* eSpeak no longer inappropriately changes in pitch, volume, etc. when NVDA reads text containing certain control characters or XML. (#3334) (regression of #437)
* In Java applications, changes to the label or value of the focused control are now announced automatically, and are reflected when subsequently querying the control. (#3119)
* In Scintilla controls, lines are now reported correctly when word wrap is enabled. (#885)
* In Mozilla applications, the name of read-only list items is now correctly reported; e.g. when navigating tweets in focus mode on twitter.com. (#3327)
* Confirmation dialogs in Microsoft Office 2013 now have their content automatically read when they appear. 
* Performance improvements when navigating certain tables in Microsoft Word. (#3326)
* NVDA's table navigation commands (control+alt+arrows) function better in certain Microsoft Word tables where a cell spans multiple rows.
* If the Add-ons Manager is already open, activating it again (either from the Tools menu or by opening an add-on file) no longer fails or makes it impossible to close the Add-ons Manager. (#3351)
* NVDA no longer freezes in certain dialogs when Japanese or Chinese Office 2010 IME is in use. (#3064)
* Multiple spaces are no longer compressed to just one space on braille displays. (#1366)
* Zend Eclipse PHP Developer Tools now functions the same as Eclipse. (#3353)
* In Internet Explorer, It is again not necessary to press tab to interact with an embedded object (such as Flash content) after pressing enter on it. (#3364)
* When editing text in Microsoft PowerPoint, the last line is no longer reported as the line above, if the final line is blank. (#3403)
* In Microsoft PowerPoint, objects are no longer sometimes spoken twice when you select them or choose to edit them. (#3394)
* NVDA no longer causes Adobe Reader to crash or freeze for certain badly formed PDF documents containing rows outside of tables. (#3399)
* NVDA now correctly detects the next slide with focus when deleting a slide in Microsoft PowerPoint's thumbnails view. (#3415)

### Changes for Developers

* windowUtils.findDescendantWindow has been added to search for a descendant window (HWND) matching the specified visibility, control ID and/or class name.
* The remote Python console no longer times out after 10 seconds while waiting for input. (#3126)
* Inclusion of the bisect module in binary builds is deprecated and may be removed in a future release. (#3368)
 * Add-ons which depend on bisect (including the urllib2 module) should be updated to include this module.

## 2013.1.1

This release fixes the problem where NVDA crashed when started if configured to use the Irish language, as well as including updates to translations and some other bug fixes.

### Bug Fixes

* Correct characters are produced when typing in NVDA's own user interface while using a Korean or Japanese input method while it is the default method. (#2909)
* In Internet Explorer and other MSHTML controls, fields marked as containing an invalid entry are now handled correctly. (#3256)
* NVDA no longer crashes when started if it is configured to use the Irish language.

## 2013.1

Highlights of this release include a more intuitive and consistent laptop keyboard layout; basic support for Microsoft PowerPoint; support for long descriptions in web browsers; and support for input of computer braille for braille displays which have a braille keyboard.

### Important

#### New Laptop Keyboard Layout

The laptop keyboard layout has been completely redesigned in order to make it more intuitive and consistent.
The new layout uses the arrow keys in combination with the NVDA key and other modifiers for review commands.

Please note the following changes to commonly used commands:

| Name |Key|
|---|---|
|Say all |NVDA+a|
|Read current line |NVDA+l|
|Read current text selection |NVDA+shift+s|
|Report status bar |NVDA+shift+end|

In addition, among other changes, all of the object navigation, text review, mouse click and synth settings ring commands have changed.
Please see the [Commands Quick Reference](keyCommands.html) document for the new keys.

### New Features

* Basic support for editing and reading Microsoft PowerPoint presentations. (#501)
* Basic support for reading and writing messages in Lotus Notes 8.5. (#543)
* Support for automatic language switching when reading documents in Microsoft Word. (#2047) 
* In Browse mode for MSHTML (e.g. Internet Explorer) and Gecko (e.g. Firefox), the existence of long descriptions are now announced. It's also possible to open the long description in a new window by pressing NVDA+d. (#809)
* Notifications in Internet Explorer 9 and above are now spoken (such as content blocking or file downloads). (#2343)
* Automatic reporting of table row and column headers is now supported for browse mode documents in Internet Explorer and other MSHTML controls. (#778)
* New language: Aragonese, Irish
* New braille translation tables: Danish grade 2, Korean grade 1. (#2737)
* Support for braille displays connected via bluetooth on a computer running the Bluetooth Stack for Windows by Toshiba. (#2419)
* Support for port selection when using Freedom Scientific displays (Automatic, USB or Bluetooth).
* Support for the BrailleNote family of notetakers from HumanWare when acting as a braille terminal for a screen reader. (#2012)
* Support for older models of Papenmeier BRAILLEX braille displays. (#2679)
* Support for input of computer braille for braille displays which have a braille keyboard. (#808)
* New keyboard settings that allow  the choice for whether NVDA should interrupt speech for typed characters and/or the Enter key. (#698)
* Support for several browsers based on Google Chrome: Rockmelt, BlackHawk, Comodo Dragon and SRWare Iron. (#2236, #2813, #2814, #2815)

### Changes

* Updated liblouis braille translator to 2.5.2. (#2737)
* The laptop keyboard layout has been completely redesigned in order to make it more intuitive and consistent. (#804)
* Updated eSpeak speech synthesizer to 1.47.11. (#2680, #3124, #3132, #3141, #3143, #3172)

### Bug Fixes

* The quick navigation keys for jumping to the next or previous separator in Browse Mode now work in Internet Explorer and other MSHTML controls. (#2781)
* If NVDA falls back to eSpeak or no speech due to the configured speech synthesizer failing when NVDA starts, the configured choice is no longer automatically set to the fallback synthesizer. This means that now, the original synthesizer will be tried again next time NVDA starts. (#2589)
* If NVDA falls back to no braille due to the configured braille display failing when NVDA starts, the configured display is no longer automatically set to no braille. This means that now, the original display will be tried again next time NVDA starts. (#2264)
* In browse mode in Mozilla applications, updates to tables are now rendered correctly. For example, in updated cells, row and column coordinates are reported and table navigation works as it should. (#2784)
* In browse mode in web browsers, certain clickable unlabelled graphics which weren't previously rendered are now rendered correctly. (#2838)
* Earlier and newer versions of SecureCRT are now supported. (#2800)
* For input  methods such as Easy Dots IME under XP, the reading string is now correctly reported.
* The candidate list in the Chinese Simplified Microsoft Pinyin input method under Windows 7 is now correctly read when changing pages with left and right arrow, and when first opening it with Home.
* When custom symbol pronunciation information is saved, the advanced "preserve" field is no longer removed. (#2852)
* When disabling automatic checking for updates, NVDA no longer has to be restarted in order for the change to fully take effect.
* NVDA no longer fails to start if an add-on cannot be removed due to its directory currently being in use by another application. (#2860)
* Tab labels in DropBox's preferences dialog can now be seen with Flat Review.
* If the input language is changed to something other than the default, NVDA now detects keys correctly for commands and input help mode.
* For languages such as German where the + (plus) sign is a single key on the keyboard, it is now possible to bind commands to it by using the word "plus". (#2898)
* In Internet Explorer and other MSHTML controls, block quotes are now reported where appropriate. (#2888)
* The HumanWare Brailliant BI/B series braille display driver can now be selected when the display is connected via Bluetooth but has never been connected via USB.
* Filtering elements in the Browse Mode Elements list with uppercase filter text now returns case-insensitive results just like lowercase rather than nothing at all. (#2951)
* In Mozilla browsers, browse mode can again be used when Flash content is focused. (#2546)
* When using a contracted braille table and expand to computer braille for the word at the cursor is enabled, the braille cursor is now positioned correctly when located after a word wherein a character is represented by multiple braille cells (e.g. capital sign, letter sign, number sign, etc.). (#2947)
* Text selection is now correctly shown on a braille display in applications such as Microsoft word 2003 and Internet Explorer edit controls.
* It is again possible to select text in a backward direction in Microsoft Word while Braille is enabled.
* When reviewing,  backspacing or deleting characters  In Scintilla edit controls, NVDA correctly announces multibyte characters. (#2855)
* NVDA will no longer fail to install when the user's profile path contains certain multibyte characters. (#2729)
* Reporting of groups for List View controls (SysListview32) in 64-bit applications no longer causes an error.
* In browse mode in Mozilla applications, text content is no longer incorrectly treated as editable in some rare cases. (#2959)
* In IBM Lotus Symphony and OpenOffice, moving the caret now moves the review cursor if appropriate.
* Adobe Flash content is now accessible in Internet Explorer in Windows 8. (#2454)
* Fixed Bluetooth support for Papenmeier Braillex Trio. (#2995)
* Fixed inability to use certain Microsoft Speech API version 5 voices such as Koba Speech 2 voices. (#2629)
* In applications using the Java Access Bridge, braille displays are now updated correctly when the caret moves in editable text fields . (#3107)
* Support the form landmark in browse mode documents that support landmarks. (#2997) 
* The eSpeak synthesizer driver now handles reading by character more appropriately (e.g. announcing a foreign letter's name or value rather than just its sound or generic name). (#3106)
* NVDA no longer fails to copy user settings for use on logon and other secure screens when the user's profile path contains non-ASCII characters. (#3092)
* NVDA no longer freezes when using Asian character input in some .NET applications. (#3005)
* it is now possible to use browse mode for pages in Internet Explorer 10 when in standards mode; e.g. [www.gmail.com](http://www.gmail.com) login page. (#3151)

### Changes for Developers

* Braille display drivers can now support manual port selection. (#426)
 * This is most useful for braille displays which support connection via a legacy serial port.
 * This is done using the getPossiblePorts class method on the BrailleDisplayDriver class.
* Braille input from braille keyboards is now supported. (#808)
 * Braille input is encompassed by the brailleInput.BrailleInputGesture class or a subclass thereof.
 * Subclasses of braille.BrailleDisplayGesture (as implemented in braille display drivers) can also inherit from brailleInput.BrailleInputGesture. This allows display commands and braille input to be handled by the same gesture class.
* You can now use comHelper.getActiveObject to get an active COM object from a normal process when NVDA is running with the UIAccess privilege. (#2483)

## 2012.3

Highlights of this release include support for Asian character input; experimental support for touch screens on Windows 8; reporting of page numbers and improved support for tables in Adobe Reader; table navigation commands in focused table rows and Windows list-view controls; support for several more braille displays; and reporting of row and column headers in Microsoft Excel.

### New Features

* NVDA can now support Asian character input using IME and text service input methods in all applications, Including:
 * Reporting and navigation of candidate lists;
 * Reporting and navigation of composition strings; and
 * Reporting of reading strings.
* The presence of underline and strikethrough is now reported in Adobe Reader documents. (#2410)
* When the Windows Sticky Keys function is enabled, the NVDA modifier key will now behave like other modifier keys. This allows you to use the NVDA modifier key without needing to hold it down while you press other keys. (#230)
* Automatic reporting of column and row headers is now supported in Microsoft Excel. Press NVDA+shift+c to set the row containing column headers and NVDA+shift+r to set the column containing row headers. Press either command twice in quick succession to clear the setting. (#1519)
* Support for HIMS Braille Sense, Braille EDGE and SyncBraille braille displays. (#1266, #1267)
* When Windows 8 Toast notifications appear, NVDA will report them if reporting of help balloons is enabled. (#2143)
* Experimental support for Touch screens on Windows 8, including:
 * Reading text directly under your finger while moving it around
 * Many gestures for performing object navigation, text review, and other NVDA commands.
* Support for VIP Mud. (#1728)
* In Adobe Reader, if a table has a summary, it is now presented. (#2465)
* In Adobe Reader, table row and column headers can now be reported. (#2193, #2527, #2528)
* New languages: Amharic, Korean, Nepali, Slovenian.
* NVDA can now read auto complete suggestions when entering email addresses in Microsoft Outlook 2007. (#689)
* New eSpeak voice variants: Gene, Gene2. (#2512)
* In Adobe Reader, page numbers can now be reported. (#2534)
 * In Reader XI, page labels are reported where present, reflecting changes to page numbering in different sections, etc. In earlier versions, this is not possible and only sequential page numbers are reported.
* It is now possible to reset NVDA's configuration to factory defaults either by pressing NVDA+control+r three times quickly or by choosing Reset to Factory Defaults from the NVDA menu. (#2086)
* Support for the Seika Version 3, 4 and 5 and Seika80 braille displays from Nippon Telesoft. (#2452)
* The first and last top routing buttons on Freedom Scientific PAC Mate and Focus Braille displays can now be used to scroll  backward and forward. (#2556)
* Many more features are supported on Freedom Scientific Focus Braille displays such as advance bars, rocker bars and certain dot combinations for common actions. (#2516)
* In applications using IAccessible2 such as Mozilla applications, table row and column headers can now be reported outside of browse mode. (#926)
* Preliminary support for the document control in Microsoft Word 2013. (#2543)
* Text alignment can now be reported in applications using IAccessible2 such as Mozilla applications. (#2612)
* When a table row or standard Windows list-view control with multiple columns is focused, you can now use the table navigation commands to access individual cells. (#828)
* New braille translation tables: Estonian grade 0, Portuguese 8 dot computer braille, Italian 6 dot computer braille. (#2319, #2662)
* If NVDA is installed on the system, directly opening an NVDA add-on package (e.g. from Windows Explorer or after downloading in a web browser) will install it into NVDA. (#2306)
* Support for newer models of Papenmeier BRAILLEX braille displays. (#1265)
* Position information (e.g. 1 of 4) is now reported for Windows Explorer list items on Windows 7 and above. This also includes any UIAutomation controls that support the itemIndex and itemCount custom properties. (#2643)

### Changes

* In the NVDA Review Cursor preferences dialog, the Follow keyboard focus option has been renamed to Follow system focus for consistency with terminology used elsewhere in NVDA.
* When braille is tethered to review and the cursor is on an object which is not a text object (e.g. an editable text field), cursor routing keys will now activate the object. (#2386)
* The Save Settings On Exit option is now on by default for new configurations.
* When updating a previously installed copy of NVDA, the desktop shortcut key is no longer forced back to control+alt+n if it was manually changed to something different by the user. (#2572)
* The add-ons list in the Add-ons Manager now shows the package name before its status. (#2548)
* If installing the same or another version of a currently installed add-on, NVDA will ask if you wish to update the add-on, rather than just showing an error and aborting installation. (#2501)
* Object navigation commands (except the report current object command) now report with less verbosity. You can still obtain the extra information by using the report current object command. (#2560)
* Updated liblouis braille translator to 2.5.1. (#2319, #2480, #2662, #2672)
* The NVDA Key Commands Quick Reference document has been renamed to Commands Quick Reference, as it now includes touch commands as well as keyboard commands.
* The Elements list in Browse mode will now remember the last element type shown (e.g. links, headings or landmarks) each time the dialog is shown within the same session of NVDA. (#365)
* Most Metro apps in Windows 8 (e.g. Mail, Calendar) no longer activate Browse Mode for the entire app.
* Updated Handy Tech BrailleDriver COM-Server to 1.4.2.0.

### Bug Fixes

* In Windows Vista and later, NVDA no longer incorrectly treats the Windows key as being held down when unlocking Windows after locking it by pressing Windows+l. (#1856)
* In Adobe Reader, row headers are now correctly recognised as table cells; i.e. coordinates are reported and they can be accessed using table navigation commands. (#2444)
* In Adobe Reader, table cells spanning more than one column and/or row are now handled correctly. (#2437, #2438, #2450)
* The NVDA distribution package now checks its integrity before executing. (#2475)
* Temporary download files are now removed if downloading of an NVDA update fails. (#2477)
* NVDA will no longer freeze when it is running as an administrator while copying the user configuration to the system configuration (for use on Windows logon and other secure screens). (#2485)
* Tiles on the Windows 8 Start Screen are now presented better in speech and braille. The name is no longer repeated, unselected is no longer reported on all tiles, and live status information is presented  as the description of the tile (e.g. current temperature for the Weather tile).
* Passwords are no longer announced when reading password fields in Microsoft Outlook and other standard edit controls that are marked as protected. (#2021)
* In Adobe Reader, changes to form fields are now correctly reflected in browse mode. (#2529)
* Improvements to support for the Microsoft Word Spell Checker, including more accurate reading of the current spelling error, and the ability to support the spell checker when running an Installed copy of NVDA on Windows Vista or higher.
* Add-ons which include files containing non-English characters can now be installed correctly in most cases. (#2505)
* In Adobe Reader, the language of text is no longer lost when it is updated or scrolled to. (#2544)
* When installing an add-on, the confirmation dialog now correctly shows the localized name of the add-on if available. (#2422)
* In applications using UI Automation (such as .net and Silverlight applications), the calculation of numeric values for controls such as sliders has been corrected. (#2417)
* The configuration for reporting of progress bars is now honoured for the indeterminate progress bars displayed by NVDA when installing, creating a portable copy, etc. (#2574)
* NVDA commands can no longer be executed from a braille display while a secure Windows screen (such as the Lock screen) is active. (#2449)
* In browse mode, braille is now updated if the text being displayed changes. (#2074)
* When on a secure Windows screen such as the Lock screen, messages from applications speaking or displaying braille directly via NVDA are now ignored.
* In Browse mode, it is no longer possible to  fall off the bottom of the document with the right arrow key when on the final character, or by jumping to the end of a container when that container is the last item in the document. (#2463)
* Extraneous content is no longer incorrectly included when reporting the text of dialogs in web applications (specifically, ARIA dialogs with no aria-describedby attribute). (#2390)
* NVDA no longer incorrectly reports or locates certain edit fields in MSHTML documents (e.g. Internet Explorer), specifically where an explicit ARIA role has been used by the web page author. (#2435)
* The backspace key is now handled correctly when speaking typed words in Windows command consoles. (#2586)
* Cell coordinates in Microsoft Excel are now shown again in Braille.
* In Microsoft Word, NVDA no longer leaves you stuck on a paragraph with list formatting when trying to navigate out over a bullet or number with left arrow or control + left arrow. (#2402)
* In browse mode in Mozilla applications, the items in certain list boxes (specifically, ARIA list boxes) are no longer incorrectly rendered.
* In browse mode in Mozilla applications, certain controls that were rendered with an incorrect label or just whitespace are now rendered with the correct label.
* In browse mode in Mozilla applications, some extraneous whitespace has been eliminated.
* In browse mode in web browsers, certain graphics that are explicitly marked as presentational (specifically, with an alt="" attribute) are now correctly ignored.
* In web browsers, NVDA now hides content which is marked as hidden from screen readers (specifically, using the aria-hidden attribute). (#2117)
* Negative currency amounts (e.g. -$123) are now correctly spoken as negative, regardless of symbol level. (#2625)
* During say all, NVDA will no longer incorrectly revert to the default language where a line does not end a sentence. (#2630)
* Font information is now correctly detected in Adobe Reader 10.1 and later. (#2175)
* In Adobe Reader, if alternate text is provided, only that text will be rendered. Previously, extraneous text was sometimes included. (#2174)
* Where a document contains an application, the content of the application is no longer included in browse mode. This prevents unexpectedly moving inside the application when navigating. You can interact with the application in the same way as for embedded objects. (#990)
* In Mozilla applications, the value of spin buttons is now correctly reported when it changes. (#2653)
* Updated support for Adobe Digital Editions so that it works in version 2.0. (#2688)
* Pressing NVDA+upArrow while on a combo box in Internet Explorer and other MSHTML documents will no longer incorrectly read all items. Rather, just the active item will be read. (#2337)
* Speech dictionaries will now properly save when using a number (#) sign within the pattern or replacement fields. (#961)
* Browse mode for MSHTML documents (e.g. Internet Explorer) now correctly displays visible content contained within hidden content (specifically, elements with a style of visibility:visible inside an element with style visibility:hidden). (#2097)
* Links in Windows XP's Security Center no longer report random junk after their names. (#1331)
* UI Automation text controls (e.g.  the search field in the Windows 7 Start Menu) are now  correctly announced when moving the mouse over them rather than staying silent.
* Keyboard layout changes are no longer reported during say all, which was particularly problematic for multilingual documents including Arabic text. (#1676)
* The entire content of some UI Automation editable text controls (e.g. the Search Box in the Windows 7/8 Start Menu) is no longer announced every time it changes.
* When moving between groups on the Windows 8 start screen, unlabeled groups no longer announce their first tile as the name of the group. (#2658)
* When opening the Windows 8 start screen, the focus is correctly placed on the first tile, rather than jumping to the root of the start screen which can confuse navigation. (#2720)
* NVDA will no longer fail to start when the user's profile path contains certain multibyte characters. (#2729)
* In browse mode in Google Chrome, the text of tabs is now rendered correctly.
* In browse mode, menu buttons are now reported correctly.
* In OpenOffice.org/LibreOffice Calc, reading spreadsheet cells now works correctly. (#2765)
* NVDA can again function in the Yahoo! Mail message list when used from Internet Explorer. (#2780)

### Changes for Developers

* Previous log file is now copied to nvda-old.log on NVDA initialization. Therefore, if NVDA crashes or is restarted, logging information from that session is still accessible for inspection. (#916)
* Fetching the role property in chooseNVDAObjectOverlayClasses no longer causes the role to be incorrect and thus not reported on focus for certain objects such as Windows command consoles and Scintilla controls. (#2569)
* The NVDA Preferences, Tools and Help menus are now accessible as attributes on gui.mainFrame.sysTrayIcon named preferencesMenu, toolsMenu and helpMenu, respectively. This allows plugins to more easily add items to these menus.
* The navigatorObject_doDefaultAction script in globalCommands has been renamed to review_activate.
* Gettext message contexts are now supported. This allows multiple translations to be defined for a single English message depending on the context. (#1524)
 * This is done using the pgettext(context, message) function.
 * This is supported for both NVDA itself and add-ons.
 * xgettext and msgfmt from GNU gettext must be used to create any PO and MO files. The Python tools do not support message contexts.
 * For xgettext, pass the --keyword=pgettext:1c,2 command line argument to enable inclusion of message contexts.
 * See http://www.gnu.org/software/gettext/manual/html_node/Contexts.html#Contexts for more information.
* It is now possible to access built-in NVDA modules where they have been overridden by third party modules. See the nvdaBuiltin module for details.
* Add-on translation support can now be used within the add-on installTasks module. (#2715)

## 2012.2.1

This release addresses  several potential security issues (by upgrading Python to 2.7.3).

## 2012.2

Highlights of this release include an in-built installer and  portable  creation feature, automatic updates, easy management of new NVDA add-ons, announcement of graphics in Microsoft Word, support for Windows 8 Metro style apps, and several important bug fixes. 

### New Features

* NVDA can now automatically check for, download and install updates. (#73)
* Extending NVDA's functionality  has been made easier with the addition of an Add-ons Manager (found under Tools in the NVDA menu) allowing you to install and uninstall new NVDA add-on packages (.nvda-addon files) containing plugins and drivers. Note the Add-on manager does not show older custom plugins and drivers manually copied in to your configuration directory. (#213)
* Many more common NVDA features now work in Windows 8 Metro style apps when using an installed release  of NVDA, including speaking of typed characters, and browse mode for web documents (includes support for metro version of Internet Explorer 10). Portable copies of NVDA cannot access metro style apps. (#1801) 
* In browse mode documents (Internet Explorer, Firefox, etc.), you can now  jump to the start and past the end of certain containing elements (such as lists and tables) with shift+, and , respectively. (#123)
* New language: Greek.
* Graphics and alt text are now reported in Microsoft Word Documents. (#2282, #1541)

### Changes

* Announcement of cell coordinates in Microsoft Excel is now after the content rather than before, and is now only included   if the report tables and report table cell coordinates settings are enabled in the Document formatting settings dialog. (#320)
* NVDA is now distributed in one package. Rather than separate portable and installer versions, there is now just one file that, when run, will start a temporary copy of NVDA and will allow you to install or generate a portable distribution. (#1715)
* NVDA is now always installed in to Program Files on all systems. Updating a previous install will also automatically move it if it was not previously installed there.

### Bug Fixes

* With auto language switching enabled, Content such as alt text for graphics and labels for other certain controls in Mozilla Gecko (e.g. Firefox) are now reported in the correct language if marked up appropriately.
* SayAll in BibleSeeker (and other TRxRichEdit controls) no longer stops in the middle of a passage.
* Lists found in the Windows 8 Explorer file properties (permitions tab) and in Windows 8 Windows Update now read correctly.
* Fixed possible freezes in MS Word which would result when it took more than 2 seconds to fetch text from a document (extremely long lines or tables of contents). (#2191)
* Detection of word breaks now works correctly where whitespace is followed by certain punctuation. (#1656)
* In browse mode in Adobe Reader, it is now possible to navigate to headings without a level using quick navigation and the Elements List. (#2181)
* In Winamp, braille is now correctly updated when you move to a different item in the Playlist Editor. (#1912)
* The tree in the Elements List (available for browse mode documents) is now properly sized to show  the text of each element. (#2276)
* In applications using the Java Access Bridge, editable text fields are now presented correctly in braille. (#2284)
* In applications using the java Access Bridge, editable text fields no longer report strange characters in certain circumstances. (#1892)
* In applications using the Java Access Bridge, when at the end of an editable text field, the current line is now reported correctly. (#1892)
* In browse mode in applications using Mozilla Gecko 14 and later (e.g. Firefox 14), quick navigation now works for block quotes and embedded objects. (#2287)
* In Internet Explorer 9, NVDA no longer reads unwanted content when focus moves inside certain landmarks or focusable elements (specifically, a div element which is focusable or has an ARIA landmark role).
* The NVDA icon for the NVDA Desktop and Start Menu shortcuts is now displayed correctly on 64 bit editions of Windows. (#354)

### Changes for Developers

* Due to the replacement of the previous NSIS installer for NVDA with a built-in installer in Python, it is no longer necessary for translaters to maintain a langstrings.txt file for the installer. All localization strings are now managed by gettext po files.

## 2012.1

Highlights of this release include features for more fluent reading of braille; indication of document formatting in braille; access to much more formatting information and improved performance in Microsoft Word; and support for the iTunes Store.

### New Features

* NVDA can announce the number of leading tabs and spaces of the current line in the order that they are entered. This can be enabled by selecting report line indentation in the document formatting dialogue. (#373)
* NVDA can now detect key presses generated from alternative keyboard input emulation such as on-screen keyboards and speech recognition software.
* NVDA can now detect colors in Windows command consoles.
* Bold, italic and underline are now indicated in braille using signs appropriate to the configured translation table. (#538)
* Much more information is now reported in Microsoft Word documents, including:
 * Inline information such as footnote and endnote numbers, heading levels, the existence of comments, table nesting levels, links, and text color;
 * Reporting when entering document sections such as the comments story, footnotes and endnotes stories, and header and footer stories.
* Braille now indicates selected text using dots 7 and 8. (#889)
* Braille now reports information about controls within documents such as links, buttons and headings. (#202)
* Support for the hedo ProfiLine and MobilLine USB braille displays. (#1863, #1897)
* NVDA now avoids splitting words in braille when possible by default. This can be disabled in the Braille Settings dialog. (#1890, #1946)
* It is now possible to have braille displayed by paragraphs instead of lines, which may allow for more fluent reading of large amounts of text. This is configurable using the Read by paragraphs option in the Braille Settings dialog. (#1891)
* In browse mode, you can activate the object under the cursor using a braille display. This is done by pressing the cursor routing key where the cursor is located (which means pressing it twice if the cursor is not already there). (#1893)
* Basic support for web areas in iTunes such as the Store. Other applications using WebKit 1 may also be supported. (#734)
* In books in Adobe Digital Editions 1.8.1 and later, pages are now turned automatically when using say all. (#1978)
* New braille translation tables: Portuguese grade 2, Icelandic 8 dot computer braille, Tamil grade 1, Spanish 8 dot computer braille, Farsi grade 1. (#2014)
* You can now configure whether frames in documents are reported from the Document Formatting preferences dialog. (#1900)
* Sleep mode is automatically enabled when using OpenBook. (#1209)
* In Poedit, translators can now read translator added and automatically extracted comments. Messages that are untranslated or fuzzy are marked with a star and a beep is heard when you navigate onto them. (#1811)
* Support for the HumanWare Brailliant BI and B series displays. (#1990)
* New languages: Norwegian Bokmål, Traditional Chinese (Hong Kong).

### Changes

* Commands to describe the current character or to spell the current word or line now will spell in the appropriate language according to the text, if auto language switching is turned on and the appropriate language information is available.
* Updated eSpeak speech synthesizer to 1.46.02.
* NVDA will now truncate extremely long (30 characters or greater) names guessed from graphic and link URLs as they are most likely garbage that gets in the way of reading. (#1989)
* Some information displayed in braille has been abbreviated. (#1955, #2043)
* When the caret or review cursor moves, braille is now scrolled in the same way as when it is manually scrolled. This makes it more appropriate when braille is configured to read by paragraphs and/or avoid splitting words. (#1996)
* Updated to new Spanish grade 1 braille translation table.
* Updated liblouis braille translator to 2.4.1.

### Bug Fixes

* In Windows 8, focus is no longer incorrectly moved away from the Windows Explorer search field, which was not allowing NVDA to interact with it.
* Major performance improvements when reading and navigating Microsoft Word documents while automatic reporting of formatting is enabled, thus now making it quite comfortable to proof read formatting etc. Performance may be also improved over all for some users.
* Browse mode is now used for full screen Adobe Flash content.
* Fixed poor audio quality in some cases when using Microsoft Speech API version 5 voices with the audio output device set to something other than the default (Microsoft Sound Mapper). (#749)
* Again allow NVDA to be used with the "no speech" synthesizer, relying purely on braille or the speech viewer. (#1963)
* Object navigation commands no longer report "No children" and "No parents", but instead report messages consistent with the documentation.
* When NVDA is configured to use a language other than English, the name of the tab key is now reported in the correct language.
* In Mozilla Gecko (e.g. Firefox), NVDA no longer intermittently switches to browse mode while navigating menus in documents. (#2025)
* In Calculator, the backspace key now reports the updated result instead of reporting nothing. (#2030)
* In browse mode, the move mouse to current navigator object command now routes to the center of the object at the review cursor instead of the top left, making it more accurate it some cases. (#2029)
* In browse mode with automatic focus mode for focus changes enabled, focusing on a toolbar will now switch to focus mode. (#1339)
* The report title command works correctly again in Adobe Reader.
* With automatic focus mode for focus changes enabled, focus mode is now correctly used for focused table cells; e.g. in ARIA grids. (#1763)
* In iTunes, position information in certain lists is now reported correctly.
* In Adobe Reader, some links are no longer treated as containing read-only editable text fields.
* The labels of some editable text fields are no longer incorrectly included when reporting the text of a dialog. (#1960)
* The description of groupings is once again reported if reporting of object descriptions is enabled.
* The human readable sizes are now included in the text of the Windows Explorer drive properties dialog.
* Double reporting of property page text has been suppressed in some cases. (#218)
* Improved tracking of the caret in editable text fields which rely on text written to the screen. In particular, this improves editing in the Microsoft Excel cell editor and the Eudora message editor. (#1658)
* In Firefox 11, the move to containing virtual buffer command (NVDA+control+space) now works as it should to escape embedded objects such as Flash content.
* NVDA now restarts itself correctly (e.g. after changing the configured language) when it is located in a directory which contains non-ASCII characters. (#2079)
* Braille correctly respects the settings for reporting of object shortcut keys, position information and descriptions.
* In Mozilla applications, switching between browse and focus modes is no longer slow with braille enabled. (#2095)
* Routing the cursor to the space at the end of the line/paragraph using braille cursor routing keys in some editable text fields now works correctly instead of routing to the start of the text. (#2096)
* NVDA again works correctly with the Audiologic Tts3 synthesizer. (#2109)
* Microsoft Word documents are correctly treated as multi-line. This causes braille to behave more appropriately when a document is focused.
* In Microsoft Internet Explorer, errors no longer occur when focusing on certain rare controls. (#2121)
* Changing the pronunciation of punctuation/symbols by the user will now take effect straight away, rather than requiring NVDA to be restarted or auto language switching to be disabled.
* When using eSpeak, speech no longer goes silent in some cases in the Save As dialog of the NVDA Log Viewer. (#2145)

### Changes for Developers

* There is now a remote Python console for situations where remote debugging is useful. See the Developer Guide for details.
* The base path of NVDA's code is now stripped from tracebacks in the log to improve readability. (#1880)
* TextInfo objects now have an activate() method to activate the position represented by the TextInfo.
 * This is used by braille to activate the position using cursor routing keys on a braille display. However, there may be other callers in future.
* TreeInterceptors and NVDAObjects which only expose one page of text at a time can support automatic page turns during say all by using the textInfos.DocumentWithPageTurns mix-in. (#1978)
* Several control and output constants have been renamed or moved. (#228)
 * speech.REASON_* constants have been moved to controlTypes.
 * In controlTypes, speechRoleLabels and speechStateLabels have been renamed to just roleLabels and stateLabels, respectively.
* Braille output is now logged at level input/output. First, the untranslated text of all regions is logged, followed by the braille cells of the window being displayed. (#2102)
* subclasses of the sapi5 synthDriver can now override _getVoiceTokens and extend init to support custom voice tokens such as with sapi.spObjectTokenCategory to get tokens from a custom registry location.

## 2011.3

Highlights of this release include automatic speech language switching when reading documents with appropriate language information; support for 64 bit Java Runtime Environments; reporting of text formatting in browse mode in Mozilla applications; better handling of application crashes and freezes; and initial fixes for Windows 8.

### New Features

* NVDA can now change the eSpeak synthesizer language on the fly when reading certain web/pdf documents with appropriate language information. Automatic language/dialect switching can be toggled on and off from the Voice Settings dialog. (#845) 
* Java Access Bridge 2.0.2 is now supported, which includes support for 64 bit Java Runtime Environments.
* In Mozilla Gecko (e.g. Firefox) Heading levels are now announced  when using object navigation.
* Text formatting can now be reported when using browse mode in Mozilla Gecko (e.g. Firefox and Thunderbird). (#394)
* Text with underline and/or strikethrough can now be detected and reported in standard IAccessible2 text controls such as in Mozilla applications.
* In browse mode in Adobe Reader, table row and column counts are now reported.
* Added support for the Microsoft Speech Platform synthesizer. (#1735)
* Page and line numbers are now reported for the caret in IBM Lotus Symphony. (#1632)
* The percentage of how much the pitch changes when speaking a capital letter is now configurable from the voice settings dialog. However, this does replace the older raise pitch for capitals checkbox (therefore to turn off this feature set the percentage to 0). (#255)
* Text and background color is now included in the reporting of formatting for cells in Microsoft Excel. (#1655)
* In applications using the Java Access Bridge, the activate current navigator object command now works on controls where appropriate. (#1744)
* New language: Tamil.
* Basic support for Design Science MathPlayer.

### Changes

* NVDA will now restart itself if it crashes.
* Some information displayed in braille has been abbreviated. (#1288)
* the Read active window script (NVDA+b) has been improved to filter out unuseful controls   and also is now much more easy to silence. (#1499)
* Automatic say all when a browse mode document loads is now optional via a setting in the Browse Mode settings dialog. (#414)  
* When trying to read the status bar (Desktop NVDA+end), If a real status bar object cannot be located, NVDA will instead resort to using the bottom line of text written to the display for the active application. (#649)
* When reading with say all in browse mode documents, NVDA will now pause at the end of headings and other block-level elements, rather than speaking the text together with the next lot of text as one long sentence.
* In browse mode, pressing enter or space on a tab now activates it instead of switching to focus mode. (#1760)
* Updated eSpeak speech synthesizer to 1.45.47.

### Bug Fixes

* NVDA  no longer shows bullets or numbering for lists in Internet Explorer and other MSHTML controls when the author has indicated that these should not be shown (i.e. the list style is "none"). (#1671)
* Restarting NVDA when it has frozen (e.g. by pressing control+alt+n) no longer exits the previous copy without starting a new one.
* Pressing backspace or arrow keys in a Windows command console no longer causes strange results in some cases. (#1612)
* The selected item in WPF combo boxes (and possibly some other combo boxes exposed using UI Automation) which do not allow text editing is now reported correctly.
* In browse mode in Adobe Reader, it is now always possible to move to the next row from the header row and vice versa using the move to next row and move to previous row commands. Also, the header row is no longer reported as row 0. (#1731)
* In browse mode in Adobe Reader, it is now possible to move to (and therefore past) empty cells in a table.
* Pointless position information (e.g. 0 of 0 level 0) is no longer reported in braille.
* When braille is tethered to review, it is now able to show  content in flat review. (#1711)
* A text control's text is no longer presented twice on a braille display in some cases, e.g. scrolling back from the start of Wordpad documents.
* In browse mode in Internet Explorer, pressing enter on a file upload button now correctly presents the dialog to choose a file to upload instead of switching to focus mode. (#1720)
* Dynamic content changes such as in Dos consoles are no longer announced if  sleep mode for that application is currently on. (#1662)
* In browse mode, the behaviour of alt+upArrow and alt+downArrow to collapse and expand combo boxes has been improved. (#1630)
* NVDA now recovers from many more situations such as applications that stop responding which previously caused it to freeze completely. (#1408)
* For Mozilla Gecko (Firefox etc) browse mode documents NVDA will no longer fail to render text in a very specific situation where an element is styled as display:table. (#1373)
* NVDA will no longer announce label controls when focus moves inside of them. Stops double announcements of labels for some form fields in Firefox (Gecko) and Internet Explorer (MSHTML). (#1650)
* NVDA no longer fails to read a cell in Microsoft Excel after pasting in to it with control+v. (#1781)
* In Adobe Reader, extraneous information about the document is no longer announced when moving to a control on a different page in focus mode. (#1659)
* In browse mode in Mozilla Gecko applications (e.g. Firefox), toggle buttons are now detected and reported correctly. (#1757)
* NVDA can now   correctly read the Windows Explorer Address Bar in Windows 8 developer preview.
* NVDA will no longer crash apps such as winver and wordpad in Windows 8 developer preview due to bad glyph translations.
* In browse mode in applications using Mozilla Gecko 10 and later (e.g. Firefox 10), the cursor is more often positioned correctly when loading a page with a target anchor. (#360)
* In browse mode in Mozilla Gecko applications (e.g. Firefox), labels for image maps are now rendered.
* With mouse tracking enabled, moving the mouse over certain editable text fields (such as in Synaptics Pointing Device Settings and SpeechLab SpeakText) no longer causes the application to crash. (#672)
* NVDA now functions correctly in several about dialogs in applications distributed with Windows XP, including the About dialog in Notepad and the About Windows dialog. (#1853, #1855)
* Fixed reviewing by word in Windows Edit controls. (#1877)
* Moving out of an editable text field with leftArrow, upArrow or pageUp while in focus mode now correctly switches to browse mode when automatic focus mode for caret movement is enabled. (#1733)

### Changes for Developers

* NVDA can now instruct speech synthesizers to switch languages for particular sections of speech.
 * To support this, drivers must handle speech.LangChangeCommand in sequences past to SynthDriver.speak().
 * SynthDriver objects should also provide the language argument to VoiceInfo objects (or override the language attribute to retrieve the current language). Otherwise, NVDA's user interface language will be used.

## 2011.2

Highlights of this release include major improvements concerning punctuation and symbols, including configurable levels, custom labelling and character descriptions; no pauses at the end of lines during say all; improved support for ARIA in Internet Explorer; better support for XFA/LiveCycle PDF documents in Adobe Reader; access to text written to the screen in more applications; and access to formatting and color information for text written to the screen.

### New Features

* It is now possible to hear the description for any given character by pressing the review current character script twice in quick succession.  For English characters this is the standard English phonetic alphabet. For pictographic languages such as traditional Chinese, one or more example phrases using the given symbol are provided. Also pressing review current word or review current line three times will spell the word/line using the first of these descriptions. (#55)
* More text can be seen in flat review for applications such as Mozilla Thunderbird that write their text directly to the display as glyphs.
* It is now possible to choose from several levels of punctuation and symbol announcement. (#332)
* When punctuation or other symbols are repeated more than four times, the number of repetitions is now announced instead of speaking the repeated symbols. (#43)
* New braille translation tables: Norwegian 8 dot computer braille, Ethiopic grade 1, Slovene grade 1, Serbian grade 1. (#1456)
* Speech no longer unnaturally pauses at the end of each line when using the say all command. (#149)
* NVDA will now announce whether something is sorted (according to the aria-sort property) in web browsers. (#1500)
* Unicode Braille Patterns are now displayed correctly on braille displays. (#1505)
* In Internet Explorer and other MSHTML controls when focus moves inside a group of controls (surrounded by a fieldset), NVDA will now announce the name of the group (the legend). (#535)
* In Internet Explorer and other MSHTML controls, the aria-labelledBy and aria-describedBy properties are now honoured.
* in Internet Explorer and other MSHTML controls, support for ARIA list, gridcell, slider and progressbar controls has been improved.
* Users can now change the pronunciation of punctuation and other symbols, as well as the symbol level at which they are spoken. (#271, #1516)
* In Microsoft Excel, the name of the active sheet is now reported when switching sheets with control+pageUp or control+pageDown. (#760)
* When navigating a table in Microsoft Word with the tab key NVDA will now announce the current cell as you move. (#159)
* You can now configure whether table cell coordinates are reported from the Document Formatting preferences dialog. (#719)
* NVDA can now detect formatting and color for text written to the screen.
* In the Outlook Express/Windows Mail/Windows Live Mail message list, NVDA will now announce the fact that a message is unread and also if it's expanded or collapsed in the case of conversation threads. (#868)
* eSpeak now has a rate boost setting which triples the speaking rate.
* Support for the  calendar control found in the Date and Time Information dialog accessed from the  Windows 7 clock. (#1637)
* Additional key bindings have been added for the MDV Lilli braille display. (#241)
* New languages: Bulgarian, Albanian.

### Changes

* To move the caret to the review cursor, now press the move focus to navigator object script (desktop NVDA+shift+numpadMinus, laptop NVDA+shift+backspace) twice in quick succession. This frees up more keys on the keyboard. (#837)
* To hear the  decimal and hexadecimal representation of the character under the review cursor, now press review current character three times rather than twice, as twice now speaks the character description.
* Updated eSpeak speech synthesiser to 1.45.03. (#1465)
* Layout tables are no longer announced in Mozilla Gecko applications while moving the focus when in focus mode or outside of a document.
* In Internet Explorer and other MSHTML controls, browse mode now works for documents inside ARIA applications. (#1452)
* Updated liblouis braille translator to 2.3.0.
* When in browse mode  and jumping to a control with quicknav or focus, the description of the control is now announced if it has one.
* Progress bars are now announced in brows mode.
* Nodes marked with an ARIA role of presentation in Internet Explorer and other MSHTML controls are now filtered out of simple review and the focus ancestry.
* NVDA's user interface and documentation now refer to virtual buffers as browse mode, as the term "virtual buffer" is rather meaningless to most users. (#1509)
* When the user wishes to copy their user settings to the system profile for use on the logon screen, etc., and their settings contain custom plugins, they are now warned that this could be a security risk. (#1426)
* The NVDA service no longer starts and stops NVDA on user input desktops.
* On Windows XP and Windows Vista, NVDA no longer makes use of UI Automation even if it is available via the platform update. Although using UI Automation can improve the accessibility of some modern applications, on XP and Vista there were too many freezes, crashes and over all performance loss while using it. (#1437)
* In applications using Mozilla Gecko 2 and later (such as Firefox 4 and later), a document can now be read in browse mode before it is fully finished loading.
* NVDA now announces the state of a container when focus moves to a control inside it (e.g. if focus moves inside a document that is still loading it will report it as busy).
* NVDA's user interface and documentation no longer use the terms "first child" and "parent" with respect to object navigation, as these terms are confusing for many users.
* Collapsed is no longer reported for some menu items which have sub-menus.
* The reportCurrentFormatting script (NVDA+f) now reports the formatting at the position of the review cursor rather than the system caret / focus. As  by default the review cursor follows the caret, most people should not notice a difference. However this now enables the user to find out the formatting when moving the review cursor, such as in flat review.

### Bug Fixes

* Collapsing combo boxes in browse mode documents when focus mode has been forced with NVDA+space no longer auto-switches back to browse mode. (#1386)
* In Gecko (e.g. Firefox) and MSHTML (e.g. Internet Explorer) documents, NVDA now correctly renders certain text on the same line which was previously rendered on separate lines. (#1378)
* When Braille is tethered to review and the navigator object is moved to a browse mode document, either manually or due to a focus change, braille will appropriately show the browse mode content. (#1406, #1407)
* When speaking of punctuation is disabled, certain punctuation is no longer incorrectly spoken when using some synthesisers. (#332)
* Problems no longer occur when loading configuration for synthesisers which do not support the voice setting such as Audiologic Tts3. (#1347)
* The Skype Extras menu is now read correctly. (#648)
* Checking the Brightness controls volume checkbox in the Mouse Settings dialog should no longer cause a major lag for beeps when moving the mouse around the screen on Windows Vista/Windows 7 with Aero enabled. (#1183)
* When NVDA is configured to use the laptop keyboard layout, NVDA+delete now works as documented to report the dimensions of the current navigator object. (#1498)
* NVDA now Appropriately honours the aria-selected attribute in Internet Explorer documents.
* When NVDA automatically switches to focus mode in browse mode documents, it now announces information about the context of the focus. For example, if a list box item receives focus, the list box will be announced first. (#1491)
* In Internet Explorer and other MSHTML controls, ARIA listbox controls are now treeted as lists, rather than list items.
* When a read-only editable text control receives focus, NVDA now reports that it is read-only. (#1436)
* In browse mode, NVDA now behaves correctly with respect to read-only editable text fields.
* In browse mode documents, NVDA no longer incorrectly switches out of focus mode when aria-activedescendant is set; e.g. when the completion list appeared in some auto complete controls.
* In Adobe Reader, the name of controls is now reported when moving focus or using quick navigation in browse mode.
* In XFA PDF documents in Adobe Reader, buttons, links and graphics are now rendered correctly.
* In XFA PDF documents in Adobe Reader, all elements are now rendered on separate lines. This change was made because large sections (sometimes even the entire document) were being rendered without breaks due to the general lack of structure in these documents.
* Fixed problems when moving focus to or away from editable text fields in XFA PDF documents in Adobe Reader.
* In XFA PDF documents in Adobe Reader, changes to the value of a focused combo box will now be reported.
* Owner-drawn Combo boxes such as the ones to choose colors in Outlook Express are now accessible with NVDA. (#1340)
* In languages which use a space as a digit group/thousands separator such as French and German, numbers from separate chunks of text are no longer pronounced as a single number. This was particularly problematic for table cells containing numbers. (#555)
* nodes with an ARIA role of description in Internet Explorer and other MSHTML controls now are classed as static text, not edit fields.
* Fixed various issues when pressing tab while focus is on a document in browse mode (e.g. tab inappropriately moving to the address bar in Internet Explorer). (#720, #1367)
* When entering lists while reading text, NVDA now says, for example, "list with 5 items" instead of "listwith 5 items". (#1515)
* In input help mode, gestures are logged even if their scripts bypass input help such as the scroll braille display forward and back commands.
* In input help mode, when a modifier is held down on the keyboard, NVDA no longer reports the modifier as if it is modifying itself; e.g. NVDA+NVDA.
* In Adobe Reader documents, pressing c or shift+c to navigate to a combo box now works.
* The selected state of selectable table rows is now reported the same way it is for list and tree view items.
* Controls in Firefox and other Gecko applications can now be activated while in browse mode even if their content has been floated off-screen. (#801)
* You can no longer show an NVDA settings dialog while a message dialog is being shown, as the settings dialog was frozen in this case. (#1451)
* In Microsoft Excel, there is no longer a lag when holding down or rapidly pressing keys to move between or select cells.
* Fixed intermittent crashes of the NVDA service which meant that NVDA stopped running on secure Windows screens.
* Fixed problems that sometimes occurred with braille displays when a change caused text that was being displayed to disappear. (#1377)
* The downloads window in Internet Explorer 9 can now be navigated and read with NVDA. (#1280)
* It is no longer possible to accidentally start multiple copies of NVDA at the same time. (#507)
* On slow systems, NVDA no longer inappropriately causes its main window to be shown all the time while running. (#726)
* NVDA no longer crashes on Windows xP when starting a WPF application. (#1437)
* Say all and say all with review are now able to work in UI automation text controls that support all required functionality. For example, you can now use say all with review on XPS Viewer documents.
* NVDA no longer inappropriately classes some list items in the Outlook Express / Windows Live Mail message rules Apply Now dialog as being checkboxes. (#576)
* Combo boxes are no longer reported as having a sub-menu.
* NVDA is  now able to read the recipiants in the To, CC and BCC fields in Microsoft Outlook. (#421)
* Fixed the issue in NVDA's Voice Settings dialog where the value of sliders was sometimes not reported when changed. (#1411)
* NVDA no longer fails to announce the new cell when moving in an Excel spreadsheet after cutting and pasting. (#1567)
* NVDA no longer becomes worse at guessing color names the more colors it announces.
* In Internet Explorer and other MSHTML controls, fixed the inability to read parts of rare pages which contain iframes marked with an ARIA role of presentation. (#1569)
* In Internet Explorer and other MSHTML controls, fixed a rare problem where the focus kept bouncing infinitely between the document and a multi-line editable text field in focus mode. (#1566)
* In Microsoft Word 2010 NVDA will now automatically read confirmation dialogs. (#1538)
* In multi-line editable text fields in Internet Explorer and other MSHTML controls, selection on lines after the first is now reported correctly. (#1590)
* Improved moving by word in many cases, including browse mode and Windows Edit controls. (#1580)
* The NVDA installer no longer shows garbled text for Hong Kong versions of Windows Vista and Windows 7. (#1596)
* NVDA no longer fails to load the Microsoft Speech API version 5 synthesizer if the configuration contains settings for that synthesizer but is missing the voice setting. (#1599)
* In editable text fields in Internet Explorer and other MSHTML controls, NVDA no longer lags or freezes when braille is enabled.
* In firefox brows mode, NVDA no longer refuses to include content that is inside a focusable node with an ARIA role of presentation.
* In Microsoft Word with braille enabled, lines on pages after the first page are now reported correctly. (#1603)
* In Microsoft Word 2003, lines of right-to-left text can once again be read with braille enabled. (#627)
* In Microsoft Word, say all now works correctly when the document does not end with a sentence ending.
* When opening a plain text message in Windows Live Mail 2011, NVDA will correctly focus on the message document allowing it to be read.
* NVDA no longer temporarily freezes or refuses to speak when in the Move to / Copy to dialogs in Windows Live Mail. (#574)
* In Outlook 2010, NVDA will now correctly track the focus in the message list. (#1285)
* Some USB connection issues have been resolved with the MDV Lilli braille display. (#241)
* In Internet explorer and other MSHTML controls, spaces are no longer ignored in browse mode in certain cases (e.g. after a link).
* In Internet Explorer and other MSHTML controls, some extraneous line breaks have been eliminated in browse mode. specifically, HTML elements with a display style of None no longer force a line break. (#1685)
* If NVDA is unable to start, failure to play the Windows critical stop sound no longer clobbers the critical error message in the log file.

### Changes for Developers

* Developer documentation can now be generated using SCons. See readme.txt at the root of the source distribution for details, including associated dependencies.
* Locales can now provide descriptions for characters. See the Character Descriptions section of the Developer Guide for details. (#55)
* Locales can now provide information about the pronunciation of specific punctuation and other symbols. See the Symbol Pronunciation section of the Developer Guide for details. (#332)
* You can now build NVDAHelper with several debugging options using the nvdaHelperDebugFlags SCons variable. See readme.txt at the root of the source distribution for details. (#1390)
* Synth drivers are now passed a sequence of text and speech commands to speak, instead of just text and an index.
 * This allows for embedded indexes, parameter changes, etc.
 * Drivers should implement SynthDriver.speak() instead of SynthDriver.speakText() and SynthDriver.speakCharacter().
 * The old methods will be used if SynthDriver.speak() is not implemented, but they are deprecated and will be removed in a future release.
* gui.execute() has been removed. wx.CallAfter() should be used instead.
* gui.scriptUI has been removed.
 * For message dialogs, use wx.CallAfter(gui.messageBox, ...).
 * For all other dialogs, real wx dialogs should be used instead.
 * A new gui.runScriptModalDialog() function simplifies using modal dialogs from scripts.
* Synth drivers can now support boolean settings. See SynthDriverHandler.BooleanSynthSetting.
* SCons now accepts a certTimestampServer variable specifying the URL of a timestamping server to use to timestamp authenticode signatures. (#1644)

## 2011.1.1

This release fixes several security and other important issues found in NVDA 2011.1.

### Bug Fixes

* The Donate item in the NVDA menu is now disabled when running on the logon, lock, UAC and other secure Windows screens, as this is a security risk. (#1419)
* It is now impossible to copy or paste within NVDA's user interface while on secure desktops (lock screen, UAC screen and windows logon) as this is a security risk. (#1421)
* In Firefox 4, the move to containing virtual buffer command (NVDA+control+space) now works as it should to escape embedded objects such as Flash content. (#1429)
* When speaking of command keys is enabled, shifted characters are no longer incorrectly spoken as command keys. (#1422)
* When speaking of command keys is enabled, pressing space with modifiers other than shift (such as control and alt) is now reported as a command key. (#1424)
* Logging is now completely disabled when running on the logon, lock, UAC and other secure Windows screens, as this is a security risk. (#1435)
* In input help mode, Gestures are now logged even if they are not bound to a script (in accordance with the user guide). (#1425)

## 2011.1

Highlights of this release include automatic reporting of new text output in mIRC, PuTTY, Tera Term and SecureCRT; support for global plugins; announcement of bullets and numbering in Microsoft Word; additional key bindings for braille displays, including keys to move to the next and previous line; support for several Baum, HumanWare and APH braille displays; and reporting of colors for some controls, including IBM Lotus Symphony text controls.

### New Features

* Colors can now be reported for some controls. Automatic announcement can be configured in the Document Formatting preferences dialog. It can also be reported on demand using the report text formatting command (NVDA+f).
 * Initially, this is supported in standard IAccessible2 editable text controls (such as in Mozilla applications), RichEdit controls (such as in Wordpad) and IBM Lotus Symphony text controls.
* In virtual buffers, you can now select by page (using shift+pageDown and shift+pageUp) and paragraph (using shift+control+downArrow and shift+control+upArrow). (#639)
* NVDA now automatically reports new text output in mIRC, PuTTY, Tera Term and SecureCRT. (#936)
* Users can now add new key bindings or override existing ones for any script in NVDA by providing a single user input gesture map. (#194)
* Support for global plugins. Global plugins can add new functionality to NVDA which works across all applications. (#281)
* A small beep is now heard when typing characters with the shift key while capslock is on. This can be turned off by unchecking the related new option in the Keyboard settings dialog. (#663)
* hard page breaks are now announced when moving by line in Microsoft Word. (#758)
* Bullets and numbering are now spoken in Microsoft Word when moving by line. (#208)  
* A command to toggle Sleep mode for the current application (NVDA+shift+s) is now available. Sleep mode (previously known as self voicing mode) disables all screen reading functionality in NVDA for a particular application. Very useful for applications that provide their own speech and or screen reading features. Press this command again to disable Sleep mode.
* Some additional braille display key bindings have been added. See the Supported Braille Displays section of the User Guide for details. (#209)
* For the convenience of third party developers, app modules as well as global plugins can now be reloaded without restarting NVDA. Use tools -> Reload plugins in the NVDA menu or NVDA+control+f3. (#544)
* NVDA now remembers the position you were at when returning to a previously visited web page. This applies until either the browser or NVDA is exited. (#132)
* Handy Tech braille displays can now be used without installing the Handy Tech universal driver. (#854)
* Support for several Baum, HumanWare and APH braille displays. (#937)
* The status bar in Media Player Classic Home Cinema is now recognised.
* The Freedom Scientific Focus 40 Blue braille display can now be used when connected via bluetooth. (#1345)

### Changes

* Position information is no longer reported by default in some cases where it was usually incorrect; e.g. most menus, the Running Applications bar, the Notification Area, etc. However, this can be turned on again by an added option in the Object Presentation settings dialog.
* Keyboard help has been renamed to input help to reflect that it handles input from sources other than the keyboard.
* Input Help no longer reports a script's code location via speech and braille as it is cryptic and irrelevant to the user. However, it is now logged for developers and advanced users.
* When NVDA detects that it has frozen, it continues to intercept NVDA modifier keys, even though it passes all other keys through to the system. This prevents the user from unintentionally toggling caps lock, etc. if they press an NVDA modifier key without realising NVDA has frozen. (#939)
* If keys are held down after using the pass next key through command, all keys (including key repeats) are now passed through until the last key is released.
* If an NVDA modifier key is pressed twice in quick succession to pass it through and the second press is held down, all key repeats will now be passed through as well.
* The volume up, down and mute keys are now reported in input help. This could be helpful if the user is uncertain as to what these keys are.
* The hotkey for the Review Cursor item in the NVDA Preferences menu has been changed from r to c to eliminate the conflict with the Braille Settings item.

### Bug Fixes

* When adding a new speech dictionary entry, the title of the dialog is now "Add dictionary entry" instead of "Edit dictionary entry". (#924)
* In speech dictionary dialogs, the content of the Regular expression and Case sensitive columns of the Dictionary entries list is now presented in the configured NVDA language instead of always in English.
* In AIM, position information is now announced in tree views.
* On sliders in the Voice Settings dialog, up arrow/page up/home now increase the setting and down arrow/page down/end decrease it. Previously, the opposite occurred, which is not logical and is inconsistent with the synth settings ring. (#221)
* In virtual buffers with screen layout disabled, some extraneous blank lines no longer appear.
* If an NVDA modifier key is pressed twice quickly but there is an intervening key press, the NVDA modifier key is no longer passed through on the second press.
* Punctuation keys are now spoken in input help even when speaking of punctuation is disabled. (#977)
* In the Keyboard Settings dialog, the keyboard layout names are now presented in the configured NVDA language instead of always in English. (#558)
* Fixed an issue where some items were rendered as empty in Adobe Reader documents; e.g. the links in the table of contents of the Apple iPhone IOS 4.1 User Guide.
* The "Use currently saved settings on the logon and other secure screens" button in NVDA's General Settings dialog now works if used immediately after NVDA is newly installed but before a secure screen has appeared. Previously, NVDA reported that copying was successful, but it actually had no effect. (#1194)
* It is no longer possible to have two NVDA settings dialogs open simultaneously. This fixes issues where one open dialog depends on another open dialog; e.g. changing the synthesiser while the Voice Settings dialog is open. (#603)
* On systems with UAC enabled, the "Use currently saved settings on the logon and other secure screens" button in NVDA's General Settings dialog no longer fails after the UAC prompt if the user's account name contains a space. (#918)
* In Internet Explorer and other MSHTML controls, NVDA now uses the URL as a last resort to determine the name of a link, rather than presenting empty links. (#633)
* NVDA no longer ignores the focus  in AOL Instant Messenger 7 menus. (#655)
* Announce the correct label for errors in the Microsoft Word Spell Check dialog (e.g. Not in dictionary, Grammar error, punctuation). Previously  they were all announced as grammar error. (#883)
* Typing in Microsoft Word while using a braille display should no longer cause garbled text to be typed, and a rare freeze when pressing a braille routing key in Word documents has been fixed. (#1212) However a limitation is that Arabic text can no longer be read in Word 2003 and below, while using a braille display. (#627)
* When pressing the delete key in an edit field, the text/cursor on a braille display should now always be updated appropriately to reflect the change. (#947)
* Changes on dynamic pages in Gecko2 documents (E.g. Firefox 4) while multiple tabs are open are now properly reflected by NVDA. Previously only changes in the first tab were reflected. (Mozilla bug 610985)
* NVDA can now properly announce the suggestions for grammar and punctuation errors in Microsoft Word spell check dialog. (#704)
* In Internet Explorer and other MSHTML controls, NVDA no longer presents destination anchors as empty links in its virtual buffer. Instead, these anchors are hidden as they should be. (#1326)
* Object navigation around and within standard groupbox windows is no longer broken and asymmetrical.
* In Firefox and other Gecko-based controls, NVDA will no longer get stuck in a subframe if it finishes loading before the outer document.
* NVDA  now appropriately announces the next character when deleting a character with numpadDelete. (#286)
* On the Windows XP logon screen, the user name is once again reported when the selected user is changed.
* Fixed problems when reading text in Windows command consoles with reporting of line numbers enabled.
* The Elements List dialog for virtual buffers is now usable by sighted users. All controls are visible on screen. (#1321)
* The list of entries in the Speech Dictionary dialog is now more readable by sighted users. The list is now large enough to show all of its columns on screen. (#90)
* On ALVA BC640/BC680 braille displays, NVDA no longer disregards display keys that are still held down after another key is released.
* Adobe Reader X no longer crashes after leaving the untagged document options before the processing dialog appears. (#1218)
* NVDA now switches to the appropriate braille display driver when you revert to saved configuration. (#1346)
* The Visual Studio 2008 Project Wizard is read correctly again. (#974)
* NVDA no longer completely fails to work in applications which contain non-ASCII characters in their executable name. (#1352)
* When reading by line in AkelPad with word wrap enabled, NVDA no longer reads the first character of the following line at the end of the current line.
* In the Visual Studio 2005/2008 code editor, NVDA no longer reads the entire text after every typed character. (#975)
* Fixed the issue where some braille displays weren't cleared properly when NVDA was exited or the display was changed.
* The initial focus is no longer sometimes spoken twice when NVDA starts. (#1359)

### Changes for Developers

* SCons is now used to prepare the source tree and create binary builds, portable archives, installers, etc. See readme.txt at the root of the source distribution for details.
* The key names used by NVDA (including key maps) have been made more friendly/logical; e.g. upArrow instead of extendedUp and numpadPageUp instead of prior. See the vkCodes module for a list.
* All input from the user is now represented by an inputCore.InputGesture instance. (#601)
 * Each source of input subclasses the base InputGesture class.
 * Key presses on the system keyboard are encompassed by the keyboardHandler.KeyboardInputGesture class.
 * Presses of buttons, wheels and other controls on a braille display are encompassed by subclasses of the braille.BrailleDisplayGesture class. These subclasses are provided by each braille display driver.
* Input gestures are bound to ScriptableObjects using the ScriptableObject.bindGesture() method on an instance or an __gestures dict on the class which maps gesture identifiers to script names. See baseObject.ScriptableObject for details.
* App modules no longer have key map files. All input gesture bindings must be done in the app module itself.
* All scripts now take an InputGesture instance instead of a key press.
 * KeyboardInputGestures can be sent on to the OS using the send() method of the gesture.
* To send an arbitrary key press, you must now create a KeyboardInputGesture using KeyboardInputGesture.fromName() and then use its send() method.
* Locales may now provide an input gesture map file to add new bindings or override existing bindings for scripts anywhere in NVDA. (#810)
 * Locale gesture maps should be placed in locale\LANG\gestures.ini, where LANG is the language code.
 * See inputCore.GlobalGestureMap for details of the file format.
* The new LiveText and Terminal NVDAObject behaviors facilitate automatic reporting of new text. See those classes in NVDAObjects.behaviors for details. (#936)
 * The NVDAObjects.window.DisplayModelLiveText overlay class can be used for objects which must retrieve text written to the display.
 * See the mirc and putty app modules for usage examples.
* There is no longer an _default app module. App modules should instead subclass appModuleHandler.AppModule (the base AppModule class).
* Support for global plugins which can globally bind scripts, handle NVDAObject events and choose NVDAObject overlay classes. (#281) See globalPluginHandler.GlobalPlugin for details.
* On SynthDriver objects, the available* attributes for string settings (e.g. availableVoices and availableVariants)  are now OrderedDicts keyed by ID instead of lists.
* synthDriverHandler.VoiceInfo now takes an optional language argument which specifies the language of the voice.
* SynthDriver objects now provide a language attribute which specifies the language of the current voice.
 * The base implementation uses the language specified on the VoiceInfo objects in availableVoices. This is suitable for most synthesisers which support one language per voice.
* Braille display drivers have been enhanced to allow buttons, wheels and other controls to be bound to NVDA scripts:
 * Drivers can provide a global input gesture map to add bindings for scripts anywhere in NVDA.
 * They can also provide their own scripts to perform display specific functions.
 * See braille.BrailleDisplayDriver for details and existing braille display drivers for examples.
* The 'selfVoicing' property on AppModule classes has now been renamed to 'sleepMode'.
* The app module events event_appLoseFocus and event_appGainFocus have now been renamed to event_appModule_loseFocus and event_appModule_gainFocus, respectivly, in order to make the naming convention consistent with app modules and tree interceptors.
* All braille display drivers should now use braille.BrailleDisplayDriver instead of braille.BrailleDisplayDriverWithCursor.
 * The cursor is now managed outside of the driver.
 * Existing drivers need only change their class statement accordingly and rename their _display method to display.

## 2010.2

Notable features of this release include greatly simplified object navigation; virtual buffers for Adobe Flash content; access to many previously inaccessible controls by retrieving text written to the screen; flat review of screen text; support for IBM Lotus Symphony documents; reporting of table row and column headers in Mozilla Firefox; and significantly improved user documentation.

### New Features

* Navigating through objects with the review cursor has been greatly simplified. The review cursor now excludes objects which aren't useful to the user; i.e. objects only used for layout purposes and unavailable objects.
* In applications using the Java Access Bridge (including OpenOffice.org), formatting can now be reported in text controls. (#358, #463)
* When moving the mouse over cells in Microsoft Excel, NVDA will appropriately announce them.
* In applications using the Java Access Bridge, the text of a dialog is now reported when the dialog appears. (#554)
* A virtualBuffer can now be used to navigate adobe Flash content. Object navigation and interacting with the controls directly (by turning on focus mode) is still supported. (#453)
* Editable text controls in the Eclipse IDE, including the code editor, are now accessible. You must be using Eclipse 3.6 or later. (#256, #641)
* NVDA can now retrieve most text written to the screen. (#40, #643)
 * This allows for reading of controls which do not expose information in more direct/reliable ways.
 * Controls made accessible by this feature include: some menu items which display icons (e.g. the Open With menu on files in Windows XP) (#151), editable text fields in Windows Live applications (#200), the errors list in Outlook Express (#582), the editable text control in TextPad (#605), lists in Eudora, many controls in Australian E-tax and the formula bar in Microsoft Excel.
* Support for the code editor in Microsoft Visual Studio 2005 and 2008. At least Visual Studio Standard is required; this does not work in the Express editions. (#457)
* Support for IBM Lotus Symphony documents.
* Early experimental support for Google Chrome. Please note that Chrome's screen reader support is far from complete and additional work may also be required in NVDA. You will need a recent development build of Chrome to try this.
* The state of toggle keys (caps lock, num lock and scroll lock) is now displayed in braille when they are pressed. (#620)
* Help balloons are now displayed in braille when they appear. (#652)
* Added a driver for the MDV Lilli braille display. (#241)
* When selecting an entire row or column in Microsoft Excel with the shortcut keys shift+space and control+space, the new selection is now reported. (#759)
* Table row and column headers can now be reported. This is configurable from the Document Formatting preferences dialog.
 * Currently, this is supported in documents in Mozilla applications such as Firefox (version 3.6.11 and later) and Thunderbird (version 3.1.5 and later). (#361)
* Introduced commands for flat review: (#58)
 * NVDA+numpad7  switches to flat review, placing the review cursor at the position of the current object, allowing you  to review the screen (or a document if within one) with the text review commands.
 * NVDA+numpad1 moves the review cursor into the object represented by the text at  the position of the review cursor, allowing you to navigate by object from that point.
* Current NVDA user settings can be  copied to be used on secure Windows screens such as the logon and UAC screens by pressing a button in the General Settings dialog. (#730)
* Support for Mozilla Firefox 4.
* Support for Microsoft Internet Explorer 9.

### Changes

* The sayAll by Navigator object (NVDA+numpadAdd), navigator object next in flow (NVDA+shift+numpad6) and navigator object previous in flow (NVDA+shift+numpad4) commands have been removed for the time being, due to bugginess and to free up the keys for other possible features.
* In the NVDA Synthesizer dialog, only the display name of the synthesizer is now listed. Previously, it was prefixed by the driver's name, which is only relevant internally.
* When in embedded applications or virtual buffers inside another virtualBuffer (e.g. Flash), you can now  press nvda+control+space to move out of the embedded application or virtual buffer to the containing document. Previously nvda+space  was used for this. Now nvda+space is specifically only for toggling brows/focus modes on virtualBuffers.
* If the speech viewer (enabled under the tools menu) is given the focus (e.g. it was clicked in) new text will not appear in the control until focus is moved away. This allows for selecting the text with greater ease (e.g. for copying).
* The Log Viewer and Python Console are maximised when activated.
* When focusing on a worksheet in Microsoft Excel and there is more than one cell selected, the selection range is announced, rather than just the active cell. (#763)
* Saving configuration and changing of particular sensitive options is now disabled when running on the logon, UAC and other secure Windows screens.
* Updated eSpeak speech synthesiser to 1.44.03.
* If NVDA is already running, activating the NVDA shortcut on the desktop (which includes pressing control+alt+n) will restart NVDA.
* Removed the report text under the mouse checkbox from the Mouse settings dialog and replaced it with an Enable mouse tracking checkbox, which better matches the toggle mouse tracking script (NVDA+m). 
* Updates to the laptop keyboard layout so that it includes all commands available in the desktop layout and works correctly on non-English keyboards. (#798, #800)
* Significant improvements and updates to the user documentation, including documentation of the laptop keyboard commands and synchronisation of the Keyboard Commands Quick Reference with the User Guide. (#455)
* Updated liblouis braille translator to 2.1.1. Notably, this fixes some issues related to Chinese braille as well as characters which are undefined in the translation table. (#484, #499)

### Bug Fixes

* In µTorrent, the focused item in the torrents list no longer reports repeatedly or steals focus when a menu is open.
* In µTorrent, the names of the files in the Torrent Contents list are now reported.
* In Mozilla applications, focus is now correctly detected when it lands on an empty table or tree.
* In Mozilla applications, "not checked" is now correctly reported for checkable controls such as checkable table cells. (#571)
* In Mozilla applications, the text of correctly implemented ARIA dialogs is no longer ignored and will now be reported when the dialog appears. (#630)
* in Internet Explorer and other MSHTML controls, the ARIA level attribute is now  honoured correctly.
* In Internet Explorer and other MSHTML controls, the ARIA role is now chosen over other type information to give a much more correct and predictable ARIA experience.
* Stopped a rare crash in Internet Explorer when navigating through frames or iFrames.
* In Microsoft Word documents, right-to-left lines (such as Arabic text) can be read again. (#627)
* Greatly reduced lag when large amounts of text are displayed in a Windows command console on 64-bit systems. (#622)
* If Skype is already started when NVDA starts, it is no longer necessary to restart Skype to enable accessibility. This may also be true for other applications which check the system screen reader flag.
* In Microsoft Office applications, NVDA no longer crashes when speak foreground (NVDA+b) is pressed or when navigating some objects on toolbars. (#616)
* Fixed incorrect speaking of numbers containing a 0 after a separator; e.g. 1,023. (#593)
* Adobe Acrobat Pro and Reader 9 no longer crash when closing a file or performing certain other tasks. (#613)
* The selection is now announced when control+a is pressed to select all text in some editable text controls such as in Microsoft Word. (#761)
* In Scintilla controls (e.g. Notepad++), text is no longer incorrectly selected when NVDA moves the caret such as during say all. (#746)
* It is again possible to review the contents of cells in Microsoft Excel with the review cursor.
* NVDA can again read by line in certain problematic textArea fields in Internet Explorer 8. (#467)
* Windows Live Messenger 2009 no longer exits immediately after it is started while NVDA is running. (#677)
* In web browsers, It is no longer necessary to press tab to interact with an embedded object (such as Flash content) after pressing enter on the embedded object or returning from another application. (#775)
* In Scintilla controls (e.g. Notepad++), the beginning of long lines is no longer truncated when it scrolls off the screen. Also, these long lines will be correctly displayed in braille when they are selected.
* In Loudtalks, it is now possible to access the contact list.
* The URL of the document and "MSAAHTML Registered Handler" are no longer sometimes spuriously reported in Internet Explorer and other MSHTML controls. (#811)
* In tree views in the Eclipse IDE, the previously focused item is no longer incorrectly announced when focus moves to a new item.
* NVDA now functions correctly on a system where the current working directory has been removed from the DLL search path (by setting the CWDIllegalInDllSearch registry entry to 0xFFFFFFFF). Note that this is not relevant to most users. (#907)
* When the table navigation commands are used outside of a table in Microsoft Word, "edge of table" is no longer spoken after "not in table". (#921)
* When the table navigation commands cannot move due to being at the edge of a table in Microsoft Word, "edge of table" is now spoken in the configured NVDA language rather than always in English. (#921)
* In Outlook Express, Windows Mail and Windows Live Mail, the state of the checkboxes in message rules lists is now reported. (#576)
* The description of message rules can now be read in Windows Live Mail 2010.

## 2010.1

This release focuses primarily on bug fixes and improvements to the user experience, including some significant stability fixes.

### New Features

* NVDA no longer fails to start on a system with no audio output devices. Obviously, a braille display or the Silence synthesiser in conjunction with the Speech Viewer will need to be used for output in this case. (#425)
* A report landmarks checkbox has been added to the Document Formatting settings dialog which allows you to configure whether NVDA should announce landmarks in web documents. For compatibility with the previous release, the option is on by default.
* If speak command keys is enabled, NVDA will now announce the names of multimedia keys (e.g. play, stop, home page, etc.) on many keyboards when they are pressed. (#472)
* NVDA now announces the word being deleted when pressing control+backspace in controls that support it. (#491)
* Arrow keys can now be used in the Web formator window to navigate and read the text. (#452)
* The entry list in the Microsoft Office Outlook address book is now supported.
* NVDA better supports embedded editable (design mode) documents in Internet Explorer. (#402)
* a new script (nvda+shift+numpadMinus) allows you to move the system focus to the current navigator object.
* New scripts to lock and unlock the left and right mouse buttons. Useful for performing drag and drop operations. shift+numpadDivide to lock/unlock the left, shift+numpadMultiply to lock/unlock the right.
* New braille translation tables: German 8 dot computer braille, German grade 2, Finnish 8 dot computer braille, Chinese (Hong Kong, Cantonese), Chinese (Taiwan, Manderin). (#344, #369, #415, #450)
* It is now possible to disable the creation of the desktop shortcut (and thus the shortcut key) when installing NVDA. (#518)
* NVDA can now use IAccessible2 when present in 64 bit applications. (#479)
* Improved support for live regions in Mozilla applications. (#246)
* The NVDA Controller Client API is now provided to allow applications to control NVDA; e.g. to speak text, silence speech, display a message in Braille, etc.
* Information and error messages are now read in the logon screen in Windows Vista and Windows 7. (#506)
* In Adobe Reader, PDF interactive forms developed with Adobe LiveCycle are now supported. (#475)
* In Miranda IM, NVDA now automatically reads incoming messages in chat windows if reporting of dynamic content changes is enabled. Also, commands have been added to report the three most recent messages (NVDA+control+number). (#546)
* Input text fields are now supported in Adobe Flash content. (#461)

### Changes

* The extremely verbose keyboard help message in the Windows 7 Start menu is no longer reported.
* The Display synth has now been replaced with a new Speech Viewer. To activate it, choose Speech Viewer from the Tools menu. The speech viewer can be used independently of what ever speech synthesizer you are using. (#44)
* Messages on the braille display will automatically be dismissed if the user presses a key that results in a change such as the focus moving. Previously the message would always stay around for its configured time.
* Setting whether braille should be tethered to the focus or the review cursor (NVDA+control+t) can now be also set from the braille settings dialog, and is also now saved in the user's configuration.
* Updated eSpeak speech synthesiser to 1.43.
* Updated liblouis braille translator to 1.8.0.
* In virtual buffers, the reporting of elements when moving by character or word has been greatly improved. Previously, a lot of irrelevant information was reported and the reporting was very different to that when moving by line. (#490)
* The Control key now simply stops speech like other keys, rather than pausing speech. To pause/resume speech, use the shift key.
* Table row and column counts are no longer announced when reporting focus changes, as this announcement is rather verbose and usually not useful.

### Bug Fixes

* NVDA no longer fails to start if UI Automation support appears to be available but fails to initialise for some reason. (#483)
* The entire contents of a table row is no longer sometimes reported when moving focus inside a cell  in Mozilla applications. (#482)
* NVDA no longer lags for a long time when expanding tree view items that contain a very large amount of sub-items.
* When listing SAPI 5 voices, NVDA now tries to detect buggy voices and excludes them from the Voice Settings dialog and synthesiser settings ring. Previously, when there was just one problematic voice, NVDA's SAPI 5 driver would sometimes fail to start.
* Virtual buffers now honour the report object shortcut keys setting found in the Object Presentation dialog. (#486)
* In virtual buffers, row/column coordinates are no longer incorrectly read for row and column headers when reporting of tables is disabled.
* In virtual buffers, row/column coordinates are now correctly read when you leave a table and then re-enter the same table cell without visiting another cell first; e.g. pressing upArrow then downArrow on the first cell of a table. (#378)
* Blank lines in Microsoft Word documents and  Microsoft HTML edit controls are now shown appropriately on braille displays. Previously NVDA was displaying the current sentence on the display, not the current line for these situations. (#420)
* Multiple security fixes when running NVDA at Windows logon and on other secure desktops. (#515)
* The cursor position (caret) is now correctly updated when performing a Say All that goes off the bottom of the screen, in standard Windows edit fields and Microsoft Word documents. (#418)
* In virtual buffers, text is no longer incorrectly included for images inside links and clickables that are marked as being irrelevant to screen readers. (#423)
* Fixes to the laptop keyboard layout. (#517)
* When Braille is tethered to review when you focus on a Dos console window, the review cursor can now properly navigate the text in the console.
* While working with TeamTalk3 or TeamTalk4 Classic, the VU meter progress bar in the main window is no longer announced as it updates. Also, special characters can be read properly in the incoming chat window.
* Items are no longer spoken twice in the Windows 7 Start Menu. (#474)
* Activating same-page links in Firefox 3.6 appropriately moves the cursor in the virtualBuffer to the correct place on the page.
* Fixed the issue where some text was not rendered in Adobe Reader in certain PDF documents.
* NVDA no longer incorrectly speaks certain numbers separated by a dash; e.g. 500-1000. (#547)
* In Windows XP, NVDA no longer causes Internet Explorer to freeze when toggling checkboxes in Windows Update. (#477)
* When using the in-built eSpeak synthesiser, simultaneous speech and beeps no longer intermittently cause freezes on some systems. This was most noticeable, for example, when copying large amounts of data in Windows Explorer.
* NVDA no longer announces that a Firefox document has become busy (e.g. due to an update or refresh) when that document is in the background. This also caused the status bar of the foreground application to be spuriously announced.
* When switching Windows keyboard layouts (with control+shift or alt+shift), the full name of the layout is reported in both speech and braille. Previously it was only reported in speech, and alternative layouts (e.g. Dvorak) were not reported at all.
* If reporting of tables is disabled, table information is no longer announced when the focus changes.
* Certain standard tree view controls in 64 bit applications (e.g. the Contents tree view in Microsoft HTML Help) are now accessible. (#473)
* Fixed some problems with logging of messages containing non-ASCII characters. This could cause spurious errors in some cases on non-English systems. (#581)
* The information in the About NVDA dialog now appears in the user's configured language instead of always appearing in English. (#586)
* Problems are no longer encountered when using the synthesiser settings ring after the voice is changed to one which has less settings than the previous voice.
* In Skype 4.2, contact names are no longer spoken twice in the contact list.
* Fixed some potentially major memory leaks in the GUI and in virtual buffers. (#590, #591)
* Work around a nasty bug in some SAPI 4 synthesisers which was causing frequent errors and crashes in NVDA. (#597)

## 2009.1

Major highlights of this release include support for 64 bit editions of Windows; greatly improved support for Microsoft Internet Explorer and Adobe Reader documents; support for Windows 7; reading of the Windows logon, control+alt+delete and User Account Control (UAC) screens; and the ability to interact with Adobe Flash and Sun Java content on web pages. There have also been several significant stability fixes and improvements to the general user experience.

### New Features

* Official support for 64 bit editions of Windows! (#309)
* Added a synthesizer driver for the Newfon synthesizer. Note that this requires a special version of Newfon. (#206)
* In virtual buffers, focus mode and browse mode can now be reported using sounds instead of speech. This is enabled by default. It can be configured from the Virtual buffers dialog. (#244)
* NVDA no longer cancels speech when volume control keys are pressed on the keyboard, allowing the user to change the volume and listen to actual results immediately. (#287)
* Completely rewritten support for Microsoft Internet Explorer and Adobe Reader documents. This support has been unified with the core support used for Mozilla Gecko, so features such as fast page rendering, extensive quick navigation, links list, text selection, auto focus mode and braille support are now available with these documents.
* Improved support for the date selection control found in the Windows Vista Date / Time properties dialog.
* improved support for the Modern XP/Vista start menu (specifically the all programs, and places menus). Appropriate level information is now announced.
* The amount of text that is announced when moving the mouse is now configurable from the Mouse settings dialog. A choice of paragraph, line, word or character can be made.
* announce spelling errors under the cursor in Microsoft Word.
* support for the Microsoft Word 2007 spell checker. Partial support may be available for prior Microsoft Word versions.
* Better support for Windows Live Mail. Plain text messages can now be read and both the plain text and HTML message composers are useable.
* In Windows Vista, if the user moves to the secure desktop (either because a UAC control dialog appeared, or because control+alt+delete was pressed), NVDA will announce the fact that the user is now on the secure desktop.
* NVDA can announce text under the mouse within dos console windows.
* Support for UI Automation via the UI Automation client API available in Windows 7, as well as fixes to improve the experience of NVDA in Windows 7.
* NVDA can be configured to start automatically after you log on to Windows. The option is in the General Settings dialog.
* NVDA can read secure Windows screens such as the Windows logon, control+alt+delete and User Account Control (UAC) screens in Windows XP and above. Reading of the Windows logon screen can be configured from the General Settings dialog. (#97)
* Added a driver for the Optelec ALVA BC6 series braille displays.
* When browsing web documents, you can now press n and shift+n to skip forward and backward past blocks of links, respectively.
* When browsing web documents, ARIA landmarks are now reported, and you can move forward and backward through them using d and shift+d, respectively. (#192)
* The Links List dialog available when browsing web documents has now become an Elements List dialog which can list links, headings and landmarks. Headings and landmarks are presented hierarchically. (#363)
* The new Elements List dialog contains a "Filter by" field which allows you to filter the list to contain only those items including the text that was typed. (#173)
* Portable versions of NVDA now look in the 'userConfig' directory inside the NVDA directory, for the user's configuration. Like for the installer version, this keeps the user's configuration separate from NVDA itself.
* Custom app modules, braille display drivers and synth drivers can now be stored in the user's configuration  directory. (#337)
* Virtual buffers are now rendered in the background, allowing the user to interact with the system to some extent during the rendering process. The user will be notified that the document is being rendered if it takes longer than a second.
* If NVDA detects that it has frozen for some reason, it will automatically pass all keystrokes through so that the user has a better chance of recovering the system.
* Support for ARIA drag and drop in Mozilla Gecko. (#239)
* The document title and current line or selection is now spoken when you move focus inside a virtual buffer. This makes the behaviour when moving focus into virtual buffers consistent with that for normal document objects. (#210)
* In virtual buffers, you can now interact with embedded objects (such as Adobe Flash and Sun Java content) by pressing enter on the object. If it is accessible, you can then tab around it like any other application. To return focus to the document, press NVDA+space. (#431)
* In virtual buffers, o and shift+o move to the next and previous embedded object, respectively.
* NVDA can now fully access applications running as administrator in Windows Vista and later. You must install an official release of NVDA for this to work. This does not work for portable versions and snapshots. (#397)

### Changes

* NVDA no longer announces "NVDA started" when it starts.
* The startup and exit sounds are now played using NVDA's configured audio output device instead of the Windows default audio output device. (#164)
* Progress bar reporting has been improved. Most notably you can now configure NVDA to announce via both speech and beeps at the same time.
* Some generic roles, such as pane, application and frame, are no longer reported on focus unless the control is unnamed.
* The review copy command (NVDA+f10) copies the text from the start marker up to and including the current review position, rather than excluding the current position. This allows the last character of a line to be copied, which was not previously possible. (#430)
* the navigatorObject_where script (ctrl+NVDA+numpad5) has been removed. This key combination did not work on some keyboards, nore was the script found to be that useful.
* the navigatorObject_currentDimentions script has been remapped to NVDA+numpadDelete. The old key combination did not work on some keyboards. This script also now reports the width and height of the object instead of the right/bottom coordinates.
* Improved performance (especially on netbooks) when many beeps occur in quick succession; e.g. fast mouse movement with audio coordinates enabled. (#396)
* The NVDA error sound is no longer played in release candidates and final releases. Note that errors are still logged.

### Bug Fixes

* When NVDA is run from an 8.3 dos path, but it is installed in the related long path (e.g. progra~1 verses program files) NVDA will correctly  identify that it is an installed copy and properly load the user's settings.
* speaking the title of the current foreground window with nvda+t now works correctly when in menus.
* braille no longer shows useless information in its focus context such as unlabeled panes.
* stop announcing some useless information when the focus changes such as root panes, layered panes and scroll panes in Java or Lotus applications.
* Make the  keyword search field in Windows Help (CHM) viewer much more usable. Due to buggyness in that control, the current keyword could not be read as it would be continually changing.
* report correct page numbers in Microsoft Word if the page numbering has been specifically offset in the document.
* Better support for edit fields found in Microsoft Word dialogs (e.g. the Font dialog). It is now possible  to navigate these controls with the arrow keys.
* better support for Dos consoles. specifically: NVDA can now read the content of particular consoles it always used to think were blank. Pressing control+break no longer terminates NVDA.
* On Windows Vista and above, the NVDA installer now starts NVDA with normal user privileges when requested to run NVDA on the finish screen.
* Backspace is now handled correctly when speaking typed words. (#306)
* Don't incorrectly report "Start menu" for certain context menus in Windows Explorer/the Windows shell. (#257)
* NVDA now correctly handles ARIA labels in Mozilla Gecko when there is no other useful content. (#156)
* NVDA no longer incorrectly enables focus mode automatically for editable text fields which update their value when the focus changes; e.g. http://tigerdirect.com/. (#220)
* NVDA will now attempt to recover from some situations which would previously cause it to freeze completely. It may take up to 10 seconds for NVDA to detect and recover from such a freeze.
* When the NVDA language is set to "User default", use the user's Windows  display language setting instead of the Windows locale setting. (#353)
* NVDA now recognises the existence of controls in AIM 7.
* The pass key through command no longer gets stuck if a key is held down. Previously, NVDA stopped accepting commands if this occurred and had to be restarted. (#413)
* The taskbar is no longer ignored when it receives focus, which often occurs when exiting an application. Previously, NVDA behaved as if the focus had not changed at all.
* When reading text fields in applications which use the Java Access Bridge (including OpenOffice.org), NVDA now functions correctly when reporting of line numbers is enabled.
* The review copy command (NVDA+f10) gracefully handles the case where it is used on a position before the start marker. Previously, this could cause problems such as crashes in Notepad++.
* A certain control character (0x1) no longer causes strange eSpeak behaviour (such as changes in volume and pitch) when it is encountered in text. (#437)
* The report text selection command (NVDA+shift+upArrow) now gracefully reports that there is no selection in objects which do not support text selection.
* Fixed the issue where pressing the enter key on certain Miranda-IM buttons or links was causing NVDA to freeze. (#440)
* The current line or selection is now properly respected when spelling or copying the current navigator object.
* Worked around a Windows bug which was causing garbage to be spoken after the name of link controls in Windows Explorer and Internet Explorer dialogs. (#451)
* Fixed a problem with the report date and time command (NVDA+f12). Previously, date reporting was truncated on some systems. (#471)
* Fixed the issue where the system screen reader flag was sometimes inappropriately cleared after interacting with secure Windows screens. This could cause problems in applications which check the screen reader flag, including Skype, Adobe Reader and Jart. (#462)
* In an Internet Explorer 6 combo box, the active item is now reported when it is changed. (#342)

## 0.6p3

### New Features

* As Microsoft Excel's formula bar is inaccessible to NVDA, provide an NVDA specific dialog box for editing when the user presses f2 on a cell.
* Support for formatting in IAccessible2 text controls, including Mozilla applications.
* Spelling errors can now be reported where possible. This is configurable from the Document Formatting preferences dialog.
* NVDA can be configured to beep for either all or only visible progress bars. Alternatively, it can be configured to speak progress bar values every 10%.
* Links can now be identified in richedit controls.
* The mouse can now be moved to the character under the review cursor in most editable text controls. Previously, the mouse could only be moved to the center of the control.
* In virtual buffers, the review cursor now reviews the text of the buffer, rather than just the internal text of the navigator object (which is often not useful to the user). This means that you can navigate the virtual buffer hierarchically using object navigation and the review cursor will move to that point in the buffer.
* Handle some additional states on Java controls.
* If the title command (NVDA+t) is pressed twice, it spells the title. If pressed thrice, it is copied to the clipboard.
* Keyboard help now reads the names of modifier keys when pressed alone.
* Key names announced by keyboard help are now translatable.
* Added support for the recognized text field in SiRecognizer. (#198)
* Support for braille displays!
* Added a command (NVDA+c) to report the text on the Windows clipboard. (#193)
* In virtualBuffers, if NVDA automatically switches to focus mode, you can use the escape key to switch back to browse mode. NVDA+space can still also be used.
* In virtual buffers, when the focus changes or the caret is moved, NVDA can automatically switch to focus mode or browse mode as appropriate for the control under the caret. This is configured from the Virtual Buffers dialog. (#157)
* Rewritten SAPI4 synthesizer driver which replaces the sapi4serotek and sapi4activeVoice drivers and should fix the problems encountered with these drivers.
* The NVDA application now includes a manifest, which means that it no longer runs in compatibility mode in Windows Vista.
* The configuration file and speech dictionaries are now saved in the user's application data directory if NVDA was installed using the installer. This is necessary for Windows Vista and also allows multiple users to have individual NVDA configurations.
* Added support for position information for IAccessible2 controls.
* Added the ability to copy text to the clipboard using the review cursor. NVDA+f9 sets the start marker to the current position of the review cursor. NVDA+f10 retrieves the text between the start marker and the current position of the review cursor and copies it to the clipboard. (#240)
* Added support for some edit controls in pinacle tv software.
* When announcing selected text for long selections (512 characters or more), NVDA now speaks the number of selected characters, rather than speaking the entire selection. (#249)

### Changes

* If the audio output device is set to use the Windows default device (Microsoft Sound Mapper), NVDA will now switch to the new default device for eSpeak and tones when the default device changes. For example, NVDA will switch to a USB audio device if it automatically becomes the default device when it is connected.
* Improve performance of eSpeak with some Windows Vista audio drivers.
* reporting of links, headings, tables, lists and block quotes can now be configured from the Document Formatting settings dialog. Previously to configure these settings for virtual buffers, the virtual buffer settings dialog would have been used. Now all documents share this configuration.
* Rate is now the default setting in the speech synthesizer settings ring.
* Improve the loading and unloading of appModules.
* The title command (NVDA+t) now only reports the title instead of the entire object. If the foreground object has no name, the application's process name is used.
* Instead of virtual buffer pass through on and off, NVDA now reports focus mode (pass through on) and browse mode (pass through off).
* Voices are now stored in the configuration file by ID instead of by index. This makes voice settings more reliable across systems and configuration changes. The voice setting will not be preserved in old configurations and an error may be logged the first time a synthesizer is used. (#19)
* The level of a tree view item is now announced first if it has changed from the previously focused item for all tree views. Previously, this was only occurring for native Windows (SysTreeView32) tree views.

### Bug Fixes

* The last chunk of audio is no longer cut off when using NVDA with eSpeak on a remote desktop server.
* Fix problems with saving speech dictionaries for certain voices.
* Eliminate the lag when moving by units other than character (word, line, etc.) towards the bottom of large plain text documents in Mozilla Gecko virtual buffers. (#155)
* If speak typed words is enabled, announce the word when enter is pressed.
* Fix some character set issues in richedit documents.
* The NVDA log viewer now uses richedit instead of just edit to display the log. This improves reading by word with NVDA.
* Fix some issues related to embedded objects in richedit controls.
* NVDA now reads page numbers in Microsoft Word. (#120)
* Fix the issue where tabbing to a checked checkbox in a Mozilla Gecko virtual buffer and pressing space would not announce that the checkbox was being unchecked.
* Correctly report partially checked checkboxes in Mozilla applications.
* If the text selection expands or shrinks in both directions, read the selection as one chunk instead of two.
* When reading with the mouse, text in Mozilla Gecko edit fields should now be read.
* Say all should no longer cause certain SAPI5 synthesizers to crash.
* Fixed an issue which meant that text selection changes were not being read in Windows standard edit controls before the first focus change after NVDA was started.
* Fix mouse tracking in Java objects. (#185)
* NVDA no longer reports Java tree view items with no children as being collapsed.
* Announce the object with focus when a Java window comes to the foreground. Previously, only the top-level Java object was announced.
* The eSpeak synthesizer driver no longer stops speaking completely after a single error.
* Fix the issue whereby updated voice parameters (rate, pitch, etc.) were not saved when the voice was changed from the synthesizer settings ring.
* Improved the speaking of typed characters and words.
* Some new text that was previously not spoken in text console applications (such as some text adventure games) is now spoken.
* NVDA now ignores focus changes in background windows. Previously, a background focus change could be treated as if the real focus changed.
* Improved the detection of the focus when leaving context menus. Previously, NVDA often didn't react at all when leaving a context menu.
* NVDA now announces when the context menu is activated in the Start menu.
* The classic Start menu is now announced as Start menu instead of Application menu.
* Improved the reading of alerts such as those encountered in Mozilla Firefox. The text should no longer be read multiple times and other extraneous information will no longer be read. (#248)
* The text of focusable, read-only edit fields will no longer be included when retrieving the text of dialogs. This fixes, for example, the automatic reading of the entire license agreement in installers.
* NVDA no longer announces the unselection of text when leaving some edit controls (example: Internet Explorer address bar, Thunderbird 3 email address fields).
* When opening plain text emails in Outlook Express and Windows Mail, focus is correctly placed in the message ready for the user to read it. Previously the user had to press tab or click on the message in order to use cursor keys to read it.
* Fixed several major issues with the "Speak command keys" functionality.
* NVDA can now read text past 65535 characters in standard edit controls (e.g. a large file in Notepad).
* Improved line reading in MSHTML edit fields (Outlook Express editable messages and Internet Explorer text input fields).
* NVDA no longer sometimes freezes completely when editing text in OpenOffice. (#148, #180)

## 0.6p2

* Improved the default ESpeak voice in NVDA
* Added a laptop keyboard layout. Keyboard layouts can be configured from NVDA's  Keyboard settings dialog. (#60)
* Support for grouping items in SysListView32 controls, mainly found in Windows Vista. (#27)
* Report the checked state of treeview items in SysTreeview32 controls.
* Added shortcut keys for many of NVDA's configuration dialogs
* Support for IAccessible2 enabled applications such as Mozilla Firefox when running NVDA from portable media, with out having to register any special Dll files
* Fix a crash with the virtualBuffers Links List in Gecko applications. (#48)
* NVDA should no longer crash Mozilla Gecko applications such as Firefox and Thunderbird if NVDA is running with higher privilages than the Mozilla Gecko application. E.g. NVDA is  running as Administrator.
* Speech dictionaries (previously User dictionaries) now can be either case sensitive or insensitive, and the patterns can optionally be regular expressions. (#39)
* Whether or not NVDA uses a 'screen layout' mode for virtual buffer documents can now be configured from a settings dialog
* No longer report anchor tags with no href in Gecko documents as links. (#47)
* The NVDA find command now remembers what you last searched for, across all applications. (#53)
* Fix issues where the checked state would not be announced for some checkboxes and radio buttons in virtualBuffers
* VirtualBuffer pass-through mode is now specific to each document, rather than NVDA globally. (#33)
* Fixed some sluggishness with focus changes and incorrect speech interuption which sometimes occured when using NVDA on a system that had been on standby or was rather slow
* Improve support for combo boxes in Mozilla Firefox. Specifically when arrowing around them text isn't repeated, and when jumping out of them, ancestor controls are not announced unnecessarily. Also virtualBuffer commands now work when focused on one  when you are in a virtualBuffer.
* Improve accuracy of finding the statusbar in many applications. (#8)
* Added the NVDA interactive Python console tool, to enable developers to look at and manipulate NVDA's internals as it is running
* sayAll, reportSelection and reportCurrentLine scripts now work properly when in virtualBuffer pass-through mode. (#52)
* The increase rate and decrease rate scripts have been removed. Users should use the synth settings ring scripts (control+nvda+arrows) or the Voice settings dialog
* Improve the range and scale of the progress bar beeps
* Added more quick keys to the new virtualBuffers:  l for list, i for list item, e for edit field, b for button, x for checkbox, r for radio button, g for graphic, q for blockquote, c for combo box, 1 through 6 for respective heading levels, s for separator, m for frame. (#67, #102, #108)
* Canceling the loading of a new document in Mozilla Firefox now allows the user to keep using the old document's virtualBuffer if the old document hadn't yet really been destroyed. (#63)
* Navigating by words in virtualBuffers is now more accurate as  words do not accidentally contain text from more than one field. (#70)
* Improved accuracy of focus tracking and focus updating when navigating in Mozilla Gecko virtualBuffers.
* Added a findPrevious script (shift+NVDA+f3) for use in new virtualBuffers
* Improved sluggishness in Mozilla Gecko dialogs (in Firefox and Thunderbird). (#66)
* Add the ability to view the current log file for NVDA. it can be found in the NVDA menu -> Tools
* Scripts such as say time and date now take the current language in to account; punctuation and ordering of words now reflects the language
* The language combo box in NVDA's General settings dialog now shows full language names for ease of use
* When reviewing text in the current navigator object, the text is always up to date if it changes dynamically. E.g. reviewing the text of a list item in Task Manager. (#15)
* When moving with the mouse, the current paragraph of text under the mouse is now announced, rather than either all the text in that particular object or just the current word. Also audio coordinates, and announcement of object roles is optional, they are turned off by default
* Support for reading text with the mouse in Microsoft Word
* Fixed bug where leaving the menu bar in applications such as Wordpad would cause text selection to not be announced anymore
* In Winamp, the title of the track is no longer announced again and again when switching tracks, or pausing/resuming/stopping playback.
* In Winamp,  Added ability to announce state of the shuffle and repeat controls as they are switched. Works in the main window and in the playlist editor
* Improve the ability to activate particular fields in Mozilla Gecko virtualBuffers. May include clickable graphics, links containing paragraphs, and other weird structures
* Fixed an initial lag when opening NVDA dialogs on some systems. (#65)
* Add specific support for the Total Commander application
* Fix bug in the sapi4serotek driver where the pitch could get locked at a particular value, i.e. stays high after reading a capital letter. (#89)
* Announce clickable text and other fields as clickable in Mozilla Gecko VirtualBuffers. e.g.  a field which has an onclick HTML attribute. (#91)
* When moving around Mozilla Gecko virtualBuffers, scroll the current field in to view -- useful so sighted peers have an idea of where the user is up to in the document. (#57)
* Add basic support for ARIA live region show events in IAccessible2 enabled applications. Useful in the Chatzilla IRC application, new messages will now be read automatically
* Some slight improvements to help use ARIA enabled web applications,  e.g. Google Docs
* Stop adding extra blank lines to text when copying it from a virtualBuffer
* Stop the space key from activating a link in the Links List. Now it can be used like other letters in order to  start typing the name of a particular link you wish to go to
* The moveMouseToNavigator script (NVDA+numpadSlash) now moves the mouse to the centre of the navigator object, rather than the top left
* Added scripts to click the left and right mouse buttons (numpadSlash and numpadStar respectively)
* Improve access to the Windows System Tray. Focus hopefully should no longer seem to keep jumping back to one particular item. Reminder: to get to the System Tray use the Windows command WindowsKey+b. (#10)
* Improve performance and stop announcing extra text when holding down a cursor key in an edit field and it hits the end
* Stop the ability for NVDA to make the user wait while particular messages are spoken. Fixes some crashes/freezes with particular speech synthesizers. (#117)
* Added support for the Audiologic Tts3 speech synthesizer, contribution by Gianluca Casalino. (#105)
* Possibly improve performance when navigating around documents in Microsoft Word
* Improved accuracy when reading text of alerts in Mozilla Gecko applications
* Stop possible crashes when trying to save configuration on non-English versions of Windows. (#114)
* Add an NVDA welcome dialog. This dialog is designed to provide essential information for new users and allows CapsLock to be configured as an NVDA modifier key. This dialog will be displayed when NVDA is started by default until it is disabled.
* Fix basic support for Adobe Reader so it is possible to read documents  in  versions 8 and 9
* Fix some errors that may have occured when holding down keys before NVDA is properly initialized
* If the user has configured NVDA to save configuration on exit, make sure the configuration is properly saved when shutting down or logging out of  Windows.
* Added an NVDA logo sound to the beginning of the installer, contributed by Victer Tsaran
* NVDA, both running in the installer and otherwise, should properly clean up its system tray icon when it exits
* Labels for standard controls in NVDA's dialogs (such as Ok and cancel buttons) should now show in the language NVDA is set to, rather than just staying in English.
* NVDA's icon should now be  used for  the NVDA shortcuts in the start menu and on the Desktop, rather than a default application icon.
* Read cells in MS Excel when moving with tab and shift+tab. (#146)
* Fix some double speaking in particular lists in Skype.
* Improved caret tracking in IAccessible2 and Java applications; e.g. in Open Office and Lotus Symphony, NVDA properly waits for the caret to move in documents rather than accidentally reading the wrong word or line at the end of some paragraphs. (#119)
* Support for AkelEdit controls found in Akelpad 4.0
* NVDA no longer locks up in Lotus Synphony when moving from the document to the menu bar.
* NVDA no longer freezes in the Windows XP Add/Remove programs applet when launching an uninstaller. (#30)
* NVDA no longer freezes when opening Spybot Search and Destroy

## 0.6p1

### Access to web content with new in-process virtualBuffers (so far for Mozilla Gecko applications including Firefox3 and Thunderbird3)

* Load times have been improved almost by a factor of thirty (you no longer have to wait at all for most web pages to load in to the buffer)
* Added a links list (NVDA+f7)
* Improved the find dialog (control+nvda+f) so that it performs a case-insencitive search, plus fixed a few focus issues with that dialog box.
* It is now possible to select and copy text in the new virtualBuffers
* By default the new virtualBuffers represent the document in a screen layout (links and controls are not on separate lines unless they really are visually). You can toggle this feature with NVDA+v.
* It is possible to move by paragraph with control+upArrow and control+downArrow.
* Improved support for dynamic content
* Improved over all accuracy of reading lines and fields when arrowing up and down.

### Internationalization

* It is now possible to type accented characters that rely on a "dead character", while NVDA is running.
* NVDA now announces when the keyboard layout is changed (when pressing alt+shift).
* The announce date and time feature now takes the system's current regional and language options in to account.
* added czech translation (by Tomas Valusek with help from Jaromir Vit)
* added vietnamese translation by Dang Hoai Phuc
* Added Africaans (af_ZA) translation, by Willem van der Walt.
* Added russian translation by Dmitry Kaslin 
* Added polish translation by DOROTA CZAJKA and friends.
* Added Japanese translation by Katsutoshi Tsuji.
* added Thai translation by Amorn Kiattikhunrat
* added croatian translation by Mario Percinic and Hrvoje Katic  
* Added galician translation by Juan C. buno 
* added ukrainian translation by Aleksey Sadovoy 

### Speech

* NVDA now comes packaged with eSpeak 1.33 which contains many improvements, among those are improved languages, named variants, ability to speak faster.
* The voice settings dialog now allows you to change the variant of a synthesizer if it supports one. Variant is usually a slight variation on the current voice. (eSpeak supports variants).
* Added the ability to change the inflection of a voice in the voice settings dialog if the current synthesizer supports this. (eSpeak supports inflection).
* Added the ability to turn off speaking of object position information(e.g. 1 of 4). This option can be found in the Object presentation settings dialog.
* NVDA can now beep when speaking a capital letter. This can be turned on and off with a check box in the voice settings dialog. Also added a raise pitch for capitals check box to configure whether NVDA should actually do its normal pitch raise for capitals. So now you can have either raise pitch, say cap, or beep, for capitals.
* Added the ability to pause speech in NVDA (like found in Voice Over for the Mac). When NVDA is speaking something, you can press the control or shift keys to silence speech just like normal, but if you then tap the shift key again (as long as you havn't pressed any other keys) speech will continue from exactly where it left off.
* Added a virtual synthDriver which outputs text to a window instead of speaking via a speech synthesiser. This should be more pleasant for sighted developers who are not used to speech synthesis but want to know what is spoken by NVDA. There are probably still some bugs, so feedback is most definitely welcome.
* NVDA no longer by default speaks punctuation, you can enable speaking of punctuation with NVDA+p.
* eSpeak by default now speaks quite a bit slower, which should make it easier for people who are using eSpeak for the first time, when installing or starting to use NVDA.
* Added user dictionaries to NVDA. These allow you to make NVDA speak certain text differently. There are three dictionaries: default, voice, and temporary. Entries you add to the default dictionary will happen all the time in NVDA. Voice dictionaries are specific to the current synthesizer and voice you currently have set. And temporary dictionary is  for those times you quickly want to set a rule while you are doing a particular task, but you don't want it to be perminant (it will disappear if you close NVDA). For now the rules are regular expressions, not just normal text.
* Synthesizers can now use any audio output device on your system, by setting the output device combo box in the Synthesizer dialog before selecting the synthesizer you want.

### Performance

* NVDA no longer takes up a huge amount of system memory , when editing messages in mshtml edit controls
* Improved performance when reviewing text inside many controls that do not actually have a real cursor. e.g. MSN Messenger history window, treeview items, listview items etc.
* Improved performance in rich edit documents.
* NVDA should no longer slowly creep up in system memory size for no reason
* Fixed bugs when  trying to focus on a dos console window more than three or so times. NVDA did have a tendency to completely crash.

### Key commands

* NVDA+shift+numpad6 and NVDA+shift+numpad4 allow you to navigate to the next or previous object in flow respectively. This means that you can navigate in an application by only using these two keys with out having to worry about going up by parent, or down to first child as you move around the object hyerarchy. For instance in a web browser such as firefox, you could navigate the document by object, by just using these two keys. If next in flow or previous in flow takes you up and out of an object, or down in to an object, ordered beeps indicate the direction.
* You can now configure voice settings with out opening the voice settings dialog, by using the Synth Settings Ring. The synth settings ring is a group of voice settings you can toggle through by pressing control+NVDA+right and control+NVDA+left. To change a setting use control+NVDA+up and control+NVDA+down.
* Added a command to report the current selection in edit fields (NVDA+shift+upArrow).
* Quite a few NVDA commands that speak text (such as report current line etc) now can spell the text if pressed twice quickly.
* the capslock, numpad insert and extended insert can all be used as the NVDA modifier key. Also if one of these keys is used, pressing the key twice with out pressing any other keys will send the key through to the operating system, just like you'd pressed the key with out NVDA running. To make one of these keys be the NVDA modifier key, check its checkbox in the Keyboard settings dialog (used to be called the keyboard echo dialog).

### Application support

* Improved support for Firefox3 and Thunderbird3 documents. Load times have been improved by almost a factor of thirty, a screen layout is used by default (press nvda+v to toggle between this and no screen layout), a links list (nvda+f7 has been added), the find dialog (control+nvda+f) is now case-insensitive, much better support for dynamic content, selecting and copying text is now possible.
* In the MSN Messenger and Windows Live Messenger history windows, it is now possible to select and copy text.
* Improved support for the audacity application
* Added support for a few edit/text controls in Skype
* Improved support for Miranda instant messenger application
* Fixed some focus issues when opening html and plain text messages in Outlook Express. 
* Outlook express newsgroup message fields are now labeled correctly
* NVDA can now read the addresses in the Outlook Express message fields (to/from/cc etc)
* NVDA should be now more accurate at announcing the next message in out look express when deleting a message from the message list.

### APIs and toolkits

* Improved object navigation for MSAA objects. If a window has a system menu, title bar, or scroll bars, you can now navigate to them.
* Added support for the IAccessible2 accessibility API. A part from the ability to announce more control types, this also allows NVDA to access the cursor in applications such as Firefox 3 and Thunderbird 3, allowing you to navigate, select or edit text.
* Added support for Scintilla edit controls (such controls can be found in Notepad++ or Tortoise SVN).
* Added support for Java applications (via the Java Access Bridge). This can provide basic support for Open Office (if Java is enabled), and any other stand-alone Java application. Note that java applets with in a web browser may not work yet.

### Mouse

* Improved support for reading what is under the mouse pointer as it moves. It is now much faster, and it also now has the ability in some controls such as standard edit fields, Java and IAccessible2 controls, to read the current word, not just the current object. This may be of some used to vision impared people who just want to read a specific bit of text with the mouse.
* Added a new config option, found in the mouse settings dialog. Play audio when mouse moves, when checked, plays a 40 ms beep each time the mouse moves, with its pitch (between 220 and 1760 hz) representing the y axis, and left/right volume, representing the x axis. This enables a blind person to get a rough idea of where the mouse is on the screen as its being moved. This feature also depends on reportObjectUnderMouse also being turned on. So this means that if you quickly need to disable both beeps and announcing of objects, then just press NVDA+m. The beeps are also louder or softer depending on how bright the screen is at that point.

### Object presentation and interaction

* Improved support for most common treeview controls. NVDA now tells you how many items are in the branch when you expand it. It also announces the level when moving in and out of branches. And, it announces the current item number and number of items, according to the current branch, not the entire treeview.
* Improved what is announced when focus changes as you move around applications or the operating system. Now instead of just hearing the control you land on, you hear information about any controls this control is positioned inside of. For instance if you tab and land on a button inside a groupbox, the groupbox will also get announced.
* NVDA now tries to speak the message inside many dialog boxes as they appear. This is accurate most of the time, though there are still many dialogs that arn't as good as they could be.
* Added a report object descriptions checkbox to the object presentation settings dialog. Power users may wish to sometimes uncheck this to stop NVDA announcing a lot of extra descriptions on particular controls,  such as in Java applications.
* NVDA automatically announces selected text in edit controls when focus moves to them. If there isn't any selected text, then it just announces the current line like usual.
* NVDA is a lot more careful now when it plays beeps to indicate progress bar changes in applications. It no longer goes crazy in Eclipse applications such as Lotus Notes/Symphony, and Accessibility Probe.

### User Interface

* Removed the NVDA interface window, and replaced it with a simple NVDA popup menu.
* NVDA's user interface settings dialog is now called General Settings. It also contains an extra setting: a combo box to set the log level, for what messages should go to NVDA's log file. Note that NVDA's log file is now called nvda.log not debug.log.
* Removed the report object group names checkBox from the object presentation settings dialog, reporting of group names now is handled differently.

## 0.5

* NVDA now has a built-in synthesizer called eSpeak, developed by Jonathan Duddington.It is very responsive and lite-weight, and has support for many different languages. Sapi synthesizers can still be used, but eSpeak will be used by default.
 * eSpeak does not depend on any special software to be installed, so it can be used with NVDA on any computer, on a USB thumb drive, or anywhere. 
 * For more info on eSpeak, or to find other versions, go to http://espeak.sourceforge.net/.
* Fix bug where the wrong character was being announced when pressing delete in Internet Explorer / Outlook Express editable panes.
* Added support for more edit fields in Skype.
* VirtualBuffers only get loaded when focus is on the window that needs to be loaded. This fixes some problems when the preview pane is turned on in Outlook Express.
* Added commandline arguments to NVDA:
 * -m, --minimal: do not play startup/exit sounds and do not show the interface on startup if set to do so.
 * -q, --quit: quit any other already running instance of NVDA and then exit
 * -s, --stderr-file fileName: specify where NVDA should place uncaught errors and exceptions
 * -d, --debug-file fileName: specify where NVDA should place debug messages
 * -c, --config-file: specify an alternative configuration file  
 * -h, -help: show a help message listing commandline arguments
* Fixed bug where punctuation symbols would not be translated to the appropriate language, when using a language other than english, and when speak typed characters was turned on.
* Added Slovak language files thanks to Peter Vagner 
* Added a Virtual Buffer settings dialog and a Document Formatting settings dialog, from Peter Vagner.
* Added French translation thanks to Michel Such 
* Added a script to toggle beeping of progress bars on and off (insert+u). Contributed by Peter Vagner.
* Made more messages in NVDA be translatable for other languages. This includes script descriptions when in keyboard help.
* Added a find dialog to the virtualBuffers (internet Explorer and Firefox). Pressing control+f when on a page brings up a dialog in which you can type some text to find. Pressing enter will then search for this text and place the virtualBuffer cursor on this line. Pressing f3 will also search for the next occurance of the text.
* When speak typed characters is turned on, more characters should be now spoken. Technically, now ascii characters from 32 to 255 can now be spoken.
* Renamed some control types for better readability. Editable text is now edit, outline is now tree view and push button is now button.
* When arrowing around list items in a list, or tree view items in a tree view, the control type (list item, tree view item) is no longer spoken, to speed up navigation.
* Has Popup (to indicate that a menu has a submenu) is now spoken as submenu.
* Where some language use control and alt (or altGR) to enter a special character, NVDA now will speak these characters when speak typed characters is on.
* Fixed some problems with reviewing static text controls.
* Added Translation for Traditional Chinese, thanks to Coscell Kao.
* Re-structured an important part of the NVDA code, which should now fix many issues with NVDA's user interface (including settings dialogs).
* Added Sapi4 support to NVDA. Currently there are two sapi4 drivers, one based on code contributed by Serotek Corporation, and one using the ActiveVoice.ActiveVoice com Interface. Both these drivers have issues, see which one works best for you.
* Now when trying to run a new copy of NVDA while an older copy is still running will cause the new copy to just exit. This fixes a major problem where running multiple copies of NVDA makes your system very unusable.
* Renamed the title of the NVDA user interface from NVDA Interface to NVDA. 
* Fixed a bug in Outlook Express where pressing backspace at the start of an editable message would cause an error.
* Added patch from Rui Batista that adds a script to report the current battery status on laptops (insert+shift+b).
* Added a synth driver called Silence. This is a synth driver that does not speak anything, allowing NVDA to stay completely silent at all times. Eventually this could be used along with Braille support, when we have it.
* Added capitalPitchChange setting for synthesizers thanks to J.J. Meddaugh
* Added patch from J.J. Meddaugh that makes the toggle report objects under mouse script more like the other toggle scripts (saying on/off rather than changing the whole statement).
* Added spanish translation (es) contributed by Juan C. buo.
* Added Hungarian language file from Tamas Gczy.
* Added Portuguese language file from Rui Batista.
* Changing the voice in the voice settings dialog now sets the rate, pitch and volume sliders to the new values according to the synthesizer, rather than forcing the synthesizer to be set to the old values. This fixes issues where a synth like eloquence or viavoice seems to speek at a much faster rate than all other synths.
* Fixed a bug where either speech would stop, or NVDA would entirely crash, when in a Dos console window.
* If support for a particular language exists, NVDA now automatically can show its interface and speak its messages in the language Windows is set to. A particular language can still be chosen manualy from the user interface settings dialog as well.
* Added script 'toggleReportDynamicContentChanges' (insert+5). This toggles whether new text, or other dynamic changes should be automatically announced. So far this only works in Dos Console Windows.
* Added script 'toggleCaretMovesReviewCursor' (insert+6). This toggles whether the review cursor should be automatically repositioned when the system caret moves. This is useful in Dos console windows when trying to read information as the screen is updating.
* Added script 'toggleFocusMovesNavigatorObject' (insert+7). This toggles whether the navigator object is repositioned on the object with focus as it changes.
* Added some documentation translated in to various languages. So far there is French, Spannish and Finish.
* Removed some developer documentation from the binary distribution of NVDA, it is only now in the source version.
* Fixed a possible bug in Windows Live Messanger and MSN Messenger where arrowing up and down the contact list would cause errors.
* New messages are now automatically spoken when in a conversation using Windows Live Messenger. (only works for English versions so far)
* The history window in a Windows Live Messenger conversation can now be read by using the arrow keys. (Only works for English versions so far) 
* Added script 'passNextKeyThrough' (insert+f2). Press this key, and then the next key pressed will be passed straight through to Windows. This is useful if you have to press a certain key in an application but NVDA uses that key for something else.
* NVDA no longer freezes up for more than a minute when opening very large documents in MS Word.
* Fixed a bug where moving out of a table in MS Word, and then moving back in, caused the current row/column numbers not to be spoken if moving back in to exactly the same cell.
* When starting NVDA with a synthesizer that doesn't exist, or is not working, the sapi5 synth will try and be loaded in stead, or if sapi5 isn't working, then speech will be set to silence.
* Increasing and decreasing rate scripts can no longer take the rate above 100 or below 0.
* If there is an error with a language when choosing it in the User Interface Settings dialog, a message box will alert the user to the fact.
* NVDA now asks if it should save configuration and restart if the user has just changed the language in the User Interface Settings Dialog. NVDA must be restarted for the language change to fully take effect.
* If a synthesizer can not be loaded, when choosing it from the synthesizer dialog, a message box alerts the user to the fact.
* When loading a synthesizer for the first time, NVDA lets the synthesizer choose the most suitable voice, rate and pitch parameters, rather than forcing it to defaults it thinks are ok. This fixes a problem where Eloquence and Viavoice sapi4 synths start speaking way too fast for the first time.
