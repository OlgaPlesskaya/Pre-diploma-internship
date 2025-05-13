# 💻Преддипломная практика

Перед работой необходимо установить следующие зависимости:

```
pip install Django transformers torch safetensors wordcloud openpyxl requests matplotlib pandas
```

## 📚 Ноутбуки

| Описание | Ссылка |
|---------|--------|
| Обучение модели BERT | [https://colab.research.google.com/drive/1YuaJge4fmBhaGICZcYYcmAzacn9_B7ep?usp=sharing](https://colab.research.google.com/drive/1YuaJge4fmBhaGICZcYYcmAzacn9_B7ep?usp=sharing) |
| Инференс | [https://colab.research.google.com/gist/OlgaPlesskaya/79a136762ed41486ea8ee184f3141d1e/-ipynb.ipynb#scrollTo=prrDe9ppMGdc](https://colab.research.google.com/gist/OlgaPlesskaya/79a136762ed41486ea8ee184f3141d1e/-ipynb.ipynb#scrollTo=prrDe9ppMGdc) |
| Предобработка (самая 1) | [[Open in Colab](https://colab.research.google.com/drive/1YuaJge4fmBhaGICZcYYcmAzacn9_B7ep )](https://colab.research.google.com/drive/1z6RiDQtVZmy60ko9eWpdVk3phRFZ7BR9?usp=sharing#scrollTo=aQOM5QdQniWT) |

## 📌 Описание проекта

Сервис предобработки текстовых сообщений на базе **Django**, предназначенный для загрузки CSV-файлов с текстами, автоматической классификации текстов с помощью модели BERT и отображения результатов в удобном виде.

---

## 🔧 Технологии

- **Python 3**
- **Django**
- **PyTorch + Transformers (HuggingFace)** — для работы с моделью BERT
- **BERT** — используется предобученная модель для классификации текстов
- **Pandas** — работа с данными
- **Matplotlib / WordCloud** — визуализация данных
- **HTML/CSS** — шаблоны Django


## 📥 Как использовать

1. Перейдите на главную страницу.
2. Загрузите CSV-файл с текстами (без заголовков).
3. После обработки:
   - Просмотрите результаты онлайн
   - Скачайте обработанный CSV
   - Ознакомьтесь с графиками и облаком слов

---

## 📦 Требования к данным

- CSV-файл должен содержать **одну колонку с текстами**.
- Формат файла: UTF-8 без заголовка.
- Пример содержимого:
  ```
  Это первый текст для анализа
  Это второй текст
  ```

---

## 📂 Дополнительные файлы

- `Классификации.xlsx` — файл с соответствием ID и названиями категорий
- `best_model/` — папка с моделью BERT (`model.safetensors`, `config.json` и др.)

Убедитесь, что эти файлы находятся в нужной директории:
```
polls/
├── best_model/
│   ├── config.json
│   ├── vocab.txt
│   ├── model.safetensors
│   └── ...
├── Классификации.xlsx
└── ...
```

---

## 📈 Возможности расширения

- Дообучение модели
- Оптимизация времени обработки файла
- Добавление аутентификации и истории загрузок
- Поддержка нескольких моделей
- Отправка результата в тг
