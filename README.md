# /dsd/ Thread FAQ

### TL;DR процветающий шапка

**Q: Я простой рабочий Иван город Тверь, желать ставить много игры и распространять много хвалебные материалы твёрдый стержень товарищ Xi, что вы можете подсказывать?**

A: Любой накопитель на основе CMR технологии, не обладающий собственными технологиями энергосбережения:
- WD: Purple, Black, Gold, SE, Red Pro (?)
- Seagate: SkyHawk, Constellation, IronWolf(?), Exos [Таблица производителя](http://https://www.seagate.com/ru/ru/internal-hard-drives/cmr-smr-list/ "Таблица производителя")
- Toshiba: P300 (HDWD1xxx), ряд S300 (см. сводку), xxxx**ACA** (наследие Hitachi, некоторые модели SMR!)
- Гелиевые диски от WD и Hitachi (статистики по ним пока ещё нет)

[Пользовательская сводка SMR/CMR](https://nascompares.com/answer/list-of-wd-cmr-and-smr-hard-drives-hdd/ "Пользовательская сводка SMR/CMR")

**Q: Что сказать про SMR диск, магазин количество много цена весьма низкий?**

A: Некачественный убыток тайваньский собака, много отключения и слабый скорость, голова болит от проблем.

**Q: Что насчет внешний? Архивировать каждый запись созыв компартии, полка хранение, просвещать подрастающее поколение.**

A: Практически все современные внешние ЖД собираются на основе SMR дисков самых отстойных линеек, проблемы всё те же самые. Их надёжность вызывает вопросы. 

**Q: Хотеть надежность! Запись созыв компартии ценный материал!**

A: Ни один из современных производителей ЖД не гарантирует надёжность хранения данных. Хочешь быть спокойным за свой архив - храни их в нескольких хранилищах одновременно: RAID1/5/6, облака, оптические, ленточные накопители.

**Q: Выглянуть на барахолку, много вкусный предложения, подводный камень?**

A: Неизвестно как эксплуатировавшиеся, возможно падавшие, диски без тестов. Не стоит принимать к рассмотрению.

**Q: Обладать старый записная книжка, какой накопитель посоветовать?**

A: Практически все современные ноутбучные диски идут с SMR и в качестве основного накопителя не годятся. С учётом же уравнения цен на гигабайт вообще рекомендуется рассмотреть вариант покупки SSD.

### Как взять жёсткий диск и не наебаться

Прежде всего стоит понимать, что после широкого распространения твердотельных накопителей потребительский сегмент HDD сходит на нет, соответственно, производители всё больше экономят на проектировании и производстве накопителей данного класса. Также стоит учитывать конъюнктуру рынка: в основном жёсткие диски берут люди а) которым не хватает денег на ёмкий SSD, а все игры ставить куда-то нужно; б) под большой массив генерируемых пользователем данных - NAS, видеонаблюдение в) энтузиасты, собирающие/раздающие какие-либо аудио/видео/программные/иные материалы, под которые неминуемо требуются дисковые пространства и SSD для данных случаев просто не подходит; г) майнинг на фоне очередной волны спекуляций на криптовалютных биржах; д) для сборки бюджетного комплекта и последующей перепродажи. Первые три не предъявляют каких-либо особенных требований ни к работе диска на запись, ни к работе диска на чтение, что в принципе понимается производителями как отсутствие потребности в оных вообще. В случае же с пунктом "в" количество энтузиастов исчезающе мало для какого-либо влияния на рынке, а про последний говорить, полагаю, не имеет смысла.



По этой самой причине сначала Seagate, а потом и остальные участники рынка, внедрили технологию черепичной записи (SMR). Подробности этой технологии ты, при желании, найдешь в интернете, но для вопроса выбора накопителя под свои задачи главное, что стоит иметь ввиду - низкая производительность в ряде задач, в первую очередь на операциях записи. В отличие от накопителя с традиционной записью (PMR/CMR), в котором есть две сущности - оперативная память для небольшого кэша операций и собственно магнитная пластина для данных, в диске с черепичкой введена так же третья сущность - CMR кэш, на который непосредственно пишутся подаваемые на диск данные, а уже потом распределяются по магнитной пластине, для чего также увеличена оперативная память, т.к. при обновлении данных на пластине требуется заново переписать некоторое количество уже имеющихся данных, и всё это дело нужно где-то хранить. В чём-то SMR напоминает современный ссд с SLC кэшем, но, в отличие от последнего, задержки между обращениями больше на порядки. Фактически же при активной записи диск с черепичкой гоняет блок головок там, где диск с традиционной записью просто пишет данные в линию. Более того, по исчерпанию CMR кэша диск начинает активно писать в SMR область, что сильно проваливает скорость (до единиц мегабайт). При чтении особых проблем не возникает ввиду устройства блока головок, но в смешанном режиме всё тоже будет достаточно печально.

