# ДЗ по графам и word2vec

Ваша задача построить сеть для произвольного [семантического поля](https://www.krugosvet.ru/enc/gumanitarnye_nauki/lingvistika/SEMANTICHESKOE_POLE.html), где узлами будут слова, а ребрами наличие косинусного расстояния ≥0.5 в word2vec-модели (можно взять любую). Алгоритм работы следующий:

1. Выберите какое-нибудь семантическое поле, например, "транспорт", "глаголы говорения" и т.п. и в качестве первого узла или нескольких первых узлов возьмите любые слова из этого поля. Слова должны быть одной части речи! 
2. Найдите соседей узла (узлов), заданного вами в качестве отправной точки, отфильтруйте их по значению косинусной близости и добавьте в граф.
3. Найдите соседей узлов, добавленных на предыдущем этапе, отфильтруйте их по значению косинусной близости и добавьте в граф.
4. Вычислите самые центральные узлы графа по degree centrality, betweenness centrality, closeness centrality и eigencentrality. 
5. Вычислите плотность графа, его диаметр, радиус, коэффициент кластеризации и коэффициент ассортативности.
6. Попробуйте разделить граф на сообщества (можно выбрать любой алгоритм) и интерпретировать эти сообщества. Интерпретацию нужно написать в отдельной текстовой ячейке после кода, разбивающего граф на сообщества, или после визуализации графа. 
7. Визуализируйте граф. Размер и цвет узлов должен соответствовать каким-то параметрам — например, размер может показывать центральность по любой из метрик, а цвет — разбиение на сообщества. Выбранные параметры должны быть указаны либо в комментариях к коду, либо в отдельной текстовой ячейке с описанием графа. Узлы должны быть подписаны. 

**NB! Задание выполняется в виде .ipynb-тетрадки. Однако, если вы решите делать веб-приложение на бонусный балл, необходимо сдать обычный .py скрипт (или несколько скриптов).**

## Критерии оценки

|Балл|Критерий|
|----|--------|
|1|Программа запускается и оформлена по PEP8. Соответствие PEP8 можно проверить с помощью команды `pycodestyle my_script_name.py` в командной строке.|
|2|Строится граф для какого либо семантического поля. Находятся соседи первого и второго порядка для изначально заданного узла (узлов).|
|1|В граф добавляются только узлы, имеющие косинусную близость **≥0.5** к любому из уже имеющихся|
|1|Реализована фильтрация по частям речи: узлами являются только существительные, только глаголы и т.п.|
|1|Рассчитана центральность узлов графа по метрикам, указанным в п.4.|
|1|Рассчитано значение метрик, указанных в п.5.|
|1|Граф разбит на сообщества, есть краткая интерпретация.|
|1|Граф визуализирован|
|1|Внешний вид графа задан в соответствии с п.7|
|5|**Бонусный балл.** Задание оформлено в виде веб-приложения, где пользователь может ввести любое слово в качестве начального узла и получить картинку с соответствующим графом и все статистики по нему (те, что указаны в задании + количество узлов и ребер).|



## Дедлайн

|Группа|Дедлайн|
|----|--------|
|1|7 июня 10:00|
|2|10 июня 10.00|
|3|7 июня 10:00|
|4|3 июня 10:00|
