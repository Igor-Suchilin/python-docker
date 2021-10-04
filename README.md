# python-docker
мтоговый проект курса "Машинное обучение в бизнесе"

Стек:

ML: sklearn, pandas, numpy API: flask Данные: с kaggle

Задача: предсказать по анализу крови диабет. Бинарная классификация

Используемые признаки:

Glucose (int)
BloodPressure (int)
Insulin (int)
Age (int)
Преобразования признаков: StandardScaler

Модель: logreg

Клонируем репозиторий и создаем образ
$ git clone https://github.com/Igor-Suchilin/python-docker.git
$ cd python-docker
$ docker build -t python-docker .
Запускаем контейнер
Здесь Вам нужно создать каталог локально и сохранить туда предобученную модель (<your_local_path_to_pretrained_models> нужно заменить на полный путь к этому каталогу)

$ docker run -d -p 8180:8180 -p 8181:8181 -v <your_local_path_to_pretrained_models>:/app/app/models python-docker
Переходим на localhost:8181
