# Git за 2 часа: Полный курс для начинающих

## 📅 Структура урока (120 минут)

- **0:00-0:15** - Введение в Git
- **0:15-0:30** - История и зачем нужен Git
- **0:30-0:50** - Установка и первоначальная настройка
- **0:50-1:20** - Основные команды Git
- **1:20-1:50** - Работа с ветками
- **1:50-2:00** - Удаленные репозитории и GitHub

---

## 📖 Модуль 1: Введение в Git (15 минут)

### Что такое Git?

**Git** — это распределенная система контроля версий (VCS - Version Control System), созданная Линусом Торвальдсом в 2005 году для разработки ядра Linux.

### Что такое система контроля версий?

**Система контроля версий** — это инструмент, который:
- **Отслеживает изменения** в файлах проекта
- **Сохраняет историю** всех изменений
- **Позволяет возвращаться** к предыдущим версиям
- **Объединяет работу** нескольких разработчиков
- **Показывает, кто и что изменил**

### Проблемы без системы контроля версий

```
project_v1.zip
project_v2.zip
project_v2_final.zip
project_v2_final_REALLY_FINAL.zip
project_v2_final_REALLY_FINAL_fixed.zip
```

**Знакомо?** 😅

### Основные понятия Git

| Термин | Описание |
|--------|----------|
| **Репозиторий (Repository)** | Папка с проектом под контролем Git |
| **Коммит (Commit)** | Снимок состояния проекта в определенный момент |
| **Ветка (Branch)** | Независимая линия разработки |
| **Рабочая область (Working Directory)** | Файлы, которые вы редактируете |
| **Индекс (Staging Area)** | Подготовленные к коммиту изменения |

### Типы систем контроля версий

#### 1. Локальные (старые)
```
Компьютер разработчика
├── Проект
└── База данных версий
```

#### 2. Централизованные (SVN, CVS)
```
Центральный сервер ← → Разработчик 1
                 ← → Разработчик 2
                 ← → Разработчик 3
```

#### 3. Распределенные (Git, Mercurial)
```
Разработчик 1 ← → Центральный сервер ← → Разработчик 2
     ↓                                        ↓
Локальная копия                        Локальная копия
```

### Преимущества Git

✅ **Скорость** — большинство операций выполняются локально  
✅ **Распределенность** — каждый разработчик имеет полную копию истории  
✅ **Надежность** — данные защищены криптографическими хешами  
✅ **Ветвление** — легкое создание и слияние веток  
✅ **Популярность** — стандарт в индустрии  

### 🎯 Задание 1.1 (3 минуты)
Ответьте на вопросы:
1. Что означает аббревиатура VCS?
2. Кто создал Git и в каком году?
3. Назовите 3 преимущества Git перед ручным управлением версиями
4. Что такое коммит?

**Ответы:** 
1. Version Control System
2. Линус Торвальдс, 2005 год
3. Автоматическое отслеживание изменений, история версий, совместная работа
4. Снимок состояния проекта в определенный момент

---

## 📚 Модуль 2: История и зачем нужен Git (15 минут)

### Краткая история систем контроля версий

**1980-е** - Первые VCS (RCS, SCCS)  
**1990** - CVS (Concurrent Versions System)  
**2000** - Subversion (SVN)  
**2005** - **Git создан Линусом Торвальдсом**  
**2008** - Запуск GitHub  
**2010-е** - Git становится стандартом  
**Сегодня** - Git используют 90%+ разработчиков  

### Почему был создан Git?

**Проблема:** Разработка ядра Linux велась с помощью патчей и архивов, что было неэффективно.

**Требования к новой системе:**
- Высокая скорость
- Простая архитектура  
- Поддержка нелинейной разработки (ветки)
- Полная распределенность
- Способность работать с большими проектами

**Результат:** За 2 недели Линус создал Git!

### Где используется Git сегодня?

#### 1. **Разработка программного обеспечения**
- 99% проектов на GitHub используют Git
- Все крупные IT-компании (Google, Microsoft, Apple)
- Open Source проекты (Linux, React, Python)

#### 2. **Не только код!**
- Документация и книги
- Конфигурационные файлы
- Дизайн-проекты
- Научные исследования
- Юридические документы

#### 3. **DevOps и автоматизация**
- CI/CD пипелайны
- Infrastructure as Code
- Автоматическое развертывание

### Популярные платформы для Git

| Платформа | Описание | Особенности |
|-----------|----------|-------------|
| **GitHub** | Самая популярная | Open Source, Actions, Pages |
| **GitLab** | Полная DevOps платформа | CI/CD встроен, самохостинг |
| **Bitbucket** | От Atlassian | Интеграция с Jira |
| **Azure DevOps** | От Microsoft | Интеграция с .NET |

### Статистика использования Git

- **90%** разработчиков используют Git
- **100 миллионов** репозиториев на GitHub
- **70 миллионов** разработчиков на GitHub
- **Каждую секунду** создается ~10 новых репозиториев

