# Подготовка данных для прогнозирования стоимости аренды квартир

## Содержание
- [Подготовка данных для прогнозирования стоимости аренды квартир](#подготовка-данных-для-прогнозирования-стоимости-аренды-квартир)
  - [Содержание](#содержание)
  - [Обзор проекта](#обзор-проекта)
  - [Члены команды](#члены-команды)
  - [Структура проекта](#структура-проекта)
  - [Итерации подготовки данных](#итерации-подготовки-данных)
    - [Релиз 1.0](#релиз-10)
    - [Релиз 2.0](#релиз-20)
    - [Релиз 3.0](#релиз-30)
  - [Источник данных](#источник-данных)
  - [Использование](#использование)
  - [Заключение](#заключение)

## Обзор проекта
Этот проект направлен на подготовку датасета для разработчиков машинного обучения, которые будут использовать его для обучения моделей прогнозирования стоимости аренды квартир. Качество их моделей во многом зависит от подготовленных нашей командой данных. Нам поручена самая сложная часть работы с данными, чтобы обеспечить высокое качество результатов.

## Члены команды и зона ответственности
- [Tolubai Dzhakeshev] - 
  Колонки: Метро/Адрес, Площадь, Кол-во комнат, Дом, Адрес. 
  Также, ответственный за релизы.
- [Еркебулан Тыныбек] - 
  Колонки: Цена, Ремонт, Балкон. 
  Также, ответственный за шутки.
- [Nastya] - 
  Колонки: последние 7 колонок от Окна до Дополнительно и др до Мусоропровод. 
  Также, общая descriptive stats / text for managers. 
  Расстановка Приоритетов (со дня 2).


## Структура проекта
Репозиторий имеет следующую структуру:
- `README.md`: Описание проекта, члены команды и подробные инструкции для каждого релиза.
- `EDA.html`: Полный отчет по разведочному анализу данных.
- `EDA.ipynb`: Jupyter ноутбук, использованный для разведочного анализа данных.
- `preprocessing.ipynb`: Jupyter ноутбук, документирующий процесс очистки и генерации признаков данных.
- `data.csv`: Очищенный и обработанный датасет, готовый для обучения моделей машинного обучения.

## Итерации подготовки данных

### Релиз 1.0
**Цель**: Провести разведочный анализ данных (EDA) для понимания структуры датасета, выявления закономерностей и аномалий.

**Результаты**:
- `README.md`: Описание проекта и члены команды.
- `EDA.html`: HTML-отчет, сгенерированный из ноутбука `EDA.ipynb`, содержащий визуализации, агрегированную информацию и минимальное количество кода.
- `EDA.ipynb`: Jupyter ноутбук с процессом разведочного анализа данных.

### Релиз 2.0
**Цель**: Очистить датасет от пропущенных значений и обеспечить его согласованность для дальнейшей обработки.

**Результаты**:
- `preprocessing.ipynb`: Jupyter ноутбук, детализирующий процесс очистки данных.
- `data.csv`: Очищенный датасет, в котором:
  - Названия колонок на английском языке, в формате snake_case.
  - Отсутствуют пропущенные значения (NaN, None и т.д.).

### Релиз 3.0
**Цель**: Финализировать датасет, добавив новые признаки, и подготовить его для обучения моделей.

**Результаты**:
- `README.md`: Обновлено с основными выводами и иллюстрациями из анализа.
- `data.csv`: Финальный датасет, в котором:
  - Все значения являются числовыми (int или float).
  - Отсутствуют полные дубликаты объявлений, только уникальные объявления.
  - Сохранена колонка с ID объявления для сравнения результатов различных команд.
- `preprocessing.ipynb`: Обновленный ноутбук, документирующий весь процесс обработки данных с комментариями, объясняющими мотивацию принятых решений.

## Источник данных
Датасет, используемый в этом проекте, был предоставлен командой инженеров данных и содержит различные атрибуты объявлений о аренде квартир.

## Использование
1. **Разведочный анализ данных**:
   - Откройте `EDA.ipynb` для просмотра процесса разведочного анализа.
   - Просмотрите `EDA.html` для получения суммарного отчета с визуализациями.

2. **Очистка данных**:
   - Следуйте ноутбуку `preprocessing.ipynb` для понимания процесса очистки данных и обработки пропущенных значений.
   - Используйте `data.csv` как очищенный датасет.

3. **Генерация признаков**:
   - Обратитесь к обновленному `preprocessing.ipynb` для полного процесса обработки данных и генерации признаков.
   - Финальный `data.csv` включает новые признаки и готов для обучения моделей.

## Заключение
Этот проект обеспечивает создание высококачественного датасета для обучения моделей машинного обучения по прогнозированию стоимости аренды квартир. Каждый релиз строится на предыдущем, постепенно улучшая качество и полезность датасета.
