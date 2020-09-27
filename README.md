# Разработка модели для классификации текстовых отзывов

## Доступные данные:
- Размеченный набор текстовых отзывов по критерию негативности комментария

## Задача
Необходимо построить модель для классификации отзывов.
Целевая метрика - f1. Качество по метрике - не менее 0.75 на тестовой выборке.

Этапы:
- Подготовка набора текстов к анализу: лемматизация, токенизация. 
- Обучение простых моделей логистической регрессии и random forest
- Обработка набора отзывов предобученной нейросетью BERT

## Выводы и результаты:
1. Наиболее высокую F1-меру на тестовой выборке (0.756) показала логистическая регрессия.
2. Модель случайного леса показала менее качественный результат в сравнении с регрессией при дОльшем обучении и подборе гиперпараметров.
3. Загружена, сконфигурирована и применена нейросеть BERT для создания эмбеддингов и модификации признаков. Качество обученной на этих признаках логистической регрессии нестабильно и не удовлетворяет требованиям. Предположительно, это вызвано недостаточным размером сэмпла, который может быть посчитан на обычном компьютере.

## Используемые библиотеки:
- nltk
- pytorch
- BERT
- sklearn
- numpy
- pandas
