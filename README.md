# Команда
Сокирка А.В.

Программная инженерия. Итоговый проект (PJ)
Анализатор комментариев — это приложение, которое позволяет пользователю получить комментарии к видео, размещенному на YouTube, а также определить эмоциональную окраску этих комментариев и визуализировать результаты в виде диаграмм.

Цель проекта: разработать Web приложение машинного обучения и развернуть его в облаке. В проекте используется модель blanchefort/rubert-base-cased-sentiment.

Итоговый проект (PJ) доступен по ссылке на Hugging Face Spaces.

Основные функции

1. Приложение позволяет пользователю получить комментарии к видео из YouTube.
2. Приложение использует модель «blanchefort/rubert-base-cased-sentiment», основанную на RUbert, для определения эмоциональной окраски каждого комментария. Модель анализирует текст комментария и выдает оценку позитивной, негативной или нейтральной эмоциональной окраски.
3. После анализа эмоциональной окраски комментариев, приложение генерирует две диаграммы для наглядного представления результатов.
4. Диаграмма эмоциональной окраски. Первая диаграмма отображает процентное соотношение комментариев с различными эмоциональными окрасками, такими как позитивная, негативная или нейтральная. Это помогает пользователю лучше понять общую тональность комментариев и оценить эмоциональную реакцию зрителей на видео.
4. Диаграмма активности. Вторая диаграмма показывает, как распределяются комментарии по часам и датам. Это помогает пользователю понять, в какое время и в какие дни была наибольшая активность комментирования. Эта информация может быть полезной для определения популярности видео и оптимизации контента в будущем.

Технологии

1. Приложение разработано на языке Python, с использованием библилотеки Streamlit.
2. Приложение использует модель [«blanchefort/rubert-base-cased-sentiment»](https://huggingface.co/blanchefort/rubert-base-cased-sentiment), основанную на RUbert, для определения эмоциональной окраски комментариев.
3. Приложение использует YouTube Data API v3 для загрузки комментариев к видео
4. Для визуализации результатов приложение использует библиотеки Matplotlib и Plotly.
5. Прриложение развернуто на платформе Hugging Face Spaces.

Установка и использование

1. Склонируйте репозиторий приложения с GitHub: [ссылка](https://github.com/sultanovemil/PI_2024).
2. Установите необходимые зависимости, выполнив команду pip install -r requirements.txt.
3. Запустите приложение, выполнив команду streamlit run project.pyв корневой папке проекта.
4. Откройте веб-браузер и перейдите по адресу http://localhost:8501.
4. Введите ссылку на видео YouTube в соответствующее поле и нажмите кнопку "Загрузить".

План улучшения качества кода

1. Вынести импорты в начало скрипта для лучшей читаемости.
2. Создать отдельные функции для разделения логики. Функцию для получения комментариев из YouTube API, функцию для анализа тональности комментариев, функцию для вывода диаграмм.
3. Добавить комментарии к каждому блоку кода для пояснения его функциональности.
4. Использовать блоки try/except для обработки возможных ошибок при запросах к API или при обработке данных.
5. Использовать session_state чтобы избежать повторной загрузки модели и повторных запросов при каждом нажатии кнопки.
6. Добавить кэширование пайплайна HuggingFace с помощью streamlit.cache_resource для ускоренного взаимодействия с моделью между несколькими клиентами.
