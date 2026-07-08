# 8-Bit ALU Design using Logisim Evolution

An **8-bit Arithmetic Logic Unit (ALU)** designed and implemented in **Logisim Evolution** using a modular, hierarchical approach. The project demonstrates the implementation of arithmetic, logical, and shift operations along with processor status flags, closely resembling the datapath of a basic processor.

This project serves as the computational core for a future **8-bit processor**, with planned extensions including a Register File, Program Counter, Control Unit, and Instruction Memory.

## Features

- Supports **12 ALU operations**
- 8-bit datapath
- Hierarchical circuit design
- Modular implementation using reusable subcircuits
- Opcode-controlled operation selection using a **16:1 Multiplexer**
- Processor status flags:
  - Carry (C)
  - Zero (Z)
  - Negative (N)
  - Overflow (V)

---

## Supported Operations

| Opcode | Operation | Description |
|:------:|-----------|-------------|
| `0000` | INC | Increment A by 1 |
| `0001` | DEC | Decrement A by 1 |
| `0010` | ADD | A + B |
| `0011` | SUB | A − B |
| `0100` | AND | Bitwise AND |
| `0101` | OR | Bitwise OR |
| `0110` | XOR | Bitwise XOR |
| `0111` | NOT | Bitwise NOT of A |
| `1000` | LSL | Logical Shift Left |
| `1001` | LSR | Logical Shift Right |
| `1010` | ASR | Arithmetic Shift Right |
| `1011` | PASS A | Pass input A directly to the output |

---

## ALU Architecture

The ALU has been implemented using a hierarchical design methodology.

```
                    +-------------------+
                    |   8-bit Inputs    |
                    |      A & B        |
                    +---------+---------+
                              |
            +-----------------+------------------+
            |                 |                  |
            |                 |                  |
     +------+-----+    +------+-----+    +-------+------+
     | Arithmetic |    | Logic Unit |    | Shift Unit   |
     |    Unit    |    |             |    |              |
     +------+-----+    +------+-----+    +-------+------+
            \                 |                  /
             \                |                 /
              +---------------+----------------+
                              |
                     16:1 Multiplexer
                              |
                        ALU Result
                              |
                 +------------+------------+
                 |                         |
            Status Flags              8-bit Output
```

---

## Project Hierarchy

```
MAIN_ALU
│
├── FULL_ADDER
│
├── RIPPLE_ADDER_8bit
│
├── ADDER_SUBTRACTOR
│
├── LOGIC_UNIT
│
├── SHIFT_UNIT
│
└── MAIN_ALU
```

---

## Status Flags

The ALU generates the following processor status flags.

| Flag | Description |
|------|-------------|
| **Carry (C)** | Indicates carry generated during arithmetic operations |
| **Zero (Z)** | Set when the ALU output is equal to zero |
| **Negative (N)** | Indicates that the result is negative (MSB = 1) |
| **Overflow (V)** | Indicates signed arithmetic overflow |

---

## Components Used

- Full Adder
- 8-bit Ripple Carry Adder
- Adder/Subtractor
- Logic Unit
- Shift Unit
- Multiplexers
- XOR, OR, AND and NOT Gates
- Splitters
- Input/Output Pins
- Opcode Decoder Logic

---

## Technologies

- **Logisim Evolution**
- Digital Logic Design
- Combinational Logic
- Hierarchical Circuit Design

---

## Running the Project

1. Install **Logisim Evolution**.
2. Clone the repository.

```bash
git clone https://github.com/<your-username>/<repository-name>.git
```

3. Open the `.circ` file in Logisim Evolution.
4. Enter 8-bit values for inputs **A** and **B**.
5. Select the desired operation using the **4-bit Opcode**.
6. Observe the ALU output and processor flags.

---

## Future Enhancements

This project is currently being extended into a complete **8-bit Processor**.

Planned modules include:

- 8-bit Register File
- Program Counter (PC)
- Instruction Decoder
- Control Unit
- Instruction Memory
- Data Memory
- Custom Instruction Set Architecture (ISA)

---

## Learning Outcomes

Through this project, the following digital design concepts were implemented and explored:

- Hierarchical Digital Circuit Design
- Ripple Carry Adder Implementation
- Arithmetic Circuit Design
- Logic Circuit Design
- Shift Operations
- Multiplexer-based Datapath Design
- Processor Status Flag Generation
- Modular Hardware Design

---

## Repository Structure

```
.
├── MAIN_ALU.circ
├── FULL_ADDER
├── RIPPLE_ADDER_8bit
├── ADDER_SUBTRACTOR
├── LOGIC_UNIT
├── SHIFT_UNIT
├── README.md
└── screenshots/
```

---

## Future Roadmap

- [x] 8-bit ALU
- [x] Arithmetic Operations
- [x] Logic Operations
- [x] Shift Operations
- [x] Status Flags
- [ ] Register File
- [ ] Program Counter
- [ ] Control Unit
- [ ] Instruction Memory
- [ ] Complete 8-bit Processor

---

## Author

**Supriya**

Junior Undergraduate , Electrical Engineering 
Indian Institute of Technology Kanpur

---

## License

This project is developed for educational and learning purposes.
