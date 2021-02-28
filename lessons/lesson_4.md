[*<< back to lessons list*](../readme.md)

# Lesson 4 - Асинхронность и корутины
## Overview
Работая над приложениями вы столкнетесь с многопоточностью. Задача урока подготовится к этому

В целом есть достаточно много способов: EventBus, AsyncTask, Loaders, ExecutorService, Handler, Rx, Coroutines (и наверняка что-то еще). Актуальные - последние два. этим и займемся ближайшие 2 урока  

## Links
#### Про многопоточность в андроиде
- документация: [Processes and threads overview](https://developer.android.com/guide/components/processes-and-threads). Читать на английском, русский вариант в устаревшей версии  
- [видео: Android Coroutines: How to manage async tasks in Kotlin](https://www.youtube.com/watch?v=6manrgTPzyA) 

#### Про Handler
Вот [урок](https://startandroid.ru/ru/uroki/vse-uroki-spiskom/143-urok-80-handler-nemnogo-teorii-nagljadnyj-primer-ispolzovanija.html)

#### Coroutines
- [документация](https://kotlinlang.org/docs/reference/coroutines/basics.html)
- [codelab](https://codelabs.developers.google.com/codelabs/kotlin-coroutines/#0)
- мой [доклад](https://github.com/dmytrobohdanov/coroutines-talk) про корутины, там и примеры, и много инфы про корутины



## Tasks
0. Пройти вышеупомянутый урок про Handler 

1. поэксперементировать с запуском корутин
- запустить несколько параллельных корутин (например 100.000), 
- понять как работает coroutineScope, coroutineContext, launch, async, join, await(), awaitAll() и т.д. Для этой части можно использовать вышеупомянутый доклад, пройти все примеры которые есть в нем

2. Написать класс Таймер, 
- Пишем на корутинах. Задача написать таймер который бы вы могли использовать в будущем в своих программах. На входе задаем временной промежуток, есть метод старта таймера, на выходе - класс должен оповещать о завершении времени, и про "тик" времени. Остальные опции по желанию, полагаемся на свою фантазию :-)
- создаем андроид проект, используем наш класс для того что бы сделать обратный отсчет времени, на экране кнопки старт, стоп, начать заново, поле ввода времени для таймера и собственно отображение минут-секунд. 
- добавить кнопку "сколько осталось до нового года"
- на данном достаточно что бы таймер работал только при запущенном приложении, прокачаем его на следующих уроках     



[*<< back to lessons list*](../readme.md)
