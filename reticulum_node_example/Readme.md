
# Примеры разметки для страниц ноды в сети Ретикулум (NomadNet)

### Стиль текста

```micron
Normal text followed by `!bold text`! then back to normal.

Here is `*italic text`* in a sentence.

And some `_underlined text`_ for emphasis.

Combine them: `!`*`_bold italic underlined`_`*`!
```

### Reset Formatting

```micron
`!`*`_All formatting on`` and now everything is reset.
```

## Цвета

### Цвет текста

```micron
`Ff00Red`f `F0f0Green`f `F00fBlue`f text.

`Ff80Orange`f `Fff0Yellow`f `F0ffCyan`f `Ff0fMagenta`f
```

### Цвет заднего фона

```micron
`Bf00 Red background `b
`B0f0 Green background `b
`B00f Blue background `b
```

### Комбинирование цветов

```micron
`Bf00`FfffWhite text on red background`f`b
`B222`FdddLight text on dark background`f`b
```

### Grayscale

```micron
`g00Black `g25Dark gray `g50Medium gray `g75Light gray `g99White`f
```

### Нотификейшен бокс

```micron
`B5d5`F222 Notice: This is an important message `f`b
`Bf55`FfffError: Something went wrong `f`b
`B5bf`F000Success: Operation completed `f`b
```

## Выравнивание

### Текст по центру страницы

```micron
`cThis text is centered.
Still centered on this line.
`aBack to default alignment.
```

### Текст справа

```micron
`rRight-aligned text
Also right-aligned
`lNow left-aligned
```

### Смешаное 

```micron
`cWelcome to My Node
`a

