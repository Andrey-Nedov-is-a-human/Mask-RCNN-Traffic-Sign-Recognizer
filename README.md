# Система распознавания дорожных знаков с использованием Mask-RCNN / Making a traffic sign recognition system using Mask-RCNN

<img src="/Release/img1.png" alt="img1" width="800"/>

*Разработчики/Developers*
1. [Олег Ботнарь](https://github.com/fronos)
2. [Андрей Недов](https://github.com/Andrey-Nedov-is-a-human)


## Задание
Сделать изолированную систему, принимающую на вход изображение с передней камеры автомобиля, отдающая на выходе JSON файл с разметкой, описывающей маски и классы всех найденных на изображении дорожных знаков.

## Архитектура системы
<img src="/Release/img2.jpg" alt="img1" width="800"/>

Общение с системой происходит по двум UDP портам: <br/> 
1. UPD UI - пользовательская консоль управления конфигурацией системы
2. UDP manager - порт по которому система получает изображения и отдаёт JSON разметку

## Mask-RCNN
Модель Mask-RCNN обучалась на датасете, составленном из записей с камер видеорегистраторов и размеченном в редакторе.

<img src="/Release/img4.png" alt="img1" width="800"/>

Обученную модель можно скачать из хранилища по ссылке [model.pt](https://drive.google.com/file/d/1vuOjKoNq4VE6BUToBDe6hceUEEWTRve_/view?usp=sharing)

## Консольный интерфейс системы

Консольный интерфейс системы (справа) имеет набор параметров, позволяющих задавать область интереса на изображении (ROI), устанавливать порог для классификатора и т.д.

<img src="/Release/img6.jpg" alt="img1" width="800"/>

## Результат работы программы

<img src="/Release/img3.jpg" alt="img1" width="800"/>

Система разрабатывалась в рамках проекта по созданию беспилотоного автомобиля - одного из главных проектов ИТ-факультета [Московского Политеха](https://new.mospolytech.ru/) и ушла дальше по пайплайну. Записей с результатом работы найти не удалось, нашлись вот только пара тестовых обработанных системой картинок.




