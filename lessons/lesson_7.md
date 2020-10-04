[*<< back to lessons list*](../readme.md)

# Lesson 7 - Architecture: part 1
## Overview
// todo 

## Links
- документация: [Guide to app architecture](https://developer.android.com/jetpack/guide)
- [урок про MVP](https://startandroid.ru/ru/blog/493-mvp-dlja-nachinajuschih-bez-bibliotek-i-interfejsov.html)
- [стили и темы](https://developer.android.com/guide/topics/ui/look-and-feel/themes)

##### Clean architecture
- [классное видео](https://www.youtube.com/watch?v=AlxMGxs2QnM)
- статья [Заблуждения Clean Architecture](https://habr.com/ru/company/mobileup/blog/335382/)
- статья [Коротко о главном: Clean Architecture, Robert C. Martin](https://habr.com/ru/post/464185/)

## Задание
#### Пишем заметки 
Clean architecture, MVP
##### 1. Базовый функционал
- на главном экране расположен список заметок, пока что это `ScrollView` и `LinearLayout`),  
в которые динамически добавляются вьюшки заметок
- заметка состоит из названия и текста
- в углу расположена [FAB](https://material.io/components/buttons-floating-action-button), по клику на неё переходим на экран создания заметки
- на экране создания заметки поля для ввода названия, текста, в меню - кнопка сохранить, отменить  
- заметки должны сохраняться, у заметки должна быть дата создания 

##### 2. Улучшаем функционал
- Убираем `ScrollView` и `LinearLayout`, вместо них располагаем заметки в `RecyclerView`
- прикручиваем возможность удалять заметку по свайпу в `RecyclerView`
- добавляем возможность по клику по заметке перейти к экрану редактирования заметки (изменить, удалить)
 
##### 3. Добавляем создание фото-заметки 
- разбираемся что такое `sealed class` в Kotlin. Разбираемся с viewtype в `RecyclerView` и как их использовать с sealed классами
- добавляем еще одну FAB по клику на которую переходим на экран создания фото заметки.
- фото получаем с активити камеры([урок](https://startandroid.ru/ru/uroki/vse-uroki-spiskom/68-urok-29-vyzyvaem-activity-i-poluchaem-rezultat-metod-startactivityforresult.html) и [документация](https://developer.android.com/training/basics/intents/result) нового способа(пока в альфе)), 
полученное изображение отображаем в `ImageView`
- к фото заметке можно точно так же добавить название
  
##### 4. Улучшаем фотозаметку 
- теперь можно выбрать источник фото: камера или галерея
- Делаем так что бы можно было рисовать по созданной фотографии (используем библиотечку)


[*<< back to lessons list*](../readme.md)
