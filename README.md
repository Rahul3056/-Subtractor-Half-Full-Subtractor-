 Subtractor (Half & Full Subtractor) - Theory, Design & Implementation**

### Concept Overview
Subtractors are essential combinational circuits used for binary subtraction. The two primary types are **Half Subtractor** and **Full Subtractor**.

### Detailed Explanation

#### ✅ Half Subtractor
- **Definition:** A half subtractor subtracts two single-bit binary numbers and produces a **Difference** and **Borrow** output.
- **Boolean Expressions:**
  - `Difference = A ⊕ B`
  - `Borrow = ~A • B`
- **Truth Table:**

| A | B | Difference | Borrow |
|:-:|:-:|:-----------:|:-------:|
| 0 | 0 |      0      |    0    |
| 0 | 1 |      1      |    1    |
| 1 | 0 |      1      |    0    |
| 1 | 1 |      0      |    0    |

**Example Application:** Used in ALUs, arithmetic circuits, and memory address calculation.

#### ✅ Full Subtractor
- **Definition:** A full subtractor subtracts three single-bit binary numbers: two inputs (`A` and `B`) and one borrow-in (`Bin`). It produces a **Difference** and a **Borrow-out**.
- **Boolean Expressions:**
  - `Difference = A ⊕ B ⊕ Bin`
  - `Borrow = (~A • B) + (~A • Bin) + (B • Bin)`
- **Truth Table:**

| A | B | Bin | Difference | Borrow |
|:-:|:-:|:---:|:-----------:|:-------:|
| 0 | 0 |  0  |      0      |    0    |
| 0 | 0 |  1  |      1      |    1    |
| 0 | 1 |  0  |      1      |    1    |
| 0 | 1 |  1  |      0      |    1    |
| 1 | 0 |  0  |      1      |    0    |
| 1 | 0 |  1  |      0      |    1    |
| 1 | 1 |  0  |      0      |    0    |
| 1 | 1 |  1  |      1      |    1    |

**Example Application:** Used in ALUs, digital counters, and control units.



### Code Explanation
- **`assign` Statements:** Implements XOR and AND logic for the half subtractor, and XOR-AND-OR logic for the full subtractor.
- **`$monitor` Task:** Displays real-time changes in inputs and outputs.
- **Test Cases:** Verifies both half subtractor and full subtractor logic for various combinations.

### Execution Steps
1. Copy the Verilog code into your simulator (e.g., ModelSim, Xilinx Vivado, etc.).
2. Compile and run the code.
3. Verify that the outputs match the expected truth table values.

### Real-World Example for Practice
- Design a **4-bit Binary Subtractor** using multiple full subtractor modules to subtract two 4-bit binary numbers.

Would you like to proceed with **Day 8: Decoder (2-to-4 and 3-to-8) - Theory, Design & Implementation** next?

