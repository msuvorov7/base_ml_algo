# base_ml_algo
implementation of basic ML algorithms 

## knn:
- KNN - базовый класс, основанный на подсчёте матрицы расстояний
- KNNClassifier - алгоритм классификации
- KNNRegressor - алгоритм регресии
- BatchedKNNClassifier - модификация классификатора для подстёта по батчам
- BatchedKNNRegressor - модификация регрессора для подсчёта по батчам

Реализация содержит:
- евклидову и косинусную метрику
- поддержку поиска методами kd_tree, ball_tree, brute из sklearn
- вычисление классов путём госования или взвешивания (регрессия Надарая-Ватсона)

## linear
- LinReg - аналитическое нахождение весов
- GradLinRed - нахождение весов градиентным спуском по всей выборке
- SGDLinReg - нахождение весов градиентным спуском по батчам
- LogReg - логистическая регрессия для бинарной классификации на градиентном спуске
- SGDLogReg - логистическая регрессия для бинарной классификации по батчам
- SoftmaxRegression - логистическая регрессия для многоклассовой классификации
- SGDSoftmaxReg - логистическая регрессия для многоклассовой классификации по батчам
- ElasticLogReg - логистическая регрессия для бинарной классификации с регуляризациями Ridge и Lasso
- ElasticSoftmaxReg логистическая регрессия для многоклассовой классификации с регуляризациями Ridge и Lasso

