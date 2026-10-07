# 📈 Algo Trading Automation System

> An automated algorithmic trading and backtesting workflow built with
> **n8n, Python/JavaScript, Angel One SmartAPI, technical indicators,
> and Google Sheets.**

## 🚀 Overview

This project automates the complete trading-analysis pipeline:

Market Data
   ↓
Angel One SmartAPI
   ↓
Candle Processing
   ↓
EMA 9 / EMA 15
   ↓
ATR(14)
   ↓
Market Structure
   ↓
Fibonacci Levels
   ↓
Trading Signal
   ↓
Position Management
   ↓
Trade Results
   ↓
Google Sheets

## ✨ Features

- 📊 1-minute SENSEX market data
- 📈 EMA 9 / EMA 15 crossover strategy
- 📐 ATR(14) volatility calculation
- 🔎 Higher High / Higher Low detection
- 📉 Lower High / Lower Low detection
- Fibonacci retracement levels
- Breakout confirmation
- Sideways-market filter
- Stop-loss and target management
- EMA-based trailing logic
- Maximum trades-per-day protection
- Backtesting mode
- Paper-trading mode
- Automated Google Sheets trade logging
- TOTP-based broker authentication
- Scheduled workflow execution

## 🧠 Trading Strategy

### Entry Conditions

A BUY signal requires:

- EMA 9 crosses above EMA 15
- Previous EMA trend is bullish
- Price breaks the previous range high
- Market is not sideways
- Price remains above EMA 9

A SELL signal requires the opposite conditions.

### Risk Management

| Parameter | Value |
|---|---:|
| Stop Loss | 30 points |
| Target | 60 points |
| Risk/Reward | 1:2 |
| Trailing Activation | +30 points |
| Max Trades/Day | 2 |
| Timeframe | 1 minute |
| Instrument | SENSEX |

## 🏗️ Architecture

The workflow consists of:

1. Schedule Trigger
2. TOTP Generator
3. Angel One Authentication
4. Historical Market Data
5. EMA Crossover
6. ATR Calculation
7. Market Structure Detection
8. Fibonacci Calculation
9. Strategy Signal
10. Position State Management
11. Google Sheets Logging

## 🔐 Security

No API keys, passwords, private keys, IP addresses,
MAC addresses, or broker credentials are included in this repository.

Configure secrets through environment variables / n8n credentials.

Example:

```env
ANGELONE_TOTP_SECRET=your_totp_secret
ANGELONE_CLIENT_CODE=your_client_code
ANGELONE_PASSWORD=your_password