### 🎯 Задание 2.1 (3 минуты)
Выберите правильные ответы:

1. Git был создан для разработки:
   - [ ] Windows
   - [ ] ядра Linux
   - [ ] веб-сайтов
   - [ ] мобильных приложений

2. Главное преимущество Git перед SVN:
   - [ ] Красивый интерфейс
   - [ ] Распределенная архитектура
   - [ ] Только для программистов
   - [ ] Платный продукт

3. Git можно использовать для:
   - [ ] Только кода
   - [ ] Только документации
   - [ ] Любых текстовых файлов
   - [ ] Только изображений

**Ответы:** 2, 2, 3

---

## 💾 Модуль 3: Установка и первоначальная настройка (20 минут)

### Установка Git

#### Windows
**Способ 1: Официальный установщик**
1. Скачайте с https://git-scm.com/download/windows
2. Установите с настройками по умолчанию
3. Откройте Git Bash или Command Prompt

**Способ 2: Через пакетный менеджер**
```powershell
# Chocolatey
choco install git

# Winget (Windows 10/11)
winget install Git.Git
```

#### macOS
```bash
# Homebrew (рекомендуется)
brew install git

# MacPorts
sudo port install git

# Или скачать с официального сайта
```

#### Linux (Ubuntu/Debian)
```bash
# Обновление пакетов
sudo apt update

# Установка Git
sudo apt install git

# Проверка версии
git --version
```

#### Linux (CentOS/RHEL/Fedora)
```bash
# CentOS/RHEL
sudo yum install git

# Fedora
sudo dnf install git
```

### Первоначальная настройка Git

После установки необходимо настроить Git:

```bash
# Настройка имени пользователя
git config --global user.name "Ваше Имя"

# Настройка email
git config --global user.email "your.email@example.com"

# Настройка редактора по умолчанию
git config --global core.editor "nano"
# или для vim:
# git config --global core.editor "vim"

# Настройка ветки по умолчанию
git config --global init.defaultBranch main
```

### Проверка настроек

```bash
# Посмотреть все настройки
git config --list

# Посмотреть конкретную настройку
git config user.name
git config user.email

# Посмотреть помощь
git help config
```

### Уровни конфигурации Git

```bash
# Системный уровень (для всех пользователей)
git config --system

# Глобальный уровень (для текущего пользователя)
git config --global

# Локальный уровень (для конкретного репозитория)
git config --local
```

### 🎯 Задание 3.1 (5 минут)
```bash
# 1. Проверьте версию Git
git --version

# 2. Настройте свое имя и email
git config --global user.name "Ваше Имя"
git config --global user.email "your@email.com"

# 3. Проверьте настройки
git config --list | grep user

# 4. Настройте редактор (выберите один)
git config --global core.editor "nano"
# или git config --global core.editor "vim"
```

### Создание первого репозитория

```bash
# Создать новую папку для проекта
mkdir my_first_project
cd my_first_project

# Инициализировать Git репозиторий
git init

# Посмотреть статус
git status

# Посмотреть скрытую папку .git
ls -la
```

### Структура папки .git

```
.git/
├── HEAD                # Указатель на текущую ветку
├── config              # Локальные настройки репозитория
├── description         # Описание репозитория
├── hooks/              # Скрипты-хуки
├── info/               # Дополнительная информация
├── objects/            # База данных объектов Git
├── refs/               # Ссылки на коммиты и ветки
└── index               # Staging area
```

### 🎯 Задание 3.2 (10 минут)
```bash
# 1. Создайте папку для тестового проекта
mkdir git_practice
cd git_practice

# 2. Инициализируйте репозиторий
git init

# 3. Создайте первый файл
echo "# Мой первый Git проект" > README.md
echo "Это файл README для изучения Git" >> README.md

# 4. Посмотрите статус
git status

# 5. Создайте еще несколько файлов
echo "print('Hello, Git!')" > hello.py
echo "console.log('Hello from JS');" > script.js

# 6. Снова проверьте статус
git status
```

---

## 🖥️ Модуль 4: Основные команды Git (30 минут)

### Жизненный цикл файлов в Git

```
Untracked → Staged → Committed
    ↑         ↑         ↓
    └─────────┴─── Modified
```

**Untracked** - файл не отслеживается Git  
**Staged** - файл добавлен в индекс (готов к коммиту)  
**Committed** - файл сохранен в репозитории  
**Modified** - файл изменен, но не добавлен в индекс  

### Основные команды

#### **git status** - статус репозитория
```bash
git status                    # Полный статус
git status --short           # Краткий статус
git status -s                # Еще более краткий
```

#### **git add** - добавление файлов в индекс
```bash
git add filename.txt         # Добавить конкретный файл
git add *.js                 # Добавить все JS файлы
git add .                    # Добавить все файлы в папке
git add -A                   # Добавить все изменения
git add -u                   # Добавить только измененные файлы
```

