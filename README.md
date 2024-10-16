# Документация к приложению обнаружения дефектов на ноутбуках

## Введение

Команда Chipsoni:
- Telegram: @miraclle_24 M/L engineer
- Telegram: @zxcdenjir M/L engineer
- Telegram: @dhsjdhydue full-stack, TeamLead
- Telegram: @Gaz228 backend developer
- Telegram: @d_sh_qw frontend developer

Данное приложение предназначено для обнаружения дефектов на ноутбуках по фотографиям. Оно использует модель YOLO (You Only Look Once) для детекции неисправностей. Приложение позволяет загружать изображения, вводить серийный номер ноутбука и генерировать отчет в формате CSV.

## Требования

- Python 3.8+
- Streamlit 1.10+
- OpenCV 4.5+
- Ultralytics 8.0+
- Pillow 9.0+
- Pandas 1.3+

## Установка

1. Установите Python и необходимые библиотеки.
   `pip install streamlit ultralytics opencv-python-headless pillow pandas`
   `pip install ultralytics --upgrade`
2. Установите папку StreamLit с моделью и сайтом.
3. Откройте терминал и перейдите в эту папку.
4. Запустите приложение с помощью команды `streamlit run app.py`.

## Использование

1. Введите серийный номер ноутбука в поле "Введите серийный номер и нажмите enter:".
2. Загрузите одно или несколько изображений ноутбука в формате JPG, JPEG или PNG.
3. Нажмите кнопку "Начать детекцию".
4. Приложение обработает изображения и покажет результаты детекции.
5. Просмотрите отчет по детекциям.
6. Нажмите кнопку "Скачать отчет", чтобы скачать отчет в формате CSV.

## Модель YOLO

Модель YOLO используется для детекции неисправностей на ноутбуках. Она обучена на датасете изображений ноутбуков с разными неисправностями. Модель может детектировать следующие классы:

- `broken_button`: сломанная кнопка
- `broken_pixel`: сломанный пиксель
- `chip`: скол
- `disassembled_laptop`: разобранный ноутбук
- `lock`: замок
- `missing_button`: отсутствующая кнопка
- `missing_screw`: отсутствующий винт
- `scratch`: царапина

## Функциональность приложения

Приложение состоит из следующих функций:

- `process_image`: обрабатывает изображение и детектирует неисправности.
- `main`: основная функция приложения, которая управляет потоком приложения.

## Недостатки и перспективы развития

- Приложение не может детектировать все возможные неисправности на ноутбуках.
- Модель YOLO требует дальнейшего обучения и улучшения.
- Приложение можно расширить для поддержки других типов изображений и моделей детекции.
