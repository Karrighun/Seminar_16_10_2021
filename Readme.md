# Инструкция по работе с Git

## Что такое Git?
**Git** - Одна из реализаций распределенных систем конторля версий. Позволяет контролироваться версионность файлов как локально, так и на удаленном сервере. Самая популарня система контроля версий

## Подготовка репозитория
**Репотизотрий** - это хранилище файлов, поддерживающее версионность. Создать репозиторий в папке можно с помощью команды *git init*, преминив эту команду в папке с будущим репозиторием.

## Создание сохранений 
Создать "сохранение" они же фиксация или коммиты, мы можем с помощью команды __*git commit*__. Для этого необходимо написать команду __*git commit -m <Сообщение к коммиту>*__ сообщение к коммиту писать обязательно. Все файлы должны быть добавлены в коммит с помощью команды __*git add*__. Если файлы не добавлены, то можно использовать флаг __*-a*__ и команда преобретет вид __*git commit -a -m "<сообщение к коммиту>*__.

## Журнал изменений

## Перемещение между сохранениями 
Для переключения между "сохранениями"(коммитами), необходимо использовать команду __*git checkout*__ следующим образом: __*git checkout <номер коммита для переключения>*__. Номер коммита берется из истории коммитов и на него произойдет переключение.

Команды __*git reset*__ и __*git revert*__ позволяют отменять изменения. Команда __*git revert*__ возвращает возвращает к указанному коммиту, создавая новый коммит, а команда __*git reset*__ возвращает к указанному коммиту и стирает историю изменений до указанного коммита. Применяется это следующим образом: __*git revert <номер коммита>*__ или __*git reset --hard <номер коммита>*__

## Ветки в Git
Для того чтобы проверить наличие веток и посмотреть на какой вы сейчас находитесь применяется команда __*git branch*__, Активная ветка будет отображаться __(*)__ и гореть зеленным цветом. Создание веток происходит путем той же команды __*git branch <название новой ветки>*__. Переключение же между веток происходит через команду __*git checkout <название ветки>*__.

## Удаление веток
Удаление веток происходит командой __*git branch -d <название ветки>*__

## Слияние веток и решение конфликтов
Слияние веток происходит путем перехода в основную ветку и ввода команды __*git merge <название ветки которую нужно интегрировать>*__. Решение конфликтов происходит путем выбора, можно оставить как оба варианта кофликта, так и какой-то один.

## Cкачивание удаленного репозитория
Для того чтобы начать работу с удаленным репозиторием, в первую очередь нам понадобится **"GitHub"**, с помощью него мы можем найти нужный репозиторий для скачивания. Находим нужный нам удаленный репозиторий, копируем ссылку с его кодом и с помощью команды __*git clone <ссылка на репозиторий>*__ вставляем его в *Visual Studio Code*.
 
## Отправка изменений в удаленный репозиторий

**1. Если изменения нужно вносить в собственный репозиторий:**
Для этого нам понадобится команда __*git push*__, с помощью нее файлы из нашего файла автоматически будут перекинуты на удаленный репозиторий. Если же мы внесли изменения с другого компьютера или через сайт GitHub и нам нужно чтобы эта информация отобразилась в Visual code, то используем команду __*git pull*__.

**2. Если изменения нужно вносить в открытый репозиторий:**
 Для этого нам поднадобится использовать систему "Fork", с помощью нее мы сможем скопировать содержимое кода и внести различные корректировки создав новую ветку. Потом повторяем все команды из прошлого пункта и отправляет наш __*pull request*__.

## Ссылка данной работы на GitHub []