#### **git commit** - сохранение изменений
```bash
git commit -m "Описание изменений"     # Коммит с сообщением
git commit -am "Сообщение"             # Add + commit для отслеживаемых файлов
git commit                             # Открыть редактор для сообщения
git commit --amend                     # Исправить последний коммит
```

### 🎯 Задание 4.1 (8 минут)
```bash
# Продолжаем работать в папке git_practice

# 1. Добавьте файлы в индекс
git add README.md
git status

# 2. Сделайте первый коммит
git commit -m "Добавлен файл README"

# 3. Добавьте остальные файлы
git add .
git status

# 4. Сделайте второй коммит
git commit -m "Добавлены файлы hello.py и script.js"

# 5. Проверьте статус
git status
```

### Просмотр истории

#### **git log** - история коммитов
```bash
git log                              # Полная история
git log --oneline                    # Кратко, по одной строке
git log --graph                      # С графическим представлением
git log --graph --oneline --all      # Красивый граф всех веток
git log -n 5                         # Последние 5 коммитов
git log --author="Имя"               # Коммиты конкретного автора
git log --since="2 weeks ago"        # За последние 2 недели
```

#### **git show** - подробности коммита
```bash
git show                             # Последний коммит
git show HEAD~1                      # Предпоследний коммит
git show <commit-hash>               # Конкретный коммит
```

#### **git diff** - различия между версиями
```bash
git diff                             # Изменения в рабочей области
git diff --staged                    # Изменения в индексе
git diff HEAD~1                      # Сравнить с предыдущим коммитом
git diff HEAD~2 HEAD~1               # Между двумя коммитами
```

### 🎯 Задание 4.2 (8 минут)
```bash
# 1. Посмотрите историю коммитов
git log
git log --oneline

# 2. Измените файл README.md
echo "" >> README.md
echo "## Что я изучил:" >> README.md
echo "- Основы Git" >> README.md
echo "- Команды add, commit, status" >> README.md

# 3. Посмотрите различия
git diff

# 4. Добавьте изменения и закоммитьте
git add README.md
git commit -m "Обновлен README с информацией об изучении"

# 5. Посмотрите обновленную историю
git log --oneline
```

### Отмена изменений

#### Отмена изменений в рабочей области
```bash
git checkout -- filename.txt        # Отменить изменения в файле
git checkout .                       # Отменить все изменения
git restore filename.txt             # Новый способ (Git 2.23+)
git restore .                        # Отменить все изменения
```

#### Отмена изменений в индексе
```bash
git reset HEAD filename.txt          # Убрать файл из индекса
git reset HEAD                       # Убрать все файлы из индекса
git restore --staged filename.txt    # Новый способ (Git 2.23+)
```

#### Отмена коммитов
```bash
git reset --soft HEAD~1              # Отменить коммит, оставить изменения в индексе
git reset --mixed HEAD~1             # Отменить коммит и индекс
git reset --hard HEAD~1              # Отменить все (ОСТОРОЖНО!)
git revert HEAD                      # Создать новый коммит, отменяющий изменения
```

### Игнорирование файлов (.gitignore)

```bash
# Создайте файл .gitignore
nano .gitignore
```

**Содержимое .gitignore:**
```
# Скомпилированные файлы
*.pyc
*.class
*.o

# Логи
*.log
logs/

# Зависимости
node_modules/
venv/

# IDE файлы
.vscode/
.idea/

# Операционная система
.DS_Store
Thumbs.db

# Секретные файлы
.env
config.secret
```

### 🎯 Задание 4.3 (8 минут)
```bash
# 1. Создайте файл, который нужно игнорировать
echo "SECRET_KEY=12345" > .env
echo "password123" > secret.txt

# 2. Создайте .gitignore
echo ".env" > .gitignore
echo "secret.txt" >> .gitignore
echo "*.log" >> .gitignore

# 3. Проверьте статус
git status

# 4. Добавьте .gitignore в репозиторий
git add .gitignore
git commit -m "Добавлен .gitignore"

# 5. Создайте лог-файл и проверьте, что он игнорируется
echo "Это лог файл" > debug.log
git status

# 6. Попробуйте отменить изменения в файле
echo "Временное изменение" >> README.md
git diff
git restore README.md
git status
```

### Полезные алиасы для Git

```bash
# Настройка коротких команд
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.unstage 'reset HEAD --'
git config --global alias.last 'log -1 HEAD'
git config --global alias.visual '!gitk'

# Теперь можно использовать:
git st      # вместо git status
git co      # вместо git checkout
git ci      # вместо git commit
```

---

## 🌿 Модуль 5: Работа с ветками (30 минут)

### Что такое ветки в Git?

**Ветка (branch)** — это независимая линия разработки. Ветки позволяют:
- Работать над разными функциями параллельно
- Экспериментировать без риска сломать основной код
- Организовать командную работу
- Легко переключаться между задачами

### Зачем нужны ветки?

