# Версии библиотеки
1. opencv-python - любая версия (у меня 4.9.0.80)
2. tensorflow - не старше 2.16.*, иначе ломается самописный слой, хорошо работают версии младше 2.12.0 (Включая саму 2.12.0)
3. jupyter - любая версия (у меня 1.0.0)
4. matplotlib - любая версия (у меня 3.8.4)
5. Python 3.11.3

# Как это работает
Запустив код первое что вас встретит это открытие окна камеры, вам нужно создать тестовые наборы данных позитивных изображений и пары якорей для работы кода, якоря - входные данные, позитивные изображения - люди которые будут верифицированы

в конце кода камера откроется снова, но в этот раз с обученной моделью, вы передаёте в неё только якоря, и в результатах она выводит True - человек с камеры верифицирован или False - Человек не верифицирован

# Советы
Модель обучена на 5 эпоха и малом сете якорей и положительных изображений, возможно из-за чего существует проблема не распознания если освещение стало другим. Полезной практикой будет делать позитивные изображения с разными уровнем освещённости и оттенка.
Если модель обучена слаба, как в данном примере на 5 эпохах, то сеть в частых случаях верифицирует человека по цвету кожи....