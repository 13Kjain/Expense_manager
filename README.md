## Expense Manager App

A simple and modern Android app to **track income and expenses** with real-time balance calculation.  
Built using **Kotlin, Jetpack Compose, MVVM, and Room Database**.

---

## Features
- Add, edit, and delete income or expense transactions  
- Categorize expenses (e.g., Spotify, Starbucks, Paypal, Upwork)  
- View **total income, total expense, and remaining balance**  
- Auto-updating UI using **LiveData**  
- Smooth database operations with **Kotlin Coroutines**  
- Persistent local storage with **Room Database**  

---

## Tech Stack
- **Language:** Kotlin  
- **UI:** Jetpack Compose  
- **Architecture:** MVVM  
- **Database:** Room (SQLite)  
- **Asynchronous Tasks:** Kotlin Coroutines + LiveData  

---

## App Architecture
The project follows **MVVM (Model-View-ViewModel)**:
- **Model:** Room Database (Entity, DAO, Database)  
- **ViewModel:** Handles business logic (HomeViewModel, AddExpenseViewModel)  
- **View:** Jetpack Compose UI observing LiveData  

Data Flow:
1. User adds an expense/income → `AddExpenseViewModel` → DAO → Room DB  
2. Room notifies LiveData → `HomeViewModel` exposes it  
3. UI updates automatically via Compose  

---
