# Шпаргалка по VIM

## Выход, сохранение, редактирование

| Команда                      | Описание                           |
| ---------------------------- | ---------------------------------- |
| :q                           | выход из файла                     |
| :w                           | сохранить файл/записать содержимое |
| :e                           | обновить содержимое файла          |
| !                            | выполнить команду в любом случае   |
| :wq                          | команды можно совмещать(в данном примере файл будет сохранен и закрыт) |
| :q!                          | команды можно совмещать(выйти в любом случае, например, после сделанных изменений, без их сохранения) |

## Общее использование

| Команда                      | Описание                          |
| ---------------------------- | --------------------------------- |
| i                            | режим вставки/ввода               |
| a                            | режим вставки/ввода               |
| ESC (Ctrl+[)                 | обычный режим                     |
| hjkl                         | перемещение в разные стороны      |
| o                            | добавить строку сразу за текущей  |
| O                            | добавить строку перед текущей     |
| u                            | отмена последней команды          |
| Ctrl+r                       | отмена отмены последней команды(redo)/повтор последней команды   |
| gg                           | перейти в начало документа        |
| Shift+g                      | перейти в конец документа         |
| Shift+a                      | перейти в конец строки и перейти в режим редактирования |
| Shift+v                      | перейти в визуальный режим        |
| dd                           | удалить текущую строку (вырезать) |
| yy                           | копировать строку                 |
| p                            | вставить из буфера обмена         |
| /                            | начать вводить поисковую фразу    |
| n                            | следующий результат поиска        |
| Shift+n                      | предыдущий результат поиска       |
| ^                            | переход в начало строки           |
| $                            | переход в конец строки            |
| Ctrl+b                       | перемещение на один экран назад   |
| Ctrl+f                       | перемещение на один экран вперед  |
| mа                           | создания закладки с именем 'a'    |
| 'a                           | переход к созданной закладке 'a'  |

## Окна, вкладки и т.д.

| Команда                      | Описание                          |
| ---------------------------- | --------------------------------- |
| ctrl+w s                     | горизонтальное разделение окна    |
| ctrl+w v                     | вертикальное разделение окна      |
| ctrl+w <клавиша перемещения> | перемещение к окну                |
| ctrl+w K                     | текущее окно сделать верхним      |
| ctrl+w _                     | текущее окно сделать макс размер  |
| ctrl+w =                     | выровнять все окна                |

## Работа со вкладками

| Команда                      | Описание                          |
| ---------------------------- | --------------------------------- |
| :tabnew [filename]	       | открыть новую вкладку             |
| :tabf pat*ern	               | открыть вкладку по шаблону        |
| :tabs	                       | список открытых вкладок           |
| gt или :tabn	               | следующая вкладка                 |
| g Shift+t или :tabp          | предыдущая вкладка                |
| :tabfirst или :tabfir        | первая вкладка                    |
| :tablast                     | последняя вкладка                 |
| :tabm n                      | переместить вкладку в n (от 0)    |
| :tabdo command               | выполнить над всеми вкладками     |

* [Небольшая статья на хабре](https://habrahabr.ru/post/102373/)

## Возможные настройки для .vimrc

### Использовать 4 пробела вместо табов

Добавьте в файл `~/.vimrc`:
```
set tabstop=4
" when indenting with '>', use 4 spaces width
set shiftwidth=4
" On pressing tab, insert 4 spaces
set expandtab
```

### Использовать стрелки для перемещения

Добавьте в файл `~/.vimrc`:
```
:set nocompatible
```

*Сразу предупреждаю, что использовать стрелки для навигации в VIM - плохая манера, ибо
десятипальцевая печать(вам приходится убирать правую руку с привычного положения),
замедляется скорость и т.д. (загуглите сами)*

## License

* MIT 2016
* based on [zualex repo](https://github.com/zualex/vim-cheat-sheet)