# Trading Strategy

## Strategy Name

**EMA Crossover + ATR + Market Structure + Fibonacci Confirmation**

## Overview

The system uses multiple technical-analysis confirmations
before generating a trading signal.

The strategy combines:

- EMA 9 / EMA 15 crossover
- ATR volatility analysis
- Higher High / Higher Low detection
- Lower High / Lower Low detection
- Fibonacci retracement levels
- Entry and position-state management

## Strategy Pipeline

Market Data
→ EMA Crossover
→ ATR
→ Market Structure
→ Fibonacci Levels
→ Strategy Signal
→ Position Management

## 1. EMA Crossover

The strategy uses:

- Fast EMA: 9
- Slow EMA: 15

The crossover provides the primary trend/signal direction.

## 2. ATR

ATR is used to evaluate market volatility and
support the trade-management logic.

## 3. Market Structure

The workflow detects:

- Higher High (HH)
- Higher Low (HL)
- Lower High (LH)
- Lower Low (LL)

This provides additional trend confirmation.

## 4. Fibonacci

Fibonacci levels are calculated from detected swing
structure and used as additional price-level context.

## 5. Signal Generation

The `Strategy Signal` node combines the available
technical confirmations to determine the trading signal.

## 6. Position Management

The `Entry + Position State` node manages the state
of an active trade and its subsequent exit conditions.

## 7. Trade Logging

The resulting trade data is sent to Google Sheets
for tracking and analysis.
