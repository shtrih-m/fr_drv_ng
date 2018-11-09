commit ac7dadcf4dfaf0d9d72becfd3c34ec8cbc79465d
Author: Alexey Mednyy <swexru@gmail.com>
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
Author: Alexey Mednyy <swexru@gmail.com>
Date:   Thu Nov 1 17:27:31 2018 +0300

    en:
    cppbase:
        > follow up fix StartFsFiscalModeCloseCommand response parsing
    
    ru:
    cppbase:
        > продолжение исправления разбора ответа на команду StartFsFiscalModeCloseCommand.


commit 86fabefaac0e37e43cf33d8a4c0c591ddff366bd
Author: Alexey Mednyy <swexru@gmail.com>
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
Author: Alexey Mednyy <swexru@gmail.com>
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
Author: Alexey Mednyy <swexru@gmail.com>
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
Author: Alexey Mednyy <swexru@gmail.com>
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
Author: Alexey Mednyy <swexru@gmail.com>  
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
Author: Alexey Mednyy <swexru@gmail.com>  
Date:   Tue Sep 11 00:26:00 2018 +0300

    en:
    CI: build qclassic(Qt classic_fr_drv_ng wrapper with properties,signals,slots)
    
    ru:
    CI: сборка библиотеки qclassic(Qt обертка classic_fr_drv_ng с поддержкой свойств, сигналов и слотов)
  
commit ccc0ad78d77fec93bd22813acfb4e28ef8f212d9  
Author: Alexey Mednyy <swexru@gmail.com>  
Date:   Tue Sep 4 22:33:42 2018 +0300

    en:
    classic:
      > implemented ReadErrorDescription method
    
    ru:
      > реализован метод ReadErrorDescription
  
commit 961132951b75b8f72e2cd6eb3d99f449df4c8f92  
Author: Alexey Mednyy <swexru@gmail.com>  
Date:   Mon Sep 3 19:19:02 2018 +0300

    en:
    classic_test:
       > update test for CI
    
    ru:
    classic_test:
       > обновлены тесты для CI
  
commit b5c3a03db5bbe31bc69b5aba8d60ba456976616e  
Author: Alexey Mednyy <swexru@gmail.com>  
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
Author: Alexey Mednyy <swexru@gmail.com>  
Date:   Thu Aug 30 14:24:38 2018 +0300

    add github fr_drv_ng submodule
  
commit b03c9df222804194cca89578aae43a02ae6eac04  
Author: Alexey Mednyy <swexru@gmail.com>  
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
Author: Alexey Mednyy <swexru@gmail.com>  
Date:   Mon Aug 20 17:35:35 2018 +0300

    en:
    ci: fix android jar build
    ru:
    ci: поправлена сборка jar библиотеки под android
  
commit 9d1b63e87926eed283a766eb60157fdaa780d8ac  
Author: Alexey Mednyy <swexru@gmail.com>  
Date:   Mon Aug 20 17:27:23 2018 +0300

    en:
    cppbase:
      > fixed FF0A on Cashcore(gives date without time) see https://git.shtrih-m.ru/fr_drv_ng/fr_drv_ng/issues/53
    
    ru:
    cppbase:
      > на устройствах с КЯ команда FF0A возкращает дату "Отчета о состоянии расчетов" без времени
  
commit 8b08067bd9b176983815a8d3e3bd170b23c397b1  
Author: Alexey Mednyy <swexru@gmail.com>  
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
Author: Alexey Mednyy <swexru@gmail.com>  
Date:   Wed Aug 8 20:53:27 2018 +0300

    en:
    cppbase:
      > Barcode1D fix workaround models
    
    ru:
    cppbase:
      > Barcode1D поправлены модели для обхода проблемы с переворотом
  
commit 0d99faaec11cdddb8b60222ac153af3aaf3dc85a  
Author: Alexey Mednyy <swexru@gmail.com>  
Date:   Tue Aug 7 14:42:45 2018 +0300

    en:
    cppbase_test:
      > fix barcode aligned tests
    
    ru:
    cppbase_test:
      > поправлены тесты выравнивания ШК
  
commit dcc5109192aa3fbe6ee95ab9151dbc3ad28933f9  
Author: Alexey Mednyy <swexru@gmail.com>  
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
Author: Alexey Mednyy <swexru@gmail.com>  
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
Author: Alexey Mednyy <swexru@gmail.com>  
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
Author: Alexey Mednyy <swexru@gmail.com>  
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
Author: Alexey Mednyy <swexru@gmail.com>  
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
Author: Alexey Mednyy <swexru@gmail.com>  
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
Author: Alexey Mednyy <swexru@gmail.com>  
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
Author: Alexey Mednyy <swexru@gmail.com>  
Date:   Wed Jul 11 13:52:39 2018 +0300

    en:
    classic:
      > fixed FNSendItemCodeData for tobacco products
    
    ru:
    classic:
      > исправлен метод FNSendItemCodeData для табачных изделий
  
commit d01ab0507e4c9b0acdc8f6f7727d01887ae68da2  
Author: Alexey Mednyy <swexru@gmail.com>  
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
Author: Alexey Mednyy <swexru@gmail.com>  
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
Author: Alexey Mednyy <swexru@gmail.com>  
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
Author: Alexey Mednyy <swexru@gmail.com>  
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
Author: Alexey Mednyy <swexru@gmail.com>  
Date:   Fri Jul 6 11:55:02 2018 +0300

    CI: fix build
  
commit a14a57fdba3e73c6e52ffff4770f84f6f8bea889  
Author: Alexey Mednyy <swexru@gmail.com>  
Date:   Fri Jul 6 03:45:07 2018 +0300

    en:
        CI Linux: move to gcc 8.1, run platform tests in qemu
        integrity tests with real device
    ru:
        CI Linux: переход на gcc 8.1, запуск тестов в виртуальных машинах qemu
        интеграционные тесты на железе
  
commit aa880eb683a2cf30ac091024ae677fe5f076a4dc  
Author: Alexey Mednyy <swexru@gmail.com>  
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
Author: Alexey Mednyy <swexru@gmail.com>  
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
Author: Alexey Mednyy <swexru@gmail.com>  
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
