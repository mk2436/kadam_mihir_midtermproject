# 🛒 ruleFinder - Association Rules Mining Comparison Tool

A Python-based tool that compares **Brute Force**, **Apriori**, and **FP-Growth** algorithms for frequent itemset mining and association rule generation.

This program allows users to analyze transaction data from various stores (e.g., Amazon, Bestbuy, Shoprite, etc.), visualize frequent itemsets and association rules, and measure the performance (execution time) of each algorithm.

---

## 📘 Features

- **Multiple Algorithm Support**
  - Brute Force (custom implementation)
  - Apriori (`mlxtend.frequent_patterns.apriori`)
  - FP-Growth (`mlxtend.frequent_patterns.fpgrowth`)

- **Association Rule Generation**
  - Uses confidence and support thresholds
  - Outputs rules in the form `A → B` with confidence and support

- **Automatic Comparison**
  - Displays execution times for all algorithms
  - Identifies the fastest algorithm for the given dataset

- **Interactive CLI Interface**
  - Select a store
  - Input minimum support and confidence thresholds
  - View tabulated results

---

## 🧠 How It Works

1. **Load Data**
   - Reads transaction and item mapping CSV files for a selected store.
   - Converts transactions into a one-hot encoded DataFrame for `mlxtend` algorithms.

2. **Run Algorithms**
   - Executes:
     - Brute Force (exhaustive search)
     - Apriori (candidate generation & pruning)
     - FP-Growth (tree-based pattern mining)

3. **Generate Rules**
   - Association rules are derived based on the minimum confidence threshold.

4. **Display Results**
   - Frequent itemsets and rules are printed in formatted tables using `tabulate`.
   - Execution times are compared.

---

## ⚙️ Installation

### 1️⃣ Clone the repository
```bash
git clone https://github.com/mk2436/kadam_mihir_midtermproject.git
cd kadam_mihir_midtermproject
```

### 2️⃣ Install dependencies
```bash
pip install -r requirements.txt
```

---

## ▶️ Usage

Run the main program:
```bash
python main.py
```

---

## 📈 Algorithms Overview

| Algorithm | Description | Pros | Cons |
|------------|-------------|------|------|
| **Brute Force** | Checks all item combinations manually. | Easy to understand. | Very slow for large datasets. |
| **Apriori** | Uses candidate generation and pruning. | Efficient for small/medium datasets. | Still slow for large datasets. |
| **FP-Growth** | Uses a prefix tree (FP-tree) structure. | Very fast and scalable. | More complex to implement. |

---

## 🧩 Dependencies

| Library | Purpose |
|----------|----------|
| `pandas` | Data handling & CSV processing |
| `mlxtend` | Apriori & FP-Growth algorithms |
| `tabulate` | Pretty-printing tables |
| `itertools` | Combination generation |
| `time` | Execution time measurement |

---


## 🪪 License

Licensed under the **MIT License**.