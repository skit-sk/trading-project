# Trading Project Structure

```
trading/
├── core/                        # Ядро системы
│   ├── agents/                 # Агенты проекта
│   │   ├── scanner.md         # Сканер паттернов
│   │   ├── analyzer.md      # Аналитик рынков
│   │   ├── predictor.md    # Предиктор
│   │   └── reporter.md    # Генератор отчётов
│   ├── skills/               # Скилы
│   │   ├── pattern-scan.md   # Сканирование паттернов
│   │   └── market-analyze.md # Анализ рынков
│   └── data/                # Данные и конфиги
│       ├── tickers.json     # Списки тикеров
│       ├── patterns.json  # Паттерны
│       └── config.json   # Конфигурация
│
├── screener/                  # ПРОДУКТ: Сканер паттернов
│   ├── app.py              # Streamlit UI
│   ├── scanner.py         # Основной сканер
│   └── requirements.txt  # Зависимости
│
├── strategy/                # СЛОЙ: Стратегии
│   ├── README.md          # Описание стратегий
│   ├── momentum/        # Momentum стратегии
│   ├── mean-revert/     # Mean reversion
│   └── breakouts/      # Breakout стратегии
│
├── journal/                  # СЛОЙ: Дневник
│   ├── trades/          # Сделки
│   ├── notes/          # Заметки
│   └── review/         # Еженедельный обзор
│
├── tester/                   # СЛОЙ: Бэктестинг
│   ├── scripts/         # Тесты стратегий
│   ├── results/        # Результаты
│   └── compare/       # Сравнение стратегий
│
├── analytics/               # СЛОЙ: Аналитика
│   ├── project/         # Анализ проекта
│   │   ├── progress.md # Прогресс
│   │   └── roadmap.md # Дорожная карта
│   ├── data/            # Анализ данных
│   │   ├── signals.md  # Сигналы
│   │   └── trends.md # Тренды
│   └── resources/        # Анализ внешних ресурсов
│       ├── reddit.md   # Reddit мониторинг
│       ├── github.md  # GitHub мониторинг
│       └── news.md   # Новости
│
├── reports/                 # Отчёты
│   ├── daily/         # Дневные
│   ├── weekly/       # Недельные
│   └── monthly/     # Месячные
│
└── docs/                   # Документация
    ├── architecture.md # Архитектура
    └── api.md       # API
```

## Слои

| Слой | Назначение | Пример |
|------|-----------|-------|
| **screener** | Продукт | 60+ паттернов, сканирование |
| **strategy** | Торговля | Momentum, Breakout |
| **journal** | Записи | Сделки, заметки |
| **tester** | Тестирование | Бэктест стратегий |
| **analytics** | Анализ | Прогресс, ресурсы |

## Workflow

```
Внешние ресурсы → Analytics → Screener/Strategy
                        ↓
                    Tester (бэктест)
                        ↓
                    Journal (записи)
                        ↓
                    Analytics (анализ результатов)
```

## Развитие

```
Week 1:  Screener - базовый сканер
Week 2:  Screener - UI + данные
Week 3:  Strategy - базовые стратегии
Week 4:  Tester - бэктест
Week 5+:  Analytics + Journal
```