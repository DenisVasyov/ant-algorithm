# ant-algorithm

Данный репозиторий содержит реализацию простого муравьиного алгоритма, предназначенного для решения задачи коммивояжера. Реализация представлена в виде тетрадки `.ipynb`

Функция поиска наилучшего маршрута `best_path()` принимает на вход матрицу, содержащую длины рёбер между вершинами графа (городами). Константные параметры a и b, использующиеся при выборе следующей вершины, подобраны "грубой силой" простым перебором. Алгоритм проходит по всем муравьям (количество которы кратно количеству вершин) и выбирает для каждого путь в соответствии с уровнями феромона (изначально инициализированными случайным образом, а в дальнейшем изменяемыми в соответствии с путями муравьёв) и в соответствии с длиной ребра. После прохождения всему муравьями матрица уровня феромонов обновляется (также присутствует эффект высыхания) и сохраняется наилучшее решение. Алгоритм проходит в 100 эпох (одна эпоха – все муравьи один раз прошли путь). Для подсчёта стоимости решения (длины всех пройденных рёбер), создания и первоначальной расстановки муравьёв, поиска следующей вершины и формирования феромонов написаны специальные функции.
