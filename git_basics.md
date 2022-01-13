# Установка, настройка доступа и основы работы с GIT

## 1. Установка GIT

1.1. На официальном [сайте](https://git-scm.com/downloads) скачать и установить GIT.

### 1.2. Настройки при установке

1.2.1. Компоненты оставляем по умолчанию

![alt_text](https://img.netpeak.ua/vinnie/GIMJTW.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GIMJTW.png)

1.2.2. Редактор тоже можно оставить по умолчанию

![alt_text](https://img.netpeak.ua/vinnie/GIMPRE.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GIMPRE.png)

1.2.3. В способе использование GIt в командной строке указываем 3-й пункт


![alt_text](https://img.netpeak.ua/vinnie/GIMW1I.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GIMW1I.png)



1.2.4. Подключение по протоколу HTTPS оставляем по умолчанию

![alt_text](https://img.netpeak.ua/vinnie/GIN7OX.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GIN7OX.png)

1.2.5. Способ обработки окончани строк выбрать 2-й вариант

![alt_text](https://img.netpeak.ua/vinnie/GINHPM.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GINHPM.png)

1.2.6. Терминал оставляем по умолчанию

![alt_text](https://img.netpeak.ua/vinnie/GINQ9Y.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GINQ9Y.png)

1.2.7. Дополнительные опции оставляем по умолчанию

![alt_text](https://img.netpeak.ua/vinnie/GIO025.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GIO025.png)

## 2. Настройка Git

2.1. После установки запускаем Git Bash.

![alt_text](https://img.netpeak.ua/vinnie/GIRKVX.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GIRKVX.png)

2.2. Задаем имя пользователя (ник в Netpeak) и почту (Gmail в Netpeak):

    git config --global user.email "you@example.com"
    git config --global user.name "name"

2.3. Создаем ssh ключ, указывая свой email (Gmail в Netpeak):

    ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

По умолчанию Git предложит создать ключ в 
C:\Users\Vinnie\ .ssh\id_rsa.
 
![alt_text](https://img.netpeak.ua/vinnie/GITD07.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GITD07.png)

Нажимаем Enter. Далее он предложит создать пароль - фразу. Пропускаем, нажимая два раза Enter.

![alt_text](https://img.netpeak.ua/vinnie/GJISVJ.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GJISVJ.png)

2.4. Открываем папку с ключом, открываем файл текстовым редактором и копируем ключ в файле.

![alt_text](https://img.netpeak.ua/vinnie/GJJ1WB.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GJJ1WB.png)



2.5. Переходим в командный акк Git (на командном Google аккаунте) и открываем настройки

![alt_text](https://img.netpeak.ua/vinnie/GJJDAM.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GJJDAM.png)

В разделе SSH ключей добавляем новый ключ, куда вставляем содержимое файла. Даем название своего ника в Netpeak.

![alt_text](https://img.netpeak.ua/vinnie/GJJP5M.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GJJP5M.png)

## 3. Работа с GIT

3.1. Установка Visual Studio Code

Visual Studio Code имеет бесплатную синхронизацию с Git, поэтому удобно работать в нем. 

Скачать его можно [тут](https://code.visualstudio.com/).

3.2. Необходимо создать папку, куда будут клонироваться Git репозитории, например

     C:\Users\Name\analytics_department

### 3.3. Работа с файлами в существующих репозиториях и новыми файлами в существующих репозиториях

3.3.1. Чтобы клонировать существующий репозиторий в Visual Studio Code в терминале нужно открыть Git

![alt_text](https://img.netpeak.ua/vinnie/GJLFZM.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GJLFZM.png)

![alt_text](https://img.netpeak.ua/vinnie/GJLMU8.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GJLMU8.png)

3.3.2. Переходим в директорию для работы с Git

    cd C:\Users\Name\analytics_department

3.3.3. В аккаунте Git скопировать ссылку (HTTPS или SSH) для клонирования

![alt_text](https://img.netpeak.ua/vinnie/GJM82R.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GJM82R.png)

3.3.4 Клонируем в терминале Git

    git clone https://github.com/VinnieNetpeak/sql.git

![alt_text](https://img.netpeak.ua/vinnie/GJMVWU.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GJMVWU.png)

После этого в папке появятся все файлы из репозитория.

3.3.5. В Visual Code Studio нажимаем File > Open Folder и выбираем папку, которая был создана для репозиториев.

![alt_text](https://img.netpeak.ua/vinnie/GJOSUL.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GJOSUL.png)

Теперь все файлы можно открыть с Explorer. Также можно создать новый файл с нуля.


![alt_text](https://img.netpeak.ua/vinnie/GJP0RD.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GJP0RD.png)


3.3.6. После того, как поработали с файлом, переходим в терминал Git. Нужно убедиться, что мы находимся в репозитории, с отредактированным файлом.

![alt_text](https://img.netpeak.ua/vinnie/GJPQXD.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GJPQXD.png)

3.3.7. Проверяем статус командой

    git status


![alt_text](https://img.netpeak.ua/vinnie/GJPW21.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GJPW21.png)

На скриншоте видно, что у нас есть один измененній файл.

3.3.8. Добавляем изменения в коммит командой

    git add . 

Точка означает все файлы, но их можно и выбирать по отдельности. После этого можно еще раз проверить статус (п. 3.3.7).

![alt_text](https://img.netpeak.ua/vinnie/GJQBK5.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GJQBK5.png)

3.3.9. Отправляем коммит командой

    git commit -m "текст коммита"

В тексте обозначать краткую суть коммита, например "Добавлен sql для …"

![alt_text](https://img.netpeak.ua/vinnie/GJQTJZ.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GJQTJZ.png)

3.3.10 Отправляем коммит командой

    git push origin master

![alt_text](https://img.netpeak.ua/vinnie/GJTYCY.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GJTYCY.png)

Все изменения теперь загружены на сервер Git.

### 3.4. Создание репозитория cс нуля

3.4.1. Создаем папку на жестком диске, где будут находится файлы репозитория. Команда для Git Bash

    mkdir new

После этого появится новая папка. 

![alt_text](https://img.netpeak.ua/vinnie/GJWDA7.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GJWDA7.png)


В Git Bash переходим в нее командой

    cd new

3.4.2. Инициируем репозиторий Git командой

    git init

Дальше можно создавать файлы и работать в них.

![alt_text](https://img.netpeak.ua/vinnie/GJWTWH.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GJWTWH.png)

3.4.3. Далее идем в аккаунт Git и создаем новый репозиторий

![alt_text](https://img.netpeak.ua/vinnie/GJWYKV.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GJWYKV.png)

![alt_text](https://img.netpeak.ua/vinnie/GJX67D.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GJX67D.png)

3.4.4. Синхронизируем репозиторий с папкой на жестком диске командой 

    git remote add origin git@github.com:VinnieNetpeak/new.git


![alt_text](https://img.netpeak.ua/vinnie/GJXIUE.png "image_tooltip")

[(ссылка)](https://img.netpeak.ua/vinnie/GJXIUE.png)


3.4.4. Дальше все повторяется как в пп. 3.3.6. - 3.3.10. 

