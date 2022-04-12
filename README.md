# GIT

[Start и основные комманды](https://github.com/alexf81xxx/GIT#start)

[Работа с репозиторием](https://github.com/alexf81xxx/GIT#%D1%80%D0%B5%D0%BF%D0%BE%D0%B7%D0%B8%D1%82%D0%BE%D1%80%D0%B8%D0%B9 "Работа с репозиторием")

[Ветки](https://github.com/alexf81xxx/GIT#%D0%B2%D0%B5%D1%82%D0%BA%D0%B8)

## Start


Создание локалоного репозитория
~~~ 
git init 
~~~

Клонирование удалённого репозитория

~~~ 
git clone {url repository} 
~~~

Переход в директорию с созданным репозиторием

~~~ 
cd {directory name} 
~~~

Статус 

~~~ 
git status
~~~

Commit 

~~~ 
git commit -m "Git start"
~~~
*-m комментарий 
Пример: Feature, Hotfix,  BREAKING CHANGE:*

Посмотреть все коммиты 

~~~ 
git log
~~~
*--oneline - более компактный вид*

Отмена последнего commit 

~~~ 
git revert
~~~

Push

~~~ 
git push -u origin master
~~~
*Где -u origin master вы устанавливаете связь между той веткой, в которой вы находитесь и веткой master на удалённом сервере. Делается единожды Master - это название ветки, в которую мы пушим*

Push из одной ветки в другую (установили соединение)

~~~ 
git push -u secondBranch {наименование ветки, которую пушим}
~~~
![](https://thumb.cloud.mail.ru/weblink/thumb/xw1/eQnR/SvATofAnS)

*Где -u target это адрес удалённого репозитория, а {наименование ветки, которую пушим} и так понятно .*


## Репозиторий

Связать с удалённой веткой локальный репозиторий

~~~ 
git remote add origin {url remote repository}
~~~
*Где origin это просто переменная с адресом удалённого репозитория, можно называть как угодно. Также можем привязать несколько репозиториев.*

![](https://thumb.cloud.mail.ru/weblink/thumb/xw1/rzGc/FDFW6YDfs)

Посмотреть все ветки

~~~ 
git remote -v
~~~
*Где fetch - можем брать данные
*Push - отправлять

## Ветки

Создать ветку

~~~ 
git branch {branch name}
~~~
*Нэйминг также важен, например feature/addPayment. Второй пример (hotfix/task155) - исправление ошибки + номер таска в Notion*

Посмотреть список веток

~~~ 
git branch (-a)
~~~

*branch - показывает в какой ветке я нахожусь, а brahch -a - список всех веток*

**Git клонирует только одну ветку main**

![](https://thumb.cloud.mail.ru/weblink/thumb/xw1/rCqM/T58ct8ofg)

Переключится на ветку

~~~ 
git checkout
~~~

Отправить ветку в удалённый репозиторий

~~~ 
git push origin {branch name}
~~~

Удалить ветку

~~~ 
$ git branch -d hotfix
~~~
*где hotfix - наименование ветки*


Слияние веток

**Сначала переключаемся на ту ветку, в которую  хотим залить изменения**

~~~ 
$ git checkout master
~~~ 
~~~ 
$ git merge --no-ff {наименование ветки, котрую словаем}
~~~ 
*--no-ff это ускоренное слияние*

Удаление ветки
~~~ 
$ git branch -d hotfix
~~~
*где hotfix - наименование ветки*

## Push pull

*Fork - клонирует проект из одного удалйнного репозитория в ваш*

Получить изменения из удалённого репозитория

*Комманда pull делает и fetch(получает изменения) и merge*
~~~ 
git pull origin main
~~~
*Где origin - адрес удалённого репозитрия, а main - наименование локальной ветки*

## Pull Request
 
 *Pull Request— это запрос на вливание изменений из вашей ветки в основную ветку исходного репозитория. Таким образом они попадут к хозяевам проекта.*


