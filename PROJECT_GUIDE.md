# Путеводитель: ru

Автономная инструкция: достаточно этой папки, исходников и перечисленных защищённых копий. История чатов и центральный каталог не требуются.

[Восстановление](RECOVERY.md) · [Карта файлов и зависимостей](PROJECT_MAP.json)

## Назначение

По [README.md](README.md): Currently, two official plugins are available:

Обнаруженные языки: JavaScript, TypeScript.

## Порядок чтения

1. Локальные AGENTS.md / CLAUDE.md и документы ниже.
2. Манифесты: версии среды, зависимости, команды.
3. Кандидаты точек входа; фактический запуск проверить по манифесту.
4. PROJECT_MAP.json: imports_local от источника к импортируемому файлу; входящие рёбра — потребители модуля.
5. RECOVERY.md: независимые данные, восстановление среды, запуск и критерии приёмки.

- [README.md](README.md)

## Манифесты

- [package.json](package.json)

## Кандидаты точек входа

- [src/app/index.tsx](src/app/index.tsx)
- [src/main.tsx](src/main.tsx)

## Основные файлы по локальным импортам

| Файл | Входящих импортов |
|---|---:|
| [src/app/App.tsx](src/app/App.tsx) | 2 |
| [src/index.css](src/index.css) | 1 |
| [src/app/styles.css](src/app/styles.css) | 1 |
| [src/features/soundPlayer/model/useSoundPlayer.ts](src/features/soundPlayer/model/useSoundPlayer.ts) | 1 |

## Проверки


## Чтение карты без специальных плагинов

PROJECT_MAP.json — UTF-8 JSON: nodes и edges. Пути файлов относительные. contains обозначает наличие файла; imports_local — статически распознанный импорт; declares_dependency — объявление пакета в манифесте. evidence содержит источник и, где доступно, строку. Карта не исполняет код.

Статус исходного анализа: static-scan-complete; ограничений чтения: 0. Исходный снимок: 2026-10-30T14:47:11.360Z.

После изменения кода перечитайте затронутые файлы: карта является снимком. Отсутствие ребра не доказывает отсутствие зависимости.
