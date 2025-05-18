# 🐺 Order Book Simulator (Python)

## 🧭 Overview
An **order book** is a real-time record of **buy** and **sell orders** for a stock or any financial asset.  
It helps traders observe **market supply & demand**, identify **price discovery**, and simulate **liquidity depth**.

---

## 📈 Why is it Important in Trading?
- 📊 Determines **liquidity** — how easily an asset can be bought or sold.
- 💰 Enables **price discovery** — matching buyers and sellers at fair value.
- ⚡ Foundation for **algorithmic and high-frequency trading (HFT)** systems.

---

## 🎯 Problem Statement

**Goal:** Build a basic CLI-based Order Book Simulator to replicate real-world exchange mechanics.

✅ Accept **buy (bid)** and **sell (ask)** orders  
✅ Maintain sorted order queues (price-time priority)  
✅ Match opposing orders on placement  
✅ Display real-time order book after each transaction

---

## 🔁 Order Book Flow

### 1️⃣ Order Placement
- A trader places a **buy** or **sell** order.
- Orders are sorted by:
  - 🟢 **Buy orders**: Highest price first
  - 🔴 **Sell orders**: Lowest price first
- Example: `Buy 10 shares of TCS @ ₹3500`

### 2️⃣ Order Matching & Execution
- New orders are checked against the opposite side of the book.
- Matching logic:
  - 🟢 A **buy order** matches with the **lowest available sell price**
  - 🔴 A **sell order** matches with the **highest available buy price**
- If matched, trade is executed and quantities are updated.

---

## 🔍 Example Input & Output

### Sample Input:
```python
place_order("buy", price=100, quantity=10)
place_order("sell", price=98, quantity=5)

Output
✅ Matched: Buy 5 @ ₹98
📘 Remaining Buy: 5 @ ₹100

⚙️ How to Run
git clone https://github.com/MihirZalavadiya/HFT-Learning-Journey.git
cd HFT-Learning-Journey/order-book-simulator
python simulator.py