**Без веток:**
```
main: A → B → C → D → E → F
         ↑
    Баг в версии B!
```

**С ветками:**
```
main:        A → B → C → D
             ↓
hotfix:      B → Fix → merge
             ↓
feature:     B → F1 → F2 → F3
```

### Основные команды для работы с ветками

#### **git branch** - управление ветками
```bash
git branch                           # Показать все ветки
git branch -a                        # Показать все ветки (включая удаленные)
git branch new-feature               # Создать новую ветку
git branch -d feature-branch         # Удалить ветку (безопасно)
git branch -D feature-branch         # Принудительно удалить ветку
git branch -m old-name new-name      # Переименовать ветку
```

#### **git checkout** / **git switch** - переключение веток
```bash
# Старый способ (git checkout)
git checkout main                    # Переключиться на ветку main
git checkout -b new-feature          # Создать и переключиться на новую ветку

# Новый способ (git switch - с версии 2.23)
git switch main                      # Переключиться на ветку main
git switch -c new-feature            # Создать и переключиться на новую ветку
```

### 🎯 Задание 5.1 (8 минут)
```bash
# 1. Посмотрите текущие ветки
git branch

# 2. Создайте новую ветку для функции
git branch feature-contact-form

# 3. Переключитесь на новую ветку
git switch feature-contact-form
# или git checkout feature-contact-form

# 4. Проверьте, что переключились
git branch

# 5. Создайте файл для новой функции
echo "<h1>Контактная форма</h1>" > contact.html
echo "<form>Имя: <input type='text'></form>" >> contact.html

# 6. Добавьте и закоммитьте изменения
git add contact.html
git commit -m "Добавлена контактная форма"

# 7. Посмотрите историю
git log --oneline
```

### Слияние веток (merge)

#### Типы слияния

**1. Fast-forward merge (быстрое слияние)**
```
main:    A → B → C
         ↓
feature: C → D → E
```
После merge:
```
main: A → B → C → D → E
```

**2. Three-way merge (трехстороннее слияние)**
```
main:    A → B → C → F
         ↓         ↗
feature: C → D → E
```
После merge:
```
main: A → B → C → F → M
              ↘     ↗
feature:       D → E
```

#### Команды слияния
```bash
git merge feature-branch             # Слить ветку в текущую
git merge --no-ff feature-branch     # Принудительно создать merge commit
git merge --squash feature-branch    # Объединить все коммиты в один
```

### 🎯 Задание 5.2 (10 минут)
```bash
# 1. Переключитесь на main
git switch main

# 2. Создайте еще один файл
echo "body { margin: 0; }" > styles.css
git add styles.css
git commit -m "Добавлены базовые стили"

# 3. Посмотрите граф истории
git log --oneline --graph --all

# 4. Слейте ветку feature-contact-form
git merge feature-contact-form

# 5. Посмотрите результат
git log --oneline --graph --all
ls

# 6. Удалите ненужную ветку
git branch -d feature-contact-form
```

### Конфликты слияния

**Конфликт** возникает, когда Git не может автоматически объединить изменения.

#### Пример конфликта:
```html
<<<<<<< HEAD
<h1>Главная страница</h1>
=======
<h1>Домашняя страница</h1>
>>>>>>> feature-branch
```

#### Разрешение конфликта:
1. Откройте файл с конфликтом
2. Найдите маркеры `<<<<<<<`, `=======`, `>>>>>>>`
3. Выберите нужный вариант или объедините их
4. Удалите маркеры
5. Добавьте файл в индекс: `git add`
6. Завершите слияние: `git commit`

### 🎯 Задание 5.3 (12 минут)
```bash
# 1. Создайте две ветки с конфликтующими изменениями
git switch main

# Создайте ветку version-1
git switch -c version-1
echo "<h1>Добро пожаловать на сайт!</h1>" > index.html
git add index.html
git commit -m "Версия 1 заголовка"

# Переключитесь на main и создайте ветку version-2
git switch main
git switch -c version-2
echo "<h1>Привет, мир!</h1>" > index.html
git add index.html
git commit -m "Версия 2 заголовка"

# 2. Слейте version-1 в main
git switch main
git merge version-1

# 3. Попытайтесь слить version-2 (возникнет конфликт)
git merge version-2

# 4. Посмотрите статус
git status

# 5. Откройте index.html и разрешите конфликт
# Выберите один из вариантов или объедините:
echo "<h1>Добро пожаловать на наш сайт!</h1>" > index.html

# 6. Завершите слияние
git add index.html
git commit -m "Разрешен конфликт слияния заголовков"

# 7. Почистите ветки
git branch -d version-1 version-2
```

### Стратегии ветвления

#### 1. **Git Flow**
```
main     ────────────────→
         ↗              ↗
develop  ──────→────────→
         ↗    ↗ ↘
feature  →────  →────→
```

#### 2. **GitHub Flow**
```
main    ────────────────→
        ↗      ↗       ↗
feature →──────→───────→
```

