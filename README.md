# Crowdfunding Platform

## Опис
Crowdfunding Platform - це веб-додаток для краудсорсингу, який дозволяє користувачам створювати проєкти, збирати фінансування та залучати учасників для виконання завдань.

## Структура проєкту
Проєкт поділений на кілька шарів для покращення читабельності та підтримуваності коду:

- **Domain**: Основна бізнес-логіка та правила.
- **Application**: Інтерфейси, юзкейси та реалізації для роботи з даними.
- **Infrastructure**: Реалізація деталей інфраструктури, таких як API та база даних.
- **Presentation**: Веб-інтерфейс, реалізований з використанням Django та HTML/CSS/JavaScript.

## Встановлення
1. Клонуйте репозиторій:
    ```bash
    git clone <URL репозитарію>
    ```
2. Перейдіть у каталог проєкту:
    ```bash
    cd crowdfunding_platform
    ```
3. Створіть віртуальне середовище та активуйте його:
    ```bash
    python -m venv env
    source env/bin/activate  # для Linux/Mac
    env\Scripts\activate  # для Windows
    ```
4. Встановіть залежності:
    ```bash
    pip install -r requirements.txt
    ```

## Запуск
Для запуску проєкту виконайте команду:
```bash
python manage.py runserver
```

## Структура каталогів
```plaintext
.
├── crowdfunding_platform/
│
├── crowdfunding/
│   ├── domain/
│   │   ├── entities/
│   │   │   └── project.py
│   │   ├── services/
│   │   │   └── project_service.py
│   │   └── repositories/
│   │       └── project_repository.py
│   ├── application/
│   │   └── usecases/
│   │       └── create_project.py
│   ├── infrastructure/
│   │   ├── models.py
│   │   ├── views.py
│   │   ├── urls.py
│   │   └── serializers.py
│   └── presentation/
│       ├── templates/
│       │   └── crowdfunding/
│       │       ├── index.html
│       │       └── project_list.html
│       ├── static/
│       │   └── crowdfunding/
│       │       └── style.css
│       └── views/
│           └── project_view.py
│
└── manage.py
```

## Опис компонентів
### Domain
- **Project**: Клас сутності проєкту.

### Application
- **CreateProjectUseCase**: Юзкейс для створення проєкту.

### Infrastructure
- **ProjectModel**: Модель даних проєкту.
- **ProjectView**: Вигляд для відображення проєктів.
- **ProjectURLs**: URL-адреси для проєктів.
- **ProjectSerializers**: Сереалізатори для проєктів.

### Presentation
- **index.html**: Шаблон головної сторінки.
- **project_list.html**: Шаблон списку проєктів.
- **style.css**: Стилі для веб-інтерфейсу.

## Ліцензія
Цей проєкт ліцензовано за ліцензією MIT. Для отримання додаткової інформації перегляньте файл LICENSE.
