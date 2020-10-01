[*<< back to lessons list*](../readme.md)

# Lesson 6 - Sevices, WorkManager, Notifications
## Overview
// todo 


## To read
#### Notifications
- [Документация](https://developer.android.com/training/notify-user/build-notification)
- [статья](https://itnext.io/android-notification-all-in-one-8df3e1218e0e)

#### WorkManager
- [video](https://www.youtube.com/watch?v=pe_yqM16hPQ)
- [Документация](https://developer.android.com/topic/libraries/architecture/workmanager/basics)
- [WorkManager codelab](https://codelabs.developers.google.com/codelabs/android-workmanager/#0)
- (optional) [Use WorkManager for immediate background execution](https://medium.com/androiddevelopers/use-workmanager-for-immediate-background-execution-a57db502603d)

#### Service
- [Документация](https://developer.android.com/guide/components/services.html)
- [урок](http://developer.alexanderklimov.ru/android/theory/services-theory.php)

#### разное
- [JobScheduler codelab](https://codelabs.developers.google.com/codelabs/android-training-job-scheduler/index.html#0)
- [Schedule repeating alarms](https://developer.android.com/training/scheduling/alarms)

## Задание
#### 1. Прокачать Таймер из предыдущего задания
- теперь он должен адекватно реагировать на сворачивание: не должен останавливаться, если сворачивается, то должна быть нотификация где будет видно продолжающийся обратный отсчет
- уведомить пользователя про то что он закончил отсчет

#### 2. TimeManagerApp 
задача написать приложение которое будет помогать нам быть продуктивными и управлять своим временем. Приложение состоит из 3 основных частей:
- таймер
- будильник
- Pomodoro manager
теперь более подробно
1. **Таймер**. Самая простая часть, берем наш прокачанный таймер из прошлого задания и гармонично размещаем в нашем приложении 
2. **Будильник**. Он должен делаьт то что делает будильник, просто, без излишеств, но удобно. И вы ему должны доверять :) 
3. **Pomodoro manager**. Нужно почитать что такое [Метод Pomodoro](https://uk.wikipedia.org/wiki/%D0%9C%D0%B5%D1%82%D0%BE%D0%B4_Pomodoro), базируясь на принципах метода, разработать приложение

Общие пожелания:
- продумать навигацию так, что бы приложением удобно было пользоваться
- вести статистику того как пользователь выполняет помодоро, отдельный экран для нее сделать