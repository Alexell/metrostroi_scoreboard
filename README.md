# Metrostroi Scoreboard Pro

**Created by:** Alexell

**Website:** https://alexell.ru/
 
![Metrostroi Scoreboard Pro](https://mss-project.org/images/addons/metrostroi_scoreboard.jpg)

**Описание:**

Продвинутая таблица с игроками, разработанная специально для серверов Метростроя. MScoreboard написан с нуля, из старых SUI Scoreboard были позаимствованы лишь малые части кода.

**Аддон полностью совместим с [GitHub версией Metrostroi](https://github.com/metrostroi-repo/MetrostroiAddon).**

**Новая панель действий для каждого игрока:**
* Появляется при нажатии ЛКМ по нику игрока
* Кнопка открытия профиля игрока на сайте. По умолчанию открывает профиль на сайте Метростроя, но вы можете заменить ссылку на свою с помощью добавления в `server.cfg` конвары `mscoreboard_website`. Необходимо прописывать ссылку ровно до того момента, как начнется SteamID игрока, он будет подставляться аддоном. Например для сайта Метростроя это выглядело бы так: `mscoreboard_website "https://metrostroi.net/profile/"`
* Кнопку открытия профиля игрока на сайте можно полностью отключить, если указать ноль, т.е. `mscoreboard_website 0`.
* Кнопка открытия профиля в Metadmin/Metadmin Extended (при наличии права ulx prid)
* Кнопка телепорта к игроку (при наличии права ulx goto)
* Кнопка телепорта к поеду/в поезд игрока (при наличии на сервере **Metrostroi Advanced** и права ulx traintp или при наличии права ulx traingoto в предстоящем обновлении Метростроя)
* **Также пара возможностей для команды сервера:**
* Кнопка "Кик" (при наличии права ulx kick), кик происходит мгновенно с сообщением "Кикнут администратором сервера".
* Кнопка "Бан" (при наличии права ulx ban), вызывает меню бана ULX, вам остается только указать причину и срок действия бана.

**Другие возможности:**
* Уведомление в чат о совпадающих номерах маршрута
* Возможность замьютить всех игроков разом (отдельная кнопка внизу справа)
* Всплывающий слайдер для управления громкостью микрофона каждого игрока (ПКМ по значку динамика)
* Локализация (RU, EN, KO)
* Поддержка мониторов шириной от 1280px
* Кастомизация цветов на клиентах
* Отображается общее число игроков и вагонов на сервере
* Отображается время клиента и время сервера
* Отображаются номера маршрута для всех существующих составов, включая 81-717.6
* Отображается кол-во вагонов игроков
* Отображается тип состава
* Отображается путь, текущая станция или перегон (с указанием предыдущей и следующей станции) для каждого состава
* Для отображения часов в аддон встроен Utime

**Необходимые аддоны:**

* Metrostroi
* ULib

**Установка на сервер:**
* Удалить из коллекции сервера любой другой Scoreboard, который есть в коллекции
* Удалить с сервера **utime**, если имеется (его нет в Steam Workshop, поэтому я добавил его в аддон)
* Добавить в коллекцию сервера [Metrostroi Scoreboard Pro](https://steamcommunity.com/sharedfiles/filedetails/?id=1910844812)

## Примечания
Для правильного отображения путей и станций требуются корректные **треки** на картах, а также правильно расставленные **gmod_track_platform**.
На станциях всегда отображается путь и название станции. В перегонах между станциями всегда отображается путь, название предыдущей станции и название следующей станции.

В случае, когда нужная информация из треков и платформ не получена, для определения местоположения состава используются точки из **Metrostroi.StationConfigurations**. В случаях, когда местопложение не найдено всеми способами, отображается **N/A**.
**N/A** всегда будет отображаться на парковых путях, в перегоне из депо на главные пути, при движении из тупика на стацию. Это нормально.

Если на какой-либо карте у вас неверно отображаются пути или станции, попробуйте найти причину, проверив треки и gmod_track_platform на карте и обратитесь к автору карты для исправления.
