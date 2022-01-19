commit af202bc82647806d962e6b1bb634f2498aa69757 (HEAD -> master, origin/master, origin/HEAD)
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Tue Jan 18 17:20:43 2022 +0300

    ru:
    classic::
      > добавлена поддержка декларативного интерфейса(DeclarativeInput,DeclarativeEndpointPath,DeclarativeOutput,RenderDeclarativeDocument)
      > python setup.py добавлен RPATH ORIGIN
      > запись версии драйвера в таблицы
    classic_java:
      > добавлена поддержка декларативного интерфейса(DeclarativeInput,DeclarativeEndpointPath,DeclarativeOutput,RenderDeclarativeDocument)
    console_test:
      > исправлена отмена документа в команде state-reset
      > поправлена загрузка шрифта
      > new command: cf-write псевдоним для put-font
      > new command: cf-reset сбрасывает пользовательский шрифт
      > new command: cf-sha256sum-kkt получить sha256sum из ККТ
      > new command: cf-sha256sum-spf посчитает sha256sum для spf файла
      > new command: cf-sort-spf отсортирует глифы внутри spf файла и выдаст сортированный spf на стандартный вывод
    cppbase_test:
      > добавлены тесты
    qclassic_fr_drv_ng:
      > добавлена поддержка декларативного интерфейса(DeclarativeInput,DeclarativeEndpointPath,DeclarativeOutput,RenderDeclarativeDocument)
    
    en:
    classic::
      > declarative api added
      > python setup.py add current directory to library runpath(RPATH ORIGIN)
      > write driver version info to tables
    classic_java:
      > declarative api added
    console_test:
      > fix document cancellation in state-reset command
      > fix spf handling
      > new command: cf-write alias for put-font
      > new command: cf-reset reset custom font
      > new command: cf-sha256sum-kkt get custom font sha256sum from device
      > new command: cf-sha256sum-spf get spf file sha256sum
      > new command: cf-sort-spf read spf font from file, sort glyphs by code and write sorted spf to stdout
    cppbase_test:
      > update tests
    qclassic_fr_drv_ng:
      > declarative api added



commit 7779d97cc2cf3498c25595b7437088a5df477508
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Wed Oct 13 15:22:21 2021 +0300

    en:
    clasic:
      > fix WaitForPrintingTimeout Get/Set for C wrapper
    
    ru:
    classic:
      > исправлено свойство WaitForPrintingTimeout для C обертки


commit 99a69a4fe0fce39d5e47ddc5973ae9411ff31f0e
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Mon Oct 11 19:30:21 2021 +0300

    en:
    cppbase:
      > fix per command timeout
    
    ru:
    cppbase:
      > исправлен специфичный для команды таймаут

commit 417531a8df74b5a05aab1d2f46daefebe8af09da
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Wed Sep 29 14:53:10 2021 +0300

    en:
    classic:
      > fixed WaitForPrintig error report for #WaitForPrintingTimeout expired case
    cppbase:
      > error codes synchronized with DrvFR driver
    
    ru:
    classic:
      > поправлена возвращаемая ошибка WaitForPrintig в случае истченеия #WaitForPrintingTimeout
    cppbase:
      > синхронизированы коды ошибок с Драйвер ФР под Windows

commit 53f21d5b84a3fc7b8e4997353986aaaf58f1a92d
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Thu Sep 23 03:55:16 2021 +0300

    en:
    classic:
      > WaitForPrintingTimeout added
    
    ru:
    classic:
      > добавлено свойство WaitForPrintingTimeout - глобальный таймаут для метода WaitForPrinting