#### 3. **GitLab Flow**
```
main        ────────────→
            ↗          ↗
production  ──────────→
```

### Полезные команды для веток

```bash
# Посмотреть последние коммиты в ветках
git branch -v

# Посмотреть объединенные ветки
git branch --merged

# Посмотреть необъединенные ветки
git branch --no-merged

# Переключиться на предыдущую ветку
git switch -

# Создать ветку из определенного коммита
git branch new-branch <commit-hash>
```

---

## 🌐 Модуль 6: Удаленные репозитории и GitHub (20 минут)

### Что такое удаленные репозитории?

**Удаленный репозиторий** — это версия вашего проекта, размещенная в интернете или сети. Позволяет:
- Синхронизировать работу между компьютерами
- Делиться кодом с другими разработчиками
- Создавать резервные копии
- Совместно работать над проектами

### Популярные хостинги Git

| Платформа | Особенности | Цена |
|-----------|-------------|------|
| **GitHub** | Самый популярный, Actions, Pages | Бесплатно для публичных |
| **GitLab** | CI/CD встроен, самохостинг | Бесплатно с ограничениями |
| **Bitbucket** | Интеграция с Atlassian | Бесплатно для команд до 5 |

### Создание репозитория на GitHub

1. Зайдите на https://github.com
2. Нажмите **"New repository"**
3. Введите название проекта
4. Выберите публичный или приватный
5. Нажмите **"Create repository"**

### Основные команды для удаленных репозиториев

#### **git remote** - управление удаленными репозиториями
```bash
git remote                           # Показать удаленные репозитории
git remote -v                        # Показать с URL
git remote add origin <url>          # Добавить удаленный репозиторий
git remote remove origin             # Удалить удаленный репозиторий
git remote rename origin upstream    # Переименовать удаленный репозиторий
```

#### **git push** - отправка изменений
```bash
git push origin main                 # Отправить ветку main
git push -u origin main              # Отправить и установить upstream
git push --all                       # Отправить все ветки
git push --tags                      # Отправить теги
git push origin --delete branch-name # Удалить удаленную ветку
```

#### **git pull** - получение изменений
```bash
git pull origin main                 # Получить изменения из main
git pull                             # Получить из upstream ветки
git pull --rebase                    # Получить с rebase вместо merge
```

#### **git fetch** - получение без слияния
```bash
git fetch origin                     # Получить все ветки
git fetch origin main                # Получить конкретную ветку
git fetch --all                      # Получить из всех удаленных репозиториев
```

#### **git clone** - клонирование репозитория
```bash
git clone <url>                      # Клонировать репозиторий
git clone <url> my-project           # Клонировать с новым именем
git clone --depth 1 <url>            # Клонировать только последний коммит
```

### 🎯 Задание 6.1 (10 минут)
```bash
# 1. Создайте репозиторий на GitHub (через веб-интерфейс)
# Назовите его: git-practice-[ваше-имя]

# 2. Добавьте удаленный репозиторий к локальному проекту
# Замените URL на ваш реальный URL
git remote add origin https://github.com/username/git-practice.git

# 3. Проверьте удаленные репозитории
git remote -v

# 4. Отправьте код на GitHub
git push -u origin main

# 5. Обновите README через веб-интерфейс GitHub
# Добавьте описание проекта

# 6. Получите изменения локально
git pull origin main

# 7. Посмотрите историю
git log --oneline
```

### Совместная работа с GitHub

#### Fork и Pull Request
1. **Fork** - создание копии чужого репозитория
2. **Clone** - клонирование вашего форка
3. **Branch** - создание ветки для изменений
4. **Commit** - внесение изменений
5. **Push** - отправка в ваш форк
6. **Pull Request** - запрос на слияние изменений

#### Синхронизация с оригинальным репозиторием
```bash
# Добавить оригинальный репозиторий
git remote add upstream <original-repo-url>

# Получить изменения из оригинала
git fetch upstream

# Слить изменения в свою ветку
git merge upstream/main
```

### SSH ключи для GitHub

#### Генерация SSH ключа
```bash
# Генерация ключа
ssh-keygen -t ed25519 -C "your_email@example.com"

# Запуск ssh-agent
eval "$(ssh-agent -s)"

# Добавление ключа в агент
ssh-add ~/.ssh/id_ed25519

# Показать публичный ключ (добавить в GitHub)
cat ~/.ssh/id_ed25519.pub
```

#### Тестирование соединения
```bash
ssh -T git@github.com
```

