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
- ElasticSoftmaxReg - логистическая регрессия для многоклассовой классификации с регуляризациями Ridge и Lasso

## tree
- ClassificationDecisionTree - алгоритм классификации на основе дерева решений
- RegressionDecisionTree - алгоритм регрессии на основе дерева решений

Реализация содержит:
- энтропийный критерий
- критерй Джини
- MSE критерий

## svm
- LinearSVC - классический линейный классификатор методом опорных векторов
- SVC - [классификатор](https://habr.com/ru/post/544282/) с использованием ядер:
  - Linear - линейное ядро
  - RBF - радиальное базисное ядро

## bagging
- Bagger - базовый класс, осуществляющий выборку без возвращений из строк и столбцов матрицы
- BaggingClassifier - поддерживает классификацию для дерева решений и ближайшего соседа
- BaggingRegressor - поддерживает регрессию для дерева решений и ближайшего соседа

Данные алгоритмы выбраны из-за своей неустойчивости, так как только с такими концепция бэггинга будет работать хорошо

## boosting
В качестве первого алгоритма выбрана линейная регрессия

- Booster - базовый класс с прототипами функций
- BoosterClassifier - градиентный бустинг для бинарной классификации, использующий производную logloss
- BoosterRegressor - градиентный бустинг для задачи регрессии, использующий производную mse loss
