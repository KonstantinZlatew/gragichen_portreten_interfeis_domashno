# React Course Project - Графичен Портретен Интерфейс

Проект за курсова работа с React, който включва 3 страници с функционалност за вход, списък и детайли.

## Функционалности

- **Login страница** - Форма за вход с валидация на полетата (email и password)
- **List страница** - Списък с постове, заредени от JSONPlaceholder API
- **Detail страница** - Детайлен изглед на избран пост
- **Диалози за потвърждение** - За операции delete и logout

## Технологии

- React 19
- Vite
- React Router v7
- Tailwind CSS
- JSONPlaceholder API

## Инсталация

1. Клонирайте репозитория:
```bash
git clone <repository-url>
cd gragichen_portreten_interfeis_domashno
```

2. Инсталирайте зависимостите:
```bash
npm install
```

## Стартиране

За да стартирате проекта в development режим:

```bash
npm run dev
```

Проектът ще се отвори на `http://localhost:5173`

## Build за production

За да създадете production build:

```bash
npm run build
```

## Структура на проекта

```
src/
├── pages/
│   ├── Login.jsx          # Login страница с форма и валидация
│   ├── List.jsx           # Списък с постове от API
│   └── Detail.jsx         # Детайлен изглед на пост
├── components/
│   └── ConfirmDialog.jsx  # Reusable диалог за потвърждение
├── App.jsx                # Главен компонент с routing
└── main.jsx               # Entry point
```

## Използване

1. Отворете приложението и отидете на `/login`
2. Въведете email и password (валидацията изисква валиден email и парола с минимум 6 символа)
3. След успешен вход ще бъдете пренасочени към `/list` със списък с постове
4. Кликнете на някой пост, за да видите детайлите му
5. Използвайте бутона "Изход" за logout (с диалог за потвърждение)
6. Използвайте бутона "Изтрий" в детайлния изглед (с диалог за потвърждение)

## API

Проектът използва JSONPlaceholder API:
- `GET https://jsonplaceholder.typicode.com/posts` - всички постове
- `GET https://jsonplaceholder.typicode.com/posts/:id` - конкретен пост

## Автентификация

Приложението използва фейк authentication, което запазва статуса в localStorage. При рестарт на браузъра, ако имате запазен статус, ще останете логнати.
