### Модель ветвления: Git Flow 

> Данная моделя является практической реализацией основных принципов разработки ПО в VCS с учетом релизных циклов ПО. 
Подходит как для Scrum, так и для Waterfall.

#### Принципы

* Две главные ветки:
⋅⋅⋅ * master - текущая стабильная версия, работающая на пром-среде
⋅⋅⋅ * develop - основная ветка разработки

* Вспомогательные ветки:
⋅⋅⋅ * feature - новый функционал или исправление некритичных багов; сливаются в develop
⋅⋅⋅ * release - фиксация и стабилизация релиза (feature-freeze); сливаются в master и develop
⋅⋅⋅ * hotfix - исправление критичных багов; сливаются в master и develop

* Все слияния происходят только через pull-request'ы

Плюсы:

| Плюсы:        | Минусы:                |
| ------------- |------------------:|
| Фиксация и стабилизация функционала релиза до попадания на пром     | Не самая простая схема работы; требует досконального понимания от разработчика, какие ветки откуда создаются и куда сливаются    |
| Возможность выпускать ночные сборки (nightly build)     | Готовый функционал попадает на пром с некоторой задержкой |

[Удачная модель ветвления для Git:](https://habr.com/ru/post/106912/)

[Previous Theme](/Git%2BTerminal/Git.md) | [Back To Contents](https://github.com/eldaroid/iosBasics) |  [Next Theme]()