  # Кроссплатформенный Драйвер ФР на C++(fr_drv_ng)

  В этом репозитории распространяются сборки драйвера fr_drv_ng и осуществляется поддержка.  
  [Примеры](https://github.com/shtrih-m/fr_drv_ng_examples)
  [Обратная связь](https://github.com/shtrih-m/fr_drv_ng/issues)

  ## Общие
  #### Поддерживаемые ОС
  * Windows XP и выше
  * Linux
  * Android
  * MacOS Mohave и выше
  * iOS 9.0 и выше

  ## Скачать 
  Cборка и тестирование осуществляется в CI проекта. Релизы выкладываются на [github](https://github.com/shtrih-m/fr_drv_ng/releases)  
  * **fr_drv_ng_android_**$ARCH - сборки под Android
  * **fr_drv_ng_java_wrappers** - java обертки для classic и unifiedpos интерфейсов
  * **fr_drv_ng_linux_**$ARCH - сборки под Linux
  * **fr_drv_ng_linux_i486_ok** - сборка под старые ядра Linux(гарантирована работа на 2.6.32, собрано с glibc 2.23)
  * **fr_drv_ng_windows_**$ARCH - сборки под Windows
  * **fr_drv_ng_darwin_x86_64** - сборка под MacOS
  * **fr_drv_ng_iOS_multarch** - сборка под iOS

  ### Содержимое сборок:
  #### Во всех сборках под ОС находятся нативные файлы библиотек(статические и динамические сборки):
  * **cppbase_fr_drv_ng** - общий код, базовый функционал. команды, протоколы и.т.д., линкуется только со стандартной библиотекой
  * **classic_fr_drv_ng** - "классический интерфейс" аналог Драйвер ФР под windows, линкуется только со стандартной библиотекой и cppbase_fr_drv_ng
  * **qclassic_fr_drv_ng** - Qt обертка вокруг classic с сигналами/слотами, свойства вынесены в Q_PROPERTY, линкуется только с Qt5Core и classic_fr_drv_ng
  #### Программы:
  * **console_test_fr_drv_ng** - консольный тест для встраивания в скриптовые окружения
  #### Утилиты
  * **android_util_fr_drv_ng** - android aar-java библиотека с функциями-утилитами под android
  * **classic_java_fr_drv_ng** - java обертка для **classic_fr_drv_ng**
  #### Дополнительно
  * В сборках под Android лежит библиотека STL с которой собирался релиз **libc++_shared.so**, необходимо включить в приложение
  * В сборках под Linux в поддиректории libs лежат библиотеки libc, STL с которыми собирался релиз, можно линковаться с ними
  #### С++ Headers
  * **classic_interface.h** - заголовочный для classic_interface
  * **QClassicFrDrvNg,qclassic_interface.h** - Qt-style заголовочные для qclassic_fr_drv_ng 

  ## Документация
  * **console_test_fr_drv_ng** - запусть тест в терминале с аргументом --help
  * **classic_fr_drv_ng** - общая справка [здесь](https://exam.shtrih-m-partners.ru/assets/materials/DriverKKT_Guide_415_16_11_20_.zip), справка для реализованных методов доступна в заголовочном файле classic_interface.h в формате doxygen. Заголовочный в сборках рядом с нативными библиотеками.
  * **WIKI** - [идёт наполнение](https://github.com/shtrih-m/fr_drv_ng/wiki)
