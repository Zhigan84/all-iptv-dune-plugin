# All IPTV

<img src="./1000x1000.png" width="256" height="256">

# [EN]

[Download latest version](https://ohlone-my.sharepoint.com/personal/jberman1_student_ohlone_edu/Documents/all_iptv-1.7.1.zip)

All IPTV is a program for converting m3u / m3u8 playlists of any iptv provider into a plugin for viewing iptv on Dune HD Players.
We do not provide a plugin for a particular provider - you build it yourself!

## Demo Video
[![DEMO](http://img.youtube.com/vi/bny51TSvB7s/0.jpg)](https://www.youtube.com/watch?v=bny51TSvB7s)


## How to use

## Register on one of the Verified IPTV Provaiders

Just drag the m3u / m3u8 playlist from any folder onto the application icon.
Also The Software supports the conversion of multiple playlists in one plugin.


## List of verified IPTV providers

- [sharavoz.tv](http://monitor.lol/www.sharavoz.tv/) 
- [cbilling.tv](http://monitor.lol/http://cbillingtv.net/)
- [ottclub.cc](http://monitor.lol/www.ottclub.cc/)
- [kineskop.club](http://monitor.lol/http://kineskop.club/)
- [antifriz](http://monitor.lol/https://antifriz.tv)
- [shara-tv.org](http://monitor.lol/https://shara-tv.org/)  
- [topiptv.info](http://monitor.lol/https://topiptv.info/)
- [itv.live](http://monitor.lol/https://itv.live/) 
- [edem.tv](http://monitor.lol/edem.tv/)
- [crdru.net](http://monitor.lol/https://www.crdru.net/)
- [ip-tv.club](http://monitor.lol/ip-tv.club/)
- [strah.tv](http://monitor.lol/strah.tv/) 
- [shara.club](http://monitor.lol/www.shara.club/)
- [sovok.tv](http://monitor.lol/sovok.tv/)
- [tv.team](http://monitor.lol/https://tv.team)

## List of verified providers (without archives)


- [fox-tv.fun](http://shop.fox-tv.fun/) ("M3U Plus" playlist recommended)
- [tvoetv.in.ua](https://tvoetv.in.ua/)
- [my.1ott.net](http://my.1ott.net/) ("ottnavm3u8.m3u8" playlist recommended)
- [voron.info](http://voron.info/)
 (required to enable "Группировать по категориям" -> "Спец полями" before downloading a playlist)
- [ottglanz.tv](http://monitor.lol/ottglanz.tv/) recommended HLS playlist 220+ channels.the HLS playlist 450+ is currently in the work on the server side
- [schuriktv.nethouse.ru](https://schuriktv.nethouse.ru/) (supported playlists "Playlist M3U", "SIP Player M3U", "SIP Player M3U8")

- [greatiptv.cc](https://bill.greatiptv.cc/) (you can get a working playlist at t.greatiptv.cc/pl/{your token}/playlist.m3u; playlists from account will not work)
- [kingmodiptv.top](http://kingmodiptv.top/) (supported playlists tv.m3u) 
- [global-iptv.net](http://global-iptv.net/) (supported playlists tv.m3u)
- [ontv.pro](http://monitor.lol/bill.ontv.pro)
- [shura.tv](https://shura.tv/)
- [tvclub.cc](https://tvclub.cc/)


Option to switch playlists in the generated plugin on the settings page

## Working With The Software

If your provider provides the ability to download playlist channels in the formats m3u/m3u8, then with the help of this converter you can turn it into a plugin for Dune HD with your own hands. We tried to reduce the number of settings to a minimum and reduce the conversion process to a few clicks and the plugin is ready to installation.

No services! No paid subscriptions! No restrictions - download the program only once and Convert as much as you want.
During processing, the program will intellectually try to find icons, a schedule, and archives to the list of channels from m3u playlist that you choose to convert.

Unfortunately, the m3u contains only information about groups and channel names, and the channel names themselves are named in any form (often also with typos), that is why a small part of the channels may not be converted in the generated plug-in. In this case, you can watch them, but without additional features. If you have a lot of patience, then you can correct this moment by manually writing configs for them.






## Adding custom icons, groups, and more

You can change the parameters of channels and icons of standard groups.

When converting, the exclusions.xml and conf.yaml files in the program root are taken into program priority, as well as the files <m3u name>.conf.yaml and <m3u name>.exclusions.yaml, which are located next to the m3u playlist. Configs next to m3u have higher priority. Thus, you have the ability to configure part of the parameters equally for all m3u, and some providers of m3u individually.

Examples of settings are in the examples folder.

### Setting Up Groups

The conf.yaml file contains a list of channel groups and icons for them in yaml format.
```yaml
'name of the group from m3u':'icon'
```
The icon can be a local or relative path or http(s) address (during the conversion, such images will be downloaded).

For convenience, you can use the online editor with checking yaml syntax https://onlineyamltools.com/edit-yaml

It is not recommended to change the standard icons in the icons directory, as they will be reset when the program is updated.

### Customize Channels 

The exclusions.xml file allows you to customize icons and channel schedules.
```xml
<?xml version="1.0" encoding="utf-8" ?>
<tv_info>
  <tv_channels>
    <tv_channel>
      <caption>name of the channel from m3u m3u</caption>
      <epg_id>id from vsetv.com</epg_id>
      <tvg_id>id from teleguide.info</tvg_id>
      <icon_url>icon</icon_url>
    </tv_channel>
    <tv_channel>
      <caption>name of the channel from m3u m3u</caption>
      <epg_id>id from vsetv.com</epg_id>
      <tvg_id>id from teleguide.info</tvg_id>
      <icon_url>icon</icon_url>
    </tv_channel>
    <!-- и т.д ... -->
  </tv_channels>
</tv_info>
```
Id from vsetv.com can be found from the channel url type http://www.vsetv.com/schedule_channel_1071_day_2019-04-04.html The number between channel_ and _day is id (1071).

Id from teleguide.info find out from the url of the channel like https://www.teleguide.info/kanal1006_20190326.html The number between kanal and _ is id (1006).

The icon can be a local absolute or relative path or http(s) address (during the conversion, such images will be downloaded).

### Main application icon

Like setting up group icons in conf.yaml, add a line or change an existing one.
```yaml
_:'icon'
```

## Questions and answers

> Archives do not work.

There are a lot of providers, they appear and disappear. At the same time, there is no single standard for specifying the syntax of archives via the m3u playlist. Each provider provides them as they feel needed to. We have added and tested the most popular providers in our opinion.

If your provider is not in the list of supported, then write to us in the telegram group [@all_iptv_dune_plugin](https://taraflex.github.io/tg/#https://t.me/all_iptv_dune_plugin) or in [issues](https://github.com/Slev7nm/all-iptv-dune-plugin/issues) - we will add it.

> Configs inconvenient to edit. Can you do something about it?

Maybe someday we will add a constructor instead of config files to the gui application, but probably not very soon.

> Do you plan to open the source of the application?

Not yet. They are fast coded and not commented , We are ashamed of the source code. the source of php plugin can be viewed by unpacking the generated zip archive.

> Your standard pictures for channel groups are terrible.

We do not mind if someone draws them more decently or offers alternative options with a free license.

> My iptv provider does not provide m3u. Can I still use your program somehow?

Write us in the telegram group [@all_iptv_dune_plugin](https://taraflex.github.io/tg/#https://t.me/all_iptv_dune_plugin) or in [issues](https://github.com/Slev7nm/all-iptv-dune-plugin/issues). We will consider the possibility of adding additional formats to the parser.

> I want to help in the development! How?

We also want to help us! Right now, we need a designer to draw application icons and channel groups. Write to the telegram group [@all_iptv_dune_plugin](https://taraflex.github.io/tg/#https://t.me/all_iptv_dune_plugin) or to [issues](https://github.com/Slev7nm/all-iptv-dune-plugin/issues). 
Well, of course, you can also help with finances.

[<img src="https://az743702.vo.msecnd.net/cdn/kofi5.png?v=2" width="202" alt="https://ko-fi.com/alliptv"/>](https://ko-fi.com/alliptv)

> Why does the program need access to the network?

To download the unrecognizable icons list of channels from vsetv.com and teleguide.info and channel icons, to well as to check for updates and also to send erorrs if there were in proccess of convertion

The program comes with a certain set of icons, but it is not always enough.

You can view with the sniffer that no additional data is transmitted.

> I do not want to send anything anywhere! Can you turn off your godless telemetry?

Yes. Simply create the notelemetry.txt file in the application directory. Remember that the collected error statistics helps to improve the 
algorithms for selecting icons and channel schedules.

> So the access tokens in my playlists are safe?
   
Yes

> Nothing works! You are the hands!

Well... nothing working at all... probably...

The world is ruled by money! So If You Left Handed Hands This can be compensated by the involvement of additional developers, with two normal working hands.

[<img src="https://az743702.vo.msecnd.net/cdn/kofi5.png?v=2" width="202" alt="https://ko-fi.com/alliptv"/>](https://ko-fi.com/alliptv)

> I want more features! Why are you so slow?

¯\\_(ツ)_/¯

# [RU]

<img src="./1000x1000.png" width="256" height="256">

[Скачать последнюю версию](https://ohlone-my.sharepoint.com/personal/jberman1_student_ohlone_edu/Documents/all_iptv-1.7.1.zip)

All IPTV - программа для конвертации m3u/m3u8 плейлиста любого iptv провайдера в плагин для просмотра iptv на приставках Dune HD.
Мы не предоставляем плагин под какого-то конкретного провайдера - вы собираете его сами!

демо видео

[![DEMO](http://img.youtube.com/vi/bny51TSvB7s/0.jpg)](https://www.youtube.com/watch?v=bny51TSvB7s)

## Как использовать

Просто перетащите m3u/m3u8 плейлист из любой папки на иконку приложения.
Также поддерживается конвертация нескольких плейлистов в один плагин.



Переключать плейлисты в сгенерированном плагине вы сможете на странице настроек. 


## Список проверенных провайдеров 

- [sharavoz.tv](http://monitor.lol/www.sharavoz.tv/) 
- [cbilling.tv](http://monitor.lol/https://cbilling.tv/)
- [ottclub.cc](http://monitor.lol/www.ottclub.cc/)
- [kineskop.club](http://monitor.lol/http://kineskop.club/)
- [antifriz](http://monitor.lol/https://antifriz.tv)
- [shara-tv.org](http://monitor.lol/https://shara-tv.org/)  
- [topiptv.info](http://monitor.lol/https://topiptv.info/)
- [itv.live](http://monitor.lol/https://itv.live/) 
- [edem.tv](http://monitor.lol/edem.tv/)
- [crdru.net](http://monitor.lol/https://www.crdru.net/)
- [ip-tv.club](http://monitor.lol/ip-tv.club/)
- [strah.tv](http://monitor.lol/strah.tv/) 
- [shara.club](http://monitor.lol/www.shara.club/)
- [sovok.tv](http://monitor.lol/sovok.tv/)


## Список проверенных провайдеров (без архивов)

- [ip-tv.club](http://monitor.lol/ip-tv.club/) 
- [fox-tv.fun](http://shop.fox-tv.fun/) (рекомендуется "M3U Plus" плейлист)
- [tvoetv.in.ua](https://tvoetv.in.ua/)
- [strah.tv](http://monitor.lol/strah.tv/) (рекомендуется включить опцию "MPEG-2 TS" перед скачиванием плейлиста)
- [my.1ott.net](http://my.1ott.net/) (рекомендуется "ottnavm3u8.m3u8" плейлист)
- [shara.club](http://monitor.lol/www.shara.club/)
- [voron.info](http://voron.info/)
- [sovok.tv](http://monitor.lol/sovok.tv/) (требуется включить "Группировать по категориям" -> "Спец полями" перед скачиванием плейлиста)














## Добавление собственных иконок, групп и прочего

Вы можете изменять параметры каналов и иконки стандартных групп.

При конвертации учитываются файлы exclusions.xml и conf.yaml в корне програмы а также файлы <имя m3u>.conf.yaml и <имя m3u>.exclusions.yaml, лежащие рядом с конвертируемым m3u плейлистом. Конфиги рядом с m3u имеют больший приоритет. Таким образом вы имеет возможность сконфигурировать часть параметров одинаково для всех m3u, а часть индивидуально. 

Примеры настроек смотрите в папке examples.

### Настройка групп

Файл conf.yaml содержит список групп каналов и иконки к ним в yaml формате 
```yaml
'имя группы из m3u':'иконка'
```
Иконка может быть локальным абсолютным или относительным путем либо http(s) адресом (во время конвертации такие изображения будут скачаны).

Для удобства можно воспользоваться онлайн редактором с проверкой yaml синтаксиса https://onlineyamltools.com/edit-yaml

Не рекомендуется изменять стандартные иконки в папке icons, так как они будут перезатерты при обновлении программы.

### Натройка каналов

Файл exclusions.xml позволяет настроить иконки и расписание каналов.
```xml
<?xml version="1.0" encoding="utf-8" ?>
<tv_info>
  <tv_channels>
    <tv_channel>
      <caption>имя канала из m3u</caption>
      <epg_id>id c vsetv.com</epg_id>
      <tvg_id>id c teleguide.info</tvg_id>
      <icon_url>иконка</icon_url>
    </tv_channel>
    <tv_channel>
      <caption>имя канала из m3u</caption>
      <epg_id>id c vsetv.com</epg_id>
      <tvg_id>id c teleguide.info</tvg_id>
      <icon_url>иконка</icon_url>
    </tv_channel>
    <!-- и т.д ... -->
  </tv_channels>
</tv_info>
```
Id c vsetv.com можно узнать из url канала вида http://www.vsetv.com/schedule_channel_1071_day_2019-04-04.html Число между channel_ и _day есть id (1071).

Id c teleguide.info узнать из url канала вида https://www.teleguide.info/kanal1006_20190326.html Число между kanal и _ есть id (1006).

Иконка может быть локальным абсолютным или относительным путем либо http(s) адресом (во время конвертации такие изображения будут скачаны).

### Главная иконка приложения

Подобно настройке иконок групп в conf.yaml добавьте строку или измените существующую
```yaml
_:'иконка'
```

## Вопросы и ответы

> Архивы не работают.

Провайдеров очень много, они появляются и исчезают. Одновременно с этим не существует единого стандарта указания расположения архивов через m3u плейлист. Каждый провайдер предоставляет их как захочет. Мы добавили и протестировали наиболее популярных провайдеров на наш взгляд.

Если вашего провайдера нет в списке поддерживаемых, то напишите нам в telegram группу [@all_iptv_dune_plugin](https://taraflex.github.io/tg/#https://t.me/all_iptv_dune_plugin) или в [issues](https://github.com/Slev7nm/all-iptv-dune-plugin/issues) - мы его добавим.

> Конфиги неудобно редактировать. Можете сделать с этим что-нибудь?

Возможно когда-нибудь мы добавим в приложение gui конструктор вместо конфигов, но наверное очень не скоро.

> Планируется открыть исходники приложения?

Пока нет. Они кошмарны. Нам стыдно. Исходники php плагина можно посмотреть, распаковав генерируемый zip архив.

> Ваши стандартные картинки для групп каналов ужасны.

Мы не против, если кто-нибудь нарисует их нам поприличнее или предложит альтернативные варианты со свободной лицензией.

> Мой iptv провайдер не предоставляет m3u. Могу ли я все равно как-нибудь использовать вашу программу?

Напишите нам в telegram группу [@all_iptv_dune_plugin](https://taraflex.github.io/tg/#https://t.me/all_iptv_dune_plugin) или в [issues](https://github.com/Slev7nm/all-iptv-dune-plugin/issues). Мы рассмотрим возможность добавления в парсер дополнительных форматов.

> Хочу помочь в развитии! Как?

Мы тоже хотим, чтобы нам помогали! Прямо сейчас нам нужен дизайнер, чтобы отрисовать иконки приложения и групп каналов. Пишите в telegram группу [@all_iptv_dune_plugin](https://taraflex.github.io/tg/#https://t.me/all_iptv_dune_plugin) или в [issues](https://github.com/Slev7nm/all-iptv-dune-plugin/issues).
Ну и финансами естественно тоже можете помогать.

[<img src="https://az743702.vo.msecnd.net/cdn/kofi5.png?v=2" width="202" alt="https://ko-fi.com/alliptv"/>](https://ko-fi.com/alliptv)

> Зачем программе требуется доступ в сеть?

Чтобы скачать неизвестные иконки каналов с vsetv.com и teleguide.info, для проверки обновлений, а также для отправки ошибок о конвертации. 

С программой поставляется определенный набор иконок, но его не всегда достаточно.

Вы можете просмотреть сниффером, что никакие дополнительные данные не передаются. 

> Я не хочу ничего никуда отправлять! Можно отключить вашу богомерзкую телеметрию?

Да. Просто создайте файл notelemetry.txt в директории приложения. Помните, что собираемая статистика ошибок помогает улучшать алгоритмы подбора иконок и расписаний каналов.  

> Значит токены доступа в моих плейлистах в безопасности?

Да. 

> Ничего не работает! Вы рукожопы!

Нуу... совсем ничего не работать не может... наверное...

Миром правят деньги! Часть рукожопости можно компенсировать привлечением дополнительных разработчиков, с более прямыми руками. 

[<img src="https://az743702.vo.msecnd.net/cdn/kofi5.png?v=2" width="202" alt="https://ko-fi.com/alliptv"/>](https://ko-fi.com/alliptv)

> Хочу больше фичь! Почему вы такие медленные? 

¯\\_(ツ)_/¯
