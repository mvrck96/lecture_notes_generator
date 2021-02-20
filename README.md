# Маленький скрипт для генерации `.md` файлов для конспектирования лекций

Основная идея: перед началом конспектирования лекции, в директории предмета выполнить скрипт, который создаст файл вида `%current_dir_name%_%date%.md`, который автоматически открывается в `Typora`.

## Пример выполнения

```bash
user@host:~/University/SQL$ lecture_maker.sh s
user@host:~/University/SQL$ ls
SQL_sem_15.02.21.md
```

Для корректной работы сrрипта надо скопировать его в любую из директорий, которая добавлена в переменную`PATH`, или добавить директорию со скриптом в `PATH`

Добавить текущую директорию в `PATH` можно так: `export PATH=$PATH:$(pwd)`

Посмотреть папки которые глобально доступны: `echo $PATH`

## Шаблон файла

Текущий шаблон выглядит вот так

```markdown
# %Название_предмета% %семинар|лекция% 20.02.21


```

## Возможные дополнения

- Добавить автоматическую нумерацию (???)
- ~~Добавить полное название предмета на русском в первую строку файла~~
- Переписать всё на `python` и посмотреть в чем будет разница (??)
- ~~Сразу передавать созданный файл в `Typora`~~
- ~~Сделать модуль для лекция и для семинаров~~
- Написать скрипт который будет формировать словарь типа `subj_handler`: `subj_name` на основании гугл таблички