>Navigation
`l`[Home`:/page/index.mu]
`[About`:/page/about.mu]

`r`*Last updated: 2024-01-15`*
```

## Секции с Заголовками

### Базовая структура

```micron
>Main Section
Content in the main section is indented.

>>Subsection
More indented content.

>>>Sub-subsection
Even more indented.

<
Back to no indentation.
```

### Ещё Секции 

```micron
>Visible Heading
Some content here.

>>
This subsection has no heading but is still indented.

<
Normal text again.
```

### Document Outline

```micron
>Introduction
Brief overview of the topic.

>Features
>>Core Functionality
Description of core features.

>>Advanced Options
Description of advanced options.

>Getting Started
>>Installation
Installation instructions.

>>Configuration
Configuration steps.
```

## Разделители

### Базовые 

```micron
Some content above.

-

Some content below.
```

### Стилизованые разделители

```micron
-∿
```

Wavy divider.

```micron
-═
```

Double-line divider.

```micron
-●
```

Dotted divider.

## Ссылки

### Simple Links

```micron
Visit `[e9eafceea9e3664a5c55611c5e8c420a:/page/index.mu]
```

### Ссылки с подписями

```micron
`[Click here to visit the home page`e9eafceea9e3664a5c55611c5e8c420a:/page/index.mu]
```

### Стилизованые ссылки

```micron
`F0af`_`[Home Page`:/page/index.mu]`_`f
`F0af`_`[About Us`:/page/about.mu]`_`f
`F0af`_`[Contact`:/page/contact.mu]`_`f
```

### Локальные ссылки

```micron
`[Go to settings`:/page/settings.mu]
`[Download file`:/file/document.pdf]
```

### Навигационное меню

```micron
>Navigation

`F0af`_`[Home`:/page/index.mu]`_`f
`F0af`_`[Browse`:/page/browse.mu]`_`f
`F0af`_`[Search`:/page/search.mu]`_`f
`F0af`_`[About`:/page/about.mu]`_`f
```

## Формы ввода

### Поле для ввода текста

```micron
>Contact Form

Name: `B444`<name`>`b

Email: `B444`<email`>`b

Message:
`B444`<60|message`>`b
```

### Поле для ввода пароля

```micron
>Login

Username: `B444`<16|username`>`b

Password: `B444`<!16|password`>`b
```

### Размеры полей

```micron
First Name: `B444`<20|first_name`>`b
Last Name: `B444`<20|last_name`>`b
Age: `B444`<3|age`>`b
```

### Чекбоксы

```micron
>Preferences

`B444`<?|newsletter|yes`>`b Subscribe to newsletter

`B444`<?|notifications|yes`>`b Enable notifications

`B444`<?|dark_mode|yes|*`>`b Use dark mode (pre-checked)
```

### Кнопки

```micron
>Select Color

`B900`<^|color|red`>`b Red

`B090`<^|color|green`>`b Green

`B009`<^|color|blue`>`b Blue
```

### Выбор по умолчанию

```micron
>Priority

`<^|priority|low`> Low
`<^|priority|medium|*`> Medium (default)
`<^|priority|high`> High
```

## Отправка форм

### Отправка всех полей

```micron
>Registration

Username: `B444`<username`>`b
Email: `B444`<email`>`b
Password: `B444`<!|password`>`b

`[Create Account`:/page/register.mu`*]
```

### Отправка некоторых полей

```micron
>Quick Search

Query: `B444`<query`>`b

`[Search`:/page/search.mu`query]
```

### Вставка переменных

```micron
`[View Page 1`:/page/list.mu`action=view|page=1]
`[View Page 2`:/page/list.mu`action=view|page=2]
`[View Page 3`:/page/list.mu`action=view|page=3]
```

### Комбинирование полей и переменных

```micron
>Search

Query: `B444`<query`>`b

Results per page:
`<^|limit|10`> 10
`<^|limit|25`> 25
`<^|limit|50`> 50

`[Search`:/page/search.mu`query|limit|sort=relevance]
```

## Комментарии

```micron
# This line is not displayed
This line is visible.

>Section
# Hidden comment in section
Visible content.
```

## Literal Mode

### Вставка блоков кода

```micron
Example code:

`=
def hello():
    print("Hello, World!")

hello()
`=
```

### Showing Micron Syntax

```micron
To make text bold, use:

`=
`!Bold text`!
`=
```

## Примеры готовых страниц

### Default Wellcome page

```micron
#!c=3600
#!fg=ddd
#!bg=222

`c`!Welcome to My Node`!
`a

-∿

>About

This is a NomadNet node hosting information and files.

>>Features

 - Browse pages
 - Download files
 - Interactive forms

>Navigation

`F0af`_`[Home`:/page/index.mu]`_`f
`F0af`_`[Files`:/page/files.mu]`_`f
`F0af`_`[About`:/page/about.mu]`_`f
`F0af`_`[Contact`:/page/contact.mu]`_`f

-∿

`c`*Powered by NomadNet`*
```

### Форма авторизации

```micron
#!c=0

>Login

`cPlease enter your credentials
`a

-

Username: `B444`<20|username`>`b

Password: `B444`<!20|password`>`b

`<?|remember|yes`> Remember me

-

`[Sign In`:/page/auth.mu`*]

`F888`*Don't have an account?`* `F0af`_`[Register`:/page/register.mu]`_`f
```

### Листинг Файлов

```micron
#!c=300
>Available Downloads

>>Documents

`[User Guide (PDF)`:/file/docs/user_guide.pdf]
`[API Reference (PDF)`:/file/docs/api_reference.pdf]
`[FAQ (TXT)`:/file/docs/faq.txt]

>>Software

`[Latest Release (ZIP)`:/file/software/release_v1.0.zip]
`[Source Code (TAR.GZ)`:/file/software/source.tar.gz]

>>Media

`[Logo (PNG)`:/file/media/logo.png]
`[Banner (PNG)`:/file/media/banner.png]

-

`c`F888Total: 7 files available`f
```

### Динамически обновляемая страница на Python

```python
#!/usr/bin/env python3
import os
import time

print("#!c=0")
print(">Node Status")
print("")
print(f"Current Time: {time.strftime('%Y-%m-%d %H:%M:%S')}")
print("")

# System info
print(">>System")
uptime = os.popen('uptime -p').read().strip()
print(f"Uptime: {uptime}")
print("")

# Show request info if available
username = os.environ.get('field_username', '')
if username:
    print(f"Hello, `!{username}`!")
else:
    print(">>Login")
    print("Username: `B444`<username`>`b")
    print("`[Submit`:/page/status.mu`username]")
```

### Доска сообщений

```python
#!/usr/bin/env python3
import time
import os

print('`!`F222`Bddd`cMessage Board')
print('-')
print('`a`b`f')
print("")

board_peer = 'e9eafceea9e3664a5c55611c5e8c420a'
print(f"To post a message, send LXMF to: `[lxmf@{board_peer}]")
print(f"Last Updated: {time.strftime('%Y-%m-%d %H:%M:%S')}")
print("")

print('>Messages')
print("")

# Read and display messages from storage
messages = [
    "2024-01-15 10:30 | Alice | Hello everyone!",
    "2024-01-15 11:45 | Bob | Great to see this working!",
    "2024-01-15 14:22 | Charlie | Testing the board.",
]

for msg in messages:
    print(f"`a{msg}")
    print("")
```
### Динамически обновляемая страница на PHP

для формирования страниц на php необходимо установить php на ноду, дать нужной странице права и незабыть указать шибэнг на адрес интерпритатора

Лайк Зыс
```php
sudo apt-get install php
cd ~/.nomadnetwork/storage/pages/
echo "Hello Everybody">php_page.mu
sudo chmod +x php_page.mu
```
затем приступить к редактированию этой страницы через vi/nano/emacs и.д.
```php
#!/usr/bin/php
Hello Everybody
<?php echo "This is my first page in Reticulum Network";?>
```
