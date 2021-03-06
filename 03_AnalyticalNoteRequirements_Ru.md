# Требования к Аналитической Записке

## Аннотация

Аналитическая Записка (АЗ) является основным рабочим и отчётным документом во время этапов НИОКР, Прототип и MVP в ходе цифрового проекта с использованием искусственного интеллекта (ПИИ). АЗ содержит описание контекста проблемы, бизнес- и математическую постановку задачи, анализ исходных данных, обсуждение предлагаемого решения и рекомендации по результатам проделанных работ. АЗ применяется для общей оценки подхода к решению и полученным результатам, без детального углубления в практическую реализацию алгоритмов и непосредственного разбора написанного кода.

АЗ в первую очередь используется в качестве обоснования для принятия управленческих решений по переходу между фазами проекта (например, от Прототипа к MVP), а также для упрощения общения по планированию и принятию решений в проектной команде в ходе реализации различных стадий проработки решения. Также этот документ используется для ретроспективного анализа реализации проекта, для общего описания комплексного многомодульного цифрового продукта с использованием ИИ и для ознакомления с контекстом задачи новых членов команды (в том числе при переводе продукта на сервисную поддержку). Таким образом, целевой аудиторией АЗ являются руководители проектов, ответственные за развитие продукта (product owner), технологические эксперты и специалисты, впервые подключаемые к разработке.

Следует заметить, что АЗ составляется и наполняется по мере ведения всех стадий проекта, что обеспечивает эффективную коммуникацию и возможность ретроспективы его эволюции. АЗ призвана фиксировать все значимые гипотезы и итерации решения, включая те, что не дали ожидаемых результатов. С точки зрения реализации, АЗ должна представлять собой часть сформированной вики-структуры, содержащей всю техническую проектную документацию. Выбор структуры остаётся за Исполнителем (рекомендуется функционал аналогичный проприетарному Confluence), с обязательным требованием возможности выгрузки информации в документы Word и Pdf. Для Газпромнефти, эта база знаний должна быть загружена в корпоративный Confluence.

Поскольку АЗ постепенно наполняется в течении нескольких месяцев, перечитывать её каждый раз целиком всем членам проектной команды – нецелесообразно. Поэтому рекомендуется выделять изменённые блоки текста цветом для быстрой навигации (более старые изменения перестают выделяться). Непосредственный момент добавления информации в АЗ следует согласовывать внутри проектной команды, но наиболее рациональным является внесение изменений перед регулярными статусными встречами. Также в ходе коммуникаций внутри проектной команды рекомендуется вести новостную ленту (например, в форме рассылок), с кратким резюме изменений в АЗ с указаниями на обновлённые разделы.

Наконец, следует упомянуть, что различные разделы АЗ заполняются разными членами проектной команды. Общую и бизнес-части обычно заполняет технический аналитик дата-саенса (TADS), информацию по данным вносит инженер данных, а исследование моделей – аналитик данных (дата-саентист). При этом, валидацию технической части осуществляет старший дата-саентист, а общую ответственность за редактуру и изложение текста несёт TADS. В случае отсутствия каких-либо ролей в проекте, заполнение их разделов берет на себя дата-саентист (подразумевается, что бизнес часть в этой ситуации ограничивается только самой общей информацией).

В заключение Аннотации, следует обратить внимание, что текущий документ содержит требования по последовательному заполнению различных разделов АЗ, в соответствии с принятым шаблоном, который охватывает минимально необходимую информацию по проекту. Впрочем, при написании АЗ авторы нисколько не ограничиваются в добавлении дополнительных разделов, требуемых для плавной подачи материала. Расположение и наименование предлагаемых разделов обусловлено общей логикой изложения, но в отдельных случаях может быть изменено, исходя из особенностей конкретной задачи. При перегруппировке разделов ключевым критерием должна являться последовательность и связанность текста, обеспечивающие наилучшее понимание материала читателем.

## 1. Постановка задачи

### 1.1 Общее описание проблемы

Общий контекст проблемы. Описание стандартного технологического и бизнес-процессов (например, “чтобы контролировать износ трубопроводов используют зонды-дефектоскопы; они состоят из 12-16 измерительных блоков, определяющих магнитные свойства трубы”). Ориентировочно, 1-2 страницы. Заполняется TADS после консультаций с техническими экспертами со стороны Заказчика.

### 1.2 Постановка бизнес-задачи

Описание ситуации по данной проблеме в ГК ГПН с приведением конкретных цифр и реалистичных оценок. Подробное описание “узкого” места и того, чего можно достичь при его устранении. Приведение бизнес-метрик и целевого результата в явном виде (например, снижение риска, сокращение сроков, уменьшение трудозатрат и т.п.). Указание (хотя бы качественная оценка) экономического эффекта и того, как он связан с техническим эффектом (например, расчёт экономии через сокращение трудозатрат). Ориентировочно, 1-2 страницы. Заполняется TADS после консультаций с техническими экспертами со стороны Заказчика.

