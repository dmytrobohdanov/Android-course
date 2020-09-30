[*<< back to lessons list*](../readme.md)

# Lesson 3 - Навигация и хранение данных
## Overview
Если раньше мы располагали элементы приложения в активити, то на 
этом уроке познакомимся с фрагментами, научимся делать навигацию по экранам, поработаем с хранением данных 


## To read
#### про фрагменты
- [документация](https://developer.android.com/guide/components/fragments)

#### Navigation component
- [видео](https://www.youtube.com/watch?v=Y0Cs2MQxyIs)
- [документация](https://developer.android.com/guide/navigation/navigation-getting-started)

#### Shared preferences
- [документация](https://developer.android.com/training/data-storage/shared-preferences)

#### `DataStore`
на момент написания находится в альфе, но пора учить, документация дело говорит: 

```If you're currently using SharedPreferences to store data, consider migrating to DataStore instead.```
- [документация](https://developer.android.com/topic/libraries/architecture/datastore)
- [статья](https://medium.com/scalereal/hello-datastore-bye-sharedpreferences-android-f46c610b81d5)

#### Room 
Это абстракция над SQLite, которая упрощает людям жизнь. очень сильно упрощает :) 
- [видео](https://www.youtube.com/watch?v=SKWh4ckvFPM&list=PLWz5rJ2EKKc9mxIBd0DRw9gwXuQshgmn2&index=5)
- [документация](https://developer.android.com/training/data-storage/room)
- [codelab](https://codelabs.developers.google.com/codelabs/android-room-with-a-view-kotlin/#0)
- [уроки](https://codelabs.developers.google.com/codelabs/kotlin-coroutines/#0) 


## Задание
### Часть 1 - экспериментируем
- Раньше, в качестве БД использовали `SQLite`. Почитайте обязательно [документацию](https://developer.android.com/training/data-storage/sqlite). И для того что бы понять, на сколько прекрасен `Room` очень рекомендую потыкать [уроки 34-36](https://startandroid.ru/ru/uroki/vse-uroki-spiskom/74-urok-34-hranenie-dannyh-sqlite.html). Гугл не рекомендует пользоваться SQLite напрямую, если вы прочитали статью, то знаете почему :), но знать про то как с этим работать нужно  
- поробуйте посохранять данные в `SharedPreferences` и `DataStore`. Попробуйте посохранять как простые типы(инт, стринг), так и кастомные объекты
В продакшене не стоит использовать библиотеки (даже гугловые) которые в альфе, но для уроков вполне ок использовать будет `DataStore` (если он конечно не будет лагать)
- потыкать этот [урок](https://startandroid.ru/ru/uroki/vse-uroki-spiskom/175-urok-105-android-3-fragments-dinamicheskaja-rabota.html) что бы понять работу с `FragmentManager`, после того как появился Navigation component это не очень актуально, но знать про него нужно 
- создайте активити, положите в нее фрагмент, залогируйте методы жизненного цикла активити и фрагментов, с помощью навигации (или фрагмент менеждера) попутешействуйте по вашим экранам, сверните, разверните приложение в разных местах, посмотрите что после чего вызывается в каких ситуациях 
- разберитесь как сделать навигацию в [Navigation Drawer](https://material.io/components/navigation-drawer) (используя Navigation component)  

### Часть 2 - пишем квиз
- в активити расположите [BottomNavigation](https://material.io/components/bottom-navigation) состоящую из 3 вкладок: "квиз", "статистика" и "настройки", каждая - свой фрагмент
#### Вкладка Настройки
тут можно менять настройки, сделать свои, вот вам [ссылка для вдохновения](https://material.io/components/selection-controls#usage), но например:
- выбрать уровень сложности квиза (легкий/сложный), выбор реализовать с помощью [Spinner](https://developer.android.com/guide/topics/ui/controls/spinner)
- показывать ли правильный ответ после выбора ответа пользователем 
в общем, используйте разные элементы для настроек

#### Вкладка Статистика  
отображать разную статистику: количество игр, количество выиграных игр, количество правильных ответов и тп

#### Вкладка Квиз  
Квиз состоит из 3 экранов 
1. экран старта игры (или продолжения если игра была прервана)
2. экран с вопросами: есть вопросы, и несколько вариантов ответа
3. экран завершения игры: по факту текст и кнопка "закрыть", по клику на которую юзер попадает на экран старта новой игры 

- вопросы брать из JSON файла который поместить в `assets`. Да, вопросы нужно придумать(или скачать где-нибудь), но суть задания не в вопросах, поэтому не сильно заморачивайтесь. Для чтения JSON строк есть очень хороший инструмент: [Gson](https://github.com/google/gson).  
- продумайте как ведет себя приложение если пользователь его свернул в разные моменты игры 