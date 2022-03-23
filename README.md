# GIT

### Start


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
*Где -u origin master вы устанавливаете связь между той веткой, в которой вы находитесь и веткой master на удалённом сервере. Делается единожды*

### Репозиторий

Связать с удалённой веткой локальный репозиторий

~~~ 
git remote add origin {url remote repository}
~~~
*Где origin это просто переменная с адресом удалённого репозитория, можно называть как угодно. Также можем привязать несколько репозиториев.

![](https://thumb.cloud.mail.ru/weblink/thumb/xw1/rzGc/FDFW6YDfs)

Посмотреть все ветки

~~~ 
git remote -v
~~~
*Где fetch - можем брать данные
*Push - отправлять
### Создание репозитория222