### 1.3 Общая постановка математической задачи

#### 1.3.1 Гипотеза

Предположение как можно решить данную задачу с помощью методов ИИ. Обоснование применения именно ИИ, а не прочих методов. Предположение о наиболее подходящих алгоритмах и математических метриках. Общие допущения при решении задачи. Перечисление конкретных математических задач, решаемых в проекте (например, решение задачи классификации, задачи оптимизации и т.п.). Ориентировочно, 1-2 страницы. Заполняется TADS совместно с дата-саентистом.

#### 1.3.2 Формальная постановка

Математическая постановка вида:
[https://ru.wikipedia.org/wiki/%D0%97%D0%B0%D0%B4%D0%B0%D1%87%D0%B0_%D0%BA%D0%BB%D0%B0%D1%81%D1%81%D0%B8%D1%84%D0%B8%D0%BA%D0%B0%D1%86%D0%B8%D0%B8]
Ориентировочно, 1 страница. Заполняется дата-саентистом.

#### 1.3.3 Критерии приёмки сервиса и требования к точности моделей

Описание требований к точности работы математического ядра, сформулированные Заказчиком, а также общих требований приёмки результатов той стадии, к которой относится данная версия АЗ (АЗ постепенно дополняется в течение нескольких этапов реализации ПИИ). Указание общих критериев успешности проекта. Увязка метрик точности моделей с ожидаемым техническим и экономическим эффектами. Заполняется TADS совместно с дата-саентистом.

## 2. Результаты анализа исходных данных

### 2.1 Описание формата данных

Перечисление основных данных, используемых в задаче. Определение необходимости использования данных, составляющих коммерческую тайну с указанием пункта перечня КТ-040 “Конфиденциальная информация”. Описание их источников (местонахождение хранилища, информация о его структуре, процесс выгрузки и актуализации данных) и того как происходила сшивка датасета. Описание как данные приводились к распространённым “читаемым” форматам (особенно касается выгрузок со специализированных датчиков). Заполняется инженерном данных.

### 2.2 Анализ полноты и качества данных

Определение метрик качества и степени репрезентативности данных. Построение гистограмм основных релевантных характеристик (в том числе по классам/кластерам), откуда можно визуально понять масштабы разброса значений данных, и наглядно видны общие тренды (например, для анализа фотографий керна перечисление всевозможных комбинаций пород, встречающихся на изображениях). Расчёт основных статистических характеристик данных (минимальное и максимальное значения, дисперсия, математическое ожидание и т.п.). Построение корреляционных матриц по всем величинам (в случае большого количества величин целесообразно вынести эту информацию либо в приложение, либо в отдельный файл). Заполняется инженерном данных.

### 2.3 Анализ статистических выбросов и аномалий

Описание выбросов/битых данных/отсутствующих данных. Их графики распределения по классам/кластерам. Заполняется инженерном данных.

### 2.4 Описание итогового датасета

Обоснование исключения какой-либо информации из датасета. Описание процесса (скриптов) восстановления данных или их фильтрации. Перечисление формата и характеристик итогового датасета. Заполняется инженерном данных.

### 2.5 Экспертная оценка

Перечисление данных, значимых с точки зрения эксперта, с обоснованием этого мнения (например, это могут быть физические закономерности или утверждённые технологической инструкцией характеристики). При наличии, существующая методика анализа данных, которую рутинно использует эксперт с указанием метрик и ожидаемых после обработки результатов. Данный раздел может частично дублироваться с документом по данным. Заполняется инженерном данных после консультаций с техническими экспертами со стороны Заказчика.

## 3. Описание решения задачи

Все подразделы заполняются дата-саентистом.

### 3.1 Общая информация

#### 3.1.1 Логика решения

Описание общей логики решения (например, в виде блок-схемы). В первую очередь необходимо, если в рамках инициативы решается несколько параллельных подзадач.

#### 3.1.2 Общие метрики

Описание и обоснование применяемых математических метрик для тестирования. Следует указать иерархию метрик, т.е. каким образом метрики отдельных моделей трансформируются в общие метрики качества для всего цифрового продукта. Само базовое описание метрик нужно давать в конце АЗ в разделе 6.1, на который, по возможности, здесь делаются ссылки. Если в рамках инициативы не решаются параллельные подзадачи, то текущий раздел пропускается, а метрики описываются сразу в разделе 3.2.1.1.

### 3.2 Решение подзадачи №1

Если отдельных подзадач нет, то текущий раздел переименовывается в Решение задачи. В этом случае, далее в шаблоне под подзадачей надо понимать просто задачу.

#### 3.2.1 Стратегия решения подзадачи

Детализированное описание логики решения подзадачи №1.

##### 3.2.1.1 Постановка математической подзадачи и выбор метрик

Математическая формулировка подзадачи №1. Граничные условия подзадачи. Описание выбранных метрик для подзадачи и аргументация их применения. Базовое описание метрик нужно давать в конце АЗ в разделе 6.1, на который, по возможности, здесь делаются ссылки.

##### 3.2.1.2 Подготовка данных

Описание разбиения итогового датасета на обучающую, валидационную и тестовую выборки. При необходимости, описание процесса балансировки данных, если они представлены в датасете неравномерно (например, имеется 100 скважин с измерениями в течении 10 месяцев и 10 скважин с измерениями в течении 100 месяцев). Также указываются прочие преобразования данных, выполняемые в рамках описываемой подзадачи.

##### 3.2.1.3 Описание исследуемых моделей

Перечисление всех моделей, используемых в рамках исследования и обоснование их выбора, в том числе подкреплённое ссылками на научно-техническую литературу, предыдущие проекты и лучшие практики (можно рассматривать данный раздел как небольшой литературный обзор). Базовое описание моделей нужно давать в конце АЗ в разделе 6.1, на который, по возможности, здесь делаются ссылки.

##### 3.2.1.4 Исследования математических моделей

Описание всех проведённых экспериментов с моделями из раздела 3.2.1.3. Указываются условия экспериментов, гиперпараметры и настройки моделей, полученные значения метрик. Каждый эксперимент ссылается на конкретный Jupiter Notebook или аналогичную вычислительную среду, где проводилось исследование для возможности независимого воспроизведения результатов. Сами результаты для наглядности приводятся в виде графиков и таблиц.

Описание дополнительных критериев выбора наилучшей модели, помимо удовлетворения заданным метрикам (необходимо, когда несколько моделей показывают схожие результаты). Выбор наилучшей  модели с учётом метрик и дополнительных критериев.

Важно подчеркнуть, что это самый главный пункт АЗ. В нём должна содержаться исчерпывающая информация о протестированных моделях, что должно подтверждаться сравнительными графиками и таблицами. При необходимости, данный раздел может содержать дополнительные подразделы для более структурированного изложения информации.

##### 3.2.1.5 Выводы по решению подзадачи №1

Результаты итоговой модели на тестовой выборке. Исследование границ её применимости. Общие выводы о качестве лучшей модели.

### 3.3 Решение подзадачи №2

Содержание раздела полностью эквивалентно 3.2 (при наличии подзадачи №2).

## 4. Предварительное видение цифрового продукта

Краткое описание дальнейшего применения разработанных моделей (внутри каких сервисов они будут функционировать, где в целевом виде будет развернуто решение, какие ожидаются сценарии работы и т.п.). При наличии приложить скриншоты интерфейса будущего сервиса или другую поясняющую инфографику. Ориентировочно, 1 страница. Заполняет TADS совместно с дата-саентистсом. 

Следует заметить, что детальные функциональные и технические требования к целевому виду решения прописываются не в АЗ, а отдельно в техническом задании на доработку MVP. В текущем разделе достаточно ссылки на указанную документацию.

## 5. Заключение

### 5.1 Выводы

Резюме выполненных работ. Явно прописанная рекомендация о переходе на следующий этап проекта, открытии нового тематически связанного НИОКР или заключение о нецелесообразности дальнейших работ с обоснованием причин. Ориентировочно, 1-2 страницы. Заполняет TADS совместно с дата-саентистсом.

### 5.2 Рекомендации

#### 5.2.1 Рекомендации к данным

Конкретные рекомендации по улучшению полноты и качества данных (например, накопление большего датасета, дооборудование измерительных систем дополнительными датчиками, изменение дискретности записи данных и т.п.). Ориентировочно, 1-2 страницы. Заполняет дата-саентист совместно с инженером данных.

#### 5.2.2 Рекомендации к решению задачи

Конкретные рекомендации по применению алгоритмов ИИ (например, предложение использовать другой тип алгоритмов или другую логику оценки точности решения). Предположения о новых задачах, которые могли возникнуть в ходе реализации инициативы.
Ориентировочно, 1-2 страницы. Заполняет TADS совместно с дата-саентистсом.

## 6. Приложение

### 6.1 Глоссарий

Справочный раздел, в котором даётся список аббревиатур, перечисляются основные понятия, и приводится базовая информация о метриках и алгоритмах. Описывается общий контекст их применения, без привязки к конкретной задаче. Возможны ссылки на внешние источники. Заполняет TADS совместно с дата-саентистсом.

### 6.2 Дополнительные материалы

Любые материалы, исключенные из основного текста АЗ (чтобы не перегружать его), но которые нецелесообразно удалять вовсе (например, дополнительные графики и таблицы). Заполняет дата-саентист и/или инженер данных.

### 6.3 История подходов к решению задачи до актуальной версии

Тезисное описание предыдущих подходов к решению или результатов работ, представляющие историческую ценность. Заполняет TADS совместно с дата-саентистсом.
