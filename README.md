# Проект: Перенос знаний (Transfer Learning) в глубоких нейронных сетях

## Описание
Этот проект посвящён применению подходов переноса знаний (transfer learning) для решения задачи классификации объектов. В качестве исходного датасета используется **Garbage Classification**. Проект реализован с использованием нескольких предобученных архитектур глубоких нейронных сетей, таких как ResNet18, GoogLeNet, Inception и VGG16.

Основной метрикой для оценки качества классификации выбрана **F1-score**.

---

## Структура проекта

- **`lab_transfer_learning.ipynb`**: Основной Notebook с кодом, реализующим обучение и тестирование моделей.
- **`README.md`**: Документация проекта.
- **`requirements.txt`**: Зависимости для запуска проекта.

---

## Установка и запуск

### Предварительные требования
- Python 3.9+
- Среда выполнения: Kaggle или локальная машина с GPU

### Установка зависимостей
1. Установите Python и виртуальную среду (рекомендуется).
2. Установите зависимости из `requirements.txt`:
   ```bash
   pip install -r requirements.txt
   ```
---

## Основные шаги

1. **Импорт библиотек и настройка среды:**
   - Используются библиотеки `torch`, `torchvision`, `pandas`, `matplotlib`, `seaborn` и `tqdm`.

2. **Загрузка данных:**
   - Датасет **Garbage Classification** загружается и предобрабатывается для подготовки данных к обучению моделей.

3. **Предобработка данных:**
   - Включает нормализацию изображений, разделение данных на тренировочные и тестовые выборки.

4. **Использование моделей переноса знаний:**
   - Реализованы и протестированы следующие модели:
     - **ResNet18**
     - **GoogLeNet**
     - **Inception**
     - **VGG16**
   - Используется три подхода к переносу знаний:
     Обучение только последнего слоя модели.

-Полное обучение архитектуры нейронной сети.

-Разморозка нескольких последних слоёв и их дообучение.

5. **Оценка модели:**
   - Основной метрикой выступает **F1-score**, которая оценивается на тестовой выборке.
   - Результаты визуализируются с использованием `matplotlib` и `seaborn`.

---

## Зависимости

Основные библиотеки, используемые в проекте:
- `torch`
- `torchvision`
- `tqdm`
- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`

Все зависимости перечислены в `requirements.txt`.

---

## Автор
Максим Балашов

---

## Примечания
- Рекомендуется использовать среду с GPU для ускорения обучения моделей.
- Убедитесь, что датасет **Garbage Classification** доступен для загрузки. Для работы на Kaggle датасет может быть подключен через Kaggle Datasets.