commit 962f5af3073d88d5ef3ecfcafef9c057f234514f
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Tue Sep 21 16:11:56 2021 +0300

    en:
    cppbase:
      > fix FF3F: https://github.com/shtrih-m/fr_drv_ng/issues/155
    console_test:
      > add fs-calculation-report command
    
    ru:
    cppbase:
      > поправлен разбор ответа на команду FF3F("Запрос количества ФД на которые нет квитанции": https://github.com/shtrih-m/fr_drv_ng/issues/155
    console_test:
      > добавлена команда: сформировать отчет о состоянии расчетов: fs-calculation-report


commit e904e8f43db91dfda19c449d905e2b7ab06461a1
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Mon Sep 13 10:38:25 2021 +0300

    en:
    classic:
      > update java wrapper
    
    ru:
    classic:
      > обновлена java обертка


commit c836ac18eb8e29326beefec69565aaaaa421cdc4
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Tue Sep 7 04:47:58 2021 +0300

    en:
    classic:
      > add FNSendUserAttribute
      > implemented FNOpenCheckCorrection
    
    ru:
    classic:
      > добавлен метод FNSendUserAttribute
      > добавлена реализация метода FNOpenCheckCorrection

commit a1e5decebc1b65ddec807b2bd590afd870e2a436
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Thu Aug 26 17:35:04 2021 +0300

    en:
    console_test:
      > font command
      > print command
    
    ru:
    console_test:
      > команда получения параметров шрифта
      > команда печати строки

commit a11ab039fe0de098793390a8c33ae57d8062a462
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Tue Aug 24 18:30:32 2021 +0300

    en:
    classic:
      > FNFindDocument FFD 1.2 support.
    cppbase:
      > fixed FF0A "FN find document" response for FFD 1.2
    
    ru:
    classic:
      > приведен метод FNFindDocument в соответствии с ФФД 1.2.
    cppbase:
      > исправлена обработка ответа на команду FF0A "Найти документ по номеру" для ФФД 1.2.

commit 97e6fc1eedc9d7a32b9769cc7ef065a5477f1c6e
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Tue Aug 24 04:33:28 2021 +0300

    en:
    classic:
      > FFD 1.2 properties properly filled in FNGetFiscalizationResult, FNGetFiscalizationResultByNumber.
    console_test:
      > added comman kkt-reg-result - get registration parameters
    cppbase:
      > fixed minutes in KKT time convertion
      > FFD 1.2 fixed for FF09 "Get registration parameters".
    
    ru:
    classic:
      > добавлено обновление свойств ФФД 1.2 в методах FNGetFiscalizationResult и FNGetFiscalizationResultByNumber.
    console_test:
      > добавлена команда kkt-reg-result - запрос параметров фискализации.
    cppbase:
      > исправлено получение минут из ответа ФРа.
      > добавлен разбор ответа в формате ФФД 1.2 для команды FF09 "Запрос параметров фискализации".

commit 182e6f02521f4048de6bfebcc23032d4e617ff45
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Wed Jul 7 19:40:16 2021 +0300

    en:
    classic
      > add optional C# and Go wrapper libraries
      > update swig classic_interface.i for csharp
    cppbase:
      > fix time_t convertion
      > removed jniutil
    
    ru:
    classic
      > добавлена опциональная сборка оберток для C# и Go
      > обновлен classic_interface.i
    cppbase:
      > поправлено преобразование time_t
      > удален jniutil

commit fc65de41e4e7caf8e59671c3ac814774d83f6b94 (HEAD -> master, origin/master, origin/HEAD)
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Tue Jun 29 02:28:10 2021 +0300

    en:
    console:
      > added mc-exchange-status
      > added mc-check-status
      > added fs-exchange-status as an alias for exchange-status
      > reordered commands help by groups
    
    ru:
    console:
      > добавлена команда mc-exchange-status
      > добавлена команда mc-check-status
      > команда fs-exchange-status как псевдоним для exchange-status
      > команды в справке сортированы по группам

commit 91fd137e0170d0dc7c8d6f35eb363f6901223c80
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Thu Jun 10 01:52:03 2021 +0300

    en:
    classic:
        > FNOperation force Quantity to 1 if DivisionalQuantity
    android_util_java:
      > BtLEHelper
      > StaticContext
    cppbase:
      > add btle bluetooth low energy (currently only for android)

    ru:
    > FNOperation выставляет Quantity в 1 если DivisionalQuantity не 0
    android_util_java:
      > добавлены класс BtLEHelper
      > добавлен класс StaticContext
    cppbase:
      > новая схема для транспорта: btle - bluetooth low energy (на данный момент только для android)

commit 48322e9052f918a3d929da657d8256d063f1fd40
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Tue Jun 1 20:09:39 2021 +0300

    en:
    classic:
      > fix FNAcceptMakringCode typo(added FNAcceptMarkingCode)
      > add FNBeginReadArchive, FNReadArchiveItem, FNSaveArchive
      > add FNMarkingClearBuffer
      > update ResetECR for interrupted FSReadDocument
      > add FNCheckItemBarcode2
    classic_java:
      > mirror current classic API
    console_test:
      > add fs-archive command
      > updated state-reset implementation
      > add fs-version command
      > add fs-parse-doc-classic
      > add fs-parse-doc-json
      > fixed write command documentation
    cppbase:
      > fix ByteArrayTLV::text
      > update UnixTimeTLV::text
    cppbase:
      > update tests
    qclassic:
      > mirror current classic API
    
    ru:
    classic:
      > поправлена опечатка в названии метода FNAcceptMakringCode (добавлен метод FNAcceptMarkingCode)
      > добавлены FNBeginReadArchive, FNReadArchiveItem, FNSaveArchive
      > добавлен FNMarkingClearBuffer
      > ResetECR теперь сбрасывает состояние в случае прерванного получения документа из ФН
      > добавлен FNCheckItemBarcode2
    classic_java:
      > добавлены текущие методы classic API
    console_test:
      > add fs-archive command
      > updated state-reset implementation
      > add fs-version command
      > add fs-parse-doc-classic
      > add fs-parse-doc-json
      > fixed write command documentation
    cppbase:
      > поправлен ByteArrayTLV::text
      > обновлен UnixTimeTLV::text
    cppbase:
      > обновлены тесты
    qclassic:
      > добавлены текущие методы classic API


commit 97415ba398eaa186e4cc1ffd4e24868d76ee8f1a
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Mon Apr 19 05:08:12 2021 +0300

    en:
    cppbase:
        > fix TLV parser. It turns out is ок to have TLV of with LEN == 0
    
    ru:
    cppbase:
        > исправлен разбор TLV. Оказалось это нормально иметь TLV с LEN == 0

commit 72863e283a9022c800492b9e52ab2d0bf53b7899
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Fri Apr 9 09:48:08 2021 +0300

    en:
    classic:
      > implement ReadLoaderVersion command
    
    ru:
    classic:
      > реализована команда ReadLoaderVersion


commit 54537cb848875b59403646ea9c91cc8a2b103890
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Tue Mar 30 01:20:25 2021 +0300

    en:
    classic:
      > FFD 1.2 commands, see classic_interface.h
    cppbase:
      > FFD 1.2 commands
      > Plain transfer mode for ProtocolV1
    console_test:
      > commands added: remote-firmware-version, remote-firmware-date, download-firmware
    
    ru:
    classic:
      > поддержка ФФД 1.2, см. classic_interface.h
    cppbase:
      > поддержка ФФД 1.2
      > Режим "чистой" передачи для стандартного протокола
    console_test:
      > добавлены команды: remote-firmware-version, remote-firmware-date, download-firmware


commit d7ee9cd28375570eef95943cf459f7dafd7d5089
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Sat Oct 31 17:10:30 2020 +0300

    en:
    classic:
      > plain C wrapper for classic_interface
    cppbase:
      > use default props if F7 || fonts not available
    ci:
      > add c_classic_interface.h to artefacts
    
    ru:
    classic:
      > C обертка вокруг classic_interface
    cppbase:
      > если в реализации отсутствует команда F7 или параметры шрифта - используются параметры по умолчанию.
    ci:
      > к артефактам добавлен c_classic_interface.h

commit c597fb2f006f0c20513a9830417b037122f5bbca
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Thu Aug 20 12:44:49 2020 +0300

    en:
    cppbase:
      > loadImage: choose image buffer automatically based on device support
    classic:
      > fix LoadImage on cashcore
    
    ru:
    cppbase:
      > loadImage: автоматически выбирается графический буфер в зависимости от устройств
    classic:
      > поправлена работа LoadImage на КЯ


commit 7f7f651ab85cd41d303bf0313d5277d77421a22f
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Fri Aug 14 05:56:19 2020 +0300

    en:
    classic:
      > add size padding for some String tags
    cppbase:
      > update taginfo add StringTLV taginfo factory method
      > FFD 1.2 WIP add commands FF68, FF70
    cppbase_test:
      > add tests for taginfo, TLV
      > fix maxDrawLineWidth512 == 0 as in cashcore
      > fix F7 font params for cashcore
    ci:
      > revert build configuration for linux(glibc 2.27, gcc 8.4)
      > new build env for linux and android
    
    ru:
    classic:
      > некоторые строковые теги автоматически дополняются до требуемого размера(все ИНН теги, заводской номер, код страны)
    cppbase:
      > обновлена таблица тегов, добавлен фабричный метод для StringTLV
      > ФФД 1.2 WIP добавлены команды FF68, FF70
      > поправлено получение параметра maxDrawLineWidth512 для КЯ
      > поправлено получения параметров шрифтов для КЯ
    cppbase_test:
      > добавлены тесты для таблицы тегов и TLV
    ci:
      > возвращена конфигурация сборок для linux(glibc 2.27 и gcc 8.4)
      > новое сборочное окружение для linux и android


commit abfb92588c408a0f0ef7389605c4b6050ef634df
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Wed Jun 17 18:17:34 2020 +0300

    en:
    cppbase:
      > fix: fixed tag 1162 construction for EAN-13 marking type.
      > Tables cache util resend command if FP_FP_IS_PRINTING_PREVIOUS_COMMAND
    cppbase_test:
      > update 1162 tests.
    
    ru:
    cppbase:
      > fix: исправлено создание тега 1162 для маркирвоки EAN-13.
      > Кеш таблиц, переповтор команды если FP_FP_IS_PRINTING_PREVIOUS_COMMAND
    cppbase_test:
      > обновлены тесты для кодирования тега 1162.


commit d159cc759bb3c2b45e626fbc37ac94fe8a88c7d8
Author: olefard <olefard@shtrih-m.ru>
Date:   Wed May 27 13:21:01 2020 +0300
    
    en:
    classic:
      > improved autofetch detailed error description
      > log detailed error description if supported
      > check if detailed error description supported when turned on
    ru:
    classic:
      > доработан автозапрос подробного описания ошибки.
      > Подробное описание ошибки, если доступно, выводится в лог.
      > При включении автозапроса делается проверка поддержки команды "Запрос описания последней ошибки"

commit 64bf8690c478ff1fdc5677d9a5db81e2e1c95851
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Wed May 27 02:56:45 2020 +0300

    en:
    classic:
      > cmake: generate swig wrapper while building
      > new function added DFE_DataPresentation, to control FiscalStorage document representation
    classic_java:
      > synchronize versions between classic and classic_java
    cppbase:
      > JSON document format added
    qclassic:
      > update header
    cmake:
      > generate java wrappers while building
    
    ru:
    classic:
      > cmake: генерировать swig обертки во время сборки
      > добавлена новая функция DFE_DataPresentation, задающая представление документа получаемого из ФН.
    classic_java:
      > синхронизированы версии между classic и оберткой
    cppbase:
      > добавлен формат JSON документа из тегов
    qclassic:
      > обновлен заголовочный файл
    cmake:
      > генерировать java обертки во время сборки


commit 04d918547d234af02f534a774d9435edd4250422
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Tue Apr 28 22:40:19 2020 +0300

    en:
    classic:
      > update FNSendItemBarcode doc
    cppbase:
      > fix FF67 item code field endiannes
    cppbase_test:
      > fixed FF67 tests
    
    ru:
    classic:
      > обновлена документация FNSendItemBarcode
    cppbase:
      > поправлен порядок байт в поле код товара в команде FF67
    cppbase_test:
      > поправлены тесты FF67

commit 235484c7fb8d413aae1f2e4c9360429b7a115617
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Fri Apr 17 19:22:40 2020 +0300

    en:
    classic:
      > fill MarkingType and MarkingTypeEx properties in FNSendItemBarcode
      > add MarkingTypeEx property
    classic_java:
      > add MarkingTypeEx property
    cppbase:
      > fix AssignMarkCommand
    qclassic:
      > add MarkingTypeEx property
    
    ru:
    classic:
      > заполнять свойства MarkingType и MarkingTypeEx в команде FNSendItemBarcode
      > добавлено свойство MarkingTypeEx
    classic_java:
      > добавлено свойство MarkingTypeEx
    cppbase:
      > поправлен возврат от команды AssignMarkCommand(Привязка  маркированного товара к позиции FF67)
    qclassic:
      > добавлено свойство MarkingTypeEx


commit 852bf722a884af66e7f9815ae1ecd2f2f1dc114b
Author: olefard <olefard@shtrih-m.ru>
Date:   Thu Apr 16 12:38:28 2020 +0300

    en:
    one_s:
      > fix error on driver description request
    
    ru:
    one_s:
      > исправлена ошибка при выдаче информации о драйвере.


commit 7f67cd453d22a83cc1577cfec1cbdec2e4d69ede
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Wed Apr 15 19:01:24 2020 +0300

    en:
    added 1C linux/windows native api driver
    cmake refactoring move to 'modern' cmake
    ci:
      > exclude cppbase from build artifacts
      > make 1c deploy package
    cppbase:
      > ProtocolV1 improvements
      > builds are always static
    classic:
      > fix https://github.com/shtrih-m/fr_drv_ng/issues/101
      > python's setup.py don't depend on cppbase
      > default ComPath now OS related(linux and windows)
    one_s:
      > first public release
      > support driver development requirements 3.2
    
    ru:
    добавлен NativeAPI драйвер 1C для linux/windows
    cmake рефакторинг, переход на "современный" cmake
    ci:
      > исключить cppbase из артефактов сборок
      > собирать 1c архив
    cppbase:
      > улучшения в протоколе версии 1
      > библиотека всегда статическая
    classic:
      > исправлено https://github.com/shtrih-m/fr_drv_ng/issues/101
      > python's setup.py не зависит от cppbase
      > свойство ComPath по умолчанию теперь зависит от ОС (linux and windows)
    one_s:
      > первый публичный релиз
      > поддерживает требования к разработке драйверов 3.2



commit b65de50b6f7d3bdfc5f7112a3ee6249d99bf877b
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Fri Feb 21 15:39:48 2020 +0300

    en:
    cppbase:
      > log and error in case of input command code not equal to output(sent) code
      > fix FDOSender warning message
      > command 0xFF67 "assign mark to position" added.
      > tag 1162 construction rules changed to comply ФНС 434
    cppbase_test:
      > test AssignMarkCommand
    examples:
      > assing marks examples.
      > android example, upgrade native libs and jar wrapper
    classic:
      > add method FNSendItemBarcode
      > add EnableCashcoreMarkCompatibility property
      > update docs
    classic_test:
      > test marking commands
    qclassic:
      > add method FNSendItemBarcode
      > add EnableCashcoreMarkCompatibility property
    
    ru:
    cppbase:
      > логгировать и сообщать ошибку в случае если код входящей команды отличается от отправленной
      > поправлены сообщения FDOSender
      > добавлена команда 0xFF67 "Привязать марку к позиции"
      > изменены правила формирования тега 1162 в соответствии с приказом ФНС 434.
    cppbase_test:
      > тесты "Привязать марку к позиции"
    examples:
      > добавлены примеры привязки марки к позиции
      > обновлены библиотеки в примере android
    classic:
      > добавлен метод FNSendItemBarcode
      > добавлено свойство EnableCashcoreMarkCompatibility
      > обновлена документация
    classic_test:
      > тест FNSendItemBarcode
    qclassic:
      > добавлен метод FNSendItemBarcode
      > добавлено свойство EnableCashcoreMarkCompatibility


commit 2e7c7ab23b19c39396a2963106b69a2c8a5d8381
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Tue Dec 10 11:46:13 2019 +0300

    en:
    cppbase:
      > check iolayer->opened in protocol doConnect routine
      > fix isTimeoutHappend in TimeoutUtil
      > asiolayer: improve error reporting
    cppbase_test:
      > new protocol tests new logger tests
    one_s:
      > Native API plugin for 1C WIP
    
    ru:
    cppbase:
      > проверяем что транспорт открыт(iolayer->opened) при инициализации протокола
      > поправлен isTimeoutHappend в TimeoutUtil
      > asiolayer: улучшено логгирование ошибок
    cppbase_test:
      > обновлены тесты для протоколов и логгирования
    one_s:
      > Native API плагин для 1C в разработке


commit 86c82da6a1a720455c1b26bd31c9f5d67f0b9d38
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Fri Nov 1 15:38:34 2019 +0300

    en:
    classic:
      > update cppbase linkage
    classic_test:
      > update cppbase linkage
    console_test:
      > update cppbase linkage
    cppbase:
      > update spdlog, fmt, Catch2 submodules
    console_test:
      > restore table input parsing fixed
      > update cppbase linkage
    ci:
      > android x86_64 build added
    
    ru:
    classic:
      > обновлен cppbase
    classic_test:
      > обновлен cppbase
    console_test:
      > обновлен cppbase
    cppbase:
      > обновлены библиотеки spdlog, fmtlib, Catch2
    console_test:
      > поправлена команда restore table
      > обновлен cppbase
    ci:
      > добавлена сборка под x86_64 под android


commit 534723950df2688184abe4c2506719825a27df65
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Fri Aug 23 17:13:14 2019 +0300

    en:
    ci:
      > add iOS and MacOS builds
    classic:
      > fix: SerialIO baudrate speed in FindDevice
    cppbase:
      > ios, macos support

    ru:
    ci:
      > сборки под iOS и MacOS
    classic:
      > fix: поправлена установка скорости SerialIO в FindDevice
    cppbase:
      > ios, macos поддержка


commit 5148ca7f0c31ba77f90c45b99a69a244a57bce4d
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Thu Jul 25 01:55:13 2019 +0300

    en:
    classic:
      > fix https://git.shtrih-m.ru/fr_drv_ng/public_issues/issues/93
      > Print2DBarcode support DelayedPrint
      > implemented LoadGraphics512
      > implemented PrintGraphics512
    cppbase:
      > update submodules
    cppbase:
      > update tests
    
    ru:
    classic:
      > поправлено https://git.shtrih-m.ru/fr_drv_ng/public_issues/issues/93
      > Print2DBarcode поддержка флага DelayedPrint
      > реализация LoadGraphics512
      > реализация PrintGraphics512
    cppbase:
      > обновлены библиотеки
    cppbase:
      > обновлены тесты


commit d2f7ef1222dc4f71d64446e279f9e51b26b3b375
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Fri Jun 14 02:50:54 2019 +0300

    en:
    console_test:
      > add beep cmd
    qclassic:
      > add missing functionality of Get/SetDeviceFunction, and related properties
    
    ru:
    console_test:
      > добавлена команда звука - beep
    qclassic:
      > добавлены обертки для функций Get/SetDeviceFunction и свойства, используемые ими


commit ec19fc4f2555b93b1de21ade95200b3a2bbe1a96
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Thu Apr 18 16:13:30 2019 +0300

    en:
    classic:
      > do not check for MarkingType in FNSendItemCodeData
      > doc update
      > localization initialization from dynamic link time to instance initialization
    classic_test:
      > add ItemCodeData test.
    
    ru:
    classic:
      > добавлена возможность передавать КТН для любого типа маркировки.
      > doc: дополнена документация.
      > инициализация локали происходит не в момент динамической линковки, а в момент первой инициализации драйвера
    classic_test:
      > добавлен тест для КТН.



commit 041e728c2abe9b6a97859675d06f04bf807acab8
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Wed Mar 20 00:57:25 2019 +0300

    en:
    ci:
      > android: use llvm linker, NDK r19c
    classic:
      > fix toTimePoint
      > SkipPrint restored
      > doc: table view improved
      > improved doc for properties DriverMajorVersion, DriverMinorVersion, DriverRelease, DriverBuild, ModelParamValue, ModelParamNumber, ModelParamDescription, DriverVersion, ErrorCode, EmailAddress, ConnectionURI
    cppbase:
      > update asio
    
    ru:
    ci:
      > android: используется линкер от llvm, NDK r19c
    classic:
      > поправлен метод toTimePoint
      > Восстановлено забытое свойство SkipPrint
      > Комментарии для документации: улучшен внешний вид всех таблиц.
      > Изменения в комментариях к свойствам DriverMajorVersion, DriverMinorVersion, DriverRelease, DriverBuild, ModelParamValue, ModelParamNumber, ModelParamDescription, DriverVersion, ErrorCode, EmailAddress, ConnectionURI
    cppbase:
      > обновлен asio


commit 0eff1614634bdf155ecb0553efe426ad4455d749
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Thu Feb 28 01:12:49 2019 +0300

    en:
    classic:
      > implemented OFDExchange
      > AutoEoD now uses OFDPollPeriod
      > AutoOFDExchange mirrors AutoEoD property
      > Property setters now not calling property changed callback
    cppbase:
      > FDOSenderService add customizable poll period
      > dont wait timeout for data on tcpsocket close(speedup "broken" connections closing)
    
    ru:
    classic:
      > реализован метод OFDExchange
      > AutoEoD теперь использует свойство OFDPollPeriod
      > AutoOFDExchange дублирует свойство AutoEoD
      > Сеттеры теперь не вызывают обратный вызов "свойство изменено"
    cppbase:
      > FDOSenderService настраиваемый промежуток между посылками
      > Не ждать данных весь таймаут при закрытии tcp сокета(быстрее закрывает сокет если соединение установлено,но той стороны не приходят данные)


commit 484ac43622fc42c874adc01e3fc273bd741a4fc4
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Sun Feb 17 21:12:19 2019 +0300

    en:
    console_test:
      > add fs-get-eol command
      > fs-status output detailed warning flags
    cppbase:
      > add FR_DRV_LANG env variable - forces messages localization. Valid values are: ru/en
    
    ru:
    console_test:
      > добавлена команда fs-get-eol - окончание срока действия ФН
      > в вывод команды fs-status добавлена детализация флагов предупреждений ФН
    cppbase:
      > добавлена обработка переменной окружения FR_DRV_LANG - принудительно меняет локализацию сообщений драйвера. Возможные значения ru/en



commit 069c3bffbd1e76dee18a72d70e32da0e3b8adb1e
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Mon Feb 11 14:47:21 2019 +0300

    en:
    classic:
      > dont LTO on win
      > setup.py fix for windows
      > setup.py reformat
    classic_java:
      > add named classic constructor
    cppbase:
      > FDO sender service fix recv timeout
      > fix build shared lib on windows
    qclassic:
      > correct exports on windows
    CI:
      > Qt upgrade to 5.12.1
      > windows i386 build with VC2017
    
    ru:
    classic:
      > не использовать LTO в сборках под windows
      > setup.py исправление для windows
      > setup.py переформатирование
    classic_java:
      > добавлен конструктор с именем устройства
    cppbase:
      > Служба отправки в ОФД исправлен таймаут приёма
      > корректная сборка разделяемых библиотек под windows
    qclassic:
      > исправлен экспорт интерфейса под windows
    CI:
      > Qt обновлен до 5.12.1
      > i386 сборки под windows собираются VC2017



commit df2297b81f59dbbe01098c63b9c77af0db2f038b
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Fri Jan 25 03:20:21 2019 +0300

    en:
    classic:
      > fix swig python bindings interface file
      > add named constructor, that name will be instance name in logs
      > small fixes
    qclassic:
      > add named constructor, that name will be instance name in logs
    cppbase:
      > do not try to load properties on lastErrorDescription(cause we gona lose last error)
    
    ru:
    classic:
      > поправлены профиль swig для python
      > в конструктор можно передать имя устройства. Это имя будет отображаться в логах
      > small fixes
    qclassic:
      > в конструктор можно передать имя устройства. Это имя будет отображаться в логах
    cppbase:
      > не пытаться получить *последнюю* ошибку если неизвестно поддерживает принтер этот функционал или нет(потому что в таком случае уйдет состояние этой ошибки)

commit d70b96de5d4f4e05c78374d23fd2e530ca32e6dc
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Sun Dec 16 21:54:20 2018 +0300

    en:
    classic_java:
      > update version number build.gradle
    
    ru:
    classic_java:
      > обновлена версия сборки

commit ecc8c3f72e1a5ac086a422da252b0ef7351267b6 (tag: 1.4.4)
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Sun Dec 16 02:56:42 2018 +0300

    en:
    classic:
      > update swig interface file
      > Get\SetDeviceFunction implemented
    classic_java:
      > Get\SetDeviceFunction added
    console_test:
      > simplify printer creation
    cppbase:
      > update cdcacm IoLayer for android
    examples:
      > SetDeviceFunction example added
    
    ru:
    classic:
      > swig обновлен файл описания интерфейса
      > Get\SetDeviceFunction добавлены
    classic_java:
      > Get\SetDeviceFunction добавлены
    console_test:
      > упрощено конструирование принтера
    cppbase:
      > обновлён cdcacm для android
    examples:
      > SetDeviceFunction пример добавлен


commit 186c0e38f327bd68bf57950eaf256ed32d3fa661
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Wed Dec 5 02:37:25 2018 +0300

    en:
    classic:
      > fix OpenCheck for ELVES etc
    cppbase:
      > ProtocolV1 add ack_timeout support
      > ProtocolV2 fix closed IOLayer loop
    
    ru:
    classic:
      > поправлен метод OpenCheck для ЭЛВЕС-МФ и других устройств с той же реализацией
    cppbase:
      > ProtocolV1 добавлена поддержка свойства ack_timeout
      > ProtocolV2 поправлен цикл до таймаута, если транспортный уровень закрыт


commit 534f6057354c7aa4c6a9fad19dc9510c6b08fcaf
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Mon Nov 26 10:43:35 2018 +0300

    en:
    classic:
      > replace fsDocTLVRead by common getFsDocumentByNumber
    console_test:
      > replace doReadTLVDoc by common getFsDocumentByNumber
    cppbase:
      > enable keepalive for TcpSocketIO
      > improve TcpSocketIO,SerialIO - do not close on recoverable errors
      > INTERPROCEDURAL_OPTIMIZATION only for Release builds
      > add getFsDocumentByNumber
    
    ru:
    classic:
      > fsDocTLVRead->getFsDocumentByNumber
    console_test:
      > doReadTLVDoc->getFsDocumentByNumber
    cppbase:
      > включен keepalive для TcpSocketIO
      > улучшены  TcpSocketIO, SerialIO - не закрывать IoLayer при не критических ошибках
      > INTERPROCEDURAL_OPTIMIZATION только для релизных сборок
      > добавлен метод getFsDocumentByNumber

commit d1855759b9e5471da7cdd14a0aa8829a23654d34
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Sat Nov 24 15:17:25 2018 +0300

    en:
    classic:
      > fix FNGetDocumentAsString on cashcore (https://github.com/shtrih-m/fr_drv_ng/issues/25)
    
    ru:
    classic:
      > поправлена работа метода FNGetDocumentAsString на Кассовом Ядре (https://github.com/shtrih-m/fr_drv_ng/issues/25)

commit a4b5e5fa71e337b192b90f3a734d1917582ab496
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Mon Nov 19 12:13:08 2018 +0300

    en:
    console_test:
      > fix optional args + parameters eq: save-tables -a "tcp:..."
    
    ru:
    console_test:
      > поправлена обработка опциональных параметров команды вместе с - аргументами

commit ba1e0e6fcc2dabd99e7434b6356e0230bb0db7f3
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Mon Nov 19 11:03:28 2018 +0300

    en:
    CI:
      android: build qclassic wrapper
      all: enable LTO(link time optimisation) for shared libraries builds
    classic:
      > DefConnectionTimeout now equals to DefTimeout
      > WaitForPrinting continue the loop if submode 4 or 5
      > implemented ResetECR
    console_test:
      > add state-reset command
      > enable LTO for dynamic/static builds
    cppbase:
      > remove GCC Android specific code
      > fix alignedString font bounds check
      > getIoFromString print URI
      > localizer update
    
    ru:
    CI:
      android: сборка включает qclassic обёртку
      all: включен LTO(link time optimisation) для динамических сборок
    classic:
      > DefConnectionTimeout теперь равен DefTimeout
      > поправлен метод WaitForPrinting ожидает завершения печати если в подрежиме 4 или 5
      > реализован метод ResetECR
    console_test:
      > добавлена команда state-reset
      > включен LTO для динамических и статических сборок
    cppbase:
      > GCC специфичный код под Android удалён(собираем только с clang)
      > поправлен метод alignedString теперь работает и с последним шрифтом
      > getIoFromString добавлена печать текущего URI
      > обновлен перевод


commit c4d0d07411eeae655833a3255f972a11c4c92096
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Mon Nov 12 11:42:06 2018 +0300

    en:
    console_test:
      > COM port discover timeout 500->1000ms
    cppbase:
      > fix device discoverer on windows with msvc
      > fix log prefix strip on winndows with msvc
      > TCP and Serial IoLayer now implemented using boost asio
    cppbase_test:
      > use asio standalone
      > add asio include
    
    ru:
    console_test:
      > Таймаут сканирования COM портов увеличен 500->1000ms на порт
    cppbase:
      > поправлено сканирование портов на windows msvc
      > поправлено обрезание префикса логгера на windows msvc
      > TCP и Serial IoLayer теперь используют boost asio
    cppbase_test:
      > use asio standalone
      > add asio include


commit ac7dadcf4dfaf0d9d72becfd3c34ec8cbc79465d
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Thu Nov 8 23:53:17 2018 +0300

    en:
    cppbase:
      > fix deviceToURI format(deprecated byte_timeout cleanup continues)
    console_test:
      > add z-report command
      > read, save-tables commands add optional args in form table[.row[.field]]
    examples:
      > add dfu update example in windows batch format
      > fix dfu_update bash example
    
    ru:
    cppbase:
      > исправлено форматирование URI deviceToURI
    console_test:
      > добавлена команда z-report (закрытие смены)
      > в команды read и save-tables можно передавать опциональные аргументы в формате table[.row[.field]]
    examples:
      > добавлен пример обновления по dfu в формате .bat под windows
      > поправлен пример dfu_update на bash


commit aee135f02c632cfe9ac5d738b95fc35092fcd4bd
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Thu Nov 1 17:27:31 2018 +0300

    en:
    cppbase:
        > follow up fix StartFsFiscalModeCloseCommand response parsing
    
    ru:
    cppbase:
        > продолжение исправления разбора ответа на команду StartFsFiscalModeCloseCommand.


commit 86fabefaac0e37e43cf33d8a4c0c591ddff366bd
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Wed Oct 31 14:14:34 2018 +0300

    en:
    classic:
      > Sale, Buy, ReturnSale, ReturnBuy add rounding description (round to 3 decimal places)
      > fix PaymentItemSign values description
    classic_java:
      > fix: update version
    console_test:
      > print current command to log
    cppbase:
      > setExchangeOptions check if current IoLayer supports baudrate changing
      > protocols improvement, use timeout for connect
      > improved max text length for ProtocolV2
    
    ru:
    classic:
      > добавлено в описание методов Sale, Buy, ReturnSale, ReturnBuy, что количество округляется до 3 знаков.
      > исправлено описание возможных значений PaymentItemSign.
    classic_java:
      > обновлена версия
    console_test:
      > печать исполняемой команды в лог
    cppbase:
      > setExchangeOptions что обмен идёт через SerialIO
      > Улучшены протоколы, использовать timeout для установки соединения
      > Поддерживают длинных строк для ProtocolV2


commit 7acc61cdc63846c7748ac22955eb05a3d1f3cb7b
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Mon Oct 15 18:03:27 2018 +0300

    en:
    classic:
      > byte_timeout deprecation cleanup
    cppbase:
      > remove byte_timeout from urlhelper
    cppbase_test:
      > update urlhelpertest
    qclassic:
      > to/fromSecsSinceEpoch->to/fromMSecsSinceEpoch for compatibility with old releases
    CI: i486_ok - old kernels support build (<= 2.6.32 glibc 2.23)
    
    ru:
    classic:
      > byte_timeout больше не используется
    cppbase:
      > byte_timeout больше не используется
    cppbase_test:
      > обновлен urlhelpertest
    qclassic:
      > to/fromSecsSinceEpoch->to/fromMSecsSinceEpoch для совместимости с Qt <= 5.8
    CI: i486_ok - сборка с поддержкой старых ядер (<= 2.6.32 glibc 2.23)

commit 44a414d1e3fb8358ea9e8cebb165932274a4ad91 (tag: 1.4.3)
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Sun Oct 14 03:41:43 2018 +0300

    en:
    classic:
      > add ReadFeatureLicenses/WriteFeatureLicenses, DigitalSign property 1.4.3
    classic_java:
      > add ReadFeatureLicenses/WriteFeatureLicenses, DigitalSign property 1.4.3
    console_test:
      > read-feature-licenses, write-feature-licenses commands added
    cppbase:
      > ProtocolV1 improvments
      > SerialIO improvements for Linux
      > add FR_DRV_CMD_TIMEOUTS support, example format: 11:123,0B:421,FF45:123412
      > PrintString* commands filled with zeroes up to minimal Protocol v1 width
      > add enq_mode to ConnectionURI parsing: 0 - old behavior, 1 - send ENQ before each command
      > byte_timeout deprecated
      > Check if response command code matches request command code
    qclassic:
      > add ReadFeatureLicenses/WriteFeatureLicenses, DigitalSign property  1.4.3
    
    ru:
    classic:
      > добавлены методы ReadFeatureLicenses/WriteFeatureLicenses, свойство DigitalSign 1.4.3
    classic_java:
      > добавлены методы ReadFeatureLicenses/WriteFeatureLicenses, свойство DigitalSign 1.4.3
    console_test:
      > добавлены команды read-feature-licenses, write-feature-licenses
    cppbase:
      > ProtocolV1 усовершенствован
      > SerialIO улучшен на Linux
      > добавлена обработка переменной окружения FR_DRV_CMD_TIMEOUTS, теперь можно задать таймаут для отдельной команды. Пример формата: 11:123,0B:421,FF45:123412
      > Команды печати заполняются нулями
      > добавлено обработка параметра enq_mode в ConnectionURI: 0 - без ENQ перед каждой команды, 1 - посылать ENQ перед каждой командой
      > byte_timeout больше не используется. Только глобалный таймаут на команду.
      > Добавлена проверка код команды ответа должен соответствовать коду команды запроса
    qclassic:
      > добавлены методы ReadFeatureLicenses/WriteFeatureLicenses, свойство DigitalSign 1.4.3

commit 37390997869da3d95eeaed016367b7fe801e6ef5
Author: Alexey Mednyy <amednyy@shtrih-m.ru>
Date:   Fri Sep 21 15:53:12 2018 +0300

    en:
    classic:
      > add PrinterMode, PrinterSubmode enums
      > implement PrintDepartmentReport, PrintTaxReport, PrintZReportFromBuffer,PrintZReportInBuffer
      > Doc update
    classic_java:
      > add PrinterMode, PrinterSubmode enums
    cppbase:
      > add SaveZReportInBuffertCommand,PrintZReportFromBuffertCommand commands
    qclassic:
      > add PrinterMode, PrinterSubmode enums
      > add QT_NO_VERSION_TAGGING to skip particular Qt version dependency
    
    ru:
    classic:
      > перечисления PrinterMode, PrinterSubmode
      > реализованы функции PrintDepartmentReport, PrintTaxReport, PrintZReportFromBuffer,PrintZReportInBuffer
      > Рефакторинг документаци
    classic_java:
      > добавлены PrinterMode, PrinterSubmode
    cppbase:
      > добавлены SaveZReportInBuffertCommand,PrintZReportFromBuffertCommand commands
    qclassic:
      > добавлены PrinterMode, PrinterSubmode
      > определен QT_NO_VERSION_TAGGING сборка линкуется без привязке к версии Qt


commit 55e28a139e8bcca41feb9619295b1211c053a872  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Tue Sep 11 00:42:18 2018 +0300

    en:
    classic:
      > add ReadLastErrorDescription method
      > fix some documentation format issues
    classic_java:
      > add ReadLastErrorDescription method
    cppbase:
      > update submodules
    examples:
      > update README for github
    qclassic:
      > add ReadLastErrorDescription method
    Doxyfile: generate XML output
    
    ru:
    classic:
      > добавлен метод ReadLastErrorDescription
      > поправлен формат документации
    classic_java:
      > добавлен метод ReadLastErrorDescription
    cppbase:
      > обновлены подмодули
    examples:
      > обновлен README для github
    qclassic:
      > добавлен метод ReadLastErrorDescription
    Doxyfile: генерировать XML
  
commit 13a20ee3b849ea75ec5ea09824db32e953c4d78a  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Tue Sep 11 00:26:00 2018 +0300

    en:
    CI: build qclassic(Qt classic_fr_drv_ng wrapper with properties,signals,slots)
    
    ru:
    CI: сборка библиотеки qclassic(Qt обертка classic_fr_drv_ng с поддержкой свойств, сигналов и слотов)
  
commit ccc0ad78d77fec93bd22813acfb4e28ef8f212d9  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Tue Sep 4 22:33:42 2018 +0300

    en:
    classic:
      > implemented ReadErrorDescription method
    
    ru:
      > реализован метод ReadErrorDescription
  
commit 961132951b75b8f72e2cd6eb3d99f449df4c8f92  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Mon Sep 3 19:19:02 2018 +0300

    en:
    classic_test:
       > update test for CI
    
    ru:
    classic_test:
       > обновлены тесты для CI
  
commit b5c3a03db5bbe31bc69b5aba8d60ba456976616e  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Mon Sep 3 18:40:59 2018 +0300

    en:
    classic:
       > add // to email will skip printing, but add TLV to operation
       > fix: wrap long string fnSendRequisite (FNSendSenderEmail,FNSendCustomerEmail)
       > FNOpenSession, FNCloseSession now behave the same as windows DrvFr.
    classic_test:
       > added a test with a long e-mail wrap
       > added test FNCloseSession with the TLV
    
    ru:
    classic:
      > добавлена возможность указать // в начале е-мейла
      > fix: исправлена печать длинного е-мейла
      > изменена реализация методов FNOpenSession, FNCloseSession для совместимости с виндовым драйвером.
    classic_test:
      > добавлен тест с печатью длинного е-мейла.
      > добавлен тест закрытия смены с тегом.
  
commit bdc448cb6cbf8c2cb29d1eb71223460d321b9906  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Thu Aug 30 14:24:38 2018 +0300

    add github fr_drv_ng submodule
  
commit b03c9df222804194cca89578aae43a02ae6eac04  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Thu Aug 30 14:23:10 2018 +0300

    en:
    ci: android builds only with clang
    ci: android deploy STL lib from NDK
    update README
    
    classic:
      > doc: mark deprecated methods
      > jni: fix Date construction, add ReadCashDrawerSum
      > doc: fixed CheckType table
      > add ReadCashDrawerSum method
      > add SkipPrint property
    classic_java:
      > add ReadCashDrawerSum method
      > add SkipPrint property
    cppbase:
      > update Catch2 submodule
      > update spdlog
    cppbase_fr_drv_ng_test:
      > update tests
    examples:
      > update readme
    qclassic:
      > add ReadCashDrawerSum method
      > add SkipPrint property
    
    ru:
    ci: android сборки только с clang
    ci: android включать STL из NDK
    обновлен README
    classic:
      > doc: помечены устаревшие методы
      > jni: исправлен конструктор Date
      > doc: исправлена таблица значений свойства CheckType
      > добавлен метод ReadCashDrawerSum
      > добавлено свойство SkipPrint
    classic_java:
      > добавлен метод ReadCashDrawerSum
      > добавлено свойство SkipPrint
    cppbase:
      > обновлен сабмодуль Catch2
      > обновлен сабмодуль spdlog
    cppbase_fr_drv_ng_test:
      > обновлен тесты
    examples:
      > обновлены справка
    qclassic:
      > добавлен метод ReadCashDrawerSum
      > добавлено свойство SkipPrint
  
commit a232fa0dd5b81e2db9b09a43bf76715cf6672c0f  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Mon Aug 20 17:35:35 2018 +0300

    en:
    ci: fix android jar build
    ru:
    ci: поправлена сборка jar библиотеки под android
  
commit 9d1b63e87926eed283a766eb60157fdaa780d8ac  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Mon Aug 20 17:27:23 2018 +0300

    en:
    cppbase:
      > fixed FF0A on Cashcore(gives date without time) see https://git.shtrih-m.ru/fr_drv_ng/fr_drv_ng/issues/53
    
    ru:
    cppbase:
      > на устройствах с КЯ команда FF0A возкращает дату "Отчета о состоянии расчетов" без времени
  
commit 8b08067bd9b176983815a8d3e3bd170b23c397b1  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Mon Aug 20 16:00:27 2018 +0300

    en:
    android clang builds
    readme update
    
    classic:
      > clang build fixes
      > CALL_METHOD macro update
    cppbase:
      > clang build fixes: urlHelper fix regex error
    
    ru:
    сборки под android с clang
    обновлен readme
    
    classic:
      > поправлена сборка с clang
      > обновлен макрос CALL_METHOD
    cppbase:
      > поправлена сборка с clang: urlHelper regex
  
commit 2edb6aa6c050cb070a3df820d2ea2ff771f2d3be  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Wed Aug 8 20:53:27 2018 +0300

    en:
    cppbase:
      > Barcode1D fix workaround models
    
    ru:
    cppbase:
      > Barcode1D поправлены модели для обхода проблемы с переворотом
  
commit 0d99faaec11cdddb8b60222ac153af3aaf3dc85a  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Tue Aug 7 14:42:45 2018 +0300

    en:
    cppbase_test:
      > fix barcode aligned tests
    
    ru:
    cppbase_test:
      > поправлены тесты выравнивания ШК
  
commit dcc5109192aa3fbe6ee95ab9151dbc3ad28933f9  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Mon Aug 6 19:12:54 2018 +0300

    en:
    classic:
      > fix build with clang
    cppbase:
      > fixed barcode 1d alignment
      > add getLastErrorDescription, fix isPrintingNow for printers that does not support readShortIBMPrinterStatus
      > поправлена сборка с clang
      > update error 161 description
    
    ru:
    classic:
      > поправлена сборка с clang
    cppbase:
      > поправлено выравнивание одномерных ШК
      > добавлена функция getLastErrorDescription для принтеров, поддерживающих
      > поправлена функция isPrintingNow для принтеров, не поддерживающих комаду readShortIBMPrinterStatus
      > поправлена сборка с clang
      > обновлено описание ошибки 161
  
commit 75839121a470614f0873a7c2c127fc80b12b4337  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Tue Jul 31 16:37:31 2018 +0300

    en:
    classic:
      > log getters return value
    cppbase:
      > LogUtil add result property
    
    ru:
    classic:
      > логгировать возвращаемые значения для геттеров свойств
    cppbase:
      > LogUtil свойство result
  
commit 677727a465fb14bafd23890a8f1e825e9967605b  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Tue Jul 31 15:00:24 2018 +0300

    en:
    cppbase:
      > UM firmware < 23.03.2018 swapBytes workaround
      > add UIN(),isUM(),isReady() to DeviceProperties
    
    ru:
    cppbase:
      > обход проблемы с переворачиванием байт на УМ с прошивкой < 23.03.2018
      > добавлены  UIN(), isUM(), isReady() в DeviceProperties
  
commit f654c86ba580db96929367f43f7aa13ce8919fd3  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Thu Jul 26 19:26:55 2018 +0300

    en:
    cppbase:
      > fix win32 linkage
    qclassic:
      > link with QT5::Core
    
    ru:
    cppbase:
      > поправлена линковка для win32 сборок
    qclassic:
      > Линковаться с QT5::Core
  
commit 214e0cc5220863fe265aac32c72ea8231781381b  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Thu Jul 26 12:27:12 2018 +0300

    en:
    classic:
      > use FontType for PrintBarcodeLine
      > update default timeouts
      > ConnectionURI doc fixed
    classic_test:
      > update test for new default timeouts
    cppbase:
      > BarcodeRenderer add detailed logging fix swap policy
      > Barcode1D reverse data while scaling
      > BasicBarcode add text font property
      > Log: cut and add an ellipsis to long log prefix names
      > default timeout and byte timeout to 15 and 10 seconds respectively
    cppbase_test:
      > Barcode1D tests
      > BitUtil tests
    
    ru:
    classic:
      > выбираемый FontType для метода PrintBarcodeLine
      > обновлены таймауты по умолчанию
      > ConnectionURI исправлена документация
    classic_test:
      > обновлены тесты таймаутов
    cppbase:
      > BarcodeRenderer добавлено детальное логгирование
      > Barcode1D по умолчанию инвертировать байты во время масштабирования
      > BasicBarcode добавлен выбор шрифта
      > Log: обрезать и добавлять многоточие для длинных префиксов
      > По умолчанию таймаут и таймаут приёма байта установлены в 15 и 10 секунд соответственно
    cppbase_test:
      > Barcode1D тесты
      > BitUtil тесты
  
commit edf15778aa5bb7af6107c774081fe5740a7753b4  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Tue Jul 24 23:50:27 2018 +0300

    en:
    classic:
      > SetSerialNumber add cashcore support
    cppbase:
      > trim last space in IoLayer logger output
      > ostream<< FrDateTime don't print timezone
      > Align/scale barcode by bits, not bytes fix #39
      > SerialIO: don't wait for IO events while reading
      > Localizer: update errors descriptions
      > get FS table number from dynamic properties
    
    ru:
    classic:
      > SetSerialNumber добавлена поддержка КЯ
    cppbase:
      > обрезать конечные пробелы в логе обмена
      > ostream<< FrDateTime убрана временная зона из формата
      > Выравнивать/масштабировать одномерный штрих-код по битам, не байтам
      > SerialIO: убрано ожидание событий ком-порта из функции чтения
      > Localizer: обновлено описание ошибок
      > Получать номер таблицы ФН динамически
  
commit 8be76c4d4706edd94ab6a2da161f1df761b86f6b  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Mon Jul 16 12:31:16 2018 +0300

    en:
    classic:
      > implement FNRequestRegistrationTLV
    console_test:
      > put-sd-update add tables variant
    cppbase:
      > hide zint symbols with gcc and clang fix https://git.shtrih-m.ru/fr_drv_ng/public_issues/issues/32
      > WriteUpdatePartCommand add tables mode
    ru:
    classic:
      > реализована команда FNRequestRegistrationTLV
    console_test:
      > put-sd-update добавлена загрузка таблиц
    cppbase:
      > скрывать символы библиотеки zint
      > WriteUpdatePartCommand добавлена загрузка таблиц
  
commit 5bfa834f0b4733b981404bc07eacf34db3546786  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Wed Jul 11 13:52:39 2018 +0300

    en:
    classic:
      > fixed FNSendItemCodeData for tobacco products
    
    ru:
    classic:
      > исправлен метод FNSendItemCodeData для табачных изделий
  
commit d01ab0507e4c9b0acdc8f6f7727d01887ae68da2  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Wed Jul 11 09:16:34 2018 +0300

    en:
    cppbase:
      > BtSerialIO: fix -Wunused str2ba on android
    CI:
      > qemu startup timeout increased
    ru:
      cppbase:
      > BtSerialIO: поправлен -Wunused str2ba на android
    CI:
      > увеличено время ожидания загрузки qemu
  
commit ae900100993b31c38d1d0ab67eff7df554c34063  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Wed Jul 11 01:24:42 2018 +0300

    en:
    classic:
      > WaitForPrinting: not only subroutine, also check printer buffer contents if supported by device
    cppbase:
      > isPrintingNow function added
      > modelType always return MT_Cashcore if F7 cashcore bit set
      > Linux: BtSerialIO remove libbluetooth dependency
      > ReadShortStatusCommand add LastPrintStatus support(cashcore)
      > add ReadShortIBMPrinterStatusCommand(0xD1)
    ru:
    classic:
      > WaitForPrinting: не только подрежим, также проверять содержимое буфера печати если поддерживается моделью
    cppbase:
      > добавлена функция isPrintingNow
      > Linux: BtSerialIO не требует линковки с libbluetooth
      > ReadShortStatusCommand добавлена поддержка поля "Статус последеней печати" (для КЯ)
      > добавлена команда ReadShortIBMPrinterStatusCommand(0xD1)
  
commit d8e45cf9ac60e5f2e23e617c24d8d1e3d26354da  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Mon Jul 9 12:36:36 2018 +0300

    en:
    cppbase:
      > fix OperateV2(FF46h) - string size 0,128 #fix https://git.shtrih-m.ru/fr_drv_ng/fr_drv_ng/issues/40
      > add SOVERSION
    CI:
      > windows builds now built with VisualStudio 2017
    
    ru:
    cppbase:
      > ОперацияV2 (FF46h) - размер поля "Наименование товара" 0-128 байт
      > добавлено версионирование
    CI:
      > windows собирается с VisualStudio 2017
  
commit 14d7356c4bfa38400ad80f842947cf4a58947c19  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Fri Jul 6 17:31:36 2018 +0300

    en:
    cppbase:
      > add SOVERSION fix: https://git.shtrih-m.ru/fr_drv_ng/public_issues/issues/29
    fr_drv_ng:
      > CI updates
    
    ru:
    cppbase:
      > добавлено версионирование SOVERSION
    fr_drv_ng:
      > CI обновление скриптов
  
commit 7cf7a284c5fc964a67aa52617ba4fd883102f03e  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Fri Jul 6 11:55:02 2018 +0300

    CI: fix build
  
commit a14a57fdba3e73c6e52ffff4770f84f6f8bea889  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Fri Jul 6 03:45:07 2018 +0300

    en:
        CI Linux: move to gcc 8.1, run platform tests in qemu
        integrity tests with real device
    ru:
        CI Linux: переход на gcc 8.1, запуск тестов в виртуальных машинах qemu
        интеграционные тесты на железе
  
commit aa880eb683a2cf30ac091024ae677fe5f076a4dc  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Fri Jul 6 03:24:58 2018 +0300

    en:
    android_util:
      > fix ACTION_USB_PERMISSION string
    classic:
      > -fno-strict-aliasing for gcc and clang on SWIG generated java wrapper(see http://www.swig.org/Doc3.0/Java.html#Java_compiling_dynamic)
      > add BlockData doc
      > BlockDataHex property just put binary data to BlockData
      > add SOVERSION fix https://git.shtrih-m.ru/fr_drv_ng/public_issues/issues/29
    classic_test:
      > CI crossplatform test prepare
    cppbase:
      > update Catch2 lib
      > cmake: use C99 standard for C code
      > PrintBarcodeLine append data to full line width(cashcore required)
      > win32: SOCKET -1 -> INVALID_SOCKET
    cppbase_test:
      > update Catch2 include
    qclassic:
      > add python qt_wrapper generator
    unifiedpos:
      > use own localtime
    
    ru:
    android_util:
      > поправлена типовая строка для получения ACTION_USB_PERMISSION
    classic:
      > -fno-strict-aliasing для gcc и clang на коде java обертки SWIG (см. http://www.swig.org/Doc3.0/Java.html#Java_compiling_dynamic)
      > добавлено свойство BlockData.
      > BlockDataHex только помещает двоичные данные в BlockData
      > добавлено версионирование SOVERSION см. https://git.shtrih-m.ru/fr_drv_ng/public_issues/issues/29
    classic_test:
      > подготовка к тестированию в виртуальных машинах в CI
    cppbase:
      > обновлена библиотека Catch2
      > cmake: для кода на C использовать стандарт C99
      > PrintBarcodeLine всегда посылать всю ширину линии (КЯ требует)
      > win32: SOCKET -1 -> INVALID_SOCKET
    cppbase_test:
      > обновление Catch2
    qclassic:
      > добавлен генератор qt обёртки над classic
    unifiedpos:
      > использовать потокобезопасный localtime
  
commit bf4c1ed74ee3b61930e79468c1446c7bb093e9ad  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Thu Jun 28 14:03:34 2018 +0300

    ru:
    classic:
      > добавлена документация LineData
      > обновлена документаци PrintBarcodeLine, PrintLine
      > добавлена поддержка свойства SwapBytesMode
      > добавлена документация  LineDataHex
      > PrintLine теперь использует свйоство SwapBytesMode
      > PrintBarcodeLine теперь использует свойство SwapBytesMode
    classic_java:
      > обновлен обертка
    cppbase:
      > ускорено перекодирование utf8->cp1251
      > BarcodeRenderer: реверс данных после масштабирования
      > BarcodeRenderer: использовать linesHeight вместо height
      > Barcode1D: добавлено явное свойство reverseByte
    examples:
      > добавлены примеры PrintLine(printLineSwaps), printBarcodeLineSwaps(PrintBarcodeLine)
    qclassic:
      > сборка с -fPIC
    qclassic_ui
      > сборка с -fPIC
    
    en:
    classic:
      > add LineData doc
      > update PrintBarcodeLine, PrintLine doc
      > add SwapBytesMode property
      > add LineDataHex doc
      > fix: PrintLine now using SwapBytesMode
      > fix: PrintBarcodeLine now using SwapBytesMode
    classic_java:
      > wrapper update
    cppbase:
      > speedup utf8->cp1251 encoding
      > BarcodeRenderer reverse bytes after scale
      > BarcodeRenderer: use linesHeight instead of height
      > Barcode1D: add explicit reverseByte property
    examples:
      > add PrintLine(printLineSwaps), printBarcodeLineSwaps(PrintBarcodeLine) examples
    qclassic:
      > -fPIC on
    qclassic_ui
      > -fPIC on
  
commit 4e52de92829236d02534d70b6f9c401a85570c5e  
Author: Alexey Mednyy <amednyy@shtrih-m.ru>  
Date:   Tue Jun 26 20:48:24 2018 +0300

    v 1.4.0
    ru:
    classic_fr_drv_ng:
      > добавленый свойства MarkingType, GTIN
      > используется swig для генерации jni обертки
      > останавливать службу отправки в ОФД при вызове Disconnect
      > ИЗМЕНЕНИЕ API: std::chrono::system_clock::time_point -> std::time_t
    classic_java_fr_drv_ng:
      > используется swig для генерации jni обертки
    console_test_fr_drv_ng:
      > переход на потокобезопасный localtime
    cppbase_fr_drv_ng:
      > ProtocolV2: исправлена ошибка при рекурсивном вызове функции отправки команды
      > получить максимальную длинну строки в зависимости от используемого протокола DeviceContext::maxStringLength
      > ProtocolV2 оптимизация
      > переход на потокобезопасный localtime
      > команды печати могут принимать длинные строки, если используется альтернативный протокол
      > BarcodeRenderer поправлено выравнивание по-левому краю при использовании с КЯ
    examples:
      > обновлен classic_interface c++ пример
      > обновлен classic_android пример
      > обновлен classic_java пример
    en:
    classic_fr_drv_ng:
      > add MarkingType, GTIN documentation
      > use swig generated jni
      > update doc
      > stop EODSenderService if Disconnect callsed
      > std::chrono::system_clock::time_point -> std::time_t
    classic_java_fr_drv_ng:
      > use swig generated wrapper classes
    console_test_fr_drv_ng:
      > use our localtime
    cppbase_fr_drv_ng:
      > ProtocolV2: fix recursive exchange
      > implement DeviceContext::maxStringLength
      > ProtocolV2 optimized
      > refactor: use own thread-safe localtime everywhere
      > printString commands now can take long strings if using protocol v2
      > BarcodeRenderer fix left alignment on cashcore
    examples:
      > update classic_interface c++ example
      > update android example
      > update classic_java example
