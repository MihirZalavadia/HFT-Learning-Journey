# Order Book Simulator (Python)

## Overview
An **order book** is a real-time record of **buy** and **sell orders** for a stock or any financial asset. It helps traders see market supply and demand.

### Why is it Important in Trading?
- Helps determine **liquidity** (how easily a stock can be bought/sold).
- Used for **price discovery** (finding the fair price).
- Crucial for **algorithmic and high-frequency trading**.

---

## Problem Statement
### Goal: Build an Order Book Simulator that can:
✅ Accept **buy (bid) and sell (ask) orders** from traders.  
✅ Store orders efficiently in a **sorted data structure**.  
✅ Match **buy and sell orders** automatically (order matching).  
✅ Print the updated order book after each transaction.  

---

## Order Book Flow (Step-by-Step Process)
This project is aligned with **NSE (National Stock Exchange) India** trading behavior.

### **1️⃣ Order Placement**
- A trader places a **buy** or **sell** order.
- Example: Buy 10 shares of TCS at ₹3500.
- The order book stores orders in **price-time priority**:
  - **Buy orders**: Highest price first.
  - **Sell orders**: Lowest price first.

### **2️⃣ Order Matching & Execution**
- A buy order is matched with the **lowest** sell
