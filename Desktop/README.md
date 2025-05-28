# Установка ОС

Выбрал Minimal Installation, файловую систему ZFS.

## Отключение отображения zpool, rpool

Чтобы в меню не отображались диски zpool, rpool, нужно: 
```
mkdir -p ~/.config/udisks2
nano ~/.config/udisks2/nodisplay.conf
```

Добавить:
```
[loop]
display=internal

[rpool]
display=false

[bpool]
display=false
```

Перезагрузить компьютер.

# Кастомизация пользовательского интерфейса
## Смена комбинации для смены раскладки

Выполнять от своей учётной записи без sudo:
```
gsettings set org.gnome.desktop.wm.keybindings switch-input-source "['<Ctrl>space']"
```

