# EnDeCoder v1.11f

Это программа для шифрования ваших файлов по ключу с моим собственным уникальным алгоритмом шифрования

Программа работает на **Windows**


## Ключ

Ключ нужен, чтобы каждый байт вашего файла шифровался по заданным командам (Не забудьте его записать!)

Ключ состоит из подряд идущих команд:

`ia ra mp rp d ser sel spr spl sbr sbl`

Чтобы самостоятельно составить ключ, вам нужно взять понравившиеся команды из списка выше (команды могут повторяться) потом без пробела подставить в одну строку

**К примеру:**
- Выбираем команды по желанию: `ra` `spr` `ia`
- Составляем список: `ra spr ra ia spr`
- Убираем пробелы, и вот твой **Ключ**: `rasprraiaspr`



## Как запустить?
- Скачать `main.exe` и `config.ini` в одну папку. Или скачать архив и разархивировать в папку
- В эту же папку с программой перенести файл, который надо зашифровать или расшифровать (*можете скопировать файл если вам удобно*)
- Запустить `main.exe`
- Ввести корректно все данные (**НЕ ЗАБУДЬТЕ СОХРАНИТЬ КЛЮЧ**)
- Подтвердить данные
- Ждать окончания выполнения программы
- После корректного завершения программы у вас будет готовый файл с дополнением в названии `_encoded` или `_decoded` в той же директории
- Ваш оригинальный файл ни как не пострадает


## Пометки
- Если программа зависает, когда прогресс-бары приближаются к значению `90-100%`, это значит, что она сохраняет в оперативную память часть байтов, чтобы распределить их по потокам, и скоро продолжит работу

- Рядом с исполняемым файлом должен быть файл `config.ini`, иначе работать не будет

- Перед началом шифрования или расшифровки у вам покажут данные, и попросят ввести `y` или `n`, там же в поле `ключ` будет показан ваш **ключ**, лучше запишите его

- Оригинальный файл не подвергается изменениям, и если преждевременно завершить программу, то с вашим файлом ничего не случиться


## Конфиг
В конфиге находятся некоторые настройки программы:
- `parts_of_giga` - Это число, на которое будет делаться Гигабайт по байтам, и полученное частное - это сколько памяти будет находиться в оперативной памяти компьютера (чем меньше, тем программе легче, но тем медленнее)

- `count_threads` - Количество потоков, которые будут обрабатывать байты, с какого-то числа (примерно с `100`) их количество будет тормозить программу, так что оставляйте примерно на `64` **НО** никто не запрещает ставить это число больше

- `width` - Это ширина прогресс-баров, влияет только на визуальную составляющую

- `clear_delay_seconds` - Это десятичное число, обозначающее через какой промежуток (в секундах) будет обновляться прогресс-бары при работе (не влияет на подвисания)

- `random_key_length_min` - Минимальная длинна случайного ключа (не в символах, а в количестве команд)

- `random_key_length_max` - Максимальная длинна случайного ключа (не в символах, а в количестве команд)