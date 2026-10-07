# System Architecture

## Data Flow

Schedule Trigger
       ↓
TOTP Authentication
       ↓
Angel One API
       ↓
Market Data
       ↓
Technical Indicators
       ↓
Signal Generation
       ↓
Position Management
       ↓
Trade Journal
       ↓
Google Sheets

## Components

### 1. Scheduler

Triggers the workflow periodically.

### 2. Authentication

Generates the required authentication flow.

### 3. Market Data

Fetches historical candle data.

### 4. Technical Analysis

Calculates EMA, ATR, market structure and Fibonacci levels.

### 5. Signal Engine

Determines BUY / SELL / HOLD.

### 6. Position Manager

Handles:

- Entry
- Stop loss
- Target
- Trailing
- Exit

### 7. Trade Journal

Stores completed trades for analysis.
