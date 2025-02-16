# Как сделать свои собственные обои (день/ночь) с Win Dynamic Desktop
В этом руководстве мы погрузимся в процесс создания двойных обоев (день/ночь) для вашего ПК или ноутбука. Многие пользователи предпочитают различные приложения для удобной смены обоев, и мы остановимся на приложении Win Dynamic Desktop. В этом приложении представлено множество готовых обоев, но иногда они могут не соответствовать вашим предпочтениям. В таких случаях вы можете создать свои собственные уникальные обои, которые идеально подойдут именно вам.

## Для начала работы нам понадобится:
1. Два изображения с расширением `.JPG` или `.PNG` (рекомендуется `.JPG`), которые будут слушить нам обоями для нашего рабочего стола ПК. Изображения могут быть совершенно любые, мы же рассмотрим на примере двух подготовленных изображений, которые находятся в папке `Background` (Названия изображений: `Mystery_Shack_1`, `Mystery_Shack_2`).
2. Непосредственно само приложение для смены обоев по времени (день/ночь) [Win Dynamic Desktop](https://apps.microsoft.com/detail/9NM8N7DQ3Z5F?hl=neutral&gl=RU&ocid=pdpshare) (Скачать приложение из официального магазина Microsoft-Store)
3. Также любой Архиватор-Файлов-Zip, который в конце нашей работы все компоненты приобразует в `файл.zip`. Для этого подойдет [WinRaR](https://www.win-rar.com/) (Скачать приложение с официального сайта WinRaR)

## Приступим к созданию/написанию `json файла`:
1. Открываем приложение Блокнот (станндартное приложение Windows, которое есть у всех пользователей) или нажимаем кнопку `Windows` и набираем слово "Блокнот"
2. Данный текстовый файл (с расширением `.json`, которое мы потом сделаем) будет служить указание для приложения Win Dynamic Desktop. Прощего говоря, в текстовом файле будет находиться указания, по которым приложение будет понимать какую картинку использовать (1 или 2 или ...) и когда (день/ночь)
3. Для ознакомления с базавыми командами для json файла, рекоммендую прочитать данную статью ([Ссылка на статью github](https://github.com/t1m0thyj/WinDynamicDesktop/wiki/Creating-custom-themes)). Статья на английском языке, но перевести страницу на русский язык не составит труда (Google translate / DeepL translate / Яндекс переводчик / Встроенный переводчик страниц в вашем бруезере).
4. В статье рассказывается про 2 вида создания `json файла`, мы же будем использовать короткий, который будет менять наши обои 2 раза в сутки (день/ночь).
5. Готовый `json код` для текстового файла:
```json
{
  "imageFilename": "Mystery_Shack_*.jpg",
  "imageCredits": "Windows",
  "dayImageList": [
    1
  ],
  "nightImageList": [
    2
  ]
}
```
___
> `"imageFilename"` - указываем название на изображение шаблон (Например: у нас есть два изображения `"Mystery_Shack_1"` и `"Mystery_Shack_2"`. Какая-то часть названия у них совпадает, мы пишем эту совпадающую часть и на конце, где цифры, мы ставим звездочку (`*`). Звездочка (`*`) обозначает у нас любой символ, любой конец нашего шаблона)
___
> `"imageCredits"` - указываем авторские права на двойные обои, имя или название создателя обоев (Например: Apple, Windows, Иван Иванович Иванов, программист_228)
___
> `"dayImageList"` - изображение, которое будет использоваться днем (во внутрь команды пишем окончание названия изображения (1 или 2 или ...). День: Шаблон + окончание = `Mystery_Shack_` + `1` = `Mystery_Shack_1`)
___
> `"nightImageList"` - изображение, которое будет использоваться ночью (во внутрь команды пишем окончание названия изображения (1 или 2 или ...). Ночь: Шаблон + окончание = `Mystery_Shack_` + `2` = `Mystery_Shack_2`)
___
6. Нажимаем `Ctrl` + `S` - наш компьютер открывает окно проводника и предлагет задать имя, формат файла (Выбираем (папку, место) куда мы хотим сохранить файл. Пишем название файла, добавляя в конце к ниму `.json`. Также выбираем тип файла `Все файлы`, чтобы файл принял форму не `текстовый файл`, а ту которую мы ему задали, дописав в конце названия `.json`) и нажимаем `сохранить`:
![](https://github.com/Un1korm/Own-Double-Wallpaper-WinDynamicDesktop/blob/main/Instruction_Files/%D0%A1%D0%BE%D1%85%D1%80%D0%B0%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5_json_%D1%84%D0%B0%D0%B9%D0%BB%D0%B0.png)
7. Выделяем `два изображения обоев (день/ночь)` и `json файл`, нажимаем провой клавишей мыши по любому из трех файлов (2-а изображения, 1 json файл) и выбираем `"добавить в архив..."`:
![](https://github.com/Un1korm/Own-Double-Wallpaper-WinDynamicDesktop/blob/main/Instruction_Files/%D0%90%D1%80%D1%85%D0%B8%D0%B2%D0%B8%D1%80%D1%83%D0%B5%D0%BC_%D1%84%D0%B0%D0%B9%D0%BB%D1%8B_1.png)
8. 
