![Huginn](https://raw.github.com/cantino/huginn/master/media/huginn-logo.png "Your agents are standing by.")

---

## Что такое Huginn?

Huginn - это система для создания агентов, которые выполняют автоматизированные задачи для вас онлайн. Они могут читать в Интернете, следить за событиями и принимать меры от вашего имени. Агенты Хугинна создают и потребляют события, распространяя их вдоль ориентированного графа. Думайте об этом как о взломанном Yahoo! Трубы плюс IFTTT на вашем собственном сервере. Вы всегда знаете, у кого есть ваши данные. Ты сделаешь.

![the origin of the name](https://raw.githubusercontent.com/cantino/huginn/master/doc/imgs/the-name.png)

#### Вот несколько вещей, которые вы можете сделать с Хугинном:

- Отслеживайте погоду и получайте электронные письма, когда завтра будет дождь (или снег) («Не забывайте свой зонтик!»)
- Перечислите термины, которые вас интересуют, и получайте электронные письма, когда их появление в Twitter меняется. (Например, хотите знать, когда что-то интересное произошло в мире машинного обучения? Хьюгинн будет смотреть термин «машинное обучение» в Твиттере и сообщать вам, когда в дискуссии будет всплеск.)
- Следите за авиаперелетами или покупками
- Следите за названиями своих проектов в Твиттере и получайте обновления, когда люди их упоминают
- Очистите веб-сайты и получайте электронные письма, когда они меняются
- Подключитесь к Adioso, HipChat, Basecamp, Growl, FTP, IMAP, Jabber, JIRA, MQTT, nextbus, Pushbullet, Pushover, RSS, Bash, Slack, StubHub, API-интерфейсам для перевода, Twilio, Twitter, Wunderground и Weibo, чтобы назвать несколько ,
- Отправляйте дайджесты по электронной почте с вещами, которые вас интересуют в определенное время в течение дня
- Отслеживайте количество высокочастотных событий и отправляйте SMS в моменты их всплеска, такие как термин «чрезвычайная ситуация в Сан-Франциско»
- Отправляйте и получайте WebHooks
- Запустите пользовательские функции JavaScript или CoffeeScript
- Отслеживайте свое местоположение с течением времени
- Создайте рабочие процессы Amazon Mechanical Turk в качестве входных или выходных данных агентов (агент Amazon Turk называется HumanTaskAgent). Например: «Один раз в день попросите 5 человек сделать забавную фотографию кота; отправьте результаты еще 5 людям для оценки; отправьте фотографию с самым высоким рейтингом 5 людям для забавного заголовка; отправьте 5 финальным людям, чтобы оценить самая смешная подпись; наконец, разместите самую лучшую фотографию в моем блоге. "

[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/cantino/huginn?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Присоединяйтесь к нам в нашей [комнате](https://gitter.im/cantino/huginn) [Gitter,](https://twitter.com/tectonic) чтобы обсудить проект и [следите](https://twitter.com/tectonic) за обновлениями [@tectonic](https://twitter.com/tectonic) по мере развития [Хугинна](https://twitter.com/tectonic) .

### Присоединяйтесь к нам!

Хотите помочь с Хугинном? Все материалы приветствуются! Вы можете улучшить пользовательский интерфейс, [добавить новых агентов](https://github.com/cantino/huginn/wiki/Creating-a-new-agent) , написать [документацию и учебные пособия](https://github.com/cantino/huginn/wiki) или попробовать [решить проблемы, помеченные # help-wanted](https://github.com/cantino/huginn/issues?direction=desc&labels=help-wanted&page=1&sort=created&state=open) . Пожалуйста, ответьте, добавьте спецификации и отправьте запросы на включение!

Действительно хотите исправить или функцию? Хотите решить некоторые проблемы сообщества и заработать дополнительные деньги на кофе? Взгляните на [текущие награды на Bountysource](https://www.bountysource.com/trackers/282580-huginn) .

У вас есть отличная идея, но вы еще не готовы внести свой вклад? Перейдите к нашей [официальной ветке 'предложить агента'](https://github.com/cantino/huginn/issues/353) и сообщите нам!

## Примеры

Пожалуйста, ознакомьтесь с [вводной заставкой Хугинна](http://vimeo.com/61976251) !

А теперь несколько примеров скриншотов. Ниже приведены инструкции по началу работы.

![Example list of agents](https://raw.githubusercontent.com/cantino/huginn/master/doc/imgs/your-agents.png)

![Event flow diagram](https://raw.githubusercontent.com/cantino/huginn/master/doc/imgs/diagram.png)

![Detecting peaks in Twitter](https://raw.githubusercontent.com/cantino/huginn/master/doc/imgs/peaks.png)

![Logging your location over time](https://raw.githubusercontent.com/cantino/huginn/master/doc/imgs/my-locations.png)

![Making a new agent](https://raw.githubusercontent.com/cantino/huginn/master/doc/imgs/new-agent.png)

## Начиная

### докер

Самый быстрый и простой способ проверить Huginn - это использовать официальное изображение Docker. Посмотрите на [документацию](https://github.com/cantino/huginn/blob/master/doc/docker/install.md) .

### Локальная установка

Если вы просто хотите поиграть, вы можете просто разветвить этот репозиторий, а затем выполнить следующие шаги:

- Запустите `git remote add upstream https://github.com/cantino/huginn.git` чтобы добавить основной репозиторий в качестве удаленного для вашего форка.
- Скопируйте `.env.example` в `.env` ( `cp .env.example .env` ) и отредактируйте `.env` , хотя бы обновив переменную `APP_SECRET_TOKEN` .
- Запустите `bundle` для установки зависимостей
- Запустите `bundle exec rake db:create` , `bundle exec rake db:migrate` , а затем `bundle exec rake db:seed` для создания базы данных MySQL для разработки с некоторыми примерами агентов.
- Запустите `bundle exec foreman start` , зайдите на [http: // localhost: 3000 /](http://localhost:3000/) и войдите в систему с именем пользователя `admin` и паролем `password` .
- Настройте несколько агентов!
- Прочитайте [вики,](https://github.com/cantino/huginn/wiki) чтобы ознакомиться с примерами использования и начать создавать новых агентов.
- Периодически запускайте `git fetch upstream` и затем `git checkout master && git merge upstream/master` для слияния с новейшей версией Huginn.

Примечание. По умолчанию электронные письма перехватываются в среде `development` Rails, которую вы только что настроили. Вы можете просмотреть их по адресу [http: // localhost: 3000 / letter_opener](http://localhost:3000/letter_opener) . Если вы хотите отправлять реальные электронные письма через SMTP при локальной игре с Huginn, установите для `SEND_EMAIL_IN_DEVELOPMENT` значение `true` в вашем файле `.env` .

Если вам нужны более подробные инструкции, см. [Руководство по настройке для начинающих](https://github.com/cantino/huginn/wiki/Novice-setup-guide) .

### развивать

Все агенты имеют спецификации! И есть также приемочные тесты, которые имитируют запуск Huginn в браузере без головы.

- Установите PhantomJS 2.1.1 или выше: 
    -  Использование [Node Package Manager](https://www.npmjs.com/) : `npm install phantomjs` 
    -  Использование [Homebrew](http://brew.sh/) на OSX `brew install phantomjs` 
- Запустите все спецификации с помощью `bundle exec rspec`
- Запустите конкретную спецификацию с помощью `bundle exec rspec path/to/specific/test_spec.rb` .
- Узнайте больше о rspec для рельсов [здесь](https://github.com/rspec/rspec-rails) .

## развертывание

### Heroku

Попробуйте Хугинн на Heroku: [![развертывание](https://www.herokucdn.com/deploy/button.png) (Установка занимает несколько минут. Прочитайте](https://heroku.com/deploy) [документацию,](https://github.com/cantino/huginn/blob/master/doc/heroku/install.md) пока вы ждете, и обязательно нажмите «Просмотр» после запуска!)

Хугинн работает над бесплатной версией Heroku [со значительными ограничениями](https://github.com/cantino/huginn/blob/master/doc/heroku/install.md) . Для не экспериментального использования мы настоятельно рекомендуем самый дешевый платный тариф Heroku или наш контейнер Docker.

Пожалуйста, смотрите [Huginn Wiki](https://github.com/cantino/huginn/wiki#deploying-huginn) для подробных стратегий развертывания для различных провайдеров.

### Ручная установка на любой сервер

Посмотрите на [руководство](https://github.com/cantino/huginn/blob/master/doc/manual/README.md) по [установке](https://github.com/cantino/huginn/blob/master/doc/manual/README.md) .

### Опциональная настройка

#### Настройка для частной разработки

Смотрите [частные инструкции](https://github.com/cantino/huginn/wiki/Private-development-instructions) по [разработке](https://github.com/cantino/huginn/wiki/Private-development-instructions) в вики.

#### Включить WeatherAgent

Чтобы использовать WeatherAgent, вам нужен [ключ API с Wunderground](http://www.wunderground.com/weather/api/) . Зарегистрируйтесь на него, а затем измените значение `api_key: your-key` в `api_key: your-key` .

#### Отключить SSL

Мы предполагаем, что ваше развертывание будет работать через SSL. Это очень хорошая идея! Однако, если вы хотите отключить это, вам, вероятно, потребуется отредактировать `config/initializers/devise.rb` и изменить строку, содержащую `config.rememberable_options = { :secure => true }` . Вам также необходимо отредактировать `config/environments/production.rb` и изменить значение `config.force_ssl` .

## Лицензия

Хугинн предоставляется по лицензии MIT.

[![Build Status](https://travis-ci.org/cantino/huginn.svg)](https://travis-ci.org/cantino/huginn) [![Coverage Status](https://coveralls.io/repos/cantino/huginn/badge.svg)](https://coveralls.io/r/cantino/huginn) [![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/cantino/huginn/trend.png)](https://bitdeli.com/free "Bitdeli Badge") [![Dependency Status](https://gemnasium.com/cantino/huginn.svg)](https://gemnasium.com/cantino/huginn) [![Bountysource](https://www.bountysource.com/badge/tracker?tracker_id=282580)](https://www.bountysource.com/trackers/282580-huginn?utm_source=282580&utm_medium=shield&utm_campaign=TRACKER_BADGE)
