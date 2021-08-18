[*<< back to lessons list*](../readme.md)

# Lesson 0 - Basic of Android
## Overview
Узнаем как-что установить, почитаем про андроид и немного про другие полезные вещи 

## Links 
##### SOLID 
https://habr.com/ru/post/508086/

##### Про ООП
https://tproger.ru/translations/oop-principles-cheatsheet/

##### Про GIT 
Нужно уметь:
- создавать репозиторий на гитхаб 
- пушить свой код на репозиторий 
- делать коммит / пуш 
- создавать новые ветки
- стягивать изменения с гита
- клонировать репозиторий с гитхаба на комп

##### Code style
- [Kotlin](https://developer.android.com/kotlin/style-guide)
- [Java](https://google.github.io/styleguide/javaguide.html) 
- [xml id naming](https://jeroenmols.com/blog/2016/03/07/resourcenaming/)

##### Немного про дизайн
Мы не на курсе по дизайну. Но приложения должны выглядеть нормально :) приятно для глаз. 

Спокойные цвета, стандартные элементы - это хорошо. Если на экран тяжело смотреть дольше 10 секунд - это плохо :)
[Тут](https://material.io/design/color/the-color-system.html) можно почитать про цветовые схемы, [тут](https://material.io/resources/color/#!/?view.left=0&view.right=0) - поэкспериментировать с палитрами цветов 

В целом, на [material.io](https://material.io/) очень много всяких советов по тому как сделать приложения которые хорошо выглядят. Очень рекомендую поизучать  

##### Основы создания приложений
https://developer.android.com/guide/components/fundamentals

##### Activity
[документация](https://developer.android.com/reference/android/app/Activity)

[жизненный цикл Активити](https://developer.android.com/guide/components/activities/activity-lifecycle)

- [Build your first app](https://developer.android.com/training/basics/firstapp)
- урок [Layout параметры](https://startandroid.ru/ru/uroki/vse-uroki-spiskom/38-urok-7-layout-parametry-dlja-view-elementov.html)
- урок [Работаем с элементами экрана из кода](https://startandroid.ru/ru/uroki/vse-uroki-spiskom/24-urok-8-rabotaem-s-elementami-ekrana-iz-koda.html)
- docs: [App resources overview](https://developer.android.com/guide/topics/resources/providing-resources.html#ResourceTypes)

## Tasks
0. Прочитать блок `Build your first app`, ссылки которые есть в этом уроке

1. Установить студию, запустить Hello world 
2. Создать (если еще нет) [github](https://github.com/) аккаунт, в репозиториях которого мы и будем работать 
3. Сделать приложение:
- вверху должно быть поле ввода, кнопка "отправить". 
ниже (с отступом) TextView для вывода данных на экран
- по клику на "отправить" текст из поля ввода удаляется и появляется в TextView вывода
- внизу экрана оставить "подпись" `made by <your name>`. 
этот текст брать из ресурсов строк, перевести на несколько языков

## Tips 
##### Вывод в консоль 
В андроиде вам не поможет System.out.println(), если нужно что-то вывести в консоль используйте [Log](https://developer.android.com/reference/android/util/Log) 

##### Выучите горячие клавиши, это вам хорошо ускорит работу 
Вот список: https://developer.android.com/studio/intro/keyboard-shortcuts
Мой топ:
- Multi-cursor: `alt+J` (select text and press it to do magic :) )
- Duplicate current line or selection	`Control+D`/`Command+D`
- Project quick fix (show intention actions and quick fixes):	`Alt+Enter`/`Option+Enter`
- Basic code completion	`Control+Space`/`Control+Space`
- ....

Вернуться к [*Lessons list*](../readme.md)  
Вперед к  [*Lesson 1 - First app*](./lesson_1.md)