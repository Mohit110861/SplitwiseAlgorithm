# 💸 Splitwise Algorithm in C++ (Using Maps and Multisets)

This C++ project implements a simplified version of the **Splitwise** algorithm to optimize the number of transactions between a group of friends after sharing expenses.

---

## 📌 Problem Statement

Imagine a group of friends who owe each other money after a series of transactions. The naive way would be to pay each person individually. However, this often results in more transactions than necessary.

🧠 **Goal**: Minimize the total number of transactions required to settle debts completely.

---

## 🔧 How It Works

We:
1. Track **net balances** of each person.
2. Use a **greedy algorithm** with a `multiset` to repeatedly match:
   - The person who owes the most (**maximum debit**),
   - The person who is owed the most (**maximum credit**),
3. Perform settlements until all balances reach zero.

---

## 🧠 Concepts Used

- `map<string, int>` → To store net balances of each friend.
- `multiset<pair<int, string>>` → Automatically sorted set for greedy settlement.
- **Greedy algorithm** → Always settle smallest/largest balances first.
- **C++ STL** → Clean and efficient code with Standard Template Library.

---

## 🧪 Sample Input & Output

### ✅ Input:
3 3
A B 100
B C 50
C A 30

**Explanation**:
- A pays 100 to B
- B pays 50 to C
- C pays 30 to A

Final balances:
- A: -70
- B: +50
- C: +20

### ✅ Output:
A will pay 50 to B
A will pay 20 to C

Without Algorithm it took: 3 transacions
With Algorithm it took: 2 transacions

✅ **Result**: Instead of 3 transactions, we reduced to just 2 — smart settlements.

---

## 💻 How to Run the Code

### 🧱 Requirements:
- C++ Compiler (g++, clang++)
- Terminal or VS Code setup

### ▶️ Compile & Run:
```bash
g++ main.cpp -o splitwise
./splitwise
