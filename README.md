# devops-netology

# Домашнее задание к занятию «Системы контроля версий»
Выполнил: Береснев Игорь Андреевич

---

Создание репозитория и первого коммита

Зарегистрируйте аккаунт на https://github.com/. Если предпочитаете другое хранилище для репозитория, можно использовать его.

Создайте публичный репозиторий, который будете использовать дальше на протяжении всего курса, желательное с названием devops-netology. Обязательно поставьте галочку Initialize this repository with a README.

Создайте авторизационный токен для клонирования репозитория.

Склонируйте репозиторий, используя протокол HTTPS (git clone ...).

### Скриншот клонирования репозитория

![clone](screenshots/clone.png)

Перейдите в каталог с клоном репозитория (cd devops-netology).

Произведите первоначальную настройку Git, указав своё настоящее имя, чтобы нам было проще общаться, и email (git config --global user.name и git config --global user.email johndoe@example.com).

Выполните команду git status и запомните результат.

### Скриншот настройки Git и команды git status

![git](screenshots/git.png)

Отредактируйте файл README.md любым удобным способом, тем самым переведя файл в состояние Modified.

### Скриншот нового коммита

![commits](screenshots/commits.png)
Это строка для проверки git diff

Ещё раз выполните git status и продолжайте проверять вывод этой команды после каждого следующего шага.

### Скриншот команды git status

![git_2](screenshots/git_2.png)

Теперь посмотрите изменения в файле README.md, выполнив команды git diff и git diff --staged.

### Скриншот команд git diff и git diff --staged

![diff](screenshots/diff.png)

И ещё раз выполните команды git diff и git diff --staged. Поиграйте с изменениями и этими командами, чтобы чётко понять, что и когда они отображают.

### Скриншот команд git diff и git diff --staged

![git_2](screenshots/diff_2.png)

### Скриншот команды git status

![git_3](screenshots/git_3.png)

Теперь можно сделать коммит git commit -m 'First commit'.

### Скриншот сделанного коммита

![first](screenshots/first.png)

И ещё раз посмотреть выводы команд git status, git diff и git diff --staged.

### Скриншот команд git status, git diff и git diff --staged.

![git_4](screenshots/git_4.png)

Создайте файл .gitignore (обратите внимание на точку в начале файла), проверьте его статус сразу после создания.

### Скриншот создания файла .gitignore и проверка статуса

![gitignore](screenshots/gitignore.png)

Добавьте файл .gitignore в следующий коммит (git add...).

На одном из следующих блоков вы будете изучать Terraform, давайте сразу создадим соотвествующий каталог terraform и внутри этого каталога — файл .gitignore по примеру: https://github.com/github/gitignore/blob/master/Terraform.gitignore.

### Скриншот добавления файла .gitignore

![gitignore_2](screenshots/gitignore_2.png)

В файле README.md опишите своими словами, какие файлы будут проигнорированы в будущем благодаря добавленному .gitignore.

### Скриншот файла README.md

![readme](screenshots/readme.png)

## .gitignore

В корне проекта добавлен файл `.gitignore` для исключения из репозитория файлов, связанных с Terraform:

- **.terraform/** — локальные каталоги с загруженными провайдерами и модулями
- **\*.tfstate, \*.tfstate.\*** — файлы состояния инфраструктуры (содержат конфиденциальные данные)
- **\*.tfvars, \*.tfvars.json** — файлы с переменными окружения (пароли, ключи, токены)
- **override.tf, \*_override.tf** — файлы локальных переопределений ресурсов
- **.terraform.tfstate.lock.info** — файлы блокировки состояния
- **.terraformrc, terraform.rc** — файлы конфигурации CLI

Эти файлы не должны попадать в репозиторий, так как они либо содержат чувствительные данные, либо являются временными/локальными.

Закоммитьте все новые и изменённые файлы. Комментарий к коммиту должен быть Added gitignore.

### Скриншот добавления коммита

![gitignore_3](screenshots/gitignore_3.png)

Создайте файлы will_be_deleted.txt (с текстом will_be_deleted) и will_be_moved.txt (с текстом will_be_moved) и закоммите их с комментарием Prepare to delete and move.

В случае необходимости обратитесь к официальной документации — здесь подробно описано, как выполнить следующие шаги.
Удалите файл will_be_deleted.txt с диска и из репозитория.

### Скриншот создания файлов

![files](screenshots/files.png)

### Скриншот добавления коммита

![commits_2](screenshots/commits_2.png)

Удалите файл will_be_deleted.txt с диска и из репозитория.

Переименуйте (переместите) файл will_be_moved.txt на диске и в репозитории, чтобы он стал называться has_been_moved.txt.

### Скриншот удаления и перееминования

![change](screenshots/change.png)

### Скриншот добавления коммита

![commits_3](screenshots/commits_3.png)
