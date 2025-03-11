# Regular Expressions to Finite Automata Implementation

## Introduction
Regular expressions and finite automata are fundamental concepts in computer science that are intimately linked to the tasks of pattern matching and string processing. Regular expressions are a robust means of describing text patterns, whereas finite automata are a mathematical model employed to identify patterns in strings. These two concepts are related in that a regular expression can be converted into a finite automaton, which can then be used to effectively match patterns in strings.

This process is called **Regular Expression to Finite Automata implementation**. This implementation involves converting regular expressions into a specific kind of finite automaton called a **Non-deterministic Finite Automaton (NFA)**, which can then be transformed into a **Deterministic Finite Automaton (DFA)**. The DFA can then be utilized for pattern recognition in strings, making it a vital tool in text processing and search applications. This article will explore the conversion of regular expressions into finite automata and discuss the different kinds of automata used in this process.

## Implementation
### 1. Input
The code takes an input **regular expression** as a string, which represents a pattern to be recognized in strings.

### 2. Shunting Yard Algorithm
The **Shunting Yard algorithm** is used to convert the input regular expression from **infix notation** (where operators appear between operands) to **postfix notation** (where operators appear after operands). This algorithm utilizes two stacks:
- **One for operators**
- **One for operands**

The algorithm processes the input regular expression and generates the corresponding postfix expression.

### 3. Thompson's Algorithm
The **postfix expression** obtained from the Shunting Yard algorithm is then used to build a **Non-Deterministic Finite Automaton (NFA)** using **Thompson's algorithm**. This method constructs an NFA from a regular expression by utilizing a stack to perform operations on operands based on encountered operators in the postfix expression.

- **Operands** in the NFA are represented as **states**.
- **Transitions** between states are determined by the **input symbols** (characters) and **epsilon (ε) transitions**.

### 4. NFA Representation
The resulting NFA is represented as a **dictionary** containing:
- **States**: Unique identifiers (e.g., integers).
- **Transition function**: Maps a state and input symbol (or epsilon) to a set of next states.
- **Start states**: The initial states of the NFA.
- **Final states**: The accepting states of the NFA.

### 5. Display
The dictionary representation of the NFA is displayed using the **tabulate library**, which presents the NFA in a tabular format. This visual representation helps in understanding the states, transition functions, start states, and final states of the NFA.

### 6. Transition Table Representation
The dictionary representation of the NFA is further converted into a **transition table representation**, which is a nested dictionary that maps each **state and input symbol (or epsilon)** to the **next set of states** reachable from the current state via that symbol. This representation allows for efficient and easy access to the transitions between states in the NFA.

### 7. Visualization
The **automaton library** is used to visualize the resulting NFA as a **graph**. This provides a **visual representation** of the NFA, aiding in better comprehension of its structure and behavior.

