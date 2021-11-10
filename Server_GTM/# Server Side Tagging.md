# Server Side Tagging

## 1. Создание серверного контейнера

1.1. Чтобы создать новый серверный контейнер нужно перейти на вкладку Admin текущего клиентского аккаунта и нажать +.

![alt_text](https://img.netpeak.ua/vinnie/5CYOPH.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/4SKSU4.png))

**Важно!** Не создавайте новый аккаунт, если у клиента уже есть аккаунт в GTM. Если аккаунта нет, то в таком случае просто создаем новый с нуля.

1.2. Заполняем название контейнера и выбираем тип - Server.


![alt_text](https://img.netpeak.ua/vinnie/4SL65C.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/4SL65C.png))

1.3. На стартовом экране выбираем Close.

![alt_text](https://img.netpeak.ua/vinnie/4SLGJB.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/4SLGJB.png))


## 2. Создание аккаунта Google Cloud для Server Side Tagging

2.1. Создаем новый аккаунт [Google](https://accounts.google.com/signup/v2/webcreateaccount?continue=https%3A%2F%2Fwww.google.com%3Fhl%3Dru&hl=ru&dsh=S1275266816%3A1634976208068055&biz=false&flowName=GlifWebSignIn&flowEntry=SignUp). Аккаунт лучше создавать на реальные данные, чтобы была возможность создать платежный аккаунт для старта трила.

2.2. Переходим в [Google Cloud](https://cloud.google.com/) и нажимаем Get started for free. \
 \

![alt_text](https://img.netpeak.ua/vinnie/4SMPYF.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/4SMPYF.png))

2.3. Заполняем первый шаг регистрации.

![alt_text](https://img.netpeak.ua/vinnie/59ISXU.png "image_tooltip")

([ссылка](https://img.netpeak.ua/vinnie/59ISXU.png.png))

2.4. Подтверждаем номер телефона.

![alt_text](https://img.netpeak.ua/vinnie/4SP5YQ.png "image_tooltip")

([ссылка](https://img.netpeak.ua/vinnie/4SP5YQ.png))

2.5. Вносим платежные данные. После подтверждение спишется 1$ с моментальным возвратом.

![alt_text](https://img.netpeak.ua/vinnie/4SPS2V.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/4SPS2V.png))


![alt_text](https://img.netpeak.ua/vinnie/4SPVMY.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/4SPVMY.png))

**Примечание!** Если платежный аккаунт заблокировали, то нужно будет сфотографировать карту (с именем и фамилией), заграничный паспорт и отправить фото на разблокировку.

![alt_text](https://img.netpeak.ua/vinnie/4SR0BU.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/4SR0BU.png))


## 3. Конфигурация App Engine

3.1. Если аккаунт Google Cloud создается на базе предоставленного клиентом аккаунта Google, то в GTM выбирается автоматическая настройка App Engine. Если Cloud создается на базе отдельного аккаунта Google, то настройка App Engine производится в ручном режиме, так как GTM нужно будет связать с новым аккаунтом Google.

3.2. Если аккаунт Google Cloud создается на базе предоставленного клиентом аккаунта Google, то в GTM выбирается автоматическая настройка App Engine.

![alt_text](https://img.netpeak.ua/vinnie/59J79T.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/59J79T.png))

3.3. Ручная настройка App Engine.

3.3.1. На домашней странице проекта идем в настройки проекта. 


![alt_text](https://img.netpeak.ua/vinnie/59JC2P.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/59JC2P.png))

3.3.2. Меняем название проекта на ID GTM контейнера (GTM-XXXXXXX). 


![alt_text](https://img.netpeak.ua/vinnie/59JIPA.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/59JIPA.png))

3.3.3. Запускаем Cloud Shell

![alt_text](https://img.netpeak.ua/vinnie/54H3ZI.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/54H3ZI.png))

3.3.4. Прописываем. Заменить <PROJECT_ID> на ID проекта. Скопировать его можно в окне, которое вызывается при нажатие на проект в хедере страницы. 

    gcloud config set project <PROJECT_ID>


![alt_text](https://img.netpeak.ua/vinnie/59K5IO.png "image_tooltip")


([ссылка](http://img.netpeak.ua/vinnie/59K5IO.png))

3.3.5. Инициализируем запуск установки GTM:

        bash -c "$(curl -fsSL (https://googletagmanager.com/static/serverjs/setup.sh))"

3.3.6. Cloud Shell в ответ запросит конфиг GTM.

![alt_text](https://img.netpeak.ua/vinnie/59KG3H.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/59KG3H.png))

3.3.7. На запрос установки URL политик и настройки логирования можно нажимать Enter

![alt_text](https://img.netpeak.ua/vinnie/58Z6FI.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/58Z6FI.png))

3.3.8. На запрос типа деплоймента прописываем “testing” и нажимаем продолжить.


![alt_text](https://img.netpeak.ua/vinnie/58ZE0P.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/58ZE0P.png))


![alt_text](https://img.netpeak.ua/vinnie/58ZKB4.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/58ZKB4.png))

3.3.9. На запрос выбора зоны расположения серверов выбираем одну из 11, 12, 13 или 14. После еще раз подтверждаем деплоймент.

![alt_text](https://img.netpeak.ua/vinnie/58ZY43.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/58ZY43.png))


![alt_text](https://img.netpeak.ua/vinnie/59KT28.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/59KT28.png))

3.3.10. После окончания установки прописываем команду

    gcloud app browse

Cloud Shell выведет на экран URL приложения. Его надо скопировать и вставить в GTM >>> Admin >>> Container Settings, после чего сохранить.



![alt_text](https://img.netpeak.ua/vinnie/596SNM.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/596SNM.png))

3.3.11. Чтобы проверить работает ли сервер, переход в Preview режим в GTM.


![alt_text](https://img.netpeak.ua/vinnie/5971J7.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/5971J7.png))

Должна открыться страница отладки на развернутом домене.

![alt_text](https://img.netpeak.ua/vinnie/597A3K.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/597A3K.png))

3.4. Привязка App Engine к домену проекта.

3.4.1. В меню Google Cloud находим App Engine. Можно сразу закрепить их меню, чтобы не искать постоянно.


![alt_text](https://img.netpeak.ua/vinnie/598C1T.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/598C1T.png))

3.4.2. На начальной странице App Engine переходим в настройки.  


![alt_text](https://img.netpeak.ua/vinnie/598F3S.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/598F3S.png))

3.4.3. Переходим на вкладку Custom Domains.

![alt_text](https://img.netpeak.ua/vinnie/598P5X.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/598P5X.png))

3.4.4. Нажимаем добавить домен


![alt_text](https://img.netpeak.ua/vinnie/59A8CW.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/59A8CW.png))

3.4.5. В первое поле вносим поддомен в формате  "collect.domain.com" и нажимаем Verify.


![alt_text](https://img.netpeak.ua/vinnie/59C3LS.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/59C3LS.png))

После чего откроется страница Google Search Console.

3.4.6. В поле регистратор домена выбираем Другое.

![alt_text](https://img.netpeak.ua/vinnie/59BW2P.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/59BW2P.png))

3.4.7. Копируем TXT запись и ставим задачу по [шаблону](https://t.netpeak.group/task/3365087).


![alt_text](https://img.netpeak.ua/vinnie/59CJ9W.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/59CJ9W.png))

3.4.8. Чтобы проверить наличие DNS записи, использовать следующие команды в терминале:

Windows: 

        nslookup -type=TXT site.com

Mac:

        host -t TXT site.com

Как выглядит правильный ответ:

![alt_text](https://img.netpeak.ua/vinnie/6I0NJP.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/6I0NJP.png))

3.4.8. На следующем шаге удаляем домен с www.

![alt_text](https://img.netpeak.ua/vinnie/6NP0F3.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/6NP0F3.png))


3.4.8. После подтверждения домена ставим задачу на вторую часть привязки DNS по [шаблону](https://t.netpeak.group/task/3395258).



## 4. Подготовка технического заданий для клиента

4.1. Facebook Conversions API для идентификации пользователей может использовать целый набор идентификаторов:

* fbp - стандартный идентификатор пользователя, которые присваивается всем браузерам, с которых посещается сайт с установленным пикселем;
* fbc - стандартный идентификатор клика по рекламе Facebook, который привел к посещению сайта с установленным пикселем;
* email_adress - почта пользователя;
* phone_number - номер телефона пользователя;
* first_name - имя пользователя;
* last_name - фамилия пользвоателя;
* city - город проживания пользователя;
* state - регион, область проживания пользователя;
* postal_code - почтовый индекс пользователя;
* country - страна проживания пользователя.

Для передачи fbp и fbc забираются с cookie. Для остальных идентификатов необходимо настроить передачу данных в dataLayer.

4.2. Для составление технического задания необходимо подходить индивидуально в зависимости от сайта: какие формы обратной связи используются, какие поля содержат эти формы, есть ли возможность передчи данных из бекенда и т.п. Дополнительно в задание также нужно включить все добавочные события, которые могут пригодиться позже.

Для составления такого технического задания обязательно изучить сайт клиента, провести мозговой штурм для того, чтобы опрдеелить все необходимые события.

Примерный [шаблон](https://docs.google.com/document/d/1Ed9Kj_tfgjVzPWtnbnsEd7S623txqY-rWvXAOzwhFZM/edit?usp=sharing) для сайта услуг с формой обратной связи с одним полем для номера телефона.

4.3. После сообщения о внедрении технического заадния со стороны клиента, необходимо провести проверку.

Открываем отладчик GTM: 



![alt_text](https://img.netpeak.ua/vinnie/6I20KF.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/6I20KF.png))

Триггерим отправку событий с сайта (отправляем формы, делаем заказы и т.п.). В отладчике должны появляться события:

![alt_text](https://img.netpeak.ua/vinnie/6I28D8.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/6I28D8.png))

Если сайт небольшой, то нужно проверить все возможные события. Если же сайт многостраничный, то достаточно проверрить каждое событие в разных сценариях, например отправку формы со страницы разных услуг или транзакцию с разным набором товаров.

## 5. Работа с GTM

5.1. Google Analytics

5.1.1. Нужно убедиться, что у клиета есть ресурс Google Analytics 4.

![alt_text](https://img.netpeak.ua/vinnie/6IO94H.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/6IO94H.png))

5.1.2. Если ресурса нет, то создаем новый. Называть новый ресурс по схеме нейминга клиента, добавляя а скобках "(GA4)" или просто "домен без www (GA4)", например "site.com (GA4)"

![alt_text](https://img.netpeak.ua/vinnie/6IQ7ZP.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/6IQ7ZP.png))

5.1.3. Будет предложено создать потоr данных, выбираем Веб.

![alt_text](https://img.netpeak.ua/vinnie/6IQPRD.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/6IQPRD.png))

5.1.4. Вводим сайт и название потока

![alt_text](https://img.netpeak.ua/vinnie/6IRY43.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/6IRY43.png))

5.1.5. В дальнейшем понадобится идентификатор потока, который будет показан в следующем экране. Его можно скопировать в блокнот.

![alt_text](https://img.netpeak.ua/vinnie/6ISEAK.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/6ISEAK.png))

После выхода, чтобы найти идентификатор потока, необходимо перейти в раздел Администратора, выбрать Потоки данных и перейти на нужный поток.

![alt_text](https://img.netpeak.ua/vinnie/6ISNJG.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/6ISNJG.png))

5.2. Facebook

5.2.1. Пиксель клиента обязательно привязывается к Business Manager Netpeak (это сделает PM). Чтобы проделать работы этого раздела, необходимо иметь досуп к нему. Если доступа еще нет, его может выдать [Slasya](https://telegram.me/an_kundelskaya). Доступ нужен на уровне Администратор.

5.2.2. В [Event Manager](https://www.facebook.com/events_manager2/) переходим в пиксель клиента на вкладку настройки. Нужно пролистать до раздела Conversions API и нажать на Сгенерировать маркер доступа. Маркер скопировать в блокнот. Также сразу скопировать ID пикселя.

![alt_text](https://img.netpeak.ua/vinnie/6NKSTO.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/6NKSTO.png))

Если такой кнопки не будет, то нажать на кнопку Начать. Запустится сценарий руковдства настройки. В нем нужно пройти все шаги до момента генерации маркера доступа. 

5.2.3. Переходим на вкладку тестироване событий и копируем в блокнот код для тестирования серверных событий.

![alt_text](https://img.netpeak.ua/vinnie/6NLG6M.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/6NLG6M.png))

5.3. Google Tag Manager.

5.3.1. Server Google Tag Manager.

5.3.1.1. Создаем новый тег типа Google Analytics 4.

![alt_text](https://img.netpeak.ua/vinnie/6NNO7K.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/6NNO7K.png))

Вносим ранее скопированный идентификатор потока.

![alt_text](https://img.netpeak.ua/vinnie/6NO0S4.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/6NO0S4.png))

Триггер выбираем Специальный. Переключаемся на некторые события и в параметрах указываем Client Name ровно GA4. После чего сохраняем тег.

![alt_text](https://img.netpeak.ua/vinnie/6NOC3Q.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/6NOC3Q.png))

5.3.1.2. Нажимаем создать новый тег и переходим в галерею пользовательских шаблонов.

![alt_text](https://img.netpeak.ua/vinnie/7DD6Y8.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/7DD6Y8.png))

5.3.1.3. В рабочую область нужно добавить Facebook Conversion API Tag (Автор: facebookincubator).

![alt_text](https://img.netpeak.ua/vinnie/7DDUEZ.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/7DDUEZ.png))

5.3.1.4. Создаем новый тег типа Facebook Conversion API. Вставляем ранее скопированные ID пикселя, маркер доступа и код для тестирования событий.

![alt_text](https://img.netpeak.ua/vinnie/7DEE0Q.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/7DEE0Q.png))

5.3.1.5. Триггер выбираем Специальный. Переключаемся на некторые события и в параметрах указываем Client Name ровно GA4. После чего сохраняем тег.

![alt_text](https://img.netpeak.ua/vinnie/6NOC3Q.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/6NOC3Q.png))

5.3.2. Web Google Tag Manager.

5.3.2.1. Создаем две переменные типа Основной файл cookie. В первую вносим в качестве названия _fbp, во вторую - _fbc.

![alt_text](https://img.netpeak.ua/vinnie/7DFEMH.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/7DFEMH.png))

![alt_text](https://img.netpeak.ua/vinnie/7DFI08.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/7DFI08.png))

5.3.2.2. Создаем переменную из галереи шаблонов типа Event Id (Автор: mbaersch). Тут ничего дополнительно указывать не надо.

![alt_text](https://img.netpeak.ua/vinnie/7DFS4X.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/7DFS4X.png))

5.3.2.3. В теге Facebook пикселя необходимо добавить идентификатор события, чтобы система могла удалять события, которые приходят от Сервера и Браузера. В строке, где указывается отслеживание просмотра страницы добавить:

        fbq('track', 'PageView', {}, {eventID: '{{FB / Event ID}}'});

где {{FB / Event ID}} - название переменной с Event ID


![alt_text](https://img.netpeak.ua/vinnie/7DGMG6.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/7DGMG6.png))

**Примечание**. Идентификатор события нужно добавить во все теги Facebook, события которых будут дублироваться с серверными событиями.

Например, если в Web контейнере (или напрямую через сайт) уже настроено отслеживание события Lead и с сервера предпологается также отправлять событие Lead, то  к браузерному событию необходимо добавлять Event ID. Как вариант избежать этого - просто переназывать событие, которое будет оптравляться с сервера другим образом, например LeadForm.

5.3.2.4. Создаем тег типа Google Аналитика: конфигурация GA4. Вносим идентификатор потока, который был скопирован ранее.

Отмечаем Отправлять в серверный контейнер и вносим URL, где развернут серверный GTM.

Далее задаем дополнительные поля:

* fbp - переменная cookie _fbp;
* fbc - переменная cookie _fbc;
* event_id - перемення с Event ID.

Триггер - App Pages.

![alt_text](https://img.netpeak.ua/vinnie/7DIIIL.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/7DIIIL.png))

После этой базовой настройки и публикации контейнер в разделе тестирование событий в Facebook Event Manager начнут поступать события просмотров страниц.

![alt_text](https://img.netpeak.ua/vinnie/7DJ5FG.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/7DJ5FG.png))

5.3.2.5. Далле для примера отправки события Lead с именем пользователя и номером телефона. 

Создаем тег типа Google Аналитика: событие GA4 и выбираем ему ранее настроенный тег конфигурации.

В качестве названия вносим Lead. Название тега будет сопоставляться с Facebook. И с таким названием в Event Manager собфтие будет отображаться как Лид.

![alt_text](https://img.netpeak.ua/vinnie/7DKOM0.png "image_tooltip")


([ссылка](https://img.netpeak.ua/vinnie/7DKOM0.png))





5.3.2.4. 




















5.1.1. Создаем тег