### 🎯 Задание 6.2 (10 минут)
```bash
# 1. Создайте новую ветку для функции
git switch -c feature-about-page

# 2. Создайте страницу "О нас"
echo "<h1>О нас</h1>" > about.html
echo "<p>Мы изучаем Git и это здорово!</p>" >> about.html

# 3. Добавьте ссылку в README
echo "" >> README.md
echo "## Страницы" >> README.md
echo "- [Главная](index.html)" >> README.md
echo "- [О нас](about.html)" >> README.md
echo "- [Контакты](contact.html)" >> README.md

# 4. Закоммитьте изменения
git add .
git commit -m "Добавлена страница О нас и навигация"

# 5. Отправьте ветку на GitHub
git push origin feature-about-page

# 6. Переключитесь на main и слейте изменения
git switch main
git merge feature-about-page

# 7. Отправьте обновленный main
git push origin main

# 8. Удалите ветку локально и удаленно
git branch -d feature-about-page
git push origin --delete feature-about-page
```

---

## 🎯 Итоговое практическое задание (20 минут)

### Финальный проект: Веб-сайт портфолио с командной работой

Создайте полноценный проект с использованием всех изученных возможностей Git.

#### Структура проекта:
```
portfolio-website/
├── README.md
├── index.html
├── about.html
├── portfolio.html
├── contact.html
├── css/
│   ├── style.css
│   └── responsive.css
├── js/
│   └── script.js
├── images/
│   └── .gitkeep
└── .gitignore
```

### Выполнение проекта:

