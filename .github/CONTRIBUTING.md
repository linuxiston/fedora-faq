# Участие в проекте

Данный документ подробно описывает участие в проекте неофициального FAQ по Fedora на русском языке.

## Заявки

Если вы нашли ошибку, неточность, либо желаете добавить ответ на новый вопрос в FAQ, создайте [новую заявку](https://github.com/RussianFedora/FAQ/issues) в системе отслеживания ошибок проекта.

Убедительная просьба правильно выбирать шаблон. Это поможет автоматически установить заявке приоритет и автоматически уведомить мейнтейнеров.

## Внести свой вклад

В проекте может принять участие любой желающий. Для этого всего лишь нужно следовать стандартной процедуре pull request.

### Отправка изменений

1.  Создайте свой собственный проекта посредством нажатия кнопки **Fork**.

2.  Скачайте репозиторий своего форка:

```bash
git clone git@github.com:YOURNAME/FAQ.git
```

3.  Создайте новую ветку, например `new_feature`, а затем переключитесь на неё:

```bash
git checkout -b new_feature
```

4.  Внесите свои правки в проект, а по окончании зафиксируйте изменения в репозитории:

```bash
git add . && git commit -sm "Full description of your changes"
```

5.  Добавьте оригинальный проект в качестве [удалённого репозитория](https://help.github.com/articles/configuring-a-remote-for-a-fork/):

```bash
git remote add upstream https://github.com/RussianFedora/FAQ.git
```

6.  В связи с тем, что проект часто изменяется, [синхронизируйте свой форк](https://help.github.com/articles/syncing-a-fork/) с апстримом:

```bash
git fetch upstream
git checkout master
git merge upstream/master
```

7.  Переместите изменения в своей рабочей ветке `new_feature` поверх обновлённого `master`:

```bash
git checkout new_feature
git rebase master
```

8.  (Опционально) Объедините свои изменения в единый коммит при помощи `git squash`.

### Дополнительная информация

- В проекте используется табуляция через 4 пробела. Отдельные символы табуляции `\t` запрещены.
- Не загружайте в репозиторий какие-либо сторонние файлы, не относящиеся напрямую к коду, включая кэши, различные временные файлы и т.д.
- Не вносите правок в `gh-pages` ветку, т.к. она строится автоматически средствами системы непрерывной интеграции (CI).
- Используйте только правильно настроенный текстовый редактор. Он не должен менять формат конца строки, заменять формат отступов и т.п.
- Используйте правильно настроенный Git клиент. Поля "имя пользователя" и "адрес электронной почты" должны быть заполнены в каждом коммите, который предлагается включить в основную кодовую базу проекта.
- Не включайте никакого кода, использующего сторонние лицензии.
