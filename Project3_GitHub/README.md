# DJIA Dictionary Analyzer — Project 3
# 📈 DJIA Dictionary Analyzer — Project 3

**Author:** Brynn Kirkham
**Course:** CS 212 — C Programming
**Purpose:** Analyze dictionary (key–value) data structures using real Dow Jones Industrial Average (DJIA) data.

---

## 📘 Overview

This project implements and benchmarks multiple dictionary data structures in C — including **arrays**, **linked lists**, and **hash tables** — to store and retrieve historical Dow Jones Industrial Average (DJIA) closing values.

It demonstrates how the choice of data structure impacts runtime performance, lookup efficiency, and overall algorithmic complexity.

---

## 📂 Project Structure

```
Project3_GitHub/
│── README.md
│── .gitignore
│── data/
│     └── DJIA.txt
│── src/
│     ├── proj3A.c      # Array-based dictionary
│     ├── proj3B.c      # Linked-list dictionary
│     ├── proj3C.c      # Hash-table dictionary
│     └── proj3D.c      # Performance comparison driver
```

---

## 📊 Dataset: Dow Jones Industrial Average (DJIA)

The dataset contains daily closing values formatted as:

```
YYYY-MM-DD   VALUE
```

Example:

```
1929-10-24   305.85
1929-10-28   260.64
1929-10-29   230.07
```

Each program loads this dataset, stores the values in a specific data structure, and performs user-specified lookups.

---

## 🧠 Program Summaries

### **proj3A — Array Dictionary**

* Uses parallel arrays (dates and values)
* Linear search lookups
* Baseline implementation

### **proj3B — Linked List Dictionary**

* Stores records in a singly linked list
* Lookup is O(n)
* Highlights pointer manipulation & dynamic memory

### **proj3C — Hash Table Dictionary**

* Hash table with chaining using linked lists
* Near-instant lookups
* Demonstrates hashing, collisions, and indexing efficiency

### **proj3D — Performance Comparison**

* Loads the dataset into all three dictionary types
* Performs lookups using each structure
* Measures search time via `clock()`

Example output:

```
Lookup test date: 1955-06-03
Array Lookup:        450.62   (0.00238400 sec)
Linked List Lookup:  450.62   (0.00391200 sec)
Hash Table Lookup:   450.62   (0.00000100 sec)
```

---

## 🛠️ Compilation

Compile each program using:

```bash
gcc -o proj3A src/proj3A.c
gcc -o proj3B src/proj3B.c
gcc -o proj3C src/proj3C.c
gcc -o proj3D src/proj3D.c
```

---

## ▶️ Running the Programs

Use the DJIA dataset during execution:

```bash
./proj3A data/DJIA.txt
./proj3B data/DJIA.txt
./proj3C data/DJIA.txt
./proj3D data/DJIA.txt
```

---

## 🚀 Key Takeaways

This project demonstrates practical understanding of:

* Dynamic memory and pointer manipulation
* File parsing and data handling
* Hashing and collision resolution
* Performance benchmarking
* Selecting optimal data structures for real datasets

**Conclusion:**
Hash tables outperform arrays and linked lists by several orders of magnitude when performing frequent lookups.

---

## 📄 License

This repository is provided for educational and demonstration purposes.