```bash
# 1. Создайте новый репозиторий
mkdir portfolio-website
cd portfolio-website
git init

# 2. Создайте базовую структуру
mkdir css js images
touch css/style.css css/responsive.css js/script.js images/.gitkeep

# 3. Создайте .gitignore
cat > .gitignore << EOF
# Временные файлы
*.tmp
*.temp
.DS_Store
Thumbs.db

# Логи
*.log

# Зависимости
node_modules/

# Среда разработки
.vscode/
.idea/
EOF

# 4. Создайте README.md
cat > README.md << EOF
# Портфолио веб-сайт

Мой личный веб-сайт портфолио, созданный для изучения Git.

## Структура проекта

- \`index.html\` - Главная страница
- \`about.html\` - Страница "О себе"
- \`portfolio.html\` - Портфолио работ
- \`contact.html\` - Контактная информация
- \`css/\` - Стили
- \`js/\` - JavaScript код

## Технологии

- HTML5
- CSS3
- JavaScript
- Git для контроля версий

## Как запустить

Просто откройте \`index.html\` в браузере.

## История разработки

Проект создан в рамках изучения Git за 2 часа.
EOF

# 5. Создайте главную страницу
cat > index.html << EOF
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Мое Портфолио</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="index.html">Главная</a></li>
                <li><a href="about.html">О себе</a></li>
                <li><a href="portfolio.html">Портфолио</a></li>
                <li><a href="contact.html">Контакты</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section class="hero">
            <h1>Добро пожаловать в мое портфолио!</h1>
            <p>Я изучаю Git и веб-разработку</p>
        </section>
    </main>
    
    <script src="js/script.js"></script>
</body>
</html>
EOF

# 6. Добавьте базовые стили
cat > css/style.css << EOF
/* Базовые стили для портфолио */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    color: #333;
}

header {
    background: #2c3e50;
    color: white;
    padding: 1rem 0;
}

nav ul {
    list-style: none;
    display: flex;
    justify-content: center;
}

nav ul li {
    margin: 0 1rem;
}

nav ul li a {
    color: white;
    text-decoration: none;
    transition: color 0.3s;
}

nav ul li a:hover {
    color: #3498db;
}

.hero {
    text-align: center;
    padding: 4rem 2rem;
    background: #ecf0f1;
}

.hero h1 {
    font-size: 2.5rem;
    margin-bottom: 1rem;
    color: #2c3e50;
}
EOF

# 7. Первый коммит
git add .
git commit -m "Начальная структура портфолио сайта"

# 8. Создайте ветку для страницы "О себе"
git switch -c feature-about-page

cat > about.html << EOF
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>О себе - Мое Портфолио</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="index.html">Главная</a></li>
                <li><a href="about.html">О себе</a></li>
                <li><a href="portfolio.html">Портфолио</a></li>
                <li><a href="contact.html">Контакты</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section class="about">
            <div class="container">
                <h1>О себе</h1>
                <p>Привет! Я изучаю Git и веб-разработку.</p>
                
                <h2>Навыки</h2>
                <ul>
                    <li>Git - система контроля версий</li>
                    <li>HTML5 - разметка веб-страниц</li>
                    <li>CSS3 - стилизация</li>
                    <li>JavaScript - интерактивность</li>
                </ul>
                
                <h2>Опыт с Git</h2>
                <p>За 2 часа изучения Git я освоил:</p>
                <ul>
                    <li>Основные команды (add, commit, push, pull)</li>
                    <li>Работу с ветками и слияние</li>
                    <li>Удаленные репозитории и GitHub</li>
                    <li>Разрешение конфликтов</li>
                </ul>
            </div>
        </section>
    </main>
</body>
</html>
EOF

git add about.html
git commit -m "Добавлена страница О себе"

# 9. Вернитесь на main и создайте ветку для портфолио
git switch main
git switch -c feature-portfolio

cat > portfolio.html << EOF
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Портфолио - Мои работы</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="index.html">Главная</a></li>
                <li><a href="about.html">О себе</a></li>
                <li><a href="portfolio.html">Портфолио</a></li>
                <li><a href="contact.html">Контакты</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section class="portfolio">
            <div class="container">
                <h1>Мои проекты</h1>
                
                <div class="project">
                    <h2>Git Practice Project</h2>
                    <p>Изучение системы контроля версий Git</p>
                    <p><strong>Технологии:</strong> Git, GitHub, Bash</p>
                </div>
                
                <div class="project">
                    <h2>Portfolio Website</h2>
                    <p>Персональный веб-сайт портфолио</p>
                    <p><strong>Технологии:</strong> HTML5, CSS3, JavaScript</p>
                </div>
                
                <div class="project">
                    <h2>Future Project</h2>
                    <p>Здесь будет мой следующий проект</p>
                    <p><strong>Технологии:</strong> React, Node.js</p>
                </div>
            </div>
        </section>
    </main>
</body>
</html>
EOF

git add portfolio.html
git commit -m "Добавлена страница портфолио"

# 10. Объедините все ветки
git switch main
git merge feature-about-page
git merge feature-portfolio

# 11. Создайте контактную страницу прямо в main
cat > contact.html << EOF
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-size=1.0">
    <title>Контакты</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="index.html">Главная</a></li>
                <li><a href="about.html">О себе</a></li>
                <li><a href="portfolio.html">Портфолио</a></li>
                <li><a href="contact.html">Контакты</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section class="contact">
            <div class="container">
                <h1>Свяжитесь со мной</h1>
                <p>Буду рад обсудить проекты и возможности сотрудничества!</p>
                
                <div class="contact-info">
                    <p><strong>Email:</strong> your.email@example.com</p>
                    <p><strong>GitHub:</strong> github.com/yourusername</p>
                    <p><strong>LinkedIn:</strong> linkedin.com/in/yourprofile</p>
                </div>
            </div>
        </section>
    </main>
</body>
</html>
EOF

git add contact.html
git commit -m "Добавлена страница контактов"

# 12. Добавьте JavaScript
cat > js/script.js << EOF
// Простая интерактивность для портфолио

document.addEventListener('DOMContentLoaded', function() {
    console.log('Портфолио загружено!');
    
    // Подсветка активной страницы в навигации
    const currentPage = window.location.pathname.split('/').pop() || 'index.html';
    const navLinks = document.querySelectorAll('nav a');
    
    navLinks.forEach(link => {
        if (link.getAttribute('href') === currentPage) {
            link.style.color = '#3498db';
            link.style.fontWeight = 'bold';
        }
    });
    
    // Простая анимация для hero секции
    const hero = document.querySelector('.hero h1');
    if (hero) {
        hero.style.opacity = '0';
        hero.style.transform = 'translateY(20px)';
        hero.style.transition = 'all 0.8s ease';
        
        setTimeout(() => {
            hero.style.opacity = '1';
            hero.style.transform = 'translateY(0)';
        }, 100);
    }
});

// Функция для отображения текущего времени изучения Git
function showStudyTime() {
    const startTime = new Date('2024-01-01 10:00:00'); // Начало изучения
    const now = new Date();
    const studyHours = Math.floor((now - startTime) / (1000 * 60 * 60));
    
    console.log(\`Изучаю Git уже \${studyHours} часов!\`);
}

showStudyTime();
EOF

git add js/script.js
git commit -m "Добавлен JavaScript для интерактивности"

# 13. Обновите стили
cat >> css/style.css << EOF

/* Дополнительные стили */
.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 2rem;
}

.about, .portfolio, .contact {
    min-height: 70vh;
}

.project {
    background: white;
    padding: 1.5rem;
    margin: 1rem 0;
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    border-left: 4px solid #3498db;
}

.contact-info {
    background: #f8f9fa;
    padding: 2rem;
    border-radius: 8px;
    margin-top: 2rem;
}

.contact-info p {
    margin: 0.5rem 0;
}

/* Адаптивность */
@media (max-width: 768px) {
    nav ul {
        flex-direction: column;
        text-align: center;
    }
    
    nav ul li {
        margin: 0.5rem 0;
    }
    
    .hero h1 {
        font-size: 2rem;
    }
    
    .container {
        padding: 1rem;
    }
}
EOF

git add css/style.css
git commit -m "Улучшены стили и добавлена адаптивность"

# 14. Финальный коммит с тегом
git tag -a v1.0 -m "Первая версия портфолио сайта"

# 15. Показать итоговую историю
echo "🎉 Проект завершен! История разработки:"
git log --oneline --graph --all

echo ""
echo "📊 Статистика проекта:"
echo "Всего коммитов: $(git rev-list --count HEAD)"
echo "Всего файлов: $(find . -type f ! -path './.git/*' | wc -l)"
echo "Строк кода: $(find . -name '*.html' -o -name '*.css' -o -name '*.js' ! -path './.git/*' | xargs wc -l | tail -1)"
```

