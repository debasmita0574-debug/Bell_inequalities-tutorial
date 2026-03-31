# Bell States and Bell Inequalities: Mathematical Foundations

## 1. Bell States and Quantum Entanglement

Bell states form an orthonormal basis for the two-qubit Hilbert space:

H = ℂ² ⊗ ℂ²

They are defined as:

|Φ⁺⟩ = (1/√2)(|00⟩ + |11⟩)  
|Φ⁻⟩ = (1/√2)(|00⟩ − |11⟩)  

|Ψ⁺⟩ = (1/√2)(|01⟩ + |10⟩)  
|Ψ⁻⟩ = (1/√2)(|01⟩ − |10⟩)

[Now the question can arise that what is orthonormal basis?
The term orthonormal has come down from two different term.
1. Orthogonal: Which means "independent"
   Two vectors are Orthogonal if:
     They dont overlap at all, which means Completely distinguishable.
2. Normalized: which means Unit length
   so they together define that states are perfectly distingushable, measurements outcome are clean and not dependable to anything]

---
### Non-separability

A quantum state is separable if it can be written as:
|ψ⟩ = |ψ_A⟩ ⊗ |ψ_B⟩
Consider |Φ⁺⟩ and assume:
|Φ⁺⟩ = (a|0⟩ + b|1⟩) ⊗ (c|0⟩ + d|1⟩)
Expanding:
= ac|00⟩ + ad|01⟩ + bc|10⟩ + bd|11⟩
Matching coefficients with:
(1/√2)(|00⟩ + |11⟩)

We get:
ac = 1/√2  
bd = 1/√2  
ad = 0  
bc = 0  

These conditions cannot be satisfied simultaneously.
Therefore:
|Φ⁺⟩ ≠ |ψ_A⟩ ⊗ |ψ_B⟩  

Hence, Bell states are entangled.

---

### Density Matrix Representation

The density matrix is:

ρ = |Φ⁺⟩⟨Φ⁺|

= (1/2)(|00⟩ + |11⟩)(⟨00| + ⟨11|)

Taking partial trace over Bob:

ρ_A = Tr_B(ρ) = I/2

This means:

- Each subsystem is maximally mixed  
- The global system is pure  

---

### Key Insight

Bell states exhibit:

- Local randomness  
- Global correlation  

This is the signature of maximal entanglement.

---

## 2. Bell Inequalities and Classical Correlation Limits

Assume a local hidden variable λ with probability distribution ρ(λ):

ρ(λ) ≥ 0  
∫ ρ(λ) dλ = 1  

Measurement outcomes:

A_i(λ), B_j(λ) ∈ {−1, +1}

Correlation:

E(A_i, B_j) = ∫ ρ(λ) A_i(λ) B_j(λ) dλ

---

### CHSH Expression

S = E(A₀,B₀) + E(A₀,B₁) + E(A₁,B₀) − E(A₁,B₁)

---

### Classical Bound Derivation

Define:

S(λ) = A₀(B₀ + B₁) + A₁(B₀ − B₁)

Since B₀, B₁ ∈ {−1, +1}:

- (B₀ + B₁) ∈ {0, ±2}  
- (B₀ − B₁) ∈ {0, ±2}  

Only one term is non-zero.

Therefore:

|S(λ)| ≤ 2  

Averaging over λ:

|S| ≤ ∫ ρ(λ) |S(λ)| dλ ≤ 2  

---

### Classical Limit

|S| ≤ 2  

---

## 3. Quantum Violation of Bell Inequality

Consider operators:

A₀ = Z  
A₁ = X  

B₀ = (Z + X)/√2  
B₁ = (Z − X)/√2  

For Bell state |Φ⁺⟩:

E(A_i, B_j) = ⟨Φ⁺| A_i ⊗ B_j |Φ⁺⟩

Results:

E(A₀,B₀) = 1/√2  
E(A₀,B₁) = 1/√2  
E(A₁,B₀) = 1/√2  
E(A₁,B₁) = −1/√2  

---

### Compute S

S = 1/√2 + 1/√2 + 1/√2 − (−1/√2)

S = 4/√2 = 2√2  

---

### Quantum Limit (Tsirelson Bound)

|S| ≤ 2√2  

---

## 4. Implications for Correlation Modeling

Classical assumption:

P(a,b | λ) = P(a | λ) P(b | λ)

Quantum reality:

P(a,b) ≠ P(a)P(b)

---

### Connection to Computational Models

In classical decoding (e.g., MWPM):

P(E) = ∏ p_e  

This assumes independence.

However, in correlated systems:

- Independence breaks  
- Factorization fails  

---

### Key Insight

Bell inequality violation shows:

→ Correlations cannot be decomposed into independent components  

This motivates:

- correlation-aware models  
- adaptive learning approaches (e.g., RL-based decoders)

---

## 5. Summary

- Bell states are maximally entangled quantum states  
- Bell inequalities define classical limits on correlations  
- Quantum mechanics violates these limits  
- This reveals the failure of independence assumptions  
- The same principle applies to correlated computational systems  
