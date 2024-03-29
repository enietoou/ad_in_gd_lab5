# АНАЛИЗ ДАННЫХ И ИСКУССТВЕННЫЙ ИНТЕЛЛЕКТ [in GameDev]
Отчет по лабораторной работе #5 выполнил:
- Бобоев Азизджон Рахматович
- РИ-220935
Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | * | 20 |
| Задание 3 | * | 20 |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

Работу проверили:
- к.т.н., доцент Денисов Д.В.
- к.э.н., доцент Панов М.А.
- ст. преп., Фадеев В.О.

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

## Цель работы
Познакомиться с программными средствами для создания системы машинного обучения и ее интеграции в Unity.

## Задание 1
### Найдите внутри C# скрипта “коэффициент корреляции ” и сделать выводы о том, как он влияет на обучение модели.
Ход работы:
- Проанализировать код скрипта, найти "коэффициент корреляции" и сделать выводы.

В нашем случае коэффициент корреляции отражает связь между объектом и его целью. Анализ кода показал, что текущую связь выражает переменная "distanceToTarget", а значение 1.42f - это важный параметр, который влияет на обучение.
Чем больше этот параметр, тем сложнее становится задача для агента, так как объект должен находиться ближе к цели. При этом увеличивается время обучения и точность модели.
Следовательно чем меньше параметр, тем легче задача, так как объект может находиться дальше от цели. Время и точность модели при этом уменьшаются.
![image](https://github.com/enietoou/ad_in_gd_lab5/assets/74960429/0b222b36-5c06-4135-9a74-f4d76cd4afc7)


## Задание 2
### Изменить параметры файла yaml-агента и определить какие параметры и как влияют на обучение модели. Привести описание не менее трех параметров.
- Изменение batch_size:
```yaml
hyperparameters:
  batch_size: 32
```
Влияние: Увеличение batch_size увеличит количество образцов, использованных для одного обновления модели. Обучение становится более стабильным, но требует больших объемов памяти.

- Изменение learning_rate:
```yaml
hyperparameters:
  learning_rate: 1.0e-4
```
Влияние: Изменение learning_rate влияет на скорость обучения. Уменьшение скорости обучения делает обучение более стабильным.

- Изменение num_layers:
```yaml
network_settings:
  num_layers: 3
```
Влияние: Увеличение num_layers увеличивает глубину нейронной сети. Это может помочь модели выучивать более сложные зависимости, но может потребовать больше времени для обучения.

- Изменение max_steps:

```yaml
max_steps: 750000
```
Влияние: Увеличение max_steps продляет время обучения. Это может быть полезно, если модель требуется больше времени для достижения оптимальных результатов, но также может привести к избыточному обучению, если увеличивать слишком сильно.

## Задание 3
### Приведите примеры, для каких игровых задачи и ситуаций могут использоваться примеры 1 и 2 с ML-Agent’ом. В каких случаях проще использовать ML-агент, а не писать программную реализацию решения?

#### Примеры использования ML-Agent в игровых задачах:

- Управление персонажем в симуляции:
Агент должен научиться управлять персонажем в виртуальной среде, избегая препятствий и собирая ресурсы.

- Обучение стратегии в стратегической игре:
Разработка и обучение искусственного интеллекта для настольной стратегической игры, где агент должен принимать сложные стратегические решения.

- Обучение ботов в компьютерных играх:
Создание ботов для многопользовательских компьютерных игр, где агенты должны соревноваться с реальными игроками.

- Автономное вождение в автосимуляторах:
Разработка системы автопилота для автомобиля в симулированной среде с разнообразными условиями дорожного движения.

#### Проще использовать ML-Agent:

- Когда задача слишком сложна или требует адаптации к изменяющейся среде.

- Когда невозможно предоставить точные инструкции или стратегии из-за большого числа вариантов.

- Когда задача требует принятия множества решений и программа должна настраиваться автоматически.

## Выводы

В ходе лабораторной работе я познакомился с инструментом ML-Agent для создания системы машинного обучения и успешно внедрил его в Unity. Попробовал изменять .yaml файл и изучить влияние параметров на обучение модели. Также я научился выводить результаты обучения через TebsorBoard.


**BigDigital Team: Denisov | Fadeev | Panov**
