## Git

### Как изучать?

1. - [x] [Git для начинающих](https://monsterlessons.com/project/categories/git?page=1)
2. - [ ] [Интерактивный курс по гиту](https://githowto.com/ru)
3. - [x] [база git, mercurial и svn, основные идеи](https://www.youtube.com/watch?v=ZGmSavvT8yk&ab_channel=%D0%A4%D0%9A%D0%9D%D0%92%D0%A8%D0%AD)
4. - [ ] [Про гит от Atlassian](https://www.atlassian.com/git/tutorials/learn-git-with-bitbucket-cloud)
5. - [x] Сбер: "Инструменты DevOps: Git"
6. - [ ] [Как работает Git](https://habr.com/ru/post/313890/)
7. - [х] [19 советов по повседневной работе с Git](https://habr.com/ru/company/mailru/blog/267595/#10)
8. - [ ] [Что скрывает от нас директория .git](https://habr.com/ru/post/143079/)

### 1) про Git

> Проект был создан [Линусом Торвальдсом](https://github.com/torvalds) для управления разработкой ядра Linux. 
На сегодняшний день его поддерживает [Джунио Хамано](https://github.com/gitster?tab=repositories).

Для каждого коммита гит запоминает снимки изменившихся файлов целиком.
![DATA](https://github.com/eldaroid/pictures/blob/master/other/git_data.png)

#### Архитектура систем контроля версий (от англ. Version Control System, VCS)

<details><summary>Open</summary>
<p>

Инструменты VCS имеют два основных типа удаленной архитектуры:

* централизованный (Centralized VCS);
Примеры таких систем: SVN, CVS.
<img src="https://github.com/eldaroid/pictures/blob/master/other/centralized_VCS.png" alt="alt text" width="250" height="250">

* распределенный (Distributed model);
Примеры таких систем: Git, Mercurial. Git имеет распределенную модель архитектуры, то есть не зависит от одного центрального сервера, на котором хранятся файлы. Вместо этого он работает полностью локально, сохраняя данные в папках на жестком диске, которые называются репозиторием. Тем не менее, вы можете хранить копию репозитория онлайн. Это облегчает работу над одним проектом для нескольких людей. Для такой работы используются сайты вроде github и bitbucket.
<img src="https://github.com/eldaroid/pictures/blob/master/other/decentralized_VCS.png" alt="alt text" width="250" height="250">

Родительский коммит - тот, от которого пошли разделения на ветки.
Имя основной ветки по умолчанию в Git — master.

</p>
</details>

#### Состояния файлов Git

<details><summary>Open</summary>
<p>

Файл в Git может находится в одном из трёх состояний:

<img src="https://github.com/eldaroid/pictures/blob/master/other/git_files.png" alt="alt text" width="800" height="400">

* untracked (:white_circle:) — не добавлен в индекс для коммита, не вошли в последний спапшот и не подготовлены к коммиту.
* modified (:red_circle:) - объекты поменяли, но еще не зафиксировались.
* staged (:green_circle:) — добавлен в индекс для включения в коммит.
* commited (:white_circle:) — объект уже сохранен на базе.

</p>
</details>

### 2) Gitflow

<details><summary>Open</summary>
<p>

Существуют различные модели ветвления, наиболее популярные: 
* [Git flow:](https://github.com/eldaroid/iosBasics/blob/master/Git%2BTerminal/Gitflow.md)

<img src="https://github.com/eldaroid/pictures/blob/master/other/GitFlow.png" alt="alt text" width="450" height="300">

* [Github flow:](https://github.com/eldaroid/iosBasics/blob/master/Git%2BTerminal/Githubflow.md)

<img src="https://github.com/eldaroid/pictures/blob/master/other/GithubFlow.jpeg" alt="alt text" width="550" height="300">

* [Gitlab flow:](https://github.com/eldaroid/iosBasics/blob/master/Git%2BTerminal/Gitlabflow.md)

<img src="https://github.com/eldaroid/pictures/blob/master/other/GitlabFlow.jpeg" alt="alt text" width="300" height="350">

> [Базовые принципы популярных моделей ветвления](https://www.atlassian.com/git/tutorials/comparing-workflows)
> * Любое значимое изменение должно оформляться как отдельная ветвь
> * Текущая версия главное ветви всегда корректна. В любой момент сборка проекта, проведенная из текущей ветви, должна быть успешной.
> * Версии проекта помечаются тегами. Выделенная и помеченная тегом версия более никогда не изменяется.
> * Любые рабочие, тестовые или демонтрационные версии проекта собираются только из репозитоиия системы. 

</p>
</details>

#### Pull Request

<details><summary>Open</summary>
<p>

Общим принципом для всех моделей ветвления является то, что все изменения между ветками переносятся с помощью запросов на слияние.
  
**Запрос на слияние** (Pull-Request - BitBucket, Merge request - Gitlab) – механизм системы контроля версий, позволяющий оформить изменения из ветки в виде предложения к слиянию в основную (или какую-то иную) ветку репозитория.
  
<img src="https://github.com/eldaroid/pictures/blob/master/other/pull_request.png" alt="alt text" width="500" height="300">
  
Что даёт:

* Описание предлагаемого изменения видно в интерфейсе системы контроля версий всем заинтересованным участникам

* Возможность провести code review и оставить комментарии ещё до включения изменений в целевую ветку

* Возможность не допустить слияния, пока не будут выполнены все необходимые условия
    
    Например:
  
        * Минимальное количество подтверждений от участников, проводящих ревью
        * Успешно прошедшая сборка в системе CI
        * Отсутствие критичных замечаний по результатам автоматического статического анализа
   
</p>
</details>

### 3) Команды

<details><summary>Open</summary>
<p>
    Разница между git fetch и git pull
  > **git fetch [remote-name]** - Получает _список изменений_ в удаленном репозитории, а также сами изменения, без слияния с вашими изменениями
  > **git pull** получает изменения из удалённой ветви и сливает их со текущей ветвью (выполняет git fetch и git merge origin/[your branch]), **git push** - отправка изменений в удаленный репозиторий.
  
  * git diff - просмотр неотслеживаемых изменений
  
  * git add - добавляет файлы в отслеживаемые. -A - флаг для добавления всех измененных файлов; git rm --cached (file) - удаляет из отслеживаемых файлов (без флага --cached удаляет файлы, которые уже закоммичены).
  
  * git show [commit_id] - показывает изменения этого коммита
  
  * git push - отправляет изменения в удаленный репозиторий. Пушит все, кроме тегом, для тегов использовать флаг --tag.
  
  * [git commit --amend -m ""](https://www.atlassian.com/ru/git/tutorials/rewriting-history) - добавляет изменения к предыдущему коммиту, не создавая новый, при это хеш меняется; -no-edit позволяет внести изменения в коммит без изменения комментария к нему. Если ветка уже запушена, то после этой команды нужно прописать `git push -f` и удалённая ветка будет перезаписана. 
  
  Опции: 
        * `git commit --amend --allow-empty -m "New"` - Бывает, что нужно исправить опечатку в комментарии к последнему коммиту, не затрагивая файлов. В этом случае удобно воспользоваться флагом allow-empty, чтобы гит не ругался на отсутствие изменений для коммита
        * `git commit --amend --no-edit` - Не добавляет новый коммит, оставляет старый, при этом не запускает редактор
  
  * git merge - это 1/2 утилит Git, которая специализируется на интеграции изменений из одной ветки в другую. Сливание двух веток в одну

  * [git rebase](https://www.atlassian.com/ru/git/tutorials/rewriting-history/git-rebase) - это 2/2 утилит Git, которая специализируется на интеграции изменений из одной ветки в другую. Меняет историю ваших коммитов.
  
  Опции: 
        * squash — строит текстовый граф
        * fixup - то же самое, что и squash, но не добавляет предыдущий коммит к новому
        * reword — измение сообщение коммита (вместо pick - reword, вместо сообщения справа от хеша - новое сообщение коммита)
        * drop — удалить коммит. Могут быть проблемы с тем, что мы дальше меняли файл после того как удалили.
        * reset — жестко меняем HEAD на новый (вся последующая история после того, на что мы сделали reset - не сохраняется)
  
  * git blame (file) - показывает кто, когда, какую строчку кода написал/изменил
  
  * git grep "test" - ищет в рабочем каталоге слово test (как в коде, так и в названии файлов) 
  
</p>
</details>

### 4) Практика
  
#### Создание ветки: 

<details><summary>Open</summary>
<p>
  
1) git checkout -b bugfix/elizarov/ASSESSMENT-191
то же самое, что и : 
git branch bugfix/elizarov/ASSESSMENT-191
git checkout bugfix/elizarov/ASSESSMENT-191
2) git push --set-upstream [1] bugfix/elizarov/ASSESSMENT-191

</p>
</details>
  
#### Просмотр истории коммитов

<details><summary>Open</summary>
<p>
  
По умолчанию `git log` вывод в таком формате:

<img src="https://github.com/eldaroid/pictures/blob/master/other/gitlog.png" alt="alt text" width="300" height="300">

Удобный формат `git log --graph --oneline --decorate --stat`

Опции: 
* --stat — выведет статистику для каждого коммита
* --graph — выводит дерево зависимостей для всех коммитов
* --decorate — покажет “головы” (HEAD)
* --all — покажет все ветки
* -- oneline - выводит сокращённые данные коммита (в виде одной строки)
</p>
</details>
  
#### Извлечение файла из другой ветки

<details><summary>Open</summary>
<p>
  
  Пример команды: `git show some-branch:some-file.js`
  
  Иногда бывает удобно посмотреть на какой-либо файл в другой ветке, не переключаясь на неё. 
  Это можно сделать с помощью команды git show some-branch-name:some-file-name.js, которая выведет содержимое файла в указанной ветке прямо в терминал.
  
  А с помощью перенаправления вывода можно сохранить этот файл в указанное место на диске, например, если вы заходите открыть два файла одновременно в своём редакторе: git show some-branch-name:some-file-name.js > deleteme.js.

  Примечание: если вам нужно всего лишь сравнить два файла, то можно выполнить такую команду: git diff some-branch some-filename.js
  
</p>
</details>
  
#### Удаляем ветку:

<details><summary>Open</summary>
<p>
  
1) git checkout develop - переключаемся на любую ветку

2) git branch -d [your branch] - удаляем локальную
  
3) git push [1] --delete [your branch] - удаляем удаленную. 
[origin] - то, что мы прописывали в git push [1] HEAD:[your branch]

</p>
</details>
  
#### Удалить локальные изменения/откат коммитов:

<details><summary>Open</summary>
<p>

  * `git reset --hard {{some-commit-hash}}` — вернуться на определённый коммит в истории. Все изменения, сделанные после этого коммита пропадут.
  
  ```
  Если я хочу отменить все внесённые изменения и начать работу с чистого листа, я использую команду `git reset --hard HEAD`.
  
  git reset --hard [1]/yourBranch - более точно указываем к чем мы хотим откатить (к оригинальной ветка, которая хранится удаленно). 
  
  git reset --hard HEAD~1 - назад на 1 коммит
  ```
  
  * `git reset {{some-commit-hash}}` — вернуться на определённый коммит в истории. Все изменения, сделанные после этого коммита, получат состояние «Not staged for commit» - надо делать git add и git commit. Чтобы вернуть их обратно, нужно использовать команды git add и git commit.
  
  ```
  Если я хочу отредактировать изменения и/или закоммитить файлы в другом порядке, я использу git reset {{some-start-point-hash}}.
  ```
  
  * `git reset --soft {{some-commit-hash}}` — вернуться на определённый коммит в истории. Все изменения, сделанные после этого коммита, получат состояние «Staged for commit». Чтобы вернуть их обратно, нужно использовать команду git commit.
  
  ```
  Если я просто хочу взять три последних коммита и слить их в один большой коммит, я использую команду git reset --soft {{some-start-point-hash}}
  ```

  или если хочется изменить только файл
 
* git checkout (our file) - заменяет ваш локальный файл на оригинальной из удаленного репозитория

</p>
</details>

#### Merge

<details><summary>Open</summary>
<p>
  
* git checkout master
* git merge my_branch
  
My_branch слилась в master 

**Merge-конфликт** все, что выше `=======` - это HEAD, все, что ниже до `>>>>>>>` - это то, что мы сливали в мастер (My_branch)
  
Merge при конфликтах становится опасной утилитой - не всегда можно заметить какие строчки добавлены или файлы (а они могут влиять на работу программы). Справитсья с такой проблемой поможет команда `git mergetool`. Выведется vimdiff, который покажет полную разницу в файлах.
  
</p>
</details>
  
#### Rebase

<details><summary>Open</summary>
<p>

  Ребейз на новую ветку
  
Куда: [1]/release
Откуда: bugfix

git checkout [1]/release && git fetch && git pull && git checkout bugfix
  
git rebase [1]/release

git push -f
  
  [только n коммитов ребейзнуть](https://stackoverflow.com/questions/39084984/how-to-rebase-only-last-two-commits-without-the-whole-branch#:~:text=First%20create%20the%20branch%20other_feature%20at%20the%20same%20commit%20as%20feature%20.&text=Rebase%20the%20previous%20two%20commits%20onto%20master%20.&text=Checkout%20feature%20.&text=Reset%20feature%20to%20the%20commit%20where%20you%20want%20it.)
  
</p>
</details>

#### Alias git

<details><summary>Open</summary>
<p>

  * git config alias.st = status - теперь вместо полной команды git status можно писать просто git st. 
  
  или
  
  * vim ~/.gitconfig, добавляем в конец [alias] и с новой строки добавлять все алиасы.
  
  <img src="https://github.com/eldaroid/pictures/blob/master/other/aliasInGit.png" alt="alt text" width="250" height="100">
  
</p>
</details>

#### Если clone слишком большой

<details><summary>Open</summary>
<p>

```console
➜ git config --global core.compression 0
➜ git config --global http.postBuffer 1048576000
➜ git config --global http.maxRequestBuffer 100M
➜ git clone
```

```
git config --global http.maxRequestBuffer 100M --depth=1 - также может помочь, означает, что надо засквошить все коммиты в 1 последний. Когда это сработает, перейдите в новый каталог и получите оставшуюся часть клона: git fetch --unshallow  и git pull --all
``` 

</p>
</details>

---

[1] origin: `git remote -v`

[2] **git fetch [remote-name]**

[Previous Theme](/Git%2BTerminal/Terminal.md) | [Back To Contents](https://github.com/eldaroid/iosBasics) |  [Next Theme](Git%2BTerminal)