### Дополнительные задания (если есть время):

```bash
# 16. Создайте GitHub репозиторий и отправьте проект
# git remote add origin <your-repo-url>
# git push -u origin main
# git push --tags

# 17. Создайте Pull Request для новой функции
# git switch -c feature-dark-theme
# # Добавьте темную тему
# git push origin feature-dark-theme
# # Создайте PR через веб-интерфейс

# 18. Попробуйте GitHub Pages
# В настройках репозитория включите Pages
# Ваш сайт будет доступен по адресу: username.github.io/repository-name
```

---

## 📝 Итоговый тест

### Проверьте свои знания:

1. **Что такое Git?**
   - [ ] Текстовый редактор
   - [ ] Система контроля версий
   - [ ] Веб-сервер
   - [ ] База данных

2. **Какая команда создает новый коммит?**
   - [ ] git save
   - [ ] git commit
   - [ ] git push
   - [ ] git add

3. **Как создать новую ветку?**
   - [ ] git branch new-branch
   - [ ] git create new-branch
   - [ ] git new new-branch
   - [ ] git make new-branch

4. **Что делает команда git pull?**
   - [ ] Отправляет изменения на сервер
   - [ ] Получает изменения с сервера
   - [ ] Создает новую ветку
   - [ ] Удаляет файлы

5. **Для чего нужен файл .gitignore?**
   - [ ] Для ускорения Git
   - [ ] Для игнорирования файлов
   - [ ] Для настройки Git
   - [ ] Для документации

6. **Как разрешить конфликт слияния?**
   - [ ] git resolve
   - [ ] Отредактировать файл и сделать git add + git commit
   - [ ] git fix
   - [ ] git merge --fix

7. **Что такое fork на GitHub?**
   - [ ] Команда Git
   - [ ] Копия чужого репозитория
   - [ ] Ветка
   - [ ] Конфликт

8. **Какая команда показывает историю коммитов?**
   - [ ] git history
   - [ ] git log
   - [ ] git show
   - [ ] git list

### Ответы:
1. 2, 2. 2, 3. 1, 4. 2, 5. 2, 6. 2, 7. 2, 8. 2

---

## 🎓 Заключение

### Что вы изучили за 2 часа:

✅ **Основы Git** - понимание системы контроля версий  
✅ **Установка и настройка** - первоначальная конфигурация  
✅ **Основные команды** - add, commit, status, log, diff  
✅ **Работа с ветками** - создание, слияние, разрешение конфликтов  
✅ **Удаленные репозитории** - GitHub, push, pull, clone  
✅ **Практические навыки** - реальный проект портфолио  

### Git команды - шпаргалка:

#### Начало работы:
```bash
git init                    # Инициализация репозитория
git clone <url>            # Клонирование
git config --global user.name "Name"
git config --global user.email "email"
```

#### Базовые операции:
```bash
git status                 # Статус
git add .                  # Добавить все файлы
git commit -m "message"    # Коммит
git log --oneline         # История
git diff                  # Различия
```

#### Ветки:
```bash
git branch                # Список веток
git switch -c new-branch  # Создать и переключиться
git merge branch-name     # Слияние
git branch -d branch-name # Удалить ветку
```

#### Удаленные репозитории:
```bash
git remote add origin <url>  # Добавить удаленный репозиторий
git push -u origin main      # Первая отправка
git pull origin main         # Получить изменения
git fetch                    # Получить без слияния
```

### Куда двигаться дальше:

1. **Продвинутые возможности Git**
   - Rebase и интерактивный rebase
   - Cherry-pick
   - Stash
   - Hooks

2. **Командная работа**
   - GitFlow и другие workflow
   - Code Review
   - Continuous Integration

3. **DevOps интеграция**
   - Git + Docker
   - Автоматическое развертывание
   - GitHub Actions / GitLab CI

4. **Инструменты**
   - GUI клиенты (GitKraken, SourceTree)
   - IDE интеграция
   - Git в VSCode

### Полезные ресурсы:

- **Pro Git Book**: https://git-scm.com/book (бесплатная книга)
- **GitHub Learning Lab**: https://lab.github.com/
- **Atlassian Git Tutorials**: https://www.atlassian.com/git/tutorials
- **Interactive Git Tutorial**: https://learngitbranching.js.org/

### Практические советы:

1. **Коммитьте часто** - маленькие, логичные изменения
2. **Пишите понятные сообщения** коммитов
3. **Используйте ветки** для каждой новой функции
4. **Регулярно синхронизируйтесь** с удаленным репозиторием
5. **Изучайте чужой код** через GitHub

**Поздравляем!** Вы освоили основы Git и готовы использовать его в реальных проектах. Git - это мощный инструмент, который станет вашим постоянным спутником в разработке. Продолжайте практиковаться и изучать новые возможности!