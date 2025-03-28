# Что нового в NVDA

## 2024.3

Магазин дополнений теперь будет уведомлять вас о доступных обновлениях при запуске NVDA.

Появились опции для применения нормализации Unicode к речи и выводу брайля.
Это может быть полезно при чтении символов, которые неизвестны конкретному синтезатору речи или таблице Брайля и которым есть совместимая альтернатива, например, жирные и курсивные символы, часто используемые в социальных сетях.
Она также позволяет читать уравнения в редакторе уравнений Microsoft Word.

Теперь поддерживаются дисплеи Брайля Help Tech Activator Pro.

Добавлены неназначенные команды для прокрутки колёсика мыши по вертикали и горизонтали.

Исправлено несколько ошибок, в частности, в панели эмодзи Windows 11 и истории буфера обмена.
Для веб-браузеров исправлены сообщения об ошибках, иллюстрации, подписи, ярлыки таблиц и пункты меню с флажками или радиокнопками.

Обновлён Liblouis, добавлены новые таблицы Брайля для кириллического сербского, идиша, нескольких древних языков, турецкого и международного фонетического алфавита.
Обновлён eSpeak, добавлена поддержка каракалпакского языка.
Также обновлён Unicode CLDR.

### Новые возможности

* Новые жесты ввода:
  * Добавлены неназначенные команды для вертикальной и горизонтальной прокрутки колёсика мыши, чтобы улучшить навигацию на веб-страницах и в приложениях с динамическим содержимым, таких как Dism++. (#16462, @Cary-Rowen)
* Добавлена поддержка нормализации Unicode для вывода речи и шрифта Брайля. (#11570, #16466 @LeonarddeR)
  * Это может быть полезно при чтении символов, которые неизвестны определённому синтезатору речи или таблице Брайля и имеют совместимую альтернативу, например жирные и курсивные символы, часто используемые в социальных сетях.
  * Нормализация Unicode также позволяет читать уравнения в редакторе уравнений Microsoft Word. (#4631)
  * Вы можете включить эту функцию как для речи, так и для Брайля в соответствующих категориях настроек в диалоге настроек NVDA.
* По умолчанию после запуска NVDA вы будете получать уведомление о доступных обновлениях дополнений. (#15035)
  * Это можно отключить в категории настроек "Магазин дополнений".
  * NVDA ежедневно проверяет наличие обновлений дополнений.
  * Проверяются только обновления в рамках одного канала (например, установленные бета-версии дополнений будут уведомлять только о наличии обновлений в бета-канале).
* Добавлена поддержка дисплеев Help Tech Activator Pro. (#16668)

### Изменения

* Обновления компонентов:
  * eSpeak NG обновлён до версии 1.52-dev коммита `54ee11a79`. (#16495)
    * Добавлен новый язык - Каракалпакский.
  * Обновлён Unicode CLDR до версии 45.0. (#16507, @OzancanKaratas)
  * Обновлён патч fast_diff_match_patch (используется для обнаружения изменений в терминалах и другом динамическом содержимом) до версии 2.1.0. (#16508, @codeofdusk)
  * Обновлён переводчик Брайля LibLouis до версии [3.30.0](https://github.com/liblouis/liblouis/releases/tag/v3.30.0). (#16652, @codeofdusk)
    * Новые таблицы Брайля:
      * кириллический сербский.
      * Идиш.
      * Несколько древних языков: Библейский иврит, аккадский, сирийский, угаритский и транслитерированный клинописный текст.
      * Турецкий язык (вторая ступень). (#16735)
      * Международный фонетический алфавит. (#16773)
  * Обновлён NSIS до версии 3.10 (#16674, @dpy013)
  * Обновлён markdown до 3.6 (#16725, @dpy013)
  * Обновлён nh3 до 0.2.17 (#16725, @dpy013)
* Входная таблица резервного Брайля теперь равна выходной таблице резервного Брайля, которая является Unified English Braille Code grade 1. (#9863, @JulienCochuyt, @LeonarddeR)
* NVDA теперь будет сообщать об иллюстрациях без доступных дочерних элементов, но с меткой или описанием. (#14514)
* При построчном чтении в режиме просмотра "подпись" больше не сообщается на каждой строке длинного рисунка или подписи к таблице. (#14874)
* В консоли Python последняя невыполненная команда больше не теряется при перемещении по истории ввода. (#16653, @CyrilleB79)
* Уникальный анонимный идентификатор теперь отправляется при сборе дополнительной статистики использования NVDA. (#16266)
* По умолчанию при создании переносной копии будет создана новая папка.
При попытке записи в непустой каталог будет выдано предупреждение. (#16684)

### Исправления ошибок

* Исправления для Windows 11:
  * NVDA больше не будет зависать при закрытии истории буфера обмена и панели эмодзи. (#16346, #16347, @josephsl)
  * NVDA будет снова объявлять контакты в сети при открытии интерфейса IME. (#14023, @josephsl)
  * NVDA больше не будет дважды объявлять "историю буфера обмена" при навигации по пунктам меню панели эмодзи. (#16532, @josephsl)
  * NVDA больше не будет обрывать речь и брайль при просмотре каомодзи и символов на панели эмодзи. (#16533, @josephsl)
* Исправления в веб-браузере:
  * Сообщения об ошибках, на которые ссылается `aria-errormessage`, теперь сообщаются в Google Chrome и Mozilla Firefox. (#8318)
  * Если присутствует, NVDA теперь будет использовать `aria-labelledby` для обеспечения доступных имён для таблиц в Mozilla Firefox. (#5183)
  * NVDA будет корректно объявлять пункты меню с радиокнопками и флажками при первом входе в подменю в Google Chrome и Mozilla Firefox. (#14550)
  * Функции поиска в режиме просмотра NVDA теперь более точны, когда страница содержит эмодзи. (#16317, @LeonarddeR)
  * В Mozilla Firefox NVDA теперь корректно сообщает текущий символ, слово и строку, когда курсор находится в  конце строки. (#3156, @jcsteh)
  * Больше не приводит к сбою работы Google Chrome при закрытии документа или выходе из Chrome. (#16893)
* NVDA корректно сообщает о предложениях автозаполнения в Eclipse и других средах на базе Eclipse на Windows 11. (#16416, @thgcode)
* Повышена надёжность автоматического чтения текста, особенно в терминальных приложениях. (#15850, #16027, @Danstiv)
* Теперь снова можно надежно восстановить заводские настройки конфигурации по умолчанию. (#16755, @Emil-18)
* NVDA будет корректно сообщать об изменении выделения при редактировании текста ячейки в Microsoft Excel. (#15843)
* В приложениях, использующих Java Access Bridge, NVDA теперь будет корректно читать последнюю пустую строку текста вместо повторения предыдущей строки. (#9376, @dmitrii-drobotov)
* В LibreOffice Writer (версия 24.8 и новее) при переключении форматирования текста (полужирный, курсив, подчёркивание, надстрочный/подстрочный индекс, выравнивание) с помощью соответствующей комбинации клавиш NVDA сообщает о новом атрибуте форматирования (например, "Полужирный включен", "Полужирный выключен"). (#4248, @michaelweghorn)
* При навигации с помощью клавиш курсора в текстовых полях в приложениях, использующих UI Automation, NVDA больше не сообщает иногда о неправильном символе, слове и т. д. (#16711, @jcsteh)
* При вставке в Калькулятор Windows 10/11 NVDA теперь корректно сообщает полное вставленное число. (#16573, @TristanBurchett)
* NVDA  больше не молчит после отключения и повторного подключения к сеансу удалённого рабочего стола. (#16722, @jcsteh)
* Добавлена поддержка команд просмотра текста для имени объекта в Visual Studio Code. (#16248, @Cary-Rowen)
* Воспроизведение звуков NVDA больше не происходит на монофоническом аудиоустройстве. (#16770, @jcsteh)
* NVDA будет сообщать адреса при переходе по стрелкам через поля To/CC/BCC в outlook.com / Modern Outlook. (#16856)
* NVDA теперь более изящно справляется со сбоями при установке дополнений. (#16704)

### Изменения для разработчиков

* NVDA теперь использует Ruff вместо flake8 для линтинга. (#14817)
* Исправлена система сборки NVDA для корректной работы при использовании Visual Studio 2022 версии 17.10 и выше. (#16480, @LeonarddeR)
* Шрифт фиксированной ширины теперь используется в просмотрщике журнала и в Консоли Python, чтобы курсор оставался в том же столбце при вертикальной навигации.
Это особенно полезно для чтения маркеров места ошибки в трассировках. (#16321, @CyrilleB79)
* Добавлена поддержка пользовательских таблиц Брайля. (#3304, #16208, @JulienCochuyt, @LeonarddeR)
  * Таблицы могут быть размещены в папке `brailleTables` в пакете дополнений.
  * Метаданные таблицы могут быть добавлены в необязательный раздел `brailleTables` в манифесте дополнения или в файл `.ini` в том же формате, находящийся в подкаталоге brailleTables каталога scratchpad.
  * Пожалуйста, обратитесь к разделу [Таблицы перевода Брайля в руководстве разработчика](https://www.nvaccess.org/files/nvda/documentation/developerGuide.html#BrailleTables) для получения более подробной информации.
* Когда событие `gainFocus` ставится в очередь с объектом, имеющим действительное свойство `focusRedirect`, объект, на который указывает свойство `focusRedirect`, теперь хранится в `eventHandler.lastQueuedFocusObject`, а не в первоначально поставленном в очередь объекте. (#15843)
* NVDA будет регистрировать архитектуру исполняемого файла (x86) при запуске. (#16432, @josephsl)
* `wx.CallAfter`, который обернут в `monkeyPatches/wxMonkeyPatches.py`, теперь включает правильную индикацию `functools.wraps`. (#16520, @XLTechie)
* Появился новый модуль для планирования задач `utils.schedule`, использующий модуль pip `schedule`. (#16636)
  * Вы можете использовать `scheduleThread.scheduleDailyJobAtStartUp` для автоматического планирования задачи, которая выполняется после запуска NVDA, и каждые 24 часа после этого.
  Задачи планируются с задержкой, чтобы избежать конфликтов.
  * `scheduleThread.scheduleDailyJob` и `scheduleJob` можно использовать для планирования задач на пользовательское время, при этом при известной нестыковке расписания задач будет выдаваться ошибка `JobClashError`.
* Теперь можно создавать модули приложений для приложений, содержащих элементы управления Edge WebView2 (msedgewebview2.exe). (#16705, @josephsl)

## 2024.2

Появилась новая функция, называемая разделением звука.
Это позволяет разделить звуки NVDA на один канал (например, левый), в то время как звуки всех других приложений направляются на другой канал (например, правый).

Появились новые команды для изменения кольца настроек синтезатора, позволяющие пользователям переходить к первой или последней настройке, а также увеличивать или уменьшать текущую настройку более крупными шагами.
Также появились новые команды быстрой навигации, позволяющие пользователям привязывать жесты для быстрого перехода между абзацем, вертикально выровненным абзацем, текстом того же стиля, текстом другого стиля, элементом меню, кнопкой переключения, индикатором выполнения, рисунком и математической формулой.

Добавлено множество новых функций Брайля и исправлены ошибки.
Был добавлен новый режим Брайля, называемый "вывод речи на дисплей".
Когда он активен, дисплей Брайля показывает именно то, что говорит NVDA.
Также была добавлена ​​поддержка дисплеев BrailleEdgeS2 и BrailleEdgeS3.
В LibLouis добавлены новые подробные (с указанием заглавных букв) белорусские и украинские брайлевские таблицы, лаосская таблица и испанская таблица для чтения греческих текстов.

eSpeak был обновлен, добавлен новый язык тигринья.

Исправлено множество мелких ошибок в таких приложениях, как Thunderbird, Adobe Reader, веб-браузерах, Nudi и Geekbench.

### Новые Возможности

* Новые комбинации клавиш:
  * Новая команда быстрой навигации `p` для перехода к следующему/предыдущему текстовому абзацу в режиме обзора. (#15998, @mltony)
  * Новые неназначенные команды быстрой навигации, которые можно использовать для перехода к следующему/предыдущему:
    * иллюстрации (#10826)
    * вертикально выровненному абзацу (#15999, @mltony)
    * элементу меню (#16001, @mltony)
    * кнопке-переключателю (#16001, @mltony)
    * индикатору выполнения (#16001, @mltony)
    * математической формуле (#16001, @mltony)
    * тексту в одном стиле (#16000, @mltony)
    * тексту в разных стилях (#16000, @mltony)
  * Добавлены команды для перехода к первому, последнему, следующему и предыдущему параметрам кольца настроек синтезатора. (#13768, #16095, @rmcpantoja)
    * На выбор первой/последней настройки кольца синтезатора не назначены жесты. (#13768)
    * Уменьшить и увеличить текущую настройку кольца настроек синтезатора на большой шаг (#13768):
      * Настольная: `NVDA+control+pageUp` or `NVDA+control+pageDown`.
      * Ноутбук: `NVDA+control+shift+pageUp` or `NVDA+control+shift+pageDown`.
  * Добавлен новый неназначенный жест ввода для переключения объявления рисунков и подписей. (#10826, #14349)
* Брайль:
  * Added support for the BrailleEdgeS2 and BrailleEdgeS3 displays. (#16033, #16279, @EdKweon)
  * A new braille mode called "display speech output" has been added. (#15898, @Emil-18)
    * When active, the braille display shows exactly what NVDA speaks.
    * It can be toggled by pressing `NVDA+alt+t`, or from the braille settings dialog.
* Звуковое разделение: (#12985, @mltony)
  * Allows splitting NVDA sounds into one channel (e.g. left) while sounds from all other applications are directed to the other channel (e.g. right).
  * Toggled by `NVDA+alt+s`.
* Заголовки строк и столбцов отчетов теперь поддерживаются в редактируемых HTML-элементах. (#14113)
* Добавлена ​​возможность отключить отображение рисунков и подписей в настройках форматирования документа. (#10826, #14349)
* В Windows 11 NVDA будет объявлять оповещения при голосовом вводе и предлагать действия, включая самое частое предложение при копировании данных, таких как номера телефонов, в буфер обмена (Windows 11 2022 Update и более поздние версии). (#16009, @josephsl)
* NVDA будет поддерживать звуковое устройство в активном состоянии после остановки речи, чтобы предотвратить обрезание начала следующей фразы некоторыми аудиоустройствами, такими как наушники Bluetooth. (#14386, @jcsteh, @mltony)
* Теперь поддерживается защищенный браузер HP. (#16377)

### Изменения

* Магазин дополнений:
  * The minimum and the last tested NVDA version for an add-on are now displayed in the "other details" area. (#15776, @Nael-Sayegh)
  * The community reviews action will be available, and the reviews webpage will be shown in the details panel, in all tabs of the store. (#16179, @nvdaes)
* Обновления компонентов:
  * Обновлён LibLouis Braille translator до [3.29.0](https://github.com/liblouis/liblouis/releases/tag/v3.29.0). (#16259, @codeofdusk)
    * Новые подробные (с указанием заглавных букв) белорусские и украинские брайлевские таблицы.
    * Новая испанская таблица для чтения греческих текстов.
    * Новая таблица для лаосского языка (первая ступень). (#16470)
  * обновлён eSpeak NG до 1.52-dev commit `cb62d93fd7`. (#15913)
    * Добавлен новый язык Тигринья. 
* Изменено несколько жестов для устройств BrailleSense, чтобы избежать конфликтов с символами французской брайлевской таблицы. (#15306)
  * `alt+leftArrow` is now mapped to `dot2+dot7+space`
  * `alt+rightArrow` is now mapped to `dot5+dot7+space`
  * `alt+upArrow` is now mapped to `dot2+dot3+dot7+space`
  * `alt+downArrow` is now mapped to `dot5+dot6+dot7+space`
* Точки-заполнители, обычно используемые в оглавлениях, больше не отображаются при низком уровне пунктуации. (#15845, @CyrilleB79)

### Исправления

* Исправления Windows 11:
  * NVDA will once again announce hardware keyboard input suggestions. (#16283, @josephsl)
  * In Version 24H2 (2024 Update and Windows Server 2025), mouse and touch interaction can be used in quick settings. (#16348, @josephsl)
* Магазин дополнений:
  * При нажатии `ctrl+tab` фокус должным образом перемещается на новый заголовок текущей вкладки. (#14986, @ABuffEr)
  * Если файлы кэша указаны неверно, NVDA больше не будет перезапускаться. (#16362, @nvdaes)
* Исправления для браузеров на базе Chromium при использовании с UIA:
  * Исправлены ошибки, приводившие к зависанию NVDA. (#16393, #16394)
  * Backspace теперь правильно работает в полях входа в Gmail. (#16395)
* Backspace теперь работает правильно при использовании Nudi 6.1 с включенной настройкой NVDA "Обрабатывать клавиши из других приложений". (#15822, @jcsteh)
* Исправлена ​​ошибка, из-за которой аудиокоординаты воспроизводились, когда приложение находится в спящем режиме, если включена опция "Воспроизводить аудиокоординаты при движении мыши". (#8059, @hwf1324)
* В Adobe Reader NVDA больше не игнорирует альтернативный текст, заданный в формулах в PDF-файлах. (#12715)
* Исправлена ​​ошибка, из-за которой NVDA не могла прочитать ленту и параметры в Geekbench. (#16251, @mzanm)
* Исправлен редкий случай, когда при сохранении конфигурации могли не сохраняться все профили. (#16343, @CyrilleB79)
* В браузерах на базе Firefox и Chromium NVDA правильно переходит в режим фокуса при нажатии клавиши Enter, когда она находится в списке представлений (ul / ol) внутри редактируемого содержимого. (#16325)
* Об изменении состояния столбца автоматически сообщается при выборе столбцов для отображения в списке сообщений Thunderbird. (#16323)
* Снова правильно работает ключ командной строки `-h`/`--help`. (#16522, @XLTechie)
* Поддержка NVDA для программы Poedit версии 3.4 или выше правильно работает при переводе с языков, содержащих 1 или более 2 форм множественного числа (например, китайский, польский). (#16318)

### Изменения для разработчиков

Пожалуйста, обратитесь к [руководству для разработчиков](https://www.nvaccess.org/files/nvda/documentation/developerGuide.html#API) для получения информации о процессе устаревания и удаления API NVDA.

* Instantiating `winVersion.WinVersion` objects with unknown Windows versions above 10.0.22000 such as 10.0.25398 returns "Windows 11 unknown" instead of "Windows 10 unknown" for release name. (#15992, @josephsl)
* Make the AppVeyor build process easier for NVDA forks, by adding configurable variables in appveyor.yml to disable or modify NV Access specific portions of the build scripts. (#16216, @XLTechie)
* Added a how-to document, explaining the process of building NVDA forks on AppVeyor. (#16293, @XLTechie)

## 2024.1

A new "on-demand" speech mode has been added.
When speech is on-demand, NVDA does not speak automatically (e.g. when moving the cursor) but still speaks when calling commands whose goal is explicitly to report something (e.g. report window title).
In the Speech category of NVDA's settings, it is now possible to exclude unwanted speech modes from the Cycle speech modes command (`NVDA+s`).

A new Native Selection mode (toggled by `NVDA+shift+f10`) is now available in NVDA's browse mode for Mozilla Firefox.
When turned on, selecting text in browse mode will also manipulate Firefox's own native selection.
Copying text with `control+c` will pass straight through to Firefox, thus copying the rich content, rather than NVDA's plain text representation.

The Add-on Store now supports bulk actions (e.g. installing, enabling add-ons) by selecting multiple add-ons
There is a new action to open a reviews webpage for the selected add-on.

The audio output device and ducking mode options have been removed from the "Select Synthesizer" dialog.
They can be found in the audio settings panel which can be opened with `NVDA+control+u`.

eSpeak-NG, LibLouis braille translator, and Unicode CLDR have been updated.
New Thai, Filipino and Romanian braille tables are available.

There are many bug fixes, particularly for the Add-on Store, braille, Libre Office, Microsoft Office and audio.

### Important notes

* This release breaks compatibility with existing add-ons.
* Windows 7, and Windows 8 are no longer supported.
Windows 8.1 is the minimum Windows version supported.

### New Features

* Add-on Store:
  * The Add-on Store now supports bulk actions (e.g. installing, enabling add-ons) by selecting multiple add-ons. (#15350, #15623, @CyrilleB79)
  * A new action has been added to open a dedicated webpage to see or provide feedback about the selected add-on. (#15576, @nvdaes)
* Added support for Bluetooth Low Energy HID Braille displays. (#15470)
* A new Native Selection mode (toggled by `NVDA+shift+f10`) is now available in NVDA's browse mode for Mozilla Firefox.
When turned on, selecting text in browse mode will also manipulate Firefox's own native selection.
Copying text with `control+c` will pass straight through to Firefox, thus copying the rich content, rather than NVDA's plain text representation. (#15830)
Note however that as Firefox is handling the actual copy, NVDA will not report a "copy to clipboard" message in this mode. (#15830)
* When copying text in Microsoft Word with NVDA's browse mode enabled, formatting is now also included. (#16129)
A side affect of this is that NVDA will no longer report a "copy to clipboard" message when pressing `control+c` in Microsoft Word / Outlook browse mode, as the application is now handling the copy, not NVDA. (#16129)
* A new "on-demand" speech mode has been added.
When speech is on-demand, NVDA does not speak automatically (e.g. when moving the cursor) but still speaks when calling commands whose goal is explicitly to report something (e.g. report window title). (#481, @CyrilleB79)
* In the Speech category of NVDA's settings, it is now possible to exclude unwanted speech modes from the Cycle speech modes command (`NVDA+s`). (#15806, @lukaszgo1)
  * If you are currently using the NoBeepsSpeechMode add-on consider uninstalling it, and disabling "beeps" and "on-demand" modes in the settings.

### Changes

* NVDA no longer supports Windows 7 and Windows 8.
Windows 8.1 is the minimum Windows version supported. (#15544)
* Component updates:
  * Updated LibLouis braille translator to [3.28.0](https://github.com/liblouis/liblouis/releases/tag/v3.28.0). (#15435, #15876, @codeofdusk)
    * Added new Thai, Romanian, and Filipino Braille tables.
  * eSpeak NG has been updated to 1.52-dev commit `530bf0abf`. (#15036)
  * CLDR emoji and symbol annotations has been updated to version 44.0. (#15712, @OzancanKaratas)
  * Updated Java Access Bridge to 17.0.9+8Zulu (17.46.19). (#15744)
* Key Commands:
  * The following commands now support two and three presses to spell the reported information and spell with character descriptions: report selection, report clipboard text and report focused object. (#15449, @CyrilleB79)
  * The command to toggle the screen curtain now has a default gesture: `NVDA+control+escape`. (#10560, @CyrilleB79)
  * When pressed four times, the report selection command now shows the selection in a browsable message. (#15858, @Emil-18)
* Microsoft Office:
  * When requesting formatting information on Excel cells, borders and background will only be reported if there is such formatting. (#15560, @CyrilleB79)
  * NVDA will again no longer report unlabelled groupings such as in recent versions of Microsoft Office 365 menus. (#15638)
* The audio output device and ducking mode options have been removed from the "Select Synthesizer" dialog.
They can be found in the audio settings panel which can be opened with `NVDA+control+u`. (#15512, @codeofdusk)
* The option "Report role when mouse enters object" in NVDA's mouse settings category has been renamed to "Report object when mouse enters it".
This option now announces additional relevant information about an object when the mouse enters it, such as states (checked/pressed) or cell coordinates in a table. (#15420, @LeonarddeR)
* New items have been added to the Help menu for the NV Access "Get Help" page and Shop. (#14631)
* NVDA's support for [Poedit](https://poedit.net) is overhauled for Poedit version 3 and above.
Users of Poedit 1 are encouraged to update to Poedit 3 if they want to rely on enhanced accessibility in Poedit, such as shortcuts to read translator notes and comments. (#15313, #7303, @LeonarddeR)
* Braille viewer and speech viewer are now disabled in secure mode. (#15680)
* During object navigation, disabled (unavailable) objects will not be ignored anymore. (#15477, @CyrilleB79)
* Added table of contents to key commands document. (#16106)

### Bug Fixes

* Add-on Store:
  * When the status of an add-on is changed while it has focus, e.g. a change from "downloading" to "downloaded", the updated item is now announced correctly. (#15859, @LeonarddeR)
  * When installing add-ons install prompts are no longer overlapped by the restart dialog. (#15613, @lukaszgo1)
  * When reinstalling an incompatible add-on it is no longer forcefully disabled. (#15584, @lukaszgo1)
  * Disabled and incompatible add-ons can now be updated. (#15568, #15029)
  * NVDA now recovers and displays an error in a case where an add-on fails to download correctly. (#15796)
  * NVDA no longer fails to restart intermittently after opening and closing Add-on Store. (#16019, @lukaszgo1)
* Audio:
  * NVDA no longer freezes briefly when multiple sounds are played in rapid succession. (#15311, #15757, @jcsteh)
  * If the audio output device is set to something other than the default and that device becomes available again after being unavailable, NVDA will now switch back to the configured device instead of continuing to use the default device. (#15759, @jcsteh)
  * NVDA now resumes audio if the configuration of the output device changes or another application releases exclusive control of the device. (#15758, #15775, @jcsteh)
* Braille:
  * Multi line braille displays will no longer crash the BRLTTY driver and are treated as one continuous display. (#15386)
  * More objects which contain useful text are detected, and text content is displayed in braille. (#15605)
  * Contracted braille input works properly again. (#15773, @aaclause)
  * Braille is now updated when moving the navigator object between table cells in more situations (#15755, @Emil-18)
  * The result of reporting current focus, current navigator object, and current selection commands is now shown in braille. (#15844, @Emil-18)
  * The Albatross braille driver no longer handles a Esp32 microcontroller as an Albatross display. (#15671)
* LibreOffice:
  * Words deleted using the `control+backspace` keyboard shortcut are now also properly announced when the deleted word is followed by whitespace (like spaces and tabs). (#15436, @michaelweghorn)
  * Announcement of the status bar using the `NVDA+end` keyboard shortcut now also works for dialogs in LibreOffice version 24.2 and newer. (#15591, @michaelweghorn)
  * All expected text attributes are now supported in LibreOffice versions 24.2 and above.
  This makes the announcement of spelling errors work when announcing a line in Writer. (#15648, @michaelweghorn)
  * Announcement of heading levels now also works for LibreOffice versions 24.2 and newer. (#15881, @michaelweghorn)
* Microsoft Office:
  * In Excel with UIA disabled, braille is updated, and the active cell content is spoken, when `control+y`, `control+z` or `alt+backspace` is pressed. (#15547)
  * In Word with UIA disabled braille is updated when `control+v`, `control+x`, `control+y`, `control+z`, `alt+backspace`, `backspace` or `control+backspace` is pressed.
  It is also updated with UIA enabled, when typing text and braille is tethered to review and review follows caret. (#3276)
  * In Word, the landing cell will now be correctly reported when using the native Word commands for table navigation `alt+home`, `alt+end`, `alt+pageUp` and `alt+pageDown`. (#15805, @CyrilleB79)
* Reporting of object shortcut keys has been improved. (#10807, #15816, @CyrilleB79)
* The SAPI4 synthesizer now properly supports volume, rate and pitch changes embedded in speech. (#15271, @LeonarddeR)
* Multi line state is now correctly reported in applications using Java Access Bridge. (#14609)
* NVDA will announce dialog content for more Windows 10 and 11 dialogs. (#15729, @josephsl)
* NVDA will no longer fail to read a newly loaded page in Microsoft Edge when using UI Automation. (#15736)
* When using say all or commands which spell text, pauses between sentences or characters no longer gradually decrease over time. (#15739, @jcsteh)
* NVDA no longer sometimes freezes when speaking a large amount of text. (#15752, @jcsteh)
* When accessing Microsoft Edge using UI Automation, NVDA is able to activate more controls in browse mode. (#14612)
* NVDA will not fail to start anymore when the configuration file is corrupted, but it will restore the configuration to default as it did in the past. (#15690, @CyrilleB79)
* Fixed support for System List view (`SysListView32`) controls in Windows Forms applications. (#15283, @LeonarddeR)
* It is not possible anymore to overwrite NVDA's Python console history. (#15792, @CyrilleB79)
* NVDA should remain responsive when being flooded with many UI Automation events, e.g. when large chunks of text are printed to a terminal or when listening to voice messages in WhatsApp messenger. (#14888, #15169)
  * This new behavior can be disabled using the new "Use enhanced event processing" setting in NVDA's advanced settings.
* NVDA is again able to track the focus in applications running within Windows Defender Application Guard (WDAG). (#15164)
* The speech text is no longer updated when the mouse moves in the Speech Viewer. (#15952, @hwf1324)
* NVDA will again switch back to browse mode when closing combo boxes with `escape` or `alt+upArrow` in Firefox or Chrome. (#15653)
* Arrowing up and down in combo boxes in iTunes will no longer inappropriately switch back to browse mode. (#15653)

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

## 2023.3.3

This is a patch release to fix a security issue.
Please responsibly disclose security issues following NVDA's [security policy](https://github.com/nvaccess/nvda/blob/master/security.md).

### Security Fixes

* Prevents possible reflected XSS attack from crafted content to cause arbitrary code execution.
([GHSA-xg6w-23rw-39r8](https://github.com/nvaccess/nvda/security/advisories/GHSA-xg6w-23rw-39r8))

### Bug Fixes

* Fixed bug which caused the NVDA process to fail to exit correctly. (#16123)
* Fixed bug where if the previous NVDA process failed to exit correctly, an NVDA installation could fail to an unrecoverable state. (#16122)

## 2023.3.3

This is a patch release to fix a security issue.
Please responsibly disclose security issues following NVDA's [security policy](https://github.com/nvaccess/nvda/blob/master/security.md).

### Security Fixes

* Prevents possible reflected XSS attack from crafted content to cause arbitrary code execution.
([GHSA-xg6w-23rw-39r8](https://github.com/nvaccess/nvda/security/advisories/GHSA-xg6w-23rw-39r8))

## 2023.3.2

This is a patch release to fix a security issue.
The security patch in 2023.3.1 was not resolved correctly.
Please responsibly disclose security issues following NVDA's [security policy](https://github.com/nvaccess/nvda/blob/master/security.md).

### Security Fixes

* The security patch in 2023.3.1 was not resolved correctly.
Prevents possible system access and arbitrary code execution with system privileges for unauthenticated users.
([GHSA-h7pp-6jqw-g3pj](https://github.com/nvaccess/nvda/security/advisories/GHSA-h7pp-6jqw-g3pj))

## 2023.3.1

This is a patch release to fix a security issue.
Please responsibly disclose security issues following NVDA's [security policy](https://github.com/nvaccess/nvda/blob/master/security.md).

### Security Fixes

* Prevents possible system access and arbitrary code execution with system privileges for unauthenticated users.
([GHSA-h7pp-6jqw-g3pj](https://github.com/nvaccess/nvda/security/advisories/GHSA-h7pp-6jqw-g3pj))

## 2023.3

This release includes improvements to performance, responsiveness and stability of audio output.
Options have been added to control the volume of NVDA sounds and beeps, or to have them follow the volume of the voice you are using.

NVDA can now periodically refresh OCR results, speaking new text as it appears.
This can be configured in the Windows OCR category of NVDA's settings dialog.

There's been several braille fixes, improving device detection and caret movement.
It is now possible to opt-out unwanted drivers from automatic detection, to improve autodetection performance.
There are also new BRLTTY commands.

There's also been bug fixes for the Add-on Store, Microsoft Office, Microsoft Edge context menus, and Windows Calculator.

### New Features

* Enhanced sound management:
  * A new Audio Settings panel:
    * This can be opened with `NVDA+control+u`. (#15497)
    * An option in Audio settings to have the volume of NVDA sounds and beeps follow the volume setting of the voice you are using. (#1409)
    * An option in Audio settings to separately configure the volume of NVDA sounds. (#1409, #15038)
    * The settings to change audio output device and toggle audio ducking have been moved to the new Audio settings panel from the Select Synthesizer dialog.
    These options will be removed from the "select synthesizer" dialog in 2024.1. (#15486, #8711)
  * NVDA will now output audio via the Windows Audio Session API (WASAPI), which may improve the responsiveness, performance and stability of NVDA speech and sounds. (#14697, #11169, #11615, #5096, #10185, #11061)
  * Note: WASAPI is incompatible with some add-ons.
  Compatible updates are available for these add-ons, please update them before updating NVDA.
  Incompatible versions of these add-ons will be disabled when updating NVDA:
    * Tony's Enhancements version 1.15 or older. (#15402)
    * NVDA global commands extension 12.0.8 or older. (#15443)
* NVDA is now able to continually update the result when performing optical character recognition (OCR), speaking new text as it appears. (#2797)
  * To enable this functionality, enable the option "Periodically refresh recognized content" in the Windows OCR category of NVDA's settings dialog.
  * Once enabled, you can toggle speaking new text by toggling report dynamic content changes (pressing `NVDA+5`).
* When using automatic detection of braille displays, it is now possible to opt-out drivers from detection from the braille display selection dialog. (#15196)
* A new option in Document Formatting settings, "Ignore blank lines for line indentation reporting". (#13394)
* Added an unassigned gesture to navigate by tab groupings in browse mode. (#15046)

### Changes

* Braille:
  * When the text in a terminal changes without updating the caret, the text on a braille display will now properly update when positioned on a changed line.
  This includes situations where braille is tethered to review. (#15115)
  * More BRLTTY key bindings are now mapped to NVDA commands (#6483):
    * `learn`: toggle NVDA input help
    * `prefmenu`: open the NVDA menu
    * `prefload`/`prefsave`: Load/save NVDA configuration
    * `time`: Show time
    * `say_line`: Speak the current line where the review cursor is located
    * `say_below`: Say all using review cursor
  * The BRLTTY driver is only available when a BRLTTY instance with BrlAPI enabled is running. (#15335)
  * The advanced setting to enable support for HID braille has been removed in favor of a new option.
  You can now disable specific drivers for braille display auto detection in the braille display selection dialog. (#15196)
* Add-on Store: Installed add-ons will now be listed in the Available Add-ons tab, if they are available in the store. (#15374)
* Some shortcut keys have been updated in the NVDA menu. (#15364)

### Bug Fixes

* Microsoft Office:
  * Fixed crash in Microsoft Word when Document formatting options "report headings" and "report comments and notes" were not enabled. (#15019)
  * In Word and Excel, text alignment will be correctly reported in more situations. (#15206, #15220)
  * Fixes the announcement of some cell formatting shortcuts in Excel. (#15527)
* Microsoft Edge:
  * NVDA will no longer jump back to the last browse mode position when opening the context menu in Microsoft Edge. (#15309)
  * NVDA is once again able to read context menus of downloads in Microsoft Edge. (#14916)
* Braille:
  * The braille cursor and selection indicators will now always be updated correctly after showing or hiding respective indicators with a gesture. (#15115)
  * Fixed bug where Albatross braille displays try to initialize although another braille device has been connected. (#15226)
* Add-on Store:
  * Fixed bug where unchecking "include incompatible add-ons" would result in incompatible add-ons still being listed in the store. (#15411)
  * Add-ons blocked due to compatibility reasons should now be filtered correctly when toggling the filter for enabled/disabled status. (#15416)
  * Fixed bug preventing overridden enabled incompatible add-ons being upgraded or replaced using the external install tool. (#15417)
  * Fixed bug where NVDA would not speak until restarted after add-on installation. (#14525)
  * Fixed bug where add-ons cannot be installed if a previous download failed or was cancelled. (#15469)
  * Fixed issues with handling incompatible add-ons when upgrading NVDA. (#15414, #15412, #15437)
* NVDA once again announces calculation results in the Windows 32bit calculator on Server, LTSC and LTSB versions of Windows. (#15230)
* NVDA no longer ignores focus changes when a nested window (grand child window) gets focus. (#15432)
* Fixed a potential cause of crashing during NVDA startup. (#15517)

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

This release introduces the Add-on Store to replace the Add-ons Manager.
In the Add-on Store you can browse, search, install and update community add-ons.
You can now manually override incompatibility issues with outdated add-ons at your own risk.

There are new braille features, commands, and display support.
There are also new input gestures for OCR and flattened object navigation.
Navigating and reporting formatting in Microsoft Office is improved.

There are many bug fixes, particularly for braille, Microsoft Office, web browsers and Windows 11.

eSpeak-NG, LibLouis braille translator, and Unicode CLDR have been updated.

### New Features

* Add-on Store has been added to NVDA. (#13985)
  * Browse, search, install and update community add-ons.
  * Manually override incompatibility issues with outdated add-ons.
  * The Add-ons Manager has been removed and replaced by the Add-on Store.
  * For more information please read the updated user guide.
* New input gestures:
  * An unbound gesture to cycle through the available languages for Windows OCR. (#13036)
  * An unbound gesture to cycle through the braille show messages modes. (#14864)
  * An unbound gesture to toggle showing the selection indicator for braille. (#14948)
  * Added default keyboard gesture assignments to move to the next or previous object in a flattened view of the object hierarchy. (#15053)
    * Desktop: `NVDA+numpad9` and `NVDA+numpad3` to move to the previous and next objects respectively.
    * Laptop: `shift+NVDA+[` and `shift+NVDA+]` to move to the previous and next objects respectively.
* New braille features:
  * Added support for the Help Tech Activator braille display. (#14917)
  * A new option to toggle showing the selection indicator (dots 7 and 8). (#14948)
  * A new option to optionally move the system caret or focus when changing the review cursor position with braille routing keys. (#14885, #3166)
  * When pressing `numpad2` three times to report the numerical value of the character at the position of the review cursor, the information is now also provided in braille. (#14826)
  * Added support for the `aria-brailleroledescription` ARIA 1.3 attribute, allowing web authors to override the type of an element shown on the braille display. (#14748)
  * Baum braille driver: added several braille chord gestures for performing common keyboard commands such as `windows+d` and `alt+tab`.
  Please refer to the NVDA User Guide for a full list. (#14714)
* Added pronunciation of Unicode symbols:
  * braille symbols such as `⠐⠣⠃⠗⠇⠐⠜`. (#13778)
  * Mac Option key symbol `⌥`. (#14682)
* Added gestures for Tivomatic Caiku Albatross braille displays. (#14844, #15002)
  * showing the braille settings dialog
  * accessing the status bar
  * cycling the braille cursor shape
  * cycling the braille show messages mode
  * toggling the braille cursor on/off
  * toggling the "braille show selection indicator" state
  * cycling the "braille move system caret when routing review cursor" mode. (#15122)
* Microsoft Office features:
  * When highlighted text is enabled Document Formatting, highlight colours are now reported in Microsoft Word. (#7396, #12101, #5866)
  * When colors are enabled Document Formatting, background colours are now reported in Microsoft Word. (#5866)
  * When using Excel shortcuts to toggle format such as bold, italic, underline and strike through of a cell in Excel, the result is now reported. (#14923)
* Experimental enhanced sound management:
  * NVDA can now output audio via the Windows Audio Session API (WASAPI), which may improve the responsiveness, performance and stability of NVDA speech and sounds. (#14697)
  * WASAPI usage can be enabled in Advanced settings.
  Additionally, if WASAPI is enabled, the following Advanced settings can also be configured.
    * An option to have the volume of NVDA sounds and beeps follow the volume setting of the voice you are using. (#1409)
    * An option to separately configure the volume of NVDA sounds. (#1409, #15038)
  * There is a known issue with intermittent crashing when WASAPI is enabled. (#15150)
* In Mozilla Firefox and Google Chrome, NVDA now reports when a control opens a dialog, grid, list or tree if the author has specified this using `aria-haspopup`. (#8235)
* It is now possible to use system variables (such as `%temp%` or `%homepath%`) in the path specification while creating portable copies of NVDA. (#14680)
* In Windows 10 May 2019 Update and later, NVDA can announce virtual desktop names when opening, changing, and closing them. (#5641)
* A system wide parameter has been added to allow users and system administrators to force NVDA to start in secure mode. (#10018)

### Changes

* Component updates:
  * eSpeak NG has been updated to 1.52-dev commit `ed9a7bcf`. (#15036)
  * Updated LibLouis braille translator to [3.26.0](https://github.com/liblouis/liblouis/releases/tag/v3.26.0). (#14970)
  * CLDR has been updated to version 43.0. (#14918)
* LibreOffice changes:
  * When reporting the review cursor location, the current cursor/caret location is now reported relative to the current page in LibreOffice Writer 7.6 and newer, similar to what is done for Microsoft Word. (#11696)
  * Announcement of the status bar (e.g. triggered by `NVDA+end`) works for LibreOffice. (#11698)
  * When moving to a different cell in LibreOffice Calc, NVDA no longer incorrectly announces the coordinates of the previously focused cell when cell coordinate announcement is disabled in NVDA's settings. (#15098)
* Braille changes:
  * When using a braille display via the Standard HID braille driver, the dpad can be used to emulate the arrow keys and enter.
  Also `space+dot1` and `space+dot4` now map to up and down arrow respectively. (#14713)
  * Updates to dynamic web content (ARIA live regions) are now displayed in braille.
  This can be disabled in the Advanced Settings panel. (#7756)
* Dash and em-dash symbols will always be sent to the synthesizer. (#13830)
* Distance reported in Microsoft Word will now honour the unit defined in Word's advanced options even when using UIA to access Word documents. (#14542)
* NVDA responds faster when moving the cursor in edit controls. (#14708)
* Script for reporting the destination of a link now reports from the caret / focus position rather than the navigator object. (#14659)
* Portable copy creation no longer requires that a drive letter be entered as part of the absolute path. (#14680)
* If Windows is configured to display seconds in the system tray clock, using `NVDA+f12` to report the time now honors that setting. (#14742)
* NVDA will now report unlabeled groupings that have useful position information, such as in recent versions of Microsoft Office 365 menus. (#14878)

### Bug Fixes

* Braille:
  * Several stability fixes to input/output for braille displays, resulting in less frequent errors and crashes of NVDA. (#14627)
  * NVDA will no longer unnecessarily switch to no braille multiple times during auto detection, resulting in a cleaner log and less overhead. (#14524)
  * NVDA will now switch back to USB if a HID Bluetooth device (such as the HumanWare Brailliant or APH Mantis) is automatically detected and an USB connection becomes available.
  This only worked for Bluetooth Serial ports before. (#14524)
  * When no braille display is connected and the braille viewer is closed by pressing `alt+f4` or clicking the close button, the display size of the braille subsystem will again be reset to no cells. (#15214)
* Web browsers:
  * NVDA no longer occasionally causes Mozilla Firefox to crash or stop responding. (#14647)
  * In Mozilla Firefox and Google Chrome, typed characters are no longer reported in some text boxes even when speak typed characters is disabled. (#8442)
  * You can now use browse mode in Chromium Embedded Controls where it was not possible previously. (#13493, #8553)
  * In Mozilla Firefox, moving the mouse over text after a link now reliably reports the text. (#9235)
  * The destination of graphic links is now reported accurately in more cases in Chrome and Edge. (#14783)
  * When trying to report the URL for a link without a href attribute NVDA is no longer silent.
  Instead NVDA reports that the link has no destination. (#14723)
  * In Browse mode, NVDA will no longer incorrectly ignore focus moving to a parent or child control e.g. moving from a control to its parent list item or gridcell. (#14611)
    * Note however that this fix only applies when the Automatically set focus to focusable elements" option in Browse Mode settings is turned off (which is the default).
* Fixes for Windows 11:
  * NVDA can once again announce Notepad status bar contents. (#14573)
  * Switching between tabs will announce the new tab name and position for Notepad and File Explorer. (#14587, #14388)
  * NVDA will once again announce candidate items when entering text in languages such as Chinese and Japanese. (#14509)
  * It is once again possible to open the Contributors and License items on the NVDA Help menu. (#14725)
* Microsoft Office fixes:
  * When rapidly moving through cells in Excel, NVDA is now less likely to report the wrong cell or selection. (#14983, #12200, #12108)
  * When landing on an Excel cell from outside a work sheet, braille and focus highlighter are no longer needlessly updated to the object that had focus previously. (#15136)
  * NVDA no longer fails to announce focusing password fields in Microsoft Excel and Outlook. (#14839)
* For symbols which do not have a symbol description in the current locale, the default English symbol level will be used. (#14558, #14417)
* It is now possible to use the backslash character in the replacement field of a dictionaries entry, when the type is not set to regular expression. (#14556)
* In Windows 10 and 11 Calculator, a portable copy of NVDA will no longer do nothing or play error tones when entering expressions in standard calculator in compact overlay mode. (#14679)
* NVDA again recovers from many more situations such as applications that stop responding which previously caused it to freeze completely. (#14759) 
* When forcing UIA support with certain terminal and consoles, a bug is fixed which caused a freeze and the log file to be spammed. (#14689)
* NVDA will no longer refuse to save the configuration after a configuration reset. (#13187)
* When running a temporary version from the launcher, NVDA will not mislead users into thinking they can save the configuration. (#14914)
* NVDA now generally responds slightly faster to commands and focus changes. (#14928)
* Displaying the OCR settings will not fail on some systems anymore. (#15017)
* Fix bug related to saving and loading the NVDA configuration, including switching synthesizers. (#14760)
* Fix bug causing text review "flick up" touch gesture to move pages rather than move to previous line. (#15127)

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

A new option has been added, "Paragraph Style" in "Document Navigation".
This can be used with text editors that do not support paragraph navigation natively, such as Notepad and Notepad++.

There is a new global command to report the destination of a link, mapped to `NVDA+k`.

Support for annotated web content (such as comments and footnotes) has improved.
Press `NVDA+d` to cycle through summaries when annotations are reported (e.g. "has comment, has footnote").

Tivomatic Caiku Albatross 46/80 braille displays are now supported.

Support for ARM64 and AMD64 versions of Windows has improved.

There are many bug fixes, notably Windows 11 fixes.

eSpeak, LibLouis, Sonic rate boost and Unicode CLDR have been updated.
There are new Georgian, Swahili (Kenya) and Chichewa (Malawi) braille tables.

Note:

* This release breaks compatibility with existing add-ons.

### New Features

* Microsoft Excel via UI Automation: Automatic reporting of column and row headers in tables. (#14228)
  * Note: This is referring to tables formatted via the "Table" button on the Insert pane of the Ribbon.
  "First Column" and "Header Row" in "Table Style Options" correspond to column and row headers respectively.
  * This is not referring to screen reader specific headers via named ranges, which is currently not supported via UI Automation.
* An unassigned script has been added to toggle delayed character descriptions. (#14267)
* Added an experimental option to leverage the UIA notification support in Windows Terminal to report new or changed text in the terminal, resulting in improved stability and responsivity. (#13781)
  * Consult the user guide for limitations of this experimental option.
* On Windows 11 ARM64, browse mode is now available in AMD64 apps such as Firefox, Google Chrome and 1Password. (#14397)
* A new option has been added, "Paragraph Style" in "Document Navigation".
This adds support for single line break (normal) and multi line break (block) paragraph navigation.
This can be used with text editors that do not support paragraph navigation natively, such as Notepad and Notepad++. (#13797)
* The presence of multiple annotations are now reported.
`NVDA+d` now cycles through reporting the summary of each annotation target for origins with multiple annotation targets.
For example, when text has a comment and a footnote associated with it. (#14507, #14480)
* Added support for Tivomatic Caiku Albatross 46/80 braille displays. (#13045)
* New global command: Report link destination (`NVDA+k`).
Pressed once will speak/braille the destination of the link that is in the navigator object.
Pressing twice will show it in a window, for more detailed review. (#14583)
* New unmapped global command (Tools category): Report link destination in a window.
Same as pressing `NVDA+k` twice, but may be more useful for braille users. (#14583)

### Changes

* Updated LibLouis braille translator to [3.24.0](https://github.com/liblouis/liblouis/releases/tag/v3.24.0). (#14436)
  * Major updates to Hungarian, UEB, and Chinese bopomofo braille.
  * Support for the Danish braille standard 2022.
  * New braille tables for Georgian literary braille, Swahili (Kenya) and Chichewa (Malawi).
* Updated Sonic rate boost library to commit `1d70513`. (#14180)
* CLDR has been updated to version 42.0. (#14273)
* eSpeak NG has been updated to 1.52-dev commit `f520fecb`. (#14281, #14675)
  * Fixed reporting of large numbers. (#14241)
* Java applications with controls using the selectable state will now announce when an item is not selected rather than when the item is selected. (#14336)

### Bug Fixes

* Windows 11 fixes:
  * NVDA will announce search highlights when opening Start menu. (#13841)
  * On ARM, x64 apps are no longer identified as ARM64 applications. (#14403)
  * Clipboard history menu items such as "pin item" can be accessed. (#14508)
  * In Windows 11 22H2 and newer, it is again possible to use mouse and touch interaction to interact with areas such as the system tray overflow window and "Open With" dialog. (#14538, #14539)
* Suggestions are reported when typing an @mention in in Microsoft Excel comments. (#13764)
* In the Google Chrome location bar, suggestion controls (switch to tab, remove suggestion etc) are now reported when selected. (#13522)
* When requesting formatting information, colors are now explicitly reported in Wordpad or log viewer, rather than only "Default color". (#13959)
* In Firefox, activating the "Show options" button on GitHub issue pages now works reliably. (#14269)
* The date picker controls in Outlook 2016 / 365 Advanced search dialog now report their label and value. (#12726)
* ARIA switch controls are now actually reported as switches in Firefox, Chrome and Edge, rather than checkboxes. (#11310)
* NVDA will automatically announce the sort state on an HTML table column header when changed by pressing an inner button. (#10890)
* A landmark or region's name is always automatically spoken when jumping inside from outside using quick navigation or focus in browse mode. (#13307)
* When beep or announce 'cap' for capitals is enabled with delayed character descriptions, NVDA no longer beeps or announces 'cap' twice. (#14239)
* Controls in tables in Java applications will now be announced more accurately by NVDA. (#14347)
* Some settings will no longer be unexpectedly different when used with multiple profiles. (#14170)
  * The following settings have been addressed:
    * Line indentation in Document formatting settings.
    * Cell borders in doc formatting settings
    * Show messages in braille settings
    * Tether Braille in braille settings
  * In some rare cases, these settings used in profiles may be unexpectedly modified when installing this version of NVDA.
  * Please check these options in your profiles after upgrading NVDA to this version.
* Emojis should now be reported in more languages. (#14433)
* The presence of an annotation is no longer missing in braille for some elements. (#13815)
* Fixed an issue where config changes not save correctly when changing between a "Default" option and the value of the "Default" option. (#14133)
* When configuring NVDA there will always be at least one key defined as an NVDA key. (#14527)
* When accessing the NVDA menu via the notification area, NVDA will not suggest a pending update anymore when no update is available. (#14523)
* Remaining, elapsed and total time is now reported correctly for audio files over a day long in foobar2000. (#14127)
* In web browsers such as Chrome and Firefox, alerts such as file downloads are shown in braille in addition to being spoken. (#14562)
* Bug fixed when navigating to the first and last column in a table in Firefox (#14554)
* When NVDA is launched with `--lang=Windows` parameter, it is again possible to open NVDA's General settings dialog. (#14407)
* NVDA no longer fails to continue reading in Kindle for PC after turning the page. (#14390)

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

This release includes several new key commands, including table say all commands.
A "Quick Start Guide" section has been added to the User Guide.
There are also several bug fixes.

eSpeak has been updated and LibLouis has been updated.
There are new Chinese, Swedish, Luganda and Kinyarwanda braille tables.

### New Features

* Added a "Quick Start Guide" section to the User Guide. (#13934)
* Introduced a new command to check the keyboard shortcut of the current focus. (#13960)
  * Desktop: `shift+numpad2`.
  * Laptop: `NVDA+ctrl+shift+.`.
* Introduced new commands to move the review cursor by page where supported by the application. (#14021)
  * Move to previous page:
    * Desktop: `NVDA+pageUp`.
    * Laptop: `NVDA+shift+pageUp`.
  * Move to next page:
    * Desktop: `NVDA+pageDown`.
    * Laptop: `NVDA+shift+pageDown`.
* Added the following table commands. (#14070)
  * Say all in column: `NVDA+control+alt+downArrow`
  * Say all in row: `NVDA+control+alt+rightArrow`
  * Read entire column: `NVDA+control+alt+upArrow`
  * Read entire row: `NVDA+control+alt+leftArrow`
* Microsoft Excel via UI Automation: NVDA now announces when moving out of a table within a spreadsheet. (#14165)
* Reporting table headers can now be configured separately for rows and columns. (#14075)

### Changes

* eSpeak NG has been updated to 1.52-dev commit `735ecdb8`. (#14060, #14079, #14118, #14203)
  * Fixed reporting of Latin characters when using Mandarin. (#12952, #13572, #14197)
* Updated LibLouis braille translator to [3.23.0](https://github.com/liblouis/liblouis/releases/tag/v3.23.0). (#14112)
  * Added braille tables:
    * Chinese common braille (simplified Chinese characters)
    * Kinyarwanda literary braille
    * Luganda literary braille
    * Swedish uncontracted braille
    * Swedish partially contracted braille
    * Swedish contracted braille
    * Chinese (China, Mandarin) Current Braille System (no tones) (#14138)
* NVDA now includes the architecture of the operating system as part of user statistics tracking. (#14019)

### Bug Fixes

* When updating NVDA using the Windows Package Manager CLI (aka winget), a released version of NVDA is no longer always treated as newer than whatever alpha version is installed. (#12469)
* NVDA will now correctly announce Group boxes in Java applications. (#13962)
* Caret properly follows spoken text during "say all" in applications such as Bookworm, WordPad, or the NVDA log viewer. (#13420, #9179)
* In programs using UI Automation, partially checked checkboxes will be reported correctly. (#13975)
* Improved performance and stability in Microsoft Visual Studio, Windows Terminal, and other UI Automation based applications. (#11077, #11209)
  * These fixes apply to Windows 11 Sun Valley 2 (version 22H2) and later.
  * Selective registration for UI Automation events and property changes now enabled by default.
* Text reporting, Braille output, and password suppression now work as expected in the embedded Windows Terminal control in Visual Studio 2022. (#14194)
* NVDA is now DPI aware when using multiple monitors.
There are several fixes for using a DPI setting higher than 100% or multiple monitors.
Issues may still exist with versions of Windows older than Windows 10 1809.
For these fixes to work, applications which NVDA interacts with also need to be DPI aware.
Note there are still known issues with Chrome and Edge. (#13254)
  * Visual highlighting frames should now be correctly placed in most applications. (#13370, #3875, #12070)
  * Touch screen interaction should now be accurate for most applications. (#7083)
  * Mouse tracking should now work for most applications. (#6722)
* Orientation state (landscape/portrait) changes are now correctly ignored when there is no change (e.g. monitor changes). (#14035)
* NVDA will announce dragging items on screen in places such as rearranging Windows 10 Start menu tiles and virtual desktops in Windows 11. (#12271, #14081)
* In advanced settings, "Play a sound for logged errors" option is now correctly restored to its default value when pressing the "Restore defaults" button. (#14149)
* NVDA can now select text using the `NVDA+f10` keyboard shortcut on Java applications. (#14163)
* NVDA will no longer get stuck in a menu when arrowing up and down threaded conversations in Microsoft Teams. (#14355)

### Changes for Developers

Please refer to [the developer guide](https://www.nvaccess.org/files/nvda/documentation/developerGuide.html#API) for information on NVDA's API deprecation and removal process.

* The [NVDA API Announcement mailing list](https://groups.google.com/a/nvaccess.org/g/nvda-api/about) was created. (#13999)
* NVDA no longer processes `textChange` events for most UI Automation applications due to their extreme negative performance impact. (#11002, #14067)

#### Deprecations

* `core.post_windowMessageReceipt` is deprecated, use `winAPI.messageWindow.pre_handleWindowMessage` instead.
* `winKernel.SYSTEM_POWER_STATUS` is deprecated and usage is discouraged, this has been moved to `winAPI._powerTracking.SystemPowerStatus`.
* `winUser.SM_*` constants are deprecated, use `winAPI.winUser.constants.SystemMetrics` instead.

## 2022.3.3

This is a minor release to fix issues with 2022.3.2, 2022.3.1 and 2022.3.
This also addresses a security issue.

### Security Fixes

* Prevents possible system access (e.g. NVDA Python console) for unauthenticated users.
([GHSA-fpwc-2gxx-j9v7](https://github.com/nvaccess/nvda/security/advisories/GHSA-fpwc-2gxx-j9v7))

### Bug Fixes

* Fixed bug where if NVDA freezes when locking, NVDA will allow access to the users desktop while on the Windows lock screen. (#14416)
* Fixed bug where if NVDA freezes when locking, NVDA will not behave correctly, as if the device was still locked. (#14416)
* Fixed accessibility issues with the Windows "forgot my PIN" process and Windows update/install experience. (#14368)
* Fixed bug when trying to install NVDA in some Windows environments, e.g. Windows Server. (#14379)

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

This is a minor release to fix regressions with 2022.3.1 and address a security issue.

### Security Fixes

* Prevents possible system level access for unauthenticated users.
([GHSA-3jj9-295f-h69w](https://github.com/nvaccess/nvda/security/advisories/GHSA-3jj9-295f-h69w))

### Bug Fixes

* Fixes a regression from 2022.3.1 where certain functionality was disabled on secure screens. (#14286)
* Fixes a regression from 2022.3.1 where certain functionality was disabled after sign-in, if NVDA started on the lock screen. (#14301)

## 2022.3.1

This is a minor release to fix several security issues.
Please responsibly disclose security issues to <info@nvaccess.org>.

### Security Fixes

* Fixed exploit where it was possible to elevate from user to system privileges.
([GHSA-q7c2-pgqm-vvw5](https://github.com/nvaccess/nvda/security/advisories/GHSA-q7c2-pgqm-vvw5))
* Fixed a security issue allowing access to the python console on the lock screen via a race condition for NVDA startup.
([GHSA-72mj-mqhj-qh4w](https://github.com/nvaccess/nvda/security/advisories/GHSA-72mj-mqhj-qh4w))
* Fixed issue where speech viewer text is cached when locking Windows.
([GHSA-grvr-j2h8-3qm4](https://github.com/nvaccess/nvda/security/advisories/GHSA-grvr-j2h8-3qm4))

### Bug Fixes

* Prevent an unauthenticated user from updating settings for speech and Braille viewer on the lock screen. ([GHSA-grvr-j2h8-3qm4](https://github.com/nvaccess/nvda/security/advisories/GHSA-grvr-j2h8-3qm4))

## 2022.3

A significant amount of this release was contributed by the NVDA development community.
This includes delayed character descriptions and improved Windows Console support.

This release also includes several bug fixes.
Notably, up-to-date versions of Adobe Acrobat/Reader will no longer crash when reading a PDF document.

eSpeak has been updated, which introduces 3 new languages: Belarusian, Luxembourgish and Totontepec Mixe.

### New Features

* In the Windows Console Host used by Command Prompt, PowerShell, and the Windows Subsystem for Linux on Windows 11 version 22H2 (Sun Valley 2) and later:
  * Vastly improved performance and stability. (#10964)
  * When pressing `control+f` to find text, the review cursor position is updated to follow the found term. (#11172)
  * Reporting of typed text that does not appear on-screen (such as passwords) is disabled by default.
It can be re-enabled in NVDA's advanced settings panel. (#11554)
  * Text that has scrolled offscreen can be reviewed without scrolling the console window. (#12669)
  * More detailed text formatting information is available. ([microsoft/terminal PR 10336](https://github.com/microsoft/terminal/pull/10336))
* A new Speech option has been added to read character descriptions after a delay. (#13509)
* A new Braille option has been added to determine if scrolling the display forward/back should interrupt speech. (#2124)

### Changes

* eSpeak NG has been updated to 1.52-dev commit `9de65fcb`. (#13295)
  * Added languages:
    * Belarusian
    * Luxembourgish
    * Totontepec Mixe
* When using UI Automation to access Microsoft Excel spreadsheet controls, NVDA is now able to report when a cell is merged. (#12843)
* Instead of reporting "has details" the purpose of details is included where possible, for example "has comment". (#13649)
* The installation size of NVDA is now shown in Windows Programs and Feature section. (#13909)

### Bug Fixes

* Adobe Acrobat / Reader 64 bit will no longer crash when reading a PDF document. (#12920)
  * Note that the most up to date version of Adobe Acrobat / Reader is also required to avoid the crash.
* Font size measurements are now translatable in NVDA. (#13573)
* Ignore Java Access Bridge events where no window handle can be found for Java applications.
This will improve performance for some Java applications including IntelliJ IDEA. (#13039)
* Announcement of selected cells for LibreOffice Calc is more efficient and no longer results in a Calc freeze when many cells are selected. (#13232)
* When running under a different user, Microsoft Edge is no longer inaccessible. (#13032)
* When rate boost is off, eSpeak's rate does not drop anymore between rates 99% and 100%. (#13876)
* Fix bug which allowed 2 Input Gestures dialogs to open. (#13854)

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

This is a patch release to fix a security issue.

### Bug Fixes

* Fixed an exploit where it was possible to open the NVDA python console via the log viewer on the lock screen.
([GHSA-585m-rpvv-93qg](https://github.com/nvaccess/nvda/security/advisories/GHSA-585m-rpvv-93qg))

## 2022.2.3

This is a patch release to fix an accidental API breakage introduced in 2022.2.1.

### Bug Fixes

* Fixed a bug where NVDA did not announce "Secure Desktop" when entering a secure desktop.
This caused NVDA remote to not recognize secure desktops. (#14094)

## 2022.2.2

This is a patch release to fix a bug introduced in 2022.2.1 with input gestures.

### Bug Fixes

* Fixed a bug where input gestures didn't always work. (#14065)

## 2022.2.1

This is a minor release to fix a security issue.
Please responsibly disclose security issues to <info@nvaccess.org>.

### Security Fixes

* Fixed exploit where it was possible to run a python console from the lockscreen. (GHSA-rmq3-vvhq-gp32)
* Fixed exploit where it was possible to escape the lockscreen using object navigation. (GHSA-rmq3-vvhq-gp32)

### Changes for Developers

#### Deprecations

These deprecations are currently not scheduled for removal.
The deprecated aliases will remain until further notice.
Please test the new API and provide feedback.
For add-on authors, please open a GitHub issue if these changes stop the API from meeting your needs.

* `appModules.lockapp.LockAppObject` should be replaced with `NVDAObjects.lockscreen.LockScreenObject`. (GHSA-rmq3-vvhq-gp32)
* `appModules.lockapp.AppModule.SAFE_SCRIPTS` should be replaced with `utils.security.getSafeScripts()`. (GHSA-rmq3-vvhq-gp32)

## 2022.2

Этот выпуск включает в себя исправления множества ошибок.
Особо примечательны значительные улучшения поддержки для Java-приложений, брайлевских дисплеев и функционала Windows.

Были добавлены новые команды навигации по таблицам.
Обновлена база данных символов Unicode.
Обновлён брайлевский транслятор LibLouis, включающий новые таблицы для немецкого языка.

### Новое

* Добавлена поддержка взаимодействия с Microsoft Loop Components из состава Microsoft Office. (#13617)
* Добавлены новые команды навигации по таблицам. (#957)
 * `Control+Alt+Home/End` для перемещения соответственно на первый и последний столбец.
 * `Control+Alt+PageUp/PageDown` для перемещения соответственно на первую и последнюю строку.
* Добавлена команда для циклического выбора между режимами автоматического переключения языков и диалектов (см. соответствующие флажки в настройках речи NVDA). Желаемое сочетание клавиш на эту команду пользователь должен назначить самостоятельно. (#10253)

### Изменения

* Инсталлятор NSIS обновлён до версии 3.08. (#9134)
* Общий репозиторий языковых данных консорциума Unicode (CLDR), используемый в NVDA для чтения символов эмодзи, обновлён до версии 41.0. (#13582)
* Брайлевский транслятор LibLouis обновлён до версии [3.22.0](https://github.com/liblouis/liblouis/releases/tag/v3.22.0). (#13775)
  * Добавлена новая таблица: Немецкий (подробная вторая ступень)
* Добавлена поддержка такого элемента управления как "Индикатор занятости". (#10644)
* Если команда NVDA не может быть выполнена, то пользователь теперь будет получать об этом соответствующее уведомление. (#13500)
  * Это происходит в следующих случаях:
    * При использовании версии NVDA из Windows Store.
    * При нахождении на безопасном рабочем столе.
    * При ожидании ответа от пользователя в модальном диалоговом окне.

### Исправления

* Ряд исправлений и улучшений для Java-приложений, а именно:
  * NVDA теперь объявляет состояние элементов управления "только для чтения". (#13692)
  * NVDA теперь корректно объявляет состояние элементов управления "отключено/включено". (#10993)
  * NVDA теперь объявляет клавиши-ускорители для элементов управления. (#13643)
  * NVDA теперь может объявлять изменения индикаторов выполнения как с помощью речи, так и тоновыми сигналами. (#13594)
  * NVDA больше не удаляет ошибочно текст из виджетов при его представлении пользователю. (#13102)
  * NVDA теперь объявляет состояние кнопок-переключателей. (#9728)
  * NVDA теперь идентифицирует отдельные окна в Java-приложении с несколькими окнами. (#9184)
  * NVDA теперь объявляет информацию о позиции для элементов-вкладок. (#13744)
* Исправления для брайлевских дисплеев:
  * Исправлен брайлевский вывод при навигации по тексту в редакторах Mozilla с поддержкой форматирования, таких как редактор составления сообщения в Thunderbird. (#12542)
  * Когда настроена автоматическая привязка брайлевского вывода и происходит перемещение указателя мыши с включённым отслеживанием мыши,
   команды просмотра текста теперь корректно обновляют брайлевский дисплей в соответствии с произносимым содержимым. (#11519)
  * Теперь возможно выполнять панорамирование брайлевского дисплея по содержимому после использования команд просмотрового курсора. (#8682)
* Инсталлятор NVDA теперь можно запускать из директорий содержащих специальные символы. (#13270)
* В Firefox, попытка чтения элементов web-страницы с невалидными атрибутами aria-rowindex, aria-colindex, aria-rowcount или aria-colcount, больше не приводит к ошибке. (#13405)
* Курсор больше не перескакивает между строками или столбцами при навигации по таблице во время перемещения через объединенные ячейки. (#7278)
* При чтении неинтерактивных PDF-документов в Adobe Reader, NVDA теперь сообщает тип и состояние полей форм (таких как флажки и радио-кнопки). (#13285)
* Элемент меню NVDA "Сбросить конфигурацию к заводским настройкам" теперь доступен и при работе NVDA на безопасном рабочем столе. (#13547)
* Все зажатые кнопки мыши теперь будут отпущены при завершении работы NVDA. Ранее при этом кнопки мыши оставались зажатыми. (#13410)
* В Visual Studio NVDA теперь может сообщать номера строк. (#13604)
  * Обратите внимание, что для работы этой функции в настройках Visual Studio должно быть включено отображение номеров строк, а в NVDA должно быть включено их чтение.
* В Visual Studio теперь корректно сообщаются отступы строк. (#13574)
* NVDA теперь снова может объявлять подробную информацию о результатах поиска в меню "Пуск" в последних выпусках Windows 10 и 11. (#13544)
* В калькуляторе Windows 10 и 11, версии 10.1908 и выше,
NVDA будет автоматически объявлять результат при нажатии большего числа команд, которые представлены в "Инженерном режиме". (#13383)
* В Windows 11, теперь снова возможно выполнять навигацию и взаимодействовать с элементами пользовательского интерфейса,
такими как панель задач с помощью мыши и сенсорного взаимодействия. (#13506)
* NVDA теперь объявляет содержимое строки состояния в Блокноте Windows 11. (#13688)
* Функция подсветки объекта навигатора теперь применяется сразу же при её активации. (#13641)
* Исправлено чтение элементов одноколоночных списков. (#13659, #13735)
* В синтезаторе eSpeak, исправлено работа функции автоматического переключения для английского и французского языков. (#13727)
* В синтезаторе Windows OneCore, исправлена функция автоматического переключения языков, при попытке переключения на ранее удалённый язык. (#13732)

### Изменения для разработчиков

* Реализована поддержка сборки зависимостей NVDA с помощью Visual Studio 2022 (17.0).
Однако для тестовых и релизных сборок, всё ещё используется Visual Studio 2019. (#13033)
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

This release includes major improvements to UIA support with MS Office.
For Microsoft Office 16.0.15000 and higher on Windows 11, NVDA will use UI Automation to access Microsoft Word documents by default.
This provides a significant performance improvement over the old Object model access.

There are improvements to braille display drivers including Seika Notetaker, Papenmeier and HID Braille. 
There are also various Windows 11 bug fixes, for apps such as Calculator, Console, Terminal, Mail and Emoji Panel.

eSpeak-NG and LibLouis have been updated, adding new Japanese, German and Catalan tables.

Note:

 * This release breaks compatibility with existing add-ons.

### Новое

* Support for reporting notes in MS Excel with UI Automation enabled on Windows 11. (#12861)
* In recent builds of Microsoft Word via UI Automation on Windows 11, the existence of bookmarks, draft comments and resolved comments are now reported in both speech and braille. (#12861)
* The new `--lang` command line parameter allows overriding the configured NVDA language. (#10044)
* NVDA now warns about command line parameters which are unknown and not used by any add-ons. (#12795)
* In Microsoft Word accessed via UI Automation, NVDA will now make use of mathPlayer to read and navigate Office math equations. (#12946)
  * For this to work, you must be running Microsoft Word 365/2016 build 14326 or later. 
  * MathType equations must also be manually converted to Office Math by selecting each, opening the context menu, choosing Equation options, Convert to Office Math.
* Reporting of "has details" and the associated command to summarize the details relation have been updated to work in focus mode. (#13106)
* Seika Notetaker can now be auto-detected when connected via USB and Bluetooth. (#13191, #13142)
  * This affects the following devices: MiniSeika (16, 24 cells), V6, and V6Pro (40 cells)
  * Manually selecting the bluetooth COM port is also now supported.
* Added a command to toggle the braille viewer; there is no default associated gesture. (#13258)
* Added commands for toggling multiple modifiers simultaneously with a Braille display (#13152)
* The Speech Dictionary dialog now features a "Remove all" button to help clear a whole dictionary. (#11802)
* Added support for Windows 11 Calculator. (#13212)
* In Microsoft Word with UI Automation enabled on Windows 11, line numbers and section numbers can now be reported. (#13283, #13515)
* For Microsoft Office 16.0.15000 and higher on Windows 11, NVDA will use UI Automation to access Microsoft Word documents by default, providing a significant performance improvement over the old Object model access. (#13437)
 * This includes documents in Microsoft Word itself, and also the message reader and composer in Microsoft Outlook. 

### Изменения

* Espeak-ng has been updated to 1.51-dev commit `7e5457f91e10`. (#12950)
* Updated liblouis braille translator to [3.21.0](https://github.com/liblouis/liblouis/releases/tag/v3.21.0). (#13141, #13438)
  * Added new braille table: Japanese (Kantenji) literary braille.
  * Added new German 6 dot computer braille table.
  * Added Catalan grade 1 braille table. (#13408)
* NVDA will report selection and merged cells in LibreOffice Calc 7.3 and above. (#9310, #6897)
* Updated Unicode Common Locale Data Repository (CLDR) to 40.0. (#12999)
* `NVDA+Numpad Delete` reports the location of the caret or focused object by default. (#13060)
* `NVDA+Shift+Numpad Delete` reports the location of the review cursor. (#13060)
* Added default bindings for toggling modifier keys to Freedom Scientific displays (#13152)
* "Baseline" is no longer reported via the report text formatting command (`NVDA+f`). (#11815)
* Activate long description no longer has a default gesture assigned. (#13380)
* Report details summary now has a default gesture (`NVDA+d`). (#13380)
* NVDA needs to be restarted after installing MathPlayer. (#13486)

### Исправления

* Clipboard manager pane should no longer incorrectly steal focus when opening some Office programs. (#12736)
* On a system where the user has chosen to swap the primary mouse button from the left to the right, NVDA will no longer accidentally bring up a context menu instead of activating an item, in applications such as web browsers. (#12642)
* When moving the review cursor past the end of text controls, such as in Microsoft Word with UI Automation, "bottom" is correctly reported in more situations. (#12808)
* NVDA can report the application name and version for binaries placed in system32 when running under 64-bit version of Windows. (#12943)
* Improved consistency of output reading in terminal programs. (#12974)
  * Note that in some situations, when inserting or deleting characters in the middle of a line, the characters after the caret may again be read out.
* MS word with UIA: heading quick nav in browse mode no longer gets stuck on the final heading of a document, nor is this heading shown twice in the NVDA elements list. (#9540)
* In Windows 8 and later, the File Explorer status bar can now be retrieved using the standard gesture NVDA+end (desktop) / NVDA+shift+end (laptop). (#12845)
* Incoming messages in the chat of Skype for Business are reported again. (#9295)
* NVDA can again duck audio when using the SAPI5 synthesizer on Windows 11. (#12913)
* In Windows 10 Calculator, NVDA will announce labels for history and memory list items. (#11858)
* Gestures such as scrolling and routing again work with HID Braille devices. (#13228)
* Windows 11 Mail: After switching focus between apps, while reading a long email, NVDA no longer gets stuck on a line of the email. (#13050)
* HID braille: chorded gestures (e.g. `space+dot4`) can be successfully performed from the Braille display. (#13326)
* Fixed an issue where multiple settings dialogs could be opened at the same time. (#12818)
* Fixed a problem where some Focus Blue Braille displays would stop working after waking the computer from sleep. (#9830)
* "Baseline" is no longer spuriously reported when the "report superscript and subscript" option is active. (#11078)
* In Windows 11, NVDA will no longer prevent navigation in emoji panel when selecting emojis. (#13104)
* Prevents a bug causing double-reporting when using Windows Console and Terminal. (#13261)
* Fixed several cases where list items could not be reported in 64 bit applications, such as REAPER. (#8175)
* In the Microsoft Edge downloads manager, NVDA will now automatically switch to focus mode once the list item with the most recent download gains focus. (#13221)
* NVDA no longer causes 64-bit versions of Notepad++ 8.3 and above to crash. (#13311)
* Adobe Reader no longer crashes on startup if Adobe Reader's protected mode is enabled. (#11568)
* Fixed a bug where selecting the Papenmeier Braille Display Driver caused NVDA to crash. (#13348)
* In Microsoft word with UIA: page number and other formatting is no longer inappropriately announced when moving from a blank table cell to a cell with content, or from the end of the document into existing content. (#13458, #13459)
* NVDA will no longer fail to report the page title and start automatically reading, when a page loads in Google chrome 100. (#13571)
* NVDA no longer crashes when resetting the NVDA configuration to factory defaults while speak command keys is on. (#13634)

### Изменения для разработчиков

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

This is a minor release to fix a security issue.
Please responsibly disclose security issues to <info@nvaccess.org>.

### Security Fixes

* Addressed security advisory `GHSA-xc5m-v23f-pgr7`.
  * The symbol pronunciation dialog is now disabled in secure mode.

## 2021.3.4

This is a minor release to fix several security issues raised.
Please responsibly disclose security issues to <info@nvaccess.org>.

### Security Fixes

* Addressed security advisory `GHSA-354r-wr4v-cx28`. (#13488)
  * Remove the ability to start NVDA with debug logging enabled when NVDA runs in secure mode.
  * Remove the ability to update NVDA when NVDA runs in secure mode.
* Addressed security advisory `GHSA-wg65-7r23-h6p9`. (#13489)
  * Remove the ability to open the input gestures dialog in secure mode.
  * Remove the ability to open the default, temporary and voice dictionary dialogs in secure mode.
* Addressed security advisory `GHSA-mvc8-5rv9-w3hx`. (#13487)
  * The wx GUI inspection tool is now disabled in secure mode.

## 2021.3.3

This release is identical to 2021.3.2.
A bug existed in NVDA 2021.3.2 where it incorrectly identified itself as 2021.3.1.
This release correctly identifies itself as 2021.3.3.

## 2021.3.2

This is a minor release to fix several security issues raised.
Please responsibly disclose security issues to <info@nvaccess.org>.

### Bug Fixes

* Security fix: Prevent object navigation outside of the lockscreen on Windows 10 and Windows 11. (#13328)
* Security fix: The addons manager dialog is now disabled on secure screens. (#13059)
* Security fix: NVDA context help is no longer available on secure screens. (#13353)

## 2021.3.1

This is a minor release to fix several issues in 2021.3.

### Changes

* The new HID Braille protocol is no longer preferred when another braille display driver can be used. (#13153)
* The new HID Braille protocol can be disabled via a setting in the advanced settings panel. (#13180)

### Bug Fixes

* Landmark is once again abbreviated in braille. #13158
* Fixed unstable braille display auto detection for Humanware Brailliant and APH Mantis Q40 braille displays when using Bluetooth. (#13153)

## 2021.3

В этом выпуске представлена поддержка новой спецификации USB HID Braille.
Целью данной спецификации является стандартизация поддержки брайлевских дисплеев без необходимости использования отдельных драйверов.
Обновлён синтезатор речи eSpeak-NG и брайлевский транслятор LibLouis, включающий помимо прочего новые таблицы для русского сокращённого брайля и языка чивенда.
Звуки происходящих ошибок теперь можно включить в стабильных версиях NVDA с помощью новой опции в дополнительных настройках.
Режим "читать всё" в Microsoft Word теперь автоматически прокручивает читаемый документ для того, чтобы текущая позиция каретки всегда оставалась видимой на экране.
Сделано множество улучшений при использовании Microsoft Office через UI Automation.
Одно из них заключается в том, что NVDA теперь игнорирует большее количество макетных таблиц при чтении сообщений в Outlook.

Важное примечание:

Из-за обновления нашего сертификата безопасности, некоторые пользователи получают сообщение об ошибке при попытке NVDA 2021.2 проверить наличие обновлений.
NVDA теперь запрашивает у Windows обновление сертификатов безопасности, что предотвратит появление этой ошибки в будущем.
Пользователям, которые всё же столкнулись с данной проблемой, необходимо загрузить этот выпуск NVDA вручную.

### Новое

* В диалог "Жесты ввода" добавлена команда для переключения способа объявления стиля границ ячеек в таблицах. (#10408)
* Реализована поддержка новой спецификации USB HID Braille, призванной стандартизировать поддержку брайлевских дисплеев. (#12523)
  * Устройства, поддерживающие эту спецификацию, будут определяться NVDA автоматически.
  * Для получения технических подробностей о реализации данной спецификации в NVDA, обратитесь к документу https://github.com/nvaccess/nvda/blob/master/devDocs/hidBrailleTechnicalNotes.md
* Добавлена поддержка устройств VisioBraille Vario 4. (#12607)
* Звуки происходящих в NVDA ошибок теперь могут быть включены для любых версий программы с помощью новой опции в категории "Дополнительно" основного диалога настроек. (#12672)
* В Windows 10 и более поздних версиях, NVDA теперь объявляет количество найденных предложений при вводе поисковых запросов в таких приложениях как "Параметры" и Microsoft Store. (#7330, #12758, #12790)
* Табличная навигация теперь поддерживается в элементах управления сетка (grid), созданных с помощью командлета Out-GridView в PowerShell. (#12928)

### Изменения

* Синтезатор речи eSpeak-NG обновлён до версии 1.51-dev (коммит `74068b91bcd578bd7030a7a6cde2085114b79b44`). (#12665)
* NVDA теперь будет использовать eSpeak-NG по умолчанию, если ни один из установленных голосов OneCore не поддерживает предпочитаемый язык NVDA. (#10451)
* Если голоса OneCore постоянно будут приводить к сбою при попытках чтения текста, то NVDA автоматически вернётся к использованию eSpeak-NG в качестве текущего синтезатора. (#11544)
* При объявлении строки состояния текущего приложения по `NVDA+end`, перемещение к ней просмотрового курсора больше не выполняется.
Если вам требуется данный функционал, то назначьте своё сочетание клавиш на соответствующую команду в категории "Объектная навигация" диалога "Жесты ввода". (#8600)
* При попытке открытия диалога настроек, который уже открыт, NVDA теперь переводит системный фокус на существующий диалог, вместо вызова ошибки. (#5383)
* Брайлевский транслятор Liblouis обновлён до версии [3.19.0](https://github.com/liblouis/liblouis/releases/tag/v3.19.0). (#12810)
  * Добавлены новые трансляционные таблицы для русского сокращённого брайля и языка чивенда.
* Текст на web-страницах, выделенный тегом "<mark>", теперь объявляется NVDA как "подсвеченный". (#12892)
* NVDA больше не будет пытаться завершать свою работу, когда открытые диалоговые окна ожидают от пользователя запрошенного действия (например "Подтверждения/Отмены"). (#12984)

### Исправления

* Отслеживание модификаторов клавиатуры (таких как Control или Insert) теперь более надёжно, когда watchdog восстанавливается. (#12609)
* Теперь снова возможно выполнять проверку наличия обновлений NVDA на некоторых системах, где это ранее не работало. Например на свежеустановленных копиях Windows. (#12729)
* NVDA теперь корректно объявляет пустые ячейки в таблицах Microsoft Word при использовании UI Automation. (#11043)
* В ячейках сетки данных ARIA на web-страницах, нажатие клавиши Escape теперь передаётся сетке и больше не приводит к безусловному отключению режима редактирования. (#12413)
* При чтении ячейки заголовка таблицы в Chrome, исправлено двойное объявление названия столбца. (#10840)
* NVDA больше не сообщает числовое значение UIA-ползунков, для которых определено текстовое представление их значения. (UIA ValuePattern теперь предпочтительнее чем RangeValuePattern). (#12724)
* NVDA больше не рассматривает значение UIA-ползунков как процентную величину.
* Объявление координат ячеек в Microsoft Excel при использовании UI Automation теперь снова корректно работает на Windows 11. (#12782)
* NVDA больше не устанавливает недопустимые Python-локали. (#12753)
* Если отключённое дополнение NVDA было удалено, а затем снова установлено, то оно вновь будет включено. (#12792)
* Исправлены ошибки, связанные с обновлением и удалением дополнений, когда каталог дополнения переименовывается или имеются открытые файлы. (#12792, #12629)
* При использовании UI Automation для доступа к таблицам Microsoft Excel, NVDA больше не делает лишних объявлений, когда в таблице выделена единственная ячейка. (#12530)
* NVDA в LibreOffice Writer теперь сообщает больше текста в диалоговых окнах, например в диалогах подтверждения. (#11687)
* Чтение/навигация в режиме обзора в Microsoft Word через UI Automation теперь гарантирует, что документ всегда прокручивается, так что текущая позиция курсора режима обзора видна на экране, а позиция системной каретки в режиме редактирования корректно отражает позицию курсора режима обзора. (#9611)
* При активации режима "читать всё" в Microsoft Word, доступ к которому осуществляется через UI Automation, документ теперь автоматически прокручивается, а позиция системной каретки корректно обновляется вслед за читаемым текстом. (#9611)
* При чтении электронных писем в Microsoft Outlook и использовании для доступа к ним UI Automation, некоторые таблицы теперь рассматриваются как макетные, что означает, что они больше не будут сообщаться по умолчанию. (#11430)
* Исправлена редкая ошибка возникающая при смене аудиоустройства. (#12620)
* Ввод с помощью таблиц литературного Брайля теперь должен вести себя более надежно в полях редактирования. (#12667)
* Теперь при навигации по календарю из области уведомлений Windows, NVDA сообщает день недели полностью. (#12757)
* При использовании китайского метода ввода, такого как "Тайвань - Microsoft Quick" в Microsoft Word, прокрутка брайлевского дисплея вперёд и назад больше не приводит к некорректному переходу в исходную позицию системной каретки. (#12855)
* При доступе к документам Microsoft Word через UI Automation, навигация по предложениям (Alt+↓ и Alt+↑) теперь работает корректно. (#9254)
* При доступе к документам Microsoft Word через UI Automation, теперь сообщается об отступах абзацев. (#12899)
* При доступе к документам Microsoft Word через UI Automation, команда переключения отслеживания изменений и некоторые другие локализованные команды теперь корректно объявляются. (#12904)
* Исправлено дублирование речевого и брайлевского вывода, когда "описание" объекта совпадает с его "содержанием" или "именем". (#12888)
* При доступе к документам Microsoft Word через UI Automation, звук для орфографических ошибок при наборе текста воспроизводится теперь более точно. (#12161)
* В Windows 11, NVDA больше не объявляет "область" при переключении между приложениями по Alt+Tab. (#12648)
* Новая боковая панель заметок теперь поддерживается в Microsoft Word при отключённой поддержке UI Automation. Нажимайте Alt+F12 для перемещения между этой панелью и документом. (#12982)

### Изменения для разработчиков

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

В этом выпуске представлена предварительная поддержка Windows 11.
Хотя Windows 11 ещё не выпущена, этот выпуск был протестирован на её предварительных версиях.
Он также включает важное исправление для функции затемнения экрана (см. Важное примечание).
Средство восстановления COM-объектов теперь может решать больше проблем при запуске NVDA.
Есть обновления синтезатора eSpeak и брайлевского транслятора LibLouis.
Также есть различные исправления ошибок и улучшения, в частности, для поддержки брайля и терминальных программ Windows, калькулятора, панели эмодзи и истории буфера обмена.

### Важное примечание

Из-за изменений в Windows Magnification API, функцию затемнения экрана пришлось обновить для поддержки новейших версий Windows.
Используйте NVDA 2021.2 для активации функции затемнения экрана в Windows 10 21H2 (10.0.19044) или более поздних версиях.
Сюда входят участники программы предварительной оценки Windows 10 и Windows 11.
В целях безопасности при использовании новой версии Windows, получите визуальное подтверждение того, что затемнение экрана делает экран полностью чёрным.

### Новое

* Экспериментальная поддержка аннотаций ARIA, а именно:
  * Добавлена команда для чтения сводки деталей объекта с aria-details. (#12364)
  * В категорию настроек "Дополнительно" добавлен флажок "Сообщать наличие дополнительных подробностей в режиме обзора". (#12439)
* В Windows 10 версии 1909 и более поздних (включая Windows 11), NVDA объявляет количество предложений при выполнении поиска в проводнике. (#10341, #12628)
* В Microsoft Word NVDA теперь объявляет результат использования горячих клавиш отступов и висячих отступов при выполнении соответствующих команд. (#6269)

### Изменения

* Синтезатор eSpeak-NG обновлён до версии 1.51-dev (коммит `ab11439b18238b7a08b965d1d5a6ef31cbb05cbb`). (#12449, #12202, #12280, #12568)
* Если чтение статей включено в настройках форматирования документа (флажок "Статьи"), то NVDA объявляет "статья" после произнесения содержимого соответствующей области, а не перед, как было раньше. (#11103)
* Брайлевский транслятор Liblouis обновлён до версии [3.18.0](https://github.com/liblouis/liblouis/releases/tag/v3.18.0). (#12526)
  * Добавлено большое число новых трансляционных таблиц.
* Название компонента Windows 10 OCR было изменено на Windows OCR. (#12690)

### Исправления

* В калькуляторе Windows 10 NVDA теперь выводит выражения калькулятора на брайлевский дисплей. (#12268)
* В терминальных программах в Windows 10 версии 1607 и более поздних при вставке или удалении символов в середине строки символы справа от каретки больше не считываются. (#3200)
  * Diff Match Patch включён по умолчанию. (#12485)
* Брайлевский ввод правильно работает со следующими сокращёнными таблицами второй ступени: арабский, испанский, урду, китайский (мандаринский диалект). (#12541)
* Средство восстановления COM-объектов теперь решает больше проблем, особенно в 64-разрядной Windows. (#12560)
* Улучшения в работе с кнопками на брайлевском устройстве Seika Notetaker от Nippon Telesoft. (#12598)
* Улучшения в оповещениях панели эмодзи Windows и истории буфера обмена. (#11485)
* Обновлены описания символов бенгальского алфавита. (#12502)
* NVDA безопасно завершает работу при запуске нового процесса. (#12605)
* Повторный выбор драйвера брайлевского дисплея Handy Tech в диалоге "Выбор брайлевского дисплея" больше не вызывает ошибок. (#12618)
* Windows версии 10.0.22000 или более поздней распознаётся как Windows 11, а не Windows 10. (#12626)
* Поддержка затемнения экрана была исправлена и протестирована для версий Windows до 10.0.22000. (#12684)
* Если при фильтрации жестов ввода не отображаются результаты, диалог настройки жестов ввода продолжает работать должным образом. (#12673)
* Исправлена ошибка, из-за которой в некоторых ситуациях не объявлялся первый пункт подменю. (#12624)

### Изменения для разработчиков

* `characterProcessing.SYMLVL_*` constants should be replaced using their equivalent `SymbolLevel.*` before 2022.1. (#11856, #12636)
* `controlTypes` has been split up into various submodules, symbols marked for deprecation must be replaced before 2022.1. (#12510)
  * `ROLE_*` and `STATE_*` constants should be replaced to their equivalent `Role.*` and `State.*`.
  * `roleLabels`, `stateLabels` and `negativeStateLabels` have been deprecated, usages such as `roleLabels[ROLE_*]` should be replaced to their equivalent `Role.*.displayString` or `State.*.negativeDisplayString`.
  * `processPositiveStates` and `processNegativeStates` have been deprecated for removal.
* On Windows 10 Version 1511 and later (including Insider Preview builds), the current Windows feature update release name is obtained from Windows Registry. (#12509)
* Deprecated: `winVersion.WIN10_RELEASE_NAME_TO_BUILDS` will be removed in 2022.1, there is no direct replacement. (#12544)

## 2021.1

Этот выпуск включает в себя экспериментальную поддержку UI Automation для Microsoft Excel и web-браузеров на основе движка Chromium.
Имеются исправления для ряда языков и улучшение в активации ссылок с брайлевского дисплея.
Обновлён общий репозиторий языковых данных консорциума Unicode, набор читаемых математических символов и брайлевский транслятор LibLouis.
А также множество других улучшений и исправлений, в том числе для Microsoft Office, Visual Studio и ряда языков.

Обратите внимание:

 * Этот выпуск нарушает совместимость с существующими дополнениями.
 * Также в нём прекращена поддержка Adobe Flash.

### Новое

* Добавлена предварительная поддержка UI Automation для web-браузеров на основе движка Chromium (таких как Microsoft Edge). (#12025)
* Добавлена экспериментальная поддержка UI Automation для Microsoft Excel. Рекомендуется только для сборок Excel 16.0.13522.10000 и выше. (#12210)
* В Python консоли NVDA, упрощена навигация по результатам выполненных команд. (#9784)
  * Команды Alt+стрелки вниз/вверх выполняют переход к следующему или предыдущему результату вывода (при зажатой клавише Shift происходит его выделение).
  * Команда Control+L очищает область вывода результатов.
* NVDA теперь сообщает категории, назначенные на встречи в Microsoft Outlook, если таковые имеются. (#11598)
* Добавлена поддержка брайлевского дисплея Seika Notetaker от Nippon Telesoft. (#11514)

### Изменения

* В режиме обзора, элементы управления теперь могут быть активированы кнопками маршрутизации на брайлевском дисплее, расположенными над их сокращённом описанием (например "с" для ссылки). Это особенно полезно при активации флажков не имеющих текстовой метки. (#7447)
* При активной функции затемнения экрана, NVDA теперь уведомляет пользователя о невозможности использования компонента Windows 10 OCR. (#11911)
* Общий репозиторий языковых данных консорциума Unicode (CLDR), используемый в NVDA для чтения символов эмодзи, обновлён до версии 39.0. (#11943, #12314)
* В таблицу символов NVDA добавлено большое количество различных математических знаков. (#11467)
* Поставляемая с NVDA документация, а именно руководство пользователя, список изменений и список горячих клавиш, теперь имеет обновлённый внешний вид. (#12027)
* NVDA теперь сообщает о неподдерживаемости экранного представления режима обзора (NVDA+V) при попытке активации этого режима в приложениях, которые его не поддерживают. Например в Microsoft Word. (#7297)
* Опция "Пытаться отменять речевой вывод для устаревших событий фокуса" в категории "Дополнительно" диалога настроек NVDA, теперь включена по умолчанию. (#10885)
  * Такое поведение можно отключить установкой этой опции в значение "Нет".
  * В таких Web-приложениях как Gmail, NVDA больше не будет сообщать устаревшую информацию при быстром перемещении фокуса.
* Библиотека брайлевской трансляции Liblouis обновлена до версии [3.17.0](https://github.com/liblouis/liblouis/releases/tag/v3.17.0). (#12137)
  * Добавлены новые таблицы для белорусского компьютерного и литературного брайля, а также таблицы первой и второй ступени для языка урду.
* Из NVDA удалена поддержка Flash-содержимого, поскольку компания Adobe прекратила поддержку этой технологии. (#11131)
* NVDA теперь может завершать свою работу даже при открытых окнах. Процесс завершения работы автоматически закроет все окна и диалоги NVDA перед выходом. (#1740)
* Окно просмотрщика речи теперь может быть закрыто сочетанием клавиш `Alt+F4`. Также оно теперь имеет стандартную кнопку закрытия окна для её нажатия с помощью указателя мыши. (#12330)
* Окно просмотрщика брайля теперь имеет стандартную кнопку для её нажатия с помощью указателя мыши. (#12328)
* В диалоге "Список элементов", клавиша-ускоритель для кнопки "Активировать" была удалена в некоторых локалях для избежания коллизий с метками радиокнопок для выбора типа элементов. Когда кнопка доступна, она по-прежнему используется по умолчанию в диалоговом окне и, как таковая, всё ещё может быть вызвана простым нажатием Enter из самого списка элементов. (#6167)

### Исправления

* Список сообщений в Microsoft Outlook 2010 снова доступен для чтения. (#12241)
* В окнах терминалов на Windows 10 версии 1607 и выше, вставка или удаление символа в середине строки, больше не приводит к чтению всех символов справа от каретки. (#3200)
  * Это экспериментальное исправление может быть включено вручную в категории "Дополнительно" диалога настроек NVDA, путём установки опции "Diff-алгоритм" в значение "Разрешить использование Diff Match Patch".
* В Microsoft Outlook, нажатие Shift+Tab для перехода от тела сообщения к его теме, больше не должно вызывать неуместное чтение расстояния до края элемента. (#10254)
* В Python-консоли NVDA, теперь поддерживается вставка символа табуляции в начало непустой строки ввода и автодополнение по клавише Tab в её середине. (#11532)
* В окне с информацией о форматировании текста (NVDA+F дважды быстро) и других подобных окнах с режимом обзора, больше не должно быть пустых строк при отключённом режиме экранного представления (NVDA+V). (#12004)
* В документах Microsoft Word, при включённой поддержке UI Automation, теперь возможно читать существующие в документе примечания. (#9285)
* Улучшена производительность при взаимодействии с Visual Studio. (#12171)
* Исправлены ошибки графического интерфейса NVDA, приводящие к исчезновению некоторых элементов управления при использовании языков с написанием справа налево. (#8859)
* Направление компоновки графического интерфейса NVDA теперь основывается на языке интерфейса NVDA, а не на системной локали. (#638)
  * Известная проблема для языков с написанием справа налево: правая граница группы элементов обрезается вместе с её метками и элементами управления. (#12181)
* Python-локаль теперь устанавливается в соответствии с выбранным в настройках NVDA языком интерфейса, что также будет происходить при использовании языка по умолчанию. (#12214)
* Вызов метода textInfos.TextInfo.getTextInChunks, относящегося к редакторам с поддержкой форматирования, таким как просмотрщик журнала NVDA, больше не вызывает его зависание. (#11613)
* Теперь снова возможно использовать NVDA на языках содержащих символ подчёркивания (_) в имени локали (например de_CH) на Windows 10 версий 1803 и 1809. (#12250)
* В WordPad, настройка чтения подстрочного и надстрочного текста теперь работает как и ожидается. (#12262)
* В NVDA больше не происходит сбой при попытке чтения обновлённого содержимого в фокусе на web-страницах, если старый фокус пропадает и заменяется новым в той же позиции. (#12147)
* Зачёркнутость, надстрочность и подстрочность теперь сообщается для всей ячейки Excel целиком, если соответствующая опция включена в настройках форматирования NVDA. (#12264)
* Исправлено копирование конфигурации во время установки NVDA из переносной копии, если целевой каталог отсутствует или является пустым. (#12071, #12205)
* Исправлено неправильное объявление некоторых букв с ударениями или диакритическими знаками, когда включена опция "Говорить „Большая“ перед заглавными буквами". (#11948)
* Исправлен сбой при изменении высоты голоса для SAPI4-синтезаторов. (#12311)
* Установщик NVDA теперь также учитывает параметр командной строки `--minimal` и не воспроизводит звук запуска, следуя тому же документированному поведению, что и исполняемый файл установленной или переносной копии NVDA. (#12289)
* В Microsoft Word или Outlook, клавиша быстрой навигации по таблицам теперь может переходить к макетным таблицам, если соответствующая опция включена в настройках режима обзора NVDA. (#11899)
* NVDA больше не будет объявлять "↑↑↑" для символов эмодзи в некоторых языках. (#11963)
* Синтезатор eSpeak теперь снова поддерживает кантонский и мандаринский языки. (#10418)
* В новом Microsoft Edge на основе Chromium, текстовые поля, такие как адресная строка, теперь корректно сообщаются даже если они являются пустыми. (#12474)
* Исправлен драйвер для брайлевских дисплеев Seika. (#10787)

### Изменения для разработчиков

* Внимание: этот выпуск нарушает совместимость с API существующих дополнений. Дополнения необходимо будет повторно протестировать и обновить их манифест.
* Система сборки NVDA теперь извлекает все Python-зависимости с помощью pip и сохраняет их в виртуальном окружении Python. Всё это делается прозрачно для пользователя.
  * Для сборки NVDA, следует как и раньше использовать SCons. То есть выполнять scons.bat в корневом каталоге репозитория. Запуск `py -m SCons` больше не поддерживается, а также `scons.py` был удалён.
  * Для запуска NVDA из исходного кода, вместо прямого выполнения `source/nvda.pyw`, разработчик теперь должен использовать `runnvda.bat` из корневого каталога репозитория. Если вы попытаетесь выполнить `source/nvda.pyw`, то получите окно с уведомлением о том, что это больше не поддерживается.
  * Для выполнения модульных тестов, выполните `rununittests.bat [<дополнительные опции тестирования>]`
  * Для выполнения системных тестов, выполните `runsystemtests.bat [<дополнительные опции тестирования>]`
  * Для выполнения статического анализа, выполните `runlint.bat <base branch>`
  * Для получения дополнительной информации, пожалуйста, обратитесь к файлу readme.md.
* Также были обновлены следующие Python-зависимости:
  * comtypes обновлён до версии 1.1.8.
  * pySerial обновлён до версии 3.5.
  * wxPython обновлён до версии 4.1.1.
  * Py2exe обновлён до версии 0.10.1.0.
* Метод `LiveText._getTextLines` был удалён. (#11639)
  * Вместо него следует переопределять метод `_getText`, который возвращает весь текст объекта.
* Экземпляры `LiveText` теперь могут вычислять разницу в текстах посимвольно. (#11639)
  * Чтобы изменить поведение в поиске различий для некоторого объекта, переопределите свойство `diffAlgo` (см. строку документации для получения дополнительной информации).
* При определении скрипта с помощью декоратора scriptHandler.script, теперь может быть указан логический аргумент 'allowInSleepMode', управляющий доступностью скрипта в режиме сна. (#11979)
* Следующие функции были удалены из модуля config. (#11935)
  * canStartOnSecureScreens - вместо него используйте config.isInstalledCopy.
  * hasUiAccess и execElevated - используйте их из модуля systemUtils.
  * getConfigDirs - вместо него используйте globalVars.appArgs.configPath.
* Константы REASON_* были удалены из модуля controlTypes. Пожалуйста, вместо них используйте controlTypes.OutputReason. (#11969)
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

Этот выпуск включает в себя поддержку новых методов ввода для китайского языка, обновлённую версию библиотеки брайлевской трансляции Liblouis, а также возможность вызова диалога "Список элементов" (NVDA+F7) в режиме редактирования.
В диалоговых окнах NVDA теперь доступна контекстно-зависимая справка при нажатии клавиши F1.
Реализованы улучшения в правилах произношения символов, речевых словарях, брайлевских сообщениях NVDA и режиме беглого чтения.
Исправлены ошибки и улучшена поддержка приложений Почта Windows 10, Outlook, Teams, Visual Studio, Azure Data Studio и Foobar2000.
При работе с web-приложениями, улучшена взаимодействие с Документами Google и значительно увеличен уровень поддержки атрибутов WAI-ARIA.
А также множество других важных улучшений и исправлений.

### Новое

* Нажатие F1 в диалоговых окнах NVDA, теперь открывает соответствующий справочный раздел руководства пользователя. (#7757)
* В Microsoft SQL Server Management Studio и Visual Studio 2017 и новее, добавлена поддержка технологии автодополнения (IntelliSense). (#7504)
* В таблице произношения символов NVDA добавлена поддержка группировки в определениях комплексных символов, а также поддержка ссылок на группы в правилах замены, что делает их более мощными и простыми в использовании. (#11107)
* NVDA теперь уведомляет пользователя при попытке создания в речевом словаре записи с неверным регулярным выражением в качестве замены. (#11407)
  * В частности, теперь обнаруживаются ошибки группировки.
* Добавлена поддержка новых методов ввода для традиционного китайского и пиньинь в Windows 10. (#11562)
* Заголовки элементов-вкладок на web-страницах теперь рассматриваются в качестве полей форм, между которыми можно выполнять быструю навигацию клавишей F. (#10432)
* В диалоге "Жесты ввода" добавлена команда для переключения чтения выделенного (подсвеченного) текста в документах (не путать с пользовательским выделением текста для последующего копирования/вырезания). Желаемый жест на эту команду пользователь должен назначить самостоятельно. (#11807)
* Добавлен новый параметр командной строки --copy-portable-config, который позволяет автоматически скопировать переданную конфигурацию в пользовательскую учётную запись при тихой установке NVDA. (#9676)
* Наведение с удержанием указателя мыши в окне просмотрщика брайля на отображаемые брайлевские ячейки теперь выполняет команду маршрутизации к этим ячейкам. (#11804)
* NVDA теперь автоматически определяет подключение устройств Humanware Brailliant BI 40X и 20X как через USB, так и по Bluetooth. (#11819)

### Изменения

* Библиотека брайлевской трансляции Liblouis обновлена до версии 3.16.1:
 * Устранены множественные крахи библиотеки.
 * Добавлена таблица башкирского брайля первой ступени.
 * Добавлена таблица коптского восьмиточечного компьютерного брайля.
 * Добавлены таблицы русского литературного брайля и русского литературного брайля с индикацией заглавных букв.
 * Добавлена таблица африкаанского брайля второй ступени.
 * Удалена старая таблица русского брайля первой ступени.
* Использование команд NVDA для поиска следующего/предыдущего фрагмента текста в документе с режимом обзора, больше не останавливает режим непрерывного чтения, если в настройках клавиатуры включена опция для беглого чтения. NVDA продолжит непрерывное чтение с позиции найденного текста. (#11563)
* Для брайлевских дисплеев HIMS, нажатие клавиши F3 было переназначено на пробел+точки 148. (#11710)
* Повышено удобство настройки отображения сообщений NVDA на брайлевском дисплее. (#11602)
* В web-браузерах и других приложениях поддерживающих режим обзора, диалог со списком элементов (NVDA+F7), теперь может быть вызван и в режиме редактирования. (#10453)
* Чтение обновлений в "живых" областях ARIA (live regions), теперь управляется настройкой "Чтения динамических изменений содержимого" (NVDA+5). (#9077)
* При копировании текста средствами NVDA (например Control+C в режиме обзора, тройное нажатие NVDA+T или при использовании команд NVDA+F9/F10), теперь сначала сообщается фраза "Скопировано в буфер обмена", а затем сам скопированный текст. (#6757)
* Улучшено чтение таблицы с графическим представлением дисков в окне стандартного средства управления дисками Windows. (#10048)
* Метки для недоступных элементов управления (выделенных серым цветом), теперь также являются недоступными. (#11809)
* Общий репозиторий языковых данных консорциума Unicode (CLDR), используемый в NVDA для чтения символов эмодзи, обновлён до версии 38. (#11817)
* Встроенная функция подсветки фокуса была переименована в визуальную подсветку. (#11700)

### Исправления

* NVDA теперь снова корректно работает с редактируемыми полями в приложении для радиолюбителей Fast Log Entry. (#8996)
* NVDA теперь корректно сообщает прошедшее время в Foobar2000, если отсутствует общее время воспроизведения (например при проигрывании интернет-потока). (#11337)
* NVDA для редактируемого содержимого на web-страницах теперь корректно учитывает атрибут aria-roledescription. (#11607)
* Сообщение "список" больше не произносится на каждой строке списка в Google Документах или в любом другом редактируемом содержимом в Google Chrome. (#7562)
* На web-страницах внутри редактируемого содержимого, NVDA теперь объявляет переход на новый элемент списка с предыдущего, происходящий при использовании клавиш-стрелок для перемещения по символам или словам. (#11569)
* NVDA теперь правильно сообщает текущую строку, когда курсор устанавливается в конец ссылки на последнем элементе списка в Google Документах или любом другом редактируемом содержимом на web-страницах. (#11606)
* Открытие и закрытие меню "Пуск" на Windows 7 теперь корректно обратно устанавливает системный фокус в исходное положение. (#10567)
* При переключении вкладок в Firefox, NVDA теперь корректно сообщает заголовок вкладки даже если активна опция "Пытаться отменять речевой вывод для устаревших событий фокуса". (#11397)
* NVDA теперь корректно сообщает элемент списка, после перехода к нему буквенно-цифровыми клавишами при использовании голосов SAPI5 Ivona. (#11651)
* Теперь снова возможно использовать режим обзора для чтения электронных писем в приложении Почта Windows 10 версии 16005.13110 и выше. (#11439)
* При использовании голосов SAPI5 Ivona от harposoftware.com, NVDA теперь корректно сохраняет свою конфигурацию, без ошибок переключает синтезаторы и больше не теряет речевой вывод при перезагрузке. (#11650)
* С клавиатур брайлевских дисплеев HIMS, при использовании компьютерного брайля, теперь возможно вводить цифру 6. (#11710)
* Значительно улучшена производительность при работе с Azure Data Studio. (#11533, #11715)
* Заголовок поиска NVDA в режиме обзора, теперь снова корректно сообщается при активной опции "Пытаться отменять речевой вывод для устаревших событий фокуса". (#11632)
* NVDA больше не должна зависать при пробуждении компьютера с установленным фокусом в документе Microsoft Edge. (#11576)
* Для восстановления функциональности режима обзора, больше нет необходимости нажимать tab или перемещать фокус после закрытия контекстного меню в Microsoft Edge. (#11202)
* NVDA теперь корректно сообщает элементы списков в 64-х разрядных приложениях, таких как Tortoise SVN. (#8175)
* В web-браузерах Google Chrome и Firefox, ARIA-элемент treegrid (древовидная сетка) теперь представляется в режиме обзора как обычная таблица. (#9715)
* Команда поиска NVDA в обратном порядке в режиме обзора (NVDA+Shift+F3), теперь при необходимости может вызывать показ диалога поиска. (#11770)
* Скрипт NVDA больше не рассматривается как повторяющийся, если между двумя исполнениями этого скрипта происходит несвязанное с ним нажатие клавиши. (#11388)
* Чтение тегов акцентирования strong и emphasis в Internet Explorer теперь снова можно отключить снятием флага "Акцентирование" в настройках форматирования документа NVDA. (#11808)
* Подвисание на несколько секунд, наблюдаемое небольшим количеством пользователей при перемещении клавишами стрелок между ячейками в Microsoft Excel, больше происходить не должно. (#11818)
* В Microsoft Teams таких версий как 1.3.00.28xxx, NVDA теперь корректно читает сообщения чата и командные каналы даже при неправильно сфокусированном меню. (#11821)
* Текст, одновременно помеченный как орфографическая и грамматическая ошибка в Google Chrome, будет соответствующим образом объявлен NVDA как орфографическая и грамматическая ошибка. (#11787)
* При использовании Microsoft Outlook с французской локалью, сочетание клавиш для команды "Ответить всем" (Control+Shift+R) теперь снова работает. (#11196)
* Всплывающие подсказки IntelliSense в Visual Studio, предоставляющие дополнительные сведения о выбранном в данный момент элементе IntelliSense, теперь сообщаются только один раз. (#11611)
* В калькуляторе Windows 10, NVDA больше не будет объявлять о ходе вычислений, если чтение вводимых символов отключено. (#9428)
* NVDA больше не завершает аварийно свою работу при использовании таблицы американского английского брайля второй ступени, при отображении некоторого содержимого, такого как URL. (#11754)
* По команде NVDA+F теперь снова возможно получать информацию о форматировании сфокусированной ячейки в Microsoft Excel. (#11914)
* На брайлевских дисплеях Papenmeier, поддерживающих QWERTY-ввод, он теперь снова работает и не вызывает случайные зависания NVDA. (#11944)
* В web-браузерах на основе движка Chromium, были решены наблюдаемые в некоторых случаях проблемы, когда не работала навигация по таблицам, а NVDA не сообщала число строк/столбцов в таблицах. (#12359)

### Изменения для разработчиков

* Системные тесты теперь могут отправлять нажатия клавиш с помощью функции spy.emulateKeyPress, которая принимает идентификатор клавиши, соответствующий собственным именам клавиш NVDA, и по умолчанию также блокируется до тех пор, пока действие не будет выполнено. (#11581)
* NVDA для нормального функционирования больше не требует в качестве текущей рабочей директории использовать директорию приложения самой NVDA. (#6491)
* Экземпляры NVDAObject теперь предоставляют свойство liveRegionPoliteness, определяющее приоритет обработки изменений в "живых" областях ARIA (live regions). (#11596)
* Теперь возможно определять отдельные жесты для Outlook и документов Word. (#11196)

## 2020.3

Этот выпуск содержит несколько значительных улучшений стабильности и производительности при работе в приложениях Microsoft Office. Добавлены настройки для отключения поддержки функционала сенсорного взаимодействия и чтения графических элементов.
NVDA теперь может объявлять наличие выделенного (подсвеченного) содержимого в web-браузерах, а также включает в себя новые брайлевские таблицы для немецкого языка.

### Новое

* В категории настроек "Форматирование документа" теперь возможно отключить чтение графических элементов. Обратите внимание, что при снятии соответствующего флажка, NVDA всё равно будет сообщать альтернативный текст для графических элементов, если он доступен. (#4837)
* В категории настроек "Сенсорное взаимодействие" теперь возможно отключить поддержку сенсорного взаимодействия со стороны NVDA. Переключать эту поддержку теперь можно также с помощью сочетания клавиш NVDA+Control+Alt+T. (#9682)
* Добавлены новые брайлевские таблицы для немецкого языка. (#11268)
* NVDA теперь определяет текстовые элементы управления UIA, доступные только для чтения. (#10494)
* NVDA во всех web-браузерах теперь сообщает наличие выделенного (подсвеченного) содержимого (обёрнутого тегом <mark> или имеющего атрибут role="mark"), как через речевой, так и через брайлевский вывод. (#11436)
 * Такое поведение можно отключить снятием нового флажка "Выделение (подсвеченный текст)" в категории настроек "Форматирование документа".
* В диалоге "Жесты ввода" теперь возможно добавлять пользовательские сочетания клавиш системной клавиатуры для их последующей эмуляции. (#6060)
  * Для этого выберите категорию "Эмулируемые клавиши системной клавиатуры" и нажмите кнопку "Добавить".
* NVDA теперь поддерживает устройства Handy Tech Active Braille с джойстиком. (#11655)
* Настройка "Автоматический переход в режим редактирования при перемещении каретки" в категории настроек режима обзора, теперь совместима с отключённой опцией "Автоматически устанавливать системный фокус на фокусируемые элементы". (#11663)

### Изменения

* Команда чтения форматирования текста под просмотровым курсором (NVDA+F) теперь предоставляет информацию о форматировании в позиции системной каретки. Для получения данных о форматировании под просмотровым курсором, теперь следует использовать команду NVDA+Shift+F. (#9505)
* По умолчанию NVDA в режиме обзора больше не устанавливает автоматически системный фокус на фокусируемые элементы при перемещении виртуального курсора, улучшая таким образом стабильность и производительность. (#11190)
* Общий репозиторий языковых данных консорциума Unicode (CLDR), используемый в NVDA для чтения символов эмодзи, обновлён с версии 36.1 до версии 37. (#11303)
* Синтезатор речи eSpeak-NG обновлён до версии 1.51-dev, коммит 1fb68ffffea4.
* В списке с элементами-флажками, теперь возможно использовать команды табличной навигации NVDA, если такой список является многоколоночным. (#8857)
* В диалоге подтверждения удаления дополнения из менеджера дополнений NVDA, фокус по умолчанию теперь установлен на кнопке "Нет". (#10015)
* Диалог "Список элементов" в Microsoft Excel теперь отображает формулы в их локализованной форме. (#9144)
* NVDA теперь использует корректную терминологию для заметок в Microsoft Excel. (#11311)
* При использовании в режиме обзора команды приведения объектного навигатора к системному фокусу, просмотровый курсор теперь корректно устанавливается в позицию виртуального курсора. (#9622)
* Отдельное окно с режимом обзора, используемое в NVDA к примеру для представления информации о форматировании текста (NVDA+F), теперь имеет немного больший размер и выровнено по центру экрана. (#9910)

### Исправления

* При перемещении по словам, NVDA теперь всегда произносит встречаемые одиночные символы (например знаки препинания) со следующими за ними пробельными символами, независимо от настроек уровня пунктуации. (#5133)
* В приложениях использующих QT 5.11 или новее, NVDA теперь снова корректно сообщает описание объектов. (#8604)
* NVDA больше не молчит при удалении слов по Control+Delete. (#3298, #11029)
  * Теперь при этом сообщается слово расположенное справа от удаляемого.
* В категории общих настроек NVDA, список языков интерфейса теперь сортируется корректно. (#10348)
* В диалоге "Жесты ввода" значительно увеличина производительность поиска команды при использовании поля "Фильтр". (#10307)
* Теперь с брайлевского дисплея можно вводить Unicode-символы с кодовыми позициями больше чем U+FFFF. (#10796)
* В Windows 10 May 2020 Update, NVDA теперь сообщает содержимое диалога "Открыть с помощью". (#11335)
* В категорию "Дополнительно" диалога настроек NVDA, добавлена новая экспериментальная опция "Включить выборочную регистрацию событий и изменений свойств UI Automation", задействование которой значительно увеличивает производительность в UIA-приложениях, таких как Microsoft Visual Studio. (#11077, #11209)
* Для отмечаемых элементов списка, NVDA больше не сообщает ненужное состояние выделенности для выбранных элементов, и в соответствующих случаях сообщает состояние не выделенности для невыбранных элементов. (#8554)
* На Windows 10 May 2020 Update, NVDA в диалоге выбора синтезатора теперь корректно показывает устройство вывода по умолчанию "Переназначение звуковых устр.". (#11349)
* В Internet Explorer, NVDA теперь корректно сообщает номера упорядоченных/нумерованных списков (элемент <ol>), если номер списка не начинается с 1. (#8438)
* NVDA в Google chrome теперь сообщает состояние "не отмечено" для всех отмечаемых элементов управления (не только флажков), которые на текущий момент не отмечены. (#11377)
* Теперь снова возможно выполнять навигацию по различным элементам управления, если в настройках NVDA выбран арагонский язык интерфейса. (#11384)
* NVDA больше не должна подвисать в Microsoft Word, что иногда наблюдалось при быстром нажатии клавиш-стрелок вверх/вниз или при вводе символов с брайлевского дисплея. (#11431, #11425, #11414)
* NVDA больше не добавляет несуществующий завершающий пробел при копировании имени и значения текущего объекта навигатора в буфер обмена. (#11438)
* NVDA больше не активирует профиль конфигурации для режима непрерывного чтения, если нет доступного текста для чтения. (#10899, #9947)
* NVDA теперь может корректно читать список возможностей в менеджере Internet Information Services (IIS). (#11468)
* NVDA теперь сохраняет устройство вывода звука открытым, улучшая тем самым производительность на некоторых звуковых картах. (#5172, #10721)
* NVDA в Microsoft Word больше не подвисает и не завершает свою работу при удерживании клавиш Control+Shift+↓. (#9463)
* NVDA в дереве каталогов Google Диска теперь всегда сообщает состояния свёрнуто/развёрнуто. (#11520)
* NVDA теперь автоматически определяет брайлевский дисплей NLS eReader Humanware при подключении по bluetooth, так как его bluetooth-именем теперь является "NLS eReader Humanware". (#11561)
* значительно улучшена производительность в редакторе кода Visual Studio Code. (#11533)

### Изменения для разработчиков

* Метод gui.guiHelper.BoxSizerHelper.addDialogDismissButtons теперь поддерживает новый именованный аргумент 'separated' для добавления в диалог стандартного горизонтального разделителя. Это не относится к диалогам сообщений для пользователя (MessageBox) и диалогам однократного пользовательского ввода. (#6468)
* Для модулей приложений добавлены новые свойства, такие как 'appPath' — содержащее путь к исполняемому файлу приложения, 'isWindowsStoreApp' — указывающее на то, что это приложение установлено из Windows Store и 'appArchitecture' — указывающее целевую архитектуру, под которую было собрано это приложение (например AMD64 или x86). (#7894)
* Теперь возможно создавать модули для приложений размещённых внутри wwahost.exe на Windows 8 и выше. (#4569)
* С помощью команды NVDA+Control+Shift+F1 теперь можно отделять новые записи журнала NVDA и копировать их в буфер обмена. (#9280)
* Удаление специфичных для NVDA Python-объектов, найденных циклическим сборщиком мусора, теперь отражается в журнале NVDA, помогая избавляться от появления циклических ссылок в коде NVDA. (#11499)
 * Отслеживаются экземпляры большинства классов NVDA, включая NVDAObject, AppModule, GlobalPlugin, SynthDriver и TreeInterceptor.
 * Отслеживаемые объекты должны быть экземплярами класса наследуемого от garbageHandler.TrackedObject.
* Более подробное отладочное журналирование MSAA-событий теперь может быть включено в категории "Дополнительно" диалога настроек NVDA. (#11521)
* События MSAA текущего объекта в фокусе больше не отфильтровываются вместе с прочими событиями, если превышено число событий для данного потока. (#11520)

## 2020.2

Основные новшества этого выпуска включают в себя поддержку нового брайлевского дисплея от компании Nattiq Technologies, улучшенную поддержку Windows Terminal и графического интерфейса антивирусных решений компании ESET, увеличенную производительность в менеджере паролей 1Password и в речевом синтезаторе Windows OneCore, а также множество других важных исправлений и улучшений.

### Новое

* Добавлена поддержка новых брайлевских дисплеев:
  * Nattiq nBraille (#10778)
* В диалоге "Жесты ввода" добавлена команда для открытия папки пользовательских настроек NVDA. Желаемое сочетание клавиш на эту команду пользователь должен назначить самостоятельно. (#2214)
* Улучшена поддержка графического интерфейса антивирусов ESET. (#10894)
* Добавлена поддержка эмулятора терминала Windows Terminal. (#10305)
* В диалоге "Жесты ввода" добавлена команда для получения имени активного профиля конфигурации NVDA. Желаемое сочетание клавиш на эту команду пользователь должен назначить самостоятельно. (#9325)
* В диалоге "Жесты ввода" добавлена команда для включения и выключения чтения надстрочного и подстрочного форматирования текста. Желаемое сочетание клавиш на эту команду пользователь должен назначить самостоятельно. (#10985)
* В некоторых web-приложениях (например в Gmail), NVDA теперь может не сообщать устаревшую информацию при быстром перемещении системного фокуса. (#10885)
  * Это экспериментальная возможность должна быть активирована вручную в комбинированном списке "Пытаться отменять речевой вывод для устаревших событий фокуса", который может быть найден в категории "Дополнительно" диалога настроек NVDA.
* В таблицу символов NVDA добавлено множество новых символов. Преимущественно это различные надстрочные и подстрочные знаки. (#11105)

### Изменения

* Liblouis braille translator обновлён до версии [3.14.0](https://github.com/liblouis/liblouis/releases/tag/v3.14.0). (#10832, #11221)
* Чтение надстрочного и подстрочного форматирования текста теперь управляется отдельным флажком в категории настроек "Форматирование документа" и не зависит от настройки чтения атрибутов шрифта. (#10919)
* Из-за изменений произошедших в редакторе кода VS Code, NVDA больше не отключает в нём по умолчанию режим обзора. (#10888)
* NVDA больше не читает сообщения "верхний" и "нижний" при использовании команд перемещения просмотрового курсора к первой и последней строке текущего объекта навигатора. (#9551)
* NVDA больше не читает сообщения "левый" и "правый" при использовании команд перемещения просмотрового курсора к первому и последнему символу текущей строки объекта навигатора. (#9551)

### Исправления

* NVDA теперь корректно запускается даже при невозможности создания файла журнала. (#6330)
* В последних выпусках Microsoft Word 365, NVDA больше не сообщает фразу "DeleteBackWord" при нажатии в документе комбинации клавиш Control+Backspace. (#10851)
* NVDA в проигрывателе Winamp теперь снова корректно сообщает переключение режимов повтора и случайного воспроизведения. (#10945)
* NVDA больше не тормозит при навигации в списках менеджера паролей 1Password. (#10508)
* Синтезатор речи Windows OneCore больше не делает задержек между отдельными читаемыми фразами. (#10721)
* NVDA больше не зависает при открытии контекстного меню 1Password из системной области уведомлений. (#11017)
* Начиная с версии Microsoft Office 2013:
  * Имена лент теперь сообщаются при первом попадании на них фокуса. (#4207)
  * Элементы контекстного меню теперь снова сообщаются корректно. (#9252)
  * Перемещение между разделами ленты с помощью комбинаций Control+стрелки влево/вправо теперь сообщается более единообразно. (#7067)
* В Mozilla Firefox и Google Chrome, текст в режиме обзора больше не размещается на отдельных строках при использовании CSS-свойства display: inline-flex. (#11075)
* При отключённой в режиме обзора автоматической установки системного фокуса на фокусируемые элементы, теперь стало возможно активировать нефокусируемые элементы.
* При отключённой в режиме обзора автоматической установки системного фокуса на фокусируемые элементы, теперь возможно активировать элементы добравшись до них клавишей Tab. (#8528)
* При отключённой в режиме обзора автоматической установки системного фокуса на фокусируемые элементы, активация некоторых элементов больше не приводит к клику мыши в неправильном месте. (#9886)
* Звук ошибок NVDA больше не слышан при обращении к текстовым элементам управления в DevExpress. (#10918)
* Во избежание дублирования сообщений, всплывающие подсказки для значков системной области уведомлений больше не читаются если их текст совпадает с именем самого значка. (#6656)
* При отключённой в режиме обзора автоматической установки системного фокуса на фокусируемые элементы, переключение к режиму редактирования по NVDA+пробел теперь устанавливает системный фокус на элемент под курсором режима обзора. (#11206)
* Проверка обновлений NVDA теперь снова работает на свежеустановленных системах. (#11253)
* Системный фокус в Java-приложениях более не изменяется, когда меняется выделение в несфокусированным дереве, таблице или списке. (#5989)

### Изменения для разработчиков

* Функции execElevated и hasUiAccess перемещены из модуля config в модуль systemUtils. Их использование через модуль config объявлено устаревшим. (#10493)
* Пакет configobj обновлён до версии 5.1.0dev (коммит f9a265c4). (#10939)
* Теперь возможно автоматизированное тестирование NVDA с Chrome и HTML-примерами. (#10553)
* Модуль IAccessibleHandler был преобразован в пакет, а OrderedWinEventLimiter выделен в отдельный модуль с добавлением unit тестов. (#10934)
* BrlApi обновлён до версии 0.8 (BRLTTY 6.1). (#11065)
* Модули для приложений теперь могут переопределять способ извлечения строки состояния в своём приложении. (#2125, #4640)
* NVDA более не прослушивает события IAccessible EVENT_OBJECT_REORDER. (#11076)
* Сломанные экземпляры ScriptableObject (например глобальные плагины в конструкторе которых забыт вызов конструктора суперкласса), больше не ломают обработку скриптов NVDA. (#5446)

## 2020.1

Основные новшества этого выпуска включают в себя поддержку ряда новых брайлевских дисплеев от HumanWare и APH, а также множество других важных исправлений, таких как возможность снова читать математическое содержимое в Microsoft Word с помощью MathPlayer/MathType.

### Новое

* В режиме обзора, выделенный элемент списка в Google Chrome теперь снова сообщается таким же образом, как это было в NVDA 2019.1. (#10713)
* На устройствах с сенсорным экраном, однократное касание экрана с удержанием, теперь выполняет щелчок правой кнопкой мыши в позиции касания. (#3886)
* Добавлена поддержка новых брайлевских дисплеев: APH Chameleon 20, APH Mantis Q40, HumanWare BrailleOne, BrailleNote Touch v2 и NLS eReader. (#10830)

### Изменения

* NVDA в режиме непрерывного чтения теперь предотвращает переход системы в спящий режим. (#10643)
* Для Mozilla Firefox добавлена поддержка встроенных фреймов (элементов iframe), обработка которых вынесена в отдельный процесс. (#10707)
* Библиотека брайлевской трансляции Liblouis обновлена до версии 3.12. (#10161)

### Исправления

* В таблицу символов NVDA добавлен знак минуса (U+2212) (в таблице русской локали он присутствовал и раньше). (#10633)
* При установке дополнений из окна менеджера дополнений, имена файлов и папок в диалоге выбора файла дополнения больше не читаются по два раза. (#10620, #2395)
* В Firefox, при загрузке соцсети Mastodon с включённом расширенном web-интерфейсом, все таймлайны в режиме обзора теперь отображаются корректно. (#10776)
* В режиме обзора, NVDA теперь корректно читает состояние "не отмечено" для не отмеченных флажков, состояние для которых не было задано ранее. (#10781)
* Для ARIA-переключателей, NVDA больше не сообщает непонятное описание состояний, такое как "не нажато отмечено" или "нажато отмечено". (#9187)
* Голоса SAPI4 больше не должны отказываться произносить текст в некоторых ситуациях. (#10792)
* NVDA теперь снова может читать и взаимодействовать с математическими выражениями в Microsoft Word. (#10803)
* NVDA теперь снова сообщает снятие выделения текста в режиме обзора, при нажатии клавиш-стрелок и наличии выделенного текста. (#10731)
* NVDA больше не выполняет аварийное завершение работы при ошибки инициализации синтезатора eSpeak NG. (#10607)
* Неверное определение горячей клавиши для запуска NVDA в той или иной локали, больше не вызывает крах установщика. Будет использовано сочетание клавиш по умолчанию (CTRL+ALT+N). (#5166, #6326)
* В режиме непрерывного чтения, и при включённой функции беглого чтения, использование клавиш быстрой навигации в режиме обзора больше не вызывает чтение сообщений о выходе из списков и таблиц. (#10706)
* Для некоторых MSHTML-элементов в Internet Explorer, исправлена функция отслеживания мыши. (#10736)

### Изменения для разработчиков

* Документация для разработчиков теперь создаётся с помощью Sphinx. (#9840)
* Ряд функций пакета speech были разделены на две. (#10593)
  Версии функций speakX сохранены, но теперь зависят от функций getXSpeech, которые возвращают речевую последовательность.
  * speakObjectProperties теперь полагается на getObjectPropertiesSpeech
  * speakObject теперь полагается на getObjectSpeech
  * speakTextInfo теперь полагается на getTextInfoSpeech
  * Функция speakWithoutPauses была перенесена в класс и переписана, но без нарушения обратной совместимости.
  * Функция getSpeechForSpelling объявлена устаревшей, но оставлена для обратной совместимости. Вместо неё используйте функцию getSpellingSpeech.
  Внутренние/приватные изменения, которые не должны влиять на разработчиков дополнений:
  * Функция _speakPlaceholderIfEmpty переименована в _getPlaceholderSpeechIfTextEmpty
  * Функция _speakTextInfo_addMath переименована в _extendSpeechSequence_addMathForTextInfo
* Значения 'reason' из пакета speech теперь являются экземплярами перечисления, см. класс controlTypes.OutputReason. (#10703)
  * Константы controlTypes.REASON_* объявлены устаревшими.
* Для сборки зависимостей NVDA теперь требуется Visual Studio 2019 (16.2 или новее). (#10169)
* SCons обновлён до версии 3.1.1. (#10169)
* Экземплярам NVDAObjects.behaviors._FakeTableCell снова разрешено не иметь расположения. (#10864)

## 2019.3

NVDA 2019.3 — это очень значительный релиз, содержащий множество внутренних изменений, включающих в том числе переход с Python 2 на Python 3 и серьёзное переписывание речевой подсистемы.
Несмотря на то, что эти изменения нарушают совместимость со старыми дополнениями NVDA, обновление на Python 3 необходимо для повышения безопасности, а переработка речевой подсистемы позволяет в ближайшем будущем реализовать некоторые интересные нововведения.
 Среди других новшеств этого выпуска можно выделить поддержку 64-х разрядных виртуальных машин Java, функциональность затемнения экрана и подсветки фокуса, поддержку большего числа брайлевских дисплеев и нового средства визуального просмотра брайлевского вывода, а также исправление большого числа других ошибок.

### Новое

* В текстовых полях Java-приложений улучшена точность установки указателя мыши при использовании команды приведения мыши к объекту навигатора. (#10157)
* Добавлена поддержка следующих брайлевских дисплеев Handy Tech (#8955):
 * Basic Braille Plus 40
 * Basic Braille Plus 32
 * Connect Braille
* Все ранее настроенные в диалоге "Жесты ввода" пользовательские жесты теперь могут быть удалены с помощью новой кнопки "Сбросить к заводским настройкам". (#10293)
* Чтение шрифта в Microsoft Word теперь включает в себя информацию о том, является ли текст скрытым. (#8713)
* Добавлена команда для перемещения просмотрового курсора к позиции ранее установленной как начало выделяемого или копируемого фрагмента текста: NVDA+Shift+F9. (#1969)
* В Internet Explorer, Microsoft Edge и последних версиях Firefox и Chrome, ориентиры теперь сообщаются как в режиме редактирования, так и при использовании объектной навигации. (#10101)
* В Internet Explorer, Google Chrome и Mozilla Firefox, теперь возможно перемещаться по статьям и группам с помощью комманд быстрой навигации. Клавиши на соответствующие команды могут быть назначены в диалоге жестов ввода, при открытии его из документа с активным режимом обзора. (#9485, #9227)
 * Также теперь поддерживаются объекты-иллюстрации (элементы figure). Они считаются встроенными объектами и перемещение между ними выполняется клавишами O и Shift+O.
* В Internet Explorer, Google Chrome и Mozilla Firefox, элементы-статьи теперь сообщаются при использовании объектной навигации и опционально в режиме обзора, если в настройках форматирования документа установлен соответствующий флажок. (#10424)
* Добавлена функция затемнения экрана, которая будучи активированной на системах начиная с Windows 8, позволяет сделать экран компьютера полностью чёрным. (#7857)
 * Для быстрой активации этого режима в диалог "Жесты ввода" добавлена соответствующая команда, однократный вызов которой включает временное затемнение экрана до следующей перезагрузки NVDA, а двойной — активирует этот режим на постоянной основе. По умолчанию на эту команду нет назначенной комбинации клавиш.
 * Затемнение экрана также может быть включено и настроено в категории "Зрение" диалога настроек NVDA.
* В NVDA добавлена возможность подсветки отдельных элементов экрана. (#971, #9064)
 * Подсветку системного фокуса, объекта навигатора и курсора режима обзора можно настроить в категории "Зрение" диалога настроек NVDA.
 * Обратите внимание, что эта функция несовместима с дополнением Focus Highlight, но его использование всё равно возможно при отключении встроенной подсветки.
* Добавлен новый инструмент "Просмотрщик брайля", позволяющий просматривать брайлевский вывод в отдельном окне на экране. (#7788)

### Изменения

* Руководство пользователя теперь описывает использование NVDA с Windows Console. (#9957)
* Запуск nvda.exe теперь по умолчанию перезагружает уже запущенную копию NVDA. Аргументы командной строки "-r" и "--replace" всё ещё могут быть переданы, но будут проигнорированы. (#8320)
* В Windows 8 и более поздних версиях, NVDA теперь будет сообщать информацию о имени и версии опубликованных приложений (например загруженных из магазина Microsoft), используя данные предоставленные самим приложением. (#4259, #10108)
* При переключении функции отслеживания исправлений в Microsoft Word по горячим клавишам, NVDA теперь сообщает новое состояние этой настройки. (#942)
* Номер версии NVDA теперь регистрируется в журнале первой записью. Это происходит даже если ведение журнала было отключено в диалоге настроек NVDA. (#9803)
* Диалог настроек NVDA больше не позволяет изменять уровень ведения журнала если он был переопределён в командной строке. (#10209)
* NVDA в Microsoft Word теперь сообщает статус отображения непечатаемых символов при его переключении по комбинации Control+Shift+8. (#10241)
* Liblouis braille translator обновлён до коммита 58d67e63. (#10094)
* Если в настройках речи включено использование базы данных консорциума Unicode, то символы из этой базы (преимущественно эмодзи) теперь будут читаться на всех уровнях пунктуации NVDA. (#8826)
* Сторонние Python пакеты включённые в NVDA (например такие как comtypes), теперь записывают свои предупреждения и ошибки в журнал NVDA. (#10393)
* Общий репозиторий языковых данных консорциума Unicode (CLDR), используемый в NVDA для чтения символов эмодзи, обновлён до версии 36.0. (#10426)
* При фокусировке на группу в режиме обзора, NVDA теперь сообщает описание этой группы. (#10095)
* Для получения доступа к Java-приложениям из коробки (в том числе использующим 64-х разрядные виртуальные машины), NVDA теперь включает в свой состав компонент Java Access Bridge. (#7724)
* Если Java Access Bridge отключён для текущего пользователя, то NVDA теперь будет автоматически включать его при своём запуске. (#7952)
* Синтезатор eSpeak-NG обновлён до версии 1.51-dev (коммит ca65812ac6019926f2fbd7f12c92d7edd3701e0c). (#10581)

### Исправления

* Эмодзи и другие 32-х разрядные символы Unicode, при их отображение в шестнадцатиричном формате теперь занимают меньше места на брайлевском дисплее. (#6695)
* В UWP-приложениях Windows 10, NVDA теперь сообщает всплывающие подсказки, если их чтение включено в категории "Представление объекта" диалога настроек NVDA. (#8118)
* На Windows 10 Anniversary Update и более поздних версиях, NVDA теперь сообщает вводимый текст в Mintty. (#1348)
* На Windows 10 Anniversary Update и более поздних версиях, вывод в консольных окнах рядом с кареткой больше не приводит к посимвольному чтению этого вывода. (#513)
* Элементы управления в диалоге компрессии звукового редактора Audacity теперь корректно сообщаются при навигации по этому диалогу. (#10103)
* В текстовых редакторах на основе Scintilla (таких как Notepad++), NVDA больше не рассматривает пробелы как отдельные слова при просмотре их в режиме объекта. (#8295)
* NVDA теперь предотвращает переход системы в режим сна при прокрутке текста на брайлевском дисплее. (#9175)
* На Windows 10, брайлевский дисплей теперь корректно отображает редактируемое содержимое ячеек в Microsoft Excel, и другие текстовые элементы управления UIA. (#9749)
* NVDA теперь снова сообщает предложения по вводу в адресной строке Microsoft Edge. (#7554)
* NVDA больше не замолкает при фокусировке на заголовке HTML-таблицы в Internet Explorer. (#8898)
* В Microsoft Edge, основанном на движке EdgeHTML, NVDA больше не воспроизводит звук предложений по вводу при разворачивании окна браузера. (#9110, #10002)
* В WEB-браузерах Mozilla Firefox и Google Chrome, NVDA теперь поддерживает комбинированные списки из стандарта ARIA 1.1. (#9616)
* NVDA больше не сообщает содержимое визуально скрытых колонок в элементах управления SysListView32. (#8268)
* При работе на защищённых экранах, NVDA в своём диалоге настроек больше не отображает значение "info" как текущий уровень ведения журнала NVDA. (#10209)
* В меню "Пуск" Windows 10 Anniversary Update и более поздних версий, NVDA теперь сообщает более подробную информацию о результатах поиска. (#10340)
* Перемещение курсора в режиме обзора, приводящее к изменениям в документе, больше не вызывает в некоторых случаях некорректное чтение содержимого этого документа. (#8831, #10343)
* В Microsoft Word были исправлены названия некоторых маркеров. (#10399)
* В Windows 10 May 2019 Update и более поздних версиях, NVDA теперь снова сообщает первый выбранный эмодзи или элемент буфера обмена при открытии панели эмодзи или истории буфера обмена соответственно. (#9204)
* В Poedit теперь снова возможно просматривать некоторые переводы для языков с написанием справа налево. (#9931)
* В приложении "Параметры" на Windows 10 April 2018 Update и более поздних версиях, NVDA больше не будет сообщать прогресс индикатора выполнения для ползунка настройки громкости на странице "Система/Звук". (#10412)
* Некорректные регулярные выражения в речевых словарях NVDA больше не приводят к полной остановки речевого вывода. (#10334)
* При чтении маркированного списка в Microsoft Word с включённой поддержкой UIA, NVDA больше не сообщает маркер следующего элемента при чтении текущего. (#9613)
* Решены некоторые редкие проблемы и ошибки с брайлевской трансляцией в Liblouis. (#9982)
* Java-приложения запущенные перед NVDA, теперь доступны без необходимости их перезапуска. (#10296)
* Когда в Mozilla Firefox элемент в фокусе помечается как текущий (с помощью атрибута aria-current), то NVDA больше не сообщает это изменение несколько раз подряд. (#8960)
* NVDA при перемещении по тексту теперь будет рассматривать составные символы Unicode (такие как e с акутом) как один единый символ. (#10550)
* NVDA теперь поддерживает Spring Tool Suite версии 4. (#10001)
* NVDA больше не читает дважды имя объекта, если его атрибут aria-labelledby ссылается на внутренний элемент. (#10552)
* В Windows 10 1607 и более поздних версиях, набор символов с клавиатуры брайлевского дисплея теперь читается в большем числе ситуаций. (#10569)
* При смене устройства вывода звука, тоновые сигналы NVDA теперь будут проигрываться через новое выбранное устройство. (#2167)
* В Mozilla Firefox, перемещение системного фокуса в режиме обзора теперь является более быстрым, что делает управление курсором режима обзора во многих случаях более отзывчивым. (#10584)

### Изменения для разработчиков

* Python обновлён до версии 3.7. (#7105)
* pySerial обновлён до версии 3.4. (#8815)
* Для поддержки Python 3.5 и выше, wxPython обновлён до версии 4.0.3. (#9630)
* Модуль six обновлён до версии 1.12.0. (#9630)
* py2exe обновлён до версии 0.9.3.2 (коммит b372a8e from albertosottile/py2exe#13). (#9856)
* UIAutomationCore.dll обновлён до версии 10.0.18362. (#9829)
* Список автодополнения по клавише tab в Python консоли NVDA, теперь предлагает атрибуты начинающиеся с символа подчёркивания только в том случае, если этот символ был набран первым. (#9918)
* Flake8 linting tool has been integrated with SCons reflecting code requirements for Pull Requests. (#5918)
* NVDA больше не зависит от pyWin32, а такие модули как win32api и win32con больше недоступны для дополнений. (#9639)
 * Вызовы win32api могут быть заменены прямыми вызовами функций dll win32 через ctypes.
 * Константы win32con должны быть определены в вашем коде.
* Параметр "async" в функции nvwave.playWaveFile был переименован в "asynchronous". (#8607)
* Экземпляры класса synthDriverHandler.SynthDriver больше не поддерживают методы speakText и speakCharacter.
 * За их функционал теперь отвечает метод speak.
* Из модуля synthDriverHandler были удалены классы SynthSetting. Вместо них теперь следует использовать классы driverHandler.DriverSetting.
* Подклассы synthDriverHandler.SynthDriver больше не должны предоставлять индексы читаемых фрагментов текста через свойство lastIndex.
 * Вместо этого они теперь должны уведомлять объект synthDriverHandler.synthIndexReached соответствующим индексом, когда проигрывание всех звуковых данных до этого индекса будет завершено.
* Подклассы synthDriverHandler.SynthDriver теперь должны уведомлять объект synthDriverHandler.synthDoneSpeaking каждый раз, когда проигрывание всех звуковых данных созданных в результате вызова метода SynthDriver.speak будет завершено.
* Подклассы synthDriverHandler.SynthDriver в своём методе speak должны соответствующим образом обрабатывать экземпляры speech.PitchCommand, так как изменение высоты голоса при посимвольном чтении теперь зависит от этой поддержки.
* Функция speech.getSpeechTextForProperties была переименована в speech.getPropertiesSpeech. (#10098)
* Функция braille.getBrailleTextForProperties была переименована в braille.getPropertiesBraille. (#10469)
* Следующие функции модуля speech теперь возвращают речевую последовательность. (#10098)
 * getControlFieldSpeech
 * getFormatFieldSpeech
 * getSpeechTextForProperties переименованная в getPropertiesSpeech
 * getIndentationSpeech
 * getTableInfoSpeech
* Добавлен модуль textUtils, упрощающий работу со строками Python 3 и unicode-строками Windows. (#9545)
 * Для получения примеров использования, обратитесь к документации этого модуля и к модулю textInfos.offsets.
* Проведена чистка кодовой базы. (#9548)
 * Удалены модули для следующих приложений:
  * Звукозапись для Windows XP.
  * Klango Player (этот проект заброшен).
 * Удалена обёртка configobj.validate.
  * Новый код должен использовать from configobj import validate вместо import validate
 * textInfos.Point и textInfos.Rect заменены на locationHelper.Point и locationHelper.RectLTRB соответственно.
 * braille.BrailleHandler._get_tether и braille.BrailleHandler.set_tether были удалены.
 * Функция config.getConfigDirs была удалена.
 * Функция config.ConfigManager.getConfigValidationParameter была заменена функцией getConfigValidation.
 * Свойство inputCore.InputGesture.logIdentifier было удалено.
   * Используйте вместо этого функцию _get_identifiers из класса inputCore.InputGesture.
 * Методы synthDriverHandler.SynthDriver.speakText/speakCharacter были удалены.
 * Удалены ряд классов synthDriverHandler.SynthSetting.
   * Сохраняемые ранее для обратной совместимости, но теперь признанные полностью устаревшими. (#8214)
   * Драйверы использующие классы SynthSetting должны быть обновлены для использования классов DriverSetting.
 * Удалён некоторый устаревший код, а именно:
  * Поддержка списка сообщений в Outlook 2003.
  * Перекрывающий класс для классического меню "Пуск", доступного только в Windows Vista и более ранних версиях.
  * Поддержка для Skype 7, так как он больше не работает.
* Реализован фреймворк для создания поставщиков средств зрительной коррекции (vision enhancement providers); модулей, которые могут изменять содержимое экрана, при необходимости основываясь на данных о расположении объектов полученных от NVDA. (#9064)
 * Дополнения NVDA могут иметь таких поставщиков в каталоге visionEnhancementProviders.
 * Для получения информации о подробностях реализации фреймворка и примеров некоторых средств зрительной коррекции, обратитесь к модулям vision и visionEnhancementProviders соответственно.
 * Доступные поставщики зрительной коррекции могут быть активированы и настроены в категории "Зрение" диалога настроек NVDA.
* Абстрактные свойства класса теперь поддерживаются для объектов наследуемых от baseObject.AutoPropertyObject (например NVDAObjects и TextInfos). (#10102)
* Добавлена константа displayModel.UNIT_DISPLAYCHUNK определяющая фрагмент текста для экземпляров DisplayModelTextInfo. (#10165)
 * Эта новая константа позволяет обходить текст в DisplayModelTextInfo способом, схожим с тем, как в базовой модели сохраняются части текста.
* Функция displayModel.getCaretRect теперь возвращает экземпляр locationHelper.RectLTRB. (#10233)
* Константы UNIT_CONTROLFIELD и UNIT_FORMATFIELD были перемещены из класса virtualBuffers.VirtualBufferTextInfo в пакет textInfos. (#10396)
* Каждая запись журнала NVDA теперь содержит информацию о сделавшим её потоке. (#10259)
* Экземпляры TextInfo для UIA-объектов теперь могут расширяться на такие единицы текста как UNIT_PAGE, UNIT_STORY и UNIT_FORMATFIELD. (#10396)
* Внешние модули (глобальные плагины и модули приложений) теперь с меньшей вероятностью могут помешать созданию экземпляров NVDAObjects.
 * Исключения происходящие в методах "chooseNVDAObjectOverlayClasses" и "event_NVDAObject_init" теперь корректно обрабатываются и логируются.
* Словарь aria.htmlNodeNameToAriaLandmarkRoles был переименован в aria.htmlNodeNameToAriaRoles. Теперь он также содержит роли не являющиеся ориентирами.
* Функция scriptHandler.isCurrentScript была удалена по причине неиспользования. (#8677)

## 2019.2.1

В этом выпуске NVDA исправлены некоторые ошибки найденные в версии 2019.2:

* В Gmail исправлены сбои, наблюдаемые в Firefox и Chrome при взаимодействии со всплывающими меню, отображаемыми при создании фильтров или изменении некоторых настроек Gmail. (#10175, #9402, #8924)
* NVDA на Windows 7 больше не вызывает аварийное завершение работы Проводника при использовании мыши в меню "Пуск". (#9435)
* NVDA на Windows 7 больше не вызывает аварийное завершение работы Проводника при обращении в его окне к полям метаданных. (#5337)
* NVDA в Mozilla Firefox и Google Chrome больше не зависает при взаимодействии с изображениями, URI которых содержит данные закодированные в base64. (#10227)

## 2019.2

Основные новшества этого выпуска включают в себя поддержку автоматического определения подключения для брайлевских дисплеев Freedom Scientific, возможность отключения следования системного фокуса за курсором виртуального буфера режима обзора (что может повысить отзывчивость), реализацию опции дополнительного ускорения речи для синтезатора Windows OneCore и исправление множества других ошибок.

### Новое

* Встроенная в NVDA поддержка Miranda NG теперь актуальна и для самых последних версий этого IM-клиента. (#9053)
* Теперь возможно отключить автоматическую активацию режима обзора на web-страницах, сняв в настройках режима обзора новый флажок "Активировать режим обзора при загрузке страницы". (#8716)
 * Обратите внимание, что даже если эта опция отключена, вы всё равно можете вручную включать режим обзора по NVDA+пробел.
* В диалоге настроек пунктуации/символов теперь доступно поле для фильтрации искомых символов по имени, также как это уже реализовано в диалоге жестов ввода и списке элементов режима обзора. (#5761)
* В диалог "Жесты ввода" добавлена новая команда для изменения размера единицы читаемого текста при перемещении указателя мыши. По умолчанию на эту команду нет назначенного жеста. (#9056)
* В настройках синтезатора Windows OneCore теперь доступна опция дополнитеьного ускорения речи. (#7498)
* Опция дополнительного ускорения для синтезаторов речи теперь может быть доступна из кольца настроек синтезатора. На текущий момент эту функцию поддерживают eSpeak-NG и Windows OneCore. (#8934)
* Профили конфигурации NVDA теперь могут вручную активироваться и деактивироваться назначаемыми пользователем жестами. (#4209)
 * Соответствующие жесты должны быть назначены в категории "Профили конфигурации" диалога "Жесты ввода".
* Для редактора кода Eclipse реализована поддержка функции автодополнения. (#5667)
 * Помимо этого, по NVDA+D теперь возможно читать текст Javadoc, если он доступен.
* В категорию дополнительных настроек добавлен флажок "Автоматически устанавливать системный фокус на фокусируемые элементы" (NVDA+8), позволяющий отключить перемещение системного фокуса вслед за курсором виртуального буфера режима обзора. (#2039) Это отключение не требуется для большинства web-страниц, но оно может помочь решить следующие проблемы:
 * Отмена в некоторых ситуациях нажатия клавиши быстрой навигации и переход к предыдущему элементу в документе.
 * Удерживание на себе системного фокуса полями редактирования на некоторых сайтах.
 * Низкий отклик клавиш быстрой навигации в режиме обзора.
* Поддерживаемые параметры драйверов брайлевских дисплеев теперь могут настраиваться в категории "Брайль" диалога настроек NVDA. (#7452)
* NVDA теперь поддерживает автоматическое определение подключения брайлевских дисплеев Freedom Scientific. (#7727)
* В категорию "Просмотр текста" диалога "Жесты ввода" добавлена новая команда показывающая заменяющий текст для символа под просмотровым курсором. (#9286)
* В категорию дополнительных настроек NVDA добавлена экспериментальная опция, позволяющая протестировать обновлённую поддержку Windows Console, использующую Microsoft UI Automation API. (#9614)
* Python консоль NVDA теперь поддерживает вставку нескольких строк из буфера обмена. (#9776)

### Изменения

* Громкость речи в кольце настроек синтезатора теперь регулируется с шагом в 5, а не в 10 процентов. (#6754)
* В окно менеджера дополнений добавлен поясняющий текст, если NVDA запущена с флагом --disable-addons. (#9473)
* Общий репозиторий языковых данных консорциума Unicode (CLDR) используемый в NVDA для чтения символов эмодзи, обновлён до версии 35.0. (#9445)
* Клавиша-ускоритель для поля фильтра в диалоге списка элементов режима обзора была изменена на alt+y (в русском интерфейсе осталась alt+т). (#8728)
* Если автоматически определённый брайлевский дисплей подключён по Bluetooth, то NVDA теперь будет продолжать поиск USB-дисплеев поддерживаемых темже драйвером и автоматически переключится на USB-подключение когда оно станет доступно. (#8853)
* Синтезатор eSpeak-NG обновлён до коммита 67324cc.
* Liblouis braille translator обновлён до версии 3.10.0. (#9439, #9678)
* NVDA теперь читает слово "выделено" после выделенного пользователем текста. (#9028, #9909)
* Режим обзора в Microsoft Visual Studio Code по умолчанию теперь отключён. (#9828)

### Исправления

* NVDA теперь запускается корректно даже если каталог какого либо дополнения оказался пустым. (#7686)
* Метки LTR и RTL больше не попадают в брайлевский или посимвольный речевой вывод в окне свойств файла/папки. (#8361)
* При перемещении по полям форм с помощью клавиш быстрой навигации режима обзора, NVDA теперь сообщает весь текст выбранного поля, а не только его первую строку. (#9388)
* В NVDA больше не пропадает речевой вывод после закрытия приложения "Почта" на Windows 10. (#9341)
* NVDA теперь корректно запускается, даже если в региональных настройках пользователя указана локаль неизвестная NVDA. Например Английский (Нидерланды). (#8726)
* Переключение между режимами обзора и редактирования в Microsoft Excel теперь сообщается корректно. (#8846)
* В Notepad++ и других редакторах основанных на Scintilla, NVDA теперь корректно читает строку под указателем мыши. (#5450)
* В Документах Google (и в других web-редакторах), брайлевский дисплей ошибочно больше не отображает в некоторых ситуациях текст "кон лст" перед курсором в середине элемента списка. (#9477)
* В Windows 10 May 2019 Update, NVDA больше не сообщает большое количество уведомлений об изменении громкости, когда она изменяется аппаратными кнопками, а фокус находится в окне проводника. (#9466)
* Открытие диалога настроек пунктуации/символов теперь стало значительно быстрее, что особенно заметно если используемая таблица символов содержит более тысячи записей. (#8790)
* В текстовых редакторах основанных на Scintilla (например Notepad++), NVDA теперь корректно читает строки при включённой функции переноса слов. (#9424)
* В Microsoft Excel, после нажатия клавиш shift+enter или shift+numpadEnter, NVDA теперь объявляет координаты новой ячейки. (#9499)
* В Visual Studio 2017 и выше, в окне обозревателя объектов, выбранный элемент в дереве объектов или дереве членов с категориями теперь сообщается корректно. (#9311)
* Дополнения NVDA, имена которых отличаются только регистром символов, больше не рассматриваются как различные. (#9334)
* Задаваемая в NVDA скорость речи для синтезатора Windows OneCore больше не зависит от установленной скорости в настройках речи Windows 10. (#7498)
* Журнал NVDA теперь может быть открыт по NVDA+F1, даже если текущий объект навигатора не предоставляет информацию для разработчиков. (#8613)
* Теперь снова стало возможно использовать команды NVDA для навигации по таблицам в Документах Google через Firefox и Chrome. (#9494)
* Клавиши для прокрутки текста на брайлевских дисплеях Freedom Scientific теперь работают корректно. (#8849)
* NVDA больше не подвисает до десяти секунд при чтении первого символа документа в 64-разрядной версии Notepad++ 7.7. (#9609)
* Приложение HTCom теперь может использоваться с брайлевскими дисплеями Handy Tech совместно с NVDA. (#9691)
* Обновления изменяющихся областей (live region) в Mozilla Firefox больше не сообщаются, если эти области находятся в неактивной вкладке. (#1318)
* Диалог поиска NVDA в режиме обзора больше не вызывает ошибку, если в фоне уже открыто окно "О NVDA". (#8566)

### Изменения для разработчиков

* В классах модулей для приложений теперь можно устанавливать свойство disableBrowseModeByDefault со значением True, чтобы по умолчанию отключить автоматическую активацию режима обзора. (#8846)
* Расширенный стиль окна для объектов Window и их производных теперь доступен через свойство `extendedWindowStyle`. (#9136)
* Пакет comtypes обновлён до версии 1.1.7. (#9440, #8522)
* При вызове команды чтения исполняемого файла и модуля текущего приложения (NVDA+Control+F1), имя загруженного модуля теперь сообщается первым. (#7338)
* Добавлен пример использования библиотеки nvdaControllerClient.dll из кода на C#. (#9600)
* В модуль winVersion добавлена новая функция isWin10, возвращающая True, если NVDA запущена как минимум на переданном ей номере версии Windows 10 (например 1903). (#9761)
* Python консоль NVDA теперь содержит больше полезных модулей в своем пространстве имён (таких как appModules, globalPlugins, config и textInfos). (#9789)
* Результат последней выполненной команды в Python консоли NVDA теперь доступен через переменную _ (подчёркивание). (#9782)
 * Обратите внимание, что эта переменная затеняет функцию перевода gettext, которая также называется "_". Для доступа к функции перевода выполните: del _

## 2019.1.1

В этом выпуске исправлены следующие ошибки:

* NVDA больше не вызывает аварийное завершение работы Excel 2007 и не прерывает речевой вывод если ячейка содержит формулу. (#9431)
* Google Chrome больше не завершает аварийно свою работу при взаимодействии с некоторыми списками. (#9364)
* Исправлена ошибка, из-за которой пользовательская конфигурация NVDA не копировалась в папку системных настроек. (#9448)
* В Microsoft Excel, NVDA теперь снова использует локализованные сообщения при чтении расположения объединённых ячеек. (#9471)

## 2019.1

Основные новшества этого выпуска включают в себя увеличение производительности при работе в Microsoft Word и Excel; улучшения стабильности и безопасности связанные с возможностью для разработчиков дополнений явно указывать совместимые версии NVDA; а также множество других исправлений и улучшений.

Обратите внимание, что начиная с этой версии NVDA, пользовательские модули приложений, глобальные плагины, драйверы брайлевских дисплеев и синтезаторов речи больше не будут автоматически загружаться из каталога пользовательской конфигурации.
Теперь для конечных пользователей они должны быть представлены в форме дополнений. Разработчики дополнений могут тестировать свой код разместив его в новом подкаталоге scratchpad каталога пользовательской конфигурации и установив флажок "Разрешить загрузку пользовательского кода из каталога Scratchpad" в новой категории "Дополнительно" диалога настроек программы.
Эти изменения необходимы для решения проблем совместимости пользовательского кода с будущими версиями NVDA.
Для получения более подробной информации об этом изменении и о том, как теперь улучшено версионирование дополнений, пожалуйста, обратитесь к списку изменений ниже.

### Новое

* Добавлены новые брайлевские таблицы: африкаанс, арабский восьмиточечный, арабский второй ступени и испанский второй ступени. (#4435, #9186)
* В категорию настроек мыши добавлен флажок, позволяющий включить обработку событий ввода мыши от сторонних приложений. (#8452)
 * Это позволит NVDA корректно отслеживать мышь во время сеанса работы TeamViewer и других программ удалённого администрирования.
* Добавлен новый аргумент командной строки `--enable-start-on-logon`, указывающий, следует ли при установке NVDA в тихом режиме включать работу программы на защищённом рабочем столе. Значение true включает эту возможность, а false отключает её. Если этот аргумент не указан, то по умолчанию запуск NVDA на защищённом рабочем столе будет включён, если это уже не было настроено при предыдущей установке. (#8574)
* Теперь возможно отключить ведение журнала NVDA, выбрав в соответствующем комбинированном списке категории "Общие" диалога настроек значение "отключено". (#8516)
* NVDA теперь сообщает наличие формул в таблицах LibreOffice и Apache OpenOffice. (#860)
* В режиме обзора в Mozilla Firefox и Google Chrome, NVDA теперь сообщает выделенные элементы списков и деревьев.
 * Это работает в Firefox начиная с версии 66.
 * Это не работает для некоторых списков (HTML-элементов select) в Chrome.
* Добавлена первоначальная поддержка таких приложений как Mozilla Firefox на компьютерах с процессорами ARM64 (например Qualcomm Snapdragon). (#9216)
* В диалог настроек NVDA добавлена новая категория "Дополнительно", в которой помимо прочего можно включить доступ к документам Microsoft Word через Microsoft UI Automation API. (#9200)
* Добавлена поддержка графического представления во встроенном средстве управления дисками Windows. (#1486)
* Добавлена поддержка брайлевских дисплеев Handy Tech Connect Braille и Basic Braille 84. (#9249)

### Изменения

* Liblouis braille translator обновлён до версии 3.8.0. (#9013)
* Разработчики дополнений теперь могут указывать минимальную версию NVDA, требуемую для корректной работы дополнения. NVDA заблокирует установку или загрузку тех дополнений, минимальная требуемая версия NVDA которых окажется выше используемой версии NVDA. (#6275)
* Разработчики дополнений теперь могут указывать последнюю версию NVDA с которой была проверена работа дополнения. NVDA заблокирует установку или загрузку тех дополнений, последняя проверенная версия NVDA которых окажется ниже используемой версии NVDA. (#6275)
* Эта версия NVDA разрешает установку и работу дополнений не указывающих минимальную требуемую и последнюю проверенную версию NVDA, но будущие выпуски NVDA (например 2019.2) могут автоматически отключить такие дополнения.
* Команда перемещения указателя мыши к объекту навигатора теперь доступна для Microsoft Word, так же как и для элементов управления UIA. В частности для элементов управления в Microsoft Edge. (#7916, #8371)
* Улучшено чтение текста под указателем мыши в Microsoft Edge и в других UIA-приложениях. (#8370)
* Если NVDA запускается с аргументом командной строки `--portable-path`, то указанный путь автоматически подставляется в соответствующие поле при попытке создания переносной копии через меню NVDA. (#8623)
* Обновлён путь к норвежской брайлевской таблице, отражающей стандарт 2015 года. (#9170)
* При навигации по абзацам (control+стрелки вверх и вниз) или по ячейкам таблиц (control+alt+стрелки), NVDA больше не будет сообщать о наличии орфографических ошибок, даже если это явно указано в настройках NVDA. Это связано с тем, что абзацы и ячейки таблиц могут быть довольно большими, и обнаружение орфографических ошибок в некоторых приложениях может быть весьма ресурсозатратно. (#9217)
* NVDA больше не загружает пользовательские модули приложений, глобальные плагины, драйверы брайлевских дисплеев и синтезаторов речи из каталога пользовательской конфигурации NVDA. Теперь этот код должен быть представлен в форме дополнений с явным указанием совместимых версий NVDA. (#9238)
 * Разработчики тестирующие свой код, должны в категории "Дополнительно" диалога настроек NVDA установить флажок "Разрешить загрузку пользовательского кода из каталога Scratchpad" и разместить свой код в подкаталоге 'scratchpad' каталога пользовательской конфигурации NVDA.

### Исправления

* При использовании синтезатора речи Windows OneCore на системах начиная с Windows 10 April 2018, больше нет больших пауз между произносимыми фразами. (#8985)
* При перемещении по символам в текстовых элементах управления (например в Блокноте) или в режиме обзора, 32-разрядные символы эмодзи состоящие из двух кодовых точек UTF-16 (например 😀), теперь читаются корректно. (#8782)
* Улучшен диалог подтверждения перезагрузки после смены языка интерфейса NVDA. Текст диалога и метки кнопок стали короче и яснее. (#6416)
* Сбой при загрузке стороннего синтезатора речи на Windows 10 теперь приводит к переключению на синтезатор Windows OneCore, вместо eSpeak NG. (#9025)
* При работе на защищённом рабочем столе, из подменю Справка главного меню NVDA, убран пункт для вызова диалога "Добро Пожаловать". (#8520)
* При использовании клавиши tab или клавиш быстрой навигации в режиме обзора, надписи на панелях вкладок теперь сообщаются более последовательно. (#709)
* NVDA теперь сообщает изменения выбора времени для элементов управления используемых в приложении Будильники и часы на Windows 10. (#5231)
* В Центре Уведомлений Windows 10, NVDA теперь сообщает состояние кнопок-переключателей для быстрых действий, таких как Яркость экрана и Фокусировка внимания. (#8954)
* В Центре Уведомлений Windows 10 October 2018 Update и более ранних версиях, NVDA теперь определяет кнопку для быстрого действия изменения яркости экрана как кнопку, а не как кнопку-переключатель. (#8845)
* NVDA теперь снова отслеживает перемещение курсора и сообщает удаляемые символы в полях редактирования "Перейти к" и "Найти" для Microsoft Excel. (#9042)
* Исправлен трудновоспроизводимый сбой режима обзора в Mozilla Firefox. (#9152)
* NVDA теперь корректно сообщает объект в системном фокусе для некоторых элементов управления свёрнутой ленты Microsoft Office 2016.
* NVDA теперь корректно сообщает предлагаемый контакт при вводе адреса в новом сообщении Microsoft Outlook 2016. (#8502)
* Несколько последних клавиш маршрутизации на 80-ти клеточных дисплеях eurobraille больше не перемещают курсор в начало брайлевской строки. (#9160)
* Для списка сообщений Mozilla Thunderbird исправлена табличная навигация при настроенной сортировке писем по обсуждениям. (#8396)
* В Mozilla Firefox и Google Chrome, переключение в режим редактирования теперь работает корректно для списков и деревьев, если фокусируемыми являются их элементы, а не они сами. (#3573, #9157)
* Режим обзора теперь корректно активируется по умолчанию при чтении сообщений в Microsoft Outlook 2016/365, даже если NVDA использует экспериментальную поддержку UI Automation для документов Microsoft Word. (#9188)
* NVDA теперь менее склонна зависать таким образом, что единственным способом решения проблемы является выход из текущего сеанса Windows. (#6291)
* В Windows 10 October 2018 Update и более новых версиях, при открытии пустого журнала облачного буфера обмена, NVDA теперь сообщает его состояние. (#9103)
* В Windows 10 October 2018 Update и более новых версиях, NVDA теперь сообщает результаты поиска в панели ввода эмодзи. (#9105)
* NVDA больше не зависает в главном окне Oracle VirtualBox версии 5.2 и новее. (#9202)
* В некоторых документах Microsoft Word, значительно улучшена отзывчивость при навигации по строкам, абзацам и ячейкам таблиц. Напоминаем, что для ещё большей производительности, настройте в Microsoft Word режим черновика с помощью клавиш alt+о,ч после открытия документа. (#9217)
* В Mozilla Firefox и Google Chrome, NVDA больше не читает пустые оповещения. (#5657)
* Значительно улучшена производительность при навигации по ячейкам в Microsoft Excel, в частности в таблицах с примечаниями и выпадающими списками. (#7348)
* В настройках Microsoft Excel 2016/365 больше не нужно запрещать редактирование в ячейках, чтобы получать доступ к содержимому ячеек с помощью NVDA. (#8146)
* Исправлено зависание NVDA в Mozilla Firefox, иногда происходящее при быстром перемещении по ориентирам с установленным дополнением Enhanced Aria. (#8980)

### Изменения для разработчиков

* Сборка NVDA теперь может быть выполнена со всеми редакциями Microsoft Visual Studio 2017, а не только с Community Edition. (#8939)
* Теперь возможно включить вывод журнала liblouis в журнал NVDA. Для этого следует в секции debugLog конфигурации NVDA, установить параметр louis в значение True. (#4554)
* Разработчики дополнений теперь могут включать в файл манифеста параметры со значениями совместимых версий NVDA. (#6275, #9055)
 * minimumNVDAVersion: Минимальная версия NVDA необходимая для корректной работы дополнения.
 * lastTestedNVDAVersion: Последняя версия NVDA с которой была проверена корректная работа дополнения.
* Объекты OffsetsTextInfo теперь могут реализовывать метод _getBoundingRectFromOffset, позволяющий извлекать ограничивающие прямоугольники использующиеся вместо экранных точек для получения информации о расположении символов. (#8572)
* Для объектов TextInfo добавлено свойство boundingRect, предназначенное для извлечения ограничивающих прямоугольников для текстовых диапазонов. (#8371)
* Свойства и методы классов в NVDA теперь могут быть помечены как абстрактные. Создание экземпляров таких классов будет вызывать исключение. (#8294, #8652, #8658)
* NVDA теперь может журналировать время от момента пользовательского ввода, до начала произнесения текста синтезатором речи, что может помочь в оценке воспринимаемой отзывчивости. Для этого следует в секции debugLog конфигурации NVDA, установить параметр timeSinceInput в значение True. (#9167)

## 2018.4.1

В этом выпуске исправлен сбой при запуске NVDA, если языком интерфейса программы является арагонский. (#9089)

## 2018.4

Основные новшества этого выпуска включают в себя улучшение производительности в последних версиях Mozilla Firefox, поддержку чтения эмодзи всеми синтезаторами речи, чтение статусов отвечено/переслано для сообщений в Microsoft Outlook, возможность чтения расстояния от курсора до краёв страницы в Microsoft Word, а также исправление множества других ошибок.

### Новое

* Добавлены новые брайлевские таблицы: Китайский (Китай, Мандарин) первой и второй ступени. (#5553)
* В списке сообщений Microsoft Outlook, NVDA теперь сообщает такие статусы писем как "Отвечено" или "Переслано". (#6911)
* NVDA теперь может читать описание для эмодзи и множества других символов из базы языковых данных Консорциума Unicode. (#6523)
* В Microsoft Word, расстояние между курсором и левым и верхним краями страницы теперь можно узнать по нажатию NVDA+numpadDelete. (#1939)
* В Google Таблицах с включённым режимом брайля, NVDA больше не произносит на каждой ячейки фразу "выделено" при перемещении фокуса между ячейками. (#8879)
* Добавлена поддержка для приложений Foxit Reader и Foxit Phantom PDF. (#8944)
* Добавлена поддержка для менеджера баз данных DBeaver. (#8905)

### Изменения

* Для более точного определения всплывающих уведомлений появившихся в Windows 8, флажок "Читать всплывающие системные сообщения" в категории "Представление объекта" диалога настроек NVDA был переименован в "Читать системные уведомления". (#5789)
* В категории "Клавиатура" диалога настроек NVDA, флажки определяющие использование клавиш-модификаторов NVDA, теперь представлены в виде списка, а не как отдельные элементы управления.
* NVDA на некоторых версиях Windows больше не сообщает избыточную информацию при чтении часов из системной области уведомлений. (#4364)
* Liblouis braille translator обновлён до версии 3.7.0. (#8697)
* Синтезатор речи eSpeak-NG обновлён до коммита 919f3240cbb.

### Исправления

* Для сообщений в Outlook 2016/365, теперь читается категория и состояние установленных флажков. (#8603)
* NVDA при своём запуске больше не показывает сообщение о неподдерживаемости операционной системой выбранного языка, если языком NVDA является киргизский, монгольский или македонский. (#8064)
* В Mozilla Firefox, Google Chrome и Acrobat Reader DC, приведение указателя мыши к объекту навигатора теперь более точно перемещает мышь к позиции курсора режима обзора. (#6460)
* На web-страницах в Mozilla Firefox, Google Chrome и Internet Explorer, улучшено взаимодействие с комбинированными списками. (#8664)
* При запуске NVDA на русских версиях Windows XP или Vista, теперь корректно показывается уведомление о необходимости более новой версии Windows. (#8771)
* В Mozilla Firefox увеличена производительность при навигации по большим документам с множеством динамически изменяющихся элементов. (#8678)
* Брайлевский дисплей больше не отображает атрибуты шрифта если они были отключены в настройках форматирования документа. (#7615)
* В Проводнике и других приложениях использующих UI Automation, NVDA теперь корректно отслеживает системный фокус когда другое приложение занято (например при пакетной обработке в GoldWave). (#7345)
* Нажатие клавиши escape в ARIA-меню на web-страницах теперь передаётся самому меню и не вызывает переключение к режиму обзора. (#3215)
* В новом интерфейсе Gmail, использование клавиш быстрой навигации внутри читаемых сообщений, больше не вызывает чтение всего тела сообщения после элемента к которому вы переместились. (#8887)
* Web-браузеры, такие как Mozilla Firefox и Google Chrome, больше не должны аварийно завершать свою работу после обновления NVDA, а режим обзора должен продолжать корректно отображать все изменения в загруженных документах. (#7641)
* NVDA больше не читает фразу "по щелчку" несколько раз на одной строке, при переходе к интерактивным элементам в режиме обзора. (#7430)
* Жесты на брайлевских дисплеях Baum Vario 40 теперь выполняются без ошибок. (#8894)
* В Google Презентациях с Mozilla Firefox, NVDA больше не читает выделенный текст на каждом элементе управления в системном фокусе. (#8964)

### Изменения для разработчиков

* В модуль gui.nvdaControls добавлены два класса для создания доступных списков с элементами-флажками. (#7325)
 * CustomCheckListBox является доступным подклассом wx.CheckListBox.
 * AutoWidthColumnCheckListCtrl добавляет доступные флажки к AutoWidthColumnListCtrl, который сам наследуется от wx.ListCtrl.
* Если вам необходимо реализовать доступность для недоступного wx-виджета, то это можно сделать с помощью экземпляра gui.accPropServer.IAccPropServer_impl. (#7491)
 * Для получения дополнительной информации, обратитесь к реализации gui.nvdaControls.ListCtrlAccPropServer.
* Модуль configobj обновлён до версии 5.1.0dev (коммит 5b5de48a). (#4470)
* Объект config.post_configProfileSwitch теперь принимает необязательный именованный аргумент prevConf, позволяющий обработчикам принять решение на основе различия конфигураций до и после переключения профиля. (#8758)

## 2018.3.2

В этом выпуске NVDA исправлена критическая ошибка, вызывающая аварийное завершение работы Google Chrome при переходе между твиттами на [www.twitter.com](http://www.twitter.com). (#8777)

## 2018.3.1

В этом выпуске NVDA исправлена критическая ошибка, вызывающая аварийное завершение работы 32-разрядной версии Mozilla Firefox. (#8759)

## 2018.3

Основные новшества этого выпуска включают в себя возможность автоматического определения подключений брайлевских дисплеев; поддержку новых возможностей Windows 10, например панели ввода эмодзи; и множество других исправлений.

### Новое

* В Mozilla Firefox и Google Chrome, NVDA теперь сообщает наличие грамматических ошибок, если web-страница предоставляет соответствующую информацию. (#8280)
* Содержимое отмеченное как "вставленное" или "удалённое" на web-страницах в Google Chrome, NVDA теперь сообщает соответствующим образом. (#8558)
* Добавлена поддержка колеса прокрутки в устройствах BrailleNote QT и Apex BT, когда они используются с NVDA в качестве брайлевских дисплеев. (#5992, #5993)
* Добавлены команды для чтения прошедшего и общего времени воспроизводимого трека в Foobar2000. (#6596)
* В таблицу символов NVDA добавлен символ Mac command key (⌘). (#8366)
* Во всех web-браузерах NVDA теперь поддерживает пользовательские ARIA-роли посредством атрибута aria-roledescription. (#8448)
* Добавлены новые брайлевские таблицы: Чешский восьмиточечный, Центральнокурдский (первая ступень), Эсперанто (первая ступень), Венгерский, Шведский восьмиточечный. (#8226, #8437)
* Добавлена поддержка автоматического определения подключений для брайлевских дисплеев. (#1271)
 * В настоящее время поддерживаются дисплеи ALVA, Baum/HumanWare/APH/Orbit, Eurobraille, Handy Tech, Hims, SuperBraille and HumanWare BrailleNote и Brailliant BI/B.
 * Для активации этой функции, в комбинированном списке "Брайлевский дисплей" диалога выбора брайлевского дисплея, выберите вариант "Определять автоматически".
 * Для получения дополнительной информации, пожалуйста, обратитесь к руководству пользователя NVDA.
* Добавлена поддержка современных функций ввода, представленных в последних выпусках Windows 10. К ним относится панель ввода эмодзи (Fall Creators Update), диктовка (Fall Creators Update), предложения по вводу для физической клавиатуры (April 2018 Update) и облачный буфер обмена (October 2018 Update). (#7273)
* В Mozilla Firefox 63 теперь поддерживается чтение блочных цитат определённых через ARIA-роль blockquote. (#8577)

### Изменения

* Список языков интерфейса в категории "Общие" диалога настроек NVDA теперь сортируется в алфавитном порядке. (#7284)
* Для всех поддерживаемых брайлевских дисплеев Freedom Scientific, добавлены жесты для эмуляции комбинаций клавиш alt+shift+tab и windows+tab. (#7387)
* Для дисплеев ALVA BC680 и protocol converter, теперь возможно назначить различные функции на левый и правый smart pad, а также на клавиши thumb и etouch. (#8230)
* Для дисплеев ALVA BC6, комбинация клавиш sp2+sp3 теперь сообщает текущее время и дату, а sp1+sp2 эмулирует нажатие клавиши windows. (#8230)
* Теперь при запуске NVDA, у пользователя спрашивается разрешение на передачу статистики использования программы в NV Access, выполняемой при проверке обновлений. (#8217)
* При проверке обновлений, если пользователь согласился на передачу статистики использования в NV Access, NVDA теперь будет отправлять название используемого синтезатора речи и брайлевского дисплея, чтобы помочь лучше определить приоритеты для будущей работы над их драйверами. (#8217)
* Liblouis braille translator обновлён до версии 3.6.0. (#8365)
* Исправлен путь к таблице русского компьютерного брайля. (#8446)
* Синтезатор речи eSpeak-ng обновлён до версии 1.49.3dev (коммит 910f4c2). (#8561)

### Исправления

* В Google Chrome, метки доступности для элементов управления не отображаемые как часть содержимого страницы в режиме обзора, теперь сообщаются при навигации клавишами-стрелками. (#4773)
* В приложении интернет-конференций Zoom теперь поддерживается чтение уведомлений. Например таких как статус вывода звука или уведомления о входящих сообщениях. (#7754)
* Переключение брайлевского представления контекста в режиме обзора, больше не вызывает последующую остановку брайлевского вывода. (#7741)
* Исправлены периодические ошибки инициализации брайлевских дисплеев ALVA BC680. (#8106)
* На брайлевских дисплеях ALVA BC6, по умолчанию больше не выполняется эмуляция клавиш системной клавиатуры с помощью комбинаций включающих в себя клавиши sp2+sp3, используемыми самими дисплеями для внутренних целей. (#8230)
* Нажатие sp2 для эмуляции клавиши alt на дисплеях ALVA BC6 теперь работает корректно. (#8360)
* NVDA больше не сообщает ошибочное переключение раскладки клавиатуры. (#7383, #8419)
* Отслеживание мыши теперь работает более корректно в Блокноте и в других текстовых элементах управления содержащих более 65535 символов. (#8397)
* NVDA теперь определяет большее число диалоговых окон в Windows 10 и в других современных приложениях. (#8405)
* NVDA теперь корректно отслеживает системный фокус в подвисших приложениях или при большом числе системных событий на Windows 10 October 2018 Update и Server 2019 и в более поздних версиях Windows. (#7345, #8535)
* Пользователь теперь уведомляется при попытке чтения или копирования в буфер обмена пустой строки состояния. (#7789)
* Исправлено чтение состояния неотмеченности для элементов управления, бывших ранее отмеченными частично. (#6946)
* Бирманский язык из комбинированного списка языков в общей категории диалога настроек NVDA на Windows 7 теперь отображается корректно. (#8544)
* NVDA теперь сообщает уведомления в Microsoft Edge, например такие как доступность режима чтения или прогресс загрузки страницы. (#8423)
* При переходе к списку на web-странице, NVDA теперь сообщает его метку доступности, если она имеется. (#7652)
* При ручном назначении жестов для конкретной модели брайлевского дисплея, эти жесты теперь всегда отображаются как назначенные именно для этого дисплея. Ранее они отображались так, как будто они были назначены на текущий активный дисплей. (#8108)
* Добавлена поддержка 64-х разрядной версии Media Player Classic. (#6066)
* Улучшена поддержка брайлевского вывода в Microsoft Word с активированным интерфейсом UI Automation:
 * Подобно другим многострочным текстовым полям, при установки каретки в начале документа Word, брайлевский дисплей теперь сначало отображает первый символ этого документа. (#8406)
 * Уменьшена чрезмерная многословность при установке системного фокуса на документ Word. (#8407)
 * Клавиши маршрутизации теперь корректно работают внутри списков документов Word. (#7971)
 * Набираемые в документе Word маркеры-цифры теперь сообщаются корректно как через речевой, так и через брайлевский вывод. (#7970)
* На Windows 10 1803 и более поздних версиях Windows, теперь возможно устанавливать дополнения даже если включена функция "Use Unicode UTF-8 for worldwide language support". (#8599)
* NVDA теперь корректно работает с iTunes версии 12.9. (#8744)

### Изменения для разработчиков

* Добавлена функция scriptHandler.script, которая может быть использована в качестве декоратора скриптов для скриптовых объектов. (#6266)
* В NVDA реализована автоматизированная система тестирования. (#708)
* В модуле hwPortUtils сделаны некоторые изменения: (#1271)
 * Функция-генератор listUsbDevices теперь перечисляет словари с информацией о доступных устройствах, включая hardwareID и devicePath.
 * Словари перечисляемые с помощью listComPorts теперь также содержат запись usbID для COM-портов с информацией о USB VID/PID в их идентификаторе оборудования.
* WXPython обновлён до версии 4.0.3. (#7077)
* Поскольку NVDA теперь поддерживает только Windows 7 SP1 и более поздние версии Windows, ключ "minWindowsVersion", используемый для проверки того, должен ли быть активирован UIA в определённых версиях Windows, был удалён. (#8422)
* Теперь вы можете подписаться на получение уведомлений о сохранении/сбросе конфигурации с помощью новых объектов config.pre_configSave, config.post_configSave, config.pre_configReset и config.post_configReset. (#7598)
 * config.pre_configSave используется для уведомления о предстоящим сохранении конфигурации, а config.post_configSave вызывается когда конфигурация уже была сохранена.
 * config.pre_configReset и config.post_configReset содержат флаг заводских настроек по умолчанию, указывающий, будет ли загружена конфигурация с диска (false) или она будет сброшена до значения по умолчанию (true).
* config.configProfileSwitch был переименован в config.post_configProfileSwitch, чтобы отразить тот факт, что это действие вызывается после переключения профиля. (#7598)
* Интерфейсы UI Automation обновлены до версий из Windows 10 October 2018 Update и Server 2019 (IUIAutomation6 / IUIAutomationElement9). (#8473)

## 2018.2.1

Этот выпуск включает в себя обновления некоторых переводов не попавших в релиз 2018.2 из-за устранения в последнюю минуту функции, которая вызывала проблемы.

## 2018.2

Основные новшества этого выпуска включают в себя поддержку таблиц в Kindle для PC, поддержку брайлевских дисплеев HumanWare BrailleNote Touch и Brailliant BI 14, улучшения в речевых синтезаторах Onecore и Sapi5, улучшения в Microsoft Outlook и многое другое.

### Новое

* NVDA теперь сообщает объединённые ячейки строк и столбцов в таблицах, как с помощью речи, так и с помощью брайлевского дисплея. (#2642)
* NVDA теперь поддерживает команды навигации по таблицам в Google-документах (с включённым режимом брайля). (#7946)
* Добавлена поддержка чтения и навигации по таблицам в Kindle для PC. (#7977)
* Добавлена поддержка брайлевских дисплеев HumanWare BrailleNote touch и Brailliant BI 14, с подключением как через bluetooth, так и через USB. (#6524)
* Начиная с Windows 10 Fall Creators Update, NVDA теперь может сообщать уведомления от таких приложений как Калькулятор и Магазин Windows (Windows Store). (#7984)
* Добавлены новые брайлевские таблицы: Литовский восьмиточечный, Украинский, Монгольский (вторая ступень). (#7839)
* Добавлен скрипт для чтения форматирования текста под определённой брайлевской ячейкой. (#7106)
* При обновлении NVDA, теперь возможно отложить установку загруженного обновления на более позднее время. (#4263)
* Добавлены новые языки интерфейса: монгольский и швейцарский немецкий.
* Теперь с помощью клавиатуры брайлевского дисплея, возможно эмулировать зажатие и отпускание клавиш-модификаторов control, shift, alt, windows и NVDA, комбинируя их с прочим брайлевским вводом (например можно выполнить нажатие control+s). (#7306)
 * Назначить желаемые жесты на эти команды эмуляции модификаторов, вы можете в разделе "Эмулируемые клавиши системной клавиатуры" диалога "Жесты ввода".
* Восстановлена поддержка брайлевских дисплеев Handy Tech Braillino и Modular со старой прошивкой. (#8016)
* Дата и время для поддерживаемых устройств Handy Tech (таких как Active Braille и Active Star) теперь будет автоматически синхронизироваться NVDA, когда рассинхронизация достигает более пяти секунд. (#8016)
* В диалоге "Жесты ввода", теперь можно назначить пользовательский жест на команду отключения/включения всех автопереключателей профилей конфигурации. (#4935)

### Изменения

* Состояния дополнений в менеджере дополнений теперь указываются как включено/отключено, вместо запущено/приостановлено. (в русском переводе так было и раньше. прим. перев.). (#7929)
* Liblouis braille translator обновлён до версии 3.5.0. (#7839)
* Брайлевская таблица для литовского языка была переименована в Литовский шеститочечный, чтобы избежать путаницы с новой восьмиточечной таблицей. (#7839)
* Брайлевские таблицы Канадского французского первой и второй ступени были удалены. Вместо них теперь используется Французский стандартный шеститочечный и Французский второй ступени соответственно. (#7839)
* Вторичные клавиши маршрутизации на брайлевских дисплеях Alva BC6, EuroBraille и Papenmeier теперь используются для получения информации о форматировании текста в брайлевских ячейках под этими клавишами. (#7106)
* Брайлевские таблицы сокращённой формы ввода теперь будут автоматически переключаться в полную форму в случае отсутствия возможности ввода текста. То есть на элементах управления, где нет каретки или активен режим обзора. (#7306)
* В календаре Outlook, NVDA теперь менее многословна, когда встреча или интервал времени охватывают весь день. (#7949)
* Все настройки NVDA теперь собраны в едином диалоговом окне, которое можно открыть из главного меню NVDA/Параметры/Настройки... (#577)
* Речевым синтезатором по умолчанию на Windows 10 теперь вместо eSpeak является Windows OneCore. (#8176)

### Исправления

* В окне входа в учётную запись Microsoft, NVDA теперь корректно читает элементы управления в фокусе после ввода E-mail и нажатия клавиши Enter. (#7997)
* NVDA теперь корректно читает web-документ при возврате на предыдущую страницу в Microsoft Edge. (#7997)
* NVDA теперь корректно сообщает последний символ PIN-кода при разблокировке компьютера под управлением Windows 10. (#7908)
* В режиме обзора, при использовании быстрой навигации или табуляции в Chrome или Firefox, метки флажков и радиокнопок теперь сообщаются только один раз. (#7960)
* NVDA теперь обрабатывает атрибут aria-current со значением false как false, а не как true. (#7892)
* Драйвер синтезатора Windows OneCore теперь загружается корректно, даже если ранее настроенный голос был удалён. (#7553)
* Смена голосов в драйвере синтезатора Windows OneCore теперь происходит значительно быстрее. (#7999)
* Исправлен некорректный брайлевский вывод для некоторых брайлевских таблиц, включая признак заглавной буквы в сокращённом Датском восьмиточечном брайле. (#7526, #7693)
* NVDA теперь может сообщать большее число разновидностей маркеров в Microsoft Word. (#6778)
* Команда чтения форматирования текста теперь больше ошибочно не перемещает просмотровый курсор и как следствие, многократный её вызов теперь всегда даёт один и тот же результат. (#7869)
* Брайлевский ввод больше не использует сокращённый брайль в неподдерживаемых ситуациях. То есть целые слова больше нельзя отправлять системе в не текстовые элементы управления или при активном режиме обзора. (#7306)
* Исправлены проблемы со стабильностью подключения брайлевских дисплеев Handy Tech Easy Braille и Braille Wave. (#8016)
* В Windows 8 и более поздних версиях, NVDA больше не сообщает фразу "неизвестно" при открытии меню быстрых ссылок (windows+x) и выборе элементов из него. (#8137)
* Назначенные для конкретных моделей жесты для кнопок брайлевских дисплеев Hims, теперь работают так, как это указано в руководстве пользователя. (#8096)
* NVDA теперь будет пытаться востанавливать регистрацию COM-объектов, используемых для доступа к таким приложениям как Firefox и Internet Explorer, исправляя проблему их доступности и убирая постоянно сообщаемую фразу "неизвестно". (#2807)
* Реализован обход ошибки в диспетчере задач, из-за которой NVDA не могла получить подробные сведения о процессах. (#8147)
* Решена проблема с отставанием речи в некоторых новых голосах Microsoft SAPI5, что делает их гораздо более удобными при навигации. (#8174)
* В последних версиях Windows, NVDA больше не сообщает метки LTR и RTL при обращении к объекту системных часов. (#5729)
* Обнаружение клавиш прокрутки на брайлевских дисплеях Hims Smart Beetle теперь снова работает правильно. (#6086)
* В некоторых текстовых элементах управления, в частности в приложениях написанных на Delphi, предоставляемая информация о редактировании и навигации теперь является намного более корректной. (#636, #8102)
* NVDA больше не сообщает излишнюю информацию при переключении между окнами по alt+tab в Windows 10 Redstone 5. (#8258)

### Изменения для разработчиков

* Информация для разработчиков (developer info) объектов UIA, теперь содержит список доступных UIA-шаблонов. (#5712)
* Модули для приложений теперь могут заставить определённые окна всегда использовать UIA, реализуя метод isGoodUIAWindow. (#7961)
* Скрытый логический флаг "outputPass1Only" в секции braille профилей конфигурации снова был удалён. Liblouis больше не поддерживает однопроходный вывод. (#7839)

## 2018.1.1

Это специальный выпуск NVDA, исправляющий баг в драйвере синтезатора Windows OneCore, из-за которого голоса этого синтезатора на Windows 10 April 2018 Update звучат с увеличенной скоростью и высотой. (#8082)

## 2018.1

Основные новшества этого выпуска включают в себя поддержку диаграмм в Microsoft word и Powerpoint, поддержку новых брайлевских дисплеев Eurobraille и Optelec protocol converter, улучшенную поддержку дисплеев Hims и Optelec, улучшение производительности в Mozilla Firefox 58 и многое другое.

### Новое

* В Microsoft Word и Microsoft Powerpoint добавлена возможность взаимодействия с диаграммами, аналогичная существующей поддержке диаграмм в Microsoft Excel. (#7046)
 * Для начала взаимодействия с диаграммой в Microsoft Word, переместите курсор в режиме обзора на желаемую диаграмму и нажмите enter.
 * В Microsoft Powerpoint, при редактировании слайда используйте клавишу tab для перехода к объекту диаграммы и enter или пробел для начала взаимодействия с ней.
 * Для прекращения взаимодействия с диаграммой нажимайте клавишу escape.
* Новый язык интерфейса: Киргизский.
* Добавлена поддержка для приложения VitalSource Bookshelf. (#7155)
* Добавлена поддержка Optelec protocol converter. Это устройство позволяет использовать брайлевские дисплеи Braille Voyager и Satellite посредством протокола связи ALVA BC6. (#6731)
* На брайлевском дисплее ALVA 640 Comfort теперь возможно использовать брайлевский ввод. (#7733)
 * Функциональность брайлевского ввода можно использовать как на этом, так и на других дисплеях BC6 с прошивкой версии 3.0.0 и более поздней версии.
* Добавлена первоначальная поддержка Таблиц Google с включённым режимом брайля. (#7935)
* Добавлена поддержка брайлевских дисплеев Eurobraille Esys, Esytime и Iris. (#7488)

### Изменения

* Драйвера брайлевских дисплеев HIMS Braille Sense/Braille EDGE/Smart Beetle и Hims Sync Braille были заменены одним единым драйвером. Новый драйвер будет автоматически активирован для бывших пользователей драйвера syncBraille. (#7459)
 * Некоторые клавиши, особенно клавиши прокрутки, были переназначены в соответствии с используемыми соглашениями для продуктов Hims. Для получения более подробной информации, обратитесь к руководству пользователя NVDA.
* При наборе текста на сенсорном экране с помощью экранной клавиатуры, теперь по умолчанию вы должны нажимать на каждую клавишу по два раза, точно также, как активируете любой другой элемент управления. (#7309)
 * Для использования существующего режима "Ввода касанием", где для активации желаемой клавиши достаточно отпустить над ней палец, следует установить соответствующий флажок в диалоге "Сенсорное взаимодействие", доступном в подменю "Параметры".
* Больше нет необходимости явно привязывать брайлевский вывод к системному фокусу или просмотровому курсору, поскольку теперь по умолчанию это будет происходить автоматически. (#2385)
 * Обратите внимание, что автоматическая привязка к просмотровому курсору будет происходить только при непосредственном использовании комманд просмотрового курсора или объектной навигации. Прокрутка с брайлевского дисплея не будет активировать это новое поведение.

### Исправления

* Окна с сообщениями в режиме обзора (такие как информация о форматировании текста, вызываемая двойным нажатием NVDA+f) теперь отображаются корректно, даже если в пути по которому установлена NVDA присутствуют не-ascii символы. (#7474)
* Фокус теперь вновь корректно восстанавливается при переходе в Spotify из окон других приложений. (#7689)
* В Windows 10 Fall Creaters update, при включённой в центре безопасности защитника Windows функции контролируемого доступа к папкам, NVDA теперь обновляется корректно. (#7696)
* Обнаружение клавиш прокрутки на брайлевских дисплеях Hims Smart Beetle теперь работает более надёжно. (#6086)
* Немного улучшена производительность при отрисовке большого объёма контента в Firefox 58 и в его более поздних версиях. (#7719)
* В Microsoft Outlook, чтение писем содержащих таблицы больше не вызывает ошибок. (#6827)
* Жесты брайлевских дисплеев, эмулирующие клавиши-модификаторы системной клавиатуры, теперь могут комбинироваться с другими эмулированными клавишами клавиатуры, даже если один или несколько используемых жестов привязаны к конкретной модели дисплея. (#7783)
* В Firefox, режим обзора теперь корректно работает во всплывающих окнах, созданных расширениями, такими как LastPass и bitwarden. (#7809)
* NVDA больше не зависает в некоторых ситуациях при каждом изменении фокуса, когда Firefox или Chrome перестают отвечать, например, из-за своего зависания или сбоя. (#7818)
* В таких twitter клиентах как Chicken Nugget, NVDA больше не игнорирует последние 20 символов при чтении твитта в 280 символов. (#7828)
* NVDA при выделенном тексте теперь использует правильный язык для чтения символов и знаков препинания. (#7687)
* В последних версиях Office 365, теперь снова можно перемещаться по диаграммам Excel с помощью клавиш-стрелок. (#7046)
* В брайлевском и речевом выводе, NVDA теперь сообщает состояния элементов управления в одном и томже порядке, независимо от их разновидности. (#7076)
* В таких приложениях как Windows 10 Mail, NVDA теперь корректно сообщает удаляемый символ при использовании клавиши backspace. (#7456)
* Все клавиши на дисплеях Hims Braille Sense Polaris теперь работают так, как и ожидается. (#7865)
* NVDA больше не падает на Windows 7, жалуясь на отсутствие некоторых динамически загружаемых библиотек (dll), если в системе уже установлена определённая версия пакета Microsoft Visual C++ 2017 Redistributable. (#7975)

### Изменения для разработчиков

* В секции braille конфигурационных профилей добавлен скрытый логический флаг "outputPass1Only". (#7301, #7693, #7702)
 * Этот флаг по умолчанию установлен в true. Если поменять значение на false, то при брайлевском выводе, liblouis будет использовать многопроходные правила.
* Для обеспечения плавного перехода пользователям, использующим заменённые драйверы брайлевских дисплеев, был добавлен новый словарь braille.RENAMED_DRIVERS. (#7459)
* Пакет comtypes обновлён до версии 1.1.3. (#7831)
* В braille.BrailleDisplayDriver для взаимодействия с дисплеями посылающими пакеты с подтверждениями, реализована система обобщений. За примером обратитесь к драйверу дисплеев handyTech. (#7590, #7721)
* Новая переменная "isAppX" в модуле config может быть использована для детектирования работы NVDA как приложения Windows Desktop Bridge Store. (#7851)
* Для реализаций документов, таких как NVDAObjects или browseMode которые имеют textInfo, теперь имеется новый класс documentBase.DocumentWithTableNavigation, который может быть унаследован, чтобы получить стандартные скрипты навигации по таблице. Пожалуйста, обратитесь к этому классу, чтобы узнать, какие вспомогательные методы должны быть предоставлены вашей реализацией для навигации по таблице. (#7849)
* Пакетный файл scons теперь лучше обрабатывает ситуацию, когда имеется установленный Python 3, используя python launcher для запуска 32-х разрядной версии Python 2.7. (#7541)
* Конструктор класса hwIo.Hid теперь принимает дополнительный параметр exclusive, значение по умолчанию которого установлено в True. Если установить значение в False, то другим приложениям будет разрешено связываться с устройством, когда оно подключено к NVDA. (#7859)

## 2017.4

Основные новшества этого выпуска включают в себя множество исправлений и улучшений при работе с web-страницами, в том числе автоматическую активацию режима обзора в web-диалогах, улучшения в чтении меток групп полей форм в режиме обзора, поддержку новых технологий Windows 10, таких как Windows Defender Application Guard и Windows 10 на платформе ARM64, а также автоматическое чтение изменений ориентации экрана и состояния батареи.
Обратите внимание, что эта версия NVDA больше не поддерживает Windows XP или Windows Vista. Теперь для работы NVDA требуется Windows 7 SP1 или более поздняя версия системы.

### Новое

* В режиме обзора, теперь возможно используя команды перехода к концу/началу элемента-контейнера (запятая и shift+запятая) перемещаться по ARIA-ориентирам (landmarks). (#5482)
* В Firefox, Chrome и Internet Explorer, быстрая навигация по полям форм и полям редакторов, теперь учитывает и элементы содержащие форматированный текст (имеющие атрибут contentEditable). (#5534)
* В web-браузерах, в диалоге "Список элементов" теперь можно получить список кнопок и полей форм. (#588)
* Добавлена начальная поддержка Windows 10 на платформе ARM64. (#7508)
* Добавлена предварительная поддержка чтения и интерактивной навигации по математическому содержимому в книгах Kindle с доступным математическом контентом. (#7536)
* Добавлена поддержка программы чтения электронных книг Azardi. (#5848)
* При обновлении уже установленных дополнений, теперь сообщается информация о версии обновления. (#5324)
* Добавлены новые параметры командной строки для создания переносной копии NVDA. (#6329)
* Добавлена поддержка web-браузера Microsoft Edge запущенного в среде Windows Defender Application Guard на Windows 10 Fall Creators Update. (#7600)
* При работе на ноутбуке или планшете, NVDA теперь автоматически сообщает о подключении/отключении зарядного устройства и об изменении ориентации экрана. (#4574, #4612)
* Добавлен македонский язык интерфейса.
* Добавлены новые брайлевские таблицы: Хорватский (первая ступень), Вьетнамский (первая ступень). (#7518, #7565)
* Добавлена поддержка брайлевского дисплея Actilino от Handy Tech. (#7590)
* Добавлена поддержка брайлевского ввода для дисплеев Handy Tech. (#7590)

### Изменения

* Минимальной поддерживаемой версией операционной системы для NVDA теперь является Windows 7 Service Pack 1 или Windows Server 2008 R2 Service Pack 1. (#7546)
* В Web-диалогах браузеров Firefox и Chrome, теперь автоматически используется режим обзора при нахождении в web-приложениях. (#4493)
* При использовании в режиме обзора табуляции и клавиш быстрой навигации, теперь больше не сообщаются выходы из элементов-контейнеров (например таблицы и списки), что делает навигацию более удобной. (#2591)
* В режиме обзора, названия групп полей форм в web-браузерах Firefox и Chrome, теперь сообщаются автоматически при переходе к ним с помощью табуляции или клавиш быстрой навигации. (#3321)
* Команды быстрой навигации режима обзора для перехода по встроенным объектам (o и shift+o), теперь учитывают аудио и видео элементы, а также элементы с ARIA-ролями application и dialog. (#7239)
* Espeak-ng был обновлён до версии 1.49.2, что решило некоторые проблемы при сборке. (#7385, #7583)
* Тройной вызов команды чтения текста строки состояния, теперь копирует этот текст в буфер обмена. (#1785)
* При назначении команд на клавиши брайлевского дисплея Baum, вы теперь можете ограничить их использование конкретной моделью дисплея (например VarioUltra или Pronto). (#7517)
* Горячая клавиша для поля "Фильтр по" в диалоге "Список элементов" режима обзора, была изменена с alt+ф на alt+т. (#7569)
* В режиме обзора добавлена команда для быстрого включения/выключения чтения таблиц используемых для разметки на web-страницах. Вы можете найти эту команду в разделе "Режим обзора" диалога "Жесты ввода". Желаемый жест на неё пользователь должен назначить самостоятельно. (#7634)
* Liblouis braille translator обновлён до версии 3.3.0. (#7565)
* Горячая клавиша для радиокнопки "Регулярное выражение" в диалоге добавления/редактирования словарной статьи, была изменена с alt+в на alt+г. (#6782)
* Файлы голосовых словарей теперь версируются и были перемещены в каталог "speechDicts/voiceDicts.v1". (#7592)
* Изменения в версированных файлах (пользовательская конфигурация, голосовые словари) более не сохраняются если NVDA запущена как временная копия из пакета установки. (#7688)
* Брайлевские дисплеи Braillino, Bookworm и Modular (со старой прошивкой) от Handy Tech больше не поддерживаются из коробки. Для их использования, вам следует установить Handy Tech Universal Driver и соответствующее дополнение к NVDA. (#7590)

### Исправления

* Ссылки в таких приложениях как Microsoft Word, теперь указываются на брайлевском дисплее. (#6780)
* В web-браузерах Firefox или Chrome, NVDA больше не становится значительно медленнее при открытии большого количества вкладок. (#3138)
* Клавиши маршрутизации на брайлевском дисплее MDV Lilli теперь корректно устанавливают курсор на желаемую ячейку, вместо его установки на следующую после желаемой. (#7469)
* В Internet Explorer и других документах MSHTML, HTML5 атрибут required теперь поддерживается для указания обязательности заполнения поля формы. (#7321)
* При наборе арабских символов в выровненном по левому краю документе WordPad, брайлевский вывод теперь обновляется корректно. (#511)
* В Mozilla Firefox, NVDA при навигации клавишами-стрелками в режиме обзора теперь сообщает текст доступных меток для элементов управления, когда они не отображаются как контент сами по себе. (#4773)
* NVDA на Windows 10 Creaters Update теперь может быть перезагружена при запущенном Firefox, без потери возможности чтения web-страниц в режиме обзора. (#7269)
* Перезагрузка NVDA при установленном фокусе в окне Mozilla Firefox больше не "ломает" режим обзора, хотя для его восстановления вам возможно потребуется переместить фокус в другое окно (alt+tab) и затем вернуться обратно. (#5758)
* Отсутствие Firefox больше не мешает на некоторых системах получить доступ к математическому содержимому в Google Chrome. (#7308)
* При обновлении NVDA, операционная система и прочие приложения до перезагрузки компьютера теперь должны работать более стабильно. (#7563)
* При вызове команды распознавания контента (например NVDA+r) при отсутствующем объекте навигатора, NVDA теперь читает сообщение об ошибке, вместо возникновения необработанного исключения. (#7567)
* Для некоторых брайлевских дисплеев Freedom Scientific была исправлена функция обратной прокрутки. (#7713)

### Изменения для разработчиков

* Команда "scons tests" теперь проверяет, что переводимые строки имеют комментарии для переводчиков. Вы также можете запустить эту проверку отдельно с помощью команды "scons checkPot". (#7492)
* Доступен новый модуль extensionPoints, который предоставляет общий механизм для обеспечения расширяемости в определённых точках кода. Он позволяет заинтересованным сторонам регистрироваться и получать уведомления, когда происходит какое либо действие (extensionPoints.Action), модифицировать конкретный тип данных (extensionPoints.Filter) и принимать решение о выполнении того или иного действия (extensionPoints.Decider). (#3393)
* Теперь с помощью config.configProfileSwitched вы можете подписаться на получение уведомлений о переключениях профилей конфигурации. (#3393)
* Жесты брайлевского дисплея, которые эмулируют клавиши-модификаторы системной клавиатуры (такие как control и alt), теперь можно комбинировать с другими эмулированными клавишами без явного определения. (#6213)
 * Например, если одна клавиша на брайлевском дисплее эмулирует нажатие alt, а другая стрелки вниз, то комбинация этих клавиш вызовет эмуляцию нажатия alt+стрелка вниз.
* Класс braille.BrailleDisplayGesture теперь имеет дополнительный атрибут model. Если этот атрибут предоставляется драйвером дисплея, то нажатие клавиши приведет к генерации дополнительного идентификатора жеста для конкретной модели. Это позволяет пользователю привязывать жесты ограниченные конкретной моделью брайлевского дисплея.
 * За примером реализации этой функции, обратитесь к драйверу брайлевских дисплеев baum.
* Для сборки NVDA из исходных кодов теперь используется Visual Studio 2017 и Windows 10 SDK. (#7568)

## 2017.3

Основные новшества этого выпуска включают в себя поддержку сокращённой формы брайлевского ввода, поддержку новых голосов Windows OneCore доступных в Windows 10, встроенную поддержку Windows 10 OCR и множество значительных улучшений в поддержке брайля и работы в интернете.

### Новое

* В диалог настроек брайля добавлена опция "Показывать сообщения бесконечно". (#6669)
* В списках сообщений Microsoft Outlook, NVDA теперь может сообщать отметки для выбранного сообщения. (#6374)
* При редактировании слайдов в Microsoft Powerpoint, NVDA теперь указывает точный тип фигуры (например такой как треугольник, круг, видео или стрелка), вместо простого чтения слова "фигура". (#7111)
* В Google Chrome теперь поддерживается чтение математического содержимого в формате MathML. (#7184)
* NVDA для синтеза речи теперь может использовать новые голоса Windows OneCore (также известные как Microsoft Mobile voices) включённые в Windows 10. Для получения доступа к этим голосам, в диалоге настроек синтезатора выберите Windows OneCore voices. (#6159)
* Файлы пользовательской конфигурации NVDA теперь могут храниться в каталоге AppData/Local текущего пользователя. Настроить такое поведение можно с помощью специального параметра в реестре Windows. Для получения дополнительной информации обратитесь к разделу 'Общесистемные параметры' в руководстве пользователя NVDA. (#6812)
* В web-браузерах, у полей форм теперь сообщаются значения атрибутов aria-placeholder. (#7004)
* В Microsoft Word, для перемещения по орфографическим ошибкам в режиме обзора теперь можно использовать клавиши быстрой навигации (w и shift+w). (#6942)
* В Microsoft Outlook, добавлена поддержка элемента управления выбора даты для диалога создания встречи. (#7217)
* NVDA теперь сообщает выбираемое предложение по вводу в полях кому/копия в Windows 10 Mail и в поле поиска настроек Windows 10. (#6241)
* NVDA теперь воспроизводит звуковой сигнал при появлении предложений по вводу в некоторых полях поиска Windows 10 (например стартовый экран, поиск настроек, поля кому/копия в приложении Windows 10 mail). (#6241)
* NVDA теперь автоматически сообщает уведомления в Skype для бизнеса (например когда кто-то начинает с вами беседу). (#7281)
* NVDA теперь автоматически сообщает входящие сообщения чата во время беседы в Skype для бизнеса. (#7286)
* NVDA теперь автоматически сообщает уведомления в Microsoft Edge (например когда начинается загрузка файла). (#7281)
* Теперь с помощью клавиатуры брайлевского дисплея вы можете использовать как сокращённый, так и полный брайлевский ввод. Для получения дополнительной информации обратитесь к разделу "Брайлевский ввод" в руководстве пользователя NVDA. (#2439)
* В диалоге настроек брайля, после выбора "Брайлевский Unicode" в качестве брайлевской таблицы ввода, теперь можно набирать брайлевские unicode символы с клавиатуры брайлевского дисплея. (#6449)
* Добавлена поддержка используемого в Тайване брайлевского дисплея SuperBraille. (#7352)
* Новые брайлевские таблицы: Датский восьмиточечный, Литовский, Персидский восьмиточечный, Персидский (первая ступень), Словенский восьмиточечный. (#6188, #6550, #6773, #7367)
* Улучшения в таблице американского английского восьмиточечного брайля, включая поддержку маркеров, знака евро и букв с диакритикой. (#6836)
* NVDA теперь может использовать функциональность оптического распознавания символов (OCR) встроенную в Windows 10 для чтения текста на изображениях или из окон недоступных приложений. (#7361)
 * Язык распознавания можно установить в новом диалоге из меню NVDA/Параметры/Windows 10 OCR.
 * Для распознавания содержимого текущего объекта навигатора, нажимайте NVDA+r.
 * Для получения дополнительной информации обратитесь к разделу "Распознавание контента" в руководстве пользователя NVDA.
* Теперь с помощью новой опции "Представление контекста" в диалоге настроек брайля вы можете выбрать, какая контекстная информация будет отображаться на брайлевском дисплее когда объект получает фокус. (#217)
 * Например значения "При изменении контекста" и "Только при прокрутке назад" могут сделать работу со списками и меню более эффективной, поскольку элементы не будут постоянно менять свое положение на дисплее.
 * Для получения дополнительной информации и примеров обратитесь к разделу "Представление контекста" в руководстве пользователя NVDA.
* В Firefox и Chrome, NVDA теперь поддерживает сложные динамические сетки, например таблицы в которых может быть загружена или отображена только часть содержимого (а именно поддерживаются атрибуты aria-rowcount, aria-colcount, aria-rowindex и aria-colindex представленные в ARIA 1.1). (#7410)

### Изменения

* В раздел "Разное" диалога "Жесты ввода" добавлена команда для быстрой перезагрузки NVDA. Желаемый жест на неё пользователь должен назначить самостоятельно. (#6396)
* Желаемую раскладку клавиатуры теперь можно выбрать в диалоге "Добро пожаловать". (#6863)
* Названия множества дополнительных типов элементов управления и их состояний, а также ориентиров были сокращены при отображении их на брайлевском дисплее. Для получения полного списка сокращений, пожалуйста обратитесь к подразделу "Сокращения для типов элементов управления, их состояния и ориентиров" в руководстве пользователя NVDA. (#7188, #3975)
* Синтезатор речи eSpeak NG обновлён до версии 1.49.1. (#7280)
* Брайлевские таблицы ввода/вывода в соответствующих списках диалога настроек брайля теперь сортируются в алфавитном порядке. (#6113)
* Liblouis Braille Translator обновлён до версии 3.2.0. (#6935)
* Брайлевской таблицей ввода/вывода по умолчанию теперь является унифицированный американский английский брайль первой ступени. (#6952)
* Теперь по умолчанию при смене фокуса, NVDA отображает на брайлевском дисплее только изменённую контекстную информацию. (#217)
 * В прошлых версиях NVDA, отображалось как можно больше контекстной информации, независимо от того, видели ли вы её ранее.
 * Вы можете вернуть старое поведение установив в диалоге настроек брайля новую опцию "Представление контекста" в значение "Всегда".
* При использовании брайлевского дисплея, форма брайлевского курсора может быть настроена отдельно для привязок к системному фокусу и просмотровому курсору. (#7112)
* Логотип NVDA был обновлён. Новый логотип использует фиолетовый цвет с логотипа NV Access и представляет собой стилизованное сочетание белых букв "NVDA" на сплошном фиолетовом фоне. Это гарантирует его видимость на любом цветовом фоне. (#7446)

### Исправления

* В режиме обзора, метки редактируемых div-элементов в Chrome больше не сообщаются как их значения. (#7153)
* В пустом документе Microsoft Word, нажатие клавиши End в режиме обзора больше не вызывает исключение RuntimeError. (#7009)
* Режим обзора теперь корректно поддерживается в Microsoft Edge, даже если открытому документу присвоена специфическая ARIA-роль. (#6998)
* В режиме обзора, клавишами shift+end теперь возможно выделить или снять выделение текста до конца строки, даже если каретка установлена на последнем символе этой строки. (#7157)
* Если диалог содержит линейку прогресса, то текст диалога на брайлевском дисплее теперь обновляется вместе с ней. Например это значит, что в диалоге загрузки обновления NVDA теперь возможно прочитать оставшееся время. (#6862)
* NVDA теперь сообщает изменение выбора в некоторых комбинированных списках Windows 10, например в таких как при настройки автозапуска со сменных носителей. (#6337)
* В диалоге создания собрания/встречи в Microsoft Outlook, NVDA больше не сообщает бессмысленную информацию. (#7216)
* Звуковой сигнал в диалогах с неопределённой линейкой прогресса (например диалог проверки обновлений) теперь проигрывается только если в NVDA настроены звуковые сигналы для линеек прогресса. (#6759)
* В Microsoft Excel 2003 и 2007, NVDA теперь снова сообщает ячейки листа при перемещении по ним стрелками. (#7243)
* В Windows 10 Creators Update и более поздних версиях, режим обзора теперь снова автоматически включается при чтении электронных писем в приложении Windows 10 Mail. (#7289)
* На большинстве брайлевских дисплеев с брайлевской клавиатурой, клавиша точка 7 теперь стирает последнюю введённую брайлевскую ячейку или символ, а точка 8 эмулирует нажатие клавиши Enter. (#6054)
* При перемещении каретки в редактируемом тексте (например с помощью курсорных клавиш или клавиши backspace), голосовой отклик NVDA во многих случаях теперь более точен, особенно это заметно в в Chrome и консольных приложениях. (#6424)
* Содержимое редактора подписи в Microsoft Outlook 2016 теперь может быть прочитано. (#7253)
* В приложениях Java Swing, NVDA больше не вызывает иногда аварийное завершение приложения при навигации по таблицам. (#6992)
* В Windows 10 Creators Update, NVDA больше не сообщает всплывающие уведомления несколько раз. (#7128)
* Закрытие меню Пуск в Windows 10 после ввода поискового запроса и нажатия Enter, больше не вызывает чтение введённого текста. (#7370)
* Быстрая навигация по заголовкам в Microsoft Edge теперь работает значительно быстрее. (#7343)
* В Microsoft Edge, при навигации в режиме обзора, NVDA больше не пропускает значительные фрагменты некоторых web-страниц, например страниц Wordpress с темой Twenty Fifteen. (#7143)
* Имена ориентиров в Microsoft Edge теперь корректно локализованы на всех языках помимо английского. (#7328)
* Брайль теперь корректно следует за выделением при выделении текста за пределами ширины дисплея. Например если вы выделяете несколько строк клавишами shift+стрелка вниз, то дисплей теперь будет отображать последнюю выделенную строку. (#5770)
* В Firefox, NVDA больше не сообщает ошибочно слово "Секция" несколько раз при открытии подробностей твитта на twitter.com. (#5741)
* Команды навигации по таблице в режиме обзора больше недоступны для макетных таблиц если чтение таких таблиц отключено в диалоге настроек режима обзора. (#7382-
* В Firefox и Chrome, команды навигации по таблице в режиме обзора теперь пропускают скрытые ячейки. (#6652, #5655)

### Изменения для разработчиков

* Метки времени в журнале NVDA теперь содержат миллисекунды. (#7163)
* Для сборки NVDA из исходного кода теперь следует использовать Visual Studio Community 2015. Visual Studio Express больше не поддерживается. (#7110)
 * Так же теперь требуются Windows 10 Tools и SDK, выбрать которые можно при установке Visual Studio.
 * Для получения дополнительной информации обратитесь к разделу "Installed Dependencies" в файле readme.md.
* Поддержка распознавателей контента, например таких как OCR и Инструментов для описания изображений может быть легко реализована с помощью нового пакета contentRecog. (#7361)
* Пакет json из стандартной библиотеки Python теперь включён в бинарные сборки NVDA. (#3050)

## 2017.2

Основные новшества этого выпуска включают в себя полную поддержку функции приглушения сторонних звуков в Windows 10 Creators Update, исправления некоторых проблем с выделением текста в режиме обзора, включая проблему выделения всего текста, значительные улучшения в поддержке Microsoft Edge, а также индикацию на web-страницах элементов коллекции помеченных как текущие (использующих атрибуты aria-current).

### Новое

* Команда чтения форматирования (NVDA+f) в Microsoft Excel теперь сообщает информацию о границах ячеек. (#3044)
* В web-браузерах, NVDA теперь указывает когда элемент коллекции отмечен как текущий (с помощью атрибута aria-current). (#6358)
* В Microsoft Edge теперь поддерживается функция автоматического переключения языка активного синтезатора. (#6852)
* В Windows 10 Server и Enterprise LTSB (редакции с длительным сроком поддержки) добавлена поддержка стандартного калькулятора Windows. (#6914)
* Тройной быстрый вызов команды чтения строки под курсором приложения, теперь осуществляет чтение фонетических описаний всех буквенных символов этой строки. (#6893)
* Новый язык интерфейса NVDA: бирманский.
* NVDA теперь корректно сообщает unicode символы дробей и стрелок вверх/вниз. (#3805)

### Изменения

* При использовании облегчённого режима просмотра в приложениях UI Automation, теперь игнорируется большее число бесполезных объектов, упрощая тем самым объектную навигацию. (#6948, #6950)

### Исправления

* Элементы меню на web-страницах теперь могут быть активированы в режиме обзора. (#6735)
* Нажатие escape в диалоге подтверждения удаления профиля конфигурации, теперь отменяет удаление и закрывает этот диалог. (#6851)
* Исправлены некоторые сбои при работе в Mozilla Firefox и в других Gecko-приложениях при включённом режиме многопроцессности. (#6885)
* При отрисовки текста на прозрачном фоне, определение цвета фона в позиции просмотрового курсора теперь стало более точным. (#6467)
* В Internet Explorer 11 улучшена поддержка описания элементов управления на web-страницах (а именно поддержка атрибутов aria-describedby внутри элементов iframe и при наличии нескольких идентификаторов). (#5784)
* Функция приглушения сторонних звуков теперь снова работает в Windows 10 Creaters Update, также как и в предыдущих выпусках Windows (то есть теперь доступны все режимы - "Приглушать при выводе речи и звуков", "Всегда приглушать" и "Не приглушать"). (#6933)
* В NVDA больше не происходит ошибка при навигации по некоторым (UIA) элементам управления, если для них не определены комбинации горячих клавиш. (#6779)
* В некоторые (UIA) элементы управления больше не добавляются два лишних пробела к информации о комбинации горячих клавиш. (#6790)
* Нажатие некоторых комбинаций клавиш на брайлевских дисплеях HIMS (например пробел+dot4) больше не вызывает сбой в некоторых ситуациях. (#3157)
* Исправлена ошибка при открытии последовательного порта на системах с некоторыми, отличными от английского языками интерфейса, приводящая в некоторых случаях к сбою при подключении к брайлевским дисплеям. (#6845)
* Уменьшена вероятность повреждения конфигурационного файла NVDA при завершении работы Windows. Конфигурационный файл теперь записывается во временный файл, после чего он заменяет свою предыдущую версию. (#3165)
* Для чтения фонетических описаний символов при тройном быстром вызове команды чтения строки под курсором приложения, теперь используется соответствующий язык. (#6726)
* В Windows 10 Creaters Update, перемещение по строкам в Microsoft Edge теперь осуществляется до трёх раз быстрее. (#6994)
* В Windows 10 Creaters Update, NVDA больше не произносит фразу "Web Runtime grouping" при фокусировке на документах Microsoft Edge. (#6948)
* Теперь NVDA поддерживает все существующие версии SecureCRT. (#6302)
* Adobe Acrobat Reader больше не падает при открытии некоторых PDF-документов (а именно документов с пустыми атрибутами ActualText). (#7021, #7034)
* В режиме обзора в Microsoft Edge, NVDA больше не пропускает интерактивные таблицы (ARIA grids) при переходе по таблицам клавишами быстрой навигации t и shift+t. (#6977)
* Нажатие shift+home в режиме обзора после выделения от начала строки, теперь как и ожидается снимает это выделение. (#5746)
* Выделение всего текста в режиме обзора (control+a) теперь корректно работает даже если каретка не находится в начале выделяемого текста. (#6909)
* Исправлены некоторые редкие проблемы выделения текста в режиме обзора. (#7131)

### Изменения для разработчиков

* Аргументы командной строки теперь обрабатываются модулем argparse вместо устаревшего optparse, что позволяет реализовать взаимное исключение таких аргуменнтов как -r и -q. (#6865)
* core.callLater теперь вставляет функцию для обратного вызова в главную очередь NVDA после указанной задержки, вместо того, чтобы будить ядро и выполнять её напрямую. Это предотвращает возможные зависания из-за случайного засыпания ядра после обработки обратного вызова в середине модального вызова, такого как отображение диалогового окна сообщения. (#6797)
* Свойство InputGesture.identifiers больше не нормализуется. (#6945)
 * Подклассам больше не нужно нормализовывать идентификаторы перед возвратом их из этого свойства.
 * Если вам требуются нормализованные идентификаторы, то теперь есть свойство InputGesture.normalizedIdentifiers которое нормализует идентификаторы возвращаемые свойством identifiers.
* Свойство InputGesture.logIdentifier теперь является устаревшим. Вместо него следует использовать InputGesture.identifiers[0]. (#6945)
* Следующий устаревший код был удалён:
 * Константы `speech.REASON_*`. Вместо них теперь следует использовать `controlTypes.REASON_*`. (#6846)
 * `i18nName` для настройки синтезатора. Вместо него теперь следует использовать `displayName` и `displayNameWithAccelerator`. (#6846, #5185)
 * `config.validateConfig`. (#6846, #667)
 * `config.save`. Вместо него теперь следует использовать `config.conf.save`. (#6846, #667)
* Список окончаний в контекстном меню автозаполнения python консоли теперь показывает только варианты завершения для последнего атрибута, без полного пути до него. (#7023)
* Для исходного кода NVDA теперь проводится модульное тестирование. (#7026)
 * Unit-тесты и необходимая инфраструктура расположены в каталоге tests/unit. Подробности смотрите в строках документации файла tests\unit\init.py.
 * Вы можете запустить тесты командой "scons tests". Подробности смотрите в разделе "Running Tests" файла readme.md.
 * Если вы отправляете pull request для NVDA, то вы должны сначала запустить тесты и убедиться в их успешном прохождении.

## 2017.1

Основные новшества этого выпуска включают в себя возможность чтения разделов и текстовых колонок в Microsoft Word; поддержку чтения, навигации и аннотирования книг в Kindle для PC и улучшения в поддержке Microsoft Edge.

### Новое

* В документах Microsoft Word, NVDA теперь может сообщать номера разделов и типы разрывов разделов. Чтение этой информации управляется флажком "Номера страниц" в диалоге настроек "Форматирование документа". (#5946)
* В документах Microsoft Word, NVDA теперь может сообщать текстовые колонки. Чтение этой информации управляется флажком "Номера страниц" в диалоге настроек "Форматирование документа". (#5946)
* Функция автоматического переключения языков синтезатора, теперь также поддерживается и в Wordpad. (#6555)
* Функция поиска в режиме обзора (NVDA+control+f), теперь также поддерживается и в Microsoft Edge. (#6580)
* Быстрая навигация по кнопкам в режиме обзора (b и shift+b), теперь также поддерживается и в Microsoft Edge. (#6577)
* При копировании листа в Microsoft Excel, заголовки строк и столбцов теперь запоминаются. (#6628)
* Добавлена поддержка чтения и навигации по книгам в приложении Kindle для PC версии 1.19, в том числе доступ к ссылкам, сноскам, графическим элементам, интересным фрагментам текста и пользовательским заметкам. Для получения дополнительной информации, пожалуйста обратитесь к разделу "Kindle для PC" в руководстве пользователя NVDA. (#6247, #6638)
* NVDA в режиме обзора теперь поддерживает навигацию по таблицам в Microsoft Edge. (#6594)
* В Microsoft Excel, команда чтения положения просмотрового курсора (настольная раскладка: NVDA+delete на цифровом блоке, раскладка для ноутбука: NVDA+delete), теперь сообщает имя активного листа и адрес текущей ячейки. (#6613)
* В диалог завершения работы NVDA добавлена опция "Перезагрузить с журналом на уровне отладки". (#6689)

### Изменения

* Минимальная скорость мигания курсора на брайлевском дисплее теперь составляет 200 мс. Если ранее было установлено меньшее значение, то оно будет автоматически увеличено до 200 мс. (#6470)
* Для включения/отключения мигания брайлевского курсора в диалог настроек брайля был добавлен флажок "Мигание курсора". Ранее отключение мигания достигалось установкой его скорости в 0 мс. (#6470)
* Синтезатор речи eSpeak NG обновлён до коммита e095f008 от 10 января 2017 года. (#6717)
* Из-за изменений в Windows 10 Creators Update, режим "Всегда приглушать" был удалён из настроек приглушения звуков. Этот режим по-прежнему доступен в более старых выпусках Windows 10. (#6684)
* Из-за изменений в Windows 10 Creators Update, режим "Приглушать при выводе речи и звуков" больше не может гарантировать полное приглушение перед началом речевого вывода, и не будет достаточно долго приглушать сторонние звуки после его окончания для избежания резкого увеличения громкости приглушаемых звуков. Эти изменения не затрагивают более старые выпуски Windows 10. (#6684)

### Исправления

* Исправлено подвисание NVDA в Microsoft Word с режимом обзора, при перемещении по абзацам в большом документе. (#6368)
* Таблицы в Microsoft Word скопированные из Microsoft Excel больше не обрабатываются как макетные таблицы и поэтому более не игнорируются. (#5927)
* При попытке ввода символов в Microsoft Excel в режиме защищённого просмотра, NVDA теперь воспроизводит звук вместо чтения набираемых символов, которые на самом деле не вводятся. (#6570)
* Нажатие escape в Microsoft Excel больше не вызывает ошибочное переключение в режим обзора, если пользователь ранее явно командой NVDA+space уже перешёл в режим обзора, а затем нажатием enter на поле формы переключился в режим редактирования. (#6569)
* NVDA больше не зависает в таблицах Microsoft Excel, в которых вся строка или столбец были объединены. (#6216)
* Чтение обрезанности/переполненности ячеек в Microsoft Excel теперь должно быть более точным. (#6472)
* NVDA теперь сообщает состояние флажка только для чтения. (#6563)
* Средство запуска NVDA больше не показывает диалог предупреждения, когда оно не может воспроизвести звук приветствия из-за отсутствия в системе доступных звуковых устройств. (#6289)
* NVDA теперь сообщает недоступные элементы управления на ленте Microsoft Excel. (#6430)
* NVDA больше не читает слово "Область" при сворачивании окон. (#6671)
* В Windows 10 Creators Update, NVDA теперь сообщает вводимые символы в приложениях универсальной платформы Windows (Universal Windows Platform, UWP) (включая Microsoft Edge). (#6017)
* Функция отслеживания мыши теперь работает на всех экранах компьютеров с несколькими мониторами. (#6598)
* NVDA больше не становится непригодной для использования после закрытия Windows Media Player с фокусом установленным на элементе-ползунке. (#5467)

### Изменения для разработчиков

* Файлы профилей конфигурации теперь автоматически обновляются в соответствии с требованиями схемы изменений. Если при обновлении произойдёт ошибка, то пользователю будет показано уведомление, конфигурация сбросится, а старый файл конфигурации будет записан в журнал NVDA под уровнем 'Info'. (#6470)

## 2016.4

Основные новшества этого выпуска включают в себя улучшенную поддержку Microsoft Edge; активацию режима обзора в приложении "Почта" на Windows 10 и значительные улучшения в диалоговых окнах NVDA.

### Новое

* NVDA теперь может указывать отступы строк используя звуковые сигналы (чем больше отступ, тем выше частота воспроизводимого сигнала). Настроить такое поведение можно с помощью комбинированного списка "Чтение отступов строк" в диалоге настроек "Форматирование документа". (#5906)
* Добавлена поддержка брайлевского дисплея Orbit Reader 20. (#6007)
* Добавлена возможность автоматического открытия просмотрщика речи при запуске NVDA. Включить данную функцию можно с помощью соответствующего флажка в окне просмотрщика. (#5050)
* При переоткрытии окна просмотрщика речи, его положение и размеры теперь сохраняются. (#5050)
* Перекрёстные ссылки в Microsoft Word теперь обрабатываются как гиперссылки. Они читаются как ссылки и могут быть активированы. (#6102)
* Добавлена поддержка для брайлевских дисплеев Baum SuperVario2, Baum Vario 340 и HumanWare Brailliant2. (#6116)
* Добавлена начальная поддержка для Microsoft Edge в Windows 10 Anniversary Update. (#6271)
* Электронные письма в приложении "Почта" на Windows 10, теперь читаются в режиме обзора. (#6271)
* Добавлен литовский язык интерфейса.

### Изменения

* Liblouis braille translator обновлён до версии 3.0.0, включающей в себя значительные улучшения унифицированного английского брайля (Unified English Braille, UEB). (#6109, #4194, #6220, #6140)
* В менеджере дополнений, для кнопок отключения и включения выбранного дополнения добавлены горячие клавиши (alt+т и alt+в соответственно). (#6388)
* Исправлены некоторые проблемы отображения элементов графического интерфейса в диалогах NVDA. (#6317, #5548, #6342, #6343, #6349)
* Диалог настроек "Форматирование документа" теперь имеет функцию прокрутки, а различные опции в нём были организованы в группы. (#6348)
* Список символов в диалоге настроек "Произношение символов/пунктуации" теперь занимает всю ширину окна диалога. (#6101)
* В режиме обзора, команды быстрой навигации для перемещения по полям форм (f и shift+f) и полям редактирования (e и shift+e), теперь также осуществляют переход и по полям редактирования только для чтения. (#4164)
* В диалоге настроек "Форматирование документа", флажок "Читать изменения формата после курсора" был переименован в "Сообщать изменения форматирования после курсора", поскольку эта опция влияет как на речевой, так и на брайлевский вывод. (#6336)
* Скорректирован внешний вид диалога "Добро пожаловать". (#6350)
* В диалоговых окнах NVDA, кнопки "OK" и "Отмена" теперь выровнены по правому краю. (#6333)
* Для ввода числовых значений в диалогах настроек NVDA (например поле "Процент смены высоты для заглавных" в диалоге настроек голоса), теперь используются поля со счётчиком, что позволяет изменять значения не только прямым вводом числа, но и клавишами стрелками вверх/вниз. (#6099)
* NVDA теперь читает документы IFrame (документы, встроенные в документы) одинаково во всех web-браузерах. В частности IFrame в Firefox теперь читается как "Фрейм", а не "IФрейм". (#6047)

### Исправления

* Исправлена редкая ошибка появляющаяся при завершении работы NVDA с открытым просмотрщиком речи. (#5050)
* Карты изображений в режиме обзора Mozilla Firefox теперь отображаются как и ожидается. (#6051)
* Нажатие клавиши Enter в диалоговом окне словаря, теперь сохраняет все сделанные изменения и закрывает его. Ранее нажатие Enter ничего не делало. (#6206)
* Сообщения об изменении режимов ввода для метода ввода теперь отображаются на брайлевском дисплее (исходный/буквенно-цифровой ввод, режим полной/частичной формы и т.д.). (#5892, #5893)
* При отключении и последующем немедленном включении дополнения или наоборот, статус дополнения в менеджере дополнений теперь корректно восстанавливается к исходному значению. (#6299)
* В Microsoft Word теперь возможно чтение полей номеров страниц в заголовках. (#6004)
* В диалоге настроек "Произношение символов/пунктуации", указатель мыши теперь можно использовать для перемещения фокуса между списком символов и полем "Замена". (#6312)
* Исправлена ошибка, которая в режиме обзора в Microsoft Word блокирует появление диалога "Список элементов", если в документе есть недействительная гиперссылка. (#5886)
* После закрытия просмотрщика речи через панель задач или по комбинации клавиш alt+f4, статус флажка в меню NVDA теперь отражает фактическую видимость окна. (#6340)
* Команда перезагрузки плагинов больше не вызывает проблемы для автопереключателей профилей конфигурации, новых документов в web-браузерах и просмотрового курсора в режиме экрана. (#2892, #5380)
* На Windows 10, в списке языков в диалоге общих настроек NVDA, такие языки как арагонский теперь отображаются корректно. (#6259)
* Клавиши эмулирующие системную клавиатуру (например кнопка на брайлевском дисплее которая эмулирует нажатие клавиши tab), в режиме справке по вводу и в диалоге "Жесты ввода", теперь представляются на текущем языке интерфейса NVDA. Ранее они всегда были представлены на английском языке. (#6212)
* Изменение языка интерфейса и сообщений NVDA (в диалоге общих настроек), теперь применяется только после перезагрузке NVDA. (#4561)
* Поле "Шаблон" для новых записей в речевом словаре больше невозможно оставить пустым. (#6412)
* Исправлена редкая проблема, делающая непригодными к использованию драйвера некоторых брайлевских дисплеев при сканировании последовательных портов на некоторых системах. (#6462)
* В Microsoft Word, нумерация и маркеры в таблице теперь читаются при перемещении по её ячейкам. (#6446)
* Для команд драйвера брайлевского дисплея Handy Tech, теперь возможно назначать жесты в диалоге "Жесты ввода". (#6461)
* При навигации по таблице в Microsoft Excel, теперь корректно сообщается переход на следующую строку при нажатии основной клавиши Enter или Enter на цифровом блоке. (#6500)
* iTunes больше не зависает время от времени при использовании режима обзора для iTunes Store, Apple Music и т.д. (#6502)
* Исправлены падения в 64-разрядных приложениях основанных на движках Firefox и Chromium. (#6497)
* При включённой многопроцессности в Firefox, режим обзора и текстовые поля редактирования теперь функционируют корректно. (#6380)

### Изменения для разработчиков

* Теперь возможно создавать модули приложений для исполняемых файлов содержащих в своих именах точку (.). В имени модуля точки заменяются на символы подчёркивания (_). (#5323)
* Новый модуль gui.guiHelper включает в себя инструменты для упрощения создания графических интерфейсов на WXPython, в том числе автоматическое управление интервалами. Это улучшает внешний вид и целостность интерфейса, а также облегчает создание нового GUI для незрячих разработчиков. (#6287)

## 2016.3

Основные новшества этого выпуска включают в себя возможность отключения отдельных дополнений в менеджере дополнений; поддержку полей форм в Microsoft Excel; значительные улучшения в чтении цветов; исправления и улучшения относящиеся к некоторым брайлевским дисплеям; а также исправления и улучшения в поддержке Microsoft Word.

### Новое

* Режим обзора в Microsoft Edge и Windows 10 Anniversary Update теперь может быть использован для чтения PDF-документов. (#5740)
* При необходимости, в Microsoft Word теперь может сообщаться зачёркивание и двойное зачёркивание текста. (#5800)
* Заголовок таблицы в Microsoft Word теперь сообщается при его наличии. Если есть описание таблицы, то его можно получить в режиме обзора командой открытия полного описания (NVDA+d). (#5943)
* NVDA теперь сообщает новое положение при перемещении абзацев в Microsoft Word (alt+shift+стрелка вниз и alt+shift+стрелка вверх). (#5945)
* В Microsoft Word, NVDA теперь сообщает междустрочный интервал при использовании команды чтения форматирования, при изменении интервала горячими клавишами Microsoft Word, а также при переходе к тексту с другим интервалом если в диалоге настроек "Форматирование документа" установлен новый флажок "Читать междустрочный интервал". (#2961)
* NVDA в Internet Explorer теперь распознаёт структурные элементы HTML5. (#5591)
* Чтение примечаний (например примечаний в Microsoft Word) теперь можно отключить, сняв новый флажок "Читать примечания" в диалоге настроек "Форматирование документа". (#5108)
* В менеджере дополнений теперь можно отключать отдельные дополнения. (#3090)
* Добавлены дополнительные назначаемые клавиши для брайлевских дисплеев линейки ALVA BC640/680. (#5206)
* Добавлена команда для перемещения брайля к текущему системному фокусу. В настоящее время, только дисплеи линейки ALVA BC640/680 имеют клавишу для этой команды, но при желании она может быть назначена вручную для других дисплеев в диалоге "Жесты ввода". (#5250)
* В Microsoft Excel теперь можно взаимодействовать с полями форм. Перемещение к формам осуществляется через диалог "Список элементов" или с помощью клавиш быстрой навигации в режиме обзора. (#4953)
* В диалоге настроек "Жесты ввода" теперь можно назначить комбинацию горячих клавиш или другой жест на включение и выключение облегчённого режима просмотра. (#6173)

### Изменения

* Вместо использования более субъективных и менее понятных названий цветов, NVDA теперь читает цвета используя более понятный набор из девяти цветовых тонов и трёх оттенков, с вариантами яркости и бледности. (#6029)
* Существующее поведение NVDA+F9 и NVDA+F10 было изменено. Теперь при первом нажатии NVDA+F10, текст выделяется (если выделение возможно). При быстром двойном нажатии NVDA+F10, текст копируется в буфер обмена. (#4636)
* eSpeak NG обновлён до версии Master 11b1a7b от 22 июня 2016 года. (#6037)

### Исправления

* В режиме обзора в Microsoft Word, копирование в буфер обмена теперь сохраняет форматирование копируемого текста. (#5956)
* NVDA теперь корректно сообщает использование собственных горячих клавиш Microsoft Word для навигации по таблице (alt+home, alt+end, alt+pageUp и alt+pageDown) и команд выделения таблицы (к командам навигации добавляется shift). (#5961)
* Объектная навигация NVDA в диалоговых окнах Microsoft Word была значительно улучшена. (#6036)
* В некоторых приложениях, таких как Visual Studio 2015, горячие клавиши (например control+c для копирования) теперь сообщаются, как и ожидается. (#6021)
* Исправлена редкая проблема, когда сканирование последовательных портов на некоторых системах, делает непригодными к использованию некоторые драйвера брайлевских дисплеев. (#6015)
* Улучшено чтение цветов в Microsoft Word, так как теперь учитываются изменения в темах Microsoft Office. (#5997)
* Режим обзора для Microsoft Edge и поддержка поисковых предложений в меню "Пуск", теперь снова доступны в сборках Windows 10 выпущенных после апреля 2016 года. (#5955)
* Улучшено автоматическое чтение заголовка таблицы при работе с объединёнными ячейками в Microsoft Word. (#5926)
* В приложении "Почта" на Windows 10, NVDA теперь корректно читает тело сообщений. (#5635)
* При включённом чтении командных клавиш, такие клавиши как caps lock и num lock больше не произносятся дважды. (#5490)
* NVDA теперь корректно читает диалоги контроля учётных записей (UAC) в Windows 10 Anniversary update. (#5942)
* В Web Conference Plugin (используемом например на out-of-sight.net), NVDA больше не озвучивает линейку прогресса связанную с микрофоном. (#5888)
* Команды поиска следующего или предыдущего вхождения текста в режиме обзора, теперь учитывают регистр искомого текста если первоначальный поиск был с учётом регистра. (#5522)
* NVDA теперь сообщает о некорректных регулярных выражениях при редактировании или добавлении словарных статей. Также NVDA больше не завершает аварийно работу если файл словаря содержит недопустимые регулярные выражения. (#4834)
* NVDA теперь автоматически прекращает использование брайлевского дисплея если не может с ним связаться (например, если он был отключён). (#1555)
* В некоторых случаях немного улучшена производительность фильтрации в диалоге "Список элементов" режима обзора. (#6126)
* Названия фоновых узоров сообщаемых NVDA в Microsoft Excel, теперь соответствуют тем, которые используются в самом Excel (в русском интерфейсе это соответствие было и ранее). (#6092)
* В Windows 10 улучшена поддержка экрана входа в систему, включающая в себя чтение предупреждений и активации касанием поля пароля. (#6010)
* NVDA теперь корректно определяет вторичные кнопки маршрутизации на брайлевских дисплеях линейки ALVA BC640/680. (#5206)
* NVDA теперь снова может читать всплывающие уведомления в последних сборках Windows 10. (#6096)
* NVDA больше не перестаёт в некоторых случаях распознавать нажатия клавиш на Baum совместимых и HumanWare Brailliant B брайлевских дисплеях. (#6035)
* При включённом чтении номеров строк в диалоге "Форматирование документа", сами номера больше не отображаются на брайлевском дисплее. (#5941)
* При режиме озвучивания "выключено", чтение объектов (например чтение системного фокуса по NVDA+tab) теперь как и ожидается, отображается в просмотрщике речи. (#6049)
* Связанные черновики в списке сообщений Outlook 2016 больше не сообщаются. (#6219)
* В Google Chrome и базирующихся на Chrome браузерах, на языке, отличающемся от английского, режим обзора больше не работает во многих документах. (#6249)

### Изменения для разработчиков

* Логирование информации напрямую из свойства, больше не приводит к бесконечной рекурсии. (#6122)

## 2016.2.1

Этот выпуск исправляет аварийное завершение работы в Microsoft Word:

* NVDA больше не вызывает аварийное завершение работы Microsoft Word сразу после его запуска на Windows XP. (#6033)
* Удалена функциональность чтения грамматических ошибок, так как она приводит к аварийному завершению работы в Microsoft Word. (#5954, #5877)

## 2016.2

Основные новшества этого выпуска включают в себя возможность указания орфографических ошибок при наборе текста; поддержку чтения грамматических ошибок в Microsoft Word; а также улучшения и исправления в поддержке Microsoft Office.

### Новое

* Использование быстрой навигации режима обзора в Internet Explorer и других элементах управления MSHTML для перемещения по примечаниям (a и shift+a), теперь также осуществляет переход к вставленному и удалённому тексту. (#5691)
* В Microsoft Excel, NVDA теперь сообщает уровень группы ячеек, а также свёрнута она или развёрнута. (#5690)
* Двойное быстрое нажатие клавиш для чтения форматирования текста (NVDA+f), теперь представляет эту информацию в отдельном окне с режимом обзора для удобного просмотра. (#4908)
* В Microsoft Excel 2010 и более поздних версиях, NVDA теперь сообщает заливку ячеек и градиентную заливку. Автоматическое чтение этой информации управляется флажком "Читать цвета" из диалога настроек "Форматирование документа". (#3683)
* Добавлена новая брайлевская таблица: Койне. (#5393)
* В просмотрщике журнала NVDA, теперь можно сохранить файл журнала с помощью горячих клавиш control+s. (#4532)
* Если чтение орфографических ошибок включено и поддерживается в текущем элементе управления, NVDA будет воспроизводить звук предупреждающий вас об орфографических ошибках сделанных во время набора текста. Эта функция может быть отключена снятием нового флажка "Воспроизводить звук для орфографических ошибок при наборе текста" в диалоге настроек клавиатуры. (#2024)
* В Microsoft Word, NVDA теперь сообщает грамматические ошибки. Эту функцию можно отключить снятием нового флажка "Читать грамматические ошибки" в диалоге настроек форматирования документа. (#5877)

### Изменения

* В режиме обзора, на редактируемых текстовых полях, NVDA теперь обрабатывает Enter на цифровом блоке также, как и основную клавишу Enter. (#5385)
* NVDA по умолчанию теперь использует речевой синтезатор eSpeak NG. (#5651)
* В Microsoft Excel, NVDA больше не игнорирует заголовок столбца для ячейки, когда есть пустая строка между ячейкой и заголовком. (#5396)
* В Microsoft Excel, координаты ячейки теперь объявляются до заголовков, для устранения неоднозначности между заголовками и содержимом ячейки. (#5396)

### Исправления

* При попытке использования быстрой навигации режима обзора для перехода к не поддерживаемому в данном документе элементу, NVDA теперь сообщает, что такое действие не поддерживается, вместо сообщения об отсутствии искомого элемента. (#5691)
* Листы Microsoft Excel содержащие только диаграммы, теперь также отображаются в диалоговом окне "Список элементов". (#5698)
* NVDA больше не сообщает постороннюю информацию при переключении между окнами в Java-приложениях с несколькими окнами, такими как IntelliJ или Android Studio. (#5732)
* В текстовых редакторах на основе Scintilla, таких как Notepad++, при перемещении курсора с помощью брайлевского дисплея, брайлевский вывод теперь обновляется корректно. (#5678)
* В некоторых редких случаях, NVDA больше не завершает аварийно работу при включении брайлевского вывода. (#4457)
* В Microsoft Word, отступ абзаца теперь всегда сообщается в единицах измерения выбранных пользователем (например, в сантиметрах или дюймах). (#5804)
* Многие сообщения NVDA, ранее произносимые только синтезатором, теперь также выводятся и на брайлевский дисплей при его использовании. (#5557)
* В доступных Java-приложениях, теперь объявляется уровень дерева элементов. (#5766)
* Исправлено падение Adobe Flash в Mozilla Firefox в некоторых случаях при работе NVDA. (#5367)
* В Google Chrome и в браузерах на основе Chromium, документы внутри web-диалогов или приложений теперь можно читать в режиме обзора. (#5818)
* В Google Chrome и в браузерах на основе Chromium, теперь можно принудительно переключить NVDA в режим обзора в web-диалогах или приложениях. (#5818)
* В Internet Explorer и других элементах управления MSHTML, перемещение фокуса к некоторым элементам управления (в частности, где используется aria-activedescendant) теперь корректно осуществляет переключение в режим обзора. Это происходит например при переходе к подсказкам в поле адреса при составлении сообщения в Gmail. (#5676)
* В Microsoft Word, NVDA больше не зависает в больших таблицах, когда включено чтение заголовков строк и столбцов. (#5878)
* В Microsoft word, NVDA теперь корректно сообщает текст с уровнем структуры (но не встроенный стиль заголовка) в качестве заголовка. (#5186)
* В режиме обзора в Microsoft Word, команды перемещения в конец или начало контейнера (б и shift+б) теперь работают и для таблиц. (#5883)

### Изменения для разработчиков

* Для сборки C++ компонентов NVDA, теперь используется Microsoft Visual Studio 2015. (#5592)
* Теперь можно представить пользователю текст или HTML сообщение в отдельном окне с режимом обзора, используя функцию ui.browseableMessage. (#4908)
* В руководстве пользователя, когда команда <!-- KC:setting используется для установки общей клавиши для всех раскладок, клавиша теперь может быть помещена после полноширинного двоеточия (：) так же, как и после обычного (:). (#5739) -->

## 2016.1

Основные новшества этого выпуска включают в себя возможность при необходимости уменьшать громкость сторонних звуков; улучшения брайлевского вывода и поддержки брайлевских дисплеев; несколько существенных исправлений в поддержке Microsoft Office; и исправления режима обзора в iTunes.

### Новое

* Добавлены новые брайлевские таблицы: Польская восьмиточечная, Монгольская. (#5537, #5574)
* Теперь можно выключить брайлевский курсор и изменить его форму, используя новые настройки отображения и формы курсора в диалоге настроек брайля. (#5198)
* NVDA теперь может по Bluetooth подключаться к брайлевскому дисплею HIMS Smart Beetle. (#5607)
* NVDA теперь может дополнительно уменьшать громкость сторонних звуков в Windows 8 и выше. Это может быть настроено с помощью опции "Режим приглушения звука" в диалоге настроек синтезатора NVDA или нажатием NVDA+shift+d. (#3830, #5575)
* Добавлена поддержка APH Refreshabraille в режиме HID, а также Baum VarioUltra и Pronto! при подключении через USB. (#5609)
* Добавлена поддержка брайлевских дисплеев HumanWare Brailliant BI/B, когда в качестве протокола выбран OpenBraille. (#5612)

### Изменения

* Флажок "Читать акцентирование" в диалоге настроек "Форматирование документа", теперь по умолчанию снят. (#4920)
* В диалоговом окне "Список элементов" для Microsoft Excel, была изменена клавиша ускоритель радиокнопки "Формулы" на alt+р, чтобы она отличалась от ускорителя поля "Фильтр по". (#5527)
* Liblouis braille translator обновлён до версии 2.6.5. (#5574)
* При перемещении фокуса или просмотрового курсора на текстовые объекты, слово "текст" более не произносится. (#5452)

### Исправления

* В iTunes 12, при загрузке новой страницы в iTunes Store, виртуальный буфер режима обзора теперь обновляется правильно. (#5191)
* В Internet Explorer и других элементах управления MSHTML, при переопределении уровня заголовка для поддержки специальных возможностей, переход по заголовкам определённого уровня с помощью клавиш быстрой навигации теперь работает как и ожидается (в частности, когда aria-level переопределяет уровень тега h). (#5434)
* В Spotify, фокус больше не попадает на "неизвестные" объекты. (#5439)
* При возврате в Spotify из другого приложения, фокус теперь восстанавливается правильно. (#5439)
* При переключении между режимами обзора и редактирования, новый режим теперь сообщается на брайлевском дисплее также, как и с помощью речи. (#5239)
* В некоторых версиях Windows, кнопка "Пуск" больше не читается как список или как выбранный элемент. (#5178)
* Такие фразы как "вставлено" больше не читаются при создании сообщений в Microsoft Outlook. (#5486)
* При использовании брайлевского дисплея и наличии выделенного текста в текущей строке (например при поиске в текстовом редакторе текста, который встречается на той же строке), брайлевский дисплей будет прокручиваться, если это уместно. (#5410)
* При закрытии окна командной строки по alt+f4 в Windows 10, NVDA больше не завершает молча работу. (#5343)
* При изменении типа элементов в списке элементов режима обзора, поле "Фильтр по" теперь очищается. (#5511)
* В приложениях Mozilla, при перемещении мыши в редактируемом тексте, теперь снова читается соответствующие строки, слова и т.д. вместо всего содержимого. (#5535)
* В приложениях Mozilla, при перемещении мыши в редактируемом тексте, чтение больше не останавливается на таких элементах как ссылки внутри слова или читаемые строки. (#2160, #5535)
* Web-сайт shoprite.com в Internet Explorer теперь корректно читается в режиме обзора, вместо произнесения "пусто". (в частности, неправильно сформированные атрибуты lang, теперь обрабатываются корректно). (#5569)
* В Microsoft Word, отслеживаемые изменения, такие как "вставка" больше не сообщаются, когда разметка изменений не отображается. (#5566)
* При фокусировке на кнопке-переключателе, NVDA теперь сообщает изменение её состояния - нажато/не нажато. (#5441)
* Информирование об изменении формы указателя мыши, теперь снова работает как ожидается. (#5595)
* При чтении отступов строк, неразрывные пробелы теперь рассматриваются как обычные пробелы. Ранее это могло вызвать такое объявление как "пробел пробел пробел" вместо "3 пробел". (#5610)
* При закрытии современного списка вариантов метода ввода Microsoft, фокус корректно восстанавливается в композицию ввода или в основной документ. (#4145)
* В Microsoft Office 2013 и более поздних версиях, когда лента отображает только вкладки, элементы на ленте теперь снова читаются, как и ожидается, при активации вкладки. (#5504)
* Исправления и улучшения в привязке и обнаружении жестов на сенсорном экране. (#5652)
* Скольжение на сенсорном экране больше не сообщается в режиме справки по вводу. (#5652)
* В диалоге "Список элементов" Microsoft Excel, больше не возникает ошибки на списке комментариев, если один из комментариев содержится на объединённой ячейке. (#5704)
* В очень редких случаях, NVDA больше не вызывает ошибку при чтении содержимого листа в Microsoft Excel при включённой опции "Читать заголовки строк и столбцов в таблицах". (#5705)
* В Google Chrome, навигация внутри композиции ввода при наборе восточно-азиатских символов, теперь работает как и ожидается. (#4080)
* При поиске Apple Music в iTunes, буфер режима обзора для документа с результатами поиска теперь обновляется должным образом. (#5659)
* В Microsoft Excel, при нажатии shift+f11 для создания нового листа, теперь вместо молчания сообщается ваша новая позиция. (#5689)
* Исправлены проблемы с брайлевским выводом при наборе Корейских символов. (#5640)

### Изменения для разработчиков

* Новый класс audioDucking.AudioDucker предоставляет код который указывает, когда устройству вывода звука следует приглушать фоновые звуки. (#3830)
* Конструктор nvwave.WavePlayer теперь имеет ключевой аргумент wantDucking, который указывает, следует ли при воспроизведении приглушать фоновые звуки. (#3830)
 * Когда этот аргумент имеет значение True (по умолчанию), важно, чтобы WavePlayer.idle вызывался при необходимости.
* Улучшения ввода/вывода для брайлевских дисплеев: (#5609)
 * Потокобезопасные драйвера дисплеев могут объявить себя таковыми с помощью атрибута BrailleDisplayDriver.isThreadSafe. Драйвер должен быть потокобезопасным, чтобы воспользоваться следующими функциями.
 * Данные в потокобезопасных драйверах записываются в фоновом режиме, тем самым улучшая производительность.
 * hwIo.Serial расширяет вызов pyserial при получении данных, вместо опроса драйверов.
 * hwIo.Hid обеспечивает поддержку брайлевских дисплеев взаимодействующих через USB HID.
 * hwPortUtils и hwIo могут дополнительно предоставить подробный журнал отладки, в том числе найденые устройства, а также все полученные и отправленные данные.
* Добавлено несколько новых свойств, доступных с помощью жестов сенсорного экрана: (#5652)
 * Объекты MultitouchTracker теперь содержат свойство childTrackers которое содержит трекер MultiTouchTrackers. Например, двойное касание двумя пальцами имеет дочерние трекеры для двух касаний двумя пальцами. Касания двумя пальцами сами по себе имеют дочерние трекеры для двух касаний.
 * Объекты MultiTouchTracker теперь также содержат свойство rawSingleTouchTracker если трекер был результатом касания одним пальцем, пролистывания или скольжения. SingleTouchTracker позволяет получить доступ к базовому ID пальца, назначенному операционной системой и определить, действительно ли палец находится в контакте на текущий момент времени.
 * TouchInputGestures теперь имеет свойства x и y, устраняя необходимость доступа к трекеру для простых случаев.
 * TouchInputGesturs теперь содержит свойство preheldTracker, который является объектом MultitouchTracker представляющим другие используемые пальцы в то время пока действие выполнялось.
* Два новых жеста сенсорного экрана теперь также могут быть использованы: (#5652)
 * Множественное касание с удержанием (например двойное касание с удержанием)
 * Обобщенный идентификатор со счётчиком убранных пальцев вместо удержания (например hold+hover вместо 1finger_hold+hover).

## 2015.4

Основные новшества этого выпуска включают в себя улучшение производительности в Windows 10; включение NVDA в центр специальных возможностей Windows 8 и более поздних версий; улучшения для Microsoft Excel, такие как получение списка и переименования листов и доступ к заблокированным ячейкам на защищённых листах; и поддержку редактирования форматированного текста в Mozilla Firefox, Google Chrome и Mozilla Thunderbird.

### Новое

* В Windows 8 и более поздних версиях, NVDA теперь присутствует в центре специальных возможностей. (#308)
* При перемещении по ячейкам в Microsoft Excel, изменение форматирования теперь сообщается автоматически, если соответствующие опции включены в диалоге "Форматирование документа". (#4878)
* В диалог настроек "Форматирование документа" был добавлен флажок "Читать акцентирование". Эта опция включённая по умолчанию, позволяет NVDA автоматически читать в документах существующий акцентированный текст. Пока это поддерживается только для тегов em и strong в режиме обзора для Internet Explorer и других элементов управления MSHTML. (#4920)
* При отмеченной опции "Читать ревизии редактора", в режиме обзора для Internet Explorer и других элементов управления MSHTML, теперь сообщается вставленный и удалённый текст. (#4920)
* При просмотре отслеживаемых изменений в списке элементов NVDA для Microsoft Word, больше информации, такой как какие свойства форматирования были изменены, теперь отображается. (#4920)
* В Microsoft Excel просмотр списка и переименование листов теперь можно делать из диалога "Список элементов" (NVDA+f7). (#4630, #4414)
* В диалоге произношения символов/пунктуации теперь можно настроить фактическую передачу символа на синтезатор речи (например для паузы или изменения интонации). (#5234)
* В Microsoft Excel, NVDA теперь читает любые сообщения для ввода установленные автором на ячейках листа. (#5051)
* Поддержка брайлевских дисплеев Baum Pronto! V4 и VarioUltra при подключении через Bluetooth. (#3717)
* Поддержка редактирования форматированного текста в приложениях Mozilla, таких как Google Docs с брайлевской поддержкой в Mozilla Firefox и HTML композиция в Mozilla Thunderbird. (#1668)
* Поддержка редактирования форматированного текста в Google Chrome и браузерах на основе Chromium, такого как Google Docs с брайлевской поддержкой. (#2634)
 * Для этого требуется Chrome версии 47 или выше.
* В режиме обзора в Microsoft Excel, теперь можно переходить к заблокированным ячейкам на защищённых листах. (#4952)

### Изменения

* Флажок "Читать ревизии редактора" в диалоге настроек "Форматирование документа" теперь по умолчанию отмечен. (#4920)
* При перемещении по символам в Microsoft Word с включённой опцией NVDA "Читать ревизии редактора", меньше информации теперь сообщается для отслеживаемых изменений, что делает навигацию более эффективной. Для просмотра дополнительной информации используйте список элементов NVDA. (#4920)
* Обновление liblouis braille translator до версии 2.6.4. (#5341)
* Некоторые символы (включая базовые математические) были перемещены на уровень "некоторые", так что они теперь читаются по умолчанию. (#3799)
* Если синтезатор поддерживает, то в речи перед скобками и дефисом (–) теперь будет пауза. (#3799)
* При выделении текста, выделенный текст теперь сообщается до слова "выделенно", а не после. (#1707)

### Исправления

* Значительно улучшена производительность при навигации по списку сообщений Outlook 2010/2013. (#5268)
* Навигация с использованием некоторых клавиш (таких как смена листов по control+pageUp и control+pageDown) в диаграммах Microsoft Excel теперь работает правильно. (#5336)
* Исправлен внешний вид кнопок в диалоге завершения работы NVDA. (#5325)
* В Windows 8 и более поздних версиях, при включённом автозапуске после входа в систему, NVDA теперь запускается значительно быстрее. (#308)
 * Если автозапуск уже был настроен в предыдущей версии NVDA, то вам следует отключить, а затем заново включить эту функцию в диалоге общих настроек, чтобы изменения вступили в силу. Для этого выполните следующие действия:
  1. Откройте диалог общих настроек.
  1. Снимите флажок "Автозагрузка NVDA после входа в Windows".
  1. Нажмите кнопку OK.
  1. Снова откройте диалог общих настроек.
  1. Отметьте флажок "Автозагрузка NVDA после входа в Windows".
  1. Нажмите кнопку OK.
* Улучшена производительность для UI Automation, включая Проводник и Диспетчер задач. (#5293)
* В режиме обзора для Mozilla Firefox и других основанных на Gecko элементов управления, NVDA теперь корректно переключается в режим редактирования при табуляции в доступный только для чтения элемент ARIA grid. (#5118)
* Если нет объекта, NVDA теперь корректно сообщает "нет предыдущего" вместо "нет следующего" при пролистывании влево на сенсорном экране.
* В диалоге "Жесты ввода" исправлены проблемы при наборе нескольких слов в поле "Фильтр по". (#5426)
* NVDA больше не зависает в некоторых случаях при переподключении через USB к дисплеям линейки HumanWare Brailliant BI/B. (#5406)
* В языках с объединёнными символами, описание символа теперь работает как и ожидается для прописных английских символов. (#5375)
* NVDA больше не должна иногда зависать при приведении к меню Пуск в Windows 10. (#5417)
* В Skype для рабочего стола теперь объявляются уведомления, которые появляются перед исчезновением предыдущего уведомления. (#4841)
* В Skype для рабочего стола 7.12 и выше, уведомления теперь сообщаются корректно. (#5405)
* NVDA теперь корректно сообщает фокус при закрытии контекстного меню в некоторых приложениях, таких как Jart. (#5302)
* В Windows 7 и более поздних версиях, цвет теперь снова объявляется в некоторых приложениях, таких как Wordpad. (#5352)
* При редактировании в Microsoft PowerPoint, нажатие Enter теперь автоматически сообщает введённый текст, такой как маркер или номер. (#5360)

## 2015.3

Основные новшества этого выпуска включают в себя начальную поддержку Windows 10; возможность отключения быстрой навигации в режиме обзора (полезно для некоторых web-приложений); улучшения при работе с Internet Explorer; и исправление искажений текста при его вводе в некоторых приложениях с работающим брайлевским дисплеем.

### Новое

* Существующие орфографические ошибки теперь объявляются в редактируемых полях Internet Explorer и других элементах управления Mshtml. (#4174)
* Теперь большее количество математических символов unicode читаются при наличии их в тексте. (#3805)
* Поисковые предложения на стартовом экране Windows 10 теперь читаются автоматически. (#5049)
* Поддержка брайлевских дисплеев EcoBraille 20, EcoBraille 40, EcoBraille 80 и EcoBraille Plus. (#4078)
* Теперь вы можете в режиме обзора включать и выключать быструю навигацию по клавишам NVDA+shift+space. Когда выключено, клавиши однобуквенной навигации передаются приложению, что полезно для некоторых web-приложений, таких как Gmail, Twitter и Facebook. (#3203)
* Новые брайлевские таблицы: Финский шеститочечный, Ирландский (первая ступень), Ирландский (вторая ступень), Корейский (первая ступень) (2006), Корейский (вторая ступень) (2006). (#5137, #5074, #5097)
* QWERTY клавиатура на брайлевском дисплее Papenmeier BRAILLEX Live Plus теперь поддерживается. (#5181)
* Экспериментальная поддержка web-браузера Microsoft Edge и браузерного движка в Windows 10. (#5212)
* Новый язык: Каннада.

### Изменения

* Обновление liblouis braille translator до версии 2.6.3. (#5137)
* Теперь при попытке установить более раннюю версию NVDA поверх уже установленной, вы будете предупреждены, что это не рекомендуется и NVDA должна быть полностью удалена перед продолжением. (#5037)

### Исправления

* В режиме обзора для Internet Explorer и других элементов управления MSHTML, быстрая навигация по полям форм больше ошибочно не включает презентационные элементы списка. (#4204)
* В Firefox, NVDA больше не читает ARIA содержимое панели вкладок при перемещении в неё фокуса. (#4638)
* В Internet Explorer и других элементах управления MSHTML, табуляция в разделы, статьи или диалоги больше не читает всё содержимое контейнера. (#5021, #5025)
* При использовании брайлевских дисплеев Baum/HumanWare/APH с брайлевской клавиатуры, брайлевский ввод больше не перестаёт работать после нажатия другого типа клавиши на дисплее. (#3541)
* В Windows 10, посторонняя информация больше не читается при нажатии alt+tab или alt+shift+tab для переключения между приложениями. (#5116)
* Набираемый текст больше не искажается при использовании некоторых приложений, таких как Microsoft Outlook с брайлевским дисплеем. (#2953)
* В Internet Explorer и других элементах управления MSHTML, в режиме обзора теперь содержимое читается правильно, когда элемент появляется/изменяется и сразу попадает в фокус. (#5040)
* В Microsoft Word, в режиме обзора, быстрая навигация теперь обновляет брайлевский дисплей и просмотровый курсор как и ожидается. (#4968)
* На брайлевских дисплеях лишние пробелы больше не отображаются между или после индикаторов форматирования и элементов управления. (#5043)
* Когда приложение медленно реагирует и вы переключаетесь на другое приложение, то NVDA в большинстве случаев теперь более отзывчева в этом приложении. (#3831)
* Всплывающие уведомления в Windows 10 теперь читаются как и ожидается. (#5136)
* В некоторых (UI Automation) комбинированных списках, где это не работало ранее, теперь читается значение при его изменении.
* В режиме обзора, в web-браузерах, табуляция к фрейму документа теперь ведёт себя ожидаемо. (#5227)
* Экран блокировки Windows 10 теперь может быть убран с помощью сенсорного экрана. (#5220)
* В Windows 7 и более поздних версиях, при использовании брайлевского дисплея текст больше не искажается при его наборе в некоторых приложениях, таких как Wordpad и Skype. (#4291)
* На экране блокировки Windows 10 больше невозможно чтение содержимого буфера обмена, получение доступа к работающим приложениям с помощью просмотрового курсора, изменение конфигурации NVDA и т.д. (#5269)

### Изменения для разработчиков

* Теперь вы можете посылать необработанный ввод от системной клавиатуры который не был обработан в Windows (например QWERTY клавиатура на брайлевском дисплее) используя новую функцию keyboardHandler.injectRawKeyboardInput. (#4576)
* eventHandler.requestEvents был добавлен для запроса определённых событий, блокируемых по умолчанию; Например показывает события от определённого элемента управления или некоторые события в фоне. (#3831)
* Вместо одного атрибута i18nName, synthDriverHandler.SynthSetting теперь имеет отдельные атрибуты displayNameWithAccelerator и displayName для избежания чтения ускорителя в кольце настроек синтезатора в некоторых языках.
 * Для обеспечения обратной совместимости, в конструкторе, displayName необязателен и если не предусмотрен, то будет получен из displayNameWithAccelerator. Однако, если вы намерены иметь ускоритель для настройки, то оба атрибута должны быть предусмотрены.
 * Атрибут i18nName устарел и может быть удалён в будущих версиях.

## 2015.2

Основные новшества этого выпуска включают в себя возможность чтения диаграмм в Microsoft Excel и поддержку чтения/интерактивной навигации по математическим выражениям.

### Новое

* Перемещаться вперед и назад по предложению в Microsoft Word и Outlook теперь можно при помощи Alt+стрелка вниз и Alt+стрелка вверх соответственно. (#3288)
* Новые брайлевские таблицы для нескольких индийских языков. (#4778)
* В Microsoft Excel, NVDA теперь сообщает, когда ячейка переполнена или её содержимое обрезано. (#3040)
* В Microsoft Excel теперь можно использовать список элементов (NVDA+f7) для получения списка диаграмм, комментариев и формул. (#1987)
* Поддержка чтения диаграмм в Microsoft Excel: Чтобы это использовать, выберите диаграмму через список элементов (NVDA+f7), а затем используйте клавиши стрелки для перемещения между точками данных. (#1987)
* Используя MathPlayer 4 от Design Science, NVDA теперь может читать и интерактивно перемещаться по математическим выражениям в веб-браузерах, приложениях Microsoft Word и PowerPoint. Смотрите раздел "Чтение математических выражений" в руководстве пользователя для получения более подробной информации. (#4673)
* Теперь можно назначить жесты (клавиатурные команды, сенсорные жесты и т.д.) для всех диалогов NVDA и параметров форматирования документа используя диалог "Жесты ввода". (#4898)

### Изменения

* В диалоге "Форматирование документа", были изменены (только для английского языка интерфейса) горячие клавиши для флажков "Читать списки", "Читать ссылки", "Читать номера строк" и "Читать название шрифта". (#4650)
* В диалоге "Мышь", были добавлены горячие клавиши для флажков "Изменяющийся сигнал при перемещении мыши" и "Контроль яркости сигнала перемещения мыши". (#4916)
* Значительно улучшено чтение названий цветов. (#4984)
* Библиотека liblouis braille translator обновлена до версии 2.6.2. (#4777)

### Исправления

* Описания символа теперь обрабатываются правильно для объединённых символов в некоторых индийских языках. (#4582)
* Если флажок "Использовать язык синтезатора для чтения знаков и символов пунктуации" отмечен, то в диалоге "Произношение символов/пунктуации" теперь правильно используется язык текущего голоса. Кроме того, язык, произношение для которого редактируется, указывается в заголовке. (#4930)
* В Internet Explorer и других элементах управления MSHTML, вводимые символы больше не будут ошибочно произноситься в редактируемых комбинированных списках, таких как поисковая строка на главной странице Google. (#4976)
* При выборе цветов в приложениях Microsoft Office, название цвета теперь сообщается. (#3045)
* Датский брайлевский вывод теперь снова работает. (#4986)
* Клавиши PageUp/PageDown теперь снова можно использовать для изменения слайдов в слайд-шоу PowerPoint. (#4850)
* В Skype для рабочего стола 7.2 и познее, оповещения о наборе теперь сообщаются, а проблемы сразу же после перемещения фокуса из окна чата были исправлены. (#4972)
* Исправлены проблемы при вводе некоторых знаков препинания (таких как скобки) в поле "Фильтр по" в диалоге "Жесты ввода". (#5060)
* В Internet Explorer и других элементах управления MSHTML, нажатие клавиши g или shift+g теперь также осуществляет переход по графическим элементам отмечеными, как изображения для целей доступности (то есть ARIA role img). (#5062)

### Изменения для разработчиков

* brailleInput.handler.sendChars(mychar) больше не будет фильтровать символ, если он равен предыдущему символу, проверяя, что клавиша отправлена правильно. (#4139)
* Скрипты изменяющие сенсорные режимы теперь будут учитывать новые метки добавленные в touchHandler.touchModeLabels. (#4699)
* Дополнения могут предоставлять свои собственные реализации математического представления. Смотрите пакет mathPres для получения более подробной информации. (#4509)
* Были реализованы речевые команды для вставки разрывов между словами, изменения высоты, громкости и скорости. Смотрите BreakCommand, PitchCommand, VolumeCommand и RateCommand в модуле speech. (#4674)
 * Существует также speech.PhonemeCommand для вставки определённого произношения, но текущая реализация поддерживает очень ограниченное число фонем.

## 2015.1

Основные новшества этого выпуска включают в себя режим обзора для документов Microsoft Word и Outlook; множество улучшений поддержки Skype для рабочего стола; и значительные исправления для Microsoft Internet Explorer.

### Новое

* Теперь возможно добавлять новые символы в диалоге произношения символов. (#4354)
* В диалоге Жестов ввода, вы можете использовать новое поле "Фильтр по", чтобы показывать только жесты, содержащие определённые слова. (#4458)
* NVDA теперь автоматически сообщает новый текст в mintty. (#4588)
* В диалоге поиска Режима обзора, теперь появилась возможность искать с учётом регистра. (#4584)
* Быстрая навигация (нажатие H для перехода по заголовкам и т.п.) и список элементов (NVDA+f7) теперь доступны в документах Microsoft Word при включении режима обзора по NVDA+space. (#2975)
* Чтение HTML сообщений в Microsoft Outlook 2007 и выше было значительно улучшено автоматическим включением режима обзора для этих сообщений. Если режим обзора не включается в некоторых редких ситуациях, то вы можете включить его нажав NVDA+space. (#2975)
* Заголовки столбцов в таблице Microsoft Word, автоматически объявляются для таблиц, где строка заголовка была явно указана автором в свойствах таблицы Microsoft Word. (#4510) 
 * Однако, для таблиц, где строки были объединены это автоматически работать не будет. В этой ситуации вы всё равно можете установить заголовки столбцов вручную используя NVDA+shift+c.
* В Skype для рабочего стола, уведомления теперь сообщаются. (#4741)
* В Skype для рабочего стола, вы можете теперь читать последние сообщения используя комбинации клавиш от NVDA+control+1 до NVDA+control+0; Например NVDA+control+1 для чтения самого последнего сообщения и NVDA+control+0 для десятого из списка последних. (#3210)
* Во время чата в Skype для рабочего стола, NVDA теперь сообщает, когда собеседник набирает текст. (#3506)
* NVDA теперь можно установить в тихом режиме через командную строку без автоматического запуска после установки. Для этого используйте опцию --install-silent. (#4206)
* Поддержка брайлевских дисплеев Papenmeier BRAILLEX Live 20, BRAILLEX Live и BRAILLEX Live Plus. (#4614)

### Изменения

* В диалоге настроек форматирования документа NVDA, настройка объявлять орфографические ошибки теперь имеет горячую клавишу в английском языке (alt+r). (#793)
* NVDA теперь использует язык синтезатора/голоса для обработки знаков и символов (Включая символы пунктуации), независимо от того, включено автоматическое переключение языков или нет. Чтобы отключить эту функцию и использовать язык интерфейса NVDA, в диалоге настроек голоса снимите новый флажок "Использовать язык синтезатора для чтения знаков и символов пунктуации". (#4210)
* Поддержка синтезатора Newfon удалена. Newfon теперь доступен в виде дополнения NVDA. (#3184)
* Для использования с NVDA теперь требуется Skype 7 для рабочего стола или выше; более ранние версии не поддерживаются. (#4218)
* Загрузка обновлений NVDA теперь более безопасна. (В частности, информация для обновления передаётся через https, а хеш-сумма файла проверяется после его загрузки.) (#4716)
* eSpeak обновлён до версии 1.48.04 (#4325)

### Исправления

* В Microsoft Excel, обрабатывается случай слияния строк и столбцов заголовков ячеек. Например, если A1 и B1 будут объединены, то B2 и B1 будут теперь объявлены как заголовки столбцов A1, вместо отсутствия какой-либо информации. (#4617)
* При редактировании содержимого текстового поля в Microsoft PowerPoint 2003, NVDA будет правильно объявлять содержимое каждой строки. Ранее строки должны были обязательно отличаться на один символ для каждого нового абзаца. (#4619)
* Все диалоги NVDA теперь выровненны по центру экрана, улучшая визуальное представление и удобство использования. (#3148)
* В Skype для рабочего стола, при вводе приветственного сообщения, во время добавления контакта, ввод и перемещение по тексту теперь работают правильно. (#3661)
* При переходе фокуса на новый элемент дерева в Eclipse IDE, если предыдущий элемент был флажком, он больше неправильно не объявляется. (#4586)
* В диалоговом окне проверки орфографии Microsoft Word, следующая ошибка будет автоматически сообщена, когда последняя была изменена или проигнорирована нажатием соответствующей комбинации клавиш. (#1938)
* Текст теперь снова корректно читается в окне терминала Tera Term Pro и документах программы Балаболка. (#4229)
* Фокус теперь корректно возвращается к редактируемому документу при завершении составного ввода текста на Корейском и других восточно-азиатских языках, при редактировании во фрейме в Internet Explorer и других документах MSHTML. (#4045)
* В диалоге Жесты ввода, при выборе раскладки клавиатуры для добавляемой комбинации клавиш, нажатие escape теперь как и ожидается закрывает меню, вместо закрытия диалога. (#3617)
* При удалении дополнения, каталог дополнения теперь корректно удаляется после перезагрузки NVDA. Ранее перезагрузка требовалась дважды. (#3461)
* Исправлены основные проблемы при использовании Skype для рабочего стола версии 7. (#4218)
* Когда вы отправляете сообщение в Skype для рабочего стола, оно больше не читается дважды. (#3616)
* В Skype для рабочего стола, NVDA больше не должна иногда ошибочно читать большой поток сообщений (возможно, даже всю беседу). (#4644)
* Исправлена проблема, когда NVDA сообщая дату/время, в некоторых случаях не учитывала региональные настройки заданные пользователем. (#2987)
* В режиме обзора, бессмысленный текст (иногда несколько строк) больше не отображается для некоторых графических элементов, например таких, которые можно найти в группах Google. (В частности, это происходило с изображениями закодированными в base64). (#4793)
* NVDA больше не должна зависать через несколько секунд после перемещения фокуса из Metro приложения Windows 8, из-за его приостановки. (#4572)
* Aria-atomic атрибут активных областей в Mozilla Firefox теперь учитывается даже тогда, когда сам atomic элемент изменяется. Ранее страдали только дочерние элементы. (#4794)
* Режим обзора будет отображать обновления, а активные области будут объявлятся для документов содержащих встроенные ARIA приложения в Internet Explorer и других элементов управления MSHTML. (#4798)
* Когда текст изменяется или добавляется в активных областях в Internet Explorer и других элементах управления MSHTML где автор указал релевантный текст, то сообщается только изменённый или добавленный текст, а не весь текст содержащийся в элементе. (#4800)
* Содержимое указанное атрибутом aria-labelledby на элементах в Internet Explorer и других элементах MSHTML, теперь корректно заменяется на оригинальное содержание там, где это уместно. (#4575)
* При проверке орфографии в Microsoft Outlook 2013, слова с ошибками теперь сообщаются. (#4848)
* В Internet Explorer и других элементах управления MSHTML, внутреннее содержимое элементов скрывается вместе с их видимостью и больше не отображается в режиме обзора. (#4839, #3776)
* В Internet Explorer и других элементах управления MSHTML, атрибут title полей форм более не имеет приоритета над другими связанными label элементами. (#4491)
* В Internet Explorer и других элементах управления MSHTML, NVDA больше не игнорирует фокусировку элементов из-за атрибута aria-activedescendant. (#4667)

### Изменения для разработчиков

* wxPython обновлён до версии 3.0.2.0. (#3763)
* Python обновлён до версии 2.7.9. (#4715)
* NVDA больше не завершает работу аварийно при перезагрузки после удаления или обновления дополнения, которое импортирует speechDictHandler в своём installTasks модуле. (#4496)

## 2014.4

### Новое

* Новые языки: Колумбийский Испанский, панджабский.
* В диалоге выхода из NVDA Теперь возможно перезагружать NVDA или перезагружать NVDA с отключенными дополнениями. (#4057)
 * также можно запускать NVDA с отключенными дополнениями с помощью параметра командной строки --disable-addons.
* В речевых словарях теперь можно указать, чтобы шаблон соответствовал только целому слову; то есть он не будет обрабатываться, являясь частью слова. (#1704)

### Изменения

* Если вы переместились с объекта на объект внутри режима обзора документа, но  объект, на котором вы находились не был в режиме обзора, этот режим автоматически установится в документе. Ранее это происходило только, если объект навигатора был перенесен в связи с изменением фокуса. (#4369)
* Списки брайлевских дисплеев и синтезаторов в соответствующих диалогах настроек сортируются в алфавитном порядке, заисключением Нет брайля/Нет речи, которые в настоящее время находятся внизу списка. (#2724)
* Библиотека liblouis braille translator обновлена до 2.6.0. (#4434, #3835)
* В режиме обзора, нажимая e и Shift+e, теперь можно ходить по списку внутри полей редактирования со списком. такое поле со списком содержится в последней версии поиска Google. (#4436)
* Левый щелчок мыши по значку NVDA в области уведомлений мыши теперь открывает меню NVDA вместо отсутствия какого-либо действия. (#4459)

### Исправления

* При перемещении фокуса назад в режим обзора документа (например, альт таб в уже открытую веб-страницу) курсор обзора правильно располагается на виртуальной каретке, а не на органе управления в фокусе (например, рядом со ссылкой). (#4369)
* В слайд-шоу PowerPoint, курсор обзора правильно следует за виртуальным курсором. (#4370)
* В Mozilla Firefox и других браузерах на основе Gecko, новое содержание в живой области будет объявлено даже если новое содержимое имеет удобный тип живой области, отличающийся от типа содержимого родительской живой области. Например Содержимое, отмеченое как утвердительное добавляется к живой области отмеченное как вежливое. (#4169).
* В Internet Explorer и других элементах управления MSHTML, документ, содержащийся в другом документе, больше не мешает пользователю получить доступ к части содержимого в некоторых случаях (в частности, фреймов внутри фреймов). (#4418)
* NVDA больше аварийно не завершается в некоторых случаях при попытке использовать брайлевский дисплей Handy Tech. (#3709)
* В Windows Vista, ложный диалог "Точка входа не найдена" больше не отображается в нескольких случаях, например, при запуске NVDA с помощью ярлыка на рабочем столе или с помощью клавиши быстрого доступа. (#4235)
* Были исправлены серьёзные проблемы с редактируемыми текстовыми органами управления в диалогах в последних версиях Eclipse. (#3872)
* В Outlook 2010, перемещение каретки теперь работает, как ожидалось в области полей назначений и планирования встречи. (#4126)
* Внутри живой области, содержимое, обозначенное как не живое (например, aria-live="off") теперь игнорируется правильно. (#4405)
* При сообщении текста поименованной строки состояния, название теперь правильно отделяется от первого слова текста строка состояния. (#4430)
* В полях ввода пароля с включённой опцией озвучивания слов, несколько звёздочек больше бессмысленно не сообщаются, при начале нового слова. (#4402)
* В списке сообщений Microsoft Outlook, больше ничего бессмысленно не объявляется как элементы данных. (#4439)
* При выделении текста в элементе управления редактирования кода в Eclipse IDE, всё выбранное больше не объявляется при  каждом изменении выделения. (#2314)
* Различные версии Eclipse, такие как Spring Tool Suite и версии, включённые в Android Developer Tools bundle, теперь распознаны как Eclipse и обрабатываются соответствующим образом. (#4360, #4454)
* Отслеживание мыши и обзор сенсорного экрана в Internet Explorer и других элементах управления MSHTML (в том числе многих приложений Windows 8.) теперь стали более точными на дисплеях высокого разрешения DPI или когда изменяется размер документа. (#3494) 
* При отслеживании мыши и обзоре сенсорного экрана в Internet Explorer и других элементах управления MSHTML будет объявляться больше меток кнопок. (#4173)
* При использовании дисплея Брайля Papenmeier BRAILLEX с BrxCom, клавиши на дисплее теперь работают, как ожидалось. (#4614)

### Изменения для Разработчиков

* Для множества приложений которые работают из одного хозяйского приложения (например javaw.exe), теперь может быть предоставлен код дополнений для каждого приложения, вместо загрузки общего модуля  для всех приложений. (#4360)
 * Более подробно смотрите документацию кода для appModuleHandler.AppModule.
 * Реализована поддержка javaw.exe.

## 2014.3

### Новое

* Звуки, проигрывающиеся при запуске и завершении NVDA, можно отключить через новую опцию в диалоге Общие настройки. (#834)
* Помощь по дополнениям можетт быть доступна из менеджера дополнений для тех дополнений, которые поддерживают её. (#2694)
* Поддержка Календаря в Microsoft Outlook 2007 и выше, (#2943) включая:
 * Объявление текущего времени при передвижении с помощью стрелок,
 * Индикация если выбранное время находится в любых назначениях,
 * Объявление выбранного назначения нажатием клавиши tab
 * Умная фильтрация даты с тем, чтобы объявлять только дату если новое выбранное время или назначение находится на другом, не на последнем дне.
* Расширенная поддержка входящих и других списков сообщений в Outlook 2010 и выше, (#3834) включая:
 * Возможность отключения заголовков столбцов (от кого, тема и т.д.), переключая ряд вариантов сообщений столбцов и заголовков таблиц в настройках форматирования документов,
 * Возможность использования навигационных команд таблиц (control + стрелки), чтобы двигаться вдоль отдельных столбцов.
* Microsoft word: Если встроенное изображение не имеет альтернативного набора текста, NVDA вместо этого сообщит название изображения, если автор предоставил его. (#4193)
* Microsoft Word: Сообщается отступ абзаца по команде объявления форматирования (NVDA+f) и автоматически при включённых объявлениях отступов абзацев в настройках форматирования документа. (#4165).
* Автоматически сообщается вставляемый текст, такой как новый маркер, номер или отступ табуляции при нажатии enter в редактируемых документах и текстовых полях. (#4185)
* Microsoft Word: Нажатие NVDA + Alt + C сообщит текст комментария, если курсор находится в его пределах. (#3528)
* Улучшена поддержка автоматического чтения заголовка столбца и строки в Microsoft Excel, (#3568) включая:
 * Поддержка определённых областей имён Excel для идентификации заголовка ячейки (совместимо с экранным чтецом Jaws) 
 * Команды выбора заголовка столбца (NVDA+shift+c) и выбора заголовка строки (NVDA+shift+r) теперь сохраняют настройки на листе, поэтому они доступны при следующем открытии листа, и будут доступны в других чтецах экрана, которые поддерживают схему определений диапазона имён.
 * Эти команды могут также теперь быть использованы несколько раз на листе для установки различных заголовков для различных регионов.
* Поддержка автоматического чтения заголовков столбца и строки в Microsoft Word, (#3110) включая:
 * Поддержка закладок MS Word для идентификации заголовков ячеек (совместимо с чтецом экрана Jaws)
 -  Команды выбора заголовка столбца (NVDA+shift+c) и выбора заголовка строки (NVDA+shift+r), при положении на первом заголовке ячейки в таблице позволяют указать NVDA, что эти заголовки должны быть предоставлены автоматически. Настройки хранятся в документе так, чтобы они были доступны  при следующем открытии документа, и будут доступны для других программ чтения с экрана, которые поддерживают схему закладок.
* Microsoft Word: Объявляется расстояние от левого края страницы, когда нажата клавиша tab. (#1353)
* Microsoft Word: обеспечена обратная связь речи и Брайля для большинства доступных горячих клавиш форматирования (полужирный, курсив, подчёркивание, выравнивание и уровень структуры). (#1353)
* Microsoft Excel: Если выбранная ячейка содержит комментарии, они могут быть в настоящее время сообщены по нажатию NVDA+alt+c (#2920)
* Microsoft Excel: Предоставляется специфический NVDA-диалог для изменения комментариев в выбранной ячейке при нажатии Excel-команды shift+f2, которая служит для входа в режим редактирования комментариев. (#2920)
* Microsoft Excel: обратная связь речи и Брайля для ещё большего количества горячих клавиш перемещения и выделения, (#4211) включая:
 * Вертикальное перемещение по страницам (pageUp и pageDown)
 * Горизонтальное перемещение по страницам (alt+pageUp и alt+pageDown)
 * Расширенное выделение (вышеуказанные клавиши с добавлением Shift).
 * Выделить текущую область (control+shift+8)
* Microsoft Excel: сообщается вертикальное и горизонтальное выравнивание для ячеек по команде объявления форматирования (NVDA+f) и автоматически, если включена опция читать выравнивания в настройках форматирования документа. (#4212)
* Microsoft Excel: сообщается стиль ячеек по команде объявления форматирования (NVDA+f) и автоматически, если включена опция читать стиль в настройках форматирования документа. (#4213)
* Microsoft Powerpoint: при перемещении форм вокруг слайдов с помощью клавиш со стрелками, текущее местоположение формы теперь объявляется, (#4214) включая:
 * сообщается расстояние между формой и каждым из направляющих краёв слайда
 * Если обложки форм перекрываются другими обложками форм или формами, то сообщаются перекрываемое расстояние и расстояние до другой формы.
 * Для сообщения этой информации в любое время без перемещения по формам, нажмите команду объявления о расположении (NVDA+delete)
 * При выделении формы, если она перекрывается другой формой, будет предоставляться сообщение состояния о её невидимости.
* Команда объявления о расположении (NVDA+delete) более зависима от конкретных условий в некоторых ситуациях. (#4219):
 * В стандартных полях ввода и режиме обзора, сообщаются позиции курсора в процентах от содержимого и её экранные координаты.
 * На формах в презентациях Powerpoint, сообщается положение формы по отношению к слайду и другим формам.
 * При двойном нажатии этой команды будет производиться старое поведение передачи информации о местоположении для всего элемента управления.
* Новый язык: Каталонский.

### Изменения

* Библиотека liblouis braille translator обновлена до 2.5.4. (#4103)

### Исправления

* В Google Chrome и браузерах на базе Chrome, некоторые куски текста (например, те, которые подчёркнуты) больше не повторяются при составлении объявлений текста оповещения или диалога. (#4066)
* В режиме просмотра в приложениях Mozilla, нажатие клавиши Enter на кнопке и т.д. больше не активирует её  (или активирует неправильный тип управления) в некоторых случаях, таких как кнопки в верхней части Facebook. (#4106)
* больше не объявляется бесполезная информация при навигации в iTunes. (#4128)
* В некоторых списках в iTunes, таких как список музыки, движение к следующему пункту с использованием объектной навигацией теперь работает правильно. (#4129)
* HTML элементы, считая заголовки разметки WAI ARIA, теперь включены в список элементов режима обзора и быстрой навигации для документов Internet Explorer. (#4140)
* В документах  режима обзора, теперь правильно осуществляется перемещение по последовательности страничных ссылок в последних версиях Internet Explorer и сообщается о назначенной позиции. (#4134)
* Microsoft outlook 2010 и выше: улучшен весь доступ к защищенным диалогам, таким как новые профили и диалоги настройки почты. (#4090, #4091, #4095)
* Microsoft outlook: уменьшено бесполезное многословие командных панелей инструментов при навигации по подписаным диалогам. (#4096)
* Microsoft word: при переходе на пустую ячейку в таблице больше неправильно не объявляется о выходе из таблицы. (#4151)
* Microsoft word: Первый символ за концом таблицы (включая символ новой пустой строки) больше неправильно не считается внутри таблицы. (#4152)
* Microsoft Word 2010 диалог проверки орфографических ошибок: Объявляет реально неправильно написанное слово, а не неуместно отмеченное полужирным первое слово. (#3431) 
* В режиме обзора в Internet Explorer и других элементах управления Mshtml, при навигации табуляцией или с помощью одиночных букв, при повторном переходе к полям форм снова сообщается метка во многих случаях, включая особые (в частности, там, где используются элементы HTML меток). (#4170)
* Microsoft Word: Объявления об имеющихся и размещаемых комментариях стали более точными. (#3528)
* Улучшение навигации по некоторым диалогам в продуктах MS Office, таким как Word, Excel и Outlook, больше не объявляются особые управления содержимого панели инструментов, которые не являются полезными для пользователя. (#4198) 
* Области задач, такие как диспетчер буфера обмена или восстановления файлов, больше случайно, мнимо, не получают фокус при открытии приложений, таких как Microsoft Word или Excel, при запуске которых пользователю иногда приходилось  переключаться в сторону и обратно в приложение, чтобы использовать документ или таблицу.  (#4199)
* NVDA БОЛЬШЕ не работает на последних Операционных Системах Windows если язык пользователя Windows установлен в Сербский (Латиница). (#4203)
* Нажатие NumLock во время режима справки по вводу теперь правильно переключает NumLock, а не блокирует клавиатуру и операционную систему, нарушая тем самым синхронизацию в отношении состояния этой клавиши. (#4226)
* В Google Chrome, название документа снова объявляется при переключении вкладок. В NVDA 2014.2 этого не произходило в некоторых случаях. (#4222)
* в Google Chrome и браузерах на базе Chrome, URL документа больше не сообщается, когда объявляется документ. (#4223)
* При запуске проговаривать всё с выбранным синтезатором Нет речи (полезно для автоматизированного тестирования), проговаривать всё сейчас же завершится вместо остановки после первых нескольких строк. (#4225)
* Microsoft Outlook диалог подписи: поле редактирования Подписи теперь доступно, и позволяет получать отслеживания курсора и определение формата. (#3833) 
* Microsoft Word: при чтении последней строки ячейки таблицы, вся ячейка таблицы больше не прочитывается. (#3421)
* Microsoft Word: При чтении первой или последней строки оглавления, всё оглавление больше не прочитывается. (#3421)
* При проговаривании набираемых слов и в некоторых других случаях, слова больше не остаются неправильно разбитыми на метки, такие как гласные и вирама в индийских языках. (#4254)
* теперь правильно обрабатываются числовые редактируемые текстовые поля в GoldWave. (#670)
* Microsoft Word: при перемещении по абзацам с помощью control+стрелки вниз / control+стрелки вверх, больше не нужно нажимать их дважды, если перемещение осуществляется по маркированным или нумерованным спискам. (#3290)

### Изменения для Разработчиков

* NVDA теперь содержит унифицированную поддержку для документации дополнения. Для получения подробной информации, смотрите раздел о документации дополнения в руководстве для разработчиков. (#2694)
* При предоставлении привязок жестов в ScriptableObject через __gestures, теперь можно указать ключевое слово None как скрипт. Это развязывает жест в любых базовых классах. (#4240)
*     Теперь возможно изменить клавиши быстрого вызова, используемые для запуска NVDA в тех локализациях, где нормальный ярлык вызывает проблемы. (#2209)
 * Это сделано с помощью Gettext.
 * Обратите внимание, что текст для опции Создать ярлык на рабочем столе в диалоге установки NVDA, а также сочетания клавиш в руководстве пользователя, должны быть обновлены.

## 2014.2

### Новое

* Объявление о выделении текста теперь доступно в некоторых пользовательских полях редактирования, где используется отображаемая информация. (#770)
* В доступных приложениях Java, теперь объявляется информация о положении радио-кнопок и других элементов управления, представляющих группу. (#3754)
* В доступных приложениях Java, сочетания клавиш для элементов управления теперь объявляются, если они есть. (#3881)
* В режиме обзора теперь сообщаются метки на ориентирах. Они также включены в диалоге списков элементов. (#1195)
* В режиме обзора, помеченые регионы в настоящее время рассматриваются как ориентиры. (#3741)
* В документах Internet Explorer и приложениях, Живые Регионы (часть стандарта W3C ARIA) теперь поддерживаются, что позволяет веб-авторам отмечать особое содержание, которое будет проговариваться автоматически  при его изменении. (#1846)

### Изменения

* При выходе из диалога или приложения в режиме обзора документа, название и тип документа в режиме обзора больше не объявляется. (#4069)

### Исправления

* Стандартное меню системы Windows больше случайно не замолкает в приложениях Java (#3882)
* При копировании текста при просмотре экрана, переходы строк больше не игнорируются. (#3900)
* Бессмысленные пустые объекты больше не сообщаются в некоторых приложениях при изменении фокуса или при использовании объектной навигации с включённым простым обзором. (#3839)
* бПовторно вызываемые блоки сообщений и другие диалоги, произведённые NVDA, теперь способны прервать предыдущую речь, прежде чем объявить диалог.
* В режиме обзора, ярлыки управления, такие как ссылки и кнопки, теперь отрисовываются правильно, где метка была изменена автором в целях специальных возможностей (в частности, с помощью aria-label или арии-labelledby). (#1354)
* В режиме обзора в Internet Explorer, текст, содержащийся внутри элемента отмеченного как презентационный (aria-presentation), больше неуместно не игнорируется. (#4031)
* Теперь снова можно набирать вьетнамский текст с помощью программного обеспечения Unikey. Для этого, снимите флажок Обрабатывать клавиши из других приложений, который добавлен в диалог настроек клавиатуры NVDA. (#4043) 
* В режиме обзора, радио и включаемые элементы меню объявляются как элементы управления, а не просто как интерактивный текст. (#4092)
* NVDA больше неправильно не переключается с режима редактирования в режим обзора, если радио-или включаемый пункт меню находится в фокусе. (#4092)
* в Microsoft PowerPoint с включённым режимом чтения слов при вводе, символы, стёртые клавишей backspace больше не объявляются как часть слова. (#3231)
* В Microsoft Office 2010 диалоги Параметров, помеченные как комбинированные списки, теперь сообщаются правильно. (#4056)
* В режиме обзора в приложениях Mozilla, помимо использования команд быстрой навигации для перехода к следующей или предыдущей кнопке или полю формы, теперь включены переключаемые кнопки, как и ожидалось. (#4098)
* содержимое предупреждений в приложениях Mozilla больше не сообщаются дважды. (#3481)
* в режиме обзора, содержимое и ориентиры уже неуместно не повторяются во время навигации по ним при изменении содержания страницы (например, при перемещении по веб-сайту Facebook и Twitter). (#2199)
* NVDA восстанавливается в ещё большем количестве случаев при переключении из приложений, которые перестают отвечать. (#3825)
* Каретка (точка вставки) снова правильно обновляется при выполнении команды sayAll во время обращения редактируемого текста напрямую к экрану. (#4125)

## 2014.1

### Новое

* Поддержка Microsoft PowerPoint 2013. [Защищённый просмотр не поддерживается]. (#3578)
* В Microsoft Word и Excel, NVDA теперь может читать выбранный символ, который выбран с помощью диалога вставки символов. (#3538)
* Теперь есть возможность выбрать, должно ли  содержание в документах  определяться как интерактивное, с помощью нового параметра в диалоговом окне настроек Форматирование документа. Эта опция включена по умолчанию (предыдущее поведение). (#3556)
* Поддержка подключения брайлевских дисплеев через Bluetooth, работающего при помощи програмного обеспечения Widcomm Bluetooth. (#2418)
* Теперь сообщаются гиперссылки при редактировании текста в PowerPoint. (#3416)
* Находясь в ARIA приложениях или диалогах Интернета, теперь можно принудительно переключать  NVDA в режим обзора по NVDA+пробел, позволяя навигацию по документу в стиле приложения или диалога. (#2023)
* В Outlook Express / Windows Mail / Windows Live Mail, NVDA теперь сообщает, если сообщение содержит вложение или флаг. (#1594)
* Во время навигации по таблицам в доступных приложениях Java, координаты строк и столбцов в настоящее время сообщаются, включая заголовки столбцов и строк, если они существуют. (#3756)

### Изменения

* Для брайлевских дисплеев Papenmeier , переход к команде плоского обзора/фокуса был удалён. Пользователи могут назначить свои собственные клавиши с помощью диалога жестов ввода. (#3652)
* NVDA теперь полагается на Microsoft VC Runtime версии 11, из этого следует, что NVDA больше не может работать на операционных системах старше Windows XP Service Pack 2 или Windows Server 2003 Service Pack 1.
* В уровне пунктуации Некоторые теперь будут проговариваться символы звёздочка (*) и плюс (+). (#3614)
* Обновлён eSpeak до версии 1.48.02, в котором включено множество языковых исправлений и нескольких сбоев. (#3842, #3739)

### Исправления

* При перемещении по ячейкам или их выделении в Microsoft Excel, NVDA больше не должна необоснованно объявлять старую ячейку  вместо новой ячейки при медленном перемещении выделения Microsoft Excel. (#3558)
* NVDA правильно обрабатывает открытие выпадающего списка ячейки в Microsoft Excel через контекстное меню. (#3586)
* Новое содержимое страниц магазина в ITunes 11  теперь отображается правильно в режиме обзора при переходе по ссылке в магазине или при открытии магазина впервые. (#3625)
* В режиме обзора кнопки для просмотра песни в магазине ITunes 11 теперь отображаются с метками. (#3638)
* В режиме обзора в Google Chrome, теперь правильно отрисовываются метки для флажков и радиокнопок. (#1562)
* В Instantbird, NVDA сообщает меньше бесполезной информации при каждом переходе на контакт в их списке. (#2667)
* В режиме обзора в Adobe Reader, теперь отображается правильный текст для кнопок и т.д., где метки были изменены с помощью всплывающих подсказок или других средств. (#3640)
* В режиме обзора в Adobe Reader посторонние графические объекты, содержащие текст "mc-ref", больше не будут отрисовываться. (#3645)
* NVDA больше не сообщает все ячейки в Microsoft Excel, как подчёркнутые в своих сведениях о форматировании. (#3669)
* Больше не отображаются бессмысленные символы в документах в режиме обзора, такие как символы, используемые в частном диапазоне юникода. В некоторых случаях они задерживали показ более полезных меток.  (#2963)
* Больше не возникает неудач при вводе восточноазиатских символов в PuTTY (#3432)
* Навигация в документе после отмены читать всё, больше не приводит к иногда неправильным объявлениям NVDA, что вы оставили поле (например, таблицу) ниже в документе, что читать всё никогда не говорил. (#3688)
* При использовании режима просмотра быстрых команд навигации во время включённого режима беглого чтения в sayAll, NVDA точнее объявляет новое поле (например, теперь проговаривается заголовок, если это заголовок, а не только его текст). (#3689)
* Прыжок в конец или начало содержимого команд быстрой навигации теперь предпочитает беглое чтение во время установки sayAll (то есть они больше не будут отменять текущий sayall). (#3675)
* Имена жестов, перечисленные в диалоге жестов ввода NVDA теперь дружелюбны и локализованы. (#3624)
* NVDA больше не вызывает крах в определённых программах при перемещении мыши над их элементами управления rich edit (TRichEdit). В программу включены Jarte 5.1 и BRfácil. (#3693, #3603, #3581)
* в Internet Explorer и других элементах управления Mshtml, содержимое, например, таблицы помеченные как презентации ARIA, больше не сообщаются пользователю. (#3713)
* в Microsoft Word, NVDA больше неуместно не повторяет информацию о строке и столбце ячейки таблицы на брайлевском дисплее несколько раз. (#3702)
* В языках, которые используют пробел как разделитель групп/тысяч цифр, например, французский и немецкий, цифры из отдельных полей текста больше не произносятся как одельные числа. Это было особенно проблематично для ячеек таблицы, содержащих числа. (#3698)
* Брайль иногда удается обновить, когда системная каретка перемещается в Microsoft Word 2013. (#3784)
* При позиционировании на первом символе заголовка в Microsoft Word, служебный текст заголовка (в том числе уровня) больше не исчезает с брайлевского дисплея. (#3701)
* Когда профиль конфигурации срабатывает для приложения, и происходит выход из этого приложения, NVDA в большинстве случаев удаётся деактивировать профиль. (#3732)
* При азиатском вводе в элементе управления внутри самой NVDA (например, диалог поиска в режиме обзора), теперь не произносится "NVDA", вместо кандидата. (#3726)
* теперь сообщаются вкладки в диалоговом окне параметров Outlook 2013. (#3826)
* Улучшена поддержка живых регионов ARIA в Firefox и в других приложениях Mozilla Gecko:
 * Поддержка обновлений aria-atomic и фильтрация обновлений aria-busy. (#2640)
 * Альтернативный текст (например, атрибут alt или aria-метка) включен, если нет другого полезного текста. (#3329)
 * область живого региона больше не молчит, если она совпадает с перемещением фокуса. (#3777)
* Определенные элементы презентации в Firefox и других приложениях Mozilla Gecko больше неуместно не отображаются в режиме обзора (в частности, когда элемент, обозначенный как aria-презентация, находится также в фокусе). (#3781)
* Улучшена производительность при навигации по документам в Microsoft Word с включённой проверкой орфографических ошибок. (#3785)
* Несколько исправлений в поддержке для доступных приложений Java:
 * первоначально находящийся в фокусе тип управления в фрейме или диалоге, теперь удаётся объявить, если фрейм или диалог выходит на передний план. 
 * Больше не объявляется бесполезная информация о положении радиокнопок (например, 1 из 1). (#3754)
 * Улучшены объявления типов управления JComboBox (больше не говорится html, улучшены объявления состояний открытости и закрытости). (#3755)
 * При сообщении текста диалогов, текст, который был ранее недоступен, теперь включён. (#3757)
 * Изменённые имя, значение или описание типа управления в фокусе теперь объявляются более точно. (#3770)
* Исправлена ошибка в NVDA в Windows 8 при фокусировке на определённых элементах управления RichEdit, содержащих большой объём текста (например просмотрщик журнала NVDA, windbg). (#3867)
* В системах с высокой настройкой дисплея DPI (которое происходит по умолчанию для многих современных экранов), NVDA больше не направляет мыши на неправильное место в некоторых приложениях. (#3758, #3703)
* Исправлена иногда возникающая проблема при обзоре интернета, когда NVDA прекращает правильную работу без перезапуска, даже если он не потерпел крах или не завис. (#3804)
* Брайлевский дисплей Papenmeier теперь можно использовать, даже если дисплей Papenmeier никогда не подключался через USB. (#3712)
* NVDA больше не зависает при выборе старых моделей брайлевских дисплеев Papenmeier BRAILLEX без подключённого дисплея.

### Изменения для Разработчиков

* Модули приложений теперь содержат свойства ProductName и PRODUCTVERSION. Эта информация также теперь включена в Информацию для разработчиков (NVDA+f1).  (#1625)
* В консоли Python, теперь можно нажать клавишу tab для завершения текущего идентификатора. (#433)
 * При существовании нескольких способов, нажмите клавишу Tab второй раз для выбора из списка.

## 2013.3

### Новое

* Поля форм теперь сообщаются в документах Microsoft Word. (#2295)
* NVDA теперь может объявить информацию о ревизии в Microsoft Word, когда отслеживание изменений включено. Обратите внимание, что опция читать ревизии редактора в диалоге форматирования документа настроек NVDA (отключена по умолчанию) также должна быть включена. (#1670)
* Выпадающие списки в Microsoft Excel с 2003 до 2010 теперь объявляются, когда они открыты для навигации по ним. (#3382)
* Новая опция 'Разрешить беглое прочтение в режиме читать всё' в диалоге настроек клавиатуры, допускает  быструю навигацию по документу в режиме обзора и переход между строкой / абзацем командами перемещения, оставаясь при этом в "читать всё". Эта опция по умолчанию отключена. (#2766)
* В настоящее время существует диалог "Жесты ввода", позволяющий выполнять простую настройку жестов ввода (например, клавиши на клавиатуре) для команд NVDA. (#1532)
* Теперь можно создавать различные настройки для различных ситуаций с помощью профилей конфигурации. Профили могут быть активированы вручную или автоматически (например, для конкретного приложения). (#87, #667, #1913)
* В Microsoft Excel ячейки, являющиеся ссылками, теперь объявляются как ссылки. (#3042)
* В Microsoft Excel существующие комментарии в ячейке теперь сообщаются пользователю. (#2921)

### Исправления

* Zend Studio теперь работает так же, как Eclipse. (#3420)
* Изменённое состояние некоторых флажков в диалоге правил для сообщений Microsoft Outlook 2010 теперь сообщается автоматически. (#3063)
* NVDA теперь сообщает состояние закрепления для закреплённых элементов управления, таких как вкладки в Mozilla Firefox. (#3372)
* Теперь есть возможность связывать скрипты с жестами клавиатуры, содержащими  в качестве модификаторов клавиши Alt и/или Windows. Раньше, если бы это было сделано, выполнение скрипта вызвало бы меню Пуск или активировало бы меню. (#3472)
* Выделение текста в режиме обзора документа (например, с помощью control+shift+end) больше не вызывает переключение раскладки клавиатуры в системах с несколькими установлеными раскладками. (#3472)
* Internet Explorer больше не должен терпеть крах или приходить в негодность при закрытии NVDA. (#3397)
* Физическое перемещение и другие события на некоторых новых компьютерах больше не рассматриваются как нарушения нажатий клавиш. Ранее это вызывало умолкание речи и иногда срабатывание команд NVDA. (#3468)
* NVDA теперь ведёт себя как ожидалось в Poedit 1.5.7. Пользователям, использующим более ранние её версии, необходимо будет обновить эту программу. (#3485)
* NVDA теперь может читать защищённые документы в Microsoft Word 2010, не приводя Microsoft Word к краху. (#1686)
* Если при запуске дистрибутивного пакета NVDA задаётся неизвестный ключ командной строки, он больше не вызывает бесконечный цикл диалогов об ошибке. (#3463)
* NVDA теперь в состоянии сообщить альтернативный текст графики и объектов в Microsoft Word, если альтернативный текст содержит кавычки или другие нестандартные символы. (#3579)
* Количество элементов, для определённых горизонтальных списков в режиме обзора теперь правильно. Ранее это мог быть двойной фактический объём. (#2151)
* При нажатии control+a на листе Microsoft Excel, обновлённый выбор будет теперь сообщаться. (#3043)
* NVDA теперь может правильно прочитать XHTML документы в Microsoft Internet Explorer и других видах управления MSHTML. (#3542)
* диалог настройки клавиатуры: Если не была выбрана ни одна клавиша для использования в качестве клавиши-модификатора NVDA, при закрытии диалога пользователю будет показана ошибка. По крайней мере одна клавиша должна быть выбрана для правильного использования NVDA. (#2871)
* В Microsoft Excel объявления NVDA для объединённых и нескольких выделенных ячеек теперь различны. (#3567)
* Курсор режима обзора теперь правильно установлен при выходе из диалогового окна или приложения внутри документа. (#3145)
* Исправлена ошибка, когда драйвер брайлевского дисплея линейки HumanWare Brailliant BI/B не отображался в диалоге настройки брайля в некоторых системах, хотя такой дисплей был подключён через USB.
* NVDA теперь может перейти к просмотру экрана, когда объект навигатора не имеет фактического расположения экрана. В этом случае просмотровый курсор теперь размещён в верхней части экрана. (#3454)
* Fixed an issue which caused the Freedom Scientific braille display driver to fail when the port was set to USB in some circumstances. (#3509, #3662)
* Fixed an issue where keys on Freedom Scientific braille displays weren't detected in some circumstances. (#3401, #3662)

### Изменения для Разработчиков

* Вы можете указать категории, в которых будут отображаться скрипты пользователю, используя атрибут scriptCategory в классах ScriptableObject и атрибут category в методах скрипта. Для подробной информации смотрите документацию по baseObject.ScriptableObject. (#1532)
* Функция config.save устарела и может быть удалена в последующих версиях. Используйте вместо неё config.conf.save. (#667)
* Функция config.validateConfig устарела и может быть удалена в последующих версиях. Дополнения, использующие эту функцию, должны быть перестроены для обеспечения её реализации внутри себя. (#667, #3632)

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
* In Browse mode for MSHTML (e.g. Internet Explorer) and Gecko (e.g. Firefox), the existance of long descriptions are now announced. It's also possible to open the long description in a new window by pressing NVDA+d. (#809)
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
 * See https://www.gnu.org/software/gettext/manual/html_node/Contexts.html#Contexts for more information.
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
 * Inline information such as footnote and endnote numbers, heading levels, the existance of comments, table nesting levels, links, and text color;
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

Список самых заметных новшеств в NVDA2011.2 включает в себя серьезные улучшения в обработке знаков пунктуации и символов, включая настраиваемые уровни произношения пунктуации, возможность изменять названия знаков пунктуации пользователем, фонетические описания символов. А также чтение без пауз в конце строки в режиме непрерывного чтения, улучшения в поддержке ARIA в браузере Internet Explorer, лучшую поддержку PDF-документов XFA/LiveCycle, перехват текста, выводящегося на экран в большем количестве приложений, доступ к информации о форматировании и цвете текста, выводящегося непосредственно на экран. 

### Новое

* Теперь возможно услышать фонетическое описание для любого символа, нажав "просмотреть текущий символ" дважды быстро. Для латинских символов  используется стандартный английский фонетический алфавит. Для языков с иероглифическим письмом, таких как традиционный китайский, для символа обеспечивается одна или больше фраз-примеров. Также, нажав "просмотреть текущее слово" или "просмотреть текущую строку" трижды, можно услышать посимвольное чтение слова/строки с использованием фонетического описания. (#55)
* В режиме плоского просмотра можно увидеть больше текста для приложений типа Mozilla Thunderbird, которые выводят свой текст непосредственно на экран в виде глифов. 
* Теперь возможно выбирать между несколькими уровнями произношения знаков пунктуации и других символов. (#332)
* Когда пунктуационный или любой другой символ повторяется четыре или больше раз, количество повторений произносится вместо повторяющихся символов. (#43)
* Новые брайлевские таблицы: Norwegian 8 dot computer braille, Ethiopic grade 1, Slovene grade 1, Serbian grade 1. (#1456)
* В речи больше нет неестественных пауз в конце каждой строки, когда используется команда "читать все". (#149)
* NVDA теперь будет объявлять, когда что-то отсортировано в браузерах (в соответствии со свойствами aria-sort). (#1500)
* Юникодные символы Брайля теперь будут корректно отображаться на брайлевских дисплеях. (#1505)
* В Internet Explorer и других MSHTML элементах, когда фокус попадает в группу элементов (набор полей), NVDA теперь будет говорить имя группы (короткое описание). (#535)
* В Internet Explorer и других MSHTML элементах теперь учитываются свойства aria-labelledBy и aria-describedBy.
* В Internet Explorer и других MSHTML элементах улучшена поддержка ARIA списка, ячейки таблицы, ползунка и индикатора выполнения.
* Пользователи теперь могут изменять произношение знаков пунктуации и других символов также, как и принадлежность символа к какому-либо уровню. (#271, #1516)
* В Microsoft Excel теперь сообщается имя активного листа, когда переключение между листами происходит по control+pageUp или control+pageDown. (#760)
* Во время перемещения по таблице в Microsoft Word с помощью клавиши tab NVDA будет объявлять текущую ячейку. (#159)
* Теперь вы можете настроить чтение координат ячейки таблицы в диалоге "Форматирование документа". (#719)
* NVDA теперь может узнавать форматирование и цвет текста написанного на экране.
* В списке сообщений Outlook Express/Windows Mail/Windows Live Mail  NVDA будет сообщать о том, что сообщение не прочитано, а также свернуто оно или развернуто, если у вас включены цепочки сообщений. (#868)
* У eSpeak теперь есть настройка экстраускорения, которая утраивает скорость речи.
* Добавлена поддержка элемента календаря, находящегося в диалоге даты и времени, доступного из часов Windows 7. (#1637) 
* Добавлены дополнительные привязки клавиш для брайлевского дисплея MDV Lilli. (#241) 
* Новые языки: болгарский и албанский.

### Изменения

* Чтобы переместить каретку к просмотровому курсору, теперь нужно дважды быстро нажать "переместить фокус к объекту навигатора" (настольная раскладка - NVDA+shift+numpadMinus, раскладка для ноутбука - NVDA+shift+backspace). Это освобождает больше клавиш для дальнейшего использования. (#837)
* Чтобы услышать ASCII и шестнадцатиричное представление символа под просмотровым курсором, теперь нужно нажать "просмотреть текущий символ" трижды, а не дважды, поскольку по двойному нажатию теперь произносится фонетическое описание символа.
* Речевой синтезатор eSpeak обновлен до версии 1.45.03. (#1465)
* Таблицы разметки больше не произносятся в приложениях на основе Mozilla Gecko при перемещениях фокуса в режиме редактирования или за границами документа.
* В Internet Explorer и других MSHTML элементах режим обзора теперь работает для документов внутри ARIA приложений. (#1452)
* Транслятор Брайля liblouis обновлен до версии  2.3.0.
* В режиме обзора при прыжке на элемент с помощью быстрой навигации или попадании на него фокусом теперь объявляется описание элемента, если оно есть.
* Индикаторы выполнения теперь объявляются в режиме обзора.
* Части страницы, у которых атрибут ARIA role установлен как presentation теперь пропускаются в Internet Explorer и других MSHTML элементах.
* Теперь в пользовательском интерфейсе и документации NVDA виртуальный буфер упоминается как режим обзора, поскольку термин "виртуальный буфер" ни о чем не говорит большинству пользователей. (#1509)
* Когда пользователь хочет скопировать свои настройки в системный профиль для использования на экране входа в систему и других защищенных экранах Windows, и эти настройкисодержат сторонние плагины, теперь появляется предупреждение о том, что копирование может представлять угрозу безопасности. (#1426)
* Служба NVDA больше не запускает NVDA на других рабочих столах пользователя.
* На Windows XP и Windows Vista, NVDA больше не использует UI Automation, даже если это доступно через обновление платформы. Хотя использование UI Automation может улучшить доступность некоторых современных приложений, на XP и Vista оно вызывает множество зависаний, аварийных завершений работы и, самое главное, потери производительности. (#1437)
* В приложениях, использующих Mozilla Gecko 2 и более поздние версии (таких как Firefox 4 и выше), документ теперь может быть прочитан в режиме обзора еще до того, как он до конца загрузится. 
* NVDA теперь сообщает состояние контейнера, когда фокус перемещается на элемент внутри него (например, если фокус перемещается внутри документа, который продолжает загружаться, она скажет "занято").
* В пользовательском интерфейсе и документации NVDA больше не используются термины "первый дочерний" и "родительский" по отношению к объектной навигации, поскольку они оказались неудобными для многих пользователей.
* "Свернуто" больше не сообщается для некоторых пунктов меню, у которых есть подменю.
* Скрипт reportCurrentFormatting (NVDA+f) теперь сообщает форматирование на позиции просмотрового курсора, а не системной каретки/ фокуса. Поскольку по умолчанию просмотровый курсор следует за кареткой, большинство людей не заметят разницы. Впрочем это теперь позволяет пользователю узнавать форматирование при перемещении просмотрового курсора например в режиме плоского просмотра.

### Исправления

* Комбинированные списки, раскрытые в режиме обзора, больше не возвращают автоматически в режим обзора, когда режим редактирования был включен принудительно по NVDA+space. (#1386)
* В документах Gecko (например, Firefox) и MSHTML (например, Internet Explorer) NVDA теперь корректно представляет определенный текст на одной и той же строке, который до этого был представлен в виде раздельных строк. (#1378)
* Когда Брайль привязан к просмотру, и объект навигатора перемещается по документу в режиме обзора вручную или из-за изменения фокуса, брайлевский дисплей будет показывать соответствующее содержимое. (#1406, #1407)
* Когда произношение пунктуации полностью выключено, некоторые синтезаторы больше не произносят отдельные символы. (#332)
* Больше не возникает проблемы при загрузке конфигурационного файла для синтезаторов, которые не поддерживают настройку голоса, таких как Audiologic Tts3. (#1347)
* Меню Skype Extras теперь читается корректно. (#648)
* Отмеченный флажок контроля яркости сигнала в диалоге настроек мыши больше не должен вызывать значительных задержек сигнала, когда мышь перемещается по экрану на Windows Vista/Windows 7 с включенным Aero. (#1183)
* Когда NVDA настроена, чтобы использовать раскладку для ноутбука, комбинация клавиш NVDA+delete теперь работает, как задокументировано: сообщает размеры текущего объекта навигатора. (#1498)
* NVDA теперь соответственно учитывает атрибут aria-selected в документах Internet Explorer.
* Теперь при автоматическом переключении из режима обзора в режим редактирования NVDA будет сообщать информацию о контексте фокуса. Например, если фокус оказывается на элементе списка, сначала будет назван список. (#1491)
* В Internet Explorer и других MSHTML элементах, списки ARIA теперь воспринимаются как списки, а не как элементы списка.
* Когда фокус окажется в редакторах только для чтения, NVDA теперь будет говорить, что они только для чтения. (#1436)
* В режиме обзора NVDA теперь корректно ведет себя с редакторами только для чтения.
* В режиме обзора NVDA больше не переходит в режим редактирования, когда aria-activedescendant установлен; например, когда появляется конец списка, что происходит в некоторых элементах с автозаполнением.
* В Adobe Reader, имя элемента теперь сообщается при перемещении фокуса или использовании быстрой навигации в режиме обзора.
* В XFA PDF документах в Adobe Reader кнопки, ссылки и графические элементы теперь отображаются корректно.
* В XFA PDF документах в Adobe Reader все элементы теперь отображаются на отдельных строках. Это изменение было вызвано тем, что большие разделы (иногда даже внутри документа) отображались слитно, что приводило к плохой структурированности этих документов.
* Исправлены проблемы при попадании фокуса в поле редактора или выходе из него в XFA PDF документах Adobe Reader.
* В XFA PDF документах в Adobe Reader теперь сообщаются изменения значения комбинированого списка в фокусе.
* Самоотрисовывающиеся комбинированые списки, такие как, например, выбор цвета в Outlook Express, теперь доступны с NVDA. (#1340)
* В языках, у которых пробел используется в качестве разделителя между числовыми группами, таких как французский и немецкий, числа в разных частях текста больше не произносятся как одно число. Эта проблема была особенно актуальной для чисел в ячейках таблиц. (#555)
* Части страницы, у которых атрибут ARIA role установлен в description, в Internet Explorer и других MSHTML элементах теперь классифицируются, как статичный текст, а не поля редактирования.
* Исправлены разнообразные проблемы, возникающие при нажатии tab, пока фокус на документе в режиме обзора (например, tab неправильно перемещал в строку адреса Internet Explorer). (#720, #1367)
* Теперь, когда во время чтения попадается список, NVDA в английской локализации будет говорить, например, "list with 5 items" вместо "listwith 5 items". (#1515)
* В режиме помощи по вводу жесты будут заносится в лог, даже если скрипты, назначенные на них, не касаются помощи по вводу, например, прокрутка брайлевского дисплея вперед и назад.
* В режиме помощи по вводу, когда клавиша-модификатор зажата на клавиатуре, NVDA больше не будет сообщать ее, если клавиша является модификатором для самой себя, например, NVDA+NVDA.
* В документах Adobe Reader нажатие c или shift+c теперь перемещает по комбинированным спискам.
* Выделенное состояние для выделяемых строк таблиц теперь сообщается точно так же, как и у элементов списка или дерева.
* Элементы в Firefox и других Gecko приложениях теперь могут быть активированы в режиме обзора, даже  если их содержимое является плавающим и уплыло за границы экрана. (#801)
* Вы больше не сможете увидеть диалог настроек NVDA, когда NVDA показывает вам сообщение, поскольку диалог настроек в таком случае нельзя использовать. (#1451)
* В Microsoft Excel больше нет задержки, когда клавиши для перемещения между ячейками или выделения ячеек зажаты или нажаты быстро. 
* Исправлена периодически возникающая критическая ошибка в NVDA service, из-за которой NVDA переставала запускаться на защищенных экранах Windows.
* Исправлена проблема, при которой иногда после изменений пропадал текст, показывающийся на брайлевском дисплее. (#1377)
* Теперь можно читать содержимое и перемещаться по окну загрузок в Internet Explorer 9 с NVDA. (#1280)
* Случайный запуск нескольких копий NVDA в одно и то же время стал невозможным. (#507)
* На медленных системах  NVDA больше не будет показывать свое главное окно на протяжении всего времени запуска. (#726)
* NVDA перестала аварийно завершать работу на Windows xP при запуске WPF приложений. (#1437)
* "Читать все" и "Читать все от просмотрового курсора" теперь работает на текстовых элементах UI automation, которые поддерживают всю требуемую функциональность. Например, теперь вы можете использовать "читать все от просмотрового курсора" в документах XPS Viewer.
* NVDA перестала неправильно классифицировать некоторые элементы списка в диалоге правил сообщений Outlook Express / Windows Live Mail, как флажки. (#576)
* Комбинированные списки больше не читаются так, как-будто у них есть подменю.
* NVDA теперь может читать поля получателя, копия и скрытая копия в  Microsoft Outlook. (#421)
* Исправлена проблема в диалоге голосовых настроек NVDA, при которой иногда не сообщалось значение ползунков после их изменения. (#1411)
* NVDA больше не выдает ошибку, сообщая новую ячейку таблицы Excel после вырезания и вставки. (#1567)
* Исправлена ошибка, при которой NVDA хуже распознавала цвета с каждым новым запросом. 
* В Internet Explorer и других MSHTML элементах теперь можно читать части страниц, чьи плавающие фреймы отмечены атрибутом ARIA role, который установлен в presentation. (#1569)
* В Internet Explorer и других MSHTML элементах исправлена редкая проблема, когда фокус бесконечно прыгал между документом и полем редактора в режиме редактирования. (#1566)
* NVDA теперь автоматически читает диалоги подтверждения в Microsoft Word 2010. (#1538) 
* Теперь правильно сообщается выделение в строках, которые идут после первой, в многострочных редакторах Internet Explorer и других MSHTML элементов. (#1590) 
* Улучшено перемещение по словам во многих случаях, включая режим обзора и элементы редактирования Windows. (#1580)
* Инсталлятор NVDA больше не показывает искаженный текст для версий Windows Vista и Windows 7 с гонгконгской локализацией. (#1596) 
* NVDA теперь загружается с синтезатором Microsoft Speech API version 5, если конфигурация содержит настройки для этого синтезатора, но не содержит настройки для текущего голоса. (#1599)
* В редакторах Internet Explorer и других MSHTML элементов NVDA больше не зависает при включенном Брайле.
* В режиме обзора в Firefox NVDA больше не игнорирует содержимое внутри фокусируемых частей страницы, у которых атрибут ARIA role установлен в presentation.
* В Microsoft Word при включенном Брайле теперь правильно сообщаются строки, которые расположены не на первой странице. (#1603) 
* В Microsoft Word 2003 строки, написанные справа налево, снова отображаются при включенном Брайле. (#627) 
* В Microsoft Word теперь корректно работает "Читать все", когда документ не заканчивается на конце предложения. 
* При открытии сообщения в формате plain text в Windows Live Mail 2011 NVDA будет правильно устанавливать фокус на текст сообщения, что позволит прочитать его. 
* NVDA больше временно не зависает или отказывается говорить в диалогах "Переместить в"/"Скопировать в" в Windows Live Mail. (#574) 
* В Outlook 2010 NVDA теперь корректно отслеживает фокус в списке писем. (#1285)
* Решены некоторые проблемы подключения через USB для брайлевского дисплея MDV Lilli. (#241)
* В Internet explorer и других MSHTML элементах пробелы больше не игнорируются в режиме обзора, как это было иногда раньше (например, после ссылок). 
* В Internet explorer и других MSHTML элементах исчезли некоторые лишние разрывы строк, которые появлялись в режиме обзора. Конкретно, HTML элементы, у которых атрибут стиля был установлен в None, больше не вызывают появление разрывов строк. (#1685) 
* Если NVDA не может запустится, невозможность проиграть стандартный звук критической ошибки больше не приводит к затиранию самого сообщения об ошибке в логе.

### Изменения для разработчиков

* Документация для разработчиков теперь может быть сгенерирована при помощи SCons. Смотрите readme.txt в корне папки с исходными кодами для подробностей, включая связанные зависимости.
* В локализациях теперь можно задавать фонетические описания для символов. Смотрите раздел "Character Descriptions" руководства для разработчиков, чтобы узнать подробнее. (#55)
* В локализациях теперь можно задавать информацию о произношении специфических пунктуационных символов. Смотрите раздел "Symbol Pronunciation" руководства для разработчиков,  чтобы узнать подробнее. (#332)
* Теперь вы можете собирать NVDAHelper с несколькими опциями отладки, используя переменную nvdaHelperDebugFlags SCons. Смотрите readme.txt в корне папки с исходными кодами для подробностей. (#1390)
* Драйвер синтезатора речи теперь получает последовательность текста и речевых команд вместо просто текста и индекса.
 * Это позволяет использовать встраиваемые индексы, изменения параметров синтезатора на лету и т.п.
 * Драйверы должны реализовывать SynthDriver.speak() вместо SynthDriver.speakText() и SynthDriver.speakCharacter().
 * Старые методы будут использованы, если SynthDriver.speak() не реализована, но, поскольку они устарели, это не будет работать в следующем релизе.
* gui.execute() была удалена. Вместо нее следует использовать wx.CallAfter().
* Модуль gui.scriptUI был удален.
 * для диалогов с сообщениями используйте wx.CallAfter(gui.messageBox, ...).
 * Для всех прочих диалогов используйте стандартные wx dialogs.
 * Новая функция gui.runScriptModalDialog() упрощает использование модальных диалогов из скриптов.
* Драйверы синтезаторов речи теперь поддерживают булевые параметры. Смотрите SynthDriverHandler.BooleanSynthSetting.
* SCons теперь понимает переменную certTimestampServer с адресом сервера времени (timestamping server) который будет использован для отпечатки времениэлектронной подписи (authenticode signatures).

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

Список самых заметных нововведений в этой версии включает в себя автоматическое озвучивание нового текста, который выводится в программах mIRC, PuTTY, Tera Term и SecureCRT; поддержка глобальных плагинов; чтение маркированных и нумерованных списков в Microsoft Word; привязка дополнительных клавиш на брайлевских дисплеях к скриптам, включая кнопки передвижения на следующую и предыдущую строку; поддержка некоторых брайлевских дисплеев от Baum, HumanWare и APH без помощи BRLTTY а так же возможность получения информации о цвете текста и фона в некоторых элементах управления, в том числе в текстовых полях IBM Lotus Symphony.

### Новое

* В некоторых элементах управления NVDA теперь может определять цвета. автоматическое сообщение цвета включается в диалоге настроек форматирования документа. Также информацию о цвете можно получить, используя команду сообщения форматирования документа (NVDA+f).
 * Сейчас NVDA определяет цвета в полях редактирования стандарта Iaccessible2 (например, как в приложениях от Mozilla), элементах типа RichEdit (wordpad), и в текстовых полях приложения IBM Lotus Symphony.
* В виртуальных буферах теперь возможно выделять постранично (используя  shift+pageDown и shift+pageUp), а также по параграфам (используя shift+control+downArrow и shift+control+upArrow). (#639)
* NVDA теперь автоматически сообщает появляющийся новый текст в приложениях mIRC, PuTTY, Tera Term и SecureCRT. (#936)
* Пользователи теперь могут добавлять новые сочетания клавиш или заменять существующие для всех скриптов в NVDA при помощи единого файла пользовательских сопоставлений жестов ввода. (#194)
* Поддержка глобальных подключаемых модулей. Глобальные модули дадут возможность добавлять новые функции в NVDA, которые будут доступны во всех приложениях. (#281)
* Теперь NVDA может издавать сигнал, если пользователь вводит букву с зажатой клавишей Shift при активной клавише CapsLock. Это можно выключить, сняв соответствующую галочку в диалоге настроек клавиатуры. (#663)
* Теперь NVDA сообщает о наличии принудительных разрывов страницы при чтении в Microsoft Word. (#758)
* Теперь NVDA читает маркированые и нумерованные списки при перемещении построчно в Microsoft Word. (#208)  
* Теперь в NVDA можно активировать Режим сна для текущего приложения (NVDA+shift+s). Режим сна отключает все функции NVDA в приложении, отдавая все команды ввода непосредственно ему. Это полезно в приложениях, которые имеют свой речевой вывод и/или функцию чтения. Чтобы отключить Режим сна, нажмите эту команду еще раз.
* Добавлена обработка дополнительных клавишь брайлевских дисплеев. См. секцию поддерживаемых брайлевских дисплеев в руководстве пользователя. (#209)
* Для удобства разработчиков, глобальные модули и модули для приложений  теперь можно перезагрузить без перезапуска NVDA. Используйте пункт меню NVDA Сервис>Перезагрузить плагины или комбинацию клавиш NVDA+control+f3. (#544)
* При возврате на уже посещенную страницу NVDA восстанавливает предыдущее положение курсора. Позиция держится в памяти до тех пор, пока вы либо не выйдете из браузера, либо не выгрузите NVDA. (#132)
* Брайлевские дисплеи от Handy Tech теперь можно использовать без установки универсального драйвера Handy Tech. (#854)
* Поддержка некоторых брайлевских дисплеев от Baum, HumanWare и APH. (#937)
* Теперь статусная строка в приложении Media Player Classic Home Cinema распознается.
* Брайлевский дисплей  Freedom Scientific Focus 40 Blue теперь можно использовать, подключая через BlueTooth. (#1345)

### Изменения

* По умолчанию позиция объекта больше не объявляется в тех случаях, где она обычно получалась не коректно, а именно  в большинстве меню, области Выполнения приложений, области уведомлений и т.д. Однако, это можно включить обратно в диалоге настроек представления объектов.
* Клавиатурная справка была переименована в Справку по вводу, чтобы показать, что теперь она охватывает не только клавиатурные комбинации.
* В справке по вводу больше не сообщается расположение скрипта, назначенного комбинации, поскольку это не нужно для пользователя. ОДнако это сохраняется в лог для разработчиков или продвинутых пользователей.
* Когда NVDA определяет, что она "подвисла" в текущем  приложении, то она все еще перехватывает клавиши-модификаторы NVDA, но передает другие клавиши непосредственно  системе. Это предотвращает нежелательное включение CapsLock и т.п. когда пользователь не заметил подвисания (#939)
* При использовании команды пропуска клавиш, все клавиши, включая повторения, будут передаваться в систему до тех пор, пока не будет отпущена последняя клавиша в сочетании.
* Теперь если один из модификаторов нажать дважды быстро и удерживать после второго нажатия, то информация о повторе будет передаваться непосредственно приложению.
* Клавиши регуляции громкости и отключения звука теперь сообщаются в справке по вводу. Это может быть полезно в случае, когда пользователь не знает какие клавиши отвечают за это в системе.
* Горячая клавиша в меню NVDA параметры для настроек просмотрового курсора была изменена с R на C во избежании конфликта с вызовом настроек брайля.

### Исправления

* При добавлении новой словарной статьи в словарь, заголовок окна теперь "Добавить словарную статью", а не "Редактировать словарную статью". (#924)
* В диалоге словаря значения в колонках списка "Регулярное выражение" и "Регистр" теперь отображаются в соответствии с выбранным языком в NVDA, а не на английском.
* В приложении AIM, в деревьях теперь сообщается позиция элемента.
* В настройках голоса значения ползунков теперь увеличиваются по стрелке вверх/страница вверх/Home, а уменьшаются, соответственно, по стрелке вниз/страница вниз/End. Раньше регулировка происходила противоположными клавишами, что не соответствовало кольцу настроек синтезатора. (#221)
* В виртуальных буферах с выключенным экранным представлением лишние пустые строки больше не отображаются.
* Если модификатор NVDA нажат  дважды быстро , и при этом в промежутке была нажата другая клавиша, то второе нажатие модификатора NVDA не передается приложению.
* В режиме справки по вводу, клавиши отвечающие за знаки пунктуации  проговариваются независимо от настроек пунктуации в NVDA. (#977)
* В диалоге настроек клавиатуры, название раскладки теперь отображается соответственно выбранному языку в NVDA, а не на английском. (#558)
* исправлено отображение некоторых элементов в документах Adobe Reader, которые выводились как пустые; Например, как ссылки в содержании руководства пользователя Apple iPhone IOS 4.1.
* Кнопка "Использовать последнюю сохраненную конфигурацию как конфигурацию NVDA на экране входа в систему и других защищенных экранах" в общих настройках NVDA теперь работает, если она была нажата непосредственно после установки NVDA но до вхождения в защищенные экраны или экран входа в Windows. Раньше NVDA сообщала, что конфигурация была успешно скопирована, но обычно это не давало никакого эффекта. (#1194)
* Теперь невозможно открыть два диалога настроек NVDA. Это решает проблему, когда один диалог настроек зависит от другого; Например, когда пользователь вызывает диалог выбора синтезатора, а в это время активен диалог настроек параметров голоса. (#603)
* На операционных системах с включенным UAC, функция использования последней конфигурации как конфигурации NVDA в защищенных экранах больше не вызывает ошибку, если в имени пользователя системы есть пробелы. (#918)
* В Internet Explorer и других элементах управления MSHTML, теперь NVDA отображает URL ссылки, если та не имеет имени. (#633)
* NVDA больше не игнорирует фокус в меню в AOL Instant Messenger 7. (#655)
* Наименование типа ошибки теперь корректно произносится при проверке правописания в Microsoft Word (например, нет в словаре, грамматическая или пунктуационная  ошибка). Раньше это означалось только как грамматическая ошибка. (#883)
* Набор текста в Microsoft Word при использовании брайлевского дисплея больше не должен вводить искаженный текст или вызывать редкие подвисания, если также нажата клавиша приведения курсора. (#1212) Однако, это вызвало проблему в том, что арабский текст теперь не будет отображаться в Word 2003 и ниже  на брайлевском дисплее. (#627)
* При нажатии клавиши Delete в полях редактирования, положение курсора и текст на брайлевском дисплее теперь всегда обновляется, чтобы показать изменения. (#947)
* Изменения динамического содержания страниц в документах Gecko2 (таких, как страницы Firefox 4), в то время как открыто несколько вкладок, теперь должны озвучиваться. Раньше NVDA реагировала только на изменения в первой вкладке. (Mozilla bug 610985)
* NVDA теперь корректно сообщает советы в диалоге проверки правописания в Microsoft Word. (#704)
* В Internet Explorer и других элементах MSHTML, NVDA теперь больше не отображает позиции для ссылоквнутри страницы как пустые ссылки в виртуальном буфере. Теперь они просто невидимы, как это и должно быть. (#1326)
* Объектная навигация возле или в пределах стандартных элементов  группировок Windows теперь работает более корректно и не асимметрична.
* В Firefox и других элементах, построенных на Gecko, NVDA больше не застревает на вложенных фреймах, если таковой загрузится раньше всего главного  документа.
* NVDA теперь объявляет непосредственно следующий символ при удалении клавишей NumpadDelete. (#286)
* на экране входа в Windows XP NVDA снова   сообщает выбранное имя пользователя при изменении выбора.
* Исправлена проблема, возникающая в консольных окнах Windows при включенном чтении номеров строк.
* Список элементов диалога для виртуальных буферов теперь удобен в использовании и для зрячих пользователей. Все элементы управления видимы на экране. (#1321)
* Диалог со списком статей в речевых словарях стал более читабелен для зрячих пользователей. Список теперь достаточного размера, чтобы показать все свои колонки на экране. (#90)
* При использовании брайлевских дисплеев ALVA BC640/BC680 NVDA больше не игнорирует нажатия клавишь на дисплее, находящихся в нажатом состоянии после отпускания других клавишь.
* Adobe Reader X теперь не завершает работу аварийно при переходе фокуса из окна опций документа без тегов в диалог обработки документа. (#1218)
* NVDA теперь переключается на установленный брайлевский дисплей при выполнении команды возврата к сохраненной конфигурации. (#1346)
* Мастер проектов в Visual Studio 2008 снова озвучивается корректно. (#974)
* Исправлена ошибка, из-за которой NVDA совсем не работала в программах, содержащих в названии исполняемого файла символы, не входящие в таблицу ASCII, например русские символы. (#1352)
* При построчном чтении в AkelPad с включенным переносом слов NVDA больше не добавляет первый символ следующей строки в конец текущей.
* В редакторе кода Visual Studio 2005/2008 NVDA больше не произносит весь текст после каждого введенного символа. (#975)
* Исправлена ошибка, когда некоторые брайлевские дисплеи неправильно очищались после завершения работы NVDA или изменения дисплея.
* Позиция первоначального фокуса после запуска NVDA больше не будет произноситься дважды в некоторых случаях. (#1359)

### Изменения для разработчиков

* Для подготовки дерева исходников, создания бинарной сборки, портабельного архива, инсталлятора и т.д. теперь используется SCons. См. файл readme.txt в корне дерева исходников для подробностей.
* Названия клавишь, используемые NVDA (в т.ч. и в файлах сопоставления) были сделаны более дружественными и логичными. Например, upArrow вместо extendedUp и numpadPageUp вместо prior. См. модуль vkCodes для полного списка.
* Любой пользовательский ввод теперь представляется экземпляром класса inputCore.InputGesture. (#601)
 * Каждый источник ввода (input source) наследуется от базового класса InputGesture.
 * Нажатия клавишь на стандартной клавиатуре представлены классом keyboardHandler.KeyboardInputGesture.
 * Нажатия клавишь, колесиков и прочих элементов на брайлевских дисплеях представляются наследниками класса braille.BrailleDisplayGesture. Они реализуются в каждом драйвере брайлевского дисплея.
* Жесты ввода (input gestures) можно сопоставить скриптабельным объектам (ScriptableObject) по средством метода ScriptableObject.BindGesture()  у экземпляра или свойством класса __gestures, которое представляет из себя словарь, сопоставляющий идентификаторы жестов (gesture identifiers) названиям скриптов. См. документацию к baseObject.ScriptableObject. для подробностей.
* Модули приложений больше не имеют файлов сопоставления клавишь (key map files). Вместо этого, все сопоставления должны назначаться в самом модуле.
* Все скрипты теперь принимают аргументом экземпляр класса InputGesture вместо key press.
 * Клавиатурные жесты ввода можно передать операционной системе посредством метода send() экземпляра gesture.
* Для того, чтобы сымитировать произвольное нажатие клавишь, создайте экземпляр KeyboardInputGesture при помощи KeyboardInputGesture.fromName(), а затем используйте его метод send().
* теперь каждая локаль может предоставить файл сопоставления ввода для изменения сочетаний для конкретного языка. (#810)
 * Файлы сопоставления локали необходимо поместить в locale\LANG\gestures.ini, где LANG - код языка.
 * См. документацию к inputCore.GlobalGestureMap для описания формата файла.
* Новые классы поведения объектов NVDA (NVDA object behavior) LiveText и Terminal реализуют поддержку автоматического чтения нового текста. См. эти классы в пакете NVDAObjects.behaviors для более подробной информации.
 * Встраиваемый кКласс (overlay class) NVDAObjects.window.DisplayModelLiveText можно использовать для объектов, которые должны получать текст, написанный на экране.
 * См. модули для приложений mirc и putty для примеров использования.
* Больше нет модуля приложений _default. Модули приложений теперь должны наследоваться от appModuleHandler.AppModule (базового класса для модулей приложений).
* Добавлена поддержка глобальных плагинов (global plugins), которые могут добавлять глобальные скрипты, обрабатыать события объектов NVDA (NVDA object events) и реализовывать встраиваемые классы (overlay classes). (#281) См. документацию к globalPluginHandler.GlobalPlugin для дополнительной информации.
* У объектов класса SynthDriver свойства available* для строковых параметров (напр. availableVoices и availableVariants) теперь типа OrderedDict (упорядоченный словарь), с ключем идентификатором,а не список.
* Конструктор synthDriverHandler.VoiceInfo теперь принимает необязательный аргумент language, который указывает язык голоса.
* Объекты класса SynthDriver теперь должны реализовывать свойство language, которое указывает язык текущего голоса.
 * Реализация в базовом классе возвращает язык, указанный в экземпляре VoiceInfo текущего голоса. Этого достаточно для большинства синтезаторов, у которых каждый голос поддерживает один язык.
* Драйвера брайлевских дисплеев теперь могут поддерживать ввод с дисплея (кнопки, колесика и пр.):
 * Драйвера могут иметь глобальные сопоставления жестов ввода для добавления сопоставлений клавишь со любыми скриптами NVDA.
 * Они также могут реализовывать свои скрипты для поддержки специфических функций для конкретного дисплея.
 * См. документацию к braille.BrailleDisplayDriver для подробностей и код существующих драйверов для примеров.
* Свойство модулей приложений 'selfVoicing' было переименовано в 'sleepMode'.
* События модулей приложений event_appLoseFocus и event_appGainFocus переименованы в event_appModule_loseFocus и event_appModule_gainFocus соответственно, чтобы следовать существующему соглашению о наименовании у перехватчиков деревьев (tree interceptors).
* Все драйверы брайлевских дисплеев теперь должны наследоваться от braille.BrailleDisplayDriver, а не от braille.BrailleDisplayDriverWithCursor.
 * Курсор теперь обрабатывается вне драйвера.
 * Существующие драйверы должны лиш изменить родительский класси переименовать метод _display в display.

## 2010.2

Заметные нововведения этой версии включают значительно упрощенную объектную навигацию; отображение Adobe flash содержимого в виртуальном буфере; доступ ко многим ранее недоступным элементам управления получая выводимый на экран текст; плоский просмотр отображаемого на экране текста; поддержку документов офисного пакета IBM Lotus Symphony; чтение заголовков таблиц в документах Mozilla Firefox; значительно улучшенную пользовательскую документацию.

### Новое

* Значительно упрощена навигация по объектам при помощи просмотрового курсора. Теперь не отображаются объекты, не представляющие интереса для пользователя: Например, объекты, используемые для форматирования, или недоступные объекты.
* В приложениях, использующих Java Access Bridge (включая OpenOffice.org), форматирование теперь может отображаться в виде текстовых элементов управления. (#358, #463)
* При перемещении курсора по ячейкам в Microsoft Excel, корректно озвучивается их содержимое.
* В приложениях, использующих Java Access Bridge, при появлении диалогового окна, теперь озвучивается его содержимое. (#554)
* Теперь содержимое adobe Flash может отображаться в виртуальном буфере. Навигация по объектам и прямое взаимодействие с элементами управления (посредством включения режима форм) по-прежнему поддерживается. (#453)
* Теперь доступны изменяемые элементы управления в приложении Eclipse IDE, включая редактор кодов. Работает в версии Eclipse 3,6 и выше. (#256, #641)
* Теперь, при помощи NVDA можно просматривать большую часть текста, отображаемого на экране. (#40, #643)
 * Это позволяет читать элементы управления, в которых текст не отображается непосредственно нарпрямую. 
 * К таким элементам управления относятся: некоторые пункты меню, отображаемые иконками (например, в меню Открыть с помощью в Windows XP) (#151), поля редактирования в приложениях пакета Windows Live (#200), список ошибок в Outlook Express (#582), панель редактирования текста в программе TextPad (#605), списки в клиенте Eudora, многие контроллеры в программе Australian E-tax и строка формул в Microsoft Excel.
* Поддержка редактора кодов в Microsoft Visual Studio 2005 и 2008. Должен соблюдаться хотя бы стандарт Visual Studio; не распространяется на версии Express. (#457)
* Поддержка документов пакета IBM Lotus Symphony.
* Начальная экспериментальная поддержка браузера Google Chrome. Обратите внимание, что работа над поддержкой этой программы еще далеко не завершена. Работает только с последней Build версией Chrome.
* При нажатии клавиш переключателей (caps lock, num lock и scroll lock) их новый статус теперь отображается на брайлевском дисплее. (#620)
* Всплывающие подсказки теперь отображаются по брайлю в момент их появления. ((#652)
* Добавлен драйвер для брайлевского дисплея MDV Lilli. (#241)
* Теперь произносится новое выделение при выделении всей строки или столбца по горячим клавишам Shift+пробел или Контрол+пробел в Microsoft Excel. (#759)
* Теперь озвучиваются заголовки строк и столбцов в таблицах. Эта опция доступна в настройках форматирования документа.
 * Пока поддерживается в приложениях Mozilla Firefox и Thunderbird. (#361) 
* Введены команды для плоского просмотра (#58)
 * Сочетание клавиш NVDA+numpad7 переключает в режим плоского просмотра, перемещая курсор к текущему объекту. В этом режиме можно просматривать экран (или документ), используя команды просмотра текста. 
 * По команде NVDA+numpad1 просмотровый курсор перемещается внутрь объекта, представленного в виде текста под просмотровым курсором, и позволяет перемещаться по объекту с позиции курсора.
* Текущие пользовательские настройки NVDA могут быть скопированы для использования в защищенных диалогах, таких как диалог входа, или диалог учетной записи пользователя. Чтобы скопировать настройки, нужно нажать кнопку в главном диалоговом окне Параметры. (#730)
* Добавлена поддержка Mozilla Firefox 4.
* Добавлена поддержка Microsoft Internet Explorer 9.

### Изменения

* Команды озвучить объект (NVDA+numpadAdd),следующий объект в потоке ((NVDA+shift+numpad6), и предыдущий файл в потоке (NVDA+shift+numpad4) удалены из-за большого количества сбоев при их выполнении, а также, чтобы освободить сочетания клавиш для других возможных функций.
* Теперь, в диалоговом окне синтезатора, озвучивается только видимое имя синтезатора. Ранее ему предшествовало название драйвера, не имеющее отношения к работе пользователя.
* Находясь внутри встроенного объекта, или виртуального буфера, встроенного в другой буфер (например, flash), теперь, по команде nvda+control+пробел можно выйти из встроенного объекта или виртуального буфера в основной документ. Ранее для этого использовалось сочетание клавиш nvda+пробел. Теперь команда nvda+пробел используется только для переключения между режимом просмотра и режимом форм. 
* Если просмотрщику речи (запускается из меню Инструменты) передан фокус (например, было выполнено нажатие по щелчку) текст не изменится пока не сместится фокус. Это делает выделение текста (например, для копирования) гораздо более простым.
* Окна просмотрщика блогов и консоли Python открываются в развернутом виде.
* Если в рабочей области Microsoft Excel выделено более одной ячейки, озвучивается диапазон выделения, а не только активная ячейка. (#763)
* В диалогах входа в систему, учетной записи и в других защищенных экранах отключено сохранение и изменение настроек.
* Синтезатор речи Espeak обновлен до версии 1.44.03.
* Если NVDA уже запущена, нажатие горящих клавиш control+alt+n приведет к перезапуску NVDA.
* Из диалога настроек мыши удален флажок Произносить текст под курсором. Он заменен флажком Включить слежение мыши, более соответствующим назначению скрипта слежения мыши за экраном (NVDA+m).
* Обновления в режиме раскладки клавиатуры Laptop (ноутбук). Теперь включены все команды настольной раскладки, и они корректно работают на не англоязычных клавиатурах. (#798, #800)
* Серьезное изменение пользовательской документации, включая обновление списка горячих клавиш для раскладки Laptop (ноутбук), а также, синхронизацию списка горячих клавиш с руководством пользователя. (#455)
* Библиотека liblouis braille translator обновлена до версии 2.1.0. Благодаря этому исправлены некоторые ошибки, связанные с отображением китайских брайлевских символов, а также символов, не обозначенных в брайлевских таблицах. (#484, #499)

### Исправления

* В приложении µTorrent, больше не произносится постоянно выделенный элемент в списке торентов, когда открыто меню.
* В приложении µTorrent теперь озвучиваются имена файлов, содержащихся в торенте.
* В приложениях Mozilla теперь правильно определяется пустая таблица или дерево просмотра.
* В приложениях Mozilla теперь корректно озвучивается "не отмечено" для переключаемых элементов управления, например, ячеек таблиц. (#571)
* В приложениях Mozilla текст правильно реализованного aria-диалога больше не игнорируется, а будет озвучиваться при появлении диалога. (#630)
* В Internet Explorer и прочих элементах управления mshtml aria атрибут "уровень" обрабатывается корректно.
* В Internet Explorer и прочих элементах управления MSHTML ARIA роль объекта теперь имеет наибольшй приоритет среди прочей информации о типе, что дает более предсказуемое и корректное поведение.
* Исправлено редкое падение которое могло наблюдаться при передвижении между фреймами в Internet Explorer.
* В документах Microsoft Word теперь снова читается текст, написанный слева на право. (#627)
* Сильно уменьшена задержка, возникающая при озвучивании динамически изменяющегося текста в дос-консолях на 64-битных системах. (#622)
* Если Skype уже запущен на время загрузки NVDA, больше не нужно перезапускать Skype, чтобы включить поддержку вспомогательных технологий. Это касается и других программ, которые проверяют системный флаг чтеца экрана.
* В приложениях Microsoft Office, NVDA больше не падает при активации функции "читать объект на переднем плане" (NVDA+b) или при перемещении между некоторыми элементами панели инструментов. (#616)
* Исправлено некорректное произнесение цифр, которые содержат 0 после разделителя: например 1,023. (#593)
* Adobe Acrobat Pro и Reader 9 больше не падают при закрытии файла и в некоторых других случаях. (#613)
* Выделяемый текст теперь произносится при нажатии клавиш control+a в некоторых редакторах, например Microsoft Word. (#761)
* Исправлена ошибка, приводящая к ненужному выделению текста в элементах управления Scintilla (например - Notepad++), когда NVDA перемещает курсор, как в случае с режимом непрерывного чтения. (#746)
* Снова стал возможным просмотр содержимого ячеек Microsoft Excel просмотровым курсором.
* NVDA снова может читать построчно в некоторых проблемных полях textArea в Internet Explorer 8. (#467)
* Windows Live Messenger 2009 больше не завершает работу сразу, как запускается NVDA. (#677)
* Теперь не обязательно нажимать tab чтобы взаимодействовать с встроенным объектом (таким, как Flash содержимое. (#775)
* В полях Scintilla controls (таких как Notepad++), начало длинных строк больше не обрезается если строка не помещается на экран. так же, эти долгие строки будут корректно отображены на брайле.
* В Loudtalks теперь озвучивается контакт-лист.
* Адрес страницы или "MSAAHTML Registered Handler" больше не произносится при открытии документа Internet Explorer и в прочих элементах управления MSHTML. (#811)
* В деревьях eclipse предыдущий выделенный пункт больше не произносится когда фокус перемещается на новый пункт.
* NVDA теперь работает на системах, когда текущая рабочая директория не входит в список директорий для поиска dll-библиотек (флаг CWDIllegalInDllSearch в реестре установлен в 0xFFFFFFFF). Это не касается большинства пользователей. (#907) 
* При использовании команд передвижения по таблице в Microsoft Word NVDA больше не говорит “edge of table” после “вне таблицы” (#921) 
* Когда достигнута граница таблицы при передвижении по таблице Microsoft Word, NVDA теперь сообщает об этом на языке пользователя, а не всегда на английском (#921) 
* В приложениях Outlook Express, Windows Mail и Windows Live Mail NVDA теперь озвучивает состояние флажков в списках правил (#576) 
* NVDA теперь читает Описание правил почтовых сообщений в Windows Live Mail 2010 

## 2010.1

В этой версии разработчики в основном сконцентрировали внимание на исправлении ошибок и увеличении удобства использования, включая серьезные улучшения в стабильности.

### Новое

* NVDA теперь запускается на системах, к которым не подключены устройства аудиовывода. Разумеется, в этом случае необходимо использовать брайлевский дисплей, либо синтезатор "Silence" (нет речи) с просмотрщиком речи. (#425)
* В диалог настроек форматирования документа добавлен флажок, регулирующий чтение ориентиров в веб-документах. Для соответствия предыдущей версии, поумолчанию этот флажок отмечен.
* Если включена функция "произносить командные клавиши", NVDA теперь произносит названия мультимедийных клавиш при нажатии (например проиграть, остановить, домашняя страница и т.д.) на многих клавиатурах. (#472)
* NVDA теперь произносит слово, которое удаляется нажатием ctrl+backspace в элементах управления, поддерживающих данную функцию. (#491)
* Клавиши стрелок теперь могут использоваться в окне програмы web formator для чтения текста и перемещения по нему. (#452)
* Добавлена поддержка списка записей в адресной книге Microsoft Office Outlook.
* Улучшена поддержка встроенных редактируемых (режим дизайна) документов в Internet Explorer. (#402)
* Новая команда (nvda+shift+numpadMinus) приводит фокус к текущему объекту навигатора.
* Добавлены новые команды для блокирования и разблокирования левой и правой кнопок мыши. Используются при перетаскивании объектов. Shift+numpad Разделить – заблокировать/разблокировать левую кнопку, Shift+numpad умножить – заблокировать/разблокировать правую кнопку мыши. 
* Добавлены новые брайлевские таблицы: German 8 dot computer braille, German grade 2, Finnish 8 dot computer braille, Chinese (Hong Kong, Cantonese), Chinese (Taiwan, Manderin). (#344, #369, #415, #450)
* Во время инсталляции NVDA появилась возможность не создавать ярлык на рабочем столе (соответственно, и сочетание клавиш для быстрого вызова). (#518)
* В 64-битных приложениях NVDA теперь может использовать информацию, предоставляемую технологией IAccessible2. (#479)
* Улучшена поддержка технологии Live regions ("живые области") в приложениях Mozilla. (#246)
* Стала доступной библиотека для управления NVDA из других приложений. Реализованы функции управления речью и вывода сообщений на брайлевский дисплей.
* Теперь озвучиваются информационные сообщения и сообщения об ошибке на экране входа в систему в Windows Vista и Windows 7. (#506)
* Добавлена поддержка интерактивных PDF форм, созданных при помощи Adobe LiveCycle. (#475)
* NVDA теперь может автоматически читать приходящие сообщения в miranda IM. Управляется опцией "читать динамические изменения  содержимого" (NVDA+5). Также, добавлены скрипты для повтора последних трех сообщений (NVDA+control+цифра). (#546)
* Добавлена поддержка текстовых полей ввода в flash-содержимом. (#461)

### Изменения

* Чересчур длинное сообщение клавиатурной справки в главном меню Windows 7 больше не произносится. 
* Дисплейный синтезатор (The Display Synth) заменен на новый "Просмотрщик речи" (Speech Viewer). Чтобы его активировать, выберите Speech Viewer в меню Сервис. Просмотрщик речи может быть использован, независимо от того, каким синтезатором речи вы пользуетесь. (#44)
* Информационные сообщения на брайлевском дисплее теперь пропадают, когда есть новая информация. Ранее, сообщение всегда оставалось на дисплее столько времени, сколько установлено в настройках.
* Настройка привязки брайля к системному курсору, либо к просмотровому курсору (NVDA+ctrl+t) теперь доступна и из диалога настроек брайля. Также, теперь она сохраняется в настройках пользователя.
* Синтезатор Espeak обновлен до версии 1.43.
* Брайлевский транслятор (liblouis Braille translator) обновлен до версии 1.8.0.
* Значительно улучшено чтение при перемещении по символам или словам в виртуальном буфере. Прежде произносилось много лишнего и очень отличалось от чтения при перемещении по строкам. (#490)
* Клавиша "control" теперь просто прерывает реч, а не приостанавливает ее, как это было раньше. Для приостановки/возобновления речи используйте клавишу "shift".
* количество строк и столбцов в таблице теперь не произносится при изменении фокуса.

### Исправления

* Больше не возникает проблем с запуском NVDA в случае, когда UI Automation доступна, но, по какой-то причине, не работает. (#483)
* больше не произносится содержимое всей строки таблицы во время перемещения внутри ячейки в приложениях Mozilla, как это иногда прежде случалось. (#482)
* NVDA теперь не тормозит при раскрытии древовидных элементов, содержащих гигантское количество вложенных веток.
* Перечисляя доступные Sapi 5 голоса, NVDA теперь пытается определить неработающие и исключить их из списка голосов и настроек синтезатора. Ранее, если находился хотя бы один проблемный голос, Sapi 5 драйвер NVDA иногда не запускался.
* В виртуальном буфере теперь произносятся горячие клавиши элементов в соответствии с настройкой  диалога представления объектов. (#486)
* В виртуальном буфере больше не озвучиваются координаты строки/столбца для заголовков ячеек, если отключено озвучивание таблиц. 
* В виртуальном буфере корректно читаются координаты строки/столбца, если вы вышли из таблицы и вернулись в ту же ячейку, не просматривая перед этим других ячеек; например, нажав стрелку вверх, а затем вернуться стрелкой вниз на первую ячейку таблицы. (#378)
* Пустые строки в документах Microsoft Word и в элементах управления MSHTML теперь корректно отображаются на брайлевском дисплее. Раньше, вместо текущей строки, отображалось текущее предложение. (#420)
* Множественные исправления безопасности при работе NVDA с экраном входа в систему и другими защищенными экранами. (#515)
* Положение курсора теперь корректно обновляется при непрерывном чтении в стандартных полях редактирования Windows и документах Microsoft Word в ситуациях, когда курсор выходит за нижнюю границу экрана. (#418)
* В виртуальном буфере больше не отображается текст для изображений внутри ссылок и элементов, активируемых по щелчку мыши, который помечен авторами страницы как не относящийся к программе экранного доступа. (#423)
* Исправления в раскладке клавиатуры для ноутбуков (laptop keyboard layout) (#517)
* Если брайль привязан к просмотровому курсору, курсор теперь корректно перемещается по тексту ДОС консолей. 
* В главном окне программы “TeamTalk3” и "TeamTalk4 classic” больше не произносится значение индикатора уровня громкости, при каждом его обновлении. Так же, теперь корректно озвучиваются специальные символы в окне входящих сообщений этой программы.
* В меню "пуск" Windows 7 NVDA больше не читает пункты дважды. (#474)
* При активации внутристраничной ссылки в Firefox 3.6, курсор корректно перемещается к нужному месту страницы.
* Устранена ошибка, приводящая к тому, что некоторый текст  в PDF документах не отображался.
* Устранена ошибка в произношении некоторых чисел, разделенных дефисом, например 500-1000. (#547)
* Устранена ошибка, приводящая к зависанию Internet Explorer в  Windows XP при работе с флажками на странице Windows Update. (#477)
* При использовании встроенного синтезатора espeak  одновременное проигрывание речи и тоновых сигналов больше не приводит в особых случаях к зависаниям на некоторых системах. Такое могло произойти, на пример, при копировании больших объемов данных в проводнике windows.
* NVDA не сообщает  о состоянии "занято" (обновление или перезагрузка страницы) для документов в firefox, которые в данный момент не видны на экране. Это также приводило к нежелательному чтению статусной строки активного приложения.
* При переключении раскладки клавиатуры (control+shift или alt+shift) на речь и брайль выводится полное имя  раскладки. Раньше эта информация выводилась только на синтезатор и альтернативные раскладки (на пример "Dvorak") вобще не произносились.
* Если чтение таблиц отключено, табличная информация больше не произносится при изменении фокуса.
* Некоторые проблемные стандартные деревья в 64 битных приложениях (На пример содержание  в Microsoft HTML Help) теперь доступны. (#473)
* Fixed some problems with logging of messages containing non-ASCII characters. This could cause spurious errors in some cases on non-English systems. (#581)
* Информация в диалоге "о программе" теперь отображается на языке пользователя, а не только на английском, как это было ранее. (#586)
* Problems are no longer encountered when using the synthesiser settings ring after the voice is changed to one which has less settings than the previous voice.
* In Skype 4.2, contact names are no longer spoken twice in the contact list.
* Fixed some potentially major memory leaks in the GUI and in virtual buffers. (#590, #591)
* Work around a nasty bug in some SAPI 4 synthesisers which was causing frequent errors and crashes in NVDA. (#597)

## 2009.1

Основные новинки этой версии: поддержка 64-битных операционных систем; значительное улучшение работы в Internet Explorer и Adobe Reader; поддержка Windows 7; обработка защищенных рабочих столов Windows: экран входа в систему, диалог контроля учетных записей, экран смены пользователя; доступность Adobe Flash и Sun Java элементов на web-страницах. Также внесено несколько существенных изменений, делающих "NVDA" ещё более стабильной и удобной в использовании.

### Новое

* Официальная поддержка 64-битных операционных систем Windows! (#309)
* добавлен  драйвер для синтезатора "Newfon". Обратите внимание, требуется специальная версия синтезатора "Newfon". (#206)
* в виртуальных буферах, режим редактирования и режим обзора озвучиваются сигналами, а не речью. Включено по умолчанию. Можно изменить настройку через диалог "Виртуальные Буферы. (#244)
* NVDA больше не прерывает речь во время изменения уровня громкости при использовании соответствующих команд, что дает пользователю возможность сразу слышать новую настройку. (#287)
* полностью переработана поддержка "Microsoft Internet Explorer" и "Adobe Acrobat". Поддержка стандартизована с компонентами core, используемыми для "Mozilla Gecko", теперь, быстрая обработка страниц, большое количество навигационных команд,  (список ссылок, выделение текста, автоматический переход между режимами обзора и редактирования) и поддержка Брайля доступна в этих документах.
* улучшена поддержка диалога настройки даты и времени (Windows Vista Date / Time properties dialog).
* улучшена поддержка для нового стиля главного меню (XP/Vista start menu), теперь, правильно озвучивается информация уровня.
* В диалог настроек мыши добавлен параметр, позволяющий изменять уровень озвучивания текста при перемещении указателя мыши. Доступны следующие варианты: абзац, строка, слово, символ.
* Теперь озвучиваются орфографические ошибки в в Microsoft Word.
* Поддерживается проверка орфографии в Microsoft Word 2007. Частичная поддержка проверки орфографии в более ранних версиях Microsoft Word.
* Улучшена поддержка Windows Live Mail. Теперь можно просматривать сообщения в текстовом формате, также доступно создание сообщения в форматах "Обычный текст" и "HTML"
* В Windows Vista, если пользователь переместился на защищенный рабочий стол (из-за того, что появился диалог смены пользователя, либо было нажато сочетание ctrl+alt+delete), NVDA сообщит о перемещении на защищенный рабочий стол.
* "NVDA" теперь озвучивает текст под курсором в консоли DOS Windows.
* Поддержка технологии автоматизации пользовательского интерфейса (UI Automation), которая появилась в windows 7, а также другие улучшения для работы с новой операционной системой.
* Добавлена возможность автоматического запуска "NVDA" при старте Windows. Настройка доступна в диалоге общих настроек.
* "NVDA" теперь может читать защищенные экраны, такие какэкран входа в систему, ctrl+alt+delete, диалог контроля учетных записей, экран смены пользователя в Windows XP и более ранних версиях. Параметр озвучивания экрана входа в систему находится в основных настройках "NVDA".
* Добавлен драйвер для брайлевских дисплеев Optelec ALVA BC6.
* Нажимая n и Shift+n, находясь в веб-документе, можно перемещаться вперед и назад по тексту, пропуская группы ссылок.
* При просмотре веб-документа теперь озвучиваются ориентиры. Для перемещения вперед и назад по ориентирам нажимайте d и shift+d соответственно.
* Список ссылок, доступный при просмотре веб-документа, теперь заменен на список элементов. Здесь отображаются ссылки, заголовки и ориентиры. Заголовки и ориентиры расположены иерархически. (n363)
* В новом списке элементов имеется поле "Фильтровать по", позволяющее отфильтровывать определенные элементы, включая введенный текст. (#173)
* Портабельные версии "NVDA" теперь обращаются к пользовательским настройкам, сохраняемым в папке ‘userConfig’, находящейся внутри папки "NVDA", что позволяет сохранять пользовательские настройки отдельно от настроек программы, как это реализовано в инсталляционных версиях.
* Custom app modules, braille display drivers and synth drivers can now be stored in the user's configuration  directory. (#337)
* Начальная обработка веб-страниц теперь происходит в фоновом режиме, что дает пользователю возможность продолжать взаимодействовать с системой. Если процесс загрузки затягивается больше, чем на секунду, пользователь будет об этом проинформирован. 
* Если "NVDA" определяет собственное зависание по какой-либо причине, она перестает перехватывать нажатия клавиш, давая пользователю больше возможностей по восстановлению системы. 
* Добавлена возможность перетаскивания объектов (Aria drag and drop) в Mozilla Gecko.
* При перемещении внутри виртуального буфера теперь озвучивается заголовок текущего документа, текущая строка, или выделенный текст. Это дает возможность перемещаться по веб-странице, как по обычному документу. (#210)
* добавилась возможность взаимодействия с встроеными объектами, такими как flash-содержимое Sun Java, . Для передачи фокуса объекту нажмите на нем “энтер”(как для полей ввода и прочих элементов форм). Если объект доступен, то вы сможете взаимодействовать с ним как с простым приложением (Нажимайте таб для перемещения по окну). Для возвращения в в буфер к просмотру страницы нажмите NVDA+space. (#431)
* Добавлены горячие клавиши o, shift+o для перемещения к следующему/предыдущему встроенному объекту соответственно.
* Теперь NVDA имеет полный доступ к приложениям, которые запущены с правами администратора в Windows Vista и Windows 7. Работает только в официальных установленых версиях. Не работает в тестовых зборках и в портабельных копиях NVDA 

### Изменения

* NVDA больше не озвучивает "NVDA готов" во время запуска.
* Звуки по загрузке и выгрузке NVDA, теперь, воспроизводятся через звуковое устройство, на которое выводится речь NVDA, вместо воспроизведения через устройство "Windows", выбранное по умолчанию. (#164)
* Улучшено озвучивание строки состояния. Теперь NVDA может озвучивать изменения как речью, так и при помощи речи и сигналов одновременно.
* Теперь, при попадании в фокус,  не озвучиваются такие настраиваемые элементы управления, как панель, приложение, фрейм,если только они не являются безымянными. 
* По команде "копировать размеченный текст в буфер обмена" (NVDA+f10) теперь копируется текст от начала фрагмента до текущей позиции просмотрового курсора, включая символ под курсором. Это позволяет копировать последний символ строки, что ранее было невозможно. (#430)
* Удален скрипт местоположения объекта (ctrl+NVDA+numpad5). Эта комбинация клавиш не работала на некоторых клавиатурах, и скрипт оказался не слишком востребованным.
* Скрипт, озвучивающий размеры текущего объекта, переназначен на сочетание клавиш NVDA+numpadDelete. Старая комбинация не работала на некоторых клавиатурах. Вместо координат объекта, теперь произносятся его ширина и высота.
* Улучшена работа NVDA (особенно на нетбуках) в ситуациях, когда воспроизводится ряд частых сигналов: например, при быстром перемещении мыши с включенным озвучиванием координат. (#396)
* Звук ошибки NVDA больше не будет проигрываться в релиз кандидатах и финальных версиях. Запись ошибок в журнал по прежнему ведется 

### Исправления

* При запуске NVDA из 8.3 dos пути, но программа установлена в папку по длинному пути (Например, "progra~1" вместо "program files") NVDA правильно определит это и, соответственно, загрузит пользовательские настройки.
* Чтение заголовка окна на переднем плане по команде "NVDA+t", теперь, корректно работает и в меню.
* На Брайлевском дисплее больше не отображается излишняя информация, например, при фокусе на не размеченной области.
* Больше не озвучивается излишняя информацияпри смене фокуса в "Java" или "Lotus". 	
* Поддержка поля ввода поискового запроса в справке (Windows Help (CHM) viewer). До устранения бага невозможно было прочитать текущее введенное слово, поскольку оно постоянно менялось.
*  Правильно озвучивается нумерация страниц в Microsoft Word.
* Улучшено взаимодействие с диалоговыми окнами Microsoft Word (диалог выбора шрифта). По контроллерам теперь можно перемещаться клавишами стрелок.
* Улучшена поддержка консолей DOS. конкретно: Теперь читается содержимое консолей, которые раньше виделись как пустые. "NVDA" больше не прерывается при нажатии ctrl+break.
* В Windows Vista и предыдущих версиях, если, при завершении инсталляции выбрано "Запустить NVDA, она запустится с обычными правами пользователя.
* При произнесении набираемого текста правильно обрабатывается клавиша Backspace. (#306)
* Больше не произносится "Главное меню" вместо некоторых контекстных меню в проводнике. (#257)
* Корректно обрабатываются маркеры в Mozilla gecko. (#156)
* Больше автоматически не перемещается фокус в поля редактирования, в которых, при изменении фокуса, обновляется текст. (#220)
* Теперь NVDA будет пробовать возобновить собственную работоспособность в некоторых ситуациях, которые до этого приводили к полному зависанию. На самодиагностику и восстановление в отдельных случаях может уйти до 10 секунд.
* Если языком "NVDA" выбран язык системы по умолчанию, То используется язык, установленный в качестве основного в региональных настройках Windows. (#353)
* NVDA теперь определяет контроллеры в AIM 7.
* NVDA больше не вылетает при выполнении команды "Пропуск клавиши". Ранее, если клавиша была нажата и удерживалась, NVDA зависала, и ее приходилось перезапускать. (#413)
* Больше не игнорируется панель задач, когда на нее перемещается курсор. Такое часто случалось при выходе из приложений. “NVDA" не сообщала о том, что фокус изменился.
* В приложениях, использующих Java Access Bridge (включая OpenOffice.org) NVDA теперь правильно сообщает о включении/отключении нумерации строк.
* Корректно обрабатывается команда копирования размеченного фрагмента (NVDA+f10), в случаях, когда курсор находится перед маркером, отмечающим начало фрагмента. Ранее, в подобных ситуациях возникали проблемы, в частности, зависания при работе в Блокноте. 
* Больше самопроизвольно не изменяются громкость и высота тембра синтезатора eSpeak, что раньше наблюдалось, если в тексте встречался управляющий символ 0x1. (#437)
* По команде "произнести выделенный текст" (NVDA+shift+стрелка вверх), в тех объектах, где выделение текста не поддерживается, NVDA теперь сообщает о том, что выделенного текста нет.
* Исправлена ошибка, приводившая к зависанию NVDA при нажатии клавиши enter на какой-либо кнопке в Миранде (Miranda-Aim). (#440)
* Исправлена обработка текущей строки, или выделенного текста при чтении по буквам, либо копировании объекта навигатора. 
* Реализован обход ошибки в windows, из-за которой в ссылках, которые можно найти в диалогах “свойства папки” и других диалогах проводника и Internet Explorer к тексту ссылки добавлялся мусор (#451) 
* Исправлена команда произнесения даты и времени (NVDA+f12). В некоторых локалях дата произносилась не до конца. (#471)
* Fixed the issue where the system screen reader flag was sometimes inappropriately cleared after interacting with secure Windows screens. This could cause problems in applications which check the screen reader flag, including Skype, Adobe Reader and Jart. (#462)
* In an Internet Explorer 6 combo box, the active item is now reported when it is changed. (#342)

## 0.6p3

### Новое

* Поскольку для "NVDA" недоступна строка формулы в Microsoft Excel, создано специальное диалоговое окно для NVDA, которое появляется, когда пользователь нажимает f2 на ячейке.
* Поддержка форматирования в элементах управления стандарта IAccessible2 text, включая приложения Mozilla
* Где возможно, озвучиваются грамматические ошибки. Параметр доступен из диалога настроек форматирования документа.
* Добавилась настройка, изменяющая озвучивание строк состояния. Сигнал может издаваться при изменении всех, или только видимых строк состояния. При желании, "NVDA" можно настроить на проговаривание каждых 10%.
* Теперь определяются ссылки в  элементах управления richedit.
* В большинстве редактируемых элементов управления курсор мыши теперь можно перемещать на символ, находящийся под просмотровым курсором. Прежде, он перемещался только к центру элемента управления.
* В виртуальных буферах, при помощи просмотрового курсора, теперь можно читать текст непосредственно самого буфера, а не только текст, находящийся внутри объекта навигатора, часто неинформативный для пользователя. Это значит, что по виртуальному буферу можно перемещаться иерархически, используя объектную навигацию, и просмотровый курсор будет следовать за курсором навигатора.
* Handle some additional states on Java controls.
* If the title command (NVDA+t) is pressed twice, it spells the title. If pressed thrice, it is copied to  the clipboard.
* Keyboard help now reads the names of modifier keys when pressed alone.
* Key names announced by keyboard help are now translatable.
* Added support for the recognized text field in SiRecognizer. (#198)
* Support for braille displays!
* Added a command (NVDA+c) to report the text on the Windows clipboard. (#193)
* In virtualBuffers, if NVDA automatically switches to focus mode, you can use the escape key to switch back  to browse mode. NVDA+space can still also be used.
* In virtual buffers, when the focus changes or the caret is moved, NVDA can automatically switch to focus  mode or browse mode as appropriate for the control under the caret. This is configured from the Virtual Buffers  dialog. (#157)
* Rewritten SAPI4 synthesizer driver which replaces the sapi4serotek and sapi4activeVoice drivers and should fix the problems encountered with these drivers.
* The NVDA application now includes a manifest, which means that it no longer runs in compatibility mode in Windows Vista.
* The configuration file and speech dictionaries are now saved in the user's application data directory if NVDA was installed using the installer. This is necessary for Windows Vista and also allows multiple users to have  individual NVDA configurations.
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
* added croatian translation by Mario Percinic and Hrvoje Katic - Added galician translation by Juan C. buno 
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

* В NVDA теперь есть встроенный синтезатор eSpeak, разработанный Джонатаном Даддингтоном. Он очень отзывчив и лёгок, и поддерживает множество языков. Синтезаторы Sapi по-прежнему можно использовать, но eSpeak будет использоваться по умолчанию. eSpeak не требует установки специального программного обеспечения, поэтому его можно использовать с NVDA на любом компьютере, на USB-накопителе или где угодно. Для получения дополнительной информации об eSpeak или поиска других версий перейдите по ссылке https://espeak.sourceforge.net/.
 * eSpeak не требует установки специального программного обеспечения, поэтому его можно использовать с NVDA на любом компьютере, на USB-накопителе или где угодно. 
 * Для получения дополнительной информации об eSpeak или поиска других версий перейдите по ссылке https://espeak.sourceforge.net/.
* Исправлена ошибка, из-за которой при нажатии кнопки delete в редактируемых панелях Internet Explorer / Outlook Express объявлялся неправильный символ.
* Добавлена поддержка большего количества полей редактирования в Skype.
* Виртуальные буферы загружаются только тогда, когда фокус находится на окне, которое необходимо загрузить. Это устраняет некоторые проблемы при включении панели предварительного просмотра в Outlook Express.
* Добавлены аргументы командной строки для NVDA:
 * -m, --minimal: не воспроизводить звуки запуска/завершения и не показывать интерфейс при запуске, если он установлен.
 * -q, --quit: выйти из любого другого уже запущенного экземпляра NVDA и затем завершить работу.
 * -s, --stderr-file fileName: указать, куда NVDA должна помещать невыловленные ошибки и исключения
 * -d, --debug-file fileName: указать, куда NVDA должна помещать отладочные сообщения
 * -c, --config-file: указать альтернативный файл конфигурации
 * -h, -help: вывести справочное сообщение со списком аргументов командной строки
* Исправлена ошибка, при которой знаки препинания при включённой функции проговаривания набранных символов не переводились на соответствующий язык при использовании языка, отличного от английского.
* Добавлен словацкий язык благодаря Петеру Вагнеру 
* Добавлены диалог настроек виртуального буфера и диалог настроек форматирования документа, от Питера Вагнера.
* Добавлен перевод на французский язык благодаря Michel Such 
* Добавлен скрипт для включения и выключения звукового сигнала индекаторов выполнения (insert+u). Внесено Питером Вагнером.
* Увеличено количество сообщений в NVDA, которые можно переводить на другие языки. Это касается и описаний скриптов в справке по клавиатуре.
* Добавлен диалог поиска в virtualBuffers (Internet Explorer и Firefox). Нажатие control+f на странице вызывает диалог, в котором вы можете ввести текст для поиска. Нажатие клавиши Enter запустит поиск этого текста и поместит курсор virtualBuffer на эту строку. Нажатие f3 приведёт к поиску следующего вхождения текста.
* Когда включена функция проговаривания набранных символов, теперь должно проговариваться больше символов. Технически, теперь могут быть озвучены символы ascii от 32 до 255.
* Переименованы некоторые типы элементов управления для лучшей читаемости. Редактируемый текст теперь редактор, контур теперь дерево, а кнопка теперь кнопка.
* При перемещении клавишами-стрелками на элементы списка или древовидного представления тип элемента управления (элемент списка, элемент древовидного представления) больше не произносится, чтобы ускорить навигацию.
* "Has Popup" (чтобы указать, что в меню есть подменю) теперь произносится как "подменю".
* Если в некоторых языках для ввода специального символа используются клавиши control и alt (или altGR), NVDA теперь будет произносить эти символы, когда включена функция "Произносить набранные символы".
* Исправлены некоторые проблемы с просмотром статических текстовых элементов управления.
* Добавлен перевод для традиционного китайского языка, спасибо Коселл Као.
* Перестроена важная часть кода NVDA, которая теперь должна исправить многие проблемы с пользовательским интерфейсом NVDA (включая диалоги настроек).
* Добавлена поддержка Sapi4 в NVDA. В настоящее время существует два драйвера sapi4, один основан на коде, предоставленном Serotek Corporation, а другой использует интерфейс ActiveVoice.ActiveVoice com Interface. У обоих этих драйверов есть проблемы, посмотрите, какой из них вам больше подходит.
* Теперь при попытке запустить новую копию NVDA, в то время как старая копия всё ещё запущена, новая копия будет просто завершена. Это устраняет серьёзную проблему, когда запуск нескольких копий NVDA делал вашу систему непригодной для использования.
* Изменено название пользовательского интерфейса NVDA с NVDA Interface на NVDA. 
* Исправлена ошибка в Outlook Express, когда нажатие backspace в начале редактируемого сообщения приводило к ошибке.
* Добавлен патч от Rui Batista, добавляющий скрипт для сообщения о текущем состоянии батареи на ноутбуках (insert+shift+b).
* Добавлен драйвер синтезатора под названием Silence (Нет речи). Это драйвер синтезатора, который ничего не говорит, позволяя NVDA всегда оставаться беззвучной. В конечном итоге это можно будет использовать вместе с поддержкой шрифта Брайля, когда он у нас появится.
* Добавлена настройка capitalPitchChange (Процент изменения высоты для заглавных) для синтезаторов благодаря J.J. Meddaugh
* Добавлен патч от J.J. Meddaugh, который делает скрипт переключения объектов отчета под мышью более похожим на другие скрипты переключения (говорит вкл/выкл, а не изменяет все утверждение).
* Добавлен испанский перевод (es), предоставленный Juan C. buo.
* Добавлен файл венгерского языка от Tamas Gczy.
* Добавлен файл португальского языка от Rui Batista.
* Изменение голоса в диалоге настроек голоса теперь устанавливает ползунки скорости, высоты тона и громкости на новые значения в соответствии с синтезатором, а не заставляет синтезатор быть настроенным на старые значения. Это устраняет проблемы, когда синтезатор типа eloquence или viavoice кажется говорящим с гораздо большей скоростью, чем все остальные синтезаторы.
* Исправлена ошибка, при которой в окне консоли Dos либо речь останавливалась, либо NVDA полностью выходила из строя.
* При наличии поддержки определённого языка NVDA теперь автоматически отображает интерфейс и произносит сообщения на том языке, который установлен в Windows. Язык по-прежнему можно выбрать вручную в диалоге настроек пользовательского интерфейса.
* Добавлен скрипт 'Чтение динамических изменений содержимого' (insert+5). Этот скри6пт устанавливает, должен ли новый текст или другие динамические изменения автоматически объявляться. Пока это работает только в Dos-консоли Windows.
* Добавлен скрипт 'Привязка просмотрового курсора к каретке' (insert+6). Этот скрипт устанавливает, должен ли курсор обзора автоматически перемещаться при перемещении системной каретки. Это полезно в окнах консоли Dos при попытке прочитать информацию, когда экран обновляется.
* Добавлен скрипт 'Привязка навигатора к фокусу' (insert+7). Он переключает, будет ли объект навигатора перемещаться на объект в фокусе при его изменении.
* Добавлена документация, переведённая на разные языки. На данный момент есть французский, испанский и финский.
* Удалена часть документации разработчика из бинарного дистрибутива NVDA, теперь она есть только в исходной версии.
* Исправлена возможная ошибка в Windows Live Messenger и MSN Messenger, когда перемещение по списку контактов при помощи стрелок вверх-вниз приводило к ошибкам.
* Новые сообщения теперь автоматически озвучиваются при общении в Windows Live Messenger. (пока работает только в английской версии)
* Окно истории в беседе Windows Live Messenger теперь можно читать с помощью клавиш-стрелок. (Пока работает только в английской версии) 
* Добавлен скрипт 'Пропуск клавиши' (insert+f2). При нажатии этого сочитания клавиш следующая нажатая клавиша будет передана Windows. Это полезно, если вам нужно нажать определённую клавишу в приложении, но NVDA использует эту клавишу для чего-то другого.
* NVDA больше не зависает более чем на минуту при открытии очень больших документов в MS Word.
* Исправлена ошибка, из-за которой при перемещении из таблицы в MS Word и последующем перемещении обратно текущие номера строк/столбцов не отображались, если перемещение происходило точно в ту же ячейку.
* При запуске NVDA с несуществующим или неработающим синтезатором вместо него будет загружен синтезатор sapi5, а если sapi5 не работает, то речь будет настроена на тишину.
* Скрипты увеличения и уменьшения скорости больше не могут поднимать скорость выше 100 или ниже 0.
* Если при выборе языка в диалоге настроек пользовательского интерфейса произошла ошибка, то в окне сообщения пользователь узнает об этом.
* NVDA теперь спрашивает, следует ли сохранить конфигурацию и перезапустить, если пользователь только что изменил язык в диалоге настроек пользовательского интерфейса. NVDA должна быть перезапущена, чтобы изменение языка полностью вступило в силу.
* Если синтезатор не может быть загружен, при его выборе в диалоге синтезатора появляется сообщение, предупреждающее пользователя об этом.
* При первой загрузке синтезатора NVDA позволяет синтезатору выбрать наиболее подходящие параметры голоса, темпа и высоты тона, а не заставляет его использовать параметры по умолчанию, которые он считает подходящими. Это устраняет проблему, когда при первой загрузке синтезаторы Eloquence и Viavoice sapi4 начинали говорить слишком быстро.
