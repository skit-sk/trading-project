# Scanner Agent

## Описание
Агент для сканирования свечных паттернов на рынках

## Инструменты
- webfetch: для получения данных
- bash: для запуска скриптов
- write: для записи результатов

## Задачи
1. Сканирование акций на паттерны
2. Сканирование криптовалют
3. Мониторинг индексов
4. Поиск паттернов в реальном времени

## Источники
- Yahoo Finance (yfinance)
- CoinGecko API
- Binance API

## Паттерны (60+)
- CDLHAMMER - Hammer
- CDLENGULFING - Engulfing
- CDLMORNINGSTAR - Morning Star
- CDLEVENINGSTAR - Evening Star
- CDLDOJI - Doji
- и ещё 55+

## Использование
```bash
cd /shared/projects/trading/screener
python scanner.py --tickers AAPL,MSFT,GOOGL
```

## Output
Записывает в `/shared/projects/trading/reports/daily/`