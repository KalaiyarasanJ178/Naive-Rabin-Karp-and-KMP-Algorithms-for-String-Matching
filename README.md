# Comparative Analysis of Naive, Rabin-Karp, and KMP Algorithms for String Matching

## 📌 Overview

This project implements and compares three classical string matching algorithms:

- Naive String Matching
- Rabin-Karp Algorithm
- Knuth-Morris-Pratt (KMP) Algorithm

The objective is to analyze their performance by comparing the number of character comparisons required to find a pattern within a given text. The project also evaluates the algorithms using randomly generated large datasets to observe their practical efficiency.

---

## 🎯 Objectives

- Implement the Naive String Matching algorithm.
- Implement the Rabin-Karp algorithm using rolling hash.
- Implement the Knuth-Morris-Pratt (KMP) algorithm using the LPS (Longest Prefix Suffix) array.
- Compare the algorithms based on:
  - Pattern matching accuracy
  - Number of character comparisons
  - Time complexity
  - Practical performance on large inputs

---

## 🛠️ Technologies Used

- Python 3.x
- Standard Python Libraries
  - `random`

---

## 📂 Project Structure

```
.
├── string_matching.py
├── README.md
```

---

## ▶️ How to Run

1. Clone the repository

```bash
git clone https://github.com/your-username/string-matching-analysis.git
```

2. Navigate to the project folder

```bash
cd string-matching-analysis
```

3. Run the program

```bash
python string_matching.py
```

---

## 📖 Algorithms Implemented

### 1. Naive String Matching

The Naive algorithm checks every possible position of the pattern in the text by comparing characters one by one.

**Time Complexity**

- Best Case: **O(n)**
- Average Case: **O(n × m)**
- Worst Case: **O(n × m)**

---

### 2. Rabin-Karp Algorithm

The Rabin-Karp algorithm uses a rolling hash technique to quickly compare pattern hashes with text window hashes before performing character-by-character verification.

**Time Complexity**

- Best Case: **O(n + m)**
- Average Case: **O(n + m)**
- Worst Case: **O(n × m)** (due to hash collisions)

---

### 3. Knuth-Morris-Pratt (KMP)

KMP improves efficiency by preprocessing the pattern into an LPS (Longest Prefix Suffix) array, allowing the algorithm to avoid unnecessary comparisons.

**Time Complexity**

- Best Case: **O(n + m)**
- Average Case: **O(n + m)**
- Worst Case: **O(n + m)**

---

## 📊 Performance Analysis

The program compares the three algorithms using:

- Fixed sample strings
- Large randomly generated text
- Multiple pattern lengths

Metrics evaluated:

- Matching positions
- Number of character comparisons
- Relative efficiency

---

## ✅ Sample Output

```
Text: AABAACAADAABAABA
Pattern: AABA

Naive -> Matches at: [0, 9, 12], Comparisons: 30
KMP    -> Matches at: [0, 9, 12], Comparisons: 18
RK     -> Matches at: [0, 9, 12], Comparisons: 12
```

The program also prints a comparison table for multiple pattern lengths using randomly generated text.

---

## 📈 Comparison Summary

| Algorithm | Best Case | Average Case | Worst Case | Extra Space |
|------------|-----------|--------------|-------------|-------------|
| Naive | O(n) | O(n × m) | O(n × m) | O(1) |
| Rabin-Karp | O(n + m) | O(n + m) | O(n × m) | O(1) |
| KMP | O(n + m) | O(n + m) | O(n + m) | O(m) |

Where:

- **n** = Length of text
- **m** = Length of pattern

---

## 📌 Conclusion

The comparison demonstrates that:

- The **Naive algorithm** is simple to implement but performs many redundant comparisons.
- **Rabin-Karp** is efficient for multiple pattern searches due to its rolling hash mechanism but may degrade because of hash collisions.
- **KMP** consistently provides the best overall performance by avoiding unnecessary re-comparisons using the LPS array, making it suitable for large datasets and real-world applications.

---

## 👨‍💻 Author

Developed as part of the **Design and Analysis of Algorithms (CS5303) Laboratory**.
