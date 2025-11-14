# AUD-CMA-v1
🔢 Drag and Carry Multiplication Algorithm v1

**AU** in AUD-CMA-v1 stands for Ahmet Ulucay. The **AU Drag and Carry Multiplication Algorithm (AUD-CMA-v1)** introduces a novel method for digit-wise multiplication using structured positional padding, non-traditional base multipliers, and a unique carry rule. Its hybrid approach blends convolutional patterns with simplified mental math, making it distinct from known multiplication methods in both theory and application.

---

## 🔢 Core Idea

Given an input number `n` and a multiplier `b` (like `222`, `111`, or `33`), the algorithm follows these steps:

1. **Multiply** each digit of `n` by the scalar `m`, where `b = m × 111...1` (length = `k`)
2. **Pad** the digit list with `k - 1` zeros on both ends
3. **Slide** a window of size `k` over the padded array and sum each window
4. **Apply Drag-and-Carry**, keeping only single-digit values (except the leftmost value, which can be multi-digit)
5. **Join the result** to get the final answer

---

## 📘 Example

Multiply: `547 × 222`

- `m = 2`, `k = 3`
- Multiply digits: `[5, 4, 7] × 2 → [10, 8, 14]`
- Pad: `[0, 0, 10, 8, 14, 0, 0]`
- Slide window size 3 → Sums: `[10, 18, 32, 22, 14]`
- Apply Drag-and-Carry → `[12, 1, 4, 3, 4]`
- Final Result: `121434`

---

## 📂 Structure



## Use Cases:

- Multiplication by numbers like 11, 111, 222...
- Mental arithmetic techniques
- Educational visualizations for elementary math
- Embedded low-power processors without complex multiplication logic
