
# Расположение проектов

| № | Название | Расположение | Статус|
|---|---|---|---|
|13|Промышленность| [industry](https://github.com/adelinagabby/data-science/tree/main/industry)|Завершен | 
|12|Определение возраста покупателей| [determining_the_age_of_buyers](https://github.com/adelinagabby/data-science/tree/main/determining_the_age_of_buyers)| Завершен |
|11|Проект для «Викишоп»| [project_for_Wikishop](https://github.com/adelinagabby/data-science/tree/main/project_for_Wikishop)| Завершен |
|10|Прогнозирование заказов такси|[forecasting_taxi_orders](https://github.com/adelinagabby/data-science/tree/main/forecasting_taxi_orders) | Завершен |
|9|Определение стоимости автомобилей| [determining_the_cost_of_cars](https://github.com/adelinagabby/data-science/tree/main/determining_the_cost_of_cars)| Завершен |
|8|Защита персональных данных клиентов| [protection_of_personal_data_of_clients](https://github.com/adelinagabby/data-science/tree/main/protection_of_personal_data_of_clients)| Завершен |
|7|Восстановление золота из руды| [recovery_of_gold_from_ore](https://github.com/adelinagabby/data-science/tree/main/recovery_of_gold_from_ore)| Завершен |
|6|Выбор локации для скважины| [choosing_the_location_for_the_well](https://github.com/adelinagabby/data-science/tree/main/choosing_the_location_for_the_well)| Завершен |
|5|Отток клиентов| [customer_outflow](https://github.com/adelinagabby/data-science/tree/main/customer_outflow)| Завершен |
|4|Рекомендация тарифов| [recommendation_of_tariffs](https://github.com/adelinagabby/data-science/tree/main/recommendation_of_tariffs)| Завершен |
|3|Исследование продаж игр интернет-магазина «Стримчик»| [online_store_game_sales_research](https://github.com/adelinagabby/data-science/tree/main/online_store_game_sales_research)| Завершен |
|2|Исследование объявлений о продаже квартир| [research_of_ads_for_the_sale_of_apartments](https://github.com/adelinagabby/data-science/tree/main/research_of_ads_for_the_sale_of_apartments)| Завершен |
|1|Исследование надежности заемщиков| [investigation_of_the_reliability_of_borrowers](https://github.com/adelinagabby/data-science/tree/main/investigation_of_the_reliability_of_borrowers)| Завершен |







# Описание проектов
# 13. Промышленность 
Расположено в папке industry
## Описание проекта
Чтобы оптимизировать производственные расходы, металлургический комбинат ООО «Так закаляем сталь» решил уменьшить потребление электроэнергии на этапе обработки стали. 

## Цель проекта
Требуется построить модель, которая предскажет температуру стали.

## Статус проекта
Завершен

## Вывод
Модель LGBMRegressor(max_depth=5, n_estimators=60, random_state=240423) показала хороший результат 6.29. Анализ важности факторов показал, что наиболее значительными признаками в данной модели являются начальная температура, время нагрева и подача газа.

# 12. Определение возраста покупателей
Расположено в папке determining_the_age_of_buyers
## Описание проекта

Сетевой супермаркет «Хлеб-Соль» внедряет систему компьютерного зрения для обработки фотографий покупателей. Фотофиксация в прикассовой зоне поможет определять возраст клиентов, чтобы:

Анализировать покупки и предлагать товары, которые могут заинтересовать покупателей этой возрастной группы;
Контролировать добросовестность кассиров при продаже алкоголя.

## Цель проекта

Постройть модель, которая по фотографии определит приблизительный возраст человека. В нашем распоряжении набор фотографий людей с указанием возраста.

## Статус проекта
Завершен

## Вывод
Для решения поставленой задачи была построена модель, которая по фотографии определяет приблизительный возраст человека. Модель решает задачу регресии, так как требуется предсказать число — количество лет. Работаем с сетью ResNet50, предобученной на датасете ImageNet. Добавили сверточный слой и слой с 10 нейронами с активацией relu. На последнем слое всего один нейрон, который возвращает число-предсказание с функцией активации relu (положительные прогнозы сети функция relu не меняет, а все отрицательные — приводит к нулю, чисел меньше 0 быть не может). Функция потерь MSE и метрикой MAE, learning rate = 0.0001. Значения MAE на тестовой выборке показало отличный результат равный 6.59.

# 11. Проект для «Викишоп»
Расположено в папке project_for_Wikishop

## Описание проекта

Интернет-магазин «Викишоп» запускает новый сервис. Теперь пользователи могут редактировать и дополнять описания товаров, как в вики-сообществах. То есть клиенты предлагают свои правки и комментируют изменения других. Магазину нужен инструмент, который будет искать токсичные комментарии и отправлять их на модерацию.

## Цель проекта

Требуется обучить модель классифицировать комментарии на позитивные и негативные.
Построить модель со значением метрики качества F1 не меньше 0.75.

## Статус проекта
Завершен

## Вывод
Были проанализированы модели с использованием алгоритма дерева решений, с использованием алгоритма случайного леса и линейной регрессии в связке GridSearchCV + pipeline. Наилучший результат f1 показала модель LogisticRegression(C=13, class_weight='balanced', random_state=12345).
Модель LogisticRegression(C=13, class_weight='balanced', random_state=12345 показала на тестовых данных результат f1 = 0.76.

# 10. Прогнозирование заказов такси
Расположено в папке forecasting_taxi_orders
## Описание проекта

Компания «Чётенькое такси» собрала исторические данные о заказах такси в аэропортах. Компания хочет привлекать больше водителей в период пиковой нагрузки.

## Цель проекта
Требуется построить модель для прогнозирования количество заказов такси на следующий час. Значение метрики RMSE на тестовой выборке должно быть не больше 48.

## Статус проекта
Завершен

## Вывод
Наилучший результат rmse показала модель LGBMRegressor(max_depth=7, n_estimators=60).
Был построен график за три дня фактических и предсказанных данных. Модель показала себя хорошо, значение метрики RMSE на тестовой выборке меньше 48, соответственно, модель успешно прошла тестирование.

# 9. Определение стоимости автомобилей
Расположено в папке determining_the_cost_of_cars
## Описание проекта

Сервис по продаже автомобилей с пробегом «Не бит, не крашен» разрабатывает приложение, чтобы привлечь новых клиентов. В нём можно будет узнать рыночную стоимость своего автомобиля. 

## Цель проекта

Необходимо построить модель, которая умеет определять рыночную стоимость автомобиля. В распоряжении данные о технических характеристиках, комплектации и ценах других автомобилей.

Критерии, которые важны заказчику:
* качество предсказания;
* время обучения модели;
* время предсказания модели.

## Статус проекта
Завершен

## Вывод
Лучший результат по времени обучения и предсказания показала модель LinearRegression, на втором месте DecisionTreeRegressor(max_depth=10, random_state=12345), на третьем LGBMRegressor, однако наилучшее значение по качеству показала модель LGBMRegressor. Следовательно, основываясь на предпочтениях клиента, можно сделать вывод, что подходят две модели DecisionTreeRegressor(max_depth=10, random_state=12345) и LGBMRegressor. Но так как качество стоит на первом месте, выберем модель LGBMRegressor. Выбранная модель показала хороший результат при тестировании.

# 8. Защита персональных данных клиентов
Расположено в папке protection_of_personal_data_of_clients
## Описание проекта 

Данные клиентов предоставлены страховой компанией «Хоть потоп». Нужно защитить данные клиентов.

## Цель проекта 

Требуется разработать такой метод преобразования данных, чтобы по ним было сложно восстановить персональную информацию.
Нужно защитить данные, чтобы при преобразовании качество моделей машинного обучения не ухудшилось. Подбирать наилучшую модель не требуется.

## Статус проекта
Завершен

## Вывод
Для защиты данных предложен алгоритм преобразования. 
Был запрограммирован алгоритм преобразования с использванием матричных операций.
Проверено, что качество линейной регрессии из sklearn не отличается до и после преобразования, с использованием метрики r2.

# 7. Восстановление золота из руды
Расположено в папке recovery_of_gold_from_ore

## Описание проекта
Компания «Цифры» разрабатывает решения для эффективной работы промышленных предприятий.

## Цель проекта
Требуется подготовить прототип модели машинного обучения, которая должна предсказать коэффициент восстановления золота из золотосодержащей руды. В нашем распоряжении данные с параметрами добычи и очистки. Модель поможет оптимизировать производство, чтобы не запускать предприятие с убыточными характеристиками.

## Статус проекта
Завершен

## Вывод
Написана функция для вычисления итоговой sMAPE.
Обучены модели с использованием логической регрессии, дерева решений и случайного леса и оценено их качество кросс-валидацией. Наилучшие результаты для признака 'rougher.output.recovery' показала модель RandomForestRegressor(n_estimators=30, max_depth=5, random_state=12345), а для признака 'final.output.recovery' - RandomForestRegressor(n_estimators=20, max_depth=2, random_state=12345).
Проверены наилучшие модели на тестовой выборке. sMAPE модели RandomForestRegressor(n_estimators=30, max_depth=5, random_state=12345) и модели RandomForestRegressor(n_estimators=20, max_depth=2, random_state=12345) показали результат лучше, чем константная модель. Итоговое sMAPE 8.9.

# 6. Выбор локации для скважины
Расположено в папке choosing_the_location_for_the_well

## Описание проекта

Предоставлены данные добывающей компанией «ГлавРосГосНефть» о пробах нефти в трёх регионах: в каждом 10 000 месторождений, где измерили качество нефти и объём её запасов.

## Цель проекта

Требуется построить модель машинного обучения, которая поможет определить регион, где добыча принесёт наибольшую прибыль.
Необходимо проанализировать возможную прибыль и риски.

## Статус проекта
Завершен

## Вывод
Для обучения модели подходит только линейная регрессия (остальные — недостаточно предсказуемые).
Посчитан средний запас предсказанного сырья и RMSE моделей.
Была написана функцим для расчёта прибыли по выбранным скважинам и предсказаниям модели.
Посчитаны риски и прибыль для каждого региона.

# 5. Отток клиентов
Расположено в папке customer_outflow

## Описание проекта

Из «Бета-Банка» стали уходить клиенты. Каждый месяц. Немного, но заметно. Банковские маркетологи посчитали: сохранять текущих клиентов дешевле, чем привлекать новых.

Источник данных: https://www.kaggle.com/barelydedicated/bank-customer-churn-modeling

## Цель проекта

Нужно спрогнозировать, уйдёт клиент из банка в ближайшее время или нет. Предоставлены исторические данные о поведении клиентов и расторжении договоров с банком.
Построить модель с предельно большим значением F1-меры. 

## Статус проекта
Завершен

## Вывод
Были построенны модели с использованием дерева решений, случайного леса и логической регрессии.
Самый лучший результат показала модель случайного леса с параметрами depth 8, est 10, успешно протестирована, F1-мера достигла значения 0.597, AUC-ROC - значение 0.84.

# 4. Рекомендация тарифов
Расположено в папке recommendation_of_tariffs

## Описание проекта
Оператор мобильной связи «Мегалайн» выяснил: многие клиенты пользуются архивными тарифами. Они хотят построить систему, способную проанализировать поведение клиентов и предложить пользователям новый тариф: «Смарт» или «Ультра».

В нашем распоряжении данные о поведении клиентов, которые уже перешли на эти тарифы.

## Цель проекта

Нужно построить модель с максимально большим значением accuracy для задачи классификации, которая выберет подходящий тариф.

## Статус проекта
Завершен

## Вывод
Модель случайный лес с параметрами глубина дерева depth 8, est 50 показала хороший результат на тестовой выборке.
Была проведена проверка модели на адекватность.
Сравнила модель полученную с моделью DummyClassifier со стратегией most_frequent.
Модель DummyClassifier со стратегией most_frequent показала качество хуже, чем модель случайный лес с параметрами глубина дерева depth 8, est 50.

# 3. Исследование продаж игр интернет-магазина «Стримчик»
Расположено в папке online_store_game_sales_research

## Описание проекта

Интернет-магазине «Стримчик» продаёт по всему миру компьютерные игры. Из открытых источников доступны исторические данные о продажах игр, оценки пользователей и экспертов, жанры и платформы

В наборе данных попадается аббревиатура ESRB (Entertainment Software Rating Board) — это ассоциация, определяющая возрастной рейтинг компьютерных игр. ESRB оценивает игровой контент и присваивает ему подходящую возрастную категорию, например, «Для взрослых», «Для детей младшего возраста» или «Для подростков».

## Цель проекта

Требуется выявить определяющие успешность игры закономерности. Это позволит сделать ставку на потенциально популярный продукт и спланировать рекламные кампании.

## Статус проекта
Завершен

## Вывод
По результатам данных на 2016 год за последние 3 года можно сделать вывод, что в 2017 году следует обратить внимание на платформы PS4, PS3, 3DS, XOne, так как они являются потенциально прибыльными, а также на жанры игр Action, Shooter, Role-Playing, так как они являются популярными во всех регионах.

# 2. Исследование объявлений о продаже квартир
Расположено в папке research_of_ads_for_the_sale_of_apartments

Входные данные — архив объявлений о продаже квартир в Санкт-Петербурге и соседних населённых пунктов за несколько лет. 

Требуется выполнить предобработку данных и изучить их, чтобы найти интересные особенности и зависимости, которые существуют на рынке недвижимости.

## Статус проекта
Завершен

## Вывод
Были изучены и преобработанны данные архива объявлений о продаже квартир в Санкт-Петербурге и соседних населённых пунктов за несколько лет и проведено исследование.

# 1. Исследование надежности заемщиков
Расположено в папке investigation_of_the_reliability_of_borrowers

Необходимо определить, влияет ли семейное положение и количество детей клиента на факт погашения кредита в срок. Входные данные от кредитного отдела банка — статистика о платёжеспособности клиентов.

## Статус проекта
Завершен

## Вывод

По результатам проведенного исследования можно сделать следующий вывод:

1) Люди, у которых 5 детей всегда возвращают кредиты в срок.

   Заемщики, у которых нет детей или 3 ребенка, возвращают в срок чаще, чем заемщики, у которых 1 или 2 ребенка.

   Хуже всего отдают кредит люди, у которых 4 ребенка;

2) Вдовцы или люди в разводе отдают деньги в срок чаще, чем женатые.

   Чаще всего задерживают с возвратом заемщики с семейным положением 'не женат / не замужем' и 'гражданский брак';

3) Реже всего задерживают с возвратом люди с уровнем дохода категории D (30001–50000) и B (200001–1000000).

   Люди с уровнем дохода E (0–30000) и A (1000001 и выше) реже всего берут кредит, однако доли должников данной категории большие.

   Заемщики с уровнем дохода C (50001–200000) чаще всего берут кредиты. Тем не менее доля должников данной категории большая;

4) Чаще всего кредиты берут на операции с недвижимостью, тем не менее заемщики с данной целью чаще вызвращают деньги в срок;

   Чаще всего задерживают с возвратом кредита в срок заемщики с целью получения образования и осуществления операции с автомобилем.




