# Co nowego w NVDA?

## 2024.3

Add-on store od teraz powiadamia o dostępności aktualizacji dodatków po uruchomieniu NVDA.

Dodano opcje do włączenia normalizacji unicode, obejmującą mowę i brajl.
To może być użyteczne podczas czytania znaków,  nierozpoznawalnych przez syntezator mowy albo znaków niezdefiniowanych w tablicy brajlowskiej. Takie znaki zazwyczaj posiadają zgodną alternatywę. Są to na przykład litery pogrubione lub kursywne, zazwyczaj używane w mediach społecznościowych.
Ta opcja także umożliwia czytanie równań w edytorze równań programu Microsoft Word.

Monitory brajlowskie Help Tech Activator Pro od teraz są wspierane.

Dodano nieprzydzielone skróty klawiszowe do pionowej i poziomej nawigacji kółkiem myszy.

Naprawione niektóre błędy ogólnie w panelu Emoji w systemie Windows 11 i historii schowka.
Naprawiono błędy także w przeglądarkach internetowych.  Poprawki dotyczą komunikatów o zgłaszaniu błędów, odczytu figur i podpisów, oznaczeń tabel a także elementów meni pól wyboru/przycisków opcji.

Liblouis został zaktualizowany z dodanymi nowymi tablicami brajlowskimi dla serbskiej cyrylicy, Jidysz, kilka starożytnych języków, tureckiego i międzynarodowego alfabetu fonetycznego.
eSpeak został zaktualizowany z dodanym wsparciem dla języka karakałpackiego.
Unicode CLDR także został zaktualizowany.

### Nowości

* Nowe skróty klawiszowe:
  * Dodano nieprzydzielone polecenia do przewijania kółka myszy w lewo, prawo górę i w dół w celu ulepszenia nawigacji po web stronach i aplikacjach z treścią dynamiczną, takich jak Dism++. (#16462, @Cary-Rowen)
* Dodano opcje do normalizacji unicode, obejmującą mowę i brajl. (#11570, #16466 @LeonarddeR).
  * To może być użyteczne podczas czytania znaków,  nierozpoznawalnych przez syntezator mowy albo znaków niezdefiniowanych w tablicy brajlowskiej. Takie znaki zazwyczaj posiadają zgodną alternatywę. Są to na przykład litery pogrubione lub kursywne, zazwyczaj używane w mediach społecznościowych.
  * Ta opcja także umożliwia czytanie równań w edytorze równań programu Microsoft Word. (#4631)
  * Tą opcje można włączyć oddzielnie dla brajla i mowy w przeznaczonych do tego kategoriach w ustawieniach NVDA.
* Od teraz, domyślnie po uruchomieniu NVDA, wyświetli się powiadomienie o dostępnych aktualizacjach dodatków. (#15035)
  * To można wyłączyć w kategorii "Add-on Store" ustawień.
  * NVDA sprawdza aktualizacje dodatków dziennie.
  * Aktualizacje dodatków będą sprawdzane z jednego kanału. Na przykład, zainstalowane dodatki z kanału beta będą sprawdzane z kanału beta.
* Dodano wsparcie dla monitorów brajlowskich Help Tech Activator Pro. (#16668)

### Zmiany

* Aktualizacje komponentów:
  * eSpeak NG został zaktualizowany do 1.52-dev commit `54ee11a79`. (#16495)
    * Dodany nowy język karakałpacki.
  * Zaktualizowano Unicode CLDR do wersji 45.0. (#16507, @OzancanKaratas)
  * Zaktualizowano fast_diff_match_patch (używany do wykrywania zmian w aplikacjach konsolowych i innych treściach dynamicznych) do wersji 2.1.0. (#16508, @codeofdusk)
  * Zaktualizowano LibLouis braille translator to [3.30.0](https://github.com/liblouis/liblouis/releases/tag/v3.30.0). (#16652, @codeofdusk)
    * Nowe tablice brajlowskie:
      * Serbski cyrylica.
      * Jidysz.
      * niektóre języki starożytne: hebrajski biblijny, akadyjski, syryjski, ugarycki i transliterowany tekst pisma klinowego.
      * tureckie skróty. (#16735)
      * międzynarodowy alfabet fonetyczny. (#16773)
  * Zaktualizowano NSIS do wersji 3.10 (#16674, @dpy013)
  * Zaktualizowano markdown do wersji 3.6 (#16725, @dpy013)
  * Zaktualizowano nh3 to 0.2.17 (#16725, @dpy013)
* Alternatywna tablica brajlowska do wpisywania znaków na monitorze brajlowskim od teraz jest taka sama jak alternatywna tablica brajlowska wyświetlania. Jest to Ujednolicony brajl angielski (UEB) pismo pełne. (#9863, @JulienCochuyt, @LeonarddeR)
* Figury bez dostępnych obiektów podrzędnych, ale z dostępną oznaką lub opisem będą odczytywane przez NVDA. (#14514)
* Podczas czytania po wierszach w trybie czytania, słowo "podpis" nie jest już wymawiane w każdej linii długiej figury lub podpisu tabeli. (#14874)
* W konsoli  Pythona ostatnie niewypełnione polecenie nie będzie stracone podczas przemieszczania się po historii wejścia. (#16653, @CyrilleB79)
* Od teraz podczas zbierania statystyk do NV access wysyłany jest unikatowy identyfikator użytkownika. (#16266)
* Podczas tworzenia przenośnej kopii, będzie tworzony nowy katalog.
Od teraz, jeżeli zostanie podjęta próba pisania do pełnego katalogu, będzie pokazane ostrzeżenie. (#16686)

### Poprawki błędów

* Poprawki dla Windowsa 11:
  * NVDA już nie będzie się zawieszała podczas zamykania panelu emoji i historii schowka. (#16346, #16347, @josephsl)
  * NVDA znowu będzie czytała widoczne kandydaty podczas otwarzania interfejsu Ime. (#14023, @josephsl)
  * NVDA nie będzie czytała dwukrotnie "historia schowka" podczas poruszania się po elementach meni panelu emoji. (#16532, @josephsl)
  * NVDA już nie będzie wycinała mowę i brajl podczas przeglądu symboli i kaomoji w panelu emoji. (#16533, @josephsl)
* Poprawki dla przeglądarek internetowych:
  * Komunikaty o błędach z odwołaniem do atrybutu  `aria-errormessage` od teraz są czytane w przeglądarkach Google Chrome i Mozilla firefox. (#8318)
  * Jeżeli są dostępne, NVDA będzie używała atrybutu `aria-labelledby` aby dostarczyć dostępne nazwy dla tabel w przeglądarce Mozilla Firefox. (#5183)
  * NVDA od teraz poprawnie będzie czytać elementy meni w postaci przycisków opcji i pól wyboru podczas pierwszego wejścia do meni rozwijanego w przeglądarkach Google Chrome i Mozilla Firefox. (#14550)
  * Funkcja wyszukiwania NVDA od teraz jest bardziej dokładniejsza gdy strona internetowa zawiera znaki emoji. (#16317, @LeonarddeR)
  * W przeglądarce  Mozilla Firefox, NVDA od teraz poprawnie odczytuje bieżący znak, słowo oraz wiersz gdy kursor znajduje się w punkcie wstawiania na końcu wiersza. (#3156, @jcsteh)
  * Google chrome już nie wysypuje się w procesie zamykania. (#16893)
* NVDA od teraz prawidłowo czyta podpowiedzi autouzupełniania w Eclipse i innych środowiskach opartych na Eclipse w systemie Windows 11. (#16416, @thgcode)
* Ulepszona niezawodność automatycznego odczytu, ogólnie w aplikacjach konsolowych. (#15850, #16027, @Danstiv)
* Przywracanie konfiguracji stało się bardziej niezawodne. (#16755, @Emil-18)
* NVDA poprawnie odczyta zmiany zaznaczenia podczas edycji tekstu komórki w programie Microsoft Excel. (#15843)
* W programach wykorzystujących technologię Java Access Bridge, NVDA poprawnie przeczyta ostatni pusty wiersz tekstu zamiast powtarzania przedostatniego. (#9376, @dmitrii-drobotov)
* W programie LibreOffice Writer (wersji 24.8 i nowszych), podczas włączania lub wyłączania formatowania tekstu (pogrubienie, kursywa, podkreślenie, indeks dolny/indeks górny, wyrównanie) używając odpowiednich skrótów klawiszowych, NVDA przeczyta włączony atrybut formatowania (np. "pogrubienie tak", "pogrubienie nie"). (#4248, @michaelweghorn)
* Podczas poruszania się klawiszami strzałek w polach edycyjnych w programach używających interfejsu UI Automation, NVDA już nie odczytuje błędnego znaku, słowa, itd. (#16711, @jcsteh)
* Podczas wklejania do Kalkulatora w systemach Windows 10/11 NVDA od teraz przeczyta pełną liczbę. (#16573, @TristanBurchett)
* Mowa już nigdy więcej nie zniknie podczas ponownego podłączenia do sesji pulpitu zdalnego. (#16722, @jcsteh)
* Dodano wsparcie poleceń przeglądu tekstu dla nazwy obiektu w Visual Studio Code. (#16248, @Cary-Rowen)
* Od teraz dźwięk będzie poprawnie odtwarzany na audiourządzeniach mono. (#16770, @jcsteh)
* NVDA od teraz przeczyta adresy podczas nawigacji po polach do/dw/UDW w programach outlook.com i współczesnym Outlooku. (#16856)
* NVDA od teraz lepiej radzi z niepoprawnie zainstalowanymi dodatkami. (#16704)

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

Dodano nową funkcję "podzielony dźwięk".
Ta funkcja umożliwia rozdzielenie dźwięku NVDA na przykład w lewym kanale gdy dźwięki z innych programów będą przekierowane do innego kanału na przykład prawego.

Dodano nowe polecenia do modyfikowania ustawień w pierścieniu ustawień mowy, tym samym umożliwiając użytkownikowi przemieszczanie sie od pierwszego do ostatniego ustawienia, a także do zmniejszania lub zwiększania ustawień w większych krokach.
Dodano także nowe polecenia do szybkiej nawigacji, umożliwiając użytkownikowi przemieszczanie się pomiędzy: akapitami, pionowo wyrównanymi akapitami, tekstem tego samego stylu, tekstem różnego stylu, elementami menu, przyciskami przełączania, paskami postępu, figurami, i formułami matematycznymi.

Dodano dużo nowych funkcji brajla, wraz z poprawkami błędów.
Nowy tryb brajla "wyświetlanie mowy" został dodany.
Gdy jest aktywny, monitor brajlowski dokładnie pokazuje, co NVDA wymówi.
Dodano także wsparcie do monitorów brajlowskich BrailleEdgeS2, BrailleEdgeS3.
Zaktualizowano LibLouis dodając nowe tablice brajlowskie z włączonym pokazywaniem wielkich liter dla języków białoruskiego i ukraińskiego, nową tablicę brajlowską do jezyka laotańskiego, a także   tablicę brajlowską dla języka hiszpańskiego ze wsparciem odczytu greki.

eSpeak został zaktualizowany z dodanym nowym językiem Tigrinya.

Naprawiono dużo błędó w aplikacjach, takich jak Thunderbird, Adobe Reader, przeglądarkach internetowych, Nudi i Geekbench.

### Nowości

* Nowe skróty klawiszowe:
  * Nowy skrót szybkiej nawigacji `p` do przemieszczania się po akapitach tekstu w trybie czytania. (#15998, @mltony)
  * Nowe nieprzydzielone skróty szybkiej nawigacjido przemieszczania się po:
    * figurach (#10826)
    * pionowo wyrównanych akapitach (#15999, @mltony)
    * elementach menu (#16001, @mltony)
    * przyciskach przełączania (#16001, @mltony)
    * paskach postępu (#16001, @mltony)
    * formułach matematycznych (#16001, @mltony)
    * tekstach tego samego stylu (#16000, @mltony)
    * tekstach o różnych stylach (#16000, @mltony)
  * Dodano polecenia do przemieszczania się po pierwszym i ostatnim ustawieniu pierścienia mowy. (#13768, #16095, @rmcpantoja)
    * Ten skrót nie jest domyślnie skojarzony. (#13768)
    * Zmniejszanie lub zwiększanie ustawień pierścienia mowy większymi krokami (#13768):
      * dla komputerów stacjonarnych: `NVDA+control+pageUp` or `NVDA+control+pageDown`.
      * dla komputerów przenośnych: `NVDA+control+shift+pageUp` or `NVDA+control+shift+pageDown`.
  * Dodano nowy nieprzydzielony skrót do regulacji odczytu figur i podpisów. (#10826, #14349)
* Brajl:
  * Dodano wsparcie dla monitorów brajlowskich BrailleEdgeS2 i BrailleEdgeS3. (#16033, #16279, @EdKweon)
  * Dodano nowy tryb brajla "wyświetlanie mowy". (#15898, @Emil-18)
    * Gdy jest aktywny, monitor brajlowski wyświetla to, co NVDA wymawia.
    * można go włączać lub wyłączać za pomocą skrótu `NVDA+alt+t`, lub z okna dialogowego ustawień brajla.
* Tryb podzielonego dźwięku: (#12985, @mltony)
  * Ta funkcja umożliwia rozdzielenie dźwięku NVDA na przykład w lewym kanale gdy dźwięki z innych programów będą przekierowane do innego kanału na przykład prawego.
  * Można przełączać za pomocą `NVDA+alt+s`.
* Odczyt nagłówków wierszy i kolumn w HTML elementach contenteditable. (#14113)
* Dodano opcję do wyłączenia odczytu figur i podpisów w ustawieniach formatowania dokumentów. (#10826, #14349)
* W systemie Windows 11, NVDA będzie odczytywała alerty pochodzące od wpisywania głosowego, a także sugerowane działania, wraz z działaniem o kopiowaniu danych, takich jak numerów telefonów do schowka (Windows 11 aktualizacja 2022 i nowsze). (#16009, @josephsl)
* NVDA zostawi włączone i obudzone urządzenie dźwiękowe po zatrzymaniu mowy, w celu zapobiegania cięcia następnej wypowiedzi na niektórych urządzeniach audio takich jak słuchawki Bluetooth. (#14386, @jcsteh, @mltony)
* HP Secure Browser jest od teraz wspierany. (#16377)

### Zmiany

* Add-on Store:
  * Minimalna i ostatnia testowana wersja są wyświetlane w rozdziale dla każdego dodatku "inne szczegóły" . (#15776, @Nael-Sayegh)
  * Działanie recenzji społeczności  będzie dostępne we wszystkich kartach właściwości add-on store. (#16179, @nvdaes)
* Aktualizacje komponentów:
  * Zaktualizowano LibLouis Braille translator do wersji [3.29.0](https://github.com/liblouis/liblouis/releases/tag/v3.29.0). (#16259, @codeofdusk)
    * Nowe tablice brajlowskie z możliwością wyświetlania wielkich liter dla języków białoruskiego i ukraińskiego.
    * Nowa tablica brajlowska dla języka hiszpańskiego ze wsparciem odczytu greki.
    * Nowa tablica brajlowska dla języka laotańskiego, pismo pełne. (#16470)
  * eSpeak NG został zaktualizowany do wersji 1.52-dev commit `cb62d93fd7`. (#15913)
    * Dodano nowy język Tigrinya. 
* Zmieniono kilka skrótów klawiszowych dla urządzeń BrailleSense w celu zapobiegania konfliktów ze znakami w tablicy brajlowskiej dla języka francuzkiego. (#15306)
  * `alt+strzałka w lewo` została skojarzona z  `punkt2+punkt7+spacja`
  * `alt+strzałka w prawo` została skojarzona z `punkt5+punkt7+spacja`
  * `alt+strzałka w górę` została skojarzona z `punkt2+punkt3+punkt7+spacja`
  * `alt+strzałka w dół` została skojarzona z `punkt5+punkt6+punkt7+spacja`
* Kropki, najczęściej używane w spisach treści nie są wymawiane na nizkich poziomach symboli. (#15845, @CyrilleB79)

### Poprawki błędów

* Poprawki błędów dla Windows 11:
  * NVDA ponownie może wymawiać podpowiedzi podczas wpisywania na klawiaturze sprzętowej. (#16283, @josephsl)
  * W wersji 24H2 (aktualizacja 2024 i Windows Server 2025), mysz i interakcja dotykiem mogą być używane w szybkich ustawieniach. (#16348, @josephsl)
* Add-on Store:
  * Gdy skrót klawiszowy`ctrl+tab` jest naciśnięty, fokus poprawnie się przemieszcza do nowego bieżącego tytułu karty właściwości. (#14986, @ABuffEr)
  * NVDA nie będzie się ponownie uruchamiała gdy pliki pamięci podręcznej są nieprawidłowe. (#16362, @nvdaes)
* Poprawki dla przeglądarek opartych na silniku Chromium gdy są używane z Uia:
  * Naprawiono błędy, powodujące zawieszanie się NVDA. (#16393, #16394)
  * Klawisz Backspace od teraz działa  prawidłowo w polach edycji logowania w Gmailu. (#16395)
* Klawisz backspace od teraz działa prawidłowo podczas używania programu Nudi 6.1 z włączoną opcją "Przetwarzaj klawisze z innych aplikacji". (#15822, @jcsteh)
* Naprawiono błąd gdy współrzędne dźwiękowe zostaną odtworzone gdy aplikacje znajdują się w trybie uśpienia, a opcja "Sygnalizuj dźwiękiem położenie myszy" jest włączona. (#8059, @hwf1324)
* W programie Adobe Reader, NVDA już nie ignoruje tekstu alternatywnego w formułach ustawionych w plikach Pdf. (#12715)
* Naprawiono błąd, który skutkował niemożliwością odczytu wstążki w programie Geekbench przez NVDA. (#16251, @mzanm)
* Naprawiono rzadki błąd przez który nie wszystkie profile konfiguracji były zachowane. (#16343, @CyrilleB79)
* W Firefoxie i w przeglądarkach opartych na Chromium, NVDA poprawnie wejdzie do trybu fokusu w polach edycyjnych w listach prezentacyjnych (ul / ol). (#16325)
* Stan kolumn jest automatycznie odczytywany podczas zaznaczania kolumn w liście wiadomości w Thunderbirdzie. (#16323)
* Opcja wiersza poleceń `-h`/`--help` ponownie działa prawidłowo. (#16522, @XLTechie)
* Wsparcie dla programu Poedit używanego do tłumaczenia w wersji 3.4 lub nowszej, działa poprawnie podczas tłumaczenia na języki z jedną lub dwie formy liczby mnogiej (na przykład, dla chińskiego i polskiego). (#16318)

### Changes for Developers

Please refer to [the developer guide](https://www.nvaccess.org/files/nvda/documentation/developerGuide.html#API) for information on NVDA's API deprecation and removal process.

* Instantiating `winVersion.WinVersion` objects with unknown Windows versions above 10.0.22000 such as 10.0.25398 returns "Windows 11 unknown" instead of "Windows 10 unknown" for release name. (#15992, @josephsl)
* Make the AppVeyor build process easier for NVDA forks, by adding configurable variables in appveyor.yml to disable or modify NV Access specific portions of the build scripts. (#16216, @XLTechie)
* Added a how-to document, explaining the process of building NVDA forks on AppVeyor. (#16293, @XLTechie)

## 2024.1

Dodano nowy tryb mowy "na żądanie".
Gdy tryb mowy na żądanie jest ustawiony, NVDA Nie mówi automatycznie (na przykład, podczas poruszania się strzałkami) ale mówi podczas naciskania skrótów klawiszowych,  które mają za cel wymawianie poszczególnej informacji (na przykład, odczyt tytułu okna).
Od teraz jest możliwe wykluczenie trybów mowy, których nie potrzebujemy z poziomu ustawień mowy w ustawieniach NVDA podczas używania polecenia przełącz tryb mowy (`NVDA+s`).

Od teraz dostępny jest nowy tryb kopiowania z zachowaniem formatowania w trybie czytania , który można przełączać za pomocą skrótu `NVDA+shift+f10`).
Gdy jest włączony, będzie używany tryb zaznaczania Firefoxu.
Polecenie kopiowania tekstu za pomocą skrótu `control+c` zostanie przekierowane do Firefoxa. To spowoduje kopiowane formatowania zamiast czystego tekstu.

Add-on Store wspiera wielokrotne działania (na przykład instalowanie, włączanie dodatków) zaznaczając wiele dodatków
Dodano nowe działanie do otwierania strony z recenzjami dodatku.

Opcje "Karta dźwiękowa" i "tryb przyciszania audio" zostały usunięte z okna dialogowego"wybór syntezatora".
Można je znaleźć w ustawieniach dźwięku, które można otworzyć za pomocą skrótu `NVDA+control+u`.

eSpeak-NG, LibLouis braille translator, i repozytorium znaków Unicode zostały zaktualizowane.
Nowe tablice brajlowskie dla Tajskiego, filipińskiego i rumuńskiego zostały dodane.

Naprawiono dużo błędów, szczególnie z Add-on Storem, wsparciem brajla, wsparciem dla Libre Office, Microsoft Office i wsparciem dźwięku.

### Uwagi

* Ta wersja nie jest zgodna z istniejącymi dodatkami.
* Systemy operacyjne Windows 7 i Windows 8 nie są więcej wspierane.
Windows 8.1 jest minimalną wspieraną wersją systemu Windows.

### Nowości

* Add-on Store:
  * Add-on Store od teraz wspiera wielokrotne działania (na przykład instalowanie, włączanie i wyłączanie dodatków) zaznaczając więcej dodatków. (#15350, #15623, @CyrilleB79)
  * Dodano nowe działanie służace do otwierania  dedykowanej strony do zaopiniowania lub czytania recenzji o dodatku. (#15576, @nvdaes)
* Dodano wsparcie dla Bluetooth niskonapięciowych monitorów brajlowskich HID. (#15470)
* Nowy tryb kopiowania z zachowaniem formatowania przełączany za pomocą  skrótu `NVDA+shift+f10` jest dodany do trybu czytania dla Mprzeglądarki Mozilla firefox.
Gdy jest włączony, zaznaczanie będzie sterowane z poziomu przeglądarki Mozilla firefox.
Polecenie kopiowania tekstu za pomocą skrótu `control+c` zostanie przekierowane do Firefoxa. To spowoduje kopiowanie formatowania zamiast czystego tekstu.
Miewajcie na uwadze, że gdy Firefox steruje kopiowaniem, NVDA nie będzie wymawiała komunikatu "skopiowano do schowka" w tym trybie. (#15830)
* Podczas kopowania tekstu w Programie Microsoft Word w trybie czytania NVDA, formatowanie jest także brane pod uwagę.
Skutek uboczny tej funkcji jest niemożliwość wymawiania komunikatu  "skopiowano do schowka" przez NVDA podczas naciskania skrótu `control+c` w trybie przeglądu Microsoft Word / Outlook, ponieaż te programy sterują kopiowaniem, nie sama NVDA. (#16129)
* Nowy tryb mowy "na żądanie" został dodany.
Gdy ten tryb mowy jest włączony, NVDA nie mówi automatycznie (na przykład, podczas poruszania się kursorem) ale mówi podczas wciskania skrótów klawiszowych, które mają za cel wimawianie konkretnej informacji (na przykład wymawiaj tytuł okna). (#481, @CyrilleB79)
* Od teraz jest możliwe wykluczenie trybów mowy z listy trybów podczas przełączania za pomocą skrótu `NVDA+s`, w ustawieniach NVDA. (#15806, @lukaszgo1)
  * Jeżeli aktualnie używasz dodatku NoBeepsSpeechMode usuń go i wyłącz tryby "dźwięki" i "na żadanie" w ustawieniach.

### Zmiany

* NVDA więcej nie wspiera wersji systemów operacyjnych Windows 7 i Windows 8.
Windows 8.1 jest minimalną wspieraną wersją. (#15544)
* Aktualizacje komponentów:
  * Zaktualizowano LibLouis braille translator do wersji [3.28.0](https://github.com/liblouis/liblouis/releases/tag/v3.28.0). (#15435, #15876, @codeofdusk)
    * Dodano nowe tablice brajlowskie dla tajskiego, rumuńskiego i filipińskiego.
  * eSpeak NG został zaktualizowany do wersji 1.52-dev commit `530bf0abf`. (#15036)
  * Tłumaczenie symboli i emoji z repozytorium Cldr zostały zaktualizowane do wersji 44.0. (#15712, @OzancanKaratas)
  * Zaktualizowano Java Access Bridge do wersji 17.0.9+8Zulu (17.46.19). (#15744)
* Skróty klawiszowe:
  * Następujące skróty od teraz wspierają dwukrotne i trzykrotne naciśnięcia dla literowania informacji , a także literowania fonetycznego: odczyt zaznaczenia, odczyt tekstu z schowka i odczyt obiektu w fokusie. (#15449, @CyrilleB79)
  * Od teraz polecenie do włączania i wyłączania kurtyny posiada domyślny skrót klawiszowy: `NVDA+control+escape`. (#10560, @CyrilleB79)
  * Gdy jest naciśnięte czterokrotnie, polecenie do odczytu zaznaczenia od teraz pokazuje zaznaczoną treść w trybie czytania. (#15858, @Emil-18)
* Microsoft Office:
  * Podczas odpytywania o formatowanie komórek w programie Excel, ramki i tło będą odczytywane jeżeli istnieje takie formatowanie. (#15560, @CyrilleB79)
  * NVDA już nie będzie odczytywała nieoznaczone grupowania, takie jak w wstążkach Microsoft Office 365. (#15638)
* Opcje "karta dźwiękowa" i "tryb przyciszania" zostały usunięte z okna dialogowego "wybór syntezatora".
Można je teraz znaleźć w panelu ustawień dźwieku, którego można wywołać za pomocą skrótu `NVDA+control+u`. (#15512, @codeofdusk)
* Nazwa opcji "Oczytaj rolę obiektu podczas poruszania się myszą" w ustawieniach myszy NVDA zostala zmieniona na "Odczytaj obiekt podczas wejścia do niego za pomocą myszy".
Ta opcja od teraz odczytuje inne ważne informacje o obiekcie podczas wejścia do niego myszą, takie jak stan, (zaznaczony /wciśnięty) lub współrzędne komórki z tabeli. (#15420, @LeonarddeR)
* Nowe elementy zostały dodane do meni pomoc "szkolenie i wsparcie" i "sklep NV access". (#14631)
* Wsparcie NVDA dla programu  [Poedit](https://poedit.net) zostało przepisane dla wersji 3 i nowszych.
Użytkownicy programu Poedit 1 są zachęcani do aktualizacji do Poedit 3 jeżeli chcą używać ulepszeń dostępnosci dla programu Poedit, takich jak skróty do odczytu notatek dla tłumaczy i komentarzy. (#15313, #7303, @LeonarddeR)
* Przegląd brajla i mowy od teraz są wyłączone w trybie bezpiecznym. (#15680)
* Podczas używania nawigacji obiektowej, wyłączone, niedostępne obiekty od teraz nie będą więcej ignorowane. (#15477, @CyrilleB79)
* Dodano spis treści do wykazu poleceń. (#16106)

### Poprawki błędów

* Add-on Store:
  * Podczas zmiany stanu aktualnie wybranego dodatku, na przykład zmiana z stanu "pobieranie" na "pobrano", odświeżony element będzie oznajmiany poprawnie. (#15859, @LeonarddeR)
  * Podczas instalacji dodatków, instrukcje instalacji nie nakładają się na okno dialogowe ponownego uruchomienia. (#15613, @lukaszgo1)
  * Podczas ponownej instalacji niezgodnego dodatku taki dodatek już nie jest automatycznie wyłączany. (#15584, @lukaszgo1)
  * Wyłączone i niezgodne dodatki teraz mogąbyć aktualizowane. (#15568, #15029)
  * NVDA od teraz odzyskuje swój proces i pokazuje błąd w przypadku nieudanego pobierania dodatku. (#15796)
  * NVDA od teraz już nie uruchamia się ponownie bez powodu po otwarciu i zamknięciu Add-on store. (#16019, @lukaszgo1)
* Dźwięk:
  * NVDA już nie zawiesza się na długi okres czasu gdy więcej dźwięków odtwarza się bardzo szybko. (#15311, #15757, @jcsteh)
  * Jeżeli karta dźwiękowa jest ustawiona na inną niżdomyślnąwartość,  a ta karta stanie sięponownie dostępna,  po czasie niedostępności, NVDA NVDA przełączy się na skonfigurowaną kartę dźwiękową, zamiast przywracania na domyślne urządzenie. (#15759, @jcsteh)
  * NVDA teraz ponownie odtwarza dźwięk jeżeli konfiguracja karty dźwiękowej konfiguracja zmieni sięlub inna aplikacja nie używa tej karty w trybie wyłączności. (#15758, #15775, @jcsteh)
* Brajl:
  * Wielowierszowe monitory brajlowskie już nie spowodują wysypke sterownika BRLTTY. Te monitoryy traktowane są jako jeden nieskończony monitor brajlowski. (#15386)
  * Od teraz wykrywano jest więcej korzystnych obiektów, a ich treść wyświetlana jest w brajlu. (#15605)
  * Wprowadzanie brajla za pomocą skrótów brajlowskich od teraz znowu działa. (#15773, @aaclause)
  * Brajl jest od teraz odświeżany podczas przemieszczania obiektu nawigatora po komórkach tabeli w więcej przypadkach (#15755, @Emil-18)
  * Wynik odczytu poleceń dla aktualnego obiektu nawigatora, pod kursorem przeglądu i aktualnego zaznaczenia pokazywane są w brajlu. (#15844, @Emil-18)
  * Sterownik Albatross już nie rozpoznaje Esp32 mikroukładu jako monitor brajlowski Albatross. (#15671)
* LibreOffice:
  * Słowa skasowane za pomocą skrótu `control+backspace` od teraz są także wymawiane, jeżeli po słowie następuję biała spacja taka jak spacja i tabulator. (#15436, @michaelweghorn)
  * Oznajmianie paska statusu używając skrótu `NVDA+end` od teraz działą w oknach dialogowych LibreOffice od wersji 24.2 and i nowszych. (#15591, @michaelweghorn)
  * od teraz wszystkie właściwości tekstu w LibreOffice od wersji 24.2 i nowszych są wspierane.
  Ta zmiana spowodowała, że od teraz oznajmianie błędów pisowni działa podczas odczytu wiersza w LibreOffice Writerze. (#15648, @michaelweghorn)
  * Oznajmianie nagłówków od teraz działą w LibreOffice wersji 24.2 i nowszych. (#15881, @michaelweghorn)
* Microsoft Office:
  * w Excelu z wyłączonym wsparciem UIA, brajl jest odświeżany, a bieżaca treść komórki zostanie przeczytana po naciśnięciu `control+y`, `control+z` lub `alt+backspace` . (#15547)
  * W Wordzie z wyłączonym  UIA brajl jest odświeżany po naciśnięciu skrótó `control+v`, `control+x`, `control+y`, `control+z`, `alt+backspace`, `backspace` lub `control+backspace`.
  Brajl jest także odświeżany z włączonym UIA, podczas wpisywania tekstu gdy brajl jest ustawiony na przegląd a kursor przeglądu śledzi fokus. (#3276)
  * W Wordzie, początkowe komórki będąwymawiane po naciśnięciu jednej z powyższych poleceń do nawigacji po tabelach `alt+home`, `alt+end`, `alt+pageUp` i `alt+pageDown`. (#15805, @CyrilleB79)
* Odczyt skrótów klawiszowych został ulepszony. (#10807, #15816, @CyrilleB79)
* Syntezator mowy SAPI4 od teraz poprawnie wspiera polecenia zmiany głośnosci , prędkości i wysokości zawarte w mowie. (#15271, @LeonarddeR)
* Stan wielowierszowej kontrolki od teraz jest prawidłowo wymawiany w aplikacjach  używajacych Java Access Bridge. (#14609)
* NVDA potrafi odczytać więcej okien dialogowych w systemie Windows 10 i 11. (#15729, @josephsl)
* NVDA od teraz przeczyta załadowaną stronę w przeglądarce Microsoft Edge podczas używania interfejsu dostępności UI Automation. (#15736)
* Podczas używania polecenia czytaj wszystko oraz poleceń do literowania informacji, pauzy jużnie zmniejszająsię z czasem. (#15739, @jcsteh)
* NVDA już nie zawiesza się w niektóych przypadkach podczas wymawiania dużej ilosci tekstu. (#15752, @jcsteh)
* Podczas używania przeglądarki Microsoft Edge za pomocą interfejsu UI Automation, NVDA od teraz potrafi aktywować więcej kotrolek w trybie czytania. (#14612)
* NVDA od teraz ponownie sięuruchomi gdy konfiguracja zostanie uszkodzona, a konfiguracja zostanie zresetowana, przywracając stan z poprzednich wersji NVDA. (#15690, @CyrilleB79)
* Naprawiono wsparcie dla System List view (`SysListView32`) kontrolek w aplikacjach Windows Forms. (#15283, @LeonarddeR)
* Od teraz już nie jest możliwe nadpisywanie historii NVDA konsssssssoli Python. (#15792, @CyrilleB79)
* NVDA nadal będzie responsywny gdy dostanie dużo zdarzeń  UI automation, na przykład podczas wyświetlania dużej ilości tekstu w konsoli oraz podczas słuchania Whatsappie. (#14888, #15169)
  * To nowe zachowanie można wyłączyć używając nowej opcji "używaj ulepszone przetwarzanie zdarzeń" w zaawansowanych ustawieniach NVDA.
* NVDA od teraz ponownie potrafi śledzić fokus w  aplikachach, uruchomionych wewnątrz Windows Defender Application Guard (WDAG). (#15164)
* Wymówiony tekst już nie jest zaktualizowania podczas poruszania się myszą w przeglądzie mowy. (#15952, @hwf1324)
* NVDA przełączy się ponownie do trybu czytania po zamknięciu list rozwijanych za pomocą `escape` lub `alt+strzałkiWgórę` w Firefoxie lub Chromie. (#15653)
* Poruszanie sięstrzałkami w góręi w dół w iTunes już nie spowoduje niechciane przełączenie do trybu czytania. (#15653)

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

To jest wersja naprawiająca łuki bezpieczeństwa i problem z instalatorem.
Prosimy odpowiedzialnie zgłaszać łuki bezpieczeństwa zgodnie z [Politykąbezpieczeństwa NVDA](https://github.com/nvaccess/nvda/blob/master/security.md).

### Poprawki bezpieczeństwa

* Już nie jest możliwe uruchamianie gdy tryb bezpieczny jest wymuszony.
([GHSA-727q-h8j2-6p45](https://github.com/nvaccess/nvda/security/advisories/GHSA-727q-h8j2-6p45))

### Poprawki błędów

* Naprawiono błąd z niepoprawnym zakończeniem procesu NVDA. (#16123)
* Naprawiono błąd, podczas którego proces programu NVDA mógł niepoprawnie zostać zamknięty, tym samym skutkując w nieodzyskiwalnej instalacji. (#16122)

## 2023.3.3

Jest to wersja naprawiająca łukę bezpieczeństwa.
Prosimy odpowiednio zgłaszać  łuki bezpieczeństwa, śledząc [Politykę bezpieczeństva NVDA](https://github.com/nvaccess/nvda/blob/master/security.md).

### Poprawki bezpieczeństwa

* Od teraz zapobiegany jest zwracany atak XSS zbudowanej treści powodujący arbitrarne uruchamianie kodu.
([GHSA-xg6w-23rw-39r8](https://github.com/nvaccess/nvda/security/advisories/GHSA-xg6w-23rw-39r8))

## 2023.3.2

To jest wersja naprawiająca łukę bezpieczeństwa.
Poprawka bezpieczeństwaw w wersji 2023.3.1 nie została poprawnie wdrożona.
Prosimy odpowiednio zgłaszać  łuki bezpieczeństwa, śledząc [Politykę bezpieczeństva NVDA](https://github.com/nvaccess/nvda/blob/master/security.md).

### Poprawki bezpieczeństwa

* Poprawka bezpieczeństwaw w wersji 2023.3.1 nie została poprawnie wdrożona.
Uniemożliwia uruchamianie dowolnego kodu z podwyższonymi uprawnieniami do nieuwierzytelnionych użytkowników.
([GHSA-h7pp-6jqw-g3pj](https://github.com/nvaccess/nvda/security/advisories/GHSA-h7pp-6jqw-g3pj))

## 2023.3.1

To jest wersja naprawiająca łukę bezpieczeństwa.
Prosimy odpowiednio zgłaszać  łuki bezpieczeństwa, śledząc [Politykę bezpieczeństva NVDA](https://github.com/nvaccess/nvda/blob/master/security.md).

### Poprawki bezpieczenstwa

* Uniemożliwia uruchamianie dowolnego kodu z podwyższonymi uprawnieniami do nieuwierzytelnionych użytkowników.
([GHSA-h7pp-6jqw-g3pj](https://github.com/nvaccess/nvda/security/advisories/GHSA-h7pp-6jqw-g3pj))

## 2023.3

Ta wersja zawiera ulepszenia wydajności, responsywności i stabilności dźwięku.
Dodano opcje do kontrolowania głośności dźwięków NVDA, oraz do ich ujednolicania z głośnością mowy.

NVDA potrafi od czasu do czasu odświeżać tekst rozpoznany za pomocą Ocr, wymawiając go po jego natychmiastowym pojawieniu się.
Tą opcję można włączyć w kategorii Windows OCR w oknie dialogowym ustawień NVDA.

Naprawiono kilka problemów z brajlem, naprawiając jednocześnie wykrywanie ruchów kursora i automatyczne wykrywanie monitorów brajlowskich.
W celu ulepszenia wydajności automatycznego wykrywania monitorów brajlowskich, od teraz istnieje możliwość wyłączania niektórych sterowników z tego procesu.
Dodano także nowe polecenia BRLTTY.

Naprawiono błędy w Add-on Store, pakiecie Microsoft Office, menu kontekstowych Microsoft Edge, i kalkulatorze Windows.

### Nowe funkcje

* Ulepszone zarządzanie dźwiękiem:
  * Nowy panel ustawień dźwięku:
    * Można go otworzyć używając skrótu `NVDA+control+u`. (#15497)
    * Dodano opcje, która umożliwia ustawienie spójności głośności dźwięków NVDA. (#1409)
    * Dodano opcję do oddzielnej konfiguracji głośności dźwięków NVDA. (#1409, #15038)
    * Opcje do wyboru karty dźwiękowej i przełączania przyciszania dźwięku zostały przeniesione do nowej kategorii dźwięk w ustawieniach NVDA z okna dialogowego "wybór syntezatora".
    Te opcje będą usunięte z okna dialogowego "wybór syntezatora" w wersji 2024.1. (#15486, #8711)
  * NVDA od teraz będzie dosyłał dźwięk za pomocą interfejsu Windows Audio Session API (WASAPI), co może wpłynąć na stabilność, responsywność i wydajność mowy i dźwięków NVDA. (#14697, #11169, #11615, #5096, #10185, #11061)
  * Uwaga: WASAPI jest niezgodny z niektórymi dodatkami.
  Zgodne aktualizacje dostępne są dla tych dodatków. Zanim zaktualizujesz NVDA, prosimy zaktualizować te dodatki.
  Niezgodne wersje tych dodatków będą wyłączone podczas aktualizacji NVDA:
    * Tony's Enhancements wersja 1.15 lub starsza. (#15402)
    * NVDA global commands extension 12.0.8 lub starsza. (#15443)
* NVDA od teraz potrafi aktualizować wynik OCR, wymawiając nowy tekst gdy się pojawi. (#2797)
  * Aby włączyć tę funkcję, włącz opcję "Od czasu do czasu odświeżaj  treść rozpoznawaną" w kategorii windows Ocr w ustawieniach NVDA.
  * Kiedy ta opcja jest włączona, możesz regulować wymawianie nowego tekstu za pomocą opcji informuj o zmianach treści dynamicznych  (naciskając `NVDA+5`).
* Podczas używania automatycznego wykrywania monitorów brajlowskich, możliwe jest wykluczenie monitorów brajlowskich z procesu automatycznego wykrywania z poziomu okna dialogowego wybór monitora brajlowskiego. (#15196)
* Nowa opcja została dodana do ustawień formatowania dokumentów: "Ignoruj puste linie podczas odczytu wcięć". (#13394)
* Dodano nieprzydzielone zdarzenie wejścia do poruszania się po kartach właściwości w trybie czytania. (#15046)

### Zmiany

* Brajl:
  * Gdy tekst w terminalu zmieni się bez aktualizacji kursora systemowego, monitor brajlowski zostanie poprawnie odświeżony, gdy znajduje się na tej linii.
  To obejmuje sytuacje, podczas któych brajl jest przywiązany do przeglądu. (#15115)
  * Więcej poleceń BRLTTY dostało zdarzenia wejścia NVDA (#6483):
    * `learn`: włącza i wyłącza pomoc klawiatury
    * `prefmenu`: otwiera NVDA menu
    * `prefload`/`prefsave`: przywracanie i zapisywanie konfiguracji NVDA
    * `time`: pokaż czas
    * `say_line`: Wymawia bieżącą linię pod kursorem przeglądu
    * `say_below`: Czyta wszystko za pomocą kursora przeglądu
  * Sterownik BRLTTY jest dostępny tylko gdy kopia BRLTTY jest uruchomiona z uruchomionym BRLAPI. (#15335)
  * Usunięto ustawienie do wyłączenia wsparcia monitorów brajlowskich HID, zastępując je nową opcją.
  Możesz wyłączyć określone sterowniki monitorów brajlowskich z procesu automatycznego wykrywania z okna dialogowego wybór monitora brajlowskiego. (#15196)
* Add-on Store: zainstalowane dodatki będą pokazane na karcie właściwości zainstalowane, jeżeli są dostępne w Add-on store. (#15374)
* Niektóre skróty klawiszowe w NVDA menu zostały zaktualizowane. (#15364)

### Poprawki błędów

* Microsoft Office:
  * Naprawiono sytuacje, w których Microsoft word zawieszał się  gdy opcje "odczytuj nagłówki" i "odczytuj komentarze i notatki" w opcjach formatowania dokumentów nie były włączone. (#15019)
  * W programach Word i Excel, wyrównanie tekstu będzie poprawnie odczytywane w więcej przypadkach. (#15206, #15220)
  * Naprawiono odczyt niektórych skrótów do formatowania komórek w programie Excel. (#15527)
* Microsoft Edge:
  * NVDA już nie będzie skakała z powrotem do poprzedniej pozycji w trybie czytania podczas otwierania menu kontekstowego w Microsoft Edge. (#15309)
  * NVDA znowu potrafi czytać menu kontekstowe pobierania w przeglądarce Microsoft Edge. (#14916)
* Brajl:
  * Kursory brajlowskie i komórki pokazujące zaznaczenie będą zawsze aktualizowane poprawnie podczas ich włączania lub wyłączania skrótem klawiszowym. (#15115)
  * Naprawiono błąd próby inicjalizacji monitorów brajlowskich Albatross, gdy inny monitor brajlowski jest podłączony. (#15226)
* Add-on Store:
  * Naprawiono błąd, który skutkował pokazywaniem niezgodnych dodatków w Add-on store, nawet gdy opcja"Uwzględnij dodatki niezgodne" była wyłączona. (#15411)
  * Dodatki zablokowane z powodów niezgodności powinne być filtrowane poprawnie podczas przełączania  stanu włączonych lub wyłączonych dodatków. (#15416)
  * Naprawiono błąd, który zapobiegał aktualizacjom nadpisanych lub zamienionych dodatków używając narzędzia do zewnętrznej instalacji. (#15417)
  * Naprawiono błąd, podczas którego NVDA nie mówiła do póki nie będzie ponownie uruchomiona po instalacji dodatków. (#14525)
  * Naprawiono błąd, podczas którego dodatki nie mogły być instalowane jeżeli poprzednie pobieranie zostało anulowane, lub instalacja nie powiodła się. (#15469)
  * Naprawiono błędy zarządzania niezgodnymi dodatkami podczas aktualizacji NVDA. (#15414, #15412, #15437)
* NVDA znowu potrafi czytać wyniki w kalkulatorze w jego 32-bitowej wersji w następujących wydaniach systemu operacyjnego windows:Server, LTSC and LTSB. (#15230)
* NVDA więcej nie ignoruje zmian fokusu gdy okno podrzędne dostaje fokus. (#15432)
* Naprawiono potencjalną wysypkę podczas uruchamiania NVDA. (#15517)

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

W tej wersji została wprowadzona funkcja Add-on store, która zamienia menedżer dodatków.
W Add-on Store można przeglądać, wyszukiwać, instalować dodatki stworzone przez społeczność.
Istnieje możliwość ręcznej zmiany zgodności przestarzałych dodatków na własną odpowiedzialność.

Dodano nowe funkcje dotyczące brajla, włączając w to polecenia i wsparcie monitorów brajlowskich.
Dodano nowe skróty klawiszowe do optycznego rozpoznawania znaków  i do spłaszczonego widoku nawigacji obiektowej.
Ulepszono nawigację i odczyt formatowania w Microsoft Office .

Zostały wdrożone liczne poprawki błędów, ogólnie do wsparcia brajla, pakietu Microsoft Office, przeglądarek internetowych i systemu Windows 11.

eSpeak-NG, LibLouis braille translator i Unicode CLDR zostały zaktualizowane.

### Nowości

* Funkcja Add-on Store została dodana do NVDA. (#13985)
  * Przeglądaj, szukaj, instaluj i aktualizuj dodatki napisane przez społeczność.
  * Ręcznie rozwiąż problemy ze zgodnością przestarzałych dodatków.
  * Menedżer dodatków został zamieniony przez Add-on Store.
  * Po więcej informacji, zajrzyj do odświerzonego podręcznika użytkownika.
* Nowe zdarzenia wejścia:
  * Nieprzydzielone zdarzenie wejścia do przełączania się między dostępnymi językami w Windows OCR. (#13036)
  * Nieprzydzielone zdarzenie wejścia do przełącznia się między trybami pokazywania wiadomości na monitorze brajlowskim. (#14864)
  * Nieprzydzielone zdarzenie wejścia do włączania i wyłączania trybu wyświetlania stanu zaznaczenia na monitorze brajlowskim. (#14948)
  * Dodano domyślne zdarzenie wejścia do przemieszczania się między następnym i poprzednim obiektem w spłaszczonym widoku chierachii obiektów. (#15053)
    * Do komputerów stacjonarnych: `NVDA+numeryczne9` i `NVDA+numeryczny3` do przełączania się między poprzednim i następnym obiektem.
    * do komputerów przenośnych: `shift+NVDA+[` i `shift+NVDA+]` do przełączania się między poprzednim i następnym obiektem.
* Nowe funkcje dotyczące brajla:
  * Dodano wsparcie dla monitora brajlowskiego Help Tech Activator. (#14917)
  * Została dodana nowa opcja do włączania i wyłączania pokazywania stanu zaznaczenia (kropki 7 i 8). (#14948)
  * Dodana nowa opcja do nieobowiązkowego przemieszczania kursora systemu oraz fokusu podczas zmiany kursora przeglądu za pomocą przycisków routing. (#14885, #3166)
  * Informacja jest pokazywana w brajlu podczas trzykrotnego naciskania skrótu klawiszowego`numeryczny2` do odczytu wartości numerycznej znaku pod kursorem przeglądu. (#14826)
  * Dodano wsparcie do atrybutu ARIA 1.3 `aria-brailleroledescription,` który umożliwia autorom nadpisywanie typu elementu wyświetlanego na monitorze brajlowskim. (#14748)
  * Sterownik do linijek brajlowskich firmy Baum: dodano kilka skrótów klawiszowych ze spacją do wykonywania niektórych kombinacji klawiszy takich jak `windows+d` i `alt+tab`.
  Aby zobaczyć pełną listę, przeczytaj podręcznik użytkownika. (#14714)
* Dodano wymowę następujących znaków unicode:
  * znaków brajlowskich, takich jak `⠐⠣⠃⠗⠇⠐⠜`. (#13778)
  * Mac klawisza option `⌥`. (#14682)
* Dodano skróty klawiszowe dla monitorów brajlowskich Tivomatic Caiku Albatross. (#14844, #15002)
  * Do pokazywania ustawień brajlowskich
  * Do odczytu paska stanu
  * Do przełączania kształtu kursora brajlowskiego
  * Do przełączania pokazywania komunikatów na monitorze brajlowskim
  * Do włączania lub wyłączania kursora brajlowskiego
  * Do włączania lub wyłączania pokazywania stanu zaznaczenia
  * Do włączania i wyłączania opcji "Przenoś kursor systemowy podczas przywoływania kursoru przeglądu". (#15122)
* Funkcje Microsoft Office:
  * Gdy opcja podświetlony tekst jest włączona w opcjach formatowania, kolor podświetlenia jest  wymawiany w Microsoft Word. (#7396, #12101, #5866)
  * Gdy włączony jest odczyt kolorów w opcjach formatowania dokumentu, kolory tła są odczytywane w Microsoft Word. (#5866)
  * Podczas używania skrótów w programie Microsoft Excel przeznaczonych do formatowania takich jak pogrubienie, kursywa, podkreślenie i przekreślenie komórki, wynik polecenia jest odczytywany. (#14923)
* Experymentalne zarządzanie dźwiękiem:
  * NVDA potrafi odtwarzać audio za pomocą interfejsu Windows Audio Session API (WASAPI), co może polepszyć responsywność, wydajność i stabilność mowy i dźwięków NVDA . (#14697)
  * Używanie WASAPI można włączyć w ustawieniach zaawansowanych.
  Jeżeli  WASAPI jest włączone, można włączyć następujące dodatkowe ustawienia.
    * Opcję do wyrównywania głośności mowy i dźwięków NVDA. (#1409)
    * Opcję do oddzielnego konfigurowania dźwięków NVDA. (#1409, #15038)
  * Istnieje znany problem periodycznego wysypywania się gdy  Wasapi jest włączony. (#15150)
* W przeglądarkach Mozilla Firefox i Google Chrome, NVDA NVDA odczytuje otwarcie dialogu, siatki, listy lub drzewa przez kontrolkę jeżeli autor to określił używając atrybutu `aria-haspopup`. (#8235)
* Od teraz możliwe jest określenie zmiennej takiej jak `%temp%` lub `%homepath%`) w ścieżkach podczas tworzenia kopii przenośnych NVDA. (#14680)
* W systemie operacyjnym Windows 10 aktualizacji z maja 2019 i nowszych wersjach, NVDA potrafi czytać nazwy pulpitów wirtualnych podczas ich otwierania, zmieniania i zamykania. (#5641)
* Dodano ogólnosystemowy parametr umożliwiający użytkownikom i administratorom systemowym wymuszone uruchamianie NVDA w trybie bezpiecznym. (#10018)

### Zmiany

* Zmiany komponentów:
  * eSpeak NG został zaktualizowany do wersji 1.52-dev commit `ed9a7bcf`. (#15036)
  * Zaktualizowano LibLouis braille translator do wersji [3.26.0](https://github.com/liblouis/liblouis/releases/tag/v3.26.0). (#14970)
  * CLDR został zaktualizowany do wersji 43.0. (#14918)
* Zmiany w LibreOffice:
  * Podczas odczytywania pozycji kursoru przeglądu, aktualna pozycja kursoru systemowego jest teraz odczytywana względem aktualnej strony w programie LibreOffice Writer 7.6 i nowszych wersjach, podobno do zachowania w programie Microsoft Word. (#11696)
  * Odczyt paska stanu (na przykład wyyzwalany przez skrót klawiszowy `NVDA+end`) funkcjonuje w LibreOffice. (#11698)
  * Podczas przemieszczania się do innej komórki w programie LibreOffice Calc, NVDA już nie odczytuje wspólrzędne  komórki w nieprawidłowy sposób gdy odczyt wspólrzędnych w ustawieniach NVDA jest wyłączony. (#15098)
* Zmiany dotyczące brajla:
  * Podczas używania monitora brajlowskiego za pomocą standardowego sterownika brajlowskiego HID, klawisze dpad mogą być używane symulacji strzałek i entera.
  Skróty klawiszowe `spacja+punkt1` i `spacja+punkt4` od teraz są używane do strzałek. (#14713)
  * Aktualizowana treść dynamiczna na stronach internetowych (aria żywe regiony) od teraz jest wyświetlana w brajlu.
  Można to wyłączyć w panelu ustawien zaawansowanych. (#7756)
* Znaki minus i półpauza zawsze będą wysyłane do syntezatora mowy. (#13830)
* Odczyt dystansu w programie Microsoft Word od teraz będzie respektował jednostkę pomiaru zdefiniowaną w ustawieniach zaawansowanych programu Microsoft Word, nawet podczas używania UIA do odczytu dokumentów Microsoft Word. (#14542)
* NVDA reaguje szybciej podczas nawigacji strzałkami w polach edycyjnych. (#14708)
* Skrót do odczytu docelowej lokalizacji linku od teraz odczytuje z pozycji fokusu a nie z obiektu nawigatora. (#14659)
* Tworzenie kopii przenośnej nie wymaga wpisywania  litery dysku jako części ścieżki absolutnej. (#14680)
* Jeżeli system Windows jest ustawiony tak, że sekundy są pokazywane w zegarze znajdującym sie w zasobniku systemowym, podczas używania  `NVDA+f12` do odczytu czasu od teraz sekundy będą odczytywane. (#14742)
* NVDA od teraz odczyta nieoznaczone grupowania zawierające przydatną informację o pozycji, takie jak menu w ostatnich wersjach pakietu Microsoft Office 365. (#14878)

### Poprawki błędów

* Brajl:
  * Pare usprawnień stabilności dla wprowadzania/wyświetlania brajla, które powodują mniejsze wysypywanie się NVDA. (#14627)
  * NVDA już nie będzie przełączała się niepotrzebnie na monitor brajlowski "bez brajla" wiele razy podczas automatycznego wykrywania, co poskutkuje mniejszym dziennikiem i wązkim gardłem informacyjnym. (#14524)
  * NVDA się teraz przełączy do portu USB jeżeli HID Bluetooth urządzenie (takie jak HumanWare Brailliant lub APH Mantis) jest zostanie automatycznie wykryte a połączenie USB stanie się dostępne.
  To działało tylko do portów szeregowych. (#14524)
  * Gdy nie ma podlączonego monitora brajlowskiego a przegląd brajla jest zamknięty za pomocą klawiszy `alt+f4` oraz klikając przycisk zamknij, wielkość monitora brajlowskiego będzie zresetowana do zera. (#15214)
* Przeglądarki internetowe:
  * NVDA już nie powoduje rzadkie wysypywanie się oraz zawieszanie przeglądarki Mozilla Firefox. (#14647)
  * W przeglądarkach Mozilla Firefox i Google Chrome, wpisywane znaki nie są już odczytywane w niektórych polach edycyjnych nawet gdy czytanie pisanycch znaków jest wyłączone. (#8442)
  * Od teraz możliwe jest używanie trybu czytania w wbudowanych kontrolkach Chromium gdzie poprzednio nie było to możliwe. (#13493, #8553)
  * W przeglądarce Mozilla Firefox, przemieszczanie wskaźnika myszy do okoła tekstu spoza linkami od teraz dokładniej wymawia tekst. (#9235)
  * Docelowa lokalizacja linków graficznych od teraz jest wymawiana dokłądniej w więcej przypadkach w  przeglądarkach Chrome i Edge. (#14783)
  * Podczas próby odczytu adresu URL dla linku bez atrybutu a href NVDA nie staje się cicha.
  Zamiast tego, NVDA poda komunikat o braku adresu docelowego. (#14723)
  * W trybie czytania, NVDA już nie będzie ignorowała fokusu podczas próby przeniesienia się do poprzedniej lub następnej kontrolki na przykłąd przemieszczanie się od kontrolki i jej nadrzędnym elemencie listy lub komórki siatki. (#14611)
    * Miewaj jednak na uwadze, że ta poprawka działa gdy opcja "automatycznie ustaw fokus do elementów fokusowalnych " w ustawieniach trybu przeglądu jest wyłączona (co jest opcją domyślna).
* Poprawki błędów dla Windows 11:
  * NVDA potrafi znowu czytać treść paska stanu w programie Notepad. (#14573)
  * Przełączanie między kartami właściwości spowoduje odczyt nazwy nowej karty właściwości w programach Notepad i File Explorer. (#14587, #14388)
  * NVDA ponownie potrafi czytać elementy kandydatów podczas wprowadzania tekstu w językach takich jak chiński i japoński. (#14509)
  * Znowu jest możliwe otwarcie elementów licencja i wspóltworcy w menu NVDA/pomoc. (#14725)
* Poprawki błędów Microsoft Office:
  * Podczas szybkiego przemieszczania się pomiędzy komórkami w programie Microsoft Excel, istnieje mniejsze prawdopodobieństwo że NVDA przeczyta błędne współrzędne komórki. (#14983, #12200, #12108)
  * Podczas pozycjonowania na komórkę w programie Microsoft excel spoza skoroszytu, Brajl i podświetlacz fokusu już nie są bezpotrzebnie aktualizowane do obiektó, który poprzednio był we fokusie. (#15136)
  * NVDA Od teraz prawidłowo będzie wymawiała fokusowane pola haseł w programach Microsoft Excel i Outlook. (#14839)
* Dla symboli które nie posiadają aktualnego opisu w aktualnie użytym języku, będzie używany domyślny poziom symboli. (#14558, #14417)
* Od teraz jest możliwe używanie znaku bekslesz w polu zamiany  wpisu słownikowego, gdy typ nie jest ustawiony na wyrażenie regularne. (#14556)
* W kalkulatorze w systemach operacyjnych Windows 10 i 11, kopia przenośna już niczego nie zrobi oraz odtworzy dźwięk błędu podczas wpisywania wyrażenia matematycznego w w trybie kompaktowym. (#14679)
* NVDA Znowu potrafi odzyskiwać się w więcej sytuacjach takich jak zawieszające się programy, które spowodowały kompletne zawieszenie NVDA. (#14759) 
* Podczas wymuszania wsparcia UIA z niektórymi wierszami poleceń, naprawiono błąd powodujący zawieszenie się NVDA i przepełnienie pliku dziennika. (#14689)
* NVDA już nie odmówi zapisywania konfiguracji po resetowaniu konfiguracji. (#13187)
* Podczas uruchamiania tymczasowej wersji z instalatora, NVDA już nie oszuka użytkownika faktem, że można zzapisać konfigurację. (#14914)
* NVDA reaguje troszeczkę szybciej na polecenia i zmiany fokusu. (#14928)
* Pokazywanie ustawień Ocr od teraz jest możliwe  w systemach, gdzie to nie było możliwe. (#15017)
* Naprawiono bląd związany z zapisywaniem i przywracaniem konfiguracji NVDA, włączając to przełączanie między syntezatorami mowy. (#14760)
* Naprawiono błąd gestu przeglądu tekstu "pociągnięcie do góry" który powodował, że wykonywanie gestu powodowało poruszanie się po stronach, zamiast po liniach. (#15127)

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

Dodano nową opcję do kategorii "nawigacja po dokumencie", "styl akapitu".
Ta opcja może być używana w edytorach tekstu, niewspierających nawigację po akapitach natywnie, na przykład Notepad i Notepad plus plus.

Dodano polecenie globalne do odczytu docelowej lokalizacji linku, `NVDA+k`.

Ulepszone wsparcie dla adnotowanej treści webowej (takiej jak komentarze i przypisy końcowe).
Naciśnij `NVDA+d` aby przemieszczać się po streszczeniach gdy adnotacje są odczytywane (na przykład: "ma komentarz, ma przypis końcowy").

Monitory brajlowskie Tivomatic Caiku Albatross 46/80 są od teraz wspierane.

Ulepszono wsparcie dla architektur ARM64 i AMD64 wersji systemu operacyjnego Windows.

Naprawiono liczne błędy, zwłaszcza w systemie operacyjnym Windows 11.

eSpeak, LibLouis, Sonic rate boost i Unicode CLDR zostały zaktualizowane.
Dodano nowe tablice brajlowskie dla języków:  gruzińskiego, Swahili (Kenia) i Cziczewa (Malawi).

Uwaga:

* W tej wersji istniejące wersje dodatków są niezgodne.

### Nowe funkcje

* Microsoft Excel z UI Automation: Automatyczny odczyt nagłówków kolumn i wierszy w tabelach. (#14228)
  * Uwaga: dotyczy to tabel formatowanych za pomocą  przycisku "tabela" na karcie właściwości wstaw wstążki.
  Opcje "pierwsza kolumna" i "nagłówek wiersza" w "opcjach stylu tabeli" równoznaczne są z nagłówkami kolumn i wierszy.
  * Nie odnosi się to do nagłówków specyficznych dla czytnika ekranu, które używają nazwanych  rozpiętości.
* Dodano nieprzydzielone zdarzenie wejścia do włączania i wyłączania opisów znaków po ruchu kursora. (#14267)
* Dodano eksperymentalną opcję do używania wsparcia powiadomie UIA w programie Windows terminal w celu odczytu nowego oraz zmienionego tekstu w konsoli, skutkując lepszą stabilnością i wydajnością. (#13781)
  * O ograniczeniach tej opcji można przeczytać w podręczniku użytkownika.
* W systemie Windows 11 ARM64, tryb czytania od teraz jest dostępny w aplikacjach AMD64 takich jak Firefox, Google Chrome i 1Password. (#14397)
* Dodano nową opcję, "styl akapitu" w kategorii "nawigacja po dokumentach".
To dodaje wsparcie dla nawigacji po akapitach w stylach pojedyńczej nowej linii (normalnej) i wieloliniowej przerwy (blokowej).
Ta opcja może być używana z edytorami tekstu, które nie wspierają  natywną nawigację po akapitach, takimi jak Notepad i Notepad++. (#13797)
* Istnienie wielu adnotacji teraz jest odczytywane.
`nvda+d` od teraz przełącza pomiędzy odczytu streszczenia każdego celu adnotacji dla więcej źródeł celnych.
Na przykład, gdy tekst zawiera komentarz i przypis końcowy związany z nim. (#14507, #14480)
* Dodano wsparcie dla monitorów brajlowskich Tivomatic Caiku Albatross 46/80. (#13045)
* Nowe polecenie globalne: odczytaj docelową lokalizacje linku (`NVDA+k`).
Gdy skrót jest naciśnięty jeden raz lokalizacja linku w obiekcie nawigatora będzie pokazana na monitorze brajlowskim i wymówiona.
Gdy skrót jest naciśnięty dwukrotnie, docelowa lokalizacja będzie pokazana w oknie w celu dokładniejszego odczytu. (#14583)
* Dodano nowe nieprzydzielone polecenie (kategoria narzędzia): pokaż lokalizację linku w oknie.
To polecenie jest równoważne dwukrotnym naciśnięciem skrótu `NVDA+k` ale z tą różnicą, że może być bardziej użyteczne dla użytkowników monitorów brajlowskich. (#14583)

### Zmiany

* Zaktualizowano LibLouis tłumacz brajla do [wersji 3.24.0](https://github.com/liblouis/liblouis/releases/tag/v3.24.0). (#14436)
  * Drastycznie zaktualizowano tablice brajlowskie dla węgierskiego, ujednoliconego angielskiego brajla, i chińskiego bopomofo.
  * Wsparcie dla nowego duńskiego standartu brajla wydanego w 2022 roku.
  * Nowe tablice brajlowskie dla gruzińskiego brajla literackiego, Swahili (Kenia) i Chichewa (Malawi).
* Zaktualizowano bibliotekę do przyśpieszania mowy Sonic  do wersji commit `1d70513`. (#14180)
* Baza znaków unicode CLDR została zaktualizowana do wersji 42.0. (#14273)
* eSpeak NG zostałzaktualizowany do wersji 1.52-dev commit `f520fecb`. (#14281, #14675)
  * Naprawiono odczyt wielkich liczb. (#14241)
* Aplikacje java z kontrolkami używającymi  stanu zaznaczenia od teraz będą zgłaszały stan elementu niezaznaczony zamiast stanu zaznaczonego. (#14336)

### Poprawki błędów

* Poprawki Windows 11:
  * NVDA od teraz odczyta podpowiedzi wyszukiwania podczas otwierania menu start. (#13841)
  * Na architekturze ARM, aplikacje x64 już nie są identyfikowane jako aplikacje ARM64. (#14403)
  * Elementy menu historii schowka , takie jak ""przypnij element" od teraz są osiągalne. (#14508)
  * W systemie Windows 11 22H2 i nowszych wersjach, od teraz znowu możliwa jest interakcja za pomocą myszy i klawiatury z elementami takie jak obszar powiadomień dodatkowych i okno dialogowe "otwórz za pomocą". (#14538, #14539)
* Od teraz dostępne są podpowiedzi podczas wpisywania @wzmianek w komentarzach Microsoft Excel. (#13764)
* Na pasku adresu Google Chrome, kontrolki podpowiedzi takie jak (przełącz do karty, usuń podpowiedź itd.) od teraz są odczytywane po zaznaczeniu. (#13522)
* Podczas dostarczania informacji o formatowaniu, kolory są ściśle odczytywane w programach Wordpad i podglądzie logu, co jest lepsze niż odczyt "kolor domyślny". (#13959)
* W przeglądarce Firefox, aktywowanie przycisku "Show options" na stronach problemów Github od teraz działa niezawodnie. (#14269)
* Kontrolki wyboru daty w oknie dialogowym zaawansowanego wyszukiwania programu Outlook 2016 / 365 od teraz są odczytywane z właściwymi oznakami i wartościami. (#12726)
* Kontrolki ARIA przełączników od teraz są rozpoznawane jako przełączniki w przeglądarkach Firefox, Chrome i Edge, co jest dokładniejsze w porównaniu z odczytem tych kontrolek jako pola wyboru. (#11310)
* NVDA od teraz automatycznie przeczyta stan sortowania w nagłówku kolumny tabeli HTML po zmianie naciskając przycisk wewnętrzny. (#10890)
* Nazwa regionu oraz punktu orientacyjnego jest automatycznie wymawiana podczas przeskakiwania wewnątrz regionu z zewnątrz używając klawiszy szybkiej nawigacji . (#13307)
* Gdy opcje Odtwarzaj dźwięk, oraz lub wymawiaj 'duże' przed dużymi literami są włączone w kombinacji z opisami po nazwie liter, NVDA więcej nie odtworzy sygnał dźwiękowy lub odczyta 'duże' dwukrotnie. (#14239)
* Od teraz kontrolki tabel w aplikacjach Java będą odczytywane precyzyjniej przez NVDA. (#14347)
* Od teraz niektóre ustawienia już nie będą inne podczas używania więcej profili. (#14170)
  * Następujące ustawienia zostały naprawione:
    * Wcięcie linii w ustawieniach formatowania.
    * Obramowania komórek w ustawieniach formatowania
    * Pokazywanie wiadomości w ustawieniach brajla
    * Przywiązanie brajla w ustawieniach brajla
  * W niektórych rzadkich przypadkach, te ustawienia, gdy używane są w profilach mogą być nieoczekiwanie zmodyfikowane gdy ta wersja NVDA zostanie zainstalowana.
  * Prosimy sprawdzić te ustawienia w profilach po zaktualizowaniu NVDA do tej wersji.
* Znaki emoji będą odczytywane w coraz więcej języków. (#14433)
* Istnienie adnotacji od teraz jest pokazywane także w brajlu dla niektórych elementów. (#13815)
* Naprawiono błąd który spowodował nie zapisywanie zmian w poprawny sposób, gdy zmieniamy opcje "domyślną" i wartość opcji "domyślnej". (#14133)
* Podczas konfiguracji NVDA zawsze będzie zdefiniowany jeden klawisz modyfikatora NVDA. (#14527)
* Podczas otwierania  menu NVDA używając obszaru powiadomień, NVDA już nie pokaże nieistniejącej oczekującej aktualizacji. (#14523)
* W Foobarze 2000, Pozostały, upłyneły i całkowity czas jest od teraz odczytywany prawidłowo w przypadku plików audio trwających ponad jeden dzień. (#14127)
* W przeglądarkach, takich jak Chrome i Firefox, alerty o pobieraniu pliku będą także wyświetlane na monitorze brajlowskim. Dotyczy to także innych alertów aria. (#14562)
* Naprawiono błąd niemożliwej nawigacji pomiędzy pierwszej i ostatniej  kolumny w tabelach w przeglądarce Firefox (#14554)
* Gdy NVDA jest uruchomiony z parametrem `--lang=Windows`, otwieranie ustawień ogólnych jest znowu możliwe. (#14407)
* NVDA już nie przestaje czytać w programie Kindle for PC po przewracaniu strony. (#14390)

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

To wydanie w sobie zawiera kilka nowych skrótów klawiszowych, włączając w to skróty do czytania całych tabel.
Do podręcznika użytkownika został dodany roździał "szybki start".
Naprawiono także niektóre błędy.

Liblouis i Espeak-ng zostały zaktualizowane.
Dodano nowe tablice brajlowskie dla chińskiego, szwedzkiego, języka luganda i języka Kinyarwanda.

### Nowe funkcje

* Dodano rozdział "szybki start" do podręcznika użytkownika. (#13934)
* Dodano nowy skrót klawiszowy do sprawdzania skrótu klawiszowego bieżącego obiektu pod fokusem. (#13960)
  * Skrót dla komputerów stacjonarnych: `shift+numeryczny2`.
  * Skrót dla komputerów przenośnych: `NVDA+ctrl+shift+.`.
* Dodano nowe skróty do przemieszczania kursoru przeglądu po stronie gdzie jest to wspierane przez program. (#14021)
  * Przechodzi do poprzedniej strony:
    * Skrót dla komputerów stacjonarnych: `NVDA+pageUp`.
    * Skrót dla komputerów przenośnych: `NVDA+shift+pageUp`.
  * Przechodzi do następnej strony:
    * Skrót dla komputerów stacjonarnych: `NVDA+pageDown`.
    * Skrót dla komputerów przenośnych: `NVDA+shift+pageDown`.
* Dodano następujące skróty klawiszowe do tabel. (#14070)
  * Czytaj wszystko w kolumnie: `NVDA+control+alt+strzałka w dół`
  * Czytaj wszystko w wierszu: `NVDA+control+alt+strzałka w prawo`
  * Czytaj całą kolumnę: `NVDA+control+alt+strzałka w górę`
  * Czytaj cały wiersz: `NVDA+control+alt+Strzałka w lewo`
* W Microsoft Excel który jest używany za pomocą interfejsu Ui Automation, NVDA od teraz ogłasza przemieszczenie spoza tabelą arkusza kalkulacyjnego. (#14165)
* Czytanie nagłówków tabeli od teraz może być oddzielnie konfigurowane dla kolumn i wierszy. (#14075)

### Zmiany

* eSpeak NG został zaktualizowany do wersji 1.52-dev commit `735ecdb8`. (#14060, #14079, #14118, #14203)
  * Naprawiono czytanie znaków alfabetu łacińskiego podczas używania języka mandaryńskiego. (#12952, #13572, #14197)
* Zaktualizowany LibLouis tłumacz znaków brajlowskich do wersji [3.23.0](https://github.com/liblouis/liblouis/releases/tag/v3.23.0). (#14112)
  * Dodano następujące tablice brajlowskie:
    * Chiński ogólny alfabet Braille'a (uproszczone chińskie znaki)
    * Kinyarwanda brajl literacki
    * Luganda brajl literacki
    * Szwedzkie pismo podstawowe
    * Szwedzkie pismo pełne
    * Szwedzkie skróty
    * Chiński (Chiny, mandaryński) aktualny standard brajlowski (bez tonów) (#14138)
* NVDA od teraz włącza do statystyki użytkowania architekturę systemu operacyjnego. (#14019)

### Poprawki błędów

* Podczas aktualizowania NVDA przy użyciu menedżeru pakietów systemu Windows z poziomu wiersza poleceń, czyli winget, stabilna wersja NVDA więcej nie jest zawsze traktowana jako nowsza niż jakakolwiek wersja Alpha zainstalowana w systemie. (#12469)
* NVDA od teraz poprawnie odczytuje grupowania w aplikacjach Java. (#13962)
* Kursor od teraz sprawnie śledzi wymawiany tekst podczas ciągłego czytania w aplikacjach takich jak Bookworm, WordPad, lub NVDA podglądu loga. (#13420, #9179)
* W programach używających UI Automation, połowicznei zaznaczone pola wyboru od teraz będą zgłaszane poprawnie. (#13975)
* Ulepszona wydajność i stabilność w programach: Microsoft Visual Studio, Windows Terminal, a także innych programach używających interfejsu UI automation. (#11077, #11209)
  * Te poprawki błędów stosowane są do wersji Windows 11 Sun Valley 2 (versja 22H2) i nowszych.
  * Rejestracja selektywna dla zmian właściwości i zdarzeń UIA od teraz jest domyślnie włączona.
* Odczytywanie tekstu, wyjście brajla, a także nieodczytywanie haseł od teraz działają poprawnie w zagnieżdżonej kontrolce Windows terminal w programie Visual Studio 2022. (#14194)
* NVDA od teraz jest DPI świadomy podczas używania więcej niż jednego monitora.
Wdrożono kilka poprawek dla używania ustawienia DPI wyższego niż 100% oraz używania więcej monitorów.
Mogą jeszcze pojawiać się problemy w wersjach systemu operacyjnego Windows starszych niż Windows 10 1809.
Aby te poprawki działały, aplikacje z którymi NVDA współpracuje także powinne być DPI świadome.
Trzeba mieć na uwadzę, że nadal istnieją problemy z przeglądarkami Chrome i Edge. (#13254)
  * Ramki podświetlenia wizualnego od teraz powinny się poprawnie umieszczać w większości aplikacji. (#13370, #3875, #12070)
  * Współpraca z ekranami dotykowymi od teraz powina być dokładniejsza dla większości programów. (#7083)
  * Śledzenie myszy od teraz powinno być dokładniejsze dla większości programów. (#6722)
* Zmiany stanu orientacji (pionowa/pozioma) od teraz są poprawnie ignorowane gdy nie ma żadnych zmian (na przykład, zmiany monitora). (#14035)
* NVDA od teraz będzie oznajmiał przeciąganie elementów na ekranie w miejscach, takich jak przemieszczanie kafelek w Menu start w systemie operacyjnym Windows 10 i pulpitów wirtualnych w systemie Windows 11. (#12271, #14081)
* W ustawieniach zaawansowanych, opcja "Odtwarzaj dźwięk do zapisanych błędów" jest teraz prawidłowo resetowana do domyślnej wartości po naciśnięciu przycisku "Przywróć do ustawień domyślnych". (#14149)
* NVDA od teraz może zaznaczać tekst używając skrótu `NVDA+f10` w aplikacjach Java. (#14163)
* NVDA od teraz nie będzie się zawieszac w menu podczas poruszania się strzałkami w górę i w dół w konwersachach wątkowanych w programie  Microsoft Teams. (#14355)

### Changes for Developers

Please refer to [the developer guide](https://www.nvaccess.org/files/nvda/documentation/developerGuide.html#API) for information on NVDA's API deprecation and removal process.

* The [NVDA API Announcement mailing list](https://groups.google.com/a/nvaccess.org/g/nvda-api/about) was created. (#13999)
* NVDA no longer processes `textChange` events for most UI Automation applications due to their extreme negative performance impact. (#11002, #14067)

#### Deprecations

* `core.post_windowMessageReceipt` is deprecated, use `winAPI.messageWindow.pre_handleWindowMessage` instead.
* `winKernel.SYSTEM_POWER_STATUS` is deprecated and usage is discouraged, this has been moved to `winAPI._powerTracking.SystemPowerStatus`.
* `winUser.SM_*` constants are deprecated, use `winAPI.winUser.constants.SystemMetrics` instead.

## 2022.3.3

Jest to pomniejsze wydanie naprawiające problemy wersji 2022.3.2, 2022.3.1 i 2022.3.
To wydanie także naprawia błędy bezpieczeństwa.

### Poprawki bezpieczeństwa

* Zapobiega niechcianemu dostępowi dla nieautoryzowanych użytkowników do np. konsoli python.
([GHSA-fpwc-2gxx-j9v7](https://github.com/nvaccess/nvda/security/advisories/GHSA-fpwc-2gxx-j9v7))

### Poprawki błędów

* Naprawiono błąd podczas zamrażania NVDA na ekranie blokady, przy którym NVDA umożliwi dostęp do pulpitu użytkownika z poziomu ekranu blokady. (#14416)
* Naprawiono błąd podczas którego NVDA się NVDA zawiesza podczas logowania i NVDA się zachowa niepoprawnie, tak jak by użądzenie było jeszcze zablokowane. (#14416)
* Naprawiono błędy dostępności z Windows doświadczeniami "zapomniałem numer Pin" i instalacji Windows Update. (#14368)
* Naprawiono błąd podczas próby instalacji NVDA w niektórych środowiskach Windows, Np. Windows Server. (#14379)

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

Jest to pomniejsze wydanie naprawiające regresje z wersji 2022.3.1 i naprawiające incydenty bezpieczeństwa.

### Poprawki bezpieczeństwa

* Zapobiega możliwemu dostępowi na poziomie systemowym dla użytkowników nieuwierzytelnionych.
([GHSA-3jj9-295f-h69w](https://github.com/nvaccess/nvda/security/advisories/GHSA-3jj9-295f-h69w))

### Poprawki błędów

* Naprawiono regresję z wersji NVDA 2022.3.1 w której większość wyłączono na bezpiecznych ekranach. (#14286)
* Naprawiono regresję z wersji NVDA 2022.3.1 w której większość funkcjonalności było wyłączone po zalogowaniu, jeżeli NVDA została uruchomiona na ekranie blokady. (#14301)

## 2022.3.1

Jest to pomniejsze wydanie naprawiające kilka incydentów bezpieczeństwa.
Prosimy o odpowiednie zgłoszenie incydentów bezpieczeństwa na adres <info@nvaccess.org>.

### Poprawki bezpieczeństwa

* Naprawiono eksploit za pomocą którego można było podnieść uprawnienia z użytkownika do systemu.
([GHSA-q7c2-pgqm-vvw5](https://github.com/nvaccess/nvda/security/advisories/GHSA-q7c2-pgqm-vvw5))
* Naprawiono incydent bezpieczeństwa umożliwiający dostępu do konsoli Pythona na ekranie logowania poprzez hazard uruchomienia NVDA.
([GHSA-72mj-mqhj-qh4w](https://github.com/nvaccess/nvda/security/advisories/GHSA-72mj-mqhj-qh4w))
* Naprawiono problem w którym tekst przeglądu mowy był przechowywany w pamięci poczas blokowania systemu operacyjnego.
([GHSA-grvr-j2h8-3qm4](https://github.com/nvaccess/nvda/security/advisories/GHSA-grvr-j2h8-3qm4))

### Poprawki błędów

* Od teraz zapobiegane jest zmienianie ustawień  przeglądu brajla i mowy na ekranie blokady przez nieuprawnionego użytkownika. ([GHSA-grvr-j2h8-3qm4](https://github.com/nvaccess/nvda/security/advisories/GHSA-grvr-j2h8-3qm4))

## 2022.3

Znaczna część tej wersji została opracowana przez społeczność programistów NVDA.
Zawiera ona opisy liter po ich nazwach  oraz poprawione wsparcie dla konsoli systemu operacyjnego Windows.

Dodano również kilka poprawek błędów.
Najistotniejsza poprawka błędów dla najnowszych wersji programów Adobe Acrobat/Reader zapobiega niespodziewanemu zamykaniu się programu z raportem o błędzie podczas wyświetlania dokumentu PDF.

Do najnowszej wersji syntezatora mowy eSpeak dodano 3 nowe języki: białoruski, luksemburski i Totontepec Mixe.

### Nowe funkcje

* W Hoście konsoli używanym przez wiersz poleceń, PowerShell oraz podsystem Linux dla systemu Windows 11 w wersji 22H2 (Sun Valley 2) i nowszych:
  * znacząco poprawiono wydajność i stabilność. (#10964)
  * Po naciśnięciu `control+f`, aby znaleźć tekst, pozycja kursora recenzji jest aktualizowana zgodnie ze znalezionym terminem. (#11172)
  * Raportowanie wpisanego tekstu, który nie pojawia się na ekranie (np. hasła), jest domyślnie wyłączone.
Można go ponownie włączyć w panelu ustawień zaawansowanych NVDA. (#11554)
  * Tekst, który został przewinięty poza ekranem, można przeglądać bez przewijania okna konsoli.. (#12669)
  * Dostępne są bardziej szczegółowe informacje o formatowaniu tekstu ([microsoft/terminal PR 10336](https://github.com/microsoft/terminal/pull/10336))
* Dodano nową opcję Mowy, aby czytać opisy znaków po literowaniu. (#13509)
* Dodano nową opcję alfabetu Braille'a, aby określić, czy przewijanie wyświetlacza do przodu/do tyłu powinno przerywać mowę. (#2124)

### Zmiany

* eSpeak NG został zaktualizowany do wersji 1.52-dev commit `9de65fcb`. (#13295)
  * Dodane języki:
    * Białoruski
    * Luksemburgski
    * Totontepec Mixe
* Używając Uia w celu uzyskania dostępu do kontrolek arkusza kalkulacyjnego programu Microsoft Excel, NVDA może teraz raportować, kiedy komórka jest scalona. (#12843)
* Zamiast zgłaszania "ma szczegóły" cel szczegółów jest zawarty tam, gdzie to możliwe, na przykład "ma komentarz". (#13649)
* Rozmiar instalacji NVDA jest teraz wyświetlany w sekcji Programy i funkcje systemu Windows. (#13909)-

### Poprawki błędów

* Adobe Acrobat / Reader 64 bit nie będzie już ulegać awarii podczas czytania dokumentu PDF. (#12920)
  * Należy pamiętać, że najbardziej aktualna wersja programu Adobe Acrobat / Reader jest również wymagana, aby uniknąć awarii.
* Pomiary rozmiaru czcionki są od teraz przetłumaczone w NVDA. (#13573)
* Ignorowane są zdarzenia Java Access Bridge, w których nie można znaleźć uchwytu okna dla aplikacji Java.
Poprawi to wydajność niektórych aplikacji Java, w tym IntelliJ IDEA. (#13039)
* Ogłaszanie wybranych komórek dla programu LibreOffice Calc jest bardziej wydajne i nie powoduje już zamrożenia programu Calc po zaznaczeniu wielu komórek. (#13232)
* Podczas uruchamiania pod innym użytkownikiem Microsoft Edge nie jest już niedostępny. (#13032)
* Gdy zwiększenie szybkości jest wyłączone, prędkość eSpeak nie spada już między wartościami prędkości 99% a 100%. (#13876)
* Naprawiono błąd, który pozwalał na otwarcie 2 dialogów gestów wejściowych. (#13854)

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

Jest to wydanie łatka, naprawiające problem bezpieczeństwa.

### Poprawki błędów

* Naprawiono eksploit za pomocą którego było możliwe wejście do konzoli pythona z poziomu podglądu logów na zablokowanym ekranie.
([GHSA-585m-rpvv-93qg](https://github.com/nvaccess/nvda/security/advisories/GHSA-585m-rpvv-93qg))

## 2022.2.3

Jest to wersja naprawiająca niechcianą niezgodność w API wprowadzoną w wersji 2022.2.1.

### Poprawki błędów

* Naprawiono błąd w którym NVDA nie zgłaszał "bezpieczny pulpit" podczas wejścia do bezpiedcznego pulpitu.
To skutkowało, że NVDA remote nie rozpoznawał bezpiecznych pulpitów. (#14094)

## 2022.2.2

Jest to wersja naprawiająca błąd w wersji 2022.2.1 dotyczący zdarzeń wejścia.

### Poprawki błędów

* Naprawiono błąd, w którym zdarzenia wejścia nie działały zawsze. (#14065)

## 2022.2.1

Jest to pomniejsza wersja naprawiająca problemy bezpieczeństwa.
Prosimy odpowiedzialnie zgłaszać problemy z bezpieczeństwem na adresie <info@nvaccess.org>.

### Poprawki bezpieczeństwa

* Naprawiono eksploit za pomocą którego było możliwe uruchomienie konzoli pythona z zablokowanego ekranu. (GHSA-rmq3-vvhq-gp32)
* Naprawiono eksploit za pomocą którego było możliwe wyjście z ekranu blokowania używając nawigacji obiektowej. (GHSA-rmq3-vvhq-gp32)

### Changes for Developers

#### Deprecations

These deprecations are currently not scheduled for removal.
The deprecated aliases will remain until further notice.
Please test the new API and provide feedback.
For add-on authors, please open a GitHub issue if these changes stop the API from meeting your needs.

* `appModules.lockapp.LockAppObject` should be replaced with `NVDAObjects.lockscreen.LockScreenObject`. (GHSA-rmq3-vvhq-gp32)
* `appModules.lockapp.AppModule.SAFE_SCRIPTS` should be replaced with `utils.security.getSafeScripts()`. (GHSA-rmq3-vvhq-gp32)

## 2022.2

To wydanie zawiera wiele poprawek błędów.
Warto zauważyć, że wprowadzono znaczące ulepszenia dla aplikacji opartych na Javie, monitorów brajlowskich i funkcji systemu Windows.

Wprowadzono nowe polecenia nawigacji po tabeli.
Unicode CLDR został zaktualizowany.
LibLouis został zaktualizowany. Zawiera on nową niemiecką tablicę brajlowską.

### Nowe funkcje

* Obsługa interakcji ze składnikami Microsoft Loop w produktach Microsoft Office. (#13617)
* Dodano nowe polecenia nawigacji po tabeli. (#957)
 * `control+alt+home/end`, aby przejść do pierwszej/ostatniej kolumny.
 * `control+alt+pageUp/pageDown`, aby przejść do pierwszego/ostatniego wiersza.
* Dodano nieprzypisany skrypt do przełączania między trybami przełączania języka i dialektu. (#10253)-

### Zmiany

* NSIS został zaktualizowany do wersji 3.08. (#9134)
* CLDR został zaktualizowany do wersji 41.0. (#13582)
* Zaktualizowano translator alfabetu Braille'a LibLouis do [3.22.0](https://github.com/liblouis/liblouis/releases/tag/v3.22.0). (#13775)
  * Nowa tablica brajlowska: niemiecki skróty (dwukierunkowe)
* Dodano nową rolę dla kontrolek "wskaźnika zajętości". (#10644)
* NVDA ogłasza teraz, kiedy nie można wykonać akcji NVDA. (#13500)
  * Obejmuje to, przypadki gdy:
    * używamy wersję NVDA ze Sklepu Windows.
    * używamy NVDA w bezpiecznym kontekście.
    * oczekujemy na odpowiedź w modalnym oknie dialogowym.

### Poprawki błędów

* Poprawki dla aplikacji opartych na Javie:
  * NVDA ogłosi teraz stan tylko do odczytu. (#13692)
  * NVDA będzie teraz poprawnie ogłaszać stan wyłączony/włączony. (#10993)
  * NVDA od teraz będzie  czytać skróty funkcyjne. (#13643)
  * NVDA może teraz emitować sygnał dźwiękowy lub mówić na paskach postępu. (#13594)
  * NVDA nie będzie już niepoprawnie usuwać tekstu z widżetów podczas prezentacji dla użytkownika. (#13102)
  * NVDA będzie czytać stan przełączników. (#9728)
  * NVDA zidentyfikuje teraz okno w aplikacji Java z wieloma oknami. (#9184)
  * NVDA będzie teraz czytać informacje o pozycji dla kontrolek kart właściwosci. (#13744)
* Poprawki Braille'a:
  * Naprawiono wyjście brajla podczas nawigacji po pewnym tekście w kontrolkach edycji w aplikacjach mozilla, takich jak sporządzanie wiadomości w Thunderbirdzie. (#12542)
  * Gdy alfabet Braillea jest automatycznie powiązany, a mysz jest poruszana z włączonym śledzeniem myszy,
   Polecenia przeglądania tekstu aktualizują teraz monitor brajlowski zawartoscią mówioną. (#11519)
  * Możliwe jest teraz przesuwanie wyświetlacza brajlowskiego po treści za pomocą poleceń przeglądania tekstu. (#8682)
* Instalator NVDA może teraz uruchamiać się z katalogów ze znakami specjalnymi. (#13270)
* W Firefoksie NVDA nie zgłasza już elementów na stronach internetowych, gdy atrybuty aria-rowindex, aria-colindex, aria-rowcount lub aria-colcount są nieprawidłowe. (#13405)
* Kursor nie przełącza już wiersza ani kolumny podczas korzystania z nawigacji po tabeli do nawigacji po scalonych komórkach. (#7278)
* Podczas czytania nieinteraktywnych plików PDF w programie Adobe Reader typ i stan pól formularza (takich jak pola wyboru i przyciski opcji) są teraz raportowane. (#13285)
* "Resetuj konfigurację do ustawień fabrycznych" jest teraz dostępny w menu NVDA w trybie bezpiecznym. (#13547)
* Wszelkie zablokowane przyciski myszy zostaną odblokowane po wyjściu z NVDA, wcześniej przyciski myszy pozostawały zablokowany. (#13410)
* Program Visual Studio zgłasza teraz numery wierszy. (#13604)
  * Zauważ, że aby raportowanie numerów wierszy działało, pokazywanie numerów wierszy musi być włączone w Visual Studio i NVDA.
* Program Visual Studio teraz poprawnie zgłasza wcięcia linii. (#13574)
* NVDA po raz kolejny ogłosi szczegóły wyników wyszukiwania w menu Start w ostatnich wydaniach Windows 10 i 11. (#13544)
* W Windows 10 i 11 Calculator w wersji 10.1908 i nowszych,
NVDA ogłosi wyniki po naciśnięciu większej liczby poleceń, takich jak polecenia z trybu naukowego. (#13383)
* W systemie Windows 11 ponownie można nawigować i wchodzić w interakcje z elementami interfejsu użytkownika,
takich jak Pasek zadań i Widok zadań za pomocą myszy i interakcji dotykowej. (#13506)
* NVDA ogłosi zawartość paska stanu w Notatniku Windows 11. (#13688)
* Podświetlanie obiektów Navigator pojawia się natychmiast po aktywacji funkcji. (#13641)
* Naprawiono czytanie elementów widoku listy jednokolumnowej. (#13659, #13735)
* Naprawiono automatyczne przełączanie języka eSpeak na angielski i francuski z powrotem na brytyjski angielski i francuski (Francja). (#13727)
* Naprawiono automatyczne przełączanie języka OneCore podczas próby przejścia na wcześniej zainstalowany język. (#13732)

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

To wydanie zawiera główne ulepszenia obsługi UIA w MS Office.
W przypadku pakietu Microsoft Office 16.0.15000 lub nowszego w systemie Windows 11 NVDA domyślnie używa automatyzacji interfejsu użytkownika do uzyskiwania dostępu do dokumentów programu Microsoft Word.
Zapewnia to znaczną poprawę wydajności w porównaniu ze starym dostępem do modelu obiektów.

Wprowadzono ulepszenia sterowników monitorów brajlowskich, w tym Seika Notetaker, Papenmeier i HID Braille. 
Istnieją również różne poprawki błędów systemu Windows 11 dla aplikacji takich jak Kalkulator, Konsola, Terminal, Poczta i Panel Emoji.

eSpeak-NG i LibLouis zostały zaktualizowane, dodając nowe tabele japońskie, niemieckie i katalońskie.

Uwaga:

 * To wydanie przerywa kompatybilność z istniejącymi dodatkami. -

### Nowości

* Obsługa notatek raportowania w MS Excel z włączoną UIA w systemie Windows 11. (#12861)
* W ostatnich kompilacjach programu Microsoft Word za pośrednictwem UIA w systemie Windows 11 istnienie zakładek, komentarzy roboczych i rozwiązanych komentarzy jest teraz zgłaszane zarówno w mowie, jak i alfabecie Braille'a. (#12861)
* Nowy parametr wiersza poleceń `--lang` umożliwia zastąpienie skonfigurowanego języka NVDA. (#10044)
* NVDA ostrzega teraz o parametrach wiersza poleceń, które są nieznane i nie są używane przez żadne dodatki. (#12795)
* W programie Microsoft Word dostępnym za pośrednictwem automatyzacji interfejsu użytkownika, NVDA będzie teraz korzystać z mathPlayer do czytania i poruszania się po równaniach matematycznych pakietu Office. (#12946)
  * Aby to zadziałało, musisz mieć uruchomiony program Microsoft Word 365/2016 kompilacja 14326 lub nowszy. 
  * Równania MathType muszą być również ręcznie konwertowane na Office Math, wybierając każde z nich, otwierając menu kontekstowe, wybierając Opcje równań, Konwertuj na Office Math.
* Raportowanie "ma szczegóły" i powiązane polecenie podsumowujące relację szczegółów zostały zaktualizowane do pracy w trybie fokusu. (#13106)
* Seika Notetaker może być teraz automatycznie wykrywany po podłączeniu przez USB i Bluetooth. (#13191, #13142)
  * Dotyczy to następujących urządzeń: MiniSeika (16, 24 komórek), V6 i V6Pro (40 komórek)
  * Ręczne wybieranie portu COM Bluetooth jest teraz również obsługiwane.
* Dodano polecenie przełączania przeglądu brajla; nie ma domyślnie skojarzonego gestu. (#13258)
* Dodano polecenia do przełączania wielu modyfikatorów jednocześnie z wyświetlaczem Braille'a (#13152)
* Okno dialogowe Słownik mowy zawiera teraz przycisk "Usuń wszystko", aby pomóc wyczyścić cały słownik. (#11802)
* Dodano obsługę Kalkulatora Windows 11. (#13212)
* W programie Microsoft Word z włączonym UIA w systemie Windows 11 NVDA teraz czyta numery wierszy i numery sekcji. (#13283, #13515)
* W przypadku pakietu Microsoft Office 16.0.15000 i nowszych wersji w systemie Windows 11 NVDA domyślnie UIA użytkownika do uzyskiwania dostępu do dokumentów Microsoft Word, zapewniając znaczną poprawę wydajności w porównaniu ze starym dostępem do modelu obiektowego. (#13437)
 * Obejmuje to dokumenty w samym programie Microsoft Word, a także czytnik i kompozytor wiadomości w programie Microsoft Outlook. 

### Zmiany

* Espeak-ng został zaktualizowany do 1.51-dev commit `7e5457f91e10`. (#12950)
* Zaktualizowano liblouis Braille translator do [3.21.0](https://github.com/liblouis/liblouis/releases/tag/v3.21.0). (#13141, #13438)
  * Dodano nową tablicę brajlowską: japoński (Kantenji) brajl literacki.
  * Dodano nową niemiecką sześciopunktową komputerową tablicę brajlowską.
  * Dodano katalońską tablicę brajlowską pismo pełne. (#13408)
* - NVDA zgłosi wybór i scalone komórki w LibreOffice Calc 7.3 i nowszych. (#9310, #6897)
* Zaktualizowano repozytorium danych regionalnych Unicode Common Locale Data Repository (CLDR) do wersji 40.0. (#12999)
* `NVDA+Numpad Delete` domyślnie zgłasza lokalizację karetki lub obiektu skupionego. (#13060)
* `NVDA+Shift+Numpad Delete` zgłasza lokalizację kursora recenzji. (#13060)
* Dodano domyślne powiązania do przełączania klawiszy modyfikatorów do wyświetlaczy Freedom Scientific (#13152)
* "Baseline" nie jest już zgłaszany za pomocą polecenia formatowania tekstu raportu (`NVDA+f`). (#11815)
* Aktywuj długi opis nie ma już przypisanego domyślnego gestu. (#13380)
* Podsumowanie szczegółów raportu ma teraz domyślny gest (`NVDA+d`). (#13380)
* NVDA musi zostać ponownie uruchomiony po zainstalowaniu MathPlayer. (#13486)-

### Poprawki błędów

* Okienko menedżera schowka nie powinno już niepoprawnie brać fokusu podczas otwierania niektórych programów pakietu Office. (#12736)
* W systemie, w którym użytkownik zdecydował się zamienić główny przycisk myszy z lewej na prawą, NVDA nie będzie już przypadkowo wyświetlać menu kontekstowego zamiast aktywować element w aplikacjach takich jak przeglądarki internetowe. (#12642)
* Podczas przesuwania kursora recenzji poza koniec kontrolek tekstowych, takich jak Microsoft Word z UIA, "dół" jest poprawnie zgłaszany w większej liczbie sytuacji. (#12808)
* NVDA może zgłaszać nazwę i wersję aplikacji dla plików binarnych umieszczonych w system32 podczas pracy w 64-bitowej wersji systemu Windows. (#12943)
* Poprawiono spójność odczytu wyjściowego w wiersza poleceń. (#12974)
  * Zauważ, że w niektórych sytuacjach, podczas wstawiania lub usuwania znaków w środku linii, znaki po kursorze mogą być ponownie odczytywane.
* MS word z UIA: nagłówek quick nav w trybie przeglądania nie utknie już na końcowym nagłówku dokumentu, ani ten nagłówek nie jest wyświetlany dwukrotnie na liście elementów NVDA. (#9540)
* W systemie Windows 8 i nowszych pasek stanu Eksploratora plików można teraz przeczytać za pomocą standardowego gestu NVDA + end (pulpit) / NVDA + shift + end (laptop). (#12845)
* Wiadomości przychodzące na czacie programu Skype dla firm są ponownie czytane. (#9295)
* NVDA może ponownie przyciszać dźwięk podczas korzystania z syntezatora SAPI5 w systemie Windows 11. (#12913)
* W kalkulatorze Windows 10 NVDA ogłosi etykiety dla elementów historii i listy pamięci. (#11858)
* Gesty, takie jak przewijanie i routing, ponownie działają z urządzeniami Braille'a HID. (#13228)
* Poczta systemu Windows 11: Po przełączeniu ostrości między aplikacjami, podczas czytania długiej wiadomości e-mail, NVDA nie utknie już w linii wiadomości e-mail. (#13050)
* HID Braille: gesty akordowe (np. `spacja+kropka4`) mogą być z powodzeniem wykonywane z wyświetlacza Braille'a. (#13326)
* Rozwiązano problem polegający na tym, że w tym samym czasie mogło być otwieranych wiele okien dialogowych ustawień. (#12818)
* Rozwiązano problem polegający na tym, że niektóre monitory Braille'a Focus Blue przestawały działać po wybudzeniu komputera ze stanu uśpienia. (#9830)
* "Baseline" nie jest już fałszywie zgłaszany, gdy aktywna jest opcja "zgłoś indeks górny i dolny". (#11078)
* W systemie Windows 11 NVDA nie będzie już uniemożliwiać nawigacji w panelu emoji podczas wybierania emotikonów. (#13104)
* Zapobiega występowaniu błędu powodującego podwójne raportowanie podczas korzystania z konsoli i terminala systemu Windows. (#13261)
* Naprawiono kilka przypadków, w których nie można było czytać elementów listy w aplikacjach 64-bitowych, takich jak REAPER. (#8175)
* W menedżerze pobierania Microsoft Edge NVDA automatycznie przełączy się w tryb koncentracji uwagi, gdy element listy z najnowszym pobraniem zyska fokus. (#13221)
* NVDA nie powoduje już awarii 64-bitowych wersji Notepad ++ 8.3 i nowszych. (#13311)
* Program Adobe Reader nie ulega już awarii podczas uruchamiania, jeśli włączony jest tryb chroniony programu Adobe Reader. (#11568)
* Naprawiono błąd, który powodował, że wybranie sterownika Papenmeier Braille Display Driver powodowało awarię NVDA. (#13348)
* W programie Microsoft Word z UIA: numer strony i inne formatowanie nie jest już niewłaściwie ogłaszane podczas przechodzenia z pustej komórki tabeli do komórki z zawartością lub z końca dokumentu do istniejącej zawartości. (#13458, #13459)
* NVDA nie będzie już nie zgłaszać tytułu strony i zacznie automatycznie czytać, gdy strona załaduje się w Google Chrome 100. (#13571)
* NVDA nie ulega już awarii podczas resetowania konfiguracji NVDA do ustawień fabrycznych, gdy poleceń Speak są włączone. (#13634)-

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

Jest to niewielka wersja mająca na celu rozwiązanie problemu z zabezpieczeniami.
Prosimy o odpowiedzialne ujawnianie <info@nvaccess.org> problemów związanych z bezpieczeństwem.

### Poprawki bezpieczeństwa

— Rozwiązano problem z poradnikiem bezpieczeństwa GHSA-xc5m-v23f-pgr7.

  * Okno dialogowe wymowy symbolu jest teraz wyłączone w trybie bezpiecznym.

## 2021.3.4

Jest to niewielka wersja mająca na celu naprawienie kilku zgłoszonych problemów z bezpieczeństwem.
Prosimy o odpowiedzialne ujawnianie <info@nvaccess.org> problemów związanych z bezpieczeństwem.

### Poprawki bezpieczeństwa

— Rozwiązano problem z poradnikiem bezpieczeństwa GHSA-354r-wr4v-cx28. (#13488)

  * Usuń możliwość uruchamiania NVDA z włączonym rejestrowaniem debugowania, gdy NVDA działa w trybie bezpiecznym.
  * Usuń możliwość aktualizacji NVDA, gdy NVDA działa w trybie bezpiecznym.

* Rozwiązano problem z poradnikiem bezpieczeństwa GHSA-wg65-7r23-h6p9. (#13489)

  * Usuń możliwość otwierania okna dialogowego gestów wejściowych w trybie bezpiecznym.
  * Usuń możliwość otwierania domyślnych, tymczasowych i głosowych okien dialogowych słownika w trybie bezpiecznym.

* Rozwiązano problem z poradnikiem bezpieczeństwa GHSA-mvc8-5rv9-w3hx. (#13487)
  * wx narzędzie do inspekcij okien jest od teraz wyłączone w trybie bezpiecznym.

## 2021.3.3

Ta wersja jest identyczna z 2021.3.2.
Błąd istniał w NVDA 2021.3.2, gdzie błędnie identyfikował się jako 2021.3.1.
To wydanie poprawnie identyfikuje się jako 2021.3.3.

## 2021.3.2

Jest to niewielka wersja mająca na celu naprawienie kilku zgłoszonych problemów z bezpieczeństwem.
Prosimy o odpowiedzialne ujawnianie <info@nvaccess.org> problemów związanych z bezpieczeństwem.

### Poprawki błędów

* Poprawka zabezpieczeń: Zapobiegaj nawigacji po obiektach poza ekranem blokady w systemach Windows 10 i Windows 11. (#13328)
* Poprawka zabezpieczeń: Okno dialogowe menedżera dodatków jest teraz wyłączone na bezpiecznych ekranach. (#13059)
* Poprawka zabezpieczeń: Pomoc kontekstowa NVDA nie jest już dostępna na bezpiecznych ekranach. (#13353)

## 2021.3.1

Jest to niewielka wersja mająca na celu naprawienie kilku problemów w 2021.3.

### Zmiany

* Nowy protokół brajlowski HID nie jest już preferowany, gdy można użyć innego sterownika monitora brajlowskiego. (#13153)
* Nowy protokół Braille'a HID można wyłączyć poprzez ustawienie w panelu ustawień zaawansowanych. (#13180)


## 2021.3

 To wydanie wprowadza wsparcie dla nowej specyfikacji brajlowskiej HID.
Celem tej specyfikacji jest zapewnienie uniwersalnego standardu wsparcia wszystkich monitorów brajlowskich bez konieczności instalowania dodatkowych sterowników.
Zaktualizowano też eSpeak-NG i LibLouis. Dodane zostały m.in. nowa tablica dla rosyjskiego i języka Tshivenda.
Do ustawień zaawansowanych dodano opcję, która pozwala włączyć Dźwięki błędu również w wersjach stabilnych NVDA.
Opcja "Czytaj wszystko" w programie Microsoft Word od teraz przewija widok tak, aby aktualna pozycja kursora zawsze była widoczna.
Dodano liczne ulepszenia dotyczące interakcji z pakietem Microsoft Office  przy użyciu UIA.
Na przykład, dzięki jednej z poprawek UIA, Outlook ignoruje więcej typów tabel układu treści w wiadomościach.

Ważne uwagi:

Po aktualizacji naszego certyfikatu bezpieczeństwa, u niektórych użytkowników pojawia się błąd gdy NVDA 2021.2 sprawdza swoje aktualizacje.
Od teraz NVDA automatycznie uzyskuje od systemu Windows aktualizacje certyfikatów bezpieczeństwa, co zapobiegnie pojawianiu się tego błędu w przyszłości.
Użytkownicy, u których występuje ten problem, powinni pobrać ręcznie aktualizacje certyfikatów.

### Nowe funkcje

* Dodano zdarzenie wejścia dla przełączania ustawień ogłaszania stylu obramowań komórki. (#10408)
* Wsparcie dla nowej specyfikacji brajlowskiej HID, którego celem jest zapewnienie uniwersalnego standardu wsparcia monitorów brajlowskich. (#12523)
  * Monitory brajlowskie, które wspierają tę specyfikację, będą automatycznie wykrywane przez NVDA.
  * Szczegóły techniczne dotyczące wprowadzenia specyfikacji HID do NVDA, są dostępne tutaj. https://github.com/nvaccess/nvda/blob/master/devDocs/hidBrailleTechnicalNotes.md
* Dodano wsparcie dla monitora brajlowskiego VisioBraille Vario 4. (#12607)
* Powiadomienia o błędach można włączyć w każdej wersji NVDA z poziomu ustawień zaawansowanych. (#12672)
* W systemie Windows 10 i nowszych, NVDA będzie ogłaszać ilość podpowiedzi wyszukiwania podczas wpisywania szukanych fraz w aplikacjach, takich jak Ustawienia lub Microsoft Store. (#7330, #12758, #12790)
* Od teraz wspierane jest nawigowanie po tabelach dla kontrolek tabeli utworzonych za pomocą Out-GridView cmdlet w PowerShell. (#12928)

### Zmiany

* Espeak-ng został zaktualizowany do wersji 1.51-dev commit `74068b91bcd578bd7030a7a6cde2085114b79b44`. (#12665)
* Gdy w systemie nie ma zainstalowanego wsparcia dla Głosów Mobilnych Windows w preferowanym języku, NVDA automatycznie wybierze eSpeak. (#10451)
* Jeżeli Głosy Mobilne Windows w dalszym ciągu nie działają, należy z powrotem przełączyć syntezator na Espeak. (#11544)
* Podczas odczytywania paska stanu poleceniem `NVDA+end`, punkt przeglądu nie jest już przenoszony do miejsca, gdzie znajduje się ten pasek.
Aby nadal móc przenosić punkt przeglądu do pasków stanu, należy przypisać polecenie do odpowiedniego skryptu w Zdarzeniach Wejścia, w kategorii Nawigacja Obiektowa. (#8600)
* Przy próbie dwókrotnego otwarcia tego samego dialogu, NVDA ustawia kursor na już otwartym dialogu, zamiast wyświetlać błąd. (#5383)
* Zaktualizowano Liblouis do wersji [3.19.0](https://github.com/liblouis/liblouis/releases/tag/v3.19.0). (#12810)
  * Nowe tablice brajlowskie: Rosyjski skróty, Tshivenda pismo pełne, Tshivenda skróty
* Komunikaty "zaznaczone" lub "mrkd" i "podkreślone" lub "hlght" będą ogłaszane zarówno brajlem, jak i mową. (#12892)
* NVDA nie będzie się już wyłączać, gdy pewne dialogi czekają na reakcję użytkownika (np. Potwierdź/Anuluj). (#12984)

### Poprawki błędów

* Śledzenie klawiszy modyfikatorów, takich jak Control lub Insert, jest bardziej wydajne gdy rdzeń wznawia pracę. (#12609)
* Znów możliwe jest sprawdzanie aktualizacji NVDA na niektórych systemach, takich jak czyste wersje instalacyjne Windows. (#12729)
* NVDA poprawnie ogłasza puste komórki tabeli w programie Microsoft Word przy włączonym wsparciu UI automation. (#11043)
* W tabeli ARIA, klawisz Escape zostanie przekierowany do tabeli i nie wyłączy już trybu czytania niezależnie od kontekstu. (#12413)
* Naprawiono błąd, przez który w przeglądarce Google Chrome, nazwa komórki będącej nagłówkiem kolumny w tabeli była ogłaszana dwókrotnie. (#10840)
* NVDA nie wymawia więcej wartość numeryczną suwaków UIA które mają zdefiniowaną tekstualną wartość. (UIA ValuePattern jest od teraz preferowany nad RangeValuePattern). (#12724)
* NVDA nie traktuje więcej wartość suwaków UIA jako oparte na procentowych wartościach.
* Wymawianie lokalizacji komórek w programie Microsoft Excel używane za pomocą UI Automation ponownie działą poprawnie w Windows 11. (#12782)
* NVDA więcej nie ustawia nieprawidłowego języka pythona. (#12753)
* Jeżeli wyłączony dodatek został usunięty a potem ponownie zainstalowany ten sam dodatek będzie ponownie włączony. (#12792)
* Naprawiono błędy dotyczące usuwania oraz instalacji dodatków w przypadkach, gdy foldery dodatków zostały usunięte lub pliko zostało otwarte. (#12792, #12629)
* Używając UI Automation dla dostępu do tabel Microsoft Excel, NVDA więcej nie ogłasza wielokrotnie stan zaznaczania komórek. (#12530)
* Od teraz więcej tekstu będzie odczytywane w LibreOffice Writer, na przykłąd, w oknach dialogowych potwierdzenia. (#11687)
* czytanie / nawigacja za pomocą trybu czytania w programie Microsoft Word za pomocą UI automation od teraz zapewnia poprawne przewijanie dokumentu co wpływa na widoczność aktualnej pozycji w dokumencie, co także wpływa na poprawną synchronizacje widocznej pozycji w trybie czytania i trybie edycji. (#9611)
* Przy odczytywaniu całego dokumentu w programie Microsoft Word uzywając UI automation, dokument jest automatycznie przewijany, a pozycja kursoru aktualizowana. (#9611)
* Przy odczytywaniu wiadomości e-mail w Outlooku a NVDA ma dostęp do kontrolki wiadomości za pomocą UI Automation, większość tabel od teraz jest oznaczona jako tabele wyglądu, co oznacza, że nie będą oczytywane domyślnie. (#11430)
* Naprawiono rzadki błąd przy zmianie urządzeń audio. (#12620)
* Wprowadzanie za pomocą tablic brajlowskich pisma pełnego będzie poprawne. (#12667)
* Przy nawigacji po kalendarzu w obszarze powiadomień, NVDA od teraz wymawia pełną nazwę dnia w tygodniu. (#12757)
* Przy używaniu metod wprowadzania dla języka chińskiego, takich jak Taiwan - Microsoft Quick w programie Microsoft Word, przewijanie w tył i w przód nie powoduje powrót do oryginalnej lokalizacji kursora. (#12855)
* Używając  Microsoft Word za pomocą UIA, nawigacja po zdaniach (alt+strzałka w dół / alt+strzałka w górę) jest pownie możliwa. (#9254)
* Uzywając MS Word za pomocą UIA, od teraz są wymawiane wcięcia akapitów (#12899)
* Używając MS Word za pomocą  UIA, polecenie do śledzenia zmian i niektóre inne lokalizowane polecenia od teraz są wymawiane w programie Word . (#12904)
* Naprawiony błąd przy podwójnym pokazywaniem w brajlu oraz wymawianiem  'opisu gdy opis zgadza sie z  'treścią' lub 'nazwą'. (#12888)
* W MS Word z włączonym wsparciem UIA, od teraz oznajmianie błędów jest bardziej prawidłowe. (#12161)
* W Windowsie 11, NVDA już nie będzie wymawiała "okno" podczas naciskania klawiszy Alt+Tab podczzas przełączania okien. (#12648)
* Nowoczesna strona komentarzy jest od teraz wspierana w programie MS Word gdy dokument nie jest używany za pomocą UIA. Naciśnij alt+f12 aby się przemieszczac pomiędzy stroną komentarzy i dokumencie. (#12982)

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

W tej wersji wprowadzono wstępne wsparcie dla systemu Windows 11.
W związku z tym, że system Windows 11 nie został jeszcze oficjalnie wydany, ta wersja NVDA została przetestowana na wersjach z niejawnego programu testów systemu Windows 11.
Ta wersja zawiera ważną poprawkę dla Kurtyny (Patrz ważne uwagi).
Narzędzie naprawy błędów rejestracji COM od teraz potrafi rozwiązać więcej problemów podczas uruchamiania NVDA.
Zaktualizowano syntezator mowy eSpeak i translator brajla LibLouis.
Naprawiono również liczne błędy i ulepszono m.in. wsparcie brajla, wiersze poleceń systemu Windows, kalkulator, panel emoji oraz historię schowka.

### Ważne uwagi

Z powodu zmiany w API Lupy Systemu Windows, należało zaktualizować Kurtynę, aby wspierała najnowsze wersje systemu Windows.
Użyj NVDA 2021.2 aby włączyć Kurtynę w systemie Windows 10 21H2 (10.0.19044) lub nowszych.
To wydanie zawiera wersje niejawnego programu testów systemu Windows 10 i Windows 11.
Jeśli używasz nowej wersji systemu Windows, dla bezpieczeństwa upewnij się, że przy włączonej Kurtynie ekran jest zupełnie czarny.

### Nowe funkcje

* Eksperymentalne wsparcie dla adnotacji ARIA:
  * Dodaje polecenie służące do odczytu podsumowania szczegółów obiektu z aria-details. (#12364)
  * Dodaje do ustawień zaawansowanych opcję ogłaszania, czy obiekt posiada szczegóły w trybie przeglądu. (#12439) 
* W systemie Windows 10 w Wersji 1909 i nowszych (włącznie z systemem Windows 11), NVDA będzie ogłaszać liczbę sugestii podczas wyszukiwania w Eksploratorze Plików. (#10341, #12628)
* W programie Microsoft Word od teraz NVDA ogłasza wynik wcięcia i skróty wysunięcia gdy zostaną naciśnięte. (#6269)

### Zmiany

* Espeak-ng został zaktualizowany do wersji 1.51-dev commit `ab11439b18238b7a08b965d1d5a6ef31cbb05cbb`. (#12449, #12202, #12280, #12568)
* Jeśli włączona została opcja "artykuły" w ustawieniach użytkownika dotyczących formatowania dokumentów, NVDA ogłasza "artykuł" po odczytaniu treści. (#11103)
* Zaktualizowano liblouis braille translator do wersji [3.18.0](https://github.com/liblouis/liblouis/releases/tag/v3.18.0). (#12526)
  * Nowe tablice brajlowskie: Bułgarski pismo pełne, Birmański pismo pełne, Birmański skróty, Kazachski pismo pełne, Khmerski pismo pełne, Północnokurdyjski pismo podstawowe, Północny Sotho pismo pełne, Północny Sotho skróty, Południowy Sotho pismo pełne, Południowy Sotho skróty, Setswana pismo pełne, Setswana skróty, Tatarski pismo pełne, Wietnamski pismo podstawowe, Wietnamski skróty, Południowy wietnamski pismo pełne, Xhosa pismo pełne, Xhosa skróty, Jakucki pismo pełne, Zulu pismo pełne, Zulu skróty
* Windows 10 OCR zmienił nazwę na Windows OCR. (#12690)

### Poprawki błędów

* W Kalkulatorze systemu Windows 10 NVDA będzie wyświetlać wyrażenia kalkulatora na monitorze brajlowskim. (#12268)
* Podczas wprowadzania lub usuwania znaków ze środka linii w programach konsolowych, znaki po prawej stronie kursora systemowego nie będą już czytane w systemie Windows 10 od wersji 1607 i nowszych. (#3200)
  * Diff Match Patch jest od teraz domyślnie włączony. (#12485)
* Wprowadzanie brajla działa prawidłowo z następującymi tablicami skrótów: Arabski skróty, Hiszpański skróty, Urdu skróty, Chiński (Chiny, Mandaryński) bez tonów. (#12541)
* Narzędzie naprawy błędów rejestracji COM od teraz rozwiązuje więcej problemów, zwłaszcza w 64 bitowym systemie Windows. (#12560)
* Poprawa zarządzania przyciskami dla monitorów brajlowskich Seika Notetaker braille device firmy Nippon Telesoft. (#12598)
* Poprawa ogłaszania panelu emoji i historii schowka w systemie Windows. (#11485)
* Zaktualizowano opisy znaków alfabetu bengalskiego. (#12502)
* NVDA zamyka się bezpiecznie podczas uruchamiania nowego procesu. (#12605)
* Ponowne wybranie sterownika monitora brajlowskiego Handy Tech z dialogu "Wybór monitora brajlowskiego" nie powoduje już błędów. (#12618)
* System Windows w wersji 10.0.22000 lub nowszych jest rozpoznawany jako Windows 11, a nie Windows 10. (#12626)
* Wsparcie Kurtyny zostało naprawione i przetestowane dla systemu Windows w wersjach do 10.0.22000. (#12684)
* Jeśli podczas filtrowania zdarzeń wejścia nie wyświetlają się żadne wyniki, ustawienia zdarzeń wejścia nadal działają tak jak powinny. (#12673)
* Naprawiono błąd, przez który pierwszy element w menu rozwijanym nie jest ogłaszany w niektórych kontekstach. (#12624)

### Changes for Developers

* `characterProcessing.SYMLVL_*` constants should be replaced using their equivalent `SymbolLevel.*` before 2022.1. (#11856, #12636)
* `controlTypes` has been split up into various submodules, symbols marked for deprecation must be replaced before 2022.1. (#12510)
  * `ROLE_*` and `STATE_*` constants should be replaced to their equivalent `Role.*` and `State.*`.
  * `roleLabels`, `stateLabels` and `negativeStateLabels` have been deprecated, usages such as `roleLabels[ROLE_*]` should be replaced to their equivalent `Role.*.displayString` or `State.*.negativeDisplayString`.
  * `processPositiveStates` and `processNegativeStates` have been deprecated for removal.
* On Windows 10 Version 1511 and later (including Insider Preview builds), the current Windows feature update release name is obtained from Windows Registry. (#12509)
* Deprecated: `winVersion.WIN10_RELEASE_NAME_TO_BUILDS` will be removed in 2022.1, there is no direct replacement. (#12544)

## 2021.1

To wydanie zawiera opcjonalne, eksperymentalne wsparcie interfejsu UIA w programie Microsoft Excel i przeglądarkach opartych na silniku Chromium.
Wprowadzono poprawki dla kilku języków. Od teraz możliwy jest też dostęp do linków za pomocą monitora brajlowskiego.
Zaktualizowano symbole matematyczne, Unicode CLDR i LibLouis.
Poprawiono też liczne błędy i dodano ulepszenia dla programów takich jak Microsoft Office lub Visual Studio, a także dla kilku języków.

Uwaga!

 * Od tego wydania obecnie używane dodatki tracą zgodność z NVDA.
 * Kończy się też wsparcie technologii Adobe Flash.

### Nowości

* Wstępne wsparcie interfejsu UIA w przeglądarkach opartych na silniku Chromium, takich jak Microsoft Edge. (#12025)
* Opcjonalne, eksperymentalne wsparcie programu Microsoft Excel poprzez interfejs UI Automation. Zalecane tylko dla programu Microsoft Excel w kompilacji 16.0.13522.10000 lub nowszej. (#12210)
* Łatwiejsza nawigacja po treści wyniku w konsoli Pythona NVDA. (#9784)
  * Alt+strzałka w górę/w dół przechodzi do poprzedniego/następnego wyniku. Dodaj shift, aby rozpocząć zaznaczanie.
  * Control+l czyści pole wyników.
* Od teraz NVDA ogłasza kategorie przypisane do zdarzenia w kalendarzu programu Microsoft Outlook, jeśli jakieś są. (#11598)
* Wsparcie dla monitora brajlowskiego Seika Notetaker firmy Nippon Telesoft. (#11514)

### Zmiany

* W trybie przeglądu, kontrolki można od teraz aktywować za pomocą przycisków routingu na opisie danej kontrolki, np. "ln" dla linku. Jest to szczególnie przydatne do aktywowania np. niezaetykietowanych pól wyboru. (#7447)
* NVDA zapobiega używaniu Windows 10 OCR gdy włączona jest kurtyna. (#11911)
* Zaktualizowano bazę danych Emoji (CLDR) do wersji 39.0. (#11943, #12314)
* Dodano więcej symboli matematycznych do słownika symboli. (#11467)
* Odświeżono wygląd podręcznika użytkownika, listy zmian oraz wykazu poleceń klawiszowych. (#12027)
* NVDA ogłasza "Niewspierane" przy próbie przełączenia układu ekranu w aplikacjach, które nie wspierają tej funkcji, np. w programie Microsoft Word. (#7297)
* Opcja 'Próba anulowania mowy dla wygasłych zdarzeń' w panelu ustawień zaawansowanych jest od teraz domyślnie włączona. (#10885)
  * Można wyłączyć to zachowanie ustawiając tę opcję na "Nie".
  * Aplikacje webowe, takie jak Gmail, nie odczytują już nieaktualnych informacji podczas szybkiego przemieszczania kursora.
* Zaktualizowano liblouis braille translator do wersji [3.17.0](https://github.com/liblouis/liblouis/releases/tag/v3.17.0). (#12137)
  * Nowe tablice brajlowskie: Białoruski brajl literacki, Białoruski brajl komputerowy, Urdu pismo pełne, Urdu skróty.
* Wsparcie treści Adobe Flash zostało usunięte z NVDA w związku z porzuceniem tej technologii przez Adobe. (#11131)
* Od teraz NVDA zamyka się nawet gdy okna czytnika ekranu są nadal otwarte. Proces zamykania programu obejmuje wszystkie okna dialogowe NVDA. (#1740)
* Podgląd mowy można zamknąć skrótem `alt+F4`. Ponad to posiada on standardowy przycisk zamykania, aby łatwiej było go zamknąć przy użyciu urządzeń wskazujących. (#12330)
* Przegląd brajla posiada standardowy przycisk zamykania, aby łatwiej było go zamknąć przy użyciu urządzeń wskazujących. (#12328)
* W liście elementów, skrót klawiszowy do przycisku "aktywuj" został usunięty dla niektórych języków aby zapobiec konflikty z przyciskiem opcji filtruj według. When available, the button is still the default of the dialog and as such can still be invoked by simply pressing enter from the elements list itself. (#6167)

### Poprawki błędów

* Lista wiadomości w programie Outlook 2010 jest ponownie czytana. (#12241)
* W programach terminalowych w  Windows 10 wersji 1607 i nowszych, przy wstawianiu oraz usuwaniu znaków w środku linii, znaki z prawa od kursa już nie są czytane. (#3200)
  * Ta eksperymentalna poprawka musi być włączona ręcznie w panelu NVDA ustawień zaawansowanych zmieniając śledzenie zmian konsoli  na Diff Match Patch.
* W MS Outlooku, niechciana odczytywanie dystansu przy naciśnięciu klawiszy shift+tab nie powinno mieć miejsca. (#10254)
* W konsoli Python, wstawianie tabulatora w celu zrobienia wcięcia na początku wypełnionej tekstem linii i wywoływania autouzupełniania w środku linii od teraz jest wspierane. (#11532)
* Informacje o formatowaniu i inne wiadomości w trybue przeglądania nie pokazują pustych linii gdy włączony jest przegląd ekranu. (#12004)
* Od teraz jest możliwe odczytywanie komentarzy w programie MS Word z włączonym interfejsem UIA. (#9285)
* Wydajność przy interakcji z Visual Studio została ulepszona. (#12171)
* Naprawione błędy graficzne takie jak brakujące elementy przy użyciu NVDA w wyglądu z prawo na lewo. (#8859)
* Respektowany jest wygląd okien zależnie od języka . (#638)
  * Znany problem dla języków pisanych z prawa na lewo: prawa granica grupowań rozmywa sie z kontrolkami. (#12181)
* Język Pythona jest ustawiony żeby był zgodny z językiem oznaczonym w ustawieniach, co też jest zastosowane w języku domyślnym. (#12214)
* TextInfo.getTextInChunks już się nie zawiesza na kontrolach wzbotgaconego tekstu takich jak NVDA przegląd logu. (#11613)
* Znowu jest możliwe używanie NVDA w językach zawierających podkreślniki w swoim kodzie Np. de_CH W windowsie 10 1803 i 1809. (#12250)
* W WordPadzie, konfiguracja czytania indeksów gornych oraz dolnych działą jak powinna. (#12262)
* NVDA już  ogłąsza nową treść na stronach internetowych jeżeli stary fokus znika, a na jego miejscu pojawia się nowy. (#12147)
* Przekreślanie, indeks górny i indeks dolny są teraz ogłaszane w Microsoft Excelu jeżeli odpowiednia opcja została włączona. (#12264)
* Naprawiono kopiowanie konfiguracji podczas instalacji kopii przenośnej kiedy domyślny folder konfiguracji jest pusty. (#12071, #12205)
* naprawiono błędne oznajmianie liter z akcentami lub diakrytyków przy włączonej opcji'mów duże przy dużych literach'. (#11948)
* Naprawiono błąd zmiany wysokości w syntezatorach SAPI4. (#12311)
* Instalator NVDA honoruje parametr `--minimal` i nie pdtwarza dźwięk uruchamiania, śledząc to samo dokumentowane zachowanie. (#12289)
* W MS Word lub Outlooku, klawisz szybkiej nawigacji do tabel może służyć do przeskakiwania do tabel wyglądu jeżeli opcja "dołączaj tabele wyglądu" jest włączona w ustawieniach trybu przeglądu. (#11899)
* NVDA już nie będzie wymawiał "↑↑↑" dla emoji w niektórych językach. (#11963)
* Espeak teraz wspeira ponownie kantoński i Mandaryński. (#10418)
* W nowym Microsoft Edgeopartym na siliniku Chromium, pola tekstowe, takie jak pasek adresu są wymawiane gdy są puste. (#12474)
* Naprawiony sterownik dla monitorów brajlowskich Seika. (#10787)

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

### Nowości

* Od teraz naciśnięcie klawisza F1 w oknach dialogowych NVDA spowoduje otwarcie pomocy podręcznej dla obecnie podświetlonej sekcji. (#7757)
* Dodano wsparcie dla technologii Intelli Sense w programach Microsoft SQL Server i Microsoft Visual Studio 2017 i nowszych. (#7504)
* Wymowa symboli: Dodano wsparcie dla grupowania referencji w zasadach zamiany. Powoduje to że zamiany są prostrze i bardziej funkcjonalne. (#11107)
* Od teraz generowane jest powiadomienie przy próbie utworzenia wpisu słownika zawierającego błędne wyrażenia regularne. (#11407)
  * W szczególności dotyczy to błędów grupowania.
* Dodano wsparcie dla nowej metody wprowadzania języka Chińskiego uproszczonego i tradycyjnego w systemie Windows 10. (#11562)
* Nagłówki zakładek są od teraz traktowane jako pola formularzy podczas szybkiej nawigacji przy pomocy klawisza F. (#10432)
* Dodano polecenie przełączające odczytywanie oznaczonego tekstu. Wymagane jest ręczne przypisanie gestu. (#11807)
* Dodano parametr wiersza poleceń --copy-portable-config pozwalający na przeniesienie konfiguracji przenośnej do konta użytkownika podczas cichej instalacji NVDA. (#9676)
* Klawisz routing jest od teraz wspierany w podglądzie brajla dla użytkowników korzystających z myszy. Aby przenieść kursor do komórki, kliknij myszą w odpowiednie miejsce. (#11804)
* NVDA automatycznie wykrywa urządzenia Humanware Brailliant BI 40X i 20X zarówno przez USB, jak i przez bluetooth. (#11819)

### Zmiany

* Zaktualizowano Liblouis do wersji 3.16.1:
 * Naprawiono krytyczne błędy.
 * Dodano tablicę brajlowską dla baszkirskiego pisma pełnego.
 * Dodano ośmiopunktową tablicę brajlowską dla języka koptyjskiego.
 * Dodano tablice brajlowskie: Rosyjski Literacki i Rosyjski Literacki Szczegółowy.
 * Usunięto tablicę brajlowską Rosyjski pismo pełne.
* Podczas czytania przy pomocy funkcji "czytaj wszystko" w trybie przeglądania, polecenia "znajdź następny" i "znajdź poprzedni" nie zatrzymują już czytania, gdy funkcja "zezwalaj na czytanie poglądowe" jest włączona. (#11563)
* Dla monitorów brajlowskich Hims F3 od teraz wywoływane jest przez naciśnięcie kombinacji klawiszy spacja +kropki 1, 4, 8. (#11710)
* Ulepszono prezentację opcji "Czas wyświetlania wiadomości brajlowskich" i "Pokazuj wiadomości brajlowskie w nieskończoność". (#11602)
* W przeglądarkach internetowych i innych aplikacjach wspierających tryb przeglądania, możliwe jest teraz wywołanie listy elementów (NVDA+F7) w trybie fokusu. (#10453)
* Zmiany w regionach ARIA nie są odczytywane, jeżeli ogłaszanie dynamicznych zmian treści jest wyłączone. (#9077)
* NVDA od teraz zgłasza status skopiowania przed skopiowanym tekstem. (#6757)
* Ulepszono prezentację widoku graficznego w menedżerze dysków systemu Windows. (#10048)
* Etykiety dla kontrolek są od teraz wyłączone (wyszarzone) kiedy kontrolka jest nieaktywna. (#11809)
* Zaktualizowano bazę danych Emoji CLDR do wersji 38. (#11817)
* Wbudowana funkcja  "podświetlanie fokusu" zmieniła nazwę na "podświetlacz wizualny". (#11700)

### Poprawki błędów

* NVDA ponownie działa poprawnie w polach edycyjnych w programie Fast Log Entry. (#8996)
* Od teraz, jeżeli nie możliwe jest uzyskanie całkowitego czasu trwania pliku w programie Foobar 2000, ogłaszany jest teraz czas, który upłynął od rozpoczęcia odtwarzania. (#11337)
* NVDA od teraz wspiera atrybut aria-roledescription w polach edycyjnych na stronach internetowych. (#11607)
* NVDA nie ogłasza już słowa 'lista' dla każdej linii listy w Google Docs lub jakiejkolwiek innej edytowalnej treści w Google Chrome. (#7562)
* Podczas przechodzenia po znakach lub słowach z jednego elementu listy do drugiego, zmiana jest od teraz ogłaszana. (#11569)
* NVDA od teraz odczytuje poprawną linię jeżeli kursor ustawiony jest na końcu linku, który znajduje się na końcu elementu listy w Google Docs lub innych edytowalnych treściach internetowych. (#11606)
* Na Windows 7, otwarcie i zamknięcie menu start z pulpitu ustawia kursor w odpowiednim miejscu. (#10567)
* Kiedy opcja "Próba anulowania mowy dla wygasłych zdarzeń" jest włączona, tytuł karty jest wymawiany podczas przełączania kart w przeglądarce Mozilla firefox. (#11397)
* NVDA od teraz poprawnie odczytuje element listy wybrany poprzez używanie nawigacji literowej podczas korzystania z syntezatora mowy Ivona. (#11651)
* Ponownie możliwe jest korzystanie z trybu przeglądania w programie Poczta Dla Windows 10. 16005.13110 i późniejsze. (#11439)
* Podczas korzystania z głosów Ivona firmy Harpo Software, NVDA ponownie może zapisywać swoje ustawienia, dokonywać zmian syntezatora i uruchamiać się ponownie. (#11650)
* Od teraz możliwe jest wpisanie cyfry 6 w brajlu komputerowym z klawiatury brajlowskiej monitora brajlowskiego Hims. (#11710)
* Znaczne poprawki wydajności w programie Azure Data Studio. (#11533, #11715)
* Kiedy włączona jest opcja "Próba anulowania mowy dla wygasłych zdarzeń" tytuł okna wyszukiwania NVDA jest od teraz oznajmiany. (#11632)
* Naprawiono błąd powodujący zawieszanie się NVDA w sytuacji gdy po wybudzeniu komputera ze stanu uśpienia kursor lądował w dokumencie programu Microsoft Edge. (#11576)
* Nie jest już wymagane wciśnięcie klawisza tab lub przesunięcie kursora po zamknięciu menu kontekstowego w przeglądarce Microsoft Edge, w celu przywrócenia poprawnego działania trybu przeglądania. (#11202)
* NVDA od teraz poprawnie odczytuje elementy list w 64-bitowych aplikacjach, takich jak Tortoise SVN. (#8175)
* Siatki aria są od teraz renderowane jak zwykłe tabele, zarówno w przeglądarce Google Chrome, jak i Mozilla Firefox. (#9715)
* Od teraz możliwe jest przeszukiwanie wstecz (NVDA+SHIFT+F3). (#11770)
* Skrypty NVDA nie są traktowane jako powtórzone, jeżeli pomiędzy ich gestami wykonany zostanie inny gest. (#11388) 
* Tagi Strong i emphasis w przeglądarce  Internet Explorer mogą być pominięte przy czytaniu przy wyłączeniu opcji zgłaszaj style w ustawieniach formatowania. (#11808)
* Występujące u niewielkiej liczby użytkowników kilkusekundowe zawieszanie się programu Microsoft Excel podczas nawigacji po komurkach nie powinno już występować. (#11818)
* W aplikacji Microsoft Teams, wersji 1.3.00.28xxx, NVDA ponownie poprawnie odczytuje wiadomości czatów prywatnych i grupowych. (#11821)
* Tekst oznaczony jako błąd gramatyczny i pisowni zarazem w Google Chrome, jest od teraz poprawnie ogłaszany przez NVDA. (#11787)
* Podczas korzystania z programu Microsoft Outlook w języku francuskim, skrót CTRL+SHIFT+R ponownie działa. (#11196)
* W programie Microsoft Visual Studio, dymki podpowiedzi funkcji Intellisense są wypowiadane tylko raz. (#11611)
* W kalkulatorze systemu Windows 10, NVDA nie ogłasza już postępu obliczeń gdy czytanie wpisywanych znaków jest wyłączone. (#9428)
* Przy wyświetlaniu adresów URL z NVDA ustawionym na tablicę brajlowską Angielski  US skróty  i włączoną opcją rozwiń słowo pod kursorem do brajla komputerowego, NVDA się już nie wysypuje. (#11754)

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

## 2020.3

To wydanie zawiera sporo poprawek dotyczących stabilności i szybkości działania szczególnie w pakiecie Microsoft Office. Dodano także ustawienia dotyczące ogłaszania grafik, jak i możliwość wyłączenia obsługi ekranu dotykowego.
Dodano również możliwość odczytywania podkreślonego tekstu w przeglądarkach, jak i nowe niemieckie tablice brajlowskie.

### Nowości

* Dodano możliwość wyłączenia odczytywania grafik. Można to uczynić z poziomu ustawień formatowania dokumentów. Alternatywny tekst dla grafik będzie wciąż odczytywany. (#4837)
* Od teraz możliwe jest przełączenie wsparcia ekranu dotykowego. Odpowiednia opcja znajduje się w ustawieniach interakcji dotykowej, a domyślne zdarzenie wejścia to CTRL+NVDA++ALT+T. (#9682)
* Dodano nowe niemieckie tablice brajlowskie. (#11268)
* NVDA od teraz odczytuje kontrolki tylko do odczytu w technologii UIA. (#10494)
* Występowanie podkreślonego tekstu jest od teraz ogłaszane zarówno w mowie, jak i w brajlu we wszystkich przeglądarkach internetowych. (#11436)
 * Opcja ta znajduje się w ustawieniach formatowania dokumentów.
* Dodano możliwość mapowania klawiszy systemowych na zdarzenia wejścia NVDA. Odpowiednia kategoria znajduje się w ustawieniach zdarzeń wejścia. (#6060)
  * Aby to zrobić, wciśnij przycisk "dodaj" po wybraniu opcji "emulowane klawisze systemowe".
* Od teraz wspierany jest model monitora brajlowskiego Handy Tech Active Braille z joystickiem. (#11655)
* Opcja "Automatyczny tryb czytania przy ruchach kursora" jest od teraz zgodna z wyłączeniem opcji "automatycznie ustaw fokus do elementów fokusujących". (#11663)

### Zmiany

* Skrypt służący do ogłaszania formatowania (NVDA+F) został zmodyfikowany tak, że od teraz ogłasza on formatowanie dla kursora systemowego, a nie kursora 	przeglądu. Aby uzyskać informacje o formatowaniu w pozycji kursora przeglądu, należy użyć skrótu NVDA+Shift+F. (#9505)
* Od teraz NVDA nie ustawia pozycji kursora systemowego na pierwszy klikalny element po wejściu w tryb przeglądania, poprawiając wydajność i stabilność. (#11190)
* Zaktualizowano CLDR z wersji 36.1 do 37. (#11303)
* Zaktualizowano Espeak-NG do wersji 1.51-dev, commit 1fb68ffffea4
* Od teraz możliwe jest używanie komend nawigacyjnych dla tabel w wielokolumnowych listach. (#8857)
* W menedżerze dodatków, "nie" jest od teraz domyślną opcją, gdy użytkownik pytany jest o usunięcie dodatku. (#10015)
* W programie Microsoft Excel, lista elementów wyświetla formuły w ich zlokalizowanej formie. (#9144)
* NVDA korzysta teraz z poprawnej terminologii dla uwag w programie Microsoft Excel. (#11311)
* W przypadku przesunięcia kursora przeglądu do fokusa w trybie przeglądania, kursor ustawia się w pozycji wirtualnego kursora. (#9622)
* Informacje ogłaszane w trybie przeglądania (takie jak informacje o formatowaniu), są teraz wyświetlane w lekko większym okienku na środku ekranu (#9910)

### Poprawki błędów

* NVDA od teraz mówi w sytuacji, gdy podczas nawigacji po wyrazach natrafi na symbol, po którym znajduje się spacja. (#5133)
* W aplikacjach korzystających z wersji QT 5.11 lub nowszych, opisy obiektów są ponownie ogłaszane. (#8604)
* Od teraz NVDA mówi, gdy usunięto słowo przy pomocy skrótu CTRL+Delete (#3298, #11029)
  * Wypowiadane jest słowo na prawo od usuniętego słowa.
* W ustawieniach ogólnych lista języków jest poprawnie sortowana. (#10348)
* W oknie "zdarzenia wejścia" znacznie poprawiono responsywność podczas filtrowania. (#10307)
* Od teraz możliwe jest wysyłanie znaków Unicode powyżej u+fff przy pomocy monitora brajlowskiego. (#10796)
* NVDA ponownie odczytuje okno dialogowe "otwórz za pomocą" w majowej aktualizacji systemu Windows 10. (#11335)
* Nowe eksperymentalne ustawienie (Włącz selektywną rejestrację zdarzeń UIA) może znacznie poprawić wydajność w programie Microsoft Visual Studio i innych aplikacjach korzystających z technologii UIA. (#11077, #11209)
* Stan "oznaczony" nie jest ogłaszany dla zaznaczalnych elementów listy. Od teraz odczytywany jest tylko stan "niezaznaczony". (#8554)
* W majowej aktualizacji systemu Windows, urządzenie "Mapowanie dźwięku Microsoft" jest ponownie pokazywana w oknie wyboru wyjścia mowy. (#11349)
* W przeglądarce Internet Explorer, indeksy listy są poprawnie odczytywane w przypadku, gdy pierwszym indeksem listy nie jest 1. (#8438)
* W przeglądarce Google Chrome, NVDA ogłasza stan zaznaczenie dla wszystkich zaznaczalnych kontrolek, nie tylko pól wyboru. (#11377)
* Ponownie możliwa jest nawigacja po pewnych kontrolkach gdy język NVDA ustawiony jest na aragoński. (#11384)
* Program NVDA nie powinien już się zawieszać kiedy dokonywana jest błyskawiczna nawigacja, lub wpisywane są znaki z włączoną obsługą brajla w programie Microsoft Word. (#11431, #11425, #11414)
* NVDA nie dodaje już nieistniejącej spacji gdy aktualny objekt nawigatora kopiowany jest do schowka. (#11438)
* NVDA nie aktywuje już profilu "czytaj wszystko", gdy nie ma nic do odczytania. (#10899, #9947)
* NVDA ponownie odczytuje listę funkcji dla Menedżera Usług Internetowych (IIS). (#11468)
* NVDA nie pozwala już na zamykanie kanału karty dźwiękowej, Znacznie poprawiając  wydajność na niektórych urządzeniach. (#5172, #10721)
* NVDA nie zamyka się, gdy przytrzymany jest skrót CTRL+Shift+Strzałka w dół. (#9463)
* Od teraz NVDA ponownie ogłasza stan drzewa w aplikacji Google Drive. (#11520)
* NVDA będzie automatycznie wykrywał NLS eReader Humanware monitor brajlowski połączony przez bluetooth ponieważ nazwa Bluetooth tego monitora brajlowskiego  od teraz jest zmieniona i brzmi "NLS eReader Humanware". (#11561)
* Niektóre głosy SAPI5 takie jak Ivona już nie omijają zdania. (#10901)
* Duże ulepszenia wydajności w Visual Studio Code. (#11533)

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

Najważniejsze zmiany w tej wersji to wsparcie nowego monitora brajlowskiego firmy Nattiq, lepsze wsparcie dla interfejsu graficznego programu antywirusowego ESET jak i programu Windows Terminal, poprawki wydajności w programie 1Password, poprawki wydajności w syntezatorach mowy OneCore jak i wiele ważnych zmian i poprawek.

### Nowości

* Wsparcie nowych monitorów brajlowskich:
  * Nattiq nBraille (#10778)
* Dodano skrypt służący do otwarcia katalogu konfiguracji użytkownika (skrót domyślnie nie przypisany). (#2214)
* Lepsze wsparcie dla interfejsu graficznego programu Esed Antivirus. (#10894)
* Dodano wsparcie dla terminala systemu Windows. (#10305)
* Dodano polecenie do odczytania aktualnego profilu konfiguracji (skrót domyślnie nieprzypisany). (#9325)
* Dodano polecenie służące do przełączania odczytywania indeksów górnych i dolnych (skrót domyślnie nieprzypisany). (#10985)
* W aplikacjach Internetowych, takich jak Gmail NVDA poprawnie odczytuje pozycję kursora, nawet jeżeli ten jest poruszany bardzo szybko. (#10885)
  * Ta eksperymentalna poprawka musi być ręcznie włączona poprzez opcję "Próba anulowania mowy dla wygasłych zdarzeń:" w panelu ustawieńń zaawansowanych.
* Dodano wiele symboli do domyślnego słownika. (#11105)

### Zmiany

* Zaktualizowano modół  liblouis braille translator z wersji 3.12 do [3.14.0](https://github.com/liblouis/liblouis/releases/tag/v3.14.0). (#10832, #11221)
* Odczytywanie indeksów górnych i dolnych jest teraz kontrolowane osobno od atrybutów czciąki. (#10919)
* Przez zmiany w programie VS Code, NVDA nie wyłącza już trybu przeglądania w widoku kodu. (#10888)
* NVDA nie wypowiada już wiadomości "Początek" i "Koniec" jeżeli kursor przeglądu  zostanie przeniesiony Na górę lub dół ekranu. (#9551)
* NVDA nie wypowiada już wiadomości "Lewy" i "Prawy" kiedy kursor przeglądu przeniesiony zostaje na pierwszy lub ostatni znak. (#9551)

### Poprawki błędów

* NVDA startuje poprawnie nawet jeżeli niie da się utworzyć pliku dziennika. (#6330)
* Naprawiono błąd powodujący niepoprawny komunikat odczytywany gdy zostanie usunięty wyraz przy pomocy skrótu CTRL+BACKSPACE w najnowszym wydaniu programu Microsoft Word 365. (#10851)
* W programie Winamp, NVDA znowu będzie odczytywać status przełączników "powtarzanie" i "losowe odtwarzanie utworów". (#10945)
* Naprawiono problem wydajności w programie 1Password. (#10508)
* Naprawiono problem, który powodował zacinanie się syntezatorów Windows OneCore. (#10721)
* NVDA już się nie zawiesza kiedy zostanie otwarte menu kontekstowe programu 1Password z zasobnika systemowego. (#11017)
* W programie Microsoft Office 2013 i starszych:
  * Wstążki są od teraz ogłaszane gdy kursor zostanie na nie przeniesiony po raz pierwszy. (#4207)
  * Elementy menu kontekstowych są ponownie ogłaszane poprawnie. (#9252)
  * Sekcje wstążki są ponownie ogłaszane podczas przemieszczania się po nich skrótem CTRL+Strzałki (#7067)
* Dla trybu przeglądania w przeglądarkach Mozilla Firefox i Google Chrome, text od teraz pojawia się poprawnie nawet, jeżeli używany jest Inline-flex (#11075)
* W trybie przeglądania z wyłączoną funkcją "Automatycznie ustaw kursor systemowy na elementach interaktywnych" możliwe jest teraz klikanie w elementy które nie normalnie nie mogą być kliknięte.
* W trybie przeglądania z wyłączoną funkcją "Automatycznie ustaw kursor systemowy na elementach interaktywnych" możliwe jest teraz klikanie w elementy normalnie aktywowane przy pomocy klawisza TAB. (#8528)
* W trybie przeglądania z wyłączoną funkcją "Automatycznie ustaw kursor systemowy na elementach interaktywnych", klikanie na niektóre elementy nie powoduje już zmian pozycji kursora. (#9886)
* NVDA nie odgrywa już dźwięków błędów przy nawigacji po kontrolkach tekstowych Dev Express. (#10918)
* Naprawiono błąd powodujący podwujne odczytywanie ikoy zasobnika systemowego, jeżeli dymek podpowiedzi był taki sam jak jej nazwa. (#6656)
* W trybie przeglądania z wyłączoną funkcją "Automatycznie ustaw kursor systemowy na elementach interaktywnych", przejście w tryb przeglądania przy pomocy skrótu NVDA+SPACJA podświetla element pod kursorem. (#11206)
* Ponownie możliwym jest sprawdzenie aktualizacji NVDA na pewnych konfiguracjach na przykład czystych instalacjach systemu Windows. (#11253)
* Poprawiono błąd uniemożliwiający poprawne pozycjonowanie kursora w aplikacjach JAVA. (#5989)

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

Najważniejsze zmiany w tej wersji to wsparcie niektórych monitorów brajlowskich HumanWare i APH, wiele ważnych poprawek błędów, takich jak ponowna możliwość odczytywania treści matematycznych W programie Microsoft Word przy użyciu MathPlayer / MathType.

### Nowości

* Aktualnie zaznaczony element na listach jest ponownie odczytywany w trybie przeglądania w przeglądarce Google Chrome, tak jak to było w NVDA 2019.1. (#10713)
* Możliwe jest teraz wykonanie symulacji prawego kliknięcia myszą na urządzeniach z ekranami dotykowymi. W tym celu, użyj gestu dwukliku z przytrzymaniem. (#3886)
* Wsparcie dla nowych monitorów brajlowskich: APH Chameleon 20, APH Mantis Q40, HumanWare BrailleOne, BrailleNote Touch v2, i NLS eReader. (#10830)

### Zmiany

* NVDA od teraz nie pozwala przejść systemowi w stan uśpienia, gdy aktywny jest tryb "czytaj wszystko". (#10643)
* Wsparcie dla ramek renderowanych poza procesem w przeglądarce Mozilla Firefox. (#10707)
* Zaktualizowano liblouis braille translator do wersji 3.12. (#10161)

### Poprawki błędów

* Poprawiono błąd uniemożliwiający prawidłowe odczytywanie symbolu Unicode (U+2212) (#10633)
* Podczas wybierania plików w menedżerze dodatków, ich nazwy nie są odczytywane podwójnie w oknie przeglądania. (#10620, #2395)
* W przeglądarce Mozilla Firefox wczytanie programu mastodon renderuje od teraz poprawnie wszystkie osie czasu. (#10776)
* W trybie przeglądania NVDA od teraz ogłasza poprawnie stany niektórych niezaznaczonych pól wyboru, które dawniej nie były odczytywane. (#10781)
* Stan przełączników Aria od teraz jest poprawnie odczytywany. (#9187)
* Głosy SAPI 4 powinny ponownie działać poprawnie. (#10792)
* NVDA może ponownie odczytywać i interagować z równaniami matematycznymi w programie Microsoft Word. (#10803)
* NVDA ponownie oznajmia usuwanie zaznaczenia z tekstu, jeżeli aktywny jest tryb przeglądania. (#10731).
* NVDA nie zamyka się, gdy występuje błąd inicjalizacji syntezatora mowy Espeak. (#10607)
* W razie błędu z dekodowaniem Unicode podczas instalacji, używane będą angielskie nazwy skrótów. (#5166, #6326)
* Wyjście strzałką z listy lub tabeli w trybie szybkiego czytania nie powoduje już ciągłego oznajmiania stanu elementu. (#10706)
* Naprawiono śledzenie myszy dla niektórych elementów MSHTML w Internet Explorerze. (#10736)

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

Wydanie 2019.3 programu NVDA jest bardzo ważne. Wiele zmian dotyczy samego silnika w tym przepisanie go z Python 2 na Python 3. Został również przepisany cały podsystem mowy.
Zmiany te powodują brak kompatybilności ze wcześniejszymi dodatkami programu, ale są konieczne dla bezpieczeństwa, a zmiany systemu mowy umożliwią w niedalekiej przyszłości wdrożenie ekscytującyh innowacyjnych ulepszeń.
 Pozostałe najważniejsze zmiany to wsparcie dla 64-bitowych maszyn wirtualnych języka Java, wsparcie nowych monitorów brajlowskich, moduł podglądu brajla, kurtyna ekranu i wiele, wiele więcej.

### Nowości

* Dokładność komendy "przesunięcie kursora do bieżącego obiektu nawigatora" została poprawiona dla pól tekstowych w aplikacjach Java. (#10157)
* Dodano wsparcie dla następujących monitorów brajlowskich firmy HandyTech (#8955):
 * Basic Braille Plus 40
 * Basic Braille Plus 32
 * Connect Braille
* Wszystkie zdarzenia wejścia zdefiniowane przez użytkownika mogą teraz zostać usunięte poprzez przycisk "Zresetuj do domyślnych" w dialogu "Zdarzenia Wejścia". (#10293)
* Zgłaszanie czcionki w programie Microsoft Word od teraz informuje czy tekst jest oznaczony jako ukryty. (#8713)
* Dodano polecenie przenoszące kursor nawigatora do początku zaznaczenia (NVDA+Shift+F9). (#1969)
* W przeglądarkach Internet Explorer, Microsoft Edge i nowszych wersjach Firefox i Chrome, znaczniki są teraz odczytywane w trybie przeglądania fokusa. (#10101)
* W przeglądarkach Internet Explorer, Google Chrome oraz Mozilla Firefox możliwa jest teraz nawigacja po artykułach i grupach przy pomocy nowych skryptów nawigacji. Te skrypty nie mają jednak przypisanych wartości domyślnych, można je przypisać z ekranu "zdarzenia wejścia" otwartego z poziomu obsługiwanego dokumentu. (#9485, #9227)
 * Figury również są teraz zgłaszane. Są one traktowane jako obiekty, toteż można po nich nawigować klawiszem O.
* W Internet Explorer, Mozilla Firefox, artykuły są od teraz zgłaszane podczas poruszania się nawigacją obiektową, oraz w trybie czytania (wymaga włączenia w ustawieniach formatowania dokumentów. (#10424)
* Dodano kurtynę. Po jej włączeniu ekran jest całkowicie czarny na Windows 8 i późniejszych. (#7857)
 * Dodano skrypt do tymczasowego włączania kurtyny, jak i do stałego jej włączenia. Skrypt nie ma domyślnie przypisanego skrótu klawiszowego.
 * Konfiguracja odbywa się poprzez odpowiednią zakładkę w oknie "Zdarzenia Wejścia"
* Dodano funkcję podświetlania ekranu (#971, #9064)
 * Podświetlanie fokusa, aktualnego obiektu nawigatora i kursora przeglądu może być teraz skonfigurowane w ustawieniach widoczności.
 * uwaga! Funkcja ta nie jest kompatybilna z dodatkiem Focus Highlight, jednakże ten dodatek wciąż może być używany, gdy wbudowane podświetlanie jest wyłączone.
* Dodano okno podglądu brajla. Pozwala ono na patrzenie na wyjście brajlowskie w małym oknie. (#7788)

### Zmiany

* Podręcznik użytkownika od teraz opisuje jak używać NVDA w oknie konsoli. (#9957)
* Uruchomienie pliku NVDA.exe od teraz zastępuje  w pamięci uruchomioną wcześniej kopię programu. Poprzednio używany przełącznik -r jest wciąż akceptowany, ale ignorowany. (#8320)
* W systemach Windows 8 i późniejszych, NVDA zgłasza teraz numer wersji i nazwę aplikacji UWP poprzez jej plik Manifest. (#4259, #10108)
* Włączanie i wyłączanie przy pomocy klawiatury ustawienia śledzenia zmian w programie Microsoft Office Word powoduje, że  NVDA od teraz zgłasza stan tego przełącznika. (#942)
* Numer wersji NVDA jest od teraz logowany jako pierwszy element w dzienniku zdarzeń NVDA. Zachodzi to nawet w wypadku wyłączenia logowania. (#9803)
* Dialog ustawień od teraz nie pozwala na zmianę ustawień logowania jeżeli została ona dokonana poprzez przełączniki wiersza poleceń. (#10209)
* W programie Microsoft Word, NVDA ogłasza teraz stan widoczności znaków niedrukowalnych po przełączeniu ich widoczności (CTRL+SHIFT+8) (#10241)
* Zaktualizowano Liblouis Braille Translator do wersji commit 58d67e63. (#10094)
* Gdy włączona jest opcja ogłaszania znaków CLDR, takich jak Emoji, są one odczytywane na wszystkich poziomach interpunkcji. (#8826)
* Pakiety firm trzecich języka Python, takie jak Comtypes zgłaszają swoje błędy bezpośrednio do dziennika zdarzeń NVDA. (#10393)
* Zaktualizowano repozytorium znaków Unicode do wersji 36.0. (#10426)
* W wypadku podświetlenia grupy elementów w trybie czytania, jej opis jest również odczytywany. (#10095)
* Java Access Bridge od teraz jest częścią NVDA. Pozwala to na dostęp do aplikacji pisanych w języku JAVA, łącznie z programami 64-bitowymi. (#7724)
* Jeżeli Java Access Bridge nie jest domyślnie aktywny dla użytkownika, NVDA dokonuje jego uruchomienia przy starcie. (#7952)
* Zaktualizowano Espeak-NG do wersji 1.51-dev, commit ca65812a. (#10581)

### Poprawki błędów

* Emoji i inne 32-bitowe znaki Unicode od teraz zajmują mniej miejsca na monitorach brajlowskich. (#6695)
* W systemie Windows 10, NVDA może odczytywać dymki powiadomień aplikacji UWP zakładając, że odczytywanie dymków jest włączone. (#8118)
* W Windows 10 Anniversary Update i późniejszych, wpisywany tekst jest teraz odczytywany w programie Mintty. (#1348)
* W Windows 10 Anniversary Update i późniejszych, tekst w konsoli pojawiający się blizko kursora nie jest literowany. (#513)
* Kontrolki w oknie kompresora programu Audacity są od teraz odczytywane podczas nawigacji po oknie.  (#10103)
* NVDA nie traktuje już spacji jako słów podczas przeglądania obiektowego w edytorach bazowanych na "Scintilla" takich jak Notepad ++. (#8295)
* NVDA od teraz nie pozwoli przejść systemowi w stan uśpienia, gdy wykryte zostanie przeglądanie przy pomocy monitora brajlowskiego. (#9175)
* W systemie Windows 10 brajl będzie teraz podążał za fokusem podczas edycji komórek w programie Excel i w innych kontrolkach UIA. (#9749)
* NVDA ponownie zgłasza sugestie w pasku adresu przeglądarki Microsoft Edge. (#7554)
* NVDA od teraz zgłasza, gdy zostanie podświetlona karta z zakładkami w programie Internet Explorer.(#8898)
* W przeglądarce Microsoft Edge bazowanej na silniku Edge HTML, NVDA nie będzie już odgrywał dźwięku sugestii wyszukiwania przy maksymalizacji okna. (#9110, #10002)
* Listy rozwijane Aria 1.1 od teraz są wspierane w przeglądarkach Mozilla Firefox i Chrome. (#9616)
* NVDA nie odczytuje niewidocznych kolumn dla kontrolki SysListView32. (#8268)
* Okno ustawień nie pokazuje teraz niepoprawnego poziomu logowania gdy NVDA uruchomione jest na ekranie bezpiecznym. (#10209)
* W menu Start systemu Windows 10 Anniversary Update i późniejszych, NVDA odczytuje szczegóły wyników wyszukiwania. (#10232)
* Jeżeli podczas poruszania kursora w trybie czytania nastąpi zmiana wyglądu, NVDA od teraz zachowuje się poprawnie. (#8831, #10343)
* Poprawiono kilka nazw punktorów w programie Microsoft Word. (#10399)
* W systemie Windows 10 aktualizacja majowa i późniejszych, NVDA ponownie ogłasza pierwszy element panelu Emoji jak i historii schowka po ich otwarciu. (#9204)
* W programie Poedit, możliwa jest edycja tłumaczeń języków zapisywanych od prawej do lewej. (#9931)
* W aplikacji ustawień systemu Windows 10, NVDA nie reaguje na paski poziomu głośności w mikserze głośności. (#10284)
* Niepoprawnie skonfigurowane wyrażenia regularne od teraz nie powodują całkowitego zawieszenia mowy. (#10334)
* Podczas czytania punktowanych elementów listy w programie Microsoft Word z włączoną obsługą UIA, wszystkie elementy będą teraz poprawnie odczytywane. (#9613)
* Kilka bardzo rzadkich błędów związanych z modułem Liblouis zostało naprawione. (#9982)
* Aplikacje Java uruchomione przed NVDA są od razu dostępne i nie wymagają restartu. (#10296)
* W przeglądarce Mozilla Firefox, gdy podświetlony element otrzymuje flagę "aria-current" ta zmiana nie jest anonsowana wielokrotnie. (#8960)
* NVDA od teraz będzie traktował niektóre złożone znaki Unicode jako pojedynczy znak podczas poruszania kursora. (#10550)
* Dodano wsparcie dla aplikacji Spring Tool Suite 4. (#10001)
* Naprawiono błąd z podwujnym czytaniem nazw, gdy są one oznaczone aria-labelledby, a docelowym elementem jest element potomny. (#10552)
* W systemie Windows 10 wersji 1607 i późniejszych, znaki wpisywane z klawiatur brajlowskich są od teraz odczytywane w większej ilości sytuacji. (#10569)
* W wypadku zmiany karty dźwiękowej w ustawieniach NVDA, dźwięki czytnika ekranu będą teraz odtwarzane przez nowowybraną kartę. (#2167)
* W przeglądarce Mozilla Firefox, przesuwanie kursora w trybie czytania jest szybsze. Powoduje to znaczne przyspieszenie działania w niektórych wypadkach. (#10584)

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

Ta wersja poprawia wiele istotnych błędów obecnych w wersji 2019.2. Poprawki obejmują:

* Naprawiono kilka błędów związanych z obsługą interfejsu sieciowego poczty Gmail, zarówno w Firefox, jak i w Chrome. Błędy te występowały podczas interakcji z niektórymi menu oraz przy zmianie pewnych ustawień poczty.(#10175, #9402, #8924)
* W systemie Windows 7, NVDA nie powoduje awarii modułu Explorer podczas używania myszy w menu start. (#9435) 
* NVDA nie zawiesza się podczas interakcji z adresami URI zakodowanymi w standardzie Base64 w przeglądarce Mozilla Firefox. (#10227)

## 2019.2

Najważniejsze zmiany w tej wersji to automatyczne wykrywanie linijek brajlowskich Freedom Scientific, eksperymentalne ustawienie zaawansowane wyłączenia podążania fokusu systemowego za kursorem trybu czytania (co może poprawić wydajność), możliwość podkręcania szybkości głosów mobilnych Windows,  oraz wiele poprawek.

### Nowości

* Wsparcie NVDA dla Miranda NG działa z nowszymi wersjami klienta. (#9053) 
* Można domyślnie wyłączyć tryb czytania poprzez odznaczenie nowej opcji "Włącz tryb czytania podczas wczytywania strony"  w ustawieniach trybu czytania NVDA. (#8716) 
 * Zauważ, że gdy opcja jest wyłączona, możesz włączać tryb czytania ręcznie, naciskając NVDA+spacja.
* Można filtrować symbole w oknie słowników wymowy i interpunkcji, działa to podobnie jak filtr na liście elementów trybu czytania czy oknie zdarzeń wejścia. (#5761)
* Dodana komenda zmiany rozdzielczości tekstu pod wskaźnikiem myszy (jak wiele tekstu zostanie wypowiedziane po ruchu myszy), nie posiada domyślnego przypisanego zdarzenia wejścia. (#9056)
* Syntezator głosów mobilnych Windows obsługuje podkręcanie prędkości mowy, co pozwala uzyskać znacząco szybszą mowę. (#7498)
* Opcja podkręcania szybkości jest konfigurowalna przez funkcję szybkiej zmiany ustawień syntezatora, jeżeli jest obsługiwana przez używany syntezator. (Obecnie eSpeak-NG and Głosy mobilne Windows). (#8934)
* Profile konfiguracji mogą być ręcznie aktywowane zdarzeniami wejścia, np. klawiszami skrótu. (#4209)
 * Zdarzenie musi być skonfigurowane w oknie "Zdarzenia wejścia".
* W Eclipse, dodana obsługa autouzupełniania w edytorze kodu. (#5667)
 * Dodatkowo, informacja Javadoc może być odczytana, jeśli jest obecna, przy użyciu NVDA+d.
* Dodana eksperymentalna opcja w ustawieniach zaawansowanych, pozwalająca wyłączyć podążanie fokusa systemowego za  kursorem trybu czytania (automatycznie ustawiaj fokus na elementach interaktywnych). (#2039) O ile wyłączanie tego może nie mieć sensu  dla wielu stron, to jednak może to rozwiązać: 
 * Efekt gumki: NVDA cofa ostatnią komendę trybu czytania i wraca do poprzedniego położenia.
 * Pola edycji na niektórych stronah przechwytujące fokus przy próbie wyjścia z nich.
 * Klawisze trybu czytania reagujące z opóźnieniem.
* Dla sterowników linijek, które to obsługują, ustawienia sterownika mogą być zmieniane w oknie ustawień brajlowskich NVDA. (#7452)
* Linijki Freedom Scientific mogą być automatycznie wykrywane. (#7727)
* Dodana komenda pokazywania zamiany dla symbolu pod kursorem przeglądu. (#9286)
* Dodana opcja w ustawieniach zaawansowanych pozwalająca  wypróbować nowy, będący jeszcze w fazie rozwoju,  sposób obsługi konsoli Windows przy użyciu Microsoft UI Automation API. (#9614)
* W konsoli Pythona pole edycyjne obsługuje wklejanie wielu linii ze schowka. (#9776)

### Zmiany

* Głośność syntezy jest teraz zwiększana i zmniejszana o 5 zamiast o 10 w mechanizmie szybkiej zmiany parametrów syntezatora. (#6754)
* Poprawione objaśnienie w managerze dodatków  pojawiające się po uruchomieniu NVDA z przełącznikiem --disable-addons. (#9473)
* Zaktualizowane opisy znaków Unicode emoji do wersji 35.0. (#9445)
* Klawisz skrótu pola filtru na liście elementów  trybu czytania, został zmieniony na alt+g. (#8728)
* Gdy automatycznie wykryta linijka brajlowska  jest podłączona przez Bluetooth, NVDA będzie poszukiwał linijki podłączonej przez USB, a obsługiwanej przy użyciu tego samego sterownika,   i przełączy się na połączenie USB, gdy stanie się dostępne. (#8853)
* eSpeak-NG zaktualizowany do commitu 67324cc.
* Translator brajlowski liblouis zaktualizowany do wersji 3.10.0. (#9439, #9678)
* NVDA wypowie słowo 'zaznaczone' po odczytaniu tekstu zaznaczone przez użytkownika. (#9028)
* W kodzie Microsoft Visual Studio, tryb czytania jest domyślnie wyłączony. (#9828)

### Poprawki błędów

* NVDA nie zawiesza się, gdy folder dodatków jest pusty. (#7686)
* Znaczniki kierunku tekstu LTR i RTL nie są od teraz zgłaszane  w brajlu lub przy czytaniu znak po znaku  w oknie właściwości. (#8361)
* Po przejściu do pola formularza przy pomocy szybkiej nawigacji trybu czytania, całe pole jest oznajmiane, a nie tylko pierwsza linia. (#9388)
* NVDA nie będzie się już uciszać po wyjściu z aplikacji Poczta systemu Windows 10. (#9341)
* Rozwiązane problemy uruchamiania NVDA , gdy język regionalnych ustawień użytkownika   nie jest rozpoznawany przez NVDA np. angielski (holandia). (#8726)
* Gdy tryb czytania jest włączony w Microsoft Excel i przełączysz się do przeglądarki w trybie formularzy lub odwrotnie, stan trybu czytania jest prawidłowo zgłaszany. (#8846)
* NVDA  prawidłowo zgłasza linię pod myszą w Notepad++  i innych edytorach bazujących na Scintilla. (#5450)
* W dokumentach Google Docs (i innych edytorach opartych na przeglądarce internetowej), brajl nie pokazuje teraz czasami nieprawidłowo znacznika końca listy przed kursorem  w środku elementu listy. (#9477)
* W aktualizacji z maja 2019 Windows 10 , NVDA nie odczytuje wielu powiadomień o głośności, gdy głośność jest zmieniana fizycznymi przyciskami  a fokus znajduje się na eksploratorze plików. (#9466)
* Otwieranie okien słowników wymowy lub interpunkcji jest teraz dużo szybsze gdy słowniki zawierają ponad 1000 wpisów. (#8790)
* w kontrolkach Scintilla  takich jak Notepad++, NVDA odczytuje prawidłową linię przy włączonym zawijaniu wierszy. (#9424)
* W Microsoft Excel, położenie komórki jest oznajmiane po jego zmianie przez shift+enter lub shift+numpadEnter. (#9499)
* W Visual Studio 2017 i nowszych, w oknie eksploratora obiektów, element zaznaczony w drzewie obiektów lub drzewie elementów z kategoriami, jest prawidłowo odczytywany. (#9311)
* Wtyczki o takich samych nazwach, różniących się tylko wielkością liter, nie są od teraz traktowane jako różne dodatki. (#9334)
* Dla głosów mobilnych Windows, prędkość ustawiona w NVDA  nie jest modyfikowana przez prędkość z ustawień mowy Windows 10. (#7498)
* Podgląd logów NVDA może być otwarty przy użyciu NVDA+F1 również wtedy, gdy nie można uzyskać informacji dla programistów z aktualnego obiektu  nawigatora. (#8613)
* Możliwe jest ponowne używanie komend NVDA nawigacji po tabelach w Google Docs w Firefox i Chrome. (#9494)
* Klawisze ochraniające  działają prawidłowo na linijkach Freedom Scientific. (#8849)
* Po odczytaniu pierwszego znaku dokumentu  w Notepad++ 7.7 X64, NVDA nie zawiesza się na czas do 10 sekund. (#9609)
* HTCom może teraz być używany z linijką brajlowską Handy Tech  w kombinacji z NVDA. (#9691)
* W Mozilla Firefox, aktualizacje obszarów dynamicznych nie są odczytywane  jeśli obszar znajduje się w zakładce będącej aktualnie w tle. (#1318)
* Poprawiona praca okna "Znajdź" w trybie czytania NVDA,  które nie funkcjonowało, gdy otwarte było w tle okno "O programie" NVDA. (#8566)

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

To wydanie poprawia następujące błędy:

* Excel 2007 : naprawione zawieszania programu powodowane przez NVDA, albo brak informacji, że komórka zawiera formułę. (#9431)
* Google Chrome  nie zawiesza się podczas interakcji z niektórymi listami. (#9364)
* Poprawka błędu, który powodował  brak możliwości skopiowania konfiguracji użytkownika do profilu systemowego. (#9448)
* W Microsoft Excel, NVDA ponownie używa przetłumaczonej informacji  przy zgłaszaniu połączonych komórek. (#9471)

## 2019.1

Najważniejsze zmiany w tej wersji to poprawki wydajności w Microsoft word i Excel, poprawki stabilności i bezpieczeństwa np. obsługa dodatków z informacjami o kompatybilności, oraz wiele innych.

Począwszy od tego wydania NVDA, dodatkowe wtyczki dla aplikacji,, sterowniki monitorów brajlowskich lub głosów, instalowane do podkatalogów appModules, globalPlugins, braille display drivers i synth drivers nie będą już wczytywane automatycznie.
Od teraz powinny one zostać zainstalowane jako dodatki NVDA. Dla autorów dodatków, kod testowy może być umieszczony w nowym podfolderze scratchpad w katalogu konfiguracji NVDA,  jeśli opcja piaskownicy NVDA jest zaznaczona w panelu zaawansowanych ustawień.
Te zmiany są konieczne dla zapewnienia lepszej kompatybilności własnego kodu, aby NVDA nie ulegał awariom, gdy ten eksperymentalny kod przestanie być kompatybilny z nowszymi wersjami.
Więcej informacji o wersjonowaniu dodatków, znajduje się na liście zmian poniżej.

### Nowości

* Nowe tablice brajlowskie: afrikaans, arabski brajl komputerowy, arabski skróty, hiszpański skróty. (#4435)
* Dodana opcja w ustawieniach myszy NVDA dla obsługi sytuacji, gdy mysz jest  kontrolowana przez inną aplikację. (#8452) 
 * Pozwoli to NVDA śledzić mysz, gdy system jest kontrolowany zdalnie przy użyciu TeamViewer lub innego oprogramowania kontroli zdalnej.
* Dodany parametr linii komend `--enable-start-on-logon`  aby umożliwić ustawianie działania na ekranie logowania w cichej instalacji NVDA. Ustaw na true aby uruchamiać na ekranie logowania, lub na false w przeciwnym wypadku. Jeśli przełącznik --enable-start-on-logon jest nieokreślony, NVDA domyślnie będzie startował na ekranie logowania, chyba że przy wcześniejszej instalacji  został inaczej skonfigurowany. (#8574)
* Można wyłączyć zapisywanie logów NVDA, ustawiając poziom logowania na "wyłączone" w ustawieniach ogólnych programu. (#8516)
* Zgłaszana jest obecność formuł w arkuszach LibreOffice i Apache OpenOffice. (#860)
* W Mozilla Firefox i Google Chrome, tryb czytania zgłasza zaznaczony element na listach i drzewach.
 * Działa to w Firefox 66 i nowszych.
 * Nie działa to dla niektórych list (kontrolki HTML select) w Chrome.
* Wczesne wsparcie aplikacji takich jak Mozilla Firefox na komputerach z procesorem ARM64 (np. Qualcom Snapdragon). (#9216)
* Ustawienia NVDA rozszerzone o kategorię zaawansowane, zawierającą opcję wypróbowania nowej obsługi Microsoft Word przy użyciu interfejsu Microsoft UI Automation. (#9200)
* Dodana obsługa graficznego podglądu zarządzania dyskami Windows. (#1486)
* Dodana obsługa Handy Tech Connect Braille and Basic Braille 84. (#9249)

### Zmiany

* Translator brajlowski liblouis zaktualizowany do wersji 3.8.0. (#9013)
* Autorzy dodatków mogą teraz ustawić minimalną wymaganą wersję NVDA dla ich dodatków. Niekompatybilne dodatki nie będą uruchamiane i instalowane. (#6275)
* Autorzy dodatków mogą teraz określić najwyższą wersję NVDA, z którą pracuje ich dodatek. Jeśli dodatek został przetestowany tylko z wersją NVDA starszą od bieżącej uruchomionej, NVDA odmówi instalacji i uruchomienia dodatku. (#6275)
* Ta wersja NVDA pozwoli na instalację i uruchamianie dodatków bez określonej wersji minimalnej  i ostatniej przetestowanej,  ale aktualizacja do przyszłych wersji NVDA (np. 2019.2)  może spowodować wyłączenie tych starszych dodatków.
* Komenda przywołania myszy do obiektu nawigatora działa teraz w Microsoft Word oraz w kontrolkach UIA controls, szczególnie Microsoft Edge. (#7916, #8371)
* Zgłaszanie tekstu pod wskaźnikiem myszy zostało poprawione w Microsoft Edge i innych aplikacjach UIA. (#8370)
* Uruchomienie NVDA z parametrem linii komend `--portable-path` powoduje, że podana ścieżka jest ustawiana jako domyślna przy tworzeniu kopii przenośnej z menu NVDA. (#8623)
* Zaktualizowana ścieżka norweskiej tablicy brajlowskiej, uwzględniająca standard z roku 2015. (#9170)
* Przy nawigacji akapitami (control+strzałki) lub po komórkach tabeli (control+alt+strzałki), nie są zgłaszane błędy pisowni, nawet jeśli NVDA jest ustawione, że ma je zgłaszać. Jest tak dlatego, że akapity lub komórki tabeli mogą mieć dużą objętość, a uzyskiwanie informacji o błędach pisowni w niektórych aplikacjach może zajmować dużo czasu. (#9217)
* NVDA od teraz nie wczytuje folderów appModules, globalPlugins oraz braille i synth drivers z folderu konfiguracji NVDA. Ten kod powinien zostać spakowany jako dodatek z poprawnymi informacjami o wersji, co zapewni, że kod niekompatybilny nie będzie uruchamiany z nowymi wersjami NVDA. (#9238)
 * Dla twórców chcących testować kod w trakcie prac nad nim,  należy włączyć tryb piaskownicy NVDA w ustawieniach zaawansowanych, oraz umieścić ten kod w podfolderze 'scratchpad' folderu konfiguracji NVDA.

### Poprawki błędów

* Głosy mobilne Windows: na Windows 10 w wersji Kwiecień 2018 i nowszych, duże fragmenty ciszy nie są od teraz wstawiane między wypowiedziami. (#8985)
* Podczas przechodzenia po znakach w kontrolkach tekstowych (takich jak Notatnik) lub w trybie czytania, 32-bitowe znaki  emoji składające się z dwóch punktów kodowych UTF-16 (takie jak 🤦) będą teraz odczytywane prawidłowo. (#8782)
* Poprawione okno potwierdzenia restartu po zmianie języka. Tekst okna i etykiety przycisków są teraz bardziej zwięzłe i mniej mylące. (#6416)
* Jeśli nie powiedzie się uruchomienie zewnętrznego syntezatora, NVDA przełączy się na głos mobilny pod Windows 10, zamiast na espeak. (#9025)
* Na zabezpieczonych ekranach, usunięte z menu okno powitalne NVDA. (#8520)
* Podczas używania tabulatora lub klawiszy szybkiej nawigacji trybu czytania, legendy zakładek są lepiej zgłaszane. (#709)
* NVDA teraz zgłasza zmiany niektórych kontrolek wyboru czasu takich jak używane w  aplikacjach alarmy i zegar. (#5231)
* W centrum akcji Windows 10, NVDA zgłasza zmiany statusu na przełącznikach takich jak jasność i asystent fokusa. (#8954)
* W centrum akcji Windows 10 aktualizacja październik 2018 i wcześniejsze, NVDA rozpoznaje szybką akcję jasności jako przycisk, a nie przełącznik. (#8845)
* NVDA ponownie śledzi kursor i zgłasza usuwane znaki w kontrolkach Idź do, oraz Znajdź w Microsoft Excel. (#9042)
* Naprawiony rzadki problem zawieszania się trybu czytania w Firefox. (#9152)
* Poprawki zgłaszania fokusa dla niektórych kontrolek zwiniętej wstążki Microsoft Office 2016.
* Poprawki zgłaszania sugerowanych kontaktów podczas wprowadzania adresów nowej wiadomości w Outlook 2016. (#8502)
* Ostatnie kilka klawiszy routingu na 80 -znakowej linijce eurobraille nie powodują przejścia kursora na początku lub tuż za początkiem linii. (#9160)
* Poprawiona nawigacja w tabeli widoku wątkowanych wiadomości w Mozilla Thunderbird. (#8396)
* W Mozilla Firefox i Google Chrome, przejście w tryb formularzy działa prawidłowo dla niektórych list i drzew (jeśli lista lub drzewo nie może uzyskać fokusu,  ale ich elementy mogą). (#3573, #9157)
* Tryb czytania jest prawidłowo domyślnie aktywny podczas czytania wiadomości w Outlook 2016/365, jeśli włączona jest eksperymentalna funkcja NVDA używania UI Automation dla obsługi dokumentów Word. (#9188)
* NVDA ma teraz dużo mniejsze szanse na zawieszenie się w taki sposób, że jedynym rozwiązaniem jest wylogowanie się z bieżącej sesji  Windows. (#6291)
* W aktualizacji Windows 10 październik 2018 i nowszych, po otwarciu historii schowka chmury z pustym schowkiem, NVDA zgłosi stan schowka. (#9112)
* W aktualizacji Windows 10 październik 2018 i nowszych, podczas szukania znaków emoji w panelu emoji, NVDA zgłasza pierwszy wynik wyszukiwania. (#9112)
* NVDA nie zawiesza się w głównym oknie Virtualbox 5.2 i nowszych. (#9202)
* Responsywność w Microsoft Word podczas nawigacji liniami, akapitami lub po komórkach tabeli, może być znacząco lepsza w niektórych dokumentach. Przypominamy, że dla najlepszej wydajności, warto ustawić widok Microsoft Word na widok wersji roboczej po otwarciu dokumentu. (#9217) 
* W Mozilla Firefox i Google Chrome, nie są zgłaszane puste alerty. (#5657)
* Znaczące poprawki wydajności podczas nawigacji w komórkach Microsoft Excel, szczególnie gdy arkusz zawiera komentarze i listy rozwijane. (#7348)
* Nie powinno być dłużej potrzebne wyłączanie edycji bezpośrednio w komórce arkusza w Microsoft Excel aby uzyskać dostęp do kontrolki edycji komórki z NVDA w Excel 2016/365. (#8146).
 * Poprawione zawieszanie w Firefox zdarzające się czasem podczas szybkiej nawigacji po punktach orientacyjnych, gdy używany był dodatek Enhanced Aria. (#8980)

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

Ta wersja naprawia zawieszanie się NVDA przy starcie, gdy język  programu był ustawiony na aragoński. (#9089)

## 2018.4

Najważniejsze zmiany w tej wersji to poprawki wydajności w najnowszych wersjach Mozilla Firefox, czytanie emoji wszystkimi syntezatorami, zgłaszanie odpowiedziano/przekazano na wiadomościach Outlook, oznajmianie odległości kursora od krawędzi strony w Microsoft Word, oraz wiele poprawek błędów.

### Nowości

* Nowe tablice brajlowskie: chiński (Chiny, mandaryński) z tonami i bez tonów. (#5553)
* Stan odpowiedziane/przekazane dalej, jest teraz zgłaszany na liście wiadomości w Microsoft Outlook. (#6911)
* NVDA może odczytywać opisy i emoji oraz inne znaki będące częścią repozytorium Unicode. (#6523)
* W Microsoft Word może być zgłaszana odległość kursora od lewej i górnej krawędzi strony po naciśnięciu NVDA+numpadDelete. (#1939)
* W arkuszach Google z włączonym trybem brajlowskim, NVDA nie anonsuje "wybrane" na każdej komórce przy zmianie punktu uwagi. (#8879)
* Dodana obsługa Foxit Reader i Foxit Phantom PDF (#8944)
* Dodana obsługa DBeaver database tool. (#8905)

### Zmiany

* W ustawieniach klawiatury NVDA, pola wyboru przełączające wybór klawiszy NVDA są teraz wyświetlane na liście, a nie jako osobne pola wyboru.
* NVDA nie będzie prezentować nadmiarowej informacji przy odczytywaniu zegara w szufladzie systemu na niektórych wersjach Windows. (#4364)
* Translator brajlowski liblouis zaktualizowany do wersji 3.7.0. (#8697)
* eSpeak-NG zaktualizowany do commit 919f3240cbb.

### Poprawki błędów

* W Outlook 2016/365, kategoria i stan flagi wiadomości są odczytywane. (#8603)
* Gdy NVDA jest ustawiony na język taki jak kirgizki, mongolski albo macedoński, nie pokazuje okna przy starcie z ostrzeżeniem, że język nie jest obsługiwany przez system operacyjny. (#8064)
* Przenoszenie wskaźnika myszy do nawigatora bardziej precyzyjnie przenosi wskaźnik do pozycji kursora trybu czytania w Mozilla Firefox, Google Chrome i Acrobat Reader DC. (#6460)
* Poprawiona interakcja z listami rozwijanymi na stronach web w Firefox, Chrome i Internet Explorer. (#8664)
* Po uruchomieniu NVDA na japońskiej wersji Windows XP lub Vista, wyświetlany jest alert wymagań wersji systemu operacyjnego. (#8771)
* Poprawki wydajności Mozilla Firefox podczas nawigacji na dużych stronach z dużą ilością dynamicznych zmian. (#8678)
* Brajl nie pokazuje atrybutów czcionki, jeśli zostały one wyłączone w  ustawieniach formatowania dokumentów NVDA. (#7615)
* Rozwiązany problem śledzenia punktu uwagi w eksploratorze Windows i innych aplikacjach używających UI Automation, gdy inna aplikacja jest zajęta (np. konwersją audio). (#7345)
* W menu ARIA na stronach internetowych, klawisz Escape będzie przekazywany do menu, zamiast bezwarunkowo przełączać tryb czytania. (#3215)
* W nowym Gmail, podczas używania szybkiej nawigacji wewnątrz wiadomości przy ich czytaniu, cała treść wiadomości nie jest od teraz zgłaszana po elemencie, do którego przeniesiony został punkt uwagi. (#8887)
* Po aktualizacji NVDA, przeglądarki takie jak Firefox i google Chrome nie powinny się zawieszać, a tryb czytania powinien nadal prawidłowo odzwierciedlać zmiany aktualnie załadowanych dokumentów. (#7641) 
* NVDA nie zgłasza wielokrotnie "Klikalne" podczas nawigacji elementów klikalnych w trybie czytania. (#7430)
* Zdarzenia wejścia wykonywane na linijkach brajlowskich baum Vario 40 będą od teraz prawidłowo uruchamiane. (#8894)
* W Slajdach Google z Mozilla Firefox, NVDA nie zgłasza zaznaczonego tekstu na każdej kontrolce z punktem uwagi. (#8964)

### Changes for Developers

* gui.nvdaControls now contains two classes to create accessible lists with check boxes. (#7325)
 * CustomCheckListBox is an accessible subclass of wx.CheckListBox.
 * AutoWidthColumnCheckListCtrl adds accessible check boxes to an AutoWidthColumnListCtrl, which itself is based on wx.ListCtrl.
* If you need to make a wx widget accessible which isn't already, it is possible to do so by using an instance of gui.accPropServer.IAccPropServer_impl. (#7491)
 * See the implementation of gui.nvdaControls.ListCtrlAccPropServer for more info.
* Updated configobj to 5.1.0dev commit 5b5de48a. (#4470)
* The config.post_configProfileSwitch action now takes the optional prevConf keyword argument, allowing handlers to take action based on differences between configuration before and after the profile switch. (#8758)

## 2018.3.2

Pomniejsze wydanie wprowadzające obejście zawieszania się Google Chrome przy nawigacji tweetów na stronie [www.twitter.com](http://www.twitter.com). (#8777)

## 2018.3.1

Pomniejsze wydanie poprawiające krytyczny błąd w NVDA, powodujący zawieszanie się 32-bitowych wersji Mozilla Firefox. (#8759)

## 2018.3

Najważniejsze zmiany w tej wersji to automatyczne wykrywanie wielu linijek brajlowskich, obsługa nowych funkcji Windows 10  (w tym panel wprowadzania EMOI) i wiele poprawek błędów.

== Nowe funkcje =

* NVDA będzie zgłaszać błędy pisowniw Mozilla Firefox, gdy są prawidłowo oznaczone przez strony internetowe. (#8280)
* Treść oznaczona jako wstawiona lub usunięta na stronach internetowych, jest teraz zgłaszana w Google Chrome. (#8558)
* Dodana obsługa kółka przewijania BrailleNote QT i Apex BT gdy BrailleNote  jest używany jako linijka brajlowska w NVDA. (#6316)
* Dodane skrypty zgłaszania czasu całkowitego i czasu, który upłynął dla bieżącej ścieżki w Foobar2000. (#6596)
* Symbol klawisza komendy Mac (⌘) jest wypowiadany podczas czytania tekstu dowolnym syntezatorem. (#8366)
* Własne role zdefiniowane atrybutem aria-roledescription  są teraz obsługiwane we wszystkich przeglądarkach.
* Nowe tablice brajlowskie: czeski 8-punktowy, środkowo kurdyjski, Esperanto, węgierski, szwedzki 8-punktowy  brajl komputerowy. (#8226, #8437)
* Dodana obsługa automatycznego wykrywania w tle linijek brajlowskich. (#1271)
 * Obsługiwane są obecnie ALVA, Baum/HumanWare/APH/Orbit, Eurobraille, Handy Tech, Hims, SuperBraille i HumanWare BrailleNote i Brailliant BI/B.
 * Można włączyć tę funkcję zaznaczając opcję automatyczny na liście linijek brajlowskich w oknie wyboru monitora brajlowskiego NVDA.
 * Więcej szczegółów w dokumentacji.
* Dodana obsługa różnych nowych metod wprowadzania z ostatnich wersji Windows 10. Są to panel emoji (aktualizacja Fall Creators), dyktowanie (aktualizacja Fall Creators), sugestie wprowadzania klawiatury sprzętowej (aktualizacja kwiecień 2018) i wklejanie ze schowka w chmurze (aktualizacja październik 2018). (#7273)
* Treść oznaczona jako blok cytatu przy użyciu ARIA (role blockquote) jest obsługiwana w Mozilla Firefox 63. (#8577)

### Zmiany

* Lista dostępnych języków w ustawieniach ogólnych jest teraz sortowana  według nazw, zamiast ich kodu ISO 639. (#7284)
* Dodano domyślne zdarzenia wejścia dla alt shift tab i windows tab we wszystkich obsługiwanych linijkach brajlowskich Freedom Scientific. (#7387)
* Dla linijek ALVA BC680 i protocol converter, można przypisać różne funkcje do lewego i prawego smart pada, oraz klawiszy thumb i etouch. (#8230)
* Dla linijek ALVA BC6, kombinacja klawiszy sp2+sp3 oznajmia aktualną datę i czas, natomiast sp1+sp2 emuluje klawisz Windows. (#8230)
* Użytkownik jest teraz jednorazowo pytany przy starcie NVDA o zgodę na przesyłanie statystyk użycia do NV Access podczas automatycznego sprawdzania aktualizacji. (#8217)
* Podczas sprawdzania aktualizacji, jeśli użytkownik zgodził się  na przesyłanie statystyk użycia do NV Access, NVDA prześle nazwę używanego sterownika syntezatora i linijki brajlowskiej, aby możliwe było lepsze oszacowanie priorytetu przyszłych prac nad tymi sterownikami. (#8217)
* Translator brajlowski liblouis zaktualizowany do wersji 3.6.0. (#8365)
* Zaktualizowana ścieżka do prawidłowej tablicy brajlowskiej rosyjski 8-punktowy. (#8446)
* Zaktualizowany eSpeak-ng do 1.49.3dev commit 910f4c2 (#8561)

### Poprawki błędów

* Etykiety dostępności dla kontrolek w Google Chrome są teraz bardziej czytelnie zgłaszane w trybie czytania, gdy etykieta nie pojawia się jako fragment treści. (#4773)
* Powiadomienia są obsługiwane w programie Zoom. Dla przykładu, obejmuje to stan wyciszenia i wiadomości przychodzące. (#7754)
* Przełączenie kontekstu prezentacji brajla w trybie czytania nie powoduje zatrzymania wyświetlania brajla. (#7741)
* Linijki ALVA BC680 nie powodują sporadycznych problemów inicjalizacji. (#8106)
* Domyślnie, linijki ALVA BC6 nie będą uruchamiać emulowanych klawiszy systemowych, gdy naciśnięto kombinacje zawierające sp2+sp3  dla uruchomienia wewnętrznych funkcji. (#8230)
* Naciśnięcie sp2 na linijce ALVA BC6  dla emulacji klawisza alt działa zgodnie z opisem. (#8360)
* NVDA nie oznajmia zbędnych zmian układu klawiatury. (#7383, #8419)
* Śledzenie myszy jest teraz bardziej dokładne w notatniku i innych kontrolkach edycji zwykłego tekstu, jeśli długość treści przekracza 65535 znaków. (#8397)
* NVDA rozpoznaje więcej okien dialogowych w Windows 10 i innych nowoczesnych aplikacjach. (#8405)
* W Windows 10 aktualizacja październik 2018 i Server 2019 lub nowszych, rozwiązany problem niepowodzenia śledzenia przez NVDA punktu uwagi, gdy aplikacja przestała odpowiadać, albo zasypuje system dużą ilością generowanych zdarzeń. (#7345, #8535)
* Użytkownicy są teraz informowani przy próbie czytania lub kopiowania pustego paska stanu. (#7789)
* Naprawiony przypadek, gdy stan "niezaznaczone"  na kontrolkach nie był zgłaszany mową jeśli kontrolka wcześniej była w stanie częściowego zaznaczenia. (#6946)
* Na liście języków w ustawieniach ogólnych NVDA, nazwa języka birmańskiego jest wyświetlana prawidłowo w Windows 7. (#8544)
* W Microsoft Edge, NVDA będzie oznajmiać powiadomienia takie jak dostępność widoku odczytu albo postęp wczytywania strony. (#8423)
* Po wejściu do listy na stronie internetowej, NVDA zgłosi etykietę listy, jeśli została zdefiniowana przez autora strony. (#7652)
* Podczas ręcznego przypisywania funkcji do zdarzeń wejścia dla konkretnej linijki brajlowskiej, te zdarzenia wejścia są wyświetlane jako przypisane do tej linijki. Wcześniej wyświetlały się jako przypisane do aktualnie używanej linijki. (#8108)
* Obsługiwana jest 64-bitowa wersja Media Player Classic. (#6066)
* Kilka poprawek obsługi brajla w Microsoft Word z włączoną UI Automation:
 * Podobnie do innych wielowierszowych kontrolek tekstu, na początku dokumentu w brajlu linijka jest tak pozycjonowana, że pierwszy znak dokumentu znajduje się na początku linijki. (#8406)
 * Zmniejszona przesadna gadatliwość prezentacji punktu uwagi w mowie i brajlu podczas ustawiania punktu uwagi na dokumencie Word. (#8407)
 * Przywoływanie kursora brajlowskiego działa prawidłowo  na listach dokumentu Word. (#7971)
 * Nowo wstawiane punktory lub numery w dokumencie Word są prawidłowo oznajmiane mową i brajlem. (#7970)
* W Windows 10 1803 i nowszych, możliwa jest teraz instalacja dodatków, gdy włączone jest używanie Unicode UTF-8 dla ogólnoświatowej obsługi języków. (#8599)
* NVDA nie powoduje, że iTunes 12.9 i nowsze stają się niemożliwe do interakcji. (#8744)

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

To wydanie zawiera aktualizacje tłumaczeń związane  z usunięciem w ostatniej chwili funkcjonalności powodującej problemy.

## 2018.2

Najważniejsze zmiany w tej wersji to obsługa tabel w Kindle dla PC, wsparcie linijek brajlowskich Humanware BrailleNote Touch i BI14 Braille, poprawki obsługi głosów mobilnych i syntezatorów Sapi5, poprawki w Microsoft Outlook i wiele więcej.

### Nowości

* Zasięg wierszy i kolumn komórek tabeli jest zgłaszany mową i brajlem. (#2642)
* Komendy nawigacji po tabelach są obsługiwane w dokumentach Google (z włączonym trybem brajlowskim). (#7946)
* Możliwość odczytywania tabel i nawigacji wewnątrz nich w Kindle dla PC. (#7977)
* Obsługa linijek HumanWare BrailleNote touch i Brailliant BI 14 przez USB i bluetooth. (#6524)
* W aktualizacji Windows 10 Fall Creators Update i nowszych, NVDA może zgłaszać powiadomienia z aplikacji takich jak Kalkulator i Sklep Windows. (#8045)
* Nowe tablice brajlowskie: litewski 8-punktowy, ukraiński, mongolski stopień 2. (#7839)
* Dodany skrypt zgłaszający informacje formatowania tekstu pod konkretną komórką brajlowską. (#7106)
* Można odłożyć na później instalację aktualizacji NVDA po jej pobraniu. (#4263) 
* Nowe języki: mongolski, szwajcarski niemiecki.
* Można teraz przełączać control, shift, alt, windows i NVDA z klawiatury brajlowskiej i łączyć te przełączniki z wprowadzaniem brajla (np. nacisnąć control+s). (#7306) 
 * Można przypisać te przełączniki do klawiszy przy użyciu poleceń w kategorii emulowane klawisze systemowe w oknie zdarzenia wejścia.
* Przywrócona obsługa linijek brajlowskich Handy Tech Braillino i Modular (ze starym firmware). (#8016)
* Data i czas obsługiwanych urządzeń Handy Tech (takich jak Active Braille i Active Star) będzie automatycznie synchronizowana przez NVDA , jeśli nastąpi rozsynchronizowanie dłuższe niż 5 sekund. (#8016)
* Można przypisać zdarzenie wejścia dla tymczasowego wyłączenia  wszystkich wyzwalaczy profili konfiguracji. (#4935)

### Zmiany

* Kolumna stanu dodatku w zarządzaniu dodatkami określa teraz czy dodatek jest włączony czy wyłączony, a nie jak dawniej - uruchomiony lub wstrzymany. (#7929)
* Translator brajlowski liblouis zaktualizowany do wersji 3.5.0. (#7839)
* Litewska tablica brajlowska nazywa się teraz litewska 6-punktowa, dla jednoznacznego odróżnienia od nowej tablicy 8-punktowej. (#7839)
* Usunięte tablice brajlowskie francuski (kanadyjski) stopień 1 i stopień 2. Zamiast tego, będą używane odpowiednio tablice brajlowskie francuski (ujednolicony) 6-punktowy brajl komputerowy i stopień 2. (#7839)
* Drugie przyciski routingu w linijkach Alva BC6, EuroBraille i Papenmeier braille teraz zgłaszają informacje formatowania tekstu pod odpowiednią komórką brajlowską powiązaną z naciśniętym przyciskiem. (#7106)
* Tablice brajlowskie wprowadzania skrótami przełączają się w tryb nieskrótowy w przypadkach nieedycyjnych (tj. kontrolek bez kursora, albo w trybie czytania). (#7306)
* NVDA jest teraz mniej gadatliwe, gdy spotkanie lub zdarzenie w kalendarzu Outlook zajmuje cały dzień. (#7949)
* Wszystkie ustawienia NVDA są teraz umieszczone w jednym oknie dialogowym w menu NVDA->Ustawienia->Preferencje, zamiast w wielu oknach. (#7302)
* Domyślnym syntezatorem dla Windows 10  są teraz głosy mobilne, zamiast eSpeak. (#8176)

### Poprawki błędów

* Naprawiony błąd braku odczytu kontrolki z punktem uwagi na ekranie logowania do konta Microsoft w ustawieniach, po wprowadzeniu adresu email. (#7997)
* Naprawiony odczyt strony gdy nastąpiło przejście z poprzedniej strony w Microsoft Edge. (#7997)
* Naprawiony problem nieprawidłowego oznajmiania ostatniego znaku PIN logowania windows 10 przy odblokowywaniu urządzenia. (#7908)
* Etykiety pól wyboru i przycisków opcji w Chrome i Firefox nie są podwójnie odczytywane po użyciu klawisza Tab lub szybkiej nawigacji w trybie czytania. (#7960)
* Prawidłowa obsługa wartości parametru aria-current. (#7892).
* Syntezator głosów mobilnych Windows nie przestaje się uruchamiać, gdy ustawiony głos został odinstalowany. (#7999)
* Zmiana głosu w syntezatorze głosów mobilnych Windows, jest obecnie dużo szybsza. (#7999)
* Naprawiono nieprawidłową treść brajlowską generowaną dla kilku tablic brajlowskich, włączając w to znaki w 8-punktowym skróconym duńskim brajlu. (#7526, #7693)
* NVDA zgłasza teraz więcej rodzajów punktorów w Microsoft Word. (#6778)
* Uruchomienie skryptu zgłaszania formatowania nie powoduje nieprawidłowego przesunięcia kursora przeglądu i w związku z tym uruchomienie polecenia wielokrotnie nie daje od teraz różnych wyników. (#7869)
* Wprowadzanie brajla nie zezwala na skróty w przypadkach, gdy nie jest to obsługiwane (tj. całe słowa nie będą od teraz wysyłane do systemu poza edycją tekstu i w trybie czytania). (#7306)
* Naprawione problemy stabilności połączenia dla linijek brajlowskich Handy Tech Easy Braille i Braille Wave. (#8016)
* W Windows 8 i nowszych, NVDA nie będzie oznajmiać "nieznane" po otwarciu szybkiego menu (Windows+X) i podczas wybierania elementów tego menu. (#8137)
* Powiązania przycisków ze zdarzeniami wejścia specyficzne dla modelu linijek brajlowskich Hims, działają teraz zgodnie z informacjami w podręczniku użytkownika. (#8096)
* NVDA próbuje teraz naprawiać problemy rejestracji  system COM powodujące niedostępność programów takich jak Firefox i Internet Explorer, skutkujące odczytywaniem  "nieznane" przez NVDA. (#2807)
* Obejście błędu w managerze zadań, powodującego brak dostępu użytkownika  do określonych szczegółów dotyczących procesów. (#8147)
* Nowsze głosy Microsoft SAPI5 nie powodują opóźnień na końcu mowy, co czyni pracę z użyciem tych głosów bardziej efektywną. (#8174)
* W Windows 10 RS5, NVDA nie zgłasza nadmiarowych zbędnych informacji  podczas przełączania zadań przy użyciu alt+tab. (#8258)

### Changes for developers

* The developer info for UIA objects now contains a list of the UIA patterns available. (#5712)
* App modules can now force certain windows to always use UIA by implementing the isGoodUIAWindow method. (#7961)
* The hidden boolean flag "outputPass1Only" in the braille section of the configuration has again been removed. Liblouis no longer supports pass 1 only output. (#7839)

## 2018.1.1

Specjalne wydanie NVDA w związku z błędem sterownika syntezatora głosów mobilnych Windows, powodującym generowanie wyższej i szybszej mowy w wersji Windows 10 Redstone 4 (1803). (#8082)  

## 2018.1

Najważniejsze zmiany w tej wersji to obsługa wykresów w Microsoft word i Powerpoint, nowe obsługiwane monitory brajlowskie: Eurobraille i Optelec protocol converter, poprawiona obsługa monitorów brajlowskich Hims i Optelec, poprawki wydajności przy współpracy z Mozilla Firefox 58 i nowszymi, oraz wiele więcej.

### Nowe funkcje

* Możliwa jest interakcja z wykresami w Microsoft Word i Microsoft Powerpoint, podobna do istniejącego wsparcia wykresów w Microsoft Excel. (#7046)
 * W Microsoft Word:  w trybie czytania, przejdź do załączonego wykresu i naciśnij Enter, aby wejść z nim w interakcję.
 * W Microsoft Powerpoint podczas edycji slajdu: przejdź klawiszem Tab do obiektu wykresu i naciśnij enter lub spację aby rozpocząć interakcję z wykresem.
 * Aby zakończyć interakcję z wykresem, naciśnij escape.
* Nowy język: kirgizki.
* Dodana obsługa VitalSource Bookshelf. (#7155)
* Dodane wsparcie Optelec protocol converter, urządzenia pozwalającego używać monitorów brajlowskich Braille Voyager i Satellite przy zastosowaniu protokołu komunikacyjnego ALVA BC6. (#6731)
* Można używać wprowadzania brajlowskiego na linijce ALVA 640 Comfort. (#7733) 
 * Funkcjonalność NVDA może być używana z tym, jak i innymi monitorami brajlowskimi BC6 posiadającymi firmware 3.0.0 i wyższe.
* Wczesne wsparcie arkuszy Google z włączonym trybem brajlowskim. (#7935)
* Obsługa monitorów brajlowskich Eurobraille Esys, Esytime i Iris. (#7488)

### Zmiany

* Sterowniki monitorów brajlowskich HIMS Braille Sense/Braille EDGE/Smart Beetle i Hims Sync Braille zostały zastąpione przez jeden sterownik. Sterownik zostanie aktywowany automatycznie dla użytkowników starszych sterowników. (#7459) 
 * Zmieniono przypisania niektórych klawiszy, szczególnie klawiszy przewijania, dla dopasowania ich do konwencji stosowanej w produktach Hims. Więcej szczegółów w podręczniku użytkownika.
* Podczas pisania na klawiaturze ekranowej przy użyciu dotyku, domyślnie należy dwukrotnie stuknąć każdy klawisz w taki sam sposób, jak aktywuje się dowolną inną kontrolkę.
 * Aby użyć istniejącego trybu "wpisywania dotykowego" , w którym podniesienie palca z dotykanego klawisza wystarczy by go aktywować, włącz tę opcję w nowym oknie dialogowym interakcji dotykowej dostępnym w menu ustawień NVDA. (#7309)
* Nie jest od teraz konieczne powiązywanie brajla z punktem uwagi lub kursorem przeglądu, ponieważ domyślnie stanie się to automatycznie. (#2385) 
 * Automatyczne przywiązywanie będzie wykonywane, gdy użyto komend kursora przeglądu lub nawigacji w hierarchii obiektów. Przewijanie nie będzie aktywować tego nowego zachowania.

### Poprawki błędów

* Wiadomości dostępne w trybie czytania, takie jak aktualne formatowanie po dwukrotnym szybkim naciśnięciu NVDA+f, działają teraz prawidłowo, gdy NVDA jest zainstalowany w lokalizacji zawierającej znaki z poza ASCII. (#7474)
* Punkt uwagi jest ponownie prawidłowo przywracany po powrocie do Spotify z innej aplikacji. (#7689)
* NVDA nie ma problemów z aktualizacją w systemach z włączoną kontrolą dostępu do folderów (dostępną w jesiennej aktualizacji dla twórców Windows 10). (#7696)
* Poprawione wykrywanie klawiszy przewijania na monitorach brajlowskich Hims Smart Beetle. (#6086)
* Niewielka poprawa wydajności przy odczytywaniu dużej ilości treści w Mozilla Firefox 58 i nowszych. (#7719)
* W Microsoft Outlook, podczas odczytywania wiadomości email zawierających tabele, nie pojawiają się błędy.  (#6827)
* Zdarzenia wprowadzania brajla, które emulują systemowe modyfikatory klawiatury, mogą teraz być łączone z innymi emulowanymi klawiszami systemowymi, jeśli jedno lub więcej takich zdarzeń jest specyficzne dla modelu. (#7783)
* W Mozilla Firefox, tryb czytania działa prawidłowo w oknach wyskakujących, utworzonych przez dodatki takie jak LastPass i bitwarden. (#7809)
* NVDA nie zawiesza się dłużej przy każdej zmianie punktu uwagi, gdy Firefox lub Chrome przestały odpowiadać np. wskutek awarii, albo zawieszenia się przeglądarki. (#7818)
* w klientach twitter takich jak Chicken Nugget, NVDA nie pomija od teraz ostatnich 20 znaków 280-znakowych tweetów podczas ich odczytywania. (#7828)
* NVDA teraz używa prawidłowego języka oznajmiając symbole, gdy zaznaczony jest tekst. (#7687)
* W nowszych wersjach Office 365, ponownie jest możliwa nawigacja w wykresach Excel przy użyciu klawiszy strzałek. (#7046)
-  w wyjściu brajla i mowy, stany kontrolek będą zawsze zgłaszane w takiej samej kolejności, niezależnie od tego, czy są pozytywne czy negatywne. (#7076)
* W aplikacjach takich jak Poczta systemu Windows 10, NVDA nie ma od teraz problemów z oznajmianiem znaków kasowanych przy użyciu backspace. (#7456)
* Wszystkie klawisze na linijce Hims Braille Sense Polaris, działają teraz tak jak powinny. (#7865)
* Rozwiązany problem uruchamiania NVDA na Windows 7 zgłaszającego wewnętrzny błąd api-ms dll, gdy konkretna wersja Visual Studio 2017 redistributables została zainstalowana przez inną aplikację. (#7975)

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

Najważniejsze zmiany w tej wersji to liczne ulepszenia aplikacji sieci web  w tym domyślne włączenie trybu czytania dla okien dialogowych stron www, lepszy odczyt grup pól w trybie czytania, obsługa nowych technologii Windows 10 takich jak strażnik aplikacji Windows Defender  oraz Windows 10 na ARM64, automatyczny odczyt orientacji ekranu i stanu baterii.  
Proszę zauważyć, że ta wersja NVDA nie obsługuje Windows XP ani Windows Vista. Minimalny wymagany system operacyjny dla  NVDA to od teraz windows 7 with Service Pack 1.

### Nowe funkcje

* W trybie czytania, można przeskoczyć poza koniec lub do początku punktów orientacyjnych przy użyciu komendy przeskocz na koniec/początek kontenera (przecinek/shift+przecinek). (#5482)
* W przeglądarkach Firefox, Chrome i Internet Explorer, szybka nawigacja do pól edycyjnych i kontrolek formularzy, uwzględnia pola edytowalne Rich Text (np. contentEditable). (#5534)
* W przeglądarkach internetowych lista elementów może wyświetlać kontrolki formularzy i przyciski. (#588)
* Wstępna obsługa Windows 10 na procesorach ARM64. (#7508)
* Wczesne wsparcie odczytywania i interaktywnej nawigacji treści matematycznych dla książek Kindle z dostępną matematyką. (#7536)
* Dodana obsługa czytnika książek Azardi. (#5848)
* Informacje o wersji dodatków są zgłaszane podczas ich aktualizacji. (#5324)
* Dodana obsługa nowych parametrów wiersza poleceń tworzących przenośną kopię NVDA. (#6329)
* Obsługa Microsoft Edge uruchomionego wewnątrz strażnika aplikacji Windows Defender (#7600)
* Podczas pracy na laptopie lub tablecie, NVDA zgłosi podłączenie lub odłączenie ładowarki, oraz zmianę orientacji ekranu. (#4574, #4612)
* Nowy język: macedoński.
* Nowe tablice brajlowskie: chorwacki stopień 1, wietnamski stopień 1. (#7565, #7518)
* Dodana obsługa monitora brajlowskiego Actilino produkcji Handy Tech. (#7590)
* Obsługiwane jest wprowadzanie brajla na monitorach Handy Tech. (#7590)

### Zmiany

* Najstarszy system operacyjny obsługiwany przez NVDA to od teraz Windows 7 z Service Pack 1, albo Windows Server 2008 R2 z Service Pack 1. (#7546)
* Okna dialogowe stron www w Firefox i Chrome używają automatycznie trybu czytania, chyba, że znajdują się wewnątrz aplikacji web. (#4493)
* W trybie czytania, przemieszczanie się między elementami przy pomocy tabulatora lub klawiszy szybkiej nawigacji, nie oznajmia wychodzenia z kontenerów, takich jak listy i tabele, co czyni nawigację bardziej efektywną. (#2591)
* W trybie czytania dla Firefox i Chrome, nazwy grup pól formularzy są wypowiadane przy wchodzeniu w ich obręb z użyciem klawiszy szybkiej nawigacji lub tabulatora. (#3321)
* W trybie czytania, komenda szybkiej nawigacji przechodzenia do obiektów zagnieżdżonych (o i shift+o) teraz uwzględnia elementy audio i video oraz elementy z rolami aria application i dialog. (#7239)
* Espeak-ng został zaktualizowany do wersji 1.49.2, co rozwiązuje pewne problemy z wytwarzaniem wydań produkcyjnych. (#7385)
* Po trzecim wywołaniu polecenia odczytania paska stanu, jego zawartość jest kopiowana do schowka. (#1785)
* Przypisując zdarzenia do klawiszy na monitorze Baum, można ograniczyć definicję do konkretnego modelu (np. VarioUltra or Pronto). (#7517)
* Nieprzypisana do klawisza komenda została dodana do trybu czytania, umożliwiająca przełączanie zgłaszania tabel układu treści. Można ją znaleźć w kategorii tryb czytania w oknie zdarzeń wejścia. (#7634)
* Translator brajlowski liblouis zaktualizowany do wersji 3.3.0. (#7565)
* Pliki słownika głosu są wersjonowane i zostały przeniesione do folderu 'speechDicts/voiceDicts.v1'. (#7592)
* Modyfikacje plików wersjonowanych (konfiguracja użytkownika, słowniki głosu) nie są zapisywane, gdy NVDA  jest uruchomiony z pakietu uruchomieniowego. (#7688)
* Monitory Braillino, Bookworm i Modular (ze starą wersją firmware) produkcji Handy Tech, nie są obsługiwane bezpośrednio. Należy zainstalować uniwersalny sterownik Handy Tech i dodatek NVDA, aby używać tych monitorów. (#7590)

### Poprawki błędów

* Linki są identyfikowane w brajlu w aplikacjach takich jak Microsoft Word. (#6780)
* NVDA nie spowalnia zauważalnie, gdy otwarte jest wiele kart w przeglądarkach Firefox lub Chrome. (#3138)
* Przywoływanie kursora na monitorach MDV Lilli Braille nie przesuwa kursora nieprawidłowo o jedną komórkę brajlowską dalej, niż powinien się znaleźć. (#7469)
* W Internet Explorer i innych dokumentach MSHTML, atrybut required języka HTML5 jest obsługiwany dla oznaczenia wymaganego stanu pola formularza. (#7321)
* Monitory brajlowskie są aktualizowane podczas wpisywania znaków arabskich w dokumentach WordPada wyrównanych do lewej (#511).
* Dostępne etykiety kontrolek w Mozilla Firefox są teraz bardziej czytelnie zgłaszane w trybie czytania, gdy sama etykieta nie jest treścią. (#4773)
* W aktualizacji dla twórców windows 10 , NVDA może ponownie uzyskać dostęp do Firefox po restarcie NVDA. (#7269)
* Po restarcie NVDA z Mozilla Firefox w punkcie uwagi, tryb czytania będzie ponownie dostępny, chociaż może być konieczne wyjście i powrót do przeglądarki przy pomocy alt+tab. (#5758)
* Można uzyskać dostęp do treści matematycznej w Google Chrome na systemie bez zainstalowanego Mozilla Firefox. (#7308)
* System operacyjny i aplikacje powinny być bardziej stabilne bezpośrednio po instalacji NVDA, a przed restartem systemu w porównaniu do instalacji wcześniejszych wersji NVDA. (#7563)
* Po użyciu komendy rozpoznawania treści (np. NVDA+r), NVDA zgłosi błąd zamiast milczenia, gdy obiekt nawigacyjny zniknął. (#7567)
* Poprawiona funkcjonalność przewijania wstecz dla monitorów freedom Scientific zawierających lewy pasek ochraniający. (#7713)

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

Najważniejsze zmiany w tej wersji to wprowadzanie brajla skrótami, obsługa nowych głosów Windows OneCore dostępnych w Windows 10, wbudowana obsługa silnika OCR Windows 10, wiele znaczących usprawnień brajla i przeglądania sieci.

### Nowe funkcje

* Dodane ustawienie brajlowskie pokazywania wiadomości w nieskończoność. (#6669)
* Na listach wiadomości Microsoft Outlook, zgłaszane są wiadomości oflagowane. (#6374)
* W Microsoft Powerpoint, zgłaszany jest typ kształtu podczas edycji slajdu (np. trójkąt, okrąg, wideo, strzałka), zamiast informacji 'kształt'. (#7111)
* Treść matematyczna (dostarczona jako MathML) jest obsługiwana w Google Chrome. (#7184)
* NVDA może mówić przy użyciu nowych głosów Windows OneCore (znanych również jako głosy mobilne Windows) zawartych w Windows 10. Dostęp do głosów jest uzyskiwany po wybraniu Głosy Windows OneCore w oknie ustawień syntezatora NVDA. (#6159)
* Pliki konfiguracyjne użytkownika NVDA  mogą być przechowywane w lokalnym folderze aplikacji użytkownika. Jest to włączane poprzez ustawienie rejestru. Więcej w rozdziale 'Parametry systemowe' w podręczniku użytkownika. (#6812)
* W przeglądarkach internetowych, NVDA odczytuje zastępcze wartości dla pól (szczególnie znacznik aria-placeholder jest teraz obsługiwany). (#7004)
* W trybie czytania w Microsoft Word, można nawigować do błędów pisowni przy użyciu szybkiej nawigacji (w i shift+w) (#6942)
* Dodana obsługa kontrolki wyboru daty w ustawieniach spotkań Microsoft Outlook. (#7217)
* Aktualnie wybrana podpowiedź jest odczytywana w polach Do i Kopia w programie Poczta Windows 10, oraz w oknie wyszukiwania Windows 10. (#6241)
* Odtwarzany jest dźwięk oznaczający pojawienie się podpowiedzi w niektórych polach wyszukiwania w Windows 10 (np. ekran startowy, wyszukiwanie ustawień, poczta Windows 10 pola Do i Kopia). (#6241)
* Automatyczne zgłaszanie powiadomień w Skype dla biznesu Desktop, np. gdy ktoś rozpoczyna z tobą konwersację.  (#7281)
* Wiadomości przychodzące na czacie są automatycznie odczytywane podczas konwersacji w Skype dla biznesu. (#7286)
* Automatyczne zgłaszanie powiadomień w Microsoft Edge, np. o rozpoczęciu pobierania.  (#7281)
* Można pisać w brajlu standardowym lub skrótami brajlowskimi na wyświetlaczu brajlowskim z klawiaturą. Więcej w rozdziale o wprowadzaniu brajla w podręczniku użytkownika NVDA. (#2439)
* Można wpisywać znaki unikodu brajlowskiego z klawiatury na monitorze brajlowskim, po wybraniu unikod brajlowski jako tablicy wprowadzania w ustawieniach brajla. (#6449)
* Dodana obsługa monitora brajlowskiego SuperBraille używanego na Tajwanie. (#7352)
* Nowe tablice brajlowskie: duński 8-punktowy brajl komputerowy, litewski, perski 8-punktowy brajl komputerowy, perski stopień 1, słoweński 8 -punktowy brajl komputerowy. (#6188, #6550, #6773, #7367)
* Poprawiona tablica brajlowska angielski (U.S.) 8 -punktowy brajl komputerowy, włączając obsługę punktorów, znaku euro i liter akcentowanych. (#6836)
* NVDA może używać mechanizmu OCR zawartego w Windows 10 aby rozpoznawać tekst obrazów lub niedostępnych aplikacji. (#7361)
 * Język może być ustawiony w nowym oknie Windows 10 OCR w ustawieniach NVDA.
 * Aby rozpoznać treść obiektu nawigacyjnego, naciśnij NVDA+r.
 * Więcejw rozdziale Rozpoznawanie treści w podręczniku użytkownika.
* Możesz wybrać informację kontekstową pokazywaną na monitorze brajlowskim gdy obiekt otrzymuje punkt uwagi przy użyciu nowego ustawienia "kontekst prezentacji punktu uwagi" w ustawieniach brajlowskich. (#217)
 * Przykładowo: opcje "Wypełnij wyświetlacz dla zmian kontekstu" i "Tylko przy przechodzeniu wstecz" mogą poprawić wydajność pracy z listami i menu, ponieważ elementy nie będą stale zmieniać położenia na monitorze.
 * Więcej w rozdziale o ustawieniu "Kontekstowa prezentacja punktu uwagi" w podręczniku użytkownika.
* W Firefox i Chrome, NVDA obsługuje złożone dynamiczne siatki takie jak arkusze kalkulacyjne, w których tylko część treści może być załadowana lub wyświetlana (szczególnie obsługiwane są atrybuty aria-rowcount, aria-colcount, aria-rowindex i aria-colindex  wprowadzone w ARIA 1.1). (#7410)

### Zmiany

* Dodana nieprzypisana komenda umożliwiająca szybki restart NVDA. Można ją znaleźć w kategorii "Różne" okna "Zdarzenia wejścia". (#6396)
* Układ klawiatury może być ustawiony w oknie powitalnym NVDA. (#6863)
* Wiele więcej stanów i typów kontrolek oraz punkty orientacyjne, zostało skrócone w brajlu. Więcej w rozdziale "Skróty typu, stanu kontrolek i punktów orientacyjnych" w podręczniku użytkownika. (#7188, #3975)
* Aktualizacja Espeak-ng do 1.49.1 (#7280).
* Listy tabel wprowadzania i wyjścia w oknie ustawień brajlowskich są teraz posortowane alfabetycznie. (#6113)
* Zaktualizowany translator brajlowski liblouis do 3.2.0. (#6935)
* Domyślną tablicą brajlowską jest teraz ujednolicony brajl angielski stopień 1. (#6952)
* Domyślnie NVDA pokazuje teraz tylko część informacji kontekstowej która zmieniła się na wyświetlaczu brajlowskim, gdy obiekt otrzymuje punkt uwagi. (#217)
 * Poprzednio pokazywane było tyle informacji kontekstowej ile było możliwe, niezależnie od tego, czy użytkownik otrzymał już te same informacje kontekstowe wcześniej.
 * Możesz wrócić do starego zachowania zmieniając nowe ustawienie "Kontekstowa prezentacja punktu uwagi"  w oknie ustawień brajlowskich na "Zawsze wypełnij wyświetlacz".
* Kursor brajlowski może mieć inny kształt przy związaniu z punktem uwagi i punktem przeglądu. (#7112)
* Zaktualizowane logo NVDA. Nowe logo to stylizowana mieszanka białych liter NVDAna stałym fioletowym tle. Zapewnia to dobrą widoczność na każdym tle, oraz nawiązuje do fioletu używanego w logo NV Access. (#7446)

### Poprawki błędów

* Edytowalne elementy div w Chrome nie mają od teraz nazwy zgłaszanej jako wartość w trybie czytania. (#7153)
* Naciśnięcie end w trybie czytania w pustym dokumencie Microsoft Word nie powoduje błędu runtime. (#7009)
* Tryb czytania jest prawidłowo obsługiwany w Microsoft Edge gdy dokument posiada rolę ARIA określoną jako dokument. (#6998)
* W trybie czytania możliwe jest zaznaczanie i odznaczanie do końca linii przy użyciu shift+end nawet, gdy kursor znajduje się na ostatnim znaku linii. (#7157)
* Jeśli okno dialogowe zawiera pasek postępu, tekst dialogu jest aktualizowany po zmianie paska postępu. Oznacza to, że np. pozostały czas może być odczytany w oknie pobierania NVDA. (#6862)
* NVDA oznajmia teraz zmiany zaznaczenia dla niektórych list rozwijanych Windows 10 np. Autoodtwarzanie w ustawieniach. (#6337).
* Bezsensowne informacje nie są od teraz odczytywane po wejściu w tworzenie spotkania w Microsoft Outlook. (#7216)
* Dźwięki powiadomień pasków postępu bez określonego czasu trwania (np. pasek sprawdzania aktualizacji) są generowane tylko gdy ustawienie sygnalizacji pasków postępu ma generować dźwięki. (#6759)
* W Microsoft Excel 2007 i 2003, komórki są znów zgłaszane podczas przechodzenia strzałkami wewnątrz arkusza. (#7243)
* W aktualizacji Windows 10 Creators update i nowszych, zapewnione automatyczne włączanie trybu czytania podczas czytania wiadomości w programie Poczta Windows 10. (#7289)
* Na większości monitorów brajlowskich z klawiaturą, punkt 7 kasuje ostatnio wprowadzony znak lub  komórkę brajlowską, a punkt 8 naciska klawisz Enter. (#6054)
* W tekście edytowalnym, podczas przemieszczania kursora strzałkami i klawiszem Backspace, informacje odczytywane przez NVDA są obecnie bardziej precyzyjne w wielu przypadkach, szczególnie w Chrome i aplikacjach terminalowych. (#6424)
* Odczytywana zawartość edytora sygnatury W Microsoft Outlook 2016. (#7253)
* W aplikacjach Java Swing, NVDA nie powoduje czasem awarii aplikacji podczas nawigowania po tabeli. (#6992)
* W Windows 10 Creators Update, NVDA nie oznajmia wielokrotnie tych samych wyskakujących powiadomień. (#7128)
* W menu start w Windows 10, naciśnięcie Enter aby zamknąć menu startowe po wyszukiwaniu, nie powoduje od teraz odczytania przez NVDA wyszukiwanego tekstu. (#7370)
* Znacząco przyśpieszona szybka nawigacja po nagłówkach w Microsoft Edge. (#7343)
* W Microsoft Edge, nawigacja w trybie czytania nie powoduje pomijania dużych części niektórych stron np. motywu Wordpress 2015. (#7143)
* W Microsoft Edge, punkty orientacyjne są prawidłowo prezentowane w językach innych niż angielski. (#7328)
* Brajl prawidłowo podąża za zaznaczeniem podczas zaznaczania tekstu przekraczającego szerokość monitora. Przykładowo, jeśli zaznaczysz wiele linii przy użyciu shift+strzałka w dół, brajl pokazuje ostatnią zaznaczoną linię. (#5770)
* W Firefox, NVDA nie zgłasza nieprawidłowo kilkukrotnie "sekcja" przy otwieraniu szczegółów tweeta na stronie twitter.com. (#5741)
* Komendy nawigacji po tabeli nie są odtąd dostępne dla tabel układu treści w trybie czytania, chyba, że włączone jest zgłaszanie tabel układu treści. (#7382)
* W Firefox i Chrome, komendy nawigacji po tabeli przeskakują ukryte komórki. (#6652, #5655)

### Changes for Developers

* Timestamps in the log now include milliseconds. (#7163)
* NVDA must now be built with Visual Studio Community 2015. Visual Studio Express is no longer supported. (#7110)
 * The Windows 10 Tools and SDK are now also required, which can be enabled when installing Visual Studio.
 * See the Installed Dependencies section of the readme for additional details.
* Support for content recognizers such as OCR and image description tools can be easily implemented using the new contentRecog package. (#7361)
* The Python json package is now included in NVDA binary builds. (#3050)

## 2017.2

Najważniejsze zmiany w tej wersji to pełna obsługa przyciszania audio w Windows 10 Creators Update; poprawki zaznaczania w trybie czytania, włączając w to problemy z zaznaczaniem wszystkiego; znaczące poprawki obsługi Microsoft Edge; poprawki działania na stronach www, takie jak oznajmianie elementów bieżących (przy użyciu aria-current).

### Nowe funkcje

* Informacja o ramkach komórek może być zgłaszana w Microsoft Excel przy użyciu NVDA+f. (#3044)
* W przeglądarkach NVDA oznajmia, że element został oznaczony jako bieżący (szczególnie przy użyciu atrybutu aria-current). (#6358)
* Obsługa automatycznej zmiany języka w Microsoft Edge. (#6852)
* Obsługa kalkulatora Windows w systemie Windows 10 Enterprise LTSB (Long-Term Servicing Branch) i Server. (#6914)
* Wywołanie trzykrotnie szybko funkcji odczytywania bieżącej linii, literuje linię z użyciem opisów znaków. (#6893)
* Nowy język: birmański.
* Unikod: strzałki w górę i dół oraz symbole ułamka są teraz prawidłowo wypowiadane. (#3805)

### Zmiany

* Podczas nawigacji przy użyciu prostego przeglądu w aplikacjach używających UI Automation, ignorowana jest większa ilość nieistotnych obiektów, co upraszcza nawigację. (#6948, #6950) 

### Poprawki błędów

* Elementy menu stron internetowych mogą teraz być aktywowane w trybie czytania. (#6735)
* Naciśnięcie ESC w oknie profili konfiguracji "Potwierdź usunięcie" zamyka okno. (#6851)
* Naprawiono awarie w Mozilla Firefox i innych aplikacjach bazujących na Gecko,  pojawiające się przy włączonym trybie wieloprocesowym. (#6885)
* Zgłaszanie koloru tła w przeglądzie ekranu jest obecnie dokładniejsze, gdy tekst został narysowany na przezroczystym tle. (#6467) 
* Poprawiona obsługa opisu obiektów w Internet Explorer 11, (szczególnie obsługę atrybutów aria-describedby, obsługę wewnątrz ramek iframe oraz sytuacje, że dostarczono wiele atrybutów ID). (#5784)
* W aktualizacji Windows 10 Creators Update, funkcja NVDA przyciszania audio działa tak jak w poprzednich wydaniach Windows (tj. dostępne są wszystkie tryby: przycisz podczas generowania mowy i dźwięku, zawsze przyciszaj i bez przyciszania). (#6933)
* Naprawiony problem nawigacji NVDA lub zgłaszania niektórych kontrolek (UIA) bez zdefiniowanego klawisza skrótu. (#6779)
* Dwie spacje nie są dodawane do informacji o skrócie klawiszowym dla niektórych kontrolek (UIA). (#6790)
* Niektóre kombinacje klawiszy na monitorach brajlowskich HIMS (np. spacja+punkt 4) nie powodują już sporadycznych problemów. (#3157)
* Naprawiono problem otwierania portu szeregowego na systemach używających niektórych języków innych niż angielski, powodujący niemożność podłączenia się do monitorów brajlowskich w niektórych przypadkach. (#6845)
* Zmniejszona szansa popsucia pliku konfiguracyjnego przy zamykaniu Windows. Pliki konfiguracyjne są zapisywane pod tymczasową nazwą, przed zastąpieniem aktualnego pliku konfiguracji. (#3165)
* Po wywołaniu dwukrotnie szybko funkcji odczytu bieżącej linii aby ją przeliterować, jest używany odpowiedni język. (#6726)
* Nawigacja po liniach w Microsoft Edge jest obecnie 3-krotnie szybsza w systemie Windows 10 Creators Update. (#6994)
* NVDA od teraz nie zgłasza "Web Runtime grouping" przy przejściu punktu uwagi do dokumentów Microsoft Edge w systemie Windows 10 Creators Update (#6948)
* Obsługiwane są wszystkie istniejące wersje SecureCRT. (#6302)
* Adobe Acrobat Reader nie zawiesza się od teraz w niektórych dokumentach PDF (zawierających puste atrybuty ActualText). (#7021, #7034)
* Tryb czytania w Microsoft Edge:  tabele interaktywne (siatki ARIA) nie są przeskakiwane podczas nawigowania do tabel klawiszami t i shift+t. (#6977)
* Tryb czytania: naciśnięcie shift+home po zaznaczeniu w przód teraz zgodnie z oczekiwaniami odznacza do początku linii. (#5746)
* W trybie czytania, komenda "Zaznacz wszystko" (control+a) nie ma od teraz problemów z zaznaczeniem całego tekstu jeśli kursor nie znajdował się na początku. (#6909)
* Naprawiono niektóre inne rzadkie problemy zaznaczania w trybie czytania. (#7131)

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

Najważniejsze zmiany w tej wersji to zgłaszanie sekcji i kolumn tekstu w Microsoft Word; obsługa czytania, nawigacji i komentowania książek w Kindle dla PC; poprawiona obsługa Microsoft Edge.

### Nowe funkcje

* W Microsoft Word mogą być zgłaszane typ podziału sekcji i numer sekcji. Jest to włączane przy pomocy opcji "Zgłaszaj numery stron"  w oknie formatowania dokumentów. (#5946)
* W Microsoft Word kolumny tekstu mogą być zgłaszane. Jest to włączane przy pomocy opcji "Zgłaszaj numery stron"  w oknie formatowania dokumentów. (#5946)
* Automatyczna zmiana języka jest obsługiwana w Wordpad. (#6555)
* Komenda znajdowania w NVDA (NVDA+control+f) jest obsługiwana w trybie czytania w Microsoft Edge. (#6580)
* Szybka nawigacja po przyciskach w trybie czytania (b i shift+b) jest obsługiwana w Microsoft Edge. (#6577)
* Podczas kopiowania arkusza w Microsoft Excel, zapamiętywane są nagłówki kolumn i wierszy. (#6628)
* Obsługa czytania i nawigacji książek  w Kindle dla PC wersja 1.19, włączając w to dostęp do linków, przypisów, grafik, podświetlonego tekstu i notatek użytkownika. Więcej informacji dostępne w rozdziale Kindle dla PC podręcznika NVDA. (#6247, #6638)
* Nawigacja wewnątrz tabel w trybie czytania jest obsługiwana w Microsoft Edge. (#6594)
* W Microsoft Excel, komenda zgłaszania położenia kursora przeglądu (desktop: NVDA+numpadDelete, laptop: NVDA+delete), zgłasza nazwę arkusza i położenie komórki .  (#6613)

### Zmiany

* Minimalna częstotliwość migotania kursora brajla to obecnie 200ms. Niższe wartości tego ustawienia zostaną podniesione do 200ms. (#6470)
* Pole wyboru zostało dodane do ustawień brajla, pozwalające włączyć lub wyłączyć migotanie kursora brajlowskiego. Poprzednio wartość zero była używana, aby to osiągnąć. (#6470)
* Zaktualizowany eSpeak NG (commit e095f008, 10 stycznia 2017). (#6717)
* W związku ze zmianami w Windows 10 Creators Update, tryb 'zawsze przyciszaj' został usunięty z ustawienia przyciszania audio w NVDA. Jest on nadal dostępny w starszych wydaniach Windows 10. (#6684)
* W związku ze zmianami w Windows 10 Creators Update, tryb 'Przycisz podczas generowania mowy i dźwięku' nie może stwierdzić, czy audio zostało w pełni przyciszone przed rozpoczęciem mowy, ani utrzymać dźwięk przyciszony na wystarczająco długi czas do zakończenia wypowiedzi.  Te zmiany nie wpływają na starsze wydania windows 10. (#6684)

### Poprawki błędów

* Naprawione zawieszenie w Microsoft Word podczas przechodzenia akapitami w dużym dokumencie przy włączonym trybie czytania. (#6368)
* W Microsoft Word tabele skopiowane z Microsoft Excel nie są od teraz pomijane jako tabele układu treści. (#5927)
* W Microsoft Excel próba wpisywania w widoku chronionym sprawia, że NVDA generuje dźwięk zamiast wypowiadać znaki, które nie zostały wpisane. (#6570)
* Naciśnięcie escape w Microsoft Excel nie przełącza błędnie do trybu czytania, chyba że użytkownik wcześniej włączył tryb czytania klawiszami NVDA+space, a następnie przeszedł do trybu formularzy naciskając Enter na kontrolce. (#6569) 
* NVDA nie zawiesza się w arkuszach Microsoft Excel , w których cała linia lub kolumna jest połączona. (#6216)
* Zgłaszanie przepełnienia lub przyciętego tekstu w komórkach Microsoft Excel powinno być teraz bardziej dokładne. (#6472)
* NVDA zgłasza pola wyboru tylko do odczytu. (#6563)
* Program uruchamiający NVDA nie będzie pokazywał okna ostrzeżenia, gdy nie może odtworzyć dźwięku logo z powodu braku dostępnego urządzenia audio. (#6289)
* Niedostępne kontrolki wstążki Microsoft Excel są teraz odpowiednio zgłaszane. (#6430)
* NVDA nie będzie zgłaszał "panel" podczas minimalizacji okien. (#6671)
* Odczytywane są wpisywane znaki w aplikacjach uniwersalnej platformy Windows (UWP) (włączając w to Microsoft Edge) w Windows 10 Creators Update. (#6017)
* Śledzenie myszy działa na wszystkich ekranach na komputerach z wieloma monitorami. (#6598)
* NVDA od teraz nie staje się bezużyteczny po wyjściu z Windows Media Player , gdy punkt uwagi znajdował się na suwaku. (#5467)

### Changes for Developers

* Profiles and configuration files are now automatically upgraded to meet the requirements of schema modifications. If there is an error during upgrade, a notification is shown, the configuration is reset and the old configuration file is available in the NVDA log at 'Info' level. (#6470)

## 2016.4

Najważniejsze zmiany w tej wersji to poprawiona obsługa Microsoft Edge; tryb czytania w aplikacji Poczta systemu Windows 10; istotne poprawki okien NVDA.

### Nowe funkcje

* NVDA może oznajmiać wcięcia linii przy użyciu dźwięków. Może to być ustawione na liście "Oznajmiaj wcięcia linii" w ustawieniach formatowania dokumentów NVDA. (#5906)
* Obsługa monitora brajlowskiego Orbit Reader 20. (#6007)
* Dodana opcja automatycznego otwierania okna podglądu mowy przy starcie NVDA. Może zostać włączona przez pole wyboru w oknie podglądu mowy. (#5050)
* Przy ponownym otwieraniu podglądu mowy, przywracane są rozmiary i położenie okna. (#5050)
* Pola odsyłacza w Microsoft Word są teraz traktowane jak hiperlinki. Są zgłaszane jako linki, i mogą być aktywowane. (#6102)
* Obsługa monitorów brajlowskich Baum SuperVario2, Baum Vario 340 i HumanWare Brailliant2. (#6116)
* Wstępna obsługa rocznicowej aktualizacji Microsoft Edge. (#6271)
* Tryb czytania jest teraz używany podczas czytania poczty w aplikacji Windows 10 mail. (#6271)
* Nowy język: litewski.

### Zmiany

* Zaktualizowany translator brajlowski liblouis do wersji 3.0.0. Zawiera znaczne zmiany ujednoliconego brajla angielskiego. (#6109, #4194, #6220, #6140)
* W managerze dodatków, przyciski włączania i wyłączania dodatków mają klawisze skrótu (w polskiej wersji językowej, klawisze te były zdefiniowane już dawniej). (#6388)
* Naprawiono różne problemy rozmieszczenia i wyrównania elementów w oknach dialogowych NVDA. (#6317, #5548, #6342, #6343, #6349)
* W oknie ustawień formatowania dokumentów, treść się przewija. (#6348)
* Naprawione okno wymowy symboli, aby cała szerokość okna była używana dla listy symboli. (#6101)
* W trybie czytania w przeglądarkach internetowych, komendy literowej nawigacji do pól edycji (e i shift+e) i pól formularza (f i shift+f) uwzględniają także pola edycji tylko do odczytu. (#4164)
* w oknie ustawień formatowania dokumentów NVDA, opcja "Oznajmiaj zmiany edycyjne za kursorem" została zmieniona na "zgłaszaj zmiany formatowania za kursorem", ponieważ dotyczy brajla, a nie tylko mowy. W polskiej wersji językowej, nowa nazwa tej opcji istniała już dawniej. (#6336)
* Poprawiony wizualny układ powitalnego okna dialogowego NVDA. (#6350)
* Okna dialogowe NVDA mają teraz przyciski "ok" i "Anuluj" wyrównane do prawej strony okna. (#6333)
* Pokrętła są teraz używane do wprowadzania wartości pól numerycznych takich jak procentowa zmiana tonu dla dużych liter w oknie ustawień głosu. (#6099)
* Ujednolicony między różnymi przeglądarkami sposób zgłaszania elementów IFrame (dokumentów zagnieżdżonych wewnątrz innych dokumentów). W przeglądarce Firefox, iframe są zgłaszane jako "Ramka". (#6047)

### Poprawki błędów

* Poprawiony rzadki problem przy wyjściu z NVDA, gdy otwarty był podgląd mowy. (#5050)
* Mapy obrazkowe są teraz renderowane zgodnie z oczekiwaniami w trybie czytania w Mozilla Firefox. (#6051)
* W oknie słownika, naciśnięcie klawisza Enter zapisuje zmiany i zamyka okno. (#6206)
* Wyświetlane komunikaty w brajlu przy zmianie trybów wprowadzania dla metody wprowadzania (wprowadzanie narodowe /alfanumeryczne, pełnokształtowe/półkształtowe, etc.). (#5892, #5893)
* Po wyłączeniu i natychmiastowym ponownym włączeniu wtyczki lub odwrotnie, status wtyczki prawidłowo zmienia się na poprzedni. (#6299)
* W Microsoft Word, pola numerów stron w nagłówku mogą być odczytywane. (#6004)
* Mysz może być użyta do zmiany punktu uwagi między listą symboli i polami edycyjnymi w oknie wymowy symboli. (#6312)
* Poprawiono błąd blokujący pojawienie się listy elementów w trybie czytania, gdy Microsoft Word zawierał nieprawidłowe łącze. (#5886)
* Po zamknięciu podglądu mowy z paska zadań lub klawiszem alt+F4, pole wyboru statusu podglądu mowy w menu NVDA  będzie odzwierciedlać aktualną widoczność okna. (#6340)
* Komenda przeładowania wtyczek nie powoduje dłużej problemów z wyzwalaczami profili konfiguracji, nowym dokumentem w przeglądarkach internetowych i przeglądem ekranu. (#2892, #5380)
* Na liście języków w oknie ustawień ogólnych NVDA, języki takie jak aragoński są teraz poprawnie wyświetlane w Windows 10. (#6259)
* Emulowane klawisze systemowe (np. przycisk na monitorze brajlowskim, który emuluje naciśnięcie klawisza tab) są teraz prezentowane w wybranym języku NVDA w pomocy klawiatury i oknie zdarzeń wejścia. Poprzednio były zawsze wyświetlane po angielsku. (#6212)
* Zmiana języka w ogólnych ustawieniach NVDA odnosi skutek dopiero po restarcie programu. (#4561)
* Pole wzorca dla nowego wpisu słownika nie może być pozostawione puste. (#6412)
* Naprawiono rzadki błąd skanowania portów szeregowych na niektórych systemach, sprawiający, że sterownik monitora brajlowskiego nie mógł być używany. (#6462)
* W Microsoft Word, numerowane punktory są teraz odczytywane w komórkach tabeli, podczas przemieszczania się o komórkę. (#6446)
* Można przypisywać zdarzenia wejścia  do poleceń dla sterownika monitora brajlowskiego Handy Tech  w oknie zdarzeń wejścia NVDA. (#6461)
* W Microsoft Excel, naciśnięcie enter lub numpadEnter podczas nawigacji w arkuszu, teraz prawidłowo  zgłasza nawigację do następnego wiersza. (#6500)
* iTunes  nie zawiesza się na zawsze podczas używania trybu czytania  w sklepie iTunes, Apple Music, etc. (#6502)
* Poprawiono awarie w 64-bitowych aplikacjach   Mozilla i bazujących na Chrome. (#6497)
* W Firefox z włączoną wieloprocesowością, tryb czytania i edytowalne pola tekstowe teraz działają prawidłowo. (#6380)

### Changes for Developers

* It is now possible to provide app modules for executables containing a dot (.) in their names. Dots are replaced with underscores (_). (#5323)
* The new gui.guiHelper module includes utilities to simplify the creation of wxPython GUIs, including automatic management of spacing. This facilitates better visual appearance and consistency, as well as easing creation of new GUIs for blind developers. (#6287)

## 2016.3

Najważniejsze zmiany w tej wersji to możliwość wyłączania pojedynczych dodatków; obsługa pól formularzy w Microsoft Excel; znaczące ulepszenia zgłaszania kolorów; poprawki dotyczące kilku monitorów brajlowskich; poprawki obsługi Microsoft Word.

### Nowe funkcje

* Tryb czytania może teraz być używany do odczytu dokumentów PDF w Microsoft Edge w rocznicowej aktualizacji Windows 10. (#5740)
* Przekreślenie i podwójne przekreślenie są odczytywane  w razie potrzeby w Microsoft Word. (#5800)
* W Microsoft Word odczytywany jest tytuł tabeli jeśli jest zdefiniowany. Jeżeli istnieje opis, można go odczytać przy pomocy komendy otwarcia długiego opisu (NVDA+d) w trybie czytania. (#5943)
* W Microsoft Word, NVDA zgłasza informację o położeniu podczas przenoszenia paragrafów (alt+shift+strzałka w dół i alt+shift+strzałka w górę). (#5945)
* Microsoft Word: zgłaszana jest interlinia poprzez komendę NVDA odczytaj formatowanie, oraz automatycznie, jeśli włączona jest opcja w ustawieniach formatowania dokumentów NVDA - przy zmianie interlinii klawiszami skrótu Microsoft word, oraz przy przejściu do tekstu o innej interlinii. (#2961)
* Internet Explorer:  rozpoznawane są strukturalne elementy HTML 5. (#6044)
* Odczytywanie komentarzy (takich jak w Microsoft Word) może teraz być wyłączone przy pomocy opcji "Czytaj komentarze" w ustawieniach formatowania dokumentów NVDA. (#5108)
* Możliwe jest teraz wyłączanie pojedynczych dodatków w managerze dodatków. (#3090)
* Dodatkowe przypisania klawiszy zostały dodane do monitorów brajlowskich serii ALVA BC640/680. (#5206)
* Dodana komenda przeniesienia monitora brajlowskiego do punktu uwagi. Obecnie, tylko monitory serii ALVA BC640/680 mają klawisz przypisany do tej komendy, ale może to zostać zdefiniowane ręcznie dla dowolnego monitora  brajlowskiego w oknie zdarzeń wejścia. (#5250)
* W Microsoft Excel, można nawigować po polach formularzy. Przejście do pola formularza możliwe jest przy pomocy listy elementów, albo nawigacji literami w trybie czytania. (#4953)
* Można przypisać zdarzenie wejścia do przełączania trybu prostego przeglądu przy pomocy okna zdarzeń wejścia. (#6173)

### Zmiany

* NVDA zgłasza teraz kolory przy użyciu podstawowego, dobrze rozumianego zestawu 9 odcieni kolorów i 3 cieni ze zmianami jasności i bladości. Zastępuje to bardziej subiektywne i mniej rozumiane nazwy kolorów. (#6029)
* Zmienione zachowanie NVDA+F9 a następnie NVDA+F10: teraz zaznacza tekst po pierwszym naciśnięciu F10. Po kolejnym naciśnięciu F10 w krótkim odstępie czasowym, tekst jest kopiowany do schowka . (#4636)
* Zaktualizowany eSpeak NG do wersji Master 11b1a7b (22 czerwiec 2016). (#6037)

### Poprawki błędów

* Kopiowanie do schowka w trybie czytania w Microsoft Word, zachowuje formatowanie. (#5956)
* W Microsoft Word, NVDA informuje prawidłowo o użyciu poleceń Worda nawigacji w tabeli (alt+home, alt+end, alt+pageUp i alt+pageDown) i komend zaznaczania tabeli (shift z klawiszami skrótu nawigacji). (#5961)
* W oknach dialogowych Microsoft Word, znacząco poprawiona nawigacja w chierarchii obiektów NVDA. (#6036)
* W niektórych aplikacjach takich jak Visual Studio 2015, klawisze skrótu (np. control+c dla skopiowania) są teraz odczytywane. (#6021)
* Poprawiono rzadki błąd skanowania portów szeregowych na niektórych systemach, który powodował bezużyteczność niektórych sterowników monitorów brajlowskich. (#6015)
* Zgłaszanie kolorów w Microsoft Word jest teraz dokładniejsze, ponieważ uwzględnia zmiany powodowane przez motywy Microsoft Office. (#5997)
* W kompilacjach Windows 10  po kwietniu 2016, ponownie dostępny jest tryb czytania Microsoft Edge i wsparcie dla sugestii wyszukiwania na ekranie startowym. (#5955)
* W Microsoft Word, automatyczny odczyt nagłówków tabeli  radzi sobie lepiej z połączonymi komórkami. (#5926)
* W aplikacji Poczta systemu Windows 10, NVDA nie ma od teraz problemów z odczytaniem treści wiadomości. (#5635) 
* przy włączonym oznajmianiu klawiszy poleceń, stan klawiszy przełącznikowych takich jak caps lock, nie jest anonsowany podwójnie. (#5490)
* Okna kontroli konta użytkownika Windows są ponownie odczytywane prawidłowo w aktualizacji rocznicowej Windows 10. (#5942)
* We wtyczce konferencji web (takiej jak używana na stronie out-of-sight.net), NVDA od teraz nie generuje dźwięków i nie wypowiada pasków postępu związanych z wejściem mikrofonu. (#5888)
* W trybie czytania, wykonanie polecenia znajdź poprzedni lub znajdź następny, prawidłowo wykona poszukiwanie z uwzględnieniem wielkości liter, jeżeli pierwsze wyszukiwanie uwzględniało wielkość liter. (#5522)
* Podczas edycji wpisów słownika, dostarczana jest informacja zwrotna dla nieprawidłowych wyrażeń regularnych. NVDA nie zawiesza się, jeżeli plik słownika zawiera nieprawidłowe wyrażenie regularne. (#4834)
* Jeśli NVDA nie może się komunikować z monitorem brajlowskim (np. ponieważ został odłączony), automatycznie wyłączy używanie monitora. (#1555)
* Nieznacznie poprawiona wydajność filtrowania listy elementów trybu czytania w niektórych sytuacjach. (#6126)
* W Microsoft Excel, nazwy wzorców tła zgłaszane przez NVDA, teraz zgadzają się z nazwami używanymi przez Excel. (#6092)
* Poprawiona obsługa ekranu logowania Windows 10, włącznie z oznajmianiem alertów i aktywowaniem pola hasła przy użyciu dotyku . (#6010)
* NVDA poprawnie wykrywa dodatkowe przyciski routingu w monitorach brajlowskich serii ALVA BC640/680. (#5206)
* NVDA ponownie może zgłaszać wyskakujące powiadomienia Windows w najnowszych kompilacjach Windows 10. (#6096)
* Rozwiązany zdarzający się czasem problem, że NVDA nie rozpoznawał naciśnięć klawiszy na monitorach brajlowskich kompatybilnych z Baum i HumanWare Brailliant B. (#6035)
* Jeśli włączone jest zgłaszanie numerów linii w ustawieniach formatowania dokumentów NVDA, numery linii są pokazywane na monitorze brajlowskim. (#5941)
* W trybie komunikacji bez mowy, odczyt obiektów (np. po naciśnięciu NVDA+tab aby odczytać punkt uwagi) teraz pojawia się w podglądzie mowy. (#6049)
* Na liście wiadomości  Outlook 2016,  informacja o powiązanym szkicu nie jest od teraz zgłaszana. (#6219)
* W Google Chrome i przeglądarkach bazujących na Chrome w językach innych niż angielski, tryb czytania nie zawodzi w wielu dokumentach. (#6249)

### Changes for Developers

* Logging information directly from a property no longer results in the property  being called recursively over and over again. (#6122)

## 2016.2.1

To wydanie naprawia awarie Microsoft Word:

* NVDA nie powoduje awarii Microsoft Word zdarzających się od razu po starcie w Windows XP. (#6033)
* Usunięte zgłaszanie błędów gramatycznych, które powodowało awarie Microsoft Word. (#5954, #5877)

## 2016.2

Najważniejsze zmiany w tej wersji to możliwość zgłaszania błędów pisowni podczas wpisywania; obsługa zgłaszania błędów gramatycznych w Microsoft Word; poprawki obsługi Microsoft Office.

### Nowości

* W trybie czytania w Internet Explorer i innych kontrolkach MSHTML, używanie nawigacji literami aby przejść do adnotacji (a i shift+a) teraz przemieszcza do wstawionego i usuniętego tekstu. (#5691)
* W Microsoft Excel, NVDA zgłasza teraz poziom grupy komórek, oraz informacje, czy są rozwinięte czy zwinięte. (#5690)
* Dwukrotne naciśnięcie komendy odczytania formatowania tekstu (NVDA+f), prezentuje informacje w trybie czytania, więc mogą być łatwo przejrzane. (#4908)
* W Microsoft Excel 2010 i nowszych, cieniowanie komórki i wypełnienie gradientowe są teraz zgłaszane. Automatyczne ogłaszanie jest kontrolowane przez opcję sygnalizuj kolory w ustawieniach formatowania dokumentów NVDA. (#3683)
* Nowa tablica brajlowska: Greka koine. (#5393)
* W podglądzie logów, możesz teraz zapisać log używając klawisza control+s. (#4532)
* Gdy włączone jest informowanie o błędach pisowni i jest  obsługiwane przez kontrolkę z punktem uwagi, NVDA wygeneruje dźwięk ostrzegawczy aby poinformować o błędzie przy wpisywaniu. Można to wyłączyć nową opcją "Odtwarzaj dźwięk przy błędach pisowni podczas wpisywania" w oknie ustawień klawiatury NVDA. (#2024)
* Błędy gramatyczne są teraz zgłaszane w Microsoft Word. Można to wyłączyć przy użyciu nowej opcji "Zgłaszaj błędy gramatyczne"  w oknie ustawień formatowania dokumentów NVDA. (#5877)

### Zmiany

* W trybie czytania i polach edycji, NVDA traktuje teraz numpad Enter tak samo jak główny klawisz enter. (#5385)
* NVDA używa teraz syntezatora eSpeak NG. (#5651)
* W Microsoft Excel, NVDA nie ignoruje nagłówka kolumny dla komórek oddzielonych pustą linią od nagłówków. (#5396)
* W Microsoft Excel, współrzędne są oznajmiane przed nagłówkami dla uniknięcia dwuznaczności między nagłówkami i treścią. (#5396)

### Poprawki błędów

* W trybie czytania, podczas próby użycia nawigacji literami aby przejść do elementu, który nie jest obsługiwany dla dokumentu, NVDA zgłasza, że nie jest to obsługiwane, zamiast informacji, że nie ma elementu w wybranym kierunku. (#5691)
* Lista elementów w trybie arkuszy Microsoft Excel, wyświetla również arkusze zawierające tylko wykresy. (#5698)
* NVDA nie zgłasza teraz nadmiarowych informacji podczas przełączania okien w wielookienkowych aplikacjach Java takich jak IntelliJ lub Android Studio. (#5732)
* W edytorach bazujących na silniku Scintilla takich jak Notepad++, brajl jest prawidłowo aktualizowany podczas przemieszczania kursora przy użyciu monitora brajlowskiego. (#5678)
* NVDA od teraz nie zawiesza się czasami podczas włączania wyświetlania na monitorze brajlowskim. (#4457)
* W Microsoft Word, wcięcie akapitu jest zawsze zgłaszane w jednostkach miary wybranych przez użytkownika (np. centymetrach lub calach). (#5804)
* Wiele komunikatów NVDA, które dawniej były tylko wypowiadane, jest teraz prezentowanych również na monitorze brajlowskim, jeśli używany. (#5557)
* W dostępnych aplikacjach Java, zgłaszany jest poziom elementów drzewa. (#5766)
* Naprawione przypadki zawieszania się NVDA w Adobe Flash w Mozilla Firefox. (#5367)
* W Google Chrome i przeglądarkach bazujących na Chrome, dokumenty w oknach dialogowych lub aplikacjach mogą być odczytywane w trybie czytania. (#5818)
* W Google Chrome i przeglądarkach bazujących na Chrome, możesz zmusić NVDA do przejścia w tryb czytania w sieciowych oknach dialogowych lub aplikacjach. (#5818)
* W Internet Explorer i innych kontrolkach MSHTML, przesunięcie punktu uwagi do niektórych kontrolek (szczególnie takich, gdzie użyty jest aria-activedescendant) nie przełącza nieprawidłowo do trybu czytania. Miało to miejsce np. podczas przejścia do podpowiedzi w polach adresowych w trakcie tworzenia wiadomości w Gmail. (#5676)
* W Microsoft Word, NVDA nie zawiesza się w dużych tabelach przy włączonym zgłaszaniu nagłówków tabel. (#5878)
* W Microsoft word, NVDA nie zgłasza nieprawidłowo jako nagłówek tekstu z poziomem konspektu (ale nie wbudowanym stylem nagłówka). (#5186)
* W trybie czytaniaW Microsoft Word, komendy przejścia do początku i końca kontenera (przecinek i Shift+przecinek) działają teraz dla tabel. (#5883)

### Changes for Developers

* NVDA's C++ components are now built with Microsoft Visual Studio 2015. (#5592)
* You can now present a text or HTML message to the user in browse mode using ui.browseableMessage. (#4908)
* In the User Guide, when a <!-- KC:setting command is used for a setting which has a common key for all layouts, the key may now be placed after a full-width colon (：) as well as the regular colon (:). (#5739) -->

## 2016.1

Najważniejsze zmiany w tej wersji to opcjonalna możliwość zmniejszenia głośności innych dźwięków; ulepszone wyświetlanie brajla i obsługa monitorów brajlowskich; kilka znaczących poprawek obsługi  Microsoft Office; poprawki trybu czytania w iTunes.

### Nowości

* Nowe tablice brajlowskie: polski 8-punktowy brajl komputerowy, mongolski. (#5537, #5574)
* Można wyłączyć kursor brajlowski, albo zmienić jego kształt, używając nowych opcji pokazywania kursora i kształtu kursora, znajdujących się w oknie ustawień brajla. (#5198)
* NVDA może się łączyć z monitorem brajlowskim HIMS Smart Beetle przez Bluetooth. (#5607)
* NVDA może opcjonalnie zmniejszać głośność innych dźwięków, gdy zainstalowane na Windows 8 i nowszych. Może to być ustawione przy użyciu opcji trybu przyciszania audio w oknie ustawień syntezatora NVDA, lub przez naciśnięcie NVDA+shift+d. (#3830, #5575)
* Wsparcie dla APH Refreshabraille w trybie HID, Baum VarioUltra i Pronto! połączonych przez USB. (#5609)
* Wsparcie monitorów brajlowskich HumanWare Brailliant BI/B, gdy protokół jest ustawiony na OpenBraille. (#5612)

### Zmiany

* Zgłaszanie podkreślenia jest teraz domyślnie wyłączone. (#4920)
* Zaktualizowany translator brajlowski liblouis do  wersji 2.6.5. (#5574)
* Słowo "tekst" nie jest ogłaszane, gdy punkt uwagi, albo punkt przeglądu zostanie przesunięty na obiekt tekstowy. (#5452)

### Poprawki błędów

* W iTunes 12, tryb czytania jest prawidłowo aktualizowany, gdy nowa strona zostanie załadowana w iTunes Store. (#5191)
* W Internet Explorer i innych kontrolkach MSHTML, przechodzenie do nagłówków określonego poziomu przy pomocy nawigacji pojedynczymi literami  teraz działa prawidłowo, gdy poziom nagłówka został nadpisany dla potrzeb dostępności (szczególnie, gdy aria-level nadpisuje poziom elementu h). (#5434)
* W Spotify, rozwiązany problem częstego lądowania punktu uwagi na obiektach "nieznane". (#5439)
* Punkt uwagi jest prawidłowo przywracany podczas powrotu do Spotify z innej aplikacji. (#5439)
* Podczas przełączania trybu czytania i trybu formularzy, aktualny tryb jest zgłaszany brajlem i mową. (#5239)
* Przycisk Start na pasku zadań nie jest od teraz zgłaszany jako lista lub jako zaznaczony w niektórych wersjach Windows. (#5178)
* Komunikaty takie jak "wstawione" nie są od teraz zgłaszane podczas edycji wiadomości w Microsoft Outlook. (#5486)
* Podczas używania monitora brajlowskiego, gdy tekst w bieżącej linii jest zaznaczony, (np. przy wyszukiwaniu w edytorze tekstu, gdy poszukiwany ciąg znajduje się w tej samej linii), wyświetlany na linijce tekst zostanie przesunięty, jeśli będzie to konieczne. (#5410)
* NVDA od teraz nie zamyka się, gdy konsola wiersza poleceń Windows zostanie zamknięta klawiszami alt+f4 w Windows 10. (#5343)
* Na liście elementów trybu czytania, gdy zmieniono typ elementu, pole filtra jest teraz czyszczone. (#5511)
* W tekstach edytowalnych aplikacji Mozilla, przesuwanie myszy powoduje odczyt odpowiedniej linii, słowa, etc. zamiast całej treści. (#5535)
* Podczas przesuwania myszy w tekstach edytowalnych aplikacji Mozilla, odczyt nie jest od teraz zatrzymywany na elementach takich jak linki, które znajdują się wewnątrz odczytywanego słowa, lub linii. (#2160, #5535)
* W Internet Explorer, strona shoprite.com może być odczytywana w trybie czytania i nie jest zgłaszana jako pusta. (Nieprawidłowo zdefiniowane atrybuty lang są obsługiwane.) (#5569)
* W Microsoft Word, śledzone zmiany takie jak "wstawione" nie są zgłaszane, gdy śledzenie zmian nie jest wyświetlane. (#5566)
* Gdy punkt uwagi znajduje się na przycisku przełączającym, NVDA zgłasza, gdy zmieni się z wciśnięte na niewciśnięte. (#5441)
* Ogłaszanie zmiany kształtu wskaźnika myszy ponownie działa zgodnie z oczekiwaniami. (#5595)
* Przy odczytywaniu wcięcia linii, twarde spacje są traktowane jak normalne. Poprzednio mogło to powodować ogłaszanie "spacja spacja spacja" zamiast "3 spacja". (#5610)
* Przy zamykaniu nowszej metody wprowadzania listy kandydatów, punkt uwagi prawidłowo wraca do pola kompozycji, lub dokumentu. (#4145)
* W Microsoft Office 2013 i nowszych, gdy wstążka jest ustawiona na pokazywanie tylko zakładek, elementy wstążki są prawidłowo odczytywane, gdy zakładka jest aktywowana. (#5504)
* Poprawki i ulepszenia wykrywania  i przypisywania gestów na ekranach dotykowych. (#5652)
* Pojedyncze dotknięcia ekranu dotykowego nie są od teraz zgłaszane w trybie pomocy. (#5652)
* Rozwiązany problem braku na liście elementów komentarzy, które znajdowały się na połączonych komórkach Excel. (#5704)
* Naprawiony bardzo rzadki problem, że NVDA nie odczytywało zawartości arkusza Excel przy włączonym odczytywaniu nagłówków tabeli. (#5705)
* W Google Chrome, nawigacja we wprowadzaniu kompozycji dla znaków wschodnio-azjatyckich  nie powoduje teraz błędu. (#4080)
* Podczas wyszukiwania w Apple Music w iTunes, tryb czytania dla dokumentu wyników wyszukiwania jest aktualizowany zgodnie z oczekiwaniami. (#5659)
* W Microsoft Excel, naciśnięcie shift+f11 aby utworzyć nowy arkusz, zgłasza teraz nową pozycję. (#5689)
* Naprawione problemy z wyświetlaniem brajla na monitorach brajlowskich, podczas wprowadzania znaków koreańskich. (#5640)

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

Najważniejsze zmiany w tej wersji to poprawki wydajności w Windows 10; obecność NVDA w centrum ułatwień dostępu Windows 8 i nowszych; zmiany w Microsoft Excel w tym lista i zmiana nazw arkuszy oraz dostęp do zablokowanych komórek w zabezpieczonych arkuszach;  obsługa edycji tekstu sformatowanego w Mozilla Firefox, Google Chrome i Mozilla Thunderbird.

### Nowości

* NVDA  pojawia się w Centrum ułatwień dostępu Windows 8 i nowszych. (#308)
* Przy przemieszczaniu się między komórkami Excel, zmiany formatowania są teraz automatycznie zgłaszane, jeśli odpowiednie opcje są włączone w ustawieniach formatowania dokumentów NVDA. (#4878)
* Opcja zgłaszania podkreślenia została dodana w ustawieniach formatowania dokumentów NVDA. Domyślnie włączona, pozwala automatycznie powiadamiać o istnieniu podkreślonego tekstu. Aktualnie działa to dla znaczników em i strong w trybie czytania w Internet Explorer i innych kontrolkach MSHTML. (#4920)
* Istnienie wstawionego i usuniętego tekstu jest zgłaszane w trybie czytania w Internet Explorer i innych kontrolkach MSHTML, jeśli zgłaszanie zmian edycyjnych jest włączone w NVDA. (#4920)
* Podczas przeglądania zmian edycyjnych na liście elementów NVDA w Microsoft Word, zgłaszane jest więcej informacji, takich jak informacje o zmienionych właściwościach formatowania. (#4920)
* Microsoft Excel: wyświetlanie listy arkuszy i zmiana nazwy arkusza jest możliwe na liście elementów (NVDA+f7). (#4630, #4414)
* Można teraz ustawić, czy symbole są przesyłane do syntezatorów mowy (np. aby spowodować pauzę lub zmianę intonacji) w ustawieniach wymowy symboli. (#5234)
* Microsoft Excel: NVDA odczytuje wiadomości wprowadzania ustawione przez autora arkuszana komórkach. (#5051)
* Obsługa monitorów brajlowskich Baum Pronto! V4 i VarioUltra połączonych przez bluetooth. (#3717)
* Wsparcie edycji tekstu sformatowanego w aplikacjach Mozilla,  np. dokumenty Google z włączoną obsługą brajla w Firefox,   albo kompozycja HTML w Mozilla Thunderbird. (#1668)
* Wsparcie edycji tekstu sformatowanego w Google Chrome i przeglądarkach bazujących na Chrome, np. Google Docs z włączoną obsługą brajla. (#2634)
 * Wymagane Chrome wersja 47 lub nowsza.
* W trybie przeglądania w Microsoft Excel, można przejść do zablokowanych komórek w zabezpieczonych arkuszach. (#4952)

### Zmiany

* W ustawieniach formatowania dokumentów, opcja zgłaszania zmian edycyjnych jest domyślnie włączona. (#4920)
* Podczas przechodzenia po znaku w Microsoft Word przy włączonej opcji zgłaszania zmian edycyjnych w NVDA, mniej informacji o zmianach jest czytane, co czyni nawigację bardziej wydajną. Aby przejrzeć dodatkowe informacje, użyj listy elementów. (#4920)
* Zaktualizowany translator brajlowski liblouis do  wersji 2.6.4. (#5341)
* Kilka symboli (włączając w to podstawowe symbole matematyczne) zostało przeniesione na poziom niektóre, więc są odczytywane domyślnie. (#3799)
* Pauzy powinny pojawiać się przy czytaniu znaków nawiasów i półpauzy (–) jeśli syntezator to obsługuje. (#3799)
* Podczas zaznaczania tekstu, tekst jest odczytywany przed informacją o zaznaczaniu, zamiast po. (#1707)

### Poprawki błędów

* Poprawa wydajności podczas nawigowania na liście wiadomości Outlook 2010/2013. (#5268)
* Na wykresie Microsoft Excel, działa teraz prawidłowo nawigacja niektórymi klawiszami (np. zmiana arkuszy przy użyciu control+pageUp i control+pageDown). (#5336)
* Poprawiony wygląd przycisków w oknie ostrzeżenia przy cofaniu do starszej wersji NVDA. (#5325)
* W Windows 8 i nowszych, jeśli włączone jest uruchamianie NVDA po zalogowaniu do Windows, NVDA uruchamia się dużo szybciej. (#308)
 * Jeśli Automatyczne uruchamianie po zalogowaniu było włączone w starszej wersji NVDA, trzeba to wyłączyć i włączyć ponownie w ustawieniach ogólnych, aby zmiana stała się zauważalna. Wykonaj następujące czynności:
  1. Otwórz Ustawienia ogólne NVDA.
  1. Odznacz pole wyboru "Uruchom NVDA po zalogowaniu do Windows".
  1. Naciśnij przycisk OK.
  1. Ponownie otwórz Ustawienia ogólne NVDA.
  1. Zaznacz pole wyboru "Uruchom NVDA po zalogowaniu do Windows".
  1. Naciśnij przycisk OK.
* Poprawki wydajności UI Automation, zauważalne w eksploratorze plików i podglądzie zadań. (#5293)
* NVDA teraz prawidłowo przełącza się do trybu formularzypo przejściu tabem do kontrolki tylko do czytania typu grid ARIA w trybie czytania w Mozilla Firefox i innych kontrolkach bazujących na Gecko. (#5118)
 * NVDA teraz prawidłowo czyta "brak poprzedniego" zamiast "brak następnego" gdy nie ma więcej obiektów podczas machania w lewo na ekranie dotykowym.
* Rozwiązane problemy po wpisaniu kilku słów do pola filtru w oknie zdarzeń wejścia. (#5426)
* NVDA nie zawiesza się w niektórych sytuacjach, podczas wznawiania połączenia przez USB z monitorami serii HumanWare Brailliant BI/B . (#5406)
* W językach z połączonymi znakami, opisy znaków działają zgodnie z oczekiwaniem dla wielkich liter angielskich. (#5375)
* NVDA nie powinien się teraz sporadycznie zawieszać przy otwieraniu menu start w Windows 10. (#5417)
* W Skype dla pulpitu odczytywane są  powiadomienia wyświetlane zanim zniknie poprzednie powiadomienie. (#4841)
* Powiadomienia są prawidłowo odczytywane w Skype dla pulpitu 7.12 i nowszych. (#5405)
* NVDA prawidłowo odczytuje punkt uwagi po anulowaniu menu kontekstowego w takich aplikacjach jak Jart. (#5302)
* W Windows 7 i nowszych, kolor jest ponownie prawidłowo zgłaszany w niektórych aplikacjach np. Wordpad. (#5352)
* Podczas edycji w Microsoft PowerPoint, naciśnięcie enter  odczytuje tekst wprowadzony automatycznie, np. punktor albo numer. (#5360)

## 2015.3

Najważniejsze zmiany w tej wersji to wstępne wsparcie dla Windows 10; możliwość wyłączenia nawigacji pojedynczymi literami w trybie czytania (użyteczne dla niektórych aplikacji webowych); poprawki obsługi Internet Explorer; poprawki nieczytelnego tekstu wpisywanego w niektórych aplikacjach z włączonym brajlem.

### Nowości

* Błędy pisowni są oznajmiane w polach edycji Internet Explorer i innych kontrolkach MSHTML. (#4174)
* Dużo więcej symboli matematycznych unikodu jest odczytywane w tekstach. (#3805)
* Sugestie wyszukiwania na ekranie startowym Windows 10 są automatycznie zgłaszane (#5049)
* Obsługa monitorów brajlowskich EcoBraille 20, EcoBraille 40, EcoBraille 80 i EcoBraille Plus. (#4078)
* W trybie czytania, można teraz włączać i wyłączać nawigację pojedynczymi literami, naciskając NVDA+shift+space. Gdy wyłączona, klawisze pojedynczych liter są przekazywane do aplikacji, co jest użyteczne dla niektórych aplikacji webowych takich jak Gmail, Twitter i Facebook. (#3203)
* Nowe tablice brajlowskie: fiński sześciopunktowy, irlandzki stopień 1, irlandzki stopień 2, koreański stopień 1 (2006), koreański stopień 2 (2006). (#5137, #5074, #5097)
* Obsługiwana klawiatura QWERTY w monitorach Papenmeier BRAILLEX Live Plus. (#5181)
* Eksperymentalna obsługa Microsoft Edge - przeglądarki www i silnika przeglądania w Windows 10. (#5212)
* Nowy język: Kannada.

### Zmiany

* Zaktualizowany translator brajlowski liblouis do  wersji 2.6.3. (#5137)
* Przy próbie instalacji wcześniejszej niż zainstalowana obecnie wersji NVDA, pojawi się ostrzeżenie, że jest to niezalecane i że NVDA powinno zostać całkowicie odinstalowane przed kontynuowaniem. (#5037)

### Poprawki błędów

* W trybie czytania w Internet Explorer i innych kontrolkach MSHTML, szybka nawigacja po polach formularza nie uwzględnia elementów listy prezentacji. (#4204)
* W Firefox, NVDA nie próbuje od teraz tworzyć opisu paneli zakładek ARIA opartego na całym tekście wewnątrz, gdy punkt uwagi jest przesuwany w zakładce. (#4638)
* W Internet Explorer i innych kontrolkach MSHTML, przejście do sekcji, artykułów lub okien dialogowych nie zgłasza od teraz całej zawartości kontenera jako nazwy. (#5021, #5025)
* Podczas używania monitorów brajlowskich Baum/HumanWare/APH z klawiaturą brajlowską, wprowadzanie brajla nie przestaje działać po naciśnięciu innego typu klawisza na monitorze. (#3541)
* W Windows 10, nadmiarowe informacje nie są zgłaszane po naciśnięciu alt+tab lub alt+shift+tab, aby przełączyć pomiędzy aplikacjami. (#5116)
* Wpisywany tekst nie jest od teraz nieczytelny podczas używania niektórych aplikacji takich jak Microsoft Outlook z monitorem brajlowskim. (#2953)
* W trybie czytania Internet Explorer i innych kontrolkach MSHTML, prawidłowa treść jest teraz odczytywana, gdy pojawia się lub zmienia element i przywołuje natychmiastowo punkt uwagi. (#5040)
* W trybie czytania w Microsoft Word, nawigacja literami aktualizuje monitor brajlowski i kursor przeglądu zgodnie z oczekiwaniami. (#4968)
* Nadmiarowe spacje nie są wyświetlane w brajlu pomiędzy lub za identyfikatorem kontrolek i formatowania. (#5043)
* Gdy aplikacja wolno odpowiada i przełączysz się z tej aplikacji, NVDA jest bardziej responsywne w innych aplikacjach w większości sytuacji. (#3831)
* Wyskakujące powiadomienia Windows 10 są teraz zgłaszane zgodnie z oczekiwaniami. (#5136)
* Wartość pól kombi (UI Automation) jest zgłaszana po zmianie w polach, gdzie to wcześniej nie działało.
* W trybie czytania w przeglądarkach www, użycie tabulatora zachowuje się zgodnie z oczekiwaniami po przejściu do dokumentu w ramce. (#5227)
* Można wyjść z ekranu blokady Windows 10 przy użyciu ekranu dotykowego. (#5220)
* W Windows 7 i nowszych, tekst nie jest już nieczytelny podczas wpisywania w niektórych aplikacjach takich jak Wordpad czy Skype, przy użyciu monitora brajlowskiego. (#4291)
* Na ekranie startowym Windows 10, nie można od teraz czytać schowka, uzyskiwać dostępu do uruchomionych aplikacji przy użyciu kursora przeglądu, zmieniać konfiguracji NVDA, etc. (#5269)

### Changes for Developers

* You can now inject raw input from a system keyboard that is not handled natively by Windows (e.g. a QWERTY keyboard on a braille display) using the new keyboardHandler.injectRawKeyboardInput function. (#4576)
* eventHandler.requestEvents has been added to request particular events that are blocked by default; e.g. show events from a specific control or certain events even when in the background. (#3831)
* Rather than a single i18nName attribute, synthDriverHandler.SynthSetting now has separate displayNameWithAccelerator and displayName attributes to avoid reporting of the accelerator in the synth settings ring in some languages.
 * For backwards compatibility, in the constructor, displayName is optional and will be derived from displayNameWithAccelerator if not provided. However, if you intend to have an accelerator for a setting, both should be provided.
 * The i18nName attribute is deprecated and may be removed in a future release.

## 2015.2

Najważniejsze zmiany w tej wersji to możliwość odczytywania wykresów w Microsoft Excel oraz wsparcie dla nawigacji i odczytu treści matematycznej.

### Nowości

* W Microsoft Word i Outlook możliwe jest przechodzenie w przód i wstecz po zdaniach przy użyciu odpowiednio alt+strzałka w dół i alt+strzałka w górę. (#3288)
* Nowe tablice brajlowskie dla kilku języków indyjskich. (#4778)
* W Microsoft Excel, NVDA zgłasza, gdy komórka jest przepełniona lub zawiera przyciętą treść. (#3040)
* Microsoft Excel: Lista elementów (NVDA+f7), pozwalająca wyświetlić wykresy, komentarze i formuły. (#1987)
* Obsługa odczytu wykresów w Microsoft Excel: wybierz wykres używając listy elementów (NVDA+f7), a następnie przy użyciu klawiszy strzałek można przejść do wszystkich punktów danych. (#1987)
* Używając MathPlayer 4 od Design Science, NVDA może odczytywać i interaktywnie nawigować w treści matematycznej w przeglądarkach internetowych oraz  Microsoft Word i PowerPoint. Więcej szczegółów zawiera rozdział "Czytanie treści matematycznej" w podręczniku użytkownika. (#4673)
* Możliwe jest obecnie przypisywanie zdarzeń wejścia (skrótów klawiszowych, gestów dotykowych, etc.) dla wszystkich okien ustawień NVDA i opcji formatowania dokumentów, używając polecenia "Zdarzenia wejścia". (#4898)

### Zmiany

* W oknie formatowania dokumentów NVDA, zmienione zostały skróty klawiszowe do zgłaszania list, linków, numerów linii i nazw czcionek (nie dotyczy polskiej wersji językowej). (#4650)
* W oknie ustawień myszy NVDA, dodano skróty klawiszowe sygnalizowania dźwiękiem położenia myszy oraz "głośność dźwięku myszy zależy od jasności obrazu" (w polskiej wersji językowej, skróty te istniały już wcześniej). (#4916)
* Znacząco poprawione oznajmianie nazw kolorów. (#4984)
* Zaktualizowany translator brajlowski liblouis do  wersji 2.6.2. (#4777)

### Poprawki błędów

* Opisy znaków są teraz poprawnie obsługiwane dla złożonych znaków w kilku indyjskich językach. (#4582)
* Jeśli opcja "Ufaj językowi głosu przetwarzając znaki i symbole" jest włączona, okno interpunkcji/wymowy prawidłowo używa języka głosu. Ponadto język, którego wymowa jest edytowana,jest wyświetlany w tytule okna. (#4930)
* W Internet Explorer i innych kontrolkach MSHTML, wpisywane znaki nie są od teraz nieprawidłowo oznajmiane w rozwijanych polach edycyjnych takich jak pole wyszukiwania na stronie domowej Google. (#4976)
* Podczas wybierania koloru w aplikacjach Microsoft Office, odczytywane są nazwy kolorów. (#3045)
* Brajl dla języka duńskiego teraz działa ponownie. (#4986)
* pageUp / pageDown mogą być znów używane do przełączania slajdów w pokazie slajdów PowerPoint . (#4850)
* W Skype dla pulpitu 7.2 i nowszych, powiadomienia o wpisywaniu są odczytywane i zostały rozwiązane problemy występujące po wyjściu punktu uwagi z konwersacji. (#4972)
* Poprawione problemy z wpisywaniem niektórych znaków interpunkcji i symboli, takich jak nawiasy, do pola filtru w oknie dialogowym zdarzeń wejścia. (#5060)
* W Internet Explorer i innych kontrolkach MSHTML, naciśnięcie g lub shift+g by nawigować po grafikach, uwzględnia teraz elementy oznaczone jako obrazki dla potrzeb dostępności (tj. rola ARIA img). (#5062)

### Changes for Developers

* brailleInput.handler.sendChars(mychar) will no longer filter out a character if it is equal to the previous character by ensuring that the key sent is correctly released. (#4139)
* Scripts for changing touch modes will now honor new labeles added to touchHandler.touchModeLabels. (#4699)
* Add-ons can provide their own math presentation implementations. See the mathPres package for details. (#4509)
* Speech commands have been implemented to insert a break between words and to change the pitch, volume and rate. See BreakCommand, PitchCommand, VolumeCommand and RateCommand in the speech module. (#4674)
 * There is also speech.PhonemeCommand to insert specific pronunciation, but the current implementations only support a very limited number of phonemes.

## 2015.1

Główne zmiany w tej wersji, to tryb czytania dla dokumentów Microsoft Word i Outlook; duże ulepszenia wsparcia Skype dla pulpitu; istotne poprawki dla Microsoft Internet Explorer.

### Nowości

* Można teraz dodawać nowe symbole w oknie wymowy symboli. (#4354)
* W oknie Zdarzeń wejścia, można używać nowego pola filtrowania, aby wyświetlić zdarzenia zawierające określone słowa. (#4458)
* NVDA automatycznie odczytuje nowy tekst w mintty. (#4588)
* W oknie wyszukiwania trybu czytania, znajduje się od teraz opcja poszukiwania z uwzględnieniem wielkości liter. (#4584)
* Szybka nawigacja (naciśnięcie litery h by przejść do nagłówka etc.) oraz lista elementów (NVDA+f7) są teraz dostępne dla dokumentów Microsoft Word, po włączeniu trybu czytania NVDA+spacja. (#2975)
* Poprawiony odczyt wiadomości HTML w Microsoft Outlook 2007 i wyższych: tryb czytania jest automatycznie włączony dla tych wiadomości. Jeśli tryb czytania nie jest włączony w niektórych rzadkich sytuacjach, możesz wymusić jego włączenie przez NVDA+spacja. (#2975) 
* Nagłówki kolumn tabeli w Microsoft word są automatycznie zgłaszane dla tabel, w których wiersz nagłówkowy został określony przez autora we właściwościach tabeli. (#4510) 
 * Dla tabel z połączonymi wierszami, nie będzie to działać automatycznie. W takiej sytuacji, można ustawić nagłówek kolumny ręcznie w NVDA, używając NVDA+shift+c.
* W Skype dla pulpitu zgłaszane są powiadomienia. (#4741)
* W Skype dla pulpitu można teraz czytać ostatnie wiadomości przy użyciu NVDA+control+1 do NVDA+control+0; np. NVDA+control+1 dla ostatniej wiadomości, NVDA+control+0 dla dziesiątej od końca. (#3210)
* W konwersacji w Skype dla pulpitu, NVDA zgłasza, gdy kontakt pisze. (#3506)
* NVDA może teraz zostać po cichu zainstalowany przy użyciu wiersza poleceń bez uruchamiania zainstalowanej kopii po instalacji. Aby to zrobić, użyj przełącznika --install-silent. (#4206)
* Wsparcie dla monitorów brajlowskich Papenmeier BRAILLEX Live 20, BRAILLEX Live i BRAILLEX Live Plus. (#4614)

### Zmiany

* W oknie ustawień formatowania dokumentu, opcja  informowania o błędach pisowni, posiada klawisz skrótu (alt+b). W polskiej wersji klawisz ten istniał już wcześniej. (#793)
* NVDA  będzie używał języka syntezatora/głosu do przetwarzania znaków i symboli (włączając w to nazwy znaków przestankowych), niezależnie od tego, czy automatyczna zmiana języka jest włączona. Aby wyłączyć tę funkcję, czyli sprawić, żeby NVDA używał języka interfejsu, odznacz nową opcję w ustawieniach głosu: Ufaj językowi głosu przetwarzając znaki i symbole. (#4210)
* Wsparcie dla syntezatora Newfon zostało usunięte. Newfon jest dostępny jako dodatek dla NVDA. (#3184)
* Skype dla pulpitu 7 lub nowszy jest wymagany przez NVDA; wcześniejsze wersje nie są wspierane. (#4218)
* Pobieranie aktualizacji NVDA jest teraz bardziej bezpieczne. (szczególnie, informacje o aktualizacji są pobierane przez https i sprawdzany jest hash pliku po pobraniu.) (#4716)
* eSpeak został zaktualizowany do wersji 1.48.04 (#4325)

### Poprawki błędów

* W Microsoft Excel obsługiwana jest  sytuacja, gdy kolumny i linie nagłówka są połączone. Przykład: Jeśli A1 i B1 są połączone, wówczas na B2 będzie teraz ogłaszany A1 i B1 jako nagłówek kolumny, zamiast braku informacji. (#4617)
* Podczas edycji zawartości pól tekstowych w Microsoft PowerPoint 2003, NVDA będzie poprawnie odczytywał zawartość każdej linii. Dawniej linie były przyrostowo ucinane po jednym znaku na każdy nowy akapit. (#4619)
* Wszystkie okna dialogowe NVDA  są od teraz wyśrodkowane na ekranie, co poprawia wizualną prezentację i użyteczność programu. (#3148)
* W Skype dla pulpitu, podczas wprowadzania zaproszenia przy dodawaniu kontaktu, prawidłowo działa wpisywanie tekstu i przemieszczanie się po nim. (#3661)
* Gdy punkt uwagi przejdzie do nowego elementu w drzewie w Eclipse IDE, jeśli element poprzednio posiadający punkt uwagi był polem wyboru, nie jest od teraz nieprawidłowo odczytywany. (#4586)
* W oknie sprawdzania błędów Microsoft Word, następny błąd zostanie automatycznie zgłoszony po zmianie lub zignorowaniu poprzedniego przy użyciu klawisza skrótu. (#1938)
* Tekst jest poprawnie odczytywany w miejscach takich jak terminal w Tera Term Pro, oraz dokumenty w programie Balabolka. (#4229)
* Punkt uwagi prawidłowo powraca do edytowanego dokumentu, po zakończeniu kompozycji wprowadzania koreańskiego i innych wschodnioazjatyckich języków, podczas edycji w ramce w Internet Explorer i dokumentach MSHTML . (#4045)
* W oknie zdarzeń wejścia, podczas dokonywania wyboru układu klawiatury dla dodawanego zdarzenia, naciśnięcie escape teraz zamyka menu, a nie jak dawniej okno dialogowe. (#3617)
* Po usunięciu dodatku, jego folder jest teraz prawidłowo usuwany po restarcie NVDA. Poprzednio trzeba było restartować dwukrotnie. (#3461)
* Naprawiono główne problemy podczas używania Skype 7 dla pulpitu. (#4218)
* Gdy wysyłasz wiadomość w Skype dla pulpitu, nie jest odczytywana podwójnie. (#3616)
* W Skype dla pulpitu, NVDA nie powinien teraz od czasu do czasu czytać dużej ilości wiadomości (nawet całej konwersacji). (#4644)
* Naprawiono problem, że komenda zgłaszania daty i czasu w NVDA w niektórych przypadkach nie uwzględniała ustawień regionalnych określonych przez użytkownika. (#2987)
* Tryb czytania: nonsensowny tekst (czasem kilkuliniowy) nie jest od teraz prezentowany dla niektórych obrazków np. w serwisie grupy  Google . (Miało to miejsce szczególnie dla obrazków kodowanych w base64.) (#4793)
* NVDA nie powinien się zawieszać po kilku sekundach, gdy punkt uwagi opuścił aplikację sklepu Windows 8, kiedy została ona wstrzymana. (#4572)
* Atrybut aria-atomic żywych obszarów w Mozilla Firefox jest uwzględniany nawet dla zmian tego elementu. Wcześniej miał wpływ tylko na elementy potomne. (#4794) 
* Tryb czytania będzie odzwierciedlał zmiany, zgłaszane będą żywe obszary dla dokumentów trybu czytania w aplikacjach ARIA osadzonych w dokumentach otwartych przez Internet Explorer lub inne kontrolki MSHTML (#4798)
* Gdy dodany lub zmieniony jest tekst w żywych obszarach w  Internet Explorer i innych kontrolkach MSHTML, ogłaszany jest dodany lub zmieniony tekst, zamiast całej zawartości elementu. (#4800)
* Treść wskazywana przez atrybut aria-labelledby na elementach w Internet Explorer i innych kontrolkach MSHTML, prawidłowo zastępuje treść oryginalną, jeśli jest to potrzebne. (#4575)
* Błędnie wpisane słowo jest teraz oznajmiane podczas sprawdzania pisowni w Microsoft Outlook 2013. (#4848)
* W Internet Explorer i innych kontrolkach MSHTML, treść wewnątrz elementów ukrytych przez visibility:hidden nie jest nieprawidłowo pokazywana w trybie czytania. (#4839, #3776)
* W Internet Explorer i innych kontrolkach MSHTML, atrybut title na kontrolkach formularza nie jest od teraz nieprawidłowo preferowany względem innych powiązań ze znacznikami label. (#4491)
* W Internet Explorer i innych kontrolkach MSHTML, NVDA nie ignoruje od teraz ustawiania punktu uwagi na elementach w związku z atrybutem aria-activedescendant. (#4667)

### Changes for Developers

* Updated wxPython to 3.0.2.0. (#3763)
* Updated Python to 2.7.9. (#4715)
* NVDA no longer crashes when restarting after removing or updating an add-on which imports speechDictHandler in its installTasks module. (#4496)

## 2014.4

### Nowości

* Nowe języki: Hiszpański kolumbijski, pendżabski.
* Możliwe jest ponowne uruchomienie NVDA, albo ponowne uruchomienie z wyłączonymi dodatkami z okna dialogowego "Zakończ NVDA". (#4057)
 * NVDA może zostać uruchomiony z wyłączonymi dodatkami również przy użyciu opcji linii komend --disable-addons.
* W słownikach wymowy, można teraz określić, że wzorzec pasuje tylko jeśli jest całym słowem; tzn. nie pojawia się jako część dłuższego słowa. (#1704)

### Zmiany

* Jeśli obiekt, do którego przeszedłeś używając nawigacji po obiektach, jest wewnątrz dokumentu trybu czytania, a obiekt, na którym znajdowałeś się poprzednio nie był, tryb przeglądu jest automatycznie zmieniany na dokument. Poprzednio, takie zachowanie miało miejsce tylko na skutek zmiany obiektu nawigacyjnego po zmianie punktu uwagi. (#4369)
* Listy monitorów brajlowskich i syntezatorów w odpowiednich oknach dialogowych ustawień, są od teraz sortowane alfabetycznie, za wyjątkiem bez brajla /bez mowy, które znajdują się na końcu. (#2724)
* Zaktualizowany translator brajlowski liblouis do  wersji 2.6.0. (#4434, #3835)
* W trybie czytania, naciśnięcie e i shift+e by nawigować po polach edycji, obecnie uwzględnia edytowalne listy rozwijane. Działa to np. w polu wyszukiwania najnowszej wersji wyszukiwarki Google. (#4436)
* Kliknięcie lewym przyciskiem myszy ikony NVDA w obszarze powiadomień, obecnie otwiera menu NVDA. (#4459)

### Poprawki błędów

* Gdy następuje powrót punktu uwagi do dokumentu trybu czytania (np. przejście klawiszami alt+tab do okna otwartej wcześniej strony internetowej), punkt przeglądu jest prawidłowo umieszczany na pozycji wirtualnego kursora, zamiast na kontrolce w punkcie uwagi (np. najbliższym linku). (#4369)
* W pokazach slajdów programu Powerpoint, punkt przeglądu prawidłowo podąża za wirtualnym kursorem. (#4370)
* W Mozilla Firefox i innych przeglądarkach bazujących na Gecko, nowa treść w żywym obszarze zostanie odczytana nawet jeśli ma typ ARIA różny od typu nadrzędnego żywego obszaru. Np. treść z atrybutem assertive dodana do żywego obszaru oznaczonego jako polite. (#4169).
* W Internet Explorer i innych kontrolkach MSHTML,  niektóre przypadki dokumentu zawartego w innym dokumencie, nie blokują teraz użytkownikowi możliwości dotarcia do niektórych treści (szczególnie ramki wewnątrz ramek). (#4418)
* NVDA nie zawiesza się przy próbie użycia monitora brajlowskiego Handy Tech w niektórych sytuacjach. (#3709)
* W Windows Vista, nieprawdziwe okno  "nie znaleziono punktu wejścia" nie jest wyświetlane w niektórych przypadkach, np. gdy uruchomiono NVDA ze skrótu na pulpicie, albo przez klawisz skrótu. (#4235)
* Naprawiono poważne problemy z polami edycji w okienkach dialogowych najnowszych wersji Eclipse . (#3872)
* Outlook 2010: przemieszczanie punktu uwagi działa zgodnie z oczekiwaniami w polu lokalizacji spotkań i próśb o spotkanie. (#4126)
* Wewnątrz żywego obszaru, treść oznaczona jako niebędąca żywą, (np. aria-live="off") jest teraz prawidłowo ignorowana. (#4405)
* Podczas zgłaszania treści paska stanu, posiadającego nazwę, nazwa jest teraz prawidłowo oddzielona od pierwszego słowa treści. (#4430)
* W polach wprowadzania haseł, przy włączonym wypowiadaniu wpisywanych słów, wielokrotne gwiazdki nie są od teraz niepotrzebnie odczytywane po rozpoczęciu wpisywania nowych słów. (#4402)
* Na liście wiadomości Microsoft Outlook , elementy nie są od teraz bezsensownie ogłaszane jako elementy danych. (#4439)
* Podczas zaznaczania tekstu w polu edycji kodu w Eclipse IDE, całe zaznaczenie nie jest odczytywane za każdym razem gdy zaznaczenie się zmieni. (#2314)
* Różne wersje Eclipse, np. wersja zawarta w  Spring Tool Suite,albo pakiecie Android Developer Tools, są teraz rozpoznawane jako Eclipse i odpowiednio obsługiwane. (#4360)
* Śledzenie myszy i eksploracja dotykowa w Internet Explorer i innych kontrolkach MSHTML (włącznie z wieloma aplikacjami dla Windows 8) jest bardziej dokładna na wyświetlaczach z wysoką rozdzielczością DPI, albo po zmianie powiększenia dokumentu. (#3494) 
 * Śledzenie myszy i eksploracja dotykowa w Internet Explorer i innych kontrolkach MSHTML  odczytuje teraz etykietę większej liczby przycisków. (#4173)
* Podczas używania monitora brajlowskiego Papenmeier BRAILLEX z BrxCom, klawisze monitora działają zgodnie z oczekiwaniami. (#4614)

### Changes for Developers

* For executables which host many different apps (e.g. javaw.exe), code can now be provided to load specific app modules for each app instead of loading the same app module for all hosted apps. (#4360)
 * See the code documentation for appModuleHandler.AppModule for details.
 * Support for javaw.exe is implemented.

## 2014.3

### Nowe funkcje

* Dźwięki odtwarzane przy uruchamianiu i zamknięciu NVDA mogą być wyłączone za pomocą nowej opcji w oknie ustawień ogólnych. (#834)
* Pomoc dodatku może być uruchomiona w zarządzaniu dodatkami dla dodatków wspierających tę funkcję. (#2694)
* Wsparcie dla kalendarza w Microsoft Outlook 2007 i nowszych (#2943) zawiera:
 * Oznajmianie aktualnego czasu podczas przemieszczania się przy użyciu strzałek.
 * Oznajmianie, jeśli wybrany czas jest wewnątrz spotkań.
 * Odczytanie wybranego spotkania po wciśnięciu tab.
 * Inteligentne filtrowanie daty, która zostanie odczytana tylko wtedy, gdy nowy wybrany czas lub spotkanie dotyczy innego dnia niż odczytany poprzednio.
* Ulepszone wsparcie skrzynki odbiorczej i innych list wiadomości w Outlook 2010 i nowszych (#3834) zawiera:
 * Możliwość wyciszenia nagłówków kolumn (Od, temat itd.) poprzez wyłączenie opcji zgłaszania nagłówków tabeli w ustawieniach formatowania dokumentu.
 * Możliwość użycia komend nawigacji po tabeli (control + alt + strzałki) do przemieszczania się po pojedynczych kolumnach.
* Microsoft word: jeżeli obraz nie posiada ustawionego alternatywnego tekstu, NVDA odczyta tytuł obrazka jeśli autor go zdefiniował. (#4193)
* Microsoft Word: NVDA zgłasza wcięcie akapitu komendą odczytywania formatowania (NVDA+f). Ta informacja może być oznajmiana automatycznie, jeśli włączone jest nowe ustawienie zgłaszania wcięcia akapitów w ustawieniach formatowania dokumentu. (#4165)
* Zgłaszaj tekst wstawiony automatycznie, taki jak nowy punktor, numer lub wcięcie tabulacji, gdy naciśnięto Enter w edytowalnych dokumentach i polach tekstowych. (#4185)
* Microsoft word: naciśnięcie NVDA+alt+c odczyta tekst komentarza, jeśli kursor się w nim znajduje. (#3528)
* Ulepszone wsparcie automatycznego odczytywania nagłówków wierszy i kolumn w Microsoft Excel (#3568) zawiera:
 * Wsparcie nazwanych obszarów Excel dla identyfikacji komórek nagłówkowych (kompatybilne z czytnikiem ekranu Jaws).
 * Polecenia ustaw nagłówek kolumny (NVDA+shift+c) i ustaw nagłówek wiersza (NVDA+shift+r), od teraz przechowują ustawienia w skoroszycie, dzięki czemu będą one dostępne przy następnym otwarciu arkusza, w tym również dla innych czytników ekranu, które wspierają system nazwanych zakresów.
 * Te polecenia mogą teraz być użyte wielokrotnie w arkuszu, dla ustawienia różnych nagłówków w różnych obszarach.
* Wsparcie automatycznego odczytywania nagłówków kolumn i wierszy w Microsoft Word (#3110) zawiera:
 * Wsparcie zakładek MS Word dla identyfikacji komórek nagłówkowych (kompatybilne z czytnikiem ekranu Jaws).
 -  Polecenia Ustaw nagłówek kolumny (NVDA+shift+c) i ustaw nagłówek wiersza (NVDA+shift+r) na pierwszej komórce nagłówkowej w tabeli, pozwalają ustawić w NVDA, że te nagłówki powinny być zgłaszane automatycznie.  Ustawienia są przechowywane w dokumencie, więc są dostępne po następnym otwarciu dokumentu, również dla innych programów czytania ekranu, które obsługują system zakładek.
* Microsoft Word: zgłaszaj odległość od lewej krawędzi strony, gdy naciśnięto klawisz tab. (#1353)
* Microsoft Word: informacja zwrotna mową i brajlem dla większości dostępnych klawiszy skrótu formatowania (pogrubienie, kursywa, podkreślenie, wyrównanie, poziom konspektu, indeks górny, indeks dolny i rozmiar czcionki). (#1353)
* Microsoft Excel: jeśli wybrana komórka zawiera komentarze, mogą one zostać odczytane po naciśnięciu NVDA+alt+c. (#2920)
* Microsoft Excel: specyficzne dla NVDA okno edycji komentarzy aktualnie wybranej komórki po naciśnięciu shift+f2 by przejść do trybu edycji komentarzy. (#2920)
* Microsoft Excel: informacja zwrotna mową i brajlem po użyciu większej liczby skrótów klawiaturowych do nawigacji i zaznaczania komórek (#4211) w tym:
 * Pionowo po stronach (pageUp i pageDown);
 * Poziomo po stronach (alt+pageUp i alt+pageDown);
 * Rozszerzenie zaznaczenia (powyższe klawisze z klawiszem Shift); oraz
 * Zaznaczenie aktualnego obszaru (control+shift+8).
* Microsoft Excel: zgłaszaj pionowe i poziome wyrównanie komórek poleceniem odczytania formatowania (NVDA+f) oraz automatycznie, jeśli włączona jest opcja odczytywania wyrównania tekstu w ustawieniach formatowania dokumentu. (#4212)
* Microsoft Excel: odczytaj styl komórki poleceniem odczytania formatowania (NVDA+f) oraz automatycznie, jeśli włączona jest opcja informowania o stylach w ustawieniach formatowania dokumentu. (#4213)
* Microsoft Powerpoint: podczas przemieszczania kształtów po slajdzie przy użyciu strzałek, zgłaszane jest teraz położenie kształtu (#4214) w tym:
 * Odczytana jest odległość kształtu od każdej krawędzi slajdu.
 * Jeśli kształt przysłania, lub jest przysłonięty przez inny kształt, podawany jest rozmiar zachodzenia, oraz inny kształt. 
 * Aby w każdej chwili otrzymać te informacje bez przesuwania kształtu, wywołaj polecenie zgłaszania położenia (NVDA+delete).
 * Podczas zaznaczania kształtu przysłoniętego przez inny kształt, zgłoszone zostanie, że jest przysłonięty.
* Polecenie odczytania położenia (NVDA+delete) jest bardziej zależne od kontekstu w niektórych sytuacjach. (#4219):
 * W polach edycji i trybie czytania, zgłaszana jest pozycja kursora jako procent treści, oraz jego współrzędne na ekranie.
 * Na kształtach w prezentacjach Powerpoint, odczytana zostanie pozycja kształtu w odniesieniu do krawędzi slajdu i innych kształtów.
 * Dwukrotne wywołanie tego polecenia spowoduje dawne zachowanie, czyli odczytanie położenia całej kontrolki.
* Nowy język: kataloński.

### Zmiany

* Zaktualizowana biblioteka liblouis braille translator do 2.5.4. (#4103)

### Poprawki błędów

* Klawisz tworzonego przez instalator skrótu NVDA na pulpicie, został dla polskiej wersji zmieniony na Ctrl+Alt+D, co rozwiązuje pojawiający się dotychczas problem z wpisywaniem litery "ń" po instalacji NVDA. (#2209)
* W Google Chrome i przeglądarkach bazujących na Chrome, niektóre fragmenty tekstu (np. podkreślone) nie są od teraz wielokrotnie powtarzane przy zgłaszaniu tekstu powiadomienia lub okna dialogowego. (#4066)
* W trybie czytania w aplikacjach Mozilla, naciśnięcie Entera na przycisku nie stwarza dłużej problemów z jego aktywowaniem (lub aktywowaniem zamiast tego niewłaściwej kontrolki) co miało miejsce w niektórych wypadkach, np. przyciski na górze Facebooka. (#4106)
* Bezużyteczne informacje nie są dłużej zgłaszane podczas przechodzenia po kontrolkach w iTunes. (#4128)
* Na niektórych listach iTunes np. liście muzyki, działa prawidłowo przechodzenie do następnego elementu przy użyciu nawigacji po obiektach. (#4129)
* Elementy HTML uznane za nagłówki z powodu znaczników WAI ARIA  są teraz uwzględniane w liście elementów oraz szybkiej nawigacji trybu czytania Internet explorer. (#4140)
* Użycie linku do innego miejsca na tej samej stronie w nowszych wersjach Internet Explorer, prawidłowo zmienia położenie i odczytuje nowe miejsce w dokumentach trybu czytania. (#4134)
* Microsoft Outlook 2010 i nowsze: poprawiony dostęp do bezpiecznych okien dialogowych, takich jak nowy profil i ustawienia poczty. (#4090, #4091, #4095)
* Microsoft Outlook: zmniejszona nadmierna gadatliwość komend pasków narzędzi podczas nawigacji w niektórych oknach dialogowych. (#4096, #3407)
* Microsoft word:  przejście do pustej komórki w tabeli nie powoduje błędnego komunikatu o wyjściu z tabeli. (#4151)
* Microsoft Word: pierwszy znak poza tabelą (włącznie z nową pustą linią) nie jest od teraz nieprawidłowo oznajmiany jako część tabeli. (#4152)
* Okno sprawdzania pisowni Microsoft Word 2010: NVDA odczytuje teraz błędnie napisane słowo, zamiast jak dawniej pierwsze pogrubione słowo. (#3431)
* Tryb czytania Internet Explorer i innych kontrolek MSHTML : użycie tabulatora, lub jednoliterowej nawigacji przejścia do pól edycyjnych ponownie zgłasza ich etykietę w wielu przypadkach, gdy to wcześniej nie działało (szczególnie, gdy użyto elementu HTML label). (#4170)
* Microsoft Word: dokładniejsze zgłaszanie istnienia i położenia komentarzy. (#3528)
* Poprawiona nawigacja w niektórych oknach produktów MS Office takich jak Word, Excel i Outlook poprzez nieodczytywanie niektórych kontenerów pasków narzędzi, które nie są przydatne dla użytkownika. (#4198) 
* Okienka zadań takie jak manager schowka lub odzyskiwanie plików, nie otrzymują od teraz przypadkowo punktu uwagi podczas otwierania aplikacji Microsoft Word, albo Excel, co czasem zmuszało użytkownika do przełączania się z i do aplikacji, aby móc używać dokumentu lub arkusza.  (#4199)
* Rozwiązany problem uruchamiania NVDA na nowszych systemach Windows, jeśli język użytkownika jest ustawiony na serbski (łaciński). (#4203) 
* Naciśnięcie klawisza numlock w trybie pomocy klawiatury, obecnie prawidłowo przełącza numlock, zamiast powodować rozsynchronizowanie systemu i klawiatury w kwestii stanu tego klawisza. (#4226)
* W Google Chrome, tytuł dokumentu jest ponownie odczytywany podczas przełączania zakładek. W NVDA 2014.2, nie działało to w niektórych przypadkach. (#4222)
* W Google Chrome i przeglądarkach bazujących na Chrome, adres dokumentu nie jest od teraz odczytywany podczas anonsowania dokumentu. (#4223)
* Po włączeniu funkcji czytaj wszystko z wybranym syntezatorem "Bez mowy" (użyteczne dla automatycznego testowania), funkcja czytaj wszystko zostanie dokończona zamiast zatrzymać się po pierwszych kilku liniach. (#4225)
* Okienko podpisu w Microsoft Outlook: pole edycji podpisu jest teraz dostępne z pełnym śledzeniem kursora i wykrywaniem formatowania. (#3833) 
* Microsoft Word: podczas czytania ostatniej linii komórki tabeli, cała zawartość komórki nie jest od teraz odczytywana. (#3421)
* Microsoft Word: podczas czytania pierwszej lub ostatniej linii spisu treści, cały spis treści nie jest od teraz odczytywany. (#3421)
* Podczas czytania pisanych słów, oraz w niektórych innych sytuacjach, słowa nie są od teraz nieprawidłowo dzielone na znakach samogłosek, albo znakach virama w językach Indyjskich. (#4254)
* Numeryczne pola edycji w GoldWave są teraz prawidłowo obsługiwane. (#670)
* Microsoft Word: podczas przemieszczania się po akapitach klawiszami control+strzałka w dół / control+strzałka w górę, nie jest od teraz konieczne naciskanie ich dwukrotnie podczas przechodzenia przez listy numerowane lub punktowane. (#3290)

### Changes for Developers

* NVDA now has unified support for add-on documentation. See the Add-on Documentation section of the Developer Guide for details. (#2694)
* When providing gesture bindings on a ScriptableObject via __gestures, it is now possible to provide the None keyword as the script. This unbinds the gesture in any base classes. (#4240)
* It is now possible to change the shortcut key used to start NVDA for locales where the normal shortcut causes problems. (#2209)
 * This is done via gettext.
 * Note that the text for the Create desktop shortcut option in the Install NVDA dialog, as well as the shortcut key in the User Guide, must also be updated.

## 2014.2

### Nowe funkcje

* Oznajmianie zaznaczania tekstu jest teraz możliwe w niektórych nietypowych polach edycyjnych, w których używana jest informacja o wyświetlaniu. (#770)
* W dostępnych aplikacjach Java, oznajmiana jest teraz informacja o pozycji dla przycisków opcji i innych kontrolek, które udostępniają te informacje. (#3754)
* W dostępnych aplikacjach Java, oznajmiane są teraz skróty klawiszowe dla kontrolek, które je posiadają. (#3881)
* W trybie czytania, zgłaszane są od teraz etykiety punktów orientacyjnych. Są również uwzględniane na liście elementów. (#1195)
* W trybie czytania, nazwane obszary są teraz traktowane jak punkty orientacyjne. (#3741)
* W dokumentach i aplikacjach Internet Explorer, obsługiwane są żywe obszary (część standardu ARIA W3c), pozwalając autorom stron oznaczać określoną treść, która ma być automatycznie odczytywana, gdy się zmienia. (#1846)

### Zmiany

* Przy wyjściu z okna lub aplikacji zawartych w dokumencie trybu czytania, nie jest od teraz ogłaszana nazwa i typ dokumentu. (#4069)

### Poprawki błędów

* Standardowe menu systemowe okien nie jest od teraz przypadkowo wyciszane w aplikacjach Java. (#3882)
* Podczas kopiowania tekstu z przeglądu ekranu, nie jest ignorowane łamanie linii. (#3900)
* Bezsensowne obiekty złożone ze spacji nie są od teraz zgłaszane w niektórych aplikacjach, przy zmianie punktu uwagi, albo podczas używania nawigatora obiektów z włączonym trybem prostego przeglądania. (#3839)
* Okna informacji i inne okienka dialogowe NVDA ponownie powodują anulowanie poprzedniej wypowiedzi przed odczytaniem okna. 
* W trybie czytania, etykiety kontrolek takich jak linki i przyciski są teraz prawidłowo odczytywane w sytuacji, gdy etykieta została nadpisana przez autora dla celów dostępności (szczególnie przy użyciu aria-label lub aria-labelledby). (#1354)
* W trybie czytania w Internet Explorer, tekst zawarty wewnątrz elementu oznaczonego jako prezentacyjny (ARIA role="presentation") nie jest od teraz ignorowany. (#4031)
* Ponownie możliwe jest wpisywanie wietnamskiego tekstu przy użyciu oprogramowania Unikey. Należy w tym celu odznaczyć pole wyboru przetwarzania klawiszy z innych aplikacji, dodane do okna ustawień klawiatury NVDA. (#4043) 
* W trybie czytania, elementy menu typu pola wyboru i przyciski opcji są odczytywane jako kontrolki, a nie tylko klikalny tekst. (#4092)
* NVDA od teraz nie przełącza się nieprawidłowo z trybu formularzy do trybu czytania gdy punkt uwagi znajduje się na elemencie menu typu pole wyboru, albo przycisk opcji. (#4092)
* W Microsoft PowerPoint przy włączonym odczytywaniu wpisywanych słów, znaki usunięte klawiszem Backspace nie są od teraz odczytywane jako część wpisanego słowa. (#3231)
* W oknach opcji Microsoft Office 2010, nazwy list rozwijanych są odczytywane prawidłowo. (#4056)
* W trybie czytania w aplikacjach Mozilla, klawisze szybkiej nawigacji przejścia do poprzedniego/następnego przycisku lub pola formularza, teraz uwzględniają również przyciski przełączające. (#4098)
* Zawartość alertów w aplikacjach Mozilla, nie jest od teraz odczytywana podwójnie. (#3481)
* W trybie czytania, kontenery i punkty orientacyjne nie są od teraz niepotrzebnie powtarzane podczas nawigowania wewnątrz nich w tym samym czasie, gdy zmienia się zawartość strony (np. na stronach Facebook i Twitter). (#2199)
* NVDA odzyskuje sprawność w większej liczbie przypadków przełączania się z aplikacji, które przestały odpowiadać. (#3825)
* Kursor (punkt wstawiania), ponownie jest prawidłowo aktualizowany po wywołaniu komendy czytaj wszystko w tekście edytowalnym, rysowanym bezpośrednio na ekranie. (#4125)

## 2014.1

### Nowe funkcje

* Wsparcie dla Microsoft PowerPoint 2013. Uwaga: widok chroniony nie jest obsługiwany. (#3578)
* W Microsoft word i Excel, NVDA może teraz czytać wybrany symbol podczas wyboru w okienku wstaw symbol. (#3538)
* W okienku ustawień formatowania dokumentu, możliwe jest obecnie określenie, czy treść w dokumentach powinna być identyfikowana jako klikalna. Ta opcja jest domyślnie włączona(poprzednie zachowanie). (#3556)
* Wsparcie monitorów brajlowskich połączonych przez Bluetooth na komputerze z uruchomionym oprogramowaniem Widcomm Bluetooth. (#2418)
* Podczas edycji tekstu w PowerPoint, raportowane są hiperłącza. (#3416)
* Wewnątrz aplikacji ARIA albo okien dialogowych na stronach www, możliwe jest przełączenie NVDA w tryb czytania klawiszami NVDA+space, co umożliwia nawigację wewnątrz aplikacji lub dialogu tak jak w dokumencie. (#2023)
* W Outlook Express / Windows Mail / Windows Live Mail, NVDA teraz informuje czy wiadomość ma załącznik lub jest oflagowana. (#1594)
* podczas nawigowania wewnątrz tabeli w dostępnych aplikacjach Java, odczytywane są współrzędne komórki oraz nagłówki wiersza i kolumny, jeśli istnieją. (#3756)

### Zmiany

* Dla monitorów brajlowskich Papenmeier, usunięta została komenda przejścia do płaskiego podglądu / punktu uwagi. Użytkownicy mogą przypisać własne klawisze w okienku Zdarzenia wejścia. (#3652)
* NVDA teraz opiera się na Microsoft VC runtime wersja 11, co oznacza, że nie może dłużej być uruchomiony na systemach operacyjnych starszych niż Windows XP Service Pack 2 lub Windows Server 2003 Service Pack 1.
* Poziom interpunkcji: Niektóre,  oznajmia od teraz znaki gwiazdka (*) i plus (+). (#3614)
* Zaktualizowano eSpeak do wersji 1.48.03 zawierającej wiele poprawek języków i kilku awarii. (#3842, #3739)

### Poprawki błędów

* Podczas przemieszczania się po komórkach i ich zaznaczania w Microsoft Excel, NVDA nie powinien od teraz nieprawidłowo czytać poprzedniej komórki, zamiast obecnej, gdy Microsoft Excel jest wolny. (#3558)
* NVDA prawidłowo obsługuje otwieranie listy rozwijanej dla komórki w Microsoft Excel przez menu kontekstowe. (#3586)
* Nowa zawartość strony sklepu w iTunes 11 jest teraz prawidłowo pokazywana w trybie czytania gdy nastąpi przejście przez link do sklepu, lub gdy otwierana jest od razu strona sklepu. (#3625)
* Przyciski podglądu piosenek w sklepie iTunes 11 teraz posiadają etykietę w trybie czytania. (#3638)
* W trybie czytania w Google Chrome, etykiety pól wyboru i przycisków opcji są teraz prawidłowo odczytywane. (#1562)
* W Instantbird, NVDA nie odczytuje dłużej bezużytecznych informacji po każdym przejściu do kontaktu na liście kontaktów. (#2667)
* W trybie czytania w Adobe Reader, prawidłowy tekst jest odczytywany dla przycisków etc., gdy etykieta została nadpisana przy użyciu podpowiedzi lub innych metod. (#3640)
* W trybie czytania w Adobe Reader, obce grafiki zawierające tekst "mc-ref" nie będą dłużej odczytywane. (#3645)
* NVDA nie zgłasza dłużej wszystkich komórek w Microsoft Excel jako podkreślone, odczytując ich informacje o formatowaniu. (#3669)
* W dokumentach trybu czytania nie są pokazywane pozbawione znaczenia znaki Unikodu np. z zakresu do prywatnego użycia. W niektórych przypadkach blokowało to możliwość pokazania bardziej użytecznych etykiet. (#2963).
* Wprowadzanie znaków wschodnioazjatyckich nie powodóje dłużej problemów w programie PuTTY (#3432)
* Nawigowanie w dokumencie po anulowanym czytaniu wszystkiego, nie powoduje od teraz, że  NVDA czasami nieprawidłowo zgłaszał wyjście z pola (takiego jak tabela) które znajdowało się w dokumencie niżej niż miejsce, w którym przerwano czytanie. (#3688)
* Podczas używania klawiszy szybkiej nawigacji trybu czytania, gdy  aktywna jest funkcja Czytaj wszystko i włączone zezwalanie na przeglądanie podczas czytania wszystkiego, NVDA bardziej dokładnie anonsuje nowe pole (np. teraz mówi że nagłówek to nagłówek, zamiast odczytywać tylko jego tekst). (#3689)
* Polecenia szybkiej nawigacji przeskoku do początku lub końca kontenera, obecnie honorują ustawienie zezwalania na przeglądanie w trybie czytaj wszystko (tj. nie będą powodować anulowania czytania wszystkiego). (#3675)
* Nazwy gestów dotykowych wymienione w oknie zdarzeń wejścia NVDA, przedstawiane są obecnie w przyjaznej, przetłumaczonej formie. (#3624)
* NVDA nie powoduje dłużej awarii niektórych programów podczas przemieszczania myszy po ich kontrolkach rich edit (TRichEdit). Programy te to m.in. Jarte 5.1 i BRfácil. (#3693, #3603, #3581)
* W Internet Explorer i innych kontrolkach MSHTML, kontenery takie jak tabele, oznaczone przez ARIA jako prezentacje, nie są od teraz zgłaszane użytkownikowi. (#3713)
* W Microsoft Word, NVDA nie powtarza od teraz na monitorze brajlowskim wielokrotnie informacji o wierszu i kolumnie tabeli dla komórki. (#3702)
* W językach używających spacji jako separatora grupy liczb / tysięcy (np. niemiecki i francuski), liczby z odrębnych kawałków tekstu nie są od teraz wymawiane jak jedna liczba. Było to szczególnie kłopotliwe dla komórek tabeli zawierających liczby. (#3698)
* Rozwiązany problem z brakiem aktualizacji brajla przy ruchach kursora, który czasem pojawiał się w Microsoft Word 2013. (#3784)
* Po ustawieniu kursora na pierwszym znaku nagłówka w Microsoft Word, tekst informujący, że jest to nagłówek (z podaniem jego poziomu) nie znika od teraz z monitora brajlowskiego. (#3701)
* Gdy został uruchomiony przez wyzwalacz profil dla aplikacji, która następnie została zamknięta, NVDA od teraz prawidłowo dezaktywuje ten profil. (#3732)
* Podczas wprowadzania znaków azjatyckich w kontrolce samego NVDA (np. okno wyszukiwania w trybie czytania), "NVDA" nie jest dłużej nieprawidłowo odczytywane zamiast znaku kandydującego. (#3726)
* Zakładki w oknie opcji Outlook 2013 są teraz odczytywane. (#3826)
* Poprawiona obsługa żywych obszarów ARIA w Firefox i innych aplikacjach Mozilla Gecko :
 * obsługa aktualizacji aria-atomic i filtrowanie aktualizacji aria-busy (#2640)
 * Tekst alternatywny (taki jak atrybut alt lub aria-label) jest dołączany, jeśli nie ma innego użytecznego tekstu. (#3329)
 * Aktualizacje żywych obszarów nie są od teraz wyciszane, jeśli nastąpiły w tym samym momencie co przesunięcie punktu uwagi. (#3777)
* Niektóre elementy prezentacji w Firefox i innych aplikacjach Mozilla Gecko nie są od teraz nieprawidłowo pokazywane w trybie czytania (szczególnie, gdy element jest oznaczony jako aria-presentation i jednocześnie może posiadać punkt uwagi). (#3781)
* Poprawka wydajności podczas nawigacji wewnątrz dokumentów w Microsoft Word przy włączonym zgłaszaniu błędów pisowni. (#3785)
* Kilka poprawek obsługi dostępnych aplikacji Java:
 * początkowo aktywna kontrolka w ramce lub oknie dialogowym jest od teraz odczytywana gdy ramka lub okno dialogowe przechodzi na pierwszy plan. (#3753)
 * bezużyteczne informacje o pozycji przycisków radiowych nie są teraz odczytywane (np. 1 z 1). (#3754)
 * Lepsza obsługa kontrolek typu JComboBox (html nie jest odczytywany, lepsze zgłaszanie stanów rozwinięte / zwinięte). (#3755)
 * Podczas odczytywania okien dialogowych, czytany jest tekst, który dawniej był pomijany. (#3757)
 * zmiany nazwy, wartości lub opisu aktywnej kontrolki są teraz zgłaszane bardziej precyzyjnie. (#3770)
* Naprawiono awarię NVDA w Windows 8 gdy punkt uwagi znajdował się na niektórych kontrolkach RichEdit zawierających dużą ilość tekstu (np. podgląd logów NVDA, windbg). (#3867)
* W systemach z ustawionym wysokim DPI ekranu (domyślnie ustawianym na wielu współczesnych komputerach), NVDA nie przenosi od teraz wskaźnika myszy do nieprawidłowego miejsca w niektórych aplikacjach. (#3758, #3703)
* Naprawiono sporadyczny problem podczas przeglądania internetu: NVDA przestawał prawidłowo pracować do czasu restartu, chociaż wcześniej nie zawiesił się, ani nie uległ awarii. (#3804)
* Monitor brajlowski Papenmeier może teraz być używany, nawet jeśli nie był wcześniej podłączony przez USB. (#3712)
* NVDA nie zawiesza się teraz, gdy wybrano starsze modele monitora brajlowskiego Papenmeier BRAILLEX, a urządzenie nie jest podłączone.

### Changes for Developers

* AppModules now contain productName and productVersion properties. This info is also now included in Developer Info (NVDA+f1). (#1625)
* In the Python Console, you can now press the tab key to complete the current identifier. (#433)
 * If there are multiple possibilities, you can press tab a second time to choose from a list.

## 2013.3

### Nowe funkcje

* W dokumentach Microsoft word zgłaszane są pola formularza. (#2295)
* Microsoft Word: NVDA może informować o zmianach w dokumencie,  gdy włączone jest śledzenie zmian. Aby ta funkcja działała, należy zaznaczyć pole wyboru "zgłaszaj zmiany edycyjne" (domyślnie niezaznaczone) w menu NVDA Ustawienia: Formatowanie dokumentów. (#1670)
* Listy rozwijane w Microsoft Excel 2003 do 2010 są teraz czytane przy otwieraniu i nawigacji wewnątrz nich. (#3382)
* Nowa opcja 'Zezwalaj na przeglądanie w trybie czytaj wszystko' w oknie ustawień klawiatury, umożliwia nawigację wewnątrz dokumentu klawiszami szybkiej nawigacji trybu czytania oraz strzałkami kursora, nie przerywając czytania. Ta opcja jest domyślnie wyłączona. (#2766) 
* Dostępne jest obecnie okienko ustawień zdarzeń wejścia, ułatwiające konfigurowanie własnych zdarzeń wejścia (takich jak naciskane klawisze) aktywujących polecenia NVDA. (#1532)
* Przy użyciu profili konfiguracji, możesz od teraz określić różne ustawienia dla różnych sytuacji. Profile mogą być aktywowane ręcznie lub automatycznie (np. dla konkretnej aplikacji). (#87, #667, #1913)
* Microsoft Excel: komórki będące linkami, są teraz anonsowane jako linki. (#3042)
* Microsoft Excel: istnienie komentarzy na komórce jest teraz zgłaszane użytkownikowi. (#2921)

### Poprawki błędów

* Zend Studio obecnie działa tak samo jak Eclipse. (#3420)
* W okienku reguł wiadomości Microsoft Outlook 2010, zmieniony stan pewnych pól wyboru zgłaszany jest automatycznie. (#3063)
* NVDA obecnie będzie ogłaszać stan przypiętych kontrolek,  takich jak karty w Mozilla Firefox. (#3372)
* Możliwe jest od teraz powiązanie skryptów ze skrótami klawiszowymi zawierającymi klawisze Alt i/lub Windows jako modyfikatory. Dawniej, jeśli zostało to zrobione, wykonanie skryptu powodowało również otwarcie menu start, lub paska menu. (#3472)
* Zaznaczanie tekstu w dokumentach trybu czytania (np. użycie control+shift+end) nie powoduje przełączenia układu klawiatury na systemach z zainstalowanymi wieloma układami klawiatury. (#3472)
* Internet Explorer : rozwiązany problem awarii przeglądarki przy zamykaniu NVDA. (#3397)
* Fizyczne przemieszczenia i inne zdarzenia na niektórych nowych komputerach, nie są od teraz traktowane jako naciśnięcia klawiszy. Dotychczas powodowały wyciszenie mowy i czasami uruchomienie innych komend NVDA. (#3468)
* NVDA teraz zachowuje się zgodnie z oczekiwaniami w programie Poedit 1.5.7. Użytkownicy korzystający ze starszych wersji powinni zaktualizować program. (#3485)
* NVDA potrafi teraz odczytywać zabezpieczone dokumenty w Microsoft Word 2010,  nie powodując awarii edytora. (#1686)
* Podanie nieznanego przełącznika linii komend przy uruchamianiu pakietu dystrybucyjnego NVDA, nie powoduje dłużej wystąpienia niekończącego się ciągu komunikatów o błędach. (#3463)
* Microsoft Word: rozwiązane problemy z oznajmianiem tekstu alternatywnego grafiki i obiektów, który zawierał cudzysłowy i inne niestandardowe znaki. (#3579)
* Prawidłowo oznajmiana liczba elementów niektórych poziomych list w trybie czytania. poprzednio mogła być podwojona. (#2151)
* Po naciśnięciu control+a w arkuszu Microsoft Excel, zgłoszone zostanie nowe zaznaczenie. (#3043)
* NVDA odczytuje teraz prawidłowo dokumenty XHTML  w Microsoft Internet Explorer i innych kontrolkach MSHTML. (#3542)
* Ustawienia klawiatury: jeśli nie wybrano żadnego klawisza NVDA, pojawia się błąd przy zamykaniu tego okna. Przynajmniej jeden klawisz NVDA musi być wybrany dla prawidłowego używania programu. (#2871)
* Microsoft Excel: NVDA inaczej anonsuje połączone komórki, a inaczej - wiele zaznaczonych komórek. (#3567)
* Kursor trybu przeglądania nie jest od teraz nieprawidłowo ustawiany po opuszczeniu okna dialogowego lub aplikacji wewnątrz dokumentu. (#3145)
* Naprawiony problem, że  monitory brajlowskie serii HumanWare Brailliant BI/B nie pojawiały się w niektórych systemach na liście w ustawieniach brajla, nawet gdy taki monitor był podłączony przez USB.
* NVDA nie ma dłużej problemów z przejściem do trybu przeglądu ekranu, gdy nie jest znana lokalizacja aktualnego obiektu nawigatora. W takim przypadku, punkt przeglądu jest umieszczany na górze ekranu. (#3454)
* Naprawiono problem powodujący w niektórych przypadkach błąd sterownika Freedom Scientific, gdy port był ustawiony na USB. (#3509, #3662)
* Naprawiony problem niewykrywania klawiszy naciskanych na monitorach Freedom Scientific w niektórych sytuacjach. (#3401, #3662)

### Changes for Developers

* You can specify the category to be displayed to the user for scripts using the scriptCategory attribute on ScriptableObject classes and the category attribute on script methods. See the documentation for baseObject.ScriptableObject for more details. (#1532)
* config.save is deprecated and may be removed in a future release. Use config.conf.save instead. (#667)
* config.validateConfig is deprecated and may be removed in a future release. Add-ons which need this should provide their own implementation. (#667, #3632)

## 2013.2

### Nowe funkcje

* Obsługa Chromium Embedded Framework - kontrolki przeglądarki sieciowej, używanej w niektórych programach. (#3108)
* Nowy wariant Espeak: Iven3
* Skype: nowe wiadomości w aktywnym oknie rozmowy tekstowej są wypowiadane automatycznie.  (#2298)
* Obsługa Twin: odczyt nazw zakładek i mniejsza gadatliwość przy anonsowaniu tweetów.
* Możesz teraz wyłączyć wyświetlanie komunikatów NVDA na monitorze brajlowskim. W ustawieniach brajla przestaw czas wygasania komunikatów na 0.  (#2482)
* Okno zarządzania dodatkami rozbudowane o przycisk "Pobierz dodatki". Powoduje on otwarcie strony, na której można pobrać i zainstalować dodatki dla NVDA. (#3209)
* W okienku "Witaj w NVDA",które pojawia się przy pierwszym uruchomieniu programu, możesz teraz określić, czy NVDA ma być uruchamiane automatycznie po zalogowaniu do systemu. (#2234)
* w programie Dolphin Cicero automatycznie aktywny jest tryb uśpienia NVDA. (#2055)
* 64-bitowe wersje Miranda IM/Miranda NG są teraz obsługiwane. (#3296)
* Windows 8: odczytywane są automatycznie sugestie wyszukiwania na ekranie startowym.  (#3322)
* Wsparcie nawigacji i edycji arkuszy w Microsoft Excel 2013.  (#3360)
* Obsługa połączonych przez bluetooth Monitorów brajlowskich  produkcji Freedom Scientific: Focus 14 Blue i Focus 80 Blue, oraz Focus 40 Blue w niektórych konfiguracjach nie obsługiwanych poprzednio. (#3307)
* Sugestie autouzupełniania są odczytywane w programie Outlook 2010. (#2816)
* Nowe tablice brajlowskie: angielski brajl komputerowy, Koreański 2 stopnia, rosyjski brajl dla kodu komputerowego.
* Nowy język: Farsi. (#1427)

### Zmiany

* Na ekranie dotykowym: machnięcie w lewo lub prawo pojedynczym palcem w trybie obiektów przesuwa do poprzedniego lub następnego poprzez wszystkie obiekty, nie tylko te w obecnym kontenerze.Machnięcie dwoma palcami wykonuje oryginalną akcję przechodzenia do poprzedniego lub następnego w aktualnym kontenerze.
* Ustawienia przeglądania: pole wyboru "zgłaszaj układ tabeli"zmienione na "Dołącz układ tabeli", aby uwidocznić fakt, że klawisze szybkiej nawigacji nie będą wyszukiwać tych tabel, gdy to pole wyboru nie jest zaznaczone. (#3140)
* Poziom podglądu zastąpiony przez tryby przeglądania obiektu, dokumentu i ekranu. (#2996)
* Przeglądanie obiektu odczytuje tekst w obrębie wybranego obiektu, przeglądanie dokumentu odczytuje tekst w buforze trybu przeglądania aktualnego dokumentu (jeśli jest), a przeglądanie ekranu - prezentuje tekst okna bieżącej aplikacji.
* Komendy, które wcześniej włączały i wyłączały poziom podglądu, teraz przełączają między wyżej omówionymi trybami.
* W trybie przeglądania dokumentu i ekranu, obiekt nawigatora automatycznie podąża za kursorem podglądu, śledząc w ten sposób najniższy w chierarchii obiekt nawigacyjny.
* Po przełączeniu się w tryb przeglądania ekranu, NVDA pozostaje w tym trybie do chwili ręcznego przełączenia w inny tryb.
* W trybie przeglądania dokumentu lub obiektu, NVDA może przełączać się między tymi trybami zależnie od tego, czy przeglądasz jakiś dokument w trybie czytania.
* Zaktualizowano bibliotekę tłumaczenia brajla liblouis do wersji 2.5.3. (#3371)

### Poprawki błędów

* Aktywowanie obiektu anonsuje akcję przed aktywacją, zamiast po niej (np. Rozwinięte, gdy rozwijasz, zamiast "Zwinięte"). (#2982)
* Dokładniejsze odczytywanie i śledzenie kursora w różnych polach wprowadzania takich jak okno czatu, albo wyszukiwania dla ostatnich wersji Skype. (#1601, #3036)
* Na liście ostatnich rozmów Skype, odczytywana jest liczba nowych zdarzeń dla każdej konwersacji jeśli ma to zastosowanie. (#1446)
* Poprawki śledzenia kursora i kolejności odczytu dla tekstu napisanego od prawej do lewej; np. edycja tekstu arabskiego w Microsoft Excel. (#1601) 
* Szybka nawigacja do przycisków i pól formularza uwzględnia linki oznaczone jako przyciski w przeglądarce Internet Explorer. (#2750)
* W trybie przeglądania, treść wewnątrz widoków drzewa nie jest przedstawiana, gdyż spłaszczona reprezentacja niczemu nie służy. Możesz nacisnąć Enter na drzewie, aby pracować z nim w trybie formularzy. (#3023)
* Klawisze alt+strzałka w górę lub w dół, rozwijające listę, nie przełączają od teraz do trybu przeglądania. (#2340)
* W Internet Explorer 10, komórki tabeli nie aktywują trybu formularza, chyba, że zostały odpowiednio oznaczone jako kontrolki przez autora strony. (#3248)
* Rozwiązane problemy z uruchomieniem NVDA, jeśli czas systemowy jest wcześniejszy od czasu ostatniego sprawdzania aktualizacji. (#3260)
* Jeśli na monitorze brajlowskim wyświetlany jest pasek postępu, monitor jest odświeżany, gdy pasek postępu się zmieni. (#3258)
* W trybie przeglądania dla aplikacji Mozilli, podpisy tabeli nie są od teraz prezentowane podwójnie. Ponadto, streszczenie jest prezentowane, jeśli istnieje również podpis. (#3196)
* Jeśli zmieniono język wprowadzania w Windows 8, NVDA ogłasza aktualny język zamiast poprzedniego.
* W Windows 8 NVDA teraz ogłasza zmiany trybu konwersji IME.
* NVDA nie ogłasza śmieci na pulpicie, gdy używane są metody wprowadzania  Google japoński, albo Atok IME. (#3234)
* W Windows 7 i wyższych, NVDA od teraz nie ogłasza rozpoznawania mowy albo gestów dotykowych jako zmian języka klawiatury.
* NVDA nie ogłasza od teraz znaku specjalnego (0x7f) gdy naciśnięto ctrl+Backspace w niektórych edytorach przy włączonym wypowiadaniu wpisywanych znaków. (#3315)
* Nie pojawiają się od teraz zmiany głośności, wysokości itp. głosu Espeak, gdy NVDA czyta tekst zawierający pewne znaki kontrolne lub XML. (#3334) (regresja #437)
* W aplikacjach Java, zmiany nazwy lub tytułu aktualnej kontrolki są ogłaszane automatycznie i są odzwierciedlone przy odpytywaniu kontrolki. (#3119)
* W kontrolkach Scintilla, linie są od teraz prawidłowo odczytywane przy włączonym zawijaniu wierszy. (#885)
* W aplikacjach Mozilla, nazwa elementów listy tylko do odczytu jest teraz prawidłowo raportowana; np. gdy nawigujesz po tweetach w trybie formularzy w serwisie twitter.com. (#3327)
* Microsoft Office 2013: okienka potwierdzeń  są teraz odczytywane automatycznie, gdy się pojawiają. 
* Microsoft Word: poprawki wydajności podczas nawigacji niektórych tabel. (#3326)
* Komendy NvDA nawigacji po tabeli (control+alt+strzałki) funkcjonują lepiej w niektórych tabelach Microsoft Word, w których komórka zajmuje wiele linii.
* Jeśli Menedżer dodatków jest już otwarty, uruchomienie go ponownie (albo z menu Narzędzia, albo przez otwarcie pliku dodatku) nie powoduje od teraz problemów z zamknięciem Menedżera. (#3351)
* Od teraz NVDA nie zawiesza się w niektórych okienkach dialogowych, gdy używane jest wprowadzanie japońskiego lub chińskiego IME Office 2010. (#3064)
* Wielokrotne spacje nie są kompresowane do pojedynczej na monitorach brajlowskich. (#1366)
* Narzędzia Zend Eclipse PHP Developer pracują teraz tak samo jak Eclipse. (#3353)
* W Internet Explorer, ponownie nie jest konieczne naciśnięcie Tab by pracować z obiektem zagnieżdżonym(takim jak Flash) po uprzednim naciśnięciu na nim Enter. (#3364)
* Podczas edycji tekstu w Microsoft PowerPoint, ostatnia linia nie jest od teraz czytana jako poprzednia, jeśli ostatnia linia jest pusta. (#3403)
* W Microsoft PowerPoint, obiekty nie są od teraz wypowiadane czasem podwójnie gdy je zaznaczasz, lub chcesz edytować. (#3394)
* NVDA nie powoduje od teraz awarii bądź zawieszania Adobe Readera przy czytaniu niektórych źle sformatowanych dokumentów PDF zawierających wiersze tabel poza tabelą. (#3399)
* NVDA obecnie prawidłowo wykrywa następny slajd, gdy usuwany jest slajd w widoku miniatur Microsoft PowerPoint. (#3415)

### Changes for Developers

* windowUtils.findDescendantWindow has been added to search for a descendant window (HWND) matching the specified visibility, control ID and/or class name.
* The remote Python console no longer times out after 10 seconds while waiting for input. (#3126)
* Inclusion of the bisect module in binary builds is deprecated and may be removed in a future release. (#3368)
 * Add-ons which depend on bisect (including the urllib2 module) should be updated to include this module.

## 2013.1.1

Ta wersja rozwiązuje problem awarii NVDA podczas uruchamiania, jeśli w ustawieniach wybrany był Język irlandzki, zawiera również aktualizacje tłumaczeń, oraz inne poprawki.

### Poprawki błędów

* Generowane są prawidłowe znaki podczas wpisywania w okienkach NVDA, jeśli używane są jako domyślne koreańskie lub japońskie metody wprowadzania tekstu . (#2909)
* W programie Internet Explorer i innych kontrolkach MSHTML, pola oznaczone jako zawierające nieprawidłową wartość są teraz prawidłowo obsługiwane. (#3256)
* Rozwiązany problem awarii NVDA podczas uruchamiania, jeśli w ustawieniach wybrany był Język irlandzki.

## 2013.1

Najważniejsze zmiany w tej wersji to bardziej intuicyjny i jednolity układ klawiatury dla laptopa; podstawowe wsparcie dla Microsoft Power Point; wsparcie długich opisów w przeglądarkach internetowych oraz możliwość wprowadzania znaków brajla komputerowego dla monitorów brajlowskich wyposażonych w klawiaturę.

### Ważne

#### Nowy układ klawiatury dla laptopa

Układ klawiatury dla laptopa został całkowicie przeprojektowany, aby uczynić go bardziej intuicyjnym i jednolitym.
Komendy przeglądu w nowym układzie używają klawiszy strzałek w połączeniu z klawiszem NVDA i innymi modyfikatorami.

Proszę zwrócić uwagę na następujące zmiany najczęściej używanych poleceń:

| Działanie |Klawisze|
|---|---|
|Czytaj wszystko |NVDA+a|
|Czytaj bieżącą linię |NVDA+l|
|Odczytaj aktualnie zaznaczony tekst |NVDA+shift+s|
|Odczytaj pasek stanu |NVDA+shift+end|

Dodatkowo, oprócz innych zmian, zmodyfikowano wszystkie polecenia nawigacji obiektów, przeglądu tekstu, kliknięć myszy i parametrów syntezatora.
Wszystkie zmiany znajdują się w [Liście klawiszy poleceń](keyCommands.html).

### Nowe funkcje

* Podstawowe wsparcie edycji i odczytu prezentacji Microsoft Poverpoint. (#501).
* Podstawowe wsparcie dla pisania i odczytu wiadomości w Lotus Notes 8.5. (#543)
* Wsparcie automatycznej zmiany języków podczas czytania dokumentów w Microsoft Word. (#2047) 
* W trybie czytania w kontrolkach MSHTML (np. Internet Explorer) i Gecko (np. Firefox), zgłaszane jest istnienie długich opisów. Można również otworzyć długi opis w nowym oknie naciskając NVDA+d. (#809)
* Wypowiadane są powiadomienia w Internet Explorer 9 i wyższych (takie jak blokowanie treści, albo pobieranie pliku). (#2343)
* Automatyczny odczyt nagłówków kolumn i wierszy tabeli jest obsługiwany dla dokumentów trybu czytania w Internet Explorer i innych kontrolkach MSHTML. (#778)
* Nowe języki: aragoński, irlandzki
* Nowe tablice brajlowskie: Duński stopnia 2, Koreański  stopień 1. (#2737)
* Wsparcie dla monitorów brajlowskich połączonych przez bluetooth do komputerów, na których bluetooth obsługuje Bluetooth Stack for Windows firmy Toshiba. (#2419)
* Wybór portów dla monitorów Freedom Scientific.
* Wsparcie dla notatników z rodziny BrailleNote firmy Humanvare działających w roli terminala brajlowskiego dla programu odczytu ekranu. (#2012)
* Wsparcie starszych modeli Pappenmeyer Braillex. (#2679).
* Wsparcie dla wprowadzania znaków przy pomocy monitorów brajlowskich posiadających klawiatórę. (#808).
* Nowe ustawienie klawiatury, umożliwiające wybór czy NVDA  powinien przerywać mowę przy wpisywaniu znaków  i/lub klawisza Enter. (#698)
* Obsługa kilku przeglądarek opartych na Google Chrome: Rockmelt, BlackHawk, Comodo Dragon i SRWare Iron. (#2236, #2813, #2814, #2815)

### Zmiany

* Zaktualizowano liblouis braille translator to 2.5.2. (#2737)
* Układ klawiatury dla laptopa został całkowicie przeprojektowany, aby uczynić go bardziej intuicyjnym i jednolitym. (#804)
* Zaktualizowano syntezator eSpeak do wersji 1.47.11. (#2680, #3124, #3132, #3141, #3143, #3172)

### Poprawki błędów

* Klawisze szybkiej nawigacji przenoszące do poprzedniego i następnego separatora w trybie czytania, teraz działają w Internet Explorer i innych kontrolkach MSHTML. (#2781)
* Jeśli NVDA musi użyć eSpeak lub trybu "bez mowy" w związku z problemami uruchomienia skonfigurowanego syntezatora, skonfigurowane ustawienie nie jest zmieniane na zapasowy syntezator. Oznacza to, że od teraz skonfigurowany syntezator będzie użyty przy następnym uruchomieniu NVDA. (#2589)
* Jeśli NVDA musi użyć trybu "bez brajla" w związku z problemami uruchomienia skonfigurowanego monitora brajlowskiego, skonfigurowane ustawienie nie jest zmieniane na bez brajla. Oznacza to, że od teraz skonfigurowany monitor będzie użyty przy następnym uruchomieniu NVDA. (#2264)
* W trybie czytania w aplikacjach Mozilla, aktualizacje tabel są teraz prawidłowo odczytywane. Dla przykładu w zaktualizowanych komórkach współrzędne wiersza i kolumny są odczytywane i nawigacja w tabeli działa prawidłowo. (#2784)
* W trybie czytania w przeglądarkach internetowych, niektóre typy nienazwanych klikalnych obrazków są odczytywane. (#2838)
* Starsze i nowsze wersje SecureCRT są teraz obsługiwane. (#2800)
* Dla metod wprowadzania takich jak Easy Dots IME w XP, łańcuch odczytu jest obecnie prawidłowo anonsowany.
* Lista znaków kandydujących w metodzie wprowadzania Microsoft Pinyin dla języka chiński uproszczony w Windows 7 jest teraz prawidłowo odczytywana przy zmianie stron strzałkami w lewo i prawo, oraz po pierwszym otwarciu klawiszem Home.
* Jeśli zapisana jest wymowa znaku użytkownika, zaawansowane pole "zachowaj" nie jest usuwane. (#2852)
* Po wyłączeniu sprawdzania aktualizacji, NVDA nie musi być uruchomiony ponownie aby ta zmiana została w pełni uwzględniona.
* NVDA nie ma od teraz problemu z uruchomieniem jeśli dodatek nie może zostać usunięty w związku z używaniem folderu dodatku przez inną aplikację. (#2860)
* Nazwy stron w ustawieniach DropBoxmogą być teraz odczytywane w widoku ekranu.
* Jeśli język wprowadzania został zmieniony na inny niż domyślny, NVDA wykrywa prawidłowo klawisze poleceń i trybu pomocy.
* Dla języków takich jak niemiecki, w których znak + (plus)  jest pojedynczym klawiszem na klawiaturze, możliwe jest od teraz powiązanie komend z tym klawiszem przy użyciu słowa "plus". (#2898)
* W Internet Explorer i innych kontrolkach MSHTML, bloki cytatu są prawidłowo odczytywane. (#2888)
* Sterownik monitora HumanWare Brailliant BI/B series może być teraz wybrany gdy monitor jest podłączony przez Bluetooth, a nigdy nie był podłączony przez USB.
* Filtrowanie elementów w trybie czytania z tekstem napisanym dużymi literami, zwraca teraz  wyniki z pominięciem wielkości liter, zamiast pustej listy. (#2951)
* W przeglądarkach Mozilla, tryb czytania może być ponownie użyty, jeśli w punkcie uwagi znajduje się zawartość Flash. (#2546)
* Gdy używana jest tablica skrótów brajlowskich, przy włączonym rozwijaniu słowa pod kursorem do brajla komputerowego, kursor brajlowski jest prawidłowo ustawiany gdy umieszczony zostanie za słowem, w którym  jeden znak jest przedstawiany na kilku komórkach brajlowskich (np. znak dużej litery, znak cyfry etc.). (#2947)
* Zaznaczenie tekstu jest prawidłowo przedstawiane na monitorach brajlowskich w aplikacjach takich jak Microsoft word 2003 i pola edycji w Internet Explorer.
* Możliwe jest ponownie zaznaczanie tekstu w tył w Microsoft Word przy włączonym brajlu.
* Przy przeglądaniu lub kasowaniu znaków w kontrolce edycyjnej Scintilla, NVDA prawidłowo odczytuje znaki wielobajtowe. (#2855)
* Rozwiązany problem instalacji NVDA, gdy ścieżka profilu użytkownika zawierała niektóre znaki wielobajtowe. (#2729)
* Zgłaszanie grup dla kontrolek widoku listy (SysListview32) w 64-bitowych  aplikacjach, nie powoduje od teraz błędu.
* W trybie czytania w aplikacjach Mozilla , zawartość tekstowa nie jest od teraz traktowana jako edytowalna, co zdarzało się dawniej w rzadkich przypadkach. (#2959)
* W IBM Lotus Symphony i OpenOffice, przesuwanie kursora w razie potrzeby przemieszcza punkt przeglądu.
* Zawartość Adobe Flash jest teraz dostępna w Internet Explorer pod Windows 8. (#2454)
* Naprawiona obsługa Bluetooth dla monitora Papenmeier Braillex Trio. (#2995)
* Naprawiona niemożność używania niektórych głosów Microsoft Speech API version 5 takich jak głosy Koba Speech 2. (#2629)
* W aplikacjach używających Java Access Bridge, monitory brajlowskie są prawidłowo aktualizowane podczas ruchów kursora w polach edycji. (#3107)
* Obsługa punktu orientacyjnego formularz w dokumentach trybu czytania, które obsługują punkty orientacyjne. (#2997) 
* Sterownik syntezatora eSpeak teraz obsługuje bardziej odpowiednio odczyt znakami (np. ogłaszając nazwę lub wartość zagranicznej litery zamiast jej brzmienia lub nazwy ogólnej). (#3106)
* Rozwiązany problem błędu kopiowania ustawień użytkownika NVDA do użycia na ekranie logowania i innych zabezpieczonych ekranach, gdy ścieżka folderu użytkownika zawierała znaki inne niż ASCII. (#3092)
* NVDA nie zawiesza się, gdy używane jest wprowadzanie znaków azjatyckich w niektórych aplikacjach .NET. (#3005)
* Możliwe jest teraz używanie trybu czytania na stronach w Internet Explorer 10 w trybie zgodności; np. strona logowania [www.gmail.com](http://www.gmail.com). (#3151)

### Changes for Developers

* Braille display drivers can now support manual port selection. (#426)
 * This is most useful for braille displays which support connection via a legacy serial port.
 * This is done using the getPossiblePorts class method on the BrailleDisplayDriver class.
* Braille input from braille keyboards is now supported. (#808)
 * Braille input is encompassed by the brailleInput.BrailleInputGesture class or a subclass thereof.
 * Subclasses of braille.BrailleDisplayGesture (as implemented in braille display drivers) can also inherit from brailleInput.BrailleInputGesture. This allows display commands and braille input to be handled by the same gesture class.
* You can now use comHelper.getActiveObject to get an active COM object from a normal process when NVDA is running with the UIAccess privilege. (#2483)

## 2012.3

Najważniejsze nowości w tej wersji obejmują wsparcie dla wprowadzania znaków azjatyckich; eksperymentalną obsłógę ekranów dotykowych w Windows 8; zgłaszanie numerów stron, uleprzone wsparcie dla tabel w dokumentach Adobe Reader, komendy nawigacyjne dla tabel z punktem uwagi oraz kontrolek list; wsparcie dla kilku nowych monitorów brajlowskich oraz zgłaszanie nagłówków kolumn i linii w Microsoft Excel.

### nowe funkcje

* NVDA wspiera wprowadzanie znaków azjatyckich przy użyciu IME i usługi metod wprowadzania tekstu we wszystkich aplikacjach, włączając w to:
 * zgłaszanie i nawigację na listach znaków kandydujących;
 * zgłaszanie i nawigację wewnątrz łańcuchów wprowadzania;
 * obecność łańcuchów odczytu.
* Zgłaszanie podkreśleń i przekreśleń w dokumentach Adobe Reader. (#2410)
* Gdy włączona jest funkcja klawiszy trwałych w systemie Windows, klawisz NVDA zachowuje się jak każdy inny klawisz modyfikujący w rodzaju shift czy alt. Pozwala to używać go bez przymusu przytrzymywania go gdy zachodzi potrzeba jego użycia. (#230)
* Automatyczne zgłaszanie nagłówków kolumn i linii w MS Excel. NVDA+shift+c by ustawić nagłówek kolumny, NVDA+shift+r by ustawić nagłówek linii. Dwukrotne wciśnięcie tych klawiszy czyści zaznaczenie. (#1519)
* Wsparcie dla Hims Braille Sense, Braille Edge i Sync Braille. (#1266, #1267)
* Wsparcie dla powiadomień w windows 8. (#2143)
* Testowe wsparcie dla ekranów dotykowych komputerów działających pod Windows 8, włączając w to:
 * odczytywanie obiektu pod palcem podczas przesuwania po ekranie
 * wiele gestów dla komend nawigacji w strukturze obiektów, przeglądania tekstu i innych.
* Wsparcie dla VIP Mud. (#1728)
* Adobe Reader: jeśli tabela posiada streszczenie, zostanie ono odczytane. (#2465)
* Adobe Reader:  mogą być zgłaszane nagłówki kolumn i wierszy tabeli. (#2193, #2527, #2528)
* Nowe języki: Koreański, Nepalski, amharski, słoweński.
* NVDA czyta sugestje autouzupełniania adresów email w programie MS Outlook 2007. (#689)
* Nowe warianty głosu espeaka: gene, gene2. (#2512)
* Zgłaszanie numerów stron w Adobe Readerze. (#2534)
* W Reader XI, etykiety stron są oznajmiane, jeśli istnieją, odzwierciedlając zmiany numerowania stron w różnych sekcjach, etc. We wcześniejszych wersjach nie jest to możliwe i zgłaszane są sekwencyjnie numery stron.
* Możliwe jest zresetowanie konfiguracji NVDA do ustawień domyślnych przez trzykrotne wciśnięcie NVDA+ctrl+r lub wybranie odpowiedniego polecenia z menu. (#2086)
* Wsparcie dla monitorów seika 3, 4, 5 i Seika80 firmy Nippon Telesoft. (#2452)
* pierwsze i ostatnie górne przyciski routingu w monitorach Pac Mate i focus mogą zostać użyte do przewijania w tył i przód. (#2556)
* Dużo więcej funkcji jest obsługiwanych na monitorach Freedom Scientific Focus przy pomocy klawiszy advance bars, rocker bars i różnych kombinacji punktów brajlowskich dla przeprowadzenia typowych akcji. (#2516)
* W programach używających Iaccessible2, kolumny i linie tabel mogą być zgłaszane poza trybem przeglądania. (#926).
* Wstępna obsługa kontroli dokumentu w Microsoft Word 2013. (#2543)
* Wyrównanie tekstu może być teraz zgłaszane w aplikacjach używających IAccessible2 takich jak aplikacje Mozilla. (#2612)
* Gdy  w punkcie uwagi znajduje się wiersz tabeli, albo widok listy z wieloma kolumnami, możesz użyć komend nawigacji w tabeli aby uzyskać dostęp do pojedynczych komórek. (#828)
* Nowe tablice brajlowskie: estoński stopień 0, portugalski 8-punktowy brajl komputerowy, włoski 6-punktowy brajl komputerowy. (#2319, #2662)
* Jeśli NVDA jest zainstalowany w systemie, kliknięcie w eksploratorze windows na plik dodatku NVDA, powoduje automatycznie jego instalację. (#2306)
* Obsługa nowszych monitorów Papenmeyer BrailleX. (#1265)
* Informacja o pozycji na liście plików np. jeden z cztery, jest podawana w systemie windows7 i nowszych. Dotyczy to także dowolnych kontrolek UI Automation które to wspierają. (#2643)

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

Najważniejsze zmiany w tym wydaniu obejmują wbudowany instalator, możliwość tworzenia przenośnych kopii programu z poziomu menu, możliwość łatwego zarządzania dodatkami rozbudowującymi funkcjonalność programu, wsparcie dla grafiki w edytorze MS Word, wsparcie dla aplikacji metro w wsystemie MS Windows 8 i kilka innych poprawek.

### nowe funkcje

* NVDA potrafi automagicznie uaktualniać się do nowszej wersji (#73)
* Rozbudowa funkcjonalności screenreadera została ułatwiona przez wsparcie zewnętrznych dodatków, którymi można zarządzać z menu narzędzia. Dodatki są to zarówno wtyczki, jak i nowe sterowniki monitorów brajlowskich. Manager dodatków nie pokazuje jednak wtyczek, które zostały zainstalowane wg starszej metody tzn przez skopiowanie plików wtyczek do katalogu konfiguracji użytkownika. (#213)
* Zainstalowana wersja NVDA jest bardziej funkcjonalna pod kontrolą Win 8. Dotyczy to wypowiadania wprowadzanych znaków i wsparcia dla metro'wej wersji Internet Explorer. Wersje przenośne nie wspierają aplikacji metro. (#1801)
* W dokumentach wymagających aktywacji trybu przeglądania (ie, Firefox, itd) możliwe jest przechodzenie do końca i początku elementu zawierającego typu lista, tabela za pomocą klawiszy przecinka i odpowiednio shift+ przecinek. (#123)
* Wsparcie dla języka greckiego.
-  Grafika i tekst alternatywny są zgłaszane w dokumentach MS word (#2282, #1541)

### Zmiany

* NVDA jest teraz rozpowszechniany wyłącznie w jednym pakiecie instalacyjnym, po uruchomieniu którego użytkownik może samodzielnie utworzyć wersję przenośną bądź zainstalować screenreader. (#1715)

### Changes for Developers

* Due to the replacement of the previous NSIS installer for NVDA with a built-in installer in Python, it is no longer necessary for translaters to maintain a langstrings.txt file for the installer. All localization strings are now managed by gettext po files.

## 2012.1

### Nowe funkcje

* Wsparcie dla odczytu wcięć. Opcja w ustawieniach formatowania dokumentu.
* NVDA potrafi wykryć wciśnięcia klawiszy generowane przez alternatywne metody emulowania standardowego wejścia jak klawiatóra ekranowa, czy oprogramowanie rozpoznawania głosu.
* Program potrafi oznajmiać kolor tekstu także w terminalu tekstowym.
* Stan czcionki jak pochylenie, pogrubienie teraz pokazywany jest także w brajlu. (#538)
* Zaznaczony tekst od teraz wyświetlany jest w brajlu po przez punkty 7 i 8. (#889)
* Na monitorach brajlowskich wyświetlane są informacje o kontrolkach wewnątrz dokumentów jak linki, przyciski czy nagłówki. (#202)
* Wsparcie dla linijki hedo ProfiLine. (#1863)
* Nvda unika rozdzielania słów w brajlu, gdy jest to możliwe. (#1890)
* Nowa opcja w ustawieniach brajla konfigurująca przeglądanie tekstu wg akapitów. (#1891)
* W trybie przeglądania można aktywować obiekt używając monitora brajlowskiego, poprzez wciśnięcie cursor routingu na obiekcie pod kursorem. Jeśli kursor nie znajduje się jeszcze na obiekcie, wciśnij klawisz dwukrotnie. (#1893).

### zmiany

* Literowanie fonetyczne odbywa się w języku zdefiniowanym przez twórcę dokumentu, gdy włączono automatyczną zmianę języka i gdy informacje o nim zostały zdeklarowane w tym dokumencie.

### Poprawki

* W Windows 8, nvda utrzymuje już punkt uwagi w polu wyszukiwarki. Wcześniej przenosił się on po za to pole, co czyniło ją niedostępną.
* Tryb przeglądania jest używany także dla pełnoekranowej zawartości adobe flash.
* Jakość dźwięku syntezatorów sapi 5, gdy urządzenie wyjściowe ustawione zostanie na kartę inną od domyślnego mapowania dźwięku windows powinna być leprza. (#749)

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

= 2011.3 =
Najważniejsze cechy tego wydania to dodana funkcjonalność automatycznej zmiany języka syntezatora mowy zgodnie z językiem czytanego dokumentu o ile zawiera on odpowiednie informacje o języku, wsparcie dla 64 bitowych wersji java runtime environment, odczyt informacji formatowania w trybie przeglądania (mozilla), leprza obsługa braku odpowiedzi aplikacji oraz pierwsze przymiarki do wsparcia dla windows8.

### Nowe Funkcje

* W trakcie czytania dokumentu pdf/przeglądania strony www z odpowiednio zdeklarowanym językiem zawartości, nvda może zmieniać język syntezatora e-speak w locie. Oznacza to, że gdy czytany dokument napisano np. w języku angielskim i zostało to odpowiednio zadeklarowane przez jego twórcę, nvda przełączy się na angielski głos syntezatora e-speak. Funkcja ta może zostać wyłączona lub włączona na rządanie, przy użyciu odpowiednich pól wyboru w oknie ustawienia głosu. (#845)
* Java Access Bridge 2.0.2 jest już wspierany. Zarówno w wersji 32, jak i 64 bitowej.
* Poziomy nagłówków w dokumentach gecko np. firefox, są odczytywane także przez nawigację obiektową.
* Informacje o formatowaniu tekstu są dostępne również w trybie przeglądania. Dotyczy to programów Mozilla Firefox, Thunderbird). (#394)
* Program automatycznie wykrywa i zgłasza przekreślenia w tekście kontrolek aplikacji opartych o IAccessible2 , jak np. w produktach Mozilli.
* NVDA zgłasza liczbę linii i kolumn tabel w programie Adobe Reader.
* Dodano wsparcie dla syntezatorów działających pod Microsoft Speech Platworm. (#1735)
* Program zgłasza liczbę stron i linii podczas ruchów kursora w IBM Lotus Symphony. (#1632)
* W oknie 'ustawienia głosu' dodano pole, w którym użytkownik może określić stopień zmiany wysokości głosu dla wielkich liter. Opcja ta zastępuje pole wyboru 'wyższy głos dla wielkich liter'. Aby wyłączyć tę funkcjonalność, wpisz 0.
* Kolor tekstu i tła jest już zgłaszany w informacji o formatowaniu komórek podczas pracy z Microsoft Excel. (#1655)
* W aplikacjach do których użycia konieczny jest Java Access Bridge, komenda aktywująca obiekt nawigacyjny działa prawidłowo. (#1744)
* Podstawowe wsparcie dla Design Science MathPlayer.

### Zmiany

* NVDA restartuje się samodzielnie, gdy wykryje swoje zawieszenie.
* Skrócono niektóre informacje pokazywane w braille'u. (#1288)
* Udoskonalono komendę odczytu zawartości aktywnego okna (NVDA+b). Nie powinna już odczytywać nie potrzebnej zawartości okien i czytanie powinno być łatwiejsze do przerwania. (#1499).
* Automatyczny odczyt całej zawartości stron w trybie przeglądania jest teraz opcjonalny i konfigurowalny z zakładki 'ustawienia trybu przeglądania'. (#414).

### Poprawki

* NVDA nie pokazuje wypunktowań lub numeracji w listach na stronach prezentowanych przy użyciu Internet Explorer, gdy autor zadeklarował, że nie powinny być widoczne. (#1671).
* Restart NVDA, którego przyczyną było zawieszenie się programu, wykonany przy użyciu skrótu klawiszowego uruchamiającego screenreader, nie powinien kończyć się jego zamknięciem bez wznowienia działania.
* Wciśnięcie klawisza backspace lub którejś ze strzałek nie będzie się już kończyć dziwnymi efektami w pewnych przypadkach. (#1612)
* Elementy list rozwijanych, nie dające możliwości edycji tekstu powinny być prawidłowo zgłaszane przez program.
* Możliwa jest nawigacja po liniach rozpoczynając od linii nagłówka w programie Adobe Reader. Linia nagłówka nie jest już także odczytywana jako zerowa. (#1731)
* Możliwa jest nawigacja do pustej linii w tabelach Adobe Reader.
* Nic nie znaczące informacje o pozycji kursora, np. zero z zero, nie są wyświetlane w braille'u.
* Gdy brajl związany jest z przeglądem, NVDA może pokazywać także zawartość w poziomie przeglądu. (#1711)
* Tekst kontrolek nie jest już przedstawiany w brajlu dwukrotnie w niektórych sytuacjach.
* Wciśnięcie przycisku słurzącego do wysłania pliku w trybie przeglądania Internet Explorer, otwiera okno dialogowe słurzące do wyboru wysyłanego pliku, zamiast jedynie wychodzić z trybu formularza. (#1720)
* Dynamiczne zmiany w konsoli tekstowej nie są zgłaszane, gdy dla okna terminala włączono tryb uśpienia. (#1662)
* Udoskonalono polecenia rozwinięcia i zwinięcia list rozwijalnych w trybie przeglądania. (#1630)
* Powinno zdarzać się mniej sytuacji, w których stabilność NVDA zależy od aktywnej aplikacji i jej zawieszenie powoduje równierz zawieszenie screenreadera. (#1408)
* NVDA nie odmawia renderowania tekstu w trybie przeglądania Mozilla Firefox w pewnych specyficznych sytuacjach. (#1373)

### Changes for Developers

* NVDA can now instruct speech synthesizers to switch languages for particular sections of speech.
 * To support this, drivers must handle speech.LangChangeCommand in sequences past to SynthDriver.speak().
 * SynthDriver objects should also provide the language argument to VoiceInfo objects (or override the language attribute to retrieve the current language). Otherwise, NVDA's user interface language will be used.

## 2011.2

Najważniejsze zmiany dotyczą obsłógi znaków interpunkcyjnych i innych symboli. Użytkownik może skonfigurować próg odczytywania znaków interpunkcyjnych. Dodano możliwość tworzenia własnych etykiet symboli, obsłógę alfabetu fonetycznego. Poprawiono komendę czytaj wszystko, wsparcie dla aria w Internet Explorer, leprza obsłóga dokumentów pdf. NVDA jest w stanie odczytać tekst wypisywany na ekran w większej ilości aplikacji, włączając w to informacje formatowania.

### nowe funkcje

* Zaimplementowano do programu możliwość fonetycznego przeliterowania konkretnego znaku przez dwukrotne wciśnięcie klawisza odczytu znaku. W przypadku języka angielskiego jest to alfabet fonetyczny. Możliwe jest także przeliterowanie konkretnego słowa lób linii, przez trzykrotne wciśnięcie odpowiednich klawiszy poleceń NVDA. (#55)
* W poziomie przeglądu można odczytać więcej tekstu, zwłaszcza w aplikacjach wypisujących go na ekran bezpośrednio.
* Użytkownik programu może ustawić najniższy próg odczytu znaków interpunkcyjnych i innych symboli. (#332)
* Gdy znaki interpunkcyjne lób inne symbole wystąpią jednocześnie więcej niż 4 razy, odczytywana jest ich liczba. (#43)
* Dodano tabele brajlowskie dla języków: Norweski ośmiopunktowy brajl komputerowy, etiopski I stopień, Słoweński I stopień, Serbski I stopień. (#1456)
* Mowa nie przerywa się już nienatóralnie na końcu każdej linii gdy używamy komendy czytaj wszystko. (#149)
* NVDA zgłasza uporządkowanie elementów zgodnie z odpowiednią właściwością ARIA w przeglądarkach internetowych. (#1500)
* Wzorce brajlowskie we formacie unicode są wyświetlane prawidłowo. (#1505)
* Lepsza obsługa właściwości ARIA na stronach internetowych.
* Użytkownicy mogą zmieniać wymowę znaków interpunkcyjnych i innych znaków, i ustawić najniższy próg ich odczytywania. (#271, #1516)
* Odczytywana jest nazwa aktywnego arkusza w Microsoft Excel, gdy przełączamy się między nimi wciskając ctrl+page up, ctrl+page down. (#760)
* Przy nawigacji po tabeli w Microsoft Word, NVDA odczytuje aktywną komórkę.
* Odczyt współżędnych komórki tabeli jest teraz konfigórowalny z okna formatowanie dokumentów. (#719)
* NVDA potrafi odczytać info o formatowaniu oraz kolorze tekstu wypisywanego na ekran.
* W outlook Express, Windows Mailu i Windows Live Mailu, NVDA zgłasza, że wiadomość została, lub nie została przeczytana, oraz czy wątek został rozwinięty lub zwinięty. (#868)
* E-speak posiada funkcję "podkręć prętkość", która wielokrotnie podnosi szybkość mówienia.
* Dodano wsparcie dla kontrolki kalendarza na zegarze systemowym w Windows 7. (#1637)
* Dodano nowe skróty klawiszowe dla monitora MDV Lilli. (#241)
* Przetłumaczono program na Albański i Bułgarski.

== Zmiany ==
* Aby przesunąć karetkę systemową do kursora przeglądu, od teraz należy wcisnąć dwukrotnie: w przypadku komputera PC NVDa+shift+minus numeryczny, w przypadku laptopa NVDA+shift+backspace. Zwalnia to nieco miejsca na klawiatórze. (#837)
* Aby usłyszeć wartości dziesiętne i szesnastkowe dla znaku, wciśnij trzykrotnie komendę odczytu znaku. Dwukrotne jej wciśnięcie od teraz literuje znak.
* Zaktualizowano syntezator mowy espeak do wersji 1.45.03. (#1465).
* Układ tabel nie jest już przedstawiany w dokumentach gecko przy przesówaniu punktu uwagi poza dokumentem.
* Dokumenty będące aplikacjami ARIA, czytane są prawidłowo gdy korzystamy z Internet Explorer. (1452)
* Zaktualizowano liblouis do 2.3.0.
* Paski postępu, są zgłaszane w trybie przeglądania.
* Interfejs programu, a także jego dokumentacja dotychczasowy termin wirtualny bufor zastępują nowym określeniem tryb przeglądania, jako że pojęcie wirtualnego bufora nie znaczy zbyt wiele dla zwykłych użytkowników. (#1509)
* Gdy użytkownik będzie chciał skopiować swoje ustawienia do profilu systemowego w celu użycia ich na ekranie logowania i innych bezpiecznych ekranach Windows, a w katalogu ustawień zostaną wykryte wtyczki, pojawi się ostrzeżenie, że mogą one stanowić zagrożenie dla bezpieczeństwa systemu. (#1426)
* Pod windows XP i Windows Vista, NVDA nie używa technologii UI automation, nawet gdy jest dostępna. Użycie UI automation może przyczynić się co prawda do poleprzenia dostępności niektórych nowoczesnych aplikacji, jednak powoduje zbyt wiele problemów ze stabilnością screenreadera pracującego pod kontrolą tych systemów. (#1437)
* W aplikacjach Mozilla Gecko, zawartość dokumentów takich jak strony internetowe może być przeglądana przez użytkownika, zanim zostanie wczytana w całości

### Poprawki

Rozwijanie list rozwijanych w wirtualnych buforach zostało wymuszone przy pomocy skrótu nvda+spacja. Program w takim polu nie powróci automatycznie do trybu przeglądania. (#1386)

* W dokumentach gecko i mshtml program renderuje poprawnie teksty jednowierszowe, które do tej pory były umieszczane w dwuch oddzielnych liniach. (#1378)
* Gdy brajl jest związany z kursorem przeglądu, i gdy obiekt w hierarchii nawigacji przenosi się do wirtualnego bufora jak strona www, wiadomość w programie pocztowym, dokument pdf czy to ręcznie, czy to przez zmianę punktu uwagi, zawartość bufora jest już wyświetlana na monitorze brajlowskim. (#1306, #1307)
* Niektóre znaki interpunkcyjne nie będą już odczytywane przez pewne syntezatory  gdy ich odczyt zostanie wyłączony. (#332)

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

### nowe funkcje

* Nvda potrafi podać kolor dla niektórych kontrolek. Automatyczne odczytywanie można skonfigurować w oknie ustawień formatowania dokumentu. Kolor może być odczytany równierz na żądanie przez komendę odczytu info o formatowaniu nvda +f.
* W  wirtualnych buforach, można nawigować po stronach dokumentu używając shift +page up lub page down, oraz po jego akapitach (shift+ctrl+strzałka w górę shift+ctrl+strzałka w duł (#639)
* Screenreader odczytuje już automagicznie nowy tekst w putty, Mirc'u, tera term i secureCRT (#936) 
* Użytkownik może tworzyć własne, lub modyfikować istniejące skróty klawiszowe poleceń nvda, przez utworzenie pliku mapy gestór (#194)
* Dodano obsługę globalnych wtyczek mogących rozszerzać funkcjonalność programu. (#281)
* Gdy włączony jest capslok i zostanie wprowadzony znak z shiftem, generowany jest dźwięk. Zachowanie to można zmienić używając stosownej opcji w oknie ustawień klawiatury. (#663)
* Podział strony jest już ogłaszany w Wordzie przy nawigacji po liniach (#758)
* Wypunktowanie tekstu wraz z numerami jest już czytane w Wordzie przy nawigacji po liniach (#208)
* Dodano wsparcie dla samo gadających programów, posiadających własne udźwiękowienie jak np. klango  tzn. tryb uśpienia. Tryb uśpienia ustawiony dla konkretnego programu powoduje, że nvda w oknie danej aplikacji milknie dopóki nie opuścimy takiego programu. Tryb ustawia się skrótem nvda+shift+s w oknie samo gadającej aplikacji. Aby wyłączyć tryb uśpienia dla konkretnego programu, naciśnij skrót ponownie w jego oknie.
* Dodano nowe skróty klawiszowe dotyczące monitorów brajlowskich. Aby poznać szczegóły przeczytaj rozdział wspierane monitory brajlowskie w podręczniku użytkownika. (#209)
* Dla wygody developerów nie związanych oficjalnie z nvda, zarówno globalne wtyczki, jak i modóły aplikacji mogą zostać przeładowane bez konieczności restartu nvda. Aby przeładować wtyczki i modóły, użyj odpowiedniej komendy w menu narzędzia lub skrótu nvda+ctrl+f3. (#544)
NVDA zapamiętuje pozycję użytkownika na poprzednio odwiedzanej stronie internetowej. Funkcja działa dopuki nie zamkniesz przeglądarki lub screenreadera. (#132)
Monitory brajlowskie firmy Handy tech mogą być używane bez konieczności instalowania uniwersalnego sterownika Handy Tech. (#854)
* Dodano wsparcie dla kilku monitorów brajlowskich firm baum, humanware i APH. (#937).
* Poprawiono obsłógę paska statusu Media Player classic home cinema.
* Monitora brajlowskiego Freedom Scientific Focus 40 Blue , można urzywać przy pomocy bluetooth. (#1345

### zmiany

* W angielskiej wersji programu opcja pomoc klawiatury zmieniła nazwę na pomoc wprowadzania. Uwzględnia to fakt, że istnieją także inne źródła wejścia. Gdy program zacznie to wspierać bardziej kompleksowo, można będzie dokonać stosownych zmian. 
* Nvda nie podaje już nie istotnych i zagadkowych dla zwykłego użytkownika informacji o lokalizacji skryptu w kodzie programu w trybie pomocy klawiatury.
* Program nie przepuszcza już klawisza nvda gdy wykryje swoje zawieszenie. Zapobiega to przypadkowemu włączaniu i wyłączaniu capslocka w sytuacji, gdy użytkownik nie zda sobie sprawy, że zamilknięcie mowy to problem screenreadera, nie systemu czy aktywnego programu. (#939) 
* W trybie przepuszczania następnego klawisza, nvda uwzględnia już skróty klawiszowe i wyjdzie z niego dopiero, gdy zostanie puszczony ostatni klawisz. Dotyczy to także powtórzeń naciśnięć np. w skrócie.
* Gdy dwukrotnie, w szybkim odstępie wciśniemy klawisz nvda i przytrzymamy go, następny klawisz zkąbinowany z nvda także zostanie przepuszczony nawet, gdy jest to skrót programu.
* W pomocy klawiatury, odczytywane są  także klawisz wyciszający, głośniej i ciszej.

### Poprawki

* Zmieniono nazwę okna edycji słownika na dodaj wpis słownika, zamiast edytuj wpis słownika. (#924)
* W oknach słowników, wyrażenia regularne są pokazywane w języku użytkownika, nie zawsze w angielskim.
* W AIM, informacje pozycji nie są czytane w przypadkach, gdy często są nie prawidłowe.
* W oknie ustawień głosu, klawisze strzałek, home end, page up down użyte na sówakach zmieniają parametry głosu. (#221)
* W pomocy klawiatury, znaki interpunkcyjne są czytane nawet, gdy w konfiguracji ich odczyt został wyłączony. (#977)
* W ustawieniach układu klawiatury, nazwy układów pokazywane są w języku użytkownika, nie zawsze tylko po angielsku. (#558)
* Poprawiono błąd polegający na renderowaniu niektórych elementów jako puste w dokumentach adobe readera, np. linki w tabelach podręcznika Apple ifone os4.
* Opcja użycia własnych ustawień na bezpiecznych oknach w stylu (UAC)  działa już prawidłowo. (#1194)
* W systemach z aktywnym UAC, wzmiankowana opcja nie zawodzi, gdy nazwa użytkownika zawiera spacje. (#918)
* W kontrolkach opartych o mshtml i w Internet Explorer, nvda używa url by określić zawartość linku, zamiast prezentować puste obiekty (#633)
* Program nie ignoruje już punktu uwagi w menu komunikatora AOL7. (#655)
* Nvda ogłasza już prawidłowo etykiety błędów występujące w module sprawdzania pisowni Worda. Np. nie ma w słowniku, zbędny odstęp itd. Poprzednio wszystko było czytane jako błąd gramatyczny. (#883)
* Pisanie w MS Word przy użyciu monitora brajlowskiego nie powoduje już wprowadzania dziwnych znaków przeinaczających tekst i osobliwego zawieszania się programu podczas użycia kursor routingów w trakcie pracy z MS_word. (#1212)
Problemu nie rozwiązano dla języka arabskiego, w którym nadal nie można czytać tekstu przy użyciu monitora brajlowskiego. (#627)
* Kursor na monitorze brajlowskim powinien teraz być uaktualniany odzwierciedlając zmiany po wciśnięciu klawisza del w polu edycyjnym. (#947)
* Dynamiczne zmiany w dokumentach gecko2 np. firefox4 są uwzględniane przez nvda, nawet gdy otwartych zakładek jest więcej. Poprzednio uwzględniane były tylko zmiany w pierwszej. (Mozilla bug 610985)
* Nvda czyta prawidłowo sugestie dotyczące błędów gramatycznych i interpunkcyjnych w wordowskim module sprawdzania pisowni. (#704)
* NVDA nie przedstawia już kotwic przeznaczenia jako pustych linków w wirtualnych buforach kontrolek MSHTMl i internet explorer. Kotwice takie teraz są ukrywane, tak jak być powinno. (#1326)
* Nawigacja po obiektach wewnątrz standardowych pól rozwijanych nie jest już niesymetryczna.
* NVDA nie zawiesza się gdy napotyka na ramkę pomocniczą w dokumentach gecko, gdy wcześniej wczytywał zewnętrzną stronę.
* Program właściwie odczytuje następny znak, gdy znaki są usówane przy użyciu numerycznego delete. (#286)
* Na ekranach logowania systemu Windows XP, NVDA ponownie odczytuje nazwę użytkownika, gdy wybrany użytkownik jest zmieniany.
-  Poprawiono błąd odczytu na konsolach tekstowych gdy włączono odczyt numerów linii.
* Lista elementów dla wirtualnych buforów jest użyteczna dla osób widzących. Wszystkie elementy są widoczne na ekranie. (#1321). Podobna poprawka dotyczy również listy wpisów słowników.
* W monitorach brajlowskich ALVA BC640/BC680, NVDA nie lekceważy już klawiszy będących wciśniętymi w chwili, gdy inne w danym momencie są puszczane.
* NVDA przełącza się na odpowiedni monitor brajlowski gdy załadowana została domyślna konfiguracja. (#1346)
* Kreator projektu w Visual studio 2008 jest znowu odczytywany. (#974).
* Screenreader nie odmawia już posłuszeństwa w programach, zawierających znaki z poza tablicy askey w nazwie swojego pliku wykonywalnego. (#1352).
* Program nie czyta już pierwszego znaku następnej linii na końcu aktualnie odczytywanej pod czas pracy z akel padem w trybie zawijania słów.
* Screenreader nie odczytuje już całego tekstu kodu w Visual studio 2008 i 2005 przy próbie wprowadzenia jakiego kolwiek znaku. (#975)
* Punkt uwagi pojawiający się jako pierwszy, nie jest odczytywany dwa razy gdy NVDA wystartuje. (#1359)

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

#### 2010.2

Najistotniejsze zmiany dotyczą nawigacji w obiektach, która została w znacznym stopniu uproszczona. Wirtualne bufory działają teraz także dla adobe flash. Nvda odczytuje niedostępne do tej pory kontrolki, dodano możliwość przeglądania zawartości ekranu z użyciem tzw. poziomu przeglądu, wsparcie dla dokumentów IBM Lotus Symphony, odczytywanie nagłówków tabel i ich linii w przeglądarce mozilla firefox oraz znacznie udoskonalono podręcznik użytkownika.

## nowe funkcje

* Nawigowanie po obiektach przy pomocy kursora przeglądu zostało znacznie uproszczone. Pomijane są te obiekty, które nie mają żadnego znaczenia dla użytkownika.
* W aplikacjach używających java access bridge, jak open office, informacje o formatowaniu są odczytywane w kontrolkach tekstowych. (#358)
* Nvda właściwie odczytuje komórki w Microsoft Excel, gdy poruszamy się przy pomocy myszy.
* W aplikacjach używających java access bridge, odczytywane są okna dialogowe. (#554)
* Wspierane są dokumenty adobe flash i ich kontrolki, dostępny jest także tryb formularza. (#453)
* Edytowalne obiekty w środowisku eclipse, jak np. edytor kodu są już wspierane, warunkiem jest użycie eclipse w wersji 3 lub wyższej. (#256)
* Nvda potrafi pobrać większość tekstu z ekranu. (#40, #643)
Pozwala to na odczytywanie kontrolek, których zawartości nie da się pokazać w sposób bardziej bezpośredni.
W ten sposób stały się dostępne niektóre elementy pokazujące ikony jak np. menu otwórz za pomocą w Windows XP (#151), pola tekstowe w aplikacjach Windows live (#200), lista błędów w programie Outlook Express (#582), edytowalne kontrolki tekstowe w textpadzie (#605), listy w programie eudora, wiele elementów w australijskim E-Tax, pasek formuły w Microsoft Excel.
* Nvda wspiera edytor kodu w Microsoft Visual studio 2005 oraz 2008 wymagana jest przynajmniej wersja standard. (#457)
* Dodano wsparcie dla dokumentów pakietu IBM Lotus Symphony. (#457)
* Nvda obsługuje eksperymentalnie Google Chrome. Trzeba jednak zaznaczyć, że wsparcie dla screenreaderów ze strony tej przeglądarki nie jest zbyt kompletne i być może potrzeba będzie dodatkowej pracy po stronie nvda. Jeśli mimo to chcesz wypróbować jak to działa, potrzebujesz najnowszej wersji rozwojowej zarówno screenreadera, jak i przeglądarki.
* Stan klawiszy caps lok, num lock i scrol lock jest prezentowany w brajlu, gdy są wciskane. (#620)
* Dymki pomocy pokazywane są w brajlu zaraz po pojawieniu się. (#652)
* dodano sterownik dla monitora brajlowskiego MDV Lilli. (#241)
* Nvda odczytuje nowe zaznaczenie podczas wyboru kolumny lub linii w MS Excel przy pomocy skrótów shift+spacja i ctrl+spacja. (#759)
* Czytane są nagłówki tabel oraz ich kolumny. Zachowanie takie można ustawić z menu ustawienia, formatowanie dokumentów.
Aktualnie wspierane jest to w dokumentach mozilli, tj. firefox 3.6.11 i wyżej i thunderbird 3.1.5 i wyżej. (#361)
* Opisano polecenia poziomu przeglądu. (#58)
Nvda+numeryczne 7 przełącza do poziomu przeglądu umieszczając kursor przeglądu w pozycji aktualnego obiektu, pozwalając na obejrzenie zawartości całego ekranu za pomocą strzałek.
* Aktualne ustawienia użytkownika mogą być użyte na ekranach zabezpieczonych w stylu UAC, ekran logowania użytkownika) (#730)
* wsparcie dla firefox 4 i Internet Explorer 9.

### zmiany

* Komendy nvda+numeryczny plus, nvda+shift+numeryczne 6 oraz nvda+numeryczne 4 zostały usunięte ze względu na ich nieprawidłowe działanie oraz w celu zwolnienia klawiszy na inne przyszłe polecenia.
* W oknie wyboru syntezatora, pokazywane są prawidłowe nazwy syntezatorów. Wcześniej były one poprzedzane nazwami sterowników.
* Podgląd logu i konsola pythona są maksymalizowane po aktywacji.
* W excelu, czytany jest cały zaznaczony obszar, nie tylko aktywna komórka w przypadku gdy zaznaczonych jest więcej. (#763)
* Zablokowana została możliwość zmiany ważnych ustawień konfiguracyjnych na ekranach logowania do systemu i innych bezpiecznych ekranach
* Zaktualizowano espeaka do wersji 1.44.03.
* Gdy nvda jest już uruchomiony, wciśnięcie klawisza skrótu uruchamiania programu  lub jego wybranie z pulpitu restartuje screenreader.
* Usunięto opcję "czytaj tekst pod myszą" w stosownych ustawieniach i zastąpiono ją śledzeniem myszy, co lepiej oddaje  zachowanie nvda po wciśnięciu nvda+m.
* Zaktualizowano układ klawiatury dla laptopa. Uwzględnia on teraz wszystkie polecenia dostępne w wersji dla komputerów stacjonarnych i działa prawidłowo w przypadku użycia klawiatur innych niż angielska. (#798, #800)
* Udoskonalono i zaktualizowano dokumentację, w której uwzględniane są już skróty w układzie dla laptopów  oraz dokonano jej synchronizacji z trybem pomocy klawiatury. (#455)
* Zaktualizowano liblouis do 2.1.1. Naprawia to problemy z brajlem chińskim oraz znakami niezdefiniowanymi w tabeli. (#484, #499)

#### poprawki

* W programie utorrent, elementy listy torrentów nie są już powtarzane bez końca i nie zatrzymują punktu uwagi pomimo otwarcia menu. Odczytywana jest także lista plików stanowiących zawartość torrenta.
* W firefoxie, punkt uwagi jest już prawidłowo wykrywany gdy dostanie się wewnątrz pustej tabeli lub drzewa.
* W firefoxie, niezaznaczone kontrolki jak zaznaczalne komórki tabel są prawidłowo ogłaszane. (#571)
* Okna ARIa nie są już ignorowane i jeśli prawidłowo zaimplementowane, będą już odczytywane we firefoxie w chwili ukazania się. (#640)
* W Internet Explorer i innych kontrolkach opartych o mshtml, atrybut ARIA level jest interpretowany prawidłowo.
* Nvda nie powoduje już zawieszania się Internet explorera, gdy nawigujemy po ramkach.
* W Wordzie, można ponownie odczytywać tekst pisany od prawej do lewej, np. tekst arabski. (#627)
* Zauważalnie zredukowano opóźnienie, gdy w konsoli na systemach 64bitowych pojawi się znaczna ilość tekstu. (#622)
* Gdy skype jest już uruchomiony w chwili startu nvda, nie jest już konieczny restart skype aby nvda zaczął go obsługiwać. Może to działać także dla innych aplikacji, wykrywających obecność screenreaderów w systemie.
* W aplikacjach MS office, nvda nie zawiesza się po użyciu komendy nvda+b lub gdy nawiguje się po niektórych paskach narzędziowych. (#616)
* Nvda prawidłowo odczytuje liczby, w których po przecinku występuje zero np. 1,023. (#593)
* Adobe Acrobat Pro i Reader 9 nie zawieszają się już podczas zamykania dokumentów lub wykonywania pewnych innych zadań. (#613)
* Zaznaczenie jest już ogłaszane gdy użyje się klawisza skrótu ctrl+a w polach edycyjnych lub dokumentach Ms word. (#761)
* W notatniku tekst nie jest już nieprawidłowo zaznaczany, gdy nvda przesuwa kursor np. pod czas komendy czytaj wszystko (nvda+strzałka w dół). (#746)
* Znów można oglądać zawartość komórek w MS Excel używając kursora przeglądu.
* Nvda ponownie może czytać po liniach w niektórych problematycznych polach edycyjnych w Internet Explorer 8. (#467)
* Windows live Messenger 2009 nie zamyka się już natychmiast po starcie nvda. (#677)
* Nie jest już konieczne użycie klawisza tab by skorzystać z zagnieżdżonego obiektu np.  aplikacji flashowych po wciśnięciu entera wewnątrz takiego obiektu lub w czasie powrotu z innego podobnego. (#755)
* W notepad ++, początki długich linii nie są już obcinane. Są także prawidłowo pokazywane na monitorach brajlowskich.
* W loudtalks'ie, dostępna jest lista kontaktów.
* Url dokumentu internet Explorer i procedury msaahtml  nie są nieprawidłowo odczytywane. (#811)
* W środowisku Eclipse, element posiadający wcześniej punkt uwagi nie jest już nieprawidłowo odczytywany, gdy został już wybrany następny.
* Gdy w MS Word użyjemy komendy nawigacji po tabelach kiedy kursor jest poza nią, nie jest już wypowiadany komunikat "koniec tabeli" wygłoszony zaraz po "poza tabelą". (#921)
* W MS Word, komunikat "koniec tabeli" wypowiadany jest w języku użytkownika, nie zaś wyłącznie po angielsku. (#921)
* Stan pul wyboru jest już podawany w regułach filtrowania MS Outlook Express, Windows mailu i Windows Live Mailu. (#576)
* W Windows Live Mailu 2010 odczytywane są opisy reguł wiadomość.

## 2010.1

To wydanie koncentruje się przede wszystkim na usuwaniu błędów i usprawnień dla użytkowników, w tym kilka istotnych poprawek stabilności.

### Nowe funkcje

-  Zostało dodane pole wyboru punktów orientacyjnych w oknie ustawień formatowania dokumentu, które pozwala skonfigurować NVDA do ogłaszania punktów orientacyjnych w dokumentach i stronach internetowych. W celu zapewnienia zgodności z poprzednimi wersjami, opcja ta jest włączona domyślnie.
-  Jeśli będzie aktywne odczytywanie klawiszy poleceń, NVDA będzie ogłaszać na wielu klawiaturach nazwy klawiszy multimedialnych, gdy zostaną naciśnięte (np. Play, Stop, strona domowa, itp.). (#472)
-  Po naciśnięciu kombinacji klawiszy kontrol+Backspace NVDA wypowiada usuwane słowa, ale tylko tam gdzie jest to obsługiwane. (# 491)
-  Klawisze strzałek mogą być teraz używane w oknie Web formatora do nawigacji i czytania tekstu. (# 452)
-  Lista pozycji w książce adresowej programu Microsoft Office Outlook jest już obsługiwana.
-  NVDA lepiej obsługuje pole edytowalne (tryb projektu) dokumentów w programie Internet Explorer. (# 402)
-  Nowy skrypt (NVDA+Shift+numpad Minus) pozwala przenieść fokus do bieżącego obiektu systemu.
-  Nowe skrypty do blokowania i odblokowywania lewego i prawego przycisku myszki. Przydatne do wykonywania operacji przeciągnij i upuść. shift+numpad slash, aby zablokować / odblokować lewy przycisk. Shift+numpad gwiazdka, aby zablokować / odblokować prawy przycisk.
-  Nowe tłumaczenia tabel Braille'a: niemiecki 8 punktowy Braille komputerowy, niemiecki klasa 2, fiński 8 punktowy Braille komputerowy. chiński (Hong Kong, kantoński), chiński (Tajwan, Manderin). (# 344, # 369, # 415, # 450)
-  Obecnie możliwe jest wyłączenie tworzenia skrótu na pulpicie (a także klawisza skrótu) podczas instalacji NVDA. (# 518)
-  NVDA może teraz używać iAccessible2 występujących w 64-bitowych aplikacjach. (# 479)
-  Kontroler, klienta API NVDA jest obecnie dostępny, aby umożliwić kontrolę aplikacji przez NVDA, np. mówienie tekstu,  podgląd mowy, wyświetlanie komunikatów w Braille'u, itp.
-  Informacje i komunikaty o błędach zostaną teraz odczytane z ekranu logowania w systemie Windows Vista i Windows 7. (# 506)
-  W programie Adobe Reader, PDF interaktywne formy opracowane z Adobe LiveCycle są obecnie obsługiwane. (# 475)
-  W Mirandzie, NVDA automatycznie odczytuje przychodzące wiadomości w oknie czatu, jeśli ogłaszanie dynamicznych zmian treści jest włączone. Polecenia ogłaszania również zostały dodane do trzech ostatnich wiadomości (NVDA+kontrol+cyfra). (# 546)
-  Wprowadzone pola tekstowe są obecnie obsługiwane w treści Adobe Flash. (# 461)

### Zmiany

-  Nie są już ogłaszane niezwykle gadatliwe komunikaty pomocy klawiatury w meni Start Windows 7.
-  Wyświetlacz synth obecnie został zastąpiony nowym podglądem mowy. Aby go uaktywnić, wybierz z meni Narzędzia, Podgląd Mowy. Podgląd mowy może być wykorzystywany niezależnie od tego, jakiego syntezatora mowy używasz. (# 44)
-  Jeśli użytkownik wciśnie klawisz, który spowoduje zmianę fokusu komunikaty na monitorze brajlowskim zostaną automatycznie odrzucone. Wcześniej zawsze komunikat pojawiał się w obrębie konfiguracji.
-  Ustalanie czy Braille powinien być powiązany z fokusem lub kursorem przeglądu skrót (NVDA+Ctrl+T), można to również ustawić w oknie ustawień Braille'a, a także zapisać w konfiguracji użytkownika.
-  Aktualizacja syntezatora eSpeak do 1.42.04.
-  Zaktualizowano liblouis Braille'a tłumacz 1.8.0.
-  Ogłaszanie elementów w wirtualnych buforach, podczas przemieszczania się przez znak lub słowo zostało znacznie ulepszone. Wcześniej raportowanie  bardzo się różniło od istotnych informacji, które zostały ogłaszane podczas przemieszczania się po wierszu. (# 490)
-  Teraz można użyć klawisza "Kontrol" do zatrzymania mowy. można również przy pomocy Klawisza "Shift" wznawiać lub zatrzymywać mowę.

#### Poprawione Błędy

-  Cała zawartość wiersza tabeli nie jest już zgłaszana podczas przemieszczania się fokusa wewnątrz komórki w aplikacji Mozilla. (# 482)
-  Wirtualne bufory honorują teraz skróty klawiszowe ogłaszania obiektu, te ustawienia znajdują się w oknie dialogowym Prezentacji obiektu. (# 486)
-  W wirtualnym buforze, współrzędne wiersz / kolumna przy ogłaszaniu tabel są wyłączone, nagłówki wierszy i kolumn nie są już czytane nieprawidłowo.
-  W wirtualnym buforze, współrzędne wiersz / kolumna są teraz czytane poprawnie po opuszczeniu tabeli, a następnie ponownie wprowadza tą samą komórkę w innej tabeli bez konieczności odwiedzania pierwszej komórki, np. naciskając strzałkę w górę następnie strzałkę w dół w pierwszej komórce tabeli. (# 378)
-  Edycja pustych wierszy będzie teraz pokazywana odpowiednio w dokumentach programu Microsoft Word i Microsoft HTML na monitorze brajlowskim. Wcześniej NVDA wyświetlał bieżące zdanie na monitorze, zamiast bieżącego wiersza w tej sytuacji. (# 420)
-  Poprawiono wiele zabezpieczeń w czasie uruchamiania NVDA podczas logowania do Windows i innych zabezpieczonych komputerów. (# 515)
-  Poprawiono układ klawiatury dla laptopa. (# 517)
-  Jeśli fokus znajduje się w konsoli Dos, kursor przeglądu może teraz prawidłowo poruszać się po tekście w konsoli, gdy Braille jest powiązany z przeglądem.
-  Pozycje Meni Start w Windows 7, nie będą już wypowiadane dwukrotnie. (# 474)
-  Aktywne linki na tej samej stronie w Firefoksie v3.6 odpowiednio przesuwają kursor w wirtualny buforze w odpowiednie miejsce na stronie.
-  NVDA nie wymawia już błędnie niektórych liczb oddzielonych myślnikiem, np. 500-1000. (# 547)
-  W systemie Windows XP, NVDA nie powoduje już zawieszania Internet Explorera, gdy następuje przełączenie pola wyboru w witrynie Windows Update. (# 477)
-  NVDA już nie ogłasza w dokumencie Firefox że jest zajęty (np. z powodu aktualizacji lub odświeżania), w przypadku gdy dokument jest w tle. Dotyczy to również paska statusu aplikacji na pierwszym planie.
-  Podczas przełączania układów klawiatury Windows (z kontrol+Shift lub Alt+Shift), pełna nazwa układu jest podawana zarówno w mowie jak i Braille'u. Wcześniej było to ogłaszane tylko mową. Alternatywne układy (np. Dvorak) nie były ogłaszane w ogóle.

### 2009.1

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
