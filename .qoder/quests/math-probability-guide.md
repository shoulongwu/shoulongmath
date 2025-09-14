# 数学一概率论与数理统计复习指南

## Overview

This comprehensive study guide covers probability theory and mathematical statistics for Mathematics I graduate entrance examination preparation. The guide includes key concepts, difficulty points, detailed examples, and practice problems with solutions.

**Difficulty Rating**: ⭐⭐⭐⭐ (High)
**Recommended Study Time**: 4-6 weeks
**Exam Weight**: 22% of total Mathematics I score

## Technology Stack & Study Resources

### Core Textbooks
- 概率论与数理统计 (浙江大学 盛骤等)
- 概率论与数理统计教程 (茆诗松)
- 历年考研真题集

### Study Tools
- Mathematical calculation software (MATLAB/Python)
- Statistical tables and formulas
- Practice problem databases

## Knowledge Architecture

### Chapter 1: Random Events and Probability

#### 1.1 Core Concepts
- Sample space and events
- Probability axioms and properties
- Conditional probability
- Independence of events

#### 1.2 Key Formulas
```
P(A∪B) = P(A) + P(B) - P(A∩B)
P(A|B) = P(A∩B)/P(B), P(B) > 0
P(A∩B) = P(A)P(B) (if A and B are independent)
```

#### 1.3 Difficulty Points Analysis

**Difficulty Point 1: Conditional Probability and Bayes' Formula**
- **Theoretical Foundation**: Understanding the concept of conditional probability and its relationship with joint probability
- **Common Pitfalls**: Confusing P(A|B) with P(B|A)
- **Memory Technique**: "Given B has occurred, what's the probability of A?"

**Example 1**: A factory has two machines A and B. Machine A produces 60% of products, Machine B produces 40%. The defect rates are 2% for A and 3% for B. If a randomly selected product is defective, what's the probability it came from machine A?

**Solution**:
Let D = defective product, A = from machine A, B = from machine B
- P(A) = 0.6, P(B) = 0.4
- P(D|A) = 0.02, P(D|B) = 0.03
- P(D) = P(D|A)P(A) + P(D|B)P(B) = 0.02×0.6 + 0.03×0.4 = 0.024
- P(A|D) = P(D|A)P(A)/P(D) = (0.02×0.6)/0.024 = 0.5

### Chapter 2: Random Variables and Distribution Functions

#### 2.1 Core Concepts
- Discrete and continuous random variables
- Distribution function properties
- Probability mass function (PMF)
- Probability density function (PDF)

#### 2.2 Common Distributions

**Discrete Distributions**:
- Binomial: B(n,p)
- Poisson: P(λ)
- Geometric: Ge(p)

**Continuous Distributions**:
- Uniform: U(a,b)
- Normal: N(μ,σ²)
- Exponential: E(λ)

#### 2.3 Difficulty Points Analysis

**Difficulty Point 2: Distribution Function Properties**
- **Theoretical Foundation**: F(x) is non-decreasing, right-continuous, with limits 0 and 1
- **Common Pitfalls**: Forgetting continuity requirements and boundary conditions
- **Memory Technique**: "Distribution function climbs from 0 to 1"

**Example 2**: Given probability density function f(x) = {cx², 0≤x≤2; 0, elsewhere}, find c and F(x).

**Solution**:
- Finding c: ∫₀² cx² dx = c[x³/3]₀² = 8c/3 = 1, so c = 3/8
- F(x) = {0, x<0; x³/8, 0≤x≤2; 1, x>2}

### Chapter 3: Multidimensional Random Variables

#### 3.1 Core Concepts
- Joint distribution function
- Marginal distributions
- Conditional distributions
- Independence of random variables

#### 3.2 Key Properties
```
F(x,y) = P(X≤x, Y≤y)
fₓ(x) = ∫ f(x,y) dy (marginal density)
f(x|y) = f(x,y)/fᵧ(y) (conditional density)
```

#### 3.3 Difficulty Points Analysis

**Difficulty Point 3: Joint Distribution Transformations**
- **Theoretical Foundation**: Jacobian transformation for continuous variables
- **Common Pitfalls**: Incorrect calculation of Jacobian determinant
- **Memory Technique**: "Transform variables, transform the measure"

**Example 3**: Let (X,Y) follow uniform distribution on triangle {(x,y): 0≤x≤1, 0≤y≤1-x}. Find the distribution of Z = X+Y.

**Solution**:
- Joint density: f(x,y) = 2 for (x,y) in triangle, 0 elsewhere
- For 0≤z≤1: Fz(z) = ∫∫ 2 dx dy = z²
- For 1<z≤2: Fz(z) = 1 - (2-z)²
- Therefore: fz(z) = {2z, 0≤z≤1; 2(2-z), 1<z≤2; 0, elsewhere}

### Chapter 4: Numerical Characteristics

#### 4.1 Core Concepts
- Mathematical expectation
- Variance and standard deviation
- Covariance and correlation coefficient
- Moment generating functions

#### 4.2 Key Formulas
```
E[X] = ∫ x f(x) dx (continuous)
Var(X) = E[X²] - (E[X])²
Cov(X,Y) = E[XY] - E[X]E[Y]
ρ(X,Y) = Cov(X,Y)/√(Var(X)Var(Y))
```

