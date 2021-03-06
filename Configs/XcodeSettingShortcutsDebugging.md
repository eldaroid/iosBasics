## 1. Удаление строки

Settings -> Key binding (связка ключей) -> Delete Line (Delitions). Sets to Ctrl + K

## 2. Настройка навигации 

<img src="https://github.com/eldaroid/pictures/blob/master/other/navigation_Xcode.png" alt="alt text" width="450" height="250">

## 2. Непонятные ошибки при компиляции

Исправить ситуацию позволяет `Clean Build Folder` ⇧⌘K и ручное удаление производных данных `rm -rf ~/Library/Developer/Xcode/DerivedData` (в папке DerivedData записываются symbolicate crash logs - расшифровки крэш-логов).

## 3. Debugging

Стоит знать основы и понимать, что Apple / Xcode пытается сказать вам через logs.

```
H = Horizontal constraint(for leading and Trailing)
V = Vertical constraint(top and bottom edge)
h = height
w = width

TopEdge    -> V:|-(points)-[VIEW:memoryAddress] 
BottomEdge -> V:[VIEW:memoryAddress]-(points)-|
Leading    -> H:|-(points)-[VIEW:memoryAddress] 
Trailing   -> H:[VIEW:memoryAddress] -(points)-|
height     -> h= --& v=--& V:[VIEW:memoryAddress((points)] 
width      -> VIEW:memoryAddress.width == points 
between    -> H:[VIEW 1]-(51)-[VIEW 2] 
```

# Буквы в навигаторе проектов

A-Added (это новый файл, который был добавлен в репозиторий)

C-конфликт (в файле есть конфликт)

D-удалено (файл был удален)

M-Modified (существующий файл был изменен)

R-переименован (файл был переименован)

U-Untracked (файл новый или был изменен, но еще не добавлен в репозиторий)

## 4 Открывать файлы

Открывать класс в новой вкладке: 

`Cmd + Ctrl + Click` - в новой вкладке

`Cmd + Ctrl + Option + Click` - в новом окне

