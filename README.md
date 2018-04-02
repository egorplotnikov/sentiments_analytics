## Задача

Сделать классификатор тональности твитов. Подразумевается бинарная классификация, а именно: положительная и отрицательная окраска.

## Используемые инструменты и библиотеки
* Язык - Python 3.6;
* Библиотеки - Pandas, Scikit-Learn, PyMorphy2;

## Данные для обучения

Датасет создавался на основе [готовой выборки](http://study.mokoron.com/), состоящей приблизительно из 225 тысяч размеченных твитов .

Из твитов удалялись все символы, не входящие в кириллицу, затем производилась лемматизация слов.

## Модель

За основу берется алгоритм SGDClassifier и осуществляется подбор параметров с помощью GreedSearchCV. Для векторизации используется TF-IDF Vectorizer. 

Её точность оказалась ≈ 0.76.