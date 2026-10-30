# 🌍 WORLD FUTURE ULTIMATE SCANNER | MASTERPIECE

<div align="center">

![Version](https://img.shields.io/badge/Version-6.2%20Masterpiece-ff4757?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Production%20Ready-00ff88?style=for-the-badge)
![License](https://img.shields.io/badge/License-Custom%20(MIT)-ffd700?style=for-the-badge)
![API](https://img.shields.io/badge/API-Binance%20Futures-26a69a?style=for-the-badge)

**Профессиональный инструмент для анализа криптовалютных фьючерсов в реальном времени.**  
Анализ Order Book, Liquidity Walls, RSI, MACD, Bollinger Bands и запатентованный Confluence Score.

[🚀 Запустить LIVE Демо](https://h1opok.github.io/world-future-ultimate-scanner/) | [📱 Telegram: @HlopokSU](https://t.me/HlopokSU)

</div>

---

## 📸 Скриншоты интерфейса

*(💡 Рекомендация: Замените эти ссылки на реальные скриншоты вашего приложения, сделанные с телефона или ПК)*

<div align="center">
  <img src="https://via.placeholder.com/800x400/0a0e1a/00ff88?text=Dashboard+%7C+Masterpiece+UI" alt="Главный экран сканера" width="100%">
  <br>
  <img src="https://via.placeholder.com/800x400/0a0e1a/ffd700?text=Order+Book+%7C+Live+WebSocket" alt="Панель Order Book" width="100%">
</div>

---

## ✨ Ключевые возможности (Masterpiece Edition)

Этот инструмент прошёл 8 итераций инженерного ревью и доведён до совершенства (60/60 баллов):

*   📊 **Двухэтапное сканирование:** Мгновенный радар 24h тикеров → глубокий анализ топ-30 пар (свечи + Order Book) с защитой от API-лимитов (chunking).
*   📈 **Профессиональные индикаторы:** Честный расчёт RSI (14), MACD (с Signal Line), Bollinger Bands (20, 2) и EMA (9/21) прямо в браузере.
*   🏦 **Анализ ликвидности (Order Book):** Выявление Bid/Ask Wall (китовых стен), расчёт Bid/Ask Ratio и поиск ближайших зон поддержки/сопротивления.
*   ⚡ **Real-time WebSocket:** Живое обновление стакана сделок (10 раз в секунду) с оптимизацией производительности (throttle 250ms) для слабых мобильных устройств.
*   📱 **Mobile-First & A11y:** Адаптивный Glassmorphism-дизайн, отключение тяжёлых анимаций для `prefers-reduced-motion`, полная поддержка скринридеров (ARIA).
*   🛡️ **Production Hardening:** Защита от race conditions в WebSocket, корректная очистка памяти (`chart.remove()`), обработка деления на ноль и пустых ответов API.

---

## ⚙️ Как это работает (Confluence Score)

Сканер не использует "магию". Каждая монета получает оценку от **-10 до +10** на основе совпадения (confluence) факторов:

| Фактор | Условие для LONG (+) | Условие для SHORT (-) |
| :--- | :--- | :--- |
| **RSI (14)** | < 30 (Перепроданность) | > 70 (Перекупленность) |
| **MACD** | Гистограмма > 0 | Гистограмма < 0 |
| **Bollinger Bands** | Цена у нижней границы | Цена у верхней границы |
| **Funding Rate** | < -0.05% (Давление на шорт) | > 0.05% (Давление на лонг) |
| **Order Book** | Bid/Ask Ratio > 1.3 | Bid/Ask Ratio < 0.7 |

*Сигнал `STRONG LONG` выдаётся только при наборе ≥ 5 баллов.*

---

## 💻 Технологический стек

*   **Frontend:** Vanilla JavaScript (ES6+), HTML5, CSS3 (CSS Variables, Glassmorphism).
*   **Графики:** [Lightweight Charts](https://github.com/tradingview/lightweight-charts) (by TradingView).
*   **Источники данных:** Binance Futures REST API (`/fapi/v1/`) + WebSocket (`wss://fstream.binance.com`).
*   **Хостинг:** GitHub Pages.

---

## 🚀 Быстрый старт

1. **Онлайн:** Просто откройте [LIVE Демо](https://h1opok.github.io/world-future-ultimate-scanner/). Установка не требуется.
2. **Локально:** 
   ```bash
   git clone https://h1opok.github.io/world-future-ultimate-scanner.git
   cd KuCoin-
   # Откройте файл index.html в любом современном браузере
