Poly proof 3 - Aditya Sharma

This Circom circuit defines three basic logic gate templates: OR, AND, and NOT gates. These templates are then used to create a custom circuit named "Vistara" which implements a specific logic pattern.

1. **OR Template (`OR()`):**
   - This template implements a logical OR gate.
   - It has two input signals (`a` and `b`) and one output signal (`out`).
   - The output signal is computed as `a + b - a*b`, which effectively performs a logical OR operation.

2. **AND Template (`AND()`):**
   - This template implements a logical AND gate.
   - It has two input signals (`a` and `b`) and one output signal (`out`).
   - The output signal is computed as `a * b`, which performs a logical AND operation.

3. **NOT Template (`NOT()`):**
   - This template implements a logical NOT gate.
   - It has one input signal (`in`) and one output signal (`out`).
   - The output signal is computed as `1 + in - 2 * in`, which effectively performs a logical NOT operation.

4. **Vistara Template (`Vistara()`):**
   - This template creates a custom circuit that uses the previously defined OR, AND, and NOT gates.
   - It has two input signals (`a` and `b`) and one output signal (`q`).
   - Inside the circuit logic, an AND gate is connected to inputs `a` and `b`, with the output assigned to the signal `x`.
   - A NOT gate is connected to input `b`, and its output is assigned to the signal `y`.
   - An OR gate is connected to inputs `x` and `y`, and its output is assigned to the signal `q`.

5. **Main Component (`main`):**
   - This component instantiates the custom circuit `Vistara`.
   - It serves as the entry point for the entire circuit.

In summary, the "Vistara" circuit implements a specific logic function using AND, NOT, and OR gates. It takes two input signals `a` and `b`, processes them using these gates, and produces the final output signal `q` based on the specified logic. The circuit has been defined using Circom, a language used for specifying and creating zero-knowledge proofs and circuits for various cryptographic applications.