В конечном итоге при покупке диска SMR имеем:
- просаженную производительность диска при длительной записи
- повышенную скорость износа актуатора блока магнитных головок
- лучшую энергоэффективность за счет меньшего количества пластин



Разница в цене между дисками с SMR и CMR технологиями записи может достигать 20%, но может и не достигать. Если ты собираешься использовать диск для частой записи - скидывание видосов с попоек, торрентокачалка, использование в СХД и с использованием RAID и/или применением журналируемых ФС, хранение основной копии БД от региональной наноборды и т.д. - диск с SMR технологией определенно не для тебя. В остальных случаях стоит оценить ситуацию на рынке и понять, есть ли смысл в экономии пары сотен рублей. В целом, SMR скорее способ явной экономии чем инновация.

### SSHD, RPM, APM, AAM и прочие аббревиатуры

В те времена, когда мониторы были большие, экраны маленькие, Билл Гейтс еще возглавлял совет директоров одной маленькой мягкой фирмы и рвал волосы от сорванных сроков по релизу очередной пушки-гонки с нескучными обоями, а скорости тогдашних накопителей едва-ли превышали таковые у рядовой китайской флешки с алиэкспресса, эти самые накопители поддерживали ряд конфигурируемых (и нет) пользователем технологий, управляющих шумом, нагревом и скоростями. Те времена давно прошли, технологии забыты, поэтому единственное, что тебе стоит принимать во внимание - скорость вращения магнитных пластин (RPM) и поддержка ошметков технологии APM.

От скорости вращения напрямую зависит скорость доступа к секторам в пределах одного семейства и, как не совсем очевидное следствие - нагрев накопителя, если 5400RPM диск при комнатной температуре в 20 градусов нагревается весьма слабо - до 30-35 градусов, и в каких-либо дополнительных телодвижениях не нуждается, то 7200RPM собрат практически всегда набирает 45 и выше, в связи с чем его длительная работа без активного обдува нежелательна (обычно верхняя граница допустимой температуры у накопителей порядка 50 градусов). В случае же потребительских характеристик 7200RPM не так уж интересен ввиду отсутствия заметной прибавки в производительности, фактически после того, как человечество перестало использовать жесткий диск в качестве системного с хранением на нём файла подкачки (swap), эта самая необходимость попросту отвалилась. Если ты крутишь какой-либо сервис, требующий разбещения своих данных на жестком диске и активного к ним обращения - посмотри на связку HDD + SSD + flashcache (если пердоля) или сопоставимый аналог под Windows (PrimoCache? Сам найдешь).


Ошмётки AAM в свою очередь проявляются в наличии автопарковки блока головок при бездействии энное количество времени во имя защиты данных от предательского толчка рукой/ногой в крышку системного блока. Имеются они не на всех дисках: например, самые ходовые диски от WD линеек Green и, теперь уже, Blue обладают зашитым интервалом автопарковки в 8 секунд; Red диски от того же производителя имеют более щадящий интервал - около 48 секунд или выше; накопители 2.5" (ноутбучного) формата любого производителя обладают минимальными интервалами для минимизации выхода из строя при падении ноутбука. Основные проблемы, к которым приводит малый интервал автопарковки - подлагивания при обращении из-за постоянной парковки-распарковки головок, и износ актуатора. При редких обращениях к содержимому диска особой погоды не составляют, но в качестве ёмкого накопителя в компьютер под контент всякого рода такие диски - не лучший выбор. Особняком стоят ноутбучные варианты, там выбрать особо не из чего.


Последняя, уже вымирающая сама по себе технология - гибридные накопители SSHD. Сказать за них особо нечего, смысл покупки таковых с расчётом на повышенную производительность исчезающе мал - SSD кэш недостаточно ёмкий чтобы покрыть какую-то часть особо востребованных операций чтения. Однако он может быть полезен для массивов с расчетом на частую случайную запись, например, используемых в качестве торрентокачалки. Кроме того, NAND подвержен износу, что может привести к проблемам в будущем. Просто напомню про flashcache, и закроем эту тему.
