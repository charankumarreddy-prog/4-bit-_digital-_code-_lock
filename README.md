# 🔐 Design and Simulation of a 4-Bit Digital Code Lock System Using Combinational and Sequential Logic

## 📌 Project Overview

This project focuses on the **design and simulation of a 4-bit digital code lock system** using fundamental concepts of **digital electronics**, specifically **combinational logic and sequential logic**.

The system allows a user to enter a 4-bit password. The entered code is compared with a predefined password, and access is granted only when the entered code matches the correct code.

The project demonstrates how combinational and sequential circuits can be integrated to build a simple and secure digital access-control system.

---

## 🎯 Objectives

* Design a functional **4-bit digital code lock system**.
* Use **combinational logic** for password comparison and decision-making.
* Use **sequential logic** for storing and controlling the entered code.
* Simulate the circuit and verify its functionality.
* Understand the practical application of digital logic in security systems.

---

## ⚙️ System Working

The basic working process of the system is:

```text
User Input
    ↓
4-Bit Code Entry
    ↓
Sequential Logic
    ↓
Code Storage
    ↓
Combinational Logic
    ↓
Password Comparison
    ↓
 ┌───────────────┐
 │               │
Match          Mismatch
 │               │
 ↓               ↓
UNLOCK          LOCK
```

### 🔑 Code Verification

The entered 4-bit code is compared with a predefined password.

For example:

```text
Correct Code:  1010
Entered Code:  1010
                 ↓
              MATCH
                 ↓
              UNLOCK
```

If the entered code does not match:

```text
Correct Code:  1010
Entered Code:  1100
                 ↓
            NO MATCH
                 ↓
               LOCK
```

---

## 🧩 Logic Used

### 1. Combinational Logic

Combinational logic is used for:

* Comparing the entered password with the stored password.
* Generating the **MATCH/UNLOCK** signal.
* Generating the **ERROR/LOCK** signal.

Logic gates such as **AND, OR, NOT, and XOR/XNOR** can be used to implement the comparison logic.

### 2. Sequential Logic

Sequential logic is used for:

* Storing the entered bits.
* Controlling the sequence of code entry.
* Maintaining the system state.
* Synchronizing operations using a clock signal.

Flip-flops/registers can be used as the storage elements.

---

## 🛠️ Components / Requirements

### Hardware Concepts

* Logic Gates
* Flip-Flops / Registers
* Clock Signal
* 4-bit Input
* LEDs for status indication
* Digital Logic Components

### Software

The circuit can be designed and simulated using digital circuit simulation software such as:

* Logisim
* Logisim Evolution
* Multisim
* Proteus
* Any compatible digital logic simulator

---

## 📊 Inputs and Outputs

| Signal   | Description                  |
| -------- | ---------------------------- |
| `A3-A0`  | 4-bit password input         |
| `CLK`    | Clock signal                 |
| `RESET`  | Resets the system            |
| `UNLOCK` | Indicates correct password   |
| `LOCK`   | Indicates incorrect password |

---

## 🔄 State Operation

The sequential portion of the system can be represented using different states:

```text
       RESET
         ↓
     IDLE STATE
         ↓
    CODE ENTRY
         ↓
 CODE COMPARISON
      ↙     ↘
   MATCH    MISMATCH
     ↓          ↓
  UNLOCK      LOCK
     ↓          ↓
       RESET / IDLE
```

---

## 🧪 Simulation

The circuit is simulated by providing different 4-bit input combinations.

### Test Cases

| Correct Code | Entered Code | Result    |
| ------------ | ------------ | --------- |
| `1010`       | `1010`       | 🔓 Unlock |
| `1010`       | `1001`       | 🔒 Lock   |
| `1010`       | `1111`       | 🔒 Lock   |
| `1010`       | `0000`       | 🔒 Lock   |

The simulation verifies that the system unlocks only when the entered code matches the predefined password.

---

## 📁 Project Structure

```text
4-bit-digital-code-lock/
│
├── README.md
├── Simulation/
│   └── code_lock_simulation.*
│
├── Circuit/
│   └── code_lock_circuit.*
│
├── Docume
```