#### 4.3 Difficulty Points Analysis

**Difficulty Point 4: Expectation of Functions of Random Variables**
- **Theoretical Foundation**: E[g(X)] = ∫ g(x) f(x) dx
- **Common Pitfalls**: Incorrectly applying linearity of expectation
- **Memory Technique**: "Function of expectation ≠ expectation of function (in general)"

**Example 4**: X ~ N(0,1), find E[X²] and E[e^X].

**Solution**:
- E[X²] = Var(X) + (E[X])² = 1 + 0² = 1
- E[e^X] = ∫₋∞^∞ eˣ · (1/√(2π)) e^(-x²/2) dx = e^(1/2) (using MGF)

### Chapter 5: Limit Theorems

#### 5.1 Core Concepts
- Law of Large Numbers (LLN)
- Central Limit Theorem (CLT)
- Convergence in probability
- Convergence in distribution

#### 5.2 Key Theorems

**Central Limit Theorem**:
If X₁, X₂, ..., Xₙ are i.i.d. with E[Xᵢ] = μ, Var(Xᵢ) = σ², then:
```
(∑Xᵢ - nμ)/(σ√n) →ᵈ N(0,1) as n→∞
```

#### 5.3 Difficulty Points Analysis

**Difficulty Point 5: Central Limit Theorem Applications**
- **Theoretical Foundation**: Normal approximation for sums of random variables
- **Common Pitfalls**: Forgetting continuity correction for discrete variables
- **Memory Technique**: "Large n makes everything normal"

**Example 5**: A factory produces items with 2% defect rate. In a batch of 1000 items, find the probability that defects are between 15 and 25.

**Solution**:
- X ~ B(1000, 0.02), approximately X ~ N(20, 19.6)
- P(15 ≤ X ≤ 25) ≈ P(14.5 ≤ X ≤ 25.5) (continuity correction)
- Standardizing: Z = (X-20)/√19.6
- P(-1.24 ≤ Z ≤ 1.24) ≈ 0.785

### Chapter 6: Mathematical Statistics

#### 6.1 Core Concepts
- Sample and sampling distribution
- Point estimation methods
- Interval estimation
- Hypothesis testing

#### 6.2 Common Sampling Distributions
- Chi-square: χ²(n)
- t-distribution: t(n)
- F-distribution: F(m,n)

#### 6.3 Difficulty Points Analysis

**Difficulty Point 6: Hypothesis Testing Procedures**
- **Theoretical Foundation**: Type I and Type II errors, power function
- **Common Pitfalls**: Confusing null and alternative hypotheses
- **Memory Technique**: "Innocent until proven guilty (null hypothesis)"

## Practice Problems Collection

### Problem Set A: Basic Probability (★★☆☆)
1. Classical probability problems
2. Conditional probability applications
3. Independence verification

### Problem Set B: Distribution Theory (★★★☆)
1. Distribution function construction
2. Transformation of variables
3. Joint distribution analysis

### Problem Set C: Statistical Inference (★★★★)
1. Parameter estimation
2. Confidence intervals
3. Hypothesis testing

## Common Exam Patterns

### Pattern 1: Probability Calculation (15-20 points)
- Basic probability rules
- Conditional probability
- Bayes' formula applications

### Pattern 2: Distribution Analysis (20-25 points)
- Random variable transformations
- Joint distributions
- Marginal and conditional distributions

### Pattern 3: Statistical Methods (10-15 points)
- Parameter estimation
- Hypothesis testing
- Confidence intervals

## Memory Techniques and Mnemonics

### Probability Rules Mnemonic
- **Addition Rule**: "Union adds, intersection subtracts"
- **Multiplication Rule**: "Intersection multiplies conditions"
- **Bayes' Formula**: "Reverse the condition, weight by prior"

### Distribution Characteristics
- **Normal**: "Bell-shaped, symmetric, infinite tails"
- **Exponential**: "Memoryless, decreasing density"
- **Uniform**: "Flat top, sharp edges"

## Test-Taking Strategies

### Time Management
- **Chapter 1-2**: 15-20 minutes
- **Chapter 3-4**: 25-30 minutes  
- **Chapter 5-6**: 15-20 minutes
- **Review**: 5-10 minutes

### Error Prevention Checklist
- [ ] Check probability sums to 1
- [ ] Verify distribution function properties
- [ ] Confirm independence assumptions
- [ ] Double-check arithmetic calculations
- [ ] Validate final answer reasonableness

## Historical Exam Analysis (2019-2024)

### High-Frequency Topics (80%+ appearance)
1. Normal distribution properties and applications
2. Central Limit Theorem applications
3. Joint distribution of continuous variables
4. Parameter estimation methods

### Medium-Frequency Topics (50-80% appearance)
1. Discrete distribution calculations
2. Conditional probability and independence
3. Moment generating functions
4. Hypothesis testing procedures

### Low-Frequency Topics (<50% appearance)
1. Order statistics
2. Sufficient statistics
3. Non-parametric methods
4. Advanced limit theorems